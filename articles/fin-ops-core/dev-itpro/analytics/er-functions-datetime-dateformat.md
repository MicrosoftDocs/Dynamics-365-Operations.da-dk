---
title: ER-funktionen DATEFORMAT
description: Denne artikel indeholder oplysninger om, hvordan funktionen DATEFORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: e48797def54150d259dd5e0a9a4206722c168bf4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852656"
---
# <a name="dateformat-er-function"></a>ER-funktionen DATEFORMAT

[!include [banner](../includes/banner.md)]

Funktionen `DATEFORMAT` returnerer en *[Streng](er-formula-supported-data-types-primitive.md#string)*-værdi, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntaks 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumenter

`date`: *[Dato](er-formula-supported-data-types-primitive.md#date)*

En datoværdi, der repræsenterer den dato, der skal formateres.

`format`: *Streng*

Outputstrengens format. Oplysninger om understøttede formater finder du under [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) og [brugerdefineret](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Der skelnes mellem store og små bogstaver i formatstrengen, når du enten bruger et standardformat eller et brugerdefineret format. F.eks. returnerer [standardformatet](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" datoen ved at bruge det korte datomønster, mens standardformatet "D" returnerer datoen ved at bruge det lange datomønster. Desuden returnerer det [brugerdefinerede](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M"-format måneden fra 1 til 12, mens det brugerdefinerede "m"-format returnerer minuttallet fra 0 til og med 59.

`culture`: *Streng*

Den kultur, du vil bruge til formatering. Du kan finde oplysninger om de understøttede kulturer under [kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den resulterende strengværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis kulturen ikke er defineret som et argument for den kaldte funktion, er værdien af `culture` defineret af den kaldende kontekst. For eksempel, hvis funktionen `DATEFORMAT` kaldes ved hjælp af syntaks 1 i et elektronisk rapporteringsformat (ER) for et **FIL**-element, der er konfigureret til at bruge den tyske kultur, vil konverteringen ske ved hjælp af den tyske kultur. Standardværdien for `culture` er **EN-US**.

## <a name="example-1"></a>Eksempel 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som strengen **"24-12-2015"**, baseret på det angivne brugerdefinerede format.

## <a name="example-2"></a>Eksempel 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returnerer datoen for den aktuelle programsession, 24. december 2015, som strengen **"24-12-2015"**, baseret på den valgte tyske kultur og det angivne format.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
