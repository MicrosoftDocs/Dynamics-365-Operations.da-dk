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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041222"
---
# <a name="CHAR">ER-funktionen CHAR</a>

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
