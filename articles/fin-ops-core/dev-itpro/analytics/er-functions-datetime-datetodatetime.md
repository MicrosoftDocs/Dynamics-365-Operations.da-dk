---
title: ER-funktionen DATETODATETIME
description: Dette emne indeholder oplysninger om, hvordan funktionen DATETODATETIME til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916378"
---
# <a name="DATETODATETIME">ER-funktionen DATETODATETIME</a>

[!include [banner](../includes/banner.md)]

Funktionen `DATETODATETIME` returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given datoværdi til en dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Syntaks

```
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenter

`date`: *Dato*

En datoværdi, der repræsenterer den dato, der skal konverteres.

## <a name="return-values"></a>Returnerede værdier

*DateTime*

Den returnerede dato-/klokkeslætsværdi.

## <a name="example-1"></a>Eksempel 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` returnerer datoen for den aktuelle Microsoft Dynamics 365 Finance-session, 24. december 2015, som **24/12/2015 12:00:00**. I dette eksempel er **CompInfo** en datakilde til elektronisk rapportering (ER) af typen **Finance and Operations/tabel** og refererer til tabellen CompanyInfo.

## <a name="example-2"></a>Eksempel 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returnerer dato-/klokkeslætsværdien **12/11/2019 12:00:00**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)