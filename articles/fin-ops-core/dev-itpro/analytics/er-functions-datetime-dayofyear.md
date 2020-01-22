---
title: ER-funktionen DAYOFYEAR
description: Dette emne indeholder oplysninger om, hvordan funktionen DAYOFYEAR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916332"
---
# <span data-ttu-id="1d9ea-103"><a name="DAYOFYEAR">ER-funktionen DAYOFYEAR</a></span><span class="sxs-lookup"><span data-stu-id="1d9ea-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d9ea-104">Funktionen `DAYOFYEAR` returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem 1. januar og den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9ea-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1d9ea-105">Syntax</span></span>

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="1d9ea-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1d9ea-106">Arguments</span></span>

<span data-ttu-id="1d9ea-107">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="1d9ea-107">`date`: *Date*</span></span>

<span data-ttu-id="1d9ea-108">En datoværdi, som repræsenterer den dato, der skal bruges til beregning af antallet af dage.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="1d9ea-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="1d9ea-109">Return values</span></span>

<span data-ttu-id="1d9ea-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="1d9ea-110">*Integer*</span></span>

<span data-ttu-id="1d9ea-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="1d9ea-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1d9ea-112">Example 1</span></span>

<span data-ttu-id="1d9ea-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returnerer **61**.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1d9ea-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1d9ea-114">Example 2</span></span>

<span data-ttu-id="1d9ea-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="1d9ea-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d9ea-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1d9ea-116">Additional resources</span></span>

[<span data-ttu-id="1d9ea-117">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="1d9ea-117">Date and time functions</span></span>](er-functions-category-datetime.md)
