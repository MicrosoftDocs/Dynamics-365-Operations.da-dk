---
title: Oversigt over Planlægningsoptimering
description: Dette emne giver et overblik over funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5b51047dbfc95406ebcdda2255b58e41044a6a6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992614"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="bbe01-103">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="bbe01-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bbe01-104">Tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management giver dig mulighed for at beregne varedisponering udenfor Dynamics 365 Supply Chain Management og den relaterede SQL-database.</span><span class="sxs-lookup"><span data-stu-id="bbe01-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="bbe01-105">De fordele, der er tilknyttet funktionen Planlægningsoptimering, omfatter forbedret ydeevne og minimal påvirkning af SQL-databasen under kørsel af varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="bbe01-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="bbe01-106">Hurtige planlægningskørsler kan udføres selv i kontortiden, så planlæggerne kan reagere øjeblikkeligt på ændringer i behov eller parametre.</span><span class="sxs-lookup"><span data-stu-id="bbe01-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="bbe01-107">Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet til Planlægningsoptimering fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS) og aktivere funktionen Planlægningsoptimering i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bbe01-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="bbe01-108">Du kan finde flere oplysninger under [Kom i gang med Planlægningsoptimering](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="bbe01-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="bbe01-109">I følgende illustration vises fordelen ved at køre Planlægningsoptimering inden for kontorets åbningstider.</span><span class="sxs-lookup"><span data-stu-id="bbe01-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Fordelen ved at køre Planlægningsoptimering inden for kontorets åbningstider](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="bbe01-111">Forbedret ydeevne</span><span class="sxs-lookup"><span data-stu-id="bbe01-111">Improved performance</span></span>

<span data-ttu-id="bbe01-112">Planlægningsoptimering kan bruges i scenarier, der involverer langvarige behovsplaner.</span><span class="sxs-lookup"><span data-stu-id="bbe01-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="bbe01-113">Den er særligt designet til meget hurtige beregninger, der omfatter meget store mængder data.</span><span class="sxs-lookup"><span data-stu-id="bbe01-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="bbe01-114">Da den er bygget som en ultra skalerbar tjeneste til flere lejere, kan flere forekomster arbejde sammen samtidigt i beregningen af planen.</span><span class="sxs-lookup"><span data-stu-id="bbe01-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="bbe01-115">Desuden fjerner planlægningstjenesten belastningen fra varedisponeringen fra systemet og arbejder sammen med en datastrøm, der minimerer serverbelastningen.</span><span class="sxs-lookup"><span data-stu-id="bbe01-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="bbe01-116">Planlægningsoptimering kan hjælpe dig med at opnå følgende mål:</span><span class="sxs-lookup"><span data-stu-id="bbe01-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="bbe01-117">Forbedret ydeevne for planlægning via en kortere kørsel.</span><span class="sxs-lookup"><span data-stu-id="bbe01-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="bbe01-118">Reducere indvirkningen på andre processer under kørslen af varedisponering.</span><span class="sxs-lookup"><span data-stu-id="bbe01-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="bbe01-119">Kør hyppigere planlægningskørsler.</span><span class="sxs-lookup"><span data-stu-id="bbe01-119">Do more frequent planning runs.</span></span> <span data-ttu-id="bbe01-120">(Du er ikke begrænset til de daglige kørsler.)</span><span class="sxs-lookup"><span data-stu-id="bbe01-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="bbe01-121">Være sikker på, at den fremtidige virksomhedsvækst ikke overbelaster planlægningssystemet.</span><span class="sxs-lookup"><span data-stu-id="bbe01-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="bbe01-122">Arkitektur og dataflow</span><span class="sxs-lookup"><span data-stu-id="bbe01-122">Architecture and data flow</span></span>

<span data-ttu-id="bbe01-123">Når tilføjelsesprogrammet Planlægningsoptimering er installeret fra LCS, oprettes der en sikker forbindelse til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bbe01-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="bbe01-124">Tjenesten er placeret i samme datacenterland eller -område som den relaterede Supply Chain Management-forekomst.</span><span class="sxs-lookup"><span data-stu-id="bbe01-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="bbe01-125">Efter Planlægningsoptimering er konfigureret, sendes der, når der køres varedisponering, masterdata og transaktionsdata fra Supply Chain Management til Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bbe01-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="bbe01-126">Hvis tilføjelsesprogrammet Planlægningsoptimering afinstalleres, fjernes alle relaterede data i Planlægningsoptimeringstjenesten.</span><span class="sxs-lookup"><span data-stu-id="bbe01-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="bbe01-127">Dataflowet på højt niveau for kørsler af regenerering</span><span class="sxs-lookup"><span data-stu-id="bbe01-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="bbe01-128">Klienten Supply Chain Management sender et signal for at anmode om en planlægningskørsel fra Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="bbe01-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="bbe01-129">Planlægningsoptimering anmoder om de påkrævede data via den integrerede forbindelse.</span><span class="sxs-lookup"><span data-stu-id="bbe01-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="bbe01-130">SQL-databasen sender de anmodede oplysninger om opsætning, master- og transaktionsdata til Planlægningsoptimering via Connector.</span><span class="sxs-lookup"><span data-stu-id="bbe01-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="bbe01-131">Connectoren oversætter oplysninger mellem Supply Chain Management og tjenesten Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="bbe01-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="bbe01-132">Planlægningsoptimeringstjenesten gemmer planlægningsrelaterede data i hukommelsen og foretager de påkrævede beregninger.</span><span class="sxs-lookup"><span data-stu-id="bbe01-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="bbe01-133">Planlægningsresultatet sendes til Supply Chain Management-databasen via Connector.</span><span class="sxs-lookup"><span data-stu-id="bbe01-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="bbe01-134">Resultaterne omfatter oplysninger, som f.eks. ordreforslag og oplysninger om udligning.</span><span class="sxs-lookup"><span data-stu-id="bbe01-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="bbe01-135">Planlægningsoptimering sender et signal til Supply Chain Management for at indikere, at planlægningskørslen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bbe01-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="bbe01-136">Den sender også alle relevante meddelelser og advarsler.</span><span class="sxs-lookup"><span data-stu-id="bbe01-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="bbe01-137">Følgende illustration viser dataflowet.</span><span class="sxs-lookup"><span data-stu-id="bbe01-137">The following illustration shows the data flow.</span></span>

![Dataflowet for kørsler af regenerering](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="bbe01-139">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="bbe01-139">Related resources</span></span>

[<span data-ttu-id="bbe01-140">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="bbe01-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="bbe01-141">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="bbe01-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="bbe01-142">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="bbe01-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="bbe01-143">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="bbe01-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="bbe01-144">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="bbe01-144">Cancel a planning job</span></span>](cancel-planning-job.md)
