---
title: ER-funktionen OR
description: Dette emne indeholder oplysninger om, hvordan funktionen OR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 7c2f110185330ee1e0cc6dc9ac534ae697e4b19b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565850"
---
# <a name="or-er-function"></a><span data-ttu-id="6b637-103">ER-funktionen OR</span><span class="sxs-lookup"><span data-stu-id="6b637-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b637-104">Funktionen `OR` returnerer en *Boolesk* værdi som værende **FALSK**, hvis alle de angivne betingelser ikke er opfyldte.</span><span class="sxs-lookup"><span data-stu-id="6b637-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="6b637-105">Hvis en eller flere af de angivne betingelser er opfyldte, returnerer denne funktion en *Boolesk* værdi som værende **SAND**.</span><span class="sxs-lookup"><span data-stu-id="6b637-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b637-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="6b637-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="6b637-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="6b637-107">Arguments</span></span>

<span data-ttu-id="6b637-108">`condition 1`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="6b637-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="6b637-109">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="6b637-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="6b637-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="6b637-110">This argument is required.</span></span>

<span data-ttu-id="6b637-111">`condition N`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="6b637-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="6b637-112">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="6b637-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="6b637-113">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="6b637-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6b637-114">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="6b637-114">Return values</span></span>

<span data-ttu-id="6b637-115">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="6b637-115">*Boolean*</span></span>

<span data-ttu-id="6b637-116">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="6b637-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="6b637-117">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6b637-117">Example</span></span>

<span data-ttu-id="6b637-118">`OR (1=2, "a"="a")` returnerer **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="6b637-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b637-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6b637-119">Additional resources</span></span>

[<span data-ttu-id="6b637-120">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="6b637-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]