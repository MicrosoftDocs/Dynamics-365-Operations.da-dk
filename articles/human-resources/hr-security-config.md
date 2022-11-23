---
title: Sikkerhedskonfigurationsbegreber for virtuelle tabelbaserede integrationer
description: I denne artikel forklares en arkitektur, der bygger på integration mellem Microsoft Dynamics 365 Human Resources og andre systemer.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759649"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Sikkerhedskonfigurationsbegreber for virtuelle tabelbaserede integrationer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives en arkitektur til brug af [Microsoft Dataverse-virtuelle tabeller (enheder)](/dev-itpro/power-platform/virtual-entities-overview) til opbygning af integration mellem Dynamics 365 Human Resources og et tredjepartssystem. Artiklens fokus er på sikkerhedskonfigurationen og på de godkendelses- og godkendelsesaspekter, der kræves mellem systemgrænserne for at opbygge et funktionelt, sikkert system.

## <a name="prerequisite-reference-articles"></a>Referenceartikler, der er en forudsætning

Følgende artikler indeholder flere oplysninger om koncepter i denne artikel:

- [Oversigt over virtuelle objekter](/dev-itpro/power-platform/virtual-entities-overview)
- [Kom i gang med virtuelle tabeller (enheder)](/developer/data-platform/virtual-entities/get-started-ve)
- [Brug godkendelse af server til server med flere lejere (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Brug OAuth-godkendelse med Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0 på klient-legitimationsflow på Microsoft identity-platformen](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Godkendelse og autorisation](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Arkitektur 

Følgende arkitekturdiagram viser de overordnede begreber i forbindelse med integration, hvor der bruges virtuelle tabeller (enheder).

![Virtuel tabelbaseret integration.](./media/Hosts.jpg)

Her er en forklaring på nogle af de elementer i foregående diagram:

- **Microsoft** – Microsoft er vært for og driver de forskellige Dynamics 365-produkter på vegne af kunder.

    - **Azure Active Directory (Azure AD) lejer C** – En Azure AD lejer, der ejes af Microsoft. Det er den lejer, som Dynamics 365-programmerne er registreret i.

- **Integrere partner**

    - **Integrationssystem** – Det system, der integreres med Dynamics 365. Det kan være et lønsystem eller et hvilket som helst system, der er baseret på data, der er lagret i Dynamics 365.
    - **Adapter** – Den software eller tjeneste, der er ansvarlig for at interagere med både Dynamics 365 og integrationssystemet.

        > [!NOTE]
        > Hvis en adapter er beregnet til at blive brugt af flere Dynamics 365-kunder, er det vigtigt, at den registreres som en anvendelse med flere formål i Azure AD.

    - **Azure AD-lejer A** – En Azure AD-lejer, der ejes af integrationspartneren. Det er den lejer, som adapterens ansøgnings-id er registreret i.

- **Gensidig kunde** – En kunde, der implementerer Dynamics 365 Human Resources og integrerer partnerens løsning.

    - **Dynamics 365 Finance eller Personale** – Den kundespecifikke forekomst af Dynamics 365 Finance eller Personale, der indeholder de kundedata, som integrationssystemet kræver.
    - **Dataverse** – Det kundespecifikke Dataverse-miljø, der er tilknyttet enten Finans eller Personale. Dataverse indeholder en web-API til interaktion med Dynamics 365-data.
    - **Azure AD-lejer B** – Kundens Azure AD-lejer. Den fungerer som identitetsudbyder (godkendelsesserver) og udsteder tokens, der giver opkaldere tilladelse til at ringe til kundens Dataverse-forekomst.

## <a name="basic-request-flow"></a>Grundlæggende forespørgselsflow

I dette afsnit beskrives det grundlæggende forløb for en typisk anmodning, der er involveret i en integration. Den refererer til arkitekturdiagrammet tidligere i denne artikel.

En typisk anmodning kræver, at adapterforespørgslen Dynamics 365 for data og derefter gemmer og synkroniserer dataene med integrationssystemet.

1. Adapteren kalder Dataverse Web-API'en for at forespørge på relevante data.

    > [!NOTE]
    > Godkendelse er en forudsætning, og tokenanskaffelse er en væsentlig del af processen. Godkendelse beskrives i afsnittet [godkendelse og autorisation ved systemgrænser](#authentication-and-authorization-at-system-boundaries).

    Dette opkald foretages mod Dataverse Web-API'en for at forespørge på programdata, der vises via en virtuel tabel. (Se "2. Første synkronisering" og "3. Delta-synkronisering" i diagrammet.)

2. Dataverse håndterer anmodningen ved at forespørge på den virtuelle tabel via plugin'et Virtuel enhed ("Virtuel tabelproxy" i diagrammet). Dataverse-anmodningen videresendes til tjenesten Finans eller tjenesten Virtuel enhed for personale for at søge efter de data, der fysisk er gemt i finans- eller personaledatabasen.
3. Tjenesten Virtuelle finans- eller personaleenhed oversætter anmodningen mod den virtuelle enhed til en forespørgsel mod den finans- eller personaleenhed, der backer den virtuelle Dataverse-enhed. Dataene hentes fra databasen, oversættes tilbage til Dataverse-enhedsrepræsentationen og returneres til kalder.
4. Adapteren fuldfører enhver påkrævet tilknytning og dataoversættelse og foretager et opkald til integrationssystemet om at bevare dataene i den integrerende systemdatabase. (Se "4. Gem data" i diagrammet.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Godkendelse og autorisation ved systemgrænser

*Godkendelse* validerer, at en brugers eller applikations identitet er blevet bekræftet, og bekræfter, at brugeren eller applikationen er den, som de siger, at de er. *Godkendelse* giver brugeren eller programmet rettigheder til at få adgang til bestemte rettigheder på programniveau. Yderligere oplysninger finder du under [Godkendelse vs. autorisation](/azure/active-directory/develop/authentication-vs-authorization).

De fleste krydssystemkald i arkitekturdiagrammet tidligere i denne artikel involverer adapteren. Adapteren skal godkende sig selv for at kunne foretage følgende kald:

- Opkaldet til Dataverse
- Opkaldet til integrationssystemet

Se på systemgrænserne i diagrammet. Alle webanmodninger mellem systemer skal godkendes, og kontrol af godkendelse på programniveau skal være bestået, før data returneres til kalderen. For en anmodning mod en virtuel dynamics 365-tabel, der udføres på baggrund af økonomi- eller personalekontrol, gennemtvinges godkendelse og autorisationskontrol ved følgende systemgrænser:

- Opkaldet mellem adapteren og Dataverse Web-API-slutpunktet (OData)
- Opkaldet mellem plugin Dataverse Virtuel enhed og tjenesten Virtuel enhed for Finans eller Personale

I begge tilfælde udføres godkendelseskontrol først. Derefter udføres kontrol af godkendelse på programniveau for at sikre, at den godkendte bruger eller applikation har de korrekte rettigheder på programniveau til at hente de ønskede data.

Godkendelse til opkald til Dataverse håndteres via et ihænderhaver-token, der skal medtages som et HTTP-header i webanmodningen til Dataverse. Adapteren skal hente et token fra forekomsten af lejer B Azure AD. (Se "1. Hent token" i diagrammet). Azure AD fungerer som identitetsprovider i godkendelsesflowet.

Adapteren godkender ved at angive program-id 'en (ikke-arkitektur, som registreret i Azure AD-lejer A) og et program eller certifikat, som kun adapterprogrammet har.

Når brugeren eller programmet er godkendt til at foretage opkald til Dataverse, udføres Dataverse-kontrol af godkendelsesniveauet i forhold til hver anmodning. Disse kontroller sikrer, at den person, der ringer til (adapterprogrammets identitet, som er angivet "\<guid A\>" i diagrammet), har de relevante programrettigheder. Godkendelse på programniveau administreres i Dataverse via en programbruger, der repræsenterer adapterens program-id. Tilladelser på programniveau administreres ved at give adgang til specifikke Dataverse-definerede programroller. Disse roller indeholder detaljerede rettigheder til programmet.

Til yderligere vejledning skal du se [Brug server til server-godkendelse for flere lejere](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Hvis Dataverse-kontrol af programrettigheder på niveau er passeret, foretager plugin'et for den virtuelle enhed et opkald til tjenesten Virtuel enhed i miljøet Finans eller Personale. S2S-godkendelse (Server-til-server) bruges til at foretage dette opkald. Det bruger den identitet og det virtuelle datakildekonfigurationspost, der er konfigureret i den virtuelle datakilde for Finans og drift.

![Konfigurationsposten for den virtuelle datakilde Finans og drift i sandkassemiljøet.](./media/sandbox.jpg)

Du kan finde flere oplysninger i [Konfigurere virtuelle Dataverse-enheder](/dev-itpro/power-platform/admin-reference).

Opkaldet fra virtuelle Dataverse-enheds plugin til Finans eller Personale omfatter adapter-id'et for det oprindelige opkald til Dataverse fra adapteren (den identitet, der er angivet "\<guid A\>" i arkitekturdiagrammet). Hvis datakilden for den virtuelle enhed er konfigureret korrekt, og S2S-godkendelseskontrol er gennemført, kører tjenesten Virtuel enhed i Finans eller Personale forespørgslen i forbindelse med den oprindelige opkalder (adapteren, \<guid A\>). Kontrol af ansøgningsrettigheder (godkendelse) på finans- eller personaleniveau udføres for at sikre, at adapteren har de rettigheder, der er nødvendige for at få adgang til de dataenheder, der anmodes om via forespørgslen.

Sikkerhed i Finans og Personale administreres på følgende måder:

1. Ved at knytte adapter-id'en (\<guid A\>) til en bestemt finans- eller personalebruger. Denne tilknytning udføres på siden **Azure Active Directory-applikationer**. Du kan finde flere oplysninger under [Registrere dit eksterne program](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Ved at tildele finans- eller personalebrugeren de relevante roller, opgaver og rettigheder på programniveau. Du kan finde flere oplysninger under [Rollebaseret sikkerhed](/dev-itpro/sysadmin/role-based-security).

Hvis adapterprogrammet (\<guid A\>) tildeles de rettigheder, der kræves for at få adgang til de ønskede data, forekommer følgende hændelser:

1. Forespørgslen køres.
2. Dataene oversættes tilbage til dens Dataverse-enhedsside.
3. Dataene returneres til adapteren.

> [!IMPORTANT]
> Under udviklingen kan adapteren køres med brug af en finans- eller personalebruger, der har rollen Administrator. I et produktionsmiljø bør adapteren dog aldrig køres med administratorrettigheder.

## <a name="key-takeaways"></a>Nøgleelementer

Her er nogle vigtige konsekvenser af arkitekturen for den virtuelle tabel eller enhed:

- Sikkerhedskonfigurationen for virtuelle tabeller, der arbejder under Personale, administreres i Personale.
- Kunden ("Gensidig kunde" i arkitekturdiagrammet tidligere i denne artikel) har fuld kontrol over, hvilke rettigheder der gives til den integrerende adapteridentitet (angivet "\<guid A\>" i diagrammet).
- Kunden er ansvarlig for den korrekte sikkerhedskonfiguration af personalemiljøet. Den integrationspartner, der opretter adapteren, skal levere vejledning i forbindelse med de rettigheder, som adapteren kræver.
