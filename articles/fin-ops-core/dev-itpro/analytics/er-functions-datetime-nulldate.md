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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916309"
---
# <span data-ttu-id="c3bb1-103"><a name="NULLDATE">ER-funktionen NULLDATE</a></span><span class="sxs-lookup"><span data-stu-id="c3bb1-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3bb1-104">Funktionen `NULLDATE` returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="c3bb1-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3bb1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c3bb1-105">Syntax</span></span>

```
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="c3bb1-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c3bb1-106">Return values</span></span>

<span data-ttu-id="c3bb1-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="c3bb1-107">*Date*</span></span>

<span data-ttu-id="c3bb1-108">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="c3bb1-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c3bb1-109">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="c3bb1-109">Example 1</span></span>

<span data-ttu-id="c3bb1-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer datoen **nul**, 1. januar 1900, som **"1900-01-01"** baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="c3bb1-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="c3bb1-111">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="c3bb1-111">Example 2</span></span>

<span data-ttu-id="c3bb1-112">Udtrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sandt**, når værdien i feltet **Dokumentdato** er lig med **nul**-datoen.</span><span class="sxs-lookup"><span data-stu-id="c3bb1-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="c3bb1-113">I dette eksempel er **Faktura** en datakilde til elektronisk rapportering (ER) af typen **Finance/Table-poster** og refererer til tabellen CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="c3bb1-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3bb1-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c3bb1-114">Additional resources</span></span>

[<span data-ttu-id="c3bb1-115">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="c3bb1-115">Date and time functions</span></span>](er-functions-category-datetime.md)
