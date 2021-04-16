---
title: ER-funktionen INTVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen INTVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755366"
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