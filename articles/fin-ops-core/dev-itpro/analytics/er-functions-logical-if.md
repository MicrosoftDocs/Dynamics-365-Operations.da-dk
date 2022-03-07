---
title: ER-funktionen IF
description: Dette emne indeholder oplysninger om, hvordan funktionen IF til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 3674618acae79170daf94413895d17d86a491996
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753162"
---
# <a name="if-er-function"></a>ER-funktionen IF

[!include [banner](../includes/banner.md)]

Funktionen `IF` returnerer den først angivne værdi, hvis den angivne betingelse er opfyldt. Ellers returneres den anden angivne værdi. Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper.

## <a name="syntax"></a>Syntaks

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumenter

`condition`: *Boolesk*

Et gyldigt betinget udtryk, der skal afprøves.

`first value`: *Alle understøttede datatyper*

Det resultat, der returneres, hvis betingelsen er opfyldt.

`second value`: *Alle understøttede datatyper*

Det resultat, der returneres, hvis betingelsen ikke er opfyldt.

## <a name="return-values"></a>Returnerede værdier

*Alle understøttede datatyper*

Den resulterende værdi af en af de understøttede datatyper.

## <a name="usage-notes"></a>Bemærkninger til brug

Argumenterne `first value` og `second value` skal angives ved hjælp af den samme datatype. Der udløses en undtagelse på designtidspunktet, hvis datatyperne for de konfigurerede værdier ikke matcher.

Hvis den første og den anden resultatværdi er værdier af datatypen *Container (post)* eller *Postliste*, indeholder resultatet kun de felter, der findes i begge værdier.

## <a name="example"></a>Eksempel

`IF (1=2, "condition is met", "condition is not met")` returnerer strengen **betingelsen er ikke opfyldt**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]