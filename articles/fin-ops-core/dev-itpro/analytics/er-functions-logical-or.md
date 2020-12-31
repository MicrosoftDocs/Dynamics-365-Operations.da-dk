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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686972"
---
# <a name="or-er-function"></a><span data-ttu-id="50903-103">ER-funktionen OR</span><span class="sxs-lookup"><span data-stu-id="50903-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50903-104">Funktionen `OR` returnerer en *Boolesk* værdi som værende **FALSK**, hvis alle de angivne betingelser ikke er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="50903-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="50903-105">Hvis en eller flere af de angivne betingelser er opfyldte, returnerer denne funktion en *Boolesk* værdi som værende **SAND**.</span><span class="sxs-lookup"><span data-stu-id="50903-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="50903-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="50903-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="50903-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="50903-107">Arguments</span></span>

<span data-ttu-id="50903-108">`condition 1`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="50903-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="50903-109">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="50903-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="50903-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="50903-110">This argument is required.</span></span>

<span data-ttu-id="50903-111">`condition N`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="50903-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="50903-112">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="50903-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="50903-113">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="50903-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="50903-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="50903-114">Return values</span></span>

<span data-ttu-id="50903-115">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="50903-115">*Boolean*</span></span>

<span data-ttu-id="50903-116">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="50903-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="50903-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="50903-117">Example</span></span>

<span data-ttu-id="50903-118">`OR (1=2, "a"="a")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="50903-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50903-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="50903-119">Additional resources</span></span>

[<span data-ttu-id="50903-120">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="50903-120">Logical functions</span></span>](er-functions-category-logical.md)
