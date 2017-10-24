--- 
title: Designe en konfiguration til generering af rapporter i OpenXML-format til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="295a5-103">Designe en konfiguration til generering af rapporter i OpenXML-format til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="295a5-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="295a5-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="295a5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="295a5-105">Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="295a5-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="295a5-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="295a5-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="295a5-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="295a5-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="295a5-108">Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen.</span><span class="sxs-lookup"><span data-stu-id="295a5-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="295a5-109">Denne fil kan åbnes fra: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="295a5-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="295a5-110">Overføre konfiguration for betalingsdatamodel</span><span class="sxs-lookup"><span data-stu-id="295a5-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="295a5-111">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="295a5-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="295a5-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="295a5-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="295a5-113">Vælg konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="295a5-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="295a5-114">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="295a5-114">Click Set active.</span></span>
4. <span data-ttu-id="295a5-115">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="295a5-115">Click Repositories.</span></span>
    * <span data-ttu-id="295a5-116">Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="295a5-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="295a5-117">Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="295a5-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="295a5-118">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="295a5-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="295a5-119">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="295a5-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="295a5-120">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="295a5-120">Click Create repository.</span></span>
8. <span data-ttu-id="295a5-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="295a5-121">Click OK.</span></span>
9. <span data-ttu-id="295a5-122">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="295a5-122">Click Open.</span></span>
10. <span data-ttu-id="295a5-123">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="295a5-124">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="295a5-124">Click Import.</span></span>
    * <span data-ttu-id="295a5-125">Importér denne datamodel.</span><span class="sxs-lookup"><span data-stu-id="295a5-125">Import this data model.</span></span> <span data-ttu-id="295a5-126">Den bruges som en datakilde i en ny formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="295a5-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="295a5-127">Spring dette trin over, hvis denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="295a5-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="295a5-128">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="295a5-128">Click Yes.</span></span>
13. <span data-ttu-id="295a5-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-129">Close the page.</span></span>
14. <span data-ttu-id="295a5-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="295a5-131">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="295a5-131">Create a new format configuration</span></span>
1. <span data-ttu-id="295a5-132">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="295a5-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="295a5-133">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="295a5-134">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="295a5-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="295a5-135">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="295a5-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="295a5-136">Opret et format, der er baseret på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="295a5-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="295a5-137">Skriv 'Eksempel på regnearksrapport' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="295a5-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="295a5-138">Eksempel på regnearksrapport</span><span class="sxs-lookup"><span data-stu-id="295a5-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="295a5-139">Skriv 'Eksempel på regnearksrapport for kreditorers betalinger' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="295a5-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="295a5-140">Eksempel på regnearksrapport for kreditorers betalinger</span><span class="sxs-lookup"><span data-stu-id="295a5-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="295a5-141">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="295a5-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="295a5-142">Vælg 'CustomerCreditTransferInitiation'-definitionen.</span><span class="sxs-lookup"><span data-stu-id="295a5-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="295a5-143">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="295a5-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="295a5-144">Designe et nyt dokument i OPENXML-regnearksformat</span><span class="sxs-lookup"><span data-stu-id="295a5-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="295a5-145">Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="295a5-146">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="295a5-146">Click Designer.</span></span>
3. <span data-ttu-id="295a5-147">Klik på Importér i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="295a5-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="295a5-148">Klik på Importér fra Excel.</span><span class="sxs-lookup"><span data-stu-id="295a5-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="295a5-149">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="295a5-149">Click Attachments.</span></span>
    * <span data-ttu-id="295a5-150">Vedhæft det eksisterende Excel-dokument som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="295a5-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="295a5-151">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="295a5-151">Click New.</span></span>
7. <span data-ttu-id="295a5-152">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="295a5-152">Click File.</span></span>
    * <span data-ttu-id="295a5-153">Peg på den eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="295a5-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="295a5-154">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-154">Close the page.</span></span>
9. <span data-ttu-id="295a5-155">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="295a5-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="295a5-156">Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.</span><span class="sxs-lookup"><span data-stu-id="295a5-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="295a5-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="295a5-157">Click OK.</span></span>
    * <span data-ttu-id="295a5-158">Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).</span><span class="sxs-lookup"><span data-stu-id="295a5-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="295a5-159">Oprette en ny datakilde for at beregne totaler efter valutakoder</span><span class="sxs-lookup"><span data-stu-id="295a5-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="295a5-160">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="295a5-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="295a5-161">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="295a5-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="295a5-162">Vælg 'Funktioner\Gruppér efter' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="295a5-163">Skriv 'PaymentByCurrency' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="295a5-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="295a5-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="295a5-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="295a5-165">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="295a5-165">Click Edit group by.</span></span>
