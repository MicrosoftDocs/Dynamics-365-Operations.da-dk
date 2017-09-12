--- 
title: "Oprette en kanban-regel for salgshændelse"
description: "Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en kanban-regel, som udløses under oprettelse af en salgsordre."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 33ae479a8479732a1857577743a22068d2059a47
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="6b04d-103">Oprette en kanban-regel for salgshændelse</span><span class="sxs-lookup"><span data-stu-id="6b04d-103">Create a sales event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b04d-104">Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en kanban-regel, som udløses under oprettelse af en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="6b04d-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="6b04d-105">Hændelses-kanban-reglen genbestiller krav, der stammer fra salgsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="6b04d-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="6b04d-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6b04d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6b04d-107">Den er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt.</span><span class="sxs-lookup"><span data-stu-id="6b04d-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="6b04d-108">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="6b04d-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="6b04d-109">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="6b04d-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="6b04d-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6b04d-110">Click New.</span></span>
3. <span data-ttu-id="6b04d-111">Vælg "Hændelse" i feltet Genopfyldningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="6b04d-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="6b04d-112">Hvis Hændelse vælges, betyder det, at kanban-reglen udløses af en hændelse, for eksempel oprettelse af en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="6b04d-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="6b04d-113">Dette gælder for områder, hvor hver kanban skal dække et specifikt behov.</span><span class="sxs-lookup"><span data-stu-id="6b04d-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="6b04d-114">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="6b04d-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="6b04d-115">Vælg Endelig samling.</span><span class="sxs-lookup"><span data-stu-id="6b04d-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="6b04d-116">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="6b04d-116">Expand the Details section.</span></span>
6. <span data-ttu-id="6b04d-117">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="6b04d-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="6b04d-118">Vælg L0050.</span><span class="sxs-lookup"><span data-stu-id="6b04d-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="6b04d-119">Definere en hændelse</span><span class="sxs-lookup"><span data-stu-id="6b04d-119">Define an event</span></span>
1. <span data-ttu-id="6b04d-120">Udvid afsnittet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="6b04d-120">Expand the Events section.</span></span>
2. <span data-ttu-id="6b04d-121">Vælg "Automatisk" i feltet Salgshændelse.</span><span class="sxs-lookup"><span data-stu-id="6b04d-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="6b04d-122">Hvis salgshændelsen Automatisk vælges, udløses denne kanban-reglen automatisk, når en salgslinje svarer til produktet og modtagelseslokaliteten.</span><span class="sxs-lookup"><span data-stu-id="6b04d-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="6b04d-123">I denne procedure er det produkt L0050 på lager 13.</span><span class="sxs-lookup"><span data-stu-id="6b04d-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="6b04d-124">Angiv Mindste antal hændelser "50".</span><span class="sxs-lookup"><span data-stu-id="6b04d-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="6b04d-125">Med et minimumantal af hændelser på 50 udløses kanban-reglen kun af hændelser med et antal på 50 eller derover.</span><span class="sxs-lookup"><span data-stu-id="6b04d-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="6b04d-126">Udvid sektionen Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="6b04d-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="6b04d-127">Bemærk, at Modtagelseslokalitet er lager 13.</span><span class="sxs-lookup"><span data-stu-id="6b04d-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="6b04d-128">Det betyder, at denne kanban-regel udløses for denne lokalitet.</span><span class="sxs-lookup"><span data-stu-id="6b04d-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="6b04d-129">I dette eksempel udløses kanban-reglen af en salgslinje for produktet L0050 med et antal på 50 eller derover på lager 13.</span><span class="sxs-lookup"><span data-stu-id="6b04d-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="6b04d-130">Oprette salgslinje for at udløse hændelses-kanban-regel</span><span class="sxs-lookup"><span data-stu-id="6b04d-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="6b04d-131">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="6b04d-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="6b04d-132">Der vises en advarsel, når kanban-reglen gemmes, hvilket betyder, at der oprettes kanbans i realtid under oprettelse af salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="6b04d-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="6b04d-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6b04d-133">Click New.</span></span>
3. <span data-ttu-id="6b04d-134">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="6b04d-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="6b04d-135">Vælg f.eks. US-003.</span><span class="sxs-lookup"><span data-stu-id="6b04d-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="6b04d-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6b04d-136">Click OK.</span></span>
5. <span data-ttu-id="6b04d-137">Skriv 'L0050' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="6b04d-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="6b04d-138">Skriv "1" i feltet Sted.</span><span class="sxs-lookup"><span data-stu-id="6b04d-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="6b04d-139">Vælg Sted 1, fordi lageret 13 er på Sted 1.</span><span class="sxs-lookup"><span data-stu-id="6b04d-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="6b04d-140">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="6b04d-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6b04d-141">Angiv Lagersted til 13.</span><span class="sxs-lookup"><span data-stu-id="6b04d-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="6b04d-142">Angiv antallet til '75'.</span><span class="sxs-lookup"><span data-stu-id="6b04d-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="6b04d-143">Angiv et mængde på 50 eller derover for at udløse den oprettede kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="6b04d-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="6b04d-144">Kontroller, at kanban er oprettet</span><span class="sxs-lookup"><span data-stu-id="6b04d-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="6b04d-145">Klik på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="6b04d-145">Click Product and supply.</span></span>
2. <span data-ttu-id="6b04d-146">Klik på Vis udligningstræ.</span><span class="sxs-lookup"><span data-stu-id="6b04d-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="6b04d-147">Bemærk, at der oprettes en kanban med den samme mængde som salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="6b04d-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="6b04d-148">Du kan også se de materialeproblemer, der er nødvendige for at producere L0050.</span><span class="sxs-lookup"><span data-stu-id="6b04d-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="6b04d-149">Dette er det sidste trin i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="6b04d-149">This is the last step in this procedure.</span></span>  


