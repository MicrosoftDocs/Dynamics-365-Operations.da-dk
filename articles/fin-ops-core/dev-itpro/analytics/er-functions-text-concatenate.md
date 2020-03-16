---
title: ER-funktionen CONCATENATE
description: Dette emne indeholder oplysninger om, hvordan funktionen CONCATENATE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 04c7b32e2a9578f8864570a552817ec3ce28fa43
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041148"
---
# <a name="CONCATENATE">ER-funktionen CONCATENATE</a>

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
