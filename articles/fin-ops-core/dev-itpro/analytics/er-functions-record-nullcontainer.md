---
title: ER-funktionen NULLCONTAINER
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLCONTAINER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746501"
---
# <a name="nullcontainer-er-function"></a>ER-funktionen NULLCONTAINER

[!include [banner](../includes/banner.md)]

Funktionen `NULLCONTAINER` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.

## <a name="syntax"></a>Syntaks

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]