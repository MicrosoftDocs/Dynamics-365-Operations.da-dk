---
title: ER-funktionen WHERE
description: Dette emne indeholder oplysninger om, hvordan funktionen WHERE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: bdf5c658fda83399c7bcffeaaf07005164c53f8a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745491"
---
# <a name="where-er-function"></a>ER-funktionen WHERE

[!include [banner](../includes/banner.md)]

Funktionen `WHERE` returnerer den angivne liste som en *Postliste*-værdi, efter at den er blevet filtreret i henhold til den angivne betingelse.

## <a name="syntax"></a>Syntaks

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`condition`: *Boolesk*

Et gyldigt betinget udtryk, der bruges til at filtrere poster på den angivne liste.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion adskiller sig fra funktionen [FILTER](er-functions-list-filter.md), fordi den angivne betingelse anvendes på enhver elektronisk rapporteringsdatakilde (ER-datakilde) af typen *Postliste*, som er tilgængelige i hukommelsen.

Hvis de argumenter, der er konfigureret for denne funktion (`list` og `condition`), tillader, at denne anmodning oversættes til det direkte SQL-kald, bliver der udløst en advarsel på designtidspunktet. Denne meddelelse informerer brugeren om, at ydeevnen kan blive forbedret, hvis funktionen [FILTER](er-functions-list-filter.md) bruges i stedet for `WHERE`.

## <a name="example-1"></a>Eksempel 1

Hvis **Leverandør** er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil udtrykket `WHERE (Vendors, Vendors.VendGroup = "40")` alene returnere en liste over de leverandører, der tilhører leverandørgruppe 40.

## <a name="example-2"></a>Eksempel 2

Hvis du angiver datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `WHERE( DS, DS.Value = "B")` en liste med blot én post, som indeholder teksten **"B"** i feltet **Værdi**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]