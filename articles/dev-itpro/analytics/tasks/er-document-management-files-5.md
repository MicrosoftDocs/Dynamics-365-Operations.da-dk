--- 
title: "Ændre og køre formater til at bruge dokumentstyringsfiler i ER-output"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 5effbecf98e633d07f9e5eb22d3df1a12967c1e4
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="modify-and-run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="8501c-103">Ændre og køre formater til at bruge dokumentstyringsfiler i ER-output</span><span class="sxs-lookup"><span data-stu-id="8501c-103">Modify and run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8501c-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="8501c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="8501c-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="8501c-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="8501c-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 4: Kør model)".</span><span class="sxs-lookup"><span data-stu-id="8501c-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="8501c-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="8501c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="8501c-108">Rediger formatet til udfyldning af vedhæftede filer til generering af meddelelser i binært format</span><span class="sxs-lookup"><span data-stu-id="8501c-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="8501c-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="8501c-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8501c-110">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="8501c-111">Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="8501c-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="8501c-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="8501c-113">Click Designer.</span></span>
    * <span data-ttu-id="8501c-114">Du udfylder fakturameddelelsen i det oprettede output som en XML-fil ved hjælp af Unicode-kodning.</span><span class="sxs-lookup"><span data-stu-id="8501c-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="8501c-115">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="8501c-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="8501c-116">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="8501c-117">Skriv "Xml-meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="8501c-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="8501c-118">Xml-meddelelse</span><span class="sxs-lookup"><span data-stu-id="8501c-118">Xml message</span></span>  
9. <span data-ttu-id="8501c-119">Skriv "UTF-8" i feltet Kodning.</span><span class="sxs-lookup"><span data-stu-id="8501c-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="8501c-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="8501c-120">UTF-8</span></span>  
10. <span data-ttu-id="8501c-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8501c-121">Click OK.</span></span>
    * <span data-ttu-id="8501c-122">Konfigurer generering af output som en zip-fil.</span><span class="sxs-lookup"><span data-stu-id="8501c-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="8501c-123">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="8501c-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="8501c-124">Vælg "Common\Folder" i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="8501c-125">Skriv "Output i zip-format" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="8501c-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="8501c-126">Output i zip-format</span><span class="sxs-lookup"><span data-stu-id="8501c-126">Zip output</span></span>  
14. <span data-ttu-id="8501c-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8501c-127">Click OK.</span></span>
15. <span data-ttu-id="8501c-128">Vælg 'Output i zip-format' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="8501c-129">Føj vedhæftede filer til den genererende zip-fil som filer med de oprindelige navne og filtyper.</span><span class="sxs-lookup"><span data-stu-id="8501c-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="8501c-130">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="8501c-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="8501c-131">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="8501c-132">Skriv 'Vedhæftet fil' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="8501c-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="8501c-133">Vedhæftet fil</span><span class="sxs-lookup"><span data-stu-id="8501c-133">Attached file</span></span>  
19. <span data-ttu-id="8501c-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8501c-134">Click OK.</span></span>
20. <span data-ttu-id="8501c-135">Vælg 'Output i zip-format\Vedhæftet fil' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="8501c-136">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="8501c-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="8501c-137">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="8501c-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8501c-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="8501c-139">Tilknyt nye formateringselementer til datamodellen</span><span class="sxs-lookup"><span data-stu-id="8501c-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="8501c-140">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="8501c-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8501c-141">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="8501c-142">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="8501c-143">Vælg 'Output i zip-format\Vedhæftet fil\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="8501c-144">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="8501c-145">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8501c-145">Click Bind.</span></span>
7. <span data-ttu-id="8501c-146">Vælg 'Output i zip-format\Vedhæftet fil' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="8501c-147">Klik på Rediger filnavn.</span><span class="sxs-lookup"><span data-stu-id="8501c-147">Click Edit filename.</span></span>
9. <span data-ttu-id="8501c-148">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="8501c-149">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="8501c-150">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="8501c-151">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="8501c-151">Click Add data source.</span></span>
13. <span data-ttu-id="8501c-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8501c-152">Click Save.</span></span>
14. <span data-ttu-id="8501c-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8501c-153">Close the page.</span></span>
15. <span data-ttu-id="8501c-154">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="8501c-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="8501c-155">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8501c-155">Click Bind.</span></span>
17. <span data-ttu-id="8501c-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8501c-156">Click Save.</span></span>
18. <span data-ttu-id="8501c-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8501c-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="8501c-158">Kør rapporten, der er designet til den valgte faktura</span><span class="sxs-lookup"><span data-stu-id="8501c-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="8501c-159">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="8501c-159">Click Run.</span></span>
2. <span data-ttu-id="8501c-160">Udvid posterne for at inkludere sektion ().</span><span class="sxs-lookup"><span data-stu-id="8501c-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="8501c-161">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="8501c-161">Click Filter.</span></span>
4. <span data-ttu-id="8501c-162">Markér rækken Debitorfakturajournal og feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="8501c-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="8501c-163">Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".</span><span class="sxs-lookup"><span data-stu-id="8501c-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="8501c-164">000148</span><span class="sxs-lookup"><span data-stu-id="8501c-164">000148</span></span>  
6. <span data-ttu-id="8501c-165">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8501c-165">Click OK.</span></span>
7. <span data-ttu-id="8501c-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8501c-166">Click OK.</span></span>
    * <span data-ttu-id="8501c-167">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="8501c-167">Review the generated output.</span></span> <span data-ttu-id="8501c-168">Bemærk, at ud over fakturameddelelsen i XML-format er der oprettet en enkelt fil for hver vedhæftet fil.</span><span class="sxs-lookup"><span data-stu-id="8501c-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="8501c-169">De vedhæftede filer er udfyldt med zip-outputtet i binært format.</span><span class="sxs-lookup"><span data-stu-id="8501c-169">The attachment files are populated with the zipped output in binary format.</span></span>  


