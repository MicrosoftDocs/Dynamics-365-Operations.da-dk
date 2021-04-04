---
title: ER-funktionen NULLDATE
description: Dette emne indeholder oplysninger om, hvordan funktionen NULLDATE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563456"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="53599-103">ER-funktionen NULLDATE</span><span class="sxs-lookup"><span data-stu-id="53599-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53599-104">Funktionen `NULLDATE` returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="53599-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="53599-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="53599-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="53599-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="53599-106">Return values</span></span>

<span data-ttu-id="53599-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="53599-107">*Date*</span></span>

<span data-ttu-id="53599-108">Den returnerede datoværdi.</span><span class="sxs-lookup"><span data-stu-id="53599-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="53599-109">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="53599-109">Example 1</span></span>

<span data-ttu-id="53599-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer datoen **nul**, 1. januar 1900, som **"1900-01-01"** baseret på det angivne brugerdefinerede format.</span><span class="sxs-lookup"><span data-stu-id="53599-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="53599-111">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="53599-111">Example 2</span></span>

<span data-ttu-id="53599-112">Udtrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sandt**, når værdien i feltet **Dokumentdato** er lig med **nul**-datoen.</span><span class="sxs-lookup"><span data-stu-id="53599-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="53599-113">I dette eksempel er **Faktura** en datakilde til elektronisk rapportering (ER) af typen **Finance/Table-poster** og refererer til tabellen CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="53599-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53599-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="53599-114">Additional resources</span></span>

[<span data-ttu-id="53599-115">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="53599-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]