---
title: Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen
description: Dette emne indeholder oplysninger om, hvordan du kan bruge funktionen til performancesporing i elektroniske rapporter (ER) til at foretage fejlfinding af problemer med ydeevnen.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295567"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="f9b1b-103">Spore kørslen af ER-formater for at foretage fejlfinding af problemer med ydeevnen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f9b1b-104">Som en del af processen med at udvikle elektroniske rapporteringskonfigurationer (ER) til generering af elektroniske dokumenter definerer du den metode, der bruges til at få data ud af programmet og angive dem i det output, der genereres.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="f9b1b-105">ER-funktionen til sporing af ydeevnen hjælper med at reducere den tid og de omkostninger, der er involveret i indsamling af oplysninger om ER-format, betragteligt, og bruger oplysningerne til fejlfinding af problemer med ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="f9b1b-106">Dette selvstudium indeholder en vejledning i, hvordan du kan tage performancesporing for kørte ER-formater, og hvordan du kan bruge oplysningerne fra disse sporinger til at forbedre ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f9b1b-107">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f9b1b-107">Prerequisites</span></span>

<span data-ttu-id="f9b1b-108">Før du kan følge eksemplerne i dette selvstudium, skal du have følgende adgang:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="f9b1b-109">Adgang til en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="f9b1b-110">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f9b1b-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="f9b1b-111">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f9b1b-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f9b1b-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="f9b1b-112">System administrator</span></span>

- <span data-ttu-id="f9b1b-113">Adgang til den forekomst af Regulatory Configuration Service (RCS), der er klargjort til den samme lejer som programmet, for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="f9b1b-114">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f9b1b-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="f9b1b-115">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f9b1b-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f9b1b-116">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="f9b1b-116">System administrator</span></span>

<span data-ttu-id="f9b1b-117">Du skal også hente og lokalt gemme følgende filer.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="f9b1b-118">Fil</span><span class="sxs-lookup"><span data-stu-id="f9b1b-118">File</span></span>                                  | <span data-ttu-id="f9b1b-119">Indhold</span><span class="sxs-lookup"><span data-stu-id="f9b1b-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="f9b1b-120">Performance trace model.version.1</span><span class="sxs-lookup"><span data-stu-id="f9b1b-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="f9b1b-121">Eksempler på ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b1b-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="f9b1b-122">Performance trace metadata.version.1</span><span class="sxs-lookup"><span data-stu-id="f9b1b-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="f9b1b-123">Eksempler på ER-metadatakonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b1b-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="f9b1b-124">Performance trace mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="f9b1b-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="f9b1b-125">Eksempler på ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b1b-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="f9b1b-126">Performance trace format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="f9b1b-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="f9b1b-127">Eksempler på ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="f9b1b-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="f9b1b-128">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="f9b1b-128">Configure ER parameters</span></span>

