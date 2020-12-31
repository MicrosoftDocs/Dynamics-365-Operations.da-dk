---
title: ER-funktionen DATEVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen DATEVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682407"
---
# <a name="datevalue-er-function"></a>ER-funktionen DATEVALUE

[!include [banner](../includes/banner.md)]

Funktionen `DATEVALUE` returnerer en værdi i form af en *Dato*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) til en datoværdi. Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Tekst, der repræsenterer den værdi, der skal formateres.

`format`: *Streng*

Den angivne tekst format.

`culture`: *Streng*

Den kultur, der bruges til formatering af den givne tekst.

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
