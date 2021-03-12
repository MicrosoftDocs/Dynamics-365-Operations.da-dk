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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8e9067cdd8851da31c07a92217001e447f400d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983385"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="23b81-103">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="23b81-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23b81-104">Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.</span><span class="sxs-lookup"><span data-stu-id="23b81-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="23b81-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="23b81-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="23b81-106">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="23b81-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="23b81-107">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="23b81-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="23b81-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="23b81-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="23b81-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="23b81-109">Click New.</span></span>
4. <span data-ttu-id="23b81-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="23b81-110">Click Sales order.</span></span>
5. <span data-ttu-id="23b81-111">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="23b81-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="23b81-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="23b81-112">Example: US-001</span></span>  
6. <span data-ttu-id="23b81-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23b81-113">Click OK.</span></span>
7. <span data-ttu-id="23b81-114">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="23b81-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="23b81-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="23b81-115">Example: P6003</span></span>  
8. <span data-ttu-id="23b81-116">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="23b81-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="23b81-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="23b81-117">Example: 50000</span></span>  
9. <span data-ttu-id="23b81-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="23b81-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="23b81-119">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="23b81-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="23b81-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23b81-120">Close the page.</span></span>
2. <span data-ttu-id="23b81-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23b81-121">Close the page.</span></span>
3. <span data-ttu-id="23b81-122">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="23b81-122">Click Master planning.</span></span>
4. <span data-ttu-id="23b81-123">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="23b81-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="23b81-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23b81-125">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="23b81-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="23b81-126">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="23b81-126">Click Run.</span></span>
7. <span data-ttu-id="23b81-127">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="23b81-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="23b81-128">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="23b81-128">Click Filter.</span></span>
9. <span data-ttu-id="23b81-129">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="23b81-130">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="23b81-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="23b81-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="23b81-131">Example: P6003</span></span>  
11. <span data-ttu-id="23b81-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23b81-132">Click OK.</span></span>
12. <span data-ttu-id="23b81-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23b81-133">Click OK.</span></span>
13. <span data-ttu-id="23b81-134">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="23b81-134">Click Planned orders.</span></span>
14. <span data-ttu-id="23b81-135">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="23b81-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="23b81-136">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="23b81-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="23b81-137">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="23b81-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="23b81-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="23b81-139">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="23b81-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="23b81-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="23b81-141">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="23b81-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="23b81-142">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23b81-143">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="23b81-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="23b81-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23b81-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="23b81-145">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="23b81-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="23b81-146">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="23b81-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="23b81-147">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="23b81-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="23b81-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="23b81-148">Click New.</span></span>
4. <span data-ttu-id="23b81-149">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="23b81-149">Click Sales order.</span></span>
5. <span data-ttu-id="23b81-150">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="23b81-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="23b81-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="23b81-151">Example: US-001</span></span>  
6. <span data-ttu-id="23b81-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23b81-152">Click OK.</span></span>
7. <span data-ttu-id="23b81-153">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="23b81-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="23b81-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="23b81-154">Example: P6003</span></span>  
8. <span data-ttu-id="23b81-155">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="23b81-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="23b81-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="23b81-156">Example: 50000</span></span>  
9. <span data-ttu-id="23b81-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="23b81-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="23b81-158">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="23b81-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="23b81-159">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="23b81-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="23b81-160">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23b81-161">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="23b81-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="23b81-162">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="23b81-162">Click Run.</span></span>
4. <span data-ttu-id="23b81-163">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="23b81-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="23b81-164">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="23b81-164">Click Filter.</span></span>
6. <span data-ttu-id="23b81-165">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="23b81-166">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="23b81-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="23b81-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="23b81-167">Example: P6003</span></span>  
8. <span data-ttu-id="23b81-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23b81-168">Click OK.</span></span>
9. <span data-ttu-id="23b81-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="23b81-169">Click OK.</span></span>
10. <span data-ttu-id="23b81-170">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="23b81-170">Click Planned orders.</span></span>
11. <span data-ttu-id="23b81-171">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="23b81-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="23b81-172">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="23b81-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="23b81-173">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="23b81-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="23b81-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="23b81-175">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="23b81-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="23b81-176">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="23b81-177">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="23b81-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="23b81-178">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="23b81-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23b81-179">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="23b81-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="23b81-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23b81-180">Close the page.</span></span>
17. <span data-ttu-id="23b81-181">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="23b81-181">Click Master planning.</span></span>
18. <span data-ttu-id="23b81-182">Gå til Varedisponering > Konfiguration > Varedisponeringsparametre.</span><span class="sxs-lookup"><span data-stu-id="23b81-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="23b81-183">Vælg Nej i afkrydsningsfeltet Deaktiver alle planlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="23b81-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="23b81-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="23b81-184">Close the page.</span></span>

