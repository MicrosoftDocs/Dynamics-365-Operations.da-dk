---
title: Foretage fejlfinding af varedisponering
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med varedisponering.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
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
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216099"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="00524-103">Foretage fejlfinding af varedisponering</span><span class="sxs-lookup"><span data-stu-id="00524-103">Troubleshoot master planning</span></span>

<span data-ttu-id="00524-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med varedisponering.</span><span class="sxs-lookup"><span data-stu-id="00524-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="00524-105">Styklisteudfoldningen opfører sig forskelligt for autoriserede produktionsordrer og forkalkulerede produktionsordrer for manuelt oprettet arbejde.</span><span class="sxs-lookup"><span data-stu-id="00524-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="00524-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="00524-106">Issue description</span></span>

<span data-ttu-id="00524-107">Når en produktionsordre autoriseres, udfoldes varerne ikke, når du udfolder styklisten.</span><span class="sxs-lookup"><span data-stu-id="00524-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="00524-108">Men når du opretter en arbejdsordre manuelt og derefter forkalkulerer produktionsordren, udfoldes varerne.</span><span class="sxs-lookup"><span data-stu-id="00524-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="00524-109">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="00524-109">Issue resolution</span></span>

<span data-ttu-id="00524-110">Systemet fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="00524-110">The system is working as expected.</span></span> <span data-ttu-id="00524-111">Den udfoldning, der opstår, når produktionsordren autoriseres, peger på ordreforslaget, men det ser ikke ud til, at ordreforslaget er autoriseret i dette tilfælde.</span><span class="sxs-lookup"><span data-stu-id="00524-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="00524-112">Men hvis produktionsordren er forkalkuleret, udløses udfoldningen fra den frigivne produktionsordre, når der ikke findes et ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="00524-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="00524-113">Forsinkelsesværdien opdateres ikke, når jeg ændrer planlægning af et ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="00524-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="00524-114">Hvis du vil opdatere forsinkelsen for ordreforslag, skal du åbne dialogboksen **Omplanlægning** for ordreforslaget.</span><span class="sxs-lookup"><span data-stu-id="00524-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="00524-115">I oversigtspanelet **Udfoldning** skal du kontrollere, at indstillingen **Foretag udfoldning efter omplanlægning** er angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="00524-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="00524-116">I produktionsplanlægning tages der ikke hensyn til de sikkerhedsmargener, der er angivet på varedisponeringen for sporede forsyninger.</span><span class="sxs-lookup"><span data-stu-id="00524-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="00524-117">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="00524-117">Issue description</span></span>

<span data-ttu-id="00524-118">Varedisponering tager højde for sikkerhedsmargener.</span><span class="sxs-lookup"><span data-stu-id="00524-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="00524-119">Sikkerhedsmargenerne ignoreres dog, når produktionsordreforslag planlægges.</span><span class="sxs-lookup"><span data-stu-id="00524-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="00524-120">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="00524-120">Issue resolution</span></span>

<span data-ttu-id="00524-121">Margener betragtes kun for varedisponering, ikke under manuel planlægning.</span><span class="sxs-lookup"><span data-stu-id="00524-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="00524-122">Margener er designet til at fungere som en buffer i planlægningsfasen, så der gives nogen "margen" for den faktiske proces.</span><span class="sxs-lookup"><span data-stu-id="00524-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="00524-123">Du kan få det ønskede resultat ved at fjerne margen.</span><span class="sxs-lookup"><span data-stu-id="00524-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="00524-124">Ruten skal derefter opdateres, så den omfatter den ønskede tid (f.eks. køtid).</span><span class="sxs-lookup"><span data-stu-id="00524-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="00524-125">Både varedisponering og manuel planlægning bør derefter give samme resultat.</span><span class="sxs-lookup"><span data-stu-id="00524-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="00524-126">Ordreforslag genereres, selvom der allerede findes varer på lager og produktionsordrer for dem.</span><span class="sxs-lookup"><span data-stu-id="00524-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="00524-127">Du kan muligvis løse dette problem ved at øge værdien af **Positive dage** for de relevante grupper på siden **Disponeringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="00524-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="00524-128">Denne ændring bevirker, at systemet afgør, om disponibel lagerbeholdning kan bruges til efterspørgslen.</span><span class="sxs-lookup"><span data-stu-id="00524-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="00524-129">Derefter vil der ikke blive genereret et nyt ordreforslag for de varer, der er på lager.</span><span class="sxs-lookup"><span data-stu-id="00524-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="00524-130">Varedisponering overholder tilsyneladende ikke kapacitetsbegrænsninger og planlægger mere end den tilgængelige kapacitet.</span><span class="sxs-lookup"><span data-stu-id="00524-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="00524-131">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="00524-131">Issue description</span></span>

