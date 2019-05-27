---
title: Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551548"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="47d58-103">Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)</span><span class="sxs-lookup"><span data-stu-id="47d58-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47d58-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="47d58-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="47d58-105">Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="47d58-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="47d58-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="47d58-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="47d58-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="47d58-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="47d58-108">Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen.</span><span class="sxs-lookup"><span data-stu-id="47d58-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="47d58-109">Denne fil kan åbnes fra [Skabelon for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="47d58-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="47d58-110">Overføre konfiguration for betalingsdatamodel</span><span class="sxs-lookup"><span data-stu-id="47d58-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="47d58-111">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="47d58-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="47d58-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="47d58-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="47d58-113">Vælg konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="47d58-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="47d58-114">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="47d58-114">Click Set active.</span></span>
4. <span data-ttu-id="47d58-115">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="47d58-115">Click Repositories.</span></span>
    * <span data-ttu-id="47d58-116">Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="47d58-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="47d58-117">Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="47d58-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="47d58-118">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="47d58-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="47d58-119">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="47d58-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="47d58-120">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="47d58-120">Click Create repository.</span></span>
8. <span data-ttu-id="47d58-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47d58-121">Click OK.</span></span>
9. <span data-ttu-id="47d58-122">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="47d58-122">Click Open.</span></span>
10. <span data-ttu-id="47d58-123">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="47d58-124">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="47d58-124">Click Import.</span></span>
    * <span data-ttu-id="47d58-125">Importér denne datamodel.</span><span class="sxs-lookup"><span data-stu-id="47d58-125">Import this data model.</span></span> <span data-ttu-id="47d58-126">Den bruges som en datakilde i en ny formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="47d58-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="47d58-127">Spring dette trin over, hvis denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="47d58-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="47d58-128">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="47d58-128">Click Yes.</span></span>
13. <span data-ttu-id="47d58-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-129">Close the page.</span></span>
14. <span data-ttu-id="47d58-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="47d58-131">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="47d58-131">Create a new format configuration</span></span>
1. <span data-ttu-id="47d58-132">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="47d58-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="47d58-133">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="47d58-134">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="47d58-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="47d58-135">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="47d58-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="47d58-136">Opret et format, der er baseret på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="47d58-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="47d58-137">Skriv 'Eksempel på regnearksrapport' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="47d58-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="47d58-138">Eksempel på regnearksrapport</span><span class="sxs-lookup"><span data-stu-id="47d58-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="47d58-139">Skriv 'Eksempel på regnearksrapport for kreditorers betalinger' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="47d58-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="47d58-140">Eksempel på regnearksrapport for kreditorers betalinger</span><span class="sxs-lookup"><span data-stu-id="47d58-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="47d58-141">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="47d58-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="47d58-142">Vælg 'CustomerCreditTransferInitiation'-definitionen.</span><span class="sxs-lookup"><span data-stu-id="47d58-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="47d58-143">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="47d58-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="47d58-144">Designe et nyt dokument i OPENXML-regnearksformat</span><span class="sxs-lookup"><span data-stu-id="47d58-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="47d58-145">Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="47d58-146">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="47d58-146">Click Designer.</span></span>
3. <span data-ttu-id="47d58-147">Klik på Importér i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="47d58-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="47d58-148">Klik på Importér fra Excel.</span><span class="sxs-lookup"><span data-stu-id="47d58-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="47d58-149">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="47d58-149">Click Attachments.</span></span>
    * <span data-ttu-id="47d58-150">Vedhæft det eksisterende Excel-dokument som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="47d58-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="47d58-151">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="47d58-151">Click New.</span></span>
7. <span data-ttu-id="47d58-152">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="47d58-152">Click File.</span></span>
    * <span data-ttu-id="47d58-153">Peg på den eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="47d58-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="47d58-154">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-154">Close the page.</span></span>
9. <span data-ttu-id="47d58-155">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="47d58-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="47d58-156">Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.</span><span class="sxs-lookup"><span data-stu-id="47d58-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="47d58-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47d58-157">Click OK.</span></span>
    * <span data-ttu-id="47d58-158">Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).</span><span class="sxs-lookup"><span data-stu-id="47d58-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="47d58-159">Oprette en ny datakilde for at beregne totaler efter valutakoder</span><span class="sxs-lookup"><span data-stu-id="47d58-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="47d58-160">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="47d58-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="47d58-161">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="47d58-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="47d58-162">Vælg 'Funktioner\Gruppér efter' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="47d58-163">Skriv 'PaymentByCurrency' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="47d58-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="47d58-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="47d58-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="47d58-165">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="47d58-165">Click Edit group by.</span></span>
