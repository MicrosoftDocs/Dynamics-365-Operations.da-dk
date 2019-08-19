---
title: Oprette en materialeplan for samprodukter
description: Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e59ff769685677b0970dbc7d4c9d4d2c1e5b63d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835952"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="de35e-103">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="de35e-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de35e-104">Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.</span><span class="sxs-lookup"><span data-stu-id="de35e-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="de35e-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="de35e-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="de35e-106">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="de35e-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="de35e-107">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="de35e-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="de35e-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="de35e-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="de35e-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="de35e-109">Click New.</span></span>
4. <span data-ttu-id="de35e-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="de35e-110">Click Sales order.</span></span>
5. <span data-ttu-id="de35e-111">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="de35e-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="de35e-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="de35e-112">Example: US-001</span></span>  
6. <span data-ttu-id="de35e-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de35e-113">Click OK.</span></span>
7. <span data-ttu-id="de35e-114">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="de35e-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="de35e-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="de35e-115">Example: P6003</span></span>  
8. <span data-ttu-id="de35e-116">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="de35e-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="de35e-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="de35e-117">Example: 50000</span></span>  
9. <span data-ttu-id="de35e-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="de35e-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="de35e-119">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="de35e-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="de35e-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="de35e-120">Close the page.</span></span>
2. <span data-ttu-id="de35e-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="de35e-121">Close the page.</span></span>
3. <span data-ttu-id="de35e-122">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="de35e-122">Click Master planning.</span></span>
4. <span data-ttu-id="de35e-123">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="de35e-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="de35e-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="de35e-125">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="de35e-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="de35e-126">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="de35e-126">Click Run.</span></span>
7. <span data-ttu-id="de35e-127">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="de35e-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="de35e-128">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="de35e-128">Click Filter.</span></span>
9. <span data-ttu-id="de35e-129">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="de35e-130">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="de35e-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="de35e-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="de35e-131">Example: P6003</span></span>  
11. <span data-ttu-id="de35e-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de35e-132">Click OK.</span></span>
12. <span data-ttu-id="de35e-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de35e-133">Click OK.</span></span>
13. <span data-ttu-id="de35e-134">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="de35e-134">Click Planned orders.</span></span>
14. <span data-ttu-id="de35e-135">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="de35e-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="de35e-136">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="de35e-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="de35e-137">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="de35e-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="de35e-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="de35e-139">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="de35e-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="de35e-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="de35e-141">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="de35e-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="de35e-142">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="de35e-143">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="de35e-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="de35e-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="de35e-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="de35e-145">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="de35e-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="de35e-146">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="de35e-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="de35e-147">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="de35e-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="de35e-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="de35e-148">Click New.</span></span>
4. <span data-ttu-id="de35e-149">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="de35e-149">Click Sales order.</span></span>
5. <span data-ttu-id="de35e-150">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="de35e-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="de35e-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="de35e-151">Example: US-001</span></span>  
6. <span data-ttu-id="de35e-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de35e-152">Click OK.</span></span>
7. <span data-ttu-id="de35e-153">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="de35e-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="de35e-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="de35e-154">Example: P6003</span></span>  
8. <span data-ttu-id="de35e-155">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="de35e-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="de35e-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="de35e-156">Example: 50000</span></span>  
9. <span data-ttu-id="de35e-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="de35e-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="de35e-158">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="de35e-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="de35e-159">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="de35e-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="de35e-160">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="de35e-161">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="de35e-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="de35e-162">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="de35e-162">Click Run.</span></span>
4. <span data-ttu-id="de35e-163">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="de35e-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="de35e-164">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="de35e-164">Click Filter.</span></span>
6. <span data-ttu-id="de35e-165">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="de35e-166">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="de35e-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="de35e-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="de35e-167">Example: P6003</span></span>  
8. <span data-ttu-id="de35e-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de35e-168">Click OK.</span></span>
9. <span data-ttu-id="de35e-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de35e-169">Click OK.</span></span>
10. <span data-ttu-id="de35e-170">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="de35e-170">Click Planned orders.</span></span>
11. <span data-ttu-id="de35e-171">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="de35e-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="de35e-172">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="de35e-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="de35e-173">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="de35e-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="de35e-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="de35e-175">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="de35e-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="de35e-176">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="de35e-177">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="de35e-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="de35e-178">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de35e-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="de35e-179">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="de35e-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="de35e-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="de35e-180">Close the page.</span></span>
17. <span data-ttu-id="de35e-181">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="de35e-181">Click Master planning.</span></span>
18. <span data-ttu-id="de35e-182">Gå til Varedisponering > Konfiguration > Varedisponeringsparametre.</span><span class="sxs-lookup"><span data-stu-id="de35e-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="de35e-183">Vælg Nej i afkrydsningsfeltet Deaktiver alle planlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="de35e-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="de35e-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="de35e-184">Close the page.</span></span>

