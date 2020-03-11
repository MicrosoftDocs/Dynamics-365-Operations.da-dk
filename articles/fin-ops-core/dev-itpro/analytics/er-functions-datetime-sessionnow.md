---
title: ER-funktionen SESSIONNOW
description: Dette emne indeholder oplysninger om, hvordan funktionen SESSIONNOW til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 5489fab61791654c2e583fc11b27aba09fb90c86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042291"
---
# <a name="">ER-funktionen SESSIONNOW</a>

[!include [banner](../includes/banner.md)]

Funktionen `SESSIONNOW` returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato og klokkeslæt for den aktuelle programsession.

## <a name="syntax"></a>Syntaks

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Returnerede værdier

*DateTime*

Den returnerede dato-/klokkeslætsværdi.

## <a name="example"></a>Eksempel

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer datoen/klokkeslættet for den aktuelle programsession, 24. december 2015, som strengen **"24.12.2015"**, baseret på den valgte tyske kultur og det angivne format.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)
