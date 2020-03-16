---
title: ER-funktionen DAYOFYEAR
description: Dette emne indeholder oplysninger om, hvordan funktionen DAYOFYEAR til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070661"
---
# <a name="DAYOFYEAR">ER-funktionen DAYOFYEAR</a>

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
