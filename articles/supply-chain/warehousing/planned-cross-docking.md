---
title: Planlagt direkte levering
description: Dette emne beskriver et avanceret planlagt cross-docking, hvor det lagerantal, der kræves til en ordre, anvises direkte ved modtagelse eller oprettelse til den korrekte dock i forsendelsesområde eller det midlertidige område. Alt restlager fra den indgående kilde sendes til den korrekte lagerplacering via den almindelige læg på lager-proces.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017753"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="1a10a-104">Planlagt cross-docking</span><span class="sxs-lookup"><span data-stu-id="1a10a-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a10a-105">Dette emne beskriver avanceret planlagt cross-docking.</span><span class="sxs-lookup"><span data-stu-id="1a10a-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="1a10a-106">Cross-docking er en lagerproces, hvor det lagerantal, der kræves til en ordre, anvises direkte ved modtagelse eller oprettelse til den korrekte dock i forsendelsesområde eller det midlertidige område.</span><span class="sxs-lookup"><span data-stu-id="1a10a-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="1a10a-107">Alt restlager fra den indgående kilde sendes til den korrekte lagerplacering via den almindelige læg på lager-proces.</span><span class="sxs-lookup"><span data-stu-id="1a10a-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="1a10a-108">Cross-docking giver arbejdere mulighed for at overspringe indgående læg på lager og udgående plukning af lager, der allerede er markeret for en udgående ordre.</span><span class="sxs-lookup"><span data-stu-id="1a10a-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="1a10a-109">Derfor minimeres det antal gange, som lageret berøres med, hvor det er muligt.</span><span class="sxs-lookup"><span data-stu-id="1a10a-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="1a10a-110">Da der desuden sker mindre interaktion med systemet, forhøjes tids- og lagerpladsbesparelserne i forhold til lagerets produktion.</span><span class="sxs-lookup"><span data-stu-id="1a10a-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="1a10a-111">Før cross-docking kan køres, skal brugeren konfigurere en ny cross-docking/skabelon, hvor forsyningskilden og andre sæt af krav til cross-docking er angivet.</span><span class="sxs-lookup"><span data-stu-id="1a10a-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="1a10a-112">Efterhånden som den udgående ordre oprettes, skal linjen markeres i forhold til en indgående ordre, der indeholder den samme vare.</span><span class="sxs-lookup"><span data-stu-id="1a10a-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="1a10a-113">På tidspunktet for modtagelse af indgående ordrer identificerer opsætningen af cross-docking automatisk behovet for cross-docking og opretter bevægelsesarbejdet for den ønskede mængde på basis af opsætningen af lokationsvejledningen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="1a10a-114">Registreringen af lagertransaktioner annulleres **ikke** , når cross-docking annulleres, også selvom indstillingen for denne funktion er aktiveret i parametrene for lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="1a10a-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="1a10a-115">Slå funktionen til planlagt cross-docking til</span><span class="sxs-lookup"><span data-stu-id="1a10a-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="1a10a-116">Før du kan bruge avanceret planlagt cross-docking, skal funktionen være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="1a10a-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="1a10a-117">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="1a10a-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1a10a-118">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="1a10a-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1a10a-119">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="1a10a-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1a10a-120">**Funktionsnavn:** *Planlagt cross docking*</span><span class="sxs-lookup"><span data-stu-id="1a10a-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="1a10a-121">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1a10a-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="1a10a-122">Genoprette lastbogføringsmetoder</span><span class="sxs-lookup"><span data-stu-id="1a10a-122">Regenerate load posting methods</span></span>

