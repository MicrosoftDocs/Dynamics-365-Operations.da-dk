---
title: ER-funktionen NULLDATE
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLDATE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 24a295a6ad8aca7718e60dd351248c9fbfdafee8
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042314"
---
# <a name="NULLDATE">ER-funktionen NULLDATE</a>

[!include [banner](../includes/banner.md)]

Funktionen `NULLDATE` returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900).

## <a name="syntax"></a>Syntaks

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Returnerede værdier

*Dato*

Den returnerede datoværdi.

## <a name="example-1"></a>Eksempel 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer datoen **nul**, 1. januar 1900, som **"1900-01-01"** baseret på det angivne brugerdefinerede format.

## <a name="example-2"></a>Eksempel 2

Udtrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sandt**, når værdien i feltet **Dokumentdato** er lig med **nul**-datoen. I dette eksempel er **Faktura** en datakilde til elektronisk rapportering (ER) af typen **Finance/Table-poster** og refererer til tabellen CustInvoiceJour.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)
