---
title: LISTJOIN ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen LISTJOIN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b300cef0a508f7cc37397480738091158efdead
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027909"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER-funktion

[!include [banner](../includes/banner.md)]

Funktionen `LISTJOIN` returnerer en *Postliste*-værdi, der repræsenterer en ny forenet liste af poster, som er oprettet på grundlag af de angivne argumenter.

## <a name="syntax"></a>Syntaks

```vb
LISTJOIN (list 1 [, list 2, …, list N])
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

![Side for ER-modeltilknytningsdesigner](./media/er-functions-list-listjoin-image1.gif)

I dette tilfælde returnerer udtrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste, der indeholder to poster.

![Designerside med to poster til ER-modeltilknytning](./media/er-functions-list-listjoin-image2.gif)

Strukturen i denne liste består af et enkelt felt for **Beløb** af typen `Real`, fordi dette felt er det eneste felt, der vises i alle argumenterne for den kaldte funktion.

![Designerside med beløbsfelt til ER-modeltilknytning](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)

[Fejlfinde datakilder for et udført ER-format for at analysere dataflow og -transformering](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
