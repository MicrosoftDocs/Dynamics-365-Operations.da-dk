---
title: Planlagt direkte levering
description: Dette emne beskriver et avanceret planlagt cross-docking, hvor det lagerantal, der kræves til en ordre, anvises direkte ved modtagelse eller oprettelse til den korrekte dock i forsendelsesområde eller det midlertidige område. Alt restlager fra den indgående kilde sendes til den korrekte lagerplacering via den almindelige læg på lager-proces.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911242"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="bff5d-104">Planlagt cross-docking</span><span class="sxs-lookup"><span data-stu-id="bff5d-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bff5d-105">Dette emne beskriver avanceret planlagt cross-docking.</span><span class="sxs-lookup"><span data-stu-id="bff5d-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="bff5d-106">Cross-docking er en lagerproces, hvor det lagerantal, der kræves til en ordre, anvises direkte ved modtagelse eller oprettelse til den korrekte dock i forsendelsesområde eller det midlertidige område.</span><span class="sxs-lookup"><span data-stu-id="bff5d-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="bff5d-107">Alt restlager fra den indgående kilde sendes til den korrekte lagerplacering via den almindelige læg på lager-proces.</span><span class="sxs-lookup"><span data-stu-id="bff5d-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="bff5d-108">Cross-docking giver arbejdere mulighed for at overspringe indgående læg på lager og udgående plukning af lager, der allerede er markeret for en udgående ordre.</span><span class="sxs-lookup"><span data-stu-id="bff5d-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="bff5d-109">Derfor minimeres det antal gange, som lageret berøres med, hvor det er muligt.</span><span class="sxs-lookup"><span data-stu-id="bff5d-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="bff5d-110">Da der desuden sker mindre interaktion med systemet, forhøjes tids- og lagerpladsbesparelserne i forhold til lagerets produktion.</span><span class="sxs-lookup"><span data-stu-id="bff5d-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="bff5d-111">Før cross-docking kan køres, skal du konfigurere en ny cross-docking/skabelon, hvor forsyningskilden og andre sæt af krav til cross-docking er angivet.</span><span class="sxs-lookup"><span data-stu-id="bff5d-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="bff5d-112">Efterhånden som den udgående ordre oprettes, skal linjen markeres i forhold til en indgående ordre, der indeholder den samme vare.</span><span class="sxs-lookup"><span data-stu-id="bff5d-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="bff5d-113">Du kan vælge feltet med vejledningskode i skabelonen for cross-docking, på samme måde som du konfigurerer genopfyldnings- og indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="bff5d-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="bff5d-114">På tidspunktet for modtagelse af indgående ordrer identificerer opsætningen af cross-docking automatisk behovet for cross-docking og opretter bevægelsesarbejdet for den ønskede mængde på basis af opsætningen af lokationsvejledningen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="bff5d-115">Registreringen af lagertransaktioner annulleres *ikke*, når cross-docking annulleres, også selvom indstillingen for denne funktion er aktiveret i parametrene for lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="bff5d-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="bff5d-116">Slå funktionerne til planlagt cross-docking til</span><span class="sxs-lookup"><span data-stu-id="bff5d-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="bff5d-117">Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funktioner i denne rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="bff5d-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="bff5d-118">*Planlagt direkte levering*</span><span class="sxs-lookup"><span data-stu-id="bff5d-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="bff5d-119">*Skabeloner til cross-docking med lokationsvejledninger*</span><span class="sxs-lookup"><span data-stu-id="bff5d-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="bff5d-120">Denne funktion gør det muligt at angive feltet **Vejledningskode** i skabelonen til cross-docking, ligesom du konfigurerer genopfyldningsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="bff5d-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="bff5d-121">Hvis du aktiverer denne funktion, kan du ikke føje en vejledningskode til linjerne i arbejdsskabelonen til cross-docking for den endelige *Læg*-linje.</span><span class="sxs-lookup"><span data-stu-id="bff5d-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="bff5d-122">Derved sikres, at den endelige læg-placering kan bestemmes under oprettelsen af arbejdet, før du overvejer arbejdsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="bff5d-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="bff5d-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bff5d-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="bff5d-124">Genoprette lastbogføringsmetoder</span><span class="sxs-lookup"><span data-stu-id="bff5d-124">Regenerate load posting methods</span></span>

