--- 
title: "Planlægge kanban-job"
description: "Denne fremgangsmåde fokuserer på planlægning af kanban-procesjob for en bestemt arbejdscelle."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 94fed8f638efa629e548947088a631292437a2b1
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="62671-103">Planlægge kanban-job</span><span class="sxs-lookup"><span data-stu-id="62671-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62671-104">Denne fremgangsmåde fokuserer på planlægning af kanban-procesjob for en bestemt arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="62671-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="62671-105">Proceduren "Klargør et kanban-procesjob, når materialerne ikke er tilgængelige" er en forudsætning for oprettelsen af denne procedure.</span><span class="sxs-lookup"><span data-stu-id="62671-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="62671-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="62671-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="62671-107">Denne opgave er beregnet til tilsynsførende og produktionsplanlæggere, der arbejder med kanbans.</span><span class="sxs-lookup"><span data-stu-id="62671-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="62671-108">Vælg kanban-job til en arbejdscelle</span><span class="sxs-lookup"><span data-stu-id="62671-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="62671-109">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="62671-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="62671-110">Udvid faktaboksen Periodekapacitet</span><span class="sxs-lookup"><span data-stu-id="62671-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="62671-111">Udvid faktaboksen Kanban.</span><span class="sxs-lookup"><span data-stu-id="62671-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="62671-112">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="62671-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="62671-113">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="62671-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="62671-114">Vælg arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="62671-114">Select work cell 1250.</span></span> <span data-ttu-id="62671-115">Dette vil filtrere visningen, så du kun får vist job for arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="62671-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="62671-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="62671-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="62671-117">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="62671-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="62671-118">Planlæg et kanban-jobbet i den første tilgængelige periode.</span><span class="sxs-lookup"><span data-stu-id="62671-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="62671-119">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="62671-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="62671-120">Markér den første række på listen, der har statussen Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="62671-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="62671-121">Ikonet med prikker i feltet Jobstatus angiver ikke-planlagte.</span><span class="sxs-lookup"><span data-stu-id="62671-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="62671-122">Klik på Planlæg.</span><span class="sxs-lookup"><span data-stu-id="62671-122">Click Schedule.</span></span>
    * <span data-ttu-id="62671-123">Dette vil planlægge kanban-jobbet i den første tilgængelige periode.</span><span class="sxs-lookup"><span data-stu-id="62671-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="62671-124">Bemærk, at kanban-jobbet flyttes til slutningen af listen, fordi den er blevet føjet til den periode, der starter fra dags dato.</span><span class="sxs-lookup"><span data-stu-id="62671-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="62671-125">Hvis den periode, der starter fra i dag er fuldt booket, flyttes jobbet til den første tilgængelige periode.</span><span class="sxs-lookup"><span data-stu-id="62671-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="62671-126">Planlæg to kanban-job for en bestemt dag</span><span class="sxs-lookup"><span data-stu-id="62671-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="62671-127">Markér række 1 på listen.</span><span class="sxs-lookup"><span data-stu-id="62671-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="62671-128">Du bør se, at den første række har statussen Ikke planlagt i feltet Jobstatus.</span><span class="sxs-lookup"><span data-stu-id="62671-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="62671-129">Markér række 2 på listen.</span><span class="sxs-lookup"><span data-stu-id="62671-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="62671-130">Du bør se, at den anden række har statussen Ikke planlagt i feltet Jobstatus.</span><span class="sxs-lookup"><span data-stu-id="62671-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="62671-131">Du har nu de to første job, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="62671-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="62671-132">Klik på Planlæg fra dato for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="62671-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="62671-133">Markér eller fjern markeringen i boksen Tilsidesæt reaktion på manglende kapacitet.</span><span class="sxs-lookup"><span data-stu-id="62671-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="62671-134">Denne indstilling giver dig mulighed for at tilsidesætte standardreaktionen på manglende kapacitet.</span><span class="sxs-lookup"><span data-stu-id="62671-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="62671-135">Vælg "Føj til den angivne periode" i feltet Reaktion på manglende kapacitet.</span><span class="sxs-lookup"><span data-stu-id="62671-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="62671-136">Denne indstilling sikrer, at jobbet føjes til den angivne periode, uanset om arbejdscellen muligvis er overbelastet.</span><span class="sxs-lookup"><span data-stu-id="62671-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="62671-137">Klik på Planlæg.</span><span class="sxs-lookup"><span data-stu-id="62671-137">Click Schedule.</span></span>
    * <span data-ttu-id="62671-138">Bemærk, at begge job er føjet til den ønskede periode.</span><span class="sxs-lookup"><span data-stu-id="62671-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="62671-139">Du kan se belastningen for hver periode i sektionen Periodekapacitet.</span><span class="sxs-lookup"><span data-stu-id="62671-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="62671-140">Feltet Forbrug viser det planlagte forbrug i denne periode.</span><span class="sxs-lookup"><span data-stu-id="62671-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="62671-141">Hvis det planlagte forbrug er højere end den tilgængelige kapacitet i denne periode, vælges det overbelastede forbrug.</span><span class="sxs-lookup"><span data-stu-id="62671-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  


