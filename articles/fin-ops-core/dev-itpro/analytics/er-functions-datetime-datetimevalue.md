---
title: ER-funktionen DATETIMEVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen DATETIMEVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 711889e23e85b05c5e4c5ab904ec12ceb0bbb4da1f17d1c994adda1eec8ccb74
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776164"
---
# <a name="datetimevalue-er-function"></a>ER-funktionen DATETIMEVALUE

[!include [banner](../includes/banner.md)]

Funktionen `DATETIMEVALUE` returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato-/klokkeslætsværdi. Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Tekst, der repræsenterer den værdi, der skal formateres.

`format`: *Streng*

Den angivne tekst format.

`culture`: *Streng*

Den kultur, der bruges til formatering af den givne tekst.

## <a name="return-values"></a>Returnerede værdier

*DateTime*

Den returnerede dato-/klokkeslætsværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst. For eksempel, hvis funktionen `DATETIMEVALUE` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur. Standardværdien for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returnerer **2:55:00 den 21. december 21 2016**, baseret på det angivne brugerdefinerede format og standardprogrammets **en-us** kultur.

## <a name="example-2"></a>Eksempel 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returnerer **2:55:00 den 21. december 21 2016**, baseret på det angivne brugerdefinerede format og kultur.

Men `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` udløser en undtagelse for at informere brugeren om, at den angivne streng ikke genkendes som en gyldig dato-/klokkeslætsværdi for den angivne kultur.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]