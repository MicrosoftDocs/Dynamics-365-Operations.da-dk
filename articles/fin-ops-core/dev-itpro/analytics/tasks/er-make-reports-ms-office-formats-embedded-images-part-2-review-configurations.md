---
title: Gennemgå konfigurationer til at generere rapporter i Office-format, der har integrerede billeder
description: For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "ER Oprette rapporter i Microsoft Office-formater med integrerede billeder (Del 1 - Konfigurere parametre)".
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 9d05020c5b83137d977d7260e269cb7d8c219406
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184778"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="ec534-103">Gennemgå konfigurationer til at generere rapporter i Office-format, der har integrerede billeder</span><span class="sxs-lookup"><span data-stu-id="ec534-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec534-104">For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "ER Oprette rapporter i Microsoft Office-formater med integrerede billeder (Del 1: Konfigurere parametre)".</span><span class="sxs-lookup"><span data-stu-id="ec534-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="ec534-105">Denne procedure viser, hvordan du designer elektroniske rapporteringskonfigurationer (ER) for at generere elektroniske dokumenter, der indeholder integrerede billeder i Microsoft Excel og Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="ec534-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="ec534-106">I dette eksempel skal du gennemse ER-konfigurationer for eksempelfirmaet Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="ec534-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="ec534-107">Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="ec534-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="ec534-108">Trinnene kan udføres ved hjælp af USMF datasættet.</span><span class="sxs-lookup"><span data-stu-id="ec534-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="ec534-109">Gennemse den importerede datamodel</span><span class="sxs-lookup"><span data-stu-id="ec534-109">Review the imported data model</span></span>
1. <span data-ttu-id="ec534-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="ec534-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ec534-111">Vælg 'Model for checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="ec534-112">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="ec534-112">Click Designer.</span></span>
    * <span data-ttu-id="ec534-113">Denne model er udviklet til at repræsentere betalingschecks fra en forretningsmæssig betragtning og tilknytningen af denne model til programmets datakilder.</span><span class="sxs-lookup"><span data-stu-id="ec534-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="ec534-114">Gennemse denne model ved hjælp af ER Operations-designeren.</span><span class="sxs-lookup"><span data-stu-id="ec534-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="ec534-115">Bemærk, at attributterne for de modelelementer, der præsenteres: struktur, navn, beskrivelse, datatype og så videre.</span><span class="sxs-lookup"><span data-stu-id="ec534-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="ec534-116">Udvid 'root' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="ec534-117">Vælg 'rod\checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="ec534-118">Udvid 'rod\checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="ec534-119">Udvid 'rod\checks\attributter' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="ec534-120">Udvid 'rod\indbetaler' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="ec534-121">Vælg 'rod\istestrun' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="ec534-122">Vælg 'rod\layout' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="ec534-123">Layoutelementet for denne model repræsenterer detaljerede oplysninger om udskrivning af checkformularlayoutet for den valgte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ec534-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="ec534-124">Den indeholder også to noder af datatypen Container til lagring af billeder.</span><span class="sxs-lookup"><span data-stu-id="ec534-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="ec534-125">Udvid 'rod\layout' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="ec534-126">Vælg 'rod\layout\firmalogo' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="ec534-127">Vælg 'rod\layout\firmalogo' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="ec534-128">Vælg 'rod\layout\firmalogo\billede' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="ec534-129">Vælg 'rod\layout\firmalogo\isprinted' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="ec534-130">Vælg 'rod\layout\signatur' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="ec534-131">Udvid 'rod\layout\signatur' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="ec534-132">Vælg 'rod\layout\signatur\billede' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="ec534-133">Vælg 'rod\layout\signatur\isprinted' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="ec534-134">Bemærk, at de to billeddatamodelelementer er bundet til felterne i de tabeller, der indeholder billeder af firmaets logo og den autoriserede persons signatur i binært format.</span><span class="sxs-lookup"><span data-stu-id="ec534-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="ec534-135">Udvid 'rod\layout\vandmærke' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="ec534-136">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="ec534-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="ec534-137">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="ec534-137">Click Designer.</span></span>
