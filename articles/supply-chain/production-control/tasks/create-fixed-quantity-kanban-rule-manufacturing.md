---
title: Oprette en regel for fastmængde-kanban til produktion
description: Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en fast produktions-kanban-regel til udløsning af transformeringsaktiviteter i en arbejdscelle i et leanmiljø.
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
ms.openlocfilehash: ece72971d2bc67482cbdda4fb0d1b3176a3f3071
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829180"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="91d9c-103">Oprette en regel for fastmængde-kanban til produktion</span><span class="sxs-lookup"><span data-stu-id="91d9c-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91d9c-104">Denne procedure fokuserer på den opsætning, der er nødvendig for at oprette en fast produktions-kanban-regel til udløsning af transformeringsaktiviteter i en arbejdscelle i et leanmiljø.</span><span class="sxs-lookup"><span data-stu-id="91d9c-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="91d9c-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="91d9c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91d9c-106">Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen af et nyt eller ændret produkt.</span><span class="sxs-lookup"><span data-stu-id="91d9c-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="91d9c-107">Opret en ny kanban-regel</span><span class="sxs-lookup"><span data-stu-id="91d9c-107">Create new kanban rule</span></span>
1. <span data-ttu-id="91d9c-108">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="91d9c-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="91d9c-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="91d9c-109">Click New.</span></span>
    * <span data-ttu-id="91d9c-110">Bemærk, at standardtypen er Produktion, og Genopfyldningsstrategi er Fast.</span><span class="sxs-lookup"><span data-stu-id="91d9c-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="91d9c-111">Du behøver ikke at ændre disse parametre.</span><span class="sxs-lookup"><span data-stu-id="91d9c-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="91d9c-112">Angiv eller vælg en værdi i feltet Første planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="91d9c-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="91d9c-113">Dette er den aktivitet, der udføres for kanbans, der er oprettet ud fra denne kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="91d9c-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="91d9c-114">Vælg "SpeakerTestAndPackaging".</span><span class="sxs-lookup"><span data-stu-id="91d9c-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="91d9c-115">Udvid afsnittet Detaljer.</span><span class="sxs-lookup"><span data-stu-id="91d9c-115">Expand the Details section.</span></span>
