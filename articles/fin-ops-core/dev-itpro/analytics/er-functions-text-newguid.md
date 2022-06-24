---
title: ER-funktionen NEWGUID
description: Denne artikel indeholder oplysninger om, hvordan funktionen NEWGUID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861810"
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
