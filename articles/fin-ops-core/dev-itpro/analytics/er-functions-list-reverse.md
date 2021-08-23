---
title: ER-funktionen REVERSE
description: Dette emne indeholder oplysninger om, hvordan funktionen REVERSE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 96fc3c2f845f84a5435fd0119a7eaa146caa2dc8da9c931ccfe0915af91ed7cb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752357"
---
# <a name="reverse-er-function"></a>ER-funktionen REVERSE

[!include [banner](../includes/banner.md)]

Funktionen `REVERSE` returnerer den angivne liste som en *Postliste*-værdi i omvendt sorteringsrækkefølge.

## <a name="syntax"></a>Syntaks

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="example-1"></a>Eksempel 1

Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` tekstværdien **"C"**.

## <a name="example-2"></a>Eksempel 2

Hvis **Leverandør** er konfigureret som en datakilde til elektronisk rapportering, der henviser til tabellen VendTable, vil udtrykket `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returnere en liste over leverandører, der er sorteret efter navn i faldende rækkefølge.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]