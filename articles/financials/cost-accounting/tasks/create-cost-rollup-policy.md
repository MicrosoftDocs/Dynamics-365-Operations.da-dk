--- 
title: Oprette en politik for omkostningstotaler
description: Denne procedure viser, hvordan du opretter en politik for omkostningstotaler og opretter regler for politikken.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="31ca2-103">Oprette en politik for omkostningstotaler</span><span class="sxs-lookup"><span data-stu-id="31ca2-103">Create a cost rollup policy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31ca2-104">Denne procedure viser, hvordan du opretter en politik for omkostningstotaler og opretter regler for politikken.</span><span class="sxs-lookup"><span data-stu-id="31ca2-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="31ca2-105">De demodata, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="31ca2-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="31ca2-106">Oprette en politik</span><span class="sxs-lookup"><span data-stu-id="31ca2-106">Create a policy</span></span>
1. <span data-ttu-id="31ca2-107">Gå til Omkostningsregnskab > Politikker > Politik for omkostningstotaler.</span><span class="sxs-lookup"><span data-stu-id="31ca2-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="31ca2-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="31ca2-108">Click New.</span></span>
3. <span data-ttu-id="31ca2-109">Angiv en værdi i feltet Navn på politik.</span><span class="sxs-lookup"><span data-stu-id="31ca2-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="31ca2-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="31ca2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="31ca2-111">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="31ca2-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-112">Vælg Omkostningstotaler CC.</span><span class="sxs-lookup"><span data-stu-id="31ca2-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="31ca2-113">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-114">Vælg Omkostningstotaler CC.</span><span class="sxs-lookup"><span data-stu-id="31ca2-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="31ca2-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="31ca2-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="31ca2-116">Oprette regler for politikken for omkostningstotaler</span><span class="sxs-lookup"><span data-stu-id="31ca2-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="31ca2-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="31ca2-117">Click New.</span></span>
2. <span data-ttu-id="31ca2-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="31ca2-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="31ca2-119">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="31ca2-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-120">Vælg 007.</span><span class="sxs-lookup"><span data-stu-id="31ca2-120">Select 007.</span></span>  
4. <span data-ttu-id="31ca2-121">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-122">Vælg Omkostningstotaler CE.</span><span class="sxs-lookup"><span data-stu-id="31ca2-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="31ca2-123">Indtast eller vælg en værdi i feltet Sekundært omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-124">I dette eksempel skal du knytte det sekundære omkostningselement CC-007 til bæreren.</span><span class="sxs-lookup"><span data-stu-id="31ca2-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="31ca2-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="31ca2-125">Click New.</span></span>
7. <span data-ttu-id="31ca2-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="31ca2-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="31ca2-127">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="31ca2-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-128">Vælg 008.</span><span class="sxs-lookup"><span data-stu-id="31ca2-128">Select 008.</span></span>  
9. <span data-ttu-id="31ca2-129">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-130">Vælg Omkostningstotaler CE.</span><span class="sxs-lookup"><span data-stu-id="31ca2-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="31ca2-131">Indtast eller vælg en værdi i feltet Sekundært omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-132">I dette eksempel skal du knytte det sekundære omkostningselement CC-008 til bæreren.</span><span class="sxs-lookup"><span data-stu-id="31ca2-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="31ca2-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="31ca2-133">Click New.</span></span>
12. <span data-ttu-id="31ca2-134">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="31ca2-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="31ca2-135">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="31ca2-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-136">Vælg 009.</span><span class="sxs-lookup"><span data-stu-id="31ca2-136">Select 009.</span></span>  
14. <span data-ttu-id="31ca2-137">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-138">Vælg Omkostningstotaler CE.</span><span class="sxs-lookup"><span data-stu-id="31ca2-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="31ca2-139">Indtast eller vælg en værdi i feltet Sekundært omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="31ca2-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="31ca2-140">I dette eksempel skal du knytte det sekundære omkostningselement CC-009 til bæreren.</span><span class="sxs-lookup"><span data-stu-id="31ca2-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="31ca2-141">Fortsæt, indtil alle bærere er knyttet til de tilsvarende sekundære omkostningselementer.</span><span class="sxs-lookup"><span data-stu-id="31ca2-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="31ca2-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="31ca2-142">Click Save.</span></span>


