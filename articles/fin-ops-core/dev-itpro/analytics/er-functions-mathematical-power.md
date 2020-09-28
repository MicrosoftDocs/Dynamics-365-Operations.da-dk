---
title: ER-funktionen POWER
description: Dette emne indeholder oplysninger om, hvordan funktionen POWER til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744569"
---
# <a name="power-er-function"></a><span data-ttu-id="7bf29-103">ER-funktionen POWER</span><span class="sxs-lookup"><span data-stu-id="7bf29-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bf29-104">Funktionen `POWER` returnerer en *Reel* værdi, der repræsenterer resultatet af at hæve det angivne positive tal til den angivne effekt.</span><span class="sxs-lookup"><span data-stu-id="7bf29-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf29-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7bf29-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="7bf29-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7bf29-106">Arguments</span></span>

<span data-ttu-id="7bf29-107">`number`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="7bf29-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="7bf29-108">En numerisk værdi, der skal opløftes til den angivne effekt.</span><span class="sxs-lookup"><span data-stu-id="7bf29-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="7bf29-109">`power`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="7bf29-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="7bf29-110">En numerisk værdi, der repræsenterer den specifikke effekt.</span><span class="sxs-lookup"><span data-stu-id="7bf29-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="7bf29-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7bf29-111">Return values</span></span>

<span data-ttu-id="7bf29-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="7bf29-112">*Real*</span></span>

<span data-ttu-id="7bf29-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="7bf29-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="7bf29-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="7bf29-114">Example 1</span></span>

<span data-ttu-id="7bf29-115">`POWER (10, 2)` returnerer **100**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7bf29-116">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="7bf29-116">Example 2</span></span>

<span data-ttu-id="7bf29-117">`POWER (4, 0.5)` returnerer **2**.</span><span class="sxs-lookup"><span data-stu-id="7bf29-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bf29-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7bf29-118">Additional resources</span></span>

[<span data-ttu-id="7bf29-119">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="7bf29-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
