---
title: ER-funktionen ORDERBY
description: Dette emne indeholder oplysninger om, hvordan funktionen ORDERBY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 6ff280d66fd2c418984f2d7fd31a32609932e89c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745003"
---
# <a name="orderby-er-function"></a>ER-funktionen ORDERBY

[!include [banner](../includes/banner.md)]

Funktionen `ORDERBY` returnerer den angivne liste som en *Postliste*-værdi, efter at den er sorteret i henhold til de angivne argumenter. Disse argumenter kan defineres som udtryk.

## <a name="syntax"></a>Syntaks

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`expression 1`: *Felt*

Den gyldige sti til et felt i datakilden, som `list`-argumentet for den kaldte funktion refererer til. Det felt, der refereres til, skal være et felt af den primitive datatype. Dette argument skal udfyldes.

`expression N`: *Felt*

Den gyldige sti til et felt i datakilden, som `list`-argumentet for den kaldte funktion refererer til. Det felt, der refereres til, skal være et felt af den primitive datatype. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="example-1"></a>Eksempel 1

Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstværdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Hvis **Leverandør** er konfigureret som en datakilde til elektronisk rapportering, der henviser til tabellen VendTable, vil udtrykket `ORDERBY (Vendors, Vendors.'name()')` returnere en liste over leverandører, der er sorteret efter navn i stigende rækkefølge.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
