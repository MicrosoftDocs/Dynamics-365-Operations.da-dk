---
title: ER-funktionen LEFT
description: Dette emne indeholder oplysninger om, hvordan funktionen LEFT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743777"
---
# <a name="left-er-function"></a>ER-funktionen LEFT

[!include [banner](../includes/banner.md)]

Funktionen `LEFT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i begyndelsen af den angivne streng.

## <a name="syntax"></a>Syntaks

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *Streng*-værdi, der repræsenterer den oprindelige tekst.

`number`: *Heltal*

Det antal tegn, der skal returneres fra begyndelsen af den oprindelige tekst.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`LEFT ("Sample", 3)` returnerer **"Eks"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
