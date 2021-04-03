---
title: Generere rapporter i Office-format, der har integrerede billeder
description: Dette emne viser, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere elektroniske dokumenter i Excel- og Word-format, der indeholder integrerede billeder.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ed0ab0042c98f063eb0ec2ab31c913d9385186c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569454"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="0bbae-103">Generere rapporter i Office-format, der har integrerede billeder</span><span class="sxs-lookup"><span data-stu-id="0bbae-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0bbae-104">Følgende trin beskriver, hvordan en bruger i rollen som enten "Systemadministrator" eller "Udvikler af elektronisk rapportering" kan designe konfigurationer til elektronisk rapportering (ER) med henblik på oprettelse af elektroniske dokumenter i MS Office-formater (Excel og Word), der indeholder integrerede billeder.</span><span class="sxs-lookup"><span data-stu-id="0bbae-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="0bbae-105">I dette eksempel skal du bruge oprettede ER-konfigurationer for eksempelfirmaet 'Litware Inc'.</span><span class="sxs-lookup"><span data-stu-id="0bbae-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="0bbae-106">For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "ER Oprette rapporter i Microsoft Office-formater med integrerede billeder (Del 2: Gennemse konfigurationer)".</span><span class="sxs-lookup"><span data-stu-id="0bbae-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="0bbae-107">Disse trin kan udføres i 'USMF'-virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0bbae-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="0bbae-108">Køre format med startmodeltilknytning</span><span class="sxs-lookup"><span data-stu-id="0bbae-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="0bbae-109">Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="0bbae-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="0bbae-110">Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="0bbae-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="0bbae-111">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="0bbae-112">Klik på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="0bbae-112">Click Check.</span></span>
5. <span data-ttu-id="0bbae-113">Klik på Udskriv prøve.</span><span class="sxs-lookup"><span data-stu-id="0bbae-113">Click Print test.</span></span>
    * <span data-ttu-id="0bbae-114">Kør formatet til testformål.</span><span class="sxs-lookup"><span data-stu-id="0bbae-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="0bbae-115">Vælg Ja i feltet Omsætteligt checkformat.</span><span class="sxs-lookup"><span data-stu-id="0bbae-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="0bbae-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bbae-116">Click OK.</span></span>
    * <span data-ttu-id="0bbae-117">Gennemse det oprettede output.</span><span class="sxs-lookup"><span data-stu-id="0bbae-117">Review the created output.</span></span> <span data-ttu-id="0bbae-118">Firmaets logo vises i rapporten sammen med den autoriserede persons signatur.</span><span class="sxs-lookup"><span data-stu-id="0bbae-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="0bbae-119">Signaturbilledet hentes fra feltet af 'Container'-datatypen i den checklayoutpost, der er tilknyttet den valgte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="0bbae-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="0bbae-120">Udvid sektionen Kopier.</span><span class="sxs-lookup"><span data-stu-id="0bbae-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="0bbae-121">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0bbae-121">Click Edit.</span></span>
10. <span data-ttu-id="0bbae-122">Angiv 'Udskriv vandmærke som Ugyldig' i feltet Vandmærke.</span><span class="sxs-lookup"><span data-stu-id="0bbae-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="0bbae-123">Rediger indstillingen for vandmærkelayout, så den viser vandmærketeksten i dokumentoprettelse i et Excel-figurelement.</span><span class="sxs-lookup"><span data-stu-id="0bbae-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="0bbae-124">Klik på Udskriv prøve.</span><span class="sxs-lookup"><span data-stu-id="0bbae-124">Click Print test.</span></span>
12. <span data-ttu-id="0bbae-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bbae-125">Click OK.</span></span>
    * <span data-ttu-id="0bbae-126">Gennemse det oprettede output.</span><span class="sxs-lookup"><span data-stu-id="0bbae-126">Review the created output.</span></span> <span data-ttu-id="0bbae-127">Vandmærket vises i den oprettede rapport i henhold til markeringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="0bbae-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="0bbae-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-128">Close the page.</span></span>
14. <span data-ttu-id="0bbae-129">Klik på Administrer betalinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="0bbae-130">Klik på Checks.</span><span class="sxs-lookup"><span data-stu-id="0bbae-130">Click Checks.</span></span>
16. <span data-ttu-id="0bbae-131">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="0bbae-131">Click Show filters.</span></span>
17. <span data-ttu-id="0bbae-132">Angiv følgende filtre: Angiv en filterværdi på "381", "385", "389" for feltet "Checknummer" ved hjælp af filteroperatoren "er én af".</span><span class="sxs-lookup"><span data-stu-id="0bbae-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="0bbae-133">Markér alle poster på listen.</span><span class="sxs-lookup"><span data-stu-id="0bbae-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="0bbae-134">Klik på Udskriv checkkopi.</span><span class="sxs-lookup"><span data-stu-id="0bbae-134">Click Print check copy.</span></span>
    * <span data-ttu-id="0bbae-135">Kør formatet for at udskrive de valgte checks igen.</span><span class="sxs-lookup"><span data-stu-id="0bbae-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="0bbae-136">Gennemse det oprettede output.</span><span class="sxs-lookup"><span data-stu-id="0bbae-136">Review the created output.</span></span> <span data-ttu-id="0bbae-137">De valgte checks er udskrevet igen.</span><span class="sxs-lookup"><span data-stu-id="0bbae-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="0bbae-138">Firmaets logo og etiketter udskrives ikke, fordi de præsenteres i den fortrykte formular.</span><span class="sxs-lookup"><span data-stu-id="0bbae-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="0bbae-139">Ændre tilknytningen af den importerede datamodel</span><span class="sxs-lookup"><span data-stu-id="0bbae-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="0bbae-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-140">Close the page.</span></span>
