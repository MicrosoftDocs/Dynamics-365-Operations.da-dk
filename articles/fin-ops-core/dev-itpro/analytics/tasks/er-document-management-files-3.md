---
title: ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til at bruge dokumentstyringsfiler i ER-output. (Del 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092610"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="2ab33-104">ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)</span><span class="sxs-lookup"><span data-stu-id="2ab33-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ab33-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="2ab33-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="2ab33-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="2ab33-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="2ab33-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 2: Udvid datamodel)".</span><span class="sxs-lookup"><span data-stu-id="2ab33-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="2ab33-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="2ab33-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="2ab33-109">Opret et format til behandling af fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ab33-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="2ab33-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="2ab33-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2ab33-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="2ab33-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2ab33-112">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="2ab33-113">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="2ab33-114">Du skal oprette et format for at generere elektroniske meddelelser med oplysninger om de filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="2ab33-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="2ab33-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="2ab33-116">Skriv "Format baseret på datamodel\Debitorfakturamodel (brugerdefineret)" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="2ab33-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="2ab33-117">Skriv 'Eksempelmeddelelse i elektronisk faktura' i feltet navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="2ab33-118">Eksempelmeddelelse i elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="2ab33-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="2ab33-119">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="2ab33-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="2ab33-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="2ab33-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="2ab33-121">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2ab33-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="2ab33-122">Design et format til udfyldning af vedhæftede filer til generering af en meddelelse i MIME-format</span><span class="sxs-lookup"><span data-stu-id="2ab33-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="2ab33-123">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="2ab33-123">Click Designer.</span></span>
2. <span data-ttu-id="2ab33-124">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="2ab33-125">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="2ab33-126">Skriv 'Faktura' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="2ab33-127">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ab33-127">Invoice</span></span>  
5. <span data-ttu-id="2ab33-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-128">Click OK.</span></span>
6. <span data-ttu-id="2ab33-129">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="2ab33-130">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="2ab33-131">Skriv 'SalesOrder' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="2ab33-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="2ab33-132">SalesOrder</span></span>  
9. <span data-ttu-id="2ab33-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-133">Click OK.</span></span>
10. <span data-ttu-id="2ab33-134">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="2ab33-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="2ab33-135">Skriv "InvoiceNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="2ab33-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="2ab33-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="2ab33-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-137">Click OK.</span></span>
13. <span data-ttu-id="2ab33-138">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="2ab33-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="2ab33-139">Skriv 'InvoiceAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="2ab33-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="2ab33-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="2ab33-141">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-141">Click OK.</span></span>
16. <span data-ttu-id="2ab33-142">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="2ab33-143">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="2ab33-144">Skriv "EnclosedDocs" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="2ab33-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="2ab33-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="2ab33-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-146">Click OK.</span></span>
20. <span data-ttu-id="2ab33-147">Vælg 'Faktura\EnclosedDocs' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="2ab33-148">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="2ab33-148">Click Add Element.</span></span>
22. <span data-ttu-id="2ab33-149">Skriv 'Dokument' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="2ab33-150">Dokument</span><span class="sxs-lookup"><span data-stu-id="2ab33-150">Document</span></span>  
23. <span data-ttu-id="2ab33-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-151">Click OK.</span></span>
24. <span data-ttu-id="2ab33-152">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="2ab33-153">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="2ab33-154">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="2ab33-155">Skriv "FileName" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="2ab33-156">FileName</span><span class="sxs-lookup"><span data-stu-id="2ab33-156">FileName</span></span>  
28. <span data-ttu-id="2ab33-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-157">Click OK.</span></span>
29. <span data-ttu-id="2ab33-158">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="2ab33-159">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="2ab33-160">Skriv 'FileContent' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="2ab33-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="2ab33-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="2ab33-161">FileContent</span></span>  
32. <span data-ttu-id="2ab33-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-162">Click OK.</span></span>
33. <span data-ttu-id="2ab33-163">Vælg 'Invoice\EnclosedDocs\Document\FileContent' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="2ab33-164">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="2ab33-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="2ab33-165">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="2ab33-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2ab33-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="2ab33-167">Knyt formateringselementer til datamodellen som en datakilde</span><span class="sxs-lookup"><span data-stu-id="2ab33-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="2ab33-168">Vælg 'Faktura\SalesOrder' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="2ab33-169">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="2ab33-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="2ab33-170">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="2ab33-171">Vælg 'model\Salgsordrenummer(SalesId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="2ab33-172">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2ab33-172">Click Bind.</span></span>
6. <span data-ttu-id="2ab33-173">Vælg 'Faktura\InvoiceNumber' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="2ab33-174">Udvid 'model\Basisfaktura(InvoiceBase)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="2ab33-175">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturanummer(Id)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="2ab33-176">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2ab33-176">Click Bind.</span></span>
10. <span data-ttu-id="2ab33-177">Vælg 'Faktura\InvoiceAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="2ab33-178">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturabeløb(Amount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="2ab33-179">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2ab33-179">Click Bind.</span></span>
13. <span data-ttu-id="2ab33-180">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="2ab33-181">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="2ab33-182">Vælg 'Invoice\EnclosedDocs\Document\FileContent\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="2ab33-183">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2ab33-183">Click Bind.</span></span>
17. <span data-ttu-id="2ab33-184">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="2ab33-185">Vælg 'Invoice\EnclosedDocs\Document\FileName' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="2ab33-186">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2ab33-186">Click Bind.</span></span>
20. <span data-ttu-id="2ab33-187">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="2ab33-188">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="2ab33-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="2ab33-189">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="2ab33-189">Click Bind.</span></span>
23. <span data-ttu-id="2ab33-190">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2ab33-190">Click Save.</span></span>
24. <span data-ttu-id="2ab33-191">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2ab33-191">Close the page.</span></span>

