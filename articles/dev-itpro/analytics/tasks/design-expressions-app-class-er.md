---
title: Designe ER-udtryk til kald af programklassemetoder
description: Denne vejledning indeholder oplysninger om, hvordan du genbruge den eksisterende programlogik i konfigurationer til elektronisk rapportering (ER) ved at kalde de krævede metoder for programklasser i ER-udtryk.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544880"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="237f1-103">Designe ER-udtryk til kald af programklassemetoder</span><span class="sxs-lookup"><span data-stu-id="237f1-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="237f1-104">Denne vejledning indeholder oplysninger om, hvordan du genbruge den eksisterende programlogik i konfigurationer til elektronisk rapportering (ER) ved at kalde de krævede metoder for programklasser i ER-udtryk.</span><span class="sxs-lookup"><span data-stu-id="237f1-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="237f1-105">Værdier for argumenter til kald af klasser kan defineres dynamisk på kørselstidspunktet, f.eks. baseret på oplysninger i parsingdokumentet for at sikre, at det er korrekt.</span><span class="sxs-lookup"><span data-stu-id="237f1-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="237f1-106">I denne guide skal du oprette de krævede ER-konfigurationer til eksempelfirmaet Litware Inc. Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="237f1-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="237f1-107">Disse trin kan udføres ved hjælp af ethvert datasæt.</span><span class="sxs-lookup"><span data-stu-id="237f1-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="237f1-108">Du skal hente og gemme følgende fil lokalt: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="237f1-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="237f1-109">Du skal først fuldføre trinnene i proceduren "ER Oprette en konfigurationsudbyder markere den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="237f1-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="237f1-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="237f1-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="237f1-111">Kontrollér, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="237f1-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="237f1-112">Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i proceduren "Oprette en ER-konfigurationsudbyder og markere den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="237f1-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="237f1-113">Lad os antage, at du designer en proces til fortolkning af indgående bankkontoudtog for en opdatering til programdata.</span><span class="sxs-lookup"><span data-stu-id="237f1-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="237f1-114">Du får de indgående bankkontoudtog som TXT-filer, der indeholder IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="237f1-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="237f1-115">Som en del af importprocessen for kontoudtog skal du validere rigtigheden af disse IBAN-koder ved brug af den logik, der allerede findes i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="237f1-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="237f1-116">Importere en ny ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="237f1-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="237f1-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="237f1-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="237f1-118">Vælg feltet Microsoft-udbyder.</span><span class="sxs-lookup"><span data-stu-id="237f1-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="237f1-119">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="237f1-119">Click Repositories.</span></span>
3. <span data-ttu-id="237f1-120">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="237f1-120">Click Show filters.</span></span>
4. <span data-ttu-id="237f1-121">Tilføje et filterfelt ‘Typenavn’.</span><span class="sxs-lookup"><span data-stu-id="237f1-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="237f1-122">Angiv værdien "ressourcer" i feltet Navn, vælg filteroperatoren "indeholder", og klik derefter på Anvend.</span><span class="sxs-lookup"><span data-stu-id="237f1-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="237f1-123">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="237f1-123">Click Open.</span></span>
6. <span data-ttu-id="237f1-124">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="237f1-125">Hvis knappen Importer i oversigtspanelet Versioner ikke er aktiveret, har du allerede importeret version 1 af ER-konfigurationen 'Betalingsmodel'.</span><span class="sxs-lookup"><span data-stu-id="237f1-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="237f1-126">Du kan springe over resten af trinnene i denne underordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="237f1-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="237f1-127">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="237f1-127">Click Import.</span></span>
8. <span data-ttu-id="237f1-128">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="237f1-128">Click Yes.</span></span>
9. <span data-ttu-id="237f1-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="237f1-129">Close the page.</span></span>
10. <span data-ttu-id="237f1-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="237f1-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="237f1-131">Tilføje en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="237f1-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="237f1-132">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="237f1-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="237f1-133">Tilføje et nyt ER-format til at fortolke indgående bankkontoudtog i TXT-formatet.</span><span class="sxs-lookup"><span data-stu-id="237f1-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="237f1-134">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="237f1-135">Klik på Opret konfiguration for at åbne dialogmenuen.</span><span class="sxs-lookup"><span data-stu-id="237f1-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="237f1-136">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="237f1-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="237f1-137">Skriv 'Importformat for bankkontoudtog (eksempel)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="237f1-138">Importformat for bankkontoudtog (eksempel)</span><span class="sxs-lookup"><span data-stu-id="237f1-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="237f1-139">Vælg Ja i feltet Understøtter dataimport.</span><span class="sxs-lookup"><span data-stu-id="237f1-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="237f1-140">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="237f1-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="237f1-141">Designe ER-formatkonfigurationen - format</span><span class="sxs-lookup"><span data-stu-id="237f1-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="237f1-142">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="237f1-142">Click Designer.</span></span>
    * <span data-ttu-id="237f1-143">Det designede format repræsenterer den forventede struktur i den eksterne fil i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="237f1-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="237f1-144">Klik på Tilføj rod for at åbne dialogmenuen.</span><span class="sxs-lookup"><span data-stu-id="237f1-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="237f1-145">Vælg 'Text\Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="237f1-146">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="237f1-147">Rod</span><span class="sxs-lookup"><span data-stu-id="237f1-147">Root</span></span>  
