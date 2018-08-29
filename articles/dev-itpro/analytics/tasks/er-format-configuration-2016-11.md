--- 
title: Oprette formatkonfigurationer til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="0e561-103">Oprette formatkonfigurationer til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="0e561-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e561-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="0e561-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="0e561-105">Denne formatkonfiguration definerer formatet af elektroniske dokumenter, der bruges til behandling af betalinger.</span><span class="sxs-lookup"><span data-stu-id="0e561-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="0e561-106">I dette eksempel skal du oprette en formatkonfiguration for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Tilknyt model til markerede datakilder".</span><span class="sxs-lookup"><span data-stu-id="0e561-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="0e561-107">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0e561-107">Create a new format configuration</span></span>
1. <span data-ttu-id="0e561-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0e561-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0e561-109">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0e561-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0e561-110">Vælg "Betalinger (forenklet mode)" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="0e561-111">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="0e561-112">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="0e561-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="0e561-113">Skriv "BACS (UK-fiktiv) i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="0e561-114">BACS (UK-fiktiv)</span><span class="sxs-lookup"><span data-stu-id="0e561-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="0e561-115">Skriv "'BACS kreditorbetalingsformat (UK-fiktiv)" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0e561-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="0e561-116">BACS kreditorbetalingsformat (UK-fiktiv)</span><span class="sxs-lookup"><span data-stu-id="0e561-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="0e561-117">Den aktive konfigurationsudbyder indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="0e561-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="0e561-118">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e561-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="0e561-119">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="0e561-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="0e561-120">Du kan definere et bestemt format for det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="0e561-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="0e561-121">Lad feltet være tomt, hvis du vil vælge et format på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="0e561-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="0e561-122">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="0e561-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="0e561-123">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e561-123">Click Create configuration.</span></span>
    * <span data-ttu-id="0e561-124">En ny konfiguration er oprettet.</span><span class="sxs-lookup"><span data-stu-id="0e561-124">A new configuration has been created.</span></span> <span data-ttu-id="0e561-125">Kladdeversionen kan bruges til at gemme designformatet til håndtering af elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="0e561-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="0e561-126">Designformat for elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="0e561-126">Design format of electronic document</span></span>
