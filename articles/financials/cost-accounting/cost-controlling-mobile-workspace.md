---
title: "Arbejdsområde til omkostningsstyring på mobilenheder"
description: "Dette emne indeholder oplysninger om arbejdsområdet til omkostningsstyring på mobilenheder. I dette arbejdsområde kan ledere af bærere se oplysninger om bærerydeevnen når som helst og hvor som helst."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 0dc79371d63818fb0f6d55389a146012c269a684
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="cost-controlling-mobile-workspace"></a>Arbejdsområde til omkostningsstyring på mobilenheder

[!include[banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Omkostningsstyring** på mobilenheder. I dette arbejdsområde kan ledere af bærere se oplysninger om bærerydeevnen når som helst og hvor som helst.

Dette arbejdsområdet til mobilenheder er beregnet til brug med Microsoft Dynamics 365 for Unified Operations-mobilappen.

## <a name="overview"></a>Overblik
Arbejdsområdet til **Omkostningsstyring** på mobilenheder giver et øjeblikkeligt overblik over den aktuelle ydeevne af bærere ved at sammenligne faktiske omkostninger med de budgetterede omkostninger. Du kan gå ned på detailniveau og se status for individuelle kostelementer.

En medarbejder modtager f.eks. en invitation til en international konference, men organisationen skal dække alle rejseudgifter. Medarbejderen spørger sin chef, om han må deltage i konferencen. Chefen åbner arbejdsområdet til **Omkostningsstyring** på sin mobiltelefon for at se, om hun har budget til, at medarbejderen kan deltage i konferencen.

### <a name="data-security"></a>Datasikkerhed
Dataene i arbejdsområdet til **Omkostningsstyring** er sikret via brugerlegitimationsoplysninger. Ledere af bærere kan kun se data for deres egen bærer. Sikkerheden på adgangsniveau administreres i modulet **Omkostningsregnskab**.

Bogholdere definerer konfiguration af arbejdsområdet til **Omkostningsstyring** i modulet **Omkostningsregnskab**. Når arbejdsområdet er publiceret på mobilappen, er det tilgængeligt i appen. Derfor kan alle bærerledere i organisationen se data i samme format.

### <a name="actions-views-and-links"></a>Handlinger, visninger og links
Arbejdsområdet **Omkostningsstyring** til mobilenheder indeholder følgende handlinger, visninger og links:

-   **Handlinger:**

    -   Brug **Vælg variant** til at vælge et layout.
    -   Brug **Vælg omkostningsobjekt** til at vælge bærere til at filtrere data på.
    
        > [!NOTE]
        > Hvilke bærere der vises på listen, afhænger af, hvilken adgang der er givet i modulet **Omkostningsregnskab**.

-   **Visninger:** Baseret på de handlinger, der er valgt og konfigurationen i modulet **Omkostningsregnskab**, kan du se følgende oplysninger om kortene:

    -   Faktisk vs. budget (aktuel periode)
    -   Faktisk vs. revideret budget (aktuel periode)
    -   Faktisk vs. budget (forrige periode)
    -   Faktisk vs. revideret budget (forrige periode)
    -   Faktisk vs. budget (år til dato)
    -   Faktisk vs. revideret budget (år til dato)

    På hvert kort vises følgende beløb: faktisk, budget, afvigelse og afvigelse i %.

-   **Links:**

    -   Detaljer for aktuel periode
    -   Detaljer for forrige periode
    -   Detaljer for år til dato

    Når du vælger et link, vises et kort for hvert omkostningselement. Følgende beløb vises på hvert kort: faktisk, budget, budgetafvigelse, budgetafvigelse i %, revideret budget, revideret budgetafvigelse og revideret budgetafvigelse i %.
    
    [![Kort til et omkostningselement](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne er forskellige, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)
Hvis Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) er implementeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Omkostningsstyring** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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

<td>KB 4013633 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Omkostningsstyring</strong> til mobilenheder. For at implementere KB 4013633 skal systemadministratoren gøre følgende.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installere metadatahotfixet</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvend den installerbare pakke</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publicer arbejdsområdet <strong>Omkostningsstyring</strong> på mobilenheder.</td>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Få vist ydeevnen for din bærer ved hjælp af arbejdsområdet til omkostningsstyring på mobilenheden

1.  På din mobilenhed skal du vælge arbejdsområdet **Omkostningsstyring**.
2.  Vælg **Styring af omkostningsobjekt**.
3.  Vælg **Handlinger**.
4.  Vælg **Vælg variant** for at vælge et omkostningsstyringslayout.
5.  Vælg **Udført**.
6.  Vælg **Handlinger**.
7.  Vælg **Vælg omkostningsobjekt** for at vælge de bærere, som du har fået adgang til.
8.  Vælg **Udført**.
9.  Se den samlede ydeevne for din bærer.
10. Vælg linket **Detaljer for aktuel periode**.
11. Se ydeevnen for individuelle omkostningselementer.
12. Du kan også søge efter bestemte omkostningselementer.