6. <span data-ttu-id="295a5-166">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="295a5-167">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="295a5-168">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="295a5-168">Click Add field to.</span></span>
9. <span data-ttu-id="295a5-169">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="295a5-169">Click What to group.</span></span>
10. <span data-ttu-id="295a5-170">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="295a5-171">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="295a5-172">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="295a5-172">Click Add field to.</span></span>
13. <span data-ttu-id="295a5-173">Klik på Grupperede felter.</span><span class="sxs-lookup"><span data-stu-id="295a5-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="295a5-174">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="295a5-175">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="295a5-175">Click Add field to.</span></span>
16. <span data-ttu-id="295a5-176">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="295a5-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="295a5-177">Vælg en indstilling i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="295a5-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="295a5-178">Vælg sammenlægningsfunktionen SUM.</span><span class="sxs-lookup"><span data-stu-id="295a5-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="295a5-179">Skriv 'TotalInstructuredAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="295a5-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="295a5-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="295a5-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="295a5-181">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="295a5-181">Click Save.</span></span>
20. <span data-ttu-id="295a5-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-182">Close the page.</span></span>
21. <span data-ttu-id="295a5-183">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="295a5-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="295a5-184">Knytte formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="295a5-184">Map format components to data sources</span></span>
1. <span data-ttu-id="295a5-185">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="295a5-186">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="295a5-187">Udvid 'model\Betalinger\Initierende part(InitiatingParty)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="295a5-188">Vælg 'model\Betalinger\Initierende part(InitiatingParty)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="295a5-189">Udvid "Excel\ReportHeader" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="295a5-190">Vælg "Excel\ReportHeader\CompanyName" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="295a5-191">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-191">Click Bind.</span></span>
8. <span data-ttu-id="295a5-192">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="295a5-193">Udvid 'model\Betalinger\Kreditor\Identifikation' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="295a5-194">Vælg 'model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="295a5-195">Udvid "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="295a5-196">Vælg "Excel\PaymLines\VendAccountName" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="295a5-197">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-197">Click Bind.</span></span>
14. <span data-ttu-id="295a5-198">Vælg "model\Betalinger\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="295a5-199">Vælg "Excel\PaymLines\VendName" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="295a5-200">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-200">Click Bind.</span></span>
17. <span data-ttu-id="295a5-201">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="295a5-202">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="295a5-203">Vælg "Excel\PaymLines\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="295a5-204">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-204">Click Bind.</span></span>
21. <span data-ttu-id="295a5-205">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="295a5-206">Vælg "Excel\PaymLines\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="295a5-207">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-207">Click Bind.</span></span>
24. <span data-ttu-id="295a5-208">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="295a5-209">Udvid 'model\Payments\Creditor Account(CreditorAccount)\Identification' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="295a5-210">Vælg 'model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\IBAN' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="295a5-211">Vælg "Excel\PaymLines\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="295a5-212">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-212">Click Bind.</span></span>
29. <span data-ttu-id="295a5-213">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="295a5-214">Vælg "Excel\PaymLines\Debit" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="295a5-215">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-215">Click Bind.</span></span>
32. <span data-ttu-id="295a5-216">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="295a5-217">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="295a5-218">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="295a5-219">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="295a5-220">Vælg "Excel\PaymLines\Currency" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="295a5-221">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-221">Click Bind.</span></span>
38. <span data-ttu-id="295a5-222">Udvid 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="295a5-223">Udvid 'PaymentByCurrency\grouped' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="295a5-224">Vælg 'PaymentByCurrency\grouped\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="295a5-225">Udvid "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="295a5-226">Vælg "Excel\SummaryLines\SummaryCurrency" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="295a5-227">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-227">Click Bind.</span></span>
44. <span data-ttu-id="295a5-228">Udvid 'PaymentByCurrency\aggregated' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="295a5-229">Vælg 'PaymentByCurrency\aggregated\TotalInstructuredAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="295a5-230">Vælg "Excel\SummaryLines\SummaryAmount" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="295a5-231">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-231">Click Bind.</span></span>
48. <span data-ttu-id="295a5-232">Vælg 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="295a5-233">Vælg "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="295a5-234">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-234">Click Bind.</span></span>
51. <span data-ttu-id="295a5-235">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="295a5-236">Vælg "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="295a5-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="295a5-237">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="295a5-237">Click Bind.</span></span>
54. <span data-ttu-id="295a5-238">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="295a5-238">Click Save.</span></span>
55. <span data-ttu-id="295a5-239">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="295a5-240">Bruge den oprettede konfiguration til behandling af betalinger</span><span class="sxs-lookup"><span data-stu-id="295a5-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="295a5-241">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="295a5-241">Click Change status.</span></span>
2. <span data-ttu-id="295a5-242">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="295a5-242">Click Complete.</span></span>
3. <span data-ttu-id="295a5-243">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="295a5-243">Click OK.</span></span>
4. <span data-ttu-id="295a5-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-244">Close the page.</span></span>
5. <span data-ttu-id="295a5-245">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-245">Close the page.</span></span>
6. <span data-ttu-id="295a5-246">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="295a5-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="295a5-247">Brug Quick Filter til at filtrere på feltet Betalingsmåde med værdien "Elektronisk".</span><span class="sxs-lookup"><span data-stu-id="295a5-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="295a5-248">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="295a5-248">Electronic</span></span>  
8. <span data-ttu-id="295a5-249">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="295a5-249">Click Edit.</span></span>
9. <span data-ttu-id="295a5-250">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="295a5-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="295a5-251">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="295a5-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="295a5-252">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="295a5-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="295a5-253">Vælg konfigurationen 'Eksempel på regnearksrapport'.</span><span class="sxs-lookup"><span data-stu-id="295a5-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="295a5-254">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="295a5-254">Click Save.</span></span>
13. <span data-ttu-id="295a5-255">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="295a5-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="295a5-256">Bruge den oprettede konfiguration til at teste betalingskladdebehandling</span><span class="sxs-lookup"><span data-stu-id="295a5-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="295a5-257">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="295a5-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="295a5-258">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="295a5-258">Click New.</span></span>
    * <span data-ttu-id="295a5-259">Opret en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="295a5-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="295a5-260">Skriv VendPay i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="295a5-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="295a5-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="295a5-261">VendPay</span></span>  
