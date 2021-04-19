---
title: Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder
description: I dette emne forklares det, hvordan du kan forbedre ydeevnen af løsninger til elektronisk rapportering (ER) ved at tilføje parameteriserede BEREGNET FELT-datakilder.
author: NickSelin
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 299570d6a94b0f9e7ee7cf490d4c1aeeb86d5716
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749507"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="f2b82-103">Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder</span><span class="sxs-lookup"><span data-stu-id="f2b82-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2b82-104">I dette emne forklares det, hvordan du kan tage [ydeevnespor](trace-execution-er-troubleshoot-perf.md) af [elektroniske rapporteringsformater (ER)](general-electronic-reporting.md), som er kørt, og derefter bruge oplysningerne fra disse spor til at forbedre ydeevnen ved at konfigurere en parameteriseret **Beregnet felt**-datakilde.</span><span class="sxs-lookup"><span data-stu-id="f2b82-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="f2b82-105">Som en del af processen med at udvikle elektroniske rapporteringskonfigurationer (ER) til generering af forretningsdokumenter definerer du den metode, der bruges til at hente data fra programmet og indtaste dem i det output, der genereres.</span><span class="sxs-lookup"><span data-stu-id="f2b82-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="f2b82-106">Ved at designe en parameteriseret datakilde af typen **Beregnet felt**, kan du mindske antallet af databasekald og reducere den tid og de omkostninger, der er involveret i indsamlingen af detaljer om udførelse af ER-format.</span><span class="sxs-lookup"><span data-stu-id="f2b82-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2b82-107">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f2b82-107">Prerequisites</span></span>

- <span data-ttu-id="f2b82-108">Hvis du vil fuldføre eksemplerne i dette emne, skal du have adgang til en af følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="f2b82-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="f2b82-109">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f2b82-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="f2b82-110">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f2b82-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f2b82-111">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="f2b82-111">System administrator</span></span>

