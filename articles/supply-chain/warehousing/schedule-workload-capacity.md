---
title: Planlægge arbejdsbyrdekapacitet
description: I dette emne beskrives, hvordan du opretter og planlægger arbejdsbyrdekapaciteten for arbejdere på et lagersted eller for hele lagerstedet.
author: MarkusFogelberg
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2458009dabd71e6c8423e8e607a0cedb4765b88
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817335"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="4ab0c-103">Planlægge arbejdsbyrdekapacitet</span><span class="sxs-lookup"><span data-stu-id="4ab0c-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4ab0c-104">Du kan planlægge arbejdsbyrdekapacitet for lagersteder, og du kan også planlægge de aktuelle og fremtidige arbejdsbyrder for medarbejderne på de forskellige lagersteder.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="4ab0c-105">Du kan planlægge arbejdsbyrden for hele lagerstedet, eller du kan planlægge arbejdsbyrden separat for indgående og udgående arbejdsbyrder.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="4ab0c-106">Hvis du vil planlægge arbejdsbyrdeoutput for udvalgte lagersteder, skal der være behovsplanlægningsdata tilgængelige for de pågældende lagersteder.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="4ab0c-107">Du kan finde flere oplysninger under [Oversigt over Behovsplaner](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="4ab0c-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="4ab0c-108">Planlægge og se arbejdsbyrder for et lagersted.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="4ab0c-109">Hvis du vil planlægge arbejdsbyrdekapacitet for et lagersted, skal du oprette en arbejdsbyrdeopsætning for et eller flere lagersteder og derefter knytte arbejdsbyrdeopsætningen til en behovsplan.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="4ab0c-110">I arbejdsbyrdekapacitetsopsætningen kan du definere grænser for vægt eller volumen for indgående og udgående transaktioner.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="4ab0c-111">Du kan også konfigurere mere end en opsætning for hvert lagersted og derefter tilknyttet opsætningen med forskellige behovsplaner.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="4ab0c-112">Du kan f.eks. bruge denne fremgangsmåde til at tilpasse sæsonbestemte ændringer til arbejdsstyrken.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="4ab0c-113">Hvis medarbejderne på et lager arbejder med transaktioner for indgående og udgående arbejdsbyrder, kan du konfigurere lagerkapacitetsopsætningen, så arbejdsbyrden vises anslået i en samlet visning.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="4ab0c-114">Hvis du vil planlægge og få vist arbejdsbyrden for lagersteder, skal du fuldføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="4ab0c-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="4ab0c-115">Opret en arbejdsbyrdekapacitetsopsætning, og definer arbejdsbyrdekapacitetsbegrænsningerne for et eller flere lagersteder.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="4ab0c-116">Knyt arbejdsbyrdekapacitetsopsætningen til en behovsplan for at oprette arbejdsbyrdeprognoser og angive, hvor længe planerne gælder.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="4ab0c-117">Oprette en arbejdsbyrdekapacitetsopsætning for et lagersted</span><span class="sxs-lookup"><span data-stu-id="4ab0c-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="4ab0c-118">Vælg **Lagerstyring** \> **Opsætning** \> **Overvågning af lagersted** \> **Arbejdsbyrdekapacitet**.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="4ab0c-119">Vælg **Ny** i handlingsruden for at oprette en arbejdsbyrdekapacitetsopsætning.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="4ab0c-120">Vælg **Ny** i oversigtspanelet **Lagersteder**, og indtast derefter værdier på linjen for at knytte et lager med arbejdsbyrdekapacitetsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="4ab0c-121">Marker afkrydsningsfeltet **Kombineret indgående og udgående arbejdsbyrde**, hvis rapporten **Arbejdsbyrdekapacitet** skal vise den samlede arbejdsbyrde for indgående og udgående transaktioner i én visning.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="4ab0c-122">Vælg de typer indgående og udgående transaktionstyper, som arbejdsbyrdebegrænsningerne skal gælde for, i oversigtspanelet **Transaktionstyper**.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4ab0c-123">Du skal vælge mindst én transaktionstype for både den indgående arbejdsbyrde og den udgående arbejdsbyrde.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="4ab0c-124">Definere grænser for volumen eller vægt</span><span class="sxs-lookup"><span data-stu-id="4ab0c-124">Define limits for volume or weight</span></span>

