---
title: Konfigurer ER-formater for at bruge de parametre, der er angivet for den enkelte juridiske enhed
description: I dette emne forklares det, hvordan du kan konfigurere Elektroniske rapporteringsformater til at bruge de parametre, der er angivet for den enkelte juridiske enhed.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9253191f9cd10e0b3c87d61991598f9b791c35d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570728"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="0d970-103">Konfigurer ER-formater for at bruge de parametre, der er angivet for den enkelte juridiske enhed</span><span class="sxs-lookup"><span data-stu-id="0d970-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="0d970-104">Oversigt</span><span class="sxs-lookup"><span data-stu-id="0d970-104">Overview</span></span>

<span data-ttu-id="0d970-105">I mange af de Elektroniske rapporteringsformater, du kommer til at designe, skal du filtrere data ved hjælp af et sæt værdier, der er specifikke for de enkelte juridiske enheder i din forekomst (f.eks. et sæt momskoder til filtrering af momstransaktioner).</span><span class="sxs-lookup"><span data-stu-id="0d970-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="0d970-106">Når filtrering af denne type i øjeblikket er konfigureret i et ER-format, bruges de værdier, der er afhængige af den juridiske enhed (f.eks. momskoder) i udtryk for ER-formatet, til at angive data filtreringsregler.</span><span class="sxs-lookup"><span data-stu-id="0d970-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="0d970-107">ER-formatet er derfor gjort specifikt for den juridiske enheds, og hvis du vil generere de nødvendige rapporter, skal du oprette afledte kopier af det oprindelige ER-format for hver juridisk enhed, hvor du skal køre ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="0d970-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="0d970-108">Hvert afledte ER-format skal redigeres for at samle de specifikke værdier for juridiske i det, og omorganiseres, når den oprindelige (basis)version er blevet opdateret, eksporteret fra et testmiljø og importeret til et produktionsmiljø, når det skal udrulles med henblik på anvendelse i produktionen osv.</span><span class="sxs-lookup"><span data-stu-id="0d970-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="0d970-109">Vedligeholdelse af denne type af konfigurerede ER-løsninger er derfor temmelig kompliceret og tidskrævende af flere årsager:</span><span class="sxs-lookup"><span data-stu-id="0d970-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="0d970-110">Jo flere juridiske enheder der er, des flere ER-formatkonfigurationer skal der vedligeholdes.</span><span class="sxs-lookup"><span data-stu-id="0d970-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="0d970-111">Vedligeholdelse af ER-konfigurationer kræver, at erhvervsbrugere er bekendt med ER.</span><span class="sxs-lookup"><span data-stu-id="0d970-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="0d970-112">De ER-programspecifikke parametre gør det muligt for superbrugere at konfigurere datafiltreringen i et ER-format, så den er baseret på et sæt abstrakte regler.</span><span class="sxs-lookup"><span data-stu-id="0d970-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="0d970-113">Dette sæt regler kan konfigureres til at bruge de datakilder, der er tilgængelige i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="0d970-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="0d970-114">Erhvervsbrugere kan derefter angive de rigtige regler ud over den bevarede ER-ramme ved hjælp af den brugergrænseflade (UI), der genereres automatisk på basis af indstillingerne for det tilsvarende ER-format og de aktuelle oplysninger om den juridiske enhed, du har adgang til i ER-formatets datakilder.</span><span class="sxs-lookup"><span data-stu-id="0d970-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="0d970-115">Regelsættet, der er angivet for et ER-format, kan eksporteres fra Dynamics 365 Finance (Finance)'s aktuelle juridiske enhed for forekomsten.</span><span class="sxs-lookup"><span data-stu-id="0d970-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="0d970-116">Det kan derefter importeres til en anden juridisk enhed af enten den samme Finance-forekomst eller en anden forekomst som et sæt regler for det samme ER-format.</span><span class="sxs-lookup"><span data-stu-id="0d970-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d970-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="0d970-117">Prerequisites</span></span>

