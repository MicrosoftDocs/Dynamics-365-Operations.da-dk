---
title: ER-funktionen INTVALUE
description: Denne artikel indeholder oplysninger om, hvordan funktionen INTVALUE til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282615"
---
# <a name="intvalue-er-function"></a>ER-funktionen INTVALUE

[!include [banner](../includes/banner.md)]

Funktionen `INTVALUE` returnerer en *Int*-værdi, der repræsenterer den angivne streng.

## <a name="syntax-1"></a>Syntaks 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstværdi, der skal konverteres til et *Int*-tal.

`number`: *Reel* eller *Heltal*

En numerisk *Reel* værdi eller *Heltals*-værdi, der skal konverteres til et *Int*-tal.

## <a name="return-values"></a>Returnerede værdier

*Int*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Eventuelle decimalpladser afkortes.

## <a name="example-1"></a>Eksempel 1

`INTVALUE ("100.77")` returnerer værdien *Int* **100**.

## <a name="example-2"></a>Eksempel 2

`INTVALUE (-100.77)` returnerer værdien *Int* **-100**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Typekonverteringsfunktioner](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
