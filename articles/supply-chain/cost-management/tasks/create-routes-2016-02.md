---
title: Oprette ruter (kun februar 2016)
description: Denne opgave drejer sig om oprettelse af produktionsruter for et færdigt produkt og et halvfabrikatprodukt.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63ad2cc0c41a5931750dffbfc64bc7ce965a1da4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563198"
---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="0e398-103">Oprette ruter (kun februar 2016)</span><span class="sxs-lookup"><span data-stu-id="0e398-103">Create routes (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e398-104">Denne opgave drejer sig om oprettelse af produktionsruter for et færdigt produkt og et halvfabrikatprodukt.</span><span class="sxs-lookup"><span data-stu-id="0e398-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="0e398-105">Det er den femte opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="0e398-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="0e398-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="0e398-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="0e398-107">Opret en rute for et halvfabrikatprodukt.</span><span class="sxs-lookup"><span data-stu-id="0e398-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="0e398-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="0e398-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0e398-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0e398-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0e398-110">Vælg varenummer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="0e398-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="0e398-111">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e398-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="0e398-112">Klik på Rute.</span><span class="sxs-lookup"><span data-stu-id="0e398-112">Click Route.</span></span>
5. <span data-ttu-id="0e398-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e398-113">Click New.</span></span>
6. <span data-ttu-id="0e398-114">Klik på Rute og ruteversion.</span><span class="sxs-lookup"><span data-stu-id="0e398-114">Click Route and route version.</span></span>
7. <span data-ttu-id="0e398-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0e398-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0e398-116">I dette eksempel skal du skrive ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="0e398-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="0e398-117">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="0e398-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-118">Skriv eller vælg Sted 1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="0e398-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e398-119">Click OK.</span></span>
10. <span data-ttu-id="0e398-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e398-120">Click New.</span></span>
11. <span data-ttu-id="0e398-121">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="0e398-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-122">Vælg Assembly i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="0e398-123">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="0e398-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="0e398-124">Skriv for eksempel 1.</span><span class="sxs-lookup"><span data-stu-id="0e398-124">For example, type 1.</span></span> <span data-ttu-id="0e398-125">Kørselstider er ofte en del af den pris, der beregnes for en vare.</span><span class="sxs-lookup"><span data-stu-id="0e398-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="0e398-126">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="0e398-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-127">Vælg Std. i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="0e398-128">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="0e398-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="0e398-129">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="0e398-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-130">Vælg Assembly i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="0e398-131">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="0e398-131">Click the Times tab.</span></span>
17. <span data-ttu-id="0e398-132">Angiv et tal i feltet Opstillingstid.</span><span class="sxs-lookup"><span data-stu-id="0e398-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="0e398-133">I dette eksempel skal du skrive 1.</span><span class="sxs-lookup"><span data-stu-id="0e398-133">For this example, type 1.</span></span> <span data-ttu-id="0e398-134">Opstillingstider er ofte en del af den pris, der beregnes for en vare.</span><span class="sxs-lookup"><span data-stu-id="0e398-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="0e398-135">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e398-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="0e398-136">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="0e398-136">Click Approve.</span></span>
20. <span data-ttu-id="0e398-137">Vælg Ja til Vil du også godkende ruten? .</span><span class="sxs-lookup"><span data-stu-id="0e398-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="0e398-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e398-138">Click OK.</span></span>
22. <span data-ttu-id="0e398-139">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e398-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="0e398-140">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="0e398-140">Click Activate.</span></span>
24. <span data-ttu-id="0e398-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e398-141">Close the page.</span></span>
25. <span data-ttu-id="0e398-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e398-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="0e398-143">Oprette en rute for et færdigt produkt</span><span class="sxs-lookup"><span data-stu-id="0e398-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="0e398-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0e398-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0e398-145">Vælg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="0e398-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="0e398-146">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e398-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="0e398-147">Klik på Rute.</span><span class="sxs-lookup"><span data-stu-id="0e398-147">Click Route.</span></span>
4. <span data-ttu-id="0e398-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e398-148">Click New.</span></span>
5. <span data-ttu-id="0e398-149">Klik på Rute og ruteversion.</span><span class="sxs-lookup"><span data-stu-id="0e398-149">Click Route and route version.</span></span>
6. <span data-ttu-id="0e398-150">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0e398-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0e398-151">I dette eksempel skal du skrive ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="0e398-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="0e398-152">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="0e398-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-153">Skriv eller vælg Sted 1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="0e398-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e398-154">Click OK.</span></span>
9. <span data-ttu-id="0e398-155">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0e398-155">Click New.</span></span>
10. <span data-ttu-id="0e398-156">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="0e398-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-157">Vælg Emballage i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="0e398-158">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="0e398-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="0e398-159">I dette eksempel skal du skrive 1.</span><span class="sxs-lookup"><span data-stu-id="0e398-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="0e398-160">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="0e398-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-161">Vælg Std. i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="0e398-162">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="0e398-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="0e398-163">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="0e398-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0e398-164">Vælg Emballage i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0e398-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="0e398-165">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="0e398-165">Click the Times tab.</span></span>
16. <span data-ttu-id="0e398-166">Angiv et tal i feltet Opstillingstid.</span><span class="sxs-lookup"><span data-stu-id="0e398-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="0e398-167">I dette eksempel skal du skrive 1.</span><span class="sxs-lookup"><span data-stu-id="0e398-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="0e398-168">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e398-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="0e398-169">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="0e398-169">Click Approve.</span></span>
19. <span data-ttu-id="0e398-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e398-170">Click OK.</span></span>
20. <span data-ttu-id="0e398-171">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e398-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="0e398-172">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="0e398-172">Click Activate.</span></span>
22. <span data-ttu-id="0e398-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e398-173">Close the page.</span></span>
23. <span data-ttu-id="0e398-174">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e398-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="0e398-175">Aktiver automatisk forbrug af opstillingstid</span><span class="sxs-lookup"><span data-stu-id="0e398-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="0e398-176">Gå til Produktionsstyring > Konfiguration > Ruter > Rutegrupper.</span><span class="sxs-lookup"><span data-stu-id="0e398-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="0e398-177">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0e398-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0e398-178">Vælg Std. på listen.</span><span class="sxs-lookup"><span data-stu-id="0e398-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="0e398-179">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0e398-179">Click Edit.</span></span>
4. <span data-ttu-id="0e398-180">Vælg Ja i feltet Opstillingstid.</span><span class="sxs-lookup"><span data-stu-id="0e398-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="0e398-181">Opstillingstider er ofte en del af den pris, der beregnes for en vare.</span><span class="sxs-lookup"><span data-stu-id="0e398-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="0e398-182">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0e398-182">Click Save.</span></span>
6. <span data-ttu-id="0e398-183">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e398-183">Close the page.</span></span>

