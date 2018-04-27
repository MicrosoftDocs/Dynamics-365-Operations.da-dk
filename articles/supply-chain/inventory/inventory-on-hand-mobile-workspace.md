---
title: "Disponibelt lager i arbejdsområde til mobilenheder"
description: "Dette emne indeholder oplysninger om arbejdsområdet Disponibelt lager på mobilenheder. I dette arbejdsområde på mobilenheder kan du få indblik i reserveret og tilgængelig lagerplads, når som helst og hvor som helst på mobilenheden."
author: Mirzaab
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 735a25d625774892ff71d4799932f15c258dfbfa
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="inventory-on-hand-mobile-workspace"></a>Disponibelt lager i arbejdsområde til mobilenheder

[!INCLUDE [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Disponibelt lager** på mobilenheder. I dette arbejdsområde kan du få indblik i reserveret og tilgængelig lagerplads, når som helst og hvor som helst på mobilenheden.

Dette arbejdsområdet til mobilenheder er beregnet til brug med Microsoft Dynamics 365 for Unified Operations-mobilappen.

## <a name="overview"></a>Overblik
Virksomheder har typisk flere forsendelser og flere tilgange på lageret hver dag. Disse bevægelser ændrer konstant status for den disponible lagerbeholdning. I arbejdsområdet **Disponibelt lager** på mobilenheder kan du se status for den disponible interne lagerbeholdning, så du kan få den nyeste indsigt i lagerdata på mobilenheder efter eget valg. Uanset om du arbejder på lageret, i indkøb, salg, produktion eller administration eller har andre roller, kan du få adgang til dataene for lagerbeholdningen når som helst og hvor som helst. 

Arbejdsområdet på mobilenheder giver en øjeblikkelig visning af den disponible lagerstatus på tværs af faciliteter. Her kan du få vist den disponible lagerbeholdning på tværs af faciliteter, aktuelle materialereservationer og ikke-reserveret disponibel lagerbeholdning. Du kan også angive varenumre for at forespørge på disponibel lagerbeholdning og udføre en søgning, der er filtreret efter disponible varer eller varianter. 

Arbejdsområdet til mobilenheder indeholder især disse funktioner:

-   Du kan søge efter produktnummer eller produktnavn for at finde produkter, som du vil se den disponible lagerbeholdningsstatus for.
-   Du kan få vist følgende oplysninger for de valgte produkter:

    -   Disponibelt lager pr. sted
    -   Disponibel lagerbeholdning pr. lagersted
    -   Disponibel lagerbeholdning pr. lokalitet
    -   Disponibel lagerbeholdning pr. batch (for batchstyrede produkter)
    -   Disponibel lagerbeholdning pr. lagerstatus
    
-   Disponibel produktlagerbeholdning vises på følgende måder:

    -   Efter fysisk lager (denne visning repræsenterer det samlede antal).
    -   Efter fysisk reserveret (denne visning repræsenterer det reserverede antal).
    -   Efter fysisk beholdning (denne visning repræsenterer tilgængelige antal, der ikke har nogen reservationer).

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne er forskellige, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Finance and Operations 
Hvis Microsoft Dynamics 365 for Finance and Operations er implementeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Disponibelt lager** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere.
Hvis Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere er implementeret for organisationen, kan systemadministratoren skal opfylde følgende forudsætninger. 

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementere KB 4013633.</td>
<td>Systemadministrator</td>

<td>KB 4013633 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Disponibelt lager</strong> til mobilenheder. For at implementere KB 4013633 skal systemadministratoren gøre følgende.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installere metadatahotfixet</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvend den installerbare pakke</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publicer arbejdsområdet <strong>Disponibelt lager</strong> til mobilenheder.</td>
<td>Systemadministrator</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen

Download og installer Dynamics 365 for Unified Operations-mobilappen:

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen

1.  Start appen på din mobilenhed.
2.  Angiv URL-adressen til din Dynamics 365.
3.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
4.  Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

    [![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Få vist oversigten over disponibel lagerbeholdning for et produkt ved hjælp af arbejdsområdet Disponibelt lager på mobilenheder

1.  På din mobilenhed skal du vælge arbejdsområdet **Disponibel lagerbeholdning**.

2.  Vælg **Kontrollér disponibel lagerbeholdning for en vare**. Der vises en liste over de produkter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Vælg **Søg efter flere**, hvis varen ikke er på listen. Søg efter produktnummer, eller skift til en søgning efter produktnavn.

4.  Vælg et produkt. Hvis varen har et billede, vises billedet.
5.  Vælg en af følgende indstillinger for at få vist status for den disponible lagerbeholdning:

    -   Vise disponibel lagerbeholdning pr. websted
    -   Vise disponibel lagerbeholdning pr. lagersted
    -   Vise disponibel lagerbeholdning pr. lokalitet
    -   Vise disponibel beholdning pr. batch (for batchstyrede produkter)
    -   Vise beholdning pr. lagerstatus

    Disponibel produktlagerbeholdning vises på følgende måder:
    -   Efter fysisk lager (denne visning repræsenterer det samlede antal).
    -   Efter fysisk reserveret (denne visning repræsenterer det reserverede antal).
    -   Efter fysisk beholdning (denne visning repræsenterer det tilgængelige antal, der ikke har nogen reservationer).

