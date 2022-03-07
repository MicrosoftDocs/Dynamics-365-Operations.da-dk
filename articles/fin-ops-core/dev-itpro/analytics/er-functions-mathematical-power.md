---
title: ER-funktionen POWER
description: Dette emne indeholder oplysninger om, hvordan funktionen POWER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570416"
---
# <a name="power-er-function"></a>ER-funktionen POWER

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]