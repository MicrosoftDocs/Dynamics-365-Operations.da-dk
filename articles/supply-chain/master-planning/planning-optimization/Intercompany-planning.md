---
title: Intern planlægning
description: Dette emne beskriver den interne planlægning og forklarer, hvordan du konfigurerer intern planlægning med Planlægningsoptimering i Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e6fff06cb6194f17444025f7ea1f9dbb46e4f3ea
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907637"
---
# <a name="intercompany-planning"></a><span data-ttu-id="0d878-103">Intern planlægning</span><span class="sxs-lookup"><span data-stu-id="0d878-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d878-104">I nogle organisationer afhænger logistikdriften af andre juridiske enheder (firmaer) i organisationen.</span><span class="sxs-lookup"><span data-stu-id="0d878-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="0d878-105">Denne drift håndteres ved hjælp af interne salg og indkøb, fordi hver juridiske enhed har en separat kontoplan.</span><span class="sxs-lookup"><span data-stu-id="0d878-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="0d878-106">Dette emne beskriver den interne planlægning og forklarer, hvordan du konfigurerer intern planlægning med Planlægningsoptimering i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d878-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0d878-107">I dette emne anvendes følgende vigtige interne begreber:</span><span class="sxs-lookup"><span data-stu-id="0d878-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="0d878-108">**Upstream** – En relativ reference i en firma- eller forsyningskæde.</span><span class="sxs-lookup"><span data-stu-id="0d878-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="0d878-109">Den angiver bevægelse i retning af råvareleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0d878-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="0d878-110">**Downstream** – En relativ reference i en firma- eller forsyningskæde.</span><span class="sxs-lookup"><span data-stu-id="0d878-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="0d878-111">Den angiver bevægelse i retning af kunden.</span><span class="sxs-lookup"><span data-stu-id="0d878-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="0d878-112">**Planlagt intern efterspørgsel** – Planlagt behov for et produkt i et firma, baseret på den planlagte efterspørgsel efter produktet fra et downstream-firma.</span><span class="sxs-lookup"><span data-stu-id="0d878-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="0d878-113">I varedisponering kan en plan i et firma omfatte planlagt intern efterspørgsel, der er relateret til ordreforslag fra en plan i et andet firma.</span><span class="sxs-lookup"><span data-stu-id="0d878-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="0d878-114">Denne funktion er nyttig, fordi den giver fuld synlighed over ordreforslag på tværs af firmaer.</span><span class="sxs-lookup"><span data-stu-id="0d878-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="0d878-115">Det sikrer også, at alle påkrævede planlagte forsyningsordrer oprettes, men uden at kræve, at ordreforslag autoriseres for den interne efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="0d878-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="0d878-116">Hvis du kører varedisponering fra en behovsplan, der omfatter planlagt downstream-behov, vil indkøbsordreforslag fra de relaterede interne leverandører blive medtaget i planen som et behov.</span><span class="sxs-lookup"><span data-stu-id="0d878-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="0d878-117">Nødvendig opsætning</span><span class="sxs-lookup"><span data-stu-id="0d878-117">Required setup</span></span>

<span data-ttu-id="0d878-118">Hvis du vil bruge intern planlægning, skal du forberede systemet på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0d878-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="0d878-119">De relevante produkter skal frigives i alle relevante firmaer.</span><span class="sxs-lookup"><span data-stu-id="0d878-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="0d878-120">Yderligere oplysninger finder du i [Konfigurere og bruge intern handel i Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) på Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="0d878-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="0d878-121">Downstream-behov skal være dækket af indkøb fra en leverandør, der har en intern relation til upstream-firmaet, og relevante standardlagerdimensioner (lokation og lagersted) på kunden.</span><span class="sxs-lookup"><span data-stu-id="0d878-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="0d878-122">Yderligere oplysninger finder du i [Konfigurere og bruge intern handel i Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) på Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="0d878-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="0d878-123">Behovsplanen i upstream-firmaet skal indeholde planlagt downstream-efterspørgsel, og det relevante firma og behovsplanen skal være angivet i de downstream-planerne.</span><span class="sxs-lookup"><span data-stu-id="0d878-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="0d878-124">Inkluder planlagt downstream-efterspørgsel</span><span class="sxs-lookup"><span data-stu-id="0d878-124">Include planned downstream demand</span></span>

