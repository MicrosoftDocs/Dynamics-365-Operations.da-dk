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
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131787"
---
# <a name="creating-work-orders"></a><span data-ttu-id="d28b3-103">Oprette arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="d28b3-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d28b3-104">Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer til dem.</span><span class="sxs-lookup"><span data-stu-id="d28b3-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="d28b3-105">Du kan udføre dette trin ved at bruge en af vedligeholdelsestidsplanerne.</span><span class="sxs-lookup"><span data-stu-id="d28b3-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="d28b3-106">De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="d28b3-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="d28b3-107">Referencetype</span><span class="sxs-lookup"><span data-stu-id="d28b3-107">Reference type</span></span> | <span data-ttu-id="d28b3-108">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="d28b3-108">Description</span></span> |
|---|---|
| <span data-ttu-id="d28b3-109">Vedligeholdelsesplaner</span><span class="sxs-lookup"><span data-stu-id="d28b3-109">Maintenance plans</span></span> | <span data-ttu-id="d28b3-110">Præventivee vedligeholdelsesjob, der er baseret på vedligeholdelsesplantypen *Tid* eller *Tæller*.</span><span class="sxs-lookup"><span data-stu-id="d28b3-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="d28b3-111">Vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="d28b3-111">Maintenance rounds</span></span> | <span data-ttu-id="d28b3-112">Præventive vedligeholdelsesjob, der indeholder flere aktiver, der kræver en lignende form for vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="d28b3-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="d28b3-113">Vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="d28b3-113">Maintenance request</span></span> | <span data-ttu-id="d28b3-114">En manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv.</span><span class="sxs-lookup"><span data-stu-id="d28b3-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="d28b3-115">Denne anmodning kan konverteres til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="d28b3-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="d28b3-116">Oprette arbejdsordrer på baggrund af din vedligeholdelsestidsplan</span><span class="sxs-lookup"><span data-stu-id="d28b3-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="d28b3-117">Hvis du vil oprette arbejdsordrer, der er baseret på din vedligeholdelsestidsplan, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="d28b3-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="d28b3-118">Åbn en af følgende sider, afhængigt af hvordan du vil vælge tidsplanselementer til dine arbejdsordrer:</span><span class="sxs-lookup"><span data-stu-id="d28b3-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="d28b3-119">Hele vedligeholdelsestidsplanen (**Aktivstyring \> Administration af tidsplaner \> Hele vedligeholdelsestidsplanen**)</span><span class="sxs-lookup"><span data-stu-id="d28b3-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="d28b3-120">Åbne vedligeholdelsestidsplanslinjer (**Aktivstyring \> Administration af tidsplaner \> Åbn vedligeholdelsestidsplanslinjer**)</span><span class="sxs-lookup"><span data-stu-id="d28b3-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="d28b3-121">Åbn vedligeholdelsestidsplanspuljer (**Aktivstyring \> Administration af tidsplaner \> Åbn vedligeholdelsestidsplanspuljer**)</span><span class="sxs-lookup"><span data-stu-id="d28b3-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="d28b3-122">I gitteret skal du markere afkrydsningsfeltet for alle planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for.</span><span class="sxs-lookup"><span data-stu-id="d28b3-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="d28b3-123">Vælg **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d28b3-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="d28b3-124">Dialogboksen **Opret arbejdsordrer** vises.</span><span class="sxs-lookup"><span data-stu-id="d28b3-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="d28b3-125">Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer**.</span><span class="sxs-lookup"><span data-stu-id="d28b3-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Dialogboksen Opret arbejdsordrer](media/18-preventive-maintenance.png)

