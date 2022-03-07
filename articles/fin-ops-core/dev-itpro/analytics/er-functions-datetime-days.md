---
title: ER-funktionen DAYS
description: Dette emne indeholder oplysninger om, hvordan funktionen DAYS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0252a68aebaa9af95de561b88ceb0666b3460d79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563480"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]