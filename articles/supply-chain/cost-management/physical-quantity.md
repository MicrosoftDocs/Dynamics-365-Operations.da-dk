---
title: "Lagerobjektværdier"
description: "Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 60f39b19a627e9c3288f30872d237b8c0ccd8ac4
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="inventory-object-values"></a><span data-ttu-id="08932-103">Lagerobjektværdier</span><span class="sxs-lookup"><span data-stu-id="08932-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08932-104">Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="08932-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="08932-105">Med en ny funktion, der hedder **Fysisk antal**, kan du se værdierne for et bestemt lagerobjektet.</span><span class="sxs-lookup"><span data-stu-id="08932-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="08932-106">Et omkostningsobjekt repræsenterer enhedsniveauet, hvor der udføres lagerregnskab.</span><span class="sxs-lookup"><span data-stu-id="08932-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="08932-107">Du kan finde flere oplysninger om omkostningsobjekter i [Omkostningsobjekter](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="08932-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="08932-108">Hvis du vil se værdierne i et bestemt lagerobjekt, skal du klikke på **Fysisk antal** på siden **Omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="08932-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="08932-109">Sådan beregnes værdien af et lagerobjekt:</span><span class="sxs-lookup"><span data-stu-id="08932-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="08932-110">Lager object.Value = Omkostning object.Average enhedskostpris × Lager object.Quantity</span><span class="sxs-lookup"><span data-stu-id="08932-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="08932-111">Følgende eksempel viser, hvordan værdierne af et lagerobjekt og et omkostningsobjekt beregnes.</span><span class="sxs-lookup"><span data-stu-id="08932-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="08932-112">To hændelser til modtagelse af produktet er registreret for vare A:</span><span class="sxs-lookup"><span data-stu-id="08932-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="08932-113">Produktkvittering 1: antal = 100 stk., beløb = $1.000,00, websted = 1, lager = 11, batchnummer</span><span class="sxs-lookup"><span data-stu-id="08932-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="08932-114">= B1</span><span class="sxs-lookup"><span data-stu-id="08932-114">= B1</span></span>
-   <span data-ttu-id="08932-115">Produktkvittering 2: antal = 50 stk., beløb = $800,00, websted = 1, lager = 11, batchnummer</span><span class="sxs-lookup"><span data-stu-id="08932-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="08932-116">= B2</span><span class="sxs-lookup"><span data-stu-id="08932-116">= B2</span></span>

