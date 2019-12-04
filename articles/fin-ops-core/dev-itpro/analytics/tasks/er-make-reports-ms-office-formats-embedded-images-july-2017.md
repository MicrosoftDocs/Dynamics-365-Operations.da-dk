---
title: Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder
description: Trinnene i dette emne giver dig oplysninger om, hvordan du designer elektroniske rapporteringskonfigurationer (ER), der genererer elektroniske dokumenter i Microsoft Office-formater (Excel og Word), der indeholder integrerede billeder.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143782413359d87f3d4c46940f9a699fbf0e8f90
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769803"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="5c566-103">Designe konfigurationer til at generere rapporter i Office-format, der har integrerede billeder</span><span class="sxs-lookup"><span data-stu-id="5c566-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c566-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="5c566-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="5c566-105">Denne procedure forklarer, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere et Microsoft Excel- og Word-dokument, der indeholder integrerede billeder.</span><span class="sxs-lookup"><span data-stu-id="5c566-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="5c566-106">I denne procedure, skal du oprette de nødvendige ER konfigurationer for eksempelvirksomheden Litware, Inc. Disse trin kan udføres ved hjælp af USMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="5c566-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="5c566-107">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="5c566-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="5c566-108">Før du går i gang, skal du hente og gemme filerne, der er vist i Hjælp-emnet [Integrer billeder og figurer i dokumenter, du har genereret ved hjælp af ER](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="5c566-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="5c566-109">Filerne er: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="5c566-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="5c566-110">Kontrollere forudsætninger</span><span class="sxs-lookup"><span data-stu-id="5c566-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="5c566-111">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5c566-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="5c566-112">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="5c566-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="5c566-113">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Oprette en konfigurationsudbyder og markere den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="5c566-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="5c566-114">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="5c566-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="5c566-115">Tilføj en ny ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5c566-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="5c566-116">I stedet for at oprette en ny model, kan du indlæse ER-modellens konfigurationsfil (Model for checks.xml), som du har gemt tidligere.</span><span class="sxs-lookup"><span data-stu-id="5c566-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="5c566-117">Denne fil indeholder eksempeldatamodellen for checkbetaling og tilknytning af datamodellen til datakomponenterne i Dynamics 365 for Operations-programmet.</span><span class="sxs-lookup"><span data-stu-id="5c566-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="5c566-118">Klik på Udveksling i oversigtspanelet Versioner.</span><span class="sxs-lookup"><span data-stu-id="5c566-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="5c566-119">Klik på Indlæs fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="5c566-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="5c566-120">Klik på Gennemse, og vælg derefter Model for checks.xml.</span><span class="sxs-lookup"><span data-stu-id="5c566-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="5c566-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c566-121">Click OK.</span></span>  
 6. <span data-ttu-id="5c566-122">Den indlæste model bruges som datakilde for oplysninger til at oprette dokumenter, der indeholder billeder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="5c566-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="5c566-123">Tilføje en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5c566-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="5c566-124">I stedet for at oprette er nyt format, kan du indlæse ER-formatets konfigurationsfil (Checkudskrivningsformat.xml), som du har gemt tidligere.</span><span class="sxs-lookup"><span data-stu-id="5c566-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="5c566-125">Denne fil indeholder prøvelayoutet af formatet til udskrivning af checks ved hjælp af den fortrykte formular og tilknytningen af dette format til datamodellen 'Model for checks'.</span><span class="sxs-lookup"><span data-stu-id="5c566-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="5c566-126">Klik på Udveksling.</span><span class="sxs-lookup"><span data-stu-id="5c566-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="5c566-127">Klik på Indlæs fra XML-fil.</span><span class="sxs-lookup"><span data-stu-id="5c566-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="5c566-128">Klik på Gennemse, og vælg Checkudskrivningsformat.xml-filen.</span><span class="sxs-lookup"><span data-stu-id="5c566-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="5c566-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c566-129">Click OK.</span></span>  
 6. <span data-ttu-id="5c566-130">Udvid 'Model for checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c566-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="5c566-131">Vælg 'Model for checks\Checkudskrivningsformat' i træet.</span><span class="sxs-lookup"><span data-stu-id="5c566-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="5c566-132">Det indlæste format bruges til at oprette dokumenter, der indeholder billeder i Excel og Word.</span><span class="sxs-lookup"><span data-stu-id="5c566-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="5c566-133">Konfigurere ER-brugerparametre</span><span class="sxs-lookup"><span data-stu-id="5c566-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="5c566-134">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5c566-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="5c566-135">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="5c566-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="5c566-136">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="5c566-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="5c566-137">Aktivér flaget 'Udkast til kørsel' for at starte kladdeversionen af det valgte format i stedet for den, der er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="5c566-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="5c566-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5c566-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="5c566-139">Konfigurerer Likviditets- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="5c566-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="5c566-140">Gå til Kontant- og bankstyring > Bankkonti > Bankkonti.</span><span class="sxs-lookup"><span data-stu-id="5c566-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="5c566-141">Brug Quick Filter til at filtrere på feltet Bankkonto med værdien "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="5c566-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="5c566-142">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5c566-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="5c566-143">Klik på Kontroller.</span><span class="sxs-lookup"><span data-stu-id="5c566-143">Click Check.</span></span>  
 5. <span data-ttu-id="5c566-144">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c566-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="5c566-145">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="5c566-145">Click Edit.</span></span>  
 7. <span data-ttu-id="5c566-146">Vælg Ja i feltet Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="5c566-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="5c566-147">Klik på Firmalogo.</span><span class="sxs-lookup"><span data-stu-id="5c566-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="5c566-148">Klik på Skift.</span><span class="sxs-lookup"><span data-stu-id="5c566-148">Click Change.</span></span>  
 10. <span data-ttu-id="5c566-149">Klik på Gennemse, og vælg den fil, du tidligere har hentet, Firmalogo.png.</span><span class="sxs-lookup"><span data-stu-id="5c566-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="5c566-150">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5c566-150">Click Save.</span></span>  
 12. <span data-ttu-id="5c566-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c566-151">Close the page.</span></span>  
 13. <span data-ttu-id="5c566-152">Udvid sektionen Signatur.</span><span class="sxs-lookup"><span data-stu-id="5c566-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="5c566-153">Vælg Ja i feltet Udskriv første underskrift.</span><span class="sxs-lookup"><span data-stu-id="5c566-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="5c566-154">Klik på Skift.</span><span class="sxs-lookup"><span data-stu-id="5c566-154">Click Change.</span></span>  
 16. <span data-ttu-id="5c566-155">Klik på Gennemse, og vælg den fil, du tidligere har hentet, Signaturbillede.png.</span><span class="sxs-lookup"><span data-stu-id="5c566-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="5c566-156">Udvid sektionen Kopier.</span><span class="sxs-lookup"><span data-stu-id="5c566-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="5c566-157">Vælg en indstilling i feltet Vandmærke.</span><span class="sxs-lookup"><span data-stu-id="5c566-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="5c566-158">Vælg Ja i feltet Generisk elektronisk eksportformat.</span><span class="sxs-lookup"><span data-stu-id="5c566-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="5c566-159">Vælg konfiguration af 'Checkudskrivningsformat'.</span><span class="sxs-lookup"><span data-stu-id="5c566-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="5c566-160">Det valgte ER-format bliver nu brugt til udskrivning af checks.</span><span class="sxs-lookup"><span data-stu-id="5c566-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="5c566-161">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="5c566-161">Click Attach.</span></span>  
 23. <span data-ttu-id="5c566-162">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5c566-162">Click New.</span></span>  
 24. <span data-ttu-id="5c566-163">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="5c566-163">Click File.</span></span>  
 25. <span data-ttu-id="5c566-164">Klik på Gennemse, og vælg den fil, du tidligere har hentet, Signaturbillede 2.png.</span><span class="sxs-lookup"><span data-stu-id="5c566-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="5c566-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c566-165">Close the page.</span></span>  
 27. <span data-ttu-id="5c566-166">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c566-166">Close the page.</span></span>  
 28. <span data-ttu-id="5c566-167">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c566-167">Close the page.</span></span>  
 29. <span data-ttu-id="5c566-168">Gå til Kontant- og bankstyring > Opsætning > Kontant- og bankstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="5c566-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="5c566-169">Vælg Ja i feltet Tillad oprettelse af adviseringer for inaktive bankkonti:</span><span class="sxs-lookup"><span data-stu-id="5c566-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="5c566-170">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5c566-170">Click Save.</span></span>  
 32. <span data-ttu-id="5c566-171">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5c566-171">Close the page.</span></span>  
