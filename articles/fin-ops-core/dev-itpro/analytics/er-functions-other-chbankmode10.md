---
title: ER-funktionen CH_BANK_MOD_10
description: Dette emne indeholder oplysninger om, hvordan funktionen CH_BANK_MOD_10 til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d634f074338831c9c767697a8b6d782289f43b0f4d4a33ea4d29f81f7d71f111
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719387"
---
# <a name="ch_bank_mod_10-er-function"></a>ER-funktionen CH_BANK_MOD_10

[!include [banner](../includes/banner.md)]

Funktionen `CH_BANK_MOD_10` returnerer en *Streng*-værdi, som repræsenterer en kreditorreference som et MOD10-udtryk, der er baseret på cifrene i det angivne fakturanummer.

## <a name="syntax"></a>Syntaks

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumenter

`invoice number digits`: *Streng*

En tekstværdi, der repræsenterer cifrene i et fakturanummer.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`CH_BANK_MOD_10 ("VEND-200002")` returnerer **3**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]