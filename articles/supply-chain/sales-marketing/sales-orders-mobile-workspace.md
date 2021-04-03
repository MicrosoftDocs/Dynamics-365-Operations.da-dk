---
title: Arbejdsområde for salgsordrer på mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet for salgsordrer på mobilenheder. Dette arbejdsområde hjælper dig med at holde dig opdateret om salgsordrer hvor som helst og når som helst.
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 41d1ec66774658de6a66a99e752d81a31cd354bf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260990"
---
# <a name="sales-orders-mobile-workspace"></a>Arbejdsområde for salgsordrer på mobilenheder

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Salgsordrer** på mobilenheder. Dette arbejdsområde hjælper dig med at holde dig opdateret om salgsordrer hvor som helst og når som helst. 

Dette mobile arbejdsområde er beregnet til brug sammen med Finance and Operations-mobilappen.

## <a name="overview"></a>Overblik
**Salgsordrer**-arbejdsområdet på mobilenheder viser detaljerede oplysninger om de enkelte salgsordrer. Disse oplysninger omfatter ordrestatus, kontaktoplysninger for debitoren og kontaktoplysninger for ordretageren. Arbejdsområdet **Salgsordrer** til mobilenheder giver en øjeblikkelig visning af salgsordrer. Du kan få vist alle salgsordrer, salgsordrer pr. kunde eller oplysninger om en bestemt salgsordre. 

Arbejdsområdet til mobile enheder indeholder to visninger, der hjælper dig med at analysere salgsordrer i dybden.

### <a name="view-all-sales-orders"></a>Vis alle salgsordrer
Denne visning viser alle salgsordrer.

-   Brug ét af følgende filtre til at vælge de salgsordrer, du vil have vist:

    -   Søg efter salgsordre
    -   Søg efter kundekonto
    -   Søg efter kundenavn
    -   Søg efter status
    -   Søg efter status for frigivelse
    -   Søg efter dato og klokkeslæt for oprettelse
    
-   Når du har valgt salgsordrerne, kan du få vist detaljerede oplysninger om bestemte ordrer. Du kan især se følgende oplysninger:

    -   Oplysninger om kundens navn og adresse
    -   Forskellige datoer for salgsordrerne, f.eks. den ønskede afsendelsesdato og den bekræftede afsendelsesdato
    -   Kontaktoplysninger for ordretageren
    -   Kundekontaktoplysninger
    -   Ordrelinjer
    -   Forsendelser, der viser, hvordan og hvornår en salgsordre blev leveret

### <a name="view-orders-for-a-customer"></a>Vis ordrer for en kunde
Denne visning angiver salgsordrer pr. kunde.

-   Brug et af følgende filtre til at se ordrer for en kunde:

    -   Søg efter navn
    -   Søg efter konto

-   Når du har valgt en kunde, kan du få vist følgende oplysninger:

    -   Kundenavn og -gruppe
    -   Kundekontaktoplysninger
    -   Salgsordrer for kunden og oplysninger om disse salgsordrer:
    
        -   Oplysninger om kundens navn og adresse
        -   Diverse salgsordredatoer
        -   Kontaktoplysninger for ordretageren
        -   Kundekontaktoplysninger
        -   Ordrelinjer
        -   Forsendelser, der viser, hvordan og hvornår en salgsordre blev leveret

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne er forskellige, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forudsætninger, hvis du bruger Supply Chain Management 
Hvis Supply Chain Management er implementeret for organisationen, skal systemadministratoren publicere mobilarbejdsområdet **Salgsordrer**. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere
Hvis Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere er implementeret for organisationen, skal systemadministratoren opfylde følgende forudsætninger. 

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementere KB 4013633.</td>
<td>Systemadministrator</td>

<td>KB 4013633 er en X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Salgsordrer</strong> til mobilenheder. For at implementere KB 4013633 skal systemadministratoren gøre følgende.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Hente metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installere metadatahotfixet</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvend den installerbare pakke</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publicere arbejdsområdet <strong>Salgsordrer</strong> til mobilenheder.</td>
<td>Systemadministrator</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen
Sådan downloades og installeres Finance and Operations-mobilappen:

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen

1.  Start appen på din mobilenhed.
2.  Angiv URL-adressen til din Dynamics 365.
3.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
4.  Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Se oplysninger om salgsordrer for en kunde ved hjælp af arbejdsområdet Salgsordre til mobilenheder

1.  På din mobilenhed skal du vælge arbejdsområdet **Salgsordrer**.
2.  Vælg **Vis ordrer for en kunde**.
3.  Brug oplysningerne om konto eller kundenavn til at finde kunden.
4.  Vælg kunden.
5.  Vælg **Kontaktoplysninger** eller **Salgsordrer**. Hvis du vælger **Salgsordrer**, vises der en liste over salgsordrer for kunden.
6.  Vælg **Salgsordre**. Du kan nu få vist oplysninger om salgsordrelinjer, oplysninger om forsendelser, kundekontaktoplysninger og kontaktoplysninger for ordretageren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]