- <span data-ttu-id="f2b82-112">Virksomheden skal angives til **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="f2b82-113">Følg trinnene i [Appendiks 1](#appendix1) i dette emne for at downloade komponenterne til Microsoft ER-eksempelløsningen, der er nødvendige for at fuldføre eksemplet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="f2b82-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="f2b82-114">Følg trinnene i [Appendiks 2](#appendix2) i dette emne for at konfigurere det minimale sæt af ER-parametre, der kræves for at bruge ER-strukturen til at forbedre ydeevnen i eksemplet på Microsoft ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="f2b82-115">Importere ER-eksempelløsningen</span><span class="sxs-lookup"><span data-stu-id="f2b82-115">Import the sample ER solution</span></span>

<span data-ttu-id="f2b82-116">Antag, at du skal designe en ER-løsning for at generere en ny rapport, der viser kreditorposteringer.</span><span class="sxs-lookup"><span data-stu-id="f2b82-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="f2b82-117">I øjeblikket kan du finde posteringerne for en valgt kreditor på siden **Kreditorposteringer** (gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**, vælg en kreditor, og vælg derefter en kreditor i handlingsruden under fanen **Kreditor** i gruppen **Transaktioner** på **Posteringer**).</span><span class="sxs-lookup"><span data-stu-id="f2b82-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="f2b82-118">Men skal have alle kreditorposteringer samlet i et elektronisk dokument i XML-format.</span><span class="sxs-lookup"><span data-stu-id="f2b82-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="f2b82-119">Denne løsning består af flere ER-konfigurationer, der indeholder den nødvendige datamodel, modeltilknytning og formatkomponenter.</span><span class="sxs-lookup"><span data-stu-id="f2b82-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="f2b82-120">Det første trin er at importere ER-løsningseksemplet for at generere en rapport over kreditorposteringer.</span><span class="sxs-lookup"><span data-stu-id="f2b82-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="f2b82-121">Log på den forekomst af Microsoft Dynamics 365 Finance, der er klargjort for dit firma.</span><span class="sxs-lookup"><span data-stu-id="f2b82-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="f2b82-122">I dette emne skal du oprette og ændre konfigurationerne for eksempelfirmaet **Litware Inc.**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="f2b82-123">Sørg for, at denne konfigurationsudbyder er føjet til din Finance-forekomst og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="f2b82-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="f2b82-124">Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f2b82-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="f2b82-125">I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="f2b82-126">På siden **Konfigurationer** skal du importere de ER-konfigurationer, som du har hentet som en forudsætning i Finance, i følgende rækkefølge: datamodel, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="f2b82-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="f2b82-127">Benyt følgende fremgangsmåde for hver konfiguration:</span><span class="sxs-lookup"><span data-stu-id="f2b82-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="f2b82-128">Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="f2b82-129">Vælg **Gennemse**, og vælg den relevante fil til ER-konfigurationen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="f2b82-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="f2b82-130">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-130">Select **OK**.</span></span>

![Importerede konfigurationer på siden Konfigurationer](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="f2b82-132">Gennemgå ER-eksempelløsningen</span><span class="sxs-lookup"><span data-stu-id="f2b82-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="f2b82-133">Gennemse modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="f2b82-133">Review the model mapping</span></span>

1. <span data-ttu-id="f2b82-134">På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model til forbedret ydeevne** og derefter vælge **Tilknytning af forbedret ydeevne**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f2b82-135">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f2b82-136">Vælg **Designer** i handlingsruden på siden **Tilknytning af model til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="f2b82-137">Denne ER-modeltilknytning er beregnet til at udføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="f2b82-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="f2b82-138">Hent listen over kreditorposteringer, der er gemt i tabellen VendTrans (**Trans**-datakilde).</span><span class="sxs-lookup"><span data-stu-id="f2b82-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="f2b82-139">For hver postering skal du fra tabellen VendTable hente den post for en kreditor, som posteringen er bogført for (**\#Vend**-datakilde).</span><span class="sxs-lookup"><span data-stu-id="f2b82-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2b82-140">Datakilden **\#Vend** er konfigureret til at hente den tilsvarende kreditorpost ved hjælp af den eksisterende mange til én-relation **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="f2b82-141">Modeltilknytningen i denne konfiguration implementerer basisdatamodellen for ethvert af de ER-formater, der er oprettet for denne model og kørt i Finance.</span><span class="sxs-lookup"><span data-stu-id="f2b82-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="f2b82-142">Derfor vises indholdet af **Trans**-datakilden for ER-formater, f.eks. abstrakte **model**-datakilder.</span><span class="sxs-lookup"><span data-stu-id="f2b82-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Trans-datakilde på siden for modeltilknytningsdesigneren](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="f2b82-144">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="f2b82-145">Luk siden **Tilknytning af model til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="f2b82-146">Gennemse format</span><span class="sxs-lookup"><span data-stu-id="f2b82-146">Review format</span></span>

1. <span data-ttu-id="f2b82-147">På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model til forbedret ydeevne** og derefter vælge **Format af forbedret ydeevne**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="f2b82-148">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f2b82-149">Vælg fanen **Tilknytning** på siden **Formatdesigner**, og vælg **Udvid/skjul**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="f2b82-150">Udvid elementerne **Model**, **Data** og **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="f2b82-151">Dette ER-format er beregnet til at oprette en rapport over kreditorposteringer i XML-format.</span><span class="sxs-lookup"><span data-stu-id="f2b82-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Formatere datakilder og konfigurerede bindinger af formatelementer på formatdesignsiden](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="f2b82-153">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="f2b82-154">Køre ER-eksempelløsningen for at spore kørslen</span><span class="sxs-lookup"><span data-stu-id="f2b82-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="f2b82-155">Forestil dig, at du er færdig med at designe den første version af ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="f2b82-156">Du vil nu teste løsningen i din Finance-forekomst og analysere kørselsydeevnen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="f2b82-157">Aktivere ER-performancesporing</span><span class="sxs-lookup"><span data-stu-id="f2b82-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="f2b82-158">Vælg firmaet **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="f2b82-159">Følg trinnene i [Aktivere ER-performancesporing](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) for at generere en performancesporing, mens et ER-format køres.</span><span class="sxs-lookup"><span data-stu-id="f2b82-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Dialogboksen Brugerparametre](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="f2b82-161">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="f2b82-161">Run the ER format</span></span>

1. <span data-ttu-id="f2b82-162">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f2b82-163">På siden **Konfigurationer** skal du vælge elementet **Format af forbedret ydeevne** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="f2b82-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="f2b82-164">Vælg **Kør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="f2b82-165">Brug performancesporing til at analysere ydeevne af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="f2b82-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="f2b82-166">På siden **Konfigurationer** skal du vælge elementet **Tilknytning af forbedret ydeevne** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="f2b82-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f2b82-167">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f2b82-168">Vælg **Designer** i handlingsruden på siden **Modeltilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f2b82-169">I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f2b82-170">Vælg den seneste sporing, der blev genereret, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="f2b82-171">Nye oplysninger er nu tilgængelige for nogle datakildeelementer i den aktuelle modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="f2b82-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="f2b82-172">Den tid, det faktisk blev brugt på at hente data vha. datakilden</span><span class="sxs-lookup"><span data-stu-id="f2b82-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="f2b82-173">Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at køre hele modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="f2b82-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Detaljer om udførelsestiden på designersiden Modeltilknytning](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="f2b82-175">Gitteret **Statistik for ydeevne** viser, at **Trans**-datakilden kalder tabellen VendTrans én gang.</span><span class="sxs-lookup"><span data-stu-id="f2b82-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="f2b82-176">Værdien **\[265\]\[Q:265\]** i **Trans**-datakilden angiver, at 265 kreditorposteringer er hentet fra programtabellen og returneret til datamodellen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="f2b82-177">Gitteret **Statistik for ydeevne** viser også, at den aktuelle modeltilknytning duplikerer databaseanmodninger, mens datakilden **\#Vend** køres.</span><span class="sxs-lookup"><span data-stu-id="f2b82-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="f2b82-178">Denne duplikering udføres af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="f2b82-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="f2b82-179">Kreditortabellen kaldes to gange for hver af de 265 gentagne kreditorposteringer, med en total på 530 kald.</span><span class="sxs-lookup"><span data-stu-id="f2b82-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="f2b82-180">Der foretages et kald for at angive kreditorkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="f2b82-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="f2b82-181">Der foretages et kald for at angive kreditornavnet.</span><span class="sxs-lookup"><span data-stu-id="f2b82-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="f2b82-182">Kreditortabellen kaldes for hver af de gentagne kreditorposteringer, selvom de hentede posteringer kun er bogført for fem kreditorer.</span><span class="sxs-lookup"><span data-stu-id="f2b82-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="f2b82-183">Af 530 kald er 525 dubletter.</span><span class="sxs-lookup"><span data-stu-id="f2b82-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="f2b82-184">I følgende illustration vises den meddelelse, du har modtaget om dubletopkald (databaseanmodninger).</span><span class="sxs-lookup"><span data-stu-id="f2b82-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Meddelelse om dublerede databaseanmodninger på siden Modeltilknytningsdesigner](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="f2b82-186">Den samlede udførelsestid for modeltilknytning (cirka otte sekunder). Bemærk, at mere end 80 procent (cirka seks sekunder) er blevet brugt på at hente værdier fra programtabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="f2b82-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="f2b82-187">Denne procentdel er for stor til to attributter af fem leverandører sammenlignet med oplysningerne om mængden fra VendTrans-programtabellen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="f2b82-188">Hvis du vil reducere antallet af kald, der oprettes for at få leverandøroplysningerne for hver transaktion og forbedre modeltilknytningens ydeevne, kan du bruge cachelagring til datakilden **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="f2b82-189">Datakilden **Trans\\\#Vend** cachelagres i området for den aktuelle transaktion i **Trans**-datakilden under kørslen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="f2b82-190">Ved at cachelagre datakilden **\#Vend** skal du reducere antallet af dublerede kald fra 525 til 260, men du fjerner ikke dubleringen fuldstændigt.</span><span class="sxs-lookup"><span data-stu-id="f2b82-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="f2b82-191">Hvis du vil fjerne dubletter helt, kan du konfigurere en ny parameterdatakilde af typen **Beregnede felt**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="f2b82-192">Forbedre modeltilknytningen på baggrund af oplysninger fra kørselssporing</span><span class="sxs-lookup"><span data-stu-id="f2b82-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="f2b82-193">Ændre modeltilknytningens logik</span><span class="sxs-lookup"><span data-stu-id="f2b82-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="f2b82-194">Udfør følgende trin for at bruge cachelagring og en datakilde af typen **Beregnet felt** for at forhindre, at der foretages dubletkald til databasen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="f2b82-195">På siden **Konfigurationer** skal du vælge elementet **Tilknytning af forbedret ydeevne** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="f2b82-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f2b82-196">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f2b82-197">Vælg **Designer** i handlingsruden på siden **Modeltilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f2b82-198">På siden **Modeltilknytningsdesigner** skal du følge disse trin for at tilføje en datakilde af typen **Tabelpost** for at få adgang til poster i programtabellen VendTable:</span><span class="sxs-lookup"><span data-stu-id="f2b82-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="f2b82-199">I ruden **Datakildetyper** skal du udvide **Dynamics 365 for Operations** og vælge **Tabelposter**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="f2b82-200">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="f2b82-201">I dialogboksen skal du angive **Vend** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="f2b82-202">Indtast **VendTable** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="f2b82-203">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-203">Select **OK**.</span></span>

5. <span data-ttu-id="f2b82-204">Du kan kun parameterisere kald til datakilder af typen **Beregnet felt**, hvis disse datakilder er placeret i en container.</span><span class="sxs-lookup"><span data-stu-id="f2b82-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="f2b82-205">Benyt derfor følgende fremgangsmåde for at føje en datakilde af typen **Tom container** til en ny parameteriseret datakilde af typen **Beregnet felt**:</span><span class="sxs-lookup"><span data-stu-id="f2b82-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="f2b82-206">I ruden **Datakildetyper** skal du udvide **Generelt** og vælge **Tom container**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="f2b82-207">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="f2b82-208">I dialogboksen skal du angive **Box** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="f2b82-209">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-209">Select **OK**.</span></span>

    ![Box-datakilde på siden for modeltilknytningsdesigneren](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="f2b82-211">Udfør følgende trin for at tilføje en parameteriseret datakilde af typen **Beregnet felt**:</span><span class="sxs-lookup"><span data-stu-id="f2b82-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="f2b82-212">Vælg **Box** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="f2b82-213">Udvid **Funktioner** i ruden **Datakildetyper**, og vælg **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="f2b82-214">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-214">Select **Add**.</span></span>
    4. <span data-ttu-id="f2b82-215">I dialogboksen skal du angive **Vend** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="f2b82-216">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="f2b82-217">På siden **Formeldesigner** skal du vælge **Parametre** for at angive de parametre, der skal leveres, når denne datakilde kaldes.</span><span class="sxs-lookup"><span data-stu-id="f2b82-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="f2b82-218">Vælg **Ny** i dialogboksen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="f2b82-219">Angiv **parmVendAccNumber** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="f2b82-220">I feltet **Type** skal du vælge **Streng**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="f2b82-221">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-221">Select **OK**.</span></span>
    11. <span data-ttu-id="f2b82-222">I feltet **Formel** skal du angive **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="f2b82-223">Vælg **Gem**, og luk derefter siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="f2b82-224">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="f2b82-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="f2b82-225">Benyt følgende fremgangsmåde for at markere den tilføjede datakilde som cachelagret under udførelsen:</span><span class="sxs-lookup"><span data-stu-id="f2b82-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="f2b82-226">Vælg **Box\\Vend** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="f2b82-227">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2b82-228">Datakilden **Box\\Vend** cachelagres i området for alle leverandørtransaktioner i **Trans**-datakilden under kørslen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="f2b82-229">Udfør følgende trin for at opdatere den indlejrede **Trans\\\#Vend**-datakilde, så den bruger datakilden **Box\\Vend**:</span><span class="sxs-lookup"><span data-stu-id="f2b82-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="f2b82-230">Udvid **Trans** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="f2b82-231">Vælg datakilden **Trans\\\#Vend**, og vælg derefter **Rediger** \> **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="f2b82-232">På siden **Formeldesigner** skal du i feltet **Formel** angive **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="f2b82-233">Vælg **Gem**, og luk derefter siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="f2b82-234">Vælg **OK** for at fuldføre ændringerne af den valgte datakilde.</span><span class="sxs-lookup"><span data-stu-id="f2b82-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="f2b82-235">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-235">Select **Save**.</span></span>

    ![Vend-datakilde på siden for modeltilknytningsdesigneren](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="f2b82-237">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="f2b82-238">Luk siden **Modeltilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="f2b82-239">Fuldføre den ændrede version af ER-modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="f2b82-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="f2b82-240">På siden **Konfigurationer** skal du i oversigtspanelet **Versioner** vælge version **1.2** af konfigurationen af **Tilknytning af forbedret ydeevne**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="f2b82-241">Vælg **Skift status** \> **Fuldført**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="f2b82-242">Køre den ændrede ER-løsning for at spore kørslen</span><span class="sxs-lookup"><span data-stu-id="f2b82-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="f2b82-243">Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.</span><span class="sxs-lookup"><span data-stu-id="f2b82-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="f2b82-244">Brug performancesporing til at analysere justeringer af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="f2b82-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="f2b82-245">På siden **Konfigurationer** skal du vælge elementet **Tilknytning af forbedret ydeevne** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="f2b82-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f2b82-246">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f2b82-247">Vælg **Designer** i handlingsruden på siden **Modeltilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f2b82-248">I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f2b82-249">Vælg den seneste sporing, der blev genereret, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="f2b82-250">Bemærk, at de justeringer, du har foretaget for modeltilknytningen, har elimineret dubletter af forespørgsler til databasen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="f2b82-251">Antallet af kald til databasetabeller og datakilder for denne modeltilknytning er også blevet reduceret.</span><span class="sxs-lookup"><span data-stu-id="f2b82-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Sporingsoplysninger på side 1 af modeltilknytningsdesigneren](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="f2b82-253">Den samlede udførelsestid er blevet reduceret ca. 20 gange (fra ca. 8 sekunder til ca. 400 millisekunder).</span><span class="sxs-lookup"><span data-stu-id="f2b82-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="f2b82-254">Derfor er ydeevnen i hele ER-løsningen blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="f2b82-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Sporingsoplysninger på side 2 af modeltilknytningsdesigneren](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="f2b82-256">Appendiks 1: Download komponenterne i Microsoft ER-eksempelløsningen</span><span class="sxs-lookup"><span data-stu-id="f2b82-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="f2b82-257">Du skal også downloade og lokalt gemme følgende filer.</span><span class="sxs-lookup"><span data-stu-id="f2b82-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="f2b82-258">Filer</span><span class="sxs-lookup"><span data-stu-id="f2b82-258">File</span></span>                                        | <span data-ttu-id="f2b82-259">Indhold</span><span class="sxs-lookup"><span data-stu-id="f2b82-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="f2b82-260">Model til forbedret ydeevne.version.1</span><span class="sxs-lookup"><span data-stu-id="f2b82-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="f2b82-261">Eksempler på ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f2b82-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f2b82-262">Tilknytning af forbedret ydeevne.version.1.1</span><span class="sxs-lookup"><span data-stu-id="f2b82-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="f2b82-263">Eksempler på ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f2b82-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f2b82-264">Format af forbedret ydeevne.version.1.1</span><span class="sxs-lookup"><span data-stu-id="f2b82-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="f2b82-265">Eksempler på ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f2b82-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="f2b82-266">Appendiks 2: Konfigurere ER-strukturen</span><span class="sxs-lookup"><span data-stu-id="f2b82-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="f2b82-267">Før du kan begynde at bruge ER-strukturen til at forbedre ydeevnen i eksemplet med Microsoft ER-løsningen, skal du konfigurere det minimale sæt med ER-parametre.</span><span class="sxs-lookup"><span data-stu-id="f2b82-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="f2b82-268">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="f2b82-268">Configure ER parameters</span></span>

1. <span data-ttu-id="f2b82-269">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f2b82-270">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="f2b82-271">På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .</span><span class="sxs-lookup"><span data-stu-id="f2b82-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="f2b82-272">På fanen **Vedhæftede filer** kan du angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="f2b82-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="f2b82-273">I feltet **Konfigurationer** skal du vælge typen **Fil** for **DEMF**-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="f2b82-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="f2b82-274">I felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="f2b82-275">Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f2b82-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="f2b82-276">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f2b82-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="f2b82-277">Alle ER-konfigurationer, der tilføjes, er markeret som ejet af en udbyder af ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f2b82-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="f2b82-278">Den udbyder af ER-konfigurationer, der aktiveres i arbejdsområdet **Elektronisk rapportering**, bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="f2b82-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="f2b82-279">Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f2b82-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="f2b82-280">Det er kun ejeren af en ER-konfiguration, der kan redigere konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f2b82-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="f2b82-281">Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="f2b82-282">Gennemse listen over udbydere af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f2b82-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="f2b82-283">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f2b82-284">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f2b82-285">På siden **Tabel over konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="f2b82-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="f2b82-286">Gennemse indholdet af denne side.</span><span class="sxs-lookup"><span data-stu-id="f2b82-286">Review the contents of this page.</span></span> <span data-ttu-id="f2b82-287">Hvis der allerede findes en post for **Litware, Inc.**, skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="f2b82-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="f2b82-288">Tilføje en ny udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f2b82-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="f2b82-289">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f2b82-290">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f2b82-291">På siden **Konfigurationsudbydere** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="f2b82-292">I feltet **Navn** skal du angive **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="f2b82-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="f2b82-293">I feltet **Internetadresse** skal du angive `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="f2b82-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="f2b82-294">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="f2b82-295">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f2b82-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="f2b82-296">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f2b82-297">Gå til siden **Lokaliseringskonkfigurationer**, og vælg feltet **Litware, Inc.** i sektionen **Konfigurationsudbydere**, og vælg derefter **Angiv som aktive**.</span><span class="sxs-lookup"><span data-stu-id="f2b82-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="f2b82-298">Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f2b82-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2b82-299">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f2b82-299">Additional resources</span></span>

- [<span data-ttu-id="f2b82-300">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f2b82-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f2b82-301">Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen</span><span class="sxs-lookup"><span data-stu-id="f2b82-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="f2b82-302">Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt</span><span class="sxs-lookup"><span data-stu-id="f2b82-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]