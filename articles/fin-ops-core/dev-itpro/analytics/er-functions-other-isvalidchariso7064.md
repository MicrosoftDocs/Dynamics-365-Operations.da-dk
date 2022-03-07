---
title: ER-funktionen ISVALIDCHARACTERISO7064
description: Dette emne indeholder oplysninger om, hvordan funktionen ISVALIDCHARACTERISO7064 til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 884fbf7371ea9d9ac931655f8b11ec1e13c83a46aaa831c96f5d558209205e09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763566"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]