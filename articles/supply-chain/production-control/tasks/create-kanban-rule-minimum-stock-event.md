---
title: Oprette en kanban-regel ved hjælp af en hændelse for minimal lagerbeholdning
description: I denne fremgangsmåde fokuseres der på den opsætning, der er nødvendig for at oprette en kanban-regel ved hjælp af en minimumlagerhændelse for at sikre, at et bestemt produkt altid er tilgængeligt på et bestemt sted.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212244"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="08061-103">Oprette en kanban-regel ved hjælp af en hændelse for minimal lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="08061-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08061-104">I denne fremgangsmåde fokuseres der på den opsætning, der er nødvendig for at oprette en kanban-regel ved hjælp af en minimumlagerhændelse for at sikre, at et bestemt produkt altid er tilgængeligt på et bestemt sted.</span><span class="sxs-lookup"><span data-stu-id="08061-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="08061-105">En kanban-regel oprettes for at overføre materiale til stedet, når lagerbeholdningen falder til under 200 enheder.</span><span class="sxs-lookup"><span data-stu-id="08061-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="08061-106">Ved at køre behandlingen af udligningshændelsen oprettes de nødvendige kanbans.</span><span class="sxs-lookup"><span data-stu-id="08061-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="08061-107">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="08061-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="08061-108">Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="08061-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="08061-109">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="08061-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="08061-110">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="08061-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="08061-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="08061-111">Click New.</span></span>
3. <span data-ttu-id="08061-112">Vælg 'Udtræk' i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="08061-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="08061-113">Denne type bruges til at oprette kanbans til overflytning.</span><span class="sxs-lookup"><span data-stu-id="08061-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="08061-114">Vælg "Hændelse" i feltet Genopfyldningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="08061-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="08061-115">Strategien Hændelse bruges til at oprette overførslen af kanbans ud fra en hændelse.</span><span class="sxs-lookup"><span data-stu-id="08061-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="08061-116">Senere i proceduren udløser du kanbans til overførsel ved hjælp af genopfyldning af lageret.</span><span class="sxs-lookup"><span data-stu-id="08061-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="08061-117">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="08061-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="08061-118">Indtast eller vælg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="08061-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="08061-119">Denne overførselsaktivitet har (output) lagersted og lokation 12 for modtagelsen, hvilket betyder, at materiale flyttes til lokation 12 på lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="08061-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="08061-120">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="08061-120">Expand the Details section.</span></span>
7. <span data-ttu-id="08061-121">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="08061-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="08061-122">Vælg M0007.</span><span class="sxs-lookup"><span data-stu-id="08061-122">Select M0007.</span></span>  
8. <span data-ttu-id="08061-123">Udvid afsnittet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="08061-123">Expand the Events section.</span></span>
9. <span data-ttu-id="08061-124">Vælg "Batch" i feltet Lagergenopfyldningshændelse.</span><span class="sxs-lookup"><span data-stu-id="08061-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="08061-125">Der oprettes kanbans for at opfylde behovet på den relaterede lokation under behandling af udligningshændelser.</span><span class="sxs-lookup"><span data-stu-id="08061-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="08061-126">Angiv minimumantallet for varen.</span><span class="sxs-lookup"><span data-stu-id="08061-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="08061-127">Klik for at følge linket i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="08061-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="08061-128">Klik for at følge linket i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="08061-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="08061-129">Udvid faktaboksen Produktbillede.</span><span class="sxs-lookup"><span data-stu-id="08061-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="08061-130">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="08061-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="08061-131">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="08061-131">Click Item coverage.</span></span>
6. <span data-ttu-id="08061-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="08061-132">Click New.</span></span>
7. <span data-ttu-id="08061-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="08061-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="08061-134">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="08061-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="08061-135">Angiv Lagersted til 12.</span><span class="sxs-lookup"><span data-stu-id="08061-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="08061-136">Angiv Minimum til '200'.</span><span class="sxs-lookup"><span data-stu-id="08061-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="08061-137">Kør jobbet til oprettelse af batchhændelse.</span><span class="sxs-lookup"><span data-stu-id="08061-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="08061-138">Gå til Produktionsstyring > Periodiske opgaver > Batchafvikling for kanban-job > Udligningshændelser.</span><span class="sxs-lookup"><span data-stu-id="08061-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="08061-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="08061-139">Click OK.</span></span>
3. <span data-ttu-id="08061-140">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="08061-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="08061-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="08061-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="08061-142">Vælg den kanban-regel, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="08061-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="08061-143">Udvid afsnittet Kanbans.</span><span class="sxs-lookup"><span data-stu-id="08061-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="08061-144">Bemærk, at der er oprettet en kanban for at overføre det nødvendige materiale til lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="08061-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

