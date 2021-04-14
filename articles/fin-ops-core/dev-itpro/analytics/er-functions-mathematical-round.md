---
title: ER-funktionen ROUND
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUND til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744481"
---
# <a name="round-er-function"></a><span data-ttu-id="063dc-103">ER-funktionen ROUND</span><span class="sxs-lookup"><span data-stu-id="063dc-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="063dc-104">Funktionen `ROUND` returnerer det angivne tal som en *Reel* værdi, når det er afrundet til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="063dc-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="063dc-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="063dc-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="063dc-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="063dc-106">Arguments</span></span>

<span data-ttu-id="063dc-107">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="063dc-107">`number`: *Real*</span></span>

<span data-ttu-id="063dc-108">En numerisk værdi, der skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="063dc-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="063dc-109">`decimals`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="063dc-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="063dc-110">En numerisk værdi, der repræsenterer antallet af decimaler.</span><span class="sxs-lookup"><span data-stu-id="063dc-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="063dc-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="063dc-111">Return values</span></span>

<span data-ttu-id="063dc-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="063dc-112">*Real*</span></span>

<span data-ttu-id="063dc-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="063dc-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="063dc-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="063dc-114">Usage notes</span></span>

<span data-ttu-id="063dc-115">Hvis værdien for argumentet `decimals` er større end 0 (nul), afrundes det angivne tal til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="063dc-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="063dc-116">Hvis værdien for argumentet `decimals` er **0** (nul), afrundes det angivne tal til det nærmeste lige heltal.</span><span class="sxs-lookup"><span data-stu-id="063dc-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="063dc-117">Hvis værdien af argumentet `decimals` er mindre end 0 (nul), afrundes det angivne tal mod venstre til decimalpunktet.</span><span class="sxs-lookup"><span data-stu-id="063dc-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="063dc-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="063dc-118">Example 1</span></span>

<span data-ttu-id="063dc-119">`ROUND (1200.767, 2)` afrunder til to decimaler og returnerer **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="063dc-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="063dc-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="063dc-120">Example 2</span></span>

<span data-ttu-id="063dc-121">`ROUND (1200.767, -3)` afrunder til det nærmeste multiplum af 1.000 og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="063dc-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="063dc-122">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="063dc-122">Example 3</span></span>

<span data-ttu-id="063dc-123">`ROUND (1200.5, 0)` afrundes til det nærmeste lige heltal og returnerer **1200**, mens `ROUND (1201.5, 0)` gør har samme og returnerer **1202**.</span><span class="sxs-lookup"><span data-stu-id="063dc-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="063dc-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="063dc-124">Additional resources</span></span>

[<span data-ttu-id="063dc-125">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="063dc-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]