5. <span data-ttu-id="237f1-148">Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.</span><span class="sxs-lookup"><span data-stu-id="237f1-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="237f1-149">Indstillingen 'Ny linje – Windows (CR LF)' er blevet valgt i feltet 'Specialtegn'.</span><span class="sxs-lookup"><span data-stu-id="237f1-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="237f1-150">Baseret på denne indstilling betragtes hver linje i parsingfilen som en separat post.</span><span class="sxs-lookup"><span data-stu-id="237f1-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="237f1-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="237f1-151">Click OK.</span></span>
7. <span data-ttu-id="237f1-152">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="237f1-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="237f1-153">Vælg 'Text\Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="237f1-154">Indtast 'Rækker' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="237f1-155">Rækker</span><span class="sxs-lookup"><span data-stu-id="237f1-155">Rows</span></span>  
10. <span data-ttu-id="237f1-156">Vælg 'Én mange' i feltet Multiplicitet.</span><span class="sxs-lookup"><span data-stu-id="237f1-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="237f1-157">Indstillingen 'én mange' er valgt i feltet 'Multiplicitet'.</span><span class="sxs-lookup"><span data-stu-id="237f1-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="237f1-158">Baseret på denne indstilling forventes det, at der vises mindst én linje i parsingfilen.</span><span class="sxs-lookup"><span data-stu-id="237f1-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="237f1-159">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="237f1-159">Click OK.</span></span>
12. <span data-ttu-id="237f1-160">Vælg 'Rod\Rækker' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="237f1-161">Klik på Tilføj rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="237f1-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="237f1-162">Skriv 'Felter' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="237f1-163">Felter</span><span class="sxs-lookup"><span data-stu-id="237f1-163">Fields</span></span>  
15. <span data-ttu-id="237f1-164">Vælg 'Nøjagtig én' i feltet Multiplicitet.</span><span class="sxs-lookup"><span data-stu-id="237f1-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="237f1-165">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="237f1-165">Click OK.</span></span>
17. <span data-ttu-id="237f1-166">I træet skal du vælge 'Rod\Rækker\Felter'.</span><span class="sxs-lookup"><span data-stu-id="237f1-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="237f1-167">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="237f1-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="237f1-168">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="237f1-169">Skriv "IBAN" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="237f1-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="237f1-170">IBAN</span></span>  
21. <span data-ttu-id="237f1-171">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="237f1-171">Click OK.</span></span>
    * <span data-ttu-id="237f1-172">Det er konfigureret, at hver linje i parsingfilen kun indeholder IBAN-kode.</span><span class="sxs-lookup"><span data-stu-id="237f1-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="237f1-173">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="237f1-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="237f1-174">Designe ER-formatkonfigurationen – tilknytning til datamodel</span><span class="sxs-lookup"><span data-stu-id="237f1-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="237f1-175">Klik på Knyt format til model.</span><span class="sxs-lookup"><span data-stu-id="237f1-175">Click Map format to model.</span></span>