<span data-ttu-id="bff5d-125">Planlagt cross-docking implementeres som en lastbogføringsmetode.</span><span class="sxs-lookup"><span data-stu-id="bff5d-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="bff5d-126">Når du har aktiveret funktionen, skal du generere metoderne igen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="bff5d-127">Gå til **Lagerstedsstyring \> Opsætning \> Lastbogføringsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="bff5d-128">Vælg **Genopret metoder** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bff5d-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="bff5d-129">Når genoprettelsen er fuldført, bør du kunne se en metode, der har værdien **planCrossDocking** for *Metodenavn*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="bff5d-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bff5d-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="bff5d-131">Oprette en skabelon for cross-docking</span><span class="sxs-lookup"><span data-stu-id="bff5d-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="bff5d-132">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Skabeloner for cross-docking**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="bff5d-133">Vælg **Ny** i handlingsruden for at oprette en skabelon.</span><span class="sxs-lookup"><span data-stu-id="bff5d-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="bff5d-134">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="bff5d-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="bff5d-135">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="bff5d-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="bff5d-136">Dette felt definerer den rækkefølge, som skabelonerne evalueres i.</span><span class="sxs-lookup"><span data-stu-id="bff5d-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="bff5d-137">**Id for skabelon for cross-docking:** *51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="bff5d-138">**Beskrivelse:** *Lagersted 51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="bff5d-139">**politik for behovsfrigivelse:** *Før leveringskvittering*</span><span class="sxs-lookup"><span data-stu-id="bff5d-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="bff5d-140">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bff5d-141">Opsætningen i oversigtspanelet **Planlægning** bestemmer, hvordan skabelonen fungerer.</span><span class="sxs-lookup"><span data-stu-id="bff5d-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="bff5d-142">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="bff5d-142">Set the following values:</span></span>

    - <span data-ttu-id="bff5d-143">**Efterspørgselskrav:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="bff5d-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="bff5d-144">Dette felt definerer kravene til lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="bff5d-145">Hvis behovet skal være knyttet til leveringen før frigivelsen, skal du vælge *Markering*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="bff5d-146">Hvis behovet skal ordrereserveres i forhold til leveringen, skal du vælge *Ordrereservation*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="bff5d-147">**Finde type:** *Forsendelseslokationer*</span><span class="sxs-lookup"><span data-stu-id="bff5d-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="bff5d-148">I dette felt defineres, om cross-docking-arbejde skal bruge de midlertidige lokationer/læsselokationer fra forsendelsen, eller om de skal bruge lokationsvejledninger til at finde dens egne midlertidige lokationer/læsselokationer.</span><span class="sxs-lookup"><span data-stu-id="bff5d-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="bff5d-149">**Arbejdsskabelon:** Lad feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="bff5d-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="bff5d-150">Dette felt definerer den arbejdsskabelon, der skal bruges, når der oprettes cross-docking-arbejde.</span><span class="sxs-lookup"><span data-stu-id="bff5d-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="bff5d-151">**Valider ved modtagelse af forsyning:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="bff5d-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="bff5d-152">Denne indstilling angiver, om forsyningen skal valideres igen under modtagelsen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="bff5d-153">Hvis denne indstilling er angivet til *Ja*, kontrolleres både det maksimale tidsinterval og udløbsintervallet i dage.</span><span class="sxs-lookup"><span data-stu-id="bff5d-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="bff5d-154">**Vejledningskode:** Lad feltet være tomt</span><span class="sxs-lookup"><span data-stu-id="bff5d-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="bff5d-155">Denne indstilling aktiveres med funktionen *Skabeloner til cross-docking med lokationsvejledninger*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="bff5d-156">Systemet bruger lokationsvejledninger som en hjælp til at bestemme, hvilken lokation cross-docking-lager skal flyttes til.</span><span class="sxs-lookup"><span data-stu-id="bff5d-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="bff5d-157">Du kan definere den ved at tildele en vejledningskode til hver relevante cross-docking-skabelon.</span><span class="sxs-lookup"><span data-stu-id="bff5d-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="bff5d-158">Hvis der er angivet en vejledningskode, når arbejde genereres, søger systemet i lokationsvejledninger ved hjælp af vejledningskoden.</span><span class="sxs-lookup"><span data-stu-id="bff5d-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="bff5d-159">På denne måde kan du begrænse lokationsvejledninger, der bruges til en bestemt cross-docking-skabelon.</span><span class="sxs-lookup"><span data-stu-id="bff5d-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="bff5d-160">**Valider tidsvindue:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="bff5d-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="bff5d-161">Denne indstilling angiver, om det maksimale tidsvindue skal evalueres, når der er valgt en forsyningskilde.</span><span class="sxs-lookup"><span data-stu-id="bff5d-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="bff5d-162">Hvis denne indstilling er angivet til *Ja*, bliver de felter, der er relateret til de maksimale og minimale tidsvinduer, tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="bff5d-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="bff5d-163">**Maksimalt tidsvindue:** *5*</span><span class="sxs-lookup"><span data-stu-id="bff5d-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="bff5d-164">Dette felt definerer den maksimale periode, der tillades mellem forsyningstilgang og efterspørgselsafgang.</span><span class="sxs-lookup"><span data-stu-id="bff5d-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="bff5d-165">**Enhed for maksimalt tidsvindue:** *Dage*</span><span class="sxs-lookup"><span data-stu-id="bff5d-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="bff5d-166">**Mindste tidsvindue:** *0*</span><span class="sxs-lookup"><span data-stu-id="bff5d-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="bff5d-167">Dette felt definerer den mindste periode, der tillades mellem forsyningstilgang og efterspørgselsafgang.</span><span class="sxs-lookup"><span data-stu-id="bff5d-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="bff5d-168">**Enhed for minimalt tidsvindue:** *Dage*</span><span class="sxs-lookup"><span data-stu-id="bff5d-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="bff5d-169">**Udløbsinterval i dage:** *0*</span><span class="sxs-lookup"><span data-stu-id="bff5d-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="bff5d-170">*FEFO-kriterier (First expiry first out):* Dette felt definerer det maksimale antal dage mellem udløbsdatoen for batchen med den første udløbsdato, der aktuelt findes på lagerstedet, og den batch, der modtages.</span><span class="sxs-lookup"><span data-stu-id="bff5d-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="bff5d-171">I oversigtspanelet **Forsyningskilder** angiver du de typer forsyning, der er gældende for denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="bff5d-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="bff5d-172">Vælg **Ny**, og vælg derefter følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="bff5d-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="bff5d-173">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="bff5d-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="bff5d-174">**Forsyningskilde:** *Indkøbsordre*</span><span class="sxs-lookup"><span data-stu-id="bff5d-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="bff5d-175">Oprette en arbejdsklasse</span><span class="sxs-lookup"><span data-stu-id="bff5d-175">Create a work class</span></span>

