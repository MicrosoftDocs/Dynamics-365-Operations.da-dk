---
title: ER-funktionen ROUND
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUND til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683250"
---
# <a name="round-er-function"></a>ER-funktionen ROUND

[!include [banner](../includes/banner.md)]

Funktionen `ROUND` returnerer det angivne tal som en *Reel* værdi, når det er afrundet til det angivne antal decimaler.

## <a name="syntax"></a>Syntaks

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reel*

En numerisk værdi, der skal afrundes.

`decimals`: *Heltal*

En numerisk værdi, der repræsenterer antallet af decimaler.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis værdien for argumentet `decimals` er større end 0 (nul), afrundes det angivne tal til det angivne antal decimaler.

Hvis værdien for argumentet `decimals` er **0** (nul), afrundes det angivne tal til det nærmeste lige heltal.

Hvis værdien af argumentet `decimals` er mindre end 0 (nul), afrundes det angivne tal mod venstre til decimalpunktet.

## <a name="example-1"></a>Eksempel 1

`ROUND (1200.767, 2)` afrunder til to decimaler og returnerer **1200,77**.

## <a name="example-2"></a>Eksempel 2

`ROUND (1200.767, -3)` afrunder til det nærmeste multiplum af 1.000 og returnerer **1000**.

## <a name="example-3"></a>Eksempel 3

`ROUND (1200.5, 0)` afrundes til det nærmeste lige heltal og returnerer **1200**, mens `ROUND (1201.5, 0)` gør har samme og returnerer **1202**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Matematiske funktioner](er-functions-category-mathematical.md)
