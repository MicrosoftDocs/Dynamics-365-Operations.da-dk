---
title: Klargøre et Dynamics 365 Commerce-sandkassemiljø
description: Denne artikel forklarer, hvordan du klargør et Microsoft Dynamics 365 Commerce-sandkassemiljø til demonstrations- eller sandkassebrug med indbyggede demodata.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283635"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Klargøre et Dynamics 365 Commerce-sandkassemiljø

[!include [banner](includes/banner.md)]

Denne artikel forklarer, hvordan du klargør et Microsoft Dynamics 365 Commerce-sandkassemiljø til demobrug med indbyggede demodata. Processen til opsætning af et produktionsmiljø er lignende, men mere omfattende, da mange af forudsætningerne for sandkassemiljøet allerede findes i demodataene.

Før du går i gang, anbefales det, at du hurtigt gennemgår denne artikel for at få et indtryk af, hvad processen kræver.

Hvis det skal lykkes at klargøre et Commerce-sandkassemiljø, skal du angive nogle parametre for miljøet og den CSU (Commerce Scale Unit), der skal bruges, når du klargør Commerce senere. Instruktionerne i denne artikel beskriver alle de påkrævede trin for klargøring og de parametre, du skal bruge.

Nå du har klargjort dit Commerce-miljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit evalueringsmiljø klar til brug. Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil bruge. Du kan altid udføre de valgfrie trin senere.

For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-miljø, efter du har klargjort det, se [Konfigurere et Commerce-sandkassemiljø](cpe-post-provisioning.md). For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-miljø, se [Konfiguration af valgfrie funktioner til et Commerce-sandkassemiljø](cpe-optional-features.md).

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være på plads, før du kan klargøre dit Commerce-miljø:

- Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).
- Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og har allerede oprettet et implementeringsprojekt, som kan bruges i LCS.  
- Du har oprettet en Azure Active Directory-sikkerhedsgruppe (Azure AD), der kan bruges som en Commerce-systemadministratorgruppe, og du har gruppens id ved hånden.
- Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens id ved hånden. (Denne sikkerhedsgruppe kan være den samme som Commerce-systemadministratorgruppen).
- Du har udrullet en hovedkontorsforekomst i LCS. Du kan finde flere oplysninger i [Installere et nyt miljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Bemærk, at denne liste ikke er udtømmende. Hvis du oplever nogen problemer, skal du rette henvendelse til din kontakt hos din Microsoft-partner for at få hjælp.

## <a name="provision-your-commerce-environment"></a>Klargøre dit Commerce-miljø

Følgende procedurer forklarer, hvordan du klargør et Commerce-miljø. Når du har fuldført trinnene, vil Commerce-miljøet være klar til konfiguration. Alle de trin, der er beskrevet nedenfor, finder sted på LCS-portalen.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Initialisere Commerce Scale Unit (sky)

Følg disse trin for at påbegynde CSU'en.

1. Vælg dit miljø på listen i LCS.
1. Vælg **Alle detaljer** i visningen **MILJØER** til højre. Visningen med miljødetaljer vises.
1. I afsnittet **Administrer miljø** under **MILJØFUNKTIONER** skal du vælge **Administrer**.
1. Under fanen **Commerce Scale Unit** skal du vælge **Initialiser**. Visningen **Tilføj skalaenhed** vises.
1. I feltet **OMRÅDE** skal du vælge det område, der er det samme som eller tæt på det område, du har udrullet miljøet i.
1. Vælg den nyeste version på rullelisten **Version**.
1. Vælg **Initialiser**.
1. Vælg **Ja** i den advarselsdialogboks, hvor du bliver bedt om at bekræfte initialiseringen af Commerce Scale Unit. CSU er nu sat i kø til klargøring.
1. Før du fortsætter, skal du sikre dig, at statussen for din CSU er **VELLYKKET**. Initialiseringen tager ca. to til fem timer.

Hvis du ikke kan finde linket **Administrer** i miljødetaljevisningen, skal du kontakte din Microsoft-kontaktperson for at få hjælp.

### <a name="initialize-e-commerce"></a>Initialisere e-handel

Følg disse trin for at initialisere Commerce.

1. Under fanen **e-handel** skal du vælge **Konfiguration**.
1. Angiv et navn for **e-Commerce-miljønavn** i feltet. Vær opmærksom på, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.
1. I feltet **Commerce Scale Unit-navn** skal du vælge din CSU på listen. (Listen bør kun have én indstilling.)

    Feltet **e-Commerce-geografi** indstilles automatisk.

1. Vælg **Næste** for at fortsætte.
1. I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.
1. I feltet **ADD-sikkerhedsgruppe for systemadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne. Vælg den korrekte sikkerhedsgruppe på listen.
1.  I feltet **ADD-sikkerhedsgruppe for vurderings- og anmeldelsesadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne. Vælg den korrekte sikkerhedsgruppe på listen.
1. Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.
1. Vælg **Initialiser**. Visningen **Commerce-administration** vises igen, hvor fanen **e-Commerce** er valgt. Din initialisering af e-Commerce er påbegyndt.
1. Før du fortsætter, skal du vente, indtil initialiseringsstatus for Commerce er **INITIALISERING BLEV UDFØRT**.
1. Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:

    * **e-Commerce-websted** – linket til roden af dit e-Commerce-websted.
    * **Commerce-webstedsgenerator** – linket til administrationsværktøjet for webstedet.

## <a name="next-steps"></a>Næste trin

For at fortsætte processen med klargøring og konfigurering af dit Commerce-miljø skal du se [Konfigurere et Commerce-sandkassemiljø](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere et Dynamics 365 Commerce-sandkassemiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-sandkassemiljø](cpe-bopis.md)

[Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-sandkassemiljø](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (sky)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-websted](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
