---
title: Oprette en kanban-regel for udbetaling
description: Denne procedure viser den konfiguration, der er nødvendig for at oprette en udtræks-kanban-regel for overførsel af materiale i et lean-miljø.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adbcdbb2d278b25dce1d8c027e66367e9c0930e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828820"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="5c528-103">Oprette en kanban-regel for udbetaling</span><span class="sxs-lookup"><span data-stu-id="5c528-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c528-104">Denne procedure viser den konfiguration, der er nødvendig for at oprette en udtræks-kanban-regel for overførsel af materiale i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="5c528-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="5c528-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="5c528-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5c528-106">Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder genopfyldning af et nyt eller ændret materiale.</span><span class="sxs-lookup"><span data-stu-id="5c528-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="5c528-107">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="5c528-107">Create new kanban rule</span></span>
1. <span data-ttu-id="5c528-108">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="5c528-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="5c528-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5c528-109">Click New.</span></span>
3. <span data-ttu-id="5c528-110">Vælg 'Udtræk' i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="5c528-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="5c528-111">Udtrækstypen bruges til kanban-regler i forbindelse med overførsel af materiale eller varer.</span><span class="sxs-lookup"><span data-stu-id="5c528-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="5c528-112">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="5c528-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="5c528-113">Vælg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="5c528-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="5c528-114">Denne aktivitet er indstillet til at flytte komponenter fra lagersted 11, lokation 11 til lagersted 12, lokation 12.</span><span class="sxs-lookup"><span data-stu-id="5c528-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="5c528-115">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="5c528-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="5c528-116">Vælg M0007.</span><span class="sxs-lookup"><span data-stu-id="5c528-116">Select M0007.</span></span>  
6. <span data-ttu-id="5c528-117">Angiv et tal i feltet Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="5c528-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="5c528-118">For eksempel 60.</span><span class="sxs-lookup"><span data-stu-id="5c528-118">For example, 60.</span></span>  
7. <span data-ttu-id="5c528-119">Indtast eller vælg en værdi i feltet Måleenhed.</span><span class="sxs-lookup"><span data-stu-id="5c528-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="5c528-120">For eksempel Minutter.</span><span class="sxs-lookup"><span data-stu-id="5c528-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="5c528-121">Indstille mængder for kanban</span><span class="sxs-lookup"><span data-stu-id="5c528-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="5c528-122">Angiv Standardmængde til "5".</span><span class="sxs-lookup"><span data-stu-id="5c528-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="5c528-123">Dette er det antal, der skal overføres for hver kanban.</span><span class="sxs-lookup"><span data-stu-id="5c528-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="5c528-124">Indtast '2' i feltet Fast kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="5c528-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="5c528-125">Dette er antallet af kanbans, der skal være aktive.</span><span class="sxs-lookup"><span data-stu-id="5c528-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="5c528-126">I dette tilfælde overfører to kanbans fem hver.</span><span class="sxs-lookup"><span data-stu-id="5c528-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="5c528-127">Angiv "1" i feltet Minimum for påmindelsesgrænse.</span><span class="sxs-lookup"><span data-stu-id="5c528-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="5c528-128">Bruges til at holde styr på det mindste antal fulde kanbans, der skal være på destinationen.</span><span class="sxs-lookup"><span data-stu-id="5c528-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="5c528-129">Den bruges f.eks. på oversigten over kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="5c528-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="5c528-130">Angiv "2" i feltet Maksimum for påmindelsesgrænse.</span><span class="sxs-lookup"><span data-stu-id="5c528-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="5c528-131">Bruges til at holde styr på det maksimale antal fulde kanbans, der må være på destinationen.</span><span class="sxs-lookup"><span data-stu-id="5c528-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="5c528-132">Den bruges f.eks. på oversigten over kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="5c528-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="5c528-133">Opret kanbans</span><span class="sxs-lookup"><span data-stu-id="5c528-133">Create kanbans</span></span>
1. <span data-ttu-id="5c528-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5c528-134">Click Save.</span></span>
    * <span data-ttu-id="5c528-135">Kanban-reglen skal gemmes, før du kan oprette kanbans.</span><span class="sxs-lookup"><span data-stu-id="5c528-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="5c528-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="5c528-136">Click Add.</span></span>
    * <span data-ttu-id="5c528-137">Bemærk, at der ikke er nogen aktive kanbans, fordi er det foreslåede 'Antal nye kanbans' er 2, hvilket svarer til 'Fast kanban-mængde'.</span><span class="sxs-lookup"><span data-stu-id="5c528-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="5c528-138">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="5c528-138">Click Create.</span></span>
    * <span data-ttu-id="5c528-139">Dette opretter to kanbans.</span><span class="sxs-lookup"><span data-stu-id="5c528-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="5c528-140">Bemærk, at der blev oprettet to kanbans for hver fem for denne udtræks-kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="5c528-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="5c528-141">Dette er det sidste trin i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="5c528-141">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]