<span data-ttu-id="1a10a-123">Planlagt cross-docking implementeres som en lastbogføringsmetode.</span><span class="sxs-lookup"><span data-stu-id="1a10a-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="1a10a-124">Når du har aktiveret funktionen, skal du generere metoderne igen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="1a10a-125">Gå til **Lagerstedsstyring \> Opsætning \> Lastbogføringsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="1a10a-126">Vælg **Genopret metoder** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1a10a-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="1a10a-127">Når genoprettelsen er fuldført, bør du kunne se en metode, der har værdien **planCrossDocking** for *Metodenavn*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="1a10a-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1a10a-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="1a10a-129">Oprette en skabelon for cross-docking</span><span class="sxs-lookup"><span data-stu-id="1a10a-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="1a10a-130">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Skabeloner for cross-docking**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="1a10a-131">Vælg **Ny** i handlingsruden for at oprette en skabelon.</span><span class="sxs-lookup"><span data-stu-id="1a10a-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="1a10a-132">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="1a10a-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="1a10a-133">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a10a-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="1a10a-134">Dette felt definerer den rækkefølge, som skabelonerne evalueres i.</span><span class="sxs-lookup"><span data-stu-id="1a10a-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="1a10a-135">**Id for skabelon for cross-docking:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="1a10a-136">**Beskrivelse:** *Lagersted 51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="1a10a-137">**politik for behovsfrigivelse:** *Før leveringskvittering*</span><span class="sxs-lookup"><span data-stu-id="1a10a-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="1a10a-138">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a10a-139">Opsætningen i oversigtspanelet **Planlægning** bestemmer, hvordan skabelonen fungerer.</span><span class="sxs-lookup"><span data-stu-id="1a10a-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="1a10a-140">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="1a10a-140">Set the following values:</span></span>

    - <span data-ttu-id="1a10a-141">**Efterspørgselskrav:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="1a10a-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="1a10a-142">Dette felt definerer kravene til lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="1a10a-143">Hvis behovet skal være knyttet til leveringen før frigivelsen, skal du vælge *Markering*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="1a10a-144">Hvis behovet skal ordrereserveres i forhold til leveringen, skal du vælge *Ordrereservation*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="1a10a-145">**Finde type:** *Forsendelseslokationer*</span><span class="sxs-lookup"><span data-stu-id="1a10a-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="1a10a-146">I dette felt defineres, om cross-docking-arbejde skal bruge de midlertidige lokationer/læsselokationer fra forsendelsen, eller om de skal bruge lokationsvejledninger til at finde dens egne midlertidige lokationer/læsselokationer.</span><span class="sxs-lookup"><span data-stu-id="1a10a-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="1a10a-147">**Arbejdsskabelon:** Lad feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="1a10a-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="1a10a-148">Dette felt definerer den arbejdsskabelon, der skal bruges, når der oprettes cross-docking-arbejde.</span><span class="sxs-lookup"><span data-stu-id="1a10a-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="1a10a-149">**Valider ved modtagelse af forsyning:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="1a10a-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="1a10a-150">Denne indstilling angiver, om forsyningen skal valideres igen under modtagelsen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="1a10a-151">Hvis denne indstilling er angivet til *Ja* , kontrolleres både det maksimale tidsinterval og udløbsintervallet i dage.</span><span class="sxs-lookup"><span data-stu-id="1a10a-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="1a10a-152">**Valider tidsvindue:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="1a10a-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="1a10a-153">Denne indstilling angiver, om det maksimale tidsvindue skal evalueres, når der er valgt en forsyningskilde.</span><span class="sxs-lookup"><span data-stu-id="1a10a-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="1a10a-154">Hvis denne indstilling er angivet til *Ja* , bliver de felter, der er relateret til de maksimale og minimale tidsvinduer, tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="1a10a-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="1a10a-155">**Maksimalt tidsvindue:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a10a-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="1a10a-156">Dette felt definerer den maksimale periode, der tillades mellem forsyningstilgang og efterspørgselsafgang.</span><span class="sxs-lookup"><span data-stu-id="1a10a-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="1a10a-157">**Enhed for maksimalt tidsvindue:** *Dage*</span><span class="sxs-lookup"><span data-stu-id="1a10a-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="1a10a-158">**Mindste tidsvindue:** *0*</span><span class="sxs-lookup"><span data-stu-id="1a10a-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="1a10a-159">Dette felt definerer den mindste periode, der tillades mellem forsyningstilgang og efterspørgselsafgang.</span><span class="sxs-lookup"><span data-stu-id="1a10a-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="1a10a-160">**Enhed for minimalt tidsvindue:** *Dage*</span><span class="sxs-lookup"><span data-stu-id="1a10a-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="1a10a-161">**Udløbsinterval i dage:** *0*</span><span class="sxs-lookup"><span data-stu-id="1a10a-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="1a10a-162">*FEFO-kriterier (First expiry first out):* Dette felt definerer det maksimale antal dage mellem udløbsdatoen for batchen med den første udløbsdato, der aktuelt findes på lagerstedet, og den batch, der modtages.</span><span class="sxs-lookup"><span data-stu-id="1a10a-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="1a10a-163">I oversigtspanelet **Forsyningskilder** angiver du de typer forsyning, der er gældende for denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="1a10a-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="1a10a-164">Vælg **Ny** , og vælg derefter følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="1a10a-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="1a10a-165">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a10a-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1a10a-166">**Forsyningskilde:** *Indkøbsordre*</span><span class="sxs-lookup"><span data-stu-id="1a10a-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="1a10a-167">Oprette en arbejdsklasse</span><span class="sxs-lookup"><span data-stu-id="1a10a-167">Create a work class</span></span>

