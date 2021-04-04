---
title: ER-funktionen NUMBERVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561416"
---
# <a name="numbervalue-er-function"></a>ER-funktionen NUMBERVALUE

[!include [banner](../includes/banner.md)]

Funktionen `NUMBERVALUE` returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi. Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.

## <a name="syntax"></a>Syntaks

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstværdi, der skal konverteres til et *Reelt* tal.

`decimal separator`: Streng

En decimalseparator. Det bruges til at adskille heltal og brøkdele af et decimaltal.

`digit grouping separator`: *Streng*

En ciffergrupperingsseparator. Det bruges som tusindtalsseparator.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="example"></a>Eksempel

`NUMBERVALUE( "1 234,56", ",", " ")` returnerer **1234,56**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Typekonverteringsfunktioner](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]