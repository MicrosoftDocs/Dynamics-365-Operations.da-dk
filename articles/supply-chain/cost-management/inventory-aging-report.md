---
title: Eksempler og logik til rapport over aldersfordelt lager
description: I dette emne vises nogle eksempler på, hvordan resultaterne af en rapport over aldersfordelt lager fortolkes.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484524"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="75cfa-103">Eksempler og logik til rapport over aldersfordelt lager</span><span class="sxs-lookup"><span data-stu-id="75cfa-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75cfa-104">I dette emne vises nogle eksempler på, hvordan resultaterne af rapporten **Aldersfordelt lager** fortolkes.</span><span class="sxs-lookup"><span data-stu-id="75cfa-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="75cfa-105">Denne rapport kategoriserer det disponible antal og lagerværdier for en valgt vare eller varegruppe i flere perioder.</span><span class="sxs-lookup"><span data-stu-id="75cfa-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="75cfa-106">I dette emne vises også rapportens interne logik.</span><span class="sxs-lookup"><span data-stu-id="75cfa-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="75cfa-107">Eksemplerne i dette emne viser resultater, der præsenteres i en rapport over standard **Aldersfordelt lager**.</span><span class="sxs-lookup"><span data-stu-id="75cfa-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="75cfa-108">Generelt anbefales det dog, at du bruger [Lagerrapport over aldersfordelt lager](inventory-aging-report-storage.md)-versionen af denne rapport, specielt hvis du har mange varer og lagersteder, der skal behandles.</span><span class="sxs-lookup"><span data-stu-id="75cfa-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="75cfa-109">Lagerrapport over aldersfordelt lager gemmer alle de rapporter, du genererer, viser resultaterne som en interaktiv side og et diagram og giver dig mulighed for at eksportere gemte rapporter.</span><span class="sxs-lookup"><span data-stu-id="75cfa-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="75cfa-110">Eksempeldata, der bruges i disse eksempler</span><span class="sxs-lookup"><span data-stu-id="75cfa-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="75cfa-111">Eksemplerne i dette emne er baseret på de eksempeldata fra lagertransaktioner, der er beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="75cfa-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="75cfa-112">Konfiguration af lagringsdimension</span><span class="sxs-lookup"><span data-stu-id="75cfa-112">Storage dimension setup</span></span>

<span data-ttu-id="75cfa-113">Systemeksemplet indeholder følgende opsætning af lagringsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="75cfa-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="75cfa-114">Navn</span><span class="sxs-lookup"><span data-stu-id="75cfa-114">Name</span></span>      | <span data-ttu-id="75cfa-115">Aktivt</span><span class="sxs-lookup"><span data-stu-id="75cfa-115">Active</span></span> | <span data-ttu-id="75cfa-116">Fysisk lager</span><span class="sxs-lookup"><span data-stu-id="75cfa-116">Physical inventory</span></span> | <span data-ttu-id="75cfa-117">Økonomisk lager</span><span class="sxs-lookup"><span data-stu-id="75cfa-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="75cfa-118">Lokation</span><span class="sxs-lookup"><span data-stu-id="75cfa-118">Site</span></span>      | <span data-ttu-id="75cfa-119">Ja</span><span class="sxs-lookup"><span data-stu-id="75cfa-119">Yes</span></span>    | <span data-ttu-id="75cfa-120">Ja</span><span class="sxs-lookup"><span data-stu-id="75cfa-120">Yes</span></span>                | <span data-ttu-id="75cfa-121">Ja</span><span class="sxs-lookup"><span data-stu-id="75cfa-121">Yes</span></span>                 |
| <span data-ttu-id="75cfa-122">Lagersted</span><span class="sxs-lookup"><span data-stu-id="75cfa-122">Warehouse</span></span> | <span data-ttu-id="75cfa-123">Ja</span><span class="sxs-lookup"><span data-stu-id="75cfa-123">Yes</span></span>    | <span data-ttu-id="75cfa-124">Ja</span><span class="sxs-lookup"><span data-stu-id="75cfa-124">Yes</span></span>                | <span data-ttu-id="75cfa-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="75cfa-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="75cfa-126">Lagermodel</span><span class="sxs-lookup"><span data-stu-id="75cfa-126">Inventory model</span></span>

