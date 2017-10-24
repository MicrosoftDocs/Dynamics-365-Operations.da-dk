---
title: Faktorafskrivning
description: Denne artikel indeholder en oversigt over faktorafskrivningsmetoden.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="factor-depreciation"></a><span data-ttu-id="2163c-103">Faktorafskrivning</span><span class="sxs-lookup"><span data-stu-id="2163c-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2163c-104">Denne artikel indeholder en oversigt over faktorafskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="2163c-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="2163c-105">Faktorer er de procentsatser, der bruges til afskrivning på aktiver.</span><span class="sxs-lookup"><span data-stu-id="2163c-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="2163c-106">Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Faktor** i feltet **Metode** på siden **Afskrivningsprofiler**, kan du oprette progressiv, degressiv eller lineær afskrivning:</span><span class="sxs-lookup"><span data-stu-id="2163c-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="2163c-107">Ved progressiv afskrivning øges afskrivningsbeløbet for hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2163c-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="2163c-108">Ved degressiv afskrivning mindskes afskrivningsbeløbet for hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2163c-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="2163c-109">Ved lineær afskrivning er afskrivningsbeløbet det samme i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2163c-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="2163c-110">Reglerne og eksemplerne, der følger nedenfor angiver, hvordan du kan oprette faktorer til de forskellige afskrivningstyper.</span><span class="sxs-lookup"><span data-stu-id="2163c-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="2163c-111">Når du vælger **Faktor** i feltet **Metode**, vises felterne **Faktor** og **Interval**.</span><span class="sxs-lookup"><span data-stu-id="2163c-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="2163c-112">Progressiv afskrivning</span><span class="sxs-lookup"><span data-stu-id="2163c-112">Progressive depreciation</span></span>
<span data-ttu-id="2163c-113">Værdien i feltet **Faktor** er større end **50**.</span><span class="sxs-lookup"><span data-stu-id="2163c-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2163c-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2163c-114">Example</span></span>

<span data-ttu-id="2163c-115">Anskaffelsesprisen er 100.000, faktoren er 70, levetiden er 10 år, og afskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="2163c-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2163c-116">Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.</span><span class="sxs-lookup"><span data-stu-id="2163c-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2163c-117">År</span><span class="sxs-lookup"><span data-stu-id="2163c-117">Year</span></span> | <span data-ttu-id="2163c-118">Periode</span><span class="sxs-lookup"><span data-stu-id="2163c-118">Period</span></span>      | <span data-ttu-id="2163c-119">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="2163c-119">Depreciation amount</span></span> | <span data-ttu-id="2163c-120">Bogført nettoværdi – beløb</span><span class="sxs-lookup"><span data-stu-id="2163c-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2163c-121">1</span><span class="sxs-lookup"><span data-stu-id="2163c-121">1</span></span>    | <span data-ttu-id="2163c-122">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-122">December 31</span></span> | <span data-ttu-id="2163c-123">307,69</span><span class="sxs-lookup"><span data-stu-id="2163c-123">307.69</span></span>              | <span data-ttu-id="2163c-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="2163c-124">99,692.31</span></span>             |
| <span data-ttu-id="2163c-125">2</span><span class="sxs-lookup"><span data-stu-id="2163c-125">2</span></span>    | <span data-ttu-id="2163c-126">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-126">December 31</span></span> | <span data-ttu-id="2163c-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="2163c-127">1,447.21</span></span>            | <span data-ttu-id="2163c-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="2163c-128">98,245.10</span></span>             |
| <span data-ttu-id="2163c-129">3</span><span class="sxs-lookup"><span data-stu-id="2163c-129">3</span></span>    | <span data-ttu-id="2163c-130">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-130">December 31</span></span> | <span data-ttu-id="2163c-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="2163c-131">3,104.50</span></span>            | <span data-ttu-id="2163c-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="2163c-132">95,140.60</span></span>             |
| <span data-ttu-id="2163c-133">4</span><span class="sxs-lookup"><span data-stu-id="2163c-133">4</span></span>    | <span data-ttu-id="2163c-134">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-134">December 31</span></span> | <span data-ttu-id="2163c-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="2163c-135">5,150.21</span></span>            | <span data-ttu-id="2163c-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="2163c-136">89,990.39</span></span>             |
| <span data-ttu-id="2163c-137">5</span><span class="sxs-lookup"><span data-stu-id="2163c-137">5</span></span>    | <span data-ttu-id="2163c-138">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-138">December 31</span></span> | <span data-ttu-id="2163c-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="2163c-139">7,522.95</span></span>            | <span data-ttu-id="2163c-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="2163c-140">82,467.44</span></span>             |
| <span data-ttu-id="2163c-141">6</span><span class="sxs-lookup"><span data-stu-id="2163c-141">6</span></span>    | <span data-ttu-id="2163c-142">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-142">December 31</span></span> | <span data-ttu-id="2163c-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="2163c-143">10,184.06</span></span>           | <span data-ttu-id="2163c-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="2163c-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="2163c-145">Degressiv afskrivning</span><span class="sxs-lookup"><span data-stu-id="2163c-145">Digressive depreciation</span></span>
<span data-ttu-id="2163c-146">Værdien i feltet **Faktor** er mindre end **50**.</span><span class="sxs-lookup"><span data-stu-id="2163c-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2163c-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2163c-147">Example</span></span>

