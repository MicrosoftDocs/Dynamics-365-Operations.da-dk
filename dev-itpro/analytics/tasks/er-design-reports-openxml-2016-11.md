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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 51208cbc5118e95fd402cca3cbc228ef1b87a47f
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="af720-103">Designe en konfiguration til generering af rapporter i OpenXML-format til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="af720-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af720-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="af720-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="af720-105">Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="af720-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="af720-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="af720-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="af720-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="af720-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="af720-108">Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen.</span><span class="sxs-lookup"><span data-stu-id="af720-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="af720-109">Denne fil kan åbnes fra: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="af720-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="af720-110">Overføre konfiguration for betalingsdatamodel</span><span class="sxs-lookup"><span data-stu-id="af720-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="af720-111">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="af720-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="af720-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="af720-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="af720-113">Vælg konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="af720-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="af720-114">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="af720-114">Click Set active.</span></span>
4. <span data-ttu-id="af720-115">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="af720-115">Click Repositories.</span></span>
    * <span data-ttu-id="af720-116">Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="af720-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="af720-117">Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="af720-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="af720-118">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="af720-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="af720-119">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="af720-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="af720-120">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="af720-120">Click Create repository.</span></span>
8. <span data-ttu-id="af720-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="af720-121">Click OK.</span></span>
9. <span data-ttu-id="af720-122">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="af720-122">Click Open.</span></span>
10. <span data-ttu-id="af720-123">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="af720-124">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="af720-124">Click Import.</span></span>
    * <span data-ttu-id="af720-125">Importér denne datamodel.</span><span class="sxs-lookup"><span data-stu-id="af720-125">Import this data model.</span></span> <span data-ttu-id="af720-126">Den bruges som en datakilde i en ny formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="af720-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="af720-127">Spring dette trin over, hvis denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="af720-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="af720-128">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="af720-128">Click Yes.</span></span>
13. <span data-ttu-id="af720-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-129">Close the page.</span></span>
14. <span data-ttu-id="af720-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="af720-131">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="af720-131">Create a new format configuration</span></span>
1. <span data-ttu-id="af720-132">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="af720-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="af720-133">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="af720-134">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="af720-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="af720-135">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="af720-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="af720-136">Opret et format, der er baseret på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="af720-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="af720-137">Skriv 'Eksempel på regnearksrapport' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="af720-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="af720-138">Eksempel på regnearksrapport</span><span class="sxs-lookup"><span data-stu-id="af720-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="af720-139">Skriv 'Eksempel på regnearksrapport for kreditorers betalinger' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="af720-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="af720-140">Eksempel på regnearksrapport for kreditorers betalinger</span><span class="sxs-lookup"><span data-stu-id="af720-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="af720-141">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="af720-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="af720-142">Vælg 'CustomerCreditTransferInitiation'-definitionen.</span><span class="sxs-lookup"><span data-stu-id="af720-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="af720-143">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="af720-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="af720-144">Designe et nyt dokument i OPENXML-regnearksformat</span><span class="sxs-lookup"><span data-stu-id="af720-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="af720-145">Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="af720-146">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="af720-146">Click Designer.</span></span>
3. <span data-ttu-id="af720-147">Klik på Importér i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="af720-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="af720-148">Klik på Importér fra Excel.</span><span class="sxs-lookup"><span data-stu-id="af720-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="af720-149">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="af720-149">Click Attachments.</span></span>
    * <span data-ttu-id="af720-150">Vedhæft det eksisterende Excel-dokument som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="af720-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="af720-151">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="af720-151">Click New.</span></span>
7. <span data-ttu-id="af720-152">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="af720-152">Click File.</span></span>
    * <span data-ttu-id="af720-153">Peg på den eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="af720-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="af720-154">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-154">Close the page.</span></span>
9. <span data-ttu-id="af720-155">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="af720-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="af720-156">Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.</span><span class="sxs-lookup"><span data-stu-id="af720-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="af720-157">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="af720-157">Click OK.</span></span>
    * <span data-ttu-id="af720-158">Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).</span><span class="sxs-lookup"><span data-stu-id="af720-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="af720-159">Oprette en ny datakilde for at beregne totaler efter valutakoder</span><span class="sxs-lookup"><span data-stu-id="af720-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="af720-160">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="af720-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="af720-161">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="af720-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="af720-162">Vælg 'Funktioner\Gruppér efter' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="af720-163">Skriv 'PaymentByCurrency' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="af720-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="af720-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="af720-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="af720-165">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="af720-165">Click Edit group by.</span></span>