<span data-ttu-id="0d970-118">For at gennemføre eksemplerne i dette emne, skal du have adgang til den forekomst af Regulatory Configuration Service (RCS), der er klargjort til den samme lejer som Finance, for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="0d970-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="0d970-119">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="0d970-119">Electronic reporting developer</span></span>
- <span data-ttu-id="0d970-120">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="0d970-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="0d970-121">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="0d970-121">System administrator</span></span>

<span data-ttu-id="0d970-122">Vi anbefaler, at du udfører trinnene i emnet [Understøt parameteriserede opkald om ER-datakilder af typen BEREGNET FELT](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="0d970-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="0d970-123">Hvis du allerede har fuldført disse trin, kan du springe trinnene i den efterfølgende sektion **Importer ER-konfigurationer til RCS** over.</span><span class="sxs-lookup"><span data-stu-id="0d970-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="0d970-124">Importer ER-konfigurationer til RCS</span><span class="sxs-lookup"><span data-stu-id="0d970-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="0d970-125">Fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448) skal du hente zip-filen **Understøt parameteriserede opkald om ER-datakilder af typen BEREGNET FELT**.</span><span class="sxs-lookup"><span data-stu-id="0d970-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="0d970-126">Den zip-fil indeholder følgende ER-konfigurationer, der skal udtrækkes og gemmes lokalt.</span><span class="sxs-lookup"><span data-stu-id="0d970-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="0d970-127">**Indholdsbeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="0d970-127">**Content description**</span></span>                        | <span data-ttu-id="0d970-128">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="0d970-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d970-129">Eksempel på konfigurationsfil for **ER-datamodel**</span><span class="sxs-lookup"><span data-stu-id="0d970-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="0d970-130">Model til at lære parameteriserede calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="0d970-131">Eksempel på konfigurationsfil for **ER-metadata**</span><span class="sxs-lookup"><span data-stu-id="0d970-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="0d970-132">Metadata til at lære parameteriserede calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="0d970-133">Eksempel på konfigurationsfil for **ER-modeltilknytning**</span><span class="sxs-lookup"><span data-stu-id="0d970-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="0d970-134">Tilknytning for at lære parameteriserede calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="0d970-135">Eksempel på konfiguration af **ER-format**</span><span class="sxs-lookup"><span data-stu-id="0d970-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="0d970-136">Format til at lære parameteriserede calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="0d970-137">Dernæst skal du logge på din RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="0d970-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="0d970-138">I dette eksempel skal du oprette en konfiguration til eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="0d970-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="0d970-139">Før du kan fuldføre denne procedure skal du fuldføre trinnene i emnet [Opret en konfigurationsudbyder og marker den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.</span><span class="sxs-lookup"><span data-stu-id="0d970-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="0d970-140">Vælg **Elektronisk rapportering** på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="0d970-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="0d970-141">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="0d970-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="0d970-142">Importér de ER-konfigurationer, som du downloadede tidligere, til RCS i følgende rækkefølge: datamodel, metadata, modeltilknytning og format.</span><span class="sxs-lookup"><span data-stu-id="0d970-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="0d970-143">Benyt følgende fremgangsmåde for hver ER-konfiguration:</span><span class="sxs-lookup"><span data-stu-id="0d970-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="0d970-144">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="0d970-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="0d970-145">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="0d970-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="0d970-146">Vælg **Gennemse** for at vælge filen til den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="0d970-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="0d970-147">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="0d970-148">Gennemse den ER-løsning, der leveres</span><span class="sxs-lookup"><span data-stu-id="0d970-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="0d970-149">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="0d970-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="0d970-150">Vælg emnet **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="0d970-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="0d970-151">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="0d970-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="0d970-152">Vælg **Udvid/skjul**.</span><span class="sxs-lookup"><span data-stu-id="0d970-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="0d970-153">ER-formatet **Format til at lære parametriserede opkald** er designet, så der oprettes en momsangivelse i XML-format, der indeholder flere momsniveauer (almindelig, reduceret og ingen).</span><span class="sxs-lookup"><span data-stu-id="0d970-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="0d970-154">Hvert niveau har et forskelligt antal detaljer.</span><span class="sxs-lookup"><span data-stu-id="0d970-154">Each level has a different number of details.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="0d970-156">På fanen **Tilknytning** skal du udvide objekterne **Model**, **Data** og **Opsummering**.</span><span class="sxs-lookup"><span data-stu-id="0d970-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="0d970-157">Datakilden **Model.Data.Opsummering** returnerer listen over momstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="0d970-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="0d970-158">Disse transaktioner opsummeres efter momskode.</span><span class="sxs-lookup"><span data-stu-id="0d970-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="0d970-159">For denne datakilde er det beregnede felt **Model.Data.Opsummering.Niveau** konfigureret til at returnere koden for momsniveauet for hver opsummeret post.</span><span class="sxs-lookup"><span data-stu-id="0d970-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="0d970-160">For alle momskoder, der kan hentes fra datakilden **Model.Data.Opsummering.Niveau** på kørselstidspunktet, returneres koden for momsniveau (**Almindelig**, **Reduceret**, **Ingen** eller **Andre**) som en tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="0d970-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="0d970-161">Det beregnede felt **Model.Data.Opsummering** bruges til at filtrere poster for datakilden **Model. Data.Opsummering** og angiver de filtrerede data i hvert XML-element, der repræsenterer et beskatningsniveau, ved hjælp af felterne **Model.Data2.Niveau1**, **Model.Data2.Niveau2** og **Model.Data2.Niveau3**.</span><span class="sxs-lookup"><span data-stu-id="0d970-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="0d970-163">Det beregnede felt **Model.Data.Opsummering** er konfigureret, så det indeholder et ET-udtryk.</span><span class="sxs-lookup"><span data-stu-id="0d970-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="0d970-164">Bemærk, at momskoderne codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) er hardcoded ind i denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d970-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="0d970-165">Derfor er dette ER-format afhængigt af den juridiske enhed, hvor disse momskoder er blevet konfigureret.</span><span class="sxs-lookup"><span data-stu-id="0d970-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="0d970-167">Hvis du vil understøtte forskellige sæt momskoder for hver juridisk enhed, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="0d970-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="0d970-168">Opret en afledt version af ER-formatet for hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="0d970-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="0d970-169">Opdater momskoderne i det beregnede felt **Model.Data.Opsummering.Niveau** ud fra indstillingen for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="0d970-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="0d970-170">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="0d970-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="0d970-171">Oprette et afledt format</span><span class="sxs-lookup"><span data-stu-id="0d970-171">Create a derived format</span></span>

