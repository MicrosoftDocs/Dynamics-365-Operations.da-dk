---
title: ER-funktionen ROUNDDOWN
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUNDDOWN til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686876"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="7c2bb-103">ER-funktionen ROUNDDOWN</span><span class="sxs-lookup"><span data-stu-id="7c2bb-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c2bb-104">Funktionen `ROUNDDOWN` returnerer det angivne tal som en *Reel* værdi, når det er rundet ned til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="7c2bb-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2bb-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7c2bb-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="7c2bb-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7c2bb-106">Arguments</span></span>

<span data-ttu-id="7c2bb-107">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="7c2bb-107">`number`: *Real*</span></span>

<span data-ttu-id="7c2bb-108">En numerisk værdi, der skal rundes ned.</span><span class="sxs-lookup"><span data-stu-id="7c2bb-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="7c2bb-109">`decimals`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="7c2bb-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="7c2bb-110">En numerisk værdi, der repræsenterer antallet af decimaler.</span><span class="sxs-lookup"><span data-stu-id="7c2bb-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c2bb-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7c2bb-111">Return values</span></span>

<span data-ttu-id="7c2bb-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="7c2bb-112">*Real*</span></span>

<span data-ttu-id="7c2bb-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="7c2bb-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7c2bb-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="7c2bb-114">Usage notes</span></span>

<span data-ttu-id="7c2bb-115">Denne funktion fungerer ligesom [ROUND](er-functions-mathematical-round.md), men den runder altid det angivne tal ned (mod nul).</span><span class="sxs-lookup"><span data-stu-id="7c2bb-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="7c2bb-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="7c2bb-116">Example 1</span></span>

<span data-ttu-id="7c2bb-117">`ROUNDDOWN (1200.767, 2)` runder ned til to decimaler og returnerer **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="7c2bb-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="7c2bb-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="7c2bb-118">Example 2</span></span>

<span data-ttu-id="7c2bb-119">`ROUNDDOWN (1700.767, -3)` runder ned til det nærmeste multiplum af 1.000 og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="7c2bb-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c2bb-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7c2bb-120">Additional resources</span></span>

[<span data-ttu-id="7c2bb-121">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="7c2bb-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
