---
title: ER-funktionen EMPTYLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYLIST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559194"
---
# <a name="emptylist-er-function"></a>ER-funktionen EMPTYLIST

[!include [banner](../includes/banner.md)]

Funktionen `EMPTYLIST` returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.

## <a name="syntax"></a>Syntaks

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="example"></a>Eksempel

`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]