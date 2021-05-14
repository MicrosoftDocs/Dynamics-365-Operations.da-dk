---
title: Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder
description: Dette emne beskriver, hvordan du designer konfigurationer for at generere elektroniske dokumenter i Excel- og Word-format, der indeholder integrerede billeder.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944551"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="f1eb0-103">Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder</span><span class="sxs-lookup"><span data-stu-id="f1eb0-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1eb0-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="f1eb0-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="f1eb0-105">Denne procedure forklarer, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere et Microsoft Excel- og Word-dokument, der indeholder integrerede billeder.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="f1eb0-106">I denne procedure, skal du oprette de nødvendige ER konfigurationer for eksempelvirksomheden Litware, Inc. Disse trin kan udføres ved hjælp af USMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="f1eb0-107">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="f1eb0-108">Før du begynder, skal du hente og gemme følgende filer:</span><span class="sxs-lookup"><span data-stu-id="f1eb0-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="f1eb0-109">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f1eb0-109">Description</span></span>                                          | <span data-ttu-id="f1eb0-110">Filnavn</span><span class="sxs-lookup"><span data-stu-id="f1eb0-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="f1eb0-111">ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1eb0-111">ER data model configuration</span></span>                          | [<span data-ttu-id="f1eb0-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="f1eb0-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="f1eb0-113">Konfiguration af ER-format</span><span class="sxs-lookup"><span data-stu-id="f1eb0-113">ER format configuration</span></span>                              | [<span data-ttu-id="f1eb0-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="f1eb0-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="f1eb0-115">Billede af firmalogo</span><span class="sxs-lookup"><span data-stu-id="f1eb0-115">Company logo image</span></span>                                   | [<span data-ttu-id="f1eb0-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="f1eb0-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="f1eb0-117">Signaturbillede</span><span class="sxs-lookup"><span data-stu-id="f1eb0-117">Signature image</span></span>                                      | [<span data-ttu-id="f1eb0-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="f1eb0-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="f1eb0-119">Alternativt signaturbillede</span><span class="sxs-lookup"><span data-stu-id="f1eb0-119">Alternative signature image</span></span>                          | [<span data-ttu-id="f1eb0-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="f1eb0-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="f1eb0-121">Microsoft Word-skabelon til udskrivning af betalingschecks</span><span class="sxs-lookup"><span data-stu-id="f1eb0-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="f1eb0-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="f1eb0-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="f1eb0-123">Kontrollere forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f1eb0-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="f1eb0-124">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="f1eb0-125">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="f1eb0-126">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="f1eb0-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="f1eb0-127">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="f1eb0-128">Tilføj en ny ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1eb0-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="f1eb0-129">I stedet for at oprette en ny model, kan du indlæse ER-modellens konfigurationsfil (Model for checks.xml), som du har gemt tidligere.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="f1eb0-130">Denne fil indeholder eksempeldatamodellen for checkbetaling og tilknytning af datamodellen til datakomponenterne i Dynamics 365 for Operations-programmet.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="f1eb0-131">Klik på Udveksling i oversigtspanelet Versioner.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="f1eb0-132">Klik på Indlæs fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="f1eb0-133">Klik på Gennemse, og vælg derefter Model for checks.xml.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="f1eb0-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-134">Click OK.</span></span>  
 6. <span data-ttu-id="f1eb0-135">Den indlæste model bruges som datakilde for oplysninger til at oprette dokumenter, der indeholder billeder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="f1eb0-136">Tilføje en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1eb0-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="f1eb0-137">I stedet for at oprette er nyt format, kan du indlæse ER-formatets konfigurationsfil (Checkudskrivningsformat.xml), som du har gemt tidligere.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="f1eb0-138">Denne fil indeholder prøvelayoutet af formatet til udskrivning af checks ved hjælp af den fortrykte formular og tilknytningen af dette format til datamodellen 'Model for checks'.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="f1eb0-139">Klik på Udveksling.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="f1eb0-140">Klik på Indlæs fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="f1eb0-141">Klik på Gennemse, og vælg Checkudskrivningsformat.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="f1eb0-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-142">Click OK.</span></span>  
 6. <span data-ttu-id="f1eb0-143">Udvid 'Model for checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="f1eb0-144">Vælg 'Model for checks\Checkudskrivningsformat' i træet.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="f1eb0-145">Det indlæste format bruges til at oprette dokumenter, der indeholder billeder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="f1eb0-146">Konfigurere ER-brugerparametre</span><span class="sxs-lookup"><span data-stu-id="f1eb0-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="f1eb0-147">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="f1eb0-148">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="f1eb0-149">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="f1eb0-150">Aktivér flaget 'Udkast til kørsel' for at starte kladdeversionen af det valgte format i stedet for den, der er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="f1eb0-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="f1eb0-152">Konfigurerer Likviditets- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="f1eb0-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="f1eb0-153">Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="f1eb0-154">Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="f1eb0-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="f1eb0-155">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="f1eb0-156">Klik på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-156">Click Check.</span></span>  
 5. <span data-ttu-id="f1eb0-157">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="f1eb0-158">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-158">Click Edit.</span></span>  
 7. <span data-ttu-id="f1eb0-159">Vælg Ja i feltet Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="f1eb0-160">Klik på Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="f1eb0-161">Klik på Skift.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-161">Click Change.</span></span>  
 10. <span data-ttu-id="f1eb0-162">Klik på Gennemse, og vælg den fil, du tidligere har hentet, Firmalogo.png.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="f1eb0-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-163">Click Save.</span></span>  
 12. <span data-ttu-id="f1eb0-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-164">Close the page.</span></span>  
 13. <span data-ttu-id="f1eb0-165">Udvid sektionen Signatur.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="f1eb0-166">Vælg Ja i feltet Udskriv første underskrift.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="f1eb0-167">Klik på Skift.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-167">Click Change.</span></span>  
 16. <span data-ttu-id="f1eb0-168">Klik på Gennemse, og vælg den fil, du tidligere har hentet, Signaturbillede.png.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="f1eb0-169">Udvid sektionen Kopier.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="f1eb0-170">Vælg en indstilling i feltet Vandmærke.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="f1eb0-171">Vælg Ja i feltet Generisk elektronisk eksportformat.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="f1eb0-172">Vælg konfiguration af 'Checkudskrivningsformat'.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="f1eb0-173">Det valgte ER-format bliver nu brugt til udskrivning af checks.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="f1eb0-174">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-174">Click Attach.</span></span>  
 23. <span data-ttu-id="f1eb0-175">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-175">Click New.</span></span>  
 24. <span data-ttu-id="f1eb0-176">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-176">Click File.</span></span>  
 25. <span data-ttu-id="f1eb0-177">Klik på Gennemse, og vælg den fil, du tidligere har hentet, Signaturbillede 2.png.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="f1eb0-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-178">Close the page.</span></span>  
 27. <span data-ttu-id="f1eb0-179">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-179">Close the page.</span></span>  
 28. <span data-ttu-id="f1eb0-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-180">Close the page.</span></span>  
 29. <span data-ttu-id="f1eb0-181">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="f1eb0-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="f1eb0-182">Vælg Ja i feltet Tillad oprettelse af adviseringer for inaktive bankkonti:</span><span class="sxs-lookup"><span data-stu-id="f1eb0-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="f1eb0-183">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-183">Click Save.</span></span>  
 32. <span data-ttu-id="f1eb0-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1eb0-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
