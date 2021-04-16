---
title: ER-funktionen ISEMPTY
description: Dette emne indeholder oplysninger om, hvordan funktionen ISEMPTY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750430"
---
# <a name="isempty-er-function"></a>ER-funktionen ISEMPTY

[!include [banner](../includes/banner.md)]

Funktionen `ISEMPTY` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne liste ikke indeholder nogen poster. Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="example-1"></a>Eksempel 1

Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `ISEMPTY(DS)` **FALSK**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `ISEMPTY (SPLIT ("",1))` returnerer **SANDT**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]