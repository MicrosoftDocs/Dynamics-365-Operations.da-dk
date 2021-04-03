---
title: ER-funktionen LIST
description: Dette emne indeholder oplysninger om, hvordan funktionen LIST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563842"
---
# <a name="list-er-function"></a>ER-funktionen LIST

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]