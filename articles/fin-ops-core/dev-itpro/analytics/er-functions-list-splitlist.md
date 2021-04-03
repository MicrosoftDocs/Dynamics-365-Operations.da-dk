---
title: ER-funktionen SPLITLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLITLIST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559132"
---
# <a name="splitlist-er-function"></a>ER-funktionen SPLITLIST

[!include [banner](../includes/banner.md)]

Funktionen `SPLITLIST` opdeler den angivne liste i underlister (eller batches), som hver især indeholder det angivne antal poster. Derefter returneres resultatet som en ny *Postliste*-værdi, der består af batches.

## <a name="syntax"></a>Syntaks

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`number`: *Heltal*

Det højeste antal viste poster per batch.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Den returnerede batchliste indeholder følgende elementer:

 - **Værdi:** *Liste*

    Listen over poster, der tilhører den aktuelle batch.

- **Batchnumber:** *Heltal*

    Antallet af aktuelle batches på den returnerede liste.

## <a name="example"></a>Eksempel

I følgende illustration er der oprettet en **Linjer**-datakilde som en postliste, der har mere end tre poster. Denne liste er opdelt i bundter, som hver indeholder op til to poster.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

I følgende illustration vises det designede formatlayout. I dette formatlayout er bindinger til datakilden **Linjer** oprettet for at generere outputtet i XML-format. Dette output viser individuelle noder for hvert parti og posterne i det.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

I følgende illustration vises resultatet, når det designede format køres.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]