---
title: ER-funktionen SPLIT
description: Denne artikel indeholder oplysninger om, hvordan funktionen SPLIT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 2acd93b645121b577d516d3ce29a3d05069b8de9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906823"
---
# <a name="split-er-function"></a>ER-funktionen SPLIT

[!include [banner](../includes/banner.md)]

Funktionen `SPLIT` opdeler den angivne inputstreng i understrenge og returnerer resultatet som en ny *Postliste*-værdi.

## <a name="syntax-1"></a>Syntaks 1

```vb
SPLIT (input, length)
```

Denne syntaks anvendes til at opdele den angivne inputstreng i understrenge, som hver især har den angivne længde.

## <a name="syntax-2"></a>Syntaks 2

```vb
SPLIT (input, delimiter)
```

Denne syntaks anvendes til at opdele den angivne inputstreng i understrenge baseret på den angivne afgrænser.

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den tekst du vil dele op.

`length`: *Heltal*

Den maksimale længde på en enkelt understreng.

`delimiter`: *Streng*

En afgrænser, der bruges til at adskille understrenge.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Poststrukturen for den returnerede liste består af feltet **Værdi** af typen *Streng*. Alle poster på listen, der returneres, indeholder genererede understrenge i dette felt.

Hvis argumentet `delimiter` er tomt, vil den nye liste, der returneres, bestå af én post, der har et **Værdi**-felt af typen *Streng*. Dette felt indeholder inputteksten.

Hvis `input`-argumentet er tomt, returneres en ny tom liste. Hvis hverken `input`- eller `delimiter`-argumentet er angivet (nul), opstår der en programundtagelse.

## <a name="example-1"></a>Eksempel 1

`SPLIT ("abcd", 3)` returnerer en ny liste, der består af to poster, som har et **Værdi**-felt af typen *Streng*. Feltet **Værdi** i den første post indeholder teksten **"abc"**, og feltet **Værdi** i den anden post indeholder teksten **"d"**.

## <a name="example-2"></a>Eksempel 2

`SPLIT ("XAb aBy", "aB")` returnerer en ny liste, der består af tre poster, som har et **Værdi**-felt af typen *Streng*. Feltet **Værdi** i den første post indeholder teksten **"X"**, feltet **Værdi** i den anden post indeholder teksten **"&nbsp;"**, og feltet **Værdi** i den tredje post indeholder teksten **"y"**. 

## <a name="example-3"></a>Eksempel 3

Du kan bruge funktionen [INDEX](er-functions-list-index.md) til at få adgang til individuelle elementer i den angivne inputstreng. Hvis du indtaster datakilden **MyList** af typen **Beregnet felt** og konfigurerer den for udtrykket `SPLIT("abc", 1)`, returnerer udtrykket `INDEX(MyList,2).Value` tekstværdien **"b"**.

## <a name="example-4"></a>Eksempel 4

Du kan også bruge funktionen [ENUMERATE](er-functions-list-enumerate.md) til at få adgang til individuelle elementer i den angivne inputstreng. Hvis du først angiver datakilden **MyList** for typen **Beregnet felt** og konfigurerer den for udtrykket `SPLIT("abc", 1)` og derefter angiver datakilden for **EnumeratedList** for typen **Beregnet felt** og konfigurerer udtrykket `ENUMERATE(MyList)` for den, returnerer udtrykket `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` teksten **"b"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
