---
title: ER-funktionen INDEX
description: Dette emne indeholder oplysninger om, hvordan funktionen INDEX til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087745"
---
# <a name="index-er-function"></a>ER-funktionen INDEX

[!include [banner](../includes/banner.md)]

Funktionen `INDEX` returnerer en *Container (post)*-værdi, der er valgt ved hjælp af det angivne numeriske indeks på den angivne liste. Der udløses en undtagelse, hvis indekset er uden for området for posterne på den angivne liste.

## <a name="syntax"></a>Syntaks

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`index`: *Heltal*

Et numerisk indeks, der angiver placeringen af den ønskede post på den angivne liste.

> [!NOTE]
> Da der bruges ettalsbaseret nummerering til denne funktion, skal du angive værdien **1** for at returnere den første post på den angivne liste.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="example-1"></a>Eksempel 1

Hvis du angiver datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `DS.Value` tekstværdien **"B"** for den anden post på denne postliste. Udtrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstværdien **"B"**.

## <a name="example-2"></a>Eksempel 2

Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, udløser udtrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` en undtagelse under kørslen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
