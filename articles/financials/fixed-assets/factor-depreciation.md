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
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d56386db5f1223dd03764d0f515aca6409f2c8a7
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="factor-depreciation"></a><span data-ttu-id="2756d-103">Faktorafskrivning</span><span class="sxs-lookup"><span data-stu-id="2756d-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2756d-104">Denne artikel indeholder en oversigt over faktorafskrivningsmetoden.</span><span class="sxs-lookup"><span data-stu-id="2756d-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="2756d-105">Faktorer er de procentsatser, der bruges til afskrivning på aktiver.</span><span class="sxs-lookup"><span data-stu-id="2756d-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="2756d-106">Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Faktor** i feltet **Metode** på siden **Afskrivningsprofiler**, kan du oprette progressiv, degressiv eller lineær afskrivning:</span><span class="sxs-lookup"><span data-stu-id="2756d-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="2756d-107">Ved progressiv afskrivning øges afskrivningsbeløbet for hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2756d-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="2756d-108">Ved degressiv afskrivning mindskes afskrivningsbeløbet for hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2756d-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="2756d-109">Ved lineær afskrivning er afskrivningsbeløbet det samme i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="2756d-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="2756d-110">Reglerne og eksemplerne, der følger nedenfor angiver, hvordan du kan oprette faktorer til de forskellige afskrivningstyper.</span><span class="sxs-lookup"><span data-stu-id="2756d-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="2756d-111">Når du vælger **Faktor** i feltet **Metode**, vises felterne **Faktor** og **Interval**.</span><span class="sxs-lookup"><span data-stu-id="2756d-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="2756d-112">Progressiv afskrivning</span><span class="sxs-lookup"><span data-stu-id="2756d-112">Progressive depreciation</span></span>
<span data-ttu-id="2756d-113">Værdien i feltet **Faktor** er større end **50**.</span><span class="sxs-lookup"><span data-stu-id="2756d-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2756d-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2756d-114">Example</span></span>

<span data-ttu-id="2756d-115">Anskaffelsesprisen er 100.000, faktoren er 70, levetiden er 10 år, og afskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="2756d-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2756d-116">Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.</span><span class="sxs-lookup"><span data-stu-id="2756d-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2756d-117">År</span><span class="sxs-lookup"><span data-stu-id="2756d-117">Year</span></span> | <span data-ttu-id="2756d-118">Periode</span><span class="sxs-lookup"><span data-stu-id="2756d-118">Period</span></span>      | <span data-ttu-id="2756d-119">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="2756d-119">Depreciation amount</span></span> | <span data-ttu-id="2756d-120">Bogført nettoværdi – beløb</span><span class="sxs-lookup"><span data-stu-id="2756d-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2756d-121">1</span><span class="sxs-lookup"><span data-stu-id="2756d-121">1</span></span>    | <span data-ttu-id="2756d-122">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-122">December 31</span></span> | <span data-ttu-id="2756d-123">307,69</span><span class="sxs-lookup"><span data-stu-id="2756d-123">307.69</span></span>              | <span data-ttu-id="2756d-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="2756d-124">99,692.31</span></span>             |
| <span data-ttu-id="2756d-125">2</span><span class="sxs-lookup"><span data-stu-id="2756d-125">2</span></span>    | <span data-ttu-id="2756d-126">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-126">December 31</span></span> | <span data-ttu-id="2756d-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="2756d-127">1,447.21</span></span>            | <span data-ttu-id="2756d-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="2756d-128">98,245.10</span></span>             |
| <span data-ttu-id="2756d-129">3</span><span class="sxs-lookup"><span data-stu-id="2756d-129">3</span></span>    | <span data-ttu-id="2756d-130">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-130">December 31</span></span> | <span data-ttu-id="2756d-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="2756d-131">3,104.50</span></span>            | <span data-ttu-id="2756d-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="2756d-132">95,140.60</span></span>             |
| <span data-ttu-id="2756d-133">4</span><span class="sxs-lookup"><span data-stu-id="2756d-133">4</span></span>    | <span data-ttu-id="2756d-134">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-134">December 31</span></span> | <span data-ttu-id="2756d-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="2756d-135">5,150.21</span></span>            | <span data-ttu-id="2756d-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="2756d-136">89,990.39</span></span>             |
| <span data-ttu-id="2756d-137">5</span><span class="sxs-lookup"><span data-stu-id="2756d-137">5</span></span>    | <span data-ttu-id="2756d-138">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-138">December 31</span></span> | <span data-ttu-id="2756d-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="2756d-139">7,522.95</span></span>            | <span data-ttu-id="2756d-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="2756d-140">82,467.44</span></span>             |
| <span data-ttu-id="2756d-141">6</span><span class="sxs-lookup"><span data-stu-id="2756d-141">6</span></span>    | <span data-ttu-id="2756d-142">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-142">December 31</span></span> | <span data-ttu-id="2756d-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="2756d-143">10,184.06</span></span>           | <span data-ttu-id="2756d-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="2756d-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="2756d-145">Degressiv afskrivning</span><span class="sxs-lookup"><span data-stu-id="2756d-145">Digressive depreciation</span></span>
<span data-ttu-id="2756d-146">Værdien i feltet **Faktor** er mindre end **50**.</span><span class="sxs-lookup"><span data-stu-id="2756d-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2756d-147">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2756d-147">Example</span></span>

