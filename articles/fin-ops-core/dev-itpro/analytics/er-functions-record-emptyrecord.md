---
title: ER-funktionen EMPTYRECORD
description: Dette emne indeholder oplysninger om, hvordan funktionen EMPTYRECORD til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916884"
---
# <a name="EMPTYRECORD">ER-funktionen EMPTYRECORD</a>

[!include [banner](../includes/banner.md)]

Funktionen `EMPTYRECORD` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.

## <a name="syntax"></a>Syntaks

```
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste* eller *Container (post)*

En datakildes gyldig sti af typen *Postliste* eller *Container (post)*.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

> [!NOTE] 
> En null-post er en post, hvor alle felter har en tom værdi. En tom værdi er **0** (nul) for tal, en tom streng for strenge, osv.

## <a name="example"></a>Eksempel

`EMPTYRECORD (SPLIT ("abc", 1))` returnerer en ny tom post, der har samme struktur som den liste, der er returneret af den anvendte `SPLIT`-funktion. Yderligere oplysninger finder du under [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Postfunktioner](er-functions-category-record.md)
