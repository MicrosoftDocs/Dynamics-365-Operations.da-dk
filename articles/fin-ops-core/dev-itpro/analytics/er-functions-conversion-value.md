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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917620"
---
# <a name="VALUE">ER-funktionen VALUE</a>

[!include [banner](../includes/banner.md)]

Funktionen `VALUE` returnerer en *Reel* værdi, der konverteres fra den angivne streng.

## <a name="syntax"></a>Syntaks

```
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
