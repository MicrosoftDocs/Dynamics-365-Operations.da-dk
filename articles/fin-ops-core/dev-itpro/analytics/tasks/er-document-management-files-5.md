---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 5: Ændrings- og kørselsformat)'
description: Dette emne beskriver, hvordan du konfigurerer et ER-format (elektronisk rapportering) til at bruge dokumentstyringsfiler (vedhæftede filer) i ER-output. (Del 5)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f954b76a09bf7c5edd4c608d400318fbd9386778
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749087"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="0a6b6-104">ER Brug dokumentstyringsfiler i formatoutput (del 5: Ændrings- og kørselsformat)</span><span class="sxs-lookup"><span data-stu-id="0a6b6-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a6b6-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0a6b6-106">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0a6b6-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 4: Kør model)".</span><span class="sxs-lookup"><span data-stu-id="0a6b6-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="0a6b6-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="0a6b6-109">Rediger formatet til udfyldning af vedhæftede filer til generering af meddelelser i binært format</span><span class="sxs-lookup"><span data-stu-id="0a6b6-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="0a6b6-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0a6b6-111">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="0a6b6-112">Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="0a6b6-113">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="0a6b6-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-114">Click Designer.</span></span>
    * <span data-ttu-id="0a6b6-115">Du udfylder fakturameddelelsen i det oprettede output som en XML-fil ved hjælp af Unicode-kodning.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="0a6b6-116">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="0a6b6-117">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="0a6b6-118">Skriv "Xml-meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="0a6b6-119">Xml-meddelelse</span><span class="sxs-lookup"><span data-stu-id="0a6b6-119">Xml message</span></span>  
9. <span data-ttu-id="0a6b6-120">Skriv "UTF-8" i feltet Kodning.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0a6b6-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0a6b6-121">UTF-8</span></span>  
10. <span data-ttu-id="0a6b6-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-122">Click OK.</span></span>
    * <span data-ttu-id="0a6b6-123">Konfigurer generering af output som en zip-fil.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="0a6b6-124">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="0a6b6-125">Vælg "Common\Folder" i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="0a6b6-126">Skriv "Output i zip-format" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="0a6b6-127">Output i zip-format</span><span class="sxs-lookup"><span data-stu-id="0a6b6-127">Zip output</span></span>  
14. <span data-ttu-id="0a6b6-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-128">Click OK.</span></span>
15. <span data-ttu-id="0a6b6-129">Vælg 'Output i zip-format' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="0a6b6-130">Føj vedhæftede filer til den genererende zip-fil som filer med de oprindelige navne og filtyper.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="0a6b6-131">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="0a6b6-132">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="0a6b6-133">Skriv 'Vedhæftet fil' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="0a6b6-134">Vedhæftet fil</span><span class="sxs-lookup"><span data-stu-id="0a6b6-134">Attached file</span></span>  
19. <span data-ttu-id="0a6b6-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-135">Click OK.</span></span>
20. <span data-ttu-id="0a6b6-136">Vælg 'Output i zip-format\Vedhæftet fil' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="0a6b6-137">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="0a6b6-138">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="0a6b6-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="0a6b6-140">Tilknyt nye formateringselementer til datamodellen</span><span class="sxs-lookup"><span data-stu-id="0a6b6-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="0a6b6-141">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0a6b6-142">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="0a6b6-143">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="0a6b6-144">Vælg 'Output i zip-format\Vedhæftet fil\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="0a6b6-145">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="0a6b6-146">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-146">Click Bind.</span></span>
7. <span data-ttu-id="0a6b6-147">Vælg 'Output i zip-format\Vedhæftet fil' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="0a6b6-148">Klik på Rediger filnavn.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-148">Click Edit filename.</span></span>
9. <span data-ttu-id="0a6b6-149">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="0a6b6-150">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="0a6b6-151">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="0a6b6-152">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-152">Click Add data source.</span></span>
13. <span data-ttu-id="0a6b6-153">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-153">Click Save.</span></span>
14. <span data-ttu-id="0a6b6-154">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-154">Close the page.</span></span>
15. <span data-ttu-id="0a6b6-155">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="0a6b6-156">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-156">Click Bind.</span></span>
17. <span data-ttu-id="0a6b6-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-157">Click Save.</span></span>
18. <span data-ttu-id="0a6b6-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="0a6b6-159">Kør rapporten, der er designet til den valgte faktura</span><span class="sxs-lookup"><span data-stu-id="0a6b6-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="0a6b6-160">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-160">Click Run.</span></span>
2. <span data-ttu-id="0a6b6-161">Udvid posterne for at inkludere sektion ().</span><span class="sxs-lookup"><span data-stu-id="0a6b6-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="0a6b6-162">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-162">Click Filter.</span></span>
4. <span data-ttu-id="0a6b6-163">Markér rækken Debitorfakturajournal og feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="0a6b6-164">Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".</span><span class="sxs-lookup"><span data-stu-id="0a6b6-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="0a6b6-165">000148</span><span class="sxs-lookup"><span data-stu-id="0a6b6-165">000148</span></span>  
6. <span data-ttu-id="0a6b6-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-166">Click OK.</span></span>
7. <span data-ttu-id="0a6b6-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-167">Click OK.</span></span>
    * <span data-ttu-id="0a6b6-168">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-168">Review the generated output.</span></span> <span data-ttu-id="0a6b6-169">Bemærk, at ud over fakturameddelelsen i XML-format er der oprettet en enkelt fil for hver vedhæftet fil.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="0a6b6-170">De vedhæftede filer er udfyldt med zip-outputtet i binært format.</span><span class="sxs-lookup"><span data-stu-id="0a6b6-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]