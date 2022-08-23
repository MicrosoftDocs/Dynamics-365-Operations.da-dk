---
title: ER-funktionen DATETODATETIME
description: Denne artikel indeholder oplysninger om, hvordan funktionen DATETODATETIME til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287302"
---
# <a name="datetodatetime-er-function"></a>ER-funktionen DATETODATETIME

[!include [banner](../includes/banner.md)]

Funktionen `DATETODATETIME` returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given datoværdi til en dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaks

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoværdi, der repræsenterer den dato, der skal konverteres.

## <a name="return-values"></a>Returnerede værdier

*DateTime*

Den returnerede dato-/klokkeslætsværdi.

## <a name="example-1"></a>Eksempel 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` returnerer datoen for den aktuelle Microsoft Dynamics 365 Finance-session, 24. december 2015, som **24/12/2015 12:00:00**. I dette eksempel er **CompInfo** en datakilde til elektronisk rapportering (ER) af typen **finans og drift/tabel** og refererer til tabellen CompanyInfo.

## <a name="example-2"></a>Eksempel 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returnerer dato-/klokkeslætsværdien **12/11/2019 12:00:00**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
