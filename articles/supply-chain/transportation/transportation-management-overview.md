---
title: Oversigt over transportstyring
description: Dette emne giver et overblik over funktionerne til transportstyring i Microsoft Dynamics 365 for Finance and Operations.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 918167a3ab72b3d3665cf710d8e509417b94a056
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561147"
---
# <a name="transportation-management-overview"></a><span data-ttu-id="c915b-103">Oversigt over transportstyring</span><span class="sxs-lookup"><span data-stu-id="c915b-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c915b-104">Dette emne giver et overblik over funktionerne til transportstyring i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c915b-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="c915b-105">Med Transportstyring kan du bruge virksomhedens transport og også identificere kreditor- og routingløsninger for indgående og udgående ordrer.</span><span class="sxs-lookup"><span data-stu-id="c915b-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="c915b-106">For eksempel kan du identificere den hurtigste rute eller den billigste sats for en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="c915b-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="c915b-107">Følgende tabel indeholder beskrivelser af hovedscenarierne for brug af transportstyring i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c915b-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c915b-108">Scenarie</span><span class="sxs-lookup"><span data-stu-id="c915b-108">Scenario</span></span></th>
<th><span data-ttu-id="c915b-109">Sådan kan du udnytte transportstyring</span><span class="sxs-lookup"><span data-stu-id="c915b-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c915b-110">Brug eksterne logistikudbydere til transportaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c915b-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="c915b-111">Brug transportstyring til indgående og/eller udgående transport.</span><span class="sxs-lookup"><span data-stu-id="c915b-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c915b-112">Virksomhedens egen flåde er klar til levering/afhentning, og leveringsgebyrer sendes videre til kunderne.</span><span class="sxs-lookup"><span data-stu-id="c915b-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="c915b-113">Du kan bruge transportstyring ved udgående processer til at bestemme transportgebyrerne for transport og sende dem videre til kunder.</span><span class="sxs-lookup"><span data-stu-id="c915b-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="c915b-114">Dog er fragtmandens fakturaafstemningsproces ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="c915b-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c915b-115">Virksomhedens egen flåde er klar til levering/afhentning, men leveringsgebyrer videreformidles ikke til kunder, fordi produktpriser omfatter transport.</span><span class="sxs-lookup"><span data-stu-id="c915b-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="c915b-116">Mange af funktionerne til projektstyring transport er ikke påkrævede.</span><span class="sxs-lookup"><span data-stu-id="c915b-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="c915b-117">Du kan dog bruge transportstyring til at bestemme transportsatserne og justere salgsprisen i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="c915b-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c915b-118">Logistiktjenesten leveres fra en anden juridisk enhed i samme firma.</span><span class="sxs-lookup"><span data-stu-id="c915b-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="c915b-119">Du kan bruge transportstyring ved at behandle den andre juridiske enhed som enhver anden fragtmand.</span><span class="sxs-lookup"><span data-stu-id="c915b-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="c915b-120">Du kan ikke automatisere de økonomiske transaktioner mellem juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="c915b-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="c915b-121">Du skal derfor håndtere disse transaktioner manuelt (for eksempel ved at oprette en indkøbsordre).</span><span class="sxs-lookup"><span data-stu-id="c915b-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="c915b-122">I den juridiske enhed, der leverer logistiktjenesterne, kan transportstyring bruges til at bestemme transportsatser.</span><span class="sxs-lookup"><span data-stu-id="c915b-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="c915b-123">Planlægning af transport i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c915b-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="c915b-124">I transportstyring kan transportplanlægning baseres på ordrer eller på de forsendelser, der oprettes på grundlag af disse ordrer.</span><span class="sxs-lookup"><span data-stu-id="c915b-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="c915b-125">Forsendelserne findes altid på et eller andet tidspunkt, men er ikke påkrævet for transportplanlægning.</span><span class="sxs-lookup"><span data-stu-id="c915b-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="c915b-126">Flytteordrer er en del af det udgående scenario og kan planlægges sammen med salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c915b-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Indlæs tegning](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="c915b-128">Indgående transport</span><span class="sxs-lookup"><span data-stu-id="c915b-128">Inbound transportation</span></span>
<span data-ttu-id="c915b-129">Når du bestiller varer fra en leverandør, og varerne skal leveres til dit lagersted, kan du selv arrangere transport af varerne, hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="c915b-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="c915b-130">Du kan bruge Finance and Operations til at planlægge transport og modtagelse af den indgående last.</span><span class="sxs-lookup"><span data-stu-id="c915b-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="c915b-131">Følgende illustration viser forretningsprocessen for planlægning af transport for en indgående belastning.</span><span class="sxs-lookup"><span data-stu-id="c915b-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Forretningsprocesflow for transport af indgående laster](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="c915b-133">Udgående transport</span><span class="sxs-lookup"><span data-stu-id="c915b-133">Outbound transportation</span></span>
<span data-ttu-id="c915b-134">Du kan planlægge og behandle en udgående belastning for at levere bestemte varer fra et firmas lager til en kunde.</span><span class="sxs-lookup"><span data-stu-id="c915b-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="c915b-135">Du kan bruge Finance and Operations til at planlægge transport og levering af den udgående last.</span><span class="sxs-lookup"><span data-stu-id="c915b-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="c915b-136">Følgende illustration viser forretningsprocessen for planlægning og behandling af udgående belastninger for levering.</span><span class="sxs-lookup"><span data-stu-id="c915b-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Planlægning og behandling af udgående laster](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="c915b-138">Lastopbygning</span><span class="sxs-lookup"><span data-stu-id="c915b-138">Load building</span></span>
<span data-ttu-id="c915b-139">Finance and Operations indeholder en lastopbygningsstrategi, der hedder Volumenbaseret lastopbygningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="c915b-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="c915b-140">Denne strategi gør det muligt for dig at bruge de maksimumværdier, der er angivet for højde og vægt i lastskabelonen, eller du kan tilsidesætte indstillingerne ved at angive nye værdier.</span><span class="sxs-lookup"><span data-stu-id="c915b-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="c915b-141">Hvis du vil bruge denne strategi, skal du vælge den i feltet **Lastopbygningsstrategi** i oversigtspanelet **Opsætning** på siden **Lastopbygningspanel**.</span><span class="sxs-lookup"><span data-stu-id="c915b-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="c915b-142">Du kan desuden tilføje dine egne lastopbygningsstrategier ved at oprette en ny klasse i AOT (Application Object Tree).</span><span class="sxs-lookup"><span data-stu-id="c915b-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>



