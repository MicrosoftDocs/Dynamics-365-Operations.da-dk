---
title: Spore kørsel af ER-format for at foretage fejlfinding af problemer med ydeevnen
description: Dette emne indeholder oplysninger om, hvordan du kan bruge funktionen til performancesporing i elektroniske rapporter (ER) til at foretage fejlfinding af problemer med ydeevnen.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576540"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="ec779-103">Spore kørslen af ER-formater for at foretage fejlfinding af problemer med ydeevnen</span><span class="sxs-lookup"><span data-stu-id="ec779-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ec779-104">Som en del af processen med at udvikle elektroniske rapporteringskonfigurationer (ER) til generering af elektroniske dokumenter definerer du den metode, der bruges til at få data ud af Microsoft Dynamics 365 for Finance and Operations og angive dem i det output, der genereres.</span><span class="sxs-lookup"><span data-stu-id="ec779-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="ec779-105">ER-funktionen til sporing af ydeevnen hjælper med at reducere den tid og de omkostninger, der er involveret i indsamling af oplysninger om ER-format, betragteligt, og bruger oplysningerne til fejlfinding af problemer med ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="ec779-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="ec779-106">Dette selvstudium indeholder en vejledning i, hvordan du kan tage performancesporing for kørte ER-formater i Finance and Operations, og hvordan du kan bruge oplysningerne fra disse sporinger til at forbedre ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="ec779-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ec779-107">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="ec779-107">Prerequisites</span></span>

<span data-ttu-id="ec779-108">Før du kan følge eksemplerne i dette selvstudium, skal du have følgende adgang:</span><span class="sxs-lookup"><span data-stu-id="ec779-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="ec779-109">Adgang til Finance and Operations for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="ec779-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="ec779-110">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ec779-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="ec779-111">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ec779-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ec779-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="ec779-112">System administrator</span></span>

- <span data-ttu-id="ec779-113">Adgang til den forekomst af Regulatory Configuration Service (RCS), der er klargjort til den samme lejer som Finance and Operations, for en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="ec779-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="ec779-114">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ec779-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="ec779-115">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ec779-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ec779-116">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="ec779-116">System administrator</span></span>

<span data-ttu-id="ec779-117">Du skal også hente og lokalt gemme følgende filer.</span><span class="sxs-lookup"><span data-stu-id="ec779-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="ec779-118">Fil</span><span class="sxs-lookup"><span data-stu-id="ec779-118">File</span></span>                                  | <span data-ttu-id="ec779-119">Indhold</span><span class="sxs-lookup"><span data-stu-id="ec779-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="ec779-120">Performance trace model.version.1</span><span class="sxs-lookup"><span data-stu-id="ec779-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="ec779-121">Eksempler på ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ec779-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="ec779-122">Performance trace metadata.version.1</span><span class="sxs-lookup"><span data-stu-id="ec779-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="ec779-123">Eksempler på ER-metadatakonfiguration</span><span class="sxs-lookup"><span data-stu-id="ec779-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="ec779-124">Performance trace mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="ec779-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="ec779-125">Eksempler på ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="ec779-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="ec779-126">Performance trace format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="ec779-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="ec779-127">Eksempler på ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="ec779-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="ec779-128">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="ec779-128">Configure ER parameters</span></span>

<span data-ttu-id="ec779-129">Hver ER-performancesporing, der genereres i Finance and Operations, gemmes som en vedhæftet fil i kørselslogposten.</span><span class="sxs-lookup"><span data-stu-id="ec779-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="ec779-130">Dokumentstyringsstrukturen i Finance and Operations bruges til at administrere disse vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="ec779-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="ec779-131">Du skal konfigurere ER-parametre i forvejen for at angive den DM-dokumenttype, der skal bruges til at tilknytte performancesporing.</span><span class="sxs-lookup"><span data-stu-id="ec779-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="ec779-132">Vælg **Parametre til elektronisk rapportering** i arbejdsområdet **Elektronisk rapportering** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec779-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="ec779-133">Vælg derefter den DM-dokumenttype, der skal bruges til performancesporing, i feltet **Andre** under fanen **vedhæftede filer** på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ec779-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametre til elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="ec779-135">Hvis en DM-dokumenttype skal være tilgængelig i opslagsfeltet **Andet**, skal den være konfigureret på følgende måde på siden **Dokumenttyper** (**Organisationsadministration \> Administration af dokument \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="ec779-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="ec779-136">**Klasse:** Vedhæft fil</span><span class="sxs-lookup"><span data-stu-id="ec779-136">**Class:** Attach file</span></span>
- <span data-ttu-id="ec779-137">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="ec779-137">**Group:** File</span></span>

