---
title: ER-funktionen SPLITLISTBYLIMIT
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLITLISTBYLIMIT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743418"
---
# <a name="splitlistbylimit-er-function"></a>ER-funktionen SPLITLISTBYLIMIT

[!include [banner](../includes/banner.md)]

Funktionen `SPLITLISTBYLIMIT` opdeler den angivne liste i en ny liste over underlister (batches). Antallet af poster i hvert batch beregnes dynamisk. Funktionen returnerer dernæst resultatet som en ny *Postliste*-værdi, der består af batches.

## <a name="syntax"></a>Syntaks

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`limit value`: *Heltal* eller *Reel*

Maksimumværdien for den grænse, der bruges til at opdele den oprindelige liste i batches.

`limit source`: *Felt*

Den gyldige sti til et felt af typen *Heltal* eller *Reel* på den angivne liste. Værdien i dette felt definerer det trin, som den samlede sum forøges med.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Den returnerede batchliste indeholder følgende elementer:

- **Værdi**: *Liste*

    Listen over poster, der tilhører den aktuelle batch.

- **Batchnumber**: *Heltal*

    Antallet af aktuelle batches på den returnerede liste.

Grænsen anvendes ikke på et enkelt element på den oprindelige liste, hvis grænsekilden overskrider den angivne grænse.

## <a name="example"></a>Eksempel

I følgende illustration vises et format til elektronisk rapportering (ER).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Følgende illustration viser de datakilder, der bruges til formatet.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

I følgende illustration vises resultatet, når formatet køres. I så fald er outputtet en simpel liste over råvarer.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

I de følgende illustrationer er det samme format blevet justeret, så den repræsenterer listen over varegoder i batches, hvis et enkelt batch skal indeholde goder, og den samlede vægt ikke må overstige en grænse 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

I følgende illustration vises resultatet, når det justerede format køres.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Grænsen anvendes ikke på den sidste vare på den oprindelige liste, da værdien (**11**) af grænsekilden (**vægt**) overskrider den angivne grænse (**9**). For at ignorere underordnede lister under oprettelse af rapporter skal du enten bruge funktionen `WHERE` eller udtrykket **Aktiveret** for det tilsvarende formatelement, du har brug for.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