5. <span data-ttu-id="91d9c-116">Indtast eller vælg en værdi i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="91d9c-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="91d9c-117">Vælg L0050.</span><span class="sxs-lookup"><span data-stu-id="91d9c-117">Select L0050.</span></span>  
6. <span data-ttu-id="91d9c-118">Indtast eller vælg en værdi i feltet Måleenhed.</span><span class="sxs-lookup"><span data-stu-id="91d9c-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="91d9c-119">Vælg minutter.</span><span class="sxs-lookup"><span data-stu-id="91d9c-119">Select minutes.</span></span>  
7. <span data-ttu-id="91d9c-120">Angiv et tal i feltet Leveringstid.</span><span class="sxs-lookup"><span data-stu-id="91d9c-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="91d9c-121">Angiv 5.</span><span class="sxs-lookup"><span data-stu-id="91d9c-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="91d9c-122">Angiv antal</span><span class="sxs-lookup"><span data-stu-id="91d9c-122">Set quantities</span></span>
1. <span data-ttu-id="91d9c-123">Udvid afsnittet Antal.</span><span class="sxs-lookup"><span data-stu-id="91d9c-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="91d9c-124">Angiv Standardmængde til "10".</span><span class="sxs-lookup"><span data-stu-id="91d9c-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="91d9c-125">Dette er det antal, der skal overføres for hver kanban.</span><span class="sxs-lookup"><span data-stu-id="91d9c-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="91d9c-126">Marker feltet Afvigelse i produktantal.</span><span class="sxs-lookup"><span data-stu-id="91d9c-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="91d9c-127">Dermed kan valgte kanbans fuldføres med en afvigelse fra standardmængden.</span><span class="sxs-lookup"><span data-stu-id="91d9c-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="91d9c-128">Angiv begge afvigelser til 2 for at tillade, at kanbans fuldføres med et antal fra 8 til 12.</span><span class="sxs-lookup"><span data-stu-id="91d9c-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="91d9c-129">Angiv Afvigelse nedenfor til "2".</span><span class="sxs-lookup"><span data-stu-id="91d9c-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="91d9c-130">Dette tillader fuldførelse ned til 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="91d9c-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="91d9c-131">Angiv Afvigelse ovenfor til "2".</span><span class="sxs-lookup"><span data-stu-id="91d9c-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="91d9c-132">Dette tillader fuldførelse op til 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="91d9c-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="91d9c-133">Skriv et tal i feltet Fast kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="91d9c-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="91d9c-134">Dette er antallet af kanbans, der skal være aktive.</span><span class="sxs-lookup"><span data-stu-id="91d9c-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="91d9c-135">I dette tilfælde 5 kanbans, som behandler 10 hver.</span><span class="sxs-lookup"><span data-stu-id="91d9c-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="91d9c-136">Angiv "2" i feltet Minimum for påmindelsesgrænse.</span><span class="sxs-lookup"><span data-stu-id="91d9c-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="91d9c-137">Bruges til at holde styr på det mindste antal fulde kanbans, der skal være på destinationen.</span><span class="sxs-lookup"><span data-stu-id="91d9c-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="91d9c-138">Den bruges f.eks. på oversigten over kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="91d9c-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="91d9c-139">Angiv "4" i feltet Maksimum for påmindelsesgrænse.</span><span class="sxs-lookup"><span data-stu-id="91d9c-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="91d9c-140">Bruges til at holde styr på det maksimale antal fulde kanbans, der må være på destinationen.</span><span class="sxs-lookup"><span data-stu-id="91d9c-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="91d9c-141">Den bruges f.eks. på oversigten over kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="91d9c-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="91d9c-142">Angiv "1" i feltet Automatisk planlægningsantal.</span><span class="sxs-lookup"><span data-stu-id="91d9c-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="91d9c-143">Hvis dette angives til 1 betyder det, at alle kanbans automatisk planlægges.</span><span class="sxs-lookup"><span data-stu-id="91d9c-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="91d9c-144">Hvis vi angav 3, ville kanbans ikke blive planlagt, før 3 tomme kanbans var klar til planlægning.</span><span class="sxs-lookup"><span data-stu-id="91d9c-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="91d9c-145">Dette er nyttigt til at gruppere arbejde og undgå for meget opsætning.</span><span class="sxs-lookup"><span data-stu-id="91d9c-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="91d9c-146">Opret kanbans</span><span class="sxs-lookup"><span data-stu-id="91d9c-146">Create Kanbans</span></span>
1. <span data-ttu-id="91d9c-147">Udvid afsnittet Kanbans.</span><span class="sxs-lookup"><span data-stu-id="91d9c-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="91d9c-148">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="91d9c-148">Click Save.</span></span>
    * <span data-ttu-id="91d9c-149">Kanban-reglen skal gemmes, før du kan oprette kanbans.</span><span class="sxs-lookup"><span data-stu-id="91d9c-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="91d9c-150">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="91d9c-150">Click Add.</span></span>
    * <span data-ttu-id="91d9c-151">Bemærk, at der ikke er nogen aktive kanbans, og derfor er det foreslåede 'antal nye kanbans' 5.</span><span class="sxs-lookup"><span data-stu-id="91d9c-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="91d9c-152">Dette er lig med 'Fast kanban-mængde'.</span><span class="sxs-lookup"><span data-stu-id="91d9c-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="91d9c-153">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="91d9c-153">Click Create.</span></span>
    * <span data-ttu-id="91d9c-154">Dette opretter 5 kanbans.</span><span class="sxs-lookup"><span data-stu-id="91d9c-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="91d9c-155">Bemærk, at der blev oprettet 5 kanbans for 10 hver for denne produktions-kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="91d9c-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="91d9c-156">Dette er det sidste trin i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="91d9c-156">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]