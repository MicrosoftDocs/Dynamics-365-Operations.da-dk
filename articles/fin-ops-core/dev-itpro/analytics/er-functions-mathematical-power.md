---
title: ER-funktionen POWER
description: Dette emne indeholder oplysninger om, hvordan funktionen POWER til elektronisk rapportering (ER) skal anvendes.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041624"
---
# <a name="POWER">ER-funktionen POWER</a>

[!include [banner](../includes/banner.md)]

Funktionen `POWER` returnerer en *Reel* værdi, der repræsenterer resultatet af at hæve det angivne positive tal til den angivne effekt.

## <a name="syntax"></a>Syntaks

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenter

`number`: *Reel* eller *Heltal*

En numerisk værdi, der skal opløftes til den angivne effekt.

`power`: *Reel* eller *Heltal*

En numerisk værdi, der repræsenterer den specifikke effekt.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="example-1"></a>Eksempel 1

`POWER (10, 2)` returnerer **100**.

## <a name="example-2"></a>Eksempel 2

`POWER (4, 0.5)` returnerer **2**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Matematiske funktioner](er-functions-category-mathematical.md)
