---
title: Automatisere test med elektronisk rapportering
description: I dette emne forklares det, hvordan du kan bruge grundlagsfunktionen for elektronisk rapporteringsstruktur (ER) til at automatisere test af nogle funktioner.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 503d4ca562df5c60ee7c475ac146dffbe0edc0c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569039"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="bde85-103">Automatisere test med elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bde85-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bde85-104">I dette emne forklares det, hvordan du kan bruge den elektroniske rapporteringsstruktur (ER) til at automatisere test af nogle funktioner.</span><span class="sxs-lookup"><span data-stu-id="bde85-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="bde85-105">I eksemplet i dette emne kan du se, hvordan du kan automatisere testen af kreditorbetalingsbehandling.</span><span class="sxs-lookup"><span data-stu-id="bde85-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="bde85-106">Programmet bruger ER-strukturen til at generere betalingsfiler og tilsvarende dokumenter under behandling af leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="bde85-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="bde85-107">ER-strukturen består af en datamodel, modeltilknytninger og formatkomponenter, der understøtter betalingsbehandling af forskellige betalingstyper og generering af dokumenter i forskellige formater.</span><span class="sxs-lookup"><span data-stu-id="bde85-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="bde85-108">Disse komponenter kan downloades fra Microsoft Dynamics Lifecycle Services (LCS) og importeres til forekomsten.</span><span class="sxs-lookup"><span data-stu-id="bde85-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="bde85-109">Du kan også tilpasse de enkelte Microsoft-komponenter og bruge dem som basis for din egen tilpassede komponent.</span><span class="sxs-lookup"><span data-stu-id="bde85-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="bde85-110">Ved at oprette en tilpasset version kan du foretage ændringer, der understøtter bestemte krav.</span><span class="sxs-lookup"><span data-stu-id="bde85-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="bde85-111">Du kan f.eks. justere ER-datamodellen og ER-modeltilknytningen til at få adgang til kundespecifikke programdata, eller du kan ændre et ER-format for at ændre layoutet af et genereret dokument.</span><span class="sxs-lookup"><span data-stu-id="bde85-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="bde85-112">Du kan bruge tilpassede ER-formater til at behandle betalingsfiler, der genererer leverandørbetalinger, og som også skal behandle kontrolrapporter.</span><span class="sxs-lookup"><span data-stu-id="bde85-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="bde85-113">Versionering understøttes i ER-komponenter.</span><span class="sxs-lookup"><span data-stu-id="bde85-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="bde85-114">Microsoft kan derfor levere opdaterede versioner af ER-løsninger til behandling af kreditorbetalinger, og du kan automatisk flette den opdaterede version med den tilpassede komponent ved at rebasere den.</span><span class="sxs-lookup"><span data-stu-id="bde85-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="bde85-115">Du skal dog teste den rebaserede version for at sikre, at den fungerer efter hensigten.</span><span class="sxs-lookup"><span data-stu-id="bde85-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="bde85-116">ER-datamodeller og ER-modeltilknytninger er fælles for mange ER-formater, der bruges til at behandle betalinger af forskellige typer og til at oprette land/område-specifikke betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bde85-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="bde85-117">Derfor er det meget ønskeligt at automatisere test af brugeraccept og integration, så det automatisk udføres i flere virksomheder, men som tager hensyn til land/område-konteksten for hvert af de pågældende destinationsfirmaer, bruger forskellige datasæt osv.</span><span class="sxs-lookup"><span data-stu-id="bde85-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="bde85-118">Du kan finde flere oplysninger om, hvordan du opretter en tilpasset version af et format, der er baseret på det format, du har modtaget fra en konfigurationsudbyder, i [Opgradere dit ER-format ved at bruge en ny basisversion af formatet](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="bde85-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="bde85-119">Nøglebegreber</span><span class="sxs-lookup"><span data-stu-id="bde85-119">Key concepts</span></span>

