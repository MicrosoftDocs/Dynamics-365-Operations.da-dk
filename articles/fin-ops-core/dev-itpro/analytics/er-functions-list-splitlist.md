---
title: ER-funktionen SPLITLIST
description: Denne artikel indeholder oplysninger om, hvordan funktionen SPLITLIST til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292520"
---
# <a name="splitlist-er-function"></a>ER-funktionen SPLITLIST

[!include [banner](../includes/banner.md)]

Funktionen `SPLITLIST` opdeler den angivne liste i underlister (eller batches), som hver især indeholder det angivne antal poster. Derefter returneres resultatet som en ny *Postliste*-værdi, der består af batches.

## <a name="syntax-1"></a>Syntaks 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`number`: *Heltal*

Det højeste antal viste poster per batch.

`on-demand reading flag`: *Boolesk*

En *boolesk* værdi, der angiver, om elementer i underlister skal genereres efter behov.

## <a name="return-values"></a>Returnerede værdier

*Liste over poster*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Den returnerede batchliste indeholder følgende elementer:

 - **Værdi:** *Liste*

    Listen over poster, der tilhører den aktuelle batch.

- **Batchnumber:** *Heltal*

    Antallet af aktuelle batches på den returnerede liste.

Når aflæsningsflaget efter behov angives til **Sand**, genereres der underlister ved anmodning, hvilket gør det muligt at reducere forbruget af hukommelse, men det kan medføre nedsat ydeevne, hvis elementer ikke bruges sekventielt.

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
