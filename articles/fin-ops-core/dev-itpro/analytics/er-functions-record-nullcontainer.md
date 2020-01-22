---
title: ER-funktionen NULLCONTAINER
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLCONTAINER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915780"
---
# <a name="NULLCONTAINER">ER-funktionen NULLCONTAINER</a>

[!include [banner](../includes/banner.md)]

Funktionen `NULLCONTAINER` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.

## <a name="syntax"></a>Syntaks

```
NULLCONTAINER (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste* eller *Container (post)*

En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

> [!NOTE] 
> Denne funktion er forældet. Brug `EMPTYRECORD`-funktionen i stedet. Yderligere oplysninger finder du under [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Eksempel

`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion. Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Postfunktioner](er-functions-category-record.md)
