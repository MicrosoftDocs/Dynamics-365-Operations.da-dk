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
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: da-dk
ms.lasthandoff: 06/29/2017


---

# <a name="factor-depreciation"></a><span data-ttu-id="48a42-103">Faktorafskrivning</span><span class="sxs-lookup"><span data-stu-id="48a42-103">Factor depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="48a42-104">Denne artikel indeholder en oversigt over faktorafskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="48a42-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="48a42-105">Faktorer er de procentsatser, der bruges til afskrivning på aktiver.</span><span class="sxs-lookup"><span data-stu-id="48a42-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="48a42-106">Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Faktor** i feltet **Metode** på siden **Afskrivningsprofiler**, kan du oprette progressiv, degressiv eller lineær afskrivning:</span><span class="sxs-lookup"><span data-stu-id="48a42-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="48a42-107">Ved progressiv afskrivning øges afskrivningsbeløbet for hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="48a42-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="48a42-108">Ved degressiv afskrivning mindskes afskrivningsbeløbet for hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="48a42-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="48a42-109">Ved lineær afskrivning er afskrivningsbeløbet det samme i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="48a42-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="48a42-110">Reglerne og eksemplerne, der følger nedenfor angiver, hvordan du kan oprette faktorer til de forskellige afskrivningstyper.</span><span class="sxs-lookup"><span data-stu-id="48a42-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="48a42-111">Når du vælger **Faktor** i feltet **Metode**, vises felterne **Faktor** og **Interval**.</span><span class="sxs-lookup"><span data-stu-id="48a42-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="48a42-112">Progressiv afskrivning</span><span class="sxs-lookup"><span data-stu-id="48a42-112">Progressive depreciation</span></span>
<span data-ttu-id="48a42-113">Værdien i feltet **Faktor** er større end **50**.</span><span class="sxs-lookup"><span data-stu-id="48a42-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="48a42-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="48a42-114">Example</span></span>

<span data-ttu-id="48a42-115">Anskaffelsesprisen er 100.000, faktoren er 70, levetiden er 10 år, og afskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="48a42-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="48a42-116">Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.</span><span class="sxs-lookup"><span data-stu-id="48a42-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="48a42-117">År</span><span class="sxs-lookup"><span data-stu-id="48a42-117">Year</span></span> | <span data-ttu-id="48a42-118">Periode</span><span class="sxs-lookup"><span data-stu-id="48a42-118">Period</span></span>      | <span data-ttu-id="48a42-119">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="48a42-119">Depreciation amount</span></span> | <span data-ttu-id="48a42-120">Bogført nettoværdi – beløb</span><span class="sxs-lookup"><span data-stu-id="48a42-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="48a42-121">1</span><span class="sxs-lookup"><span data-stu-id="48a42-121">1</span></span>    | <span data-ttu-id="48a42-122">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-122">December 31</span></span> | <span data-ttu-id="48a42-123">307,69</span><span class="sxs-lookup"><span data-stu-id="48a42-123">307.69</span></span>              | <span data-ttu-id="48a42-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="48a42-124">99,692.31</span></span>             |
| <span data-ttu-id="48a42-125">2</span><span class="sxs-lookup"><span data-stu-id="48a42-125">2</span></span>    | <span data-ttu-id="48a42-126">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-126">December 31</span></span> | <span data-ttu-id="48a42-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="48a42-127">1,447.21</span></span>            | <span data-ttu-id="48a42-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="48a42-128">98,245.10</span></span>             |
| <span data-ttu-id="48a42-129">3</span><span class="sxs-lookup"><span data-stu-id="48a42-129">3</span></span>    | <span data-ttu-id="48a42-130">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-130">December 31</span></span> | <span data-ttu-id="48a42-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="48a42-131">3,104.50</span></span>            | <span data-ttu-id="48a42-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="48a42-132">95,140.60</span></span>             |
| <span data-ttu-id="48a42-133">4</span><span class="sxs-lookup"><span data-stu-id="48a42-133">4</span></span>    | <span data-ttu-id="48a42-134">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-134">December 31</span></span> | <span data-ttu-id="48a42-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="48a42-135">5,150.21</span></span>            | <span data-ttu-id="48a42-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="48a42-136">89,990.39</span></span>             |
| <span data-ttu-id="48a42-137">5</span><span class="sxs-lookup"><span data-stu-id="48a42-137">5</span></span>    | <span data-ttu-id="48a42-138">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-138">December 31</span></span> | <span data-ttu-id="48a42-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="48a42-139">7,522.95</span></span>            | <span data-ttu-id="48a42-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="48a42-140">82,467.44</span></span>             |
| <span data-ttu-id="48a42-141">6</span><span class="sxs-lookup"><span data-stu-id="48a42-141">6</span></span>    | <span data-ttu-id="48a42-142">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-142">December 31</span></span> | <span data-ttu-id="48a42-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="48a42-143">10,184.06</span></span>           | <span data-ttu-id="48a42-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="48a42-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="48a42-145">Degressiv afskrivning</span><span class="sxs-lookup"><span data-stu-id="48a42-145">Digressive depreciation</span></span>
<span data-ttu-id="48a42-146">Værdien i feltet **Faktor** er mindre end **50**.</span><span class="sxs-lookup"><span data-stu-id="48a42-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="48a42-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="48a42-147">Example</span></span>

