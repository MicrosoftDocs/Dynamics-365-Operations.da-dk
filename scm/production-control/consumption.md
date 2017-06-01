---
title: Beregne materialeforbrug
description: Denne artikel indeholder oplysninger om forskellige indstillinger, der er relateret til beregning af materialeforbrug.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1bd3168e80719c86e9a0541200fdb1608410c8f5
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="calculate-material-consumption"></a>Beregne materialeforbrug

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om forskellige indstillinger, der er relateret til beregning af materialeforbrug. 

Følgende indstillinger, der er knyttet til beregning af materialeforbruge er tilgængelige på fanerne **Opsætning** og **Trinforbrug** på oversigtspanelet **Linjedetaljer** på siden **Stykliste**.

## <a name="variable-and-constant-consumption"></a>Variabelt eller konstant forbrug
I feltet **Forbrug er** kan du vælge, om forbruget skal beregnes som et konstant antal eller et variabelt antal. Vælg **Konstant**, hvis et fast antal eller volumen kræves til produktionen, uanset det producerede antal. Vælg **Variabelt**, som er standardindstillingen, hvis den påkrævede materiale i de færdige varer er proportionelt med antallet af færdigvarer, der er produceret.

## <a name="calculating-consumption-from-a-formula"></a>Beregne forbrug fra en formel
I feltet **Formel** kan du oprette forskellige formler til beregning af materialeforbruget. Hvis du bruger standardværdien, **Standard**, beregnes forbruger ikke fra en formel. Følgende formler fungerer sammen med felterne **Højde**, **Bredde**, **Dybde**, **Massefylde** og **Konstant**:

-   Højde \* Konstant
-   Højde \* Bredde \* Konstant
-   Højde \* Bredde \* Dybde \* Konstant
-   (Højde \* Bredde \* Dybde/Massefylde) \* Konstant

## <a name="rounding-up-and-multiples"></a>Afrunding og multipla
Sammen giver felterne **Afrunding** og **Multipla** dig mulighed for at afrunde materialeforbrugsværdien. Du kan for eksempel afrunde værdien i overensstemmelse med den materialehåndteringsenhed, hvori råvaren plukkes til produktion. Følgende indstillinger er tilgængelige i feltet **Afrunding**: **Antal**, **Måling** og **Forbrug**.

### <a name="quantity"></a>Antal

Hvis du vælger **Antal** som afrundingsmekanisme, skal antallet være et multiplum af det angivne antal. Hvis der f.eks. skal bruges hele tal, skal du angive **1** i feltet **Multipla**. Tal afrundes derefter til et antal, der er delelig med 1.

### <a name="measurement"></a>Mål

Typisk ville du vælge **Måling** som afrundingsmekanisme, når råvarer leveres i bestemte dimensioner. For eksempel et stykke metalrør på 2 meter, der kræves for en færdigvare, og metalrøret gemmes i længder på 4,5 meter. I dette tilfælde kan afrundingsmekanismen **Måling** bruges til at beregne, hvor mange metalrør, der kræves for at producere et bestemt antal stykker af den færdige vare. I dette eksempel er feltet **Formel** indstillet til **Højde \* konstant**. Feltet **Højde** er angivet til **2** for at angive længden af røret, der kræves for færdigvaren. Feltet **Multiplum** angives til **4,5** for at angive, at røret er plukket i længder på 4,5 meter. Her er beregningen:

1.  Antal multipla, der kræves til 10 stk. af færdigvaren: 10 ÷ 2 = 5 styk
2.  Samlet forbrug: 4,5 × 5 = 22,5 meter metalrør

Det antages, at 0,5 meter af røret er kasseret for hver fem stykker af rør, der forbruges.

### <a name="consumption"></a>Forbrug

Du vælger typisk**Forbrug** som afrundingsmekanisme, når råvaren skal plukkes i hele mængder af en bestemt materialehåndteringsenhed for produktet. 2 quarts maling anvendes f.eks. til at producere et stykke af en færdigvare, og malingen er plukket i bøtter a 25 quarts. I dette tilfælde kan afrundingsmekanismen **Forbrug** bruges til at afrunde forbrug af bøtter a 25 quarts til hele tal. Her er beregningen for den mængde af maling, der er påkrævet, hvis der skal produceres 180 stk. færdige varer:

1.  Maling, der skal bruges, uden spild: 180 × 2 = 360 quarts
2.  Antal bøtter: 360 ÷ 25 = 14.4, der afrundes til 15
3.  Maling, der skal bruges, med spild: 15 × 25 = 375 quarts

## <a name="step-consumption"></a>Trinforbrug
Trinforbrug bruges til at beregne konstant forbrug i antalsintervaller. Hvis du vælger **Trinforbrug** i feltet **Formel** på fanen **Opsætning**, kan du tilføje oplysninger om trinnene på fanen **Trinforbrug**. Det fast forbrugte antal kan være oprettet i intervaller af den producerede mængde. Trinforbrug er f.eks. angivet som vist i følgende tabel.

| Fra serie | Antal |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

Styklistens antal er 1, og produktionsantallet er 110. Formlen for forbruget er Fra serie (antal) = forbrug. Da produktionsmængden er 110, falder den ind i "Fra 100-serien." Antallet er der for 20.