1. <span data-ttu-id="0e561-127">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0e561-127">Click Designer.</span></span>
2. <span data-ttu-id="0e561-128">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="0e561-129">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="0e561-130">Skriv "Xml" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="0e561-131">Xml</span><span class="sxs-lookup"><span data-stu-id="0e561-131">Xml</span></span>  
5. <span data-ttu-id="0e561-132">Skriv "UTF-8" i feltet Kodning.</span><span class="sxs-lookup"><span data-stu-id="0e561-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0e561-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0e561-133">UTF-8</span></span>  
6. <span data-ttu-id="0e561-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-134">Click OK.</span></span>
7. <span data-ttu-id="0e561-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="0e561-136">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="0e561-137">Skriv "Meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="0e561-138">Melding</span><span class="sxs-lookup"><span data-stu-id="0e561-138">Message</span></span>  
10. <span data-ttu-id="0e561-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-139">Click OK.</span></span>
11. <span data-ttu-id="0e561-140">Vælg "Xml\Meddelelse" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="0e561-141">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-141">Click Add Element.</span></span>
13. <span data-ttu-id="0e561-142">Skriv "ProcessingDate" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="0e561-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="0e561-143">ProcessingDate</span></span>  
14. <span data-ttu-id="0e561-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-144">Click OK.</span></span>
15. <span data-ttu-id="0e561-145">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-145">Click Add Element.</span></span>
16. <span data-ttu-id="0e561-146">Skriv "MessageId" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="0e561-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="0e561-147">MessageId</span></span>  
17. <span data-ttu-id="0e561-148">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-148">Click OK.</span></span>
18. <span data-ttu-id="0e561-149">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-149">Click Add Element.</span></span>
19. <span data-ttu-id="0e561-150">Skriv "Betalinger" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0e561-151">Betalinger</span><span class="sxs-lookup"><span data-stu-id="0e561-151">Payments</span></span>  
20. <span data-ttu-id="0e561-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-152">Click OK.</span></span>
21. <span data-ttu-id="0e561-153">Vælg "Xml\Meddelelse\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="0e561-154">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-154">Click Add Element.</span></span>
23. <span data-ttu-id="0e561-155">Skriv "Vare" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="0e561-156">Post</span><span class="sxs-lookup"><span data-stu-id="0e561-156">Item</span></span>  
24. <span data-ttu-id="0e561-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-157">Click OK.</span></span>
25. <span data-ttu-id="0e561-158">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="0e561-159">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="0e561-160">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="0e561-161">Skriv "Id" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="0e561-162">Id</span><span class="sxs-lookup"><span data-stu-id="0e561-162">Id</span></span>  
29. <span data-ttu-id="0e561-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-163">Click OK.</span></span>
30. <span data-ttu-id="0e561-164">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="0e561-165">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="0e561-166">Skriv "Kreditor" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="0e561-167">Leverandør</span><span class="sxs-lookup"><span data-stu-id="0e561-167">Vendor</span></span>  
33. <span data-ttu-id="0e561-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-168">Click OK.</span></span>
34. <span data-ttu-id="0e561-169">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="0e561-170">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-170">Click Add Element.</span></span>
36. <span data-ttu-id="0e561-171">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0e561-172">Navn</span><span class="sxs-lookup"><span data-stu-id="0e561-172">Name</span></span>  
37. <span data-ttu-id="0e561-173">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-173">Click OK.</span></span>
38. <span data-ttu-id="0e561-174">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-174">Click Add Element.</span></span>
39. <span data-ttu-id="0e561-175">Skriv "Bank" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="0e561-176">Pengeinstitut</span><span class="sxs-lookup"><span data-stu-id="0e561-176">Bank</span></span>  
40. <span data-ttu-id="0e561-177">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-177">Click OK.</span></span>
41. <span data-ttu-id="0e561-178">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="0e561-179">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-179">Click Add Element.</span></span>
43. <span data-ttu-id="0e561-180">Skriv "RoutingNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="0e561-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="0e561-181">RoutingNumber</span></span>  
44. <span data-ttu-id="0e561-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-182">Click OK.</span></span>
45. <span data-ttu-id="0e561-183">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-183">Click Add Element.</span></span>
46. <span data-ttu-id="0e561-184">Skriv "AccountNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="0e561-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="0e561-185">AccountNumber</span></span>  
47. <span data-ttu-id="0e561-186">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-186">Click OK.</span></span>
48. <span data-ttu-id="0e561-187">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="0e561-188">Klik på Kopiér.</span><span class="sxs-lookup"><span data-stu-id="0e561-188">Click Copy.</span></span>
50. <span data-ttu-id="0e561-189">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="0e561-190">Klik på Sæt ind.</span><span class="sxs-lookup"><span data-stu-id="0e561-190">Click Paste.</span></span>
52. <span data-ttu-id="0e561-191">Skriv "Betaler" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="0e561-192">Betaler</span><span class="sxs-lookup"><span data-stu-id="0e561-192">Payer</span></span>  
53. <span data-ttu-id="0e561-193">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="0e561-194">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-194">Click Add Element.</span></span>
55. <span data-ttu-id="0e561-195">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0e561-196">Valuta</span><span class="sxs-lookup"><span data-stu-id="0e561-196">Currency</span></span>  
56. <span data-ttu-id="0e561-197">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-197">Click OK.</span></span>
57. <span data-ttu-id="0e561-198">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-198">Click Add Element.</span></span>
58. <span data-ttu-id="0e561-199">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="0e561-200">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="0e561-200">Description</span></span>  
59. <span data-ttu-id="0e561-201">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-201">Click OK.</span></span>
60. <span data-ttu-id="0e561-202">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-202">Click Add Element.</span></span>
61. <span data-ttu-id="0e561-203">Skriv "TransDate" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="0e561-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="0e561-204">TransDate</span></span>  
62. <span data-ttu-id="0e561-205">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-205">Click OK.</span></span>
63. <span data-ttu-id="0e561-206">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="0e561-206">Click Add Element.</span></span>
64. <span data-ttu-id="0e561-207">Skriv "Beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0e561-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="0e561-208">Beløb</span><span class="sxs-lookup"><span data-stu-id="0e561-208">Amount</span></span>  
65. <span data-ttu-id="0e561-209">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="0e561-210">Klargør formatkomponenter til tilknytning til datamodelelementer</span><span class="sxs-lookup"><span data-stu-id="0e561-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="0e561-211">Vælg "Xml\Meddelelse\ProcessingDate" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="0e561-212">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="0e561-213">Vælg "Tekst\DateTime" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="0e561-214">Skriv 'åååå-MM-dd' i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="0e561-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="0e561-215">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="0e561-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="0e561-216">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-216">Click OK.</span></span>
6. <span data-ttu-id="0e561-217">Vælg "Xml\Meddelelse\Betalinger\TransDate" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="0e561-218">Klik på Tilføj DateTime.</span><span class="sxs-lookup"><span data-stu-id="0e561-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="0e561-219">Skriv 'åååå-MM-dd' i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="0e561-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="0e561-220">åååå-MM-dd</span><span class="sxs-lookup"><span data-stu-id="0e561-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="0e561-221">Vælg "Date" i feltet DateTime-type.</span><span class="sxs-lookup"><span data-stu-id="0e561-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="0e561-222">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-222">Click OK.</span></span>
11. <span data-ttu-id="0e561-223">Vælg "Xml\Meddelelse\MessageId" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="0e561-224">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0e561-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="0e561-225">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="0e561-226">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-226">Click OK.</span></span>
15. <span data-ttu-id="0e561-227">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="0e561-228">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-228">Click Add String.</span></span>
17. <span data-ttu-id="0e561-229">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-229">Click OK.</span></span>
18. <span data-ttu-id="0e561-230">Vælg "Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="0e561-231">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-231">Click Add String.</span></span>
20. <span data-ttu-id="0e561-232">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-232">Click OK.</span></span>
21. <span data-ttu-id="0e561-233">Vælg "Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="0e561-234">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-234">Click Add String.</span></span>
23. <span data-ttu-id="0e561-235">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-235">Click OK.</span></span>
24. <span data-ttu-id="0e561-236">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="0e561-237">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-237">Click Add String.</span></span>
26. <span data-ttu-id="0e561-238">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-238">Click OK.</span></span>
27. <span data-ttu-id="0e561-239">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="0e561-240">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-240">Click Add String.</span></span>
29. <span data-ttu-id="0e561-241">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-241">Click OK.</span></span>
30. <span data-ttu-id="0e561-242">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="0e561-243">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-243">Click Add String.</span></span>
32. <span data-ttu-id="0e561-244">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-244">Click OK.</span></span>
33. <span data-ttu-id="0e561-245">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\Valuta" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="0e561-246">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-246">Click Add String.</span></span>
35. <span data-ttu-id="0e561-247">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-247">Click OK.</span></span>
36. <span data-ttu-id="0e561-248">Vælg "Xml\Meddelelse\Betalinger\Vare\Beskrivelse" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="0e561-249">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-249">Click Add String.</span></span>
38. <span data-ttu-id="0e561-250">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-250">Click OK.</span></span>
39. <span data-ttu-id="0e561-251">Vælg "Xml\Meddelelse\Betalinger\Vare\Beløb" i træet.</span><span class="sxs-lookup"><span data-stu-id="0e561-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="0e561-252">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="0e561-252">Click Add String.</span></span>
41. <span data-ttu-id="0e561-253">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e561-253">Click OK.</span></span>
42. <span data-ttu-id="0e561-254">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0e561-254">Click Save.</span></span>
43. <span data-ttu-id="0e561-255">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e561-255">Close the page.</span></span>