<span data-ttu-id="0d970-172">Derefter skal du bruge funktionen programspecifikke parametre for ER til at understøtte et andet sæt momskoder for hver juridisk enhed i et enkelt ER-format.</span><span class="sxs-lookup"><span data-stu-id="0d970-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="0d970-173">Udvid indholdet af elementet **Model til at lære parameteriserede kald** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="0d970-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="0d970-174">Vælg emnet **Format til at lære parameteriserede kald**.</span><span class="sxs-lookup"><span data-stu-id="0d970-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="0d970-175">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0d970-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="0d970-176">Vælg indstillingen **Afledt fra navn: Format til at lære parameteriserede kald, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="0d970-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="0d970-177">Gå til feltet **Navn**, og angiv **Format til at lære, hvordan man leder efter LE-data**.</span><span class="sxs-lookup"><span data-stu-id="0d970-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="0d970-178">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0d970-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="0d970-179">Konfigurer et afledt format</span><span class="sxs-lookup"><span data-stu-id="0d970-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="0d970-180">Tilføj et fasttekst-format</span><span class="sxs-lookup"><span data-stu-id="0d970-180">Add a format enumeration</span></span>

<span data-ttu-id="0d970-181">Derefter skal du tilføje et nyt ER-fasttekstformat.</span><span class="sxs-lookup"><span data-stu-id="0d970-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="0d970-182">Værdierne i dette fasttekstformat vises for erhvervsbrugere, der angiver de juridiske enheds-afhængige sæt momskoder for de forskellige beskatningsniveauer, der bruges i ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="0d970-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="0d970-183">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="0d970-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="0d970-184">Vælg **Fasttekst-formater**.</span><span class="sxs-lookup"><span data-stu-id="0d970-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="0d970-185">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="0d970-185">Select **Add**.</span></span>
4.  <span data-ttu-id="0d970-186">I feltet **Navn** skal du angive **Liste med beskatningsniveauer**.</span><span class="sxs-lookup"><span data-stu-id="0d970-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="0d970-187">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-187">Select **Save**.</span></span>
6.  <span data-ttu-id="0d970-188">Vælg **Tilføj** under fanen **Værdier for fasttekstformat**.</span><span class="sxs-lookup"><span data-stu-id="0d970-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="0d970-189">I feltet **Navn** skal du angive **Almindelig beskatning**.</span><span class="sxs-lookup"><span data-stu-id="0d970-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="0d970-190">Vælg **Tilføj** igen.</span><span class="sxs-lookup"><span data-stu-id="0d970-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="0d970-191">I feltet **Navn** skal du angive **Reduceret beskatning**.</span><span class="sxs-lookup"><span data-stu-id="0d970-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="0d970-192">Vælg **Tilføj** igen.</span><span class="sxs-lookup"><span data-stu-id="0d970-192">Select **Add** again.</span></span>
11. <span data-ttu-id="0d970-193">I feltet **Navn** skal du angive **Ingen beskatning**.</span><span class="sxs-lookup"><span data-stu-id="0d970-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="0d970-194">Vælg **Tilføj** igen.</span><span class="sxs-lookup"><span data-stu-id="0d970-194">Select **Add** again.</span></span>
13. <span data-ttu-id="0d970-195">I feltet **Navn** skal du skrive **Andet**.</span><span class="sxs-lookup"><span data-stu-id="0d970-195">In the **Name** field, enter **Other**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="0d970-197">Da erhvervsbrugere kan bruge forskellige sprog til at angive juridisk enheds-afhængige sæt momskoder, anbefales det, at du oversætter værdierne i denne optælling til de sprog, der er konfigureret som de foretrukne sprog for disse brugere i Finance.</span><span class="sxs-lookup"><span data-stu-id="0d970-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="0d970-198">Vælg en post for **Ingen beskatning**.</span><span class="sxs-lookup"><span data-stu-id="0d970-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="0d970-199">Klik på feltet **Etikette**.</span><span class="sxs-lookup"><span data-stu-id="0d970-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="0d970-200">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="0d970-200">Select **Translate**.</span></span>
17. <span data-ttu-id="0d970-201">I panelet **Tekstoversættelse** i feltet **Etikette-ID** skal du indtaste **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="0d970-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="0d970-202">I feltet **Tekst i standardsprog** skal du indtaste **Ingen beskatning**.</span><span class="sxs-lookup"><span data-stu-id="0d970-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="0d970-203">I feltet **Sprog** skal du vælge **DE**.</span><span class="sxs-lookup"><span data-stu-id="0d970-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="0d970-204">I feltet **Oversat tekst** skal du indtaste **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="0d970-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="0d970-205">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="0d970-205">Select **Translate**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="0d970-207">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-207">Select **Save**.</span></span>
23. <span data-ttu-id="0d970-208">Luk siden **Fasttekstformat**.</span><span class="sxs-lookup"><span data-stu-id="0d970-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="0d970-209">Tilføje en ny opslagsdatakilde</span><span class="sxs-lookup"><span data-stu-id="0d970-209">Add a new lookup data source</span></span>