1. <span data-ttu-id="1a10a-168">Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="1a10a-169">Vælg **Ny** i handlingsruden for at oprette en arbejdsklasse.</span><span class="sxs-lookup"><span data-stu-id="1a10a-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="1a10a-170">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="1a10a-170">Set the following values:</span></span>

    - <span data-ttu-id="1a10a-171">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="1a10a-172">**Beskrivelse:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="1a10a-173">**Arbejdsordretype:** *Cross-docking*</span><span class="sxs-lookup"><span data-stu-id="1a10a-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="1a10a-174">Oprette en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="1a10a-174">Create a work template</span></span>

1. <span data-ttu-id="1a10a-175">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1a10a-176">Angiv feltet **Arbejdsordretype** til *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="1a10a-177">Gå til handlingsruden, og vælg **Ny** for at føje en linje til fanen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="1a10a-178">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-179">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a10a-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1a10a-180">**Arbejdsskabelon:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="1a10a-181">**Arbejdsskabelonbeskrivelse:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="1a10a-182">Vælg **Gem** for at gøre oversigtspanelet **Arbejdsskabelondetaljer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="1a10a-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="1a10a-183">Gå til oversigtspanelet **Arbejdsskabelondetaljer** , og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="1a10a-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a10a-184">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-185">**Arbejdstype:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="1a10a-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="1a10a-186">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="1a10a-187">Vælg **Ny** for at tilføje en anden linje, og angiv følgende værdier på den:</span><span class="sxs-lookup"><span data-stu-id="1a10a-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="1a10a-188">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="1a10a-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="1a10a-189">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="1a10a-190">Vælg **Gem** , og kontroller, at afkrydsningsfeltet **Gyldig** er markeret for skabelonen *51 Cross Dock*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="1a10a-191">Arbejdsklasse-id'erne for arbejdstyperne *Pluk* og *Læg på lager* skal være ens.</span><span class="sxs-lookup"><span data-stu-id="1a10a-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="1a10a-192">Oprette lokalitetsvejledninger</span><span class="sxs-lookup"><span data-stu-id="1a10a-192">Create location directives</span></span>

