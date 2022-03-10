---
title: ER-funktionen TODAY
description: Dette emne indeholder oplysninger om, hvordan funktionen TODAY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 12c4489751e9e0c06d4b628e7c297eee472054369f7cfacee048622cbc39d074
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755820"
---
# <a name="today-er-function"></a>ER-funktionen TODAY

[!include [banner](../includes/banner.md)]

Funktionen `TODAY` returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programserver.

## <a name="syntax"></a>Syntaks

```xpp
TODAY ()
```

## <a name="return-values"></a>Returnerede værdier

*Dato*

Den returnerede datoværdi.

## <a name="example"></a>Eksempel

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returnerer den aktuelle dato-/klokkeslætsværdi på programserver, 24. december 2015, som strengen **"24-12-2015"**, baseret på det angivne brugerdefinerede format.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]