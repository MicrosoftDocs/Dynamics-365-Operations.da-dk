---
title: ER-funktionen CURCREDREF
description: Dette emne indeholder oplysninger om, hvordan funktionen CURCREDREF til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567610"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="461d2-103">ER-funktionen CURCREDREF</span><span class="sxs-lookup"><span data-stu-id="461d2-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="461d2-104">Funktionen `CURCREDREF` returnerer en *Streng*-værdi, som repræsenterer en kreditorreference, der er baseret på cifrene i det angivne fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="461d2-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="461d2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="461d2-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="461d2-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="461d2-106">Arguments</span></span>

<span data-ttu-id="461d2-107">`invoice number digits`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="461d2-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="461d2-108">En tekstværdi, der repræsenterer cifrene i et fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="461d2-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="461d2-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="461d2-109">Return values</span></span>

<span data-ttu-id="461d2-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="461d2-110">*String*</span></span>

<span data-ttu-id="461d2-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="461d2-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="461d2-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="461d2-112">Example</span></span>

<span data-ttu-id="461d2-113">`CURCredRef ("VEND-200002")` returnerer **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="461d2-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="461d2-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="461d2-114">Additional resources</span></span>

[<span data-ttu-id="461d2-115">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="461d2-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]