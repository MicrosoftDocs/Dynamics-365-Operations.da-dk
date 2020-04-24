---
title: LISTJOIN ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTJOIN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249029"
---
# <a name=""></a><a name="LISTJOIN">LISTJOIN ER-funktion</a>

[!include [banner](../includes/banner.md)]

Funktionen `LISTJOIN` returnerer en *Postliste*-værdi, der repræsenterer en ny forenet liste af poster, som er oprettet på grundlag af de angivne argumenter.

## <a name="syntax"></a>Syntaks

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumenter

`list 1`: *Postliste*

En reference til en datakilde af datatypen *Postliste*. Dette argument skal udfyldes.

`list N`: *Postliste*

En reference til en datakilde af datatypen *Postliste*. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Strukturen i den liste, der oprettes, indeholder kun de felter, som findes i strukturen for hver postliste, der er henvist til i argumenterne.

## <a name="example"></a>Eksempel

Du indtaster datakilde **Post 1** af typen `Container`. Denne datakilde indeholder følgende indlejrede felter af typen `Calculated field`:

- **Kode**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `String`.
- **Beløb**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Real`.

Du indtaster derefter datakilde **Post 2** af typen `Container`. Denne datakilde indeholder følgende indlejrede felter af typen `Calculated field`:

- **Beløb**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Real`.
- **ErGyldig**: Dette felt indeholder et udtryk, der returnerer en værdi af typen `Boolean`.

I dette tilfælde returnerer udtrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste, der indeholder to poster. Strukturen i denne liste består af et enkelt felt for **Beløb** af typen `Real`, fordi dette felt er det eneste felt, der vises i alle argumenterne for den kaldte funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
