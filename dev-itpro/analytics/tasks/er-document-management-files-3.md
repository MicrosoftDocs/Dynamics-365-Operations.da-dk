--- 
title: Oprette format til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5548839c4d394d45cfb39da50ca78dab4b4e08e4
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="d2ebe-103">Oprette format til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="d2ebe-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2ebe-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d2ebe-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d2ebe-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 2: Udvid datamodel)".</span><span class="sxs-lookup"><span data-stu-id="d2ebe-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="d2ebe-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="d2ebe-108">Opret et format til behandling af fakturaer</span><span class="sxs-lookup"><span data-stu-id="d2ebe-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="d2ebe-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d2ebe-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d2ebe-111">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="d2ebe-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="d2ebe-113">Du skal oprette et format for at generere elektroniske meddelelser med oplysninger om de filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="d2ebe-114">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="d2ebe-115">Skriv "Format baseret på datamodel\Debitorfakturamodel (brugerdefineret)" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="d2ebe-116">Skriv 'Eksempelmeddelelse i elektronisk faktura' i feltet navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="d2ebe-117">Eksempelmeddelelse i elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="d2ebe-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="d2ebe-118">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="d2ebe-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="d2ebe-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="d2ebe-120">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="d2ebe-121">Design et format til udfyldning af vedhæftede filer til generering af en meddelelse i MIME-format</span><span class="sxs-lookup"><span data-stu-id="d2ebe-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="d2ebe-122">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-122">Click Designer.</span></span>
2. <span data-ttu-id="d2ebe-123">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="d2ebe-124">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="d2ebe-125">Skriv 'Faktura' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="d2ebe-126">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="d2ebe-126">Invoice</span></span>  
5. <span data-ttu-id="d2ebe-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-127">Click OK.</span></span>
6. <span data-ttu-id="d2ebe-128">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="d2ebe-129">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="d2ebe-130">Skriv 'SalesOrder' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="d2ebe-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="d2ebe-131">SalesOrder</span></span>  
9. <span data-ttu-id="d2ebe-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-132">Click OK.</span></span>
10. <span data-ttu-id="d2ebe-133">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="d2ebe-134">Skriv "InvoiceNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="d2ebe-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="d2ebe-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="d2ebe-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-136">Click OK.</span></span>
13. <span data-ttu-id="d2ebe-137">Klik på Tilføj attribut.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="d2ebe-138">Skriv 'InvoiceAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="d2ebe-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="d2ebe-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="d2ebe-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-140">Click OK.</span></span>
16. <span data-ttu-id="d2ebe-141">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="d2ebe-142">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="d2ebe-143">Skriv "EnclosedDocs" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="d2ebe-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="d2ebe-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="d2ebe-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-145">Click OK.</span></span>
20. <span data-ttu-id="d2ebe-146">Vælg 'Faktura\EnclosedDocs' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="d2ebe-147">Klik på Tilføj element.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-147">Click Add Element.</span></span>
22. <span data-ttu-id="d2ebe-148">Skriv 'Dokument' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="d2ebe-149">Dokument</span><span class="sxs-lookup"><span data-stu-id="d2ebe-149">Document</span></span>  
23. <span data-ttu-id="d2ebe-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-150">Click OK.</span></span>
24. <span data-ttu-id="d2ebe-151">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="d2ebe-152">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="d2ebe-153">Vælg "XML\Attribut" i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="d2ebe-154">Skriv "FileName" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="d2ebe-155">FileName</span><span class="sxs-lookup"><span data-stu-id="d2ebe-155">FileName</span></span>  
28. <span data-ttu-id="d2ebe-156">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-156">Click OK.</span></span>
29. <span data-ttu-id="d2ebe-157">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="d2ebe-158">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="d2ebe-159">Skriv 'FileContent' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="d2ebe-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="d2ebe-160">FileContent</span></span>  
32. <span data-ttu-id="d2ebe-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-161">Click OK.</span></span>
33. <span data-ttu-id="d2ebe-162">Vælg 'Invoice\EnclosedDocs\Document\FileContent' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="d2ebe-163">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="d2ebe-164">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="d2ebe-165">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="d2ebe-166">Knyt formateringselementer til datamodellen som en datakilde</span><span class="sxs-lookup"><span data-stu-id="d2ebe-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="d2ebe-167">Vælg 'Faktura\SalesOrder' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="d2ebe-168">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="d2ebe-169">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="d2ebe-170">Vælg 'model\Salgsordrenummer(SalesId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="d2ebe-171">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-171">Click Bind.</span></span>
6. <span data-ttu-id="d2ebe-172">Vælg 'Faktura\InvoiceNumber' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="d2ebe-173">Udvid 'model\Basisfaktura(InvoiceBase)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="d2ebe-174">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturanummer(Id)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="d2ebe-175">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-175">Click Bind.</span></span>
10. <span data-ttu-id="d2ebe-176">Vælg 'Faktura\InvoiceAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="d2ebe-177">Vælg 'model\Basisfaktura(InvoiceBase)\Fakturabeløb(Amount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="d2ebe-178">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-178">Click Bind.</span></span>
13. <span data-ttu-id="d2ebe-179">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="d2ebe-180">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="d2ebe-181">Vælg 'Invoice\EnclosedDocs\Document\FileContent\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="d2ebe-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-182">Click Bind.</span></span>
17. <span data-ttu-id="d2ebe-183">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="d2ebe-184">Vælg 'Invoice\EnclosedDocs\Document\FileName' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="d2ebe-185">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-185">Click Bind.</span></span>
20. <span data-ttu-id="d2ebe-186">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="d2ebe-187">Vælg 'Faktura\EnclosedDocs\Dokument' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="d2ebe-188">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-188">Click Bind.</span></span>
23. <span data-ttu-id="d2ebe-189">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-189">Click Save.</span></span>
24. <span data-ttu-id="d2ebe-190">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d2ebe-190">Close the page.</span></span>


