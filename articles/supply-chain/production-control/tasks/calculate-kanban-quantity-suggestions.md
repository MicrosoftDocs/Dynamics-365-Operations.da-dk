--- 
title: "Beregne forslag til kanban-mængder"
description: "Denne fremgangsmåde fokuserer på optimering af kanban-størrelse og -mængder for en specifik kanban-regel ved at bruge beregningen af kanban-mængden."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a817dbc02890d863f68c5bf2a6cc11b9a5328060
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="775e8-103">Beregne forslag til kanban-mængder</span><span class="sxs-lookup"><span data-stu-id="775e8-103">Calculate kanban quantity suggestions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="775e8-104">Denne fremgangsmåde fokuserer på optimering af kanban-størrelse og -mængder for en specifik kanban-regel ved at bruge beregningen af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="775e8-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="775e8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="775e8-106">Denne procedure er beregnet til værdistrømlederen.</span><span class="sxs-lookup"><span data-stu-id="775e8-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="775e8-107">Det er en forudsætning, at du har gennemført proceduren Føj en ny politik til beregning af kanban-mængde til en kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="775e8-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="775e8-108">Opret en beregning af kanban-mængde</span><span class="sxs-lookup"><span data-stu-id="775e8-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="775e8-109">Gå til Produktionsstyring > Periodiske opgaver > Beregning af kanban-mængde > Beregn kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="775e8-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="775e8-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="775e8-110">Click New.</span></span>
3. <span data-ttu-id="775e8-111">Skriv "Speaker2016" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="775e8-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="775e8-112">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="775e8-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="775e8-113">Vælg den politik, du har oprettet i proceduren Føj en politik til beregning af kanban-mængde til en kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="775e8-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="775e8-114">F.eks. Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="775e8-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="775e8-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="775e8-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="775e8-116">I feltet Regel aktiv fra og med dato skal du angive dato og klokkeslæt til "2012-12-17T08:00:00".</span><span class="sxs-lookup"><span data-stu-id="775e8-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="775e8-117">Den dato bruges som basis for bestemmelse af, hvilke faste kanban-regler der medtages i beregning af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="775e8-118">I feltet Opfyldt efterspørgselsperiodes startdato skal du angive dato og klokkeslæt til "2012-11-17T09:00:00".</span><span class="sxs-lookup"><span data-stu-id="775e8-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="775e8-119">Datoen, fra hvilken tidligere efterspørgselstransaktioner medtages til beregning af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="775e8-120">I feltet Opfyldt efterspørgselsperiodes slutdato skal du angive dato og klokkeslæt til "2012-12-17T07:59:59".</span><span class="sxs-lookup"><span data-stu-id="775e8-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="775e8-121">Datoen, indtil hvilken tidligere efterspørgselstransaktioner medtages til beregning af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="775e8-122">I feltet Efterspørgselsperiodens startdato skal du angive dato og klokkeslæt til "2012-12-17T08:00:00".</span><span class="sxs-lookup"><span data-stu-id="775e8-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="775e8-123">Datoen, fra hvilken aktuelle efterspørgselstransaktioner medtages til beregning af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="775e8-124">I feltet Efterspørgselsperiodens slutdato skal du angive dato og klokkeslæt til "2013-01-16T07:59:59".</span><span class="sxs-lookup"><span data-stu-id="775e8-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="775e8-125">Datoen, indtil hvilken aktuelle efterspørgselstransaktioner medtages til beregning af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="775e8-126">Generer forslag til kanban-mængde</span><span class="sxs-lookup"><span data-stu-id="775e8-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="775e8-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="775e8-127">Click Save.</span></span>
2. <span data-ttu-id="775e8-128">Klik på Generer.</span><span class="sxs-lookup"><span data-stu-id="775e8-128">Click Generate.</span></span>
    * <span data-ttu-id="775e8-129">Dette genererer en forslagslinje til kanban-mængde i kanban-reglen 000020.</span><span class="sxs-lookup"><span data-stu-id="775e8-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="775e8-130">Kør beregning af kanban-mængde</span><span class="sxs-lookup"><span data-stu-id="775e8-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="775e8-131">Klik på Beregn.</span><span class="sxs-lookup"><span data-stu-id="775e8-131">Click Calculate.</span></span>
    * <span data-ttu-id="775e8-132">Derved beregnes forslaget til kanban-mængde.</span><span class="sxs-lookup"><span data-stu-id="775e8-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="775e8-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="775e8-133">Click OK.</span></span>
