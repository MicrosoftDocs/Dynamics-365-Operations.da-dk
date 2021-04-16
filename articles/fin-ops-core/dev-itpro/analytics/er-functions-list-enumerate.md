---
title: ER-funktionen ENUMERATE
description: Dette emne indeholder oplysninger om, hvordan funktionen ENUMERATE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746645"
---
# <a name="enumerate-er-function"></a>ER-funktionen ENUMERATE

[!include [banner](../includes/banner.md)]

Funktionen `ENUMERATE` returnerer en ny *Postliste*-værdi, der består af optalte poster på den angivne liste.

## <a name="syntax"></a>Syntaks

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Listen over optalte poster, der returneres, udsætter følgende yderligere elementer:

- Feltposter (**Værdi**-komponent)
- Det aktuelle postindeks (**Tal**-komponent)

## <a name="example"></a>Eksempel

I følgende illustration er **Enumerated**-datakilden oprettet som en fasttekstliste over kreditorposter fra **Vendors**-datakilden, der henviser til VendTable-tabellen.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

I følgende illustration vises formatet elektronisk rapportering (ER). I dette format oprettes databindinger for at generere outputtet i XML-format. Dette output viser individuelle leverandører som optalte noder.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

I følgende illustration vises resultatet, når det designede format køres.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]