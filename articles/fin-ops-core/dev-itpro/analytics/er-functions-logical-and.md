---
title: ER-funktionen AND
description: Dette emne indeholder oplysninger om, hvordan funktionen AND til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041808"
---
# <a name="AND">ER-funktionen AND</a>

[!include [banner](../includes/banner.md)]

Funktionen `AND` returnerer en *Boolesk* værdi som værende **SAND**, hvis alle de angivne betingelser er opfyldte. Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenter

`condition 1`: *Boolesk*

Et gyldigt betinget udtryk, der skal afprøves. Dette argument skal udfyldes.

`condition N`: *Boolesk*

Et gyldigt betinget udtryk, der skal afprøves. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

I argumenterne for logiske funktioner kan du bruge datakildereferencer, numeriske værdier og tekstværdien, Boolesk værdier, sammenligningsoperatorer samt andre funktioner til elektronisk rapportering (ER). Alle argumenterne skal dog evalueres til en *Boolesk* værdi af **SANDT** eller **FALSK**.

## <a name="example"></a>Eksempel

`AND (1=1, "a"="a")` returnerer **SANDT**.

`AND (1=2, "a"="a")` returnerer **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
