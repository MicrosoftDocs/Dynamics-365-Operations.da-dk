---
title: Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed
description: Regler for omkostningsfordeling bruges til at fordele omkostninger, der er optalt i økonomisk sammenhæng på en kollektiv bærer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d040f9495c7fb36985b5f96c15ac43aa226da24
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841315"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="e1204-103">Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="e1204-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1204-104">Regler for omkostningsfordeling bruges til at fordele omkostninger, der er optalt i økonomisk sammenhæng på en kollektiv bærer.</span><span class="sxs-lookup"><span data-stu-id="e1204-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="e1204-105">Bogholderen sikrer, at omkostningerne fordeles til bærerne baseret på den valgte fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="e1204-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="e1204-106">En politik og de tilsvarende regler tildeles til en enhed til en omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="e1204-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="e1204-107">Denne opgaveguide bruger et eksempel til at vise, hvordan du opretter en politik for fordeling af omkostninger og de tilsvarende regler.</span><span class="sxs-lookup"><span data-stu-id="e1204-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="e1204-108">Oprette en politik</span><span class="sxs-lookup"><span data-stu-id="e1204-108">Create a policy</span></span>
1. <span data-ttu-id="e1204-109">Gå til Omkostningsregnskab > Politikker > Politikker for omkostningsfordeling.</span><span class="sxs-lookup"><span data-stu-id="e1204-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="e1204-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1204-110">Click New.</span></span>
3. <span data-ttu-id="e1204-111">Angiv en værdi i feltet Navn på politik.</span><span class="sxs-lookup"><span data-stu-id="e1204-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="e1204-112">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e1204-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e1204-113">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e1204-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-114">Vælg organisation.</span><span class="sxs-lookup"><span data-stu-id="e1204-114">Select Organization.</span></span>  
6. <span data-ttu-id="e1204-115">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="e1204-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-116">Vælg CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="e1204-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="e1204-117">Indtast eller vælg en værdi i feltet Statistisk dimension.</span><span class="sxs-lookup"><span data-stu-id="e1204-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-118">Vælg Statistiske elementer.</span><span class="sxs-lookup"><span data-stu-id="e1204-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="e1204-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1204-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="e1204-120">Oprette regler for politikken</span><span class="sxs-lookup"><span data-stu-id="e1204-120">Create rules for the policy</span></span>
1. <span data-ttu-id="e1204-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1204-121">Click New.</span></span>
2. <span data-ttu-id="e1204-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e1204-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e1204-123">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e1204-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-124">Udvid hierarkiet ved at vælge 094.</span><span class="sxs-lookup"><span data-stu-id="e1204-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="e1204-125">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="e1204-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-126">Vælge Andre driftsudgifter, og vælg derefter 605110 Rengøring.</span><span class="sxs-lookup"><span data-stu-id="e1204-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="e1204-127">Vælg en indstilling i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="e1204-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="e1204-128">Vælg Fast omkostning.</span><span class="sxs-lookup"><span data-stu-id="e1204-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="e1204-129">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="e1204-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="e1204-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1204-130">Click New.</span></span>
8. <span data-ttu-id="e1204-131">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e1204-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e1204-132">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e1204-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-133">Udvid hierarkiet ved at vælge 094.</span><span class="sxs-lookup"><span data-stu-id="e1204-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="e1204-134">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="e1204-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="e1204-135">Vælge Andre driftsudgifter, og vælg derefter 605150 Leje.</span><span class="sxs-lookup"><span data-stu-id="e1204-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="e1204-136">Vælg en indstilling i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="e1204-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="e1204-137">Vælg Fast omkostning.</span><span class="sxs-lookup"><span data-stu-id="e1204-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="e1204-138">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="e1204-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="e1204-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1204-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="e1204-140">Tildele regler til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="e1204-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="e1204-141">Klik på Politiktildelinger for omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="e1204-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="e1204-142">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e1204-142">Click New.</span></span>
3. <span data-ttu-id="e1204-143">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e1204-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e1204-144">Indtast en dato i feltet Gyldig fra regnskabsdato.</span><span class="sxs-lookup"><span data-stu-id="e1204-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="e1204-145">Vælg den 1. september i det regnskabsår, der gælder.</span><span class="sxs-lookup"><span data-stu-id="e1204-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="e1204-146">Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="e1204-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="e1204-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1204-147">Click Save.</span></span>

