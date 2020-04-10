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
ms.openlocfilehash: 7bbbc81eaf8c13e8d13e30a0276e38453e07ead9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142518"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="0b7a8-103">ER Bruge økonomiske dimensioner som en datakilde (del 3: Design rapporten)</span><span class="sxs-lookup"><span data-stu-id="0b7a8-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b7a8-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="0b7a8-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0b7a8-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren den "ER-brug af økonomiske dimensioner som datakilde (del 2: Modeltilknytning)".</span><span class="sxs-lookup"><span data-stu-id="0b7a8-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="0b7a8-107">Opret en rapport til visning af økonomiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="0b7a8-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="0b7a8-108">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0b7a8-109">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0b7a8-110">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="0b7a8-111">Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="0b7a8-112">Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="0b7a8-113">Skriv "Finanskladderapport" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="0b7a8-114">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="0b7a8-115">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-115">Click Create configuration.</span></span>
8. <span data-ttu-id="0b7a8-116">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-116">Click Designer.</span></span>
9. <span data-ttu-id="0b7a8-117">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="0b7a8-118">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="0b7a8-119">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="0b7a8-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-120">Click OK.</span></span>
13. <span data-ttu-id="0b7a8-121">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="0b7a8-122">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="0b7a8-123">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="0b7a8-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-124">Click OK.</span></span>
17. <span data-ttu-id="0b7a8-125">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="0b7a8-126">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="0b7a8-127">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="0b7a8-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-128">Click OK.</span></span>
21. <span data-ttu-id="0b7a8-129">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="0b7a8-130">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="0b7a8-131">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="0b7a8-132">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="0b7a8-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-133">Click OK.</span></span>
26. <span data-ttu-id="0b7a8-134">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="0b7a8-135">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="0b7a8-136">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="0b7a8-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-137">Click OK.</span></span>
30. <span data-ttu-id="0b7a8-138">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="0b7a8-139">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="0b7a8-140">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="0b7a8-141">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="0b7a8-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-142">Click OK.</span></span>
35. <span data-ttu-id="0b7a8-143">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="0b7a8-144">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="0b7a8-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-145">Click OK.</span></span>
38. <span data-ttu-id="0b7a8-146">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="0b7a8-147">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="0b7a8-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-148">Click OK.</span></span>
41. <span data-ttu-id="0b7a8-149">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="0b7a8-150">Skriv 'Dt' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="0b7a8-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-151">Click OK.</span></span>
44. <span data-ttu-id="0b7a8-152">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="0b7a8-153">Skriv 'Ct' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="0b7a8-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-154">Click OK.</span></span>
47. <span data-ttu-id="0b7a8-155">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="0b7a8-156">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="0b7a8-157">Skriv 'Dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="0b7a8-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-158">Click OK.</span></span>
51. <span data-ttu-id="0b7a8-159">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="0b7a8-160">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="0b7a8-161">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="0b7a8-162">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="0b7a8-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-163">Click OK.</span></span>
56. <span data-ttu-id="0b7a8-164">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="0b7a8-165">Skriv 'Værdi' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="0b7a8-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-166">Click OK.</span></span>
59. <span data-ttu-id="0b7a8-167">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="0b7a8-168">Skriv 'Desc' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="0b7a8-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="0b7a8-170">Knyt rapportelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="0b7a8-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="0b7a8-171">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0b7a8-172">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0b7a8-173">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="0b7a8-174">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="0b7a8-175">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="0b7a8-176">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Desc: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="0b7a8-177">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Beskrivelse: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="0b7a8-178">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-178">Click Bind.</span></span>
9. <span data-ttu-id="0b7a8-179">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Værdi: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="0b7a8-180">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="0b7a8-181">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-181">Click Bind.</span></span>
12. <span data-ttu-id="0b7a8-182">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element\Kode: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="0b7a8-183">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Navn: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="0b7a8-184">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-184">Click Bind.</span></span>
15. <span data-ttu-id="0b7a8-185">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="0b7a8-186">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dimensions: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="0b7a8-187">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-187">Click Bind.</span></span>
18. <span data-ttu-id="0b7a8-188">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Ct: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="0b7a8-189">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="0b7a8-190">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-190">Click Bind.</span></span>
21. <span data-ttu-id="0b7a8-191">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Dt: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="0b7a8-192">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="0b7a8-193">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-193">Click Bind.</span></span>
24. <span data-ttu-id="0b7a8-194">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Valuta: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="0b7a8-195">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="0b7a8-196">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-196">Click Bind.</span></span>
27. <span data-ttu-id="0b7a8-197">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Data: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="0b7a8-198">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="0b7a8-199">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-199">Click Bind.</span></span>
30. <span data-ttu-id="0b7a8-200">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element\Bilag: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="0b7a8-201">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="0b7a8-202">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-202">Click Bind.</span></span>
33. <span data-ttu-id="0b7a8-203">Vælg 'Root: XML-element\Journal: XML-element\Transaction: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="0b7a8-204">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="0b7a8-205">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-205">Click Bind.</span></span>
36. <span data-ttu-id="0b7a8-206">Vælg 'Root: XML-element\Journal: XML-element\Batch: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="0b7a8-207">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="0b7a8-208">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-208">Click Bind.</span></span>
39. <span data-ttu-id="0b7a8-209">Vælg 'Root: XML Element\Journal: XML-element' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="0b7a8-210">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="0b7a8-211">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-211">Click Bind.</span></span>
42. <span data-ttu-id="0b7a8-212">Vælg 'Root: XML-element\Firma: XML-attribut' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="0b7a8-213">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="0b7a8-214">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-214">Click Bind.</span></span>
45. <span data-ttu-id="0b7a8-215">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-215">Click Save.</span></span>
46. <span data-ttu-id="0b7a8-216">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0b7a8-216">Close the page.</span></span>

