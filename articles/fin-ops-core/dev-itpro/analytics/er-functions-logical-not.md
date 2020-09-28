---
title: ER-funktionen NOT
description: Dette emne indeholder oplysninger om, hvordan funktionen NOT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744641"
---
# <a name="not-er-function"></a>ER-funktionen NOT

[!include [banner](../includes/banner.md)]

Funktionen `NOT` returnerer den omvendte logiske værdi af den angivne betingelse som en *Boolesk* værdi.

## <a name="syntax"></a>Syntaks

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumenter

`condition`: *Boolesk*

Et gyldigt betinget udtryk, der skal tilbageføres.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="example"></a>Eksempel

`NOT (TRUE)` returnerer **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