<span data-ttu-id="08932-117">I følgende tabel vises resultatet af beregningen for et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="08932-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="08932-118">Du kan få vist fakturaen på siden **Omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="08932-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08932-119">Objekttype</span><span class="sxs-lookup"><span data-stu-id="08932-119">Object type</span></span></th>
<th><span data-ttu-id="08932-120">Varenummer</span><span class="sxs-lookup"><span data-stu-id="08932-120">Item number</span></span></th>
<th><span data-ttu-id="08932-121">Lokation</span><span class="sxs-lookup"><span data-stu-id="08932-121">Site</span></span></th>
<th><span data-ttu-id="08932-122">Antal</span><span class="sxs-lookup"><span data-stu-id="08932-122">Quantity</span></span></th>
<th><span data-ttu-id="08932-123">Lagerenhed</span><span class="sxs-lookup"><span data-stu-id="08932-123">Inventory unit</span></span></th>
<th><span data-ttu-id="08932-124">Værdi</span><span class="sxs-lookup"><span data-stu-id="08932-124">Value</span></span></th>
<th><span data-ttu-id="08932-125">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="08932-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08932-126">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="08932-126">Cost object</span></span></td>
<td><span data-ttu-id="08932-127">A</span><span class="sxs-lookup"><span data-stu-id="08932-127">A</span></span></td>
<td><span data-ttu-id="08932-128">1</span><span class="sxs-lookup"><span data-stu-id="08932-128">1</span></span></td>
<td><span data-ttu-id="08932-129">150</span><span class="sxs-lookup"><span data-stu-id="08932-129">150</span></span></td>
<td><span data-ttu-id="08932-130">Styk</span><span class="sxs-lookup"><span data-stu-id="08932-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="08932-131">$1800,00</span><span class="sxs-lookup"><span data-stu-id="08932-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="08932-132">$12,00</span><span class="sxs-lookup"><span data-stu-id="08932-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="08932-133">I følgende tabel vises resultatet af beregningen for et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="08932-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="08932-134">Du kan få vist resultatet ved at klikke på **Fysisk antal** på siden **Omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="08932-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08932-135">Objekttype</span><span class="sxs-lookup"><span data-stu-id="08932-135">Object type</span></span></th>
<th><span data-ttu-id="08932-136">Varenummer</span><span class="sxs-lookup"><span data-stu-id="08932-136">Item number</span></span></th>
<th><span data-ttu-id="08932-137">Lokation</span><span class="sxs-lookup"><span data-stu-id="08932-137">Site</span></span></th>
<th><span data-ttu-id="08932-138">Lagersted</span><span class="sxs-lookup"><span data-stu-id="08932-138">Warehouse</span></span></th>
<th><span data-ttu-id="08932-139">Batch nr.</span><span class="sxs-lookup"><span data-stu-id="08932-139">Batch No.</span></span></th>
<th><span data-ttu-id="08932-140">Antal</span><span class="sxs-lookup"><span data-stu-id="08932-140">Quantity</span></span></th>
<th><span data-ttu-id="08932-141">Lagerenhed</span><span class="sxs-lookup"><span data-stu-id="08932-141">Inventory unit</span></span></th>
<th><span data-ttu-id="08932-142">Værdi</span><span class="sxs-lookup"><span data-stu-id="08932-142">Value</span></span></th>
<th><span data-ttu-id="08932-143">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="08932-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08932-144">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="08932-144">Inventory object</span></span></td>
<td><span data-ttu-id="08932-145">A</span><span class="sxs-lookup"><span data-stu-id="08932-145">A</span></span></td>
<td><span data-ttu-id="08932-146">1</span><span class="sxs-lookup"><span data-stu-id="08932-146">1</span></span></td>
<td><span data-ttu-id="08932-147">11</span><span class="sxs-lookup"><span data-stu-id="08932-147">11</span></span></td>
<td><span data-ttu-id="08932-148">B1</span><span class="sxs-lookup"><span data-stu-id="08932-148">B1</span></span></td>
<td><span data-ttu-id="08932-149">100</span><span class="sxs-lookup"><span data-stu-id="08932-149">100</span></span></td>
<td><span data-ttu-id="08932-150">Styk</span><span class="sxs-lookup"><span data-stu-id="08932-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="08932-151">$1200,00</span><span class="sxs-lookup"><span data-stu-id="08932-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="08932-152">$12,00</span><span class="sxs-lookup"><span data-stu-id="08932-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08932-153">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="08932-153">Inventory object</span></span></td>
<td><span data-ttu-id="08932-154">T</span><span class="sxs-lookup"><span data-stu-id="08932-154">A</span></span></td>
<td><span data-ttu-id="08932-155">1</span><span class="sxs-lookup"><span data-stu-id="08932-155">1</span></span></td>
<td><span data-ttu-id="08932-156">11</span><span class="sxs-lookup"><span data-stu-id="08932-156">11</span></span></td>
<td><span data-ttu-id="08932-157">B2</span><span class="sxs-lookup"><span data-stu-id="08932-157">B2</span></span></td>
<td><span data-ttu-id="08932-158">50</span><span class="sxs-lookup"><span data-stu-id="08932-158">50</span></span></td>
<td><span data-ttu-id="08932-159">Styk</span><span class="sxs-lookup"><span data-stu-id="08932-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="08932-160">$600,00</span><span class="sxs-lookup"><span data-stu-id="08932-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="08932-161">$12,00</span><span class="sxs-lookup"><span data-stu-id="08932-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="08932-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="08932-162">Additional resources</span></span>
--------

[<span data-ttu-id="08932-163">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="08932-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="08932-164">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="08932-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="08932-165">Nyheder og ændringer</span><span class="sxs-lookup"><span data-stu-id="08932-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)




