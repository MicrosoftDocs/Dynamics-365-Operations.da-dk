---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684781"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="0e538-103">ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)</span><span class="sxs-lookup"><span data-stu-id="0e538-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e538-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="0e538-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="0e538-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0e538-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0e538-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 2: Modeltilknytning)".</span><span class="sxs-lookup"><span data-stu-id="0e538-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="0e538-107">Opret en rapport til visning af økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="0e538-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="0e538-108">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0e538-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0e538-109">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0e538-110">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="0e538-111">Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="0e538-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="0e538-112">Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.</span><span class="sxs-lookup"><span data-stu-id="0e538-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="0e538-113">Skriv "Finanskladderapport" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="0e538-114">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="0e538-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="0e538-115">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e538-115">Click Create configuration.</span></span>
8. <span data-ttu-id="0e538-116">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0e538-116">Click Designer.</span></span>
9. <span data-ttu-id="0e538-117">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="0e538-118">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="0e538-119">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="0e538-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-120">Click OK.</span></span>
13. <span data-ttu-id="0e538-121">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="0e538-122">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="0e538-123">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="0e538-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-124">Click OK.</span></span>
17. <span data-ttu-id="0e538-125">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="0e538-126">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="0e538-127">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="0e538-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-128">Click OK.</span></span>
21. <span data-ttu-id="0e538-129">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="0e538-130">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="0e538-131">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="0e538-132">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="0e538-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-133">Click OK.</span></span>
26. <span data-ttu-id="0e538-134">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="0e538-135">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="0e538-136">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="0e538-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-137">Click OK.</span></span>
30. <span data-ttu-id="0e538-138">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="0e538-139">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="0e538-140">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="0e538-141">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="0e538-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-142">Click OK.</span></span>
35. <span data-ttu-id="0e538-143">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0e538-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="0e538-144">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="0e538-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-145">Click OK.</span></span>
38. <span data-ttu-id="0e538-146">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0e538-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="0e538-147">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="0e538-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-148">Click OK.</span></span>
41. <span data-ttu-id="0e538-149">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0e538-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="0e538-150">Skriv 'Dt' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="0e538-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-151">Click OK.</span></span>
44. <span data-ttu-id="0e538-152">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0e538-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="0e538-153">Skriv 'Ct' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="0e538-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-154">Click OK.</span></span>
47. <span data-ttu-id="0e538-155">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="0e538-156">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="0e538-157">Skriv 'Dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="0e538-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-158">Click OK.</span></span>
51. <span data-ttu-id="0e538-159">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="0e538-160">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e538-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="0e538-161">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="0e538-162">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="0e538-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-163">Click OK.</span></span>
56. <span data-ttu-id="0e538-164">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0e538-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="0e538-165">Skriv 'Værdi' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="0e538-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-166">Click OK.</span></span>
59. <span data-ttu-id="0e538-167">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0e538-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="0e538-168">Skriv 'Desc' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e538-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="0e538-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e538-169">Click OK.</span></span>
<span data-ttu-id="0e538-170">![Side med ER-operationsdesigner](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="0e538-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="0e538-171">Knyt rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="0e538-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="0e538-172">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="0e538-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0e538-173">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0e538-174">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="0e538-175">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="0e538-176">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="0e538-177">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Desc: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="0e538-178">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Beskrivelse: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="0e538-179">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-179">Click Bind.</span></span>
9. <span data-ttu-id="0e538-180">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Værdi: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="0e538-181">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="0e538-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-182">Click Bind.</span></span>
12. <span data-ttu-id="0e538-183">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Kode: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="0e538-184">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Navn: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="0e538-185">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-185">Click Bind.</span></span>
15. <span data-ttu-id="0e538-186">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="0e538-187">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="0e538-188">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-188">Click Bind.</span></span>
18. <span data-ttu-id="0e538-189">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Ct: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="0e538-190">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="0e538-191">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-191">Click Bind.</span></span>
21. <span data-ttu-id="0e538-192">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dt: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="0e538-193">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="0e538-194">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-194">Click Bind.</span></span>
24. <span data-ttu-id="0e538-195">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Valuta: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="0e538-196">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="0e538-197">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-197">Click Bind.</span></span>
27. <span data-ttu-id="0e538-198">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Data: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="0e538-199">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="0e538-200">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-200">Click Bind.</span></span>
30. <span data-ttu-id="0e538-201">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Bilag: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="0e538-202">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="0e538-203">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-203">Click Bind.</span></span>
33. <span data-ttu-id="0e538-204">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="0e538-205">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="0e538-206">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-206">Click Bind.</span></span>
36. <span data-ttu-id="0e538-207">Vælg 'Root: XML-element\Journal: XML-element\Batch: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="0e538-208">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="0e538-209">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-209">Click Bind.</span></span>
39. <span data-ttu-id="0e538-210">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="0e538-211">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="0e538-212">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-212">Click Bind.</span></span>
42. <span data-ttu-id="0e538-213">Vælg 'Root: XML-element\Firma: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="0e538-214">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e538-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="0e538-215">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0e538-215">Click Bind.</span></span>
45. <span data-ttu-id="0e538-216">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0e538-216">Click Save.</span></span>
46. <span data-ttu-id="0e538-217">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e538-217">Close the page.</span></span>
<span data-ttu-id="0e538-218">![Side med ER-operationsdesigner](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="0e538-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

