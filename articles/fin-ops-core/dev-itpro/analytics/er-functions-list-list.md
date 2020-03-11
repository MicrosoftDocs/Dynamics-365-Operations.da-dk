---
title: ER-funktionen LIST
description: Dette emne indeholder oplysninger om, hvordan funktionen LIST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: ee51b6da008d1c0fcfb303e9659f507629237333
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042015"
---
# <a name="LIST">ER-funktionen LIST</a>

[!include [banner](../includes/banner.md)]

Funktionen `LIST` returnerer en ny *Postliste*-værdi, der består af en ny postliste, som er oprettet på grundlag af de angivne argumenter.

## <a name="syntax"></a>Syntaks

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumenter

`record 1`: *Container (post)*

En reference til en datakilde af datatypen *Post*. Dette argument skal udfyldes.

`record N`: *Container (post)*

En reference til en datakilde af datatypen *Post*. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Strukturen i den liste, der oprettes, indeholder kun de felter, der vises i strukturen for hver post, der er nævnt i argumenterne.

## <a name="example"></a>Eksempel

Du indtaster datakilde **Post 1** af typen *Container*. Denne datakilde indeholder følgende indlejrede felter af typen *Beregnet felt*:

- **Kode:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Streng*.
- **Beløb:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Reel*.

Du indtaster dernæst datakilde **Post 2** af typen *Container*. Denne datakilde indeholder følgende indlejrede felter af typen *Beregnet felt*:

- **Beløb:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Reel*.
- **IsValid:** Dette felt indeholder et udtryk, der returnerer en værdi af typen *Boolesk*.

I dette tilfælde returnerer udtrykket `LIST('Record 1', 'Record 2')` en ny liste, der indeholder to poster. Strukturen i denne liste består af et enkelt felt for **Beløb** af typen *Reel*, fordi dette felt er det eneste felt, der vises i alle argumenterne for den kaldte funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
