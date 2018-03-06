---
title: Forberede at vedligeholde standardomkostninger for producerede varer
description: I dette emne beskrives trinnene til forberedelse af vedligeholdelse af omkostninger for producerede varer.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 605f4c6391e9c40b1b80fab93d61b88553369069
ms.openlocfilehash: 6f52d2d90d655d1ab465e1808ca55ef3d5ea9e56
ms.contentlocale: da-dk
ms.lasthandoff: 01/19/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="5e95b-103">Forberede at vedligeholde standardomkostninger for producerede varer</span><span class="sxs-lookup"><span data-stu-id="5e95b-103">Prepare to maintain standard costs for manufactured items</span></span>

<span data-ttu-id="5e95b-104">I dette emne beskrives trinnene til forberedelse af vedligeholdelse af omkostninger for producerede varer.</span><span class="sxs-lookup"><span data-stu-id="5e95b-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="5e95b-105">Trinnene for producerede varer varierer en smule fra trinnene for købte varer.</span><span class="sxs-lookup"><span data-stu-id="5e95b-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="5e95b-106">Regler, der er knyttet til producerede varer, kan påvirke omkostningsberegningerne for de overordnede producerede varer.</span><span class="sxs-lookup"><span data-stu-id="5e95b-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="5e95b-107">Benyt følgende fremgangsmåde, hvis du vil forberede vedligeholdelse af omkostninger for producerede varer.</span><span class="sxs-lookup"><span data-stu-id="5e95b-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="5e95b-108">Knyt en varemodelgruppe til den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="5e95b-109">Varemodelgruppen identificerer, at der skal bruges standardomkostninger.</span><span class="sxs-lookup"><span data-stu-id="5e95b-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="5e95b-110">Knyt en varegruppe til den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="5e95b-111">Varegruppen indeholder finanskonti, der gælder for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="5e95b-112">Finanskontiene for en produceret vare, der har en lagermodel af typen standardomkostninger, omfatter flere produktionsafvigelser, en ændring for omkostningsafvigelse og værdiregulering af lageromkostninger.</span><span class="sxs-lookup"><span data-stu-id="5e95b-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="5e95b-113">Knyt måleenheder for lageret til varen.</span><span class="sxs-lookup"><span data-stu-id="5e95b-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="5e95b-114">Varens omkostninger er altid udtrykt i varens måleenhed for lageret.</span><span class="sxs-lookup"><span data-stu-id="5e95b-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="5e95b-115">Du skal ikke knytte en kostprisgruppe til den producerede vare, medmindre varen skal behandles som en købt vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="5e95b-116">Knyt en styklisteberegningsgruppe til den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="5e95b-117">Varens styklisteberegningsgruppe definerer advarselssituationer, der gælder.</span><span class="sxs-lookup"><span data-stu-id="5e95b-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="5e95b-118">På denne måde, kan advarselsmeddelelser, når der udføres en styklisteberegning, oprettes om mulige kilder til beregningsfejl.</span><span class="sxs-lookup"><span data-stu-id="5e95b-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="5e95b-119">En advarsel kan f.eks. identificere, hvornår der ikke findes en aktiv stykliste eller rute.</span><span class="sxs-lookup"><span data-stu-id="5e95b-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="5e95b-120">Styklisteberegningsgruppen indeholder en regel om stop af udfoldning, der angiver, hvornår en produceret vare skal behandles som en købt vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="5e95b-121">Hvis den producerede vare har konstante omkostninger, kan du knyt et standardordreantal til den.</span><span class="sxs-lookup"><span data-stu-id="5e95b-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="5e95b-122">Standardordreantallet er en regnskabsmæssig lotstørrelse til amortisering af konstante omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5e95b-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="5e95b-123">Eksempler på konstante omkostninger omfatter opsætningstider i ruteoperationer og et konstant komponentantal på styklisten.</span><span class="sxs-lookup"><span data-stu-id="5e95b-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="5e95b-124">Definer styklisten for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="5e95b-125">Der kan defineres en eller flere styklisteversioner for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="5e95b-126">Kontroller, at de versioner, du ønsker, er markeret som godkendt og aktive, og at de har de ønskede ikrafttrædelsesdatoer.</span><span class="sxs-lookup"><span data-stu-id="5e95b-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="5e95b-127">Styklisteversionen kan gælde for hele firmaet eller være lokationsspecifik.</span><span class="sxs-lookup"><span data-stu-id="5e95b-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="5e95b-128">Definer ruten for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="5e95b-129">Der kan defineres en eller flere ruter for den producerede vare.</span><span class="sxs-lookup"><span data-stu-id="5e95b-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="5e95b-130">Kontroller, at de versioner, du ønsker, er markeret som godkendt og aktive, og at de har de ønskede ikrafttrædelsesdatoer.</span><span class="sxs-lookup"><span data-stu-id="5e95b-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="5e95b-131">Ruten skal være lokationsspecifik.</span><span class="sxs-lookup"><span data-stu-id="5e95b-131">The route version must be site-specific.</span></span>

<span data-ttu-id="5e95b-132">Hvis du vil bruge ruteoplysninger i forbindelse med efterkalkulation, er der brug for flere trin i forberedelsen.</span><span class="sxs-lookup"><span data-stu-id="5e95b-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="5e95b-133">Omkostningskategorier, der er knyttet til ruteoperationer, skal f.eks. være korrekte og fuldførte.</span><span class="sxs-lookup"><span data-stu-id="5e95b-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="5e95b-134">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="5e95b-134">Related topics</span></span>
--------

[<span data-ttu-id="5e95b-135">Amortisere konstante omkostninger for en produceret vare</span><span class="sxs-lookup"><span data-stu-id="5e95b-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="5e95b-136">Konfigurere produkter, som kan være produceret eller indkøbt</span><span class="sxs-lookup"><span data-stu-id="5e95b-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

