---
title: ER-funktionen EMPTYRECORD
description: Denne artikel indeholder oplysninger om, hvordan funktionen EMPTYRECORD til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280149"
---
# <a name="emptyrecord-er-function"></a>ER-funktionen EMPTYRECORD

[!include [banner](../includes/banner.md)]

Funktionen `EMPTYRECORD` returnerer en nulværdi for *Container (post)*, som har samme struktur, som den angivne postliste eller post.

## <a name="syntax"></a>Syntaks

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
