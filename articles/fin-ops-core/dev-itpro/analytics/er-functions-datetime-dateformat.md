---
title: ER-funktionen DATEFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen DATEFORMAT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 4e9347937d088f15b4f489f0b85704a8688f8131
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743297"
---
# <a name="dateformat-er-function"></a>ER-funktionen DATEFORMAT

[!include [banner](../includes/banner.md)]

Funktionen `DATEFORMAT` returnerer en *Streng*-værdi, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoværdi, der repræsenterer den dato, der skal formateres.

`format`: *Streng*

Outputstrengens format.

`culture`: *Streng*

Den kultur, du vil bruge til formatering.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den resulterende strengværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Når kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst. For eksempel, hvis funktionen `DATEFORMAT` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur. Standardværdien for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som strengen **"24-12-2015"**, baseret på det angivne brugerdefinerede format.

## <a name="example-2"></a>Eksempel 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer datoen for den aktuelle programsession, 24. december 2015, som strengen **"24-12-2015"**, baseret på den valgte tyske kultur og det angivne format.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)
