---
title: ER-funktionen INDEX
description: Dette emne indeholder oplysninger om, hvordan funktionen INDEX til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042061"
---
# <a name="INDEX">ER-funktionen INDEX</a>

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

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="example-1"></a>Eksempel 1

Hvis du angiver datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `DS.Value` tekstværdien **"B"** for den anden post på denne postliste. Udtrykket `INDEX (SPLIT ("A|B|C", "|"), 2).Value` returnerer også tekstværdien **"B"**.

## <a name="example-2"></a>Eksempel 2

Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, udløser udtrykket `INDEX (SPLIT ("A|B|C", "|"), 4).Value` en undtagelse under kørslen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
