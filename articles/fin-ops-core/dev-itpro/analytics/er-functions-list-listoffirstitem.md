---
title: ER-funktionen LISTOFFIRSTITEM
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTOFFIRSTITEM til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: f2e1f7e55c61f883aebb9d5a522a883a9a9de694
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569834"
---
# <a name="listoffirstitem-er-function"></a>ER-funktionen LISTOFFIRSTITEM

[!include [banner](../includes/banner.md)]

Funktionen `LISTOFFIRSTITEM` returnerer en ny *Postliste*-værdi, der udelukkende består af de første poster på den angivne liste.

## <a name="syntax"></a>Syntaks

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="example"></a>Eksempel

Udtrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstværdien **"A"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]