6. <span data-ttu-id="47d58-166">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="47d58-167">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="47d58-168">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="47d58-168">Click Add field to.</span></span>
9. <span data-ttu-id="47d58-169">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="47d58-169">Click What to group.</span></span>
10. <span data-ttu-id="47d58-170">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="47d58-171">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="47d58-172">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="47d58-172">Click Add field to.</span></span>
13. <span data-ttu-id="47d58-173">Klik på Grupperede felter.</span><span class="sxs-lookup"><span data-stu-id="47d58-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="47d58-174">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="47d58-175">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="47d58-175">Click Add field to.</span></span>
16. <span data-ttu-id="47d58-176">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="47d58-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="47d58-177">Vælg en indstilling i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="47d58-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="47d58-178">Vælg sammenlægningsfunktionen SUM.</span><span class="sxs-lookup"><span data-stu-id="47d58-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="47d58-179">Skriv 'TotalInstructuredAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="47d58-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="47d58-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="47d58-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="47d58-181">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47d58-181">Click Save.</span></span>
20. <span data-ttu-id="47d58-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-182">Close the page.</span></span>
21. <span data-ttu-id="47d58-183">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47d58-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="47d58-184">Knytte formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="47d58-184">Map format components to data sources</span></span>
1. <span data-ttu-id="47d58-185">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="47d58-186">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="47d58-187">Udvid 'model\Betalinger\Initierende part(InitiatingParty)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="47d58-188">Vælg 'model\Betalinger\Initierende part(InitiatingParty)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="47d58-189">Udvid "Excel\ReportHeader" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="47d58-190">Vælg "Excel\ReportHeader\CompanyName" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="47d58-191">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-191">Click Bind.</span></span>
8. <span data-ttu-id="47d58-192">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="47d58-193">Udvid 'model\Betalinger\Kreditor\Identifikation' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="47d58-194">Vælg 'model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="47d58-195">Udvid "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="47d58-196">Vælg "Excel\PaymLines\VendAccountName" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="47d58-197">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-197">Click Bind.</span></span>
14. <span data-ttu-id="47d58-198">Vælg "model\Betalinger\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="47d58-199">Vælg "Excel\PaymLines\VendName" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="47d58-200">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-200">Click Bind.</span></span>
17. <span data-ttu-id="47d58-201">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="47d58-202">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="47d58-203">Vælg "Excel\PaymLines\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="47d58-204">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-204">Click Bind.</span></span>
21. <span data-ttu-id="47d58-205">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="47d58-206">Vælg "Excel\PaymLines\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="47d58-207">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-207">Click Bind.</span></span>
24. <span data-ttu-id="47d58-208">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="47d58-209">Udvid 'model\Payments\Creditor Account(CreditorAccount)\Identification' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="47d58-210">Vælg 'model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\IBAN' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="47d58-211">Vælg "Excel\PaymLines\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="47d58-212">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-212">Click Bind.</span></span>
29. <span data-ttu-id="47d58-213">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="47d58-214">Vælg "Excel\PaymLines\Debit" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="47d58-215">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-215">Click Bind.</span></span>
32. <span data-ttu-id="47d58-216">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="47d58-217">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="47d58-218">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="47d58-219">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="47d58-220">Vælg "Excel\PaymLines\Currency" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="47d58-221">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-221">Click Bind.</span></span>
38. <span data-ttu-id="47d58-222">Udvid 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="47d58-223">Udvid 'PaymentByCurrency\grouped' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="47d58-224">Vælg 'PaymentByCurrency\grouped\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="47d58-225">Udvid "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="47d58-226">Vælg "Excel\SummaryLines\SummaryCurrency" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="47d58-227">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-227">Click Bind.</span></span>
44. <span data-ttu-id="47d58-228">Udvid 'PaymentByCurrency\aggregated' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="47d58-229">Vælg 'PaymentByCurrency\aggregated\TotalInstructuredAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="47d58-230">Vælg "Excel\SummaryLines\SummaryAmount" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="47d58-231">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-231">Click Bind.</span></span>
48. <span data-ttu-id="47d58-232">Vælg 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="47d58-233">Vælg "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="47d58-234">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-234">Click Bind.</span></span>
51. <span data-ttu-id="47d58-235">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="47d58-236">Vælg "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="47d58-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="47d58-237">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="47d58-237">Click Bind.</span></span>
54. <span data-ttu-id="47d58-238">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47d58-238">Click Save.</span></span>
55. <span data-ttu-id="47d58-239">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="47d58-240">Bruge den oprettede konfiguration til behandling af betalinger</span><span class="sxs-lookup"><span data-stu-id="47d58-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="47d58-241">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="47d58-241">Click Change status.</span></span>
2. <span data-ttu-id="47d58-242">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="47d58-242">Click Complete.</span></span>
3. <span data-ttu-id="47d58-243">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47d58-243">Click OK.</span></span>
4. <span data-ttu-id="47d58-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-244">Close the page.</span></span>
5. <span data-ttu-id="47d58-245">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-245">Close the page.</span></span>
6. <span data-ttu-id="47d58-246">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="47d58-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="47d58-247">Brug Quick Filter til at filtrere på feltet Betalingsmåde med værdien "Elektronisk".</span><span class="sxs-lookup"><span data-stu-id="47d58-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="47d58-248">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="47d58-248">Electronic</span></span>  
8. <span data-ttu-id="47d58-249">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="47d58-249">Click Edit.</span></span>
9. <span data-ttu-id="47d58-250">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="47d58-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="47d58-251">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="47d58-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="47d58-252">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="47d58-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="47d58-253">Vælg konfigurationen 'Eksempel på regnearksrapport'.</span><span class="sxs-lookup"><span data-stu-id="47d58-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="47d58-254">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47d58-254">Click Save.</span></span>
13. <span data-ttu-id="47d58-255">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="47d58-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="47d58-256">Bruge den oprettede konfiguration til at teste betalingskladdebehandling</span><span class="sxs-lookup"><span data-stu-id="47d58-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="47d58-257">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="47d58-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="47d58-258">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="47d58-258">Click New.</span></span>
    * <span data-ttu-id="47d58-259">Opret en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="47d58-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="47d58-260">Skriv VendPay i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="47d58-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="47d58-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="47d58-261">VendPay</span></span>  
