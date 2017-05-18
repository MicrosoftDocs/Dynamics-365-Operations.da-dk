---
title: "Arbejdsområde til omkostningsstyring på mobilenheder"
description: "Dette emne indeholder oplysninger om arbejdsområdet til omkostningsstyring på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Operations-mobilappen. I dette arbejdsområde kan ledere af bærere se oplysninger om bærerydeevnen når som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Arbejdsområde til omkostningsstyring på mobilenheder

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om arbejdsområdet til omkostningsstyring på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Operations-mobilappen. I dette arbejdsområde kan ledere af bærere se oplysninger om bærerydeevnen når som helst og hvor som helst. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Oversigt over arbejdsområde til omkostningsstyring på mobilenheder
-------------------------------------------------

Arbejdsområdet til **Omkostningsstyring** på mobilenheder giver et øjeblikkeligt overblik over den aktuelle ydeevne af bærere ved at sammenligne faktiske omkostninger med de budgetterede omkostninger. Du kan gå ned på detailniveau og se status for individuelle kostelementer. En medarbejder modtager f.eks. en invitation til en international konference, men organisationen skal dække alle rejseudgifter. Medarbejderen spørger sin chef, om han må deltage i konferencen. Chefen åbner arbejdsområdet til **Omkostningsstyring** på sin mobiltelefon for at se, om hun har budget til, at medarbejderen kan deltage i konferencen.

### <a name="data-security"></a>Datasikkerhed

Dataene i arbejdsområdet til **Omkostningsstyring** er sikret via brugerlegitimationsoplysninger. Ledere af bærere kan kun se data for deres egen bærer. Sikkerheden på adgangsniveau administreres i modulet **Omkostningsregnskab**. Bogholdere definerer konfiguration af arbejdsområdet til **Omkostningsstyring** i modulet **Omkostningsregnskab**. Når arbejdsområdet er publiceret på Microsoft Dynamics 365 for Operations-mobilappen, er det tilgængeligt i appen. Derfor kan alle bærerledere i organisationen se data i samme format.

### <a name="actions-views-and-links"></a>Handlinger, visninger og links

Arbejdsområdet til **Omkostningsstyring** på mobilenheder til Dynamics 365 for Operations-appen indeholder følgende handlinger, visninger og links:

-   **Handlinger:**
    -   Brug **Vælg variant** til at vælge et layout.
    -   Brug **Vælg omkostningsobjekt** til at vælge bærere til at filtrere data på. **Bemærk!** De bærere, der vises på listen, afhænger af, hvilken adgang der er givet i modulet **Omkostningsregnskab**.
-   **Visninger:** Baseret på de handlinger, der er valgt og konfigurationen i modulet **Omkostningsregnskab**, kan du se følgende oplysninger om kortene.
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
    
    [![Kort til et omkostningselement ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Forudsætninger
Før du kan bruge arbejdsområdet **Omkostningsstyring** på mobilenheder, skal systemadministratoren have sørget for, at følgende forudsætninger er opfyldt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere skal være implementeret.</td>
<td>Systemadministrator</td>
<td>Hvis Dynamics 365 for Operations ikke allerede er installeret i organisationen, kan systemadministratoren se under <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Installere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 skal være implementeret.</td>
<td>Systemadministrator</td>
<td>KB 4013633 (en X ++ opdatering eller et metadatahotfix) indeholder fire arbejdsområder til mobilenheder til supply chain management. For at implementere KB 4013633 skal systemadministratoren benytte følgende fremgangsmåde:
<ol>
<li>Hent KB 4013633 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installere metadatahotfixet</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Anvend den installerbare pakke</a> på dit Microsoft Dynamics 365 for Operations-system.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Arbejdsområdet <strong>Omkostningsstyring</strong> til mobilenheder skal være publiceret til Dynamics 365 for Operations-mobilappen.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Start Dynamics 365 for Operations i din browser.</li>
<li>På siden <strong>Systemparametre</strong> skal du vælge <strong>Administrer arbejdsområder til mobile enheder</strong>.</li>
<li>Vælg arbejdsområdet <strong>Oversigt over omkostningsobjekt</strong>.</li>
<li>Klik på <strong>Publicer arbejdsområde til mobilenheder</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Hent og installer Dynamics 365 for Operations-mobilappen
Hent og installer Microsoft Dynamics 365 for Operations-mobilappen i din mobilappbutik.

-   Til Android: [Dynamics 365 for Operations i Google Play Butik](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Til iPhone: [Dynamics 365 for Operations i iTunes-appbutikken](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Log på Dynamics 365 for Operations-mobilappen
1.  Start appen på din mobilenhed.
2.  Angiv din URL til Dynamics 365 for Operations.
3.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
4.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Dynamics 365 for Operations-konto. Angiv dine legitimationsoplysninger.
5.  Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren senere publicerer et nyt arbejdsområde, kan du trække for at opdatere listen over arbejdsområder til mobilenheder. 

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