1. <span data-ttu-id="bff5d-176">Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="bff5d-177">Vælg **Ny** i handlingsruden for at oprette en arbejdsklasse.</span><span class="sxs-lookup"><span data-stu-id="bff5d-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="bff5d-178">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="bff5d-178">Set the following values:</span></span>

    - <span data-ttu-id="bff5d-179">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="bff5d-180">**Beskrivelse:** *Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="bff5d-181">**Arbejdsordretype:** *Cross-docking*</span><span class="sxs-lookup"><span data-stu-id="bff5d-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="bff5d-182">Oprette en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="bff5d-182">Create a work template</span></span>

1. <span data-ttu-id="bff5d-183">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="bff5d-184">Angiv feltet **Arbejdsordretype** til *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="bff5d-185">Gå til handlingsruden, og vælg **Ny** for at føje en linje til fanen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="bff5d-186">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-187">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="bff5d-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="bff5d-188">**Arbejdsskabelon:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="bff5d-189">**Arbejdsskabelonbeskrivelse:** *51 Cross Dock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="bff5d-190">Vælg **Gem** for at gøre oversigtspanelet **Arbejdsskabelondetaljer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="bff5d-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="bff5d-191">Gå til oversigtspanelet **Arbejdsskabelondetaljer**, og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="bff5d-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bff5d-192">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-193">**Arbejdstype:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="bff5d-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="bff5d-194">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="bff5d-195">Vælg **Ny** for at tilføje en anden linje, og angiv følgende værdier på den:</span><span class="sxs-lookup"><span data-stu-id="bff5d-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="bff5d-196">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="bff5d-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bff5d-197">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="bff5d-198">Vælg **Gem**, og kontroller, at afkrydsningsfeltet **Gyldig** er markeret for skabelonen *51 Cross Dock*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="bff5d-199">Arbejdsklasse-id'erne for arbejdstyperne *Pluk* og *Læg på lager* skal være ens.</span><span class="sxs-lookup"><span data-stu-id="bff5d-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="bff5d-200">Oprette lokalitetsvejledninger</span><span class="sxs-lookup"><span data-stu-id="bff5d-200">Create location directives</span></span>

