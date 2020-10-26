---
title: Oprette og tildele politik for omkostningsfunktionalitet til en omkostningskontrolenhed
description: Omkostningsfunktionalitet er klassificeringen af omkostninger som enten faste eller variable.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfdff9b1af9183d21e988dd53559e749eed077eb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976228"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="d75c9-103">Oprette og tildele politik for omkostningsfunktionalitet til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="d75c9-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d75c9-104">Omkostningsfunktionalitet er klassificeringen af omkostninger som enten faste eller variable.</span><span class="sxs-lookup"><span data-stu-id="d75c9-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="d75c9-105">En politik og de tilsvarende regler skal tildeles til en omkostningskontrolenhed, hvis politikken skal træde i kraft.</span><span class="sxs-lookup"><span data-stu-id="d75c9-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="d75c9-106">Du kan bruge denne procedure til at oprette en politik og derefter tildele politikken til en omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="d75c9-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="d75c9-107">Oprette et hierarki for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="d75c9-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="d75c9-108">Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.</span><span class="sxs-lookup"><span data-stu-id="d75c9-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="d75c9-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-109">Click New.</span></span>
3. <span data-ttu-id="d75c9-110">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="d75c9-110">Click Create.</span></span>
4. <span data-ttu-id="d75c9-111">Skriv 'Hierarki for omkostningsfunktionalitet' i feltet Dimensionshierarki.</span><span class="sxs-lookup"><span data-stu-id="d75c9-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="d75c9-112">Indtast eller vælg en værdi i feltet Dimension.</span><span class="sxs-lookup"><span data-stu-id="d75c9-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-113">Vælg Omkostningselementer.</span><span class="sxs-lookup"><span data-stu-id="d75c9-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="d75c9-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-114">Click Save.</span></span>
7. <span data-ttu-id="d75c9-115">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="d75c9-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="d75c9-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-116">Click New.</span></span>
9. <span data-ttu-id="d75c9-117">Angiv en værdi i feltet Node.</span><span class="sxs-lookup"><span data-stu-id="d75c9-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d75c9-118">Skriv Fast omkostning.</span><span class="sxs-lookup"><span data-stu-id="d75c9-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="d75c9-119">Vælg 'Hierarki for omkostningsfunktionalitet' i træet.</span><span class="sxs-lookup"><span data-stu-id="d75c9-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="d75c9-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-120">Click New.</span></span>
12. <span data-ttu-id="d75c9-121">Angiv en værdi i feltet Node.</span><span class="sxs-lookup"><span data-stu-id="d75c9-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d75c9-122">Angiv Variabel omkostning.</span><span class="sxs-lookup"><span data-stu-id="d75c9-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="d75c9-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-123">Click Save.</span></span>
14. <span data-ttu-id="d75c9-124">Vælg 'Hierarki for omkostningsfunktionalitet\Fast omkostning' i træet.</span><span class="sxs-lookup"><span data-stu-id="d75c9-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="d75c9-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-125">Click New.</span></span>
16. <span data-ttu-id="d75c9-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d75c9-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d75c9-127">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-128">Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="d75c9-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="d75c9-129">Indtast eller vælg en værdi i feltet Til dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-130">Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="d75c9-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="d75c9-131">Vælg 'Hierarki for omkostningsfunktionalitet\Variabel omkostning' i træet.</span><span class="sxs-lookup"><span data-stu-id="d75c9-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="d75c9-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-132">Click New.</span></span>
21. <span data-ttu-id="d75c9-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d75c9-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="d75c9-134">Indtast eller vælg en værdi i feltet Fra dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-135">Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="d75c9-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="d75c9-136">Indtast eller vælg en værdi i feltet Til dimensionsmedlem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-137">Der må gerne være mellemrum mellem dimensionsmedlemmer, men medlemmerne må ikke overlappe hinanden.</span><span class="sxs-lookup"><span data-stu-id="d75c9-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="d75c9-138">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="d75c9-139">Oprette politikken og reglerne</span><span class="sxs-lookup"><span data-stu-id="d75c9-139">Create the policy and rules</span></span>
1. <span data-ttu-id="d75c9-140">Gå til Omkostningsregnskab > Politikker > Politikker for funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="d75c9-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="d75c9-141">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-141">Click New.</span></span>
3. <span data-ttu-id="d75c9-142">Angiv en værdi i feltet Navn på politik.</span><span class="sxs-lookup"><span data-stu-id="d75c9-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d75c9-143">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="d75c9-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-144">Vælg det politikhierarki, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="d75c9-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="d75c9-145">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d75c9-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-146">Vælg organisation.</span><span class="sxs-lookup"><span data-stu-id="d75c9-146">Select Organization.</span></span>  
6. <span data-ttu-id="d75c9-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-147">Click Save.</span></span>
7. <span data-ttu-id="d75c9-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-148">Click New.</span></span>
8. <span data-ttu-id="d75c9-149">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d75c9-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d75c9-150">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="d75c9-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-151">Udvid hierarkiet ved at vælge Variabel omkostning.</span><span class="sxs-lookup"><span data-stu-id="d75c9-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="d75c9-152">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d75c9-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d75c9-153">Som standard er den variable procentdel 100 %.</span><span class="sxs-lookup"><span data-stu-id="d75c9-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="d75c9-154">Klik på Politiktildelinger for omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="d75c9-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="d75c9-155">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d75c9-155">Click New.</span></span>
13. <span data-ttu-id="d75c9-156">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d75c9-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="d75c9-157">Indtast en dato i feltet Gyldig fra regnskabsdato.</span><span class="sxs-lookup"><span data-stu-id="d75c9-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d75c9-158">Reglerne er datorelaterede, og en bruger eller systemet kan lade en regel udløbe, hvis der oprettes en nyere version.</span><span class="sxs-lookup"><span data-stu-id="d75c9-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="d75c9-159">Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="d75c9-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="d75c9-160">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d75c9-160">Click Save.</span></span>

