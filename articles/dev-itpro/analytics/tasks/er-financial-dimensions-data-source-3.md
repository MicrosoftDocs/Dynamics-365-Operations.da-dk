---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45096a728ad6f9e331b53b4e12ca0ff9317a3939
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "362987"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="33b07-103">ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)</span><span class="sxs-lookup"><span data-stu-id="33b07-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33b07-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="33b07-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="33b07-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="33b07-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="33b07-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 2: Modeltilknytning)".</span><span class="sxs-lookup"><span data-stu-id="33b07-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="33b07-107">Opret en rapport til visning af økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="33b07-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="33b07-108">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="33b07-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="33b07-109">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="33b07-110">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="33b07-111">Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="33b07-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="33b07-112">Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.</span><span class="sxs-lookup"><span data-stu-id="33b07-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="33b07-113">Skriv "Finanskladderapport" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="33b07-114">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="33b07-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="33b07-115">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="33b07-115">Click Create configuration.</span></span>
8. <span data-ttu-id="33b07-116">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="33b07-116">Click Designer.</span></span>
9. <span data-ttu-id="33b07-117">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="33b07-118">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="33b07-119">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="33b07-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-120">Click OK.</span></span>
13. <span data-ttu-id="33b07-121">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="33b07-122">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="33b07-123">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="33b07-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-124">Click OK.</span></span>
17. <span data-ttu-id="33b07-125">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="33b07-126">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="33b07-127">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="33b07-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-128">Click OK.</span></span>
21. <span data-ttu-id="33b07-129">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="33b07-130">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="33b07-131">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="33b07-132">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="33b07-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-133">Click OK.</span></span>
26. <span data-ttu-id="33b07-134">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="33b07-135">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="33b07-136">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="33b07-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-137">Click OK.</span></span>
30. <span data-ttu-id="33b07-138">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="33b07-139">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="33b07-140">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="33b07-141">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="33b07-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-142">Click OK.</span></span>
35. <span data-ttu-id="33b07-143">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="33b07-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="33b07-144">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="33b07-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-145">Click OK.</span></span>
38. <span data-ttu-id="33b07-146">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="33b07-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="33b07-147">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="33b07-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-148">Click OK.</span></span>
41. <span data-ttu-id="33b07-149">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="33b07-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="33b07-150">Skriv 'Dt' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="33b07-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-151">Click OK.</span></span>
44. <span data-ttu-id="33b07-152">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="33b07-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="33b07-153">Skriv 'Ct' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="33b07-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-154">Click OK.</span></span>
47. <span data-ttu-id="33b07-155">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="33b07-156">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="33b07-157">Skriv 'Dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="33b07-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-158">Click OK.</span></span>
51. <span data-ttu-id="33b07-159">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="33b07-160">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="33b07-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="33b07-161">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="33b07-162">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="33b07-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-163">Click OK.</span></span>
56. <span data-ttu-id="33b07-164">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="33b07-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="33b07-165">Skriv 'Værdi' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="33b07-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-166">Click OK.</span></span>
59. <span data-ttu-id="33b07-167">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="33b07-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="33b07-168">Skriv 'Desc' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33b07-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="33b07-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33b07-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="33b07-170">Knyt rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="33b07-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="33b07-171">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="33b07-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="33b07-172">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="33b07-173">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="33b07-174">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="33b07-175">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="33b07-176">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Desc: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="33b07-177">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Beskrivelse: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="33b07-178">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-178">Click Bind.</span></span>
9. <span data-ttu-id="33b07-179">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Værdi: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="33b07-180">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="33b07-181">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-181">Click Bind.</span></span>
12. <span data-ttu-id="33b07-182">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Kode: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="33b07-183">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Navn: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="33b07-184">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-184">Click Bind.</span></span>
15. <span data-ttu-id="33b07-185">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="33b07-186">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="33b07-187">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-187">Click Bind.</span></span>
18. <span data-ttu-id="33b07-188">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Ct: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="33b07-189">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="33b07-190">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-190">Click Bind.</span></span>
21. <span data-ttu-id="33b07-191">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dt: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="33b07-192">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="33b07-193">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-193">Click Bind.</span></span>
24. <span data-ttu-id="33b07-194">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Valuta: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="33b07-195">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="33b07-196">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-196">Click Bind.</span></span>
27. <span data-ttu-id="33b07-197">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Data: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="33b07-198">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="33b07-199">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-199">Click Bind.</span></span>
30. <span data-ttu-id="33b07-200">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Bilag: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="33b07-201">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="33b07-202">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-202">Click Bind.</span></span>
33. <span data-ttu-id="33b07-203">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="33b07-204">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="33b07-205">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-205">Click Bind.</span></span>
36. <span data-ttu-id="33b07-206">Vælg 'Root: XML-element\Journal: XML-element\Batch: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="33b07-207">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="33b07-208">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-208">Click Bind.</span></span>
39. <span data-ttu-id="33b07-209">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="33b07-210">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="33b07-211">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-211">Click Bind.</span></span>
42. <span data-ttu-id="33b07-212">Vælg 'Root: XML-element\Firma: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="33b07-213">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="33b07-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="33b07-214">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="33b07-214">Click Bind.</span></span>
45. <span data-ttu-id="33b07-215">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="33b07-215">Click Save.</span></span>
46. <span data-ttu-id="33b07-216">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33b07-216">Close the page.</span></span>