<span data-ttu-id="0d970-210">Derefter skal du tilføje en ny datakilde for at angive, hvordan erhvervsbrugere skal angive de juridiske enhedsafhængige regler for at genkende det korrekte beskatningsniveau for hver enkelt opsummerede transaktionspost.</span><span class="sxs-lookup"><span data-stu-id="0d970-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="0d970-211">På fanen **Tilknytning** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="0d970-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="0d970-212">Vælg **Fasttekst-format\Opslag**.</span><span class="sxs-lookup"><span data-stu-id="0d970-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="0d970-213">Du har netop identificeret, at de enkelte regler, som erhvervsbrugere angiver for genkendelse af beskatningsniveau, skal returnere en værdi i et ER-fasttekstformat.</span><span class="sxs-lookup"><span data-stu-id="0d970-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="0d970-214">Bemærk, at datakildetypen **Opslag** kan tilgås under blokkene **Datamodel** og **Dynamics 365 for Operations** ud over blokken **Fasttekstformat**.</span><span class="sxs-lookup"><span data-stu-id="0d970-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="0d970-215">Du kan derfor bruge fasttekst for ER-datamodeller og programmer til at angive den type værdier, der skal returneres for datakilder af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="0d970-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="0d970-216">I feltet **Navn** skal du angive **Vælger**.</span><span class="sxs-lookup"><span data-stu-id="0d970-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="0d970-217">I feltet **Fasttekstformat** skal du vælge **Liste med beskatningsniveauer**.</span><span class="sxs-lookup"><span data-stu-id="0d970-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="0d970-218">Du har netop angivet, at for hver regel, der er angivet i denne datakilde, skal en erhvervsbruger vælge en af værdierne fra fasttekstformatet **Listen over beskatningsniveauer** som en returneret værdi.</span><span class="sxs-lookup"><span data-stu-id="0d970-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="0d970-219">Vælg **Rediger opslag**.</span><span class="sxs-lookup"><span data-stu-id="0d970-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="0d970-220">Vælg **Kolonner**.</span><span class="sxs-lookup"><span data-stu-id="0d970-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="0d970-221">Udvid elementet **Model**.</span><span class="sxs-lookup"><span data-stu-id="0d970-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="0d970-222">Udvid elementet **Data**.</span><span class="sxs-lookup"><span data-stu-id="0d970-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="0d970-223">Udvid elementet **Moms**.</span><span class="sxs-lookup"><span data-stu-id="0d970-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="0d970-224">Vælg elementet varen **Model.Data.Moms.Code**.</span><span class="sxs-lookup"><span data-stu-id="0d970-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="0d970-225">Klik på knappen **Tilføj** (pilen til højre).</span><span class="sxs-lookup"><span data-stu-id="0d970-225">Select the **Add** button (the right arrow).</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="0d970-227">Du har netop angivet, at for hver regel, der er angivet i denne datakilde for genkendelse af beskatningsniveau, skal en erhvervsbruger vælge en af momskoderne som en betingelse.</span><span class="sxs-lookup"><span data-stu-id="0d970-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="0d970-228">Den liste over momskoder, som erhvervsbrugeren kan vælge, vil blive returneret af datakilden **Model.Data.Moms**.</span><span class="sxs-lookup"><span data-stu-id="0d970-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="0d970-229">Da denne datakilde indeholder feltet **Navn**, vises navnet på momskoden for hver momskodeværdi i det opslag, der vises for erhvervsbrugeren.</span><span class="sxs-lookup"><span data-stu-id="0d970-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="0d970-230">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-230">Select **OK**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="0d970-232">Erhvervsbrugere kan tilføje flere regler som poster i denne datakilde.</span><span class="sxs-lookup"><span data-stu-id="0d970-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="0d970-233">Hver post nummereres af en stregkode.</span><span class="sxs-lookup"><span data-stu-id="0d970-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="0d970-234">Reglerne evalueres i rækkefølge efter stigende linjenummer.</span><span class="sxs-lookup"><span data-stu-id="0d970-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="0d970-235">Da du har valgt feltet **Momskode** som en betingelse for reglerne i denne opslagsdatakilde, og idet **Momskode** er konfigureret som et felt af datatypen **Streng**, evalueres hver regel på tidspunktet for kørslen ved at sammenligne den momskode, der overføres til datakilden med den momskode, der er defineret i denne post i datakilden.</span><span class="sxs-lookup"><span data-stu-id="0d970-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="0d970-236">Når der findes en regel, der opfylder den konfigurerede betingelse, returnerer denne datakilde opslagsværdien for den regel, der er defineret i feltet **Opslagsresultat**.</span><span class="sxs-lookup"><span data-stu-id="0d970-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="0d970-237">Hvis der ikke findes en regel, udløses der en undtagelse, der giver brugeren besked om, at den aktuelle datakilde ikke kan returnere en korrekt værdi.</span><span class="sxs-lookup"><span data-stu-id="0d970-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="0d970-238">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-238">Select **Save**.</span></span>
14. <span data-ttu-id="0d970-239">Luk siden **Opslagsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="0d970-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="0d970-240">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-240">Select **OK**.</span></span>

    <span data-ttu-id="0d970-241">Bemærk, at du har tilføjet en ny datakilde, der returnerer beskatningsniveauet, som værdi i fasttekstformatet **Liste over beskatningsniveauværdier**, som videregives til datakilden som argument for parametret **Kode** i datatypen **Streng**.</span><span class="sxs-lookup"><span data-stu-id="0d970-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="0d970-243">Bemærk, at evalueringen af konfigurerede regler afhænger af datatypen for de felter, der er valgt til at skulle definere betingelserne for disse regler.</span><span class="sxs-lookup"><span data-stu-id="0d970-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="0d970-244">Når du vælger et felt, der er konfigureret som et felt af datatypen **Numerisk** eller **data**, vil kriterierne være forskellige fra de kriterier, der blev beskrevet tidligere for datatypen **Streng**.</span><span class="sxs-lookup"><span data-stu-id="0d970-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="0d970-245">I felterne **Numerisk** og **Dato** skal reglen angives som et værdiinterval.</span><span class="sxs-lookup"><span data-stu-id="0d970-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="0d970-246">Reglens betingelse betragtes derefter som opfyldt, når en værdi, der overføres til datakilden, ligger inden for det konfigurerede interval.</span><span class="sxs-lookup"><span data-stu-id="0d970-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="0d970-247">I følgende illustration vises et eksempel på denne type opsætning.</span><span class="sxs-lookup"><span data-stu-id="0d970-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="0d970-248">Ud over feltet **Model.Data.Moms.Kode** af datatypen **Streng** er det feltet **Model.Moms.Opsummering.Grundlag** for datatypen **Reel**, der bruges til at angive betingelser for en opslagsdatakilde.</span><span class="sxs-lookup"><span data-stu-id="0d970-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="0d970-250">Da felterne **Model.Data.Moms.Kode** og **Model.Moms.Opsummering.Grundlag** er markeret for denne opslagsdatakilde, konfigureres hver enkelt regel i denne datakilde på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0d970-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="0d970-251">På den liste, der vises, skal værdien af fasttekstformatet **Listen over beskatningsniveauer** være angivet som en returneret værdi.</span><span class="sxs-lookup"><span data-stu-id="0d970-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="0d970-252">Momskoden skal angives som betingelse for reglen.</span><span class="sxs-lookup"><span data-stu-id="0d970-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="0d970-253">Det er kun de momskoder, der leveres af datakilden **Model.Data.Moms**, der er anvendelige.</span><span class="sxs-lookup"><span data-stu-id="0d970-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="0d970-254">Minimum- og maksimumværdierne for momsgrundlagsbeløbet skal angives som betingelser for reglen.</span><span class="sxs-lookup"><span data-stu-id="0d970-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="0d970-255">Her er, hvordan hver regel i denne datakilde evalueres under kørsel:</span><span class="sxs-lookup"><span data-stu-id="0d970-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="0d970-256">Er koden for datatypen **Streng**, der blev overført til denne datakilde, lig med en regels momskode?</span><span class="sxs-lookup"><span data-stu-id="0d970-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="0d970-257">Falder værdien af datatypen **Reel**, der blev overført til denne datakilde, mellem bestemte minimum- og maksimumværdier?</span><span class="sxs-lookup"><span data-stu-id="0d970-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="0d970-258">En regel anses for at være anvendelig, når begge betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="0d970-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="0d970-259">Oversæt etiketten for den opslagsdatakilde, der blev tilføjet</span><span class="sxs-lookup"><span data-stu-id="0d970-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="0d970-260">Da erhvervsbrugere kan bruge forskellige sprog til at angive juridisk enheds-afhængige sæt momskoder, anbefales det, at du oversætter etiketten i alle opslagsdatakilder, som du har tilføjet, således at det fremstår i hver brugers foretrukne sprog på den tilsvarende side.</span><span class="sxs-lookup"><span data-stu-id="0d970-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="0d970-261">Vælg datakilden **Model.Data.Vælger**.</span><span class="sxs-lookup"><span data-stu-id="0d970-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="0d970-262">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0d970-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="0d970-263">Klik på feltet **Etikette**.</span><span class="sxs-lookup"><span data-stu-id="0d970-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="0d970-264">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="0d970-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="0d970-265">I panelet **Tekstoversættelse** i feltet **Etikette-ID** skal du indtaste **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="0d970-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="0d970-266">I feltet **Tekst i standardsprog** skal du angive **Vælg beskatningsniveau efter momskode**.</span><span class="sxs-lookup"><span data-stu-id="0d970-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="0d970-267">I feltet **Sprog** skal du vælge **DE**.</span><span class="sxs-lookup"><span data-stu-id="0d970-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="0d970-268">I feltet **Oversat tekst** skal du angive **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="0d970-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="0d970-269">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="0d970-269">Select **Translate**.</span></span>
