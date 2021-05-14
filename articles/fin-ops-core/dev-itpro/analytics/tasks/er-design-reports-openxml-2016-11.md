---
title: Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)
description: Dette emne beskriver, hvordan du opretter en ny konfiguration af elektronisk rapportering, der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f23748f6f1d2c3045b1dc69d8e46821f67da593
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944262"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="d0715-103">Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)</span><span class="sxs-lookup"><span data-stu-id="d0715-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0715-104">Dette emne beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en skabelon til oprettelse af elektroniske dokumenter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="d0715-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="d0715-105">Denne konfiguration vil blive brugt til behandling af kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="d0715-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="d0715-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="d0715-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="d0715-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="d0715-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="d0715-108">Du skal også have en Excel-fil, der vil blive importeret, når du opretter skabelonen.</span><span class="sxs-lookup"><span data-stu-id="d0715-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="d0715-109">Denne fil kan åbnes fra [Skabelon for betalingsrapport](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).</span><span class="sxs-lookup"><span data-stu-id="d0715-109">This file can be accessed from the [Template of Payment Report](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="d0715-110">Overføre konfiguration for betalingsdatamodel</span><span class="sxs-lookup"><span data-stu-id="d0715-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="d0715-111">Gå i navigationsruden til **Moduler > Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d0715-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="d0715-112">Markér konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. på listen. Hvis du ikke kan se konfigurationsudbyderen, skal du først fuldføre trinnene i proceduren [Oprette konfigurationsudbydere og markere dem som aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d0715-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don't see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="d0715-113">Vælg **Angiv aktive**.</span><span class="sxs-lookup"><span data-stu-id="d0715-113">Select **Set active**.</span></span>
4. <span data-ttu-id="d0715-114">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d0715-114">Select **Repositories**.</span></span> <span data-ttu-id="d0715-115">Vælg et lager for typen Operationsressourcer, hvis det er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="d0715-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="d0715-116">Hvis det er tilgængeligt, skal du springe over dette trin om oprettelse af et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="d0715-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="d0715-117">Vælg **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d0715-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="d0715-118">Skriv `Operations resourcesdd` i feltet **Konfigurationslagertype**.</span><span class="sxs-lookup"><span data-stu-id="d0715-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="d0715-119">Vælg **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="d0715-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="d0715-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0715-120">Select **OK**.</span></span>
9. <span data-ttu-id="d0715-121">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="d0715-121">Select **Open**.</span></span>
10. <span data-ttu-id="d0715-122">Vælg **Betalingsmodel** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="d0715-123">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="d0715-123">Select **Import**.</span></span> <span data-ttu-id="d0715-124">Importér denne datamodel.</span><span class="sxs-lookup"><span data-stu-id="d0715-124">Import this data model.</span></span> <span data-ttu-id="d0715-125">Den bruges som en datakilde i en ny formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d0715-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="d0715-126">Spring dette trin over, hvis denne konfiguration allerede er importeret.</span><span class="sxs-lookup"><span data-stu-id="d0715-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="d0715-127">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d0715-127">Select **Yes**.</span></span>
13. <span data-ttu-id="d0715-128">Luk siderne, indtil du vender tilbage til den elektroniske rapporteringsside.</span><span class="sxs-lookup"><span data-stu-id="d0715-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="d0715-129">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d0715-129">Create a new format configuration</span></span>
1. <span data-ttu-id="d0715-130">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="d0715-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="d0715-131">Vælg **Betalingsmodel** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="d0715-132">Vælg **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d0715-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="d0715-133">Angiv `Format based on data model PaymentModel` i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d0715-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="d0715-134">Opret et format, der er baseret på PaymentModel-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="d0715-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="d0715-135">Skriv `Sample worksheet report` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d0715-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="d0715-136">Eksempel på regnearksrapport</span><span class="sxs-lookup"><span data-stu-id="d0715-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="d0715-137">Skriv `Sample worksheet report for vendors' payments` i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d0715-137">In the **Description** field, type `Sample worksheet report for vendors' payments`.</span></span> <span data-ttu-id="d0715-138">Eksempel på regnearksrapport for kreditorers betalinger.</span><span class="sxs-lookup"><span data-stu-id="d0715-138">Sample worksheet report for vendors' payments.</span></span>  
7. <span data-ttu-id="d0715-139">Indtast eller vælg en værdi i feltet **Definition af datamodel**.</span><span class="sxs-lookup"><span data-stu-id="d0715-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="d0715-140">Vælg definitionen **CustomerCreditTransferInitiation**.</span><span class="sxs-lookup"><span data-stu-id="d0715-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="d0715-141">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d0715-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="d0715-142">Designe et nyt dokument i OPENXML-regnearksformat</span><span class="sxs-lookup"><span data-stu-id="d0715-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="d0715-143">Vælg **Betalingsmodel\Eksempel på regnearksrapport** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="d0715-144">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="d0715-144">Select **Designer**.</span></span>
3. <span data-ttu-id="d0715-145">Vælg **Importér** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d0715-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="d0715-146">Vælg **Importér fra Excel**.</span><span class="sxs-lookup"><span data-stu-id="d0715-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="d0715-147">Vælg **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="d0715-147">Select **Attachments**.</span></span> <span data-ttu-id="d0715-148">Vedhæft det eksisterende Excel-dokument som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="d0715-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="d0715-149">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d0715-149">Select **New**.</span></span>
7. <span data-ttu-id="d0715-150">Vælg **Fil**.</span><span class="sxs-lookup"><span data-stu-id="d0715-150">Select **File**.</span></span> <span data-ttu-id="d0715-151">Peg på den eksisterende Excel-fil.</span><span class="sxs-lookup"><span data-stu-id="d0715-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="d0715-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d0715-152">Close the page.</span></span>
9. <span data-ttu-id="d0715-153">Indtast eller vælg en værdi i feltet **Skabelon**.</span><span class="sxs-lookup"><span data-stu-id="d0715-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="d0715-154">Vælg den vedhæftede Excel-fil, der skal bruges som skabelon.</span><span class="sxs-lookup"><span data-stu-id="d0715-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="d0715-155">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0715-155">Select **OK**.</span></span> <span data-ttu-id="d0715-156">Bemærk, at der er oprettet ER-formatkomponenter i designformatet, som er baseret på strukturen i den henvisende MS Excel-dokument (navngivne områder).</span><span class="sxs-lookup"><span data-stu-id="d0715-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="d0715-157">Oprette en ny datakilde for at beregne totaler efter valutakoder</span><span class="sxs-lookup"><span data-stu-id="d0715-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="d0715-158">Vælg fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="d0715-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="d0715-159">Vælg **Tilføj rod** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d0715-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="d0715-160">Vælg **Funktioner\Gruppér efter** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="d0715-161">Skriv `PaymentByCurrency` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d0715-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="d0715-162">Vælg **Rediger gruppe efter**.</span><span class="sxs-lookup"><span data-stu-id="d0715-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="d0715-163">Udvid **model** i træet, og vælg derefter **model\Betalinger**.</span><span class="sxs-lookup"><span data-stu-id="d0715-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="d0715-164">Vælg **Føj felt til**.</span><span class="sxs-lookup"><span data-stu-id="d0715-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="d0715-165">Vælg **Hvad skal grupperes**.</span><span class="sxs-lookup"><span data-stu-id="d0715-165">Select **What to group**.</span></span>
9. <span data-ttu-id="d0715-166">Udvid **model\Betalinger** i træet, og vælg derefter **model\Betalinger\Valuta**.</span><span class="sxs-lookup"><span data-stu-id="d0715-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="d0715-167">Vælg **Føj felt til**.</span><span class="sxs-lookup"><span data-stu-id="d0715-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="d0715-168">Vælg **Grupperede felter**.</span><span class="sxs-lookup"><span data-stu-id="d0715-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="d0715-169">Vælg **model\Betalinger\Instrueret beløb(InstructedAmount)** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="d0715-170">Vælg **Føj felt til**, og vælg derefter **Aggregeringsfelter**.</span><span class="sxs-lookup"><span data-stu-id="d0715-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="d0715-171">Vælg en indstilling i feltet **Metode**.</span><span class="sxs-lookup"><span data-stu-id="d0715-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="d0715-172">Vælg aggregeringsfunktionen **SUM**.</span><span class="sxs-lookup"><span data-stu-id="d0715-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="d0715-173">Skriv `TotalInstructuredAmount` i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d0715-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="d0715-174">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0715-174">Select **Save**.</span></span>
17. <span data-ttu-id="d0715-175">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d0715-175">Close the page.</span></span>
18. <span data-ttu-id="d0715-176">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0715-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="d0715-177">Knytte formatkomponenter til datakilder</span><span class="sxs-lookup"><span data-stu-id="d0715-177">Map format components to data sources</span></span>
1. <span data-ttu-id="d0715-178">Vælg **model\Betalinger\Initierende part(InitiatingParty)\Navn** og **Excel\ReportHeader\CompanyName** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="d0715-179">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-179">Select **Bind**.</span></span>
3. <span data-ttu-id="d0715-180">Vælg **model\Betalinger\Kreditor\Identifikation\Kilde-id(SourceID)** og **Excel\PaymLines\VendAccountName** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="d0715-181">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-181">Select **Bind**.</span></span>
5. <span data-ttu-id="d0715-182">Vælg **model\Betalinger\Kreditor\Navn** og **Excel\PaymLines\VendName** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="d0715-183">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-183">Select **Bind**.</span></span>
7. <span data-ttu-id="d0715-184">Vælg **model\Betalinger\Kreditagent(CreditorAgent)\Navn** og **Excel\PaymLines\Bank** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="d0715-185">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-185">Select **Bind**.</span></span>
9. <span data-ttu-id="d0715-186">Vælg **model\Betalinger\Kreditagent(CreditorAgent)\Registreringsnummer(RoutingNumber)** og **Excel\PaymLines\RoutingNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="d0715-187">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-187">Select **Bind**.</span></span>
11. <span data-ttu-id="d0715-188">Vælg **model\Betalinger\Kreditkonto(CreditorAccount)\Identifikation\Nummer** og **Excel\PaymLines\AccountNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="d0715-189">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-189">Select **Bind**.</span></span>
13. <span data-ttu-id="d0715-190">Vælg **model\Betalinger\Instrueret beløb(InstructedAmount)** og **Excel\PaymLines\Debit** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="d0715-191">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-191">Select **Bind**.</span></span>
15. <span data-ttu-id="d0715-192">Vælg **model\Betalinger\Valuta** og **Excel\PaymLines\Currency** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="d0715-193">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-193">Select **Bind**.</span></span>
17. <span data-ttu-id="d0715-194">Vælg **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="d0715-195">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-195">Select **Bind**.</span></span>
19. <span data-ttu-id="d0715-196">Vælg **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount**  i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="d0715-197">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-197">Select **Bind**.</span></span>
21. <span data-ttu-id="d0715-198">Vælg **PaymentByCurrency** og **Excel\SummaryLines** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="d0715-199">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-199">Select **Bind**.</span></span>
23. <span data-ttu-id="d0715-200">Vælg **model\Betalinger** og **Excel\PaymLines** i træet.</span><span class="sxs-lookup"><span data-stu-id="d0715-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="d0715-201">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="d0715-201">Select **Bind**.</span></span>
25. <span data-ttu-id="d0715-202">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="d0715-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="d0715-203">Bruge den oprettede konfiguration til behandling af betalinger</span><span class="sxs-lookup"><span data-stu-id="d0715-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="d0715-204">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="d0715-204">Select **Change status**.</span></span>
2. <span data-ttu-id="d0715-205">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="d0715-205">Select **Complete**.</span></span>
3. <span data-ttu-id="d0715-206">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0715-206">Select **OK**.</span></span>
4. <span data-ttu-id="d0715-207">I navigationsruden skal du gå til **Moduler > Kreditor > Betalingsopsætning > Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="d0715-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="d0715-208">Brug Quick Filter til at filtrere på feltet **Betalingsmåde** med værdien **Elektronisk**.</span><span class="sxs-lookup"><span data-stu-id="d0715-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="d0715-209">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d0715-209">Select **Edit**.</span></span>
7. <span data-ttu-id="d0715-210">Udvid sektionen **Filformater**.</span><span class="sxs-lookup"><span data-stu-id="d0715-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="d0715-211">Vælg **Ja** i feltet **Generisk elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="d0715-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="d0715-212">Skriv eller vælg en værdi i feltet **Eksportér formatkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d0715-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="d0715-213">Vælg konfigurationen **Eksempel på regnearksrapport**.</span><span class="sxs-lookup"><span data-stu-id="d0715-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="d0715-214">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0715-214">Select **Save**.</span></span>
11. <span data-ttu-id="d0715-215">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d0715-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="d0715-216">Bruge den oprettede konfiguration til at teste betalingskladdebehandling</span><span class="sxs-lookup"><span data-stu-id="d0715-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="d0715-217">Gå i navigationsruden til **Moduler > Kreditorer > Betalinger > Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="d0715-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="d0715-218">Vælg **Ny** for at oprette en ny betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="d0715-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="d0715-219">Skriv **VendPay** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d0715-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="d0715-220">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="d0715-220">Select **Lines**.</span></span>
5. <span data-ttu-id="d0715-221">I feltet **Konto** skal du angive værdien `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="d0715-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="d0715-222">Angiv **Debet** til `1000`.</span><span class="sxs-lookup"><span data-stu-id="d0715-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="d0715-223">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d0715-223">Select **New**.</span></span>
8. <span data-ttu-id="d0715-224">I feltet **Konto** skal du angive værdien `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="d0715-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="d0715-225">Angiv **Debet** til `2000`.</span><span class="sxs-lookup"><span data-stu-id="d0715-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="d0715-226">Skriv `EUR` i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="d0715-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="d0715-227">I feltet **Modkonto** skal du angive værdien `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="d0715-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="d0715-228">Skriv `Electronic` i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="d0715-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="d0715-229">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d0715-229">Select **Save**.</span></span>
14. <span data-ttu-id="d0715-230">Vælg **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="d0715-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="d0715-231">Skriv `Electronic` i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="d0715-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="d0715-232">Skriv `Payments` i feltet **Filnavn**.</span><span class="sxs-lookup"><span data-stu-id="d0715-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="d0715-233">Skriv `GBSI OPER` i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="d0715-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="d0715-234">Vælg **OK**, og vælg derefter **OK** igen.</span><span class="sxs-lookup"><span data-stu-id="d0715-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="d0715-235">Gennemse det oprettede regneark, herunder oplysninger om betalingslinjer samt totaler for hver valutakode, der bruges i denne betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="d0715-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
