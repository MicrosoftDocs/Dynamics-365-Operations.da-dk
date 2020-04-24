---
title: Aktivere udskrivning af id-etiket
description: Dette emne viser, hvordan du aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 484a1465dd41429fe201de18aac55f118a483cab
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217005"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="c89e1-103">Aktivere udskrivning af id-etiket</span><span class="sxs-lookup"><span data-stu-id="c89e1-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c89e1-104">Dette emne viser, hvordan du aktiverer automatisk udskrivning af en SSCC-etiket (Serial Shipping Container Code), efter at sidste vare er plukket fra lager i en arbejdsproces til salgspluk.</span><span class="sxs-lookup"><span data-stu-id="c89e1-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="c89e1-105">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="c89e1-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="c89e1-106">Hvis du vil køre den med dine egne data, skal du have en nummerserie defineret for id'er.</span><span class="sxs-lookup"><span data-stu-id="c89e1-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="c89e1-107">Du skal konfigurere en etiketprinter, før du begynder denne opgave.</span><span class="sxs-lookup"><span data-stu-id="c89e1-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="c89e1-108">Gå til Virksomhedsadministration > Opsætning > Netværksprintere.</span><span class="sxs-lookup"><span data-stu-id="c89e1-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="c89e1-109">I handlingsruden skal du klikke på indstillinger og derefter klikke på knappen til Download-installationsprogram for dokumentets ruteplanlægningsagent.</span><span class="sxs-lookup"><span data-stu-id="c89e1-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="c89e1-110">Kør installationsprogrammet, og sørg for, at du har en fungerende netværksprinter, der er aktiveret, før du fortsætter med proceduren.</span><span class="sxs-lookup"><span data-stu-id="c89e1-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="c89e1-111">Angiv GS1-virksomhedspræfikset</span><span class="sxs-lookup"><span data-stu-id="c89e1-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="c89e1-112">Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Parametre til lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="c89e1-113">Indtast de 7 tal for dit GS1-firmanummer i feltet **GS1-firmapræfiks**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="c89e1-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-114">Select **Save**.</span></span>
4. <span data-ttu-id="c89e1-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="c89e1-116">Konfigurer SSCC-id-nummersekvensen</span><span class="sxs-lookup"><span data-stu-id="c89e1-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="c89e1-117">Gå til **Navigationsrude > Moduler > Organisationsadministration > Nummerserier > Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="c89e1-118">Vælg en indstilling i feltet **Område**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="c89e1-119">Vælg en indstilling i feltet **Reference**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="c89e1-120">Skriv en værdi i feltet **Firma**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="c89e1-121">Udvid sektionen **Segmenter**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="c89e1-122">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-122">Select **Edit**.</span></span>
7. <span data-ttu-id="c89e1-123">Markér den første række i tabellen **Segmenter**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="c89e1-124">Vælg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-124">Select **Remove**.</span></span>
9. <span data-ttu-id="c89e1-125">Vælg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-125">Select **Remove**.</span></span>
10. <span data-ttu-id="c89e1-126">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-126">Select **Save**.</span></span>
11. <span data-ttu-id="c89e1-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="c89e1-128">Opret dokumentrutelayoutet</span><span class="sxs-lookup"><span data-stu-id="c89e1-128">Create the document route layout</span></span>
1. <span data-ttu-id="c89e1-129">Gå til **Navigationsrude > Moduler > Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrutelayout**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="c89e1-130">Aktivér SSCC-layoutet.</span><span class="sxs-lookup"><span data-stu-id="c89e1-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="c89e1-131">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-131">Select **New**.</span></span>
3. <span data-ttu-id="c89e1-132">Indtast en værdi i feltet **Layout-id**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="c89e1-133">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c89e1-134">Vælg **Indsæt i slutningen af tekst**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="c89e1-135">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-135">Select **Save**.</span></span>
7. <span data-ttu-id="c89e1-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="c89e1-137">Konfigurer dokumentruten</span><span class="sxs-lookup"><span data-stu-id="c89e1-137">Set up the document routing</span></span>
1. <span data-ttu-id="c89e1-138">Gå til **Navigationsrude > Moduler > Lagerstedsstyring > Opsætning > Dokumentrute > Dokumentrute**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="c89e1-139">Vælg en indstilling i feltet **Arbejdsordretype**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="c89e1-140">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-140">Select **New**.</span></span>
4. <span data-ttu-id="c89e1-141">Skriv en værdi i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="c89e1-142">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="c89e1-143">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-143">Select **New**.</span></span>
7. <span data-ttu-id="c89e1-144">Indtast eller vælg en værdi i feltet **Layout-id**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="c89e1-145">Angiv det printernavn, du vil bruge, i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="c89e1-146">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-146">Select **Save**.</span></span>
10. <span data-ttu-id="c89e1-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="c89e1-148">Opret menu til mobilenhed</span><span class="sxs-lookup"><span data-stu-id="c89e1-148">Create mobile device menu</span></span>
1. <span data-ttu-id="c89e1-149">Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="c89e1-150">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-150">Select **New**.</span></span>
3. <span data-ttu-id="c89e1-151">Skriv en værdi i feltet **Menupunktnavn**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="c89e1-152">Skriv en værdi i feltet **Titel**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="c89e1-153">Vælg en indstilling i feltet **Tilstand**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="c89e1-154">Vælg **Ja** i feltet **Brug eksisterende arbejde**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="c89e1-155">Vælg **Ja** i feltet **Generér id**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="c89e1-156">Udvid sektionen **Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="c89e1-157">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-157">Select **New**.</span></span>
10. <span data-ttu-id="c89e1-158">Skriv en værdi i feltet **Arbejdsklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="c89e1-159">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-159">Select **Save**.</span></span>
12. <span data-ttu-id="c89e1-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-160">Close the page.</span></span>
13. <span data-ttu-id="c89e1-161">Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Mobilenhed > Menu i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="c89e1-162">Vælg det menupunkt, du tidligere har oprettet, i træet.</span><span class="sxs-lookup"><span data-stu-id="c89e1-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="c89e1-163">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-163">Select **Edit**.</span></span>
16. <span data-ttu-id="c89e1-164">Vælg pilen for at tilføje menupunktet i menuen.</span><span class="sxs-lookup"><span data-stu-id="c89e1-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="c89e1-165">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-165">Select **Save**.</span></span>
18. <span data-ttu-id="c89e1-166">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="c89e1-167">Opdater en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="c89e1-167">Update a work template</span></span>
1. <span data-ttu-id="c89e1-168">Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Arbejde > Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="c89e1-169">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-169">Select **Edit**.</span></span>
3. <span data-ttu-id="c89e1-170">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-170">Select **New**.</span></span>
4. <span data-ttu-id="c89e1-171">Vælg **Udskriv** i feltet **Arbejdstype**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="c89e1-172">Indtast eller vælg en værdi i feltet **Arbejdsklasse-id**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="c89e1-173">Vælg **Flyt op**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-173">Select **Move up**.</span></span>
7. <span data-ttu-id="c89e1-174">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c89e1-174">Select **Save**.</span></span>
8. <span data-ttu-id="c89e1-175">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c89e1-175">Close the page.</span></span>

