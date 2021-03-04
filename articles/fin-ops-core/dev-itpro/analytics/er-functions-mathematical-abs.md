---
title: ER-funktionen ABS
description: Dette emne indeholder oplysninger om, hvordan funktionen ABS til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683275"
---
# <a name="abs-er-function"></a>ER-funktionen ABS

[!include [banner](../includes/banner.md)]

Funktionen `ABS` returnerer den absolutte værdi (modulus) af det angivne tal som en *Reel* værdi. Returnerer med andre ord tallet uden dets fortegn.

## <a name="syntax"></a>Syntaks

```vb
ABS (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Reel*

En numerisk værdi, som du vil have modulus af.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="example"></a>Eksempel

`ABS (-1)` returnerer **1**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Matematiske funktioner](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]