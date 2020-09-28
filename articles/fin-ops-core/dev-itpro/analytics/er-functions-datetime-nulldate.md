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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744281"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="ad6bc-103">ER-funktionen NULLDATE</span><span class="sxs-lookup"><span data-stu-id="ad6bc-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad6bc-104">Funktionen `NULLDATE` returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="ad6bc-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6bc-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ad6bc-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="ad6bc-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="ad6bc-106">Return values</span></span>

<span data-ttu-id="ad6bc-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="ad6bc-107">*Date*</span></span>

<span data-ttu-id="ad6bc-108">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="ad6bc-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ad6bc-109">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="ad6bc-109">Example 1</span></span>

<span data-ttu-id="ad6bc-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer datoen **nul**, 1. januar 1900, som **"1900-01-01"** baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="ad6bc-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ad6bc-111">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="ad6bc-111">Example 2</span></span>

<span data-ttu-id="ad6bc-112">Udtrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sandt**, når værdien i feltet **Dokumentdato** er lig med **nul**-datoen.</span><span class="sxs-lookup"><span data-stu-id="ad6bc-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="ad6bc-113">I dette eksempel er **Faktura** en datakilde til elektronisk rapportering (ER) af typen **Finance/Table-poster** og refererer til tabellen CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="ad6bc-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad6bc-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ad6bc-114">Additional resources</span></span>

[<span data-ttu-id="ad6bc-115">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="ad6bc-115">Date and time functions</span></span>](er-functions-category-datetime.md)
