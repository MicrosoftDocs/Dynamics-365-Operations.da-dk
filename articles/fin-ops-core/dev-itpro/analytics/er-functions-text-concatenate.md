---
title: ER-funktionen CONCATENATE
description: Denne artikel indeholder oplysninger om, hvordan funktionen CONCATENATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 926c3acf92fc8017c3c4a7814855a6871c1cacc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863258"
---
# <a name="concatenate-er-function"></a>ER-funktionen CONCATENATE

[!include [banner](../includes/banner.md)]

Funktionen `CONCATENATE` returnerer alle de angivne tekststrenge som en *Streng*-værdi, når de er blevet sammenkædet i en streng.

## <a name="syntax"></a>Syntaks

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumenter

`text 1`: *Streng*

En reference til en datakilde af datatypen *Streng*. Dette argument skal udfyldes.

`text N`: *Streng*

En reference til en datakilde af datatypen *Streng*. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.

## <a name="usage-notes"></a>Bemærkninger til brug

Udtrykket `"abc" & "def"` returnerer også **"abcdef"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]