<span data-ttu-id="48a42-148">Anskaffelsesprisen er 100.000, faktoren er 20, levetiden er 10 år, og afskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="48a42-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="48a42-149">Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.</span><span class="sxs-lookup"><span data-stu-id="48a42-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="48a42-150">År</span><span class="sxs-lookup"><span data-stu-id="48a42-150">Year</span></span> | <span data-ttu-id="48a42-151">Periode</span><span class="sxs-lookup"><span data-stu-id="48a42-151">Period</span></span>      | <span data-ttu-id="48a42-152">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="48a42-152">Depreciation amount</span></span> | <span data-ttu-id="48a42-153">Bogført nettoværdi – beløb</span><span class="sxs-lookup"><span data-stu-id="48a42-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="48a42-154">1</span><span class="sxs-lookup"><span data-stu-id="48a42-154">1</span></span>    | <span data-ttu-id="48a42-155">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-155">December 31</span></span> | <span data-ttu-id="48a42-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="48a42-156">56,080.43</span></span>           | <span data-ttu-id="48a42-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="48a42-157">43,919.57</span></span>             |
| <span data-ttu-id="48a42-158">2</span><span class="sxs-lookup"><span data-stu-id="48a42-158">2</span></span>    | <span data-ttu-id="48a42-159">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-159">December 31</span></span> | <span data-ttu-id="48a42-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="48a42-160">10,665.70</span></span>           | <span data-ttu-id="48a42-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="48a42-161">33,253.87</span></span>             |
| <span data-ttu-id="48a42-162">3</span><span class="sxs-lookup"><span data-stu-id="48a42-162">3</span></span>    | <span data-ttu-id="48a42-163">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-163">December 31</span></span> | <span data-ttu-id="48a42-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="48a42-164">7,156.22</span></span>            | <span data-ttu-id="48a42-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="48a42-165">26,097.65</span></span>             |
| <span data-ttu-id="48a42-166">4</span><span class="sxs-lookup"><span data-stu-id="48a42-166">4</span></span>    | <span data-ttu-id="48a42-167">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-167">December 31</span></span> | <span data-ttu-id="48a42-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="48a42-168">5,538.06</span></span>            | <span data-ttu-id="48a42-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="48a42-169">20,559.59</span></span>             |
| <span data-ttu-id="48a42-170">5</span><span class="sxs-lookup"><span data-stu-id="48a42-170">5</span></span>    | <span data-ttu-id="48a42-171">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-171">December 31</span></span> | <span data-ttu-id="48a42-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="48a42-172">4,579.89</span></span>            | <span data-ttu-id="48a42-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="48a42-173">15,979.70</span></span>             |
| <span data-ttu-id="48a42-174">6</span><span class="sxs-lookup"><span data-stu-id="48a42-174">6</span></span>    | <span data-ttu-id="48a42-175">31. december</span><span class="sxs-lookup"><span data-stu-id="48a42-175">December 31</span></span> | <span data-ttu-id="48a42-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="48a42-176">3,937.36</span></span>            | <span data-ttu-id="48a42-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="48a42-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="48a42-178">Lineær afskrivning</span><span class="sxs-lookup"><span data-stu-id="48a42-178">Straight line depreciation</span></span>
<span data-ttu-id="48a42-179">Værdien i feltet **Faktor** er lig med **50**.</span><span class="sxs-lookup"><span data-stu-id="48a42-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="48a42-180">I dette tilfælde er afskrivningen den samme i hver periode, og derfor skal du overveje konsekvensen af de værdier, du har angivet i andre felter, som beskrevet i [Lineær afskrivning for levetiden](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="48a42-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




