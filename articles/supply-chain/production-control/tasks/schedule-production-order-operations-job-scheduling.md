--- 
title: "Planlægge en produktionsordre med grov- og finplanlægning"
description: "Denne procedure drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0f443918890a36cebf5935b60ed66b495e5f353e
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="6806c-103">Planlægge en produktionsordre med grov- og finplanlægning</span><span class="sxs-lookup"><span data-stu-id="6806c-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6806c-104">Denne procedure drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="6806c-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="6806c-105">Der oprettes ingen job med grovplanlægning, kun job med finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="6806c-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="6806c-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6806c-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="6806c-107">Denne procedure er beregnet til produktionslederen, produktionsplanlæggeren eller den produktionstilsynsførende, der arbejder i et dedikeret produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="6806c-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="6806c-108">Oprette en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="6806c-108">Create a production order</span></span>
1. <span data-ttu-id="6806c-109">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="6806c-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="6806c-110">Klik på Ny produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="6806c-110">Click New production order.</span></span>
3. <span data-ttu-id="6806c-111">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="6806c-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6806c-112">Vælg varenummer D0001.</span><span class="sxs-lookup"><span data-stu-id="6806c-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="6806c-113">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="6806c-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="6806c-114">Grovplanlægge for en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="6806c-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="6806c-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6806c-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6806c-116">Vælg den produktionsordre, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="6806c-116">Select the production order that you have just created.</span></span> <span data-ttu-id="6806c-117">Det skal være øverst på listen.</span><span class="sxs-lookup"><span data-stu-id="6806c-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="6806c-118">Klik på Planlæg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6806c-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="6806c-119">Klik på Grovplanlægge.</span><span class="sxs-lookup"><span data-stu-id="6806c-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="6806c-120">Vælg 'Fremad fra planlægningsdato' i feltet Planlægningsvej.</span><span class="sxs-lookup"><span data-stu-id="6806c-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="6806c-121">Angiv en dato i feltet Planlægningsdato.</span><span class="sxs-lookup"><span data-stu-id="6806c-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="6806c-122">Vælg en dato i fremtiden, for eksempel i dag plus en uge.</span><span class="sxs-lookup"><span data-stu-id="6806c-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="6806c-123">Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.</span><span class="sxs-lookup"><span data-stu-id="6806c-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="6806c-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6806c-124">Click OK.</span></span>
7. <span data-ttu-id="6806c-125">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6806c-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6806c-126">Bemærk, at status ændres til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="6806c-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="6806c-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6806c-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6806c-128">Klik på Alle job.</span><span class="sxs-lookup"><span data-stu-id="6806c-128">Click All jobs.</span></span>
    * <span data-ttu-id="6806c-129">Bemærk, at der ikke oprettes nogen job til grovplanlægning.</span><span class="sxs-lookup"><span data-stu-id="6806c-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="6806c-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6806c-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="6806c-131">Finplanlægge for en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="6806c-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="6806c-132">Klik på Planlæg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6806c-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="6806c-133">Klik på Finplanlægge.</span><span class="sxs-lookup"><span data-stu-id="6806c-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="6806c-134">Vælg 'Fremad fra planlægningsdato' i feltet Planlægningsvej.</span><span class="sxs-lookup"><span data-stu-id="6806c-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="6806c-135">Angiv en dato i feltet Planlægningsdato.</span><span class="sxs-lookup"><span data-stu-id="6806c-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="6806c-136">Vælg en dato i fremtiden, for eksempel i dag plus en uge.</span><span class="sxs-lookup"><span data-stu-id="6806c-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="6806c-137">Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.</span><span class="sxs-lookup"><span data-stu-id="6806c-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="6806c-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6806c-138">Click OK.</span></span>
6. <span data-ttu-id="6806c-139">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6806c-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="6806c-140">Klik på Alle job.</span><span class="sxs-lookup"><span data-stu-id="6806c-140">Click All jobs.</span></span>
    * <span data-ttu-id="6806c-141">Bemærk, at der baseret på den aktive rute oprettes fem jo med finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="6806c-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


