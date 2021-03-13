---
title: Manuelt oprettede arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer manuelt i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c787dbc9889139df76b9b102deb18fce567e382
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017862"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="7eca5-103">Manuelt oprettede arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="7eca5-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="7eca5-104">Du kan oprette arbejdsordre manuelt på to måder:</span><span class="sxs-lookup"><span data-stu-id="7eca5-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="7eca5-105">På siden **Alle arbejdsordrer** eller **Aktive arbejdsordrer**</span><span class="sxs-lookup"><span data-stu-id="7eca5-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="7eca5-106">På siden **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**</span><span class="sxs-lookup"><span data-stu-id="7eca5-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="7eca5-107">Opret arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="7eca5-107">Create work order</span></span>

1. <span data-ttu-id="7eca5-108">Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="7eca5-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-109">Select **New**.</span></span>

3. <span data-ttu-id="7eca5-110">I dialogboksen **Opret arbejdsordre** skal du vælge en arbejdsordretype i feltet **Arbejdsordretype**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="7eca5-111">Vælg evt. en **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="7eca5-112">Vælg aktivet i feltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="7eca5-113">Når du vælger et aktiv, kan der være tre faner tilgængelige i rullemenuen **Aktiv**:</span><span class="sxs-lookup"><span data-stu-id="7eca5-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="7eca5-114">**Aktive aktiver** - Denne fane indeholder en liste over alle aktiver med status som "Aktiv" for aktivets livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="7eca5-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="7eca5-115">**Aktiv visning** - Denne fane har en trævisning af arbejdssteder og de aktiver, der er installeret på dem.</span><span class="sxs-lookup"><span data-stu-id="7eca5-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="7eca5-116">**Mine aktiver** - Denne fane indeholder aktiver, der er relateret til de arbejdssteder, som du (den arbejder, der er logget på systemet), kan blive allokeret til.</span><span class="sxs-lookup"><span data-stu-id="7eca5-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="7eca5-117">Du kan finde oplysninger om opsætningen under [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md). Hvis der ikke er konfigureret nogen arbejdssteder i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md), er fanen **Mine aktiver** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="7eca5-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="7eca5-118">Vælg en vedligeholdelsesjobtype for arbejdsordren i feltet **Vedligeholdelsesjobtype**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="7eca5-119">Vælg om nødvendigt **Vedligeholdelsesjobtypevariant** og **Fag**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="7eca5-120">Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="7eca5-121">Vælg **Forventet startdato** og **Forventet slutdato** i de relaterede felter.</span><span class="sxs-lookup"><span data-stu-id="7eca5-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="7eca5-122">Klik på **OK** for at oprette arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="7eca5-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="7eca5-123">På siden **Alle arbejdsordrer** kan du redigere arbejdsordren, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="7eca5-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="7eca5-124">Vær opmærksom på følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="7eca5-124">Note the following points:</span></span>