6. <span data-ttu-id="af720-166">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="af720-167">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="af720-168">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="af720-168">Click Add field to.</span></span>
9. <span data-ttu-id="af720-169">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="af720-169">Click What to group.</span></span>
10. <span data-ttu-id="af720-170">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="af720-171">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="af720-172">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="af720-172">Click Add field to.</span></span>
13. <span data-ttu-id="af720-173">Klik på Grupperede felter.</span><span class="sxs-lookup"><span data-stu-id="af720-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="af720-174">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="af720-175">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="af720-175">Click Add field to.</span></span>
16. <span data-ttu-id="af720-176">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="af720-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="af720-177">Vælg en indstilling i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="af720-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="af720-178">Vælg sammenlægningsfunktionen SUM.</span><span class="sxs-lookup"><span data-stu-id="af720-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="af720-179">Skriv 'TotalInstructuredAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="af720-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="af720-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="af720-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="af720-181">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="af720-181">Click Save.</span></span>
20. <span data-ttu-id="af720-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-182">Close the page.</span></span>
21. <span data-ttu-id="af720-183">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="af720-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="af720-184">Knytte formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="af720-184">Map format components to data sources</span></span>
1. <span data-ttu-id="af720-185">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="af720-186">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="af720-187">Udvid 'model\Betalinger\Initierende part(InitiatingParty)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="af720-188">Vælg 'model\Betalinger\Initierende part(InitiatingParty)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="af720-189">Udvid "Excel\ReportHeader" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="af720-190">Vælg "Excel\ReportHeader\CompanyName" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="af720-191">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-191">Click Bind.</span></span>
8. <span data-ttu-id="af720-192">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="af720-193">Udvid 'model\Betalinger\Kreditor\Identifikation' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="af720-194">Vælg 'model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="af720-195">Udvid "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="af720-196">Vælg "Excel\PaymLines\VendAccountName" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="af720-197">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-197">Click Bind.</span></span>
14. <span data-ttu-id="af720-198">Vælg "model\Betalinger\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="af720-199">Vælg "Excel\PaymLines\VendName" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="af720-200">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-200">Click Bind.</span></span>
17. <span data-ttu-id="af720-201">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="af720-202">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="af720-203">Vælg "Excel\PaymLines\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="af720-204">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-204">Click Bind.</span></span>
21. <span data-ttu-id="af720-205">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="af720-206">Vælg "Excel\PaymLines\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="af720-207">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-207">Click Bind.</span></span>
24. <span data-ttu-id="af720-208">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="af720-209">Udvid 'model\Payments\Creditor Account(CreditorAccount)\Identification' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="af720-210">Vælg 'model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\IBAN' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="af720-211">Vælg "Excel\PaymLines\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="af720-212">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-212">Click Bind.</span></span>
29. <span data-ttu-id="af720-213">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="af720-214">Vælg "Excel\PaymLines\Debit" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="af720-215">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-215">Click Bind.</span></span>
32. <span data-ttu-id="af720-216">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="af720-217">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="af720-218">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="af720-219">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="af720-220">Vælg "Excel\PaymLines\Currency" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="af720-221">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-221">Click Bind.</span></span>
38. <span data-ttu-id="af720-222">Udvid 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="af720-223">Udvid 'PaymentByCurrency\grouped' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="af720-224">Vælg 'PaymentByCurrency\grouped\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="af720-225">Udvid "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="af720-226">Vælg "Excel\SummaryLines\SummaryCurrency" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="af720-227">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-227">Click Bind.</span></span>
44. <span data-ttu-id="af720-228">Udvid 'PaymentByCurrency\aggregated' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="af720-229">Vælg 'PaymentByCurrency\aggregated\TotalInstructuredAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="af720-230">Vælg "Excel\SummaryLines\SummaryAmount" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="af720-231">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-231">Click Bind.</span></span>
48. <span data-ttu-id="af720-232">Vælg 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="af720-233">Vælg "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="af720-234">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-234">Click Bind.</span></span>
51. <span data-ttu-id="af720-235">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="af720-236">Vælg "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="af720-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="af720-237">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="af720-237">Click Bind.</span></span>
54. <span data-ttu-id="af720-238">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="af720-238">Click Save.</span></span>
55. <span data-ttu-id="af720-239">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="af720-240">Bruge den oprettede konfiguration til behandling af betalinger</span><span class="sxs-lookup"><span data-stu-id="af720-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="af720-241">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="af720-241">Click Change status.</span></span>
2. <span data-ttu-id="af720-242">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="af720-242">Click Complete.</span></span>
3. <span data-ttu-id="af720-243">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="af720-243">Click OK.</span></span>
4. <span data-ttu-id="af720-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-244">Close the page.</span></span>
5. <span data-ttu-id="af720-245">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-245">Close the page.</span></span>
6. <span data-ttu-id="af720-246">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="af720-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="af720-247">Brug Quick Filter til at filtrere på feltet Betalingsmåde med værdien "Elektronisk".</span><span class="sxs-lookup"><span data-stu-id="af720-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="af720-248">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="af720-248">Electronic</span></span>  
8. <span data-ttu-id="af720-249">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="af720-249">Click Edit.</span></span>
9. <span data-ttu-id="af720-250">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="af720-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="af720-251">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="af720-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="af720-252">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="af720-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="af720-253">Vælg konfigurationen 'Eksempel på regnearksrapport'.</span><span class="sxs-lookup"><span data-stu-id="af720-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="af720-254">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="af720-254">Click Save.</span></span>
13. <span data-ttu-id="af720-255">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="af720-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="af720-256">Bruge den oprettede konfiguration til at teste betalingskladdebehandling</span><span class="sxs-lookup"><span data-stu-id="af720-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="af720-257">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="af720-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="af720-258">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="af720-258">Click New.</span></span>
    * <span data-ttu-id="af720-259">Opret en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="af720-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="af720-260">Skriv VendPay i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="af720-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="af720-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="af720-261">VendPay</span></span>  