<span data-ttu-id="f9b1b-129">Hver ER-performancesporing, der genereres i programmet, gemmes som en vedhæftet fil i kørselslogposten.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="f9b1b-130">Dokumentstyringsstrukturen bruges til at administrere disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="f9b1b-131">Du skal konfigurere ER-parametre i forvejen for at angive den DM-dokumenttype, der skal bruges til at tilknytte performancesporing.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="f9b1b-132">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="f9b1b-133">Vælg derefter den DM-dokumenttype, der skal bruges til performancesporing, i feltet **Andre** under fanen **vedhæftede filer** på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametre til elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="f9b1b-135">Hvis en DM-dokumenttype skal være tilgængelig i opslagsfeltet **Andet**, skal den være konfigureret på følgende måde på siden **Dokumenttyper** (**Organisationsadministration \> Administration af dokument \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="f9b1b-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="f9b1b-136">**Klasse:** Vedhæft fil</span><span class="sxs-lookup"><span data-stu-id="f9b1b-136">**Class:** Attach file</span></span>
- <span data-ttu-id="f9b1b-137">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="f9b1b-137">**Group:** File</span></span>

![Siden Dokumenttyper](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="f9b1b-139">Den valgte dokumenttype skal være tilgængelig i alle firmaer i den aktuelle forekomst, da vedhæftede DM-filer er firmaspecifikke.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="f9b1b-140">Konfigurere RCS-parametre</span><span class="sxs-lookup"><span data-stu-id="f9b1b-140">Configure RCS parameters</span></span>

<span data-ttu-id="f9b1b-141">ER-performancesporing, der genereres, bliver importeret til RCS til analyse ved hjælp af ER-formatdesigneren og ER-tilknytningsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="f9b1b-142">Da ER-performancesporinger gemmes som vedhæftede filer i den kørselslogpost, der er relateret til ER-formatet, skal du konfigurere RCS-parametrene på forhånd for at angive den DM-dokumenttype, der skal bruges til at tilknytte performancesporinger.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="f9b1b-143">I den forekomst af RCS, der er klargjort for dit firma, skal du vælge **Parametre til elektronisk rapportering** i arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="f9b1b-144">Vælg derefter den DM-dokumenttype, der skal bruges til performancesporing, i feltet **Andre** under fanen **vedhæftede filer** på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametre til elektronisk rapportering i RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="f9b1b-146">Hvis en DM-dokumenttype skal være tilgængelig i opslagsfeltet **Andet**, skal den være konfigureret på følgende måde på siden **Dokumenttyper** (**Organisationsadministration \> Administration af dokument \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="f9b1b-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="f9b1b-147">**Klasse:** Vedhæft fil</span><span class="sxs-lookup"><span data-stu-id="f9b1b-147">**Class:** Attach file</span></span>
- <span data-ttu-id="f9b1b-148">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="f9b1b-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="f9b1b-149">Designe en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="f9b1b-149">Design an ER solution</span></span>

<span data-ttu-id="f9b1b-150">Antag, at du er begyndt at designe en ny ER-løsning for at generere en ny rapport, der viser kreditorposteringer.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="f9b1b-151">I øjeblikket kan du finde posteringerne for en valgt kreditor på siden **Kreditorposteringer** (gå til **Kreditor \> Kreditorer \> Alle kreditorer**, vælg en kreditor, og vælg derefter i handlingsruden under fanen **Kreditor** i gruppen **Transaktioner** på **Posteringer**).</span><span class="sxs-lookup"><span data-stu-id="f9b1b-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="f9b1b-152">Men du vil have alle kreditorposteringer samtidig i et elektronisk dokument i XML-format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="f9b1b-153">Denne løsning består af flere ER-konfigurationer, der indeholder den nødvendige datamodel, metadata, modeltilknytning og formatkomponenter.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="f9b1b-154">Log på den forekomst af RCS, der er klargjort for dit firma.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="f9b1b-155">I dette selvstudium skal du oprette og ændre ER-konfigurationerne for eksempelfirmaet **Litware Inc.**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="f9b1b-156">Kontroller derfor, at denne konfigurationsudbyder er føjet til RCS og valgt som aktiv.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="f9b1b-157">Du kan finde instruktioner i proceduren [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f9b1b-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="f9b1b-158">I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="f9b1b-159">På siden **Konfigurationer** skal du importere de ER-konfigurationer, som du har hentet som en forudsætning i RCS, i følgende rækkefølge: datamodel, metadata, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="f9b1b-160">Benyt følgende fremgangsmåde for hver konfiguration:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="f9b1b-161">Vælg **Exchange \> Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="f9b1b-162">Vælg **Gennemse** for at vælge den relevante fil til den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="f9b1b-163">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-163">Select **OK**.</span></span>

    ![Siden Konfigurationer i RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="f9b1b-165">Køre ER-løsningen for at spore kørslen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="f9b1b-166">Antag, at du er færdig med at designe den første version af ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="f9b1b-167">Du vil nu teste den i din forekomst og analysere kørselsydeevnen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="f9b1b-168">Importere en ER-konfigurationer fra RCS til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f9b1b-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="f9b1b-169">Log på din programforekomst.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="f9b1b-170">I dette selvstudium skal du importere konfigurationer fra din RCS-forekomst (hvor du udformer dine ER-komponenter) i din forekomst (hvor du tester og til slut bruger dem).</span><span class="sxs-lookup"><span data-stu-id="f9b1b-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="f9b1b-171">Du skal derfor sikre dig, at alle påkrævede artefakter er forberedt.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="f9b1b-172">Du kan finde instruktioner i proceduren [Importer konfigurationer af elektronisk rapportering (ER) fra Regulatory Configuration Services (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="f9b1b-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="f9b1b-173">Udfør følgende trin for at importere konfigurationerne fra RCS i programmet:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="f9b1b-174">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** i feltet for **Litware, Inc.**-konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="f9b1b-175">På siden **Konfigurationslager** skal du vælge lageret for **RCS**-typen og derefter vælge **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="f9b1b-176">I oversigtspanelet **Varianter** skal du vælge konfigurationen **Format for performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="f9b1b-177">I oversigtspanelet **Versioner** skal du vælge version **1.1** af den valgte ER-konfiguration og derefter vælge **Importer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Siden Konfigurationslager](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="f9b1b-179">De tilsvarende versioner af datamodellen og modeltilknytningskonfigurationerne importeres automatisk som forudsætninger for den importerede ER-formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="f9b1b-180">Aktivere ER-performancesporing</span><span class="sxs-lookup"><span data-stu-id="f9b1b-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="f9b1b-181">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f9b1b-182">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f9b1b-183">Udfør følgende trin i sektionen **Kørselssporing** i dialogboksen **Brugerparametre**:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="f9b1b-184">I feltet **Fejlfinding af sporingsformat** kan du angive formatet for den genererede performancesporing, som kørselsoplysningerne skal gemmes i, for ER-format- og tilknytningselementer:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="f9b1b-185">**Fejlfinding af sporingsformat** – Vælg denne værdi, hvis du har planer om interaktiv kørsel af et ER-format med en kort udførelsestid.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="f9b1b-186">Indsamlingen af oplysninger om kørsel i ER-format startes derefter.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="f9b1b-187">Når denne værdi er valgt, indsamler performancesporing oplysninger om den tid, der bruges på følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="f9b1b-188">Kørsel af hver datakilde i den modeltilknytning, der kaldes for at hente data</span><span class="sxs-lookup"><span data-stu-id="f9b1b-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="f9b1b-189">Behandling af hvert formatelement for at angive data i det output, der genereres</span><span class="sxs-lookup"><span data-stu-id="f9b1b-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="f9b1b-190">Hvis du vælger værdien **Fejlfinding af sporingsformat**, kan du analysere indholdet af sporingen i ER-operationsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="f9b1b-191">Her kan du se det ER-format eller de tilknytningselementer, der er nævnt i sporingen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="f9b1b-192">**Samlet sporingsformat** – Vælg denne værdi, hvis du har planer om at køre et ER-format med en lang udførelsestid i batchtilstand.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="f9b1b-193">Indsamlingen af de samlede oplysninger om kørsel i ER-format startes derefter.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="f9b1b-194">Når denne værdi er valgt, indsamler performancesporing oplysninger om den tid, der bruges på følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="f9b1b-195">Kørsel af hver datakilde i den modeltilknytning, der kaldes for at hente data</span><span class="sxs-lookup"><span data-stu-id="f9b1b-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="f9b1b-196">Kørsel af hver datakilde i den formattilknytning, der kaldes for at hente data</span><span class="sxs-lookup"><span data-stu-id="f9b1b-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="f9b1b-197">Behandling af hvert formatelement for at angive data i det output, der genereres</span><span class="sxs-lookup"><span data-stu-id="f9b1b-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="f9b1b-198">Værdien **Samlet sporingsformat** er tilgængelig i Microsoft Dynamics 365 Finance version 10.0.20 og senere.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="f9b1b-199">I ER-formatdesigner og ER-modeltilknytningsdesigner kan du få vist den samlede udførelsestid for en enkelt komponent.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="f9b1b-200">Sporingen indeholder desuden detaljer om udførelsen, f.eks. antallet af udførelser samt minimum- og maksimumtiden for en enkelt udførelse.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="f9b1b-201">Denne sporing indsamles på baggrund af stien til de sporede komponenter.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="f9b1b-202">Derfor kan statistikken være forkert, når en enkelt overordnet komponent indeholder flere unavngivne underordnede komponenter, eller når flere underordnede komponenter har samme navn.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="f9b1b-203">Angiv følgende indstillinger til **Ja** for at indsamle specifikke oplysninger om kørslen af ER-modeltilknytningerne og ER-formatkomponenterne:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="f9b1b-204">**Indsaml forespørgselsstatistikker** – Når denne indstilling er aktiveret, indsamler performancesporing følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="f9b1b-205">Det antal databasekald, der er udført af datakilder</span><span class="sxs-lookup"><span data-stu-id="f9b1b-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="f9b1b-206">Antallet af dobbeltkald til databasen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="f9b1b-207">Oplysninger om de SQL-sætninger, der blev brugt til at foretage databasekald</span><span class="sxs-lookup"><span data-stu-id="f9b1b-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="f9b1b-208">**Spor adgang for cachelagring** – Når denne indstilling er slået til, indsamler performancesporing oplysninger om ER-modeltilknytningens cacheforbrug.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="f9b1b-209">**Spor dataadgang** – Når denne indstilling er aktiveret, indsamler performancesporing oplysninger om antallet af kald til databasen for de afviklede datakilder af postlistetypen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="f9b1b-210">**Fasttekst til sporingsliste** – Når denne indstilling er aktiveret, indsamler performancesporing oplysninger om antallet af poster, der er anmodet om fra datakilder af postlistetypen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9b1b-211">Parametrene i dialogboksen **Brugerparametre** er specifikke for brugeren og det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Dialogboksen Brugerparametre](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="f9b1b-213">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-213">Run the ER format</span></span>

1. <span data-ttu-id="f9b1b-214">Vælg firmaet **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="f9b1b-215">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="f9b1b-216">På siden **Konfigurationer** skal du vælge elementet **Format for performancesporing** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="f9b1b-217">Vælg **Kør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="f9b1b-218">Bemærk, at den fil, der genereres, indeholder oplysninger om 265 posteringer for seks kreditorer.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="f9b1b-219">Gennemse kørselssporingen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="f9b1b-220">Eksportere den genererede sporing fra programmet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-220">Export the generated trace from the application</span></span>

<span data-ttu-id="f9b1b-221">Performancesporing fjernes fra ER-kildeformatet og kan serialiseres til en ekstern zip-fil.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="f9b1b-222">Gå til **Organisationsadministration \> Elektronisk rapportering \> Fejlfindingslogs for konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="f9b1b-223">Vælg **Format for performancesporing** i feltet **Konfigurationsnavn** i den venstre rude på siden **Kørselslogge for elektronisk rapportering** for at finde de poster i loggen, der blev genereret ved kørslen af konfigurationen **Format for performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="f9b1b-224">Vælg knappen **Vedhæftede filer** (symbolet med papirklip) i øverste højre hjørne af siden eller tryk på **Ctrl+Skift+A**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Knappen Vedhæftede filer på siden Kørselslogge for elektronisk rapportering](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="f9b1b-226">Vælg **Åbn** i handlingsruden på siden **Vedhæftede filer til kørselslogge for elektronisk rapportering** for at få vist performance-sporing som en zip-fil og gemme den lokalt.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Vedhæftede filer til elektroniske rapporteringslogfiler](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="f9b1b-228">Den sporing, der genereres, har en reference til ER-kilderapporten via et entydigt rapport-id i **GUID**-format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="f9b1b-229">Formatets versionsnummer tages ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="f9b1b-230">Bemærk, at tilknytningen mellem den performancesporing, der er genereret for det kørte ER-format og ER-modeltilknytningen, er baseret på den rodbeskrivelse, der blev brugt, og den fælles datamodel.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="f9b1b-231">Formatets versionsnummer og modeltilknytningen tages ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="f9b1b-232">Indstillingen af **Standard for modeltilknytning**-flaget for modeltilknytningen tages heller ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="f9b1b-233">Import af den genererede sporing i RCS</span><span class="sxs-lookup"><span data-stu-id="f9b1b-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="f9b1b-234">I RCS i arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="f9b1b-235">Udvid elementet **Performancesporingsmodel** i konfigurationstræet på siden **Konfigurationer**, og vælg elementet **Performancesporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="f9b1b-236">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f9b1b-237">I oversigtspanelet på siden **Formatdesigner** skal du vælge **Performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f9b1b-238">Vælg **Importér performancesporing** i dialogboksen Indstillinger for resultat af **Indstillinger for resultat af performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="f9b1b-239">Vælg **Gennemse**, og vælg den zip-fil, du eksporterede tidligere.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="f9b1b-240">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-240">Select **OK**.</span></span>

    ![Dialogboksen Indstillinger for resultat af performancesporing i RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="f9b1b-242">Bruge performancesporing til analyse i RCS – formatkørsel</span><span class="sxs-lookup"><span data-stu-id="f9b1b-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="f9b1b-243">I RCS på siden **Formatdesigner** skal du vælge **Udvid/skjul** for at udvide indholdet af alle formatelementer.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="f9b1b-244">Bemærk, at der vises yderligere oplysninger for nogle af elementerne i det aktuelle format:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="f9b1b-245">Den faktiske tid, der er brugt på at indtaste data i det genererede output ved hjælp af formatelementet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="f9b1b-246">Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at generere hele outputtet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Siden Formatdesigner i RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="f9b1b-248">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="f9b1b-249">Bruge performancesporing til analyse i RCS – modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="f9b1b-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="f9b1b-250">I RCS på siden **Konfigurationer** skal du vælge elementet **Tilknytning af performancesporing** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="f9b1b-251">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f9b1b-252">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-252">Select **Designer**.</span></span>
4. <span data-ttu-id="f9b1b-253">I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f9b1b-254">Vælg den sporing, du tidligere har importeret.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="f9b1b-255">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-255">Select **OK**.</span></span>

<span data-ttu-id="f9b1b-256">Bemærk, at nye oplysninger bliver tilgængelige for nogle datakildeelementer i den aktuelle modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="f9b1b-257">Den tid, det faktisk blev brugt på at hente data vha. datakilden</span><span class="sxs-lookup"><span data-stu-id="f9b1b-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="f9b1b-258">Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at køre hele modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="f9b1b-259">Bemærk, at du får besked om, at den aktuelle modeltilknytning duplikerer databaseanmodninger, mens VendTable/\<Relationer/VendTrans.VendTable\_AccountNum-data køres.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="f9b1b-260">Denne duplikering sker, fordi listen over kreditorposteringer kaldes to gange for hver af de gentagne kreditorposter:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="f9b1b-261">Der foretages ét kald for at angive detaljer om hver transaktion i datamodellen baseret på konfigurerede bindinger.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="f9b1b-262">Der foretages ét kald for at angive det beregnede antal posteringer pr. kreditor i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Meddelelse om dublerede databaseanmodninger på siden Modeltilknytningsdesigner i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="f9b1b-264">Værdien **\[Q:530\]** angiver, at VendTrans-tabellen blev kaldt 530 gange for at returnere en post fra denne tabel til datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="f9b1b-265">Værdien **\[530\]** angiver, at datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum blev kaldt 530 gange for at returnere en post fra den pågældende datakilde og angive oplysningerne fra den i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="f9b1b-266">Det anbefales, at du bruger cachelagring til datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum for at reducere antallet af kald, der foretages, for at få oplysninger om 265-transaktioner og hjælpe med at forbedre modeltilknytningens performance.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="f9b1b-267">Det kan også være nyttigt at reducere antallet af kald, der foretages til LedgerTransTypeList-datakilden.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="f9b1b-268">Denne datakilde bruges til at knytte hver værdi i **LedgerTransType**-fastteksten til dens etiket.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="f9b1b-269">Hvis du bruger denne datakilde, kan du finde en passende etiket og angive den i datamodellen for hver enkelt kreditorpostering.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="f9b1b-270">Det aktuelle antal kald til denne datakilde (9.027) er meget højt for 265 transaktioner.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Modeltilknytningsdesigner i RCS, der viser 9.027 kald til datakilden](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="f9b1b-272">Forbedre modeltilknytningen på baggrund af oplysninger fra kørselssporing</span><span class="sxs-lookup"><span data-stu-id="f9b1b-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="f9b1b-273">Ændre modeltilknytningens logik</span><span class="sxs-lookup"><span data-stu-id="f9b1b-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="f9b1b-274">Udfør følgende trin for at bruge cachelagring til at forhindre, at der foretages identiske kald til databasen:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="f9b1b-275">I RCS på siden **Modeltilknytningsdesigner** skal du i ruden **Datakilder** vælge elementet **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="f9b1b-276">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="f9b1b-277">Udvid elementet **VendTable**, udvid listen over en-til-mange-relationer til datakilden VendTable (**\<Relationer**-elementet), og vælg **VendTrans. VendTable\_-AccountNum**-elementet.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="f9b1b-278">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-278">Select **Cache**.</span></span>

    ![Konfigurere cachelagring til at forhindre dobbelte kald](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="f9b1b-280">Udfør følgende trin for at bringe LedgerTransTypeList-datakilden ind i området for datakilden VendTable:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="f9b1b-281">Udvid elementet **Funktioner** i ruden **Datakildetyper**, og vælg elementet **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="f9b1b-282">Vælg elementet **VendTable** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="f9b1b-283">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-283">Select **Add**.</span></span>
    4. <span data-ttu-id="f9b1b-284">I feltet **Navn** skal du skrive **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="f9b1b-285">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="f9b1b-286">Skriv **LedgerTransTypeList** i feltet **Formel**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="f9b1b-287">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-287">Select **Save**.</span></span>
    8. <span data-ttu-id="f9b1b-288">Luk siden **Formeleditor**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="f9b1b-289">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-289">Click **OK**.</span></span>

3. <span data-ttu-id="f9b1b-290">Udfør følgende trin for at cachelagre feltet **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="f9b1b-291">Vælg elementet **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="f9b1b-292">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="f9b1b-293">Vælg elementet **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="f9b1b-294">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-294">Select **Cache**.</span></span>

    ![Konfigurere cachelagring for feltet $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="f9b1b-296">Udfør følgende trin for at ændre feltet **\$TransTypeRecord**, så det begynder at bruge det cachelagrede felt **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="f9b1b-297">Udvid elementet **VendTable** i ruden **Datakilder**, udvid **\<Relationer**-elementet, udvid **VendTrans.VendTable\_AccountNum**, og vælg elementet **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="f9b1b-298">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="f9b1b-299">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="f9b1b-300">Find følgende udtryk i feltet **Formel**:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="f9b1b-301">FIRSTORNULL (HVOR (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="f9b1b-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="f9b1b-302">Angiv følgende udtryk i feltet **Formel**:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="f9b1b-303">FIRSTORNULL (HVOR (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="f9b1b-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="f9b1b-304">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-304">Select **Save**.</span></span>
    7. <span data-ttu-id="f9b1b-305">Luk siden **Formeleditor**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="f9b1b-306">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-306">Select **OK**.</span></span>

5. <span data-ttu-id="f9b1b-307">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-307">Select **Save**.</span></span>
6. <span data-ttu-id="f9b1b-308">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="f9b1b-309">Luk siden **Modeltilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="f9b1b-310">Fuldføre den ændrede version af ER-modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="f9b1b-311">I RCS på siden **Konfigurationer** skal du i oversigtspanelet **Versioner** vælge version **1.2** af konfigurationen af **Tilknytning af performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="f9b1b-312">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-312">Select **Change status**.</span></span>
3. <span data-ttu-id="f9b1b-313">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="f9b1b-314">Importere konfigurationen af den ændrede modeltilknytning fra RCS til programmet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="f9b1b-315">Gentag trinnene i afsnittet [Importere en ER-konfiguration fra RCS til Finance and Operations](#import-configuration) tidligere i dette emne for at importere version 1.2 af **Tilknytning af performancesporing**-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="f9b1b-316">Køre den ændrede ER-løsning for at spore kørslen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="f9b1b-317">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-317">Run the ER format</span></span>

<span data-ttu-id="f9b1b-318">Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="f9b1b-319">Arbejde med sporingen af udførelsen</span><span class="sxs-lookup"><span data-stu-id="f9b1b-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="f9b1b-320">Eksportere den genererede sporing fra programmet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-320">Export the generated trace from the application</span></span>

<span data-ttu-id="f9b1b-321">Gentag trinnene i afsnittet [Eksportere den genererede sporing fra programmet](#export-trace) tidligere i dette emne, hvis du vil gemme en ny performancesporing lokalt.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="f9b1b-322">Import af den genererede sporing i RCS</span><span class="sxs-lookup"><span data-stu-id="f9b1b-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="f9b1b-323">Gentag trinnene i afsnittet [Importere de genererede sporinger i RCS](#import-trace) tidligere i dette emne for at importere den nye performancesporing til RCS.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="f9b1b-324">Bruge performancesporing til analyse i RCS – modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="f9b1b-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="f9b1b-325">Gentag trinnene i afsnittet [Bruge performancesporing til analyse i RCS – modeltilknytning](#use-trace) tidligere i dette emne for at analysere den seneste performancesporing.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="f9b1b-326">Bemærk, at de justeringer, du har foretaget for modeltilknytningen, har elimineret dubletter af forespørgsler til databasen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="f9b1b-327">Antallet af kald til databasetabeller og datakilder for denne modeltilknytning er også blevet reduceret.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="f9b1b-328">Derfor er ydeevnen i hele ER-løsningen forbedret.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![Spore oplysninger for VendTable-datakilde i RCS på siden Modeltilknytningsdesigner](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="f9b1b-330">I sporingsoplysningerne angiver værdien **\[12\]** for datakilden VendTable, at denne datakilde blev kaldt 12 gange.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="f9b1b-331">Værdien **\[Q:6\]** angiver, at seks kald blev oversat til databasekald til tabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="f9b1b-332">Værdien **\[C:6\]** angiver, at de poster, der blev hentet fra databasen, blev cachelagret, og seks andre kald blev behandlet ved hjælp af cachen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="f9b1b-333">Bemærk, at antallet af kald til datakilden LedgerTransTypeList er blevet reduceret fra 9.027 til 240.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Spore oplysninger for LedgerTransTypeList-datakilde i RCS på siden Modeltilknytningsdesigner](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="f9b1b-335">Gennemse udførelsessporingen i programmet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-335">Review the execution trace in the application</span></span>

<span data-ttu-id="f9b1b-336">Foruden RCS kan nogle versioner af tilbyde funktioner til ER-strukturdesigner.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="f9b1b-337">Disse versioner har indstillingen **Aktivér designtilstand**, der kan slås til.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="f9b1b-338">Du kan finde denne indstilling under fanen **Generelt** på siden **Parametre til elektronisk rapportering**, som du kan åbne fra arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Aktivere indstillingen designtilstand på siden med parametre for elektronisk rapportering](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="f9b1b-340">Hvis du bruger en af disse versioner, kan du analysere detaljerne for genererede performancesporinger direkte i programmet.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="f9b1b-341">Du behøver ikke at eksportere dem fra programmet og importere dem til RCS.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="f9b1b-342">Gennemse kørselssporing ved hjælp af eksterne værktøjer</span><span class="sxs-lookup"><span data-stu-id="f9b1b-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="f9b1b-343">Konfigurere brugerparametre</span><span class="sxs-lookup"><span data-stu-id="f9b1b-343">Configure user parameters</span></span>

1. <span data-ttu-id="f9b1b-344">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f9b1b-345">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f9b1b-346">Vælg **PerfView XML** i feltet **Udførelsessporingsformat** i afsnittet **Kørselssporing** i dialogboksen **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="f9b1b-347">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-347">Run the ER format</span></span>

<span data-ttu-id="f9b1b-348">Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="f9b1b-349">Bemærk, at webbrowseren kan hente en zip-fil til overførsel.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="f9b1b-350">Denne fil indeholder performancesporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="f9b1b-351">Du kan derefter bruge værktøjet PerfView-performanceanalyse til at analysere detaljerne i ER-formatkørslen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Oplysninger om performancesporing i PerfView-format](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="f9b1b-353">Brug eksterne værktøjer til at gennemse en udførelsessporing, der indeholder databaseforespørgsler</span><span class="sxs-lookup"><span data-stu-id="f9b1b-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="f9b1b-354">På grund af de forbedringer, der er foretaget i ER-strukturen, indeholder den performancesporing, der er genereret i PerfView-format, nu flere detaljer om udførelse af ER-format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="f9b1b-355">I Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (juli 2019) kan denne sporing også omfatte oplysninger om udførte SQL-forespørgsler i programdatabasen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="f9b1b-356">Konfigurere brugerparametre</span><span class="sxs-lookup"><span data-stu-id="f9b1b-356">Configure user parameters</span></span>

1. <span data-ttu-id="f9b1b-357">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f9b1b-358">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f9b1b-359">Angiv følgende parametre i sektionen **Kørselssporing** i dialogboksen **Brugerparametre**:</span><span class="sxs-lookup"><span data-stu-id="f9b1b-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="f9b1b-360">I feltet **Udførelsessporingsformat** skal du vælge **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="f9b1b-361">Angiv indstillingen **Indsaml forespørgselsstatistikker** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="f9b1b-362">Angiv indstillingen **Sporingsforespørgsel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Sektionen Sporing af udførelse, dialogboksen Brugerparametre](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="f9b1b-364">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="f9b1b-364">Run the ER format</span></span>

<span data-ttu-id="f9b1b-365">Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="f9b1b-366">Bemærk, at webbrowseren kan hente en zip-fil til overførsel.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="f9b1b-367">Denne fil indeholder performancesporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="f9b1b-368">Du kan derefter bruge værktøjet PerfView-performanceanalyse til at analysere detaljerne i ER-formatkørslen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="f9b1b-369">Denne sporing indeholder nu oplysninger om SQL-databaseadgang under udførelsen af ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Sporingsoplysninger om det udførte ER-format i PerfView](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="f9b1b-371">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f9b1b-371">Additional resources</span></span>

- [<span data-ttu-id="f9b1b-372">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f9b1b-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f9b1b-373">Forbedre ydeevnen af ER-løsninger ved at tilføje parameteriserede BEREGNET FELT-datakilder</span><span class="sxs-lookup"><span data-stu-id="f9b1b-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
