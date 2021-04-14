---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)'
description: Dette emne beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 3)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752406"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="ebd4e-104">ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)</span><span class="sxs-lookup"><span data-stu-id="ebd4e-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebd4e-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ebd4e-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="ebd4e-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 2: Modeltilknytning)".</span><span class="sxs-lookup"><span data-stu-id="ebd4e-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="ebd4e-108">Opret en rapport til visning af økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="ebd4e-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="ebd4e-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ebd4e-110">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ebd4e-111">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="ebd4e-112">Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="ebd4e-113">Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="ebd4e-114">Skriv "Finanskladderapport" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="ebd4e-115">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="ebd4e-116">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-116">Click Create configuration.</span></span>
8. <span data-ttu-id="ebd4e-117">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-117">Click Designer.</span></span>
9. <span data-ttu-id="ebd4e-118">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="ebd4e-119">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="ebd4e-120">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="ebd4e-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-121">Click OK.</span></span>
13. <span data-ttu-id="ebd4e-122">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="ebd4e-123">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="ebd4e-124">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="ebd4e-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-125">Click OK.</span></span>
17. <span data-ttu-id="ebd4e-126">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="ebd4e-127">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="ebd4e-128">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="ebd4e-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-129">Click OK.</span></span>
21. <span data-ttu-id="ebd4e-130">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="ebd4e-131">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ebd4e-132">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="ebd4e-133">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="ebd4e-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-134">Click OK.</span></span>
26. <span data-ttu-id="ebd4e-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="ebd4e-136">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="ebd4e-137">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="ebd4e-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-138">Click OK.</span></span>
30. <span data-ttu-id="ebd4e-139">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="ebd4e-140">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="ebd4e-141">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="ebd4e-142">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="ebd4e-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-143">Click OK.</span></span>
35. <span data-ttu-id="ebd4e-144">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="ebd4e-145">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="ebd4e-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-146">Click OK.</span></span>
38. <span data-ttu-id="ebd4e-147">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="ebd4e-148">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="ebd4e-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-149">Click OK.</span></span>
41. <span data-ttu-id="ebd4e-150">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="ebd4e-151">Skriv 'Dt' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="ebd4e-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-152">Click OK.</span></span>
44. <span data-ttu-id="ebd4e-153">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="ebd4e-154">Skriv 'Ct' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="ebd4e-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-155">Click OK.</span></span>
47. <span data-ttu-id="ebd4e-156">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="ebd4e-157">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="ebd4e-158">Skriv 'Dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="ebd4e-159">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-159">Click OK.</span></span>
51. <span data-ttu-id="ebd4e-160">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="ebd4e-161">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="ebd4e-162">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="ebd4e-163">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="ebd4e-164">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-164">Click OK.</span></span>
56. <span data-ttu-id="ebd4e-165">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="ebd4e-166">Skriv 'Værdi' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="ebd4e-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-167">Click OK.</span></span>
59. <span data-ttu-id="ebd4e-168">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="ebd4e-169">Skriv 'Desc' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="ebd4e-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-170">Click OK.</span></span>
<span data-ttu-id="ebd4e-171">![Side med ER-operationsdesigner](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="ebd4e-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="ebd4e-172">Knyt rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="ebd4e-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="ebd4e-173">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ebd4e-174">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ebd4e-175">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="ebd4e-176">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="ebd4e-177">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="ebd4e-178">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Desc: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="ebd4e-179">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Beskrivelse: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="ebd4e-180">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-180">Click Bind.</span></span>
9. <span data-ttu-id="ebd4e-181">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Værdi: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="ebd4e-182">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="ebd4e-183">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-183">Click Bind.</span></span>
12. <span data-ttu-id="ebd4e-184">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Kode: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="ebd4e-185">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Navn: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="ebd4e-186">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-186">Click Bind.</span></span>
15. <span data-ttu-id="ebd4e-187">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="ebd4e-188">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="ebd4e-189">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-189">Click Bind.</span></span>
18. <span data-ttu-id="ebd4e-190">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Ct: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="ebd4e-191">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="ebd4e-192">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-192">Click Bind.</span></span>
21. <span data-ttu-id="ebd4e-193">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dt: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="ebd4e-194">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="ebd4e-195">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-195">Click Bind.</span></span>
24. <span data-ttu-id="ebd4e-196">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Valuta: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="ebd4e-197">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="ebd4e-198">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-198">Click Bind.</span></span>
27. <span data-ttu-id="ebd4e-199">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Data: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="ebd4e-200">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="ebd4e-201">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-201">Click Bind.</span></span>
30. <span data-ttu-id="ebd4e-202">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Bilag: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="ebd4e-203">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="ebd4e-204">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-204">Click Bind.</span></span>
33. <span data-ttu-id="ebd4e-205">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="ebd4e-206">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="ebd4e-207">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-207">Click Bind.</span></span>
36. <span data-ttu-id="ebd4e-208">Vælg 'Root: XML-element\Journal: XML-element\Batch: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="ebd4e-209">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="ebd4e-210">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-210">Click Bind.</span></span>
39. <span data-ttu-id="ebd4e-211">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="ebd4e-212">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="ebd4e-213">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-213">Click Bind.</span></span>
42. <span data-ttu-id="ebd4e-214">Vælg 'Root: XML-element\Firma: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="ebd4e-215">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="ebd4e-216">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-216">Click Bind.</span></span>
45. <span data-ttu-id="ebd4e-217">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-217">Click Save.</span></span>
46. <span data-ttu-id="ebd4e-218">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ebd4e-218">Close the page.</span></span>
<span data-ttu-id="ebd4e-219">![Side med ER-operationsdesigner](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="ebd4e-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]