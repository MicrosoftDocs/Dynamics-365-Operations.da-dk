---
title: ER-funktionen ROUNDAMOUNT
description: Denne artikel indeholder oplysninger om, hvordan funktionen ROUNDAMOUNT til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286023"
---
# <a name="roundamount-er-function"></a>ER-funktionen ROUNDAMOUNT

[!include [banner](../includes/banner.md)]

Funktionen `ROUNDAMOUNT` returnerer en *Reel* værdi som resultatet af afrundingen af det angivne tal til nærmeste multiplum af et andet tal i henhold til den angivne afrundingsregel.

## <a name="syntax"></a>Syntaks

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumenter

`number`: *Int* eller *Reel*

En numerisk værdi, der skal afrundes.

`decimals`: *Int* eller *Reel*

Det tal, som værdien af parametret `number` skal afrundes til et multiplum af.

`round rule`: *Fasttekstværdi*

En fasttekstværdi af fastteksten **RoundOffType**, der definerer afrundingsreglen. Denne fasttekst indeholder følgende værdier:

- Normal (almindelig)
- Nedad (rund nedad)
- Oprunding (rund op)

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi er et multiplum af den værdi, der er angivet af parametret `decimals`, og er tættest på den værdi, der er angivet af parametret `number`.

## <a name="usage-notes"></a>Bemærkninger til brug

Når parametret `number` er nul, returnerer denne funktion altid nul.

Når parametret `decimals` er nul, afrundes denne funktion til standardværdien for afrunding. Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, er standardværdien for afrunding **0,01**. Ellers er standardværdien for afrunding **1,0**.

Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, afrundes denne funktion til nærmeste afrundede beløb.

Når parametret `round rule` er angivet til **RoundOffType.RoundDown**, afrunder denne funktion ned til nul for nærmeste afrundede beløb.

Når parametret `round rule` er angivet til **RoundOffType.RoundUP**, afrunder denne funktion op fra til det nærmeste afrundede beløb.

Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, fungerer denne funktion som Excel-funktionen [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) og X+ +-funktionen [ROUND](../dev-ref/xpp-math-run-time-functions.md#round).

## <a name="remarks"></a>Kommentarer

Hvis du vil afrunde en numerisk værdi til et angivet antal decimaler, skal du bruge funktionen [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Eksempel

Hvis parametret **model.RoundOff** er indstillet til **RoundOffType.Ordinary**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Hvis parametret **model.RoundOff** er indstillet til **RoundOffType.RoundDown**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35. 

Hvis parametret **model.RoundOff** er indstillet til **RoundOffType.RoundUp**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)

[Matematiske funktioner](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
