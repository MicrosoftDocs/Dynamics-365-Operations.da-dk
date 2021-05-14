---
title: Implementere en ny e-handelslejer
description: I dette emne beskrives, hvordan du implementerer et nyt Dynamics 365 Commerce-e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936700"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Implementere en ny e-handelslejer

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du implementerer et nyt Dynamics 365 Commerce-e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).

Microsoft Dynamics Lifecycle Services (LCS) er et skybaseret arbejdsområde til samarbejde, som partnere og kunder kan bruge til at styre deres projekter og miljøer, få vist de seneste oplysninger om Microsoft Dynamics-produkter og -funktioner og oprette, spore og gennemse supporthændelser. Funktioner til styring e-handel er integreret i LCS.

Du kan få mere at vide om LCS i [Brugervejledning til Lifecycle Services](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Introduktion

Før du kan initialisere e-handel, skal du initialisere et projekt, et miljø og en Retail Cloud Scale Unit (RCSU). Når du vil udføre initialiseringen i LCS, skal du have rettigheder til enten Projektejer- eller Miljøadministrator-rollen. Topologierne for produktions- og sandkassemiljøet understøttes.

Du kan finde flere oplysninger om miljøer under [Miljøplanlægning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Du kan finde flere oplysninger om RCSU under [Initialisere Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Initialisere e-handel

Du kan bruge denne procedure til at initialisere e-handelsfunktionen i et eksisterende miljø.

Før du går i gang, skal du sikre dig, at du har følgende påkrævede oplysninger:

- Den RCSU, der skal bruges.
- Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til administratorer af e-handelssystemet.
- Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til vurderings- og anmeldelsesredaktører.
- De domæner, der skal knyttes til miljøet.

Derudover kan du indsamle følgende valgfrie oplysninger:

- Oplysninger om Azure AD business-to-consumer (B2C):

    - Navn på lejer.
    - Klient-id.
    - Logon på brugerdefineret domæne.
    - Svar-URL-adresse.
    - Politik-id for tilmelding og logon.
    - Politik-id for nulstilling af adgangskode.
    - Rediger profilpolitik-id.

> [!NOTE]
> Disse oplysninger kan tilføjes senere via en serviceanmodning.

Når du har indsamlet de nødvendige oplysninger, skal du udføre disse trin for at initialisere e-handel.

1. Log på [LCS](https://lcs.dynamics.com).
1. Åbn det projekt, der indeholder det miljø, hvor du vil initialisere e-handel.
1. Vælg miljøet i sektionen **Miljøer**.
1. Vælg linket **Retail administration** under **Funktioner i miljøet**.
1. Under fanen **e-handel** skal du vælge **Konfiguration**. Der vises en dialogboks, hvor du skal angive de oplysninger, der skal bruges til klargøring.
1. Udfyld de påkrævede oplysninger, og gå derefter til næste side.
1. På næste side skal du udfylde de påkrævede oplysninger og derefter sende formularen. Du vender tilbage til fanen **e-handel**, hvor du kan se, at initialiseringen er startet.
1. Hvis du vil have vist initialiseringsstatus, skal du enten vælge **Opdater** eller vende tilbage til fanen **e-handel** senere.
    
Når e-handel initialiseres fra LCS, klargør systemet flere komponenter, der kræves til e-handel, og knytter dem til miljøet. Når klargøringen er fuldført, opdateres fanen **e-handel** på siden **Detailstyring**, så den afspejler klargøringen. På siden vises de seneste tilpasningsinstallationer og status for eventuelle andre igangværende installationer. Siden indeholder også links til e-handelswebstedet og generatoren til e-handelswebsteder, hvor websteder oprettes.

## <a name="access-commerce-site-builder"></a>Få adgang til Commerce-webstedsgenerator

Hvis du vil have adgang til Commerce-webstedsgeneratoren, skal du gå til fanen **e-handel** på siden **Detailstyring** i LCS og vælge linket **Administrationsværktøj til websted for e-handel**. Landingssiden for webstedsgeneratoren viser en visning på lejerniveau. Fra denne side kan du:

- Redigere indstillinger på lejerniveau.
- Navigere til et websted, du har oprettet og har tilladelse til at få vist. 
- Få adgang til funktioner til gennemsyn, f.eks. redigering og rapportering.
- Oprette et nyt websted. Du kan finde flere oplysninger om, hvordan du opretter et nyt websted [Oprette et websted for e-handel](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]