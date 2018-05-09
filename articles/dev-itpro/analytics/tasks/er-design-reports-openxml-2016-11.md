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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d410e49e2248e503c5935a0d7e95b63a8381a6a8
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="4d384-103">Designe en konfiguration til generering af rapporter i OpenXML-format til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="4d384-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d384-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="4d384-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="4d384-105">Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="4d384-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="4d384-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="4d384-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="4d384-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="4d384-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="4d384-108">Du skal også hente og gemme Microsoft Excel-filen, [Skabelon for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="4d384-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="4d384-109">Overføre konfiguration for betalingsdatamodel</span><span class="sxs-lookup"><span data-stu-id="4d384-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="4d384-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="4d384-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4d384-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4d384-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4d384-112">Vælg konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="4d384-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="4d384-113">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="4d384-113">Click Set active.</span></span>
4. <span data-ttu-id="4d384-114">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="4d384-114">Click Repositories.</span></span>
    * <span data-ttu-id="4d384-115">Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="4d384-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="4d384-116">Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="4d384-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="4d384-117">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4d384-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="4d384-118">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="4d384-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="4d384-119">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="4d384-119">Click Create repository.</span></span>
8. <span data-ttu-id="4d384-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4d384-120">Click OK.</span></span>
9. <span data-ttu-id="4d384-121">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="4d384-121">Click Open.</span></span>
10. <span data-ttu-id="4d384-122">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="4d384-123">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="4d384-123">Click Import.</span></span>
    * <span data-ttu-id="4d384-124">Importér denne datamodel.</span><span class="sxs-lookup"><span data-stu-id="4d384-124">Import this data model.</span></span> <span data-ttu-id="4d384-125">Den bruges som en datakilde i en ny formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d384-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="4d384-126">Spring dette trin over, hvis denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="4d384-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="4d384-127">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="4d384-127">Click Yes.</span></span>
13. <span data-ttu-id="4d384-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-128">Close the page.</span></span>
14. <span data-ttu-id="4d384-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="4d384-130">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4d384-130">Create a new format configuration</span></span>
1. <span data-ttu-id="4d384-131">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="4d384-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="4d384-132">Vælg 'Betalingsmodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="4d384-133">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4d384-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="4d384-134">Skriv "Format baseret på datamodel PaymentModel" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="4d384-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="4d384-135">Opret et format, der er baseret på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="4d384-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="4d384-136">Skriv 'Eksempel på regnearksrapport' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="4d384-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="4d384-137">Eksempel på regnearksrapport</span><span class="sxs-lookup"><span data-stu-id="4d384-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="4d384-138">Skriv 'Eksempel på regnearksrapport for kreditorers betalinger' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4d384-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="4d384-139">Eksempel på regnearksrapport for kreditorers betalinger</span><span class="sxs-lookup"><span data-stu-id="4d384-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="4d384-140">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="4d384-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="4d384-141">Vælg 'CustomerCreditTransferInitiation'-definitionen.</span><span class="sxs-lookup"><span data-stu-id="4d384-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="4d384-142">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d384-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="4d384-143">Designe et nyt dokument i OPENXML-regnearksformat</span><span class="sxs-lookup"><span data-stu-id="4d384-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="4d384-144">Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="4d384-145">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="4d384-145">Click Designer.</span></span>
3. <span data-ttu-id="4d384-146">Klik på Importér i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4d384-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="4d384-147">Klik på Importér fra Excel.</span><span class="sxs-lookup"><span data-stu-id="4d384-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="4d384-148">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="4d384-148">Click Attachments.</span></span>
    * <span data-ttu-id="4d384-149">Vedhæft det eksisterende Excel-dokument som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="4d384-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="4d384-150">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4d384-150">Click New.</span></span>
7. <span data-ttu-id="4d384-151">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="4d384-151">Click File.</span></span>
    * <span data-ttu-id="4d384-152">Peg på den eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="4d384-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="4d384-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-153">Close the page.</span></span>
9. <span data-ttu-id="4d384-154">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="4d384-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="4d384-155">Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.</span><span class="sxs-lookup"><span data-stu-id="4d384-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="4d384-156">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4d384-156">Click OK.</span></span>
    * <span data-ttu-id="4d384-157">Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).</span><span class="sxs-lookup"><span data-stu-id="4d384-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="4d384-158">Oprette en ny datakilde for at beregne totaler efter valutakoder</span><span class="sxs-lookup"><span data-stu-id="4d384-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="4d384-159">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="4d384-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="4d384-160">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="4d384-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="4d384-161">Vælg 'Funktioner\Gruppér efter' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="4d384-162">Skriv 'PaymentByCurrency' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="4d384-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="4d384-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="4d384-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="4d384-164">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="4d384-164">Click Edit group by.</span></span>
