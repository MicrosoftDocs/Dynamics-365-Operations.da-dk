---
title: Oprette arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 76306fb31e7e5297e6a5d64b97b5bd09b64349ee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500568"
---
# <a name="creating-work-orders"></a><span data-ttu-id="c5d21-103">Oprette arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="c5d21-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5d21-104">Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer til dem.</span><span class="sxs-lookup"><span data-stu-id="c5d21-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="c5d21-105">Du kan udføre dette trin ved at bruge en af vedligeholdelsestidsplanerne.</span><span class="sxs-lookup"><span data-stu-id="c5d21-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="c5d21-106">De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="c5d21-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="c5d21-107">Referencetype</span><span class="sxs-lookup"><span data-stu-id="c5d21-107">Reference type</span></span> | <span data-ttu-id="c5d21-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c5d21-108">Description</span></span> |
|---|---|
| <span data-ttu-id="c5d21-109">Vedligeholdelsesplaner</span><span class="sxs-lookup"><span data-stu-id="c5d21-109">Maintenance plans</span></span> | <span data-ttu-id="c5d21-110">Præventivee vedligeholdelsesjob, der er baseret på vedligeholdelsesplantypen *Tid* eller *Tæller*.</span><span class="sxs-lookup"><span data-stu-id="c5d21-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="c5d21-111">Vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="c5d21-111">Maintenance rounds</span></span> | <span data-ttu-id="c5d21-112">Præventive vedligeholdelsesjob, der indeholder flere aktiver, der kræver en lignende form for vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="c5d21-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="c5d21-113">Vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="c5d21-113">Maintenance request</span></span> | <span data-ttu-id="c5d21-114">En manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv.</span><span class="sxs-lookup"><span data-stu-id="c5d21-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="c5d21-115">Denne anmodning kan konverteres til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="c5d21-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="c5d21-116">Oprette arbejdsordrer på baggrund af din vedligeholdelsestidsplan</span><span class="sxs-lookup"><span data-stu-id="c5d21-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="c5d21-117">Hvis du vil oprette arbejdsordrer, der er baseret på din vedligeholdelsestidsplan, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="c5d21-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="c5d21-118">Åbn en af følgende sider, afhængigt af hvordan du vil vælge tidsplanselementer til dine arbejdsordrer:</span><span class="sxs-lookup"><span data-stu-id="c5d21-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="c5d21-119">Hele vedligeholdelsestidsplanen (**Aktivstyring \> Administration af tidsplaner \> Hele vedligeholdelsestidsplanen**)</span><span class="sxs-lookup"><span data-stu-id="c5d21-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="c5d21-120">Åbne vedligeholdelsestidsplanslinjer (**Aktivstyring \> Administration af tidsplaner \> Åbn vedligeholdelsestidsplanslinjer**)</span><span class="sxs-lookup"><span data-stu-id="c5d21-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="c5d21-121">Åbn vedligeholdelsestidsplanspuljer (**Aktivstyring \> Administration af tidsplaner \> Åbn vedligeholdelsestidsplanspuljer**)</span><span class="sxs-lookup"><span data-stu-id="c5d21-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="c5d21-122">I gitteret skal du markere afkrydsningsfeltet for alle planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for.</span><span class="sxs-lookup"><span data-stu-id="c5d21-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="c5d21-123">Vælg **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5d21-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="c5d21-124">Dialogboksen **Opret arbejdsordrer** vises.</span><span class="sxs-lookup"><span data-stu-id="c5d21-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="c5d21-125">Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer**.</span><span class="sxs-lookup"><span data-stu-id="c5d21-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Dialogboksen Opret arbejdsordrer](media/18-preventive-maintenance.png)

