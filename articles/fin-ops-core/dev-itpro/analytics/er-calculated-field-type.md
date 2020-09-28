---
title: Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt
description: Dette emne indeholder oplysninger om, hvordan du bruger typen Beregnet felt til ER-datakilder.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c68f0a0e2481c69add8c50a1581466ad0b1483c0
ms.sourcegitcommit: 5472005274f2f94fba82dda90de128f39d8b8390
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759905"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="401e6-103">Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="401e6-104">Dette emne forklarer, hvordan du kan designe en elektronisk rapport (ER)-datakilde ved at bruge typen **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="401e6-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="401e6-105">Denne datakilde kan indeholde et ER-udtryk, der, når det udføres, kan styres af værdierne for de parameterargumenter, der er konfigureret i en binding, som kalder denne datakilde.</span><span class="sxs-lookup"><span data-stu-id="401e6-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="401e6-106">Ved at konfigurere parameteriserede kald af en sådan datakilde kan du genbruge en enkelt datakilde i mange bindinger, hvilket reducerer det samlede antal datakilder, der skal konfigureres i ER-modeltilknytninger eller ER-formater.</span><span class="sxs-lookup"><span data-stu-id="401e6-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="401e6-107">Det forenkler også den konfigurerede ER-komponent, hvilket reducerer vedligeholdelsesomkostningerne og omkostningerne ved at bruge andre forbrugere.</span><span class="sxs-lookup"><span data-stu-id="401e6-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="401e6-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="401e6-108">Prerequisites</span></span>
<span data-ttu-id="401e6-109">Før du kan følge eksemplerne i dette emne, skal du have følgende adgang:</span><span class="sxs-lookup"><span data-stu-id="401e6-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="401e6-110">Adgang til en af disse roller:</span><span class="sxs-lookup"><span data-stu-id="401e6-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="401e6-111">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="401e6-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="401e6-112">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="401e6-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="401e6-113">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="401e6-113">System administrator</span></span>

- <span data-ttu-id="401e6-114">Adgang til RCS (Regulatory Configuration Services), der er klargjort til den samme lejer som Finance and Operations for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="401e6-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="401e6-115">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="401e6-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="401e6-116">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="401e6-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="401e6-117">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="401e6-117">System administrator</span></span>

<span data-ttu-id="401e6-118">Du skal også hente og lokalt gemme følgende filer.</span><span class="sxs-lookup"><span data-stu-id="401e6-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="401e6-119">**Indhold**</span><span class="sxs-lookup"><span data-stu-id="401e6-119">**Content**</span></span>                           | <span data-ttu-id="401e6-120">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="401e6-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="401e6-121">Eksempler på ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="401e6-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="401e6-122">Model til at lære parameteriserede calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="401e6-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="401e6-123">Eksempler på ER-metadatakonfiguration</span><span class="sxs-lookup"><span data-stu-id="401e6-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="401e6-124">Metadata til at lære parameteriserede calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="401e6-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="401e6-125">Eksempler på ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="401e6-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="401e6-126">Tilknytning for at lære parameteriserede calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="401e6-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="401e6-127">Eksempler på ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="401e6-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="401e6-128">Format til at lære parameteriserede calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="401e6-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="401e6-129">Log på din RCS-forekomst</span><span class="sxs-lookup"><span data-stu-id="401e6-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="401e6-130">I dette eksempel skal du oprette en konfiguration for eksempelfirmaet, Litware Inc. Først skal du i RCS fuldføre disse trin i proceduren [Opret konfigurationsudbydere, og markér dem som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="401e6-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="401e6-131">Vælg **Elektronisk rapportering**på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="401e6-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="401e6-132">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="401e6-133">Importér de downloadede konfigurationer til RCS i følgende rækkefølge: datamodel, metadata, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="401e6-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="401e6-134">Udfør følgende trin for hver ER-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="401e6-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="401e6-135">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="401e6-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="401e6-136">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="401e6-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="401e6-137">Vælg **Gennemse**, og vælg den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="401e6-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="401e6-138">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="401e6-139">Gennemse den leverede ER-løsning</span><span class="sxs-lookup"><span data-stu-id="401e6-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="401e6-140">Gennemse modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="401e6-140">Review model mapping</span></span>

