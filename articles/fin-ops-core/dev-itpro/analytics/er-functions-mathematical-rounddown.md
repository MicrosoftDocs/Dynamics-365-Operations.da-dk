---
title: ER-funktionen ROUNDDOWN
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUNDDOWN til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686876"
---
# <a name="rounddown-er-function"></a>ER-funktionen ROUNDDOWN

[!include [banner](../includes/banner.md)]

Funktionen `ROUNDDOWN` returnerer det angivne tal som en *Reel* værdi, når det er rundet ned til det angivne antal decimaler.

## <a name="syntax"></a>Syntaks

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reel*

En numerisk værdi, der skal rundes ned.

`decimals`: *Heltal*

En numerisk værdi, der repræsenterer antallet af decimaler.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion fungerer ligesom [ROUND](er-functions-mathematical-round.md), men den runder altid det angivne tal ned (mod nul).

## <a name="example-1"></a>Eksempel 1

`ROUNDDOWN (1200.767, 2)` runder ned til to decimaler og returnerer **1200,76**. 

## <a name="example-2"></a>Eksempel 2

`ROUNDDOWN (1700.767, -3)` runder ned til det nærmeste multiplum af 1.000 og returnerer **1000**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Matematiske funktioner](er-functions-category-mathematical.md)