4. <span data-ttu-id="af720-262">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="af720-262">Click Lines.</span></span>
5. <span data-ttu-id="af720-263">I feltet Konto skal du angive værdierne 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="af720-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="af720-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="af720-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="af720-265">Angiv Debet til '1000'.</span><span class="sxs-lookup"><span data-stu-id="af720-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="af720-266">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="af720-266">Click New.</span></span>
8. <span data-ttu-id="af720-267">I feltet Konto skal du angive værdierne 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="af720-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="af720-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="af720-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="af720-269">Angiv Debet til '2000'.</span><span class="sxs-lookup"><span data-stu-id="af720-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="af720-270">Skriv 'EUR' i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="af720-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="af720-271">EUR</span><span class="sxs-lookup"><span data-stu-id="af720-271">EUR</span></span>  
11. <span data-ttu-id="af720-272">I feltet Modkonto skal du angive værdierne 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="af720-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="af720-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="af720-273">GBSI OPER</span></span>  
12. <span data-ttu-id="af720-274">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="af720-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="af720-275">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="af720-275">Electronic</span></span>  
13. <span data-ttu-id="af720-276">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="af720-276">Click Save.</span></span>
14. <span data-ttu-id="af720-277">Klik på Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="af720-277">Click Generate payments.</span></span>
15. <span data-ttu-id="af720-278">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="af720-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="af720-279">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="af720-279">Electronic</span></span>  
16. <span data-ttu-id="af720-280">Skriv "Betalinger" i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="af720-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="af720-281">Skriv f.eks. Betalinger.</span><span class="sxs-lookup"><span data-stu-id="af720-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="af720-282">Skriv 'GBSI OPER' i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="af720-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="af720-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="af720-283">GBSI OPER</span></span>  
18. <span data-ttu-id="af720-284">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="af720-284">Click OK.</span></span>
19. <span data-ttu-id="af720-285">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="af720-285">Click OK.</span></span>
    * <span data-ttu-id="af720-286">Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="af720-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


