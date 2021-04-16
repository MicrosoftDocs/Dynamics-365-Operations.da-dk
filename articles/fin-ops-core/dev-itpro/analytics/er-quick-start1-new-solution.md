---
title: Designe en ny ER-løsning til udskrivning af en brugerdefineret rapport
description: Dette emne forklarer, hvordan du kan designe en elektronisk rapporteringsløsning (ER) til udskrivning af en brugerdefineret rapport.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 986beb6d46ac69192206c86fc3660c2e2345d6a9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743721"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="e387c-103">Designe en ny ER-løsning til udskrivning af en brugerdefineret rapport</span><span class="sxs-lookup"><span data-stu-id="e387c-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e387c-104">I følgende fremgangsmåde forklares det, hvordan en bruger i rollen Systemadministrator, Udvikler af elektronisk rapportering eller Funktionel konsulent til elektronisk rapportering kan konfigurere parametre for ER-strukturen, designe de krævede konfigurationer af en ny ER-løsning for at få adgang til dataene i et bestemt virksomhedsdomæne og generere en brugerdefineret rapport i Microsoft Office-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="e387c-105">Disse trin kan udføres i **USMF**-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="e387c-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="e387c-106">Konfigurere ER-strukturen</span><span class="sxs-lookup"><span data-stu-id="e387c-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="e387c-107">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="e387c-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="e387c-108">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="e387c-109">Gennemse listen over udbydere af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="e387c-110">Tilføje en ny udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="e387c-111">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="e387c-112">Designe en domænespecifik datamodel</span><span class="sxs-lookup"><span data-stu-id="e387c-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="e387c-113">Importere en datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="e387c-114">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="e387c-115">Navngive datamodellen</span><span class="sxs-lookup"><span data-stu-id="e387c-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="e387c-116">Tilføje datamodelfelter</span><span class="sxs-lookup"><span data-stu-id="e387c-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="e387c-117">Fuldføre designet af datamodellen</span><span class="sxs-lookup"><span data-stu-id="e387c-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="e387c-118">Designe en modeltilknytning til den konfigurerede datamodel</span><span class="sxs-lookup"><span data-stu-id="e387c-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="e387c-119">Importere en ny konfiguration af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="e387c-120">Oprette en ny konfiguration af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="e387c-121">Designe en ny komponent til modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="e387c-122">Tilføje datakilder for at få adgang til programtabeller</span><span class="sxs-lookup"><span data-stu-id="e387c-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="e387c-123">Tilføje datakilder for at få adgang til programoptællinger</span><span class="sxs-lookup"><span data-stu-id="e387c-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="e387c-124">Tilføje ER-etiketter for at generere en rapport på et angivet sprog</span><span class="sxs-lookup"><span data-stu-id="e387c-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="e387c-125">Tilføje en datakilde for at transformere resultaterne af sammenligning af optællingsværdier med en tekstværdi</span><span class="sxs-lookup"><span data-stu-id="e387c-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="e387c-126">Knytte datakilder til datamodelfelter</span><span class="sxs-lookup"><span data-stu-id="e387c-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="e387c-127">Fuldføre designet af modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="e387c-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="e387c-128">Designe en skabelon til en brugerdefineret rapport</span><span class="sxs-lookup"><span data-stu-id="e387c-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="e387c-129">Design et format</span><span class="sxs-lookup"><span data-stu-id="e387c-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="e387c-130">Importere en designet formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="e387c-131">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="e387c-132">Importere en rapportskabelon</span><span class="sxs-lookup"><span data-stu-id="e387c-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="e387c-133">Konfigurere et format</span><span class="sxs-lookup"><span data-stu-id="e387c-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="e387c-134">Definere databinding for en rapporttitel</span><span class="sxs-lookup"><span data-stu-id="e387c-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="e387c-135">Gennemse modeldatakilden</span><span class="sxs-lookup"><span data-stu-id="e387c-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="e387c-136">Binde formatelementer til datakildefelter</span><span class="sxs-lookup"><span data-stu-id="e387c-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="e387c-137">Køre et designet format fra ER</span><span class="sxs-lookup"><span data-stu-id="e387c-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="e387c-138">Finjustere et designet format</span><span class="sxs-lookup"><span data-stu-id="e387c-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="e387c-139">Ændre et format for at ændre navnet på et oprettet dokument</span><span class="sxs-lookup"><span data-stu-id="e387c-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="e387c-140">Redigere et format for at ændre rækkefølgen af spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="e387c-141">Køre et ændret format fra ER</span><span class="sxs-lookup"><span data-stu-id="e387c-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="e387c-142">Fuldføre formatdesignet</span><span class="sxs-lookup"><span data-stu-id="e387c-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="e387c-143">Udvikle programartefakter for at kalde den designede rapport</span><span class="sxs-lookup"><span data-stu-id="e387c-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="e387c-144">Ændre kildekode</span><span class="sxs-lookup"><span data-stu-id="e387c-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="e387c-145">Tilføje en datakontraktklasse</span><span class="sxs-lookup"><span data-stu-id="e387c-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="e387c-146">Tilføje en klasse for brugergrænsefladegenerator</span><span class="sxs-lookup"><span data-stu-id="e387c-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="e387c-147">Tilføje en klasse for dataprovider</span><span class="sxs-lookup"><span data-stu-id="e387c-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="e387c-148">Tilføje en etiketfil</span><span class="sxs-lookup"><span data-stu-id="e387c-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="e387c-149">Tilføje en rapportserviceklasse</span><span class="sxs-lookup"><span data-stu-id="e387c-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="e387c-150">Tilføje en klasse for rapport-controller</span><span class="sxs-lookup"><span data-stu-id="e387c-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="e387c-151">Tilføje et menupunkt</span><span class="sxs-lookup"><span data-stu-id="e387c-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="e387c-152">Tilføje et menupunkt til en menu</span><span class="sxs-lookup"><span data-stu-id="e387c-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="e387c-153">Bygge et Visual Studio-projekt</span><span class="sxs-lookup"><span data-stu-id="e387c-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="e387c-154">Køre et format fra applikationen</span><span class="sxs-lookup"><span data-stu-id="e387c-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="e387c-155">Tilpasse en designet ER-løsning</span><span class="sxs-lookup"><span data-stu-id="e387c-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="e387c-156">Redigere en modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="e387c-157">Tilføje datakilder for at få adgang til et datakontraktobjekt</span><span class="sxs-lookup"><span data-stu-id="e387c-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="e387c-158">Føje en datakilde for at få adgang til poster for ER-formattilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="e387c-159">Føje en datakilde for at få adgang til en formattilknytningspost for et aktuelt ER-format</span><span class="sxs-lookup"><span data-stu-id="e387c-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="e387c-160">Angive navnet på det aktuelle ER-format i datamodellen</span><span class="sxs-lookup"><span data-stu-id="e387c-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="e387c-161">Fuldføre designet af modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="e387c-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="e387c-162">Redigere et format</span><span class="sxs-lookup"><span data-stu-id="e387c-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="e387c-163">Tilføje et nyt formatelement</span><span class="sxs-lookup"><span data-stu-id="e387c-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="e387c-164">Binde det tilføjede formatelement</span><span class="sxs-lookup"><span data-stu-id="e387c-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="e387c-165">Fuldføre formatdesignet</span><span class="sxs-lookup"><span data-stu-id="e387c-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="e387c-166">Køre et format fra applikationen</span><span class="sxs-lookup"><span data-stu-id="e387c-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="e387c-167">Køre et format fra ER</span><span class="sxs-lookup"><span data-stu-id="e387c-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="e387c-168">Konfigurere en formatdestination til visning på skærmen</span><span class="sxs-lookup"><span data-stu-id="e387c-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="e387c-169">Køre et format fra applikationen for at vise det som et PDF-dokument</span><span class="sxs-lookup"><span data-stu-id="e387c-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="e387c-170">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e387c-170">Additional resources</span></span>](#References)

<span data-ttu-id="e387c-171">I dette eksempel skal du oprette en ny ER-løsning til modulet [Spørgeskema](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires).</span><span class="sxs-lookup"><span data-stu-id="e387c-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="e387c-172">Med denne nye ER-løsning kan du oprette en rapport ved at bruge et Microsoft Excel-regneark som skabelon.</span><span class="sxs-lookup"><span data-stu-id="e387c-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="e387c-173">Du kan derefter generere rapporten for **Spørgeskema** i Excel- eller PDF-format, ud over at generere den eksisterende rapport for SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="e387c-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="e387c-174">Du kan også ændre den nye rapport senere og efter anmodning.</span><span class="sxs-lookup"><span data-stu-id="e387c-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="e387c-175">Der kræves ingen kodning.</span><span class="sxs-lookup"><span data-stu-id="e387c-175">No coding is required.</span></span>