1. <span data-ttu-id="1a10a-193">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1a10a-194">I venstre rude skal du angive feltet **Arbejdsordretype** til *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="1a10a-195">I handlingsruden skal du vælge **Ny** og derefter vælge følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="1a10a-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="1a10a-196">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a10a-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="1a10a-197">**Navn:** *51 Cross Dock – læg på lager*</span><span class="sxs-lookup"><span data-stu-id="1a10a-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="1a10a-198">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="1a10a-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="1a10a-199">**Lokation:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a10a-199">**Site:** *5*</span></span>
    - <span data-ttu-id="1a10a-200">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a10a-201">Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="1a10a-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="1a10a-202">Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="1a10a-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a10a-203">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-204">**Fra antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="1a10a-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="1a10a-205">**Til antal:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="1a10a-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="1a10a-206">Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="1a10a-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="1a10a-207">Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="1a10a-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a10a-208">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-209">**Navn:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="1a10a-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="1a10a-210">**Anvendelse af fast lokation:** *Faste og ikke-faste lokationer*</span><span class="sxs-lookup"><span data-stu-id="1a10a-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="1a10a-211">Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig på værktøjslinjen **Handlinger i lokationsvejledning**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="1a10a-212">Vælg **Rediger forespørgsel** for at åbne forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="1a10a-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="1a10a-213">Kontroller, at følgende to linjer er konfigureret under fanen **Område** :</span><span class="sxs-lookup"><span data-stu-id="1a10a-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="1a10a-214">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="1a10a-214">Line 1:</span></span>

        - <span data-ttu-id="1a10a-215">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="1a10a-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="1a10a-216">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="1a10a-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="1a10a-217">**Felt:** *Lagersted*</span><span class="sxs-lookup"><span data-stu-id="1a10a-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="1a10a-218">**Afgrænsning:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="1a10a-219">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="1a10a-219">Line 2:</span></span>

        - <span data-ttu-id="1a10a-220">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="1a10a-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="1a10a-221">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="1a10a-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="1a10a-222">**Felt:** *Lokation*</span><span class="sxs-lookup"><span data-stu-id="1a10a-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="1a10a-223">**Afgrænsning:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="1a10a-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="1a10a-224">Vælg **OK** for at lukke forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="1a10a-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="1a10a-225">Oprette et menupunkt på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="1a10a-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="1a10a-226">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1a10a-227">På listen over menupunkter i ruden til venstre skal du vælge **Læg indkøb på lager**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="1a10a-228">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-228">Select **Edit**.</span></span>
1. <span data-ttu-id="1a10a-229">Gå til oversigtspanelet **Arbejdsklasser** , og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="1a10a-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1a10a-230">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-231">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="1a10a-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="1a10a-232">**Arbejdsordretype:** *Cross-docking*</span><span class="sxs-lookup"><span data-stu-id="1a10a-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="1a10a-233">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="1a10a-234">Scenario</span><span class="sxs-lookup"><span data-stu-id="1a10a-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="1a10a-235">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="1a10a-235">Create a purchase order</span></span>

<span data-ttu-id="1a10a-236">Udfør følgende trin for at oprette en indkøbsordre som en kilde til levering.</span><span class="sxs-lookup"><span data-stu-id="1a10a-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="1a10a-237">Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="1a10a-238">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1a10a-239">Angiv følgende værdier i dialogboksen **Opret indkøbsordre** :</span><span class="sxs-lookup"><span data-stu-id="1a10a-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1a10a-240">**Kreditorkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="1a10a-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="1a10a-241">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a10a-242">Vælg **OK** , og noter ordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="1a10a-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="1a10a-243">Der føjes en ny linje til gitteret i oversigtspanelet **Indkøbsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="1a10a-244">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-245">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a10a-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1a10a-246">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a10a-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="1a10a-247">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="1a10a-247">Create a sales order</span></span>

<span data-ttu-id="1a10a-248">Udfør følgende trin for at oprette en salgsordre som en kilde til efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="1a10a-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="1a10a-249">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1a10a-250">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1a10a-251">Angiv følgende værdier i dialogboksen **Opret salgsordre** :</span><span class="sxs-lookup"><span data-stu-id="1a10a-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1a10a-252">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="1a10a-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="1a10a-253">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="1a10a-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="1a10a-254">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-254">Select **OK**.</span></span>
1. <span data-ttu-id="1a10a-255">Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1a10a-256">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="1a10a-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a10a-257">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a10a-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1a10a-258">**Antal:** *3*</span><span class="sxs-lookup"><span data-stu-id="1a10a-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="1a10a-259">Oprette planlagt cross-docking</span><span class="sxs-lookup"><span data-stu-id="1a10a-259">Create planned cross-docking</span></span>

