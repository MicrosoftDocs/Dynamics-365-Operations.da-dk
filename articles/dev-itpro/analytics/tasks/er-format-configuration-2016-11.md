--- 
title: Oprette en ER-formatkonfiguration (november 2016)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="c5398-103">Oprette en ER-formatkonfiguration (november 2016)</span><span class="sxs-lookup"><span data-stu-id="c5398-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5398-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="c5398-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="c5398-105">Denne formatkonfiguration definerer formatet af elektroniske dokumenter, der bruges til behandling af betalinger.</span><span class="sxs-lookup"><span data-stu-id="c5398-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="c5398-106">I dette eksempel skal du oprette en formatkonfiguration for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Tilknyt model til markerede datakilder".</span><span class="sxs-lookup"><span data-stu-id="c5398-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="c5398-107">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c5398-107">Create a new format configuration</span></span>
1. <span data-ttu-id="c5398-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="c5398-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c5398-109">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="c5398-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c5398-110">Vælg "Betalinger (forenklet mode)" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="c5398-111">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="c5398-112">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="c5398-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="c5398-113">Skriv "BACS (UK-fiktiv) i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="c5398-114">BACS (UK-fiktiv)</span><span class="sxs-lookup"><span data-stu-id="c5398-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="c5398-115">Skriv "'BACS kreditorbetalingsformat (UK-fiktiv)" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c5398-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="c5398-116">BACS kreditorbetalingsformat (UK-fiktiv)</span><span class="sxs-lookup"><span data-stu-id="c5398-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="c5398-117">Den aktive konfigurationsudbyder indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="c5398-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c5398-118">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5398-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c5398-119">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="c5398-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="c5398-120">Du kan definere et bestemt format for det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="c5398-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="c5398-121">Lad feltet være tomt, hvis du vil vælge et format på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="c5398-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="c5398-122">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="c5398-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="c5398-123">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5398-123">Click Create configuration.</span></span>
    * <span data-ttu-id="c5398-124">En ny konfiguration er oprettet.</span><span class="sxs-lookup"><span data-stu-id="c5398-124">A new configuration has been created.</span></span> <span data-ttu-id="c5398-125">Kladdeversionen kan bruges til at gemme designformatet til håndtering af elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="c5398-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="c5398-126">Designformat for elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="c5398-126">Design format of electronic document</span></span>
