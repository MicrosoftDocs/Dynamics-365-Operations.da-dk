---
title: ER-funktionen ISVALIDCHARACTERISO7064
description: Dette emne indeholder oplysninger om, hvordan funktionen ISVALIDCHARACTERISO7064 til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680656"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ER-funktionen ISVALIDCHARACTERISO7064

[!include [banner](../includes/banner.md)]

Funktionen `ISVALIDCHARACTERISO7064` returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN). Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstværdi, der repræsenterer et IBAN.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returnerer **SANDT**. 

`ISVALIDCHARACTERISO7064 ("AT61")` returnerer **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)
