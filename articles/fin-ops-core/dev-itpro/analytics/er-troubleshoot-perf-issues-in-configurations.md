---
title: Fejlfinde problemer med ydeevnen i ER-konfigurationer
description: Dette emne forklarer, hvordan du kan finde og rette problemer med ydeevne i ER-konfigurationer (elektronisk rapportering).
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216859"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="f71b9-103">Fejlfinde problemer med ydeevnen i ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f71b9-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="f71b9-104">Dette emne forklarer, hvordan du kan finde og løse problemer med ydeevne i [Elektronisk rapportering](general-electronic-reporting.md) (ER) [konfigurationer](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="f71b9-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="f71b9-105">Undersøgelser af ydeevne består typisk af flere trin.</span><span class="sxs-lookup"><span data-stu-id="f71b9-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="f71b9-106">[Indsamle](#collecting-data) data.</span><span class="sxs-lookup"><span data-stu-id="f71b9-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="f71b9-107">Analysere de indsamlede data.</span><span class="sxs-lookup"><span data-stu-id="f71b9-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="f71b9-108">På grundlag af resultaterne af analysen kan du bruge ER-konfigurationer til at [foretage ændringer](#making-changes) eller vælge at indsamle flere data.</span><span class="sxs-lookup"><span data-stu-id="f71b9-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f71b9-109">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="f71b9-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="f71b9-110">Analysere udførelsestid</span><span class="sxs-lookup"><span data-stu-id="f71b9-110">Analyze execution time</span></span>

