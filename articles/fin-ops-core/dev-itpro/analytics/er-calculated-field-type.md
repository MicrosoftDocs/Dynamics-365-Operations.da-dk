---
title: Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt
description: Dette emne indeholder oplysninger om, hvordan du bruger typen Beregnet felt til ER-datakilder.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
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
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550078"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="dedd5-103">Understøtte parameteriserede kald af ER-datakilder for typen Beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dedd5-104">Dette emne forklarer, hvordan du kan designe en elektronisk rapport (ER)-datakilde ved at bruge typen **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="dedd5-105">Denne datakilde kan indeholde et ER-udtryk, der, når det udføres, kan styres af værdierne for de parameterargumenter, der er konfigureret i en binding, som kalder denne datakilde.</span><span class="sxs-lookup"><span data-stu-id="dedd5-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="dedd5-106">Ved at konfigurere parameteriserede kald af en sådan datakilde kan du genbruge en enkelt datakilde i mange bindinger, hvilket reducerer det samlede antal datakilder, der skal konfigureres i ER-modeltilknytninger eller ER-formater.</span><span class="sxs-lookup"><span data-stu-id="dedd5-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="dedd5-107">Det forenkler også den konfigurerede ER-komponent, hvilket reducerer vedligeholdelsesomkostningerne og omkostningerne ved at bruge andre forbrugere.</span><span class="sxs-lookup"><span data-stu-id="dedd5-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dedd5-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="dedd5-108">Prerequisites</span></span>
<span data-ttu-id="dedd5-109">Før du kan følge eksemplerne i dette emne, skal du have følgende adgang:</span><span class="sxs-lookup"><span data-stu-id="dedd5-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="dedd5-110">Adgang til en af disse roller:</span><span class="sxs-lookup"><span data-stu-id="dedd5-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="dedd5-111">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dedd5-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="dedd5-112">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dedd5-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="dedd5-113">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="dedd5-113">System administrator</span></span>

- <span data-ttu-id="dedd5-114">Adgang til RCS (Regulatory Configuration Service), der er klargjort til den samme lejer som Finance and Operations for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="dedd5-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="dedd5-115">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dedd5-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="dedd5-116">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dedd5-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="dedd5-117">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="dedd5-117">System administrator</span></span>

