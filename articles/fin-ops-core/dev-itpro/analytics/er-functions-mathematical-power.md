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
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041624"
---
# <span data-ttu-id="25448-103"><a name="POWER">ER-funktionen POWER</a></span><span class="sxs-lookup"><span data-stu-id="25448-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25448-104">Funktionen `POWER` returnerer en *Reel* værdi, der repræsenterer resultatet af at hæve det angivne positive tal til den angivne effekt.</span><span class="sxs-lookup"><span data-stu-id="25448-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="25448-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="25448-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="25448-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="25448-106">Arguments</span></span>

<span data-ttu-id="25448-107">`number`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="25448-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="25448-108">En numerisk værdi, der skal opløftes til den angivne effekt.</span><span class="sxs-lookup"><span data-stu-id="25448-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="25448-109">`power`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="25448-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="25448-110">En numerisk værdi, der repræsenterer den specifikke effekt.</span><span class="sxs-lookup"><span data-stu-id="25448-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="25448-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="25448-111">Return values</span></span>

<span data-ttu-id="25448-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="25448-112">*Real*</span></span>

<span data-ttu-id="25448-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="25448-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="25448-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="25448-114">Example 1</span></span>

<span data-ttu-id="25448-115">`POWER (10, 2)` returnerer **100**.</span><span class="sxs-lookup"><span data-stu-id="25448-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="25448-116">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="25448-116">Example 2</span></span>

<span data-ttu-id="25448-117">`POWER (4, 0.5)` returnerer **2**.</span><span class="sxs-lookup"><span data-stu-id="25448-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25448-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="25448-118">Additional resources</span></span>

[<span data-ttu-id="25448-119">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="25448-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
