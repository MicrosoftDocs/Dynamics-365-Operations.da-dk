--- 
title: Oprette styklister (februar 2016)
description: "Denne opgave drejer sig om oprettelse af styklistestrukturen for et færdigt produkt og et halvfabrikatprodukt."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="a57e1-103">Oprette styklister (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="a57e1-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a57e1-104">Denne opgave drejer sig om oprettelse af styklistestrukturen for et færdigt produkt og et halvfabrikatprodukt.</span><span class="sxs-lookup"><span data-stu-id="a57e1-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="a57e1-105">Det er den fjerde opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="a57e1-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="a57e1-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="a57e1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="a57e1-107">Opret stykliste for et halvfabrikatprodukt</span><span class="sxs-lookup"><span data-stu-id="a57e1-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="a57e1-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="a57e1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a57e1-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a57e1-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a57e1-110">Vælg varenummer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a57e1-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="a57e1-111">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="a57e1-112">Klik på Styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="a57e1-112">Click BOM versions.</span></span>
5. <span data-ttu-id="a57e1-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a57e1-113">Click New.</span></span>
6. <span data-ttu-id="a57e1-114">Klik på Stykliste og Styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="a57e1-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="a57e1-115">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a57e1-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a57e1-116">Skriv f.eks. BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a57e1-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="a57e1-117">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="a57e1-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a57e1-118">Skriv eller vælg Sted 1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="a57e1-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="a57e1-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a57e1-119">Click OK.</span></span>
10. <span data-ttu-id="a57e1-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a57e1-120">Click New.</span></span>
11. <span data-ttu-id="a57e1-121">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="a57e1-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a57e1-122">I dette eksempel skal du skrive ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="a57e1-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="a57e1-123">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="a57e1-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a57e1-124">Skriv eller vælg 11 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="a57e1-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="a57e1-125">Klik på Overskrift.</span><span class="sxs-lookup"><span data-stu-id="a57e1-125">Click Header.</span></span>
14. <span data-ttu-id="a57e1-126">Klik på Godkendelse til at godkende styklister.</span><span class="sxs-lookup"><span data-stu-id="a57e1-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="a57e1-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a57e1-127">Click OK.</span></span>
16. <span data-ttu-id="a57e1-128">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="a57e1-128">Click Approve.</span></span>
    * <span data-ttu-id="a57e1-129">Knappen Godkend vises på værktøjslinjen i sektionen Styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="a57e1-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a57e1-130">Hvis det er usynligt, skal du klikke på sidehovedet øverst til højre på siden Styklister for at få vist Godkend.</span><span class="sxs-lookup"><span data-stu-id="a57e1-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="a57e1-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a57e1-131">Click OK.</span></span>
18. <span data-ttu-id="a57e1-132">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="a57e1-132">Click Activate.</span></span>
19. <span data-ttu-id="a57e1-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-133">Close the page.</span></span>
20. <span data-ttu-id="a57e1-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-134">Close the page.</span></span>
21. <span data-ttu-id="a57e1-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="a57e1-136">Opret stykliste for et færdigt produkt</span><span class="sxs-lookup"><span data-stu-id="a57e1-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="a57e1-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a57e1-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a57e1-138">Vælg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a57e1-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="a57e1-139">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="a57e1-140">Klik på Styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="a57e1-140">Click BOM versions.</span></span>
4. <span data-ttu-id="a57e1-141">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a57e1-141">Click New.</span></span>
5. <span data-ttu-id="a57e1-142">Klik på Stykliste og Styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="a57e1-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="a57e1-143">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a57e1-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a57e1-144">Skriv f.eks. BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a57e1-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="a57e1-145">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="a57e1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a57e1-146">Skriv eller vælg Sted 1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="a57e1-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="a57e1-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a57e1-147">Click OK.</span></span>
9. <span data-ttu-id="a57e1-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a57e1-148">Click New.</span></span>
10. <span data-ttu-id="a57e1-149">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="a57e1-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a57e1-150">I dette eksempel skal du skrive ITEM_A</span><span class="sxs-lookup"><span data-stu-id="a57e1-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="a57e1-151">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="a57e1-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a57e1-152">I dette eksempel skal du vælge 11.</span><span class="sxs-lookup"><span data-stu-id="a57e1-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="a57e1-153">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a57e1-153">Click New.</span></span>
13. <span data-ttu-id="a57e1-154">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="a57e1-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a57e1-155">I dette eksempel skal du skrive ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="a57e1-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="a57e1-156">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="a57e1-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a57e1-157">Skriv eller vælg 11 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="a57e1-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="a57e1-158">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a57e1-158">Click New.</span></span>
16. <span data-ttu-id="a57e1-159">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="a57e1-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a57e1-160">I dette eksempel skal du skrive BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a57e1-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="a57e1-161">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a57e1-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a57e1-162">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="a57e1-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a57e1-163">Skriv eller vælg lagersted 11 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="a57e1-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="a57e1-164">Klik på Overskrift.</span><span class="sxs-lookup"><span data-stu-id="a57e1-164">Click Header.</span></span>
20. <span data-ttu-id="a57e1-165">Klik på Godkendelse til at godkende styklister.</span><span class="sxs-lookup"><span data-stu-id="a57e1-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="a57e1-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a57e1-166">Click OK.</span></span>
22. <span data-ttu-id="a57e1-167">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="a57e1-167">Click Approve.</span></span>
    * <span data-ttu-id="a57e1-168">Knappen Godkend vises på værktøjslinjen i sektionen Styklisteversioner.</span><span class="sxs-lookup"><span data-stu-id="a57e1-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a57e1-169">Hvis det er usynligt, skal du klikke på sidehovedet øverst til højre på siden Styklister for at få vist Godkend.</span><span class="sxs-lookup"><span data-stu-id="a57e1-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="a57e1-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a57e1-170">Click OK.</span></span>
24. <span data-ttu-id="a57e1-171">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="a57e1-171">Click Activate.</span></span>
25. <span data-ttu-id="a57e1-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-172">Close the page.</span></span>
26. <span data-ttu-id="a57e1-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-173">Close the page.</span></span>
27. <span data-ttu-id="a57e1-174">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a57e1-174">Close the page.</span></span>


