---
title: ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til at bruge dokumentstyringsfiler i ER-output. (Del 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755004"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="bfb69-104">ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)</span><span class="sxs-lookup"><span data-stu-id="bfb69-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bfb69-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="bfb69-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="bfb69-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="bfb69-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="bfb69-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 2: Udvid datamodel)".</span><span class="sxs-lookup"><span data-stu-id="bfb69-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="bfb69-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="bfb69-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="bfb69-109">Opret et format til behandling af fakturaer</span><span class="sxs-lookup"><span data-stu-id="bfb69-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="bfb69-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="bfb69-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="bfb69-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bfb69-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="bfb69-112">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="bfb69-113">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="bfb69-114">Du skal oprette et format for at generere elektroniske meddelelser med oplysninger om de filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="bfb69-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="bfb69-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="bfb69-116">Skriv "Format baseret på datamodel\Debitorfakturamodel (brugerdefineret)" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="bfb69-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="bfb69-117">Skriv 'Eksempelmeddelelse i elektronisk faktura' i feltet navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="bfb69-118">Eksempelmeddelelse i elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="bfb69-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="bfb69-119">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="bfb69-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="bfb69-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="bfb69-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="bfb69-121">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bfb69-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="bfb69-122">Design et format til udfyldning af vedhæftede filer til generering af en meddelelse i MIME-format</span><span class="sxs-lookup"><span data-stu-id="bfb69-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="bfb69-123">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="bfb69-123">Click Designer.</span></span>
2. <span data-ttu-id="bfb69-124">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="bfb69-125">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="bfb69-126">Skriv 'Faktura' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="bfb69-127">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="bfb69-127">Invoice</span></span>  
5. <span data-ttu-id="bfb69-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-128">Click OK.</span></span>
6. <span data-ttu-id="bfb69-129">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="bfb69-130">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="bfb69-131">Skriv 'SalesOrder' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="bfb69-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="bfb69-132">SalesOrder</span></span>  
9. <span data-ttu-id="bfb69-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-133">Click OK.</span></span>
10. <span data-ttu-id="bfb69-134">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="bfb69-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="bfb69-135">Skriv "InvoiceNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="bfb69-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="bfb69-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="bfb69-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-137">Click OK.</span></span>
13. <span data-ttu-id="bfb69-138">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="bfb69-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="bfb69-139">Skriv 'InvoiceAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="bfb69-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="bfb69-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="bfb69-141">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-141">Click OK.</span></span>
16. <span data-ttu-id="bfb69-142">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="bfb69-143">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="bfb69-144">Skriv "EnclosedDocs" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="bfb69-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="bfb69-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="bfb69-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-146">Click OK.</span></span>
20. <span data-ttu-id="bfb69-147">Vælg 'Faktura\EnclosedDocs' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="bfb69-148">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="bfb69-148">Click Add Element.</span></span>
22. <span data-ttu-id="bfb69-149">Skriv 'Dokument' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="bfb69-150">Dokument</span><span class="sxs-lookup"><span data-stu-id="bfb69-150">Document</span></span>  
23. <span data-ttu-id="bfb69-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-151">Click OK.</span></span>
24. <span data-ttu-id="bfb69-152">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="bfb69-153">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="bfb69-154">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="bfb69-155">Skriv "FileName" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="bfb69-156">FileName</span><span class="sxs-lookup"><span data-stu-id="bfb69-156">FileName</span></span>  
28. <span data-ttu-id="bfb69-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-157">Click OK.</span></span>
29. <span data-ttu-id="bfb69-158">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="bfb69-159">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="bfb69-160">Skriv 'FileContent' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bfb69-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="bfb69-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="bfb69-161">FileContent</span></span>  
32. <span data-ttu-id="bfb69-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-162">Click OK.</span></span>
33. <span data-ttu-id="bfb69-163">Vælg 'Invoice\EnclosedDocs\Document\FileContent' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="bfb69-164">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bfb69-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="bfb69-165">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="bfb69-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bfb69-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="bfb69-167">Knyt formateringselementer til datamodellen som en datakilde</span><span class="sxs-lookup"><span data-stu-id="bfb69-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="bfb69-168">Vælg 'Faktura\SalesOrder' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="bfb69-169">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="bfb69-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="bfb69-170">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="bfb69-171">Vælg 'model\Salgsordrenummer(SalesId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="bfb69-172">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="bfb69-172">Click Bind.</span></span>
6. <span data-ttu-id="bfb69-173">Vælg 'Faktura\InvoiceNumber' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="bfb69-174">Udvid 'model\Basisfaktura(InvoiceBase)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="bfb69-175">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturanummer(Id)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="bfb69-176">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="bfb69-176">Click Bind.</span></span>
10. <span data-ttu-id="bfb69-177">Vælg 'Faktura\InvoiceAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="bfb69-178">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturabeløb(Amount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="bfb69-179">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="bfb69-179">Click Bind.</span></span>
13. <span data-ttu-id="bfb69-180">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="bfb69-181">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="bfb69-182">Vælg 'Invoice\EnclosedDocs\Document\FileContent\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="bfb69-183">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="bfb69-183">Click Bind.</span></span>
17. <span data-ttu-id="bfb69-184">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="bfb69-185">Vælg 'Invoice\EnclosedDocs\Document\FileName' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="bfb69-186">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="bfb69-186">Click Bind.</span></span>
20. <span data-ttu-id="bfb69-187">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="bfb69-188">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="bfb69-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="bfb69-189">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="bfb69-189">Click Bind.</span></span>
23. <span data-ttu-id="bfb69-190">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bfb69-190">Click Save.</span></span>
24. <span data-ttu-id="bfb69-191">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bfb69-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]