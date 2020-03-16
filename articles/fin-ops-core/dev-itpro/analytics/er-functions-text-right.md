---
title: ER-funktionen RIGHT
description: Dette emne indeholder oplysninger om, hvordan funktionen RIGHT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040865"
---
# <a name="RIGHT">ER-funktionen RIGHT</a>

[!include [banner](../includes/banner.md)]

Funktionen `RIGHT` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng.

## <a name="syntax"></a>Syntaks

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *Streng*-værdi, der repræsenterer den oprindelige tekst.

`number`: *Heltal*

Det antal tegn, der skal returneres fra slutningen af den oprindelige tekst.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`RIGHT ("Sample", 3)` returnerer **"pel"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
