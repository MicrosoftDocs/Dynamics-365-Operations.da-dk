---
title: ER-funktionen ROUNDUP
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUNDUP til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744433"
---
# <a name="roundup-er-function"></a><span data-ttu-id="22b74-103">ER-funktionen ROUNDUP</span><span class="sxs-lookup"><span data-stu-id="22b74-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22b74-104">Funktionen `ROUNDUP` returnerer det angivne tal som en *Reel* værdi, når det er rundet op til det angivne antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="22b74-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b74-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="22b74-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="22b74-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="22b74-106">Arguments</span></span>

<span data-ttu-id="22b74-107">`number`: *Reel*</span><span class="sxs-lookup"><span data-stu-id="22b74-107">`number`: *Real*</span></span>

<span data-ttu-id="22b74-108">En numerisk værdi, der skal rundes op.</span><span class="sxs-lookup"><span data-stu-id="22b74-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="22b74-109">`decimals`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="22b74-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="22b74-110">En numerisk værdi, der repræsenterer antallet af decimaler.</span><span class="sxs-lookup"><span data-stu-id="22b74-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="22b74-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="22b74-111">Return values</span></span>

<span data-ttu-id="22b74-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="22b74-112">*Real*</span></span>

<span data-ttu-id="22b74-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="22b74-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="22b74-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="22b74-114">Usage notes</span></span>

<span data-ttu-id="22b74-115">Denne funktion fungerer ligesom [ROUND](er-functions-mathematical-round.md), men den runder altid det angivne tal op (væk fra nul).</span><span class="sxs-lookup"><span data-stu-id="22b74-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="22b74-116">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="22b74-116">Example 1</span></span>

<span data-ttu-id="22b74-117">`ROUNDUP (1200.763, 2)` runder op til to decimaler og returnerer **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="22b74-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="22b74-118">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="22b74-118">Example 2</span></span>

<span data-ttu-id="22b74-119">`ROUNDUP (1200.767, -3)` runder op til det nærmeste multiplum af 1.000 og returnerer **2000**.</span><span class="sxs-lookup"><span data-stu-id="22b74-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22b74-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="22b74-120">Additional resources</span></span>

[<span data-ttu-id="22b74-121">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="22b74-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]