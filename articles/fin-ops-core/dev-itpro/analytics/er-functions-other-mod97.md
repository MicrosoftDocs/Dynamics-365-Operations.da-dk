---
title: ER-funktionen MOD_97
description: Dette emne indeholder oplysninger om, hvordan funktionen MOD_97 til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: edc29cac14014929e0672183be1c5db44fe6b5afe9543cd00942a95c79ec8897
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734762"
---
# <a name="mod_97-er-function"></a>ER-funktionen MOD_97

[!include [banner](../includes/banner.md)]

Funktionen `MOD_97` returnerer en *Streng*-værdi, som repræsenterer en kreditorreference som et MOD97-udtryk, der er baseret på cifrene i det angivne fakturanummer.

## <a name="syntax"></a>Syntaks

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumenter

`invoice number digits`: *Streng*

En tekstværdi, der repræsenterer cifrene i et fakturanummer.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`MOD_97 ("VEND-200002")` returnerer **"20000285"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]