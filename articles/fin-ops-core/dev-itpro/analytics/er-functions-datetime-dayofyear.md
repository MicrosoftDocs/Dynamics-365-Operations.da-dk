---
title: ER-funktionen DAYOFYEAR
description: Dette emne indeholder oplysninger om, hvordan funktionen DAYOFYEAR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746909"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="074fd-103">ER-funktionen DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="074fd-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="074fd-104">Funktionen `DAYOFYEAR` returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem 1. januar og den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="074fd-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="074fd-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="074fd-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="074fd-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="074fd-106">Arguments</span></span>

<span data-ttu-id="074fd-107">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="074fd-107">`date`: *Date*</span></span>

<span data-ttu-id="074fd-108">En datoværdi, som repræsenterer den dato, der skal bruges til beregning af antallet af dage.</span><span class="sxs-lookup"><span data-stu-id="074fd-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="074fd-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="074fd-109">Return values</span></span>

<span data-ttu-id="074fd-110">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="074fd-110">*Integer*</span></span>

<span data-ttu-id="074fd-111">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="074fd-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="074fd-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="074fd-112">Example 1</span></span>

<span data-ttu-id="074fd-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returnerer **61**.</span><span class="sxs-lookup"><span data-stu-id="074fd-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="074fd-114">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="074fd-114">Example 2</span></span>

<span data-ttu-id="074fd-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="074fd-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="074fd-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="074fd-116">Additional resources</span></span>

[<span data-ttu-id="074fd-117">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="074fd-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]