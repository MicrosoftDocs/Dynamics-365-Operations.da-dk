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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92150bb23e76f82907e0f3e8f0738b25801958bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041555"
---
# <span data-ttu-id="916f1-103"><a name="ROUNDDOWN">ER-funktionen ROUNDDOWN</a></span><span class="sxs-lookup"><span data-stu-id="916f1-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="916f1-104">Funktionen `ROUNDDOWN` returnerer det angivne tal som en *Reel* værdi, når det er rundet ned til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="916f1-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="916f1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="916f1-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="916f1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="916f1-106">Arguments</span></span>

<span data-ttu-id="916f1-107">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="916f1-107">`number`: *Real*</span></span>

<span data-ttu-id="916f1-108">En numerisk værdi, der skal rundes ned.</span><span class="sxs-lookup"><span data-stu-id="916f1-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="916f1-109">`decimals`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="916f1-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="916f1-110">En numerisk værdi, der repræsenterer antallet af decimaler.</span><span class="sxs-lookup"><span data-stu-id="916f1-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="916f1-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="916f1-111">Return values</span></span>

<span data-ttu-id="916f1-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="916f1-112">*Real*</span></span>

<span data-ttu-id="916f1-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="916f1-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="916f1-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="916f1-114">Usage notes</span></span>

<span data-ttu-id="916f1-115">Denne funktion fungerer ligesom [ROUND](er-functions-mathematical-round.md), men den runder altid det angivne tal ned (mod nul).</span><span class="sxs-lookup"><span data-stu-id="916f1-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="916f1-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="916f1-116">Example 1</span></span>

<span data-ttu-id="916f1-117">`ROUNDDOWN (1200.767, 2)` runder ned til to decimaler og returnerer **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="916f1-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="916f1-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="916f1-118">Example 2</span></span>

<span data-ttu-id="916f1-119">`ROUNDDOWN (1700.767, -3)` runder ned til det nærmeste multiplum af 1.000 og returnerer **1000**.</span><span class="sxs-lookup"><span data-stu-id="916f1-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="916f1-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="916f1-120">Additional resources</span></span>

[<span data-ttu-id="916f1-121">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="916f1-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
