---
title: Oprette en materialeplan for samprodukter
description: Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920723"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="57575-103">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="57575-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57575-104">Produktionsplanlæggeren planlægger materialebehovet for varer, der er formelsamprodukter.</span><span class="sxs-lookup"><span data-stu-id="57575-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="57575-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="57575-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="57575-106">Opret krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="57575-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="57575-107">Gå til **Salg og marketing \> Arbejdsområder \> Salgsordrebehandling og -forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="57575-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="57575-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="57575-108">Select **New**.</span></span>
1. <span data-ttu-id="57575-109">Vælg **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="57575-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="57575-110">Skriv en værdi i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="57575-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="57575-111">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="57575-111">Example: US-001</span></span>  
1. <span data-ttu-id="57575-112">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57575-112">Select **OK**.</span></span>
1. <span data-ttu-id="57575-113">Indtast en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="57575-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="57575-114">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="57575-114">Example: P6003</span></span>  
1. <span data-ttu-id="57575-115">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="57575-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="57575-116">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="57575-116">Example: 50000</span></span>  
1. <span data-ttu-id="57575-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="57575-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="57575-118">Oprette en materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="57575-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="57575-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57575-119">Close the page.</span></span>
1. <span data-ttu-id="57575-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57575-120">Close the page.</span></span>
1. <span data-ttu-id="57575-121">Vælg **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="57575-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="57575-122">Vælg rullelistens kap i feltet **Plan** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="57575-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="57575-123">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="57575-124">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="57575-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="57575-125">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="57575-125">Select **Run**.</span></span>
1. <span data-ttu-id="57575-126">Udvid eller skjul sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="57575-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="57575-127">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="57575-127">Select **Filter**.</span></span>
1. <span data-ttu-id="57575-128">Vælg rækken for **Felt** = *Varenummer* på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="57575-129">Skriv en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="57575-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="57575-130">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="57575-130">Example: P6003</span></span>  
1. <span data-ttu-id="57575-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57575-131">Select **OK**.</span></span>
1. <span data-ttu-id="57575-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57575-132">Select **OK**.</span></span>
1. <span data-ttu-id="57575-133">Vælg **Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="57575-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="57575-134">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="57575-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="57575-135">Filtrer f.eks. efter feltet **Varenummer** med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="57575-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="57575-136">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="57575-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="57575-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="57575-138">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="57575-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="57575-139">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="57575-140">Udvid sektionen **Udligning**.</span><span class="sxs-lookup"><span data-stu-id="57575-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="57575-141">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="57575-142">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="57575-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="57575-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57575-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="57575-144">Oprette et andet krav om et samprodukt</span><span class="sxs-lookup"><span data-stu-id="57575-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="57575-145">Gå til **Salg og marketing \> Arbejdsområder \> Salgsordrebehandling og -forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="57575-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="57575-146">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="57575-146">Select **New**.</span></span>
1. <span data-ttu-id="57575-147">Vælg **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="57575-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="57575-148">Skriv en værdi i feltet **Kundekonto**.</span><span class="sxs-lookup"><span data-stu-id="57575-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="57575-149">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="57575-149">Example: US-001</span></span>  
1. <span data-ttu-id="57575-150">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57575-150">Select **OK**.</span></span>
1. <span data-ttu-id="57575-151">Indtast en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="57575-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="57575-152">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="57575-152">Example: P6003</span></span>  
1. <span data-ttu-id="57575-153">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="57575-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="57575-154">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="57575-154">Example: 50000</span></span>  
1. <span data-ttu-id="57575-155">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="57575-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="57575-156">Oprette en anden materialeplan for samprodukter</span><span class="sxs-lookup"><span data-stu-id="57575-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="57575-157">Vælg rullelistens kap i feltet **Plan** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="57575-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="57575-158">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="57575-159">Eksempel: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="57575-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="57575-160">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="57575-160">Select **Run**.</span></span>
4. <span data-ttu-id="57575-161">Udvid eller skjul sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="57575-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="57575-162">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="57575-162">Select **Filter**.</span></span>
6. <span data-ttu-id="57575-163">Vælg rækken for **Felt** = *Varenummer* på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="57575-164">Skriv en værdi i feltet *Kriterier*.</span><span class="sxs-lookup"><span data-stu-id="57575-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="57575-165">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="57575-165">Example: P6003</span></span>  
8. <span data-ttu-id="57575-166">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57575-166">Select **OK**.</span></span>
9. <span data-ttu-id="57575-167">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57575-167">Select **OK**.</span></span>
10. <span data-ttu-id="57575-168">Vælg **Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="57575-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="57575-169">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="57575-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="57575-170">Filtrer f.eks. efter feltet **Varenummer** med værdien "P6000".</span><span class="sxs-lookup"><span data-stu-id="57575-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="57575-171">Filtrer efter den formelvare, der har et samprodukt af den vare, du har oprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="57575-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="57575-172">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="57575-173">Vælg en af de rækker, der returneres af filteret.</span><span class="sxs-lookup"><span data-stu-id="57575-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="57575-174">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="57575-175">Udvid eller skjul sektionen **Udligning**.</span><span class="sxs-lookup"><span data-stu-id="57575-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="57575-176">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="57575-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="57575-177">Ordreforslaget er udlignet til salgsordren for samproduktet.</span><span class="sxs-lookup"><span data-stu-id="57575-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="57575-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57575-178">Close the page.</span></span>
17. <span data-ttu-id="57575-179">Vælg **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="57575-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="57575-180">Gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="57575-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="57575-181">Vælg *Nej* i feltet **Deaktiver alle planlægningsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="57575-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="57575-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="57575-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]