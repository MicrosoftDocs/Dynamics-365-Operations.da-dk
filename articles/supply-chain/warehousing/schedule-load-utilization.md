---
title: Planlæg lastningsudnyttelse
description: I dette emne beskrives, hvordan du kan oprette og planlægge belastningen for et lagersted.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424419"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="73d9d-103">Planlæg lastningsudnyttelse</span><span class="sxs-lookup"><span data-stu-id="73d9d-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="73d9d-104">Du kan planlægge lastningsudnyttelse for udvalgte lokationstyper, og du kan også oprette prognoser for den aktuelle og fremtidige belastning.</span><span class="sxs-lookup"><span data-stu-id="73d9d-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="73d9d-105">Du kan oprette prognoser for belastningen på en eller flere lokationer, for lastningsenheder (zone eller lagersted) eller for en kombination af en zone og et lagersted.</span><span class="sxs-lookup"><span data-stu-id="73d9d-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="73d9d-106">Planlægge og få vist belastning for et lagersted eller en lokation</span><span class="sxs-lookup"><span data-stu-id="73d9d-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="73d9d-107">For at planlægge belastningen for lokationer, lagersteder eller zoner, skal du oprette en pladsudnyttelseskonfiguration og knytte den til en behovsplan.</span><span class="sxs-lookup"><span data-stu-id="73d9d-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="73d9d-108">I pladsudnyttelseskonfigurationen skal du bruge lokationstyper, f.eks. **Bulkvarelokation** og **Plukplads**, til at angive, hvordan pladsudnyttelsen skal planlægges.</span><span class="sxs-lookup"><span data-stu-id="73d9d-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="73d9d-109">Du også angive en lagringslastningstilstand, f.eks **Zone**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="73d9d-110">Prognosen for fremtidig pladsudnyttelse er baseret på oplysninger, der er beregnet på den tilknyttede behovsplan.</span><span class="sxs-lookup"><span data-stu-id="73d9d-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="73d9d-111">Behovsplaner anslår ressourceplanlægningen for indgående og udgående ordrer for produktion og operationer.</span><span class="sxs-lookup"><span data-stu-id="73d9d-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="73d9d-112">Prognosen over tilgængelig plads er baseret på forholdet mellem pladsudnyttelseskonfigurationen og den valgte behovsplan.</span><span class="sxs-lookup"><span data-stu-id="73d9d-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="73d9d-113">Ved hjælp af belastningstilstanden, du valgte i opsætning af pladsudnyttelse, kan du angive, om belastningen skal anslås for hvert enkelt lagersted eller zone, eller om prognosen skal indeholde oplysninger om både lagersteder og zoner.</span><span class="sxs-lookup"><span data-stu-id="73d9d-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="73d9d-114">Du kan også angive, om blokerede lagersteder skal udelukkes fra beregningen af lastningsudnyttelsen.</span><span class="sxs-lookup"><span data-stu-id="73d9d-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="73d9d-115">Du kan planlægge pladsudnyttelsen ved at generere rapporten **Lagerstedslastningsudnyttelse**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="73d9d-116">Når du opretter denne rapport, kan du angive, om lastningsudnyttelsen skal anslås for hver lokation eller på tværs af lokationer eller for den valgte lastningsenhed, f.eks. zone eller lagersted.</span><span class="sxs-lookup"><span data-stu-id="73d9d-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="73d9d-117">Oprette en pladsudnyttelsesopsætning for et lagersted</span><span class="sxs-lookup"><span data-stu-id="73d9d-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="73d9d-118">Vælg **Lagerstyring** \> **Opsætning** \> **Overvågning af lagersted** \> **Pladsudnyttelse**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="73d9d-119">Vælg **Ny** for at oprette en pladsudnyttelsesopsætning.</span><span class="sxs-lookup"><span data-stu-id="73d9d-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="73d9d-120">Angiv et id og et navn til den nye konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="73d9d-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="73d9d-121">I feltet **Lagerlastningstilstand** skal du vælge, om oversigten over pladsudnyttelse skal vise oplysninger pr. lagersted, zone eller lagersted og zone.</span><span class="sxs-lookup"><span data-stu-id="73d9d-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="73d9d-122">Vælg **Ja** i indstillingen **Udelad spærrede adresser** for at udelade spærrede lagerplaceringer i beregningen af ledig plads.</span><span class="sxs-lookup"><span data-stu-id="73d9d-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="73d9d-123">Du kan blokere en lagerstedsplacering for input og output ved at angive en blokeringsårsag for lokationen i feltet **Indlagring spærret** eller **Udlagring spærret** i oversigtspanelet **Andet** på siden **Lagerlokationer**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="73d9d-124">I oversigtspanelet **Lokationstype** skal du vælge de lokationstyper, der skal medtages i beregningen af pladsudnyttelsen.</span><span class="sxs-lookup"><span data-stu-id="73d9d-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="73d9d-125">Du skal vælge mindst én lokationstype til prognosen.</span><span class="sxs-lookup"><span data-stu-id="73d9d-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="73d9d-126">Knytte en pladsudnyttelsesopsætning til til en behovsplan</span><span class="sxs-lookup"><span data-stu-id="73d9d-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="73d9d-127">Vælg **Lagerstyring** \> **Periodiske opgaver** \> **Planlæg lastningsudnyttelse**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="73d9d-128">Vælg en behovsplan i feltet **Behovsplan**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="73d9d-129">I feltet **Antal dage** skal du angive antallet dage, der skal medtages i prognosen over aktuelle og fremtidige arbejdsbyrder.</span><span class="sxs-lookup"><span data-stu-id="73d9d-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="73d9d-130">I feltet **Pladsudnyttelse** skal du vælge den pladsudnyttelsesopsætning, der skal bruges til at anslå den aktuelle og fremtidige arbejdsbelastning.</span><span class="sxs-lookup"><span data-stu-id="73d9d-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="73d9d-131">Angive lastningsudnyttelseprognose og få vist oplysninger</span><span class="sxs-lookup"><span data-stu-id="73d9d-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="73d9d-132">Vælg **Lagerstyring** \> **Forespørgsler og rapporter** \> **Fysiske lagerrapporter** \> **Lagerstedslastningsudnyttelse**.</span><span class="sxs-lookup"><span data-stu-id="73d9d-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="73d9d-133">I feltet **Vis efter** skal du vælge niveauet for pladsudnyttelseprognoser:</span><span class="sxs-lookup"><span data-stu-id="73d9d-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="73d9d-134">**Lokation** – Vælg denne indstilling for at anslå pladsudnyttelsen pr. lokation.</span><span class="sxs-lookup"><span data-stu-id="73d9d-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="73d9d-135">Denne prognose er nyttig, hvis du f.eks. vil have vist alle lagersteder for en lokation, så du kan afstemme udnyttelse af pladsen mellem lagerstederne.</span><span class="sxs-lookup"><span data-stu-id="73d9d-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="73d9d-136">**Lastningsenhed** – Vælg denne indstilling for at anslå pladsudnyttelsen for zoner eller lagersteder.</span><span class="sxs-lookup"><span data-stu-id="73d9d-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="73d9d-137">Den tilgængelige plads anslås herefter i overensstemmelse med den værdi, du valgte i feltet **Lagerlastningstilstand** på siden **Pladsudnyttelse**, da du oprettede pladsudnyttelsesopsætningen.</span><span class="sxs-lookup"><span data-stu-id="73d9d-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="73d9d-138">Benyt en af følgende fremgangsmåder, afhængigt af den værdi du valgte i forrige trin:</span><span class="sxs-lookup"><span data-stu-id="73d9d-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="73d9d-139">Hvis du valgte **Lokation** i feltet **Vis efter**, er feltet **Lokation** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="73d9d-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="73d9d-140">Vælg en eller flere lokationer, der skal medtages i prognosen.</span><span class="sxs-lookup"><span data-stu-id="73d9d-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="73d9d-141">Hvis du valgte **Lastningsenhed** i feltet **Vis efter**, er feltet **Lastningsenhed** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="73d9d-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="73d9d-142">Vælg lastningsenheden.</span><span class="sxs-lookup"><span data-stu-id="73d9d-142">Select the load unit.</span></span>

4. <span data-ttu-id="73d9d-143">I feltet **Lastningstype** skal du vælge **Enhed** eller **Vægt** for at angive den lagerdriftsenhed, der skal anslås plads for.</span><span class="sxs-lookup"><span data-stu-id="73d9d-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="73d9d-144">I feltet **Opsætning af pladsudnyttelse** skal du vælge den pladsudnyttelsesopsætning, som prognosen skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="73d9d-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