1. <span data-ttu-id="c5d21-127">Angiv det antal arbejdsordrer, der skal oprettes, under **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="c5d21-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="c5d21-128">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="c5d21-128">Select one of the following options:</span></span>

    - <span data-ttu-id="c5d21-129">**Én arbejdsordre pr. linje** – Opret én arbejdsordre pr. vedligeholdelsesplanlinje.</span><span class="sxs-lookup"><span data-stu-id="c5d21-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="c5d21-130">**én arbejdsordre pr.** – Opret arbejdsordrer, der er grupperet i henhold til indstillingerne for de andre indstillinger, der bliver tilgængelige, når du vælger denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="c5d21-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="c5d21-131">Vælg den arbejdsordretype, der skal bruges til alle de arbejdsordrer, du opretter, i feltet **Arbejdsordretype**.</span><span class="sxs-lookup"><span data-stu-id="c5d21-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="c5d21-132">Vælg **OK** for at oprette arbejdsordrerne i overensstemmelse med indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="c5d21-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="c5d21-133">Gruppere arbejdsordrelinjer, som oprettes automatisk, mens vedligeholdelsesplanen køres</span><span class="sxs-lookup"><span data-stu-id="c5d21-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="c5d21-134">Denne funktion giver dig mulighed for at definere regler for gruppering af arbejdsordrelinjer under en enkelt arbejdsordre, når systemet er konfigureret til at generere arbejdsordrer automatisk på baggrund af en vedligeholdelsesplan.</span><span class="sxs-lookup"><span data-stu-id="c5d21-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="c5d21-135">Tidligere kunne automatisk genererede arbejdsordrer kun indeholde én linje.</span><span class="sxs-lookup"><span data-stu-id="c5d21-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="c5d21-136">Men du kan nu gruppere arbejdsordrer efter f.eks. aktiv, aktivtype eller arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="c5d21-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="c5d21-137">(Manuelt genererede arbejdsordrer kan allerede være grupperet på denne måde som beskrevet i forrige afsnit i dette emne).</span><span class="sxs-lookup"><span data-stu-id="c5d21-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="c5d21-138">Aktivere gruppering for automatisk genererede arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="c5d21-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="c5d21-139">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="c5d21-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c5d21-140">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="c5d21-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c5d21-141">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c5d21-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c5d21-142">**Modul:** *Aktivadministration*</span><span class="sxs-lookup"><span data-stu-id="c5d21-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="c5d21-143">**Funktionsnavn:** *(forhåndsversion) Anvende regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres*</span><span class="sxs-lookup"><span data-stu-id="c5d21-143">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="c5d21-144">Konfigurere gruppering for automatisk genererede arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="c5d21-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="c5d21-145">Følg disse trin for at konfigurere gruppering for automatisk genererede arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="c5d21-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="c5d21-146">Gå til **Styring af aktiver \> Opsætning \> Forebyggende vedligeholdelse \> Vedligeholdelsesplaner**.</span><span class="sxs-lookup"><span data-stu-id="c5d21-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="c5d21-147">Benyt følgende fremgangsmåde for hver plan, hvor du vil generere grupperede arbejdsordrer:</span><span class="sxs-lookup"><span data-stu-id="c5d21-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="c5d21-148">Vælg planen i listeruden.</span><span class="sxs-lookup"><span data-stu-id="c5d21-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="c5d21-149">Kontrollér, at afkrydsningsfeltet **Opret automatisk** er markeret på alle linjer i oversigtspanelet **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="c5d21-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="c5d21-150">Gå til **Styring af aktiver \> Periodisk \> Forebyggende vedligeholdelse \> Planlæg vedligeholdelsesplaner**.</span><span class="sxs-lookup"><span data-stu-id="c5d21-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="c5d21-151">I dialogboksen **Planlæg vedligeholdelsesplaner** i sektionen **Periode** skal du angive tidshorisont for planen (hvor langt der skal kigges frem, når der skal søges efter planlagte vedligeholdelsesjob, der skal genereres arbejde for).</span><span class="sxs-lookup"><span data-stu-id="c5d21-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="c5d21-152">Angiv indstillingen **Opret arbejdsordre automatisk fra tidsplan** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="c5d21-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="c5d21-153">Vælg en af følgende indstillinger i sektionen **Arbejdsordre**:</span><span class="sxs-lookup"><span data-stu-id="c5d21-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="c5d21-154">**Én arbejdsordre pr. linje** – Opret én arbejdsordre pr. vedligeholdelsesplanlinje.</span><span class="sxs-lookup"><span data-stu-id="c5d21-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="c5d21-155">(Denne indstilling giver den samme funktionalitet, som er tilgængelig, når funktionen *Anvend regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres* er deaktiveret).</span><span class="sxs-lookup"><span data-stu-id="c5d21-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="c5d21-156">**én arbejdsordre pr.** – Opret arbejdsordrer, der er grupperet i henhold til indstillingerne for de andre indstillinger, der bliver tilgængelige, når du vælger denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="c5d21-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="c5d21-157">Hvis du ønsker, at indstillingerne skal anvendes, når du kun kører nogle af dine vedligeholdelsesplaner, skal du tilføje filtre efter behov i oversigtspanelet **Poster, der skal indgå** på samme måde som ved andre batchjob i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c5d21-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="c5d21-158">I oversigtspanelet **Kør i baggrunden** skal du konfigurere batch- og planlægningsindstillinger efter behov på samme måde som ved andre batchjob i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c5d21-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="c5d21-159">Vælg **OK** for at køre og/eller planlægge de valgte vedligeholdelsesplaner.</span><span class="sxs-lookup"><span data-stu-id="c5d21-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]