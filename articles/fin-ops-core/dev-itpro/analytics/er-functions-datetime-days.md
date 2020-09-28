---
title: ER-funktionen DAYS
description: Dette emne indeholder oplysninger om, hvordan funktionen DAYS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743561"
---
# <a name="days-er-function"></a>ER-funktionen DAYS

[!include [banner](../includes/banner.md)]

Funktionen `DAYS` returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem to angivne datoer.

## <a name="syntax"></a>Syntaks

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumenter

`date 1`: *Dato*

En datoværdi, som repræsenterer den startdato, der skal bruges til beregning af antallet af dage.

`date 2`: *Dato*

En datoværdi, som repræsenterer den slutdato, der skal bruges til beregning af antallet af dage.

## <a name="return-values"></a>Returnerede værdier

*Heltal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Funktionen `DAYS` returnerer en positiv værdi, når den første dato er senere end den anden dato; den returnerer **0** (nul), når den første dato er lig med den anden dato, og den returnerer en negativ værdi, når den første date er før den anden dato.

## <a name="example"></a>Eksempel

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returnerer **-1**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)