2. <span data-ttu-id="237f1-176">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="237f1-176">Click New.</span></span>
3. <span data-ttu-id="237f1-177">Skriv "BankToCustomerDebitCreditNotificationInitiation" i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="237f1-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="237f1-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="237f1-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="237f1-179">ResolveChanges definitionen.</span><span class="sxs-lookup"><span data-stu-id="237f1-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="237f1-180">Skriv 'Tilknytning til datamodel' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="237f1-181">Tilknytning til datamodel</span><span class="sxs-lookup"><span data-stu-id="237f1-181">Mapping to data model</span></span>  
6. <span data-ttu-id="237f1-182">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="237f1-182">Click Save.</span></span>
7. <span data-ttu-id="237f1-183">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="237f1-183">Click Designer.</span></span>
8. <span data-ttu-id="237f1-184">Vælg 'Dynamics 365 for Operations\Klasse' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="237f1-185">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="237f1-185">Click Add root.</span></span>
    * <span data-ttu-id="237f1-186">Tilføje en ny datakilde for at kalde den eksisterende programlogik til validering af IBAN-koder.</span><span class="sxs-lookup"><span data-stu-id="237f1-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="237f1-187">Skriv 'checkkoder' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="237f1-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="237f1-188">Kontrollér koder</span><span class="sxs-lookup"><span data-stu-id="237f1-188">check_codes</span></span>  
11. <span data-ttu-id="237f1-189">Skriv 'ISO7064' i feltet Klasse.</span><span class="sxs-lookup"><span data-stu-id="237f1-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="237f1-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="237f1-190">ISO7064</span></span>  
12. <span data-ttu-id="237f1-191">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="237f1-191">Click OK.</span></span>
13. <span data-ttu-id="237f1-192">Udvid 'format' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="237f1-193">Udvid 'format\Rod: Sequence(Root)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="237f1-194">Vælg 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)'.</span><span class="sxs-lookup"><span data-stu-id="237f1-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="237f1-195">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="237f1-195">Click Bind.</span></span>
17. <span data-ttu-id="237f1-196">Udvid ' format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="237f1-197">Udvid 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)\Felter: sekvens 1..1 (felter)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="237f1-198">Vælg 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)\Felter: sekvens 1..1 (felter)\IBAN: String(IBAN)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="237f1-199">Udvid 'Betalinger = format.Root.Rows' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="237f1-200">Udvid 'Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="237f1-201">Udvid 'Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identifikation' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="237f1-202">Vælg 'Betalinger = format.Root.Rows\Creditor Account(CreditorAccount)\Identifikation\IBAN' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="237f1-203">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="237f1-203">Click Bind.</span></span>
25. <span data-ttu-id="237f1-204">Klik på fanen Valideringer.</span><span class="sxs-lookup"><span data-stu-id="237f1-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="237f1-205">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="237f1-205">Click New.</span></span>
    * <span data-ttu-id="237f1-206">Tilføje en ny valideringsregel, der vises en fejlmeddelelse for hver linje i parsingfilen, der indeholder ugyldig IBAN-kode.</span><span class="sxs-lookup"><span data-stu-id="237f1-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="237f1-207">Klik på Rediger betingelse.</span><span class="sxs-lookup"><span data-stu-id="237f1-207">Click Edit condition.</span></span>
