---
title: Implementere en ny e-handelslejer
description: I dette emne beskrives, hvordan du installerer en ny e-handelslejer ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945507"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Implementere en ny e-handelslejer

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du implementerer et nyt e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>Oversigt
    
Microsoft Dynamics Lifecycle Services (LCS) er et skybaseret arbejdsområde til samarbejde, som partnere og kunder kan bruge til at styre deres projekter og miljøer, få vist de seneste oplysninger om Microsoft Dynamics-produkter og -funktioner og oprette, spore og gennemse supporthændelser. Funktioner til styring e-handel er integreret i LCS.

Du kan få mere at vide om LCS i [Brugervejledning til Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Introduktion

Før du kan initialisere e-handel, skal du initialisere et projekt, et miljø og en Retail Cloud Scale Unit (RCSU). Når du vil udføre initialiseringen i LCS, skal du have rettigheder til enten Projektejer- eller Miljøadministrator-rollen. Topologierne for produktions- og sandkassemiljøet understøttes.

Du kan finde flere oplysninger om miljøer under [Miljøplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Du kan finde flere oplysninger om RCSU under [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Initialisere e-handel

Du kan bruge denne procedure til at initialisere e-handelsfunktionen i et eksisterende miljø.

Før du går i gang, skal du sikre dig, at du har følgende påkrævede oplysninger:

- Den RCSU, der skal bruges.
- Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til administratorer af e-handel-systemet.
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

[!NOTE]
Disse oplysninger kan tilføjes senere via en serviceanmodning.

Når du har indsamlet de nødvendige oplysninger, skal du udføre disse trin for at initialisere e-handel.

1. Log på [LCS](https://lcs.dynamics.com).
1. Åbn det projekt, der indeholder det miljø, hvor du vil initialisere e-handel.
1. Vælg miljøet i sektionen **Miljøer**.
1. Vælg linket **Retail administration** under **Funktioner i miljøet**.
1. Under fanen **e-handel** skal du vælge **Konfiguration**. Der vises en dialogboks, hvor du skal angive de oplysninger, der skal bruges til klargøring.
1. Udfyld de påkrævede oplysninger, og gå derefter til næste side.
1. På næste side skal du udfylde de påkrævede oplysninger og derefter sende formularen. Du vender tilbage til fanen **e-handel**, hvor du kan se, at initialiseringen er startet.
1. Hvis du vil have vist initialiseringsstatus, skal du enten vælge **Opdater** eller vende tilbage til fanen **e-handel** senere.
    
Når e-handel initialiseres fra LCS, klargør systemet flere komponenter, der kræves til e-handel, og knytter dem til miljøet. Når klargøringen er fuldført, opdateres fanen **e-handel** på siden **Detailstyring** og afspejler klargøringen. På siden vises de seneste tilpasningsinstallationer og status for eventuelle andre igangværende installationer. Siden indeholder også links til e-handelswebstedet og værktøjet til administration af e-handelswebsteder (oprettelsesværktøj).

## <a name="access-the-authoring-environment"></a>Adgang til oprettelsesmiljøet

For at få adgang til oprettelsesmiljøet skal du gå til fanen **e-handel** på siden **Detailstyring**. Her finder du links til e-handelswebstedet og webstedets administrationsværktøj.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Administrer robots.txt-filer](manage-robots-txt-files.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)
