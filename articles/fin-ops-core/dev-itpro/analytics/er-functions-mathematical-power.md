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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683323"
---
# <a name="power-er-function"></a><span data-ttu-id="8c06d-103">ER-funktionen POWER</span><span class="sxs-lookup"><span data-stu-id="8c06d-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c06d-104">Funktionen `POWER` returnerer en *Reel* værdi, der repræsenterer resultatet af at hæve det angivne positive tal til den angivne effekt.</span><span class="sxs-lookup"><span data-stu-id="8c06d-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c06d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8c06d-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="8c06d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8c06d-106">Arguments</span></span>

<span data-ttu-id="8c06d-107">`number`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="8c06d-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="8c06d-108">En numerisk værdi, der skal opløftes til den angivne effekt.</span><span class="sxs-lookup"><span data-stu-id="8c06d-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="8c06d-109">`power`: *Reel* eller *Heltal*</span><span class="sxs-lookup"><span data-stu-id="8c06d-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="8c06d-110">En numerisk værdi, der repræsenterer den specifikke effekt.</span><span class="sxs-lookup"><span data-stu-id="8c06d-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c06d-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="8c06d-111">Return values</span></span>

<span data-ttu-id="8c06d-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="8c06d-112">*Real*</span></span>

<span data-ttu-id="8c06d-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="8c06d-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="8c06d-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="8c06d-114">Example 1</span></span>

<span data-ttu-id="8c06d-115">`POWER (10, 2)` returnerer **100**.</span><span class="sxs-lookup"><span data-stu-id="8c06d-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8c06d-116">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="8c06d-116">Example 2</span></span>

<span data-ttu-id="8c06d-117">`POWER (4, 0.5)` returnerer **2**.</span><span class="sxs-lookup"><span data-stu-id="8c06d-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c06d-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8c06d-118">Additional resources</span></span>

[<span data-ttu-id="8c06d-119">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="8c06d-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