2. <span data-ttu-id="0bbae-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-141">Close the page.</span></span>
3. <span data-ttu-id="0bbae-142">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="0bbae-143">Vælg 'Model for checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="0bbae-144">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-144">Click Designer.</span></span>
6. <span data-ttu-id="0bbae-145">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="0bbae-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="0bbae-146">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-146">Click Designer.</span></span>
    * <span data-ttu-id="0bbae-147">Vi ændrer bindingen af datamodellens signaturelement for at få signaturbilledet fra den fil, der var vedhæftet i den checklayoutpost, der er tilknyttet den valgte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="0bbae-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="0bbae-148">Slå Vis detaljer fra.</span><span class="sxs-lookup"><span data-stu-id="0bbae-148">Turn off Show details.</span></span>
9. <span data-ttu-id="0bbae-149">Udvid 'layout' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="0bbae-150">Udvid 'layout\signatur' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="0bbae-151">Vælg 'layout\signatur\billede = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="0bbae-152">Udvid 'chequesaccount' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="0bbae-153">Udvid 'chequesaccount\<Relationer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="0bbae-154">Udvid 'chequesaccount\<Relationer\BankChequeLayout' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="0bbae-155">Udvid 'chequesaccount\<Relationer\BankChequeLayout\<Relationer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="0bbae-156">Udvid 'chequesaccount\<Relationer\BankChequeLayout\<Relationer\<Dokumenter' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="0bbae-157">Vælg 'chequesaccount\<Relationer\BankChequeLayout\<Relationer\<Dokumenter\getFileContentAsContainer()' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="0bbae-158">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="0bbae-158">Click Bind.</span></span>
19. <span data-ttu-id="0bbae-159">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0bbae-159">Click Save.</span></span>
20. <span data-ttu-id="0bbae-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-160">Close the page.</span></span>
21. <span data-ttu-id="0bbae-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-161">Close the page.</span></span>
22. <span data-ttu-id="0bbae-162">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-162">Close the page.</span></span>
23. <span data-ttu-id="0bbae-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="0bbae-164">Kør format ved hjælp af tilpasset modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="0bbae-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="0bbae-165">Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="0bbae-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="0bbae-166">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="0bbae-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0bbae-167">Filtrer f.eks. efter feltet Bankkonto med værdien "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="0bbae-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="0bbae-168">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="0bbae-169">Klik på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="0bbae-169">Click Check.</span></span>
5. <span data-ttu-id="0bbae-170">Klik på Udskriv prøve.</span><span class="sxs-lookup"><span data-stu-id="0bbae-170">Click Print test.</span></span>
6. <span data-ttu-id="0bbae-171">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bbae-171">Click OK.</span></span>
    * <span data-ttu-id="0bbae-172">Gennemse det oprettede output.</span><span class="sxs-lookup"><span data-stu-id="0bbae-172">Review the created output.</span></span> <span data-ttu-id="0bbae-173">Billedet fra den vedhæftede fil i Dokumentstyring vises som en autoriseret persons signatur.</span><span class="sxs-lookup"><span data-stu-id="0bbae-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="0bbae-174">Bruge MS Word-dokument som en skabelon i det importerede format</span><span class="sxs-lookup"><span data-stu-id="0bbae-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="0bbae-175">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-175">Close the page.</span></span>
2. <span data-ttu-id="0bbae-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-176">Close the page.</span></span>
3. <span data-ttu-id="0bbae-177">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="0bbae-178">Udvid 'Model for checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="0bbae-179">Vælg 'Model for checks\Checkudskrivningsformat' i træet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="0bbae-180">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-180">Click Designer.</span></span>
7. <span data-ttu-id="0bbae-181">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-181">Click Attachments.</span></span>
8. <span data-ttu-id="0bbae-182">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="0bbae-182">Click Delete.</span></span>
9. <span data-ttu-id="0bbae-183">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="0bbae-183">Click Yes.</span></span>
10. <span data-ttu-id="0bbae-184">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0bbae-184">Click New.</span></span>
11. <span data-ttu-id="0bbae-185">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="0bbae-185">Click File.</span></span>
    * <span data-ttu-id="0bbae-186">Klik på Gennemse, og vælg skabelonfilen 'Cheque template Word.docx', der er hentet på forhånd.</span><span class="sxs-lookup"><span data-stu-id="0bbae-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="0bbae-187">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-187">Close the page.</span></span>
13. <span data-ttu-id="0bbae-188">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="0bbae-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="0bbae-189">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0bbae-189">Click Save.</span></span>
15. <span data-ttu-id="0bbae-190">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-190">Close the page.</span></span>
16. <span data-ttu-id="0bbae-191">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0bbae-191">Click Edit.</span></span>
17. <span data-ttu-id="0bbae-192">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="0bbae-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="0bbae-193">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0bbae-193">Close the page.</span></span>
19. <span data-ttu-id="0bbae-194">Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="0bbae-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="0bbae-195">Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="0bbae-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="0bbae-196">Klik på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="0bbae-196">Click Check.</span></span>
22. <span data-ttu-id="0bbae-197">Klik på Udskriv prøve.</span><span class="sxs-lookup"><span data-stu-id="0bbae-197">Click Print test.</span></span>
23. <span data-ttu-id="0bbae-198">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bbae-198">Click OK.</span></span>
    * <span data-ttu-id="0bbae-199">Gennemse det oprettede output.</span><span class="sxs-lookup"><span data-stu-id="0bbae-199">Review the created output.</span></span> <span data-ttu-id="0bbae-200">Outputtet er oprettet som et Word-dokument med integrerede billeder, der viser firmaets logo, en autoriseret persons signatur og den markerede tekst i vandmærket.</span><span class="sxs-lookup"><span data-stu-id="0bbae-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]