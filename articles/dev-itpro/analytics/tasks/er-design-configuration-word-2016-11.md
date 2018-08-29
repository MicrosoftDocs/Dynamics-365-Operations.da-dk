--- 
title: Designe ER-konfigurationer til at generere rapporter i Word-format
description: "Følgende trin beskriver, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapporteringsformat (ER) til at generere rapporter som Microsoft Word-filer."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.openlocfilehash: 615ab4a4f932478b8b847112d4fed8310187f03b
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="d53fa-103">Designe ER-konfigurationer til at generere rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="d53fa-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d53fa-104">Følgende trin beskriver, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapporteringsformat (ER) til at generere rapporter som Microsoft Word-filer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="d53fa-105">Disse trin kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="d53fa-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="d53fa-106">For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "Oprette en ER-konfiguration til generering af rapporter i OPENXML-format".</span><span class="sxs-lookup"><span data-stu-id="d53fa-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="d53fa-107">På forhånd skal du også hente og gemme følgende skabeloner lokalt for eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="d53fa-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

[<span data-ttu-id="d53fa-108">Skabelon for betalingsrapport</span><span class="sxs-lookup"><span data-stu-id="d53fa-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

[<span data-ttu-id="d53fa-109">Bundet skabelon for betalingsrapport</span><span class="sxs-lookup"><span data-stu-id="d53fa-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="d53fa-110">Denne fremgangsmåde er til en funktion, der blev tilføjet i Microsoft Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="d53fa-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="d53fa-111">Vælg den eksisterende ER-rapportkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d53fa-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="d53fa-112">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d53fa-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d53fa-113">Sørg for, at konfigurationsprovideren "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="d53fa-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="d53fa-114">er markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d53fa-114">is selected as active.</span></span>  
2. <span data-ttu-id="d53fa-115">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d53fa-116">Vi genbruger den eksisterende ER-konfiguration, der oprindeligt er udviklet til at generere rapporten i OPENXML-formatet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="d53fa-117">Udvid "Betalingsmodel" i træet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="d53fa-118">Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="d53fa-119">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="d53fa-120">Erstat Excel-skabelonen med Word-skabelonen</span><span class="sxs-lookup"><span data-stu-id="d53fa-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="d53fa-121">Aktuelt bruges Excel-dokumentet som en skabelon til at generere outputtet i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="d53fa-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="d53fa-122">Vi importerer rapportens skabelon i Word-format.</span><span class="sxs-lookup"><span data-stu-id="d53fa-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="d53fa-123">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-123">Click Attachments.</span></span>
    * <span data-ttu-id="d53fa-124">Erstat den eksisterende Excel-skabelon med Word-skabelonen, som du downloadede tidligere, Skabelon for betalingsrapport.</span><span class="sxs-lookup"><span data-stu-id="d53fa-124">Replace the existing Excel template with the Word template that you downloaded earlier, Template of Payment Report.</span></span> <span data-ttu-id="d53fa-125">Bemærk, at denne skabelon kun indeholder layoutet på det dokument, vi vil generere som ER-output.</span><span class="sxs-lookup"><span data-stu-id="d53fa-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="d53fa-126">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-126">Click Delete.</span></span>
3. <span data-ttu-id="d53fa-127">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="d53fa-127">Click Yes.</span></span>
4. <span data-ttu-id="d53fa-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d53fa-128">Click New.</span></span>
5. <span data-ttu-id="d53fa-129">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-129">Click File.</span></span>
6. <span data-ttu-id="d53fa-130">Klik på Gennemse.</span><span class="sxs-lookup"><span data-stu-id="d53fa-130">Click Browse.</span></span> <span data-ttu-id="d53fa-131">Naviger til og vælg SampleVendPaymDocReport.docx, som du tidligere downloadede.</span><span class="sxs-lookup"><span data-stu-id="d53fa-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="d53fa-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d53fa-132">Click OK.</span></span>
    * <span data-ttu-id="d53fa-133">Vælg den skabelon, du downloadede i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="d53fa-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="d53fa-134">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="d53fa-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="d53fa-135">Udvid Word-skabelonen ved at tilføje en brugerdefineret XML-del</span><span class="sxs-lookup"><span data-stu-id="d53fa-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="d53fa-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d53fa-136">Click Save.</span></span>
    * <span data-ttu-id="d53fa-137">I tillæg til at lagre konfigurationsændringer opdaterer handlingen Gem også den vedhæftede Word-skabelon.</span><span class="sxs-lookup"><span data-stu-id="d53fa-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="d53fa-138">Strukturen på det designede format overføres til det vedhæftede Word-dokument som en ny brugerdefineret XML-del med navnet "Rapport".</span><span class="sxs-lookup"><span data-stu-id="d53fa-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="d53fa-139">Bemærk, at den vedhæftede Word-skabelon ikke kun indeholder layoutet på det dokument, vi vil generere som ER-output, den indeholder også strukturen af data, som ER udfylder i denne skabelon på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="d53fa-140">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-140">Click Attachments.</span></span>
    * <span data-ttu-id="d53fa-141">Nu skal du binde elementerne i den brugerdefinerede XML-del "Rapport" til Word-dokumentdelene.</span><span class="sxs-lookup"><span data-stu-id="d53fa-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="d53fa-142">Hvis du har kendskab til Word-dokumenter, der kan designes som formularer, der indeholder indholdskontrolelementer, der er bundet til elementer i brugerdefinerede XML-dele – kan du afspille alle trin i den næste underopgave for at oprette et sådant dokument.</span><span class="sxs-lookup"><span data-stu-id="d53fa-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="d53fa-143">Se dette link for at få flere oplysninger https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="d53fa-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="d53fa-144">Ellers skal du springe alle trin i den næste underopgave over.</span><span class="sxs-lookup"><span data-stu-id="d53fa-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="d53fa-145">Få Word med brugerdefineret XML-del til at udføre databindinger</span><span class="sxs-lookup"><span data-stu-id="d53fa-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="d53fa-146">Åbn dette dokument i Word og gør følgende: - Åbn fanen Developer i Word (tilpas båndet, hvis den endnu ikke er aktiveret).</span><span class="sxs-lookup"><span data-stu-id="d53fa-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="d53fa-147">- Vælg XML-tilknytningsrude.</span><span class="sxs-lookup"><span data-stu-id="d53fa-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="d53fa-148">- Vælg den brugerdefinerede del "Rapport" i opslaget.</span><span class="sxs-lookup"><span data-stu-id="d53fa-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="d53fa-149">- Udfør tilknytningen af elementerne i den markerede brugerdefinerede XML-del og indholdskontrolelementerne i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="d53fa-150">- Gem det opdaterede Word-dokument på et lokalt drev.</span><span class="sxs-lookup"><span data-stu-id="d53fa-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="d53fa-151">Upload Word-skabelonen med brugerdefineret XML-del bundet til indholdskontrolelementer</span><span class="sxs-lookup"><span data-stu-id="d53fa-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="d53fa-152">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="d53fa-152">Click Delete.</span></span>
2. <span data-ttu-id="d53fa-153">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="d53fa-153">Click Yes.</span></span>
    * <span data-ttu-id="d53fa-154">Tilføj en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="d53fa-154">Add a new template.</span></span> <span data-ttu-id="d53fa-155">Hvis du udførte trinnene i den tidligere underopgave, skal du markere det Word-dokument, som du har klargjort og gemt lokalt.</span><span class="sxs-lookup"><span data-stu-id="d53fa-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="d53fa-156">Ellers skal du vælge MS Word-skabelonen SampleVendPaymDocReportBounded.docx, som du tidligere downloadede.</span><span class="sxs-lookup"><span data-stu-id="d53fa-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="d53fa-157">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d53fa-157">Click New.</span></span>
4. <span data-ttu-id="d53fa-158">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-158">Click File.</span></span>
5. <span data-ttu-id="d53fa-159">Klik på Gennemse.</span><span class="sxs-lookup"><span data-stu-id="d53fa-159">Click Browse.</span></span> <span data-ttu-id="d53fa-160">Naviger til og vælg SampleVendPaymDocReportBounded.docx, som du tidligere downloadede.</span><span class="sxs-lookup"><span data-stu-id="d53fa-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="d53fa-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d53fa-161">Click OK.</span></span>
6. <span data-ttu-id="d53fa-162">Vælg det dokument i feltet Skabelon, som du downloadede i det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="d53fa-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="d53fa-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d53fa-163">Click Save.</span></span>
8. <span data-ttu-id="d53fa-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d53fa-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="d53fa-165">Udfør formatet for at oprette Word-output</span><span class="sxs-lookup"><span data-stu-id="d53fa-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="d53fa-166">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d53fa-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="d53fa-167">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="d53fa-167">Click User parameters.</span></span>
3. <span data-ttu-id="d53fa-168">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="d53fa-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="d53fa-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d53fa-169">Click OK.</span></span>
5. <span data-ttu-id="d53fa-170">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d53fa-170">Click Edit.</span></span>
6. <span data-ttu-id="d53fa-171">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="d53fa-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="d53fa-172">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d53fa-172">Click Save.</span></span>
8. <span data-ttu-id="d53fa-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d53fa-173">Close the page.</span></span>
9. <span data-ttu-id="d53fa-174">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d53fa-174">Close the page.</span></span>
10. <span data-ttu-id="d53fa-175">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="d53fa-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="d53fa-176">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="d53fa-176">Click Lines.</span></span>
12. <span data-ttu-id="d53fa-177">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="d53fa-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="d53fa-178">Klik på Betalingsstatus.</span><span class="sxs-lookup"><span data-stu-id="d53fa-178">Click Payment status.</span></span>
14. <span data-ttu-id="d53fa-179">Klik på Ingen.</span><span class="sxs-lookup"><span data-stu-id="d53fa-179">Click None.</span></span>
15. <span data-ttu-id="d53fa-180">Klik på Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="d53fa-180">Click Generate payments.</span></span>
16. <span data-ttu-id="d53fa-181">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d53fa-181">Click OK.</span></span>
17. <span data-ttu-id="d53fa-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d53fa-182">Click OK.</span></span>
    * <span data-ttu-id="d53fa-183">Analysér det genererede output.</span><span class="sxs-lookup"><span data-stu-id="d53fa-183">Analyze the generated output.</span></span> <span data-ttu-id="d53fa-184">Bemærk, at det oprettede output vises i Word-format og indeholder oplysninger om de behandlede betalinger.</span><span class="sxs-lookup"><span data-stu-id="d53fa-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