23. <span data-ttu-id="ec534-138">Udvid 'chequesselected' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="ec534-139">Udvid 'layout' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="ec534-140">Vælg 'layout\firmalogo' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="ec534-141">Udvid 'layout\signatur' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="ec534-142">Udvid 'layout\vandmærke' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="ec534-143">Slå "Vis detaljer" til.</span><span class="sxs-lookup"><span data-stu-id="ec534-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="ec534-144">Bemærk, at checkdatamodelelementet er bundet til tabellen TmpChequePrintout, der på kørselstidspunktet indeholder poster for checks, som brugeren har valgt til udskrivning.</span><span class="sxs-lookup"><span data-stu-id="ec534-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="ec534-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec534-145">Close the page.</span></span>
30. <span data-ttu-id="ec534-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec534-146">Close the page.</span></span>
31. <span data-ttu-id="ec534-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec534-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="ec534-148">Gennemse det importerede format</span><span class="sxs-lookup"><span data-stu-id="ec534-148">Review the imported format</span></span>
1. <span data-ttu-id="ec534-149">Udvid 'Model for checks' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="ec534-150">Vælg 'Model for checks\Checkudskrivningsformat' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="ec534-151">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="ec534-151">Click Designer.</span></span>
4. <span data-ttu-id="ec534-152">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="ec534-152">Click Attachments.</span></span>
5. <span data-ttu-id="ec534-153">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="ec534-153">Click Open.</span></span>
    * <span data-ttu-id="ec534-154">Åbn den vedhæftede rapports skabelon i Excel.</span><span class="sxs-lookup"><span data-stu-id="ec534-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="ec534-155">Gennemse den vedhæftede rapports Excel-skabelon, der skal bruges til at udskrive checks.</span><span class="sxs-lookup"><span data-stu-id="ec534-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="ec534-156">Skabelonen indeholder to checks pr. side og er designet til at udskrive checks til den fortrykte formular.</span><span class="sxs-lookup"><span data-stu-id="ec534-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="ec534-157">Bemærk, at to tomme billeder er integreret.</span><span class="sxs-lookup"><span data-stu-id="ec534-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="ec534-158">Disse tomme billeder er beregnet til firmalogoet og signaturen fra den person, der godkender en betaling.</span><span class="sxs-lookup"><span data-stu-id="ec534-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="ec534-159">Kontroller, at billederne hedder henholdsvis CompLogo og SignatureImage i Excel.</span><span class="sxs-lookup"><span data-stu-id="ec534-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="ec534-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec534-160">Close the page.</span></span>
7. <span data-ttu-id="ec534-161">Udvid 'Rapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="ec534-162">Udvid 'Rapport\ChequeLines' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="ec534-163">Vælg 'Rapport\ChequeLines\CompLogo' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="ec534-164">Slå "Vis detaljer" til.</span><span class="sxs-lookup"><span data-stu-id="ec534-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="ec534-165">Bemærk, at celleelementet for formatet 'CompLogo' repræsenterer det Excel-element, der bruges til at udfylde feltet med firmalogobilledet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="ec534-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="ec534-166">Dette formatelement er bundet til det billeddatamodelelement, der på kørselstidspunktet indeholder et billede af firmalogoet i binært format.</span><span class="sxs-lookup"><span data-stu-id="ec534-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="ec534-167">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ec534-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="ec534-168">Klik på Rediger aktiveret.</span><span class="sxs-lookup"><span data-stu-id="ec534-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="ec534-169">Bemærk, at du kan ændre celleelementet for formatet 'CompLogo', så det ikke længere er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="ec534-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="ec534-170">I så fald skjuler det tilknyttede Excel-billedelement et firmalogo i den genererede rapport.</span><span class="sxs-lookup"><span data-stu-id="ec534-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="ec534-171">Hvis det aktiverede udtryk returnerer TRUE, og den definerede binding ikke viser et billede, viser det tilknyttede Excel-billedelement et billede, der er gemt i Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="ec534-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="ec534-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec534-172">Close the page.</span></span>
14. <span data-ttu-id="ec534-173">Udvid 'labels: Container' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec534-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="ec534-174">Nogle etiketter, der vises i den fortrykte checkformular, medtages i rapporten, når den oprettes til testformål.</span><span class="sxs-lookup"><span data-stu-id="ec534-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="ec534-175">Disse etiketter udskrives dog ikke under den egentlige udskrivning, fordi den fortrykte formular allerede indeholder dem.</span><span class="sxs-lookup"><span data-stu-id="ec534-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="ec534-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec534-176">Close the page.</span></span>

