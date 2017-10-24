--- 
title: "Oprette råmaterialer (kun februar 2016)"
description: "Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="f0a4c-103">Oprette råmaterialer (kun februar 2016)</span><span class="sxs-lookup"><span data-stu-id="f0a4c-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0a4c-104">Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="f0a4c-105">Det er den tredje opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="f0a4c-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="f0a4c-107">Opret det første materiale</span><span class="sxs-lookup"><span data-stu-id="f0a4c-107">Create the first material</span></span>
1. <span data-ttu-id="f0a4c-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f0a4c-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-109">Click New.</span></span>
3. <span data-ttu-id="f0a4c-110">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f0a4c-111">Skriv ITEM_A i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="f0a4c-112">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-113">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-113">Select STD.</span></span> <span data-ttu-id="f0a4c-114">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f0a4c-115">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-116">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-116">For example, select Audio.</span></span> <span data-ttu-id="f0a4c-117">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f0a4c-118">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-119">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-119">Select SiteWH.</span></span> <span data-ttu-id="f0a4c-120">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="f0a4c-121">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-122">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f0a4c-123">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-123">Select None.</span></span>  
8. <span data-ttu-id="f0a4c-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-124">Click OK.</span></span>
9. <span data-ttu-id="f0a4c-125">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f0a4c-126">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-126">Click Default order settings.</span></span>
11. <span data-ttu-id="f0a4c-127">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-128">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f0a4c-129">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-130">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f0a4c-131">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-132">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f0a4c-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-133">Close the page.</span></span>
15. <span data-ttu-id="f0a4c-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-134">Close the page.</span></span>
16. <span data-ttu-id="f0a4c-135">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f0a4c-136">Klik på ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="f0a4c-137">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="f0a4c-138">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f0a4c-139">I dette eksempel skal du skrive M2.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="f0a4c-140">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="f0a4c-141">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-141">Click Item price.</span></span>
21. <span data-ttu-id="f0a4c-142">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-142">Click New.</span></span>
22. <span data-ttu-id="f0a4c-143">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-144">I dette eksempel skal du vælge 10, som er en omkostningstype for standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="f0a4c-145">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-146">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="f0a4c-147">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f0a4c-148">I dette eksempel skal du skrive 10.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="f0a4c-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-149">Click Save.</span></span>
26. <span data-ttu-id="f0a4c-150">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f0a4c-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="f0a4c-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-151">Close the page.</span></span>
28. <span data-ttu-id="f0a4c-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="f0a4c-153">Opret det andet materiale</span><span class="sxs-lookup"><span data-stu-id="f0a4c-153">Create the second material</span></span>
1. <span data-ttu-id="f0a4c-154">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-154">Click New.</span></span>
2. <span data-ttu-id="f0a4c-155">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f0a4c-156">I dette eksempel skal du skrive ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="f0a4c-157">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-158">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-158">Select STD.</span></span> <span data-ttu-id="f0a4c-159">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f0a4c-160">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-161">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-161">For example, select Audio.</span></span> <span data-ttu-id="f0a4c-162">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f0a4c-163">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-164">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-164">Select SiteWH.</span></span> <span data-ttu-id="f0a4c-165">Kun lokalitet og lagersted bruges til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="f0a4c-166">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-167">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f0a4c-168">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-168">Select None.</span></span>  
7. <span data-ttu-id="f0a4c-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-169">Click OK.</span></span>
8. <span data-ttu-id="f0a4c-170">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f0a4c-171">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-171">Click Default order settings.</span></span>
10. <span data-ttu-id="f0a4c-172">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-173">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f0a4c-174">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-175">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f0a4c-176">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-177">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f0a4c-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-178">Close the page.</span></span>
14. <span data-ttu-id="f0a4c-179">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-179">Close the page.</span></span>
15. <span data-ttu-id="f0a4c-180">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f0a4c-181">Klik på ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="f0a4c-182">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f0a4c-183">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f0a4c-184">I dette eksempel skal du skrive M2.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="f0a4c-185">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f0a4c-186">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-186">Click Item price.</span></span>
20. <span data-ttu-id="f0a4c-187">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-187">Click New.</span></span>
21. <span data-ttu-id="f0a4c-188">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-189">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-189">For this example, select 10.</span></span> <span data-ttu-id="f0a4c-190">Dette er omkostningstypen for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="f0a4c-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f0a4c-191">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-192">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f0a4c-193">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f0a4c-194">Skriv 10 i demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="f0a4c-195">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-195">Click Save.</span></span>
25. <span data-ttu-id="f0a4c-196">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f0a4c-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f0a4c-197">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-197">Close the page.</span></span>
27. <span data-ttu-id="f0a4c-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="f0a4c-199">Opret det tredje materiale</span><span class="sxs-lookup"><span data-stu-id="f0a4c-199">Create the third material</span></span>
1. <span data-ttu-id="f0a4c-200">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-200">Click New.</span></span>
2. <span data-ttu-id="f0a4c-201">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f0a4c-202">Skriv ITEM_C i demonstrationen</span><span class="sxs-lookup"><span data-stu-id="f0a4c-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="f0a4c-203">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-204">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-204">Select STD.</span></span> <span data-ttu-id="f0a4c-205">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f0a4c-206">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-207">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-207">For example, select Audio.</span></span> <span data-ttu-id="f0a4c-208">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f0a4c-209">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-210">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-210">Select SiteWH.</span></span> <span data-ttu-id="f0a4c-211">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="f0a4c-212">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-213">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f0a4c-214">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-214">Select None.</span></span>  
7. <span data-ttu-id="f0a4c-215">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-215">Click OK.</span></span>
8. <span data-ttu-id="f0a4c-216">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f0a4c-217">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-217">Click Default order settings.</span></span>
10. <span data-ttu-id="f0a4c-218">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-219">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f0a4c-220">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-221">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f0a4c-222">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-223">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f0a4c-224">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-224">Close the page.</span></span>
14. <span data-ttu-id="f0a4c-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-225">Close the page.</span></span>
15. <span data-ttu-id="f0a4c-226">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f0a4c-227">Klik på ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="f0a4c-228">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f0a4c-229">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f0a4c-230">I dette eksempel skal du skrive M1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="f0a4c-231">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f0a4c-232">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-232">Click Item price.</span></span>
20. <span data-ttu-id="f0a4c-233">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-233">Click New.</span></span>
21. <span data-ttu-id="f0a4c-234">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-235">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-235">For this example, select 10.</span></span> <span data-ttu-id="f0a4c-236">Dette er omkostningstypen for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="f0a4c-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f0a4c-237">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0a4c-238">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f0a4c-239">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f0a4c-240">I dette eksempel skal du skrive 10.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="f0a4c-241">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-241">Click Save.</span></span>
25. <span data-ttu-id="f0a4c-242">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f0a4c-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f0a4c-243">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-243">Close the page.</span></span>
27. <span data-ttu-id="f0a4c-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f0a4c-244">Close the page.</span></span>