1. <span data-ttu-id="401e6-141">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="401e6-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="401e6-142">Vælg **Tilknytning for at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="401e6-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="401e6-143">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-143">Select **Designer**.</span></span>
4. <span data-ttu-id="401e6-144">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="401e6-145">Denne ER-modeltilknytning er beregnet til at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="401e6-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="401e6-146">Hent listen over momskoder (**Moms**-datakilde), der findes i **TaxTrans**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="401e6-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="401e6-147">Hent listen over momstransaktioner (**Trans**-datakilde), der findes i **TaxTrans**-tabellen:</span><span class="sxs-lookup"><span data-stu-id="401e6-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="401e6-148">Grupper listen over hentede transaktioner (**Gr**-datakilde) efter momskode.</span><span class="sxs-lookup"><span data-stu-id="401e6-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="401e6-149">Beregn for grupperede transaktioner følgende aggregerede værdier pr. momskode:</span><span class="sxs-lookup"><span data-stu-id="401e6-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="401e6-150">Summen af momsgrundlagsværdier.</span><span class="sxs-lookup"><span data-stu-id="401e6-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="401e6-151">Summen af momsværdier.</span><span class="sxs-lookup"><span data-stu-id="401e6-151">Sum of tax values.</span></span>
            - <span data-ttu-id="401e6-152">Minimumværdi for anvendt momssats.</span><span class="sxs-lookup"><span data-stu-id="401e6-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="401e6-153">Modeltilknytningen i denne konfiguration implementerer basisdatamodellen for ethvert af de ER-formater, der er oprettet for denne model, og udføres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="401e6-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="401e6-154">Derfor vises indholdet af **Moms**- og **Gr**-datakilderne for ER-formater, f. eks. abstrakte datakilder.</span><span class="sxs-lookup"><span data-stu-id="401e6-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Siden Modeltilknytningsdesigner, der viser moms- og gr-datakilder](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="401e6-156">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="401e6-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="401e6-157">Luk siden **Modeltilknytning**.</span><span class="sxs-lookup"><span data-stu-id="401e6-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="401e6-158">Gennemse format</span><span class="sxs-lookup"><span data-stu-id="401e6-158">Review format</span></span>

