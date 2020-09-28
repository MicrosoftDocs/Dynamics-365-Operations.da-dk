---
title: ER-funktionen ABS
description: Dette emne indeholder oplysninger om, hvordan funktionen ABS til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744593"
---
# <a name="abs-er-function"></a><span data-ttu-id="c54d4-103">ER-funktionen ABS</span><span class="sxs-lookup"><span data-stu-id="c54d4-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c54d4-104">Funktionen `ABS` returnerer den absolutte værdi (modulus) af det angivne tal som en *Reel* værdi.</span><span class="sxs-lookup"><span data-stu-id="c54d4-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="c54d4-105">Returnerer med andre ord tallet uden dets fortegn.</span><span class="sxs-lookup"><span data-stu-id="c54d4-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="c54d4-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c54d4-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="c54d4-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c54d4-107">Arguments</span></span>

<span data-ttu-id="c54d4-108">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="c54d4-108">`number`: *Real*</span></span>

<span data-ttu-id="c54d4-109">En numerisk værdi, som du vil have modulus af.</span><span class="sxs-lookup"><span data-stu-id="c54d4-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="c54d4-110">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c54d4-110">Return values</span></span>

<span data-ttu-id="c54d4-111">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="c54d4-111">*Real*</span></span>

<span data-ttu-id="c54d4-112">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="c54d4-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="c54d4-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c54d4-113">Example</span></span>

<span data-ttu-id="c54d4-114">`ABS (-1)` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="c54d4-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c54d4-115">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c54d4-115">Additional resources</span></span>

[<span data-ttu-id="c54d4-116">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="c54d4-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
