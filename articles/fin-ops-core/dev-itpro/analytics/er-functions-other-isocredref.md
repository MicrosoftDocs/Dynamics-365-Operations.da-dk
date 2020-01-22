---
title: ER-funktionen ISOCREDREF
description: Dette emne indeholder oplysninger om, hvordan funktionen ISOCREDREF til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916953"
---
# <a name="ISOCREDREF">ER-funktionen ISOCREDREF</a>

[!include [banner](../includes/banner.md)]

Funktionen `ISOCREDREF` returnerer en *Streng*-værdi, som repræsenterer en International Organization for Standardization (ISO)-kreditorreference, der er baseret på cifrene og bogstaverne i det angivne fakturanummer.

## <a name="syntax"></a>Syntaks

```
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