<span data-ttu-id="0d878-125">Hvis du vil konfigurere din behovsplan, så den omfatter planlagt downstream-efterspørgsel, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="0d878-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="0d878-126">Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="0d878-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="0d878-127">Vælg eller opret en behovsplan.</span><span class="sxs-lookup"><span data-stu-id="0d878-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="0d878-128">I oversigtspanelet **Intern planlægning** skal du indstille følgende felter:</span><span class="sxs-lookup"><span data-stu-id="0d878-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="0d878-129">**Medtag planlagt downstream-efterspørgsel** – Angiv denne indstilling til *Ja* for at aktivere intern planlægning for behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="0d878-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="0d878-130">**Downstream-planer** – Hvis du angiver indstillingen **Medtag planlagt downstream-efterspørgsel** til *Ja*, skal du bruge værktøjslinjen og gitteret til at tilføje de ønskede behovsplaner fra andre firmaer.</span><span class="sxs-lookup"><span data-stu-id="0d878-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="0d878-131">Udligne på tværs af firmaer ved hjælp af udligning på flere niveauer</span><span class="sxs-lookup"><span data-stu-id="0d878-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="0d878-132">I udligninger på flere niveauer kan du få vist udligning på tværs af firmaer for at se den første kilde til efterspørgslen, der er dækket af en forsyning.</span><span class="sxs-lookup"><span data-stu-id="0d878-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="0d878-133">Benyt følgende fremgangsmåde for at få vist oplysninger om udligning på flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="0d878-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="0d878-134">Gå til **Varedisponering \> Varedisponering \> Ordreforslag**.</span><span class="sxs-lookup"><span data-stu-id="0d878-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="0d878-135">Vælg eller åbn et ordreforslag.</span><span class="sxs-lookup"><span data-stu-id="0d878-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="0d878-136">Vælg **Udligning på flere niveauer** i gruppen **Krav** under fanen **Vis** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0d878-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="0d878-137">Internt eksempel, der involverer to firmaer</span><span class="sxs-lookup"><span data-stu-id="0d878-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="0d878-138">I dette eksempel oprettes der et produktionsordreforslag i USMF-firmaet, der dækker en salgsordrer i DEMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="0d878-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="0d878-139">I USMF er den direkte efterspørgsel en planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="0d878-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="0d878-140">For at få dette behov vist i USMF, køres varedisponering først i DEMF og derefter i USMF.</span><span class="sxs-lookup"><span data-stu-id="0d878-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="0d878-141">I følgende illustration vises, hvordan dette eksempel kan se ud på siden **Udligning på flere niveauer** for den planlagte produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="0d878-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Internt eksempel, der involverer to firmaer](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="0d878-143">Internt eksempel, der involverer tre firmaer</span><span class="sxs-lookup"><span data-stu-id="0d878-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="0d878-144">I dette eksempel oprettes der et indkøbsordreforslag i USMF-firmaet, der dækker en salgsordrer i FRRT-firmaet.</span><span class="sxs-lookup"><span data-stu-id="0d878-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="0d878-145">I firmaerne DEMF og USMF er den direkte efterspørgsel en planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="0d878-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="0d878-146">For at få dette behov vist i USMF, køres varedisponering først i FRRT , derefter i DEMF og til sidst i USMF.</span><span class="sxs-lookup"><span data-stu-id="0d878-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="0d878-147">I følgende illustration vises, hvordan dette eksempel kan se ud på siden **Udligning på flere niveauer** for den planlagte produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="0d878-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Internt eksempel, der involverer tre firmaer](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]