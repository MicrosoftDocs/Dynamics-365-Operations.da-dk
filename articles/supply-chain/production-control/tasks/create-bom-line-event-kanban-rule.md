--- 
title: "Oprette en kanban-regel for styklistelinjehændelse"
description: "Opgaven fokuserer på den konfiguration, der er nødvendig for at oprette en kanban-hændelsesregel for at sikre forsyning til produktionsstyklistelinjer i et blandet lean-miljø og et klassisk produktionsmiljø."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4168a515f5bc1b69a24aac616aba7e447ccda11a
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="72dde-103">Oprette en kanban-regel for styklistelinjehændelse</span><span class="sxs-lookup"><span data-stu-id="72dde-103">Create a BOM line event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72dde-104">Opgaven fokuserer på den konfiguration, der er nødvendig for at oprette en kanban-hændelsesregel for at sikre forsyning til produktionsstyklistelinjer i et blandet lean-miljø og et klassisk produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="72dde-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="72dde-105">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="72dde-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="72dde-106">Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt.</span><span class="sxs-lookup"><span data-stu-id="72dde-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="72dde-107">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="72dde-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="72dde-108">Gå til Produktionsstyring > Periodiske opgaver > Beregning af kanban-mængde > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="72dde-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="72dde-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="72dde-109">Click New.</span></span>
3. <span data-ttu-id="72dde-110">Vælg 'Udtræk' i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="72dde-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="72dde-111">Udtrækstypen bruges til at oprette kanbans til overflytning.</span><span class="sxs-lookup"><span data-stu-id="72dde-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="72dde-112">Vælg "Hændelse" i feltet Genopfyldningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="72dde-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="72dde-113">Strategien Hændelse er valgt for at oprette overførslen af kanbans ud fra en hændelse.</span><span class="sxs-lookup"><span data-stu-id="72dde-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="72dde-114">Senere i opgavevejledningen vil vi udløse den ved at forkalkulere en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="72dde-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="72dde-115">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="72dde-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="72dde-116">Indtast eller vælg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="72dde-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="72dde-117">Denne overførselsaktivitet har (output) lagersted og lokation 12 for modtagelsen, hvilket betyder, at materiale flyttes til lokation 12 på lagersted 12.</span><span class="sxs-lookup"><span data-stu-id="72dde-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="72dde-118">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="72dde-118">Expand the Details section.</span></span>
7. <span data-ttu-id="72dde-119">Indtast eller vælg M0001 i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="72dde-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="72dde-120">Udvid afsnittet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="72dde-120">Expand the Events section.</span></span>
9. <span data-ttu-id="72dde-121">Vælg 'Automatisk' i feltet Styklistehændelse.</span><span class="sxs-lookup"><span data-stu-id="72dde-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="72dde-122">Når feltet Styklistelinjehændelse er indstillet til Automatisk, oprettes der kanbans for at opfylde materialebehovet for produktionsordrens styklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="72dde-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="72dde-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72dde-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="72dde-124">Oprette og redigere en ny produktionsordre</span><span class="sxs-lookup"><span data-stu-id="72dde-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="72dde-125">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="72dde-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="72dde-126">Klik på Ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="72dde-126">Click New production order.</span></span>
3. <span data-ttu-id="72dde-127">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="72dde-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="72dde-128">Angiv eller vælg 'L0001'.</span><span class="sxs-lookup"><span data-stu-id="72dde-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="72dde-129">Vi bruger vare L0001, fordi vare M0001 indgår i styklisten for vare L0001.</span><span class="sxs-lookup"><span data-stu-id="72dde-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="72dde-130">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="72dde-130">Click Create.</span></span>
5. <span data-ttu-id="72dde-131">Klik på linket i rækken for L0001 på listen.</span><span class="sxs-lookup"><span data-stu-id="72dde-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="72dde-132">Klik på Stykliste.</span><span class="sxs-lookup"><span data-stu-id="72dde-132">Click BOM.</span></span>
7. <span data-ttu-id="72dde-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72dde-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="72dde-134">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="72dde-134">Click Edit.</span></span>
9. <span data-ttu-id="72dde-135">Vælg 'Sporet forsyning' i feltet Linjetype.</span><span class="sxs-lookup"><span data-stu-id="72dde-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="72dde-136">Sporet forsyning er valgt for at udløse oprettelse af forsyning for en kanban.</span><span class="sxs-lookup"><span data-stu-id="72dde-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="72dde-137">Vælg Nej i feltet Ressourceforbrug.</span><span class="sxs-lookup"><span data-stu-id="72dde-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="72dde-138">Når markeringen i afkrydsningsfeltet Ressourceforbrug fjernes, kan lagerstedet ændres.</span><span class="sxs-lookup"><span data-stu-id="72dde-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="72dde-139">Udvid sektionen Lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="72dde-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="72dde-140">Skriv 12 i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="72dde-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="72dde-141">Lageret er indstillet til 12, fordi dette er lagerstedet til udlagring for udtræksaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="72dde-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="72dde-142">Skriv '12' i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="72dde-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="72dde-143">Lokationen er indstillet til 12, fordi dette er lokationen til udlagring for udtræksaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="72dde-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="72dde-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72dde-144">Close the page.</span></span>
15. <span data-ttu-id="72dde-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72dde-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="72dde-146">Forkalkulere produktionsordren og få vist den oprettede kanban</span><span class="sxs-lookup"><span data-stu-id="72dde-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="72dde-147">Klik på Forkalkulation.</span><span class="sxs-lookup"><span data-stu-id="72dde-147">Click Estimate.</span></span>
    * <span data-ttu-id="72dde-148">Forkalkulation af produktionsordren udløser oprettelsen af den tilknyttede kanban for at levere varen M0001.</span><span class="sxs-lookup"><span data-stu-id="72dde-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="72dde-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="72dde-149">Click OK.</span></span>
3. <span data-ttu-id="72dde-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72dde-150">Close the page.</span></span>
4. <span data-ttu-id="72dde-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72dde-151">Close the page.</span></span>
5. <span data-ttu-id="72dde-152">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="72dde-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="72dde-153">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72dde-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="72dde-154">Vælg den kanban-hændelsesregel, der er oprettet for varen M0001.</span><span class="sxs-lookup"><span data-stu-id="72dde-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="72dde-155">Udvid afsnittet Kanbans.</span><span class="sxs-lookup"><span data-stu-id="72dde-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="72dde-156">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="72dde-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="72dde-157">Bemærk den kanban, der er oprettet for at levere M0001 til den forkalkulerede produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="72dde-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="72dde-158">Dette er det sidste trin!</span><span class="sxs-lookup"><span data-stu-id="72dde-158">This is the last step!</span></span>  