<span data-ttu-id="bde85-120">Funktionelle superbrugere kan oprette test af brugeraccept og-integration uden at skulle skrive kildekode.</span><span class="sxs-lookup"><span data-stu-id="bde85-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="bde85-121">Brug den grundlæggende ER-funktion til at sammenligne genererede dokumenter med masterkopier.</span><span class="sxs-lookup"><span data-stu-id="bde85-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="bde85-122">Du kan finde flere oplysninger under [Spore genererede rapportresultater og sammenligne dem med basisværdier](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="bde85-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="bde85-123">Brug Arbejdsrutineoptager til at registrere testsager og inkludere basisvurdering.</span><span class="sxs-lookup"><span data-stu-id="bde85-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="bde85-124">Du kan finde flere oplysninger under [Arbejdsrutineoptagerressourcer](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="bde85-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="bde85-125">Gruppér testsager for nødvendige testsituationer.</span><span class="sxs-lookup"><span data-stu-id="bde85-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="bde85-126">Du kan finde flere oplysninger under [Opret og automatiser test af brugeraccept](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="bde85-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="bde85-127">Brug Forretningsmodeldesigner (BPM) i LCS til at oprette biblioteker til test af brugeraccept.</span><span class="sxs-lookup"><span data-stu-id="bde85-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="bde85-128">Brug BPM-testbiblioteker til at oprette en testplan og testpakker i Microsoft Azure DevOps Services (Azure DevOps).</span><span class="sxs-lookup"><span data-stu-id="bde85-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="bde85-129">Funktionelle superbrugere kan køre test af brugeraccept og -integration.</span><span class="sxs-lookup"><span data-stu-id="bde85-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="bde85-130">Brug Regression Suite Automation Tool (RSAT) til at køre testsager af den ønskede testpakke.</span><span class="sxs-lookup"><span data-stu-id="bde85-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="bde85-131">Rapportér resultaterne af testen til Azure DevOps, og brug denne tjeneste til at undersøge disse resultater.</span><span class="sxs-lookup"><span data-stu-id="bde85-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bde85-132">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="bde85-132">Prerequisites</span></span>

<span data-ttu-id="bde85-133">Før du kan fuldføre opgaverne i dette emne, skal du fuldføre følgende forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="bde85-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="bde85-134">Implementer en topologi, der understøtter testautomatisering.</span><span class="sxs-lookup"><span data-stu-id="bde85-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="bde85-135">Du skal have adgang til forekomsten af denne topologi for rollen **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="bde85-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="bde85-136">Denne topologi skal indeholde de demodata, der vil blive brugt i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="bde85-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="bde85-137">Du kan finde flere oplysninger under [Installer og anvend et miljø, som understøtter fortløbende build og automatisering af test](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="bde85-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="bde85-138">Hvis du vil køre test af brugergodkendelse og -integration automatisk, skal du installere RSAT i den topologi, du bruger, og konfigurere den på en passende måde.</span><span class="sxs-lookup"><span data-stu-id="bde85-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="bde85-139">Du kan finde oplysninger om, hvordan du installerer og konfigurerer RSAT og konfigurerer den til at virke sammen Finance and Operations-apps og Azure DevOps, i [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="bde85-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="bde85-140">Vær opmærksom på forudsætningerne for at bruge værktøjet.</span><span class="sxs-lookup"><span data-stu-id="bde85-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="bde85-141">I følgende illustration vises et eksempel på RSAT-indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="bde85-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="bde85-142">Det blå rektangel omgiver de parametre, der er angivet for adgang til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="bde85-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="bde85-143">Det grønne rektangel omgiver de parametre, der angiver adgangen til forekomsten.</span><span class="sxs-lookup"><span data-stu-id="bde85-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="bde85-144">![RSAT-indstillinger](media/GER-Configure.png "Skærmbillede af dialogboksen RSAT-indstillinger")</span><span class="sxs-lookup"><span data-stu-id="bde85-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="bde85-145">Hvis du vil organisere testsager i pakker for at hjælpe med at sikre den korrekte kørselssekvens, så du kan indsamle logfiler med testkørsler til yderligere rapportering og undersøgelse, skal du have adgang til Azure DevOps fra den installerede topologi.</span><span class="sxs-lookup"><span data-stu-id="bde85-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="bde85-146">Hvis du vil fuldføre eksemplet i dette emne, anbefales du at downloade [ER-brug for RSAT-test](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="bde85-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="bde85-147">Denne zip-fil indeholder følgende opgaveguider:</span><span class="sxs-lookup"><span data-stu-id="bde85-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="bde85-148">Indhold</span><span class="sxs-lookup"><span data-stu-id="bde85-148">Content</span></span>                                           | <span data-ttu-id="bde85-149">Filens navn og placering</span><span class="sxs-lookup"><span data-stu-id="bde85-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="bde85-150">Eksempel på opgaveregistrering for at forberede data til test</span><span class="sxs-lookup"><span data-stu-id="bde85-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="bde85-151">Forberede\\Registrering.xml</span><span class="sxs-lookup"><span data-stu-id="bde85-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="bde85-152">Eksempel på opgaveregistrering for at behandle kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="bde85-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="bde85-153">Behandle\\Registrering.xml</span><span class="sxs-lookup"><span data-stu-id="bde85-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="bde85-154">Forberede modulet Kreditor til behandling af kreditorbetalinger</span><span class="sxs-lookup"><span data-stu-id="bde85-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="bde85-155">Log på din forekomst.</span><span class="sxs-lookup"><span data-stu-id="bde85-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="bde85-156">Download følgende ER-konfigurationer fra LCS.</span><span class="sxs-lookup"><span data-stu-id="bde85-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="bde85-157">Der er instruktioner under [Importere ER-konfiguration fra Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="bde85-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="bde85-158">**Betalingsmodel** ER-modelkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="bde85-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="bde85-159">**Betalingsmodel-tilknytning 1611** Konfiguration af ER-modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="bde85-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="bde85-160">**BACS (UK)** ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bde85-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="bde85-161">![Konfigurationer for elektronisk rapportering](media/GER-Configurations.png "Skærmbillede af siden Konfigurationer i elektronisk rapportering")</span><span class="sxs-lookup"><span data-stu-id="bde85-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="bde85-162">Vælg det **GBSI**-demodatafirma, som har en land/område-kontekst i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="bde85-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="bde85-163">Konfigurer kreditorparametre:</span><span class="sxs-lookup"><span data-stu-id="bde85-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="bde85-164">Gå til **Kreditor \> Opsætning af betaling \> Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="bde85-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="bde85-165">Vælg betalingsmetoden **Elektronisk**.</span><span class="sxs-lookup"><span data-stu-id="bde85-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="bde85-166">Konfigurer den valgte betalingsmåde, så den bruger ER-formatet **BACS (UK)**, som du har downloadet tidligere til behandling af kreditorbetalinger:</span><span class="sxs-lookup"><span data-stu-id="bde85-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="bde85-167">Brug oversigtspanelet **Filformater** til at angive indstillingen **Generisk elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bde85-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="bde85-168">Vælg **BACS (UK)** i feltet **Eksportér formatkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="bde85-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="bde85-169">![Side med betalingsmetoder](media/GER-APParameters.png "Skærmbillede af siden Betalingsmetoder")</span><span class="sxs-lookup"><span data-stu-id="bde85-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="bde85-170">Hvis du har den afledte version af dette ER-format, der er oprettet for at understøtte tilpasninger, kan du vælge denne konfiguration i **Elektronisk** betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="bde85-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="bde85-171">Opret et eksempel på en kreditorbetaling:</span><span class="sxs-lookup"><span data-stu-id="bde85-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="bde85-172">Gå til **Kreditor \> Betalinger \> Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="bde85-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="bde85-173">Kontrollér, at du ikke har bogført betalingskladden.</span><span class="sxs-lookup"><span data-stu-id="bde85-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="bde85-174">![Side med betalingskladde](media/GER-APJournal.png "Skærmbillede af siden Betalingskladde")</span><span class="sxs-lookup"><span data-stu-id="bde85-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="bde85-175">Vælg **Linjer**, og angiv en linje med følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="bde85-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="bde85-176">Felt</span><span class="sxs-lookup"><span data-stu-id="bde85-176">Field</span></span>               | <span data-ttu-id="bde85-177">Eksempelværdi</span><span class="sxs-lookup"><span data-stu-id="bde85-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="bde85-178">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="bde85-178">Vendor name</span></span>         | <span data-ttu-id="bde85-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="bde85-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="bde85-180">Debet</span><span class="sxs-lookup"><span data-stu-id="bde85-180">Debit</span></span>               | <span data-ttu-id="bde85-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="bde85-181">1,000.00</span></span>        |
        | <span data-ttu-id="bde85-182">Valuta</span><span class="sxs-lookup"><span data-stu-id="bde85-182">Currency</span></span>            | <span data-ttu-id="bde85-183">GBP</span><span class="sxs-lookup"><span data-stu-id="bde85-183">GBP</span></span>             |
        | <span data-ttu-id="bde85-184">Modkontotype</span><span class="sxs-lookup"><span data-stu-id="bde85-184">Offset account type</span></span> | <span data-ttu-id="bde85-185">Bank</span><span class="sxs-lookup"><span data-stu-id="bde85-185">Bank</span></span>            |
        | <span data-ttu-id="bde85-186">Modkonto</span><span class="sxs-lookup"><span data-stu-id="bde85-186">Offset account</span></span>      | <span data-ttu-id="bde85-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="bde85-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="bde85-188">Betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="bde85-188">Method of payment</span></span>   | <span data-ttu-id="bde85-189">Elektronisk</span><span class="sxs-lookup"><span data-stu-id="bde85-189">Electronic</span></span>      |

    <span data-ttu-id="bde85-190">![Side med leverandørbetalinger](media/GER-APJournalLines.png "Skærmbillede af siden Leverandørbetalinger")</span><span class="sxs-lookup"><span data-stu-id="bde85-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="bde85-191">Forberede ER-strukturen til at teste behandling af kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="bde85-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="bde85-192">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="bde85-192">Configure ER parameters</span></span>

1. <span data-ttu-id="bde85-193">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="bde85-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="bde85-194">Under fanen **Vedhæftede filer** i feltet **Grundlag** skal du vælge **Fil** som den dokumenttype, som dokumentstyringsstrukturen (DM) bruger til at holde på dokumenter, der er relateret til basisfunktionen, som vedhæftede DM-filer.</span><span class="sxs-lookup"><span data-stu-id="bde85-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="bde85-195">![Siden Parametre til elektronisk rapportering](media/GER-ERParameters.png "Skærmbillede af siden Elektroniske rapporteringsparametre")</span><span class="sxs-lookup"><span data-stu-id="bde85-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="bde85-196">Generere basiskopier af kreditorbetaling – relaterede dokumenter</span><span class="sxs-lookup"><span data-stu-id="bde85-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="bde85-197">Gå til **Kreditor \> Betalinger \> Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="bde85-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="bde85-198">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="bde85-198">Select **Lines**.</span></span>
3. <span data-ttu-id="bde85-199">Vælg **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="bde85-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="bde85-200">Vælg betalingsmetoden **Elektronisk**.</span><span class="sxs-lookup"><span data-stu-id="bde85-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="bde85-201">Vælg bankkontoen **GBSI OPER**</span><span class="sxs-lookup"><span data-stu-id="bde85-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="bde85-202">Angiv indstillingen **Udskriv kontrolrapport** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bde85-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="bde85-203">Download det genererede output som en zip-fil.</span><span class="sxs-lookup"><span data-stu-id="bde85-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="bde85-204">Åbn den downloadede fil.</span><span class="sxs-lookup"><span data-stu-id="bde85-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="bde85-205">Udtræk følgende filer fra den downloadede fil:</span><span class="sxs-lookup"><span data-stu-id="bde85-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="bde85-206">**Fil**: betalingsfil i tekstformat</span><span class="sxs-lookup"><span data-stu-id="bde85-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="bde85-207">**ERVendOutPaymControlReport**: kontrolrapportfil i xlsx-format</span><span class="sxs-lookup"><span data-stu-id="bde85-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="bde85-208">![Udpakkede filer](media/GER-APJournalProcessed.png "Skærmbillede af udtrukket filnavne i Windows Stifinder")</span><span class="sxs-lookup"><span data-stu-id="bde85-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="bde85-209">Slå funktionen for ER-grundlag til</span><span class="sxs-lookup"><span data-stu-id="bde85-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="bde85-210">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="bde85-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="bde85-211">I handlingsruden skal du på fanen **Konfigurationer** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="bde85-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="bde85-212">Angv indstillingen **Kør i fejlfindingstilstand** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bde85-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="bde85-213">Når du aktiverer parameteren **Kør i fejlfindingstilstand**, tvinger du ER-strukturen til at udføre følgende handlinger efter udførelse af ethvert ER-format, der genererer udgående dokumenter:</span><span class="sxs-lookup"><span data-stu-id="bde85-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="bde85-214">Bestem, om der er konfigureret et grundlag for nogen af komponenterne i det afviklede ER-format.</span><span class="sxs-lookup"><span data-stu-id="bde85-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="bde85-215">Bestem, om hvert konfigurerede grundlag gælder under de aktuelle betingelser (firmakoden for det firma, der er logget på, og filnavnet og filtypenavnet for det genererede output osv.).</span><span class="sxs-lookup"><span data-stu-id="bde85-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="bde85-216">Udfør følgende handlinger for hvert relevante grundlag:</span><span class="sxs-lookup"><span data-stu-id="bde85-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="bde85-217">Sammenlign det output, der genereres under kørslen af ER-formatet, med det tilsvarende grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="bde85-218">Gem resultaterne af sammenligningen i fejlfindingsloggen for ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bde85-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="bde85-219">Konfigurere ER-grundlag til behandling af kreditorbetalinger</span><span class="sxs-lookup"><span data-stu-id="bde85-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="bde85-220">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="bde85-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="bde85-221">Vælg **Grundlag**.</span><span class="sxs-lookup"><span data-stu-id="bde85-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="bde85-222">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bde85-222">Select **New**.</span></span>
4. <span data-ttu-id="bde85-223">Vælg formatet **BACS (UK)** i feltet **Reference**.</span><span class="sxs-lookup"><span data-stu-id="bde85-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="bde85-224">Vælg **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="bde85-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="bde85-225">Tilføj et nyt grundlag for kreditorbetalingsfilen:</span><span class="sxs-lookup"><span data-stu-id="bde85-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="bde85-226">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bde85-226">Select **New**.</span></span>
    2. <span data-ttu-id="bde85-227">Vælg den **Fil**-DM-dokumenttype i feltet **Type**, du har konfigureret i ER-parametrene til lagring af grundlæggende artefakter.</span><span class="sxs-lookup"><span data-stu-id="bde85-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="bde85-228">Naviger for at vælge den lokalt gemte **Fil**-betalingsfil i tekstformat.</span><span class="sxs-lookup"><span data-stu-id="bde85-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="bde85-229">I feltet **Beskrivelse** skal du angive **TXT-betalingsfil**.</span><span class="sxs-lookup"><span data-stu-id="bde85-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="bde85-230">Tilføj et nyt grundlag for kontrolrapporten til kreditorbetalingen:</span><span class="sxs-lookup"><span data-stu-id="bde85-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="bde85-231">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bde85-231">Select **New**.</span></span>
    2. <span data-ttu-id="bde85-232">Vælg den **Fil**-DM-dokumenttype i feltet **Type**, du har konfigureret i ER-parametrene til lagring af grundlæggende artefakter.</span><span class="sxs-lookup"><span data-stu-id="bde85-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="bde85-233">Naviger for at vælge den lokalt gemte **ERVendOutPaymControlReport**-kontrolrapportfil i xlsx-format.</span><span class="sxs-lookup"><span data-stu-id="bde85-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="bde85-234">I feltet **Beskrivelse** skal du angive **XLSX-betalingskontrolrapport**.</span><span class="sxs-lookup"><span data-stu-id="bde85-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="bde85-235">![Basislinjer for leverandørbetalingsfiler og kontrolrapport](media/GER-BaselineAttachments.png "Skærmbillede af siden Konfigurationer med rapporten Betalingskontrol XLSX valgt")</span><span class="sxs-lookup"><span data-stu-id="bde85-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="bde85-236">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bde85-236">Close the page.</span></span>
9. <span data-ttu-id="bde85-237">Vælg **Nyt** i oversigtspanelet **Grundlag** for at konfigurere et grundlag for betalingsfilen:</span><span class="sxs-lookup"><span data-stu-id="bde85-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="bde85-238">Navngiv linjen **Indstilling af grundlag for betalingsfil**.</span><span class="sxs-lookup"><span data-stu-id="bde85-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="bde85-239">Vælg **Fil** i feltet **Filkomponentnavn** for at anvende dette grundlag på det ER-formatoutput, der genererer betalingsfilen i tekstformatet BACS (UK).</span><span class="sxs-lookup"><span data-stu-id="bde85-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="bde85-240">I feltet **Firmaer** skal du vælge **GBSI** for at anvende dette grundlag, når **BACS (UK)** ER-formatet køres i GBSI-firmaet.</span><span class="sxs-lookup"><span data-stu-id="bde85-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="bde85-241">Brug feltet **Filnavnsmaske** til at angive **\*.TXT** for kun at anvende dette grundlag på output i **fil**-formatkomponenten, der har filtypenavnet **.txt**.</span><span class="sxs-lookup"><span data-stu-id="bde85-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="bde85-242">Vælg **TXT-betalingsfil** i feltet **Grundlag**, så dette grundlag bruges til sammenligning med det genererede output.</span><span class="sxs-lookup"><span data-stu-id="bde85-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="bde85-243">Vælg **Ny** for at konfigurere et grundlag for kontrolrapporten:</span><span class="sxs-lookup"><span data-stu-id="bde85-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="bde85-244">Navngiv linjen **Indstilling af grundlag for kontrolrapport**.</span><span class="sxs-lookup"><span data-stu-id="bde85-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="bde85-245">Vælg **ERVendOutPaymControlReport** i feltet **Filkomponentnavn** for at anvende dette grundlag på det ER-formatoutput, der genererer kontrolrapporten.</span><span class="sxs-lookup"><span data-stu-id="bde85-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="bde85-246">I feltet **Firmaer** skal du vælge **GBSI** for at anvende dette grundlag, når **BACS (UK)** ER-formatet køres i GBSI-firmaet.</span><span class="sxs-lookup"><span data-stu-id="bde85-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="bde85-247">Brug feltet **Filnavnsmaske** til at angive **\*.XLSX** for kun at anvende dette grundlag på output i **ERVendOutPaymControlReport**-formatkomponenten, der har filtypenavnet **.xslx**.</span><span class="sxs-lookup"><span data-stu-id="bde85-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="bde85-248">Vælg **XLSX-betalingskontrolrapport** i feltet **Grundlag**, så dette grundlag bruges til sammenligning med det genererede output.</span><span class="sxs-lookup"><span data-stu-id="bde85-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="bde85-249">![Basislinjers oversigtspanel på siden Konfigurationer](media/GER-BaselineRules.png "Skærmbillede af oversigtspanelet Basislinjer på Konfigurationsside")</span><span class="sxs-lookup"><span data-stu-id="bde85-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="bde85-250">Registrere test for at validere behandling af kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="bde85-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="bde85-251">Som funktionel superbruger kan du registrere dine egne trin for at teste behandling af leverandørbetaling.</span><span class="sxs-lookup"><span data-stu-id="bde85-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="bde85-252">Det anbefales, at du afspiller (og redigerer, efter behov) opgaveregistreringen **Forberede\\Registrering.xml**, som du har downloadet tidligere.</span><span class="sxs-lookup"><span data-stu-id="bde85-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="bde85-253">Denne registrering bruges til at indstille alle testdata til den korrekte tilstand.</span><span class="sxs-lookup"><span data-stu-id="bde85-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="bde85-254">Dette trin er nødvendigt, fordi testen kan udføres mange gange, og alle test skal bruge data, der findes i samme tilstand.</span><span class="sxs-lookup"><span data-stu-id="bde85-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="bde85-255">Nulstille brugerindstillinger</span><span class="sxs-lookup"><span data-stu-id="bde85-255">Reset user settings</span></span>

1. <span data-ttu-id="bde85-256">Åbn standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="bde85-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="bde85-257">Vælg knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="bde85-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="bde85-258">Vælg **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="bde85-258">Select **User options**.</span></span>
4. <span data-ttu-id="bde85-259">Vælg **Brugsdata**.</span><span class="sxs-lookup"><span data-stu-id="bde85-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="bde85-260">Vælg **Nulstil**.</span><span class="sxs-lookup"><span data-stu-id="bde85-260">Select **Reset**.</span></span>
6. <span data-ttu-id="bde85-261">Vælg **Ja** for at bekræfte, at du vil nulstille brugsdata.</span><span class="sxs-lookup"><span data-stu-id="bde85-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="bde85-262">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bde85-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="bde85-263">Registrere de trin, der skal forberede data til test</span><span class="sxs-lookup"><span data-stu-id="bde85-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="bde85-264">Vælg knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="bde85-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="bde85-265">Vælg **Arbejdsrutineoptager**.</span><span class="sxs-lookup"><span data-stu-id="bde85-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="bde85-266">Vælg **Afspil registrering**.</span><span class="sxs-lookup"><span data-stu-id="bde85-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="bde85-267">Vælg **Åbn fra denne pc**.</span><span class="sxs-lookup"><span data-stu-id="bde85-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="bde85-268">Vælg **Gennemse**, og vælg den lokalt gemte fil **Forberede\\Registrering.xml**.</span><span class="sxs-lookup"><span data-stu-id="bde85-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="bde85-269">Vælg **Start**.</span><span class="sxs-lookup"><span data-stu-id="bde85-269">Select **Start**.</span></span>
7. <span data-ttu-id="bde85-270">Bliv ved med at vælge **Afspil næste ventende trin**, indtil alle trin i registreringen er blevet afspillet.</span><span class="sxs-lookup"><span data-stu-id="bde85-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="bde85-271">Denne opgaveregistrering udfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="bde85-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="bde85-272">Angiv status for den behandlede betalingslinje til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="bde85-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="bde85-273">![Opgaveregistrering trin 3 til 4](media/GER-Recording1Review1.png "Skærmbillede af opgaveregistrering trin 3 til 4")</span><span class="sxs-lookup"><span data-stu-id="bde85-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="bde85-274">Aktivér ER-brugerparameteren **Kør i fejlfindingstilstand**.</span><span class="sxs-lookup"><span data-stu-id="bde85-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="bde85-275">![Opgaveregistrering trin 9 til 10](media/GER-Recording1Review2.png "Skærmbillede af opgaveregistrering trin 9 til 10")</span><span class="sxs-lookup"><span data-stu-id="bde85-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="bde85-276">Ryd op i den ER-fejlfindingslog, som indeholder resultaterne af sammenligningen af oprettede filer med grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="bde85-277">![Opgaveregistrering trin 13 til 15](media/GER-Recording1Review3.png "Skærmbillede af opgaveregistrering trin 13 til 15")</span><span class="sxs-lookup"><span data-stu-id="bde85-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="bde85-278">Registrere trin for at teste behandling af kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="bde85-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="bde85-279">Det anbefales, at du afspiller (og redigerer, efter behov) opgaveregistreringen **Behandle\\Registrering.xml**, som du har downloadet tidligere.</span><span class="sxs-lookup"><span data-stu-id="bde85-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="bde85-280">Denne registrering bruges til at behandle kreditorbetalinger og validere resultaterne af sammenligningen af genererede dokumenter med de tilsvarende grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="bde85-281">Vælg knappen **Indstillinger** (tandhjulsymbolet).</span><span class="sxs-lookup"><span data-stu-id="bde85-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="bde85-282">Vælg **Arbejdsrutineoptager**.</span><span class="sxs-lookup"><span data-stu-id="bde85-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="bde85-283">Vælg **Afspil registrering**.</span><span class="sxs-lookup"><span data-stu-id="bde85-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="bde85-284">Vælg **Åbn fra denne pc**.</span><span class="sxs-lookup"><span data-stu-id="bde85-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="bde85-285">Vælg **Gennemse**, og vælg den lokalt gemte fil **Behandle\\Registrering.xml**.</span><span class="sxs-lookup"><span data-stu-id="bde85-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="bde85-286">Vælg **Start**.</span><span class="sxs-lookup"><span data-stu-id="bde85-286">Select **Start**.</span></span>
7. <span data-ttu-id="bde85-287">Bliv ved med at vælge **Afspil næste ventende trin**, indtil alle trin i registreringen er blevet afspillet.</span><span class="sxs-lookup"><span data-stu-id="bde85-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="bde85-288">Denne opgaveregistrering udfører følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="bde85-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="bde85-289">Start behandling af kreditorbetaling.</span><span class="sxs-lookup"><span data-stu-id="bde85-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="bde85-290">Vælg de korrekte kørselsparametre, og aktivér generering af en kontrolrapport.</span><span class="sxs-lookup"><span data-stu-id="bde85-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="bde85-291">![Opgaveregistrering trin 3 til 8](media/GER-Recording2Review1.png "Skærmbillede af opgaveregistrering trin 3 til 8")</span><span class="sxs-lookup"><span data-stu-id="bde85-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="bde85-292">Åbn ER-fejlfindingsloggen for at registrere resultaterne af sammenligningen af genereret output med grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="bde85-293">I ER-fejlfindingsloggen vises resultaterne af sammenligningen i **Genereret**-tekstfeltet.</span><span class="sxs-lookup"><span data-stu-id="bde85-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="bde85-294">Felterne **Formatkomponent** og **Formatsti, der medførte en post i logfil** refererer til den filkomponent, for hvilken det genererede output er sammenlignet med grundlaget.</span><span class="sxs-lookup"><span data-stu-id="bde85-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="bde85-295">![Posteringer på siden Kørselslogge for elektronisk rapportering](media/GER-ERDebugLog.png "Skærmbillede af posteringer på siden Kørselslogge for elektronisk rapportering")</span><span class="sxs-lookup"><span data-stu-id="bde85-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="bde85-296">Sammenligningen af det aktuelle output med grundlaget registreres ved at bruge indstillingen **Valider** for Arbejdsrutineoptager og vælge **Aktuel værdi**.</span><span class="sxs-lookup"><span data-stu-id="bde85-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="bde85-297">![Bruge indstillingen Valider til at sammenligne med den aktuelle værdi](media/GER-TRRecordValidation.png "Skærmbillede af anvendelse af indstillingen Valider til at sammenligne med den aktuelle værdi")</span><span class="sxs-lookup"><span data-stu-id="bde85-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="bde85-298">I følgende illustration vises det, hvordan de registrerede valideringstrin ser ud i opgaveregistreringen.</span><span class="sxs-lookup"><span data-stu-id="bde85-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="bde85-299">![Opgaveregistrering trin 13 og 15](media/GER-Recording2Review2.png "Skærmbillede af opgaveregistrering trin 13 og 15")</span><span class="sxs-lookup"><span data-stu-id="bde85-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="bde85-300">Tilføje de registrerede test i Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="bde85-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="bde85-301">Åbn Azure DevOps-miljøet.</span><span class="sxs-lookup"><span data-stu-id="bde85-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="bde85-302">Vælg det projekt, du har defineret i RSAT-parametrene, da du [konfigurerede værktøjet](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="bde85-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="bde85-303">Vælg den testplan, du har defineret i RSAT-parametrene, da du [konfigurerede værktøjet](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="bde85-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="bde85-304">Opret en ny testsag til den valgte testplan:</span><span class="sxs-lookup"><span data-stu-id="bde85-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="bde85-305">Navngiv testsagen **Forberede data til testbehandling af kreditors elektroniske betaling**.</span><span class="sxs-lookup"><span data-stu-id="bde85-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="bde85-306">Vedhæft filen **Registrering.xml** fra den **Forberede**-mappe, du har downloadet tidligere.</span><span class="sxs-lookup"><span data-stu-id="bde85-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="bde85-307">Opret en ny testsag til den valgte testplan:</span><span class="sxs-lookup"><span data-stu-id="bde85-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="bde85-308">Navngiv testsagen **Test behandling af kreditorbetalinger ved hjælp af ER-format BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="bde85-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="bde85-309">Vedhæft filen **Registrering.xml** fra den **Behandle**-mappe, du har downloadet tidligere.</span><span class="sxs-lookup"><span data-stu-id="bde85-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="bde85-310">![Nye testsager for den valgte testplan](media/GER-RSAT-DevOps-Tests-Passed.png "Skærmbillede af de nye testsager for den valgte testplan")</span><span class="sxs-lookup"><span data-stu-id="bde85-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="bde85-311">Vær opmærksom på den korrekte udførelsesrækkefølge af de test, der er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="bde85-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="bde85-312">Forberede RSAT til at køre de registrerede test</span><span class="sxs-lookup"><span data-stu-id="bde85-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="bde85-313">Indlæs testene fra Azure DevOps til RSAT</span><span class="sxs-lookup"><span data-stu-id="bde85-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="bde85-314">Åbn det lokale RSAT-program i den aktuelle topologi.</span><span class="sxs-lookup"><span data-stu-id="bde85-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="bde85-315">Vælg **Indlæs** for at indlæse de test, der aktuelt findes i Azure DevOps, i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="bde85-316">![Test indlæst i RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Skærmbillede af de test, der er indlæst i RSAT")</span><span class="sxs-lookup"><span data-stu-id="bde85-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="bde85-317">Oprette automatisering og parameterfiler</span><span class="sxs-lookup"><span data-stu-id="bde85-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="bde85-318">Vælg de test, du har indlæst fra Azure DevOps, i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="bde85-319">Vælg **Ny** for at oprette RSAT-automatiserings- og parameterfiler.</span><span class="sxs-lookup"><span data-stu-id="bde85-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="bde85-320">![RSAT-automatisering og parameterfiler oprettede i RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Skærmbillede af RSAT-automatisering og parameterfiler oprettede i RSAT")</span><span class="sxs-lookup"><span data-stu-id="bde85-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="bde85-321">Redigere parameterfilerne</span><span class="sxs-lookup"><span data-stu-id="bde85-321">Modify the parameters files</span></span>

1. <span data-ttu-id="bde85-322">Vælg testsagen **Forberede data til testbehandling af kreditors elektroniske betaling** i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="bde85-323">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bde85-323">Select **Edit**.</span></span>
3. <span data-ttu-id="bde85-324">I den Microsoft Excel-projektmappe, der åbnes, skal du i regnearket **Generelt** ændre firmakoden til **GBSI**, da dette firma skal bruges til testkørslen.</span><span class="sxs-lookup"><span data-stu-id="bde85-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="bde85-325">Vælg testsagen **Test behandling af kreditorbetalinger ved hjælp af ER-format BACS (UK)** i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="bde85-326">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bde85-326">Select **Edit**.</span></span>
6. <span data-ttu-id="bde85-327">I den Excel-projektmappe, der åbnes, skal du i regnearket **Generelt** ændre firmakoden til **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="bde85-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="bde85-328">I regnearket **ERFormatMappingRunLogTable** skal du bemærke, at cellerne A:3 og C:3 indeholder teksten fra felterne i ER-fejlfindingslogtabellen, der bruges til at validere resultaterne af sammenligningen af outputtet med grundlaget.</span><span class="sxs-lookup"><span data-stu-id="bde85-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="bde85-329">Disse tekster bruges til at evaluere poster i ER-fejlfindingsloggen, som oprettes under testkørslen.</span><span class="sxs-lookup"><span data-stu-id="bde85-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="bde85-330">![Regneark med ERFormatMappingRunLogTable](media/GER-RSAT-RSAT-ExcelParameters.png "Skærmbillede af ERFormatMappingRunLogTable-regnearket")</span><span class="sxs-lookup"><span data-stu-id="bde85-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="bde85-331">Køre testene, og analysere resultaterne</span><span class="sxs-lookup"><span data-stu-id="bde85-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="bde85-332">Køre testene i RSAT</span><span class="sxs-lookup"><span data-stu-id="bde85-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="bde85-333">Vælg de indlæste test i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="bde85-334">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="bde85-334">Select **Run**.</span></span>

<span data-ttu-id="bde85-335">Bemærk, at testsager automatisk køres i programmet ved hjælp af en webbrowser.</span><span class="sxs-lookup"><span data-stu-id="bde85-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="bde85-336">Analysere resultaterne af testkørsel</span><span class="sxs-lookup"><span data-stu-id="bde85-336">Analyze the results of test execution</span></span>

<span data-ttu-id="bde85-337">Resultaterne af testkørslen gemmes i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="bde85-338">Bemærk, at begge test blev bestået.</span><span class="sxs-lookup"><span data-stu-id="bde85-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="bde85-339">![Test, der bestod i RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Skærmbillede af test, der er bestået i RSAT")</span><span class="sxs-lookup"><span data-stu-id="bde85-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="bde85-340">Bemærk, at resultaterne af testkørslen også sendes til Azure DevOps, så du kan foretage yderligere analyser.</span><span class="sxs-lookup"><span data-stu-id="bde85-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="bde85-341">![Resultater af udførelse af test i Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Skærmbillede af resultaterne af testudførelsen i Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="bde85-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="bde85-342">Simulere en situation, hvor test mislykkes</span><span class="sxs-lookup"><span data-stu-id="bde85-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="bde85-343">Denne testpakke skal mislykkes, når mindst et af de genererede output ikke matcher det tilsvarende grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="bde85-344">For at opnå denne situation kan du bruge den afledte version af formatet **BACS (UK)**, der genererer en betalingsfil, der har et andet indhold end det tilsvarende grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="bde85-345">Hvis du vil simulere denne situation, kan du bruge samme **BACS (UK)**-format, men ændre betalingsbeløbet på den behandlede betalingslinje.</span><span class="sxs-lookup"><span data-stu-id="bde85-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="bde85-346">Åbn programmet og gå til **Kreditorer \> Betalinger \> Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="bde85-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="bde85-347">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="bde85-347">Select **Lines**.</span></span>
3. <span data-ttu-id="bde85-348">Vælg betalingslinjen, og vælg derefter **Betalingsstatus \> Ingen**.</span><span class="sxs-lookup"><span data-stu-id="bde85-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="bde85-349">I feltet **Debet** skal du ændre værdien fra **1.000,00** til **2.000,00**.</span><span class="sxs-lookup"><span data-stu-id="bde85-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="bde85-350">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="bde85-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="bde85-351">Køre testene i RSAT</span><span class="sxs-lookup"><span data-stu-id="bde85-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="bde85-352">Vælg de indlæste test i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="bde85-353">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="bde85-353">Select **Run**.</span></span>

<span data-ttu-id="bde85-354">Bemærk, at testsager automatisk køres i programmet ved hjælp af en webbrowser.</span><span class="sxs-lookup"><span data-stu-id="bde85-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="bde85-355">Analysere resultaterne af testkørsel</span><span class="sxs-lookup"><span data-stu-id="bde85-355">Analyze the results of test execution</span></span>

<span data-ttu-id="bde85-356">Resultaterne af testkørslen gemmes i RSAT.</span><span class="sxs-lookup"><span data-stu-id="bde85-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="bde85-357">Bemærk, at den anden test mislykkedes under den anden kørsel.</span><span class="sxs-lookup"><span data-stu-id="bde85-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="bde85-358">![Mislykkede testresultater i RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Skærmbillede af resultaterne af den mislykkede testudførelsen RSAT")</span><span class="sxs-lookup"><span data-stu-id="bde85-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="bde85-359">Bemærk, at resultaterne af testkørslen også sendes til Azure DevOps, så du kan foretage yderligere analyser.</span><span class="sxs-lookup"><span data-stu-id="bde85-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="bde85-360">![Mislykkede testresultater i Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Skærmbillede af resultaterne af den mislykkede testudførelse i Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="bde85-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="bde85-361">Du kan få adgang til status for hver test.</span><span class="sxs-lookup"><span data-stu-id="bde85-361">You can access the status of each test.</span></span> <span data-ttu-id="bde85-362">Du kan også få adgang til kørselsloggen, så du kan analysere årsagerne til eventuelle fejl.</span><span class="sxs-lookup"><span data-stu-id="bde85-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="bde85-363">I følgende illustration viser kørselslogfilen, at fejlen opstod på grund af forskellen i indhold mellem den genererede betalingsfil og dens grundlag.</span><span class="sxs-lookup"><span data-stu-id="bde85-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="bde85-364">![Udførelseslogfil for analysefejl i Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Skærmbillede af kørselsloggen for analyse af fejl i Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="bde85-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="bde85-365">Som du har set, kan ER-formatets funktionsmåde evalueres automatisk ved hjælp af RSAT som testplatform og ved hjælp af Arbejdsrutineoptager-baserede testsager, der bruger ER-grundlagsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="bde85-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bde85-366">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bde85-366">Additional resources</span></span>

- [<span data-ttu-id="bde85-367">Ressourcer til arbejdsrutineoptager</span><span class="sxs-lookup"><span data-stu-id="bde85-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="bde85-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="bde85-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="bde85-369">Oprette og automatisere test af brugeraccept</span><span class="sxs-lookup"><span data-stu-id="bde85-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="bde85-370">Installer og anvend et miljø, der understøtter fortløbende build og automatisering af test</span><span class="sxs-lookup"><span data-stu-id="bde85-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="bde85-371">Spore genererede rapportresultater og sammenligne dem med basisværdier</span><span class="sxs-lookup"><span data-stu-id="bde85-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="bde85-372">ER Opgradere dit format ved at bruge en ny basisversion af formatet</span><span class="sxs-lookup"><span data-stu-id="bde85-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="bde85-373">Importere ER-konfiguration fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="bde85-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]