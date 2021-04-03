---
title: ER-funktionen ROUNDAMOUNT
description: Dette emne indeholder oplysninger om, hvordan funktionen ROUNDAMOUNT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 2a80587236d17160a996d701ca4ae38be21c818c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563288"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="16449-103">ER-funktionen ROUNDAMOUNT</span><span class="sxs-lookup"><span data-stu-id="16449-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16449-104">Funktionen `ROUNDAMOUNT` returnerer en *Reel* værdi som resultatet af afrundingen af det angivne tal til nærmeste multiplum af et andet tal i henhold til den angivne afrundingsregel.</span><span class="sxs-lookup"><span data-stu-id="16449-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="16449-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="16449-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="16449-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="16449-106">Arguments</span></span>

<span data-ttu-id="16449-107">`number`: *Int* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="16449-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="16449-108">En numerisk værdi, der skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="16449-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="16449-109">`decimals`: *Int* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="16449-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="16449-110">Det tal, som værdien af parametret `number` skal afrundes til et multiplum af.</span><span class="sxs-lookup"><span data-stu-id="16449-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="16449-111">`round rule`: *Fasttekstværdi*</span><span class="sxs-lookup"><span data-stu-id="16449-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="16449-112">En fasttekstværdi af fastteksten **RoundOffType**, der definerer afrundingsreglen.</span><span class="sxs-lookup"><span data-stu-id="16449-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="16449-113">Denne fasttekst indeholder følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="16449-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="16449-114">Normal (almindelig)</span><span class="sxs-lookup"><span data-stu-id="16449-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="16449-115">Nedad (rund nedad)</span><span class="sxs-lookup"><span data-stu-id="16449-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="16449-116">Oprunding (rund op)</span><span class="sxs-lookup"><span data-stu-id="16449-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="16449-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="16449-117">Return values</span></span>

<span data-ttu-id="16449-118">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="16449-118">*Real*</span></span>

<span data-ttu-id="16449-119">Den resulterende numeriske værdi er et multiplum af den værdi, der er angivet af parametret `decimals`, og er tættest på den værdi, der er angivet af parametret `number`.</span><span class="sxs-lookup"><span data-stu-id="16449-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="16449-120">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="16449-120">Usage notes</span></span>

<span data-ttu-id="16449-121">Når parametret `number` er nul, returnerer denne funktion altid nul.</span><span class="sxs-lookup"><span data-stu-id="16449-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="16449-122">Når parametret `decimals` er nul, afrundes denne funktion til standardværdien for afrunding.</span><span class="sxs-lookup"><span data-stu-id="16449-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="16449-123">Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, er standardværdien for afrunding **0,01**.</span><span class="sxs-lookup"><span data-stu-id="16449-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="16449-124">Ellers er standardværdien for afrunding **1,0**.</span><span class="sxs-lookup"><span data-stu-id="16449-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="16449-125">Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, afrundes denne funktion til nærmeste afrundede beløb.</span><span class="sxs-lookup"><span data-stu-id="16449-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="16449-126">Når parametret `round rule` er angivet til **RoundOffType.RoundDown**, afrunder denne funktion ned til nul for nærmeste afrundede beløb.</span><span class="sxs-lookup"><span data-stu-id="16449-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="16449-127">Når parametret `round rule` er angivet til **RoundOffType.RoundUP**, afrunder denne funktion op fra til det nærmeste afrundede beløb.</span><span class="sxs-lookup"><span data-stu-id="16449-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="16449-128">Når parametret `round rule` er angivet til **RoundOffType.Ordinary**, fungerer denne funktion som Excel-funktionen [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) og X+ +-funktionen [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).</span><span class="sxs-lookup"><span data-stu-id="16449-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="16449-129">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="16449-129">Remarks</span></span>

<span data-ttu-id="16449-130">Hvis du vil afrunde en numerisk værdi til et angivet antal decimaler, skal du bruge funktionen [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="16449-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="16449-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="16449-131">Example</span></span>

<span data-ttu-id="16449-132">Hvis parametret **model.RoundOff** er indstillet til **RoundOffType.Ordinary**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="16449-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="16449-133">Hvis parametret **model.RoundOff** er indstillet til **RoundOffType.RoundDown**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35.</span><span class="sxs-lookup"><span data-stu-id="16449-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="16449-134">Hvis parametret **model.RoundOff** er indstillet til **RoundOffType.RoundUp**, returnerer `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4.</span><span class="sxs-lookup"><span data-stu-id="16449-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16449-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="16449-135">Additional resources</span></span>

[<span data-ttu-id="16449-136">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="16449-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="16449-137">Matematiske funktioner</span><span class="sxs-lookup"><span data-stu-id="16449-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]