--- 
title: "Oprette en kanban-regel ved hjælp af en kanban-linjehændelse"
description: "Denne fremgangsmåde opretter en kanban-regel ved at bruge indstillingen for kanban-linjehændelsen til at udløse træk fra en procesaktivitet."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.openlocfilehash: 9ef7b8e920d22cbc4f96676e68a263f2da7f232c
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="48ee8-103">Oprette en kanban-regel ved hjælp af en kanban-linjehændelse</span><span class="sxs-lookup"><span data-stu-id="48ee8-103">Create a kanban rule using a kanban line event</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48ee8-104">Denne fremgangsmåde opretter en kanban-regel ved at bruge indstillingen for kanban-linjehændelsen til at udløse træk fra en procesaktivitet.</span><span class="sxs-lookup"><span data-stu-id="48ee8-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="48ee8-105">Kanban-reglen udløses af en kanban-procesaktivitet, med en mængde lig med eller større end 25 hver.</span><span class="sxs-lookup"><span data-stu-id="48ee8-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="48ee8-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="48ee8-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="48ee8-107">Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="48ee8-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="48ee8-108">Oprette en kanban-regel</span><span class="sxs-lookup"><span data-stu-id="48ee8-108">Create a kanban rule</span></span>
1. <span data-ttu-id="48ee8-109">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="48ee8-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="48ee8-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="48ee8-110">Click New.</span></span>
3. <span data-ttu-id="48ee8-111">Vælg "Hændelse" i feltet Genopfyldningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="48ee8-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="48ee8-112">Derved genereres kanbans direkte ud fra efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="48ee8-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="48ee8-113">Den bruges til at konfigurere regler, der definerer et scenario for fremstilling efter ordre.</span><span class="sxs-lookup"><span data-stu-id="48ee8-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="48ee8-114">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="48ee8-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="48ee8-115">Indtast eller vælg SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="48ee8-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="48ee8-116">Den første aktivitet i en produktionskanban-regel er en procesaktivitet i produktionsflowet.</span><span class="sxs-lookup"><span data-stu-id="48ee8-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="48ee8-117">Når du vælger aktiviteten, kopieres gyldighedsdatoerne for aktiviteten til gyldighedsdatoerne for kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="48ee8-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="48ee8-118">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="48ee8-118">Expand the Details section.</span></span>
6. <span data-ttu-id="48ee8-119">Skriv 'L0001' i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="48ee8-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="48ee8-120">Udvid afsnittet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="48ee8-120">Expand the Events section.</span></span>
8. <span data-ttu-id="48ee8-121">Vælg 'Automatisk' i feltet Kanban-linjehændelse.</span><span class="sxs-lookup"><span data-stu-id="48ee8-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="48ee8-122">Dette genererer hændelses-kanbans efter behov.</span><span class="sxs-lookup"><span data-stu-id="48ee8-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="48ee8-123">Dette felt bruges til at konfigurere kanban-regler, der genopfylder materiale, som kræves i en downstream-procesaktivitet.</span><span class="sxs-lookup"><span data-stu-id="48ee8-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="48ee8-124">Når du vælger Automatisk, oprettes der hændelses-kanbans med behovet.</span><span class="sxs-lookup"><span data-stu-id="48ee8-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="48ee8-125">Denne indstilling anbefales, hvis du forventer at køre produktionen samme dag.</span><span class="sxs-lookup"><span data-stu-id="48ee8-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="48ee8-126">Angiv Mindste antal hændelser "25".</span><span class="sxs-lookup"><span data-stu-id="48ee8-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="48ee8-127">Hændelses-kanbans genereres, når behovsmængden er lig med eller mere end dette felt.</span><span class="sxs-lookup"><span data-stu-id="48ee8-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="48ee8-128">Dette er nyttigt, hvis du vil producere en ordremængde, der er mindre end dette felt på én maskine, og mere end dette felt på en anden maskine.</span><span class="sxs-lookup"><span data-stu-id="48ee8-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="48ee8-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48ee8-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="48ee8-130">Opret salgsordre, og udløs kanban-kæde</span><span class="sxs-lookup"><span data-stu-id="48ee8-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="48ee8-131">Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="48ee8-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="48ee8-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="48ee8-132">Click New.</span></span>
3. <span data-ttu-id="48ee8-133">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="48ee8-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="48ee8-134">Vælg debitorkontoen US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="48ee8-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="48ee8-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="48ee8-135">Click OK.</span></span>
5. <span data-ttu-id="48ee8-136">Skriv 'L0001' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="48ee8-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="48ee8-137">L0001 er den vare, du har oprettet kanban-reglen for.</span><span class="sxs-lookup"><span data-stu-id="48ee8-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="48ee8-138">Angiv antallet til '27'.</span><span class="sxs-lookup"><span data-stu-id="48ee8-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="48ee8-139">Da 27 er højere end minimumantallet på 25 for kanban-reglen, udløser det en hændelses-kanban.</span><span class="sxs-lookup"><span data-stu-id="48ee8-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="48ee8-140">Skriv "1" i feltet Sted.</span><span class="sxs-lookup"><span data-stu-id="48ee8-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="48ee8-141">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="48ee8-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="48ee8-142">Vælg lagersted 13.</span><span class="sxs-lookup"><span data-stu-id="48ee8-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="48ee8-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="48ee8-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="48ee8-144">Få vist den kanban, der er genereret af kanban-reglen</span><span class="sxs-lookup"><span data-stu-id="48ee8-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="48ee8-145">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="48ee8-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="48ee8-146">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="48ee8-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="48ee8-147">Udvid afsnittet Kanbans.</span><span class="sxs-lookup"><span data-stu-id="48ee8-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="48ee8-148">Bemærk, at en kanban for 27 blev oprettet for at behandle aktiviteten ud fra den oprettede kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="48ee8-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="48ee8-149">Dette er det sidste trin.</span><span class="sxs-lookup"><span data-stu-id="48ee8-149">This is the last step.</span></span>  


