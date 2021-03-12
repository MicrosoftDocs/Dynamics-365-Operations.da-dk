---
title: Lagerobjektværdier
description: Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 914c7e8c757664ec791b46924600b74c9c979e8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967427"
---
# <a name="inventory-object-values"></a><span data-ttu-id="9557a-103">Lagerobjektværdier</span><span class="sxs-lookup"><span data-stu-id="9557a-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9557a-104">Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="9557a-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="9557a-105">Med en ny funktion, der hedder **Fysisk antal**, kan du se værdierne for et bestemt lagerobjektet.</span><span class="sxs-lookup"><span data-stu-id="9557a-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="9557a-106">Et omkostningsobjekt repræsenterer enhedsniveauet, hvor der udføres lagerregnskab.</span><span class="sxs-lookup"><span data-stu-id="9557a-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="9557a-107">Du kan finde flere oplysninger om omkostningsobjekter i [Omkostningsobjekter](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="9557a-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="9557a-108">Hvis du vil se værdierne i et bestemt lagerobjekt, skal du klikke på **Fysisk antal** på siden **Omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="9557a-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="9557a-109">Sådan beregnes værdien af et lagerobjekt:</span><span class="sxs-lookup"><span data-stu-id="9557a-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="9557a-110">Lager object.Value = Omkostning object.Average enhedskostpris × Lager object.Quantity</span><span class="sxs-lookup"><span data-stu-id="9557a-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="9557a-111">Følgende eksempel viser, hvordan værdierne af et lagerobjekt og et omkostningsobjekt beregnes.</span><span class="sxs-lookup"><span data-stu-id="9557a-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="9557a-112">To hændelser til modtagelse af produktet er registreret for vare A:</span><span class="sxs-lookup"><span data-stu-id="9557a-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="9557a-113">Produktkvittering 1: antal = 100 stk., beløb = $1.000,00, websted = 1, lager = 11, batchnummer</span><span class="sxs-lookup"><span data-stu-id="9557a-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="9557a-114">= B1</span><span class="sxs-lookup"><span data-stu-id="9557a-114">= B1</span></span>
-   <span data-ttu-id="9557a-115">Produktkvittering 2: antal = 50 stk., beløb = $800,00, websted = 1, lager = 11, batchnummer</span><span class="sxs-lookup"><span data-stu-id="9557a-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="9557a-116">= B2</span><span class="sxs-lookup"><span data-stu-id="9557a-116">= B2</span></span>