1. <span data-ttu-id="bff5d-201">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="bff5d-202">I venstre rude skal du angive feltet **Arbejdsordretype** til *Cross-docking*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="bff5d-203">I handlingsruden skal du vælge **Ny** og derefter vælge følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="bff5d-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="bff5d-204">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="bff5d-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="bff5d-205">**Navn:** *51 Cross Dock – læg på lager*</span><span class="sxs-lookup"><span data-stu-id="bff5d-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="bff5d-206">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="bff5d-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="bff5d-207">**Lokation:** *5*</span><span class="sxs-lookup"><span data-stu-id="bff5d-207">**Site:** *5*</span></span>
    - <span data-ttu-id="bff5d-208">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bff5d-209">Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="bff5d-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="bff5d-210">Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="bff5d-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bff5d-211">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-212">**Fra antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="bff5d-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="bff5d-213">**Til antal:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="bff5d-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="bff5d-214">Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="bff5d-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="bff5d-215">Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="bff5d-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bff5d-216">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-217">**Navn:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="bff5d-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="bff5d-218">**Anvendelse af fast lokation:** *Faste og ikke-faste lokationer*</span><span class="sxs-lookup"><span data-stu-id="bff5d-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="bff5d-219">Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig på værktøjslinjen **Handlinger i lokationsvejledning**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="bff5d-220">Vælg **Rediger forespørgsel** for at åbne forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="bff5d-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="bff5d-221">Kontroller, at følgende to linjer er konfigureret under fanen **Område**:</span><span class="sxs-lookup"><span data-stu-id="bff5d-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="bff5d-222">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="bff5d-222">Line 1:</span></span>

        - <span data-ttu-id="bff5d-223">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="bff5d-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="bff5d-224">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="bff5d-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="bff5d-225">**Felt:** *Lagersted*</span><span class="sxs-lookup"><span data-stu-id="bff5d-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="bff5d-226">**Afgrænsning:** *51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="bff5d-227">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="bff5d-227">Line 2:</span></span>

        - <span data-ttu-id="bff5d-228">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="bff5d-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="bff5d-229">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="bff5d-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="bff5d-230">**Felt:** *Lokation*</span><span class="sxs-lookup"><span data-stu-id="bff5d-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="bff5d-231">**Afgrænsning:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="bff5d-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="bff5d-232">Vælg **OK** for at lukke forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="bff5d-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="bff5d-233">Oprette et menupunkt på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="bff5d-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="bff5d-234">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bff5d-235">På listen over menupunkter i ruden til venstre skal du vælge **Læg indkøb på lager**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="bff5d-236">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-236">Select **Edit**.</span></span>
1. <span data-ttu-id="bff5d-237">Gå til oversigtspanelet **Arbejdsklasser**, og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="bff5d-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="bff5d-238">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-239">**Arbejdsklasse-id:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="bff5d-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="bff5d-240">**Arbejdsordretype:** *Cross-docking*</span><span class="sxs-lookup"><span data-stu-id="bff5d-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="bff5d-241">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="bff5d-242">Scenario</span><span class="sxs-lookup"><span data-stu-id="bff5d-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="bff5d-243">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="bff5d-243">Create a purchase order</span></span>

<span data-ttu-id="bff5d-244">Udfør følgende trin for at oprette en indkøbsordre som en kilde til levering.</span><span class="sxs-lookup"><span data-stu-id="bff5d-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="bff5d-245">Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="bff5d-246">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bff5d-247">Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:</span><span class="sxs-lookup"><span data-stu-id="bff5d-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bff5d-248">**Kreditorkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="bff5d-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="bff5d-249">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bff5d-250">Vælg **OK**, og noter ordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="bff5d-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="bff5d-251">Der føjes en ny linje til gitteret i oversigtspanelet **Indkøbsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="bff5d-252">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-253">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="bff5d-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="bff5d-254">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="bff5d-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="bff5d-255">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="bff5d-255">Create a sales order</span></span>

