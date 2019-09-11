---
title: Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)
description: Dette emne beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
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
ms.openlocfilehash: d1229c89f43f9ded955dadf2f4d87825c9ab4e71
ms.sourcegitcommit: e552111e148a80544a3468da60ea0464f02a658d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/15/2019
ms.locfileid: "1875266"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="e76e9-103">Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)</span><span class="sxs-lookup"><span data-stu-id="e76e9-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e76e9-104">Dette emne beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="e76e9-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="e76e9-105">Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="e76e9-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="e76e9-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="e76e9-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="e76e9-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="e76e9-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="e76e9-108">Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e76e9-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="e76e9-109">Denne fil kan åbnes fra [Skabelon for betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="e76e9-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="e76e9-110">Overføre konfiguration for betalingsdatamodel</span><span class="sxs-lookup"><span data-stu-id="e76e9-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="e76e9-111">Gå i navigationsruden til **Moduler > Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="e76e9-112">Markér konfigurationsudbyderen for eksempelvirksomheden Litware, Inc på listen. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren [Oprette en konfigurationsudbyder og markere den som aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e76e9-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="e76e9-113">Vælg **Angiv aktive**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-113">Select **Set active**.</span></span>
4. <span data-ttu-id="e76e9-114">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-114">Select **Repositories**.</span></span> <span data-ttu-id="e76e9-115">Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="e76e9-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="e76e9-116">Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="e76e9-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="e76e9-117">Vælg **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e76e9-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="e76e9-118">Skriv `Operations resourcesdd` i feltet **Konfigurationslagertype**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="e76e9-119">Vælg **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="e76e9-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-120">Select **OK**.</span></span>
9. <span data-ttu-id="e76e9-121">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-121">Select **Open**.</span></span>
10. <span data-ttu-id="e76e9-122">Vælg **Betalingsmodel** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="e76e9-123">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-123">Select **Import**.</span></span> <span data-ttu-id="e76e9-124">Importér denne datamodel.</span><span class="sxs-lookup"><span data-stu-id="e76e9-124">Import this data model.</span></span> <span data-ttu-id="e76e9-125">Den bruges som en datakilde i en ny formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e76e9-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="e76e9-126">Spring dette trin over, hvis denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="e76e9-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="e76e9-127">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-127">Select **Yes**.</span></span>
13. <span data-ttu-id="e76e9-128">Luk siderne, indtil du vender tilbage til den elektroniske rapporteringsside.</span><span class="sxs-lookup"><span data-stu-id="e76e9-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="e76e9-129">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e76e9-129">Create a new format configuration</span></span>
1. <span data-ttu-id="e76e9-130">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="e76e9-131">Vælg **Betalingsmodel** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="e76e9-132">Vælg **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e76e9-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="e76e9-133">Angiv `Format based on data model PaymentModel` i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="e76e9-134">Opret et format, der er baseret på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="e76e9-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="e76e9-135">Skriv `Sample worksheet report` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="e76e9-136">Eksempel på regnearksrapport</span><span class="sxs-lookup"><span data-stu-id="e76e9-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="e76e9-137">Skriv `Sample worksheet report for vendors’ payments` i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-137">In the **Description** field, type `Sample worksheet report for vendors’ payments`.</span></span> <span data-ttu-id="e76e9-138">Eksempel på regnearksrapport for kreditorers betalinger</span><span class="sxs-lookup"><span data-stu-id="e76e9-138">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="e76e9-139">Indtast eller vælg en værdi i feltet **Definition af datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="e76e9-140">Vælg definitionen **CustomerCreditTransferInitiation**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="e76e9-141">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="e76e9-142">Designe et nyt dokument i OPENXML-regnearksformat</span><span class="sxs-lookup"><span data-stu-id="e76e9-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="e76e9-143">Vælg **Betalingsmodel\Eksempel på regnearksrapport** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="e76e9-144">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-144">Select **Designer**.</span></span>
3. <span data-ttu-id="e76e9-145">Vælg **Importér** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e76e9-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="e76e9-146">Vælg **Importér fra Excel**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="e76e9-147">Vælg **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-147">Select **Attachments**.</span></span> <span data-ttu-id="e76e9-148">Vedhæft det eksisterende Excel-dokument som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="e76e9-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="e76e9-149">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-149">Select **New**.</span></span>
7. <span data-ttu-id="e76e9-150">Vælg **Fil**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-150">Select **File**.</span></span> <span data-ttu-id="e76e9-151">Peg på den eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="e76e9-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="e76e9-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e76e9-152">Close the page.</span></span>
9. <span data-ttu-id="e76e9-153">Indtast eller vælg en værdi i feltet **Skabelon**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="e76e9-154">Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.</span><span class="sxs-lookup"><span data-stu-id="e76e9-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="e76e9-155">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-155">Select **OK**.</span></span> <span data-ttu-id="e76e9-156">Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).</span><span class="sxs-lookup"><span data-stu-id="e76e9-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="e76e9-157">Oprette en ny datakilde for at beregne totaler efter valutakoder</span><span class="sxs-lookup"><span data-stu-id="e76e9-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="e76e9-158">Vælg fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="e76e9-159">Vælg **Tilføj rod** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e76e9-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="e76e9-160">Vælg **Funktioner\Gruppér efter** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="e76e9-161">Skriv `PaymentByCurrency` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="e76e9-162">Vælg **Rediger gruppe efter**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="e76e9-163">Udvid **model** i træet, og vælg derefter **model\Betalinger**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="e76e9-164">Vælg **Føj felt til**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="e76e9-165">Vælg **Hvad skal grupperes**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-165">Select **What to group**.</span></span>
9. <span data-ttu-id="e76e9-166">Udvid **model\Betalinger** i træet, og vælg derefter **model\Betalinger\Valuta**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="e76e9-167">Vælg **Føj felt til**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="e76e9-168">Vælg **Grupperede felter**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="e76e9-169">Vælg **model\Betalinger\Instrueret beløb(InstructedAmount)** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="e76e9-170">Vælg **Føj felt til**, og vælg derefter **Aggregeringsfelter**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="e76e9-171">Vælg en indstilling i feltet **Metode**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="e76e9-172">Vælg aggregeringsfunktionen **SUM**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="e76e9-173">Skriv `TotalInstructuredAmount` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="e76e9-174">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-174">Select **Save**.</span></span>
17. <span data-ttu-id="e76e9-175">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e76e9-175">Close the page.</span></span>
18. <span data-ttu-id="e76e9-176">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="e76e9-177">Knytte formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="e76e9-177">Map format components to data sources</span></span>
1. <span data-ttu-id="e76e9-178">Vælg **model\Betalinger\Initierende part(InitiatingParty)\Navn** og **Excel\ReportHeader\CompanyName** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="e76e9-179">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-179">Select **Bind**.</span></span>
3. <span data-ttu-id="e76e9-180">Vælg **model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)** og **Excel\PaymLines\VendAccountName** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="e76e9-181">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-181">Select **Bind**.</span></span>
5. <span data-ttu-id="e76e9-182">Vælg **model\Betalinger\Kreditor\Navn** og **Excel\PaymLines\VendName** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="e76e9-183">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-183">Select **Bind**.</span></span>
7. <span data-ttu-id="e76e9-184">Vælg **model\Betalinger\Kreditagent(CreditorAgent)\Navn** og **Excel\PaymLines\Bank** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="e76e9-185">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-185">Select **Bind**.</span></span>
9. <span data-ttu-id="e76e9-186">Vælg **model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)** og **Excel\PaymLines\RoutingNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="e76e9-187">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-187">Select **Bind**.</span></span>
11. <span data-ttu-id="e76e9-188">Vælg **model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\Nummer** og **Excel\PaymLines\AccountNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="e76e9-189">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-189">Select **Bind**.</span></span>
13. <span data-ttu-id="e76e9-190">Vælg **model\Betalinger\Instrueret beløb(InstructedAmount)** og **Excel\PaymLines\Debit** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="e76e9-191">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-191">Select **Bind**.</span></span>
15. <span data-ttu-id="e76e9-192">Vælg **model\Betalinger\Valuta** og **Excel\PaymLines\Currency** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="e76e9-193">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-193">Select **Bind**.</span></span>
17. <span data-ttu-id="e76e9-194">Vælg **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="e76e9-195">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-195">Select **Bind**.</span></span>
19. <span data-ttu-id="e76e9-196">Vælg **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount**  i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="e76e9-197">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-197">Select **Bind**.</span></span>
21. <span data-ttu-id="e76e9-198">Vælg **PaymentByCurrency** og **Excel\SummaryLines** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="e76e9-199">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-199">Select **Bind**.</span></span>
23. <span data-ttu-id="e76e9-200">Vælg **model\Betalinger** og **Excel\PaymLines** i træet.</span><span class="sxs-lookup"><span data-stu-id="e76e9-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="e76e9-201">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-201">Select **Bind**.</span></span>
25. <span data-ttu-id="e76e9-202">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="e76e9-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="e76e9-203">Bruge den oprettede konfiguration til behandling af betalinger</span><span class="sxs-lookup"><span data-stu-id="e76e9-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="e76e9-204">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-204">Select **Change status**.</span></span>
2. <span data-ttu-id="e76e9-205">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-205">Select **Complete**.</span></span>
3. <span data-ttu-id="e76e9-206">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-206">Select **OK**.</span></span>
4. <span data-ttu-id="e76e9-207">I navigationsruden skal du gå til **Moduler > Kreditor > Betalingsopsætning > Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="e76e9-208">Brug Quick Filter til at filtrere på feltet **Betalingsmåde** med værdien **Elektronisk**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="e76e9-209">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-209">Select **Edit**.</span></span>
7. <span data-ttu-id="e76e9-210">Udvid sektionen **Filformater**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="e76e9-211">Vælg **Ja** i feltet **Generisk elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="e76e9-212">Skriv eller vælg en værdi i feltet **Eksportér formatkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="e76e9-213">Vælg konfigurationen **Eksempel på regnearksrapport**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="e76e9-214">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-214">Select **Save**.</span></span>
11. <span data-ttu-id="e76e9-215">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e76e9-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="e76e9-216">Bruge den oprettede konfiguration til at teste betalingskladdebehandling</span><span class="sxs-lookup"><span data-stu-id="e76e9-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="e76e9-217">Gå i navigationsruden til **Moduler > Kreditorer > Betalinger > Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="e76e9-218">Vælg **Ny** for at oprette en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="e76e9-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="e76e9-219">Skriv **VendPay** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="e76e9-220">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-220">Select **Lines**.</span></span>
5. <span data-ttu-id="e76e9-221">I feltet **Konto** skal du angive værdien `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="e76e9-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="e76e9-222">Angiv **Debet** til `1000`.</span><span class="sxs-lookup"><span data-stu-id="e76e9-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="e76e9-223">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-223">Select **New**.</span></span>
8. <span data-ttu-id="e76e9-224">I feltet **Konto** skal du angive værdien `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="e76e9-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="e76e9-225">Angiv **Debet** til `2000`.</span><span class="sxs-lookup"><span data-stu-id="e76e9-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="e76e9-226">Skriv `EUR` i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="e76e9-227">I feltet **Modkonto** skal du angive værdien `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="e76e9-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="e76e9-228">Skriv `Electronic` i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="e76e9-229">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-229">Select **Save**.</span></span>
14. <span data-ttu-id="e76e9-230">Vælg **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="e76e9-231">Skriv `Electronic` i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="e76e9-232">Skriv `Payments` i feltet **Filnavn**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="e76e9-233">Skriv `GBSI OPER` i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="e76e9-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="e76e9-234">Vælg **OK**, og vælg derefter **OK** igen.</span><span class="sxs-lookup"><span data-stu-id="e76e9-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="e76e9-235">Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="e76e9-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

