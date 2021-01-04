---
title: Oprette og tildele omkostningstildelingspolitik til en omkostningskontrolenhed
description: Du kan bruge denne procedure til at oprette og tildele en politik for omkostningsfordeling og de tilsvarende regler til en omkostningskontrolenhed.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad95752ce40faaa84747dac9bfbf2887f7a5af42
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441706"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="80951-103">Oprette og tildele omkostningstildelingspolitik til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="80951-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80951-104">Du kan bruge denne procedure til at oprette og tildele en politik for omkostningsfordeling og de tilsvarende regler til en omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="80951-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="80951-105">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="80951-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="80951-106">Oprette en politik</span><span class="sxs-lookup"><span data-stu-id="80951-106">Create a policy</span></span>
1. <span data-ttu-id="80951-107">Gå til Omkostningsregnskab > Politikker > Politikker for omkostningstildeling.</span><span class="sxs-lookup"><span data-stu-id="80951-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="80951-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="80951-108">Click New.</span></span>
3. <span data-ttu-id="80951-109">Angiv en værdi i feltet Navn på politik.</span><span class="sxs-lookup"><span data-stu-id="80951-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="80951-110">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="80951-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="80951-111">Vælg organisation.</span><span class="sxs-lookup"><span data-stu-id="80951-111">Select Organization.</span></span>  
5. <span data-ttu-id="80951-112">Indtast eller vælg en værdi i feltet Statistisk dimension.</span><span class="sxs-lookup"><span data-stu-id="80951-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="80951-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="80951-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="80951-114">Oprette fordelingsregler</span><span class="sxs-lookup"><span data-stu-id="80951-114">Create allocation rules</span></span>
1. <span data-ttu-id="80951-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="80951-115">Click New.</span></span>
2. <span data-ttu-id="80951-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="80951-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="80951-117">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="80951-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="80951-118">Vælg 'Total' i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="80951-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="80951-119">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="80951-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="80951-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="80951-120">Click New.</span></span>
7. <span data-ttu-id="80951-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="80951-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="80951-122">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="80951-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="80951-123">Vælg 'Total' i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="80951-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="80951-124">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="80951-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="80951-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="80951-125">Click New.</span></span>
12. <span data-ttu-id="80951-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="80951-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="80951-127">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="80951-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="80951-128">Vælg 'Total' i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="80951-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="80951-129">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="80951-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="80951-130">Fortsæt, indtil du har oprettet alle regler.</span><span class="sxs-lookup"><span data-stu-id="80951-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="80951-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="80951-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="80951-132">Tildele politikken til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="80951-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="80951-133">Klik på Politiktildelinger for omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="80951-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="80951-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="80951-134">Click New.</span></span>
3. <span data-ttu-id="80951-135">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="80951-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="80951-136">Indtast en dato i feltet Gyldig fra regnskabsdato.</span><span class="sxs-lookup"><span data-stu-id="80951-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="80951-137">Reglerne er datorelaterede.</span><span class="sxs-lookup"><span data-stu-id="80951-137">The rules are date-effective.</span></span> <span data-ttu-id="80951-138">En bruger eller systemet kan lade reglerne udløbe, hvis der oprettes en nyere version.</span><span class="sxs-lookup"><span data-stu-id="80951-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="80951-139">Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="80951-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="80951-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="80951-140">Click Save.</span></span>