<span data-ttu-id="bff5d-256">Udfør følgende trin for at oprette en salgsordre som en kilde til efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="bff5d-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="bff5d-257">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="bff5d-258">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="bff5d-259">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="bff5d-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="bff5d-260">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="bff5d-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="bff5d-261">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="bff5d-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="bff5d-262">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-262">Select **OK**.</span></span>
1. <span data-ttu-id="bff5d-263">Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="bff5d-264">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="bff5d-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="bff5d-265">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="bff5d-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="bff5d-266">**Antal:** *3*</span><span class="sxs-lookup"><span data-stu-id="bff5d-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="bff5d-267">Oprette planlagt cross-docking</span><span class="sxs-lookup"><span data-stu-id="bff5d-267">Create planned cross-docking</span></span>

<span data-ttu-id="bff5d-268">Udfør følgende trin for at oprette planlagt cross-docking fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="bff5d-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="bff5d-269">På siden **Salgsordredetaljer** for den salgsordre, du netop har oprettet, skal du i handlingsruden vælge **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Frigiv til lagersted**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="bff5d-270">Handlingen Frigiv til lagersted opretter en forsendelses- og lastlinje for salgsordrelinjen og forsøger at fordele lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="bff5d-271">Du får en orienterende meddelelse.</span><span class="sxs-lookup"><span data-stu-id="bff5d-271">You receive an informational message.</span></span> <span data-ttu-id="bff5d-272">Du får også vist følgende advarselsmeddelelse: "Der blev ikke oprettet noget arbejde for bølge XXXX.</span><span class="sxs-lookup"><span data-stu-id="bff5d-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="bff5d-273">Du kan finde flere oplysninger i logfilen over historik for oprettelse af arbejde."</span><span class="sxs-lookup"><span data-stu-id="bff5d-273">See the work creation history log for details."</span></span> <span data-ttu-id="bff5d-274">Denne funktionsmåde forventes, fordi der ikke er nogen lagerbeholdning på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="bff5d-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="bff5d-275">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Forsendelsesoplysninger** i menuen **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="bff5d-276">Siden **Forsendelsesoplysninger** vises og viser den forsendelse, der er oprettet for salgsorden.</span><span class="sxs-lookup"><span data-stu-id="bff5d-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="bff5d-277">I oversigtspanelet **Lastlinjer** skal du bemærke, at feltet **Planlagt antal til cross-docking** er angivet til *3*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="bff5d-278">Da der ikke var en tilgængelig lagerbeholdning på lagerstedet, men der vil blive oprettet en gyldig forsyningskilde inden for det tidsvindue, der er defineret i skabelonen til cross-docking, blev antallet for cross-docking angivet.</span><span class="sxs-lookup"><span data-stu-id="bff5d-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="bff5d-279">I oversigtspanelet **Lastlinjer** skal du vælge **Planlagt cross-docking** for at få vist detaljerne om den cross-docking, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="bff5d-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="bff5d-280">Behandle cross-docking</span><span class="sxs-lookup"><span data-stu-id="bff5d-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="bff5d-281">Købsordre, der modtages på Warehouse Mobile App</span><span class="sxs-lookup"><span data-stu-id="bff5d-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="bff5d-282">Systemet vil modtage antallet på 5 fra indkøbsordren til modtagelseslokationen og oprette to x arbejde.</span><span class="sxs-lookup"><span data-stu-id="bff5d-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="bff5d-283">Det første arbejds-id, der oprettes, har værdien **Cross-docking** for *Arbejdsordretype* og er knyttet til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="bff5d-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="bff5d-284">Det har antallet 3 og sendes til den endelige afsendelseslokation, så det kan leveres med det samme.</span><span class="sxs-lookup"><span data-stu-id="bff5d-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="bff5d-285">Det andet arbejds-id, der oprettes, har værdien **Indkøbsordrer** for *Arbejdsordretype* og er knyttet til indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="bff5d-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="bff5d-286">Den har det resterende antal på 2, der ikke blev cross-docked, og som sendes til opbevaring med læg på lager.</span><span class="sxs-lookup"><span data-stu-id="bff5d-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="bff5d-287">Log på mobilenheden som en bruger på lagerstedet *51*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="bff5d-288">Gå til **indgående \> Købsmodtagelse**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="bff5d-289">Angiv dit indkøbsordrenummer i feltet **IO-num**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="bff5d-290">Angiv **5** i feltet *Antal*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="bff5d-291">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-291">Select **OK**.</span></span>
1. <span data-ttu-id="bff5d-292">På næste side skal du angive feltet **Vare** til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="bff5d-293">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-293">Select **OK**.</span></span>
1. <span data-ttu-id="bff5d-294">På næste side skal du bekræfte værdierne for **IO-num**, **Vare** og **Antal** ved at vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="bff5d-295">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="bff5d-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="bff5d-296">Vælg **Annuller** for at afslutte.</span><span class="sxs-lookup"><span data-stu-id="bff5d-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="bff5d-297">Læg på lager til cross-docking og masse</span><span class="sxs-lookup"><span data-stu-id="bff5d-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="bff5d-298">I øjeblikket har begge arbejds-id'er samme målnummerplade.</span><span class="sxs-lookup"><span data-stu-id="bff5d-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="bff5d-299">Hvis du vil udføre de næste trin, skal du hente arbejds-id'et og målnummerplade-id'et.</span><span class="sxs-lookup"><span data-stu-id="bff5d-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="bff5d-300">Du kan få disse oplysninger fra arbejdsdetaljerne om indkøbsordrelinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="bff5d-301">Du kan også gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer** og filtrere efter arbejde, hvor værdien **Lagersted** er *51*.</span><span class="sxs-lookup"><span data-stu-id="bff5d-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="bff5d-302">På mobilenheden skal du gå til **Indgående \> Læg køb på lager** og angive målnummerpladen fra arbejdet.</span><span class="sxs-lookup"><span data-stu-id="bff5d-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="bff5d-303">I feltet **Id** skal du angive målnummerplade-id'et fra arbejdsdetaljerne.</span><span class="sxs-lookup"><span data-stu-id="bff5d-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="bff5d-304">Siden til plukning til cross-docking viser pluklokationen (*RECV*), målnummerpladen (*nummerplade*), varen (*A0001*) og antallet (*3*).</span><span class="sxs-lookup"><span data-stu-id="bff5d-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="bff5d-305">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-305">Select **OK**.</span></span>
1. <span data-ttu-id="bff5d-306">I feltet **Mål-NP** skal du angive en målnummerplade for nummerplade-id'et, der skal lægges på lager (cross-docked) på forsendelseslokationen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="bff5d-307">Du kan vælge et hvilket som helst nummerplade-id efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="bff5d-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="bff5d-308">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-308">Select **OK**.</span></span>
1. <span data-ttu-id="bff5d-309">På den næste side skal du i feltet **Id** angive målnummerplade-id'et.</span><span class="sxs-lookup"><span data-stu-id="bff5d-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="bff5d-310">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-310">Select **OK**.</span></span>
1. <span data-ttu-id="bff5d-311">Bekræft arbejdet til plukning af det resterende antal på 2, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="bff5d-312">På næste side skal du vælge **Udfør** for at afslutte plukprocessen og begynde læg på lager-processen.</span><span class="sxs-lookup"><span data-stu-id="bff5d-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="bff5d-313">Mobilappen indeholder lokationen og nummerpladen, hvor varen skal lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="bff5d-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="bff5d-314">Bekræft **Læg på lager** ved masseopbevaring ved at vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="bff5d-315">På den næste side skal du bekræfte **Læg på lager** for cross-docking ved at vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="bff5d-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="bff5d-316">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="bff5d-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="bff5d-317">Vælg **Annuller** for at afslutte.</span><span class="sxs-lookup"><span data-stu-id="bff5d-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="bff5d-318">I følgende illustration vises, hvordan det færdige arbejde til cross-docking kan blive vist i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bff5d-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="bff5d-319">![Arbejde med cross-docking udført](media/PlannedCrossDockingWork.png "Arbejde med cross-docking udført")</span><span class="sxs-lookup"><span data-stu-id="bff5d-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]