1. <span data-ttu-id="e387c-176">Hvis du vil køre den eksisterende rapport skal du gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Valg af menupunktet Rapport for spørgeskemaer i modulet Spørgeskema for at køre den eksisterende SSRS-rapport](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="e387c-178">Angiv valgkriterier i dialogboksen **Rapport for spørgeskemaer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="e387c-179">Anvend et filter, så rapporten kun indeholder spørgeskemaet **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="e387c-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Angivelse af valgkriterier i dialogboksen Rapport for spørgeskemaer](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="e387c-181">I følgende illustration vises den genererede version af SSRS-rapporten for spørgeskemaet **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="e387c-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Genereret SSRS-rapport](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="e387c-183">Konfigurere ER-strukturen</span><span class="sxs-lookup"><span data-stu-id="e387c-183">Configure the ER framework</span></span>

<span data-ttu-id="e387c-184">Som bruger i rollen Udvikler af elektronisk rapportering skal du konfigurere det minimale sæt af ER-parametre, før du kan begynde at bruge ER-strukturen til at designe din nye ER-løsning.</span><span class="sxs-lookup"><span data-stu-id="e387c-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="e387c-185">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="e387c-185">Configure ER parameters</span></span>

1. <span data-ttu-id="e387c-186">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e387c-187">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e387c-188">På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .</span><span class="sxs-lookup"><span data-stu-id="e387c-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="e387c-189">På fanen **Vedhæftede filer** kan du angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="e387c-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="e387c-190">Angiv feltet **Konfigurationer** til **Fil** for **USMF**-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="e387c-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="e387c-191">Angiv felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.</span><span class="sxs-lookup"><span data-stu-id="e387c-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="e387c-192">Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="e387c-193">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="e387c-194">Alle ER-konfigurationer er markeret som ejet af en udbyder af ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e387c-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="e387c-195">Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere nogen ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e387c-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="e387c-196">Det er kun ejeren af en ER-konfiguration, der kan redigere den.</span><span class="sxs-lookup"><span data-stu-id="e387c-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="e387c-197">Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="e387c-198">Gennemse listen over udbydere af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="e387c-199">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e387c-200">Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Konfigurationsudbydere** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="e387c-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="e387c-201">På siden **Konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e387c-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="e387c-202">Gennemse indholdet af denne side.</span><span class="sxs-lookup"><span data-stu-id="e387c-202">Review the contents of this page.</span></span> <span data-ttu-id="e387c-203">Hvis der allerede findes en post for **Litware, Inc.** (`https://www.litware.com`), skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="e387c-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="e387c-204">Tilføje en ny udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="e387c-205">På siden **Konfigurationsudbydere** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e387c-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="e387c-206">I feltet **Navn** skal du angive **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="e387c-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="e387c-207">I feltet **Internetadresse** skal du angive `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="e387c-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="e387c-208">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e387c-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="e387c-209">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="e387c-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="e387c-210">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e387c-211">I arbejdsområdet **Elektronisk rapportering** skal du vælge konfigurationsudbyderen **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="e387c-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="e387c-212">Vælg **Angiv aktive**.</span><span class="sxs-lookup"><span data-stu-id="e387c-212">Select **Set active**.</span></span>

<span data-ttu-id="e387c-213">Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="e387c-214">Designe en domænespecifik datamodel</span><span class="sxs-lookup"><span data-stu-id="e387c-214">Design a domain-specific data model</span></span>

<span data-ttu-id="e387c-215">Du skal oprette en ny ER-konfiguration, der indeholder en komponent til [datamodellen](general-electronic-reporting.md#data-model-and-model-mapping-components) til forretningsdomænet **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="e387c-216">Denne datamodel vil senere blive brugt som en datakilde, når du designer et ER-format til at generere rapporten for **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="e387c-217">Når du udfører fremgangsmåden i afsnittet [Importere en ny datamodelkonfiguration](#ImportDataModel), kan du importere den ønskede datamodel fra den angivne XML-fil.</span><span class="sxs-lookup"><span data-stu-id="e387c-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="e387c-218">Du kan også udføre fremgangsmåden i afsnittet [Oprette en ny datamodelkonfiguration](#DesignDataModel) for at designe denne datamodel fra bunden.</span><span class="sxs-lookup"><span data-stu-id="e387c-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="e387c-219">Importere en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="e387c-220">Hent filen [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="e387c-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e387c-221">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e387c-222">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="e387c-223">Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e387c-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="e387c-224">Vælg **Gennemse**, og find og vælg derefter filen **Questionnaires model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="e387c-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="e387c-225">Vælg **OK** for at importere konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e387c-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="e387c-226">Hvis du vil fortsætte, skal du springe over den næste procedure [Oprette en ny datamodelkonfiguration](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="e387c-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="e387c-227">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="e387c-228">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e387c-229">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e387c-230">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e387c-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="e387c-231">Åbn **Spørgeskemamodel** i feltet **Navn** i rulledialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e387c-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="e387c-232">Vælg **Opret konfiguration** for at oprette konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e387c-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="e387c-233">Navngive datamodellen</span><span class="sxs-lookup"><span data-stu-id="e387c-233">Name the data model</span></span>

1. <span data-ttu-id="e387c-234">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="e387c-235">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-235">Select **Designer**.</span></span>
3. <span data-ttu-id="e387c-236">Åbn <a name="DataModeName"></a>**Spørgeskemaer** i feltet **Navn** i oversigtspanelet **Generelt** på siden **Datamodeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="e387c-237">Tilføje nye datamodelfelter</span><span class="sxs-lookup"><span data-stu-id="e387c-237">Add new data model fields</span></span>

1. <span data-ttu-id="e387c-238">På siden **Datamodeldesigner** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e387c-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="e387c-239">Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:</span><span class="sxs-lookup"><span data-stu-id="e387c-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-240">Vælg **Modelrod** som type for den nye node.</span><span class="sxs-lookup"><span data-stu-id="e387c-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="e387c-241">I feltet **Navn** skal du skrive <a name="RootDefinitionName"></a>**Rod**.</span><span class="sxs-lookup"><span data-stu-id="e387c-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="e387c-242">Vælg **Tilføj** for at tilføje en ny node.</span><span class="sxs-lookup"><span data-stu-id="e387c-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="e387c-243">Denne rodbeskrivelse bruges til at levere data til rapporten for **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="e387c-244">En enkelt datamodel kan have flere beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="e387c-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="e387c-245">Hver beskrivelse kan angives for et enkelt ER-format for at identificere de data, der skal bruges til at generere rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="e387c-246">Vælg **Ny** igen, og udfør dernæst følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:</span><span class="sxs-lookup"><span data-stu-id="e387c-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-247">Vælg **Underordnet til en aktiv node** som typen af den nye node.</span><span class="sxs-lookup"><span data-stu-id="e387c-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="e387c-248">I feltet **Navn** skal du skrive **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="e387c-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="e387c-249">Vælg **Streng** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="e387c-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="e387c-250">Vælg **Tilføj** for at tilføje et nyt felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="e387c-251">Dette felt skal bruges til at overføre navnet på den aktuelle virksomhed til en ER-rapport, der bruger denne datamodel som datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="e387c-252">Vælg **Ny** igen, og udfør dernæst følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:</span><span class="sxs-lookup"><span data-stu-id="e387c-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-253">Vælg **Underordnet til en aktiv node** som typen af den nye node.</span><span class="sxs-lookup"><span data-stu-id="e387c-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="e387c-254">I feltet **Navn** skal du skrive **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="e387c-255">Vælg **Liste over poster** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="e387c-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="e387c-256">Vælg **Tilføj** for at tilføje et nyt felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="e387c-257">Dette felt skal bruges til at overføre listen over spørgeskemaer til en ER-rapport, der bruger denne datamodel som datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="e387c-258">Vælg noden **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="e387c-259">Fortsæt med at tilføje de krævede felter fra den redigerbare datamodel på samme måde, indtil du har fuldført følgende datamodelstruktur.</span><span class="sxs-lookup"><span data-stu-id="e387c-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="e387c-260">Feltsti</span><span class="sxs-lookup"><span data-stu-id="e387c-260">Field path</span></span>                                                    | <span data-ttu-id="e387c-261">Datatype</span><span class="sxs-lookup"><span data-stu-id="e387c-261">Data type</span></span>   | <span data-ttu-id="e387c-262">Feltbetegnelse/returneret værdi</span><span class="sxs-lookup"><span data-stu-id="e387c-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="e387c-263">Rod</span><span class="sxs-lookup"><span data-stu-id="e387c-263">Root</span></span>                                                          |             | <span data-ttu-id="e387c-264">Referencepunktet til anmodning om spørgeskemadata.</span><span class="sxs-lookup"><span data-stu-id="e387c-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="e387c-265">Rod\\Firmanavn</span><span class="sxs-lookup"><span data-stu-id="e387c-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="e387c-266">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-266">String</span></span>      | <span data-ttu-id="e387c-267">Navnet på den aktuelle virksomhed.</span><span class="sxs-lookup"><span data-stu-id="e387c-267">The name of the current company.</span></span> |
    | <span data-ttu-id="e387c-268">Rod\\Udførelseskontekst</span><span class="sxs-lookup"><span data-stu-id="e387c-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="e387c-269">Optag</span><span class="sxs-lookup"><span data-stu-id="e387c-269">Record</span></span>      | <span data-ttu-id="e387c-270">Detaljer om formatudførelse.</span><span class="sxs-lookup"><span data-stu-id="e387c-270">Format execution details.</span></span> |
    | <span data-ttu-id="e387c-271">Rod\\Udførelseskontekst\\Formatnavn</span><span class="sxs-lookup"><span data-stu-id="e387c-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="e387c-272">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-272">String</span></span>      | <span data-ttu-id="e387c-273">Navnet på det ER-format, der køres.</span><span class="sxs-lookup"><span data-stu-id="e387c-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="e387c-274">Rod\\Spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e387c-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="e387c-275">Liste over poster</span><span class="sxs-lookup"><span data-stu-id="e387c-275">Record list</span></span> | <span data-ttu-id="e387c-276">Listen over spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="e387c-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="e387c-277">Rod\\Spørgeskema\\Aktiv</span><span class="sxs-lookup"><span data-stu-id="e387c-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="e387c-278">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-278">String</span></span>      | <span data-ttu-id="e387c-279">Statussen for det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-280">Rod\\Spørgeskema\\Kode</span><span class="sxs-lookup"><span data-stu-id="e387c-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="e387c-281">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-281">String</span></span>      | <span data-ttu-id="e387c-282">Koden for det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-283">Rod\\Spørgeskema\\Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e387c-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="e387c-284">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-284">String</span></span>      | <span data-ttu-id="e387c-285">Beskrivelsen for det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-286">Rod\\Spørgeskema\\Spørgeskematype</span><span class="sxs-lookup"><span data-stu-id="e387c-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="e387c-287">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-287">String</span></span>      | <span data-ttu-id="e387c-288">Typen af det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-289">Rod\\Spørgeskema\\Spørgsmålsrækkefølge</span><span class="sxs-lookup"><span data-stu-id="e387c-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="e387c-290">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-290">String</span></span>      | <span data-ttu-id="e387c-291">Den numeriske rækkefølge for det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-292">Rod\\Spørgeskema\\Resultatgruppe</span><span class="sxs-lookup"><span data-stu-id="e387c-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="e387c-293">Optag</span><span class="sxs-lookup"><span data-stu-id="e387c-293">Record</span></span>      | <span data-ttu-id="e387c-294">Resultatparametre for det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-295">Rod\\Spørgeskema\\Resultatgruppe\\Kode</span><span class="sxs-lookup"><span data-stu-id="e387c-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="e387c-296">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-296">String</span></span>      | <span data-ttu-id="e387c-297">Identifikationskoden for den aktuelle resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="e387c-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="e387c-298">Rod\\Spørgeskema\\Resultatgruppe\\Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e387c-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="e387c-299">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-299">String</span></span>      | <span data-ttu-id="e387c-300">Beskrivelsen for den aktuelle resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="e387c-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="e387c-301">Rod\\Spørgeskema\\Resultatgruppe\\MaksAntalPoint</span><span class="sxs-lookup"><span data-stu-id="e387c-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="e387c-302">Kommatal</span><span class="sxs-lookup"><span data-stu-id="e387c-302">Real</span></span>        | <span data-ttu-id="e387c-303">Det maksimale antal point, der kunne optjenes.</span><span class="sxs-lookup"><span data-stu-id="e387c-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="e387c-304">Rod\\Spørgeskema\\Spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="e387c-305">Liste over poster</span><span class="sxs-lookup"><span data-stu-id="e387c-305">Record list</span></span> | <span data-ttu-id="e387c-306">Listen over spørgsmål til det aktuelle spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="e387c-307">Rod\\Spørgeskema\\Spørgsmål\\SamlingsSekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="e387c-308">Heltal</span><span class="sxs-lookup"><span data-stu-id="e387c-308">Integer</span></span>     | <span data-ttu-id="e387c-309">Sekvensnummeret for den aktuelle svarsamling.</span><span class="sxs-lookup"><span data-stu-id="e387c-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="e387c-310">Rod\\Spørgeskema\\Spørgsmål\\Id</span><span class="sxs-lookup"><span data-stu-id="e387c-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="e387c-311">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-311">String</span></span>      | <span data-ttu-id="e387c-312">Identifikationskoden for det aktuelle spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e387c-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="e387c-313">Rod\\Spørgeskema\\Spørgsmål\\SkalFuldføres</span><span class="sxs-lookup"><span data-stu-id="e387c-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="e387c-314">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-314">String</span></span>      | <span data-ttu-id="e387c-315">Et flag, der angiver, om det aktuelle spørgsmål skal besvares.</span><span class="sxs-lookup"><span data-stu-id="e387c-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="e387c-316">Rod\\Spørgeskema\\Spørgsmål\\PrimærtSpørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="e387c-317">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-317">String</span></span>      | <span data-ttu-id="e387c-318">Et flag, der angiver, om det aktuelle spørgsmål er primært.</span><span class="sxs-lookup"><span data-stu-id="e387c-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="e387c-319">Rod\\Spørgeskema\\Spørgsmål\\Sekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="e387c-320">Heltal</span><span class="sxs-lookup"><span data-stu-id="e387c-320">Integer</span></span>     | <span data-ttu-id="e387c-321">Sekvensnummeret for det aktuelle spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e387c-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="e387c-322">Rod\\Spørgeskema\\Spørgsmål\\Tekst</span><span class="sxs-lookup"><span data-stu-id="e387c-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="e387c-323">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-323">String</span></span>      | <span data-ttu-id="e387c-324">Teksten i det aktuelle spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e387c-324">The text of the current question.</span></span> |
    | <span data-ttu-id="e387c-325">Rod\\Spørgeskema\\Spørgsmål\\Svar</span><span class="sxs-lookup"><span data-stu-id="e387c-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="e387c-326">Liste over poster</span><span class="sxs-lookup"><span data-stu-id="e387c-326">Record list</span></span> | <span data-ttu-id="e387c-327">Listen over svar for det aktuelle spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e387c-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="e387c-328">Rod\\Spørgeskema\\Spørgsmål\\Svar\\KorrektSvar</span><span class="sxs-lookup"><span data-stu-id="e387c-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="e387c-329">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-329">String</span></span>      | <span data-ttu-id="e387c-330">Et flag, der angiver, om det aktuelle svar er korrekt.</span><span class="sxs-lookup"><span data-stu-id="e387c-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="e387c-331">Rod\\Spørgeskema\\Spørgsmål\\Svar\\Point</span><span class="sxs-lookup"><span data-stu-id="e387c-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="e387c-332">Kommatal</span><span class="sxs-lookup"><span data-stu-id="e387c-332">Real</span></span>        | <span data-ttu-id="e387c-333">De point, der optjenes, når det aktuelle svar er valgt.</span><span class="sxs-lookup"><span data-stu-id="e387c-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="e387c-334">Rod\\Spørgeskema\\Spørgsmål\\Svar\\Sekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="e387c-335">Heltal</span><span class="sxs-lookup"><span data-stu-id="e387c-335">Integer</span></span>     | <span data-ttu-id="e387c-336">Sekvensnummeret for det aktuelle svar.</span><span class="sxs-lookup"><span data-stu-id="e387c-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="e387c-337">Rod\\Spørgeskema\\Spørgsmål\\Svar\\Tekst</span><span class="sxs-lookup"><span data-stu-id="e387c-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="e387c-338">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-338">String</span></span>      | <span data-ttu-id="e387c-339">Teksten i det aktuelle svar.</span><span class="sxs-lookup"><span data-stu-id="e387c-339">The text of the current answer.</span></span> |

    <span data-ttu-id="e387c-340">I følgende illustration vises den fuldførte redigerbare datamodel på siden **Datamodeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Konfigureret datamodel i ER-datamodeldesigneren](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="e387c-342">Gem ændringerne.</span><span class="sxs-lookup"><span data-stu-id="e387c-342">Save your changes.</span></span>
8. <span data-ttu-id="e387c-343">Luk siden **Datamodeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="e387c-344">Fuldføre designet af datamodellen</span><span class="sxs-lookup"><span data-stu-id="e387c-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="e387c-345">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-346">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="e387c-347">I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e387c-348">Vælg **Skift status** \> **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e387c-349">Status for version 1 af denne konfiguration ændres fra **Kladde** til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="e387c-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e387c-350">Version 1 kan ikke længere ændres.</span><span class="sxs-lookup"><span data-stu-id="e387c-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="e387c-351">Denne version indeholder den konfigurerede datamodel og kan bruges som grundlag for andre ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e387c-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e387c-352">Version 2 af denne konfiguration er oprettet og har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e387c-353">Du kan redigere denne version for at justere datamodellen **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Versioner af den redigerbare ER-konfiguration på siden Konfigurationer](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="e387c-355">Yderligere oplysninger om versionering for ER-konfigurationer finder du i [Oversigt over elektronisk rapportering (ER)](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="e387c-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="e387c-356">Den konfigurerede datamodel er din abstrakte repræsentation af forretningsdomæne **Spørgeskema** og indeholder ingen relationer til artefakter, der er specifikke for Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e387c-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="e387c-357">Designe en modeltilknytning for den konfigurerede datamodel</span><span class="sxs-lookup"><span data-stu-id="e387c-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="e387c-358">Som bruger i rollen Udvikler afelektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for [modeltilknytning](general-electronic-reporting.md#data-model-and-model-mapping-components) til datamodellen **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="e387c-359">Da denne komponent implementerer den konfigurerede datamodel for Finance, er den specifik for Finance.</span><span class="sxs-lookup"><span data-stu-id="e387c-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="e387c-360">Du skal konfigurere komponenten for modeltilknytning for at angive de applikationsobjekter, der skal bruges til at udfylde den konfigurerede datamodel med applikationsdata under kørsel.</span><span class="sxs-lookup"><span data-stu-id="e387c-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="e387c-361">For at fuldføre denne opgave skal du være opmærksom på implementeringsoplysningerne om datastrukturen i forretningsdomænet **Spørgeskema** i Finance.</span><span class="sxs-lookup"><span data-stu-id="e387c-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="e387c-362">Når du udfører fremgangsmåden i det efterfølgende afsnit [Importere en ny konfiguration af modeltilknytning](#ImportModelMapping), kan du importere den krævede konfiguration af modeltilknytning fra den angivne XML-fil.</span><span class="sxs-lookup"><span data-stu-id="e387c-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="e387c-363">Du kan også udføre fremgangsmåden i afsnittet [Oprette en ny konfiguration af modeltilknytning](#CreateModelMapping) for at designe denne modeltilknytning fra bunden.</span><span class="sxs-lookup"><span data-stu-id="e387c-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="e387c-364">Importere en ny konfiguration af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="e387c-365">Hent filen [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="e387c-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e387c-366">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e387c-367">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="e387c-368">Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e387c-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="e387c-369">Vælg **Gennemse**, og find og vælg derefter filen **Questionnaires mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="e387c-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="e387c-370">Vælg **OK** for at importere konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e387c-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="e387c-371">Hvis du vil fortsætte, skal du springe over den næste procedure [Oprette en ny konfiguration af modeltilknytning](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="e387c-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="e387c-372">Oprette en ny konfiguration af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="e387c-373">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-374">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="e387c-375">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e387c-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="e387c-376">Følg disse trin i rulledialogboksen:</span><span class="sxs-lookup"><span data-stu-id="e387c-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-377">Vælg **Modeltilknytning baseret på datamodellen Spørgeskemaer** i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e387c-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="e387c-378">Skriv **Tilknytning af spørgeskema** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="e387c-379">Vælg definitionen **Rod** i feltet **Definition af datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="e387c-380">Vælg **Opret konfiguration** for at oprette konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e387c-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="e387c-381">Designe en ny komponent til modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="e387c-382">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilknytning af spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="e387c-383">Vælg **Designer** for at åbne listen over tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="e387c-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="e387c-384">Vælg tilknytningen **Tilknytning af spørgeskemaer**, der automatisk er tilføjet for definitionen **Rod**</span><span class="sxs-lookup"><span data-stu-id="e387c-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="e387c-385">Vælg **Designer** for at konfigurere den valgte tilknytning.</span><span class="sxs-lookup"><span data-stu-id="e387c-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="e387c-386">Der tilføjes automatisk en ny tilknytning for definitionen **Rod**.</span><span class="sxs-lookup"><span data-stu-id="e387c-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="e387c-387">Denne tilknytning har retningen **Til model**.</span><span class="sxs-lookup"><span data-stu-id="e387c-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="e387c-388">Denne tilknytning kan derfor bruges til at udfylde en datamodel med de nødvendige data.</span><span class="sxs-lookup"><span data-stu-id="e387c-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="e387c-389">Tilføje datakilder for at få adgang til programtabeller</span><span class="sxs-lookup"><span data-stu-id="e387c-389">Add data sources to access application tables</span></span>

<span data-ttu-id="e387c-390">Du skal konfigurere datakilder for at få adgang til de programtabeller, der indeholder spørgeskemaoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e387c-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="e387c-391">Vælg **Dynamics 365 for Operations\\Tabelposter** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="e387c-392">Tilføj en ny datakilde, der skal bruges til at få adgang til tabellen KMCollection, hvor hver post repræsenterer et enkelt spørgeskema:</span><span class="sxs-lookup"><span data-stu-id="e387c-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="e387c-393">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-394">Åbn **Spørgeskema** i feltet **Navn** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e387c-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="e387c-395">Indtast **KMCollection** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="e387c-396">Angiv indstillingen **Spørg efter forespørgsel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e387c-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="e387c-397">Du kan derefter angive indstillinger for [filtrering](../../fin-ops/get-started/advanced-filtering-query-options.md) for tabellen i systemets dialogboks under kørsel.</span><span class="sxs-lookup"><span data-stu-id="e387c-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="e387c-398">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="e387c-399">Vælg **Dynamics 365 for Operations\\Tabelposter** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="e387c-400">Tilføj en ny datakilde, der skal bruges til at få adgang til tabellen KMQuestion, hvor hver post repræsenterer et enkelt spørgsmål i et spørgeskema:</span><span class="sxs-lookup"><span data-stu-id="e387c-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="e387c-401">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-402">I dialogboksen skal du angive **Spørgsmål** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="e387c-403">Indtast **KMQuestion** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="e387c-404">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="e387c-405">Vælg **Dynamics 365 for Operations\\Tabelposter** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="e387c-406">Tilføj en ny datakilde, der skal bruges til at få adgang til tabellen KMAnswer, hvor hver post repræsenterer et enkelt svar på et spørgsmål i et spørgeskema:</span><span class="sxs-lookup"><span data-stu-id="e387c-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="e387c-407">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-408">I feltet **Navn** skal du skrive **Svar**.</span><span class="sxs-lookup"><span data-stu-id="e387c-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="e387c-409">Indtast **KMAnswer** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="e387c-410">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="e387c-411">Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="e387c-412">Tilføj et nyt beregnet felt, der skal bruges til at få adgang til en post i tabellen KMQuestionResultGroup fra alle poster i den overordnede KMCollection-tabel:</span><span class="sxs-lookup"><span data-stu-id="e387c-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="e387c-413">Vælg **Spørgeskema** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="e387c-414">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="e387c-414">Select **Add**.</span></span>
    3. <span data-ttu-id="e387c-415">I dialogboksen skal du angive **\$Resultatgruppe** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="e387c-416">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="e387c-417">I [ER-formeleditoren](general-electronic-reporting-formula-designer.md) i feltet **Formel** skal du skrive **FIRSTORNULL (\@.'\<Relations'.KMQuestionResultGroup)** for at bruge [stien](er-formula-language.md#paths) til en-til-mange-relationen mellem KMCollection- og KMQuestionResultGroup-tabellerne.</span><span class="sxs-lookup"><span data-stu-id="e387c-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="e387c-418">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="e387c-419">Vælg **OK** for at tilføje det nye beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="e387c-420">Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="e387c-421">Tilføj et nyt beregnet felt, der skal bruges til at få adgang til spørgsmålsposter i tabellen KMQuestion fra alle poster i den overordnede KMCollectionQuestion-tabel:</span><span class="sxs-lookup"><span data-stu-id="e387c-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="e387c-422">Vælg **Spørgeskema** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="e387c-423">Udvid noden **\<Relationer**, der indeholder én til mange-relationer i tabellen KMCollection.</span><span class="sxs-lookup"><span data-stu-id="e387c-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="e387c-424">Vælg den relaterede tabel **KMCollectionQuestion**, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="e387c-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="e387c-425">I dialogboksen skal du angive **\$Spørgsmål** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="e387c-426">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="e387c-427">I formeleditoren i feltet **Formel** skal du indtaste **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** for gå tilbage til den relevante spørgsmålspost fra tabellen KMQuestion.</span><span class="sxs-lookup"><span data-stu-id="e387c-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="e387c-428">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="e387c-429">Vælg **OK** for at tilføje det nye beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="e387c-430">Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="e387c-431">Tilføj et nyt beregnet felt, der skal bruges til at få adgang til svarposter i tabellen KMAnswer fra alle poster i den overordnede KMQuestion-tabel:</span><span class="sxs-lookup"><span data-stu-id="e387c-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="e387c-432">I ruden **Datakilder** skal du vælge **Spørgeskema.\<Relationer.KMCollectionQuestion.\$Spørgsmål** og derefter vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="e387c-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="e387c-433">I dialogboksen skal du angive **\$Svar** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="e387c-434">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="e387c-435">I formeleditoren i feltet **Formel** skal du angive **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** for gå tilbage til den relevante spørgsmålspost fra tabellen KMAnswer.</span><span class="sxs-lookup"><span data-stu-id="e387c-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="e387c-436">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="e387c-437">Vælg **OK** for at tilføje det nye beregnede felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="e387c-438">Vælg **Dynamics 365 for Operations\\Tabel** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="e387c-439">Tilføj en ny datakilde, der skal bruges til at få adgang til metoder i tabellen CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="e387c-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="e387c-440">Bemærk, at metoden **find()** i denne tabel returnerer en post, der repræsenterer et firma for den aktuelle Finance-forekomst, som denne tilknytning kaldes i forbindelse med.</span><span class="sxs-lookup"><span data-stu-id="e387c-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="e387c-441">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-442">I dialogboksen skal du angive **CompanyInfo** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="e387c-443">Indtast **CompanyInfo** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="e387c-444">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="e387c-445">Tilføje datakilder for at få adgang til programoptællinger</span><span class="sxs-lookup"><span data-stu-id="e387c-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="e387c-446">Du skal konfigurere datakilder for at få adgang til programoptællinger og sammenligne deres værdier med feltværdierne af typen **Optælling** i programtabellerne.</span><span class="sxs-lookup"><span data-stu-id="e387c-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="e387c-447">Du skal bruge resultatet af sammenligningen til at udfylde de relevante felter i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="e387c-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="e387c-448">Vælg **Dynamics 365 for Operations\\Optælling** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="e387c-449">Tilføj en ny datakilde, der skal bruges til at få adgang til værdier i optællingen **EnumAppNoYes**.</span><span class="sxs-lookup"><span data-stu-id="e387c-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="e387c-450">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-451">I dialogboksen skal du angive **EnumAppNoYes** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="e387c-452">Angiv **NoYes** i feltet **Optælling**.</span><span class="sxs-lookup"><span data-stu-id="e387c-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="e387c-453">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="e387c-454">Vælg **Dynamics 365 for Operations\\Optælling** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="e387c-455">Tilføj en ny datakilde, der skal bruges til at få adgang til værdierne i optællingen **KMCollectionQuestionMode**.</span><span class="sxs-lookup"><span data-stu-id="e387c-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="e387c-456">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-457">Gå til dialogboksen, og angiv **EnumAppQuestionOrder** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="e387c-458">Angiv **KMCollectionQuestionMode** i feltet **Optælling**.</span><span class="sxs-lookup"><span data-stu-id="e387c-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="e387c-459">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="e387c-460">Tilføje ER-etiketter for at generere en rapport på et angivet sprog</span><span class="sxs-lookup"><span data-stu-id="e387c-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="e387c-461">Du kan tilføje ER-etiketter for at konfigurere nogle af dine datakilder til at returnere værdier, der afhænger af det sprog, der er defineret i sammenhæng med modeltilknytningens kald.</span><span class="sxs-lookup"><span data-stu-id="e387c-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="e387c-462">På siden **Modeltilknytningsdesigner** skal du i ruden **Datakilder** vælge **Svar** og derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e387c-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="e387c-463">Aktivér feltet **Etiket**.</span><span class="sxs-lookup"><span data-stu-id="e387c-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="e387c-464">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="e387c-464">Select **Translate**.</span></span>
4. <span data-ttu-id="e387c-465">Følg disse trin i dialogboksen **Tekstoversættelse**:</span><span class="sxs-lookup"><span data-stu-id="e387c-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-466">Angiv **PositiveAnswer** i feltet **Etiket-id**.</span><span class="sxs-lookup"><span data-stu-id="e387c-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="e387c-467">I feltet **Tekst på standardsprog** skal du indtaste **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e387c-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="e387c-468">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="e387c-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="e387c-469">Angiv **NegativtSvar** i feltet **Etiket-id**.</span><span class="sxs-lookup"><span data-stu-id="e387c-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="e387c-470">I feltet **Tekst på standardsprog** skal du indtaste **Nej**.</span><span class="sxs-lookup"><span data-stu-id="e387c-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="e387c-471">Vælg **Oversæt**.</span><span class="sxs-lookup"><span data-stu-id="e387c-471">Select **Translate**.</span></span>

5. <span data-ttu-id="e387c-472">Luk dialogboksen **Tekstoversættelse**.</span><span class="sxs-lookup"><span data-stu-id="e387c-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="e387c-473">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="e387c-473">Select **Cancel**.</span></span>

![Tilføje ER-etiketter til den redigerbare modeltilknytning](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="e387c-475">Du har kun indtastet ER-etiketter for standardsproget.</span><span class="sxs-lookup"><span data-stu-id="e387c-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="e387c-476">Oplysninger om, hvordan ER-etiketter kan oversættes til andre sprog, finder du i afsnittet [Designe flersprogede rapporter](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="e387c-477">Tilføje en datakilde for at transformere resultaterne af sammenligning af optællingsværdier med en tekstværdi</span><span class="sxs-lookup"><span data-stu-id="e387c-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="e387c-478">Da du skal transformere resultaterne af sammenligningen mellem optællingsværdier og tekstværdier flere gange for at finde differencekilder, er det en god ide at konfigurere denne logik som en enkelt datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="e387c-479">Hvis du vil bruge denne datakilde, skal du dog konfigurere den som parametrized-datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="e387c-480">Du kan finde flere oplysninger i [Understøtte parameteriserede opkald om ER-datakilder af typen Beregnet felt](er-calculated-field-type.md)</span><span class="sxs-lookup"><span data-stu-id="e387c-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="e387c-481">Vælg **Generelt\\Tom container** i ruden **Datakildetyper** på siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="e387c-482">Tilføj en ny containerdatakilde:</span><span class="sxs-lookup"><span data-stu-id="e387c-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="e387c-483">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="e387c-484">I dialogboksen skal du angive **Hjælpefunktion** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="e387c-485">Vælg **OK** for at tilføje den nye containerdatakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="e387c-486">Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="e387c-487">Tilføj en ny datakilde:</span><span class="sxs-lookup"><span data-stu-id="e387c-487">Add a new data source:</span></span>

    1. <span data-ttu-id="e387c-488">Vælg **Hjælpefunktion** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="e387c-489">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="e387c-489">Select **Add**.</span></span>
    3. <span data-ttu-id="e387c-490">Gå til dialogboksen, og angiv **NoYesEnumToString** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="e387c-491">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="e387c-492">Vælg **Parametre** i formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="e387c-493">Benyt følgende fremgangsmåde for at angive parametre for det konfigurerede udtryk:</span><span class="sxs-lookup"><span data-stu-id="e387c-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="e387c-494">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e387c-494">Select **New**.</span></span>
        2. <span data-ttu-id="e387c-495">I dialogboksen skal du angive **Argument** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="e387c-496">Vælg datatypen **Boolesk** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="e387c-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="e387c-497">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-497">Select **OK**.</span></span>

    7. <span data-ttu-id="e387c-498">I feltet **Formel** skal du angive **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** for at returnere teksten for det relevante ER-navn, afhængigt af sproget i udførelseskonteksten og værdien af den angivne parameter.</span><span class="sxs-lookup"><span data-stu-id="e387c-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="e387c-499">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="e387c-500">Vælg **OK** for at tilføje den nye datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-500">Select **OK** to add the new data source.</span></span>

![Konfigureret modeltilknytning i ER-modeltilknytningsdesigneren](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="e387c-502">Binde datakilder til datamodelfelter</span><span class="sxs-lookup"><span data-stu-id="e387c-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="e387c-503">Du skal binde de konfigurerede datakilder til felterne i datamodellen for at angive, hvordan datamodellen skal udfyldes med programdata under kørsel.</span><span class="sxs-lookup"><span data-stu-id="e387c-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="e387c-504">Vælg **Firmanavn** på siden **Modeltilknytningsdesigner** i ruden **Datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="e387c-505">Udvid **Firmainfo** i ruden **Datakilder**, og benyt derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="e387c-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="e387c-506">Udvid noden **Firmainfo.find()**, der repræsenterer metoden **find()** i tabellen Firmainfo.</span><span class="sxs-lookup"><span data-stu-id="e387c-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="e387c-507">Vælg **Firmainfo.find().Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="e387c-508">Vælg **Bind** for at angive navnet på den virksomhed, som den konfigurerede modeltilknytning kaldes i forbindelse med kørsel.</span><span class="sxs-lookup"><span data-stu-id="e387c-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="e387c-509">Vælg **Spørgeskema** i ruden **Datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="e387c-510">I ruden **Datakilder** skal du vælge **Spørgeskema** og derefter vælge **Bind** for at udfylde spørgeskemaposterne.</span><span class="sxs-lookup"><span data-stu-id="e387c-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="e387c-511">Udvid **Spørgeskema** i ruden **Datamodel**, og benyt derefter følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="e387c-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="e387c-512">Vælg **Aktiv** i ruden **Datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="e387c-513">Vælg **Rediger** i ruden **Datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="e387c-514">Angiv i feltet **Formel** **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** for at udfylde det tekstafhængige og sprogafhængige resultat af sammenligningen mellem optællingsværdierne.</span><span class="sxs-lookup"><span data-stu-id="e387c-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="e387c-515">Fortsæt med at binde datakilder til datamodelfelter på samme måde, indtil du opnår følgende resultat.</span><span class="sxs-lookup"><span data-stu-id="e387c-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="e387c-516">Feltsti</span><span class="sxs-lookup"><span data-stu-id="e387c-516">Field path</span></span>                                              | <span data-ttu-id="e387c-517">Datatype</span><span class="sxs-lookup"><span data-stu-id="e387c-517">Data type</span></span>   | <span data-ttu-id="e387c-518">Handling</span><span class="sxs-lookup"><span data-stu-id="e387c-518">Action</span></span> | <span data-ttu-id="e387c-519">Bindingsudtryk</span><span class="sxs-lookup"><span data-stu-id="e387c-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="e387c-520">Firmanavn</span><span class="sxs-lookup"><span data-stu-id="e387c-520">CompanyName</span></span>                                             | <span data-ttu-id="e387c-521">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-521">String</span></span>      | <span data-ttu-id="e387c-522">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-522">Bind</span></span>   | <span data-ttu-id="e387c-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="e387c-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="e387c-524">Spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e387c-524">Questionnaire</span></span>                                           | <span data-ttu-id="e387c-525">Liste over poster</span><span class="sxs-lookup"><span data-stu-id="e387c-525">Record list</span></span> | <span data-ttu-id="e387c-526">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-526">Bind</span></span>   | <span data-ttu-id="e387c-527">Spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e387c-527">Questionnaire</span></span> |
    | <span data-ttu-id="e387c-528">Spørgeskema\\Aktiv</span><span class="sxs-lookup"><span data-stu-id="e387c-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="e387c-529">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-529">String</span></span>      | <span data-ttu-id="e387c-530">Edit</span><span class="sxs-lookup"><span data-stu-id="e387c-530">Edit</span></span>   | <span data-ttu-id="e387c-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="e387c-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="e387c-532">Spørgeskema\\Kode</span><span class="sxs-lookup"><span data-stu-id="e387c-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="e387c-533">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-533">String</span></span>      | <span data-ttu-id="e387c-534">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-534">Bind</span></span>   | <span data-ttu-id="e387c-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="e387c-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="e387c-536">Spørgeskema\\Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e387c-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="e387c-537">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-537">String</span></span>      | <span data-ttu-id="e387c-538">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-538">Bind</span></span>   | <span data-ttu-id="e387c-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="e387c-539">\@.Description</span></span> |
    | <span data-ttu-id="e387c-540">Spørgeskema\\Spørgeskematype</span><span class="sxs-lookup"><span data-stu-id="e387c-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="e387c-541">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-541">String</span></span>      | <span data-ttu-id="e387c-542">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-542">Bind</span></span>   | <span data-ttu-id="e387c-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="e387c-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="e387c-544">Spørgeskema\\Spørgsmålsrækkefølge</span><span class="sxs-lookup"><span data-stu-id="e387c-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="e387c-545">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-545">String</span></span>      | <span data-ttu-id="e387c-546">Edit</span><span class="sxs-lookup"><span data-stu-id="e387c-546">Edit</span></span>   | <span data-ttu-id="e387c-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="e387c-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="e387c-548">EnumAppQuestionOrder.Conditional, "Betinget",</span><span class="sxs-lookup"><span data-stu-id="e387c-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="e387c-549">EnumAppQuestionOrder.Random, "Tilfældig (procent i spørgeskema)",</span><span class="sxs-lookup"><span data-stu-id="e387c-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="e387c-550">EnumAppQuestionOrder.RandomGroup, "Tilfældig (procent i resultatgrupper)",</span><span class="sxs-lookup"><span data-stu-id="e387c-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="e387c-551">EnumAppQuestionOrder.Sequence, "Sekventiel",</span><span class="sxs-lookup"><span data-stu-id="e387c-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="e387c-552">"")</span><span class="sxs-lookup"><span data-stu-id="e387c-552">"")</span></span> |
    | <span data-ttu-id="e387c-553">Spørgeskema\\Resultatgruppe</span><span class="sxs-lookup"><span data-stu-id="e387c-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="e387c-554">Optag</span><span class="sxs-lookup"><span data-stu-id="e387c-554">Record</span></span>      |        | |
    | <span data-ttu-id="e387c-555">Spørgeskema\\Resultatgruppe\\Kode</span><span class="sxs-lookup"><span data-stu-id="e387c-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="e387c-556">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-556">String</span></span>      | <span data-ttu-id="e387c-557">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-557">Bind</span></span>   | <span data-ttu-id="e387c-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="e387c-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="e387c-559">Spørgeskema\\Resultatgruppe\\Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e387c-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="e387c-560">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-560">String</span></span>      | <span data-ttu-id="e387c-561">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-561">Bind</span></span>   | <span data-ttu-id="e387c-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="e387c-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="e387c-563">Spørgeskema\\Resultatgruppe\\MaksAntalPoint</span><span class="sxs-lookup"><span data-stu-id="e387c-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="e387c-564">Kommatal</span><span class="sxs-lookup"><span data-stu-id="e387c-564">Real</span></span>        | <span data-ttu-id="e387c-565">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-565">Bind</span></span>   | <span data-ttu-id="e387c-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="e387c-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="e387c-567">Spørgeskema\\Spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="e387c-568">Liste over poster</span><span class="sxs-lookup"><span data-stu-id="e387c-568">Record list</span></span> | <span data-ttu-id="e387c-569">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-569">Bind</span></span>   | <span data-ttu-id="e387c-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="e387c-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="e387c-571">Spørgeskema\\Spørgsmål\\SamlingsSekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="e387c-572">Heltal</span><span class="sxs-lookup"><span data-stu-id="e387c-572">Integer</span></span>     | <span data-ttu-id="e387c-573">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-573">Bind</span></span>   | <span data-ttu-id="e387c-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e387c-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="e387c-575">Spørgeskema\\Spørgsmål\\Id</span><span class="sxs-lookup"><span data-stu-id="e387c-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="e387c-576">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-576">String</span></span>      | <span data-ttu-id="e387c-577">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-577">Bind</span></span>   | <span data-ttu-id="e387c-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="e387c-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="e387c-579">Spørgeskema\\Spørgsmål\\SkalFuldføres</span><span class="sxs-lookup"><span data-stu-id="e387c-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="e387c-580">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-580">String</span></span>      | <span data-ttu-id="e387c-581">Edit</span><span class="sxs-lookup"><span data-stu-id="e387c-581">Edit</span></span>   | <span data-ttu-id="e387c-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="e387c-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="e387c-583">Spørgeskema\\Spørgsmål\\PrimærtSpørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="e387c-584">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-584">String</span></span>      | <span data-ttu-id="e387c-585">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-585">Bind</span></span>   | <span data-ttu-id="e387c-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="e387c-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="e387c-587">Spørgeskema\\Spørgsmål\\Sekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="e387c-588">Heltal</span><span class="sxs-lookup"><span data-stu-id="e387c-588">Integer</span></span>     | <span data-ttu-id="e387c-589">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-589">Bind</span></span>   | <span data-ttu-id="e387c-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e387c-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="e387c-591">Spørgeskema\\Spørgsmål\\Tekst</span><span class="sxs-lookup"><span data-stu-id="e387c-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="e387c-592">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-592">String</span></span>      | <span data-ttu-id="e387c-593">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-593">Bind</span></span>   | <span data-ttu-id="e387c-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="e387c-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="e387c-595">Spørgeskema\\Spørgsmål\\Svar</span><span class="sxs-lookup"><span data-stu-id="e387c-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="e387c-596">Liste over poster</span><span class="sxs-lookup"><span data-stu-id="e387c-596">Record list</span></span> | <span data-ttu-id="e387c-597">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-597">Bind</span></span>   | <span data-ttu-id="e387c-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="e387c-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="e387c-599">Spørgeskema\\Spørgsmål\\Svar\\KorrektSvar</span><span class="sxs-lookup"><span data-stu-id="e387c-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="e387c-600">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-600">String</span></span>      | <span data-ttu-id="e387c-601">Edit</span><span class="sxs-lookup"><span data-stu-id="e387c-601">Edit</span></span>   | <span data-ttu-id="e387c-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="e387c-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="e387c-603">Spørgeskema\\Spørgsmål\\Svar\\Point</span><span class="sxs-lookup"><span data-stu-id="e387c-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="e387c-604">Kommatal</span><span class="sxs-lookup"><span data-stu-id="e387c-604">Real</span></span>        | <span data-ttu-id="e387c-605">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-605">Bind</span></span>   | <span data-ttu-id="e387c-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="e387c-606">\@.point</span></span> |
    | <span data-ttu-id="e387c-607">Spørgeskema\\Spørgsmål\\Svar\\Sekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="e387c-608">Heltal</span><span class="sxs-lookup"><span data-stu-id="e387c-608">Integer</span></span>     | <span data-ttu-id="e387c-609">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-609">Bind</span></span>   | <span data-ttu-id="e387c-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e387c-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="e387c-611">Spørgeskema\\Spørgsmål\\Svar\\Tekst</span><span class="sxs-lookup"><span data-stu-id="e387c-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="e387c-612">Streng</span><span class="sxs-lookup"><span data-stu-id="e387c-612">String</span></span>      | <span data-ttu-id="e387c-613">Bind</span><span class="sxs-lookup"><span data-stu-id="e387c-613">Bind</span></span>   | <span data-ttu-id="e387c-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="e387c-614">\@.text</span></span> |

    <span data-ttu-id="e387c-615">I følgende illustration vises den endelige tilstand for den konfigurerede modeltilknytning på siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Fuldt konfigureret modeltilknytning i ER-modeltilknytningsdesigneren](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="e387c-617">Gem ændringerne.</span><span class="sxs-lookup"><span data-stu-id="e387c-617">Save your changes.</span></span>
8. <span data-ttu-id="e387c-618">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="e387c-619">Fuldføre designet af modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="e387c-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="e387c-620">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-621">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Tilknytning af spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="e387c-622">I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e387c-623">Vælg **Skift status** \> **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e387c-624">Status for version 1.1 af denne konfiguration ændres fra **Kladde** til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="e387c-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e387c-625">Version 1.1 kan ikke længere ændres.</span><span class="sxs-lookup"><span data-stu-id="e387c-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="e387c-626">Denne version indeholder den konfigurerede modeltilknytning og kan bruges som grundlag for andre ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e387c-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e387c-627">Version 1.2 af denne konfiguration er oprettet og har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e387c-628">Du kan redigere denne version for at justere konfigurationen **Tilknytning af spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Versioner af den redigerbare ER-konfiguration på siden Konfigurationer](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="e387c-630">Den konfigurerede modeltilknytning er den Finance-specifikke implementering af den abstrakte datamodel, der repræsenterer forretningsdomænet **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="e387c-631">Designe en skabelon til en brugerdefineret rapport</span><span class="sxs-lookup"><span data-stu-id="e387c-631">Design a template for a custom report</span></span>

<span data-ttu-id="e387c-632">ER-strukturen bruger foruddefinerede skabeloner til at oprette rapporter i Microsoft Office-formater (Excel-projektmapper eller Word-dokumenter).</span><span class="sxs-lookup"><span data-stu-id="e387c-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="e387c-633">Mens den påkrævede rapport oprettes, udfyldes en skabelon med de krævede data i henhold til det konfigurerede dataflow.</span><span class="sxs-lookup"><span data-stu-id="e387c-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="e387c-634">Derfor skal du først designe en skabelon til den brugerdefinerede rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="e387c-635">Denne skabelon skal være designet som en Excel-projektmappe, og strukturen repræsenterer layoutet for en brugerdefineret rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="e387c-636">Du skal navngive alle Excel-elementer, som du vil udfylde med de krævede data.</span><span class="sxs-lookup"><span data-stu-id="e387c-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="e387c-637">Hent filen [Questionnaires report template.xslxl](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="e387c-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e387c-638">Åbn filen i Excel, og gennemse projektmappens struktur.</span><span class="sxs-lookup"><span data-stu-id="e387c-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="e387c-639">Som følgende illustration viser, er den hentede skabelon designet til at udskrive bestemte spørgeskemaer, der viser et spørgeskemas spørgsmål sammen med relevante svar.</span><span class="sxs-lookup"><span data-stu-id="e387c-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Excel-skabelon til udskrivning af angivne spørgeskemaer](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="e387c-641">Der er føjet Excel-navne til denne skabelon for udfylde spørgeskemaoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e387c-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="e387c-642">Du kan bruge Navnestyring til at gennemse Excel-navnene.</span><span class="sxs-lookup"><span data-stu-id="e387c-642">You can use Name Manager to review the Excel names.</span></span>

![Bruge Navnestyring til at gennemse Excel-navne i den viste Excel-skabelon](./media/er-quick-start1-template-names.png)

<span data-ttu-id="e387c-644">Rapportetiketter er tilføjet som fasttekst på engelsk.</span><span class="sxs-lookup"><span data-stu-id="e387c-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="e387c-645">Du kan erstatte rapportetiketterne med nye Excel-navne, der udfylder etiketterne med sprogafhængig tekst, ved at bruge [etiketter](#AddMmLabels) for ER-format, som du gjorde for sprogafhængige udtryk i den konfigurerede modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="e387c-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="e387c-646">I dette tilfælde skal der tilføjes-navne i det redigerbare ER-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="e387c-647">I følgende illustration vises det brugerdefinerede rapporthoved, der gør det muligt at foretage sideinddeling i Excel.</span><span class="sxs-lookup"><span data-stu-id="e387c-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Brugerdefineret rapporthoved i den tilgængelige Excel-skabelon](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="e387c-649">Design et format</span><span class="sxs-lookup"><span data-stu-id="e387c-649">Design a format</span></span>

<span data-ttu-id="e387c-650">Som bruger med rollen Funktionel konsulent i elektronisk rapportering skal du oprette en ny ER-konfiguration, der indeholder en komponent for [format](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="e387c-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="e387c-651">Du skal konfigurere formatkomponenten format for at angive, hvordan en rapportskabelon skal udfyldes med de nødvendige data under kørsel.</span><span class="sxs-lookup"><span data-stu-id="e387c-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="e387c-652">Når du udfører fremgangsmåden i afsnittet [Importere en designet formatkonfiguration](#FormatImport), kan du importere det ønskede format fra den angivne XML-fil.</span><span class="sxs-lookup"><span data-stu-id="e387c-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="e387c-653">Du kan også udføre fremgangsmåden i afsnittet [Oprette en ny formatkonfiguration](#FormatCreate) for at designe dette format fra bunden.</span><span class="sxs-lookup"><span data-stu-id="e387c-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="e387c-654">Importere en designet formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="e387c-655">Hent filen [Questionnairesformat.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448), og gem den på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="e387c-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="e387c-656">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="e387c-657">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="e387c-658">Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e387c-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="e387c-659">Vælg **Gennemse**, og find og vælg derefter filen **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="e387c-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="e387c-660">Vælg **OK** for at importere konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e387c-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="e387c-661">Hvis du vil fortsætte, skal du springe over den næste procedure [Oprette en ny formatkonfiguration](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="e387c-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="e387c-662">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="e387c-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="e387c-663">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-664">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="e387c-665">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e387c-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="e387c-666">Følg disse trin i rulledialogboksen:</span><span class="sxs-lookup"><span data-stu-id="e387c-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-667">Vælg **Format baseret på datamodellen Spørgeskemaer** i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e387c-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="e387c-668">Skriv **Spørgeskemarapport** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="e387c-669">Vælg **1** i feltet **Datamodelversion**.</span><span class="sxs-lookup"><span data-stu-id="e387c-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="e387c-670">Hvis du vælger en bestemt version af stamdatamodellen, vises strukturen i den tilsvarende version af datamodellen som strukturen i datakilden **Model** i det format, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="e387c-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="e387c-671">Du kan lade feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="e387c-671">You can leave this field blank.</span></span> <span data-ttu-id="e387c-672">Hvis det er tilfældet, vises strukturen i **Kladde**-versionen af datamodellen som strukturen i datakilden **Model** i det format, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="e387c-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="e387c-673">Du kan derefter justere modellen og straks se disse justeringer i dit format.</span><span class="sxs-lookup"><span data-stu-id="e387c-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="e387c-674">Denne metode kan forbedre effektiviteten af ER-løsningsdesign, når du konfigurerer datamodellen, modeltilknytningen og formatet samtidigt.</span><span class="sxs-lookup"><span data-stu-id="e387c-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="e387c-675">Hvis du vælger en bestemt version af stamdatamodellen, kan du skifte til at bruge **Kladde**-versionen senere, når du begynder at redigere et format.</span><span class="sxs-lookup"><span data-stu-id="e387c-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="e387c-676">Vælg definitionen **Rod** i feltet **Definition af datamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="e387c-677">Vælg **Opret konfiguration** for at oprette konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e387c-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="e387c-678">Importere en rapportskabelon</span><span class="sxs-lookup"><span data-stu-id="e387c-678">Import a report template</span></span>

1. <span data-ttu-id="e387c-679">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Spørgeskemarapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="e387c-680">Vælg **Designer** for at begynde at konfigurere et brugerdefineret format.</span><span class="sxs-lookup"><span data-stu-id="e387c-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="e387c-681">I oversigtspanelet på siden **Formatdesigner** skal du vælge **Importér** \> **Importér fra Excel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e387c-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="e387c-682">Følg disse trin i dialogboksen:</span><span class="sxs-lookup"><span data-stu-id="e387c-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-683">Vælg **Tilføj skabelon**.</span><span class="sxs-lookup"><span data-stu-id="e387c-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="e387c-684">Find og vælg den lokalt gemte filen **Questionnaires report template.xslx**, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="e387c-685">Vælg **OK** for at importere skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e387c-685">Select **OK** to import the template.</span></span>

    ![Import af en rapportskabelon](./media/er-quick-start1-template-import.png)

<span data-ttu-id="e387c-687">Formatelementet **Excel\\Fil** føjes automatisk til det redigerbare format som et rodelement.</span><span class="sxs-lookup"><span data-stu-id="e387c-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="e387c-688">Derudover tilføjes formatelementet **Excel\\Område** eller **Excel\\Celle** automatisk for hvert genkendeligt Excel-navn i den importerede skabelon.</span><span class="sxs-lookup"><span data-stu-id="e387c-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="e387c-689">Formatet **Excel\\Overskrift**, der indeholder det indlejrede element **Streng**, tilføjes automatisk for at afspejle overskriftsindstillingerne for den importerede skabelon.</span><span class="sxs-lookup"><span data-stu-id="e387c-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Formatstruktur, der omfatter automatisk tilføjede elementer i ER-operationsdesigneren](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="e387c-691">Konfigurere et format</span><span class="sxs-lookup"><span data-stu-id="e387c-691">Configure a format</span></span>

1. <span data-ttu-id="e387c-692">Vælg rodelementet **Excel** i formattræet på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="e387c-693">Angiv <a name="AddFormatRootElement"></a>**Rapport** i feltet **Navn** under fanen **Format** i højre side af siden.</span><span class="sxs-lookup"><span data-stu-id="e387c-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="e387c-694">I feltet **Foretrukket sprog** skal du vælge **Brugerindstilling** for at køre rapporten på brugerens foretrukne sprog.</span><span class="sxs-lookup"><span data-stu-id="e387c-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="e387c-695">I feltet **Foretrukket kultur** skal du vælge **Brugerindstilling** for at køre rapporten på brugerens foretrukne kultur.</span><span class="sxs-lookup"><span data-stu-id="e387c-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="e387c-696">Du kan finde oplysninger om, hvordan du angiver sprog- og kulturkontekster for en ER-proces, under [Designe flersprogede rapporter](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Konfigurere indstillinger for sprog og kultur for den designede rapport i ER-operationsdesigneren](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="e387c-698">Udvid rodnoden i formattræet, og vælg derefter **Resultatgruppe**.</span><span class="sxs-lookup"><span data-stu-id="e387c-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="e387c-699">Under fanen **Format** i feltet **Replikeringsretning** skal du vælge **Ingen replikering**, da du ikke forventer flere resultatgrupper for et enkelt spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![Definere replikeringsretningen for formatelementer af typen Område i ER-operationsdesigneren](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="e387c-701">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e387c-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="e387c-702">Definere databinding for en rapporttitel</span><span class="sxs-lookup"><span data-stu-id="e387c-702">Define the data binding for a report title</span></span>

<span data-ttu-id="e387c-703">Du skal angive en databinding for et formatelement, der bruges til at udfylde titlen på en genereret rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="e387c-704">Vælg elementet **Rapport\\Rapporttitel** på siden **Formatdesigner** under fanen **Tilknytning** til højre.</span><span class="sxs-lookup"><span data-stu-id="e387c-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="e387c-705">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="e387c-706">Vælg **Oversæt** i formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="e387c-707">Følg disse trin i dialogboksen **Tekstoversættelse**:</span><span class="sxs-lookup"><span data-stu-id="e387c-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="e387c-708">Angiv **Rapporttitel** i feltet **Etiket-id**.</span><span class="sxs-lookup"><span data-stu-id="e387c-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="e387c-709">I feltet **Tekst i standardsprog** skal du indtaste **Rapport for spørgeskemaer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="e387c-710">Vælg **Oversæt**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e387c-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="e387c-711">Vælg **Oversæt** for at lukke dialogboksen **Tekstoversættelse**.</span><span class="sxs-lookup"><span data-stu-id="e387c-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="e387c-712">Luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-712">Close the formula editor.</span></span>

    ![Konfiguration af bindingen for at udfylde titlen på en genereret rapport](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="e387c-714">Du kan bruge denne teknik til at gøre alle andre etiketter for den aktuelle skabelon sprogafhængige.</span><span class="sxs-lookup"><span data-stu-id="e387c-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="e387c-715">Oplysninger om, hvordan de tilføjede etiketter til en enkelt ER-konfiguration kan oversættes til alle understøttede sprog, finder du i [Designe flersprogede rapporter](er-design-multilingual-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="e387c-716">Gennemse modeldatakilden</span><span class="sxs-lookup"><span data-stu-id="e387c-716">Review model data source</span></span>

1. <span data-ttu-id="e387c-717">På siden **Formatdesigner** under fanen **Tilknytning** skal du vælge datakilden for <a name="ModelDSName"></a>**modellen**, der repræsenterer basisdatamodellen for dette ER-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="e387c-718">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e387c-718">Select **Edit**.</span></span>
3. <span data-ttu-id="e387c-719">Gennemse oplysningerne i dialogboksen **Egenskaber for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="e387c-720">Denne datakilde repræsenterer version 1 af datamodelkomponenten **Spørge skemaer**, der findes i ER-konfiguraitonen for **Spørgeskemamodel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Egenskaber for modeldatakilden i ER-operationsdesigneren](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="e387c-722">Binde formatelementer til datakildefelter</span><span class="sxs-lookup"><span data-stu-id="e387c-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="e387c-723">Hvis du vil angive, hvordan en skabelon skal udfyldes på kørselstidspunktet, skal du binde alle formatelementer, der er knyttet til et relevant Excel-navn, til et enkelt felt i dette formats datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="e387c-724">Vælg formatelementet **Rapport\\Firmanavn** i formattræet på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="e387c-725">Under fanen **Tilknytning** skal du vælge datakildefeltet **model.CompanyName** for typen **Streng**.</span><span class="sxs-lookup"><span data-stu-id="e387c-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="e387c-726">Vælg **Bind** for at angive et firmanavn i en skabelon.</span><span class="sxs-lookup"><span data-stu-id="e387c-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="e387c-727">Vælg elementet **Rapport\\Spørgeskema** i formattræet.</span><span class="sxs-lookup"><span data-stu-id="e387c-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="e387c-728">Under fanen **Tilknytning** skal du vælge datakildefeltet **model.Questionnaire** for typen **Postliste**.</span><span class="sxs-lookup"><span data-stu-id="e387c-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="e387c-729">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="e387c-729">Select **Bind**.</span></span>
7. <span data-ttu-id="e387c-730">Vælg **Vis detaljer** for at få vist flere oplysninger om formatelementer.</span><span class="sxs-lookup"><span data-stu-id="e387c-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="e387c-731">Formatelementet for området for **Spørgeskema** konfigureres som lodret replikeret.</span><span class="sxs-lookup"><span data-stu-id="e387c-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="e387c-732">Når den er bundet til en datakilde af typen **Postliste**, gentages det relevante område for **Spørgeskema** for Excel-skabelonen for hver post i den bundne datakilde.</span><span class="sxs-lookup"><span data-stu-id="e387c-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Binding af formatelementet for spørgeskemaområdet til de relevante postlistedatakilder i ER-operationsdesigneren](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="e387c-734">Da området **Spørgeskema** for Excel-skabelonen er defineret fra række 5 til 14, gentages disse rækker for hvert rapporteret spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e387c-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Rækker i Excel-skabelonen, der vil blive gentaget i en genereret rapport for hver post på postlistens datakilder](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="e387c-736">Konfigurer lignende bindinger for de resterende formatelementer som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e387c-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e387c-737">I denne tabel antager oplysningerne i kolonnen "Sti til datakilde", at ER-funktionen for den [relative sti](relative-path-data-bindings-er-models-format.md) er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="e387c-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="e387c-738">Formatere elementsti</span><span class="sxs-lookup"><span data-stu-id="e387c-738">Format element path</span></span>                                      | <span data-ttu-id="e387c-739">Datakildesti</span><span class="sxs-lookup"><span data-stu-id="e387c-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="e387c-740">Excel\\Rapporttitel</span><span class="sxs-lookup"><span data-stu-id="e387c-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="e387c-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="e387c-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="e387c-742">Excel\\Firmanavn</span><span class="sxs-lookup"><span data-stu-id="e387c-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="e387c-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="e387c-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="e387c-744">Excel\\Spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e387c-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="e387c-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="e387c-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="e387c-746">Excel\\Spørgeskema\\Aktiv</span><span class="sxs-lookup"><span data-stu-id="e387c-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="e387c-747">**\@.Active**, hvor **\@** er **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="e387c-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="e387c-748">Excel\\Spørgeskema\\Kode</span><span class="sxs-lookup"><span data-stu-id="e387c-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="e387c-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="e387c-749">**\@.Code**</span></span> |
    | <span data-ttu-id="e387c-750">Excel\\Spørgeskema\\Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e387c-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="e387c-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="e387c-751">**\@.Description**</span></span> |
    | <span data-ttu-id="e387c-752">Excel\\Spørgeskema\\Spørgeskematype</span><span class="sxs-lookup"><span data-stu-id="e387c-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="e387c-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="e387c-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="e387c-754">Excel\\Spørgeskema\\Spørgsmålsrækkefølge</span><span class="sxs-lookup"><span data-stu-id="e387c-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="e387c-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="e387c-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="e387c-756">Excel\\Spørgeskema\\Resultatgruppe\\Kode\_</span><span class="sxs-lookup"><span data-stu-id="e387c-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="e387c-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="e387c-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="e387c-758">Excel\\Spørgeskema\\Resultatgruppe\\Beskrivelse\_</span><span class="sxs-lookup"><span data-stu-id="e387c-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="e387c-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="e387c-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="e387c-760">Excel\\Spørgeskema\\Resultatgruppe\\MaksAntalPoint</span><span class="sxs-lookup"><span data-stu-id="e387c-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="e387c-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="e387c-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="e387c-762">Excel\\Spørgeskema\\Spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="e387c-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="e387c-763">**\@.Question**</span></span> |
    | <span data-ttu-id="e387c-764">Excel\\Spørgeskema\\Spørgsmål\\SamlingsSekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="e387c-765">**\@.CollectionSequenceNumber**, hvor **\@** er **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="e387c-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="e387c-766">Excel\\Spørgeskema\\Spørgsmål\\Id</span><span class="sxs-lookup"><span data-stu-id="e387c-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="e387c-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="e387c-767">**\@.Id**</span></span> |
    | <span data-ttu-id="e387c-768">Excel\\Spørgeskema\\Spørgsmål\\SkalFuldføres</span><span class="sxs-lookup"><span data-stu-id="e387c-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="e387c-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="e387c-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="e387c-770">Excel\\Spørgeskema\\Spørgsmål\\PrimærtSpørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="e387c-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="e387c-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="e387c-772">Excel\\Spørgeskema\\Spørgsmål\\Sekvensnummer</span><span class="sxs-lookup"><span data-stu-id="e387c-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="e387c-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e387c-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="e387c-774">Excel\\Spørgeskema\\Spørgsmål\\Tekst</span><span class="sxs-lookup"><span data-stu-id="e387c-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="e387c-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="e387c-775">**\@.Text**</span></span> |
    | <span data-ttu-id="e387c-776">Excel\\Spørgeskema\\Spørgsmål\\Svar</span><span class="sxs-lookup"><span data-stu-id="e387c-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="e387c-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="e387c-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="e387c-778">Excel\\Spørgeskema\\Spørgsmål\\Svar\\KorrektSvar</span><span class="sxs-lookup"><span data-stu-id="e387c-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="e387c-779">**\@.CorrectAnswer**, hvor **\@** er **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="e387c-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="e387c-780">Excel\\Spørgeskema\\Spørgsmål\\Svar\\Point</span><span class="sxs-lookup"><span data-stu-id="e387c-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="e387c-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="e387c-781">**\@.Points**</span></span> |
    | <span data-ttu-id="e387c-782">Excel\\Spørgeskema\\Spørgsmål\\Svar\\Tekst</span><span class="sxs-lookup"><span data-stu-id="e387c-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="e387c-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="e387c-783">**\@.Text**</span></span> |

9. <span data-ttu-id="e387c-784">Vælg **Gem**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="e387c-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="e387c-785">I følgende illustration vises den endelige tilstand for de konfigurerede databindinger på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Konfigurerede databindinger i ER-operationsdesigneren](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="e387c-787">Hele samlingen af angivne datakilder og bindinger repræsenterer en komponent til formattilknytning i det konfigurerede format.</span><span class="sxs-lookup"><span data-stu-id="e387c-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="e387c-788">Denne formattilknytning kaldes, når du kører det konfigurerede format for oprettelse af rapporter.</span><span class="sxs-lookup"><span data-stu-id="e387c-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="e387c-789">Køre et designet format fra ER</span><span class="sxs-lookup"><span data-stu-id="e387c-789">Run a designed format from ER</span></span>

<span data-ttu-id="e387c-790">Du kan nu køre et designet format til testformål fra siden **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="e387c-791">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-792">På siden **Konfiguration** i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e387c-793">Vælg **Designer** for den formatversion, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e387c-794">På siden **Formatdesigner** skal du vælge **Kør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="e387c-795">Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **ER-parametre**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e387c-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="e387c-796">Vælg **OK** for at bekræfte filtreringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="e387c-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="e387c-797">Vælg **OK** for at køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="e387c-798">Gennemse den oprettede rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-798">Review the generated report.</span></span>

<span data-ttu-id="e387c-799">Som [standard](electronic-reporting-destinations.md#default-behavior) leveres en oprettet rapport som en Excel-fil, som du kan hente.</span><span class="sxs-lookup"><span data-stu-id="e387c-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="e387c-800">I følgende illustrationer vises to sider med den oprettede rapport i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Eksempel på en oprettet rapport i Excel-format, side 1](./media/er-quick-start1-report1a.png)

![Eksempel på en oprettet rapport i Excel-format, side 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="e387c-803">Finjustere et designet format</span><span class="sxs-lookup"><span data-stu-id="e387c-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="e387c-804">Ændre et format for at ændre navnet på et oprettet dokument</span><span class="sxs-lookup"><span data-stu-id="e387c-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="e387c-805">Et oprettet dokument navngives som standard ved hjælp af aliasset for den aktuelle bruger.</span><span class="sxs-lookup"><span data-stu-id="e387c-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="e387c-806">Ved at ændre formatet kan du ændre denne funktionsmåde, så et oprettet dokument navngives på baggrund af din brugerdefinerede logik.</span><span class="sxs-lookup"><span data-stu-id="e387c-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="e387c-807">Navnet på et oprettet dokument kan f.eks. være baseret på den aktuelle sessionsdato og -klokkeslæt og på rapportens titel.</span><span class="sxs-lookup"><span data-stu-id="e387c-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="e387c-808">Vælg rodelementet **Rapport** på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="e387c-809">Vælg **Rediger filnavn** under fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="e387c-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="e387c-810">I feltet **Formel** skal du skrive **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span><span class="sxs-lookup"><span data-stu-id="e387c-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="e387c-811">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="e387c-812">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e387c-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="e387c-813">Redigere et format for at ændre rækkefølgen af spørgsmål</span><span class="sxs-lookup"><span data-stu-id="e387c-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="e387c-814">Spørgsmålene er ikke placeret i korrekt rækkefølge i en oprettet rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="e387c-815">Du kan ændre rækkefølgen ved at ændre formatet.</span><span class="sxs-lookup"><span data-stu-id="e387c-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="e387c-816">Vælg rodelementet **Rapport** på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="e387c-817">Under fanen **Tilknytning** i formattræet skal du udvide **Rapport\\Spørgeskema\\Spørgsmål**.</span><span class="sxs-lookup"><span data-stu-id="e387c-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Spørgsmålsformatelement for intervaltypen i ER-operationsdesigneren](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="e387c-819">Vælg **model.Questionnaire** under fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="e387c-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="e387c-820">Vælg **Tilføj** \> **Funktioner\\Beregnet felt** og angiv derefter **OrderedQuestions** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="e387c-821">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="e387c-822">I formeleditoren i feltet **Formel** skal du skrive **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** for at arrangere listen over spørgsmål i det aktuelle spørgeskema efter sekvensrækkefølgenummeret.</span><span class="sxs-lookup"><span data-stu-id="e387c-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="e387c-823">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="e387c-824">Vælg **OK** for at fuldføre indtastningen af et nyt beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="e387c-825">Vælg **model.Questionnaire.OrderedQuestions** under fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="e387c-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="e387c-826">Vælg **Excel\\Spørgeskema\\Spørgsmål** i formattræet.</span><span class="sxs-lookup"><span data-stu-id="e387c-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="e387c-827">Vælg **Bind**, og bekræft derefter, at den aktuelle sti for **model.Questionnaire.Questions** erstattes af den nye sti for **model.Questionnaire.OrderedQuestions** i alle bindinger af indlejrede elementer.</span><span class="sxs-lookup"><span data-stu-id="e387c-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="e387c-828">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e387c-828">Select **Save**.</span></span>

![Binding af formatelementet Spørgsmål til den konfigurerede datakilde for OrderedQuestions i ER-operationsdesigneren](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="e387c-830">Køre et ændret format fra ER</span><span class="sxs-lookup"><span data-stu-id="e387c-830">Run a modified format from ER</span></span>

<span data-ttu-id="e387c-831">Du kan nu køre et ændret format til testformål fra ER-strukturen.</span><span class="sxs-lookup"><span data-stu-id="e387c-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="e387c-832">På siden **Formatdesigner** skal du vælge **Kør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="e387c-833">Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **ER-parametre**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e387c-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="e387c-834">Vælg **OK** for at bekræfte filtreringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="e387c-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="e387c-835">Vælg **OK** for at køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="e387c-836">Gennemse den oprettede rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-836">Review the generated report.</span></span>

<span data-ttu-id="e387c-837">I følgende illustration vises en oprettet rapport i Excel-format, hvor spørgsmålene er placeret i korrekt rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e387c-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Oprettet rapport i Excel-format, der har placeret spørgsmålene i korrekt rækkefølge](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="e387c-839">Fuldføre formatdesignet</span><span class="sxs-lookup"><span data-stu-id="e387c-839">Complete the format design</span></span>

1. <span data-ttu-id="e387c-840">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-841">På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e387c-842">I oversigtspanelet **Versioner** skal du vælge den konfigurationsversion, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="e387c-843">Vælg **Skift status** \> **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e387c-844">Status for version 1.1 af denne konfiguration ændres fra **Kladde** til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="e387c-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e387c-845">Version 1.1 kan ikke længere ændres.</span><span class="sxs-lookup"><span data-stu-id="e387c-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="e387c-846">Denne version indeholder det konfigurerede format og kan bruges til at udskrive den brugerdefinerede rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="e387c-847">Version 1.2 af denne konfiguration er oprettet og har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e387c-848">Du kan redigere denne version for at justere formatet for rapporten for **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Versioner af den redigerbare ER-konfiguration på siden Konfigurationer](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="e387c-850">Det konfigurerede format er designet af rapporten for **Spørgeskema** og indeholder ingen relationer til de Finance-specifikke artefakter.</span><span class="sxs-lookup"><span data-stu-id="e387c-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="e387c-851">Udvikle programartefakter for at kalde den designede rapport</span><span class="sxs-lookup"><span data-stu-id="e387c-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="e387c-852">Som bruger i rollen Systemadministrator skal du udvikle ny logik, så det konfigurerede ER-format kan kaldes fra applikationens brugergrænseflade (UI) for at oprette den brugerdefinerede rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="e387c-853">I øjeblikket giver ER ikke mulighed for at konfigurere denne type logik.</span><span class="sxs-lookup"><span data-stu-id="e387c-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="e387c-854">Dette kræver derfor udviklingsarbejde.</span><span class="sxs-lookup"><span data-stu-id="e387c-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="e387c-855">Hvis du vil udvikle den nye logik, skal du installere en topologi, der understøtter fortløbende build.</span><span class="sxs-lookup"><span data-stu-id="e387c-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="e387c-856">Du kan finde flere oplysninger under [Installere topologier, der understøtter fortløbende build og automatisering af test](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="e387c-857">Du skal også have adgang til udviklingsmiljøet for denne topologi.</span><span class="sxs-lookup"><span data-stu-id="e387c-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="e387c-858">Du kan finde flere oplysninger om den tilgængelige API for ER under [API for ER-struktur](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="e387c-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="e387c-859">Ændre kildekode</span><span class="sxs-lookup"><span data-stu-id="e387c-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="e387c-860">Tilføje en datakontraktklasse</span><span class="sxs-lookup"><span data-stu-id="e387c-860">Add a data contract class</span></span>

<span data-ttu-id="e387c-861">Føj den nye klasse **QuestionnairesErReportContract** til dit Microsoft Visual Studio-projekt, og skriv kode, der angiver den datakontrakt, der skal bruges til at køre det konfigurerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="e387c-862">Tilføje en klasse for brugergrænsefladegenerator</span><span class="sxs-lookup"><span data-stu-id="e387c-862">Add a UI builder class</span></span>

<span data-ttu-id="e387c-863">Føj den nye klasse **QuestionnairesErReportUIBuilder** til dit Visual Studio-projekt, og skriv kode for at generere en dialogboks til kørsel, som skal bruges til at søge efter formattilknytnings-id'et for det ER-format, der skal køres.</span><span class="sxs-lookup"><span data-stu-id="e387c-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="e387c-864">Den leverede kode søger kun efter ER-formater, der indeholder en datakilde af typen **Datamodel**, som refererer til datamodellen for **[Spørgeskemaer](#DataModeName)** ved hjælp af definitionen af **[Rod](#RootDefinitionName)**.</span><span class="sxs-lookup"><span data-stu-id="e387c-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="e387c-865">Du kan også bruge ER-integrationspunkter til at filtrere ER-formater.</span><span class="sxs-lookup"><span data-stu-id="e387c-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="e387c-866">Du kan finde flere oplysninger under [API til at vise et opslag i formattilknytning](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span><span class="sxs-lookup"><span data-stu-id="e387c-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="e387c-867">Tilføje en klasse for dataprovider</span><span class="sxs-lookup"><span data-stu-id="e387c-867">Add a data provider class</span></span>

<span data-ttu-id="e387c-868">Føj den nye klasse **QuestionnairesErReportDP** til dit Microsoft Visual Studio-projekt, og skriv kode, der indsætter den dataprovider, der skal bruges til at køre det konfigurerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="e387c-869">Den leverede kode omfatter kun datakontrakten for denne dataprovider.</span><span class="sxs-lookup"><span data-stu-id="e387c-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="e387c-870">Tilføje en etiketfil</span><span class="sxs-lookup"><span data-stu-id="e387c-870">Add a labels file</span></span>

<span data-ttu-id="e387c-871">Føj den nye etiketfil **QuestionnairesErReportLabels\_en-US** til dit Visual Studio-projekt, og angiv følgende etiketter til nye ressourcer til brugergrænsefladen:</span><span class="sxs-lookup"><span data-stu-id="e387c-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="e387c-872">Etiketten **\@QuestionnairesReport** for et nyt menupunkt, der indeholder følgende tekst på amerikansk engelsk (en-US): **Rapport for spørgeskemaer (drevet af ER)**</span><span class="sxs-lookup"><span data-stu-id="e387c-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="e387c-873">Etiketten **\@QuestionnairesReportBatchJobDescription** for en titel på et batchjob, hvis et valgt ER-format er planlagt til udførelse som et batchjob</span><span class="sxs-lookup"><span data-stu-id="e387c-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="e387c-874">Tilføje en rapportserviceklasse</span><span class="sxs-lookup"><span data-stu-id="e387c-874">Add a report service class</span></span>

<span data-ttu-id="e387c-875">Føj den nye klasse **QuestionnairesErReportService** til dit Visual Studio-projekt, og skriv kode, der kalder et ER-format, identificerer det ud fra formattilknytnings-id'et og angiver en datakontrakt som parameter.</span><span class="sxs-lookup"><span data-stu-id="e387c-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="e387c-876">Når du skal bruge et ER-format, der kører programdata, skal du konfigurere en datakilde af typen **Datamodel** i formattilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e387c-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="e387c-877">Denne datakilde refererer til en bestemt del af den angivne datamodel ved hjælp af en enkelt roddefinition.</span><span class="sxs-lookup"><span data-stu-id="e387c-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="e387c-878">Når ER-formatet er kørt, kalder det denne datakilde for at få adgang til den tilsvarende ER-modeltilknytning, der er konfigureret for en bestemt model og roddefinition.</span><span class="sxs-lookup"><span data-stu-id="e387c-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="e387c-879">Alle de oplysninger, du kan forberede i kildekoden og -lageret som en del af datakontrakten, kan overføres til det aktuelle ER-format ved hjælp af en ER-modeltilknytning af denne type.</span><span class="sxs-lookup"><span data-stu-id="e387c-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="e387c-880">I ER-modeltilknytningen skal du konfigurere en datakilde af typen **Objekt**, der refererer til klassen **[QuestionnairesErReportContract](#DataContractClass)**.</span><span class="sxs-lookup"><span data-stu-id="e387c-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="e387c-881">Hvis du vil identificere en modeltilknytning, skal du angive en datakilde, der kalder denne modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="e387c-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="e387c-882">I den leverede kode specificerede denne datakilde med konstanten **ERModelDataSourceName**, der har værdien for **[model](#ModelDSName)**.</span><span class="sxs-lookup"><span data-stu-id="e387c-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="e387c-883">For at identificere, hvilken datakilde der skal bruges til at eksponere datakontrakten i modeltilknytningen, skal du angive et datakildenavn.</span><span class="sxs-lookup"><span data-stu-id="e387c-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="e387c-884">I den leverede kode er dette navn angivet med konstanten **ParametersDataSourceName**, der har værdien <a name="DataContractDSName"></a>**RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="e387c-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="e387c-885">I et nyt miljø skal du muligvis opdatere ER-metadataene, så denne klassetype er tilgængelig i ER-modeltilknytningsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="e387c-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="e387c-886">Du kan finde flere oplysninger under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="e387c-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="e387c-887">Tilføje en klasse for rapport-controller</span><span class="sxs-lookup"><span data-stu-id="e387c-887">Add a report controller class</span></span>

<span data-ttu-id="e387c-888">Føj den nye klasse **QuestionnairesErReportController** til dit Visual Studio-projekt, og skriv kode, der kører et ER-formatet enten i synkron tilstand eller batchtilstand, som du foretrækker, i den dialogboks, der er bygget på baggrund af logikken i den leverede klasse **QuestionnairesErReportUIBuilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="e387c-889">Tilføje et menupunkt</span><span class="sxs-lookup"><span data-stu-id="e387c-889">Add a menu item</span></span>

<span data-ttu-id="e387c-890">Føj det nye menupunkt **QuestionnairesErReport** til Visual Studio-projektet.</span><span class="sxs-lookup"><span data-stu-id="e387c-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="e387c-891">I egenskaben **Object** refererer dette menupunkt til klassen **QuestionnairesErReportController**, og det bruges til at angive en brugerrettighed til at vælge og køre et ER-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="e387c-892">I egenskaben **Etiket** refererer dette menupunkt til etiketten **\@QuestionnairesReport**, du har oprettet tidligere, så der vises en korrekt tekst på applikationens brugergrænseflade.</span><span class="sxs-lookup"><span data-stu-id="e387c-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="e387c-893">Tilføje et menupunkt til en menu</span><span class="sxs-lookup"><span data-stu-id="e387c-893">Add a menu item to a menu</span></span>

<span data-ttu-id="e387c-894">Tilføj den eksisterende menu **KM** i Visual Studio-projektet.</span><span class="sxs-lookup"><span data-stu-id="e387c-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="e387c-895">Du skal føje et nyt element for **QuestionnairesErReport** af typen **Output** til denne menu.</span><span class="sxs-lookup"><span data-stu-id="e387c-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="e387c-896">Dette element skal henvise til menupunktet **QuestionnairesErReport**, der er beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="e387c-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="e387c-897">Bygge et Visual Studio-projekt</span><span class="sxs-lookup"><span data-stu-id="e387c-897">Build a Visual Studio project</span></span>

<span data-ttu-id="e387c-898">Opbyg dit projekt for at gøre et nyt menupunkt tilgængeligt for brugerne.</span><span class="sxs-lookup"><span data-stu-id="e387c-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="e387c-899">Køre et format fra applikationen</span><span class="sxs-lookup"><span data-stu-id="e387c-899">Run a format from the application</span></span>

1. <span data-ttu-id="e387c-900">Gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer (leveret af ER)**.</span><span class="sxs-lookup"><span data-stu-id="e387c-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![Valg af menupunktet Rapport for spørgeskemaer (leveret af ER) i modulet Spørgeskema for at køre det konfigurerede ER-format](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="e387c-902">Vælg **Rapport for spørgeskemaer** i feltet **Formattilknytning** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e387c-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="e387c-903">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-903">Select **OK**.</span></span>
4. <span data-ttu-id="e387c-904">Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **Parametre for elektronisk rapportering**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e387c-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e387c-905">Vælg **OK** for at bekræfte filtreringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="e387c-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="e387c-906">Vælg **OK** for at køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-906">Select **OK** to run the report.</span></span>

    ![Angivelse af valgkriterierne i dialogboksen Elektronisk rapportering](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="e387c-908">Gennemse den oprettede rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="e387c-909">Tilpasse en designet ER-løsning</span><span class="sxs-lookup"><span data-stu-id="e387c-909">Tune a designed ER solution</span></span>

<span data-ttu-id="e387c-910">Du kan redigere den konfigurerede ER-løsning, så den bruger den dataproviderklasse, du har udviklet til at få adgang til oplysninger om det aktive ER-format, og så den angiver navnet på dette ER-format i en oprettet rapport.</span><span class="sxs-lookup"><span data-stu-id="e387c-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="e387c-911">Redigere en modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="e387c-912">Tilføje datakilder for at få adgang til et datakontraktobjekt</span><span class="sxs-lookup"><span data-stu-id="e387c-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="e387c-913">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-914">På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Tilknytning af spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="e387c-915">Vælg **Designer** for at åbne siden **Tilknytning af model til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="e387c-916">Vælg **Designer** for at åbne den valgte tilknytning i modeltilknytningsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="e387c-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="e387c-917">Vælg **Dynamics 365 for Operations\\Objekt** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="e387c-918">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="e387c-919">Angiv **[RunTimeParameters](#DataContractDSName)** i feltet **Navn** i dialogboksen som defineret i kildekoden for klassen **QuestionnairesErReportService**.</span><span class="sxs-lookup"><span data-stu-id="e387c-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="e387c-920">I feltet **Klasse** skal du angive **[QuestionnairesErReportContract](#DataContractClass)**, som er kodet tidligere.</span><span class="sxs-lookup"><span data-stu-id="e387c-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="e387c-921">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-921">Select **OK**.</span></span>
10. <span data-ttu-id="e387c-922">Udvid **RunTimeParameters**.</span><span class="sxs-lookup"><span data-stu-id="e387c-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="e387c-923">Den tilføjede datakilde indeholder oplysninger om post-id'et for den aktuelle ER-formattilknytning.</span><span class="sxs-lookup"><span data-stu-id="e387c-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Tilføjet datakilde i ER-modeltilknytningsdesigneren](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="e387c-925">Føje en datakilde for at få adgang til poster for ER-formattilknytning</span><span class="sxs-lookup"><span data-stu-id="e387c-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="e387c-926">Fortsæt med at redigere den valgte modeltilknytning ved at tilføje en datakilde for at få adgang til poster for ER-formattilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e387c-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="e387c-927">Vælg **Dynamics 365 for Operations\\Tabelposter** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.</span><span class="sxs-lookup"><span data-stu-id="e387c-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="e387c-928">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="e387c-929">I dialogboksen skal du angive **ER1** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="e387c-930">Indtast **ERFormatMappingTable** i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="e387c-931">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="e387c-932">Føje en datakilde for at få adgang til en formattilknytningspost for et aktuelt ER-format</span><span class="sxs-lookup"><span data-stu-id="e387c-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="e387c-933">Fortsæt med at redigere den valgte modeltilknytning ved at tilføje en datakilde for at få adgang til posten for formattilknytningen med det aktuelle ER-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="e387c-934">Vælg **Funktioner\\Beregnet felt** i ruden **Datakildetyper** på siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="e387c-935">Vælg **Tilføj rod** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="e387c-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="e387c-936">I dialogboksen skal du angive **ER2** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="e387c-937">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="e387c-938">I formeleditoren i feltet **Formel** skal du angive **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span><span class="sxs-lookup"><span data-stu-id="e387c-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="e387c-939">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="e387c-940">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="e387c-941">Angive navnet på det aktuelle ER-format i datamodellen</span><span class="sxs-lookup"><span data-stu-id="e387c-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="e387c-942">Fortsæt med at redigere den valgte modeltilknytning, så navnet på det aktuelle ER-format angives i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="e387c-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="e387c-943">På siden **Modeltilknytningsdesigner** skal du i ruden **Datamodel** skal du udvide **Udførelseskontekst** og derefter vælge **Udførelseskontekst\\Formatnavn**.</span><span class="sxs-lookup"><span data-stu-id="e387c-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="e387c-944">Vælg **Rediger** i ruden **Datamodel** for at konfigurere en databinding for den valgte datamodels felt.</span><span class="sxs-lookup"><span data-stu-id="e387c-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="e387c-945">I formeleditoren skal du angive **FIRSTORNULL (ER2.'\>Relations'.Format).Name** i feltet **Formel**.</span><span class="sxs-lookup"><span data-stu-id="e387c-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="e387c-946">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="e387c-947">Da du har brugt feltet **Formatnavn**, viser den konfigurerede modeltilknytning nu navnet på et ER-format, der kalder denne modeltilknytning under udførelsen.</span><span class="sxs-lookup"><span data-stu-id="e387c-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Binding af datamodelfeltet til metoden for den tilføjede datakilde i ER-modeltilknytningsdesigneren](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="e387c-949">Fuldføre designet af modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="e387c-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="e387c-950">Vælg **Gem** på siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="e387c-951">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e387c-951">Close the page.</span></span>
3. <span data-ttu-id="e387c-952">Luk siden for modeltilknytninger.</span><span class="sxs-lookup"><span data-stu-id="e387c-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="e387c-953">På siden **Konfigurationer** i konfigurationstræet skal du sikre, at konfigurationen **Tilknytning af spørgeskema** stadig er valgt.</span><span class="sxs-lookup"><span data-stu-id="e387c-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="e387c-954">Vælg derefter den konfigurationsversion, der har statussen **Kladde** på oversigtspanelet **Versioner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="e387c-955">Vælg **Skift status** \> **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e387c-956">Status for version 1.2 af denne konfiguration ændres fra **Kladde** til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="e387c-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e387c-957">Version 1.2 kan ikke længere ændres.</span><span class="sxs-lookup"><span data-stu-id="e387c-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="e387c-958">Denne version indeholder den konfigurerede modeltilknytning og kan bruges som grundlag for andre ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e387c-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e387c-959">Version 1.3 af denne konfiguration er oprettet og har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e387c-960">Du kan redigere denne version for at justere datatilknytningen **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="e387c-961">Redigere et format</span><span class="sxs-lookup"><span data-stu-id="e387c-961">Modify a format</span></span>

<span data-ttu-id="e387c-962">Du kan redigere det konfigurerede ER-format, så navnet vises i sidefoden i en rapport, der oprettes, når ER-formatet køres.</span><span class="sxs-lookup"><span data-stu-id="e387c-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="e387c-963">Tilføje et nyt formatelement.</span><span class="sxs-lookup"><span data-stu-id="e387c-963">Add a new format element</span></span>

1. <span data-ttu-id="e387c-964">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-965">På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e387c-966">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-966">Select **Designer**.</span></span>
4. <span data-ttu-id="e387c-967">Vælg rodelementet **Rapport** på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="e387c-968">Vælg **Tilføj** for at tilføje et nyt indlejret formatelement for det valgte rodelement for **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="e387c-969">Vælg **Excel\\Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="e387c-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="e387c-970">I feltet **Navn** skal du skrive **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="e387c-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="e387c-971">Vælg **Rapport\Sidefod**, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="e387c-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="e387c-972">Vælg **Tekst\\Streng**.</span><span class="sxs-lookup"><span data-stu-id="e387c-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="e387c-973">Binde det tilføjede formatelement</span><span class="sxs-lookup"><span data-stu-id="e387c-973">Bind the added format element</span></span>

1. <span data-ttu-id="e387c-974">Vælg **Rediger formel** for det aktive element for **Sidefod\\Streng** på siden **Formatdesigner** under fanen **Tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="e387c-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="e387c-975">Angiv **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** i feltet **Formel** i formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="e387c-976">Vælg **Gem**, og luk formeleditoren.</span><span class="sxs-lookup"><span data-stu-id="e387c-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="e387c-977">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e387c-977">Select **Save**.</span></span>

<span data-ttu-id="e387c-978">Det konfigurerede format er nu ændret, så navnet indsættes i sidefoden i en genereret rapport ved hjælp af elementet for **Sidefod\\Streng**.</span><span class="sxs-lookup"><span data-stu-id="e387c-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Tilføjelse af formatelementet Sidefod til det konfigurerede format i ER-operationsdesigneren](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="e387c-980">Fuldføre formatdesignet</span><span class="sxs-lookup"><span data-stu-id="e387c-980">Complete the format design</span></span>

1. <span data-ttu-id="e387c-981">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="e387c-982">På siden **Konfigurationer** i konfigurationstræet skal du sikre, at konfigurationen **Spørgeskemarapport** stadig er valgt.</span><span class="sxs-lookup"><span data-stu-id="e387c-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="e387c-983">Vælg derefter den konfigurationsversion, der har statussen **Kladde** på oversigtspanelet **Versioner**.</span><span class="sxs-lookup"><span data-stu-id="e387c-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="e387c-984">Vælg **Skift status** \> **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="e387c-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="e387c-985">Status for version 1.2 af denne konfiguration ændres fra **Kladde** til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="e387c-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="e387c-986">Version 1.2 kan ikke længere ændres.</span><span class="sxs-lookup"><span data-stu-id="e387c-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="e387c-987">Denne version indeholder det konfigurerede format og kan bruges som grundlag for andre ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e387c-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="e387c-988">Version 1.3 af denne konfiguration er oprettet og har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="e387c-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="e387c-989">Du kan redigere denne version for at justere rapporten **Spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e387c-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="e387c-990">Køre et format fra applikationen</span><span class="sxs-lookup"><span data-stu-id="e387c-990">Run a format from the application</span></span>

1. <span data-ttu-id="e387c-991">Gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer (leveret af ER)**.</span><span class="sxs-lookup"><span data-stu-id="e387c-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="e387c-992">Vælg **Rapport for spørgeskemaer** i feltet **Formattilknytning** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e387c-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="e387c-993">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-993">Select **OK**.</span></span>
4. <span data-ttu-id="e387c-994">Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **ER-parametre**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e387c-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e387c-995">Vælg **OK** for at bekræfte filtreringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="e387c-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="e387c-996">Vælg **OK** for at køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="e387c-997">Gennemse den oprettede rapport i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="e387c-998">Bemærk, at sidefoden i den oprettede rapport indeholder navnet på det ER-format, der blev brugt til at oprette den.</span><span class="sxs-lookup"><span data-stu-id="e387c-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Genereret rapport i Excel-format](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="e387c-1000">Køre et format fra ER</span><span class="sxs-lookup"><span data-stu-id="e387c-1000">Run a format from ER</span></span>

1. <span data-ttu-id="e387c-1001">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e387c-1002">På siden **Konfigurationer** skal du i konfigurationstræet skal du udvide **Spørgeskemamodel** og derefter vælge **Spørgeskemarapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="e387c-1003">Vælg **Kør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e387c-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="e387c-1004">Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **Parametre for elektronisk rapportering**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e387c-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e387c-1005">Vælg **OK** for at bekræfte filtreringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="e387c-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="e387c-1006">Vælg **OK** for at køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="e387c-1007">Gennemse den oprettede rapport i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="e387c-1008">Bemærk, at sidefoden i den oprettede rapport ikke indeholder navnet på det ER-format, der blev brugt til at generere den, da datakontraktobjektet ikke blev overført til den aktuelle modeltilknytning, da det blev kaldt af det ER-format, der blev kørt fra ER.</span><span class="sxs-lookup"><span data-stu-id="e387c-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="e387c-1009">Konfigurere en formatdestination til visning på skærmen</span><span class="sxs-lookup"><span data-stu-id="e387c-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="e387c-1010">Gå til **Virksomhedsadministration** \> **Elektronisk rapportering** \> **Destination for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="e387c-1011">På siden **Destination for elektronisk rapportering** skal du tilføje en destinationspost for det konfigurerede ER-format for **Spørgeskemarapport**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="e387c-1012">Konfigurer [destinationen](er-destination-type-screen.md) for **Skærm** for den formatkomponent for **Rapport**, der er [tilføjet](#AddFormatRootElement) som rodelementet for det konfigurerede ER-format for **Spørgeskemarapport**, i oversigtspanelet **Fildestination**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="e387c-1013">I oversigtspanelet **PDF-konverteringsindstillinger** kan du konfigurere destinationen til at konvertere en rapport til [PDF-format](electronic-reporting-destinations.md#OutputConversionToPDF), som bruger **Liggende** sideretning.</span><span class="sxs-lookup"><span data-stu-id="e387c-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![Konfiguration af den brugerdefinerede skærmdestination til ER-formatet på siden Destination for elektronisk rapportering](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="e387c-1015">Køre et format fra applikationen for at vise det som et PDF-dokument</span><span class="sxs-lookup"><span data-stu-id="e387c-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="e387c-1016">Gå til **Spørgeskema** \> **Design** \> **Rapport for spørgeskemaer (leveret af ER)**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="e387c-1017">Vælg **Rapport for spørgeskemaer** i feltet **Formattilknytning** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e387c-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="e387c-1018">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1018">Select **OK**.</span></span>
4. <span data-ttu-id="e387c-1019">Konfigurer filtreringsindstillingen på oversigtspanelet **Poster, der skal medtages** i dialogboksen **Parametre for elektronisk rapportering**, så det kun er **SBCCrsExam**-spørgeskemaet, der inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e387c-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="e387c-1020">Vælg **OK** for at bekræfte filtreringsindstillingen.</span><span class="sxs-lookup"><span data-stu-id="e387c-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="e387c-1021">Bemærk, at feltet **Output** i oversigtspanelet **Destinationer** er indstillet til **Skærm**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="e387c-1022">Hvis du vil ændre den konfigurerede destination, skal du vælge **Skift**.</span><span class="sxs-lookup"><span data-stu-id="e387c-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Dialogboks for ER-rapportens kørsel, hvor du kan ændre den konfigurerede destination](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="e387c-1024">Vælg **OK** for at køre rapporten.</span><span class="sxs-lookup"><span data-stu-id="e387c-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="e387c-1025">Gennemse den oprettede rapport i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="e387c-1025">Review the generated report in PDF format.</span></span>

    ![Eksempel på skærmen af den oprettede rapport i PDF-format.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="e387c-1027">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e387c-1027">Additional resources</span></span>

- [<span data-ttu-id="e387c-1028">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="e387c-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e387c-1029">Formelsprog i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="e387c-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="e387c-1030">Designe flersprogede rapporter</span><span class="sxs-lookup"><span data-stu-id="e387c-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="e387c-1031">API til ER-struktur</span><span class="sxs-lookup"><span data-stu-id="e387c-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="e387c-1032">Funktionen CASE</span><span class="sxs-lookup"><span data-stu-id="e387c-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="e387c-1033">Funktionen CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="e387c-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="e387c-1034">Funktionen DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="e387c-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="e387c-1035">Funktionen FILTER</span><span class="sxs-lookup"><span data-stu-id="e387c-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="e387c-1036">Funktionen FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="e387c-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="e387c-1037">Funktionen FORMAT</span><span class="sxs-lookup"><span data-stu-id="e387c-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="e387c-1038">Funktionen IF</span><span class="sxs-lookup"><span data-stu-id="e387c-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="e387c-1039">Funktionen ORDERBY</span><span class="sxs-lookup"><span data-stu-id="e387c-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="e387c-1040">Funktionen SESSIONNOW</span><span class="sxs-lookup"><span data-stu-id="e387c-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]