- <span data-ttu-id="7eca5-125">I detaljevisningen på listesiden **Alle arbejdsordrer** kan du føje flere aktiver til en arbejdsordre ved at tilføje linjer i oversigtspanelet **Vedligeholdelsesjob for arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="7eca5-126">I et aktiv kan du kun vælge de vedligeholdelsesjobtyper, der er defineret i den aktivtype, der er valgt på aktivet.</span><span class="sxs-lookup"><span data-stu-id="7eca5-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="7eca5-127">Hvis du ændrer et aktivserviceniveau eller en aktivkritikalitet, efter at du har brugt aktivet på en arbejdsordre, opdateres serviceniveauet eller kritikaliteten ikke på arbejdsordren i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="7eca5-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="7eca5-128">Du kan finde flere oplysninger om serviceniveauer og kritikaliteter under [Serviceniveauer for aktiv](../setup-for-objects/object-priorities.md) og [Kritikalitetstyper for aktiver](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="7eca5-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="7eca5-129">Kritikaliteten på en arbejdsordre genberegnes, hver gang et arbejdsordrejob føjes til eller slettes fra arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="7eca5-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="7eca5-130">I detaljevisningen **Alle arbejdsordrer** > fanen **Hoved** > oversigtspanelet **Tidsplan** kan du vælge en ansvarlig vedligeholdelsesarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder i feltet **Ansvarlig gruppe** eller **Ansvarlig**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="7eca5-131">Disse indstillinger kan ændres, mens arbejdsordren er aktiv.</span><span class="sxs-lookup"><span data-stu-id="7eca5-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="7eca5-132">De kan f.eks. ændres, når livscyklustilstanden for arbejdsordren ændres.</span><span class="sxs-lookup"><span data-stu-id="7eca5-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="7eca5-133">Det automatiske valg, der foretages under oprettelsen af en arbejdsordre, baseres på opsætningen på siden **Ansvarlige vedligeholdelsesarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="7eca5-134">Hvis du tilføjer eller fjerner arbejdsordrejob, efter at du har oprettet en arbejdsordre, og hvis felterne **Ansvarlig gruppe** og **Ansvarlig** er tomme, når du opdaterer arbejdsordren, søger funktionen Styring af aktiver efter et en ansvarlig vedligeholdelsesarbejdergruppe eller en ansvarlig vedligeholdelsesarbejder på opsætningssiden.</span><span class="sxs-lookup"><span data-stu-id="7eca5-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="7eca5-135">Hvis feltet **Ansvarlig gruppe** eller **Ansvarlig** allerede er udfyldt, når du opdaterer arbejdsordren, foretages der ingen ændringer.</span><span class="sxs-lookup"><span data-stu-id="7eca5-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="7eca5-136">Du finder flere oplysninger om ansvarlige vedligeholdelsesarbejdere og arbejdergrupper i [Ansvarlige vedligeholdelsesarbejdere](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="7eca5-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="7eca5-137">På siden [Vedligeholdelsesstatus](../controlling-and-reporting/maintenance-status.md) kan du foretage en beregning for at få en oversigt over arbejdsbyrden for indgående og fuldførte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="7eca5-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="7eca5-138">Du kan bruge felterne **Breddegrad** og **Længdegrad** i oversigtspanelet **Linjedetaljer** i den detaljerede visning af siden **Alle arbejdsordrer** til at tilføje geografiske koordinater for det aktiv, der er valgt på arbejdsordrejobbet.</span><span class="sxs-lookup"><span data-stu-id="7eca5-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="7eca5-139">Opret relateret arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="7eca5-139">Create related work order</span></span>

<span data-ttu-id="7eca5-140">Du kan oprette en arbejdsordre, der er relateret til en eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="7eca5-141">Dette er nyttigt, hvis du f.eks. vil arbejde med primære og sekundære arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="7eca5-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="7eca5-142">En ny arbejdsordre er baseret på et arbejdsordrejob fra en eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="7eca5-143">Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="7eca5-144">Vælg den arbejdsordre, du vil oprette en relateret arbejdsordre for.</span><span class="sxs-lookup"><span data-stu-id="7eca5-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="7eca5-145">Vælg **Relateret arbejdsordre** i gruppen **Ny** under fanen **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7eca5-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="7eca5-146">I dialogboksen **Opret relateret arbejdsordre** skal du vælge det arbejdsordrejob, som du vil oprette en relateret arbejdsordre for, i feltet **Arbejdsordrejob**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="7eca5-147">Vælg en vedligeholdelsesjobtype i feltet **Vedligeholdelsesjobtype**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="7eca5-148">I felterne **Vedligeholdelsesjobtypevariant** og **Fag** skal du vælge den variant og det fag, der er relateret til vedligeholdelsesjobtypen.</span><span class="sxs-lookup"><span data-stu-id="7eca5-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="7eca5-149">Hvis denne arbejdsordre er den første relaterede arbejdsordre, der er oprettet for den valgte arbejdsordre, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="7eca5-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="7eca5-150">Vælg indstillingen **Ny arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="7eca5-151">I feltet **Arbejdsordretype** skal du vælge en arbejdsordretype.</span><span class="sxs-lookup"><span data-stu-id="7eca5-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="7eca5-152">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="7eca5-153">Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="7eca5-154">Vælg start- og slutdatoerne i felterne **Forventet start** og **Forventet afslutning**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="7eca5-155">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-155">Select **OK**.</span></span> <span data-ttu-id="7eca5-156">Den nye relaterede arbejdsordre vises på listesiden **Alle arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="7eca5-157">Hvis den arbejdsordre, du opretter denne relaterede arbejdsordre for, allerede har relaterede arbejdsordrer, skal du udføre følgende trin for at føje et nyt arbejdsordrejob til en eksisterende relateret arbejdsordre:</span><span class="sxs-lookup"><span data-stu-id="7eca5-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="7eca5-158">Vælg indstillingen **Føj til relateret arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="7eca5-159">Vælg den relaterede arbejdsordre, som du vil føje et nyt arbejdsordrejob til, i feltet **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="7eca5-160">Hvis det er nødvendigt, kan du ændre serviceniveauet for arbejdsordren i feltet **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="7eca5-161">Ret start- og slutdatoerne eftr behov i felterne **Forventet start** og **Forventet afslutning**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="7eca5-162">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-162">Select **OK**.</span></span> <span data-ttu-id="7eca5-163">Arbejdsordrejobbet føjes til den eksisterende relaterede arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="7eca5-164">I illustrationen herunder vises et eksempel på dialogboksen **Opret relateret arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Figur 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="7eca5-166">Hvis du har oprettet en relateret arbejdsordremaske i **Parametre til aktivstyring** > **Arbejdsordrer**-fanen > feltet **Relateret arbejdsordremaske**, oprettes arbejdsordre-id'er i overensstemmelse med maskeopsætningen.</span><span class="sxs-lookup"><span data-stu-id="7eca5-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="7eca5-167">Hvis der ikke er konfigureret nogen tilknyttet arbejdsordremaske, bruges det næste tilgængelige arbejdsordre-id til relaterede arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="7eca5-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="7eca5-168">Kopiere en arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="7eca5-168">Copy a work order</span></span>

<span data-ttu-id="7eca5-169">Du kan hurtigt at oprette en ny arbejdsordre ud fra en eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="7eca5-170">Denne måde at arbejde med arbejdsordrer på er ikke den samme, som når du opretter arbejdsordrer på basis af [vedligeholdelsesplaner](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="7eca5-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="7eca5-171">Den er nyttig, hvis du f.eks. har en arbejdsordre, der indeholder mange arbejdsordrejob, og de forskellige job skal udføres på forskellige aktiver med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="7eca5-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="7eca5-172">Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="7eca5-173">Vælg den arbejdsordre, du vil kopiere indhold fra.</span><span class="sxs-lookup"><span data-stu-id="7eca5-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="7eca5-174">Vælg **Kopiér arbejdsordre** i gruppen **Ny** under fanen **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7eca5-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="7eca5-175">Arbejdsordreopsætningen fra den valgte arbejdsordre vises.</span><span class="sxs-lookup"><span data-stu-id="7eca5-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="7eca5-176">Hvis det er nødvendigt, kan du redigere nogle af felterne.</span><span class="sxs-lookup"><span data-stu-id="7eca5-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="7eca5-177">Vælg **OK** for at oprette den nye arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="7eca5-178">På siden **Alle arbejdsordrer** kan du redigere arbejdsordren, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="7eca5-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="7eca5-179">Når den nye arbejdsordre oprettes, kopieres nogle oplysninger direkte fra den eksisterende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="7eca5-180">Oplysninger om budgetter, værktøjer, vedligeholdelsestjeklister, arbejdssted, adresser og planlægning kopieres ikke.</span><span class="sxs-lookup"><span data-stu-id="7eca5-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="7eca5-181">De er i stedet initialiseret fra den aktuelle opsætning i aktivstyring.</span><span class="sxs-lookup"><span data-stu-id="7eca5-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="7eca5-182">Hvis disse oplysninger derfor er ændret mellem det tidspunkt, hvor den første arbejdsordre blev oprettet, og det tidspunkt, hvor du oprettede en kopi af arbejdsordren, medtages ændringerne i den nye arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7eca5-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="7eca5-183">Eksempler er ændringer i prognoser og opdaterede vedligeholdelsestjeklister.</span><span class="sxs-lookup"><span data-stu-id="7eca5-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="7eca5-184">I illustrationen nedenfor vises et eksempel på dialogboksen **Kopiér arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Figur 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="7eca5-186">Oprette en arbejdsordre baseret på en vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="7eca5-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="7eca5-187">Vælg **Styring af aktiver** > **Almindeligt** > **Vedligeholdelsesanmodninger** > **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="7eca5-188">Vælg de vedligeholdelsesanmodninger, du vil oprette en arbejdsordre for, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="7eca5-189">Vælg **Arbejdsordre** i gruppen **Ny** under fanen **Vedligeholdelsesanmodning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7eca5-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="7eca5-190">Udfyld felterne i dialogboksen **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="7eca5-191">Hvis der er valgt en vedligeholdelsesjobtype i vedligeholdelsesanmodningen, kan du vælge en anden type vedligeholdelsesjob, hvis det er nødvendigt, når du opretter arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="7eca5-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="7eca5-192">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-192">Select **OK**.</span></span> <span data-ttu-id="7eca5-193">Meddelelsen fortæller dig, at salgsordren er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="7eca5-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="7eca5-194">Hvis du vil se de arbejdsordrer, der er knyttet til en vedligeholdelsesanmodning, skal du vælge vedligeholdelsesanmodningen på listen **Alle vedligeholdelsesanmodninger** eller **Aktive vedligeholdelsesanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="7eca5-195">Vælg derefter **Arbejdsordrer** i gruppen **Vis** under fanen **Vedligeholdelsesanmodning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7eca5-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="7eca5-196">I illustrationen nedenfor vises et eksempel på dialogboksen **Opret arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="7eca5-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Figur 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="7eca5-198">Du kan også oprette arbejdsordrer automatisk ved at planlægge vedligeholdelsesplanjob eller ved at konfigurere "Automatisk oprettelse" af [vedligeholdelsesplaner](../preventive-and-reactive-maintenance/maintenance-plans.md) eller [vedligeholdelsesrunder](../preventive-and-reactive-maintenance/maintenance-rounds.md) for et aktiv.</span><span class="sxs-lookup"><span data-stu-id="7eca5-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="7eca5-199">Arbejdsordrer, der er oprettet ud fra vedligeholdelsesanmodninger på siden **Hele vedligeholdelsestidsplanen**, har de vedligeholdelsesjobtyper, der er valgt i vedligeholdelsesanmodningerne.</span><span class="sxs-lookup"><span data-stu-id="7eca5-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