3. <span data-ttu-id="775e8-134">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="775e8-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="775e8-135">Bemærk, at den foreslåede kanban-mængden er 2.</span><span class="sxs-lookup"><span data-stu-id="775e8-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="775e8-136">Ændr produktmængde, og beregn igen</span><span class="sxs-lookup"><span data-stu-id="775e8-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="775e8-137">Angiv Produktmængde til "5".</span><span class="sxs-lookup"><span data-stu-id="775e8-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="775e8-138">Klik på Beregn.</span><span class="sxs-lookup"><span data-stu-id="775e8-138">Click Calculate.</span></span>
3. <span data-ttu-id="775e8-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="775e8-139">Click OK.</span></span>
    * <span data-ttu-id="775e8-140">Bemærk, at med en kanban-mængde på 5 ændres forslaget til en kanban-mængde på 4.</span><span class="sxs-lookup"><span data-stu-id="775e8-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="775e8-141">Dette skyldes, at med en lavere produktmængde har vi brug for flere kanbans for at opfylde behovet.</span><span class="sxs-lookup"><span data-stu-id="775e8-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="775e8-142">Opdater kanban-regel</span><span class="sxs-lookup"><span data-stu-id="775e8-142">Update kanban rule</span></span>
1. <span data-ttu-id="775e8-143">Angiv en dato og et klokkeslæt i feltet Reglens ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="775e8-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="775e8-144">Angiv "Regel aktiv fra og med dato" til en dato i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="775e8-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="775e8-145">F.eks. dags dato + et år.</span><span class="sxs-lookup"><span data-stu-id="775e8-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="775e8-146">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="775e8-146">Click Update.</span></span>
3. <span data-ttu-id="775e8-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="775e8-147">Click OK.</span></span>
4. <span data-ttu-id="775e8-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="775e8-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="775e8-149">Valider ændring af kanban-regel</span><span class="sxs-lookup"><span data-stu-id="775e8-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="775e8-150">Gå til Administration af produktoplysninger > Lean manufacturing > Kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="775e8-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="775e8-151">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="775e8-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="775e8-152">Vælg den kanban-regel, der er oprettet i den tidligere underopgave.</span><span class="sxs-lookup"><span data-stu-id="775e8-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="775e8-153">Dette bør være den første kanban-regel på listen sorteret efter nummer.</span><span class="sxs-lookup"><span data-stu-id="775e8-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="775e8-154">Slå udvidelsen af sektionen afsnittet Detaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="775e8-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="775e8-155">Bemærk ikrafttrædelsesdatoen, hvilket betyder at denne regel ikke aktiveres før denne dato.</span><span class="sxs-lookup"><span data-stu-id="775e8-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="775e8-156">Slå udvidelsen af sektionen Antal til/fra.</span><span class="sxs-lookup"><span data-stu-id="775e8-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="775e8-157">Bemærk, at dette er den standardmængde, som du angav i beregningen af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="775e8-158">Bemærk, at dette er den faste kanban-mængde på 4 fra beregningen af kanban-mængden.</span><span class="sxs-lookup"><span data-stu-id="775e8-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="775e8-159">Klik på fanen ListPanel.</span><span class="sxs-lookup"><span data-stu-id="775e8-159">Click the ListPanel tab.</span></span>