<span data-ttu-id="1a10a-260">Udfør følgende trin for at oprette planlagt cross-docking fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="1a10a-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="1a10a-261">På siden **Salgsordredetaljer** for den salgsordre, du netop har oprettet, skal du i handlingsruden vælge **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Frigiv til lagersted**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="1a10a-262">Handlingen Frigiv til lagersted opretter en forsendelses- og lastlinje for salgsordrelinjen og forsøger at fordele lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="1a10a-263">Du får en orienterende meddelelse.</span><span class="sxs-lookup"><span data-stu-id="1a10a-263">You receive an informational message.</span></span> <span data-ttu-id="1a10a-264">Du får også vist følgende advarselsmeddelelse: "Der blev ikke oprettet noget arbejde for bølge XXXX.</span><span class="sxs-lookup"><span data-stu-id="1a10a-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="1a10a-265">Du kan finde flere oplysninger i logfilen over historik for oprettelse af arbejde."</span><span class="sxs-lookup"><span data-stu-id="1a10a-265">See the work creation history log for details."</span></span> <span data-ttu-id="1a10a-266">Denne funktionsmåde forventes, fordi der ikke er nogen lagerbeholdning på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="1a10a-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="1a10a-267">Gå til oversigtspanelet **Salgsordrelinjer** , og vælg **Forsendelsesoplysninger** i menuen **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="1a10a-268">Siden **Forsendelsesoplysninger** vises og viser den forsendelse, der er oprettet for salgsorden.</span><span class="sxs-lookup"><span data-stu-id="1a10a-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="1a10a-269">I oversigtspanelet **Lastlinjer** skal du bemærke, at feltet **Planlagt antal til cross-docking** er angivet til *3*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="1a10a-270">Da der ikke var en tilgængelig lagerbeholdning på lagerstedet, men der vil blive oprettet en gyldig forsyningskilde inden for det tidsvindue, der er defineret i skabelonen til cross-docking, blev antallet for cross-docking angivet.</span><span class="sxs-lookup"><span data-stu-id="1a10a-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="1a10a-271">I oversigtspanelet **Lastlinjer** skal du vælge **Planlagt cross-docking** for at få vist detaljerne om den cross-docking, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="1a10a-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="1a10a-272">Behandle cross-docking</span><span class="sxs-lookup"><span data-stu-id="1a10a-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="1a10a-273">Købsordre, der modtages på Warehouse Mobile App</span><span class="sxs-lookup"><span data-stu-id="1a10a-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="1a10a-274">Systemet vil modtage antallet på 5 fra indkøbsordren til modtagelseslokationen og oprette to x arbejde.</span><span class="sxs-lookup"><span data-stu-id="1a10a-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="1a10a-275">Det første arbejds-id, der oprettes, har værdien **Cross-docking** for *Arbejdsordretype* og er knyttet til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="1a10a-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="1a10a-276">Det har antallet 3 og sendes til den endelige afsendelseslokation, så det kan leveres med det samme.</span><span class="sxs-lookup"><span data-stu-id="1a10a-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="1a10a-277">Det andet arbejds-id, der oprettes, har værdien **Indkøbsordrer** for *Arbejdsordretype* og er knyttet til indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="1a10a-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="1a10a-278">Den har det resterende antal på 2, der ikke blev cross-docked, og som sendes til opbevaring med læg på lager.</span><span class="sxs-lookup"><span data-stu-id="1a10a-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="1a10a-279">Log på mobilenheden som en bruger på lagerstedet *51*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="1a10a-280">Gå til **indgående \> Købsmodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="1a10a-281">Angiv dit indkøbsordrenummer i feltet **IO-num**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="1a10a-282">Angiv **5** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="1a10a-283">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-283">Select **OK**.</span></span>
1. <span data-ttu-id="1a10a-284">På næste side skal du angive feltet **Vare** til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="1a10a-285">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-285">Select **OK**.</span></span>
1. <span data-ttu-id="1a10a-286">På næste side skal du bekræfte værdierne for **IO-num** , **Vare** og **Antal** ved at vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="1a10a-287">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="1a10a-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="1a10a-288">Vælg **Annuller** for at afslutte.</span><span class="sxs-lookup"><span data-stu-id="1a10a-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="1a10a-289">Læg på lager til cross-docking og masse</span><span class="sxs-lookup"><span data-stu-id="1a10a-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="1a10a-290">I øjeblikket har begge arbejds-id'er samme målnummerplade.</span><span class="sxs-lookup"><span data-stu-id="1a10a-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="1a10a-291">Hvis du vil udføre de næste trin, skal du hente arbejds-id'et og målnummerplade-id'et.</span><span class="sxs-lookup"><span data-stu-id="1a10a-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="1a10a-292">Du kan få disse oplysninger fra arbejdsdetaljerne om indkøbsordrelinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="1a10a-293">Du kan også gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer** og filtrere efter arbejde, hvor værdien **Lagersted** er *51*.</span><span class="sxs-lookup"><span data-stu-id="1a10a-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="1a10a-294">På mobilenheden skal du gå til **Indgående \> Læg køb på lager** og angive målnummerpladen fra arbejdet.</span><span class="sxs-lookup"><span data-stu-id="1a10a-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="1a10a-295">I feltet **Id** skal du angive målnummerplade-id'et fra arbejdsdetaljerne.</span><span class="sxs-lookup"><span data-stu-id="1a10a-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="1a10a-296">Siden til plukning til cross-docking viser pluklokationen ( *RECV* ), målnummerpladen ( *nummerplade* ), varen ( *A0001* ) og antallet ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="1a10a-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="1a10a-297">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-297">Select **OK**.</span></span>
1. <span data-ttu-id="1a10a-298">I feltet **Mål-NP** skal du angive en målnummerplade for nummerplade-id'et, der skal lægges på lager (cross-docked) på forsendelseslokationen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="1a10a-299">Du kan vælge et hvilket som helst nummerplade-id efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="1a10a-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="1a10a-300">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-300">Select **OK**.</span></span>
1. <span data-ttu-id="1a10a-301">På den næste side skal du i feltet **Id** angive målnummerplade-id'et.</span><span class="sxs-lookup"><span data-stu-id="1a10a-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="1a10a-302">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-302">Select **OK**.</span></span>
1. <span data-ttu-id="1a10a-303">Bekræft arbejdet til plukning af det resterende antal på 2, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="1a10a-304">På næste side skal du vælge **Udfør** for at afslutte plukprocessen og begynde læg på lager-processen.</span><span class="sxs-lookup"><span data-stu-id="1a10a-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="1a10a-305">Mobilappen indeholder lokationen og nummerpladen, hvor varen skal lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="1a10a-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="1a10a-306">Bekræft **Læg på lager** ved masseopbevaring ved at vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="1a10a-307">På den næste side skal du bekræfte **Læg på lager** for cross-docking ved at vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a10a-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="1a10a-308">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="1a10a-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="1a10a-309">Vælg **Annuller** for at afslutte.</span><span class="sxs-lookup"><span data-stu-id="1a10a-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="1a10a-310">I følgende illustration vises, hvordan det færdige arbejde til cross-docking kan blive vist i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1a10a-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="1a10a-311">![Arbejde med cross-docking udført](media/PlannedCrossDockingWork.png "Arbejde med cross-docking udført")</span><span class="sxs-lookup"><span data-stu-id="1a10a-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
