---
title: ER-funktionen CN_GBT_ADDITIONALDIMENSIONID
description: Dette emne indeholder oplysninger om, hvordan funktionen CN_GBT_ADDITIONALDIMENSIONID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686804"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>ER-funktionen CN_GBT_ADDITIONALDIMENSIONID

[!include [banner](../includes/banner.md)]

Funktionen `CN_GBT_ADDITIONALDIMENSIONID` returnerer en *Streng*-værdi, som repræsenterer et enkelt økonomisk dimensions-ID, der er hentet fra den angivne streng. Den angivne streng præsenterer alle dimensioner som en kommasepareret liste over ID'er.

## <a name="syntax"></a>Syntaks

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *Streng*-værdi der præsenterer alle dimensioner som en kommasepareret liste over ID'er.

`number`: Heltal

En *Heltals*-værdi, der definerer nummerseriekoden for den ønskede dimension i den angivne streng.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returnerer **"CC"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]