---
title: ER-funktionen TRANSLATE
description: Dette emne indeholder oplysninger om, hvordan funktionen TRANSLATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744233"
---
# <a name="translate-er-function"></a>ER-funktionen TRANSLATE

[!include [banner](../includes/banner.md)]

Funktionen `TRANSLATE` returnerer en *Streng*-værdi, der indeholder resultatet af tegnerstatningen af den angivne tekst i tegn for et andet angivet sæt tegn.

## <a name="syntax"></a>Syntaks

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

`pattern`: *Streng*

Den tekst, der skal erstattes.

`replacement`: *Streng*

Den tekst, der skal bruges som erstatning.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Funktionen `TRANSLATE` erstatter ét tegn ad gangen. Funktionen erstatter det første tegn i argumentet `text`med det første tegn i argumentet `pattern` og derefter det andet tegn og følger det samme forløb, indtil det er afsluttet. Når et tegn fra argumenterne `text` og `pattern` matcher, erstattes det af et tegn fra argumentet `replacement`, der er placeret i samme position som tegnet fra argumentet `pattern`. Hvis et tegn vises flere gange i argumentet `pattern`, bruges den `replacement`-argumenttilknytning, der svarer til den første forekomst af dette tegn.

## <a name="example-1"></a>Eksempel 1

`TRANSLATE ("abcdef", "cd", "GH")` erstatter tegnet **C**-tegnet i den angivne **"abcdef-**-tekst med tegnet **" G "** i `replacement`-teksten på grund af følgende:
-   Tegnet **"C"** vises i `pattern`-teksten i første position.
-   Den første position af `replacement`-teksten indeholder tegnet **"G"**.

## <a name="example-2"></a>Eksempel 2

`TRANSLATE ("abcdef", "ccd", "GH")` returnerer **"abGdef"**.

## <a name="example-3"></a>Eksempel 3

`TRANSLATE ("abccba", "abc", "123")` returnerer **"123321"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