<span data-ttu-id="00524-132">Når du bruger grovplanlægning, hvor der er kapacitetsbegrænsning, og hvor ruten angiver en blanding af behov for både en ressourcegruppe og de enkelte ressourcer, er der en lille risiko for at overbooke på grund af den måde, som algoritmen validerer for kapacitetskonflikter.</span><span class="sxs-lookup"><span data-stu-id="00524-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="00524-133">Denne overbooking kan forekomme, når du bruger hjælpefunktioner til at køre varedisponering.</span><span class="sxs-lookup"><span data-stu-id="00524-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="00524-134">Det sker oftest, hvis der er mange job med forholdsvis kort kørselstid.</span><span class="sxs-lookup"><span data-stu-id="00524-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="00524-135">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="00524-135">Issue resolution</span></span>

<span data-ttu-id="00524-136">Hvis det er vigtigt, at der ikke opstår nogen overbooking til grovplanlægning, kan du gøre planlægningsdelen af varedisponering enkelttrådet ved at aktivere indstillingen **Præcis kapacitetsbegrænsning for grovplanlægning** på siden **Parametre for varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="00524-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="00524-137">Denne indstilling er som standard ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="00524-137">This option isn't available by default.</span></span> <span data-ttu-id="00524-138">Du skal manuelt føje den til siden ved hjælp af tilpasningsfunktioner.</span><span class="sxs-lookup"><span data-stu-id="00524-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="00524-139">Når du bruger denne indstilling, kører planlægningen langsommere på grund af manglende parallel behandling.</span><span class="sxs-lookup"><span data-stu-id="00524-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="00524-140">Det tager lang tid at opdatere ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="00524-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="00524-141">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="00524-141">Issue description</span></span>

<span data-ttu-id="00524-142">Når behovsantallet og/eller leveringsdatoen opdateres på et ordreforslag, tager det normalt mindst 30 sekunder pr. ordre at gemme opdateringen.</span><span class="sxs-lookup"><span data-stu-id="00524-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="00524-143">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="00524-143">Issue resolution</span></span>

<span data-ttu-id="00524-144">Dette er et kendt problem med det indbyggede varedisponeringsprogram.</span><span class="sxs-lookup"><span data-stu-id="00524-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="00524-145">Det skyldes den underliggende automatiske udfoldning via styklistestrukturen under redigeringer.</span><span class="sxs-lookup"><span data-stu-id="00524-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="00524-146">Dette problem håndteres i Planlægningsoptimering, hvor en planlægger kan opdatere og godkende de relevante ordrer og, hvor det er relevant, udløse en planlægningskørsel for at opdatere ordreforslag for den underliggende styklistestruktur.</span><span class="sxs-lookup"><span data-stu-id="00524-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="00524-147">En måde at forbedre ydeevnen med det indbyggede varedisponeringsprogram på er at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="00524-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="00524-148">Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="00524-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="00524-149">Vælg en plan.</span><span class="sxs-lookup"><span data-stu-id="00524-149">Select a plan.</span></span>
1. <span data-ttu-id="00524-150">Udvid oversigtspanelet **Tidshorisont i dage**.</span><span class="sxs-lookup"><span data-stu-id="00524-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="00524-151">Angiv **Udfoldning** til *Ja*, og angiv feltet under denne indstilling til 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="00524-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="00524-152">Dette vil begrænse den periode for udfoldning, der udføres for denne behovsplan, til en enkelt dag.</span><span class="sxs-lookup"><span data-stu-id="00524-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]