<span data-ttu-id="dedd5-118">Fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) skal du hente den ZIP-komprimerede fil **Understøt parameteriserede kald af ER-datakilder for typen Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="dedd5-119">Den indeholder følgende ER-konfigurationer, der skal udtrækkes og gemmes lokalt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="dedd5-120">**Indhold**</span><span class="sxs-lookup"><span data-stu-id="dedd5-120">**Content**</span></span>                           | <span data-ttu-id="dedd5-121">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="dedd5-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dedd5-122">Eksempler på ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="dedd5-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="dedd5-123">Model til at lære parameteriserede calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="dedd5-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="dedd5-124">Eksempler på ER-metadatakonfiguration</span><span class="sxs-lookup"><span data-stu-id="dedd5-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="dedd5-125">Metadata til at lære parameteriserede calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="dedd5-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="dedd5-126">Eksempler på ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="dedd5-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="dedd5-127">Tilknytning for at lære parameteriserede calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="dedd5-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="dedd5-128">Eksempler på ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="dedd5-128">Sample ER format configuration</span></span>        | <span data-ttu-id="dedd5-129">Format til at lære parameteriserede calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="dedd5-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="dedd5-130">Log på din RCS-forekomst</span><span class="sxs-lookup"><span data-stu-id="dedd5-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="dedd5-131">I dette eksempel skal du oprette en konfiguration for eksempelfirmaet, Litware Inc. Først skal du i RCS fuldføre disse trin i proceduren [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="dedd5-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="dedd5-132">Vælg **Elektronisk rapportering**på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="dedd5-133">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="dedd5-134">Importér de downloadede konfigurationer til RCS i følgende rækkefølge: datamodel, metadata, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="dedd5-135">Udfør følgende trin for hver ER-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="dedd5-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="dedd5-136">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="dedd5-137">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="dedd5-138">Vælg **Gennemse**, og vælg den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="dedd5-139">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="dedd5-140">Gennemse den leverede ER-løsning</span><span class="sxs-lookup"><span data-stu-id="dedd5-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="dedd5-141">Gennemse modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="dedd5-141">Review model mapping</span></span>

1. <span data-ttu-id="dedd5-142">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="dedd5-143">Vælg **Tilknytning for at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="dedd5-144">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-144">Select **Designer**.</span></span>
4. <span data-ttu-id="dedd5-145">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="dedd5-146">Denne ER-modeltilknytning er beregnet til at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="dedd5-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="dedd5-147">Hent listen over momskoder (**Moms**-datakilde), der findes i **TaxTrans**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="dedd5-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="dedd5-148">Hent listen over momstransaktioner (**Trans**-datakilde), der findes i **TaxTrans**-tabellen:</span><span class="sxs-lookup"><span data-stu-id="dedd5-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="dedd5-149">Grupper listen over hentede transaktioner (**Gr**-datakilde) efter momskode.</span><span class="sxs-lookup"><span data-stu-id="dedd5-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="dedd5-150">Beregn for grupperede transaktioner følgende aggregerede værdier pr. momskode:</span><span class="sxs-lookup"><span data-stu-id="dedd5-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="dedd5-151">Summen af momsgrundlagsværdier.</span><span class="sxs-lookup"><span data-stu-id="dedd5-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="dedd5-152">Summen af momsværdier.</span><span class="sxs-lookup"><span data-stu-id="dedd5-152">Sum of tax values.</span></span>
        - <span data-ttu-id="dedd5-153">Minimumværdi for anvendt momssats.</span><span class="sxs-lookup"><span data-stu-id="dedd5-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="dedd5-154">Modeltilknytningen i denne konfiguration implementerer basisdatamodellen for ethvert af de ER-formater, der er oprettet for denne model, og udføres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dedd5-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="dedd5-155">Derfor vises indholdet af **Moms**- og **Gr**-datakilderne for ER-formater, f. eks. abstrakte datakilder.</span><span class="sxs-lookup"><span data-stu-id="dedd5-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Siden Modeltilknytningsdesigner, der viser moms- og gr-datakilder](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="dedd5-157">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="dedd5-158">Luk siden **Modeltilknytning**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="dedd5-159">Gennemse format</span><span class="sxs-lookup"><span data-stu-id="dedd5-159">Review format</span></span>

1. <span data-ttu-id="dedd5-160">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="dedd5-161">Vælg **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="dedd5-162">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-162">Select **Designer**.</span></span> <span data-ttu-id="dedd5-163">Dette ER-format er designet til at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="dedd5-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="dedd5-164">Generer en momsafstemning i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="dedd5-165">Præsenter følgende beskatningsniveauer i momsangivelsen: normal, reduceret og ingen.</span><span class="sxs-lookup"><span data-stu-id="dedd5-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="dedd5-166">Vis flere detaljer på hvert beskatningsniveau med forskellige antal detaljer inden for hvert niveau.</span><span class="sxs-lookup"><span data-stu-id="dedd5-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Siden Formatdesigner](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="dedd5-168">Vælg **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="dedd5-169">Udvid elementerne **Model**, **Data** og **Resume**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="dedd5-170">Det beregnede felt **Model.Data.Summary.Level** indeholder det udtryk, der returnerer koden for beskatningsniveauet (**Almindelig**, **Reduceret**, **Ingen** eller **Andet**) som en tekstværdi for enhver momskode, der kan hentes fra **Model.Data.Summary**-datakilden på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Siden Formatdesigner, der viser oplysninger om datamodellen Model til at lære om parameteriserede kald.](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="dedd5-172">Udvid elementet **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="dedd5-173">Udvid elementet **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="dedd5-174">**Model**.**Data2.Summary2**-datakilden er konfigureret til at gruppere **Model.Data.Summary**-datakildens transaktionsoplysninger efter beskatningsniveau (returneret af det beregnede felt **Model.Data.Summary.Level**) og beregne aggregeringerne.</span><span class="sxs-lookup"><span data-stu-id="dedd5-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Siden Formatdesigner, der viser detaljer om Model.Data2.Summary2-datakilden](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="dedd5-176">Gennemse de beregnede felter **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="dedd5-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="dedd5-177">Disse beregnede felter bruges til at filtrere **Model**.**Data2. Summary2**-postlisten og kun returnere poster, der repræsenterer et bestemt beskatningsniveau.</span><span class="sxs-lookup"><span data-stu-id="dedd5-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="dedd5-178">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="dedd5-179">Oprette et afledt format</span><span class="sxs-lookup"><span data-stu-id="dedd5-179">Create a derived format</span></span>
<span data-ttu-id="dedd5-180">Du kan forbedre det angivne format ved at tilføje et beregnet felt til at filtrere det krævede beskatningsniveau i stedet for at bruge de tre eksisterende felter: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="dedd5-181">Det krævede beskatningsniveau kan angives på den placering, hvor dette nye beregnede felt skal kaldes.</span><span class="sxs-lookup"><span data-stu-id="dedd5-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="dedd5-182">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="dedd5-183">Vælg **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="dedd5-184">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="dedd5-185">Vælg **Afledt fra navn: Format til at lære parameteriserede kald, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="dedd5-186">Gå til feltet **Navn**, og angiv **Format til at lære parameteriserede kald (brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="dedd5-187">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="dedd5-188">Konfigurer et beregnet felt med parametre, der returnerer en liste over poster</span><span class="sxs-lookup"><span data-stu-id="dedd5-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="dedd5-189">Begynd tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="dedd5-190">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-190">Select **Designer**.</span></span>
2. <span data-ttu-id="dedd5-191">Vælg **Udvid/skjul** for at udvide alle formatelementer.</span><span class="sxs-lookup"><span data-stu-id="dedd5-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="dedd5-192">Vælg **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="dedd5-193">Udvid elementet **Model**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="dedd5-194">Vælg elementet varen **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="dedd5-195">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-195">Select **Add**.</span></span>
7. <span data-ttu-id="dedd5-196">Vælg **Funktioner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="dedd5-197">I feltet **Navn** skal du skrive **Niveauer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="dedd5-198">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="dedd5-199">Definer en parameter til tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="dedd5-200">Vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="dedd5-201">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-201">Select **New**.</span></span>
3. <span data-ttu-id="dedd5-202">I feltet **Navn** skal du angive **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="dedd5-203">I feltet **Type** skal du vælge **Streng**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="dedd5-204">Der kan kun bruges primitive datatyper til at angive typen af parameterens argument.</span><span class="sxs-lookup"><span data-stu-id="dedd5-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="dedd5-205">Derfor kan typerne **Postliste**, **Post** og **Fastteksttype** ikke bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="dedd5-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="dedd5-206">Det maksimale antal parametre, der kan angives for et enkelt beregnet felt, er 8.</span><span class="sxs-lookup"><span data-stu-id="dedd5-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Datakildeliste for parameter](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="dedd5-208">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-208">Select **OK**.</span></span>

<span data-ttu-id="dedd5-209">Hvis du tilføjer denne parameter, angiver du den betingelse, der skal være angivet for at kalde dette beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="dedd5-210">Når du kalder dette beregnede felt, skal du angive argumentet for parameteren for **Beskatningsniveau** som en værdi med formatet **Streng**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="dedd5-211">Sørg for, at du kun definerer parametre for de beregnede felter, der er placeret i en container (enten **Postliste**, **Post** eller **Container**).</span><span class="sxs-lookup"><span data-stu-id="dedd5-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="dedd5-212">Den konfigurerede parameter er tilgængelig på listen over datakilder for dette beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="dedd5-213">Du kan føje parameteren til det konfigurerede udtryk ved at vælge **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datakildefelter](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="dedd5-215">Definer et udtryk for tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="dedd5-216">I feltet **Formel** skal du angive:</span><span class="sxs-lookup"><span data-stu-id="dedd5-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="dedd5-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="dedd5-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="dedd5-218">Vælg parameteren **Beskatningsniveau** på listen over datakilder.</span><span class="sxs-lookup"><span data-stu-id="dedd5-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="dedd5-219">Vælg **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="dedd5-220">I feltet **Formel** skal du fuldføre udtrykket som:</span><span class="sxs-lookup"><span data-stu-id="dedd5-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="dedd5-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Beskatningsniveau')**</span><span class="sxs-lookup"><span data-stu-id="dedd5-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="dedd5-222">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-222">Select **Save**.</span></span>

    ![Oplysninger om datakildefelt](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="dedd5-224">Luk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="dedd5-225">Afslut tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="dedd5-226">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-226">Select **OK**.</span></span>

<span data-ttu-id="dedd5-227">På siden **Formatdesigner** kræver det konfigurerede beregnede felt med parametre **Niveauer** et **Streng**-argument.</span><span class="sxs-lookup"><span data-stu-id="dedd5-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Udvidet liste over beregnede feltniveauer](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="dedd5-229">Brug det konfigurerede beregnede felt til bindingsformatelementer</span><span class="sxs-lookup"><span data-stu-id="dedd5-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="dedd5-230">Vælg **Model.Data2.Levels** for at vælge det konfigurerede beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="dedd5-231">Vælg formatelementet **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="dedd5-232">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-232">Select **Bind**.</span></span>
4. <span data-ttu-id="dedd5-233">Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde **Level1** med den nye datakilde **Niveauer** i alle indlejrede formatelementer i det valgte formatelement.</span><span class="sxs-lookup"><span data-stu-id="dedd5-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="dedd5-234">Den anvendte binding er oprettet som et kald af det beregnede felt med parametre.</span><span class="sxs-lookup"><span data-stu-id="dedd5-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="dedd5-235">Navnet på det bundne formatelement bruges som et argument for det beregnede felt med parametre under følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="dedd5-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="dedd5-236">Det beregnede felt er konfigureret til at bruge en enkelt parameter.</span><span class="sxs-lookup"><span data-stu-id="dedd5-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="dedd5-237">Datatypen for denne parameter er defineret som **Streng**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="dedd5-238">Når navnet på det bundne formatelement er tomt, bruges datakildens navn for dette element i anvendt binding.</span><span class="sxs-lookup"><span data-stu-id="dedd5-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="dedd5-239">Vælg formatelementet **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="dedd5-240">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-240">Select **Bind**.</span></span>
7. <span data-ttu-id="dedd5-241">Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde **Level2** med den nye datakilde **Niveauer** i alle indlejrede formatelementer under det valgte formatelement.</span><span class="sxs-lookup"><span data-stu-id="dedd5-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="dedd5-242">Vælg formatelementet **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="dedd5-243">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-243">Select **Bind**.</span></span>
10. <span data-ttu-id="dedd5-244">Vælg **Ja** for at bekræfte erstatningen af den aktuelt anvendte datakilde, **Level3** med den nye datakilde **Niveauer** i alle indlejrede formatelementer under det valgte formatelement.</span><span class="sxs-lookup"><span data-stu-id="dedd5-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="dedd5-245">Når du angiver argumentet for det beregnede felt med parametre for det XML-element, der repræsenterer beskatningsniveau (f.eks. **Model.Data2.Levels("Reduced")** som en tekstværdi), behøver du ikke gøre det samme for indlejrede XML-attributter – deres bindinger overtager automatisk værdien af det argument, der er defineret på det overordnede niveau (**Model.Data2.Levels.aggregated.Base**, ikke **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="dedd5-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="dedd5-246">Tilbagevendende kald af beregnet felt med parametre understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="dedd5-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="dedd5-247">Du kan vælge **Rediger formel** og ændre det anvendte argument, der er angivet som standard, i det beregnede felt med parametre i den valgte binding.</span><span class="sxs-lookup"><span data-stu-id="dedd5-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="dedd5-248">Hvis dette argument mangler, kan det medføre fejl på procestiden – brugerne får besked om denne situation, når det aktuelle format er valideret.</span><span class="sxs-lookup"><span data-stu-id="dedd5-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Meddelelse om valideringsadvarsel](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="dedd5-250">Konfigurer et beregnet felt med parametre til at returnere en post</span><span class="sxs-lookup"><span data-stu-id="dedd5-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="dedd5-251">Når et beregnet felt med parametre returnerer en post, skal du understøtte binding af individuelle felter i denne post for at formatere elementer.</span><span class="sxs-lookup"><span data-stu-id="dedd5-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="dedd5-252">I sådanne tilfælde vil der ikke være nogen overordnet binding, der indeholder værdien af et argument til kald af et beregnet felt med parametre – denne værdi skal defineres i bindingen for en enkelt posts felt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="dedd5-253">Begynd tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="dedd5-254">Vælg elementet varen **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="dedd5-255">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-255">Select **Add**.</span></span>
3. <span data-ttu-id="dedd5-256">Vælg **Funktioner\\Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="dedd5-257">I feltet **Navn** skal du skrive **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="dedd5-258">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="dedd5-259">Definer en parameter til tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="dedd5-260">Vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="dedd5-261">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-261">Select **New**.</span></span>
3. <span data-ttu-id="dedd5-262">I feltet **Navn** skal du angive **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="dedd5-263">I feltet **Type** skal du vælge **Streng**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="dedd5-264">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="dedd5-265">Definer et udtryk for tilføjelse af et beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="dedd5-266">I feltet **Formel** skal du angive følgende udtryk:</span><span class="sxs-lookup"><span data-stu-id="dedd5-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="dedd5-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="dedd5-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="dedd5-268">Vælg parameteren **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="dedd5-269">Vælg **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="dedd5-270">I feltet **Formel** skal du føje **'Beskatningsniveau'))** til det, du har angivet i trin 1, for at afslutte udtrykket til:</span><span class="sxs-lookup"><span data-stu-id="dedd5-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="dedd5-271">**FIRSTORNULL(\@.Levels('Beskatningsniveau'))**</span><span class="sxs-lookup"><span data-stu-id="dedd5-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="dedd5-272">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-272">Select **Save**.</span></span>
6. <span data-ttu-id="dedd5-273">Luk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="dedd5-274">Afslut tilføjelse af et nyt beregnet felt</span><span class="sxs-lookup"><span data-stu-id="dedd5-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="dedd5-275">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="dedd5-276">Brug det konfigurerede beregnede felt for at binde formatelementer</span><span class="sxs-lookup"><span data-stu-id="dedd5-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="dedd5-277">Udvid **Model.Data2.LevelRecord** for at vælge det konfigurerede beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="dedd5-278">Udvid containeren **Model.Data2.LevelRecord.aggregated** for det konfigurerede beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="dedd5-279">Vælg feltet **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="dedd5-280">Vælg formatelementet **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="dedd5-281">Vælg **Ophæv binding**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="dedd5-282">Vælg formatelementet **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="dedd5-283">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-283">Select **Bind**.</span></span>
8. <span data-ttu-id="dedd5-284">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="dedd5-285">Skift udtrykket til **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Opdateret udtryk](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="dedd5-287">Fjerne beregnede felter, der ikke bruges</span><span class="sxs-lookup"><span data-stu-id="dedd5-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="dedd5-288">Vælg **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="dedd5-289">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-289">Select **Delete**.</span></span>
3. <span data-ttu-id="dedd5-290">Vælg **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="dedd5-291">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-291">Select **Delete**.</span></span>
5. <span data-ttu-id="dedd5-292">Vælg **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="dedd5-293">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-293">Select **Delete**.</span></span>
7. <span data-ttu-id="dedd5-294">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="dedd5-295">Du har genbrugt det samme beregnede felt **Model.Data2.Levels** flere gange i formatbindinger.</span><span class="sxs-lookup"><span data-stu-id="dedd5-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="dedd5-296">Det er meget lettere at bruge og vedligeholde et enkelt beregnet felt i stedet for at gøre dette for flere ens felter.</span><span class="sxs-lookup"><span data-stu-id="dedd5-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="dedd5-297">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="dedd5-298">Fuldfør tilpasset version af et afledt format</span><span class="sxs-lookup"><span data-stu-id="dedd5-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="dedd5-299">I oversigtspanelet **Versioner** skal du vælge **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="dedd5-300">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="dedd5-301">Eksportér fuldført version af et afledt format</span><span class="sxs-lookup"><span data-stu-id="dedd5-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="dedd5-302">Vælg **Format til at lære parameteriserede kald (brugerdefineret)** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="dedd5-303">I oversigtspanelet **Versioner** skal du vælge den fuldførte version 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="dedd5-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="dedd5-304">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="dedd5-305">Vælg **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="dedd5-306">Gem den hentede konfiguration lokalt i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="dedd5-307">Test ER-formater</span><span class="sxs-lookup"><span data-stu-id="dedd5-307">Test ER formats</span></span> 
<span data-ttu-id="dedd5-308">Du kan køre det første og det forbedrede ER-format for at sikre dig, at konfigurerede parameteriserede beregnede felter fungerer korrekt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="dedd5-309">Importér ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="dedd5-309">Import ER configurations</span></span>
<span data-ttu-id="dedd5-310">Du kan importere evaluerede konfigurationer fra RCS ved hjælp af ER-lageret af typen **RCS**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="dedd5-311">Hvis du allerede har gennemgået trinnene i emnet, kan du [Importere konfigurationer af elektronisk rapportering (ER) fra Regulatory Configuration Services (RCS)](rcs-download-configurations.md), kan du bruge det konfigurerede ER-lager til at importere konfigurationer, der er beskrevet tidligere i dette emne, for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="dedd5-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="dedd5-312">Ellers kan du udføre disse trin:</span><span class="sxs-lookup"><span data-stu-id="dedd5-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="dedd5-313">Vælg **DEMF**-firma, og vælg **Elektronisk rapportering** i standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="dedd5-314">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="dedd5-315">Importér konfigurationer fra Microsoft Download Center i følgende rækkefølge: datamodel, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="dedd5-316">Udfør følgende trin for hver ER-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="dedd5-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="dedd5-317">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="dedd5-318">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="dedd5-319">Vælg **Gennemse** for at vælge den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="dedd5-320">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-320">Select **OK**.</span></span>

4. <span data-ttu-id="dedd5-321">Importér de eksporterede fra den fuldførte RCS version 1.1.1 i formatet **Format til at lære parameteriserede kald (brugerdefineret)**:</span><span class="sxs-lookup"><span data-stu-id="dedd5-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="dedd5-322">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="dedd5-323">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="dedd5-324">Vælg **Gennemse** for at vælge den lokalt lagrede fil for **Format til at lære parameteriserede kald (brugerdefineret)** i XML-format.</span><span class="sxs-lookup"><span data-stu-id="dedd5-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="dedd5-325">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="dedd5-326">Kør ER-formater</span><span class="sxs-lookup"><span data-stu-id="dedd5-326">Run ER formats</span></span>

1. <span data-ttu-id="dedd5-327">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="dedd5-328">Vælg **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="dedd5-329">Vælg **Kør** på det øverste niveau af båndet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="dedd5-330">Gem det lokalt oprettede output.</span><span class="sxs-lookup"><span data-stu-id="dedd5-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="dedd5-331">Vælg emnet **Format til at lære parameteriserede kald (brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="dedd5-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="dedd5-332">Vælg **Kør** på det øverste niveau af båndet.</span><span class="sxs-lookup"><span data-stu-id="dedd5-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="dedd5-333">Gem det oprettede output lokalt.</span><span class="sxs-lookup"><span data-stu-id="dedd5-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="dedd5-334">Sammenlign indholdet af de genererede output.</span><span class="sxs-lookup"><span data-stu-id="dedd5-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dedd5-335">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dedd5-335">Additional resources</span></span>
[<span data-ttu-id="dedd5-336">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="dedd5-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