<span data-ttu-id="9557a-117">I følgende tabel vises resultatet af beregningen for et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="9557a-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="9557a-118">Du kan få vist fakturaen på siden **Omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="9557a-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="9557a-119">Objekttype</span><span class="sxs-lookup"><span data-stu-id="9557a-119">Object type</span></span></th>
<th><span data-ttu-id="9557a-120">Varenummer</span><span class="sxs-lookup"><span data-stu-id="9557a-120">Item number</span></span></th>
<th><span data-ttu-id="9557a-121">Lokation</span><span class="sxs-lookup"><span data-stu-id="9557a-121">Site</span></span></th>
<th><span data-ttu-id="9557a-122">Antal</span><span class="sxs-lookup"><span data-stu-id="9557a-122">Quantity</span></span></th>
<th><span data-ttu-id="9557a-123">Lagerenhed</span><span class="sxs-lookup"><span data-stu-id="9557a-123">Inventory unit</span></span></th>
<th><span data-ttu-id="9557a-124">Værdi</span><span class="sxs-lookup"><span data-stu-id="9557a-124">Value</span></span></th>
<th><span data-ttu-id="9557a-125">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="9557a-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9557a-126">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9557a-126">Cost object</span></span></td>
<td><span data-ttu-id="9557a-127">A</span><span class="sxs-lookup"><span data-stu-id="9557a-127">A</span></span></td>
<td><span data-ttu-id="9557a-128">1</span><span class="sxs-lookup"><span data-stu-id="9557a-128">1</span></span></td>
<td><span data-ttu-id="9557a-129">150</span><span class="sxs-lookup"><span data-stu-id="9557a-129">150</span></span></td>
<td><span data-ttu-id="9557a-130">Styk</span><span class="sxs-lookup"><span data-stu-id="9557a-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="9557a-131">$1800,00</span><span class="sxs-lookup"><span data-stu-id="9557a-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="9557a-132">$12,00</span><span class="sxs-lookup"><span data-stu-id="9557a-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9557a-133">I følgende tabel vises resultatet af beregningen for et lagerobjekt.</span><span class="sxs-lookup"><span data-stu-id="9557a-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="9557a-134">Du kan få vist resultatet ved at klikke på **Fysisk antal** på siden **Omkostningsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="9557a-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="9557a-135">Objekttype</span><span class="sxs-lookup"><span data-stu-id="9557a-135">Object type</span></span></th>
<th><span data-ttu-id="9557a-136">Varenummer</span><span class="sxs-lookup"><span data-stu-id="9557a-136">Item number</span></span></th>
<th><span data-ttu-id="9557a-137">Lokation</span><span class="sxs-lookup"><span data-stu-id="9557a-137">Site</span></span></th>
<th><span data-ttu-id="9557a-138">Lagersted</span><span class="sxs-lookup"><span data-stu-id="9557a-138">Warehouse</span></span></th>
<th><span data-ttu-id="9557a-139">Batch nr.</span><span class="sxs-lookup"><span data-stu-id="9557a-139">Batch No.</span></span></th>
<th><span data-ttu-id="9557a-140">Antal</span><span class="sxs-lookup"><span data-stu-id="9557a-140">Quantity</span></span></th>
<th><span data-ttu-id="9557a-141">Lagerenhed</span><span class="sxs-lookup"><span data-stu-id="9557a-141">Inventory unit</span></span></th>
<th><span data-ttu-id="9557a-142">Værdi</span><span class="sxs-lookup"><span data-stu-id="9557a-142">Value</span></span></th>
<th><span data-ttu-id="9557a-143">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="9557a-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9557a-144">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="9557a-144">Inventory object</span></span></td>
<td><span data-ttu-id="9557a-145">A</span><span class="sxs-lookup"><span data-stu-id="9557a-145">A</span></span></td>
<td><span data-ttu-id="9557a-146">1</span><span class="sxs-lookup"><span data-stu-id="9557a-146">1</span></span></td>
<td><span data-ttu-id="9557a-147">11</span><span class="sxs-lookup"><span data-stu-id="9557a-147">11</span></span></td>
<td><span data-ttu-id="9557a-148">B1</span><span class="sxs-lookup"><span data-stu-id="9557a-148">B1</span></span></td>
<td><span data-ttu-id="9557a-149">100</span><span class="sxs-lookup"><span data-stu-id="9557a-149">100</span></span></td>
<td><span data-ttu-id="9557a-150">Styk</span><span class="sxs-lookup"><span data-stu-id="9557a-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="9557a-151">$1200,00</span><span class="sxs-lookup"><span data-stu-id="9557a-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="9557a-152">$12,00</span><span class="sxs-lookup"><span data-stu-id="9557a-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9557a-153">Lagerobjekt</span><span class="sxs-lookup"><span data-stu-id="9557a-153">Inventory object</span></span></td>
<td><span data-ttu-id="9557a-154">T</span><span class="sxs-lookup"><span data-stu-id="9557a-154">A</span></span></td>
<td><span data-ttu-id="9557a-155">1</span><span class="sxs-lookup"><span data-stu-id="9557a-155">1</span></span></td>
<td><span data-ttu-id="9557a-156">11</span><span class="sxs-lookup"><span data-stu-id="9557a-156">11</span></span></td>
<td><span data-ttu-id="9557a-157">B2</span><span class="sxs-lookup"><span data-stu-id="9557a-157">B2</span></span></td>
<td><span data-ttu-id="9557a-158">50</span><span class="sxs-lookup"><span data-stu-id="9557a-158">50</span></span></td>
<td><span data-ttu-id="9557a-159">Styk</span><span class="sxs-lookup"><span data-stu-id="9557a-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="9557a-160">$600,00</span><span class="sxs-lookup"><span data-stu-id="9557a-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="9557a-161">$12,00</span><span class="sxs-lookup"><span data-stu-id="9557a-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="9557a-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9557a-162">Additional resources</span></span>
--------

[<span data-ttu-id="9557a-163">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="9557a-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="9557a-164">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="9557a-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="9557a-165">Nyheder og ændringer</span><span class="sxs-lookup"><span data-stu-id="9557a-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



