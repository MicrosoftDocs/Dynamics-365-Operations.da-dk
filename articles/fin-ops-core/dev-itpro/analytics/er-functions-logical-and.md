---
title: ER-funktionen AND
description: Dette emne indeholder oplysninger om, hvordan funktionen AND til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745467"
---
# <a name="and-er-function"></a><span data-ttu-id="fdd69-103">ER-funktionen AND</span><span class="sxs-lookup"><span data-stu-id="fdd69-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdd69-104">Funktionen `AND` returnerer en *Boolesk* værdi som værende **SAND**, hvis alle de angivne betingelser er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="fdd69-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="fdd69-105">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd69-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="fdd69-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="fdd69-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="fdd69-107">Arguments</span></span>

<span data-ttu-id="fdd69-108">`condition 1`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="fdd69-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="fdd69-109">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="fdd69-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="fdd69-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="fdd69-110">This argument is required.</span></span>

<span data-ttu-id="fdd69-111">`condition N`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="fdd69-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="fdd69-112">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="fdd69-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="fdd69-113">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="fdd69-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="fdd69-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="fdd69-114">Return values</span></span>

<span data-ttu-id="fdd69-115">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="fdd69-115">*Boolean*</span></span>

<span data-ttu-id="fdd69-116">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="fdd69-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fdd69-117">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="fdd69-117">Usage notes</span></span>

<span data-ttu-id="fdd69-118">I argumenterne for logiske funktioner kan du bruge datakildereferencer, numeriske værdier og tekstværdien, Boolesk værdier, sammenligningsoperatorer samt andre funktioner til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="fdd69-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="fdd69-119">Alle argumenterne skal dog evalueres til en *Boolesk* værdi af **SANDT** eller **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="fdd69-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fdd69-120">Example</span></span>

<span data-ttu-id="fdd69-121">`AND (1=1, "a"="a")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="fdd69-122">`AND (1=2, "a"="a")` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdd69-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fdd69-123">Additional resources</span></span>

[<span data-ttu-id="fdd69-124">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="fdd69-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]