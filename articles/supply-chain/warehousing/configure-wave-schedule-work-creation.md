---
title: Planlægge oprettelse af arbejde under bølge
description: I dette emne beskrives, hvordan du kan konfigurere og bruge behandlingsmetoden til planlægning af arbejdsoprettelse i bølge.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501216"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="f4069-103">Planlægge oprettelse af arbejde under bølge</span><span class="sxs-lookup"><span data-stu-id="f4069-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f4069-104">Brug funktionen *Planlæg oprettelse af arbejde* som en del af din bølgeproces for at øge gennemløbet af bølgearbejde ved at lade systemet oprette arbejde via parallel behandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="f4069-105">Når funktionaliteten er aktiveret, oprettes der automatisk planlagt arbejde, som systemet i den sidste ende behandler for at oprette faktisk arbejde.</span><span class="sxs-lookup"><span data-stu-id="f4069-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="f4069-106">Hvis antallet af bølgelastlinjer når en foruddefineret grænseværdi, opretter systemet det faktiske arbejde hurtigere ved at anvende parallel asynkron behandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="f4069-107">Aktivere funktionen Planlæg oprettelse af arbejde</span><span class="sxs-lookup"><span data-stu-id="f4069-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="f4069-108">Aktivere funktionen i funktionsstyring</span><span class="sxs-lookup"><span data-stu-id="f4069-108">Enable the feature in feature management</span></span>

<span data-ttu-id="f4069-109">Før du kan bruge funktionen *Planlæg oprettelse af arbejde*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="f4069-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="f4069-110">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="f4069-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f4069-111">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="f4069-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f4069-112">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="f4069-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f4069-113">**Funktionsnavn:** *Planlæg oprettelse af arbejde*</span><span class="sxs-lookup"><span data-stu-id="f4069-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="f4069-114">Funktionen *Blokering af arbejde i hele organisationen* skal være aktiveret, før du kan aktivere *Planlæg oprettelse af arbejde*.</span><span class="sxs-lookup"><span data-stu-id="f4069-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="f4069-115">Aktivere batchafvikling af bølger manuelt</span><span class="sxs-lookup"><span data-stu-id="f4069-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="f4069-116">Hvis du vil have fordel af en parallel asynkron metode til oprettelse af lagerstedsarbejde, skal din bølgeproces køres i batch.</span><span class="sxs-lookup"><span data-stu-id="f4069-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="f4069-117">Sådan konfigurerer du dette:</span><span class="sxs-lookup"><span data-stu-id="f4069-117">To set this up:</span></span>

1. <span data-ttu-id="f4069-118">Gå til **Lokationsstyring \> Opsætning \> Parametre til lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="f4069-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="f4069-119">Angiv **Udfør behandling af bølger i batch** til **Ja** under fanen *Generelt*.</span><span class="sxs-lookup"><span data-stu-id="f4069-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="f4069-120">Du kan også vælge en dedikeret **Batchgruppe til behandling af bølger** for at forhindre, at batchkøbehandlingen køres på samme tid som andre processer.</span><span class="sxs-lookup"><span data-stu-id="f4069-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="f4069-121">Indstil **Vent på lås (ms.)**, som gælder, når systemet behandler flere bølger samtidig.</span><span class="sxs-lookup"><span data-stu-id="f4069-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="f4069-122">Ved de fleste større bølgeprocesser anbefales en værdi af *60000*.</span><span class="sxs-lookup"><span data-stu-id="f4069-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="f4069-123">Aktivere den nye metode til bølgetrin manuelt for eksisterende bølgeskabeloner</span><span class="sxs-lookup"><span data-stu-id="f4069-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="f4069-124">Start med at oprette den nye metode til bølgetrin, og aktivér den til parallel asynkron opgavebehandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="f4069-125">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="f4069-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="f4069-126">Vælg  **Genopret metoder**, og bemærk, at *WSScheduleWorkCreationUroStepMethod* er føjet til listen over metoder til behandling af bølger, du kan bruge i dine forsendelsesbølgeskabeloner.</span><span class="sxs-lookup"><span data-stu-id="f4069-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="f4069-127">Vælg posten med **Metodenavn** *WSScheduleWorkCreationHodStepMethod*, og vælg **Opgavekonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f4069-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="f4069-128">Gå til handlingsruden, og vælg **Ny** for at føje en ny række til gitteret med følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f4069-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="f4069-129">**Lagersted** – Vælg det lagersted, som du vil bruge til at planlægge behandling af oprettelse af arbejde.</span><span class="sxs-lookup"><span data-stu-id="f4069-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="f4069-130">**Maksimalt antal batchopgaver** – Angiv et maksimalt antal batchopgaver.</span><span class="sxs-lookup"><span data-stu-id="f4069-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="f4069-131">I de fleste tilfælde skal denne værdi være i intervallet fra 8-16, men du anbefales at eksperimentere med den optimale indstilling baseret på dine scenarier.</span><span class="sxs-lookup"><span data-stu-id="f4069-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="f4069-132">**Batchgruppe til bølgebehandling** – Vælg en dedikeret batchgruppe til behandling af bølger for at optimere batchkøbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="f4069-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="f4069-133">Nu er du klar til at opdatere en eksisterende bølgeskabelon (eller oprette en ny) til at bruge metoden *Planlæg oprettelse af arbejde* til bølgebehandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="f4069-134">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="f4069-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="f4069-135">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f4069-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="f4069-136">I listeruden skal du vælge den bølgeskabelon, som du vil opdatere (hvis du tester med demodata, kan du bruge *24 Standard for forsendelse*).</span><span class="sxs-lookup"><span data-stu-id="f4069-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="f4069-137">Udvid oversigtspanelet **Metoder**, og vælg rækken med **Navn** *Planlæg oprettelse af arbejde* i gitteret **Resterende metoder**.</span><span class="sxs-lookup"><span data-stu-id="f4069-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="f4069-138">Vælg pilen, der peger på kolonnen **Valgte metoder**, så den valgte række flyttes til den pågældende kolonne.</span><span class="sxs-lookup"><span data-stu-id="f4069-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="f4069-139">(Du kan kun have én valgt metode ad gangen, der bruger enten *WSScheduleWorkCreationHodStepMethod* eller *createWork*, så den eksisterende række med **Metodenavn** *createWork* automatisk flyttes til gitteret **Resterende metoder**).</span><span class="sxs-lookup"><span data-stu-id="f4069-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="f4069-140">Angive tærskeldata for behandling af bølgeopgave</span><span class="sxs-lookup"><span data-stu-id="f4069-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="f4069-141">Systemet opretter standardtærskeldata for behandling af bølgeopgaver, første gang en bølgeproces køres ved hjælp af opgavebaseret behandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="f4069-142">Dataene bruges til at styre, hvornår behandling af bølger vil køre asynkront og være opgavebaseret, hvilket gør det muligt at behandle og oprette arbejde parallelt.</span><span class="sxs-lookup"><span data-stu-id="f4069-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="f4069-143">Standarddataene vil først bruge en grænseværdi på 15 for minimumantallet af belastningslinjer (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="f4069-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="f4069-144">Det betyder, at når systemet behandler en bølge med mere end 15 belastningslinjer, vil systemet bruge asynkron opgavebehandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="f4069-145">Du kan manuelt indsætte/opdatere disse data i tabellen **WHSWaveTaskProcessingThresholdParameters** i testmiljøet, men hvis du har brug for at ændre denne indstilling i et produktionsmiljø, skal du kontakte Microsoft Support for at anmode om opdateringen.</span><span class="sxs-lookup"><span data-stu-id="f4069-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="f4069-146">Arbejde med funktionen</span><span class="sxs-lookup"><span data-stu-id="f4069-146">Work with the feature</span></span>

