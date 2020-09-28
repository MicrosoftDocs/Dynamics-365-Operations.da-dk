---
title: ER-funktionen OR
description: Dette emne indeholder oplysninger om, hvordan funktionen OR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744617"
---
# <a name="or-er-function"></a><span data-ttu-id="3fac2-103">ER-funktionen OR</span><span class="sxs-lookup"><span data-stu-id="3fac2-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fac2-104">Funktionen `OR` returnerer en *Boolesk* værdi som værende **FALSK**, hvis alle de angivne betingelser ikke er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="3fac2-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="3fac2-105">Hvis en eller flere af de angivne betingelser er opfyldte, returnerer denne funktion en *Boolesk* værdi som værende **SAND**.</span><span class="sxs-lookup"><span data-stu-id="3fac2-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fac2-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3fac2-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="3fac2-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3fac2-107">Arguments</span></span>

<span data-ttu-id="3fac2-108">`condition 1`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="3fac2-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="3fac2-109">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="3fac2-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="3fac2-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="3fac2-110">This argument is required.</span></span>

<span data-ttu-id="3fac2-111">`condition N`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="3fac2-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="3fac2-112">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="3fac2-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="3fac2-113">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="3fac2-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="3fac2-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="3fac2-114">Return values</span></span>

<span data-ttu-id="3fac2-115">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="3fac2-115">*Boolean*</span></span>

<span data-ttu-id="3fac2-116">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="3fac2-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="3fac2-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3fac2-117">Example</span></span>

<span data-ttu-id="3fac2-118">`OR (1=2, "a"="a")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="3fac2-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fac2-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3fac2-119">Additional resources</span></span>

[<span data-ttu-id="3fac2-120">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="3fac2-120">Logical functions</span></span>](er-functions-category-logical.md)