1. <span data-ttu-id="401e6-159">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="401e6-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="401e6-160">Vælg **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="401e6-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="401e6-161">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-161">Select **Designer**.</span></span> <span data-ttu-id="401e6-162">Dette ER-format er designet til at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="401e6-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="401e6-163">Generer en momsafstemning i XML-format.</span><span class="sxs-lookup"><span data-stu-id="401e6-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="401e6-164">Præsenter følgende beskatningsniveauer i momsangivelsen: normal, reduceret og ingen.</span><span class="sxs-lookup"><span data-stu-id="401e6-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="401e6-165">Vis flere detaljer på hvert beskatningsniveau med forskellige antal detaljer inden for hvert niveau.</span><span class="sxs-lookup"><span data-stu-id="401e6-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Siden Formatdesigner](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="401e6-167">Vælg **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="401e6-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="401e6-168">Udvid elementerne **Model**, **Data** og **Resume**.</span><span class="sxs-lookup"><span data-stu-id="401e6-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="401e6-169">Det beregnede felt **Model.Data.Summary.Level** indeholder det udtryk, der returnerer koden for beskatningsniveauet (**Almindelig**, **Reduceret**, **Ingen** eller **Andet**) som en tekstværdi for enhver momskode, der kan hentes fra **Model.Data.Summary**-datakilden på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="401e6-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Siden Formatdesigner, der viser oplysninger om datamodellen Model til at lære om parameteriserede kald.](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="401e6-171">Udvid elementet **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="401e6-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="401e6-172">Udvid elementet **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="401e6-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="401e6-173">**Model**.**Data2.Summary2**-datakilden er konfigureret til at gruppere **Model.Data.Summary**-datakildens transaktionsoplysninger efter beskatningsniveau (returneret af det beregnede felt **Model.Data.Summary.Level**) og beregne aggregeringerne.</span><span class="sxs-lookup"><span data-stu-id="401e6-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Siden Formatdesigner, der viser detaljer om Model.Data2.Summary2-datakilden](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="401e6-175">Gennemse de beregnede felter **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="401e6-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="401e6-176">Disse beregnede felter bruges til at filtrere **Model**.**Data2. Summary2**-postlisten og kun returnere poster, der repræsenterer et bestemt beskatningsniveau.</span><span class="sxs-lookup"><span data-stu-id="401e6-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="401e6-177">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="401e6-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="401e6-178">Oprette et afledt format</span><span class="sxs-lookup"><span data-stu-id="401e6-178">Create a derived format</span></span>
<span data-ttu-id="401e6-179">Du kan forbedre det angivne format ved at tilføje et beregnet felt til at filtrere det krævede beskatningsniveau i stedet for at bruge de tre eksisterende felter: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="401e6-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="401e6-180">Det krævede beskatningsniveau kan angives på den placering, hvor dette nye beregnede felt skal kaldes.</span><span class="sxs-lookup"><span data-stu-id="401e6-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="401e6-181">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="401e6-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="401e6-182">Vælg **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="401e6-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="401e6-183">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="401e6-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="401e6-184">Vælg **Afledt fra navn: Format til at lære parameteriserede kald, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="401e6-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="401e6-185">Gå til feltet **Navn**, og angiv **Format til at lære parameteriserede kald (brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="401e6-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="401e6-186">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="401e6-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="401e6-187">Konfigurer et beregnet felt med parametre, der returnerer en liste over poster</span><span class="sxs-lookup"><span data-stu-id="401e6-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="401e6-188">Begynd tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="401e6-189">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-189">Select **Designer**.</span></span>
2. <span data-ttu-id="401e6-190">Vælg **Udvid/skjul** for at udvide alle formatelementer.</span><span class="sxs-lookup"><span data-stu-id="401e6-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="401e6-191">Vælg **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="401e6-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="401e6-192">Udvid elementet **Model**.</span><span class="sxs-lookup"><span data-stu-id="401e6-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="401e6-193">Vælg elementet varen **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="401e6-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="401e6-194">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="401e6-194">Select **Add**.</span></span>
7. <span data-ttu-id="401e6-195">Vælg **Funktioner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="401e6-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="401e6-196">I feltet **Navn** skal du skrive **Niveauer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="401e6-197">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="401e6-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="401e6-198">Definer en parameter til tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="401e6-199">Vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="401e6-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="401e6-200">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="401e6-200">Select **New**.</span></span>
3. <span data-ttu-id="401e6-201">I feltet **Navn** skal du angive **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="401e6-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="401e6-202">I feltet **Type** skal du vælge **Streng**.</span><span class="sxs-lookup"><span data-stu-id="401e6-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="401e6-203">Der kan kun bruges primitive datatyper til at angive typen af parameterens argument.</span><span class="sxs-lookup"><span data-stu-id="401e6-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="401e6-204">Derfor kan typerne **Postliste**, **Post** og **Fastteksttype** ikke bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="401e6-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="401e6-205">Det maksimale antal parametre, der kan angives for et enkelt beregnet felt, er 8.</span><span class="sxs-lookup"><span data-stu-id="401e6-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Datakildeliste for parameter](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="401e6-207">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-207">Select **OK**.</span></span>

<span data-ttu-id="401e6-208">Hvis du tilføjer denne parameter, angiver du den betingelse, der skal være angivet for at kalde dette beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="401e6-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="401e6-209">Når du kalder dette beregnede felt, skal du angive argumentet for parameteren for **Beskatningsniveau** som en værdi med formatet **Streng**.</span><span class="sxs-lookup"><span data-stu-id="401e6-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="401e6-210">Sørg for, at du kun definerer parametre for de beregnede felter, der er placeret i en container (enten **Postliste**, **Post** eller **Container**).</span><span class="sxs-lookup"><span data-stu-id="401e6-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="401e6-211">Den konfigurerede parameter er tilgængelig på listen over datakilder for dette beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="401e6-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="401e6-212">Du kan føje parameteren til det konfigurerede udtryk ved at vælge **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="401e6-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datakildefelter](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="401e6-214">Definer et udtryk for tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="401e6-215">I feltet **Formel** skal du angive:</span><span class="sxs-lookup"><span data-stu-id="401e6-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="401e6-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="401e6-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="401e6-217">Vælg parameteren **Beskatningsniveau** på listen over datakilder.</span><span class="sxs-lookup"><span data-stu-id="401e6-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="401e6-218">Vælg **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="401e6-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="401e6-219">I feltet **Formel** skal du fuldføre udtrykket som:</span><span class="sxs-lookup"><span data-stu-id="401e6-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="401e6-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Beskatningsniveau')**</span><span class="sxs-lookup"><span data-stu-id="401e6-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="401e6-221">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="401e6-221">Select **Save**.</span></span>

    ![Oplysninger om datakildefelt](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="401e6-223">Luk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="401e6-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="401e6-224">Afslut tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="401e6-225">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-225">Select **OK**.</span></span>

<span data-ttu-id="401e6-226">På siden **Formatdesigner** kræver det konfigurerede beregnede felt med parametre **Niveauer** et **Streng**-argument.</span><span class="sxs-lookup"><span data-stu-id="401e6-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Udvidet liste over beregnede feltniveauer](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="401e6-228">Brug det konfigurerede beregnede felt til bindingsformatelementer</span><span class="sxs-lookup"><span data-stu-id="401e6-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="401e6-229">Vælg **Model.Data2.Levels** for at vælge det konfigurerede beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="401e6-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="401e6-230">Vælg formatelementet **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="401e6-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="401e6-231">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="401e6-231">Select **Bind**.</span></span>
4. <span data-ttu-id="401e6-232">Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde **Level1** med den nye datakilde **Niveauer** i alle indlejrede formatelementer i det valgte formatelement.</span><span class="sxs-lookup"><span data-stu-id="401e6-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="401e6-233">Den anvendte binding er oprettet som et kald af det beregnede felt med parametre.</span><span class="sxs-lookup"><span data-stu-id="401e6-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="401e6-234">Navnet på det bundne formatelement bruges som et argument for det beregnede felt med parametre under følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="401e6-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="401e6-235">Det beregnede felt er konfigureret til at bruge en enkelt parameter.</span><span class="sxs-lookup"><span data-stu-id="401e6-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="401e6-236">Datatypen for denne parameter er defineret som **Streng**.</span><span class="sxs-lookup"><span data-stu-id="401e6-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="401e6-237">Når navnet på det bundne formatelement er tomt, bruges datakildens navn for dette element i anvendt binding.</span><span class="sxs-lookup"><span data-stu-id="401e6-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="401e6-238">Vælg formatelementet **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="401e6-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="401e6-239">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="401e6-239">Select **Bind**.</span></span>
7. <span data-ttu-id="401e6-240">Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde **Level2** med den nye datakilde **Niveauer** i alle indlejrede formatelementer under det valgte formatelement.</span><span class="sxs-lookup"><span data-stu-id="401e6-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="401e6-241">Vælg formatelementet **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="401e6-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="401e6-242">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="401e6-242">Select **Bind**.</span></span>
10. <span data-ttu-id="401e6-243">Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde, **Level3** med den nye datakilde **Niveauer** i alle indlejrede formatelementer under det valgte formatelement.</span><span class="sxs-lookup"><span data-stu-id="401e6-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="401e6-244">Når du angiver argumentet for det beregnede felt med parametre for det XML-element, der repræsenterer beskatningsniveau (f.eks. **Model.Data2.Levels("Reduced")** som en tekstværdi), behøver du ikke gøre det samme for indlejrede XML-attributter – deres bindinger overtager automatisk værdien af det argument, der er defineret på det overordnede niveau (**Model.Data2.Levels.aggregated.Base**, ikke **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="401e6-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="401e6-245">Tilbagevendende kald af beregnet felt med parametre understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="401e6-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="401e6-246">Du kan vælge **Rediger formel** og ændre det anvendte argument, der er angivet som standard, i det beregnede felt med parametre i den valgte binding.</span><span class="sxs-lookup"><span data-stu-id="401e6-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="401e6-247">Hvis dette argument mangler, kan det medføre fejl på procestiden – brugerne får besked om denne situation, når det aktuelle format er valideret.</span><span class="sxs-lookup"><span data-stu-id="401e6-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Meddelelse om valideringsadvarsel](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="401e6-249">Konfigurer et beregnet felt med parametre til at returnere en post</span><span class="sxs-lookup"><span data-stu-id="401e6-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="401e6-250">Når et beregnet felt med parametre returnerer en post, skal du understøtte binding af individuelle felter i denne post for at formatere elementer.</span><span class="sxs-lookup"><span data-stu-id="401e6-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="401e6-251">I sådanne tilfælde vil der ikke være nogen overordnet binding, der indeholder værdien af et argument til kald af et beregnet felt med parametre – denne værdi skal defineres i bindingen for en enkelt posts felt.</span><span class="sxs-lookup"><span data-stu-id="401e6-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="401e6-252">Begynd tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="401e6-253">Vælg elementet varen **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="401e6-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="401e6-254">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="401e6-254">Select **Add**.</span></span>
3. <span data-ttu-id="401e6-255">Vælg **Funktioner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="401e6-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="401e6-256">I feltet **Navn** skal du skrive **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="401e6-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="401e6-257">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="401e6-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="401e6-258">Definer en parameter til tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="401e6-259">Vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="401e6-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="401e6-260">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="401e6-260">Select **New**.</span></span>
3. <span data-ttu-id="401e6-261">I feltet **Navn** skal du angive **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="401e6-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="401e6-262">I feltet **Type** skal du vælge **Streng**.</span><span class="sxs-lookup"><span data-stu-id="401e6-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="401e6-263">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="401e6-264">Definer et udtryk for tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="401e6-265">I feltet **Formel** skal du angive følgende udtryk:</span><span class="sxs-lookup"><span data-stu-id="401e6-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="401e6-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="401e6-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="401e6-267">Vælg parameteren **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="401e6-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="401e6-268">Vælg **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="401e6-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="401e6-269">I feltet **Formel** skal du føje **'Beskatningsniveau'))** til det, du har angivet i trin 1, for at afslutte udtrykket til:</span><span class="sxs-lookup"><span data-stu-id="401e6-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="401e6-270">**FIRSTORNULL(\@.Levels('Beskatningsniveau'))**</span><span class="sxs-lookup"><span data-stu-id="401e6-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="401e6-271">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="401e6-271">Select **Save**.</span></span>
6. <span data-ttu-id="401e6-272">Luk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="401e6-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="401e6-273">Afslut tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="401e6-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="401e6-274">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="401e6-275">Brug det konfigurerede beregnede felt for at binde formatelementer</span><span class="sxs-lookup"><span data-stu-id="401e6-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="401e6-276">Udvid **Model.Data2.LevelRecord** for at vælge det konfigurerede beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="401e6-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="401e6-277">Udvid containeren **Model.Data2.LevelRecord.aggregated** for det konfigurerede beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="401e6-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="401e6-278">Vælg feltet **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="401e6-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="401e6-279">Vælg formatelementet **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="401e6-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="401e6-280">Vælg **Ophæv binding**.</span><span class="sxs-lookup"><span data-stu-id="401e6-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="401e6-281">Vælg formatelementet **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="401e6-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="401e6-282">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="401e6-282">Select **Bind**.</span></span>
8. <span data-ttu-id="401e6-283">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="401e6-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="401e6-284">Skift udtrykket til **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="401e6-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Opdateret udtryk](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="401e6-286">Fjerne beregnede felter, der ikke bruges</span><span class="sxs-lookup"><span data-stu-id="401e6-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="401e6-287">Vælg **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="401e6-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="401e6-288">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="401e6-288">Select **Delete**.</span></span>
3. <span data-ttu-id="401e6-289">Vælg **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="401e6-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="401e6-290">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="401e6-290">Select **Delete**.</span></span>
5. <span data-ttu-id="401e6-291">Vælg **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="401e6-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="401e6-292">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="401e6-292">Select **Delete**.</span></span>
7. <span data-ttu-id="401e6-293">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="401e6-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="401e6-294">Du har genbrugt det samme beregnede felt **Model.Data2.Levels** flere gange i formatbindinger.</span><span class="sxs-lookup"><span data-stu-id="401e6-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="401e6-295">Det er meget lettere at bruge og vedligeholde et enkelt beregnet felt i stedet for at gøre dette for flere ens felter.</span><span class="sxs-lookup"><span data-stu-id="401e6-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="401e6-296">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="401e6-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="401e6-297">Fuldfør tilpasset version af et afledt format</span><span class="sxs-lookup"><span data-stu-id="401e6-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="401e6-298">I oversigtspanelet **Versioner** skal du vælge **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="401e6-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="401e6-299">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="401e6-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="401e6-300">Eksportér fuldført version af et afledt format</span><span class="sxs-lookup"><span data-stu-id="401e6-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="401e6-301">Vælg **Format til at lære parameteriserede kald (brugerdefineret)** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="401e6-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="401e6-302">I oversigtspanelet **Versioner** skal du vælge den fuldførte version 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="401e6-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="401e6-303">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="401e6-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="401e6-304">Vælg **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="401e6-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="401e6-305">Gem den hentede konfiguration lokalt i XML-format.</span><span class="sxs-lookup"><span data-stu-id="401e6-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="401e6-306">Test ER-formater</span><span class="sxs-lookup"><span data-stu-id="401e6-306">Test ER formats</span></span> 
<span data-ttu-id="401e6-307">Du kan køre det første og det forbedrede ER-format for at sikre dig, at konfigurerede parameteriserede beregnede felter fungerer korrekt.</span><span class="sxs-lookup"><span data-stu-id="401e6-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="401e6-308">Importér ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="401e6-308">Import ER configurations</span></span>
<span data-ttu-id="401e6-309">Du kan importere evaluerede konfigurationer fra RCS ved hjælp af ER-lageret af typen **RCS**.</span><span class="sxs-lookup"><span data-stu-id="401e6-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="401e6-310">Hvis du allerede har gennemgået trinnene i emnet, kan du [Importere konfigurationer af Elektronisk rapportering (ER) fra Regulatory Configuration Services (RCS)](rcs-download-configurations.md), og bruge det konfigurerede ER-lager til at importere konfigurationer, der er beskrevet tidligere i dette emne, for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="401e6-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="401e6-311">Ellers kan du udføre disse trin:</span><span class="sxs-lookup"><span data-stu-id="401e6-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="401e6-312">Vælg **DEMF**-firma, og vælg **Elektronisk rapportering** i standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="401e6-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="401e6-313">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="401e6-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="401e6-314">Importér konfigurationer fra Microsoft Download Center i følgende rækkefølge: datamodel, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="401e6-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="401e6-315">Udfør følgende trin for hver ER-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="401e6-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="401e6-316">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="401e6-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="401e6-317">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="401e6-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="401e6-318">Vælg **Gennemse** for at vælge den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="401e6-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="401e6-319">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-319">Select **OK**.</span></span>

4. <span data-ttu-id="401e6-320">Importér de eksporterede fra den fuldførte RCS version 1.1.1 i formatet **Format til at lære parameteriserede kald (brugerdefineret)**:</span><span class="sxs-lookup"><span data-stu-id="401e6-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="401e6-321">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="401e6-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="401e6-322">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="401e6-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="401e6-323">Vælg **Gennemse** for at vælge den lokalt lagrede fil for **Format til at lære parameteriserede kald (brugerdefineret)** i XML-format.</span><span class="sxs-lookup"><span data-stu-id="401e6-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="401e6-324">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="401e6-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="401e6-325">Kør ER-formater</span><span class="sxs-lookup"><span data-stu-id="401e6-325">Run ER formats</span></span>

1. <span data-ttu-id="401e6-326">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="401e6-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="401e6-327">Vælg **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="401e6-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="401e6-328">Vælg **Kør** på det øverste niveau af båndet.</span><span class="sxs-lookup"><span data-stu-id="401e6-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="401e6-329">Gem det lokalt oprettede output.</span><span class="sxs-lookup"><span data-stu-id="401e6-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="401e6-330">Vælg emnet **Format til at lære parameteriserede kald (brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="401e6-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="401e6-331">Vælg **Kør** på det øverste niveau af båndet.</span><span class="sxs-lookup"><span data-stu-id="401e6-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="401e6-332">Gem det oprettede output lokalt.</span><span class="sxs-lookup"><span data-stu-id="401e6-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="401e6-333">Sammenlign indholdet af de genererede output.</span><span class="sxs-lookup"><span data-stu-id="401e6-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="401e6-334">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="401e6-334">Additional resources</span></span>

- [<span data-ttu-id="401e6-335">Formeldesigner i elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="401e6-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="401e6-336">Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder</span><span class="sxs-lookup"><span data-stu-id="401e6-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)