<span data-ttu-id="f4069-147">Når funktionen *Planlæg oprettelse af arbejde* er aktiveret, opretter bølgebehandling det planlagte arbejde, som senere vil blive brugt af den nye arbejdsoprettelsesproces.</span><span class="sxs-lookup"><span data-stu-id="f4069-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="f4069-148">Under oprettelse af arbejde blokeres arbejdet ved hjælp af funktionen *Blokering af arbejde i hele organisationen*.</span><span class="sxs-lookup"><span data-stu-id="f4069-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="f4069-149">Følgende rutediagram viser, hvordan planlagt arbejde oprettes under bølgebehandling.</span><span class="sxs-lookup"><span data-stu-id="f4069-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Planlæg arbejdsoprettelse](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="f4069-151">Planlagt arbejde</span><span class="sxs-lookup"><span data-stu-id="f4069-151">Planned work</span></span>

<span data-ttu-id="f4069-152">På siden **Detaljer om planlagt arbejde** (**Lokationsstyring \> Arbejde \> Detaljer om planlagt arbejde**) vises oplysninger om det planlagte arbejde, der oprindeligt blev oprettet under behandling af bølger.</span><span class="sxs-lookup"><span data-stu-id="f4069-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="f4069-153">Følgende værdier af **Processtatus** er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="f4069-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="f4069-154">**Sat i kø** – Det planlagte arbejde venter på at blive brugt til at oprette arbejde.</span><span class="sxs-lookup"><span data-stu-id="f4069-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="f4069-155">**Fuldført** – Det planlagte arbejde er brugt til at oprette arbejde.</span><span class="sxs-lookup"><span data-stu-id="f4069-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="f4069-156">**Mislykkedes** – Bølgebehandlingen er mislykket.</span><span class="sxs-lookup"><span data-stu-id="f4069-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="f4069-157">Bemærk, at det planlagte arbejde kan være i tilstanden **Mislykkedes** med eller uden relateret faktisk arbejde.</span><span class="sxs-lookup"><span data-stu-id="f4069-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="f4069-158">Når den faktiske arbejdsoprettelsesproces mislykkes, forbliver det faktiske arbejde med status *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="f4069-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="f4069-159">Batchjob for processen til oprettelse af arbejde</span><span class="sxs-lookup"><span data-stu-id="f4069-159">Batch job for the work creation process</span></span>

<span data-ttu-id="f4069-160">Hvis du vil have vist batchjobbene til behandling af bølger, skal du vælge **Batchjob** i handlingsruden på siden **Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="f4069-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="f4069-161">Herfra kan du få vist alle oplysninger om batchopgaven for hvert enkelt batchjob-id.</span><span class="sxs-lookup"><span data-stu-id="f4069-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]