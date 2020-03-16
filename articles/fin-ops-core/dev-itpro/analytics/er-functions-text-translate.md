---
title: ER-funktionen TRANSLATE
description: Dette emne indeholder oplysninger om, hvordan funktionen TRANSLATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040911"
---
# <a name="TRANSLATE">ER-funktionen TRANSLATE</a>

[!include [banner](../includes/banner.md)]

Funktionen `TRANSLATE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.

## <a name="syntax"></a>Syntaks

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

`pattern`: *Streng*

Den tekst, der skal erstattes.

`replacement`: *Streng*

Den tekst, der skal bruges som erstatning.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`TRANSLATE ("abcdef", "cd", "GH")` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
