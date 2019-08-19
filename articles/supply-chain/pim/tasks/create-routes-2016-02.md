---
title: Opret ruter (februar 2016)
description: Denne opgave drejer sig om oprettelse af produktionsruter for et færdigt produkt og et halvfabrikatprodukt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844555"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="c5256-103">Opret ruter (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="c5256-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5256-104">Denne opgave drejer sig om oprettelse af produktionsruter for et færdigt produkt og et halvfabrikatprodukt.</span><span class="sxs-lookup"><span data-stu-id="c5256-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="c5256-105">Det er den femte opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="c5256-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="c5256-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c5256-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="c5256-107">Opret en rute for et halvfabrikatprodukt.</span><span class="sxs-lookup"><span data-stu-id="c5256-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="c5256-108">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="c5256-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c5256-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c5256-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c5256-110">Vælg varenummer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="c5256-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="c5256-111">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5256-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="c5256-112">Klik på Rute.</span><span class="sxs-lookup"><span data-stu-id="c5256-112">Click Route.</span></span>
5. <span data-ttu-id="c5256-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c5256-113">Click New.</span></span>
6. <span data-ttu-id="c5256-114">Klik på Rute og ruteversion.</span><span class="sxs-lookup"><span data-stu-id="c5256-114">Click Route and route version.</span></span>
7. <span data-ttu-id="c5256-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c5256-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c5256-116">I dette eksempel skal du skrive ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="c5256-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="c5256-117">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="c5256-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-118">Skriv eller vælg Sted 1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="c5256-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5256-119">Click OK.</span></span>
10. <span data-ttu-id="c5256-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c5256-120">Click New.</span></span>
11. <span data-ttu-id="c5256-121">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="c5256-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-122">Vælg Assembly i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="c5256-123">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="c5256-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="c5256-124">Skriv for eksempel 1.</span><span class="sxs-lookup"><span data-stu-id="c5256-124">For example, type 1.</span></span> <span data-ttu-id="c5256-125">Kørselstider er ofte en del af den pris, der beregnes for en vare.</span><span class="sxs-lookup"><span data-stu-id="c5256-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="c5256-126">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="c5256-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-127">Vælg Std. i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="c5256-128">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="c5256-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="c5256-129">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="c5256-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-130">Vælg Assembly i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="c5256-131">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="c5256-131">Click the Times tab.</span></span>
17. <span data-ttu-id="c5256-132">Angiv et tal i feltet Opstillingstid.</span><span class="sxs-lookup"><span data-stu-id="c5256-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="c5256-133">I dette eksempel skal du skrive 1.</span><span class="sxs-lookup"><span data-stu-id="c5256-133">For this example, type 1.</span></span> <span data-ttu-id="c5256-134">Opstillingstider er ofte en del af den pris, der beregnes for en vare.</span><span class="sxs-lookup"><span data-stu-id="c5256-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="c5256-135">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5256-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="c5256-136">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="c5256-136">Click Approve.</span></span>
20. <span data-ttu-id="c5256-137">Vælg Ja til Vil du også godkende ruten? .</span><span class="sxs-lookup"><span data-stu-id="c5256-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="c5256-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5256-138">Click OK.</span></span>
22. <span data-ttu-id="c5256-139">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5256-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="c5256-140">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="c5256-140">Click Activate.</span></span>
24. <span data-ttu-id="c5256-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5256-141">Close the page.</span></span>
25. <span data-ttu-id="c5256-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5256-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="c5256-143">Oprette en rute for et færdigt produkt</span><span class="sxs-lookup"><span data-stu-id="c5256-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="c5256-144">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c5256-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c5256-145">Vælg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="c5256-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="c5256-146">Klik på Tekniker i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5256-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="c5256-147">Klik på Rute.</span><span class="sxs-lookup"><span data-stu-id="c5256-147">Click Route.</span></span>
4. <span data-ttu-id="c5256-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c5256-148">Click New.</span></span>
5. <span data-ttu-id="c5256-149">Klik på Rute og ruteversion.</span><span class="sxs-lookup"><span data-stu-id="c5256-149">Click Route and route version.</span></span>
6. <span data-ttu-id="c5256-150">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c5256-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c5256-151">I dette eksempel skal du skrive ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="c5256-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="c5256-152">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="c5256-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-153">Skriv eller vælg Sted 1 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="c5256-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5256-154">Click OK.</span></span>
9. <span data-ttu-id="c5256-155">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c5256-155">Click New.</span></span>
10. <span data-ttu-id="c5256-156">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="c5256-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-157">Vælg Emballage i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="c5256-158">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="c5256-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="c5256-159">I dette eksempel skal du skrive 1.</span><span class="sxs-lookup"><span data-stu-id="c5256-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="c5256-160">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="c5256-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-161">Vælg Std. i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="c5256-162">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="c5256-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="c5256-163">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="c5256-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="c5256-164">Vælg Emballage i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5256-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="c5256-165">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="c5256-165">Click the Times tab.</span></span>
16. <span data-ttu-id="c5256-166">Angiv et tal i feltet Opstillingstid.</span><span class="sxs-lookup"><span data-stu-id="c5256-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="c5256-167">I dette eksempel skal du skrive 1.</span><span class="sxs-lookup"><span data-stu-id="c5256-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="c5256-168">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5256-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="c5256-169">Klik på Godkend.</span><span class="sxs-lookup"><span data-stu-id="c5256-169">Click Approve.</span></span>
19. <span data-ttu-id="c5256-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5256-170">Click OK.</span></span>
20. <span data-ttu-id="c5256-171">Klik på Ruteversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5256-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="c5256-172">Klik på Aktiver.</span><span class="sxs-lookup"><span data-stu-id="c5256-172">Click Activate.</span></span>
22. <span data-ttu-id="c5256-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5256-173">Close the page.</span></span>
23. <span data-ttu-id="c5256-174">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5256-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="c5256-175">Aktiver automatisk forbrug af opstillingstid</span><span class="sxs-lookup"><span data-stu-id="c5256-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="c5256-176">Gå til Produktionsstyring > Konfiguration > Ruter > Rutegrupper.</span><span class="sxs-lookup"><span data-stu-id="c5256-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="c5256-177">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c5256-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c5256-178">Vælg Std. på listen.</span><span class="sxs-lookup"><span data-stu-id="c5256-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="c5256-179">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="c5256-179">Click Edit.</span></span>
4. <span data-ttu-id="c5256-180">Vælg Ja i feltet Opstillingstid.</span><span class="sxs-lookup"><span data-stu-id="c5256-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="c5256-181">Opstillingstider er ofte en del af den pris, der beregnes for en vare.</span><span class="sxs-lookup"><span data-stu-id="c5256-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="c5256-182">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c5256-182">Click Save.</span></span>
6. <span data-ttu-id="c5256-183">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5256-183">Close the page.</span></span>

