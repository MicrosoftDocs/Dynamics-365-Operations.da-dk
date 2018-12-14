--- 
title: Flytte planlagte kanban-job
description: "Denne fremgangsmåde fokuserer på flytning af planlagte kanban-procesjob til en anden periode."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="398cf-103">Flytte planlagte kanban-job</span><span class="sxs-lookup"><span data-stu-id="398cf-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="398cf-104">Denne fremgangsmåde fokuserer på flytning af planlagte kanban-procesjob til en anden periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="398cf-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="398cf-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="398cf-106">Denne procedure er beregnet til tilsynsførende eller produktionsplanlæggere, der arbejder med kanbans.</span><span class="sxs-lookup"><span data-stu-id="398cf-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="398cf-107">Vælg planlagte kanban-job.</span><span class="sxs-lookup"><span data-stu-id="398cf-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="398cf-108">Gå til **Produktionsstyring > Kanban > Tidsplanlægning af kanban-job**.</span><span class="sxs-lookup"><span data-stu-id="398cf-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="398cf-109">Klik på rullelisten i feltet **Arbejdscelle** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="398cf-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="398cf-110">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="398cf-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="398cf-111">Vælg arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="398cf-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="398cf-112">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="398cf-112">Click **Select**.</span></span> 

5. <span data-ttu-id="398cf-113">Vælg **Planlagt** i feltet **Vis jobstatus**.</span><span class="sxs-lookup"><span data-stu-id="398cf-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="398cf-114">Dette filtrerer joblisten, så du får vist de planlagte kanban-job.</span><span class="sxs-lookup"><span data-stu-id="398cf-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="398cf-115">Flyt kanban-job til en anden periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="398cf-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="398cf-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="398cf-117">Vælg et job, der har statussen **Planlagt job**, f.eks et job, der er planlagt til 20. december 2012 i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="398cf-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="398cf-118">Flyt derefter jobbet til forrige periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="398cf-119">Klik på **Forrige periode**.</span><span class="sxs-lookup"><span data-stu-id="398cf-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="398cf-120">Klik på **Slut** for at flytte jobbet til slutningen af joblisten som det sidste job i den foregående periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="398cf-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="398cf-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="398cf-122">Vælg et job, der har statussen **Planlagt job**, f.eks et job, der er planlagt til 18. december 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="398cf-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="398cf-123">Flyt derefter jobbet til næste periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="398cf-124">Klik på **Næste periode**.</span><span class="sxs-lookup"><span data-stu-id="398cf-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="398cf-125">Klik på **Start** for at flytte jobbet til starten af joblisten som det første job i den foregående periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="398cf-126">Flyt et job inden for en periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="398cf-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="398cf-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="398cf-128">Vælg et job, der har statussen Planlagt job, f.eks det andet job, der er planlagt til 19. december 2012, i feltet **Planlagt periode**.</span><span class="sxs-lookup"><span data-stu-id="398cf-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="398cf-129">Flyt derefter jobbet inden for den planlagte periode.</span><span class="sxs-lookup"><span data-stu-id="398cf-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="398cf-130">Klik på **Fremad**.</span><span class="sxs-lookup"><span data-stu-id="398cf-130">Click **Forward**.</span></span> <span data-ttu-id="398cf-131">Bemærk, at jobbet er flyttet én linje ned på listen.</span><span class="sxs-lookup"><span data-stu-id="398cf-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="398cf-132">Klik på **Baglæns**.</span><span class="sxs-lookup"><span data-stu-id="398cf-132">Click **Backward**.</span></span> <span data-ttu-id="398cf-133">Bemærk, at jobbet er flyttet én linje op på listen.</span><span class="sxs-lookup"><span data-stu-id="398cf-133">Notice that the job is moved one line up on the list.</span></span>