4. <span data-ttu-id="295a5-262">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="295a5-262">Click Lines.</span></span>
5. <span data-ttu-id="295a5-263">I feltet Konto skal du angive værdierne 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="295a5-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="295a5-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="295a5-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="295a5-265">Angiv Debet til '1000'.</span><span class="sxs-lookup"><span data-stu-id="295a5-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="295a5-266">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="295a5-266">Click New.</span></span>
8. <span data-ttu-id="295a5-267">I feltet Konto skal du angive værdierne 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="295a5-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="295a5-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="295a5-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="295a5-269">Angiv Debet til '2000'.</span><span class="sxs-lookup"><span data-stu-id="295a5-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="295a5-270">Skriv 'EUR' i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="295a5-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="295a5-271">EUR</span><span class="sxs-lookup"><span data-stu-id="295a5-271">EUR</span></span>  
11. <span data-ttu-id="295a5-272">I feltet Modkonto skal du angive værdierne 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="295a5-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="295a5-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="295a5-273">GBSI OPER</span></span>  
12. <span data-ttu-id="295a5-274">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="295a5-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="295a5-275">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="295a5-275">Electronic</span></span>  
13. <span data-ttu-id="295a5-276">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="295a5-276">Click Save.</span></span>
14. <span data-ttu-id="295a5-277">Klik på Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="295a5-277">Click Generate payments.</span></span>
15. <span data-ttu-id="295a5-278">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="295a5-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="295a5-279">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="295a5-279">Electronic</span></span>  
16. <span data-ttu-id="295a5-280">Skriv "Betalinger" i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="295a5-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="295a5-281">Skriv f.eks. Betalinger.</span><span class="sxs-lookup"><span data-stu-id="295a5-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="295a5-282">Skriv 'GBSI OPER' i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="295a5-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="295a5-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="295a5-283">GBSI OPER</span></span>  
18. <span data-ttu-id="295a5-284">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="295a5-284">Click OK.</span></span>
19. <span data-ttu-id="295a5-285">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="295a5-285">Click OK.</span></span>
    * <span data-ttu-id="295a5-286">Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="295a5-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


