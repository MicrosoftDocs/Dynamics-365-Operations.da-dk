---
title: ER-funktionen ABS
description: Dette emne indeholder oplysninger om, hvordan funktionen ABS til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565778"
---
# <a name="abs-er-function"></a><span data-ttu-id="009b7-103">ER-funktionen ABS</span><span class="sxs-lookup"><span data-stu-id="009b7-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="009b7-104">Funktionen `ABS` returnerer den absolutte værdi (modulus) af det angivne tal som en *Reel* værdi.</span><span class="sxs-lookup"><span data-stu-id="009b7-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="009b7-105">Returnerer med andre ord tallet uden dets fortegn.</span><span class="sxs-lookup"><span data-stu-id="009b7-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="009b7-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="009b7-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="009b7-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="009b7-107">Arguments</span></span>

<span data-ttu-id="009b7-108">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="009b7-108">`number`: *Real*</span></span>

<span data-ttu-id="009b7-109">En numerisk værdi, som du vil have modulus af.</span><span class="sxs-lookup"><span data-stu-id="009b7-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="009b7-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="009b7-110">Return values</span></span>

<span data-ttu-id="009b7-111">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="009b7-111">*Real*</span></span>

<span data-ttu-id="009b7-112">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="009b7-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="009b7-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="009b7-113">Example</span></span>

<span data-ttu-id="009b7-114">`ABS (-1)` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="009b7-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="009b7-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="009b7-115">Additional resources</span></span>

[<span data-ttu-id="009b7-116">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="009b7-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]