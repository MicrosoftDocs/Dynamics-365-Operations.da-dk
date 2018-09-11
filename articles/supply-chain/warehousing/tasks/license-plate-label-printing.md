--- 
title: Aktivere udskrivning af nummerpladeetiket
description: Denne procedure aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk.
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d562e3a757ed0d8dd0ccc88119cfaadb7d8e1c1f
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="12fec-103">Aktivere udskrivning af nummerpladeetiket</span><span class="sxs-lookup"><span data-stu-id="12fec-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12fec-104">Denne procedure aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk.</span><span class="sxs-lookup"><span data-stu-id="12fec-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="12fec-105">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="12fec-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="12fec-106">Hvis du vil køre den med dine egne data, skal du have en nummerserie defineret for id'er.</span><span class="sxs-lookup"><span data-stu-id="12fec-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="12fec-107">Du skal konfigurere en etiketprinter, før du begynder denne opgave.</span><span class="sxs-lookup"><span data-stu-id="12fec-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="12fec-108">Gå til Virksomhedsadministration > Opsætning > Netværksprintere.</span><span class="sxs-lookup"><span data-stu-id="12fec-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="12fec-109">I handlingsruden skal du klikke på indstillinger og derefter klikke på knappen til Download-installationsprogram for dokumentets ruteplanlægningsagent.</span><span class="sxs-lookup"><span data-stu-id="12fec-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="12fec-110">Kør installationsprogrammet, og sørg for, at du har en fungerende netværksprinter, der er aktiveret, før du fortsætter med proceduren.</span><span class="sxs-lookup"><span data-stu-id="12fec-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="12fec-111">Angiv GS1-virksomhedspræfikset</span><span class="sxs-lookup"><span data-stu-id="12fec-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="12fec-112">Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="12fec-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="12fec-113">Indtast de 7 tal for dit GS1-virksomhedsnummer i feltet til GS1-firmapræfikset.</span><span class="sxs-lookup"><span data-stu-id="12fec-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="12fec-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-114">Click Save.</span></span>
4. <span data-ttu-id="12fec-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="12fec-116">Konfigurer SSCC-id-sekvensen</span><span class="sxs-lookup"><span data-stu-id="12fec-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="12fec-117">Gå til Virksomhedsadministration > Nummerserier > Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="12fec-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="12fec-118">Vælg en indstilling i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="12fec-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="12fec-119">Vælg en indstilling i feltet Reference.</span><span class="sxs-lookup"><span data-stu-id="12fec-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="12fec-120">Skriv en værdi i feltet Firma.</span><span class="sxs-lookup"><span data-stu-id="12fec-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="12fec-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="12fec-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="12fec-123">Udvid sektionen Segmenter.</span><span class="sxs-lookup"><span data-stu-id="12fec-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="12fec-124">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="12fec-124">Click Edit.</span></span>
9. <span data-ttu-id="12fec-125">Markér den første række i tabellen Segmenter</span><span class="sxs-lookup"><span data-stu-id="12fec-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="12fec-126">Klik på Fjern.</span><span class="sxs-lookup"><span data-stu-id="12fec-126">Click Remove.</span></span>
11. <span data-ttu-id="12fec-127">Klik på Fjern.</span><span class="sxs-lookup"><span data-stu-id="12fec-127">Click Remove.</span></span>
12. <span data-ttu-id="12fec-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-128">Click Save.</span></span>
13. <span data-ttu-id="12fec-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="12fec-130">Opret dokumentrutelayoutet</span><span class="sxs-lookup"><span data-stu-id="12fec-130">Create the document route layout</span></span>
1. <span data-ttu-id="12fec-131">Gå til Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrutelayout.</span><span class="sxs-lookup"><span data-stu-id="12fec-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="12fec-132">Aktivér SSCC-layoutet.</span><span class="sxs-lookup"><span data-stu-id="12fec-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="12fec-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12fec-133">Click New.</span></span>
3. <span data-ttu-id="12fec-134">Indtast en værdi i feltet Layout-id.</span><span class="sxs-lookup"><span data-stu-id="12fec-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="12fec-135">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12fec-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="12fec-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="12fec-137">Klik på Indsæt i slutningen af teksten.</span><span class="sxs-lookup"><span data-stu-id="12fec-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="12fec-138">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-138">Click Save.</span></span>
8. <span data-ttu-id="12fec-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="12fec-140">Konfigurer dokumentruten</span><span class="sxs-lookup"><span data-stu-id="12fec-140">Set up the document routing</span></span>
1. <span data-ttu-id="12fec-141">Gå til Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrute.</span><span class="sxs-lookup"><span data-stu-id="12fec-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="12fec-142">Vælg en indstilling i feltet Arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="12fec-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="12fec-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12fec-143">Click New.</span></span>
4. <span data-ttu-id="12fec-144">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="12fec-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="12fec-145">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="12fec-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="12fec-146">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12fec-146">Click New.</span></span>
7. <span data-ttu-id="12fec-147">Indtast eller vælg en værdi i feltet Layout-id.</span><span class="sxs-lookup"><span data-stu-id="12fec-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="12fec-148">Vælg det printernavn, du vil bruge, i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="12fec-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="12fec-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-149">Click Save.</span></span>
10. <span data-ttu-id="12fec-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="12fec-151">Opret menu til mobilenhed</span><span class="sxs-lookup"><span data-stu-id="12fec-151">Create mobile device menu</span></span>
1. <span data-ttu-id="12fec-152">Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="12fec-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="12fec-153">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12fec-153">Click New.</span></span>
3. <span data-ttu-id="12fec-154">Skriv en værdi i feltet Menupunktnavn.</span><span class="sxs-lookup"><span data-stu-id="12fec-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="12fec-155">Skriv en værdi i feltet Titel.</span><span class="sxs-lookup"><span data-stu-id="12fec-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="12fec-156">Vælg en indstilling i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="12fec-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="12fec-157">Vælg Ja i feltet Brug eksisterende arbejde.</span><span class="sxs-lookup"><span data-stu-id="12fec-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="12fec-158">Vælg Ja i feltet Generér id.</span><span class="sxs-lookup"><span data-stu-id="12fec-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="12fec-159">Udvid sektionen Arbejdsklasser.</span><span class="sxs-lookup"><span data-stu-id="12fec-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="12fec-160">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12fec-160">Click New.</span></span>
10. <span data-ttu-id="12fec-161">Skriv en værdi i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="12fec-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="12fec-162">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-162">Click Save.</span></span>
12. <span data-ttu-id="12fec-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-163">Close the page.</span></span>
13. <span data-ttu-id="12fec-164">Gå til Lagerstedsstyring > Opsætning > Mobilenhed > Menu i mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="12fec-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="12fec-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="12fec-166">Vælg i træet "Vælg det menupunkt, du oprettede før, i træet".</span><span class="sxs-lookup"><span data-stu-id="12fec-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="12fec-167">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="12fec-167">Click Edit.</span></span>
17. <span data-ttu-id="12fec-168">Klik på pilen for at føje menupunktet til menuen.</span><span class="sxs-lookup"><span data-stu-id="12fec-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="12fec-169">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-169">Click Save.</span></span>
19. <span data-ttu-id="12fec-170">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="12fec-171">Opdater en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="12fec-171">Update a work template</span></span>
1. <span data-ttu-id="12fec-172">Gå til Lagerstedsstyring > Opsætning > Arbejde > Arbejdsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="12fec-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="12fec-173">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="12fec-174">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="12fec-174">Click Edit.</span></span>
4. <span data-ttu-id="12fec-175">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="12fec-175">Click New.</span></span>
5. <span data-ttu-id="12fec-176">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="12fec-177">Vælg "Udskriv" i feltet Arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="12fec-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="12fec-178">Indtast eller vælg en værdi i feltet Arbejdsklasse-id.</span><span class="sxs-lookup"><span data-stu-id="12fec-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="12fec-179">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12fec-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="12fec-180">Klik på Flyt op.</span><span class="sxs-lookup"><span data-stu-id="12fec-180">Click Move up.</span></span>
10. <span data-ttu-id="12fec-181">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="12fec-181">Click Save.</span></span>
11. <span data-ttu-id="12fec-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="12fec-182">Close the page.</span></span>