<span data-ttu-id="75cfa-127">I forbindelse med eksempelsystemet er lagermodellen for de frigivne produkter *FIFO* og **Kostpris**-indstillingen for lagermodellen er *Medtag fysisk værdi*.</span><span class="sxs-lookup"><span data-stu-id="75cfa-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="75cfa-128">Lagerbevægelser</span><span class="sxs-lookup"><span data-stu-id="75cfa-128">Inventory transactions</span></span>

<span data-ttu-id="75cfa-129">Eksempelsystemet indeholder følgende lagertransaktioner for et frigivet produkt, der har varenummeret *1000*.</span><span class="sxs-lookup"><span data-stu-id="75cfa-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="75cfa-130">Reference</span><span class="sxs-lookup"><span data-stu-id="75cfa-130">Reference</span></span>      | <span data-ttu-id="75cfa-131">Lokation</span><span class="sxs-lookup"><span data-stu-id="75cfa-131">Site</span></span> | <span data-ttu-id="75cfa-132">Lagersted</span><span class="sxs-lookup"><span data-stu-id="75cfa-132">Warehouse</span></span> | <span data-ttu-id="75cfa-133">Tilgang</span><span class="sxs-lookup"><span data-stu-id="75cfa-133">Receipt</span></span>   | <span data-ttu-id="75cfa-134">Udsted</span><span class="sxs-lookup"><span data-stu-id="75cfa-134">Issue</span></span> | <span data-ttu-id="75cfa-135">Fysisk dato</span><span class="sxs-lookup"><span data-stu-id="75cfa-135">Physical date</span></span> | <span data-ttu-id="75cfa-136">Økonomisk dato</span><span class="sxs-lookup"><span data-stu-id="75cfa-136">Financial date</span></span> | <span data-ttu-id="75cfa-137">Kvantitet</span><span class="sxs-lookup"><span data-stu-id="75cfa-137">Quantity</span></span> | <span data-ttu-id="75cfa-138">Kostbeløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-138">Cost amount</span></span> | <span data-ttu-id="75cfa-139">Fysisk kostbeløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="75cfa-140">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="75cfa-140">Purchase order</span></span> | <span data-ttu-id="75cfa-141">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-141">1</span></span>    | <span data-ttu-id="75cfa-142">11</span><span class="sxs-lookup"><span data-stu-id="75cfa-142">11</span></span>        | <span data-ttu-id="75cfa-143">Købt</span><span class="sxs-lookup"><span data-stu-id="75cfa-143">Purchased</span></span> |       | <span data-ttu-id="75cfa-144">15. marts</span><span class="sxs-lookup"><span data-stu-id="75cfa-144">March 15</span></span>      | <span data-ttu-id="75cfa-145">15. marts</span><span class="sxs-lookup"><span data-stu-id="75cfa-145">March 15</span></span>       | <span data-ttu-id="75cfa-146">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-146">10</span></span>       | <span data-ttu-id="75cfa-147">1.000</span><span class="sxs-lookup"><span data-stu-id="75cfa-147">1,000</span></span>       | <span data-ttu-id="75cfa-148">1.000</span><span class="sxs-lookup"><span data-stu-id="75cfa-148">1,000</span></span>                |
| <span data-ttu-id="75cfa-149">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="75cfa-149">Purchase order</span></span> | <span data-ttu-id="75cfa-150">2</span><span class="sxs-lookup"><span data-stu-id="75cfa-150">2</span></span>    | <span data-ttu-id="75cfa-151">21</span><span class="sxs-lookup"><span data-stu-id="75cfa-151">21</span></span>        | <span data-ttu-id="75cfa-152">Købt</span><span class="sxs-lookup"><span data-stu-id="75cfa-152">Purchased</span></span> |       | <span data-ttu-id="75cfa-153">15. marts</span><span class="sxs-lookup"><span data-stu-id="75cfa-153">March 15</span></span>      | <span data-ttu-id="75cfa-154">15. marts</span><span class="sxs-lookup"><span data-stu-id="75cfa-154">March 15</span></span>       | <span data-ttu-id="75cfa-155">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-155">10</span></span>       | <span data-ttu-id="75cfa-156">2,000</span><span class="sxs-lookup"><span data-stu-id="75cfa-156">2,000</span></span>       | <span data-ttu-id="75cfa-157">2,000</span><span class="sxs-lookup"><span data-stu-id="75cfa-157">2,000</span></span>                |
| <span data-ttu-id="75cfa-158">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="75cfa-158">Purchase order</span></span> | <span data-ttu-id="75cfa-159">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-159">1</span></span>    | <span data-ttu-id="75cfa-160">11</span><span class="sxs-lookup"><span data-stu-id="75cfa-160">11</span></span>        | <span data-ttu-id="75cfa-161">Modtaget</span><span class="sxs-lookup"><span data-stu-id="75cfa-161">Received</span></span>  |       | <span data-ttu-id="75cfa-162">15. april</span><span class="sxs-lookup"><span data-stu-id="75cfa-162">April 15</span></span>      |                | <span data-ttu-id="75cfa-163">5</span><span class="sxs-lookup"><span data-stu-id="75cfa-163">5</span></span>        |             | <span data-ttu-id="75cfa-164">375</span><span class="sxs-lookup"><span data-stu-id="75cfa-164">375</span></span>                  |
| <span data-ttu-id="75cfa-165">Overførselsordre</span><span class="sxs-lookup"><span data-stu-id="75cfa-165">Transfer order</span></span> | <span data-ttu-id="75cfa-166">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-166">1</span></span>    | <span data-ttu-id="75cfa-167">11</span><span class="sxs-lookup"><span data-stu-id="75cfa-167">11</span></span>        |           | <span data-ttu-id="75cfa-168">Solgt</span><span class="sxs-lookup"><span data-stu-id="75cfa-168">Sold</span></span>  | <span data-ttu-id="75cfa-169">Maj 2</span><span class="sxs-lookup"><span data-stu-id="75cfa-169">May 2</span></span>         | <span data-ttu-id="75cfa-170">Maj 2</span><span class="sxs-lookup"><span data-stu-id="75cfa-170">May 2</span></span>          | <span data-ttu-id="75cfa-171">-5</span><span class="sxs-lookup"><span data-stu-id="75cfa-171">-5</span></span>       | <span data-ttu-id="75cfa-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="75cfa-172">-458.33</span></span>     | <span data-ttu-id="75cfa-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="75cfa-173">-458.33</span></span>              |
| <span data-ttu-id="75cfa-174">Overførselsordre</span><span class="sxs-lookup"><span data-stu-id="75cfa-174">Transfer order</span></span> | <span data-ttu-id="75cfa-175">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-175">1</span></span>    | <span data-ttu-id="75cfa-176">12</span><span class="sxs-lookup"><span data-stu-id="75cfa-176">12</span></span>        | <span data-ttu-id="75cfa-177">Købt</span><span class="sxs-lookup"><span data-stu-id="75cfa-177">Purchased</span></span> |       | <span data-ttu-id="75cfa-178">Maj 2</span><span class="sxs-lookup"><span data-stu-id="75cfa-178">May 2</span></span>         | <span data-ttu-id="75cfa-179">Maj 2</span><span class="sxs-lookup"><span data-stu-id="75cfa-179">May 2</span></span>          | <span data-ttu-id="75cfa-180">5</span><span class="sxs-lookup"><span data-stu-id="75cfa-180">5</span></span>        | <span data-ttu-id="75cfa-181">458.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-181">458.33</span></span>      | <span data-ttu-id="75cfa-182">458.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-182">458.33</span></span>               |
| <span data-ttu-id="75cfa-183">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="75cfa-183">Sales order</span></span>    | <span data-ttu-id="75cfa-184">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-184">1</span></span>    | <span data-ttu-id="75cfa-185">12</span><span class="sxs-lookup"><span data-stu-id="75cfa-185">12</span></span>        |           | <span data-ttu-id="75cfa-186">Solgt</span><span class="sxs-lookup"><span data-stu-id="75cfa-186">Sold</span></span>  | <span data-ttu-id="75cfa-187">Maj 3</span><span class="sxs-lookup"><span data-stu-id="75cfa-187">May 3</span></span>         | <span data-ttu-id="75cfa-188">Maj 3</span><span class="sxs-lookup"><span data-stu-id="75cfa-188">May 3</span></span>          | <span data-ttu-id="75cfa-189">-1</span><span class="sxs-lookup"><span data-stu-id="75cfa-189">-1</span></span>       | <span data-ttu-id="75cfa-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="75cfa-190">-91.67</span></span>      | <span data-ttu-id="75cfa-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="75cfa-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="75cfa-192">Hvordan antal og beløb i hver periodes filsæt beregnes</span><span class="sxs-lookup"><span data-stu-id="75cfa-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="75cfa-193">Ved hjælp af de eksempeldata, der er beskrevet i de forrige afsnit, kan du køre en **Aldersfordelt lager**-rapport, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="75cfa-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="75cfa-194">**Pr. dato:** *9. maj 2020*</span><span class="sxs-lookup"><span data-stu-id="75cfa-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="75cfa-195">**Lokation:** *Vis*</span><span class="sxs-lookup"><span data-stu-id="75cfa-195">**Site:** *View*</span></span>
- <span data-ttu-id="75cfa-196">**Lagersted:** *Nr.*</span><span class="sxs-lookup"><span data-stu-id="75cfa-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="75cfa-197">**Varenummer:** *Total*</span><span class="sxs-lookup"><span data-stu-id="75cfa-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="75cfa-198">**Forældelsesperiode:** Angiv dette felt, hvis du vil generere månedlige filsæt.</span><span class="sxs-lookup"><span data-stu-id="75cfa-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="75cfa-199">I dette tilfælde ligner indholdet af den rapport, der genereres, følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="75cfa-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="75cfa-200">varenummer</span><span class="sxs-lookup"><span data-stu-id="75cfa-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-201">Lokation</span><span class="sxs-lookup"><span data-stu-id="75cfa-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-202">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="75cfa-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-203">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="75cfa-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-204">Lagerværdimængde</span><span class="sxs-lookup"><span data-stu-id="75cfa-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-205">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="75cfa-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-206">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="75cfa-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-207">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-208">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-209">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="75cfa-210">P1:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-211">P1:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="75cfa-212">P2:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-213">P2:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="75cfa-214">P3:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-215">P3:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="75cfa-216">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-216">1000</span></span></td>
    <td><span data-ttu-id="75cfa-217">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-217">1</span></span></td>
    <td><span data-ttu-id="75cfa-218">14</span><span class="sxs-lookup"><span data-stu-id="75cfa-218">14</span></span></td>
    <td><span data-ttu-id="75cfa-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-219">1,283.33</span></span></td>
    <td><span data-ttu-id="75cfa-220">14</span><span class="sxs-lookup"><span data-stu-id="75cfa-220">14</span></span></td>
    <td><span data-ttu-id="75cfa-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-221">1,283.33</span></span></td>
    <td><span data-ttu-id="75cfa-222">91.67</span><span class="sxs-lookup"><span data-stu-id="75cfa-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-223">5.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-223">5.00</span></span></td>
    <td><span data-ttu-id="75cfa-224">458.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-224">458.33</span></span></td>
    <td><span data-ttu-id="75cfa-225">9.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-225">9.00</span></span></td>
    <td><span data-ttu-id="75cfa-226">825.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="75cfa-227">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-227">1000</span></span></td>
    <td><span data-ttu-id="75cfa-228">2</span><span class="sxs-lookup"><span data-stu-id="75cfa-228">2</span></span></td>
    <td><span data-ttu-id="75cfa-229">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-229">10</span></span></td>
    <td><span data-ttu-id="75cfa-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-230">2,000.00</span></span></td>
    <td><span data-ttu-id="75cfa-231">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-231">10</span></span></td>
    <td><span data-ttu-id="75cfa-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-232">2,000.00</span></span></td>
    <td><span data-ttu-id="75cfa-233">200.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-234">10.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-234">10.00</span></span></td>
    <td><span data-ttu-id="75cfa-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="75cfa-236"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="75cfa-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="75cfa-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="75cfa-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="75cfa-243">Bemærk følgende oplysninger i følgende eksempelrapport:</span><span class="sxs-lookup"><span data-stu-id="75cfa-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="75cfa-244">De værdier af **Lagerværdiantal**, **Lagerværdi** og **Gennemsnitlig enhedskostpris**, der vises i rapporten, er værdier for den økonomiske lagerdimension (**Lokation** i dette tilfælde).</span><span class="sxs-lookup"><span data-stu-id="75cfa-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="75cfa-245">I rapporten for lokation 1 vises f.eks. følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="75cfa-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="75cfa-246">Værdien af **Lagerværdiantal** er *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="75cfa-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="75cfa-247">Værdien af **Lagerværdi** er *1.283,33* (= 1.000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="75cfa-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="75cfa-248">Værdien af **Gennemsnitlig enhedskostpris** er *91,67*.</span><span class="sxs-lookup"><span data-stu-id="75cfa-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="75cfa-249">Værdien af **Disponibel værdi** og **Beløb**-værdien i hver periodes filsæt beregnes ved hjælp af **Gennemsnitlig enhedskostpris**-værdien.</span><span class="sxs-lookup"><span data-stu-id="75cfa-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="75cfa-250">Rapporten bestemmer det disponible antal for hvert periodefilsæt ved at opsummere det samlede modtagne lagerantal for hvert periodefilsæt.</span><span class="sxs-lookup"><span data-stu-id="75cfa-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="75cfa-251">Derefter anvendes FIFO-princippet (First In – First Out) til at fratrække det samlede afgåede antal, uanset hvilken lagermodel varerne bruges til.</span><span class="sxs-lookup"><span data-stu-id="75cfa-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="75cfa-252">Hvis du kører den samme rapport igen, men denne gang angiver både feltet **Lokation** og **Lagersted** til *Vis*, minder den nye rapport om følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="75cfa-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="75cfa-253">varenummer</span><span class="sxs-lookup"><span data-stu-id="75cfa-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-254">Lokation</span><span class="sxs-lookup"><span data-stu-id="75cfa-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-255">Lagersted</span><span class="sxs-lookup"><span data-stu-id="75cfa-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-256">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="75cfa-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-257">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="75cfa-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-258">Lagerværdimængde</span><span class="sxs-lookup"><span data-stu-id="75cfa-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-259">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="75cfa-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-260">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="75cfa-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-261">5/8/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-262">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-263">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="75cfa-264">P1:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-265">P1:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="75cfa-266">P2:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-267">P2:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="75cfa-268">P3:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-269">P3:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="75cfa-270">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-270">1000</span></span></td>
    <td><span data-ttu-id="75cfa-271">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-271">1</span></span></td>
    <td><span data-ttu-id="75cfa-272">11</span><span class="sxs-lookup"><span data-stu-id="75cfa-272">11</span></span></td>
    <td><span data-ttu-id="75cfa-273">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-273">10</span></span></td>
    <td><span data-ttu-id="75cfa-274">916.67</span><span class="sxs-lookup"><span data-stu-id="75cfa-274">916.67</span></span></td>
    <td><span data-ttu-id="75cfa-275">14</span><span class="sxs-lookup"><span data-stu-id="75cfa-275">14</span></span></td>
    <td><span data-ttu-id="75cfa-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-276">1,283.33</span></span></td>
    <td><span data-ttu-id="75cfa-277">91.67</span><span class="sxs-lookup"><span data-stu-id="75cfa-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-278">5.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-278">5.00</span></span></td>
    <td><span data-ttu-id="75cfa-279">458.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-279">458.33</span></span></td>
    <td><span data-ttu-id="75cfa-280">5.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-280">5.00</span></span></td>
    <td><span data-ttu-id="75cfa-281">458.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="75cfa-282">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-282">1000</span></span></td>
    <td><span data-ttu-id="75cfa-283">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-283">1</span></span></td>
    <td><span data-ttu-id="75cfa-284">12</span><span class="sxs-lookup"><span data-stu-id="75cfa-284">12</span></span></td>
    <td><span data-ttu-id="75cfa-285">4</span><span class="sxs-lookup"><span data-stu-id="75cfa-285">4</span></span></td>
    <td><span data-ttu-id="75cfa-286">366.67</span><span class="sxs-lookup"><span data-stu-id="75cfa-286">366.67</span></span></td>
    <td><span data-ttu-id="75cfa-287">14</span><span class="sxs-lookup"><span data-stu-id="75cfa-287">14</span></span></td>
    <td><span data-ttu-id="75cfa-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="75cfa-288">1,283.33</span></span></td>
    <td><span data-ttu-id="75cfa-289">91.67</span><span class="sxs-lookup"><span data-stu-id="75cfa-289">91.67</span></span></td>
    <td><span data-ttu-id="75cfa-290">4.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-290">4.00</span></span></td>
    <td><span data-ttu-id="75cfa-291">366.67</span><span class="sxs-lookup"><span data-stu-id="75cfa-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="75cfa-292">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-292">1000</span></span></td>
    <td><span data-ttu-id="75cfa-293">2</span><span class="sxs-lookup"><span data-stu-id="75cfa-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="75cfa-294">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-294">10</span></span></td>
    <td><span data-ttu-id="75cfa-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-295">2,000.00</span></span></td>
    <td><span data-ttu-id="75cfa-296">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-296">10</span></span></td>
    <td><span data-ttu-id="75cfa-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-297">2,000.00</span></span></td>
    <td><span data-ttu-id="75cfa-298">200.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-299">10.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-299">10.00</span></span></td>
    <td><span data-ttu-id="75cfa-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="75cfa-301"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="75cfa-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="75cfa-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="75cfa-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="75cfa-310">Denne gang er lokation 1 opdelt i to rækker, én for lagersted 11 og én til lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="75cfa-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="75cfa-311">Men værdierne af **Lagerværdiantal**, **Lagerværdi** og **Gennemsnitlig enhedskostpris** er de samme, fordi **Lagersted** ikke er en økonomisk lagerdimension.</span><span class="sxs-lookup"><span data-stu-id="75cfa-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="75cfa-312">Bemærk desuden, at antalsfordelingen på lokation 1 er anderledes.</span><span class="sxs-lookup"><span data-stu-id="75cfa-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="75cfa-313">I den første rapport, du har kørt, ignorerede systemet den flytteordre, der fandt sted på samme lokation, og trak antallet i salgsfakturaen fra perioden **3/31/2020-3/1/2020** på lokation 1.</span><span class="sxs-lookup"><span data-stu-id="75cfa-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="75cfa-314">Men i den nye rapport trækker systemet antallet i salgsfakturaen fra perioden **5/8/2020 - 5/1/2020** på lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="75cfa-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="75cfa-315">Virkning af lagerlukning</span><span class="sxs-lookup"><span data-stu-id="75cfa-315">Effects of inventory closing</span></span>

<span data-ttu-id="75cfa-316">Hvis du kører lagerlukning for maj og derefter kører den forrige rapport igen, men angiver feltet **Pr. dato** til *31. maj 2020*, vil du bemærke følgende resultater:</span><span class="sxs-lookup"><span data-stu-id="75cfa-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="75cfa-317">Værdierne af **Lagerværdi** og **Gennemsnitlig enhedskostpris** opdateres.</span><span class="sxs-lookup"><span data-stu-id="75cfa-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="75cfa-318">Værdien af **Disponibel værdi** og alle **Beløb**-værdier i alle perioder opdateres tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="75cfa-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="75cfa-319">Rapporten ser nu ud som i følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="75cfa-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="75cfa-320">varenummer</span><span class="sxs-lookup"><span data-stu-id="75cfa-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-321">Lokation</span><span class="sxs-lookup"><span data-stu-id="75cfa-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-322">Lagersted</span><span class="sxs-lookup"><span data-stu-id="75cfa-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-323">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="75cfa-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-324">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="75cfa-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-325">Lagerværdimængde</span><span class="sxs-lookup"><span data-stu-id="75cfa-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-326">Lagerværdi</span><span class="sxs-lookup"><span data-stu-id="75cfa-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="75cfa-327">Gennemsnitlig enhedskostpris</span><span class="sxs-lookup"><span data-stu-id="75cfa-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-328">5/31/2020 - 5/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-329">4/30/2020 - 4/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="75cfa-330">3/31/2020 - 3/1/2020</span><span class="sxs-lookup"><span data-stu-id="75cfa-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="75cfa-331">P1:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-332">P1:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="75cfa-333">P2:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-334">P2:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="75cfa-335">P3:antal</span><span class="sxs-lookup"><span data-stu-id="75cfa-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="75cfa-336">P3:beløb</span><span class="sxs-lookup"><span data-stu-id="75cfa-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="75cfa-337">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-337">1000</span></span></td>
    <td><span data-ttu-id="75cfa-338">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-338">1</span></span></td>
    <td><span data-ttu-id="75cfa-339">11</span><span class="sxs-lookup"><span data-stu-id="75cfa-339">11</span></span></td>
    <td><span data-ttu-id="75cfa-340">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-340">10</span></span></td>
    <td><span data-ttu-id="75cfa-341">910.70</span><span class="sxs-lookup"><span data-stu-id="75cfa-341">910.70</span></span></td>
    <td><span data-ttu-id="75cfa-342">14</span><span class="sxs-lookup"><span data-stu-id="75cfa-342">14</span></span></td>
    <td><span data-ttu-id="75cfa-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-343">1,275.00</span></span></td>
    <td><span data-ttu-id="75cfa-344">91.07</span><span class="sxs-lookup"><span data-stu-id="75cfa-344">91.07</span></span></td>
    <td><span data-ttu-id="75cfa-345">0,00</span><span class="sxs-lookup"><span data-stu-id="75cfa-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="75cfa-346">5.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-346">5.00</span></span></td>
    <td><span data-ttu-id="75cfa-347">455.36</span><span class="sxs-lookup"><span data-stu-id="75cfa-347">455.36</span></span></td>
    <td><span data-ttu-id="75cfa-348">5.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-348">5.00</span></span></td>
    <td><span data-ttu-id="75cfa-349">455.36</span><span class="sxs-lookup"><span data-stu-id="75cfa-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="75cfa-350">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-350">1000</span></span></td>
    <td><span data-ttu-id="75cfa-351">1</span><span class="sxs-lookup"><span data-stu-id="75cfa-351">1</span></span></td>
    <td><span data-ttu-id="75cfa-352">12</span><span class="sxs-lookup"><span data-stu-id="75cfa-352">12</span></span></td>
    <td><span data-ttu-id="75cfa-353">4</span><span class="sxs-lookup"><span data-stu-id="75cfa-353">4</span></span></td>
    <td><span data-ttu-id="75cfa-354">364.29</span><span class="sxs-lookup"><span data-stu-id="75cfa-354">364.29</span></span></td>
    <td><span data-ttu-id="75cfa-355">14</span><span class="sxs-lookup"><span data-stu-id="75cfa-355">14</span></span></td>
    <td><span data-ttu-id="75cfa-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-356">1,275.00</span></span></td>
    <td><span data-ttu-id="75cfa-357">91.07</span><span class="sxs-lookup"><span data-stu-id="75cfa-357">91.07</span></span></td>
    <td><span data-ttu-id="75cfa-358">4.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-358">4.00</span></span></td>
    <td><span data-ttu-id="75cfa-359">364.29</span><span class="sxs-lookup"><span data-stu-id="75cfa-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="75cfa-360">1000</span><span class="sxs-lookup"><span data-stu-id="75cfa-360">1000</span></span></td>
    <td><span data-ttu-id="75cfa-361">2</span><span class="sxs-lookup"><span data-stu-id="75cfa-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="75cfa-362">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-362">10</span></span></td>
    <td><span data-ttu-id="75cfa-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-363">2,000.00</span></span></td>
    <td><span data-ttu-id="75cfa-364">10</span><span class="sxs-lookup"><span data-stu-id="75cfa-364">10</span></span></td>
    <td><span data-ttu-id="75cfa-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-365">2,000.00</span></span></td>
    <td><span data-ttu-id="75cfa-366">200.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-367">10.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-367">10.00</span></span></td>
    <td><span data-ttu-id="75cfa-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="75cfa-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="75cfa-369"><strong>1000 totaler</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="75cfa-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="75cfa-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="75cfa-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="75cfa-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="75cfa-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="75cfa-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>