6. <span data-ttu-id="4d384-165">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="4d384-166">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="4d384-167">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="4d384-167">Click Add field to.</span></span>
9. <span data-ttu-id="4d384-168">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="4d384-168">Click What to group.</span></span>
10. <span data-ttu-id="4d384-169">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="4d384-170">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="4d384-171">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="4d384-171">Click Add field to.</span></span>
13. <span data-ttu-id="4d384-172">Klik på Grupperede felter.</span><span class="sxs-lookup"><span data-stu-id="4d384-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="4d384-173">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="4d384-174">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="4d384-174">Click Add field to.</span></span>
16. <span data-ttu-id="4d384-175">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="4d384-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="4d384-176">Vælg en indstilling i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="4d384-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="4d384-177">Vælg sammenlægningsfunktionen SUM.</span><span class="sxs-lookup"><span data-stu-id="4d384-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="4d384-178">Skriv 'TotalInstructuredAmount' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="4d384-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="4d384-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="4d384-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="4d384-180">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4d384-180">Click Save.</span></span>
20. <span data-ttu-id="4d384-181">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-181">Close the page.</span></span>
21. <span data-ttu-id="4d384-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4d384-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="4d384-183">Knytte formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="4d384-183">Map format components to data sources</span></span>
1. <span data-ttu-id="4d384-184">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="4d384-185">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="4d384-186">Udvid 'model\Betalinger\Initierende part(InitiatingParty)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="4d384-187">Vælg 'model\Betalinger\Initierende part(InitiatingParty)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="4d384-188">Udvid "Excel\ReportHeader" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="4d384-189">Vælg "Excel\ReportHeader\CompanyName" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="4d384-190">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-190">Click Bind.</span></span>
8. <span data-ttu-id="4d384-191">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="4d384-192">Udvid 'model\Betalinger\Kreditor\Identifikation' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="4d384-193">Vælg 'model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="4d384-194">Udvid "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="4d384-195">Vælg "Excel\PaymLines\VendAccountName" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="4d384-196">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-196">Click Bind.</span></span>
14. <span data-ttu-id="4d384-197">Vælg "model\Betalinger\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="4d384-198">Vælg "Excel\PaymLines\VendName" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="4d384-199">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-199">Click Bind.</span></span>
17. <span data-ttu-id="4d384-200">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="4d384-201">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="4d384-202">Vælg "Excel\PaymLines\Bank" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="4d384-203">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-203">Click Bind.</span></span>
21. <span data-ttu-id="4d384-204">Vælg 'model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="4d384-205">Vælg "Excel\PaymLines\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="4d384-206">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-206">Click Bind.</span></span>
24. <span data-ttu-id="4d384-207">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="4d384-208">Udvid 'model\Payments\Creditor Account(CreditorAccount)\Identification' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="4d384-209">Vælg 'model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\IBAN' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="4d384-210">Vælg "Excel\PaymLines\AccountNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="4d384-211">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-211">Click Bind.</span></span>
29. <span data-ttu-id="4d384-212">Vælg 'model\Betalinger\Instrueret beløb(InstructedAmount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="4d384-213">Vælg "Excel\PaymLines\Debit" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="4d384-214">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-214">Click Bind.</span></span>
32. <span data-ttu-id="4d384-215">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="4d384-216">Udvid 'model\Payments\Creditor Account(CreditorAccount)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="4d384-217">Udvid 'model\Betalinger\Kreditagent(CreditorAgent)' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="4d384-218">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="4d384-219">Vælg "Excel\PaymLines\Currency" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="4d384-220">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-220">Click Bind.</span></span>
38. <span data-ttu-id="4d384-221">Udvid 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="4d384-222">Udvid 'PaymentByCurrency\grouped' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="4d384-223">Vælg 'PaymentByCurrency\grouped\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="4d384-224">Udvid "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="4d384-225">Vælg "Excel\SummaryLines\SummaryCurrency" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="4d384-226">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-226">Click Bind.</span></span>
44. <span data-ttu-id="4d384-227">Udvid 'PaymentByCurrency\aggregated' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="4d384-228">Vælg 'PaymentByCurrency\aggregated\TotalInstructuredAmount' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="4d384-229">Vælg "Excel\SummaryLines\SummaryAmount" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="4d384-230">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-230">Click Bind.</span></span>
48. <span data-ttu-id="4d384-231">Vælg 'PaymentByCurrency' i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="4d384-232">Vælg "Excel\SummaryLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="4d384-233">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-233">Click Bind.</span></span>
51. <span data-ttu-id="4d384-234">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="4d384-235">Vælg "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="4d384-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="4d384-236">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="4d384-236">Click Bind.</span></span>
54. <span data-ttu-id="4d384-237">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4d384-237">Click Save.</span></span>
55. <span data-ttu-id="4d384-238">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="4d384-239">Bruge den oprettede konfiguration til behandling af betalinger</span><span class="sxs-lookup"><span data-stu-id="4d384-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="4d384-240">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="4d384-240">Click Change status.</span></span>
2. <span data-ttu-id="4d384-241">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="4d384-241">Click Complete.</span></span>
3. <span data-ttu-id="4d384-242">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4d384-242">Click OK.</span></span>
4. <span data-ttu-id="4d384-243">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-243">Close the page.</span></span>
5. <span data-ttu-id="4d384-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-244">Close the page.</span></span>
6. <span data-ttu-id="4d384-245">Gå til Kreditor > Opsætning af betaling > Betalingsmåder.</span><span class="sxs-lookup"><span data-stu-id="4d384-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="4d384-246">Brug Quick Filter til at filtrere på feltet Betalingsmåde med værdien "Elektronisk".</span><span class="sxs-lookup"><span data-stu-id="4d384-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="4d384-247">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="4d384-247">Electronic</span></span>  
8. <span data-ttu-id="4d384-248">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="4d384-248">Click Edit.</span></span>
9. <span data-ttu-id="4d384-249">Udvid sektionen Filformater.</span><span class="sxs-lookup"><span data-stu-id="4d384-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="4d384-250">Vælg Ja i feltet Generisk elektronisk indberetning.</span><span class="sxs-lookup"><span data-stu-id="4d384-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="4d384-251">Skriv eller vælg en værdi i feltet Eksportér formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d384-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="4d384-252">Vælg konfigurationen 'Eksempel på regnearksrapport'.</span><span class="sxs-lookup"><span data-stu-id="4d384-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="4d384-253">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4d384-253">Click Save.</span></span>
13. <span data-ttu-id="4d384-254">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4d384-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="4d384-255">Bruge den oprettede konfiguration til at teste betalingskladdebehandling</span><span class="sxs-lookup"><span data-stu-id="4d384-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="4d384-256">Gå til Kreditor > Betalinger > Betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="4d384-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="4d384-257">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4d384-257">Click New.</span></span>
    * <span data-ttu-id="4d384-258">Opret en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="4d384-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="4d384-259">Skriv VendPay i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="4d384-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="4d384-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="4d384-260">VendPay</span></span>  
