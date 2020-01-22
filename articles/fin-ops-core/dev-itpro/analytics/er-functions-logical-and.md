---
title: ER-funktionen AND
description: Dette emne indeholder oplysninger om, hvordan funktionen AND til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917160"
---
# <span data-ttu-id="90903-103"><a name="AND">ER-funktionen AND</a></span><span class="sxs-lookup"><span data-stu-id="90903-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90903-104">Funktionen `AND` returnerer en *Boolesk* værdi som værende **SAND**, hvis alle de angivne betingelser er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="90903-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="90903-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="90903-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="90903-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="90903-106">Syntax</span></span>

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="90903-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="90903-107">Arguments</span></span>

<span data-ttu-id="90903-108">`condition 1`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="90903-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="90903-109">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="90903-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="90903-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="90903-110">This argument is required.</span></span>

<span data-ttu-id="90903-111">`condition N`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="90903-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="90903-112">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="90903-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="90903-113">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="90903-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="90903-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="90903-114">Return values</span></span>

<span data-ttu-id="90903-115">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="90903-115">*Boolean*</span></span>

<span data-ttu-id="90903-116">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="90903-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="90903-117">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="90903-117">Usage notes</span></span>

<span data-ttu-id="90903-118">I argumenterne for logiske funktioner kan du bruge datakildereferencer, numeriske værdier og tekstværdien, Boolesk værdier, sammenligningsoperatorer samt andre funktioner til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="90903-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="90903-119">Alle argumenterne skal dog evalueres til en *Boolesk* værdi af **SANDT** eller **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="90903-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="90903-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="90903-120">Example</span></span>

<span data-ttu-id="90903-121">`AND (1=1, "a"="a")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="90903-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="90903-122">`AND (1=2, "a"="a")` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="90903-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90903-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="90903-123">Additional resources</span></span>

[<span data-ttu-id="90903-124">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="90903-124">Logical functions</span></span>](er-functions-category-logical.md)
