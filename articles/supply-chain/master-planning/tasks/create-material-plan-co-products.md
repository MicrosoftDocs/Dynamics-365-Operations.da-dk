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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209668"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="26101-103">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="26101-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26101-104">Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.</span><span class="sxs-lookup"><span data-stu-id="26101-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="26101-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="26101-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="26101-106">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="26101-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="26101-107">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="26101-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="26101-108">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="26101-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="26101-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="26101-109">Click New.</span></span>
4. <span data-ttu-id="26101-110">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="26101-110">Click Sales order.</span></span>
5. <span data-ttu-id="26101-111">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="26101-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="26101-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="26101-112">Example: US-001</span></span>  
6. <span data-ttu-id="26101-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26101-113">Click OK.</span></span>
7. <span data-ttu-id="26101-114">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="26101-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26101-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="26101-115">Example: P6003</span></span>  
8. <span data-ttu-id="26101-116">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="26101-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="26101-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="26101-117">Example: 50000</span></span>  
9. <span data-ttu-id="26101-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="26101-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="26101-119">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="26101-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="26101-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26101-120">Close the page.</span></span>
2. <span data-ttu-id="26101-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26101-121">Close the page.</span></span>
3. <span data-ttu-id="26101-122">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="26101-122">Click Master planning.</span></span>
4. <span data-ttu-id="26101-123">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="26101-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="26101-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26101-125">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="26101-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="26101-126">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="26101-126">Click Run.</span></span>
7. <span data-ttu-id="26101-127">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="26101-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="26101-128">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="26101-128">Click Filter.</span></span>
9. <span data-ttu-id="26101-129">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="26101-130">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="26101-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="26101-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="26101-131">Example: P6003</span></span>  
11. <span data-ttu-id="26101-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26101-132">Click OK.</span></span>
12. <span data-ttu-id="26101-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26101-133">Click OK.</span></span>
13. <span data-ttu-id="26101-134">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="26101-134">Click Planned orders.</span></span>
14. <span data-ttu-id="26101-135">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="26101-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="26101-136">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="26101-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="26101-137">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="26101-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="26101-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="26101-139">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="26101-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="26101-140">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="26101-141">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="26101-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="26101-142">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26101-143">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="26101-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="26101-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26101-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="26101-145">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="26101-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="26101-146">Gå til Standarddashboard.</span><span class="sxs-lookup"><span data-stu-id="26101-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="26101-147">Klik på Salgsordrebehandling og -forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="26101-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="26101-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="26101-148">Click New.</span></span>
4. <span data-ttu-id="26101-149">Klik på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="26101-149">Click Sales order.</span></span>
5. <span data-ttu-id="26101-150">Skriv en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="26101-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="26101-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="26101-151">Example: US-001</span></span>  
6. <span data-ttu-id="26101-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26101-152">Click OK.</span></span>
7. <span data-ttu-id="26101-153">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="26101-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26101-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="26101-154">Example: P6003</span></span>  
8. <span data-ttu-id="26101-155">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="26101-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="26101-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="26101-156">Example: 50000</span></span>  
9. <span data-ttu-id="26101-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="26101-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="26101-158">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="26101-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="26101-159">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="26101-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="26101-160">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26101-161">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="26101-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="26101-162">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="26101-162">Click Run.</span></span>
4. <span data-ttu-id="26101-163">Udvis eller skjul sektionen Poster, der skal indgå.</span><span class="sxs-lookup"><span data-stu-id="26101-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="26101-164">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="26101-164">Click Filter.</span></span>
6. <span data-ttu-id="26101-165">Vælg rækken for Felt = Varenummer på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="26101-166">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="26101-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="26101-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="26101-167">Example: P6003</span></span>  
8. <span data-ttu-id="26101-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26101-168">Click OK.</span></span>
9. <span data-ttu-id="26101-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26101-169">Click OK.</span></span>
10. <span data-ttu-id="26101-170">Klik på Ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="26101-170">Click Planned orders.</span></span>
11. <span data-ttu-id="26101-171">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="26101-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="26101-172">Filtrer f.eks. efter feltet Varenummer med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="26101-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="26101-173">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="26101-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="26101-174">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="26101-175">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="26101-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="26101-176">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="26101-177">Udvid eller skjul sektionen Udligning.</span><span class="sxs-lookup"><span data-stu-id="26101-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="26101-178">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="26101-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26101-179">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="26101-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="26101-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26101-180">Close the page.</span></span>
17. <span data-ttu-id="26101-181">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="26101-181">Click Master planning.</span></span>
18. <span data-ttu-id="26101-182">Gå til Varedisponering > Konfiguration > Varedisponeringsparametre.</span><span class="sxs-lookup"><span data-stu-id="26101-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="26101-183">Vælg Nej i afkrydsningsfeltet Deaktiver alle planlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="26101-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="26101-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26101-184">Close the page.</span></span>

