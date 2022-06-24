---
title: ER-funktionen NOT
description: Denne artikel indeholder oplysninger om, hvordan funktionen NOT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da30e9a0092f594da7cef7b425e2b89af7bda491
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890479"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]