---
title: Oprette en kanban-regel ved hjælp af en hændelse for minimal lagerbeholdning
description: I denne fremgangsmåde fokuseres der på den opsætning, der er nødvendig for at oprette en kanban-regel ved hjælp af en minimumlagerhændelse for at sikre, at et bestemt produkt altid er tilgængeligt på et bestemt sted.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a9ba8ec2abb26e3b9ee7e14bdf882c1ffcb205b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558520"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="6543a-103">Oprette en kanban-regel ved hjælp af en hændelse for minimal lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="6543a-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6543a-104">I denne fremgangsmåde fokuseres der på den opsætning, der er nødvendig for at oprette en kanban-regel ved hjælp af en minimumlagerhændelse for at sikre, at et bestemt produkt altid er tilgængeligt på et bestemt sted.</span><span class="sxs-lookup"><span data-stu-id="6543a-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="6543a-105">En kanban-regel oprettes for at overføre materiale til stedet, når lagerbeholdningen falder til under 200 enheder.</span><span class="sxs-lookup"><span data-stu-id="6543a-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="6543a-106">Ved at køre behandlingen af udligningshændelsen oprettes de nødvendige kanbans.</span><span class="sxs-lookup"><span data-stu-id="6543a-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="6543a-107">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6543a-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6543a-108">Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="6543a-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="6543a-109">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="6543a-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="6543a-110">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="6543a-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="6543a-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6543a-111">Click New.</span></span>
3. <span data-ttu-id="6543a-112">Vælg 'Udtræk' i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="6543a-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="6543a-113">Denne type bruges til at oprette kanbans til overflytning.</span><span class="sxs-lookup"><span data-stu-id="6543a-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="6543a-114">Vælg "Hændelse" i feltet Genopfyldningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="6543a-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="6543a-115">Strategien Hændelse bruges til at oprette overførslen af kanbans ud fra en hændelse.</span><span class="sxs-lookup"><span data-stu-id="6543a-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="6543a-116">Senere i proceduren udløser du kanbans til overførsel ved hjælp af genopfyldning af lageret.</span><span class="sxs-lookup"><span data-stu-id="6543a-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="6543a-117">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="6543a-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="6543a-118">Indtast eller vælg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="6543a-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="6543a-119">Denne overførselsaktivitet har (output) lagersted og lokation 12 for modtagelsen, hvilket betyder, at materiale flyttes til lokation 12 på lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="6543a-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="6543a-120">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="6543a-120">Expand the Details section.</span></span>
7. <span data-ttu-id="6543a-121">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="6543a-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="6543a-122">Vælg M0007.</span><span class="sxs-lookup"><span data-stu-id="6543a-122">Select M0007.</span></span>  
8. <span data-ttu-id="6543a-123">Udvid afsnittet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="6543a-123">Expand the Events section.</span></span>
9. <span data-ttu-id="6543a-124">Vælg "Batch" i feltet Lagergenopfyldningshændelse.</span><span class="sxs-lookup"><span data-stu-id="6543a-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="6543a-125">Der oprettes kanbans for at opfylde behovet på den relaterede lokation under behandling af udligningshændelser.</span><span class="sxs-lookup"><span data-stu-id="6543a-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="6543a-126">Angiv minimumantallet for varen.</span><span class="sxs-lookup"><span data-stu-id="6543a-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="6543a-127">Klik for at følge linket i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="6543a-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="6543a-128">Klik for at følge linket i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="6543a-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="6543a-129">Udvid faktaboksen Produktbillede.</span><span class="sxs-lookup"><span data-stu-id="6543a-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="6543a-130">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6543a-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="6543a-131">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="6543a-131">Click Item coverage.</span></span>
6. <span data-ttu-id="6543a-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6543a-132">Click New.</span></span>
7. <span data-ttu-id="6543a-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6543a-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6543a-134">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="6543a-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="6543a-135">Angiv Lagersted til 12.</span><span class="sxs-lookup"><span data-stu-id="6543a-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="6543a-136">Angiv Minimum til '200'.</span><span class="sxs-lookup"><span data-stu-id="6543a-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="6543a-137">Kør jobbet til oprettelse af batchhændelse.</span><span class="sxs-lookup"><span data-stu-id="6543a-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="6543a-138">Gå til Produktionsstyring > Periodiske opgaver > Batchafvikling for kanban-job > Udligningshændelser.</span><span class="sxs-lookup"><span data-stu-id="6543a-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="6543a-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6543a-139">Click OK.</span></span>
3. <span data-ttu-id="6543a-140">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="6543a-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="6543a-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6543a-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6543a-142">Vælg den kanban-regel, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="6543a-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="6543a-143">Udvid afsnittet Kanbans.</span><span class="sxs-lookup"><span data-stu-id="6543a-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="6543a-144">Bemærk, at der er oprettet en kanban for at overføre det nødvendige materiale til lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="6543a-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

