---
title: Eksempler og logik til rapport over aldersfordelt lager
description: I dette emne vises nogle eksempler på, hvordan resultaterne af en rapport over aldersfordelt lager fortolkes.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d9c70a7931c009cd53fbd28a3f4c768d04964a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214412"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="3c48e-103">Eksempler og logik til rapport over aldersfordelt lager</span><span class="sxs-lookup"><span data-stu-id="3c48e-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c48e-104">I dette emne vises nogle eksempler på, hvordan resultaterne af rapporten **Aldersfordelt lager** fortolkes.</span><span class="sxs-lookup"><span data-stu-id="3c48e-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="3c48e-105">Denne rapport kategoriserer det disponible antal og lagerværdier for en valgt vare eller varegruppe i flere perioder.</span><span class="sxs-lookup"><span data-stu-id="3c48e-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="3c48e-106">I dette emne vises også rapportens interne logik.</span><span class="sxs-lookup"><span data-stu-id="3c48e-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="3c48e-107">Eksemplerne i dette emne viser resultater, der præsenteres i en rapport over standard **Aldersfordelt lager**.</span><span class="sxs-lookup"><span data-stu-id="3c48e-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="3c48e-108">Generelt anbefales det dog, at du bruger [Lagerrapport over aldersfordelt lager](inventory-aging-report-storage.md)-versionen af denne rapport, specielt hvis du har mange varer og lagersteder, der skal behandles.</span><span class="sxs-lookup"><span data-stu-id="3c48e-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="3c48e-109">Lagerrapport over aldersfordelt lager gemmer alle de rapporter, du genererer, viser resultaterne som en interaktiv side og et diagram og giver dig mulighed for at eksportere gemte rapporter.</span><span class="sxs-lookup"><span data-stu-id="3c48e-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="3c48e-110">Eksempeldata, der bruges i disse eksempler</span><span class="sxs-lookup"><span data-stu-id="3c48e-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="3c48e-111">Eksemplerne i dette emne er baseret på de eksempeldata fra lagertransaktioner, der er beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="3c48e-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="3c48e-112">Konfiguration af lagringsdimension</span><span class="sxs-lookup"><span data-stu-id="3c48e-112">Storage dimension setup</span></span>

<span data-ttu-id="3c48e-113">Systemeksemplet indeholder følgende opsætning af lagringsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="3c48e-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="3c48e-114">Navn</span><span class="sxs-lookup"><span data-stu-id="3c48e-114">Name</span></span>      | <span data-ttu-id="3c48e-115">Aktivt</span><span class="sxs-lookup"><span data-stu-id="3c48e-115">Active</span></span> | <span data-ttu-id="3c48e-116">Fysisk lager</span><span class="sxs-lookup"><span data-stu-id="3c48e-116">Physical inventory</span></span> | <span data-ttu-id="3c48e-117">Økonomisk lager</span><span class="sxs-lookup"><span data-stu-id="3c48e-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="3c48e-118">Lokation</span><span class="sxs-lookup"><span data-stu-id="3c48e-118">Site</span></span>      | <span data-ttu-id="3c48e-119">Ja</span><span class="sxs-lookup"><span data-stu-id="3c48e-119">Yes</span></span>    | <span data-ttu-id="3c48e-120">Ja</span><span class="sxs-lookup"><span data-stu-id="3c48e-120">Yes</span></span>                | <span data-ttu-id="3c48e-121">Ja</span><span class="sxs-lookup"><span data-stu-id="3c48e-121">Yes</span></span>                 |
| <span data-ttu-id="3c48e-122">Lagersted</span><span class="sxs-lookup"><span data-stu-id="3c48e-122">Warehouse</span></span> | <span data-ttu-id="3c48e-123">Ja</span><span class="sxs-lookup"><span data-stu-id="3c48e-123">Yes</span></span>    | <span data-ttu-id="3c48e-124">Ja</span><span class="sxs-lookup"><span data-stu-id="3c48e-124">Yes</span></span>                | <span data-ttu-id="3c48e-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c48e-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="3c48e-126">Lagermodel</span><span class="sxs-lookup"><span data-stu-id="3c48e-126">Inventory model</span></span>