28. <span data-ttu-id="237f1-208">Udvid "checkkoder" i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="237f1-209">Vælg 'check_codes\verifyMOD1271_36' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="237f1-210">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="237f1-210">Click Add data source.</span></span>
31. <span data-ttu-id="237f1-211">Skriv "check_codes.verifyMOD1271_36(" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="237f1-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="237f1-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="237f1-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="237f1-213">Udvid 'format' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="237f1-214">Udvid 'format\Rod: Sequence(Root)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="237f1-215">Udvid ' format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="237f1-216">Udvid 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)\Felter: sekvens 1..1 (felter)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="237f1-217">Vælg 'format\Rod: Sequence(Root)\Rækker: sekvens 1.. \* (rækker)\Felter: sekvens 1..1 (felter)\IBAN: String(IBAN)' i træet.</span><span class="sxs-lookup"><span data-stu-id="237f1-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="237f1-218">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="237f1-218">Click Add data source.</span></span>
38. <span data-ttu-id="237f1-219">Angiv 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="237f1-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="237f1-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="237f1-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="237f1-221">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="237f1-221">Click Save.</span></span>
40. <span data-ttu-id="237f1-222">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="237f1-222">Close the page.</span></span>
    * <span data-ttu-id="237f1-223">Valideringsbetingelsen er konfigureret til at returnere FALSE for eventuel ugyldige IBAN-kode ved at kalde den eksisterende metode 'verifyMOD1271_36' i programklassen 'ISO7064'.</span><span class="sxs-lookup"><span data-stu-id="237f1-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="237f1-224">Bemærk, at værdien af IBAN-koden defineres dynamisk under kørsel som argument i kaldemetoden baseret på indholdet af TXT-filen til parsing.</span><span class="sxs-lookup"><span data-stu-id="237f1-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="237f1-225">Klik på Rediger meddelelse.</span><span class="sxs-lookup"><span data-stu-id="237f1-225">Click Edit message.</span></span>
42. <span data-ttu-id="237f1-226">Angiv 'CONCATENATE("Ugyldig IBAN-kode er fundet: ", format.Root.Rows.Fields.IBAN)' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="237f1-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="237f1-227">CONCATENATE("Ugyldig IBAN-kode er fundet: ", format. Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="237f1-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="237f1-228">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="237f1-228">Click Save.</span></span>
44. <span data-ttu-id="237f1-229">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="237f1-229">Close the page.</span></span>
45. <span data-ttu-id="237f1-230">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="237f1-230">Click Save.</span></span>
46. <span data-ttu-id="237f1-231">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="237f1-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="237f1-232">Kør formattilknytningen</span><span class="sxs-lookup"><span data-stu-id="237f1-232">Run the format mapping</span></span>
<span data-ttu-id="237f1-233">Til testformål skal du udføre formattilknytningen ved hjælp af filen SampleIncomingMessage.txt, som du tidligere har hentet.</span><span class="sxs-lookup"><span data-stu-id="237f1-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="237f1-234">Det genererede output omfatter data, der importeres fra den valgte TXT-fil og udfylder den brugerdefinerede datamodel under den faktiske import.</span><span class="sxs-lookup"><span data-stu-id="237f1-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="237f1-235">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="237f1-235">Click Run.</span></span>
    * <span data-ttu-id="237f1-236">Klik på Gennemse, og naviger til filen SampleIncomingMessage.txt, som du tidligere har downloadet.</span><span class="sxs-lookup"><span data-stu-id="237f1-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="237f1-237">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="237f1-237">Click OK.</span></span>
    * <span data-ttu-id="237f1-238">Gennemgå outputtet i XML-format, som viser de data, der er importeret fra den valgte fil og overført til datamodellen.</span><span class="sxs-lookup"><span data-stu-id="237f1-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="237f1-239">Bemærk, at kun 3 linjer i den importerede TXT-fil blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="237f1-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="237f1-240">IBAN-koden på linje 4, der er ugyldig, blev sprunget over, og der findes en fejlmeddelelse i infologgen.</span><span class="sxs-lookup"><span data-stu-id="237f1-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  

