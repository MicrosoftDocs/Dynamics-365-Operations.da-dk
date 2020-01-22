---
title: ER-funktionen ROUNDUP
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUNDUP til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917045"
---
# <a name="ROUNDUP">ER-funktionen ROUNDUP</a>

[!include [banner](../includes/banner.md)]

Funktionen `ROUNDUP` returnerer det angivne tal som en *Reel* værdi, når det er rundet op til det angivne antal decimaler.

## <a name="syntax"></a>Syntaks

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenter

`number`: *Reel*

En numerisk værdi, der skal rundes op.

`decimals`: *Heltal*

En numerisk værdi, der repræsenterer antallet af decimaler.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion fungerer ligesom [ROUND](er-functions-mathematical-round.md), men den runder altid det angivne tal op (væk fra nul).

## <a name="example-1"></a>Eksempel 1

`ROUNDUP (1200.763, 2)` runder op til to decimaler og returnerer **1200,77**.

## <a name="example-2"></a>Eksempel 2

`ROUNDUP (1200.767, -3)` runder op til det nærmeste multiplum af 1.000 og returnerer **2000**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Matematiske funktioner](er-functions-category-mathematical.md)