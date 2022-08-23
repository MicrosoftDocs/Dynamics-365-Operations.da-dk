---
title: ER-funktionen NEWGUID
description: Denne artikel indeholder oplysninger om, hvordan funktionen NEWGUID til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274766"
---
# <a name="newguid-er-function"></a>ER-funktionen NEWGUID

[!include [banner](../includes/banner.md)]

Funktionen `NEWGUID` genererer et nyt globalt entydigt id (GUID - Globally Unique Identifier) og returnerer det som en *[GUID](er-formula-supported-data-types-primitive.md#guid)*-værdi.

## <a name="syntax"></a>Syntaks

```vb
NEWGUID ()
```

## <a name="return-values"></a>Returnerede værdier

*GUID*

Den returnerede GUID-værdi.

## <a name="example"></a>Eksempel

`NEWGUID()` returnerer altid en ny *GUID*-værdi, f.eks. **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
