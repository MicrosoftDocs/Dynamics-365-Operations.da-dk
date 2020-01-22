---
title: ER-funktionen OR
description: Dette emne indeholder oplysninger om, hvordan funktionen OR til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917114"
---
# <a name="OR">ER-funktionen OR</a>

[!include [banner](../includes/banner.md)]

Funktionen `OR` returnerer en *Boolesk* værdi som værende **FALSK**, hvis alle de angivne betingelser ikke er opfyldte. Hvis en eller flere af de angivne betingelser er opfyldte, returnerer denne funktion en *Boolesk* værdi som værende **SAND**.

## <a name="syntax"></a>Syntaks

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenter

`condition 1`: *Boolesk*

Et gyldigt betinget udtryk, der skal afprøves. Dette argument skal udfyldes.

`condition N`: *Boolesk*

Et gyldigt betinget udtryk, der skal afprøves. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="example"></a>Eksempel

`OR (1=2, "a"="a")` returnerer **SANDT**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
