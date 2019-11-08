---
title: ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)
description: Følgende trin beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER-output.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 618fabc96bdfeb0c2b577aa686702d9f1257ed70
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550711"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="5c855-103">ER Brug dokumentstyringsfiler i formatoutput (del 3 - Opret format)</span><span class="sxs-lookup"><span data-stu-id="5c855-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c855-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="5c855-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5c855-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="5c855-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5c855-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 2: Udvid datamodel)".</span><span class="sxs-lookup"><span data-stu-id="5c855-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="5c855-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="5c855-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="5c855-108">Opret et format til behandling af fakturaer</span><span class="sxs-lookup"><span data-stu-id="5c855-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="5c855-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5c855-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5c855-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="5c855-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5c855-111">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="5c855-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="5c855-113">Du skal oprette et format for at generere elektroniske meddelelser med oplysninger om de filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="5c855-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="5c855-114">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="5c855-115">Skriv "Format baseret på datamodel\Debitorfakturamodel (brugerdefineret)" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="5c855-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="5c855-116">Skriv 'Eksempelmeddelelse i elektronisk faktura' i feltet navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="5c855-117">Eksempelmeddelelse i elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="5c855-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="5c855-118">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="5c855-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="5c855-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="5c855-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="5c855-120">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c855-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="5c855-121">Design et format til udfyldning af vedhæftede filer til generering af en meddelelse i MIME-format</span><span class="sxs-lookup"><span data-stu-id="5c855-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="5c855-122">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="5c855-122">Click Designer.</span></span>
2. <span data-ttu-id="5c855-123">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="5c855-124">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="5c855-125">Skriv 'Faktura' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="5c855-126">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="5c855-126">Invoice</span></span>  
5. <span data-ttu-id="5c855-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-127">Click OK.</span></span>
6. <span data-ttu-id="5c855-128">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="5c855-129">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="5c855-130">Skriv 'SalesOrder' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="5c855-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="5c855-131">SalesOrder</span></span>  
9. <span data-ttu-id="5c855-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-132">Click OK.</span></span>
10. <span data-ttu-id="5c855-133">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="5c855-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="5c855-134">Skriv "InvoiceNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="5c855-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="5c855-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="5c855-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-136">Click OK.</span></span>
13. <span data-ttu-id="5c855-137">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="5c855-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="5c855-138">Skriv 'InvoiceAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="5c855-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="5c855-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="5c855-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-140">Click OK.</span></span>
16. <span data-ttu-id="5c855-141">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="5c855-142">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="5c855-143">Skriv "EnclosedDocs" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="5c855-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="5c855-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="5c855-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-145">Click OK.</span></span>
20. <span data-ttu-id="5c855-146">Vælg 'Faktura\EnclosedDocs' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="5c855-147">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="5c855-147">Click Add Element.</span></span>
22. <span data-ttu-id="5c855-148">Skriv 'Dokument' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="5c855-149">Dokument</span><span class="sxs-lookup"><span data-stu-id="5c855-149">Document</span></span>  
23. <span data-ttu-id="5c855-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-150">Click OK.</span></span>
24. <span data-ttu-id="5c855-151">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="5c855-152">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="5c855-153">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="5c855-154">Skriv "FileName" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="5c855-155">FileName</span><span class="sxs-lookup"><span data-stu-id="5c855-155">FileName</span></span>  
28. <span data-ttu-id="5c855-156">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-156">Click OK.</span></span>
29. <span data-ttu-id="5c855-157">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="5c855-158">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="5c855-159">Skriv 'FileContent' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5c855-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="5c855-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="5c855-160">FileContent</span></span>  
32. <span data-ttu-id="5c855-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-161">Click OK.</span></span>
33. <span data-ttu-id="5c855-162">Vælg 'Invoice\EnclosedDocs\Document\FileContent' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="5c855-163">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5c855-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="5c855-164">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="5c855-165">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c855-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="5c855-166">Knyt formateringselementer til datamodellen som en datakilde</span><span class="sxs-lookup"><span data-stu-id="5c855-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="5c855-167">Vælg 'Faktura\SalesOrder' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="5c855-168">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="5c855-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="5c855-169">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="5c855-170">Vælg 'model\Salgsordrenummer(SalesId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="5c855-171">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c855-171">Click Bind.</span></span>
6. <span data-ttu-id="5c855-172">Vælg 'Faktura\InvoiceNumber' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="5c855-173">Udvid 'model\Basisfaktura(InvoiceBase)' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="5c855-174">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturanummer(Id)' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="5c855-175">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c855-175">Click Bind.</span></span>
10. <span data-ttu-id="5c855-176">Vælg 'Faktura\InvoiceAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="5c855-177">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturabeløb(Amount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="5c855-178">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c855-178">Click Bind.</span></span>
13. <span data-ttu-id="5c855-179">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="5c855-180">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="5c855-181">Vælg 'Invoice\EnclosedDocs\Document\FileContent\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="5c855-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c855-182">Click Bind.</span></span>
17. <span data-ttu-id="5c855-183">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="5c855-184">Vælg 'Invoice\EnclosedDocs\Document\FileName' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="5c855-185">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c855-185">Click Bind.</span></span>
20. <span data-ttu-id="5c855-186">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="5c855-187">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c855-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="5c855-188">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="5c855-188">Click Bind.</span></span>
23. <span data-ttu-id="5c855-189">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5c855-189">Click Save.</span></span>
24. <span data-ttu-id="5c855-190">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c855-190">Close the page.</span></span>