1. <span data-ttu-id="c5398-127">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="c5398-127">Click Designer.</span></span>
2. <span data-ttu-id="c5398-128">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c5398-129">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="c5398-130">Skriv "Xml" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="c5398-131">Xml</span><span class="sxs-lookup"><span data-stu-id="c5398-131">Xml</span></span>  
5. <span data-ttu-id="c5398-132">Skriv "UTF-8" i feltet Kodning.</span><span class="sxs-lookup"><span data-stu-id="c5398-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c5398-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c5398-133">UTF-8</span></span>  
6. <span data-ttu-id="c5398-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-134">Click OK.</span></span>
7. <span data-ttu-id="c5398-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="c5398-136">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="c5398-137">Skriv "Meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="c5398-138">Melding</span><span class="sxs-lookup"><span data-stu-id="c5398-138">Message</span></span>  
10. <span data-ttu-id="c5398-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-139">Click OK.</span></span>
11. <span data-ttu-id="c5398-140">Vælg "Xml\Meddelelse" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="c5398-141">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-141">Click Add Element.</span></span>
13. <span data-ttu-id="c5398-142">Skriv "ProcessingDate" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="c5398-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="c5398-143">ProcessingDate</span></span>  
14. <span data-ttu-id="c5398-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-144">Click OK.</span></span>
15. <span data-ttu-id="c5398-145">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-145">Click Add Element.</span></span>
16. <span data-ttu-id="c5398-146">Skriv "MessageId" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="c5398-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="c5398-147">MessageId</span></span>  
17. <span data-ttu-id="c5398-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-148">Click OK.</span></span>
18. <span data-ttu-id="c5398-149">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-149">Click Add Element.</span></span>
19. <span data-ttu-id="c5398-150">Skriv "Betalinger" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="c5398-151">Betalinger</span><span class="sxs-lookup"><span data-stu-id="c5398-151">Payments</span></span>  
20. <span data-ttu-id="c5398-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-152">Click OK.</span></span>
21. <span data-ttu-id="c5398-153">Vælg "Xml\Meddelelse\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="c5398-154">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-154">Click Add Element.</span></span>
23. <span data-ttu-id="c5398-155">Skriv "Vare" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="c5398-156">Post</span><span class="sxs-lookup"><span data-stu-id="c5398-156">Item</span></span>  
24. <span data-ttu-id="c5398-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-157">Click OK.</span></span>
25. <span data-ttu-id="c5398-158">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="c5398-159">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="c5398-160">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="c5398-161">Skriv "Id" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="c5398-162">Id</span><span class="sxs-lookup"><span data-stu-id="c5398-162">Id</span></span>  
29. <span data-ttu-id="c5398-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-163">Click OK.</span></span>
30. <span data-ttu-id="c5398-164">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="c5398-165">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="c5398-166">Skriv "Kreditor" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="c5398-167">Leverandør</span><span class="sxs-lookup"><span data-stu-id="c5398-167">Vendor</span></span>  
33. <span data-ttu-id="c5398-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-168">Click OK.</span></span>
34. <span data-ttu-id="c5398-169">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="c5398-170">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-170">Click Add Element.</span></span>
36. <span data-ttu-id="c5398-171">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="c5398-172">Navn</span><span class="sxs-lookup"><span data-stu-id="c5398-172">Name</span></span>  
37. <span data-ttu-id="c5398-173">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-173">Click OK.</span></span>
38. <span data-ttu-id="c5398-174">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-174">Click Add Element.</span></span>
39. <span data-ttu-id="c5398-175">Skriv "Bank" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="c5398-176">Pengeinstitut</span><span class="sxs-lookup"><span data-stu-id="c5398-176">Bank</span></span>  
40. <span data-ttu-id="c5398-177">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-177">Click OK.</span></span>
41. <span data-ttu-id="c5398-178">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="c5398-179">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-179">Click Add Element.</span></span>
43. <span data-ttu-id="c5398-180">Skriv "RoutingNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="c5398-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="c5398-181">RoutingNumber</span></span>  
44. <span data-ttu-id="c5398-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-182">Click OK.</span></span>
45. <span data-ttu-id="c5398-183">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-183">Click Add Element.</span></span>
46. <span data-ttu-id="c5398-184">Skriv "AccountNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="c5398-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="c5398-185">AccountNumber</span></span>  
47. <span data-ttu-id="c5398-186">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-186">Click OK.</span></span>
48. <span data-ttu-id="c5398-187">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="c5398-188">Klik på Kopiér.</span><span class="sxs-lookup"><span data-stu-id="c5398-188">Click Copy.</span></span>
50. <span data-ttu-id="c5398-189">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="c5398-190">Klik på Sæt ind.</span><span class="sxs-lookup"><span data-stu-id="c5398-190">Click Paste.</span></span>
52. <span data-ttu-id="c5398-191">Skriv "Betaler" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="c5398-192">Betaler</span><span class="sxs-lookup"><span data-stu-id="c5398-192">Payer</span></span>  
53. <span data-ttu-id="c5398-193">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="c5398-194">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-194">Click Add Element.</span></span>
55. <span data-ttu-id="c5398-195">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="c5398-196">Valuta</span><span class="sxs-lookup"><span data-stu-id="c5398-196">Currency</span></span>  
56. <span data-ttu-id="c5398-197">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-197">Click OK.</span></span>
57. <span data-ttu-id="c5398-198">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-198">Click Add Element.</span></span>
58. <span data-ttu-id="c5398-199">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="c5398-200">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="c5398-200">Description</span></span>  
59. <span data-ttu-id="c5398-201">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-201">Click OK.</span></span>
60. <span data-ttu-id="c5398-202">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-202">Click Add Element.</span></span>
61. <span data-ttu-id="c5398-203">Skriv "TransDate" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="c5398-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="c5398-204">TransDate</span></span>  
62. <span data-ttu-id="c5398-205">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-205">Click OK.</span></span>
63. <span data-ttu-id="c5398-206">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="c5398-206">Click Add Element.</span></span>
64. <span data-ttu-id="c5398-207">Skriv "Beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5398-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="c5398-208">Beløb</span><span class="sxs-lookup"><span data-stu-id="c5398-208">Amount</span></span>  
65. <span data-ttu-id="c5398-209">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="c5398-210">Klargør formatkomponenter til tilknytning til datamodelelementer</span><span class="sxs-lookup"><span data-stu-id="c5398-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="c5398-211">Vælg "Xml\Meddelelse\ProcessingDate" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="c5398-212">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="c5398-213">Vælg "Tekst\DateTime" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="c5398-214">Skriv 'åååå-MM-dd' i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="c5398-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c5398-215">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c5398-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="c5398-216">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-216">Click OK.</span></span>
6. <span data-ttu-id="c5398-217">Vælg "Xml\Meddelelse\Betalinger\TransDate" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="c5398-218">Klik på Tilføj DateTime.</span><span class="sxs-lookup"><span data-stu-id="c5398-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="c5398-219">Skriv 'åååå-MM-dd' i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="c5398-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c5398-220">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c5398-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="c5398-221">Vælg "Date" i feltet DateTime-type.</span><span class="sxs-lookup"><span data-stu-id="c5398-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="c5398-222">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-222">Click OK.</span></span>
11. <span data-ttu-id="c5398-223">Vælg "Xml\Meddelelse\MessageId" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="c5398-224">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5398-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="c5398-225">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="c5398-226">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-226">Click OK.</span></span>
15. <span data-ttu-id="c5398-227">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="c5398-228">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-228">Click Add String.</span></span>
17. <span data-ttu-id="c5398-229">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-229">Click OK.</span></span>
18. <span data-ttu-id="c5398-230">Vælg "Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="c5398-231">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-231">Click Add String.</span></span>
20. <span data-ttu-id="c5398-232">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-232">Click OK.</span></span>
21. <span data-ttu-id="c5398-233">Vælg "Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="c5398-234">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-234">Click Add String.</span></span>
23. <span data-ttu-id="c5398-235">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-235">Click OK.</span></span>
24. <span data-ttu-id="c5398-236">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="c5398-237">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-237">Click Add String.</span></span>
26. <span data-ttu-id="c5398-238">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-238">Click OK.</span></span>
27. <span data-ttu-id="c5398-239">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="c5398-240">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-240">Click Add String.</span></span>
29. <span data-ttu-id="c5398-241">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-241">Click OK.</span></span>
30. <span data-ttu-id="c5398-242">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="c5398-243">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-243">Click Add String.</span></span>
32. <span data-ttu-id="c5398-244">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-244">Click OK.</span></span>
33. <span data-ttu-id="c5398-245">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\Valuta" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="c5398-246">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-246">Click Add String.</span></span>
35. <span data-ttu-id="c5398-247">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-247">Click OK.</span></span>
36. <span data-ttu-id="c5398-248">Vælg "Xml\Meddelelse\Betalinger\Vare\Beskrivelse" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="c5398-249">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-249">Click Add String.</span></span>
38. <span data-ttu-id="c5398-250">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-250">Click OK.</span></span>
39. <span data-ttu-id="c5398-251">Vælg "Xml\Meddelelse\Betalinger\Vare\Beløb" i træet.</span><span class="sxs-lookup"><span data-stu-id="c5398-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="c5398-252">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="c5398-252">Click Add String.</span></span>
41. <span data-ttu-id="c5398-253">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5398-253">Click OK.</span></span>
42. <span data-ttu-id="c5398-254">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c5398-254">Click Save.</span></span>
43. <span data-ttu-id="c5398-255">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5398-255">Close the page.</span></span>