4. <span data-ttu-id="4d384-261">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="4d384-261">Click Lines.</span></span>
5. <span data-ttu-id="4d384-262">I feltet Konto skal du angive værdierne 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="4d384-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="4d384-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="4d384-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="4d384-264">Angiv Debet til '1000'.</span><span class="sxs-lookup"><span data-stu-id="4d384-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="4d384-265">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4d384-265">Click New.</span></span>
8. <span data-ttu-id="4d384-266">I feltet Konto skal du angive værdierne 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="4d384-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="4d384-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="4d384-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="4d384-268">Angiv Debet til '2000'.</span><span class="sxs-lookup"><span data-stu-id="4d384-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="4d384-269">Skriv 'EUR' i feltet Valuta.</span><span class="sxs-lookup"><span data-stu-id="4d384-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="4d384-270">EUR</span><span class="sxs-lookup"><span data-stu-id="4d384-270">EUR</span></span>  
11. <span data-ttu-id="4d384-271">I feltet Modkonto skal du angive værdierne 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="4d384-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="4d384-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="4d384-272">GBSI OPER</span></span>  
12. <span data-ttu-id="4d384-273">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="4d384-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="4d384-274">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="4d384-274">Electronic</span></span>  
13. <span data-ttu-id="4d384-275">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4d384-275">Click Save.</span></span>
14. <span data-ttu-id="4d384-276">Klik på Generer betalinger.</span><span class="sxs-lookup"><span data-stu-id="4d384-276">Click Generate payments.</span></span>
15. <span data-ttu-id="4d384-277">Skriv 'Elektronisk' i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="4d384-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="4d384-278">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="4d384-278">Electronic</span></span>  
16. <span data-ttu-id="4d384-279">Skriv "Betalinger" i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="4d384-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="4d384-280">Skriv f.eks. Betalinger.</span><span class="sxs-lookup"><span data-stu-id="4d384-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="4d384-281">Skriv 'GBSI OPER' i feltet Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="4d384-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="4d384-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="4d384-282">GBSI OPER</span></span>  
18. <span data-ttu-id="4d384-283">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4d384-283">Click OK.</span></span>
19. <span data-ttu-id="4d384-284">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4d384-284">Click OK.</span></span>
    * <span data-ttu-id="4d384-285">Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="4d384-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


