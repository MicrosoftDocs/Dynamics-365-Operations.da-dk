---
title: ER-funktionen TRANSLATE
description: Denne artikel indeholder oplysninger om, hvordan funktionen TRANSLATE til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 04/02/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278435"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
