---
title: ER-funktionen MOD_97
description: Dette emne indeholder oplysninger om, hvordan funktionen MOD_97 til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: b58e06a034fc6d26c891b78c26ac53c87a39b92b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744041"
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
