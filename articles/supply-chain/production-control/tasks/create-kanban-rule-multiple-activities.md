---
title: Oprette en kanban-regel for flere aktiviteter
description: Denne fremgangsmåde viser, hvordan du kan oprette en kanban-regel, der omfatter flere aktiviteter fra et produktionsflow.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68cac0f581e786cdb3801e03fb60db7bc05ffb2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212207"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="f722d-103">Oprette en kanban-regel for flere aktiviteter</span><span class="sxs-lookup"><span data-stu-id="f722d-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f722d-104">Denne fremgangsmåde viser, hvordan du kan oprette en kanban-regel, der omfatter flere aktiviteter fra et produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="f722d-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="f722d-105">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f722d-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f722d-106">Denne opgave er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="f722d-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="f722d-107">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="f722d-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="f722d-108">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="f722d-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f722d-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f722d-109">Click New.</span></span>
3. <span data-ttu-id="f722d-110">Vælg 'Planlagt' i feltet Genopfyldningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="f722d-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="f722d-111">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="f722d-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f722d-112">Vælg SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="f722d-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="f722d-113">Markér afkrydsningsfeltet Flere aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f722d-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="f722d-114">Formålet er at inkludere mere end én aktivitet i kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="f722d-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="f722d-115">Du kan vælge en sti i produktionsflowet, når du vælger den sidste planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="f722d-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="f722d-116">Angiv eller vælg en værdi i feltet Sidste planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="f722d-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f722d-117">Vælg SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="f722d-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="f722d-118">Når du vælger værdien, åbnes en side automatisk.</span><span class="sxs-lookup"><span data-stu-id="f722d-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="f722d-119">Vælg kanban-flowet SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="f722d-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="f722d-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f722d-120">Click OK.</span></span>  
7. <span data-ttu-id="f722d-121">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="f722d-121">Expand the Details section.</span></span>
8. <span data-ttu-id="f722d-122">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="f722d-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="f722d-123">Vælg vare L0006.</span><span class="sxs-lookup"><span data-stu-id="f722d-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="f722d-124">Opret kanban, og se job</span><span class="sxs-lookup"><span data-stu-id="f722d-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="f722d-125">Udvid afsnittet Kanbans.</span><span class="sxs-lookup"><span data-stu-id="f722d-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="f722d-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f722d-126">Click Add.</span></span>
3. <span data-ttu-id="f722d-127">Skriv "1" i feltet Antal nye kanbans.</span><span class="sxs-lookup"><span data-stu-id="f722d-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="f722d-128">Dette opretter én kanban.</span><span class="sxs-lookup"><span data-stu-id="f722d-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="f722d-129">Angiv Produktmængde til "3".</span><span class="sxs-lookup"><span data-stu-id="f722d-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="f722d-130">Kanban skal behandle 3 produkter.</span><span class="sxs-lookup"><span data-stu-id="f722d-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="f722d-131">Angiv en dato og et klokkeslæt i feltet Forfaldsdato/-klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="f722d-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="f722d-132">Du kan angive I dag.</span><span class="sxs-lookup"><span data-stu-id="f722d-132">You can enter Today.</span></span>  
6. <span data-ttu-id="f722d-133">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="f722d-133">Click Create.</span></span>
7. <span data-ttu-id="f722d-134">Klik på Detaljer.</span><span class="sxs-lookup"><span data-stu-id="f722d-134">Click Details.</span></span>
    * <span data-ttu-id="f722d-135">Bemærk, at den pågældende kanban har to procesjob fra produktionsflowet.</span><span class="sxs-lookup"><span data-stu-id="f722d-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="f722d-136">Det første er SpeakerAssemblyAndPolish, og det andet er SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="f722d-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="f722d-137">Dette er det sidste trin!</span><span class="sxs-lookup"><span data-stu-id="f722d-137">This is the last step!</span></span>  