1. <span data-ttu-id="d28b3-127">Angiv det antal arbejdsordrer, der skal oprettes, under **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="d28b3-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="d28b3-128">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="d28b3-128">Select one of the following options:</span></span>

    - <span data-ttu-id="d28b3-129">**Én arbejdsordre pr. linje** – Opret én arbejdsordre pr. vedligeholdelsesplanlinje.</span><span class="sxs-lookup"><span data-stu-id="d28b3-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="d28b3-130">**én arbejdsordre pr.** – Opret arbejdsordrer, der er grupperet i henhold til indstillingerne for de andre indstillinger, der bliver tilgængelige, når du vælger denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="d28b3-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="d28b3-131">Vælg den arbejdsordretype, der skal bruges til alle de arbejdsordrer, du opretter, i feltet **Arbejdsordretype**.</span><span class="sxs-lookup"><span data-stu-id="d28b3-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="d28b3-132">Vælg **OK** for at oprette arbejdsordrerne i overensstemmelse med indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="d28b3-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="d28b3-133">Gruppere arbejdsordrelinjer, som oprettes automatisk, mens vedligeholdelsesplanen køres</span><span class="sxs-lookup"><span data-stu-id="d28b3-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d28b3-134">De funktioner, der er anført i dette afsnit, er tilgængelige som en del af en privat forhåndsversion.</span><span class="sxs-lookup"><span data-stu-id="d28b3-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="d28b3-135">Indholdet og funktionaliteten kan blive ændret.</span><span class="sxs-lookup"><span data-stu-id="d28b3-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="d28b3-136">Du kan finde flere oplysninger om prøveversioner i [Ofte stillede spørgsmål om One Version-tjenesteopdateringer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="d28b3-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="d28b3-137">Denne funktion giver dig mulighed for at definere regler for gruppering af arbejdsordrelinjer under en enkelt arbejdsordre, når systemet er konfigureret til at generere arbejdsordrer automatisk på baggrund af en vedligeholdelsesplan.</span><span class="sxs-lookup"><span data-stu-id="d28b3-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="d28b3-138">Tidligere kunne automatisk genererede arbejdsordrer kun indeholde én linje.</span><span class="sxs-lookup"><span data-stu-id="d28b3-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="d28b3-139">Men du kan nu gruppere arbejdsordrer efter f.eks. aktiv, aktivtype eller arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="d28b3-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="d28b3-140">(Manuelt genererede arbejdsordrer kan allerede være grupperet på denne måde som beskrevet i forrige afsnit i dette emne).</span><span class="sxs-lookup"><span data-stu-id="d28b3-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="d28b3-141">Aktivere gruppering for automatisk genererede arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="d28b3-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="d28b3-142">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="d28b3-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d28b3-143">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="d28b3-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="d28b3-144">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="d28b3-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d28b3-145">**Modul:** *Aktivadministration*</span><span class="sxs-lookup"><span data-stu-id="d28b3-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="d28b3-146">**Funktionsnavn:** *(forhåndsversion) Anvende regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres*</span><span class="sxs-lookup"><span data-stu-id="d28b3-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="d28b3-147">Konfigurere gruppering for automatisk genererede arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="d28b3-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="d28b3-148">Følg disse trin for at konfigurere gruppering for automatisk genererede arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="d28b3-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="d28b3-149">Gå til **Styring af aktiver \> Opsætning \> Forebyggende vedligeholdelse \> Vedligeholdelsesplaner**.</span><span class="sxs-lookup"><span data-stu-id="d28b3-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="d28b3-150">Benyt følgende fremgangsmåde for hver plan, hvor du vil generere grupperede arbejdsordrer:</span><span class="sxs-lookup"><span data-stu-id="d28b3-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="d28b3-151">Vælg planen i listeruden.</span><span class="sxs-lookup"><span data-stu-id="d28b3-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="d28b3-152">Kontrollér, at afkrydsningsfeltet **Opret automatisk** er markeret på alle linjer i oversigtspanelet **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="d28b3-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="d28b3-153">Gå til **Styring af aktiver \> Periodisk \> Forebyggende vedligeholdelse \> Planlæg vedligeholdelsesplaner**.</span><span class="sxs-lookup"><span data-stu-id="d28b3-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="d28b3-154">I dialogboksen **Planlæg vedligeholdelsesplaner** i sektionen **Periode** skal du angive tidshorisont for planen (hvor langt der skal kigges frem, når der skal søges efter planlagte vedligeholdelsesjob, der skal genereres arbejde for).</span><span class="sxs-lookup"><span data-stu-id="d28b3-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="d28b3-155">Angiv indstillingen **Opret arbejdsordre automatisk fra tidsplan** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d28b3-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="d28b3-156">Vælg en af følgende indstillinger i sektionen **Arbejdsordre**:</span><span class="sxs-lookup"><span data-stu-id="d28b3-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="d28b3-157">**Én arbejdsordre pr. linje** – Opret én arbejdsordre pr. vedligeholdelsesplanlinje.</span><span class="sxs-lookup"><span data-stu-id="d28b3-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="d28b3-158">(Denne indstilling giver den samme funktionalitet, som er tilgængelig, når funktionen *Anvend regler for gruppering af arbejdsordrer, mens en vedligeholdelsesplan køres* er deaktiveret).</span><span class="sxs-lookup"><span data-stu-id="d28b3-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="d28b3-159">**én arbejdsordre pr.** – Opret arbejdsordrer, der er grupperet i henhold til indstillingerne for de andre indstillinger, der bliver tilgængelige, når du vælger denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="d28b3-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="d28b3-160">Hvis du ønsker, at indstillingerne skal anvendes, når du kun kører nogle af dine vedligeholdelsesplaner, skal du tilføje filtre efter behov i oversigtspanelet **Poster, der skal indgå** på samme måde som ved andre batchjob i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d28b3-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="d28b3-161">I oversigtspanelet **Kør i baggrunden** skal du konfigurere batch- og planlægningsindstillinger efter behov på samme måde som ved andre batchjob i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d28b3-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="d28b3-162">Vælg **OK** for at køre og/eller planlægge de valgte vedligeholdelsesplaner.</span><span class="sxs-lookup"><span data-stu-id="d28b3-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