<span data-ttu-id="f71b9-111">Udførelsestiden kan afhænge af uventede faktorer som f.eks. andre opgaver, der kører i samme miljø, og cachelagring, der bruger data, når de kaldes første gang.</span><span class="sxs-lookup"><span data-stu-id="f71b9-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="f71b9-112">Derfor skal du gentage udførelsen og målingen flere gange.</span><span class="sxs-lookup"><span data-stu-id="f71b9-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="f71b9-113">Af og til forårsages ydeevneproblemer ikke af en ER-formatkonfiguration, der bruges til rapportering.</span><span class="sxs-lookup"><span data-stu-id="f71b9-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="f71b9-114">De forårsages i stedet af den X++ kode, der bruges til at åbne konfigurationen af ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="f71b9-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="f71b9-115">I enten [Handlingscenter](#infolog-time) eller [hændelsesloggen](#event-log-time) kan du se udførelsestiden for rapporten.</span><span class="sxs-lookup"><span data-stu-id="f71b9-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="f71b9-116">Sammenlign rapportens udførelsestid med den samlede udførelsestid i scenariet.</span><span class="sxs-lookup"><span data-stu-id="f71b9-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="f71b9-117">Hvis rapportens udførelsestid er meget mindre end den samlede udførelsestid, skal du overveje, hvor mange data rapporten behandler:</span><span class="sxs-lookup"><span data-stu-id="f71b9-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="f71b9-118">Hvis rapporten behandler en lille mængde data, kan problemet omfatte indlæsningstiden for konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="f71b9-119">Hvis rapporten behandler en stor mængde data, kan problemet omfatte forbehandling af X++.</span><span class="sxs-lookup"><span data-stu-id="f71b9-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="f71b9-120">Brug [sporingsparser](#analyze-trace-parser-trace) til at analysere sagen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="f71b9-121">Du kan finde oplysninger om andre sager i de næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="f71b9-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="f71b9-122">Kør flere test, der involverer forskellige datamængder, for at finde ud af, hvordan udførelsestiden afhænger af datamængden.</span><span class="sxs-lookup"><span data-stu-id="f71b9-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="f71b9-123">Analysere sporinger ved hjælp af sporingsparser</span><span class="sxs-lookup"><span data-stu-id="f71b9-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="f71b9-124">Forbered et lille eksempel, eller indsaml flere sporinger under tilfældige dele af rapportgenereringen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="f71b9-125">Derefter skal du i [sporingsparser](#trace-parser) foretage en standardanalyse nedefra og op og besvare følgende spørgsmål:</span><span class="sxs-lookup"><span data-stu-id="f71b9-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="f71b9-126">Hvilke topmetoder er der med hensyn til tidsforbrug?</span><span class="sxs-lookup"><span data-stu-id="f71b9-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="f71b9-127">Hvilken del af den samlede tid bruger disse metoder?</span><span class="sxs-lookup"><span data-stu-id="f71b9-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="f71b9-128">Besvar de samme spørgsmål til forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="f71b9-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="f71b9-129">Hvis du kan se, at metoderne har præfikset "ER", skal du gå videre til næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="f71b9-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="f71b9-130">Hvis du kan se, at metoder eller forespørgsler er fra programpakken, skal du overveje generiske optimeringer (f.eks. oprette indekser).</span><span class="sxs-lookup"><span data-stu-id="f71b9-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="f71b9-131">Analysér antallet af kald.</span><span class="sxs-lookup"><span data-stu-id="f71b9-131">Analyze the number of calls.</span></span> <span data-ttu-id="f71b9-132">Hvis antallet er væsentligt højere end forventet, skal du overveje cachelagring af de tilsvarende noder for konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="f71b9-133">Analysere databasekald</span><span class="sxs-lookup"><span data-stu-id="f71b9-133">Analyze database calls</span></span>

<span data-ttu-id="f71b9-134">Forbered et eksempel med en lille mængde data, så du kan indsamle en [ER-sporing](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="f71b9-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="f71b9-135">Åbn derefter sporingen i ER-modeltilknytningsdesigneren, og se den nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="f71b9-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="f71b9-136">Besvar følgende spørgsmål:</span><span class="sxs-lookup"><span data-stu-id="f71b9-136">Answer the following questions:</span></span>

- <span data-ttu-id="f71b9-137">Er der nogen forespørgselsdublet?</span><span class="sxs-lookup"><span data-stu-id="f71b9-137">Is there any query duplication?</span></span> <span data-ttu-id="f71b9-138">Hvis der er, skal du overveje en af følgende rettelser:</span><span class="sxs-lookup"><span data-stu-id="f71b9-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="f71b9-139">[Brug cachelagring](#use-caching), hvis du mener, at der er flere kald i én overordnet post.</span><span class="sxs-lookup"><span data-stu-id="f71b9-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="f71b9-140">[Brug et cachelagret, parameteriseret beregnet felt](#cached-parameterized), hvis du mener, at der er kald til samme post i forskellige poster.</span><span class="sxs-lookup"><span data-stu-id="f71b9-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="f71b9-141">[Brug en **JOIN**-datakilde](#use-join-datasource), hvis du skal læse et stort antal forskellige poster fra en database.</span><span class="sxs-lookup"><span data-stu-id="f71b9-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="f71b9-142">Svarer antallet af forespørgsler og hentede poster til den overordnede mængde data?</span><span class="sxs-lookup"><span data-stu-id="f71b9-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="f71b9-143">Hvis et dokument f.eks. indeholder 10 linjer, viser statistikken så, at rapporten udtrækker 10 linjer eller 1.000 linjer?</span><span class="sxs-lookup"><span data-stu-id="f71b9-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="f71b9-144">Hvis du har stort antal hentede poster, skal du overveje en af følgende rettelser:</span><span class="sxs-lookup"><span data-stu-id="f71b9-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="f71b9-145">[Brug **FILTER**-funktionen i stedet for funktionen **WHERE**](#filter) til at behandle data på SQL Server-siden.</span><span class="sxs-lookup"><span data-stu-id="f71b9-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="f71b9-146">Brug cachelagring for at undgå at hente de samme data.</span><span class="sxs-lookup"><span data-stu-id="f71b9-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="f71b9-147">[Brug indsamlede datafunktioner](#collected-data) for at undgå at hente de samme data til opsummering.</span><span class="sxs-lookup"><span data-stu-id="f71b9-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="f71b9-148">Analysere PerfView-sporinger</span><span class="sxs-lookup"><span data-stu-id="f71b9-148">Analyze PerfView traces</span></span>

<span data-ttu-id="f71b9-149">[PerfView](#perfview) er et værktøj til erfarne udviklere.</span><span class="sxs-lookup"><span data-stu-id="f71b9-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="f71b9-150">Du kan finde mere detaljerede oplysninger om følgende trin i [Grundlæggende oplysninger om tidsundersøgelse af vægur](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="f71b9-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="f71b9-151">Samle en sporing ved at bruge trådtid.</span><span class="sxs-lookup"><span data-stu-id="f71b9-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="f71b9-152">Medtag kun stakke, der bruger **runUnattended**, til kun at filtrere den tråd, der har konfigurationsudførelse.</span><span class="sxs-lookup"><span data-stu-id="f71b9-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="f71b9-153">(Føj **runUnattended** til inputfeltet **IncPats**).</span><span class="sxs-lookup"><span data-stu-id="f71b9-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="f71b9-154">Fold al CPU-, netværks- og blokeret tid.</span><span class="sxs-lookup"><span data-stu-id="f71b9-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="f71b9-155">Indlæs [ER-forudindstillinger for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="f71b9-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="f71b9-156">Vælg **ER** \> **Anden forudindstilling**.</span><span class="sxs-lookup"><span data-stu-id="f71b9-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="f71b9-157">Se på navnene:</span><span class="sxs-lookup"><span data-stu-id="f71b9-157">Look at the names:</span></span>

    - <span data-ttu-id="f71b9-158">Du vil sandsynligvis se den platformskode, der bruger mest tid.</span><span class="sxs-lookup"><span data-stu-id="f71b9-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="f71b9-159">Du kan dobbelttrykke (eller dobbeltklikke) og gå op gennem **opkaldsmodtagere**.</span><span class="sxs-lookup"><span data-stu-id="f71b9-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="f71b9-160">Hvis du finder klasser, der har præfikset "ERExpression", og hvis de er funktioner, der er relateret til formler, kan du regne funktionsnavnet ud på basis af klassenavnet, og du kan se på ER-informationsbasen for at få vist attributterne.</span><span class="sxs-lookup"><span data-stu-id="f71b9-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="f71b9-161">Rettelser</span><span class="sxs-lookup"><span data-stu-id="f71b9-161">Fixes</span></span>

- <span data-ttu-id="f71b9-162">Hvis du kan se, at den meste CPU-tid forbruges af forespørgsler, skal du prøve at reducere antallet af forespørgsler:</span><span class="sxs-lookup"><span data-stu-id="f71b9-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="f71b9-163">[Gennemse ER-sporingen](#analyze-database-calls) for dublerede forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="f71b9-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="f71b9-164">Se, hvor mange poster der hentes, og evaluer, hvor mange data der skal hentes teoretisk.</span><span class="sxs-lookup"><span data-stu-id="f71b9-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="f71b9-165">Hvis du kan se, at den meste CPU-tid forbruges af de funktioner, der anvendes, skal du prøve at finde den plads i konfigurationen, der bruger de fleste ressourcer.</span><span class="sxs-lookup"><span data-stu-id="f71b9-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="f71b9-166">Hvis du kan se, at den meste CPU-tid forbruges af funktioner til indsamling af data, skal du overveje at erstatte dem med *SQL group by* på modeltilknytningssiden.</span><span class="sxs-lookup"><span data-stu-id="f71b9-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="f71b9-167">Dataindsamling</span><span class="sxs-lookup"><span data-stu-id="f71b9-167">Collecting data</span></span>

<span data-ttu-id="f71b9-168">Afhængigt af dit miljø kan du indsamle tilgængelige data på flere måder:</span><span class="sxs-lookup"><span data-stu-id="f71b9-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="f71b9-169">Få den samlede kørselstid:</span><span class="sxs-lookup"><span data-stu-id="f71b9-169">Get the total running time:</span></span>

    - <span data-ttu-id="f71b9-170">Fra handlingscenteret</span><span class="sxs-lookup"><span data-stu-id="f71b9-170">From the Action center</span></span>
    - <span data-ttu-id="f71b9-171">Fra hændelsesloggen</span><span class="sxs-lookup"><span data-stu-id="f71b9-171">From the event log</span></span>

- <span data-ttu-id="f71b9-172">Sådan profilerer du udførelsen:</span><span class="sxs-lookup"><span data-stu-id="f71b9-172">Profile the execution:</span></span>

    - <span data-ttu-id="f71b9-173">Ved hjælp af ER-værktøjer</span><span class="sxs-lookup"><span data-stu-id="f71b9-173">By using ER tools</span></span>
    - <span data-ttu-id="f71b9-174">Ved at bruge sporingsparser</span><span class="sxs-lookup"><span data-stu-id="f71b9-174">By using Trace parser</span></span>
    - <span data-ttu-id="f71b9-175">Ved hjælp af PerfView</span><span class="sxs-lookup"><span data-stu-id="f71b9-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="f71b9-176">Indsamle data i et produktionsmiljø</span><span class="sxs-lookup"><span data-stu-id="f71b9-176">Collecting data in a production environment</span></span>

<span data-ttu-id="f71b9-177">Sommetider kan problemer kun genskabes i et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="f71b9-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="f71b9-178">Du kan indsamle data på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="f71b9-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="f71b9-179">Med sporinger ved hjælp af [sporingsparser](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="f71b9-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="f71b9-180">Ved at bruge [ER-udførelsesspor](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="f71b9-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="f71b9-181">Ved at bruge den samlede udførelsestid</span><span class="sxs-lookup"><span data-stu-id="f71b9-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="f71b9-182">Indsamle data i et udviklingsmiljø</span><span class="sxs-lookup"><span data-stu-id="f71b9-182">Collecting data in a development environment</span></span>

<span data-ttu-id="f71b9-183">Udover de værktøjer, der kan bruges i et produktionsmiljø, er der flere forskellige værktøjer, du kan bruge i et udviklingsmiljø:</span><span class="sxs-lookup"><span data-stu-id="f71b9-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="f71b9-184">Hændelseslog (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="f71b9-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="f71b9-185">Denne log kan give dig den samlede udførelsestid.</span><span class="sxs-lookup"><span data-stu-id="f71b9-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="f71b9-186">Almindelige .NET-værktøjer, f.eks. PerfView.</span><span class="sxs-lookup"><span data-stu-id="f71b9-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="f71b9-187">Desuden giver et udviklingsmiljø dig større fleksibilitet til at eksperimentere.</span><span class="sxs-lookup"><span data-stu-id="f71b9-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="f71b9-188">Du kan f.eks. deaktivere dele af rapporter for at se, hvordan udførelsestiden påvirkes.</span><span class="sxs-lookup"><span data-stu-id="f71b9-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="f71b9-189">Værktøjer</span><span class="sxs-lookup"><span data-stu-id="f71b9-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="f71b9-190">Udførelsestid i handlingscenteret</span><span class="sxs-lookup"><span data-stu-id="f71b9-190">Execution time in the Action center</span></span>

<span data-ttu-id="f71b9-191">ER kan vise udførelsestiden for konfigurationen i handlingscenteret.</span><span class="sxs-lookup"><span data-stu-id="f71b9-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="f71b9-192">Denne indstilling fungerer kun for en bestemt bruger og et bestemt firma og kun for interaktive sessioner.</span><span class="sxs-lookup"><span data-stu-id="f71b9-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="f71b9-193">Benyt følgende fremgangsmåde for at gøre denne funktion tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="f71b9-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="f71b9-194">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f71b9-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f71b9-195">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="f71b9-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f71b9-196">I dialogboksen **Brugerparametre** skal du angive indstillingen **Vis filoprettelsestid** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f71b9-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="f71b9-197">Udførelsestid i hændelsesloggen</span><span class="sxs-lookup"><span data-stu-id="f71b9-197">Execution time in the event log</span></span>

1. <span data-ttu-id="f71b9-198">Åbn Windows Logbog.</span><span class="sxs-lookup"><span data-stu-id="f71b9-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="f71b9-199">Åbn **Microsoft-Dynamics-ElectronicReporting/Operational** under **Program- og tjenestelogfiler**.</span><span class="sxs-lookup"><span data-stu-id="f71b9-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="f71b9-200">Søg efter **FormatMapingRun**-hændelser, hvor **EventID=2**, da disse hændelser indeholder oplysninger om tidsforløbet.</span><span class="sxs-lookup"><span data-stu-id="f71b9-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="f71b9-201">Sporinger ved hjælp af sporingsparser</span><span class="sxs-lookup"><span data-stu-id="f71b9-201">Trace parser traces</span></span> 

<span data-ttu-id="f71b9-202">Da ER er implementeret i X++, kan du bruge almindelige X++ værktøjer til at analysere ydeevne.</span><span class="sxs-lookup"><span data-stu-id="f71b9-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="f71b9-203">Du kan finde flere oplysninger i [Udføre sporinger ved hjælp af sporingsparser](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="f71b9-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="f71b9-204">Der er nogle få begrænsninger for denne metode.</span><span class="sxs-lookup"><span data-stu-id="f71b9-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="f71b9-205">Da en del af ER er implementeret i C#, er det ikke alle detaljer, der er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="f71b9-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="f71b9-206">Du kan dog få vist oplysningerne om dataforbrug.</span><span class="sxs-lookup"><span data-stu-id="f71b9-206">However, you can view the data usage details.</span></span> <span data-ttu-id="f71b9-207">Lange rapportkørsler kan desuden overstige sporingens lagergrænse.</span><span class="sxs-lookup"><span data-stu-id="f71b9-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="f71b9-208">ER-sporinger</span><span class="sxs-lookup"><span data-stu-id="f71b9-208">ER traces</span></span>

<span data-ttu-id="f71b9-209">ER kan indsamle egne sporinger og har visualiserings- og analyseværktøjer til disse sporinger.</span><span class="sxs-lookup"><span data-stu-id="f71b9-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="f71b9-210">Du kan finde flere oplysninger i [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="f71b9-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="f71b9-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="f71b9-211">PerfView</span></span>

<span data-ttu-id="f71b9-212">Da både X++ og ER er implementeret oven på .NET-platformen, kan du bruge almindelige .NET-værktøjer.</span><span class="sxs-lookup"><span data-stu-id="f71b9-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="f71b9-213">Du kan f.eks. bruge det gratis værktøj [PerfView](https://github.com/Microsoft/perfview).</span><span class="sxs-lookup"><span data-stu-id="f71b9-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="f71b9-214">Du kan også indsamle data fra kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-214">You can also collect data from the command line.</span></span> <span data-ttu-id="f71b9-215">Følgende Windows PowerShell-script indsamler f.eks. udførelsestiden, indtil en formatudførelse stoppes på maskinen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="f71b9-216">Der er nogle få begrænsninger for denne metode.</span><span class="sxs-lookup"><span data-stu-id="f71b9-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="f71b9-217">Du skal have administrativ adgang til maskinen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="f71b9-218">Desuden skal du være en erfaren udvikler, fordi der er en stejl læringskurve.</span><span class="sxs-lookup"><span data-stu-id="f71b9-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="f71b9-219">Foretage ændringer</span><span class="sxs-lookup"><span data-stu-id="f71b9-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="f71b9-220">Bruge cachelagring</span><span class="sxs-lookup"><span data-stu-id="f71b9-220">Use caching</span></span>

<span data-ttu-id="f71b9-221">Selvom cachelagring reducerer den tid, der kræves for at hente data igen, koster den hukommelse.</span><span class="sxs-lookup"><span data-stu-id="f71b9-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="f71b9-222">Brug cachelagring i tilfælde, hvor mængden af hentede data ikke er meget stor.</span><span class="sxs-lookup"><span data-stu-id="f71b9-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="f71b9-223">Du kan finde flere oplysninger om og et eksempel på, hvordan du bruger cachelagring, i [Forbedre modeltilknytning baseret på oplysninger fra udførelsessporet](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="f71b9-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="f71b9-224">Bruge et cachelagret, parameteriseret beregnet felt</span><span class="sxs-lookup"><span data-stu-id="f71b9-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="f71b9-225">Sommetider skal værdier slås op gentagne gange.</span><span class="sxs-lookup"><span data-stu-id="f71b9-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="f71b9-226">Det kan f.eks. være kontonavne og kontonumre.</span><span class="sxs-lookup"><span data-stu-id="f71b9-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="f71b9-227">Du kan spare tid ved at oprette et beregnet felt med parametre på øverste niveau og derefter føje feltet til cachen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="f71b9-228">Det anbefales, at du kun bruger denne fremgangsmåde, når størrelsen på cachelagrede data er lille.</span><span class="sxs-lookup"><span data-stu-id="f71b9-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="f71b9-229">Yderligere oplysninger finder du i [Forbedre ER-løsningers ydeevne ved at tilføje parameteriserede BEREGNET FELT-datakilder](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="f71b9-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="f71b9-230">Bruge en JOIN-datakilde</span><span class="sxs-lookup"><span data-stu-id="f71b9-230">Use a JOIN data source</span></span>

<span data-ttu-id="f71b9-231">Med en **JOIN**-datakilde kan du hente flere tilknyttede poster ved hjælp af én forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="f71b9-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="f71b9-232">Der behøver ikke bruge en separat forespørgsel til at hente hver tilknyttede post.</span><span class="sxs-lookup"><span data-stu-id="f71b9-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="f71b9-233">Hvis du f.eks. har 1.000 linjer, og du henter varedata for hver linje efter relation, har du 1.001 forespørgsler (= 1.000 + 1).</span><span class="sxs-lookup"><span data-stu-id="f71b9-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="f71b9-234">Hvis du bruger en **JOIN**-datakilde, bruger du kun én forespørgsel til at hente de samme data.</span><span class="sxs-lookup"><span data-stu-id="f71b9-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="f71b9-235">Du kan finde flere oplysninger under [Bruge JOIN-datakilder til at hente data fra flere programtabeller i ER-modeltilknytninger](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f71b9-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="f71b9-236">Bruge FILTER-funktionen i stedet for WHERE-funktionen</span><span class="sxs-lookup"><span data-stu-id="f71b9-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="f71b9-237">Funktionen **[FILTER](er-functions-list-filter.md)** kører betingelser på SQL Server, mens **WHERE**-funktionen henter alle data på listen, én post ad gangen, og anvender betingelsen for hver post.</span><span class="sxs-lookup"><span data-stu-id="f71b9-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="f71b9-238">Du kan f.eks. vælge én post ud af 1.000 poster.</span><span class="sxs-lookup"><span data-stu-id="f71b9-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="f71b9-239">Hvis du bruger **WHERE**, hentes alle 1.000 poster.</span><span class="sxs-lookup"><span data-stu-id="f71b9-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="f71b9-240">Men hvis du bruger **FILTER**, hentes der præcis én post.</span><span class="sxs-lookup"><span data-stu-id="f71b9-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="f71b9-241">**FILTER** kan også bruge indekser på databasesiden.</span><span class="sxs-lookup"><span data-stu-id="f71b9-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="f71b9-242">Bruge indsamlede datafunktioner eller en akkumuleret datakilde</span><span class="sxs-lookup"><span data-stu-id="f71b9-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="f71b9-243">Hvis konfigurationen har en *Gruppér efter*-komponent, der opsummerer tidligere hentede data ved hjælp af en rapport, henter komponenten alle dataene igen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="f71b9-244">Ved at bruge indsamlede datafunktioner sætter du ER i stand til at akkumulere data under første hentning.</span><span class="sxs-lookup"><span data-stu-id="f71b9-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="f71b9-245">Du kan finde flere oplysninger i [Konfigurere ER-format for at udføre optælling og sammenlægning](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="f71b9-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="f71b9-246">Omskrive dele af konfigurationen i X++</span><span class="sxs-lookup"><span data-stu-id="f71b9-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="f71b9-247">ER understøtter kaldmetoder for tabeller og klasser, herunder udvidelser.</span><span class="sxs-lookup"><span data-stu-id="f71b9-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="f71b9-248">Overvej at omskrive dele af modeltilknytningen i X++ for at forbedre ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="f71b9-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="f71b9-249">ER kan forbruge data fra følgende kilder:</span><span class="sxs-lookup"><span data-stu-id="f71b9-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="f71b9-250">Klasser (datakilderne **objekt** og **klasse**)</span><span class="sxs-lookup"><span data-stu-id="f71b9-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="f71b9-251">Tabeller (datakilderne **tabel** og **tabelposter**)</span><span class="sxs-lookup"><span data-stu-id="f71b9-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="f71b9-252">Med [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) er det også muligt at sende forudberegnede data fra opkaldskoden.</span><span class="sxs-lookup"><span data-stu-id="f71b9-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="f71b9-253">Programpakken indeholder adskillige eksempler på denne metode.</span><span class="sxs-lookup"><span data-stu-id="f71b9-253">The application suite contains numerous examples of this approach.</span></span>
