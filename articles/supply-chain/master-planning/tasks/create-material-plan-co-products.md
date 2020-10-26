---
title: Oprette en materialeplan for samprodukter
description: Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982203"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="590e2-103">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="590e2-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="590e2-104">Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.</span><span class="sxs-lookup"><span data-stu-id="590e2-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="590e2-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="590e2-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="590e2-106">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="590e2-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="590e2-107">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="590e2-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="590e2-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="590e2-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="590e2-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="590e2-109">Click New.</span></span>
4. <span data-ttu-id="590e2-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="590e2-110">Click Sales order.</span></span>
5. <span data-ttu-id="590e2-111">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="590e2-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="590e2-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="590e2-112">Example: US-001</span></span>  
6. <span data-ttu-id="590e2-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="590e2-113">Click OK.</span></span>
7. <span data-ttu-id="590e2-114">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="590e2-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="590e2-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="590e2-115">Example: P6003</span></span>  
8. <span data-ttu-id="590e2-116">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="590e2-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="590e2-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="590e2-117">Example: 50000</span></span>  
9. <span data-ttu-id="590e2-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="590e2-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="590e2-119">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="590e2-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="590e2-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="590e2-120">Close the page.</span></span>
2. <span data-ttu-id="590e2-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="590e2-121">Close the page.</span></span>
3. <span data-ttu-id="590e2-122">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="590e2-122">Click Master planning.</span></span>
4. <span data-ttu-id="590e2-123">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="590e2-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="590e2-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="590e2-125">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="590e2-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="590e2-126">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="590e2-126">Click Run.</span></span>
7. <span data-ttu-id="590e2-127">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="590e2-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="590e2-128">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="590e2-128">Click Filter.</span></span>
9. <span data-ttu-id="590e2-129">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="590e2-130">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="590e2-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="590e2-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="590e2-131">Example: P6003</span></span>  
11. <span data-ttu-id="590e2-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="590e2-132">Click OK.</span></span>
12. <span data-ttu-id="590e2-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="590e2-133">Click OK.</span></span>
13. <span data-ttu-id="590e2-134">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="590e2-134">Click Planned orders.</span></span>
14. <span data-ttu-id="590e2-135">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="590e2-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="590e2-136">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="590e2-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="590e2-137">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="590e2-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="590e2-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="590e2-139">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="590e2-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="590e2-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="590e2-141">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="590e2-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="590e2-142">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="590e2-143">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="590e2-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="590e2-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="590e2-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="590e2-145">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="590e2-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="590e2-146">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="590e2-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="590e2-147">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="590e2-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="590e2-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="590e2-148">Click New.</span></span>
4. <span data-ttu-id="590e2-149">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="590e2-149">Click Sales order.</span></span>
5. <span data-ttu-id="590e2-150">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="590e2-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="590e2-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="590e2-151">Example: US-001</span></span>  
6. <span data-ttu-id="590e2-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="590e2-152">Click OK.</span></span>
7. <span data-ttu-id="590e2-153">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="590e2-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="590e2-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="590e2-154">Example: P6003</span></span>  
8. <span data-ttu-id="590e2-155">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="590e2-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="590e2-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="590e2-156">Example: 50000</span></span>  
9. <span data-ttu-id="590e2-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="590e2-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="590e2-158">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="590e2-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="590e2-159">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="590e2-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="590e2-160">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="590e2-161">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="590e2-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="590e2-162">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="590e2-162">Click Run.</span></span>
4. <span data-ttu-id="590e2-163">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="590e2-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="590e2-164">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="590e2-164">Click Filter.</span></span>
6. <span data-ttu-id="590e2-165">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="590e2-166">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="590e2-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="590e2-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="590e2-167">Example: P6003</span></span>  
8. <span data-ttu-id="590e2-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="590e2-168">Click OK.</span></span>
9. <span data-ttu-id="590e2-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="590e2-169">Click OK.</span></span>
10. <span data-ttu-id="590e2-170">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="590e2-170">Click Planned orders.</span></span>
11. <span data-ttu-id="590e2-171">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="590e2-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="590e2-172">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="590e2-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="590e2-173">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="590e2-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="590e2-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="590e2-175">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="590e2-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="590e2-176">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="590e2-177">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="590e2-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="590e2-178">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="590e2-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="590e2-179">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="590e2-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="590e2-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="590e2-180">Close the page.</span></span>
17. <span data-ttu-id="590e2-181">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="590e2-181">Click Master planning.</span></span>
18. <span data-ttu-id="590e2-182">Gå til Varedisponering > Konfiguration > Varedisponeringsparametre.</span><span class="sxs-lookup"><span data-stu-id="590e2-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="590e2-183">Vælg Nej i afkrydsningsfeltet Deaktiver alle planlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="590e2-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="590e2-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="590e2-184">Close the page.</span></span>

