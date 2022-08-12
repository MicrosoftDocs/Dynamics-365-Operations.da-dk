---
title: Arbejdsområde til omkostningsstyring på mobilenheder
description: Denne artikel indeholder oplysninger om arbejdsområdet til omkostningsstyring på mobilenheder. I dette arbejdsområde kan ledere af bærere se oplysninger om bærerydeevnen når som helst og hvor som helst.
author: AndersGirke
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d6d3fdcc0b0387a92f138b0ba7cf537f473b91a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069557"
---
# <a name="cost-controlling-mobile-workspace"></a>Arbejdsområde til omkostningsstyring på mobilenheder

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Denne artikel indeholder oplysninger om arbejdsområdet **Omkostningsstyring** på mobilenheder. I dette arbejdsområde kan ledere af bærere se oplysninger om bærerydeevnen når som helst og hvor som helst.

Dette mobile arbejdsområde er beregnet til brug sammen med mobilappen finans og drift (Dynamics 365).

## <a name="overview"></a>Overblik
Arbejdsområdet til **Omkostningsstyring** på mobilenheder giver et øjeblikkeligt overblik over den aktuelle ydeevne af bærere ved at sammenligne faktiske omkostninger med de budgetterede omkostninger. Du kan gå ned på detailniveau og se status for individuelle kostelementer.

En medarbejder modtager f.eks. en invitation til en international konference, men organisationen skal dække alle rejseudgifter. Medarbejdere spørger chefen, om de må deltage i konferencen. Chefen åbner arbejdsområdet til **Omkostningsstyring** på mobilenheden for at se, om der er budget til, at medarbejdere kan deltage i konferencen.

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

    På hvert kort vises følgende beløb: Faktisk, budget, afvigelse og afvigelse i %.

-   **Links:**

    -   Detaljer for aktuel periode
    -   Detaljer for forrige periode
    -   Detaljer for år til dato

    Når du vælger et link, vises et kort for hvert omkostningselement. Følgende beløb vises på hvert kort: faktisk, budget, budgetafvigelse, budgetafvigelse i %, revideret budget, revideret budgetafvigelse og revideret budgetafvigelse i %.
    
    [![Kort til et omkostningselement.](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne er forskellige, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 Finance
Hvis Finance er implementeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Omkostningsstyring** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger version 1611 med Platform update 3 eller nyere
Hvis version 1611 med Platform update 3 eller nyere er implementeret for organisationen, skal systemadministratoren opfylde følgende forudsætninger.

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

<td>KB 4013633 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Omkostningsstyring</strong> til mobilenheder. For at implementere KB 4013633 skal systemadministratoren gøre følgende.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Hente metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installere metadatahotfixet</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publicer arbejdsområdet <strong>Omkostningsstyring</strong> på mobilenheder.</td>
<td>Systemadministrator</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen
Download og installer mobilappen finans og drift (Dynamics 365):

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen

1.  Start appen på din mobilenhed.
2.  Angiv URL-adressen til din Dynamics 365.
3.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
4.  Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

[![Træk ned for at opdatere.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

