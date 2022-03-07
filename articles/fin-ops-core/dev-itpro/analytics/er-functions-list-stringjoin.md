---
title: ER-funktionen STRINGJOIN
description: Dette emne indeholder oplysninger om, hvordan funktionen STRINGJOIN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 651cc261e6a33b1a824feb94afa767e439196e249bb13b0fc4886dc72bfdd184
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776092"
---
# <a name="stringjoin-er-function"></a>ER-funktionen STRINGJOIN

[!include [banner](../includes/banner.md)]

Funktionen `STRINGJOIN` returnerer en *Streng*-værdi, der består af sammenføjede værdier for det angivne felt fra den angivne liste. Værdierne kan være adskilt af et angivet separatortegn.

## <a name="syntax"></a>Syntaks

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`field`: *Felt*

Den gyldige sti til et felt af datatypen *Streng* på den angivne liste.

`delimiter`: *Streng*

En afgrænser, der bruges til at adskille understrenge.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

Hvis du indtaster `SPLIT("abc" , 1)` som datakilde **DS**, returnerer udtrykket `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]