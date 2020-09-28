---
title: ER-funktionen ROUND
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUND til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744545"
---
# <a name="round-er-function"></a><span data-ttu-id="b1f3f-103">ER-funktionen ROUND</span><span class="sxs-lookup"><span data-stu-id="b1f3f-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1f3f-104">Funktionen `ROUND` returnerer det angivne tal som en *Reel* værdi, når det er afrundet til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f3f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b1f3f-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="b1f3f-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b1f3f-106">Arguments</span></span>

<span data-ttu-id="b1f3f-107">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="b1f3f-107">`number`: *Real*</span></span>

<span data-ttu-id="b1f3f-108">En numerisk værdi, der skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="b1f3f-109">`decimals`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="b1f3f-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="b1f3f-110">En numerisk værdi, der repræsenterer antallet af decimaler.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1f3f-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="b1f3f-111">Return values</span></span>

<span data-ttu-id="b1f3f-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="b1f3f-112">*Real*</span></span>

<span data-ttu-id="b1f3f-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1f3f-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="b1f3f-114">Usage notes</span></span>

<span data-ttu-id="b1f3f-115">Hvis værdien for argumentet `decimals` er større end 0 (nul), afrundes det angivne tal til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="b1f3f-116">Hvis værdien for argumentet `decimals` er **0** (nul), afrundes det angivne tal til det nærmeste heltal.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="b1f3f-117">Hvis værdien af argumentet `decimals` er mindre end 0 (nul), afrundes det angivne tal mod venstre til decimalpunktet.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="b1f3f-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b1f3f-118">Example 1</span></span>

<span data-ttu-id="b1f3f-119">`ROUND (1200.767, 2)` afrunder til to decimaler og returnerer **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b1f3f-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b1f3f-120">Example 2</span></span>

<span data-ttu-id="b1f3f-121">`ROUND (1200.767, -3)` afrunder til det nærmeste multiplum af 1.000 og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="b1f3f-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1f3f-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b1f3f-122">Additional resources</span></span>

[<span data-ttu-id="b1f3f-123">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="b1f3f-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
