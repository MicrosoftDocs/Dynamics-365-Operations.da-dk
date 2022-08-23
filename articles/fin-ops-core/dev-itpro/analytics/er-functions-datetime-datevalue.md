---
title: ER-funktionen DATEVALUE
description: Denne artikel indeholder oplysninger om, hvordan funktionen DATEVALUE til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268692"
---
# <a name="datevalue-er-function"></a>ER-funktionen DATEVALUE

[!include [banner](../includes/banner.md)]

Funktionen `DATEVALUE` returnerer en værdi i form af en *[Dato](er-formula-supported-data-types-primitive.md#date)*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en datoværdi. Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Tekst, der repræsenterer den værdi, der skal formateres.

`format`: *Streng*

Den angivne tekst format. Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Streng*

Den kultur, der bruges til formatering af den givne tekst. Du kan finde oplysninger om de understøttede kulturer under [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Returnerede værdier

*Dato*

Den returnerede datoværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst. For eksempel, hvis funktionen `DATEVALUE` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur. Standardværdien for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returnerer datoværdien **21. december 21 2016**, baseret på det angivne brugerdefinerede format og standardprogrammets **en-us** kultur.

## <a name="example-2"></a>Eksempel 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returnerer datoværdien **21. januar 2016**, baseret på det angivne brugerdefinerede format og kultur.

Men `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` udløser en undtagelse for at informere brugeren om, at den angivne streng ikke genkendes som en gyldig dato for den angivne kultur.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
