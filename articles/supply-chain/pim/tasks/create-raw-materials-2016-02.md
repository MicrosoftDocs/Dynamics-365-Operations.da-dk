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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552664"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="355f1-103">Oprette råvarer (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="355f1-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="355f1-104">Denne opgave drejer sig om oprettelse af færdige produkter og halvfabrikataprodukter.</span><span class="sxs-lookup"><span data-stu-id="355f1-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="355f1-105">Det er den tredje opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="355f1-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="355f1-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="355f1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="355f1-107">Opret det første materiale</span><span class="sxs-lookup"><span data-stu-id="355f1-107">Create the first material</span></span>
1. <span data-ttu-id="355f1-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="355f1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="355f1-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="355f1-109">Click New.</span></span>
3. <span data-ttu-id="355f1-110">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="355f1-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="355f1-111">Skriv ITEM_A i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="355f1-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="355f1-112">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-113">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="355f1-113">Select STD.</span></span> <span data-ttu-id="355f1-114">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="355f1-115">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-116">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="355f1-116">For example, select Audio.</span></span> <span data-ttu-id="355f1-117">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="355f1-118">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-119">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="355f1-119">Select SiteWH.</span></span> <span data-ttu-id="355f1-120">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="355f1-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="355f1-121">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-122">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="355f1-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="355f1-123">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="355f1-123">Select None.</span></span>  
8. <span data-ttu-id="355f1-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="355f1-124">Click OK.</span></span>
9. <span data-ttu-id="355f1-125">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="355f1-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="355f1-126">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="355f1-126">Click Default order settings.</span></span>
11. <span data-ttu-id="355f1-127">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="355f1-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-128">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="355f1-129">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="355f1-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-130">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="355f1-131">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="355f1-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-132">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="355f1-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-133">Close the page.</span></span>
15. <span data-ttu-id="355f1-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-134">Close the page.</span></span>
16. <span data-ttu-id="355f1-135">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="355f1-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="355f1-136">Klik på ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="355f1-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="355f1-137">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="355f1-138">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="355f1-139">I dette eksempel skal du skrive M2.</span><span class="sxs-lookup"><span data-stu-id="355f1-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="355f1-140">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="355f1-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="355f1-141">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="355f1-141">Click Item price.</span></span>
21. <span data-ttu-id="355f1-142">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="355f1-142">Click New.</span></span>
22. <span data-ttu-id="355f1-143">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="355f1-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-144">I dette eksempel skal du vælge 10, som er en omkostningstype for standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="355f1-145">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="355f1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-146">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="355f1-147">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="355f1-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="355f1-148">I dette eksempel skal du skrive 10.</span><span class="sxs-lookup"><span data-stu-id="355f1-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="355f1-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="355f1-149">Click Save.</span></span>
26. <span data-ttu-id="355f1-150">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="355f1-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="355f1-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-151">Close the page.</span></span>
28. <span data-ttu-id="355f1-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="355f1-153">Opret det andet materiale</span><span class="sxs-lookup"><span data-stu-id="355f1-153">Create the second material</span></span>
1. <span data-ttu-id="355f1-154">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="355f1-154">Click New.</span></span>
2. <span data-ttu-id="355f1-155">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="355f1-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="355f1-156">I dette eksempel skal du skrive ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="355f1-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="355f1-157">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-158">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="355f1-158">Select STD.</span></span> <span data-ttu-id="355f1-159">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="355f1-160">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-161">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="355f1-161">For example, select Audio.</span></span> <span data-ttu-id="355f1-162">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="355f1-163">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-164">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="355f1-164">Select SiteWH.</span></span> <span data-ttu-id="355f1-165">Kun lokalitet og lagersted bruges til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="355f1-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="355f1-166">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-167">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="355f1-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="355f1-168">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="355f1-168">Select None.</span></span>  
7. <span data-ttu-id="355f1-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="355f1-169">Click OK.</span></span>
8. <span data-ttu-id="355f1-170">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="355f1-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="355f1-171">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="355f1-171">Click Default order settings.</span></span>
10. <span data-ttu-id="355f1-172">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="355f1-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-173">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="355f1-174">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="355f1-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-175">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="355f1-176">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="355f1-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-177">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="355f1-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-178">Close the page.</span></span>
14. <span data-ttu-id="355f1-179">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-179">Close the page.</span></span>
15. <span data-ttu-id="355f1-180">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="355f1-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="355f1-181">Klik på ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="355f1-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="355f1-182">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="355f1-183">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="355f1-184">I dette eksempel skal du skrive M2.</span><span class="sxs-lookup"><span data-stu-id="355f1-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="355f1-185">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="355f1-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="355f1-186">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="355f1-186">Click Item price.</span></span>
20. <span data-ttu-id="355f1-187">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="355f1-187">Click New.</span></span>
21. <span data-ttu-id="355f1-188">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="355f1-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-189">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="355f1-189">For this example, select 10.</span></span> <span data-ttu-id="355f1-190">Dette er omkostningstypen for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="355f1-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="355f1-191">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="355f1-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-192">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="355f1-193">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="355f1-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="355f1-194">Skriv 10 i demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="355f1-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="355f1-195">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="355f1-195">Click Save.</span></span>
25. <span data-ttu-id="355f1-196">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="355f1-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="355f1-197">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-197">Close the page.</span></span>
27. <span data-ttu-id="355f1-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="355f1-199">Opret det tredje materiale</span><span class="sxs-lookup"><span data-stu-id="355f1-199">Create the third material</span></span>
1. <span data-ttu-id="355f1-200">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="355f1-200">Click New.</span></span>
2. <span data-ttu-id="355f1-201">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="355f1-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="355f1-202">Skriv ITEM_C i demonstrationen</span><span class="sxs-lookup"><span data-stu-id="355f1-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="355f1-203">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-204">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="355f1-204">Select STD.</span></span> <span data-ttu-id="355f1-205">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="355f1-206">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-207">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="355f1-207">For example, select Audio.</span></span> <span data-ttu-id="355f1-208">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="355f1-209">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-210">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="355f1-210">Select SiteWH.</span></span> <span data-ttu-id="355f1-211">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="355f1-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="355f1-212">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-213">Sporingsdimensioner bliver ikke brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="355f1-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="355f1-214">Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="355f1-214">Select None.</span></span>  
7. <span data-ttu-id="355f1-215">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="355f1-215">Click OK.</span></span>
8. <span data-ttu-id="355f1-216">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="355f1-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="355f1-217">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="355f1-217">Click Default order settings.</span></span>
10. <span data-ttu-id="355f1-218">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="355f1-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-219">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="355f1-220">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="355f1-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-221">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="355f1-222">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="355f1-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-223">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="355f1-224">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-224">Close the page.</span></span>
14. <span data-ttu-id="355f1-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-225">Close the page.</span></span>
15. <span data-ttu-id="355f1-226">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="355f1-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="355f1-227">Klik på ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="355f1-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="355f1-228">Udvid sektionen Administrer omkostninger.</span><span class="sxs-lookup"><span data-stu-id="355f1-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="355f1-229">Skriv en værdi i feltet Omkostningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="355f1-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="355f1-230">I dette eksempel skal du skrive M1.</span><span class="sxs-lookup"><span data-stu-id="355f1-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="355f1-231">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="355f1-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="355f1-232">Klik på Varepris.</span><span class="sxs-lookup"><span data-stu-id="355f1-232">Click Item price.</span></span>
20. <span data-ttu-id="355f1-233">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="355f1-233">Click New.</span></span>
21. <span data-ttu-id="355f1-234">Indtast eller vælg en værdi i feltet Version.</span><span class="sxs-lookup"><span data-stu-id="355f1-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-235">I dette eksempel skal du vælge 10.</span><span class="sxs-lookup"><span data-stu-id="355f1-235">For this example, select 10.</span></span> <span data-ttu-id="355f1-236">Dette er omkostningstypen for standardomkostninger</span><span class="sxs-lookup"><span data-stu-id="355f1-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="355f1-237">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="355f1-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="355f1-238">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="355f1-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="355f1-239">Angiv et tal i feltet Pris.</span><span class="sxs-lookup"><span data-stu-id="355f1-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="355f1-240">I dette eksempel skal du skrive 10.</span><span class="sxs-lookup"><span data-stu-id="355f1-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="355f1-241">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="355f1-241">Click Save.</span></span>
25. <span data-ttu-id="355f1-242">Klik på Aktivér afventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="355f1-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="355f1-243">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-243">Close the page.</span></span>
27. <span data-ttu-id="355f1-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="355f1-244">Close the page.</span></span>

