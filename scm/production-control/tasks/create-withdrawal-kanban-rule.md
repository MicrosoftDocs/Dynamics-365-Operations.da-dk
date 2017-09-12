--- 
title: Oprette en kanban-regel for udbetaling
description: "Denne procedure viser den konfiguration, der er nødvendig for at oprette en udtræks-kanban-regel for overførsel af materiale i et lean-miljø."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="f1130-103">Oprette en kanban-regel for udbetaling</span><span class="sxs-lookup"><span data-stu-id="f1130-103">Create a withdrawal kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1130-104">Denne procedure viser den konfiguration, der er nødvendig for at oprette en udtræks-kanban-regel for overførsel af materiale i et lean-miljø.</span><span class="sxs-lookup"><span data-stu-id="f1130-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="f1130-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f1130-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f1130-106">Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder genopfyldning af et nyt eller ændret materiale.</span><span class="sxs-lookup"><span data-stu-id="f1130-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="f1130-107">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="f1130-107">Create new kanban rule</span></span>
1. <span data-ttu-id="f1130-108">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="f1130-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="f1130-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f1130-109">Click New.</span></span>
3. <span data-ttu-id="f1130-110">Vælg 'Udtræk' i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="f1130-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="f1130-111">Udtrækstypen bruges til kanban-regler i forbindelse med overførsel af materiale eller varer.</span><span class="sxs-lookup"><span data-stu-id="f1130-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="f1130-112">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="f1130-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f1130-113">Vælg ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="f1130-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="f1130-114">Denne aktivitet er indstillet til at flytte komponenter fra lagersted 11, lokation 11 til lagersted 12, lokation 12.</span><span class="sxs-lookup"><span data-stu-id="f1130-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="f1130-115">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="f1130-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="f1130-116">Vælg M0007.</span><span class="sxs-lookup"><span data-stu-id="f1130-116">Select M0007.</span></span>  
6. <span data-ttu-id="f1130-117">Angiv et tal i feltet Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="f1130-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="f1130-118">For eksempel 60.</span><span class="sxs-lookup"><span data-stu-id="f1130-118">For example, 60.</span></span>  
7. <span data-ttu-id="f1130-119">Indtast eller vælg en værdi i feltet Måleenhed.</span><span class="sxs-lookup"><span data-stu-id="f1130-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="f1130-120">For eksempel Minutter.</span><span class="sxs-lookup"><span data-stu-id="f1130-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="f1130-121">Indstille mængder for kanban</span><span class="sxs-lookup"><span data-stu-id="f1130-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="f1130-122">Angiv Standardmængde til "5".</span><span class="sxs-lookup"><span data-stu-id="f1130-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="f1130-123">Dette er det antal, der skal overføres for hver kanban.</span><span class="sxs-lookup"><span data-stu-id="f1130-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="f1130-124">Indtast '2' i feltet Fast kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="f1130-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="f1130-125">Dette er antallet af kanbans, der skal være aktive.</span><span class="sxs-lookup"><span data-stu-id="f1130-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="f1130-126">I dette tilfælde overfører to kanbans fem hver.</span><span class="sxs-lookup"><span data-stu-id="f1130-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="f1130-127">Angiv "1" i feltet Minimum for påmindelsesgrænse.</span><span class="sxs-lookup"><span data-stu-id="f1130-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="f1130-128">Bruges til at holde styr på det mindste antal fulde kanbans, der skal være på destinationen.</span><span class="sxs-lookup"><span data-stu-id="f1130-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="f1130-129">Den bruges f.eks. på oversigten over kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="f1130-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="f1130-130">Angiv "2" i feltet Maksimum for påmindelsesgrænse.</span><span class="sxs-lookup"><span data-stu-id="f1130-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="f1130-131">Bruges til at holde styr på det maksimale antal fulde kanbans, der må være på destinationen.</span><span class="sxs-lookup"><span data-stu-id="f1130-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="f1130-132">Den bruges f.eks. på oversigten over kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="f1130-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="f1130-133">Opret kanbans</span><span class="sxs-lookup"><span data-stu-id="f1130-133">Create kanbans</span></span>
1. <span data-ttu-id="f1130-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f1130-134">Click Save.</span></span>
    * <span data-ttu-id="f1130-135">Kanban-reglen skal gemmes, før du kan oprette kanbans.</span><span class="sxs-lookup"><span data-stu-id="f1130-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="f1130-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f1130-136">Click Add.</span></span>
    * <span data-ttu-id="f1130-137">Bemærk, at der ikke er nogen aktive kanbans, fordi er det foreslåede 'Antal nye kanbans' er 2, hvilket svarer til 'Fast kanban-mængde'.</span><span class="sxs-lookup"><span data-stu-id="f1130-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="f1130-138">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="f1130-138">Click Create.</span></span>
    * <span data-ttu-id="f1130-139">Dette opretter to kanbans.</span><span class="sxs-lookup"><span data-stu-id="f1130-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="f1130-140">Bemærk, at der blev oprettet to kanbans for hver fem for denne udtræks-kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="f1130-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="f1130-141">Dette er det sidste trin i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="f1130-141">This is the last step in this procedure.</span></span>  


