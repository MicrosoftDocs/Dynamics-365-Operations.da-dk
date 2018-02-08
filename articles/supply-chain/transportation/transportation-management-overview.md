---
title: Oversigt over transportstyring
description: Dette emne giver et overblik over funktionerne til transportstyring i Microsoft Dynamics 365 for Finance and Operations.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 0ec45fcf7cebf530b3a5889a857214b97b3fffbb
ms.contentlocale: da-dk
ms.lasthandoff: 02/08/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="ec752-103">Oversigt over transportstyring</span><span class="sxs-lookup"><span data-stu-id="ec752-103">Transportation management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ec752-104">Dette emne giver et overblik over funktionerne til transportstyring i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec752-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ec752-105">Med Transportstyring kan du bruge virksomhedens transport og også identificere kreditor- og routingløsninger for indgående og udgående ordrer.</span><span class="sxs-lookup"><span data-stu-id="ec752-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="ec752-106">For eksempel kan du identificere den hurtigste rute eller den billigste sats for en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="ec752-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="ec752-107">Nedenstående tabel indeholder beskrivelser af hovedscenarierne for brug af transportstyring i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec752-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec752-108">Scenarie</span><span class="sxs-lookup"><span data-stu-id="ec752-108">Scenario</span></span></th>
<th><span data-ttu-id="ec752-109">Sådan kan du udnytte transportstyring</span><span class="sxs-lookup"><span data-stu-id="ec752-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec752-110">Brug eksterne logistikudbydere til transportaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="ec752-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="ec752-111">Brug transportstyring til indgående og/eller udgående transport.</span><span class="sxs-lookup"><span data-stu-id="ec752-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec752-112">Virksomhedens egen flåde er klar til levering/afhentning, og leveringsgebyrer sendes videre til kunderne.</span><span class="sxs-lookup"><span data-stu-id="ec752-112">The company's own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="ec752-113">Du kan bruge transportstyring ved udgående processer til at bestemme transportgebyrerne for transport og sende dem videre til kunder.</span><span class="sxs-lookup"><span data-stu-id="ec752-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="ec752-114">Dog er fragtmandens fakturaafstemningsproces ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="ec752-114">However, the carrier invoice reconciliation process isn't required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec752-115">Virksomhedens egen flåde er klar til levering/afhentning, men leveringsgebyrer videreformidles ikke til kunder, fordi produktpriser omfatter transport.</span><span class="sxs-lookup"><span data-stu-id="ec752-115">The company's own fleet is available for delivery/pickup, but delivery charges aren't passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="ec752-116">Mange af funktionerne til projektstyring transport er ikke påkrævede.</span><span class="sxs-lookup"><span data-stu-id="ec752-116">A lot of the Transportation management functionality isn't required.</span></span> <span data-ttu-id="ec752-117">Du kan dog bruge transportstyring til at bestemme transportsatserne og justere salgsprisen i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="ec752-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec752-118">Logistiktjenesten leveres fra en anden juridisk enhed i samme firma.</span><span class="sxs-lookup"><span data-stu-id="ec752-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="ec752-119">Du kan bruge transportstyring ved at behandle den andre juridiske enhed som enhver anden fragtmand.</span><span class="sxs-lookup"><span data-stu-id="ec752-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="ec752-120">Du kan ikke automatisere de økonomiske transaktioner mellem juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="ec752-120">You can't automate the economic transactions between legal entities.</span></span> <span data-ttu-id="ec752-121">Du skal derfor håndtere disse transaktioner manuelt (for eksempel ved at oprette en indkøbsordre).</span><span class="sxs-lookup"><span data-stu-id="ec752-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="ec752-122">I den juridiske enhed, der leverer logistiktjenesterne, kan transportstyring bruges til at bestemme transportsatser.</span><span class="sxs-lookup"><span data-stu-id="ec752-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="ec752-123">Planlægning af transport i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec752-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="ec752-124">I transportstyring kan transportplanlægning baseres på ordrer eller på de forsendelser, der oprettes på grundlag af disse ordrer.</span><span class="sxs-lookup"><span data-stu-id="ec752-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="ec752-125">Forsendelserne findes altid på et eller andet tidspunkt, men er ikke påkrævet for transportplanlægning.</span><span class="sxs-lookup"><span data-stu-id="ec752-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="ec752-126">Flytteordrer er en del af det udgående scenario og kan planlægges sammen med salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="ec752-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Indlæs tegning](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="ec752-128">Indgående transport</span><span class="sxs-lookup"><span data-stu-id="ec752-128">Inbound transportation</span></span>
<span data-ttu-id="ec752-129">Når du bestiller varer fra en leverandør, og varerne skal leveres til dit lagersted, kan du selv arrangere transport af varerne, hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="ec752-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="ec752-130">Du kan bruge Finance and Operations til at planlægge transport og modtagelse af den indgående last.</span><span class="sxs-lookup"><span data-stu-id="ec752-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="ec752-131">Følgende illustration viser forretningsprocessen for planlægning af transport for en indgående belastning.</span><span class="sxs-lookup"><span data-stu-id="ec752-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Forretningsprocesflow for transport af indgående laster](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="ec752-133">Udgående transport</span><span class="sxs-lookup"><span data-stu-id="ec752-133">Outbound transportation</span></span>
<span data-ttu-id="ec752-134">Du kan planlægge og behandle en udgående belastning for at levere bestemte varer fra et firmas lager til en kunde.</span><span class="sxs-lookup"><span data-stu-id="ec752-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="ec752-135">Du kan bruge Finance and Operations til at planlægge transport og levering af den udgående last.</span><span class="sxs-lookup"><span data-stu-id="ec752-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="ec752-136">Følgende illustration viser forretningsprocessen for planlægning og behandling af udgående belastninger for levering.</span><span class="sxs-lookup"><span data-stu-id="ec752-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Planlægning og behandling af udgående laster](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="ec752-138">Lastopbygning</span><span class="sxs-lookup"><span data-stu-id="ec752-138">Load building</span></span>
<span data-ttu-id="ec752-139">Finance and Operations indeholder en lastopbygningsstrategi, der hedder Volumenbaseret lastopbygningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="ec752-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="ec752-140">Denne strategi gør det muligt for dig at bruge de maksimumværdier, der er angivet for højde og vægt i lastskabelonen, eller du kan tilsidesætte indstillingerne ved at angive nye værdier.</span><span class="sxs-lookup"><span data-stu-id="ec752-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="ec752-141">Hvis du vil bruge denne strategi, skal du vælge den i feltet **Lastopbygningsstrategi** i oversigtspanelet **Opsætning** på siden **Lastopbygningspanel**.</span><span class="sxs-lookup"><span data-stu-id="ec752-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="ec752-142">Du kan desuden tilføje dine egne lastopbygningsstrategier ved at oprette en ny klasse i AOT (Application Object Tree).</span><span class="sxs-lookup"><span data-stu-id="ec752-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




