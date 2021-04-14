---
title: ER-funktionen CASE
description: Dette emne indeholder oplysninger om, hvordan funktionen CASE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 44815160957922f508fccd72174be2c4145a8d89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745443"
---
# <a name="case-er-function"></a>ER-funktionen CASE

[!include [banner](../includes/banner.md)]

Funktionen `CASE` evaluerer værdien af det angivne udtryk i forhold til de angivne alternative indstillinger og returnerer resultatet af den første indstilling, der er lig med værdien af det angivne udtryk. Ellers returneres det valgfrie standardresultat, hvis der er angivet et standardresultat som det sidste argument i den kaldte funktion, hvor der ikke er foretaget en forudgående indstilling. Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper.

## <a name="syntax"></a>Syntaks

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumenter

`expression`: *Primitiv datatype* (Boolesk, numerisk eller tekst)

Et gyldigt udtryk, der returnerer en værdi af den primitive datatype.

`option 1`: *Primitiv datatype* (Boolesk, numerisk eller tekst)

Et gyldigt udtryk, der returnerer en værdi af samme primitive datatype som argumentet `expression` for den kaldte funktion. Dette argument skal udfyldes.

`result 1`: *Alle understøttede datatyper*

Det returnerede resultat, der svarer til den foregående indstilling. Dette argument skal udfyldes.

`option N`: *Primitiv datatype* (Boolesk, numerisk eller tekst)

Et gyldigt udtryk, der returnerer en værdi af samme primitive datatype som argumentet `expression` for den kaldte funktion. Dette argument er valgfrit.

`result N`: *Alle understøttede datatyper*

Det returnerede resultat, der svarer til den foregående indstilling. Dette argument er valgfrit.

`default result`: *Alle understøttede datatyper*

Det resultat, der skal returneres, hvis der ikke er noget match. Dette argument er valgfrit.

## <a name="return-values"></a>Returnerede værdier

*Alle understøttede datatyper*

Den resulterende værdi af en af de understøttede datatyper.

## <a name="usage-notes"></a>Bemærkninger til brug

Der bliver udløst en undtagelse på kørselstidspunktet, hvis det ikke er et match, og et valgfrit standardresultat ikke er defineret.

Alle resultater skal angives ved hjælp af den samme datatype. Der udløses en undtagelse på designtidspunktet, hvis datatyperne for de konfigurerede resultater ikke matcher.

Hvis den første resultatværdi og den *N*'te resultatværdi er værdier af datatypen *Container (post)* eller *Postliste*, indeholder resultatet kun de felter, der findes i begge værdier.

## <a name="example"></a>Eksempel

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returnerer strengen **"VINTER"**, hvis den aktuelle dato for programsessionen er mellem oktober og december. Ellers returneres en tom streng.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]