4. <span data-ttu-id="47d58-262">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="47d58-262">Click Lines.</span></span>
5. <span data-ttu-id="47d58-263">I feltet Konto skal du angive værdierne 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="47d58-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="47d58-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="47d58-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="47d58-265">Angiv Debet til '1000'.</span><span class="sxs-lookup"><span data-stu-id="47d58-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="47d58-266">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="47d58-266">Click New.</span></span>
8. <span data-ttu-id="47d58-267">I feltet Konto skal du angive værdierne 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="47d58-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="47d58-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="47d58-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="47d58-269">Angiv Debet til '2000'.</span><span class="sxs-lookup"><span data-stu-id="47d58-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="47d58-270">Skriv 'EUR' i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="47d58-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="47d58-271">EUR</span><span class="sxs-lookup"><span data-stu-id="47d58-271">EUR</span></span>  
11. <span data-ttu-id="47d58-272">I feltet Modkonto skal du angive værdierne 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="47d58-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="47d58-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="47d58-273">GBSI OPER</span></span>  
12. <span data-ttu-id="47d58-274">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="47d58-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="47d58-275">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="47d58-275">Electronic</span></span>  
13. <span data-ttu-id="47d58-276">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="47d58-276">Click Save.</span></span>
14. <span data-ttu-id="47d58-277">Klik på Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="47d58-277">Click Generate payments.</span></span>
15. <span data-ttu-id="47d58-278">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="47d58-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="47d58-279">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="47d58-279">Electronic</span></span>  
16. <span data-ttu-id="47d58-280">Skriv "Betalinger" i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="47d58-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="47d58-281">Skriv f.eks. Betalinger.</span><span class="sxs-lookup"><span data-stu-id="47d58-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="47d58-282">Skriv 'GBSI OPER' i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="47d58-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="47d58-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="47d58-283">GBSI OPER</span></span>  
18. <span data-ttu-id="47d58-284">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47d58-284">Click OK.</span></span>
19. <span data-ttu-id="47d58-285">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="47d58-285">Click OK.</span></span>
    * <span data-ttu-id="47d58-286">Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="47d58-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