<span data-ttu-id="4ab0c-125">Du kan konfigurere grænser for volumen eller vægt på baggrund af de begrænsninger, der er relevante for lagerstedets medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="4ab0c-126">De angivne grænser medtages i arbejdsbyrdekapacitetsplanlægningen, som du kan se i rapporten **Arbejdsbyrdekapacitet**.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="4ab0c-127">Hvis du vil oprette planer med oplysninger om volumen og vægt for varer, skal standardvolumen af en lagervare og vægten af en lagervare angives for alle produkter.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="4ab0c-128">De påkrævede felter er tilgængelige i følgende feltgrupper i oversigtspanelet **Styr lager** på siden **Frigivne produktdetaljer**:</span><span class="sxs-lookup"><span data-stu-id="4ab0c-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="4ab0c-129">Ekspederes</span><span class="sxs-lookup"><span data-stu-id="4ab0c-129">Handling</span></span>
- <span data-ttu-id="4ab0c-130">Fysiske dimensioner</span><span class="sxs-lookup"><span data-stu-id="4ab0c-130">Physical dimensions</span></span>
- <span data-ttu-id="4ab0c-131">Måleenheder for vægt</span><span class="sxs-lookup"><span data-stu-id="4ab0c-131">Weight measurements</span></span>

<span data-ttu-id="4ab0c-132">Hvis disse oplysninger ikke angives korrekt, du får vist en meddelelse, når du genererer rapporten **Arbejdsbyrdekapacitet**.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="4ab0c-133">I rapporten kan du derefter dykke ned for at identificere de manglende oplysninger, der stadig skal angives, for at den fremtidige arbejdsbyrde kan planlægges.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="4ab0c-134">Knytte en arbejdsbyrdekapacitetsopsætning til en behovsplan</span><span class="sxs-lookup"><span data-stu-id="4ab0c-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="4ab0c-135">Vælg **Lagerstyring** \> **Periodisk** \> **Planlæg arbejdsbyrde**.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="4ab0c-136">I feltet **Behovsplan** skal du vælge den behovsplan, der skal bruges til prognoser for arbejdsbyrde.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="4ab0c-137">I feltet **Antal dage** skal du angive antallet dage, der dækkes arbejdsbyrdeplanen.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="4ab0c-138">I feltet **Arbejdsbyrde** skal du vælge den arbejdsbyrdeopsætning, der skal tilknyttes behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="4ab0c-139">Få vist arbejdsbyrdekapacitet</span><span class="sxs-lookup"><span data-stu-id="4ab0c-139">View workload capacity</span></span>

1. <span data-ttu-id="4ab0c-140">Vælg **Lagerstyring** \> **Forespørgsler og rapporter** \> **Fysiske lagerrapporter** \> **Arbejdsbyrdekapacitet**.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="4ab0c-141">I feltet **Antal kolonner** skal du angive antallet af kolonner, der skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="4ab0c-142">I feltet **Ordretype** skal du vælge **Planlagt og bekræftet**, **Planlagt** eller **Bekræftet** for at angive den type ordrer, der skal anslås i rapporten.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="4ab0c-143">I feltet **Lastningstype** skal du vælge en belastningstype for at angive, om arbejdsbyrdekapaciteten skal planlægges for paller, volumen eller vægt.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="4ab0c-144">I feltet **Arbejdsbyrdekapacitet** skal du vælge en arbejdsbyrdekapacitetsopsætning.</span><span class="sxs-lookup"><span data-stu-id="4ab0c-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]