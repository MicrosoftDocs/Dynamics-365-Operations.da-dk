---
title: ER-funktionen NOT
description: Dette emne indeholder oplysninger om, hvordan funktionen NOT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041716"
---
# <span data-ttu-id="7fdc0-103"><a name="NOT">ER-funktionen NOT</a></span><span class="sxs-lookup"><span data-stu-id="7fdc0-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fdc0-104">Funktionen `NOT` returnerer den omvendte logiske værdi af den angivne betingelse som en *Boolesk* værdi.</span><span class="sxs-lookup"><span data-stu-id="7fdc0-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fdc0-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7fdc0-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="7fdc0-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7fdc0-106">Arguments</span></span>

<span data-ttu-id="7fdc0-107">`condition`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="7fdc0-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="7fdc0-108">Et gyldigt betinget udtryk, der skal tilbageføres.</span><span class="sxs-lookup"><span data-stu-id="7fdc0-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="7fdc0-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7fdc0-109">Return values</span></span>

<span data-ttu-id="7fdc0-110">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="7fdc0-110">*Boolean*</span></span>

<span data-ttu-id="7fdc0-111">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="7fdc0-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="7fdc0-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7fdc0-112">Example</span></span>

<span data-ttu-id="7fdc0-113">`NOT (TRUE)` returnerer **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7fdc0-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fdc0-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7fdc0-114">Additional resources</span></span>

[<span data-ttu-id="7fdc0-115">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="7fdc0-115">Logical functions</span></span>](er-functions-category-logical.md)
