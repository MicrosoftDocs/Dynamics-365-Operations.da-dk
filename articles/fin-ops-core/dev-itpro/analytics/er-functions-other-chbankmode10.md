---
title: ER-funktionen CH_BANK_MOD_10
description: Dette emne indeholder oplysninger om, hvordan funktionen CH_BANK_MOD_10 til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915872"
---
# <a name="CH_BANK_MOD_10">ER-funktionen CH_BANK_MOD_10</a>

[!include [banner](../includes/banner.md)]

Funktionen `CH_BANK_MOD_10` returnerer en *Streng*-værdi, som repræsenterer en kreditorreference som et MOD10-udtryk, der er baseret på cifrene i det angivne fakturanummer.

## <a name="syntax"></a>Syntaks

```
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