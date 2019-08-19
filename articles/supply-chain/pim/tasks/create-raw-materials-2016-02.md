---
title: Oprette råvarer (februar 2016)
description: Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844579"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="e5f50-103">Oprette råvarer (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="e5f50-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5f50-104">Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter.</span><span class="sxs-lookup"><span data-stu-id="e5f50-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="e5f50-105">Det er den tredje opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="e5f50-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="e5f50-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="e5f50-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="e5f50-107">Opret det første materiale</span><span class="sxs-lookup"><span data-stu-id="e5f50-107">Create the first material</span></span>
1. <span data-ttu-id="e5f50-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="e5f50-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e5f50-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5f50-109">Click New.</span></span>
3. <span data-ttu-id="e5f50-110">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="e5f50-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e5f50-111">Skriv ITEM_A i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e5f50-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="e5f50-112">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-113">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="e5f50-113">Select STD.</span></span> <span data-ttu-id="e5f50-114">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e5f50-115">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-116">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="e5f50-116">For example, select Audio.</span></span> <span data-ttu-id="e5f50-117">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e5f50-118">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-119">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e5f50-119">Select SiteWH.</span></span> <span data-ttu-id="e5f50-120">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e5f50-121">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-122">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e5f50-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e5f50-123">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-123">Select None.</span></span>  
8. <span data-ttu-id="e5f50-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5f50-124">Click OK.</span></span>
9. <span data-ttu-id="e5f50-125">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e5f50-126">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="e5f50-126">Click Default order settings.</span></span>
11. <span data-ttu-id="e5f50-127">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="e5f50-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-128">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e5f50-129">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="e5f50-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-130">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e5f50-131">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="e5f50-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-132">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e5f50-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-133">Close the page.</span></span>
15. <span data-ttu-id="e5f50-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-134">Close the page.</span></span>
16. <span data-ttu-id="e5f50-135">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e5f50-136">Klik på ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="e5f50-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="e5f50-137">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="e5f50-138">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e5f50-139">I dette eksempel skal du skrive M2.</span><span class="sxs-lookup"><span data-stu-id="e5f50-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="e5f50-140">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="e5f50-141">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="e5f50-141">Click Item price.</span></span>
21. <span data-ttu-id="e5f50-142">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5f50-142">Click New.</span></span>
22. <span data-ttu-id="e5f50-143">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="e5f50-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-144">I dette eksempel skal du vælge 10, som er en omkostningstype for standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="e5f50-145">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="e5f50-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-146">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="e5f50-147">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="e5f50-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e5f50-148">I dette eksempel skal du skrive 10.</span><span class="sxs-lookup"><span data-stu-id="e5f50-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="e5f50-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e5f50-149">Click Save.</span></span>
26. <span data-ttu-id="e5f50-150">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="e5f50-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="e5f50-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-151">Close the page.</span></span>
28. <span data-ttu-id="e5f50-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="e5f50-153">Opret det andet materiale</span><span class="sxs-lookup"><span data-stu-id="e5f50-153">Create the second material</span></span>
1. <span data-ttu-id="e5f50-154">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5f50-154">Click New.</span></span>
2. <span data-ttu-id="e5f50-155">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="e5f50-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e5f50-156">I dette eksempel skal du skrive ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="e5f50-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="e5f50-157">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-158">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="e5f50-158">Select STD.</span></span> <span data-ttu-id="e5f50-159">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="e5f50-160">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-161">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="e5f50-161">For example, select Audio.</span></span> <span data-ttu-id="e5f50-162">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="e5f50-163">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-164">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e5f50-164">Select SiteWH.</span></span> <span data-ttu-id="e5f50-165">Kun lokalitet og lagersted bruges til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e5f50-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="e5f50-166">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-167">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e5f50-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e5f50-168">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-168">Select None.</span></span>  
7. <span data-ttu-id="e5f50-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5f50-169">Click OK.</span></span>
8. <span data-ttu-id="e5f50-170">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="e5f50-171">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="e5f50-171">Click Default order settings.</span></span>
10. <span data-ttu-id="e5f50-172">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="e5f50-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-173">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="e5f50-174">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="e5f50-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-175">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e5f50-176">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="e5f50-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-177">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e5f50-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-178">Close the page.</span></span>
14. <span data-ttu-id="e5f50-179">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-179">Close the page.</span></span>
15. <span data-ttu-id="e5f50-180">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e5f50-181">Klik på ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="e5f50-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="e5f50-182">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="e5f50-183">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e5f50-184">I dette eksempel skal du skrive M2.</span><span class="sxs-lookup"><span data-stu-id="e5f50-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="e5f50-185">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="e5f50-186">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="e5f50-186">Click Item price.</span></span>
20. <span data-ttu-id="e5f50-187">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5f50-187">Click New.</span></span>
21. <span data-ttu-id="e5f50-188">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="e5f50-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-189">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="e5f50-189">For this example, select 10.</span></span> <span data-ttu-id="e5f50-190">Dette er omkostningstypen for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="e5f50-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="e5f50-191">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="e5f50-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-192">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="e5f50-193">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="e5f50-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e5f50-194">Skriv 10 i demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="e5f50-195">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e5f50-195">Click Save.</span></span>
25. <span data-ttu-id="e5f50-196">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="e5f50-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="e5f50-197">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-197">Close the page.</span></span>
27. <span data-ttu-id="e5f50-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="e5f50-199">Opret det tredje materiale</span><span class="sxs-lookup"><span data-stu-id="e5f50-199">Create the third material</span></span>
1. <span data-ttu-id="e5f50-200">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5f50-200">Click New.</span></span>
2. <span data-ttu-id="e5f50-201">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="e5f50-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e5f50-202">Skriv ITEM_C i demonstrationen</span><span class="sxs-lookup"><span data-stu-id="e5f50-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="e5f50-203">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-204">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="e5f50-204">Select STD.</span></span> <span data-ttu-id="e5f50-205">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="e5f50-206">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-207">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="e5f50-207">For example, select Audio.</span></span> <span data-ttu-id="e5f50-208">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="e5f50-209">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-210">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e5f50-210">Select SiteWH.</span></span> <span data-ttu-id="e5f50-211">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="e5f50-212">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-213">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="e5f50-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e5f50-214">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-214">Select None.</span></span>  
7. <span data-ttu-id="e5f50-215">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5f50-215">Click OK.</span></span>
8. <span data-ttu-id="e5f50-216">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="e5f50-217">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="e5f50-217">Click Default order settings.</span></span>
10. <span data-ttu-id="e5f50-218">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="e5f50-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-219">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="e5f50-220">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="e5f50-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-221">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e5f50-222">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="e5f50-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-223">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e5f50-224">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-224">Close the page.</span></span>
14. <span data-ttu-id="e5f50-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-225">Close the page.</span></span>
15. <span data-ttu-id="e5f50-226">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e5f50-227">Klik på ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="e5f50-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="e5f50-228">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5f50-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="e5f50-229">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5f50-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e5f50-230">I dette eksempel skal du skrive M1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="e5f50-231">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="e5f50-232">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="e5f50-232">Click Item price.</span></span>
20. <span data-ttu-id="e5f50-233">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e5f50-233">Click New.</span></span>
21. <span data-ttu-id="e5f50-234">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="e5f50-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-235">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="e5f50-235">For this example, select 10.</span></span> <span data-ttu-id="e5f50-236">Dette er omkostningstypen for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="e5f50-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="e5f50-237">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="e5f50-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e5f50-238">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="e5f50-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="e5f50-239">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="e5f50-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e5f50-240">I dette eksempel skal du skrive 10.</span><span class="sxs-lookup"><span data-stu-id="e5f50-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="e5f50-241">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e5f50-241">Click Save.</span></span>
25. <span data-ttu-id="e5f50-242">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="e5f50-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="e5f50-243">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-243">Close the page.</span></span>
27. <span data-ttu-id="e5f50-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-244">Close the page.</span></span>