<span data-ttu-id="3c48e-127">I forbindelse med eksempelsystemet er lagermodellen for de frigivne produkter *FIFO* og **Kostpris**-indstillingen for lagermodellen er *Medtag fysisk værdi*.</span><span class="sxs-lookup"><span data-stu-id="3c48e-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="3c48e-128">Lagerbevægelser</span><span class="sxs-lookup"><span data-stu-id="3c48e-128">Inventory transactions</span></span>

<span data-ttu-id="3c48e-129">Eksempelsystemet indeholder følgende lagertransaktioner for et frigivet produkt, der har varenummeret *1000*.</span><span class="sxs-lookup"><span data-stu-id="3c48e-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="3c48e-130">Reference</span><span class="sxs-lookup"><span data-stu-id="3c48e-130">Reference</span></span>      | <span data-ttu-id="3c48e-131">Lokation</span><span class="sxs-lookup"><span data-stu-id="3c48e-131">Site</span></span> | <span data-ttu-id="3c48e-132">Lagersted</span><span class="sxs-lookup"><span data-stu-id="3c48e-132">Warehouse</span></span> | <span data-ttu-id="3c48e-133">Tilgang</span><span class="sxs-lookup"><span data-stu-id="3c48e-133">Receipt</span></span>   | <span data-ttu-id="3c48e-134">Udsted</span><span class="sxs-lookup"><span data-stu-id="3c48e-134">Issue</span></span> | <span data-ttu-id="3c48e-135">Fysisk dato</span><span class="sxs-lookup"><span data-stu-id="3c48e-135">Physical date</span></span> | <span data-ttu-id="3c48e-136">Økonomisk dato</span><span class="sxs-lookup"><span data-stu-id="3c48e-136">Financial date</span></span> | <span data-ttu-id="3c48e-137">Kvantitet</span><span class="sxs-lookup"><span data-stu-id="3c48e-137">Quantity</span></span> | <span data-ttu-id="3c48e-138">Kostbeløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-138">Cost amount</span></span> | <span data-ttu-id="3c48e-139">Fysisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="3c48e-140">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="3c48e-140">Purchase order</span></span> | <span data-ttu-id="3c48e-141">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-141">1</span></span>    | <span data-ttu-id="3c48e-142">11</span><span class="sxs-lookup"><span data-stu-id="3c48e-142">11</span></span>        | <span data-ttu-id="3c48e-143">Købt</span><span class="sxs-lookup"><span data-stu-id="3c48e-143">Purchased</span></span> |       | <span data-ttu-id="3c48e-144">15. marts</span><span class="sxs-lookup"><span data-stu-id="3c48e-144">March 15</span></span>      | <span data-ttu-id="3c48e-145">15. marts</span><span class="sxs-lookup"><span data-stu-id="3c48e-145">March 15</span></span>       | <span data-ttu-id="3c48e-146">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-146">10</span></span>       | <span data-ttu-id="3c48e-147">1.000</span><span class="sxs-lookup"><span data-stu-id="3c48e-147">1,000</span></span>       | <span data-ttu-id="3c48e-148">1.000</span><span class="sxs-lookup"><span data-stu-id="3c48e-148">1,000</span></span>                |
| <span data-ttu-id="3c48e-149">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="3c48e-149">Purchase order</span></span> | <span data-ttu-id="3c48e-150">2</span><span class="sxs-lookup"><span data-stu-id="3c48e-150">2</span></span>    | <span data-ttu-id="3c48e-151">21</span><span class="sxs-lookup"><span data-stu-id="3c48e-151">21</span></span>        | <span data-ttu-id="3c48e-152">Købt</span><span class="sxs-lookup"><span data-stu-id="3c48e-152">Purchased</span></span> |       | <span data-ttu-id="3c48e-153">15. marts</span><span class="sxs-lookup"><span data-stu-id="3c48e-153">March 15</span></span>      | <span data-ttu-id="3c48e-154">15. marts</span><span class="sxs-lookup"><span data-stu-id="3c48e-154">March 15</span></span>       | <span data-ttu-id="3c48e-155">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-155">10</span></span>       | <span data-ttu-id="3c48e-156">2,000</span><span class="sxs-lookup"><span data-stu-id="3c48e-156">2,000</span></span>       | <span data-ttu-id="3c48e-157">2,000</span><span class="sxs-lookup"><span data-stu-id="3c48e-157">2,000</span></span>                |
| <span data-ttu-id="3c48e-158">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="3c48e-158">Purchase order</span></span> | <span data-ttu-id="3c48e-159">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-159">1</span></span>    | <span data-ttu-id="3c48e-160">11</span><span class="sxs-lookup"><span data-stu-id="3c48e-160">11</span></span>        | <span data-ttu-id="3c48e-161">Modtaget</span><span class="sxs-lookup"><span data-stu-id="3c48e-161">Received</span></span>  |       | <span data-ttu-id="3c48e-162">15. april</span><span class="sxs-lookup"><span data-stu-id="3c48e-162">April 15</span></span>      |                | <span data-ttu-id="3c48e-163">5</span><span class="sxs-lookup"><span data-stu-id="3c48e-163">5</span></span>        |             | <span data-ttu-id="3c48e-164">375</span><span class="sxs-lookup"><span data-stu-id="3c48e-164">375</span></span>                  |
| <span data-ttu-id="3c48e-165">Overførselsordre</span><span class="sxs-lookup"><span data-stu-id="3c48e-165">Transfer order</span></span> | <span data-ttu-id="3c48e-166">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-166">1</span></span>    | <span data-ttu-id="3c48e-167">11</span><span class="sxs-lookup"><span data-stu-id="3c48e-167">11</span></span>        |           | <span data-ttu-id="3c48e-168">Solgt</span><span class="sxs-lookup"><span data-stu-id="3c48e-168">Sold</span></span>  | <span data-ttu-id="3c48e-169">Maj 2</span><span class="sxs-lookup"><span data-stu-id="3c48e-169">May 2</span></span>         | <span data-ttu-id="3c48e-170">Maj 2</span><span class="sxs-lookup"><span data-stu-id="3c48e-170">May 2</span></span>          | <span data-ttu-id="3c48e-171">-5</span><span class="sxs-lookup"><span data-stu-id="3c48e-171">-5</span></span>       | <span data-ttu-id="3c48e-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="3c48e-172">-458.33</span></span>     | <span data-ttu-id="3c48e-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="3c48e-173">-458.33</span></span>              |
| <span data-ttu-id="3c48e-174">Overførselsordre</span><span class="sxs-lookup"><span data-stu-id="3c48e-174">Transfer order</span></span> | <span data-ttu-id="3c48e-175">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-175">1</span></span>    | <span data-ttu-id="3c48e-176">12</span><span class="sxs-lookup"><span data-stu-id="3c48e-176">12</span></span>        | <span data-ttu-id="3c48e-177">Købt</span><span class="sxs-lookup"><span data-stu-id="3c48e-177">Purchased</span></span> |       | <span data-ttu-id="3c48e-178">Maj 2</span><span class="sxs-lookup"><span data-stu-id="3c48e-178">May 2</span></span>         | <span data-ttu-id="3c48e-179">Maj 2</span><span class="sxs-lookup"><span data-stu-id="3c48e-179">May 2</span></span>          | <span data-ttu-id="3c48e-180">5</span><span class="sxs-lookup"><span data-stu-id="3c48e-180">5</span></span>        | <span data-ttu-id="3c48e-181">458.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-181">458.33</span></span>      | <span data-ttu-id="3c48e-182">458.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-182">458.33</span></span>               |
| <span data-ttu-id="3c48e-183">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="3c48e-183">Sales order</span></span>    | <span data-ttu-id="3c48e-184">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-184">1</span></span>    | <span data-ttu-id="3c48e-185">12</span><span class="sxs-lookup"><span data-stu-id="3c48e-185">12</span></span>        |           | <span data-ttu-id="3c48e-186">Solgt</span><span class="sxs-lookup"><span data-stu-id="3c48e-186">Sold</span></span>  | <span data-ttu-id="3c48e-187">Maj 3</span><span class="sxs-lookup"><span data-stu-id="3c48e-187">May 3</span></span>         | <span data-ttu-id="3c48e-188">Maj 3</span><span class="sxs-lookup"><span data-stu-id="3c48e-188">May 3</span></span>          | <span data-ttu-id="3c48e-189">-1</span><span class="sxs-lookup"><span data-stu-id="3c48e-189">-1</span></span>       | <span data-ttu-id="3c48e-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="3c48e-190">-91.67</span></span>      | <span data-ttu-id="3c48e-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="3c48e-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="3c48e-192">Hvordan antal og beløb i hver periodes filsæt beregnes</span><span class="sxs-lookup"><span data-stu-id="3c48e-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="3c48e-193">Ved hjælp af de eksempeldata, der er beskrevet i de forrige afsnit, kan du køre en **Aldersfordelt lager**-rapport, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3c48e-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="3c48e-194">**Pr. dato:** *9. maj 2020*</span><span class="sxs-lookup"><span data-stu-id="3c48e-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="3c48e-195">**Lokation:** *Vis*</span><span class="sxs-lookup"><span data-stu-id="3c48e-195">**Site:** *View*</span></span>
- <span data-ttu-id="3c48e-196">**Lagersted:** *Nr.*</span><span class="sxs-lookup"><span data-stu-id="3c48e-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="3c48e-197">**Varenummer:** *Total*</span><span class="sxs-lookup"><span data-stu-id="3c48e-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="3c48e-198">**Forældelsesperiode:** Angiv dette felt, hvis du vil generere månedlige filsæt.</span><span class="sxs-lookup"><span data-stu-id="3c48e-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="3c48e-199">I dette tilfælde ligner indholdet af den rapport, der genereres, følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="3c48e-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="3c48e-200">varenummer</span><span class="sxs-lookup"><span data-stu-id="3c48e-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-201">Lokation</span><span class="sxs-lookup"><span data-stu-id="3c48e-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-202">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="3c48e-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-203">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="3c48e-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-204">Lagerværdimængde</span><span class="sxs-lookup"><span data-stu-id="3c48e-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-205">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="3c48e-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-206">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="3c48e-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="3c48e-210">P1:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-211">P1:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="3c48e-212">P2:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-213">P2:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="3c48e-214">P3:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-215">P3:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="3c48e-216">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-216">1000</span></span></td>
    <td><span data-ttu-id="3c48e-217">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-217">1</span></span></td>
    <td><span data-ttu-id="3c48e-218">14</span><span class="sxs-lookup"><span data-stu-id="3c48e-218">14</span></span></td>
    <td><span data-ttu-id="3c48e-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-219">1,283.33</span></span></td>
    <td><span data-ttu-id="3c48e-220">14</span><span class="sxs-lookup"><span data-stu-id="3c48e-220">14</span></span></td>
    <td><span data-ttu-id="3c48e-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-221">1,283.33</span></span></td>
    <td><span data-ttu-id="3c48e-222">91.67</span><span class="sxs-lookup"><span data-stu-id="3c48e-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-223">5.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-223">5.00</span></span></td>
    <td><span data-ttu-id="3c48e-224">458.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-224">458.33</span></span></td>
    <td><span data-ttu-id="3c48e-225">9.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-225">9.00</span></span></td>
    <td><span data-ttu-id="3c48e-226">825.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="3c48e-227">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-227">1000</span></span></td>
    <td><span data-ttu-id="3c48e-228">2</span><span class="sxs-lookup"><span data-stu-id="3c48e-228">2</span></span></td>
    <td><span data-ttu-id="3c48e-229">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-229">10</span></span></td>
    <td><span data-ttu-id="3c48e-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-230">2,000.00</span></span></td>
    <td><span data-ttu-id="3c48e-231">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-231">10</span></span></td>
    <td><span data-ttu-id="3c48e-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-232">2,000.00</span></span></td>
    <td><span data-ttu-id="3c48e-233">200.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-234">10.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-234">10.00</span></span></td>
    <td><span data-ttu-id="3c48e-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="3c48e-236"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="3c48e-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="3c48e-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="3c48e-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="3c48e-243">Bemærk følgende oplysninger i følgende eksempelrapport:</span><span class="sxs-lookup"><span data-stu-id="3c48e-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="3c48e-244">De værdier af **Lagerværdiantal**, **Lagerværdi** og **Gennemsnitlig enhedskostpris**, der vises i rapporten, er værdier for den økonomiske lagerdimension (**Lokation** i dette tilfælde).</span><span class="sxs-lookup"><span data-stu-id="3c48e-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="3c48e-245">I rapporten for lokation 1 vises f.eks. følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="3c48e-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="3c48e-246">Værdien af **Lagerværdiantal** er *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="3c48e-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="3c48e-247">Værdien af **Lagerværdi** er *1.283,33* (= 1.000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="3c48e-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="3c48e-248">Værdien af **Gennemsnitlig enhedskostpris** er *91,67*.</span><span class="sxs-lookup"><span data-stu-id="3c48e-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="3c48e-249">Værdien af **Disponibel værdi** og **Beløb**-værdien i hver periodes filsæt beregnes ved hjælp af **Gennemsnitlig enhedskostpris**-værdien.</span><span class="sxs-lookup"><span data-stu-id="3c48e-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="3c48e-250">Rapporten bestemmer det disponible antal for hvert periodefilsæt ved at opsummere det samlede modtagne lagerantal for hvert periodefilsæt.</span><span class="sxs-lookup"><span data-stu-id="3c48e-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="3c48e-251">Derefter anvendes FIFO-princippet (First In – First Out) til at fratrække det samlede afgåede antal, uanset hvilken lagermodel varerne bruges til.</span><span class="sxs-lookup"><span data-stu-id="3c48e-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="3c48e-252">Hvis du kører den samme rapport igen, men denne gang angiver både feltet **Lokation** og **Lagersted** til *Vis*, minder den nye rapport om følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="3c48e-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="3c48e-253">varenummer</span><span class="sxs-lookup"><span data-stu-id="3c48e-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-254">Lokation</span><span class="sxs-lookup"><span data-stu-id="3c48e-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-255">Lagersted</span><span class="sxs-lookup"><span data-stu-id="3c48e-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-256">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="3c48e-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-257">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="3c48e-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-258">Lagerværdimængde</span><span class="sxs-lookup"><span data-stu-id="3c48e-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-259">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="3c48e-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-260">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="3c48e-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="3c48e-264">P1:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-265">P1:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="3c48e-266">P2:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-267">P2:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="3c48e-268">P3:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-269">P3:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="3c48e-270">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-270">1000</span></span></td>
    <td><span data-ttu-id="3c48e-271">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-271">1</span></span></td>
    <td><span data-ttu-id="3c48e-272">11</span><span class="sxs-lookup"><span data-stu-id="3c48e-272">11</span></span></td>
    <td><span data-ttu-id="3c48e-273">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-273">10</span></span></td>
    <td><span data-ttu-id="3c48e-274">916.67</span><span class="sxs-lookup"><span data-stu-id="3c48e-274">916.67</span></span></td>
    <td><span data-ttu-id="3c48e-275">14</span><span class="sxs-lookup"><span data-stu-id="3c48e-275">14</span></span></td>
    <td><span data-ttu-id="3c48e-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-276">1,283.33</span></span></td>
    <td><span data-ttu-id="3c48e-277">91.67</span><span class="sxs-lookup"><span data-stu-id="3c48e-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-278">5.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-278">5.00</span></span></td>
    <td><span data-ttu-id="3c48e-279">458.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-279">458.33</span></span></td>
    <td><span data-ttu-id="3c48e-280">5.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-280">5.00</span></span></td>
    <td><span data-ttu-id="3c48e-281">458.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="3c48e-282">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-282">1000</span></span></td>
    <td><span data-ttu-id="3c48e-283">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-283">1</span></span></td>
    <td><span data-ttu-id="3c48e-284">12</span><span class="sxs-lookup"><span data-stu-id="3c48e-284">12</span></span></td>
    <td><span data-ttu-id="3c48e-285">4</span><span class="sxs-lookup"><span data-stu-id="3c48e-285">4</span></span></td>
    <td><span data-ttu-id="3c48e-286">366.67</span><span class="sxs-lookup"><span data-stu-id="3c48e-286">366.67</span></span></td>
    <td><span data-ttu-id="3c48e-287">14</span><span class="sxs-lookup"><span data-stu-id="3c48e-287">14</span></span></td>
    <td><span data-ttu-id="3c48e-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3c48e-288">1,283.33</span></span></td>
    <td><span data-ttu-id="3c48e-289">91.67</span><span class="sxs-lookup"><span data-stu-id="3c48e-289">91.67</span></span></td>
    <td><span data-ttu-id="3c48e-290">4.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-290">4.00</span></span></td>
    <td><span data-ttu-id="3c48e-291">366.67</span><span class="sxs-lookup"><span data-stu-id="3c48e-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="3c48e-292">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-292">1000</span></span></td>
    <td><span data-ttu-id="3c48e-293">2</span><span class="sxs-lookup"><span data-stu-id="3c48e-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="3c48e-294">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-294">10</span></span></td>
    <td><span data-ttu-id="3c48e-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-295">2,000.00</span></span></td>
    <td><span data-ttu-id="3c48e-296">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-296">10</span></span></td>
    <td><span data-ttu-id="3c48e-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-297">2,000.00</span></span></td>
    <td><span data-ttu-id="3c48e-298">200.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-299">10.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-299">10.00</span></span></td>
    <td><span data-ttu-id="3c48e-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="3c48e-301"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="3c48e-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="3c48e-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="3c48e-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="3c48e-310">Denne gang er lokation 1 opdelt i to rækker, én for lagersted 11 og én til lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="3c48e-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="3c48e-311">Men værdierne af **Lagerværdiantal**, **Lagerværdi** og **Gennemsnitlig enhedskostpris** er de samme, fordi **Lagersted** ikke er en økonomisk lagerdimension.</span><span class="sxs-lookup"><span data-stu-id="3c48e-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="3c48e-312">Bemærk desuden, at antalsfordelingen på lokation 1 er anderledes.</span><span class="sxs-lookup"><span data-stu-id="3c48e-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="3c48e-313">I den første rapport, du har kørt, ignorerede systemet den flytteordre, der fandt sted på samme lokation, og trak antallet i salgsfakturaen fra perioden **3/31/2020-3/1/2020** på lokation 1.</span><span class="sxs-lookup"><span data-stu-id="3c48e-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="3c48e-314">Men i den nye rapport trækker systemet antallet i salgsfakturaen fra perioden **5/8/2020 - 5/1/2020** på lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="3c48e-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="3c48e-315">Virkning af lagerlukning</span><span class="sxs-lookup"><span data-stu-id="3c48e-315">Effects of inventory closing</span></span>

<span data-ttu-id="3c48e-316">Hvis du kører lagerlukning for maj og derefter kører den forrige rapport igen, men angiver feltet **Pr. dato** til *31. maj 2020*, vil du bemærke følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="3c48e-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="3c48e-317">Værdierne af **Lagerværdi** og **Gennemsnitlig enhedskostpris** opdateres.</span><span class="sxs-lookup"><span data-stu-id="3c48e-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="3c48e-318">Værdien af **Disponibel værdi** og alle **Beløb**-værdier i alle perioder opdateres tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="3c48e-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="3c48e-319">Rapporten ser nu ud som i følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="3c48e-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="3c48e-320">varenummer</span><span class="sxs-lookup"><span data-stu-id="3c48e-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-321">Lokation</span><span class="sxs-lookup"><span data-stu-id="3c48e-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-322">Lagersted</span><span class="sxs-lookup"><span data-stu-id="3c48e-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-323">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="3c48e-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-324">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="3c48e-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-325">Lagerværdimængde</span><span class="sxs-lookup"><span data-stu-id="3c48e-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-326">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="3c48e-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3c48e-327">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="3c48e-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3c48e-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="3c48e-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="3c48e-331">P1:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-332">P1:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="3c48e-333">P2:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-334">P2:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="3c48e-335">P3:antal</span><span class="sxs-lookup"><span data-stu-id="3c48e-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="3c48e-336">P3:beløb</span><span class="sxs-lookup"><span data-stu-id="3c48e-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="3c48e-337">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-337">1000</span></span></td>
    <td><span data-ttu-id="3c48e-338">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-338">1</span></span></td>
    <td><span data-ttu-id="3c48e-339">11</span><span class="sxs-lookup"><span data-stu-id="3c48e-339">11</span></span></td>
    <td><span data-ttu-id="3c48e-340">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-340">10</span></span></td>
    <td><span data-ttu-id="3c48e-341">910.70</span><span class="sxs-lookup"><span data-stu-id="3c48e-341">910.70</span></span></td>
    <td><span data-ttu-id="3c48e-342">14</span><span class="sxs-lookup"><span data-stu-id="3c48e-342">14</span></span></td>
    <td><span data-ttu-id="3c48e-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-343">1,275.00</span></span></td>
    <td><span data-ttu-id="3c48e-344">91.07</span><span class="sxs-lookup"><span data-stu-id="3c48e-344">91.07</span></span></td>
    <td><span data-ttu-id="3c48e-345">0,00</span><span class="sxs-lookup"><span data-stu-id="3c48e-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="3c48e-346">5.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-346">5.00</span></span></td>
    <td><span data-ttu-id="3c48e-347">455.36</span><span class="sxs-lookup"><span data-stu-id="3c48e-347">455.36</span></span></td>
    <td><span data-ttu-id="3c48e-348">5.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-348">5.00</span></span></td>
    <td><span data-ttu-id="3c48e-349">455.36</span><span class="sxs-lookup"><span data-stu-id="3c48e-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="3c48e-350">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-350">1000</span></span></td>
    <td><span data-ttu-id="3c48e-351">1</span><span class="sxs-lookup"><span data-stu-id="3c48e-351">1</span></span></td>
    <td><span data-ttu-id="3c48e-352">12</span><span class="sxs-lookup"><span data-stu-id="3c48e-352">12</span></span></td>
    <td><span data-ttu-id="3c48e-353">4</span><span class="sxs-lookup"><span data-stu-id="3c48e-353">4</span></span></td>
    <td><span data-ttu-id="3c48e-354">364.29</span><span class="sxs-lookup"><span data-stu-id="3c48e-354">364.29</span></span></td>
    <td><span data-ttu-id="3c48e-355">14</span><span class="sxs-lookup"><span data-stu-id="3c48e-355">14</span></span></td>
    <td><span data-ttu-id="3c48e-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-356">1,275.00</span></span></td>
    <td><span data-ttu-id="3c48e-357">91.07</span><span class="sxs-lookup"><span data-stu-id="3c48e-357">91.07</span></span></td>
    <td><span data-ttu-id="3c48e-358">4.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-358">4.00</span></span></td>
    <td><span data-ttu-id="3c48e-359">364.29</span><span class="sxs-lookup"><span data-stu-id="3c48e-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="3c48e-360">1000</span><span class="sxs-lookup"><span data-stu-id="3c48e-360">1000</span></span></td>
    <td><span data-ttu-id="3c48e-361">2</span><span class="sxs-lookup"><span data-stu-id="3c48e-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="3c48e-362">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-362">10</span></span></td>
    <td><span data-ttu-id="3c48e-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-363">2,000.00</span></span></td>
    <td><span data-ttu-id="3c48e-364">10</span><span class="sxs-lookup"><span data-stu-id="3c48e-364">10</span></span></td>
    <td><span data-ttu-id="3c48e-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-365">2,000.00</span></span></td>
    <td><span data-ttu-id="3c48e-366">200.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-367">10.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-367">10.00</span></span></td>
    <td><span data-ttu-id="3c48e-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3c48e-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="3c48e-369"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3c48e-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="3c48e-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="3c48e-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="3c48e-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="3c48e-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="3c48e-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]