<span data-ttu-id="2756d-148">Anskaffelsesprisen er 100.000, faktoren er 20, levetiden er 10 år, og afskrivningen starter 1. januar.</span><span class="sxs-lookup"><span data-stu-id="2756d-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2756d-149">Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.</span><span class="sxs-lookup"><span data-stu-id="2756d-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2756d-150">År</span><span class="sxs-lookup"><span data-stu-id="2756d-150">Year</span></span> | <span data-ttu-id="2756d-151">Periode</span><span class="sxs-lookup"><span data-stu-id="2756d-151">Period</span></span>      | <span data-ttu-id="2756d-152">Afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="2756d-152">Depreciation amount</span></span> | <span data-ttu-id="2756d-153">Bogført nettoværdi – beløb</span><span class="sxs-lookup"><span data-stu-id="2756d-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2756d-154">1</span><span class="sxs-lookup"><span data-stu-id="2756d-154">1</span></span>    | <span data-ttu-id="2756d-155">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-155">December 31</span></span> | <span data-ttu-id="2756d-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="2756d-156">56,080.43</span></span>           | <span data-ttu-id="2756d-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="2756d-157">43,919.57</span></span>             |
| <span data-ttu-id="2756d-158">2</span><span class="sxs-lookup"><span data-stu-id="2756d-158">2</span></span>    | <span data-ttu-id="2756d-159">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-159">December 31</span></span> | <span data-ttu-id="2756d-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="2756d-160">10,665.70</span></span>           | <span data-ttu-id="2756d-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="2756d-161">33,253.87</span></span>             |
| <span data-ttu-id="2756d-162">3</span><span class="sxs-lookup"><span data-stu-id="2756d-162">3</span></span>    | <span data-ttu-id="2756d-163">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-163">December 31</span></span> | <span data-ttu-id="2756d-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="2756d-164">7,156.22</span></span>            | <span data-ttu-id="2756d-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="2756d-165">26,097.65</span></span>             |
| <span data-ttu-id="2756d-166">4</span><span class="sxs-lookup"><span data-stu-id="2756d-166">4</span></span>    | <span data-ttu-id="2756d-167">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-167">December 31</span></span> | <span data-ttu-id="2756d-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="2756d-168">5,538.06</span></span>            | <span data-ttu-id="2756d-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="2756d-169">20,559.59</span></span>             |
| <span data-ttu-id="2756d-170">5</span><span class="sxs-lookup"><span data-stu-id="2756d-170">5</span></span>    | <span data-ttu-id="2756d-171">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-171">December 31</span></span> | <span data-ttu-id="2756d-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="2756d-172">4,579.89</span></span>            | <span data-ttu-id="2756d-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="2756d-173">15,979.70</span></span>             |
| <span data-ttu-id="2756d-174">6</span><span class="sxs-lookup"><span data-stu-id="2756d-174">6</span></span>    | <span data-ttu-id="2756d-175">31. december</span><span class="sxs-lookup"><span data-stu-id="2756d-175">December 31</span></span> | <span data-ttu-id="2756d-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="2756d-176">3,937.36</span></span>            | <span data-ttu-id="2756d-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="2756d-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="2756d-178">Lineær afskrivning</span><span class="sxs-lookup"><span data-stu-id="2756d-178">Straight line depreciation</span></span>
<span data-ttu-id="2756d-179">Værdien i feltet **Faktor** er lig med **50**.</span><span class="sxs-lookup"><span data-stu-id="2756d-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="2756d-180">I dette tilfælde er afskrivningen den samme i hver periode, og derfor skal du overveje konsekvensen af de værdier, du har angivet i andre felter, som beskrevet i [Lineær afskrivning for levetiden](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="2756d-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>