10. <span data-ttu-id="0d970-270">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-270">Select **OK**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="0d970-272">Tilføje et nyt felt som skal bruge det konfigurerede opslag</span><span class="sxs-lookup"><span data-stu-id="0d970-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="0d970-273">Udvid elementet **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="0d970-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="0d970-274">Vælg elementet **Model.Data.Opsummering**.</span><span class="sxs-lookup"><span data-stu-id="0d970-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="0d970-275">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="0d970-275">Select **Add**.</span></span>
4.  <span data-ttu-id="0d970-276">Vælg **Funktioner/Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="0d970-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="0d970-277">I feltet **Navn** skal du angive **NiveauViaOpslag**.</span><span class="sxs-lookup"><span data-stu-id="0d970-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="0d970-278">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="0d970-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="0d970-279">I **Formelfeltet** skal du angive **Model.Vælger (Model.Data.Opsummering.Kode)**.</span><span class="sxs-lookup"><span data-stu-id="0d970-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="0d970-280">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-280">Select **Save**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="0d970-282">Luk siden **Formeleditor**.</span><span class="sxs-lookup"><span data-stu-id="0d970-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="0d970-283">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-283">Select **OK**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="0d970-285">Bemærk, at det beregnede felt **NiveauViaOpslag**, som du har tilføjet, returnerer beskatningsniveauet som værdien fasttekstformatet **Liste over beskatningsniveauer** for hver enkelt opsummeret momstransaktionspost.</span><span class="sxs-lookup"><span data-stu-id="0d970-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="0d970-286">Postens momskode overføres til opslagsdatakilden **Model.Vælger**, og regelsættet for denne datakilde vil blive brugt til at vælge det korrekte beskatningsniveau.</span><span class="sxs-lookup"><span data-stu-id="0d970-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="0d970-287">Tilføj en ny datakilde baseret på fasttekstformat</span><span class="sxs-lookup"><span data-stu-id="0d970-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="0d970-288">Derefter skal du tilføje en ny datakilde, der henviser til fasttekstformat, som du tidligere har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="0d970-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="0d970-289">Værdierne i denne datakilde vil blive brugt i et ET-formatudtryk senere.</span><span class="sxs-lookup"><span data-stu-id="0d970-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="0d970-290">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="0d970-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="0d970-291">Vælg **Fasttekst-formater\Fasttekst**.</span><span class="sxs-lookup"><span data-stu-id="0d970-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="0d970-292">I feltet **Navn** skal du angive **Beskatningsniveau**.</span><span class="sxs-lookup"><span data-stu-id="0d970-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="0d970-293">I feltet **Fasttekstformat** skal du vælge **Liste med beskatningsniveauer**.</span><span class="sxs-lookup"><span data-stu-id="0d970-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="0d970-294">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="0d970-295">Rediger et eksisterende felt for at begynde at bruge opslaget</span><span class="sxs-lookup"><span data-stu-id="0d970-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="0d970-296">Derefter skal du redigere det eksisterende beregnede felt, så det bruger den konfigurerede opslagsdatakilde til at returnere den korrekte værdi for værdier for beskatningsniveau, afhængigt af momskoden.</span><span class="sxs-lookup"><span data-stu-id="0d970-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="0d970-297">Vælg elementet **Model.Data.Opsummering.Niveau**.</span><span class="sxs-lookup"><span data-stu-id="0d970-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="0d970-298">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0d970-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="0d970-299">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="0d970-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="0d970-300">Bemærk, at det aktuelle udtryk for feltet **Model.Data.Opsummering.Niveau** indeholder følgende hardcodede momskoder:</span><span class="sxs-lookup"><span data-stu-id="0d970-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="0d970-301">SAG (@.Kode, "MOMS19", "Almindelig", "InVAT19", "Almindelig", "MOMS7", "Reduceret", "InVAT7", "Reduceret", "TREDJE", "Ingen", "InVAT0", "Ingen", "Andet")</span><span class="sxs-lookup"><span data-stu-id="0d970-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="0d970-302">I feltet **Formel** skal du skrive **SAG(@.NiveauViaOpslag, Beskatningsniveau.'Almindelig beskatning', "Almindelig", Beskatningsniveau.'Reduceret beskatning', "Reduceret", Beskatningsniveau.'Ingen beskatning', "Ingen", "Andet")**.</span><span class="sxs-lookup"><span data-stu-id="0d970-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![Side med ER-operationsdesigner](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="0d970-304">Bemærk, at udtrykket i feltet **Model.Data.Opsummering.Niveau** returnerer nu beskatningsniveauet baseret på momskoden for den aktuelle post og det sæt regler, som en erhvervsbruger konfigurerer i opslagsdatakilden **Model.Data.Vælger**.</span><span class="sxs-lookup"><span data-stu-id="0d970-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="0d970-305">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-305">Select **Save**.</span></span>
6.  <span data-ttu-id="0d970-306">Luk siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="0d970-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="0d970-307">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-307">Select **OK**.</span></span>
8.  <span data-ttu-id="0d970-308">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="0d970-308">Select **Save**.</span></span>
9.  <span data-ttu-id="0d970-309">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="0d970-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="0d970-310">Fuldfør kladdeversionen af et afledt format</span><span class="sxs-lookup"><span data-stu-id="0d970-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="0d970-311">På oversigtspanelet **Versioner** skal du vælge **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="0d970-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="0d970-312">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="0d970-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="0d970-313">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="0d970-314">Eksportér den fuldførte version af et tilpasset format</span><span class="sxs-lookup"><span data-stu-id="0d970-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="0d970-315">I konfigurationstræet skal du vælge elementet **Format for at lære, hvordan man slår LE-data op**.</span><span class="sxs-lookup"><span data-stu-id="0d970-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="0d970-316">På fanen **Versioner** skal du vælge den post, der har statussen **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="0d970-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="0d970-317">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="0d970-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="0d970-318">Vælg **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="0d970-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="0d970-319">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d970-319">Select **OK**.</span></span>
6.  <span data-ttu-id="0d970-320">Webbrowseren henter en **Format for at lære, hvordan du søger efter LE-data.xml**-fil.</span><span class="sxs-lookup"><span data-stu-id="0d970-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="0d970-321">Gem filen lokalt.</span><span class="sxs-lookup"><span data-stu-id="0d970-321">Store this file locally.</span></span>

<span data-ttu-id="0d970-322">Gentag trinnene i dette afsnit for overordnede elementer i formatet **Format til at lære, hvordan du søger efter LE-data**, og gem følgende filer lokalt:</span><span class="sxs-lookup"><span data-stu-id="0d970-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="0d970-323">Format til at lære parameteriserede kald.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="0d970-324">Tilknytning for at lære parameteriserede kald.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="0d970-325">Model til at lære parameteriserede kald.xml</span><span class="sxs-lookup"><span data-stu-id="0d970-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="0d970-326">Du kan få mere at vide om konfigurationen af ER-formatet **Format til at lære, hvordan du søger efter LE-data** til at konfigurere juridisk enhedsafhængige sæt af momskoder for at filtrere momstransaktioner efter forskellige beskatningsniveauer ved at fuldføre trinnene i emnet [Konfigurer parametrene for et ER-format for hver juridisk enhed](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="0d970-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d970-327">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0d970-327">Additional resources</span></span>

[<span data-ttu-id="0d970-328">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="0d970-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="0d970-329">Konfigurer parametrene for et ER-format for hver juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="0d970-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]