---
title: ER-funktionen CHAR
description: Dette emne indeholder oplysninger om, hvordan funktionen CHAR til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744955"
---
# <a name="char-er-function"></a>ER-funktionen CHAR

[!include [banner](../includes/banner.md)]

Funktionen `CHAR` returnerer en *Streng*-værdi, som er udtryk for et enkelt tegn, der refereres til af det angivne Unicode-nummer.

## <a name="syntax"></a>Syntaks

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltal*

Et tal, der svarer til et forventet enkelt tegn.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Den streng, som denne funktion returnerer, afhænger af den kodning, der er valgt i det overordnede **FIL**-formatelement. Du kan finde en liste over understøttede kodninger under [Kodningsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Eksempel

`CHAR (255)` returnerer **"ÿ"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
