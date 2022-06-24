---
title: ER-funktionen ISOCREDREF
description: Denne artikel indeholder oplysninger om, hvordan funktionen ISOCREDREF til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: dcbd53ec1939e6fb4bcd829bad01b353e823795a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896757"
---
# <a name="isocredref-er-function"></a>ER-funktionen ISOCREDREF

[!include [banner](../includes/banner.md)]

Funktionen `ISOCREDREF` returnerer en *Streng*-værdi, som repræsenterer en International Organization for Standardization (ISO)-kreditorreference, der er baseret på cifrene og bogstaverne i det angivne fakturanummer.

## <a name="syntax"></a>Syntaks

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumenter

`invoice number digits`: *Streng*

En tekstværdi, der repræsenterer cifrene i et fakturanummer.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

> [!NOTE] 
> For at eliminere symboler fra alfabeter, der ikke er ISO-kompatible, skal argumentet `invoice number digits` oversættes, før den videresendes til denne funktion.

## <a name="example"></a>Eksempel

`ISOCredRef ("VEND-200002")` returnerer **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]