---
title: ER-funktionen INT64VALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen INT64VALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686044"
---
# <a name="int64value-er-function"></a>ER-funktionen INT64VALUE

[!include [banner](../includes/banner.md)]

Funktionen `INT64VALUE` returnerer en *Int64*-værdi, der repræsenterer den angivne streng.

## <a name="syntax-1"></a>Syntaks 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstværdi, der skal konverteres til et *Int64*-tal.

`number`: *Reel* eller *Heltal*

En numerisk *Reel* værdi eller *Heltals*-værdi, der skal konverteres til et *Int64*-tal.

## <a name="return-values"></a>Returnerede værdier

*Int64*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Eventuelle decimalpladser afkortes.

## <a name="example-1"></a>Eksempel 1

`INT64VALUE ("22565422744")` returnerer værdien *Int64* **22565422744**.

## <a name="example-2"></a>Eksempel 2

`INT64VALUE ( VALUE("22565422744.77"))` returnerer værdien *Int64* **22565422744**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Typekonverteringsfunktioner](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]