---
title: ER-funktionen LISTOFFIRSTITEM
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTOFFIRSTITEM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 069ec0c6d5578ca6ab68814adf325bd79e73b9e8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745051"
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