<span data-ttu-id="2163c-148">Anskaffelsesprisen er 100.000, faktoren er 20, levetiden er 10 år, og afskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="2163c-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2163c-149">Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.</span><span class="sxs-lookup"><span data-stu-id="2163c-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2163c-150">År</span><span class="sxs-lookup"><span data-stu-id="2163c-150">Year</span></span> | <span data-ttu-id="2163c-151">Periode</span><span class="sxs-lookup"><span data-stu-id="2163c-151">Period</span></span>      | <span data-ttu-id="2163c-152">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="2163c-152">Depreciation amount</span></span> | <span data-ttu-id="2163c-153">Bogført nettoværdi – beløb</span><span class="sxs-lookup"><span data-stu-id="2163c-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2163c-154">1</span><span class="sxs-lookup"><span data-stu-id="2163c-154">1</span></span>    | <span data-ttu-id="2163c-155">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-155">December 31</span></span> | <span data-ttu-id="2163c-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="2163c-156">56,080.43</span></span>           | <span data-ttu-id="2163c-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="2163c-157">43,919.57</span></span>             |
| <span data-ttu-id="2163c-158">2</span><span class="sxs-lookup"><span data-stu-id="2163c-158">2</span></span>    | <span data-ttu-id="2163c-159">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-159">December 31</span></span> | <span data-ttu-id="2163c-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="2163c-160">10,665.70</span></span>           | <span data-ttu-id="2163c-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="2163c-161">33,253.87</span></span>             |
| <span data-ttu-id="2163c-162">3</span><span class="sxs-lookup"><span data-stu-id="2163c-162">3</span></span>    | <span data-ttu-id="2163c-163">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-163">December 31</span></span> | <span data-ttu-id="2163c-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="2163c-164">7,156.22</span></span>            | <span data-ttu-id="2163c-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="2163c-165">26,097.65</span></span>             |
| <span data-ttu-id="2163c-166">4</span><span class="sxs-lookup"><span data-stu-id="2163c-166">4</span></span>    | <span data-ttu-id="2163c-167">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-167">December 31</span></span> | <span data-ttu-id="2163c-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="2163c-168">5,538.06</span></span>            | <span data-ttu-id="2163c-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="2163c-169">20,559.59</span></span>             |
| <span data-ttu-id="2163c-170">5</span><span class="sxs-lookup"><span data-stu-id="2163c-170">5</span></span>    | <span data-ttu-id="2163c-171">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-171">December 31</span></span> | <span data-ttu-id="2163c-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="2163c-172">4,579.89</span></span>            | <span data-ttu-id="2163c-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="2163c-173">15,979.70</span></span>             |
| <span data-ttu-id="2163c-174">6</span><span class="sxs-lookup"><span data-stu-id="2163c-174">6</span></span>    | <span data-ttu-id="2163c-175">31. december</span><span class="sxs-lookup"><span data-stu-id="2163c-175">December 31</span></span> | <span data-ttu-id="2163c-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="2163c-176">3,937.36</span></span>            | <span data-ttu-id="2163c-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="2163c-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="2163c-178">Lineær afskrivning</span><span class="sxs-lookup"><span data-stu-id="2163c-178">Straight line depreciation</span></span>
<span data-ttu-id="2163c-179">Værdien i feltet **Faktor** er lig med **50**.</span><span class="sxs-lookup"><span data-stu-id="2163c-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="2163c-180">I dette tilfælde er afskrivningen den samme i hver periode, og derfor skal du overveje konsekvensen af de værdier, du har angivet i andre felter, som beskrevet i [Lineær afskrivning for levetiden](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="2163c-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




