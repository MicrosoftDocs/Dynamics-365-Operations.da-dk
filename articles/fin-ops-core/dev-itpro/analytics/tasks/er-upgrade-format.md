---
title: ER Opgradere dit format ved at bruge en ny basisversion af formatet
description: Dette emne forklarer, hvordan du vedligeholder en formatkonfiguration til elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 336551f4e9858269010ec7debd1750a8d8453163
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564236"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="77c02-103">ER Opgradere dit format ved at bruge en ny basisversion af formatet</span><span class="sxs-lookup"><span data-stu-id="77c02-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77c02-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan bevare en formatkonfiguration af elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="77c02-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="77c02-105">Denne fremgangsmåde forklarer, hvordan en brugerdefineret version af et format kan oprettes ud fra det format, der er modtaget fra konfigurationsudbyderen (CP).</span><span class="sxs-lookup"><span data-stu-id="77c02-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="77c02-106">Det forklares også, hvordan en ny basisversion af det pågældende format skal implementeres.</span><span class="sxs-lookup"><span data-stu-id="77c02-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="77c02-107">For at fuldføre denne fremgangsmåde, skal du først udføre trinnene i procedurerne "Oprette en konfigurationsudbyder og markere den som aktiv" og "Bruge oprettet format for at generere elektroniske dokumenter til betalinger".</span><span class="sxs-lookup"><span data-stu-id="77c02-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="77c02-108">Disse trin kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="77c02-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="77c02-109">Vælge formatkonfiguration, der skal tilpasses</span><span class="sxs-lookup"><span data-stu-id="77c02-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="77c02-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="77c02-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="77c02-111">I dette eksempel fungerer eksempelfirmaet Litware, Inc. (https://www.litware.com) som en konfigurationsudbyder, der understøtter formatkonfigurationer af elektroniske betalinger for et bestemt land/område.</span><span class="sxs-lookup"><span data-stu-id="77c02-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="77c02-112">Eksempelfirmaet Proseware, Inc. (http://www.proseware.com) vil fungere som en forbruger af den formatkonfiguration, som Litware, Inc har leveret.</span><span class="sxs-lookup"><span data-stu-id="77c02-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="77c02-113">Proseware, Inc. bruger formater i bestemte dele af det pågældende land/område.</span><span class="sxs-lookup"><span data-stu-id="77c02-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="77c02-114">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="77c02-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="77c02-115">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="77c02-115">Click Show filters.</span></span>
4. <span data-ttu-id="77c02-116">Anvend følgende filtre: Angiv filterværdien "BACS (UK-fiktiv)" i feltet "Navn" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="77c02-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="77c02-117">Den valgte BACS-formatkonfiguration (UK fiktivt brugerdefineret), som ejes af udbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="77c02-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="77c02-118">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="77c02-118">Click Show filters.</span></span>
6. <span data-ttu-id="77c02-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="77c02-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="77c02-120">Versionen af formatet med statussen Fuldført vil blive brugt af Proseware, Inc. til tilpasning.</span><span class="sxs-lookup"><span data-stu-id="77c02-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="77c02-121">Oprette en ny konfiguration af det brugerdefinerede format for elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="77c02-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="77c02-122">Proseware, Inc. modtog version 1.1 af BACS-konfigurationen (UK fiktiv), der indeholder det oprindelige format til oprettelse af elektroniske betalingsdokumenter fra Litware, Inc. i overensstemmelse med deres serviceabonnement.</span><span class="sxs-lookup"><span data-stu-id="77c02-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="77c02-123">Proseware, Inc. ønsker at begynde at bruge det som en standard for deres land/område, men nogle tilpasninger er påkrævet for at understøtte specifikke regionale krav.</span><span class="sxs-lookup"><span data-stu-id="77c02-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="77c02-124">Proseware, Inc. ønsker også at bevare muligheden for at opgradere et brugerdefineret format, så snart der kommer en ny version af det (med ændringer for at understøtte nye land/område-specifikke krav) fra Litware, Inc., og de ønsker at udføre denne opgradering med de laveste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="77c02-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="77c02-125">For at kunne gøre dette skal Proseware, Inc. oprette en konfiguration og bruge BACS-konfigurationen af Litware, Inc. (UK fiktiv) som udgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="77c02-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="77c02-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77c02-126">Close the page.</span></span>
2. <span data-ttu-id="77c02-127">Vælg Proseware, Inc., for at gøre den til en aktiv udbyder.</span><span class="sxs-lookup"><span data-stu-id="77c02-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="77c02-128">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="77c02-128">Click Set active.</span></span>
4. <span data-ttu-id="77c02-129">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="77c02-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="77c02-130">Udvid 'Betalinger (forenklet model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="77c02-131">Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="77c02-132">Vælg BACS-konfigurationen (UK fiktiv) fra Litware, Inc. Proseware, Inc. bruger version 1.1 som udgangspunkt for den brugerdefinerede version.</span><span class="sxs-lookup"><span data-stu-id="77c02-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="77c02-133">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="77c02-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="77c02-134">Dette gør det muligt at oprette en ny konfiguration for et brugerdefineret betalingsformat.</span><span class="sxs-lookup"><span data-stu-id="77c02-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="77c02-135">Angiv 'Afled af navn: BACS (UK fiktivt), Litware, Inc.' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="77c02-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="77c02-136">Vælg indstillingen Afled for at bekræfte brugen af BACS (UK fiktivt) som basis for at oprette den brugerdefinerede version.</span><span class="sxs-lookup"><span data-stu-id="77c02-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="77c02-137">Skriv 'BACS (UK-fiktivt brugerdefineret) i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="77c02-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="77c02-138">Skriv "BACS kreditorbetalingsformat (UK fiktivt brugerdefineret)" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="77c02-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="77c02-139">Den aktive konfigurationsudbyder (Proseware, Inc.) indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="77c02-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="77c02-140">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="77c02-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="77c02-141">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="77c02-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="77c02-142">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="77c02-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="77c02-143">Tilpasse format for det elektroniske dokument</span><span class="sxs-lookup"><span data-stu-id="77c02-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="77c02-144">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="77c02-144">Click Designer.</span></span>
2. <span data-ttu-id="77c02-145">Klik på Udvid/skjul.</span><span class="sxs-lookup"><span data-stu-id="77c02-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="77c02-146">Klik på Udvid/skjul.</span><span class="sxs-lookup"><span data-stu-id="77c02-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="77c02-147">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="77c02-148">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="77c02-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="77c02-149">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="77c02-150">Skriv "IBAN" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="77c02-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="77c02-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-151">Click OK.</span></span>
9. <span data-ttu-id="77c02-152">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\IBAN" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="77c02-153">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="77c02-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="77c02-154">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="77c02-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-155">Click OK.</span></span>
13. <span data-ttu-id="77c02-156">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="77c02-157">Angiv '60' i feltet Maksimumlængde.</span><span class="sxs-lookup"><span data-stu-id="77c02-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="77c02-158">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="77c02-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="77c02-159">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="77c02-160">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="77c02-161">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="77c02-162">Udvid 'model\Betalinger\Kreditor\Konto' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="77c02-163">Vælg "model\Betalinger\Kreditor\Konto\IBAN" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="77c02-164">Vælg "Xml\Meddelelse\Betalinger\Vare = model.Betalinger\Kreditor\Bank\IBAN\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="77c02-165">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="77c02-165">Click Bind.</span></span>
23. <span data-ttu-id="77c02-166">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="77c02-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="77c02-167">Validere det tilpassede format</span><span class="sxs-lookup"><span data-stu-id="77c02-167">Validate the customized format</span></span>
1. <span data-ttu-id="77c02-168">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="77c02-168">Click Validate.</span></span>

    <span data-ttu-id="77c02-169">Validér det tilpassede formatlayout og ændringer af datatilknytningen til at sikre, at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="77c02-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="77c02-170">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77c02-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="77c02-171">Ændre statussen for den aktuelle version af den brugerdefinerede formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="77c02-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="77c02-172">Skift status for den designede formatkonfiguration fra Kladde til Fuldført for at gøre den tilgængelig for oprettelse af betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="77c02-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="77c02-173">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="77c02-173">Click Change status.</span></span>

    <span data-ttu-id="77c02-174">Bemærk, at den aktuelle version af den valgte konfiguration har statussen Kladde.</span><span class="sxs-lookup"><span data-stu-id="77c02-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="77c02-175">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="77c02-175">Click Complete.</span></span>
3. <span data-ttu-id="77c02-176">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="77c02-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="77c02-177">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-177">Click OK.</span></span>
5. <span data-ttu-id="77c02-178">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="77c02-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="77c02-179">Bemærk, at den oprettede konfiguration gemmes som fuldført version 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="77c02-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="77c02-180">Det betyder, at det er version 1 af det brugerdefinerede BACS-format (UK fiktivt brugerdefineret), der er baseret på version 1 af BACS-formatet (UK fiktivt), der er baseret på version 1 af datamodellen Betalinger (forenklet model).</span><span class="sxs-lookup"><span data-stu-id="77c02-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="77c02-181">Teste det tilpassede format for at generere betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="77c02-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="77c02-182">Udfør trinnene i proceduren "Bruge oprettet format for at generere elektroniske dokumenter til betalinger" i en parallel Finance and Operations-session.</span><span class="sxs-lookup"><span data-stu-id="77c02-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="77c02-183">Vælg BACS-formatet (UK fiktivt brugerdefineret) i parametrene for den elektroniske betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="77c02-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="77c02-184">Sørg for, at den oprettede betalingsfil indeholder den netop indførte XML-node, som præsenterer IBAN-kode i henhold til de regionale krav.</span><span class="sxs-lookup"><span data-stu-id="77c02-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="77c02-185">Opdatere den eksisterende landespecifikke konfiguration</span><span class="sxs-lookup"><span data-stu-id="77c02-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="77c02-186">Litware, Inc. skal opdatere konfigurationen af BACS (UK fiktivt) og benytte nye land/område-specifikke krav til håndtering af formatet på det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="77c02-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="77c02-187">Senere bliver det inkluderet i en ny version af denne konfiguration, som vil blive tilbudt til serviceabonnenter, herunder Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="77c02-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="77c02-188">I processer, der er relateret til reelle tjenesteydelser, kan hver ny version af BACS (UK fiktivt) importeres af Proseware, Inc. fra Litware, Inc.-konfigurationers LCS-lager.</span><span class="sxs-lookup"><span data-stu-id="77c02-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="77c02-189">I denne procedure vil vi simulere dette ved at opdatere BACS (UK fiktivt) på vegne af en serviceudbyder.</span><span class="sxs-lookup"><span data-stu-id="77c02-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="77c02-190">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77c02-190">Close the page.</span></span>
2. <span data-ttu-id="77c02-191">Vælg Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="77c02-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="77c02-192">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="77c02-192">Click Set active.</span></span>
4. <span data-ttu-id="77c02-193">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="77c02-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="77c02-194">Udvid 'Betalinger (forenklet model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="77c02-195">Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="77c02-196">Kladdeversionen, som ejes af BACS-udbyderen Litware, Inc. (UK fiktivt), er valgt til at sikre, at ændringer understøtter de nye land/område-specifikke krav.</span><span class="sxs-lookup"><span data-stu-id="77c02-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="77c02-197">Lokalisere basisformatet for det elektroniske dokument</span><span class="sxs-lookup"><span data-stu-id="77c02-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="77c02-198">Antag, at der er nye landespecifikke krav, der skal understøttes af Litware, Inc.:</span><span class="sxs-lookup"><span data-stu-id="77c02-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="77c02-199">En værdi for kreditors banks SWIFT-kode i hver betalingstransaktion.</span><span class="sxs-lookup"><span data-stu-id="77c02-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="77c02-200">En grænse på 100 tegn for tekstlængden på kreditorens navn i en fil, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="77c02-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="77c02-201">Nye land/område-specifikke krav</span><span class="sxs-lookup"><span data-stu-id="77c02-201">New country-specific requirements</span></span>  
- <span data-ttu-id="77c02-202">Vælg kladdeversionen af den ønskede konfiguration for at indføre de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="77c02-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="77c02-203">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="77c02-203">Click Designer.</span></span>
2. <span data-ttu-id="77c02-204">Klik på Udvid/skjul.</span><span class="sxs-lookup"><span data-stu-id="77c02-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="77c02-205">Klik på Udvid/skjul.</span><span class="sxs-lookup"><span data-stu-id="77c02-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="77c02-206">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="77c02-207">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="77c02-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="77c02-208">Vælg "XML\Element'' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="77c02-209">Skriv "SWIFT" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="77c02-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="77c02-210">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-210">Click OK.</span></span>
9. <span data-ttu-id="77c02-211">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\SWIFT" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="77c02-212">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="77c02-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="77c02-213">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="77c02-214">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-214">Click OK.</span></span>
13. <span data-ttu-id="77c02-215">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="77c02-216">Angiv '100' i feltet Maksimumlængde.</span><span class="sxs-lookup"><span data-stu-id="77c02-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="77c02-217">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="77c02-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="77c02-218">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="77c02-219">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="77c02-220">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="77c02-221">Udvid "model\Betalinger\Kreditor\Speditør" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="77c02-222">Vælg "model\Betalinger\Kreditor\Speditør\SWIFT" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="77c02-223">Vælg "Xml\Meddelelse\Betalinger\Vare = model.Betalinger\Kreditor\Bank\SWIFT\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="77c02-224">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="77c02-224">Click Bind.</span></span>
23. <span data-ttu-id="77c02-225">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="77c02-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="77c02-226">Validere det lokaliserede format</span><span class="sxs-lookup"><span data-stu-id="77c02-226">Validate the localized format</span></span>
1. <span data-ttu-id="77c02-227">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="77c02-227">Click Validate.</span></span>
2. <span data-ttu-id="77c02-228">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77c02-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="77c02-229">Ændre statussen for den aktuelle version af basisformatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="77c02-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="77c02-230">Skift status for den opdaterede basisformatkonfiguration fra Kladde til Fuldført for at gøre den tilgængelig for oprettelse af betalingsdokumenter og opdateringer af de formatkonfigurationer, der er afledt af den.</span><span class="sxs-lookup"><span data-stu-id="77c02-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="77c02-231">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="77c02-231">Click Change status.</span></span>

    <span data-ttu-id="77c02-232">Bemærk, at den aktuelle version af den valgte konfiguration har statussen Kladde.</span><span class="sxs-lookup"><span data-stu-id="77c02-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="77c02-233">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="77c02-233">Click Complete.</span></span>
3. <span data-ttu-id="77c02-234">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="77c02-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="77c02-235">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-235">Click OK.</span></span>
5. <span data-ttu-id="77c02-236">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="77c02-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="77c02-237">Ændre basisversionen af den brugerdefinerede formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="77c02-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="77c02-238">Proseware, Inc. får besked om, at en ny version 1.2 af BACS-konfigurationen (UK fiktivt) er tilgængelig for oprettelse af elektroniske betalingsdokumenter i henhold til de nyligt annoncerede land/område-specifikke krav.</span><span class="sxs-lookup"><span data-stu-id="77c02-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="77c02-239">Proseware, Inc. ønsker at begynde at bruge den som en standard for landet/området.</span><span class="sxs-lookup"><span data-stu-id="77c02-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="77c02-240">For at kunne gøre dette skal Proseware, Inc. ændre basiskonfigurationsversionen af den brugerdefinerede BACS-konfigurationen (UK fiktivt brugerdefineret).</span><span class="sxs-lookup"><span data-stu-id="77c02-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="77c02-241">Brug den nye version 1.2, i stedet for version 1.1 af BACS (UK fiktivt).</span><span class="sxs-lookup"><span data-stu-id="77c02-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="77c02-242">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="77c02-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="77c02-243">Vælg udbyderen Proseware, Inc., for at markere den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="77c02-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="77c02-244">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="77c02-244">Click Set active.</span></span>
4. <span data-ttu-id="77c02-245">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="77c02-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="77c02-246">Udvid 'Betalinger (forenklet model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="77c02-247">Udvid 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="77c02-248">Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)\BACS (UK fiktivt brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="77c02-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="77c02-249">Vælg BACS-konfigurationen (UK fiktivt brugerdefineret), som ejes af Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="77c02-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="77c02-250">Brug kladdeversionen af den valgte konfiguration for at indføre de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="77c02-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="77c02-251">Klik på Rebasér.</span><span class="sxs-lookup"><span data-stu-id="77c02-251">Click Rebase.</span></span>

    <span data-ttu-id="77c02-252">Vælg den nye version 1.2 af den basiskonfiguration, der skal anvendes som ny basis for opdatering af konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="77c02-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="77c02-253">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-253">Click OK.</span></span>

    <span data-ttu-id="77c02-254">Bemærk, at der er fundet nogle konflikter mellem fletning af den brugerdefinerede version og en ny basisversion, der repræsenterer nogle formatændringer, der ikke kan flettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="77c02-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="77c02-255">Løse rebaseringskonflikter</span><span class="sxs-lookup"><span data-stu-id="77c02-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="77c02-256">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="77c02-256">Click Designer.</span></span>
    
    <span data-ttu-id="77c02-257">Bemærk, at ændringer af grænsen for tekstlængen på kreditorens navn ikke kunne løses automatisk.</span><span class="sxs-lookup"><span data-stu-id="77c02-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="77c02-258">Dette vises derfor på en liste over konflikter.</span><span class="sxs-lookup"><span data-stu-id="77c02-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="77c02-259">For hver konflikt af typen Opdatering er følgende indstillinger tilgængelige: - Anvend en tidligere basisværdi (knap oven på gitteret) for at overføre den tidligere basisversions værdi (0 i vores tilfælde).</span><span class="sxs-lookup"><span data-stu-id="77c02-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="77c02-260">- Anvend en basisværdi (knap oven på gitteret) for at overføre den nye basisversions værdi (100 i vores tilfælde).</span><span class="sxs-lookup"><span data-stu-id="77c02-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="77c02-261">- Bevar din egen (brugerdefineret) værdi (60 i dette tilfælde).</span><span class="sxs-lookup"><span data-stu-id="77c02-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="77c02-262">Klik på Anvend basisværdi for at anvende en land/område-specifik grænse på 100 tegn for tekstlængden på kreditorens navn.</span><span class="sxs-lookup"><span data-stu-id="77c02-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="77c02-263">Bemærk, at Proseware, Inc. og Litware, Inc. har brugerdefinerede og lokale versioner af dette format, som benytter IBAN- og SWIFT-koder med relaterede komponenter, der flettes automatisk i håndteringen af formatet.</span><span class="sxs-lookup"><span data-stu-id="77c02-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="77c02-264">Klik på Anvend basisværdi.</span><span class="sxs-lookup"><span data-stu-id="77c02-264">Click Apply base value.</span></span>

    <span data-ttu-id="77c02-265">Klik på Anvend basisværdi for at anvende den landespecifikke grænse på 100 tegn for kreditornavne.</span><span class="sxs-lookup"><span data-stu-id="77c02-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="77c02-266">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="77c02-266">Click Save.</span></span>

    <span data-ttu-id="77c02-267">Hvis du gemmer formatet, fjernes løste konflikter fra listen over konflikter.</span><span class="sxs-lookup"><span data-stu-id="77c02-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="77c02-268">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="77c02-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="77c02-269">Ændre statussen for den nye version af den brugerdefinerede formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="77c02-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="77c02-270">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="77c02-270">Click Change status.</span></span>

    <span data-ttu-id="77c02-271">Skift status for den opdaterede, brugerdefinerede formatkonfiguration fra Kladde til Fuldført.</span><span class="sxs-lookup"><span data-stu-id="77c02-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="77c02-272">Dette vil gøre formatkonfigurationen tilgængelig for oprettelse af betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="77c02-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="77c02-273">Bemærk, at den aktuelle version af den valgte konfiguration har statussen Kladde.</span><span class="sxs-lookup"><span data-stu-id="77c02-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="77c02-274">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="77c02-274">Click Complete.</span></span>
3. <span data-ttu-id="77c02-275">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="77c02-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="77c02-276">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="77c02-276">Click OK.</span></span>

    <span data-ttu-id="77c02-277">Bemærk, at den oprettede konfiguration gemmes som fuldført version 1.2.2: version 2 af BACS-basisformatet (UK fiktivt brugerdefineret), der er baseret på version 2 af BACS-basisformatet (UK fiktivt), der er baseret på version 1 af datamodellen Betalinger (forenklet model).</span><span class="sxs-lookup"><span data-stu-id="77c02-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="77c02-278">Teste det tilpassede format for generering af betalingsfiler</span><span class="sxs-lookup"><span data-stu-id="77c02-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="77c02-279">Udfør trinnene i proceduren "Bruge oprettet format for at generere elektroniske dokumenter til betalinger" i en parallel Finance and Operations-session.</span><span class="sxs-lookup"><span data-stu-id="77c02-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="77c02-280">Vælg det oprettede 'BACS-format (UK fiktivt brugerdefineret)' i parametrene for den elektroniske betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="77c02-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="77c02-281">Sørg for, at den oprettede betalingsfil indeholder Proseware, Inc.s netop indførte XML-node, som præsenterer IBAN-kontokode i henhold til de regionale krav.</span><span class="sxs-lookup"><span data-stu-id="77c02-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="77c02-282">Filen skal også indeholde Litware, Inc.s netop indførte XML-node, som præsenterer SWIFT-bankkode i overensstemmelse med kravene i landet.</span><span class="sxs-lookup"><span data-stu-id="77c02-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]