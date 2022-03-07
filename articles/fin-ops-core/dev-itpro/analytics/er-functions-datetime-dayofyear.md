---
title: ER-funktionen DAYOFYEAR
description: Dette emne indeholder oplysninger om, hvordan funktionen DAYOFYEAR til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: ab252b6194267836ba9e1d85f3b96fb100c9f598c783bd9c849c6490c2e54e21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712303"
---
# <a name="dayofyear-er-function"></a>ER-funktionen DAYOFYEAR

[!include [banner](../includes/banner.md)]

Funktionen `DAYOFYEAR` returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem 1. januar og den angivne dato.

## <a name="syntax"></a>Syntaks

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoværdi, som repræsenterer den dato, der skal bruges til beregning af antallet af dage.

## <a name="return-values"></a>Returnerede værdier

*Heltal*

Den resulterende numeriske værdi.

## <a name="example-1"></a>Eksempel 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returnerer **61**.

## <a name="example-2"></a>Eksempel 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returnerer **1**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]