![Siden Dokumenttyper i Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="ec779-139">Den valgte dokumenttype skal være tilgængelig i alle firmaer i den aktuelle Finance and Operations-forekomst, da vedhæftede DM-filer er firmaspecifikke.</span><span class="sxs-lookup"><span data-stu-id="ec779-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="ec779-140">Konfigurere RCS-parametre</span><span class="sxs-lookup"><span data-stu-id="ec779-140">Configure RCS parameters</span></span>

<span data-ttu-id="ec779-141">ER-performancesporing, der genereres i Finance and Operations, bliver importeret til RCS til analyse ved hjælp af ER-formatdesigneren og ER-tilknytningsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="ec779-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="ec779-142">Da ER-performancesporinger gemmes som vedhæftede filer i den kørselslogpost, der er relateret til ER-formatet, skal du konfigurere RCS-parametrene på forhånd for at angive den DM-dokumenttype, der skal bruges til at tilknytte performancesporinger.</span><span class="sxs-lookup"><span data-stu-id="ec779-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="ec779-143">I den forekomst af RCS, der er klargjort for dit firma, skal du vælge **Parametre til elektronisk rapportering** i arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ec779-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="ec779-144">Vælg derefter den DM-dokumenttype, der skal bruges til performancesporing, i feltet **Andre** under fanen **vedhæftede filer** på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ec779-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Siden Parametre til elektronisk rapportering i RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="ec779-146">Hvis en DM-dokumenttype skal være tilgængelig i opslagsfeltet **Andet**, skal den være konfigureret på følgende måde på siden **Dokumenttyper** (**Organisationsadministration \> Administration af dokument \> Dokumenttyper**):</span><span class="sxs-lookup"><span data-stu-id="ec779-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="ec779-147">**Klasse:** Vedhæft fil</span><span class="sxs-lookup"><span data-stu-id="ec779-147">**Class:** Attach file</span></span>
- <span data-ttu-id="ec779-148">**Gruppe:** Fil</span><span class="sxs-lookup"><span data-stu-id="ec779-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="ec779-149">Designe en ER-løsning</span><span class="sxs-lookup"><span data-stu-id="ec779-149">Design an ER solution</span></span>

<span data-ttu-id="ec779-150">Antag, at du er begyndt at designe en ny ER-løsning for at generere en ny rapport, der viser kreditorposteringer.</span><span class="sxs-lookup"><span data-stu-id="ec779-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="ec779-151">I øjeblikket kan du finde posteringerne for en valgt kreditor på siden **Kreditorposteringer** (gå til **Kreditor \> Kreditorer \> Alle kreditorer**, vælg en kreditor, og vælg derefter i handlingsruden under fanen **Kreditor** i gruppen **Transaktioner** på **Posteringer**).</span><span class="sxs-lookup"><span data-stu-id="ec779-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="ec779-152">Men du vil have alle kreditorposteringer samtidig i et elektronisk dokument i XML-format.</span><span class="sxs-lookup"><span data-stu-id="ec779-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="ec779-153">Denne løsning består af flere ER-konfigurationer, der indeholder den nødvendige datamodel, metadata, modeltilknytning og formatkomponenter.</span><span class="sxs-lookup"><span data-stu-id="ec779-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="ec779-154">Log på den forekomst af RCS, der er klargjort for dit firma.</span><span class="sxs-lookup"><span data-stu-id="ec779-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="ec779-155">I dette selvstudium skal du oprette og ændre ER-konfigurationerne for eksempelfirmaet **Litware Inc.**.</span><span class="sxs-lookup"><span data-stu-id="ec779-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="ec779-156">Kontroller derfor, at denne konfigurationsudbyder er føjet til RCS og valgt som aktiv.</span><span class="sxs-lookup"><span data-stu-id="ec779-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="ec779-157">Du kan finde instruktioner i proceduren [Oprette konfigurationsudbydere og markere dem som aktive](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="ec779-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="ec779-158">I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="ec779-159">På siden **Konfigurationer** skal du importere de ER-konfigurationer, som du har hentet som en forudsætning i RCS, i følgende rækkefølge: datamodel, metadata, modeltilknytning, format.</span><span class="sxs-lookup"><span data-stu-id="ec779-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="ec779-160">Benyt følgende fremgangsmåde for hver konfiguration:</span><span class="sxs-lookup"><span data-stu-id="ec779-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="ec779-161">Vælg **Exchange \> Indlæs fra XML-fil** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec779-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="ec779-162">Vælg **Gennemse** for at vælge den relevante fil til den krævede ER-konfiguration i XML-format.</span><span class="sxs-lookup"><span data-stu-id="ec779-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="ec779-163">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec779-163">Select **OK**.</span></span>

    ![Siden Konfigurationer i RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="ec779-165">Køre ER-løsningen for at spore kørslen</span><span class="sxs-lookup"><span data-stu-id="ec779-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="ec779-166">Antag, at du er færdig med at designe den første version af ER-løsningen.</span><span class="sxs-lookup"><span data-stu-id="ec779-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="ec779-167">Du vil nu teste den i din Finance and Operations-forekomst og analysere kørselsydeevnen.</span><span class="sxs-lookup"><span data-stu-id="ec779-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="ec779-168">Importere en ER-konfiguration fra RCS til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec779-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="ec779-169">Log på din forekomst af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec779-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="ec779-170">I dette selvstudium skal du importere konfigurationer fra din RCS-forekomst (hvor du udformer dine ER-komponenter) i din Finance and Operations-forekomst (hvor du tester og til slut bruger dem).</span><span class="sxs-lookup"><span data-stu-id="ec779-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="ec779-171">Du skal derfor sikre dig, at alle påkrævede artefakter er forberedt.</span><span class="sxs-lookup"><span data-stu-id="ec779-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="ec779-172">Du kan finde instruktioner i proceduren [Importer konfigurationer af elektronisk rapportering (ER) fra Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="ec779-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="ec779-173">Udfør følgende trin for at importere konfigurationerne fra RCS i Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="ec779-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="ec779-174">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** i feltet for **Litware, Inc.**-konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="ec779-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="ec779-175">På siden **Konfigurationslager** skal du vælge lageret for **RCS**-typen og derefter vælge **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="ec779-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="ec779-176">I oversigtspanelet **Varianter** skal du vælge konfigurationen **Format for performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="ec779-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="ec779-177">I oversigtspanelet **Versioner** skal du vælge version **1.1** af den valgte ER-konfiguration og derefter vælge **Importer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Siden Konfigurationslager i Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="ec779-179">De tilsvarende versioner af datamodellen og modeltilknytningskonfigurationerne importeres automatisk som forudsætninger for den importerede ER-formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ec779-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="ec779-180">Aktivere ER-performancesporing</span><span class="sxs-lookup"><span data-stu-id="ec779-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="ec779-181">I Finance and Operations skal du gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ec779-182">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="ec779-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ec779-183">Udfør følgende trin i sektionen **Kørselssporing** i dialogboksen **Brugerparametre**:</span><span class="sxs-lookup"><span data-stu-id="ec779-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="ec779-184">Vælg **Fejlfinding af sporingsformat** i feltet **Udførelsessporingsformat** for at starte indsamling af oplysninger om ER-format.</span><span class="sxs-lookup"><span data-stu-id="ec779-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="ec779-185">Når denne værdi er valgt, indsamler performancesporing oplysninger om den tid, der bruges på følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="ec779-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="ec779-186">Kørsel af hver datakilde i den modeltilknytning, der kaldes for at hente data</span><span class="sxs-lookup"><span data-stu-id="ec779-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="ec779-187">Behandling af hvert formatelement for at angive data i det output, der genereres</span><span class="sxs-lookup"><span data-stu-id="ec779-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="ec779-188">Du kan bruge feltet **Fejlfinding af sporingsformat** til at angive formatet for den genererede performancesporing, som kørselsoplysningerne gemmes i, for ER-format- og tilknytningselementer.</span><span class="sxs-lookup"><span data-stu-id="ec779-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="ec779-189">Hvis du vælger **Fejlfinding af sporingsformat** som værdi, kan du analysere indholdet af sporingen i ER Operations-designeren og se de ER-format eller -tilknytningselementer, der er nævnt i sporingen.</span><span class="sxs-lookup"><span data-stu-id="ec779-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="ec779-190">Angiv følgende indstillinger til **Ja** for at indsamle specifikke oplysninger om kørslen af ER-modeltilknytningerne og ER-formatkomponenterne:</span><span class="sxs-lookup"><span data-stu-id="ec779-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="ec779-191">**Indsaml forespørgselsstatistikker** – Når denne indstilling er aktiveret, indsamler performancesporing følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="ec779-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="ec779-192">Det antal databasekald, der er udført af datakilder</span><span class="sxs-lookup"><span data-stu-id="ec779-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="ec779-193">Antallet af dobbeltkald til databasen</span><span class="sxs-lookup"><span data-stu-id="ec779-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="ec779-194">Oplysninger om de SQL-sætninger, der blev brugt til at foretage databasekald</span><span class="sxs-lookup"><span data-stu-id="ec779-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="ec779-195">**Spor adgang for cachelagring** – Når denne indstilling er slået til, indsamler performancesporing oplysninger om ER-modeltilknytningens cacheforbrug.</span><span class="sxs-lookup"><span data-stu-id="ec779-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="ec779-196">**Spor dataadgang** – Når denne indstilling er aktiveret, indsamler performancesporing oplysninger om antallet af kald til databasen for de afviklede datakilder af postlistetypen.</span><span class="sxs-lookup"><span data-stu-id="ec779-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="ec779-197">**Fasttekst til sporingsliste** – Når denne indstilling er aktiveret, indsamler performancesporing oplysninger om antallet af poster, der er anmodet om fra datakilder af postlistetypen.</span><span class="sxs-lookup"><span data-stu-id="ec779-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec779-198">Parametrene i dialogboksen **Brugerparametre** er specifikke for brugeren og det aktuelle firma.</span><span class="sxs-lookup"><span data-stu-id="ec779-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Dialogboksen Brugerparametre i Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="ec779-200">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="ec779-200">Run the ER format</span></span>

1. <span data-ttu-id="ec779-201">I Finance and Operations skal du vælge **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="ec779-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="ec779-202">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="ec779-203">På siden **Konfigurationer** skal du vælge elementet **Format for performancesporing** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="ec779-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="ec779-204">Vælg **Kør** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec779-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="ec779-205">Bemærk, at den fil, der genereres, indeholder oplysninger om 265 posteringer for seks kreditorer.</span><span class="sxs-lookup"><span data-stu-id="ec779-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="ec779-206">Gennemse kørselssporingen</span><span class="sxs-lookup"><span data-stu-id="ec779-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="ec779-207">Eksportere den genererede sporing fra Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec779-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="ec779-208">Performancesporing fjernes fra ER-kildeformatet og kan serialiseres til en ekstern zip-fil.</span><span class="sxs-lookup"><span data-stu-id="ec779-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="ec779-209">I Finance and Operations skal du gå til **Virksomhedsadministration \> Elektronisk rapportering \> Fejlfindingslogs for konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="ec779-210">Vælg **Format for performancesporing** i feltet **Konfigurationsnavn** i den venstre rude på siden **Kørselslogge for elektronisk rapportering** for at finde de poster i loggen, der blev genereret ved kørslen af konfigurationen **Format for performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="ec779-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="ec779-211">Vælg knappen **Vedhæftede filer** (symbolet med papirklip) i øverste højre hjørne af siden eller tryk på **Ctrl+Skift+A**.</span><span class="sxs-lookup"><span data-stu-id="ec779-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Knappen Vedhæftede filer på siden Kørselslogge for elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="ec779-213">Vælg **Åbn** i handlingsruden på siden **Vedhæftede filer til kørselslogge for elektronisk rapportering** for at få vist performance-sporing som en zip-fil og gemme den lokalt.</span><span class="sxs-lookup"><span data-stu-id="ec779-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Vedhæftede filer i Kørselslogge for elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="ec779-215">Den sporing, der genereres, har en reference til ER-kilderapporten via et entydigt rapport-id i **GUID**-format.</span><span class="sxs-lookup"><span data-stu-id="ec779-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="ec779-216">Formatets versionsnummer tages ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="ec779-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="ec779-217">Bemærk, at tilknytningen mellem den performancesporing, der er genereret for det kørte ER-format og ER-modeltilknytningen, er baseret på den rodbeskrivelse, der blev brugt, og den fælles datamodel.</span><span class="sxs-lookup"><span data-stu-id="ec779-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="ec779-218">Formatets versionsnummer og modeltilknytningen tages ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="ec779-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="ec779-219">Indstillingen af **Standard for modeltilknytning**-flaget for modeltilknytningen tages heller ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="ec779-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="ec779-220">Import af den genererede sporing i RCS</span><span class="sxs-lookup"><span data-stu-id="ec779-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="ec779-221">I RCS i arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="ec779-222">Udvid elementet **Performancesporingsmodel** i konfigurationstræet på siden **Konfigurationer**, og vælg elementet **Performancesporingsformat**.</span><span class="sxs-lookup"><span data-stu-id="ec779-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="ec779-223">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec779-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="ec779-224">I oversigtspanelet på siden **Formatdesigner** skal du vælge **Performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="ec779-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="ec779-225">Vælg **Importér performancesporing** i dialogboksen Indstillinger for resultat af **Indstillinger for resultat af performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="ec779-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="ec779-226">Vælg **Gennemse** for at vælge den zip-fil, du har eksporteret fra Finance and Operations tidligere.</span><span class="sxs-lookup"><span data-stu-id="ec779-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="ec779-227">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec779-227">Select **OK**.</span></span>

    ![Dialogboksen Indstillinger for resultat af performancesporing i RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="ec779-229">Bruge performancesporing til analyse i RCS – formatkørsel</span><span class="sxs-lookup"><span data-stu-id="ec779-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="ec779-230">I RCS på siden **Formatdesigner** skal du vælge **Udvid/skjul** for at udvide indholdet af alle formatelementer.</span><span class="sxs-lookup"><span data-stu-id="ec779-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="ec779-231">Bemærk, at der vises yderligere oplysninger for nogle af elementerne i det aktuelle format:</span><span class="sxs-lookup"><span data-stu-id="ec779-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="ec779-232">Den faktiske tid, der er brugt på at indtaste data i det genererede output ved hjælp af formatelementet</span><span class="sxs-lookup"><span data-stu-id="ec779-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="ec779-233">Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at generere hele outputtet</span><span class="sxs-lookup"><span data-stu-id="ec779-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Siden Formatdesigner i RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="ec779-235">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="ec779-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="ec779-236">Bruge performancesporing til analyse i RCS – modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="ec779-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="ec779-237">I RCS på siden **Konfigurationer** skal du vælge elementet **Tilknytning af performancesporing** i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="ec779-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="ec779-238">Vælg **Designer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ec779-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="ec779-239">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-239">Select **Designer**.</span></span>
4. <span data-ttu-id="ec779-240">I oversigtspanelet på siden **Modeltilknytningsdesigner** skal du vælge **Performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="ec779-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="ec779-241">Vælg den sporing, du tidligere har importeret.</span><span class="sxs-lookup"><span data-stu-id="ec779-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="ec779-242">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec779-242">Select **OK**.</span></span>

<span data-ttu-id="ec779-243">Bemærk, at nye oplysninger bliver tilgængelige for nogle datakildeelementer i den aktuelle modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="ec779-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="ec779-244">Den tid, det faktisk blev brugt på at hente data vha. datakilden</span><span class="sxs-lookup"><span data-stu-id="ec779-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="ec779-245">Den samme tid angivet som en procentdel af den samlede tid, der blev brugt på at køre hele modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="ec779-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="ec779-246">Bemærk, at du får besked om, at den aktuelle modeltilknytning duplikerer databaseanmodninger, mens VendTable/\<Relationer/VendTrans.VendTable\_AccountNum-data køres.</span><span class="sxs-lookup"><span data-stu-id="ec779-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="ec779-247">Denne duplikering sker, fordi listen over kreditorposteringer kaldes to gange for hver af de gentagne kreditorposter:</span><span class="sxs-lookup"><span data-stu-id="ec779-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="ec779-248">Der foretages ét kald for at angive detaljer om hver transaktion i datamodellen baseret på konfigurerede bindinger.</span><span class="sxs-lookup"><span data-stu-id="ec779-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="ec779-249">Der foretages ét kald for at angive det beregnede antal posteringer pr. kreditor i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="ec779-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Meddelelse om dublerede databaseanmodninger på siden Modeltilknytningsdesigner i RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="ec779-251">Værdien **\[Q:530\]** angiver, at VendTrans-tabellen blev kaldt 530 gange for at returnere en post fra denne tabel til datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="ec779-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="ec779-252">Værdien **\[530\]** angiver, at datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum blev kaldt 530 gange for at returnere en post fra den pågældende datakilde og angive oplysningerne fra den i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="ec779-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="ec779-253">Det anbefales, at du bruger cachelagring til datakilden VendTable/\<Relationer/VendTrans.VendTable\_AccountNum for at reducere antallet af kald, der foretages, for at få oplysninger om 265-transaktioner og hjælpe med at forbedre modeltilknytningens performance.</span><span class="sxs-lookup"><span data-stu-id="ec779-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="ec779-254">Det kan også være nyttigt at reducere antallet af kald, der foretages til LedgerTransTypeList-datakilden.</span><span class="sxs-lookup"><span data-stu-id="ec779-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="ec779-255">Denne datakilde bruges til at knytte hver værdi i **LedgerTransType**-fastteksten til dens etiket.</span><span class="sxs-lookup"><span data-stu-id="ec779-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="ec779-256">Hvis du bruger denne datakilde, kan du finde en passende etiket og angive den i datamodellen for hver enkelt kreditorpostering.</span><span class="sxs-lookup"><span data-stu-id="ec779-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="ec779-257">Det aktuelle antal kald til denne datakilde (9.027) er meget højt for 265 transaktioner.</span><span class="sxs-lookup"><span data-stu-id="ec779-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Modeltilknytningsdesigner i RCS, der viser 9.027 kald til datakilden](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="ec779-259">Forbedre modeltilknytningen på baggrund af oplysninger fra kørselssporing</span><span class="sxs-lookup"><span data-stu-id="ec779-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="ec779-260">Ændre modeltilknytningens logik</span><span class="sxs-lookup"><span data-stu-id="ec779-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="ec779-261">Udfør følgende trin for at bruge cachelagring til at forhindre, at der foretages identiske kald til databasen:</span><span class="sxs-lookup"><span data-stu-id="ec779-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="ec779-262">I RCS på siden **Modeltilknytningsdesigner** skal du i ruden **Datakilder** vælge elementet **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="ec779-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="ec779-263">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="ec779-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="ec779-264">Udvid elementet **VendTable**, udvid listen over en-til-mange-relationer til datakilden VendTable (**\<Relationer**-elementet), og vælg **VendTrans. VendTable\_-AccountNum**-elementet.</span><span class="sxs-lookup"><span data-stu-id="ec779-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="ec779-265">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="ec779-265">Select **Cache**.</span></span>

    ![Konfigurere cachelagring til at forhindre dobbelte kald](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="ec779-267">Udfør følgende trin for at bringe LedgerTransTypeList-datakilden ind i området for datakilden VendTable:</span><span class="sxs-lookup"><span data-stu-id="ec779-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="ec779-268">Udvid elementet **Funktioner** i ruden **Datakildetyper**, og vælg elementet **Beregnet felt**.</span><span class="sxs-lookup"><span data-stu-id="ec779-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="ec779-269">Vælg elementet **VendTable** i ruden **Datakilder**.</span><span class="sxs-lookup"><span data-stu-id="ec779-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="ec779-270">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="ec779-270">Select **Add**.</span></span>
    4. <span data-ttu-id="ec779-271">I feltet **Navn** skal du skrive **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="ec779-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="ec779-272">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="ec779-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="ec779-273">Skriv **LedgerTransTypeList** i feltet **Formel**.</span><span class="sxs-lookup"><span data-stu-id="ec779-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="ec779-274">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec779-274">Select **Save**.</span></span>
    8. <span data-ttu-id="ec779-275">Luk siden **Formeleditor**.</span><span class="sxs-lookup"><span data-stu-id="ec779-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="ec779-276">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec779-276">Click **OK**.</span></span>

3. <span data-ttu-id="ec779-277">Udfør følgende trin for at cachelagre feltet **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="ec779-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="ec779-278">Vælg elementet **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="ec779-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="ec779-279">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="ec779-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="ec779-280">Vælg elementet **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="ec779-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="ec779-281">Vælg **Cache**.</span><span class="sxs-lookup"><span data-stu-id="ec779-281">Select **Cache**.</span></span>

    ![Konfigurere cachelagring for feltet $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="ec779-283">Udfør følgende trin for at ændre feltet **\$TransTypeRecord**, så det begynder at bruge det cachelagrede felt **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="ec779-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="ec779-284">Udvid elementet **VendTable** i ruden **Datakilder**, udvid **\<Relationer**-elementet, udvid **VendTrans.VendTable\_AccountNum**, og vælg elementet **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="ec779-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="ec779-285">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ec779-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="ec779-286">Vælg **Rediger formel**.</span><span class="sxs-lookup"><span data-stu-id="ec779-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="ec779-287">Find følgende udtryk i feltet **Formel**:</span><span class="sxs-lookup"><span data-stu-id="ec779-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="ec779-288">FIRSTORNULL (HVOR (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="ec779-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="ec779-289">Angiv følgende udtryk i feltet **Formel**:</span><span class="sxs-lookup"><span data-stu-id="ec779-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="ec779-290">FIRSTORNULL (HVOR (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="ec779-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="ec779-291">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec779-291">Select **Save**.</span></span>
    7. <span data-ttu-id="ec779-292">Luk siden **Formeleditor**.</span><span class="sxs-lookup"><span data-stu-id="ec779-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="ec779-293">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec779-293">Select **OK**.</span></span>

5. <span data-ttu-id="ec779-294">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ec779-294">Select **Save**.</span></span>
6. <span data-ttu-id="ec779-295">Luk siden **Modeltilknytningsdesigner**.</span><span class="sxs-lookup"><span data-stu-id="ec779-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="ec779-296">Luk siden **Modeltilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="ec779-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="ec779-297">Fuldføre den ændrede version af ER-modeltilknytningen</span><span class="sxs-lookup"><span data-stu-id="ec779-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="ec779-298">I RCS på siden **Konfigurationer** skal du i oversigtspanelet **Versioner** vælge version **1.2** af konfigurationen af **Tilknytning af performancesporing**.</span><span class="sxs-lookup"><span data-stu-id="ec779-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="ec779-299">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="ec779-299">Select **Change status**.</span></span>
3. <span data-ttu-id="ec779-300">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="ec779-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="ec779-301">Importere konfigurationen af den ændrede modeltilknytning fra RCS til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec779-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="ec779-302">Gentag trinnene i afsnittet [Importere en ER-konfiguration fra RCS til Finance and Operations](#import-configuration) tidligere i dette emne for at importere version 1.2 af **Tilknytning af performancesporing** konfigurationen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec779-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="ec779-303">Køre den ændrede ER-løsning for at spore kørslen</span><span class="sxs-lookup"><span data-stu-id="ec779-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="ec779-304">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="ec779-304">Run the ER format</span></span>

<span data-ttu-id="ec779-305">Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.</span><span class="sxs-lookup"><span data-stu-id="ec779-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="ec779-306">Gennemse kørselssporingen</span><span class="sxs-lookup"><span data-stu-id="ec779-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="ec779-307">Eksportere den genererede sporing fra Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec779-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="ec779-308">Gentag trinnene i afsnittet [Eksporter den genererede sporing fra Finance and Operations](#export-trace) tidligere i dette emne, hvis du vil gemme en ny performancesporing lokalt.</span><span class="sxs-lookup"><span data-stu-id="ec779-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="ec779-309">Import af den genererede sporing i RCS</span><span class="sxs-lookup"><span data-stu-id="ec779-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="ec779-310">Gentag trinnene i afsnittet [Importere de genererede sporinger i RCS](#import-trace) tidligere i dette emne for at importere den nye performancesporing til RCS.</span><span class="sxs-lookup"><span data-stu-id="ec779-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="ec779-311">Bruge performancesporing til analyse i RCS – modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="ec779-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="ec779-312">Gentag trinnene i afsnittet [Bruge performancesporing til analyse i RCS – modeltilknytning](#use-trace) tidligere i dette emne for at analysere den seneste performancesporing.</span><span class="sxs-lookup"><span data-stu-id="ec779-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="ec779-313">Bemærk, at de justeringer, du har foretaget for modeltilknytningen, har elimineret dubletter af forespørgsler til databasen.</span><span class="sxs-lookup"><span data-stu-id="ec779-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="ec779-314">Antallet af kald til databasetabeller og datakilder for denne modeltilknytning er også blevet reduceret.</span><span class="sxs-lookup"><span data-stu-id="ec779-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="ec779-315">Derfor er ydeevnen i hele ER-løsningen forbedret.</span><span class="sxs-lookup"><span data-stu-id="ec779-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Spore oplysninger for VendTable-datakilde i RCS på siden Modeltilknytningsdesigner](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="ec779-317">I sporingsoplysningerne angiver værdien **\[12\]** for datakilden VendTable, at denne datakilde blev kaldt 12 gange.</span><span class="sxs-lookup"><span data-stu-id="ec779-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="ec779-318">Værdien **\[Q:6\]** angiver, at seks kald blev oversat til databasekald til tabellen VendTable.</span><span class="sxs-lookup"><span data-stu-id="ec779-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="ec779-319">Værdien **\[C:6\]** angiver, at de poster, der blev hentet fra databasen, blev cachelagret, og seks andre kald blev behandlet ved hjælp af cachen.</span><span class="sxs-lookup"><span data-stu-id="ec779-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="ec779-320">Bemærk, at antallet af kald til datakilden LedgerTransTypeList er blevet reduceret fra 9.027 til 240.</span><span class="sxs-lookup"><span data-stu-id="ec779-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Spore oplysninger for LedgerTransTypeList-datakilde i RCS på siden Modeltilknytningsdesigner](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="ec779-322">Gennemse kørselssporingen i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec779-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="ec779-323">Ud over RCS kan nogle versioner af Finance and Operations tilbyde funktioner til ER-strukturdesigner.</span><span class="sxs-lookup"><span data-stu-id="ec779-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="ec779-324">Disse versioner af Finance and Operations har indstillingen **Aktiver designtilstand**, der kan slås til.</span><span class="sxs-lookup"><span data-stu-id="ec779-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="ec779-325">Du kan finde denne indstilling under fanen **Generelt** på siden **Parametre til elektronisk rapportering**, som du kan åbne fra arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ec779-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Aktivere designtilstandsindstillingen på siden Parametre for elektronisk rapportering i Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="ec779-327">Hvis du bruger en af disse versioner af Finance and Operations, kan du analysere detaljerne for genererede performancesporinger direkte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec779-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="ec779-328">Du behøver ikke at eksportere dem fra Finance and Operations og importere dem til RCS.</span><span class="sxs-lookup"><span data-stu-id="ec779-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="ec779-329">Gennemse kørselssporing ved hjælp af eksterne værktøjer</span><span class="sxs-lookup"><span data-stu-id="ec779-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="ec779-330">Konfigurere brugerparametre</span><span class="sxs-lookup"><span data-stu-id="ec779-330">Configure user parameters</span></span>

1. <span data-ttu-id="ec779-331">I Finance and Operations skal du gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="ec779-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ec779-332">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="ec779-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ec779-333">Vælg **PerfView XML** i feltet **Udførelsessporingsformat** i afsnittet **Kørselssporing** i dialogboksen **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="ec779-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="ec779-334">Køre ER-formatet</span><span class="sxs-lookup"><span data-stu-id="ec779-334">Run the ER format</span></span>

<span data-ttu-id="ec779-335">Gentag trinnene i afsnittet [Køre ER-formatet](#run-format) tidligere i dette emne for at generere en ny performancesporing.</span><span class="sxs-lookup"><span data-stu-id="ec779-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="ec779-336">Bemærk, at webbrowseren kan hente en zip-fil til overførsel.</span><span class="sxs-lookup"><span data-stu-id="ec779-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="ec779-337">Denne fil indeholder performancesporingen i PerfView-format.</span><span class="sxs-lookup"><span data-stu-id="ec779-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="ec779-338">Du kan derefter bruge værktøjet PerfView-performanceanalyse til at analysere detaljerne i ER-formatkørslen.</span><span class="sxs-lookup"><span data-stu-id="ec779-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>
