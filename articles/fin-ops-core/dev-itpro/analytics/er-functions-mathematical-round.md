---
title: ER-funktionen ROUND
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUND til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683250"
---
# <a name="round-er-function"></a><span data-ttu-id="14587-103">ER-funktionen ROUND</span><span class="sxs-lookup"><span data-stu-id="14587-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14587-104">Funktionen `ROUND` returnerer det angivne tal som en *Reel* værdi, når det er afrundet til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="14587-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="14587-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="14587-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="14587-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="14587-106">Arguments</span></span>

<span data-ttu-id="14587-107">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="14587-107">`number`: *Real*</span></span>

<span data-ttu-id="14587-108">En numerisk værdi, der skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="14587-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="14587-109">`decimals`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="14587-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="14587-110">En numerisk værdi, der repræsenterer antallet af decimaler.</span><span class="sxs-lookup"><span data-stu-id="14587-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="14587-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="14587-111">Return values</span></span>

<span data-ttu-id="14587-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="14587-112">*Real*</span></span>

<span data-ttu-id="14587-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="14587-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14587-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="14587-114">Usage notes</span></span>

<span data-ttu-id="14587-115">Hvis værdien for argumentet `decimals` er større end 0 (nul), afrundes det angivne tal til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="14587-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="14587-116">Hvis værdien for argumentet `decimals` er **0** (nul), afrundes det angivne tal til det nærmeste lige heltal.</span><span class="sxs-lookup"><span data-stu-id="14587-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="14587-117">Hvis værdien af argumentet `decimals` er mindre end 0 (nul), afrundes det angivne tal mod venstre til decimalpunktet.</span><span class="sxs-lookup"><span data-stu-id="14587-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="14587-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="14587-118">Example 1</span></span>

<span data-ttu-id="14587-119">`ROUND (1200.767, 2)` afrunder til to decimaler og returnerer **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="14587-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="14587-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="14587-120">Example 2</span></span>

<span data-ttu-id="14587-121">`ROUND (1200.767, -3)` afrunder til det nærmeste multiplum af 1.000 og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="14587-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="14587-122">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="14587-122">Example 3</span></span>

<span data-ttu-id="14587-123">`ROUND (1200.5, 0)` afrundes til det nærmeste lige heltal og returnerer **1200**, mens `ROUND (1201.5, 0)` gør har samme og returnerer **1202**.</span><span class="sxs-lookup"><span data-stu-id="14587-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14587-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="14587-124">Additional resources</span></span>

[<span data-ttu-id="14587-125">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="14587-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)
