---
title: ER-funktionen NUMBERFORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMBERFORMAT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070546"
---
# <a name="NUMBERFORMAT">ER-funktionen NUMBERFORMAT</a>

[!include [banner](../includes/banner.md)]

Funktionen `NUMBERFORMAT` returnerer en *Streng*-værdi, som præsenterer det angivne tal i det angivne format og i en eventuelt angivet [kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntaks 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltal* eller *Reel*

En numerisk værdi, der angiver det tal, der skal formateres.

`format`: *Streng*

En *Streng*-værdi, der repræsenterer formatet.

`culture`: *Streng*

En *Streng*-værdi, som repræsenterer den kultur, der skal bruges til formatering.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis kulturen ikke er defineret som et argument for den kaldte funktion, bestemmer den kontekst, som denne funktion køres i, den kultur, der bruges til at formatere tal.

## <a name="example-1"></a>Eksempel 1

For kulturen **EN-US** returnerer `NUMBERFORMAT (0.45, "p")` **"45,00 %"**, og `NUMBERFORMAT (10.45, "#")` returner **"10"**.

## <a name="example-2"></a>Eksempel 2

`NUMBERFORMAT (10/3, "F2", "de")` returnerer **3.33**, mens `NUMBERFORMAT (10/3, "F2", "en-us")` returnerer **3,33**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
