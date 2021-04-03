---
title: ER-funktionen ROUNDAMOUNT
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUNDAMOUNT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a80587236d17160a996d701ca4ae38be21c818c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563288"
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

Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, fungerer denne funktion som Excel-funktionen [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) og X+ +-funktionen [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).

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