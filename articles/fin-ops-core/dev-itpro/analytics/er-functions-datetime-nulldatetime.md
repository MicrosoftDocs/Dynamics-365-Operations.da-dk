---
title: ER-funktionen NULLDATETIME
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLDATETIME til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 79bdcaa90ce4002d92a4a0d959c9b94d8c47d7c7c855584d49818fb713bda4b7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745228"
---
# <a name="nulldatetime-er-function"></a>ER-funktionen NULLDATETIME

[!include [banner](../includes/banner.md)]

Funktionen `NULLDATETIME` returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato-/klokkeslætsværdien **nul** (1. januar 1900) i UTC-tid (Coordinated Universal Time) (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaks

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Returnerede værdier

*DateTime*

Den returnerede dato-/klokkeslætsværdi.

## <a name="example"></a>Eksempel

`DATETIMEFORMAT( NULLDATETIME(), "O")` returnerer strengværdien **1900-01-01T00:00:00.0000000+00:00**, når den kaldes under en proces, der blev initieret af en programbruger, der har tidszoneværdien **(GMT) UTC-tid (Coordinated Universal Time)** i afsnittet **Sprog og land/område-præferencer**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]