---
title: "Delvis cyklusoptælling for sted"
description: "Cyklusoptællingsplaner guider de faktiske optællingshandlinger. Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0e72df11e8fc4a43d74a6fe596a223266ddf5b09
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="bac66-104">Delvis cyklusoptælling for sted</span><span class="sxs-lookup"><span data-stu-id="bac66-104">Partial location cycle counting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bac66-105">Cyklusoptællingsplaner guider de faktiske optællingshandlinger.</span><span class="sxs-lookup"><span data-stu-id="bac66-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="bac66-106">Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet.</span><span class="sxs-lookup"><span data-stu-id="bac66-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="bac66-107">Ved at bruge cyklusoptællingsplaner til at oprette optællingsarbejde kan du styre de faktiske optællingshandlinger.</span><span class="sxs-lookup"><span data-stu-id="bac66-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="bac66-108">Du kan anmode om, at kun specifikke produkter og produktvarianter optælles i stedet for alle disponible lagerbeholdninger på en lokalitet.</span><span class="sxs-lookup"><span data-stu-id="bac66-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="bac66-109">Ved at filtrere på bestemte produkter kan lagerchefen reducere evalueringsomkostninger, undgå konsolideringsfejl og spare tid.</span><span class="sxs-lookup"><span data-stu-id="bac66-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="bac66-110">Sådan konfigureres delvis cyklusoptælling for sted</span><span class="sxs-lookup"><span data-stu-id="bac66-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="bac66-111">Når du bruger lagerstedsarbejdsprocesser til optællingshandlinger, oprettes der en opgaveoverskrift for hvert sted.</span><span class="sxs-lookup"><span data-stu-id="bac66-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="bac66-112">Når du definerer cyklusoptællingsplanen, kan du bruge forespørgslen **Vælg lokationer** for at begrænse det cyklusoptællingsarbejde, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="bac66-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="bac66-113">Når du vælger produkter til cyklusoptællingsplanen, kan du vælge både produkt- og produktvariantforespørgsler for at præcisere, hvad der skal optælles.</span><span class="sxs-lookup"><span data-stu-id="bac66-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="bac66-114">Du kan knytte en **arbejdsskabelon** til en cyklusoptællingsplan for at definere, hvordan cyklusoptællingsarbejdet skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="bac66-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="bac66-115">Der henvises direkte til arbejdsskabelonen til cyklusoptællingshandlinger fra cyklusoptællingsplanen.</span><span class="sxs-lookup"><span data-stu-id="bac66-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="bac66-116">Når du definerer oplysningerne i arbejdsskabelonen, kan du bruge indstillingen **Arbejdslinjeskift** til at angive, om optællingsarbejdslinjerne skal grupperes efter varenummer eller produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="bac66-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="bac66-117">Denne opsætning er påkrævet, hvis der kun skal optælles disponible lagerbeholdninger for bestemte produkter på en lokalitet.</span><span class="sxs-lookup"><span data-stu-id="bac66-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="bac66-118">De cyklusoptællingsarbejdslinjer, der oprettes, har det oplysningsniveau, du angiver her, og den styrede optællingshandlingen håndteres baseret på dette niveau.</span><span class="sxs-lookup"><span data-stu-id="bac66-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="bac66-119">Hvis du knytter cyklusoptællingsplaner til arbejdsskabeloner ved hjælp af indstillingen **Arbejdslinjeskift**, markeres feltet **Delvis cyklusoptælling** for det cyklusoptællingsarbejde, der oprettes, og flere cyklusoptællingsarbejdslinjer oprettes på baggrund af definitionen af arbejdsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="bac66-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="bac66-120">Før delvis cyklusoptællingsarbejde kan behandles, skal du som minimum vælge **Vis varenummer** for menupunktet på mobilenheden som et led i opsætningen af cyklusoptællingen.</span><span class="sxs-lookup"><span data-stu-id="bac66-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="bac66-121">Operatøren på lagerstedet bliver bedt om kun at registrere kun optællingsoplysninger, der er relateret til optællingslinjerne (varenumre og produktdimensioner).</span><span class="sxs-lookup"><span data-stu-id="bac66-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="bac66-122">Alle andre disponible lagerbeholdninger bliver ignoreret for denne optællingsproces.</span><span class="sxs-lookup"><span data-stu-id="bac66-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="bac66-123">For den delvise cyklusoptællingsproces bliver dato og klokkeslæt for **Seneste optællingscyklus** ikke opdateret for lokationen.</span><span class="sxs-lookup"><span data-stu-id="bac66-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="bac66-124">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bac66-124">Example</span></span>
<span data-ttu-id="bac66-125">I dette eksempel skal kun varenummer A0001 optælles på lagersted 61.</span><span class="sxs-lookup"><span data-stu-id="bac66-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="bac66-126">Der oprettes en ny arbejdsskabelon for cyklusoptælling.</span><span class="sxs-lookup"><span data-stu-id="bac66-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="bac66-127">Indstillingen **Arbejdslinjeskift** bruges til at gruppere optællingsarbejdslinjer efter varenummer.</span><span class="sxs-lookup"><span data-stu-id="bac66-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="bac66-128">Derfor har det cyklusoptællingsarbejde, der oprettes, linjer pr. varenummer.</span><span class="sxs-lookup"><span data-stu-id="bac66-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="bac66-129">Du kan også gruppere linjerne efter produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="bac66-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="bac66-130">Der oprettes en ny cyklusoptællingsplan, der refererer til den nyoprettede arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="bac66-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="bac66-131">Cyklusoptællingsplanen omfatter alle lokationer på lagersted 61 (forespørgslen **Vælg lokationer**), der har en lagerbeholdning for varenummeret A0001.</span><span class="sxs-lookup"><span data-stu-id="bac66-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="bac66-132">Valget af bestemte produkter defineres i afsnittet **Produktvalg for cyklusoptælling**.</span><span class="sxs-lookup"><span data-stu-id="bac66-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="bac66-133">Du kan vælge produkter til cyklusoptællingsplaner ved at angive feltet **Tomme lokationer** til **Udeluk tomme**.</span><span class="sxs-lookup"><span data-stu-id="bac66-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="bac66-134">Når cyklusoptællingsplanen behandles, oprettes delvist cyklusoptællingsarbejde for varenummer A0001.</span><span class="sxs-lookup"><span data-stu-id="bac66-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="bac66-135">Den faktiske optællingsproces kan udføres ved hjælp af menupunktet for cyklusoptælling på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="bac66-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="bac66-136">Se også</span><span class="sxs-lookup"><span data-stu-id="bac66-136">See also</span></span>
--------

[<span data-ttu-id="bac66-137">Cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="bac66-137">Cycle counting</span></span>](cycle-counting.md)


