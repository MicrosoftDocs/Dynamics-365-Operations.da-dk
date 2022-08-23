---
title: ER-funktionen FIRST
description: Denne artikel indeholder oplysninger om, hvordan funktionen FIRST til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b06f07c4cfef5c74c22f60dfa37986ee88c544cf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275470"
---
# <a name="first-er-function"></a>ER-funktionen FIRST

[!include [banner](../includes/banner.md)]

Funktionen `FIRST` returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne liste ikke er tom. Hvis listen er tom, udløser denne funktion en undtagelse.

## <a name="syntax"></a>Syntaks

```vb
FIRST (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="example-1"></a>Eksempel 1

Udtrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstværdien **"A"**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `FIRST(SPLIT("",1)).Value` udløser en undtagelse under kørslen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
