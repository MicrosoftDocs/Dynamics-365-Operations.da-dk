---
title: ER-funktionen DATETIMEVALUE
description: Denne artikel indeholder oplysninger om, hvordan funktionen DATETIMEVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 7e3af6a279163183546255908730ba32d790a22b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870429"
---
# <a name="datetimevalue-er-function"></a>ER-funktionen DATETIMEVALUE

[!include [banner](../includes/banner.md)]

Funktionen `DATETIMEVALUE` returnerer en værdi i form af *[DatoKlokkeslæt](er-formula-supported-data-types-primitive.md#datetime)*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en dato-/klokkeslætsværdi. Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Tekst, der repræsenterer den værdi, der skal formateres.

`format`: *Streng*

Den angivne tekst format. Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Streng*

Den kultur, der bruges til formatering af den givne tekst. Du kan finde oplysninger om de understøttede kulturer under [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Returnerede værdier

*Dato/klokkeslæt*

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
