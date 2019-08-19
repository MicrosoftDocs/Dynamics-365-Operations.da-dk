---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 5: Ændrings- og kørselsformat)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba9cc4dcdfcfbc1bdb933336e85da9b4b6d97a40
ms.sourcegitcommit: f5556189a80ad9f23f1af3333837eae034ddb247
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/29/2019
ms.locfileid: "1791850"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="856b6-103">ER Brug dokumentstyringsfiler i formatoutput (del 5: Ændrings- og kørselsformat)</span><span class="sxs-lookup"><span data-stu-id="856b6-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="856b6-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="856b6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="856b6-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="856b6-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="856b6-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 4: Kør model)".</span><span class="sxs-lookup"><span data-stu-id="856b6-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="856b6-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="856b6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="856b6-108">Rediger formatet til udfyldning af vedhæftede filer til generering af meddelelser i binært format</span><span class="sxs-lookup"><span data-stu-id="856b6-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="856b6-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="856b6-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="856b6-110">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="856b6-111">Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="856b6-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="856b6-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="856b6-113">Click Designer.</span></span>
    * <span data-ttu-id="856b6-114">Du udfylder fakturameddelelsen i det oprettede output som en XML-fil ved hjælp af Unicode-kodning.</span><span class="sxs-lookup"><span data-stu-id="856b6-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="856b6-115">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="856b6-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="856b6-116">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="856b6-117">Skriv "Xml-meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="856b6-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="856b6-118">Xml-meddelelse</span><span class="sxs-lookup"><span data-stu-id="856b6-118">Xml message</span></span>  
9. <span data-ttu-id="856b6-119">Skriv "UTF-8" i feltet Kodning.</span><span class="sxs-lookup"><span data-stu-id="856b6-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="856b6-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="856b6-120">UTF-8</span></span>  
10. <span data-ttu-id="856b6-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="856b6-121">Click OK.</span></span>
    * <span data-ttu-id="856b6-122">Konfigurer generering af output som en zip-fil.</span><span class="sxs-lookup"><span data-stu-id="856b6-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="856b6-123">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="856b6-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="856b6-124">Vælg "Common\Folder" i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="856b6-125">Skriv "Output i zip-format" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="856b6-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="856b6-126">Output i zip-format</span><span class="sxs-lookup"><span data-stu-id="856b6-126">Zip output</span></span>  
14. <span data-ttu-id="856b6-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="856b6-127">Click OK.</span></span>
15. <span data-ttu-id="856b6-128">Vælg 'Output i zip-format' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="856b6-129">Føj vedhæftede filer til den genererende zip-fil som filer med de oprindelige navne og filtyper.</span><span class="sxs-lookup"><span data-stu-id="856b6-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="856b6-130">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="856b6-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="856b6-131">Vælg "Common\File" i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="856b6-132">Skriv 'Vedhæftet fil' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="856b6-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="856b6-133">Vedhæftet fil</span><span class="sxs-lookup"><span data-stu-id="856b6-133">Attached file</span></span>  
19. <span data-ttu-id="856b6-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="856b6-134">Click OK.</span></span>
20. <span data-ttu-id="856b6-135">Vælg 'Output i zip-format\Vedhæftet fil' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="856b6-136">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="856b6-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="856b6-137">Vælg 'Text\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="856b6-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="856b6-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="856b6-139">Tilknyt nye formateringselementer til datamodellen</span><span class="sxs-lookup"><span data-stu-id="856b6-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="856b6-140">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="856b6-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="856b6-141">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="856b6-142">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="856b6-143">Vælg 'Output i zip-format\Vedhæftet fil\Base64' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="856b6-144">Vælg 'model\Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="856b6-145">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="856b6-145">Click Bind.</span></span>
7. <span data-ttu-id="856b6-146">Vælg 'Output i zip-format\Vedhæftet fil' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="856b6-147">Klik på Rediger filnavn.</span><span class="sxs-lookup"><span data-stu-id="856b6-147">Click Edit filename.</span></span>
9. <span data-ttu-id="856b6-148">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="856b6-149">Udvid 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="856b6-150">Vælg 'model\Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="856b6-151">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="856b6-151">Click Add data source.</span></span>
13. <span data-ttu-id="856b6-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="856b6-152">Click Save.</span></span>
14. <span data-ttu-id="856b6-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="856b6-153">Close the page.</span></span>
15. <span data-ttu-id="856b6-154">Vælg 'model\Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="856b6-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="856b6-155">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="856b6-155">Click Bind.</span></span>
17. <span data-ttu-id="856b6-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="856b6-156">Click Save.</span></span>
18. <span data-ttu-id="856b6-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="856b6-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="856b6-158">Kør rapporten, der er designet til den valgte faktura</span><span class="sxs-lookup"><span data-stu-id="856b6-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="856b6-159">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="856b6-159">Click Run.</span></span>
2. <span data-ttu-id="856b6-160">Udvid posterne for at inkludere sektion ().</span><span class="sxs-lookup"><span data-stu-id="856b6-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="856b6-161">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="856b6-161">Click Filter.</span></span>
4. <span data-ttu-id="856b6-162">Markér rækken Debitorfakturajournal og feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="856b6-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="856b6-163">Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".</span><span class="sxs-lookup"><span data-stu-id="856b6-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="856b6-164">000148</span><span class="sxs-lookup"><span data-stu-id="856b6-164">000148</span></span>  
6. <span data-ttu-id="856b6-165">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="856b6-165">Click OK.</span></span>
7. <span data-ttu-id="856b6-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="856b6-166">Click OK.</span></span>
    * <span data-ttu-id="856b6-167">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="856b6-167">Review the generated output.</span></span> <span data-ttu-id="856b6-168">Bemærk, at ud over fakturameddelelsen i XML-format er der oprettet en enkelt fil for hver vedhæftet fil.</span><span class="sxs-lookup"><span data-stu-id="856b6-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="856b6-169">De vedhæftede filer er udfyldt med zip-outputtet i binært format.</span><span class="sxs-lookup"><span data-stu-id="856b6-169">The attachment files are populated with the zipped output in binary format.</span></span>  

