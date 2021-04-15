---
title: Oprette en politik for omkostningstotaler
description: Denne procedure viser, hvordan du opretter en politik for omkostningstotaler og opretter regler for politikken.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50a50dc359dc4c2741ac4d280a9f97c6a7f2c259
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810008"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="2f765-103">Oprette en politik for omkostningstotaler</span><span class="sxs-lookup"><span data-stu-id="2f765-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f765-104">Denne procedure viser, hvordan du opretter en politik for omkostningstotaler og opretter regler for politikken.</span><span class="sxs-lookup"><span data-stu-id="2f765-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="2f765-105">De demodata, der bruges til at oprette denne procedure, er USP2.</span><span class="sxs-lookup"><span data-stu-id="2f765-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="2f765-106">Oprette en politik</span><span class="sxs-lookup"><span data-stu-id="2f765-106">Create a policy</span></span>
1. <span data-ttu-id="2f765-107">Gå til Omkostningsregnskab > Politikker > Politik for omkostningstotaler.</span><span class="sxs-lookup"><span data-stu-id="2f765-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="2f765-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2f765-108">Click New.</span></span>
3. <span data-ttu-id="2f765-109">Angiv en værdi i feltet Navn på politik.</span><span class="sxs-lookup"><span data-stu-id="2f765-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="2f765-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2f765-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2f765-111">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2f765-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-112">Vælg Omkostningstotaler CC.</span><span class="sxs-lookup"><span data-stu-id="2f765-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="2f765-113">Indtast eller vælg en værdi i feltet Dimensionshierarki for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-114">Vælg Omkostningstotaler CC.</span><span class="sxs-lookup"><span data-stu-id="2f765-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="2f765-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2f765-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="2f765-116">Oprette regler for politikken for omkostningstotaler</span><span class="sxs-lookup"><span data-stu-id="2f765-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="2f765-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2f765-117">Click New.</span></span>
2. <span data-ttu-id="2f765-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2f765-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2f765-119">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2f765-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-120">Vælg 007.</span><span class="sxs-lookup"><span data-stu-id="2f765-120">Select 007.</span></span>  
4. <span data-ttu-id="2f765-121">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-122">Vælg Omkostningstotaler CE.</span><span class="sxs-lookup"><span data-stu-id="2f765-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="2f765-123">Indtast eller vælg en værdi i feltet Sekundært omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-124">I dette eksempel skal du knytte det sekundære omkostningselement CC-007 til bæreren.</span><span class="sxs-lookup"><span data-stu-id="2f765-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="2f765-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2f765-125">Click New.</span></span>
7. <span data-ttu-id="2f765-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2f765-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="2f765-127">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2f765-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-128">Vælg 008.</span><span class="sxs-lookup"><span data-stu-id="2f765-128">Select 008.</span></span>  
9. <span data-ttu-id="2f765-129">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-130">Vælg Omkostningstotaler CE.</span><span class="sxs-lookup"><span data-stu-id="2f765-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="2f765-131">Indtast eller vælg en værdi i feltet Sekundært omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-132">I dette eksempel skal du knytte det sekundære omkostningselement CC-008 til bæreren.</span><span class="sxs-lookup"><span data-stu-id="2f765-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="2f765-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="2f765-133">Click New.</span></span>
12. <span data-ttu-id="2f765-134">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2f765-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="2f765-135">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2f765-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-136">Vælg 009.</span><span class="sxs-lookup"><span data-stu-id="2f765-136">Select 009.</span></span>  
14. <span data-ttu-id="2f765-137">Indtast eller vælg en værdi i feltet Dimensionshierarkinode for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-138">Vælg Omkostningstotaler CE.</span><span class="sxs-lookup"><span data-stu-id="2f765-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="2f765-139">Indtast eller vælg en værdi i feltet Sekundært omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="2f765-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="2f765-140">I dette eksempel skal du knytte det sekundære omkostningselement CC-009 til bæreren.</span><span class="sxs-lookup"><span data-stu-id="2f765-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="2f765-141">Fortsæt, indtil alle bærere er knyttet til de tilsvarende sekundære omkostningselementer.</span><span class="sxs-lookup"><span data-stu-id="2f765-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="2f765-142">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2f765-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]