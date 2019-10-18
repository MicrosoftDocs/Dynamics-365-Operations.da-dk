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
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176979"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="53048-103">Oprette og tildele omkostningstildelingspolitik til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="53048-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53048-104">Du kan bruge denne procedure til at oprette og tildele en politik for omkostningsfordeling og de tilsvarende regler til en omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="53048-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="53048-105">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="53048-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="53048-106">Oprette en politik</span><span class="sxs-lookup"><span data-stu-id="53048-106">Create a policy</span></span>
1. <span data-ttu-id="53048-107">Gå til Omkostningsregnskab > Politikker > Politikker for omkostningstildeling.</span><span class="sxs-lookup"><span data-stu-id="53048-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="53048-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53048-108">Click New.</span></span>
3. <span data-ttu-id="53048-109">Angiv en værdi i feltet Navn på politik.</span><span class="sxs-lookup"><span data-stu-id="53048-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="53048-110">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="53048-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="53048-111">Vælg organisation.</span><span class="sxs-lookup"><span data-stu-id="53048-111">Select Organization.</span></span>  
5. <span data-ttu-id="53048-112">Indtast eller vælg en værdi i feltet Statistisk dimension.</span><span class="sxs-lookup"><span data-stu-id="53048-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="53048-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="53048-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="53048-114">Oprette fordelingsregler</span><span class="sxs-lookup"><span data-stu-id="53048-114">Create allocation rules</span></span>
1. <span data-ttu-id="53048-115">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53048-115">Click New.</span></span>
2. <span data-ttu-id="53048-116">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53048-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="53048-117">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="53048-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="53048-118">Vælg 'Total' i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="53048-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="53048-119">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="53048-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="53048-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53048-120">Click New.</span></span>
7. <span data-ttu-id="53048-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53048-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="53048-122">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="53048-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="53048-123">Vælg 'Total' i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="53048-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="53048-124">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="53048-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="53048-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53048-125">Click New.</span></span>
12. <span data-ttu-id="53048-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53048-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="53048-127">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="53048-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="53048-128">Vælg 'Total' i feltet Funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="53048-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="53048-129">Indtast eller vælg en værdi i feltet Fordelingsbasis.</span><span class="sxs-lookup"><span data-stu-id="53048-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="53048-130">Fortsæt, indtil du har oprettet alle regler.</span><span class="sxs-lookup"><span data-stu-id="53048-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="53048-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="53048-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="53048-132">Tildele politikken til en omkostningskontrolenhed</span><span class="sxs-lookup"><span data-stu-id="53048-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="53048-133">Klik på Politiktildelinger for omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="53048-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="53048-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53048-134">Click New.</span></span>
3. <span data-ttu-id="53048-135">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53048-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="53048-136">Indtast en dato i feltet Gyldig fra regnskabsdato.</span><span class="sxs-lookup"><span data-stu-id="53048-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="53048-137">Reglerne er datorelaterede.</span><span class="sxs-lookup"><span data-stu-id="53048-137">The rules are date-effective.</span></span> <span data-ttu-id="53048-138">En bruger eller systemet kan lade reglerne udløbe, hvis der oprettes en nyere version.</span><span class="sxs-lookup"><span data-stu-id="53048-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="53048-139">Indtast eller vælg en værdi i feltet Omkostningskontrolenhed.</span><span class="sxs-lookup"><span data-stu-id="53048-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="53048-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="53048-140">Click Save.</span></span>

