--- 
title: Flytte planlagte kanban-job
description: "Denne fremgangsmåde fokuserer på flytning af planlagte kanban-procesjob til en anden periode."
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="efaa5-103">Flytte planlagte kanban-job</span><span class="sxs-lookup"><span data-stu-id="efaa5-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efaa5-104">Denne fremgangsmåde fokuserer på flytning af planlagte kanban-procesjob til en anden periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="efaa5-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="efaa5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="efaa5-106">Denne procedure er beregnet til tilsynsførende eller produktionsplanlæggere, der arbejder med kanbans.</span><span class="sxs-lookup"><span data-stu-id="efaa5-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="efaa5-107">Vælg planlagte kanban-job</span><span class="sxs-lookup"><span data-stu-id="efaa5-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="efaa5-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="efaa5-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="efaa5-109">!MtCMR!Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="efaa5-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="efaa5-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="efaa5-110">áçêìõý !</span></span>
3. <span data-ttu-id="efaa5-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="efaa5-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="efaa5-112">Vælg arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="efaa5-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="efaa5-113">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="efaa5-113">Klik på Select.</span></span>
5. <span data-ttu-id="efaa5-114">Vælg 'Planlagt' i feltet Vis jobstatus.</span><span class="sxs-lookup"><span data-stu-id="efaa5-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="efaa5-115">Dette filtrerer joblisten, så du får vist de planlagte kanban-job.</span><span class="sxs-lookup"><span data-stu-id="efaa5-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="efaa5-116">Flyt kanban-job til en anden periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="efaa5-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="efaa5-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="efaa5-118">Vælg et job, der har statussen Planlagt job, f.eks et job, der er planlagt til 20. december 2012 i feltet Planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="efaa5-119">Flyt derefter jobbet til forrige periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="efaa5-120">Klik på Forrige periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="efaa5-121">Klik på Afslut.</span><span class="sxs-lookup"><span data-stu-id="efaa5-121">Klik på End.</span></span>
    * <span data-ttu-id="efaa5-122">Dette vil flytte jobbet til slutningen af joblisten som det sidste job i den foregående periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="efaa5-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="efaa5-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="efaa5-124">Vælg et job, der har statussen Planlagt job, f.eks et job, der er planlagt til 18. december 2012 i feltet Planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="efaa5-125">Flyt derefter jobbet til næste periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="efaa5-126">Klik på Næste periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-126">Klik på Next period.</span></span>
6. <span data-ttu-id="efaa5-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="efaa5-127">Klik på Start.</span></span>
    * <span data-ttu-id="efaa5-128">Dette vil flytte jobbet til starten af joblisten som det første job i den foregående periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="efaa5-129">Opgave: Flyt et job inden for en periode</span><span class="sxs-lookup"><span data-stu-id="efaa5-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="efaa5-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="efaa5-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="efaa5-131">Vælg et job, der har statussen Planlagt job, f.eks det andet job, der er planlagt til 19. december 2012, i feltet Planlagt periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="efaa5-132">Flyt derefter jobbet inden for den planlagte periode.</span><span class="sxs-lookup"><span data-stu-id="efaa5-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="efaa5-133">Klik på Videresend.</span><span class="sxs-lookup"><span data-stu-id="efaa5-133">Klik på Forward.</span></span>
    * <span data-ttu-id="efaa5-134">Bemærk, at jobbet er flyttet én linje ned på listen.</span><span class="sxs-lookup"><span data-stu-id="efaa5-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="efaa5-135">Klik på Bagud.</span><span class="sxs-lookup"><span data-stu-id="efaa5-135">Klik på Backward.</span></span>
    * <span data-ttu-id="efaa5-136">Bemærk, at jobbet er flyttet én linje op på listen.</span><span class="sxs-lookup"><span data-stu-id="efaa5-136">Notice that the job is moved one line up on the list.</span></span>  


