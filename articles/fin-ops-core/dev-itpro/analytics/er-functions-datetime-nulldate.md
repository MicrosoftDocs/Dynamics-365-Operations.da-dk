---
title: ER-funktionen NULLDATE
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLDATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746837"
---
# <a name="nulldate-er-function"></a>ER-funktionen NULLDATE

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]