---
title: Planlægning med negative disponible lagerantal
description: I dette emne beskrives, hvordan negative lagerbeholdninger håndteres, når du bruger planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323502"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="5c819-103">Planlægning med negative disponible lagerantal</span><span class="sxs-lookup"><span data-stu-id="5c819-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c819-104">Hvis systemet viser et negativt samlet disponibelt lagerantal, behandler planlægningsmotoren antallet som 0 (nul) for at undgå overforsyning.</span><span class="sxs-lookup"><span data-stu-id="5c819-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="5c819-105">Funktionen fungerer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5c819-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="5c819-106">Planlægningsoptimeringsfunktionen aggregerer de disponible antal i det laveste niveau af disponeringsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="5c819-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="5c819-107">(Hvis f.eks. *sted* ikke er en disponeringsdimension, aggregerer planlægningsoptimering antallet på *lagersteds*-niveau.)</span><span class="sxs-lookup"><span data-stu-id="5c819-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="5c819-108">Hvis det samlede disponible antal på det laveste niveau af disponeringsdimensionen er negativt, antager systemet, at den disponible mængde er 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="5c819-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c819-109">Planlægningssystemet kan være så præcist som inputdata.</span><span class="sxs-lookup"><span data-stu-id="5c819-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="5c819-110">Hvis inputdataene er unøjagtige, vil negative poster i den disponible beholdning angive, at lageroplysningerne i Microsoft Dynamics 365 Supply Chain Management ikke er synkroniseret med den virkelige verden.</span><span class="sxs-lookup"><span data-stu-id="5c819-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="5c819-111">Derfor vil planlægningsresultatet være fejlbehæftet.</span><span class="sxs-lookup"><span data-stu-id="5c819-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="5c819-112">Hvis du vil have et præcist planlægningsresultat, skal du minimere antallet af poster, der viser et negativt antal.</span><span class="sxs-lookup"><span data-stu-id="5c819-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="5c819-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="5c819-113">Example 1</span></span>

<span data-ttu-id="5c819-114">Lagersted 13 er konfigureret på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5c819-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="5c819-115">**Dækningskode:** Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="5c819-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="5c819-116">**Minimum:** 15 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="5c819-117">**Maksimum:** 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="5c819-118">Det laveste niveau for disponeringsdimensioner er *lagersted*, og det følgende disponible antal registreres på *sted*-niveau:</span><span class="sxs-lookup"><span data-stu-id="5c819-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="5c819-119">**Sted 1, lagersted 13, sted 1** : 20 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="5c819-120">**Sted 1 lagersted 13, sted 2:** &minus;8 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="5c819-121">Den samlede disponible beholdning for lagersted 13 er derfor 12 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="5c819-122">(= 20 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-122">(= 20 pcs.</span></span> <span data-ttu-id="5c819-123">&minus; 8 stk.).</span><span class="sxs-lookup"><span data-stu-id="5c819-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="5c819-124">I dette tilfælde bruger planlægningsprogrammet et samlet disponibelt antal på 12 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="5c819-125">til lagersted 13.</span><span class="sxs-lookup"><span data-stu-id="5c819-125">for warehouse 13.</span></span>

<span data-ttu-id="5c819-126">Resultatet er en planlagt ordre på 13 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="5c819-127">(= 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-127">(= 25 pcs.</span></span> <span data-ttu-id="5c819-128">&minus; 12 stk.) til påfyldning af lagersted 13 fra 12 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="5c819-129">til 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="5c819-130">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="5c819-130">Example 2</span></span>

<span data-ttu-id="5c819-131">Lagersted 13 er konfigureret på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="5c819-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="5c819-132">**Dækningskode:** Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="5c819-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="5c819-133">**Minimum:** 15 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="5c819-134">**Maksimum:** 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="5c819-135">Det laveste niveau for disponeringsdimensioner er *lagersted*, og det følgende disponible antal registreres på *sted*-niveau:</span><span class="sxs-lookup"><span data-stu-id="5c819-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="5c819-136">**Sted 1, lagersted 13, sted 1** : 4 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="5c819-137">**Sted 1 lagersted 13, sted 2:** &minus;8 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="5c819-138">Den samlede disponible beholdning for lagersted 13 er derfor &minus;4 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="5c819-139">(= 4 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-139">(= 4 pcs.</span></span> <span data-ttu-id="5c819-140">&minus; 8 stk.).</span><span class="sxs-lookup"><span data-stu-id="5c819-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="5c819-141">Den er med andre ord mindre end 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="5c819-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="5c819-142">I dette tilfælde antager planlægningsprogrammet, at den disponible beholdning for lagersted 13 er 0 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="5c819-143">I stedet for &minus;4 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="5c819-144">Resultatet er en planlagt ordre på 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="5c819-145">(= 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-145">(= 25 pcs.</span></span> <span data-ttu-id="5c819-146">&minus; 0 stk.) til påfyldning af lagersted 13 fra 0 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="5c819-147">til 25 stk.</span><span class="sxs-lookup"><span data-stu-id="5c819-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5c819-148">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="5c819-148">Related resources</span></span>

[<span data-ttu-id="5c819-149">Oversigt over planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="5c819-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5c819-150">Kom i gang med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="5c819-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5c819-151">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="5c819-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5c819-152">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="5c819-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5c819-153">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="5c819-153">Cancel a planning job</span></span>](cancel-planning-job.md)
