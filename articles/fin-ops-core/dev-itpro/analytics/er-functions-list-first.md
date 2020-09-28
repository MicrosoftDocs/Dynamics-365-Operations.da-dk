---
title: ER-funktionen FIRST
description: Dette emne indeholder oplysninger om, hvordan funktionen FIRST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745219"
---
# <a name="first-er-function"></a>ER-funktionen FIRST

[!include [banner](../includes/banner.md)]

Funktionen `FIRST` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne liste ikke er tom. Hvis listen er tom, udløser denne funktion en undtagelse.

## <a name="syntax"></a>Syntaks

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="example-1"></a>Eksempel 1

Udtrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstværdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `FIRST(SPLIT("",1)).Value` udløser en undtagelse under kørslen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
