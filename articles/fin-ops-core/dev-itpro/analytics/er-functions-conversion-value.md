---
title: ER-funktionen VALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen VALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681202"
---
# <a name="value-er-function"></a>ER-funktionen VALUE

[!include [banner](../includes/banner.md)]

Funktionen `VALUE` returnerer en *Reel* værdi, der konverteres fra den angivne streng.

## <a name="syntax"></a>Syntaks

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En strengværdi, der skal konverteres til en numerisk værdi.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som et negativt fortegn. Der udløses en undtagelse under kørslen, hvis den angivne streng indeholder andre ikke-numeriske tegn.

## <a name="example-1"></a>Eksempel 1

`VALUE ("1 234,56")` udløser en undtagelse.

## <a name="example-2"></a>Eksempel 2

`VALUE ("1234,56")` returnerer **1234,56**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Typekonverteringsfunktioner](er-functions-category-type-conversion.md)
