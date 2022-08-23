---
title: ER-funktionen LIST
description: Denne artikel indeholder oplysninger om, hvordan funktionen LIST til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7a5f27baa248ec84c75725cf32a1f482841424c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277626"
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
