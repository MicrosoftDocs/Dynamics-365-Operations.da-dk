---
title: Fjerne et kanban-job fra planen
description: Denne fremgangsmåde fokuserer på at fjerne et planlagt kanban-procesjob fra tidsplanen ved at gendanne jobstatussen til Ikke planlagt.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566a174c631391577441e0f890bd9553dac0891c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204514"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="d28bc-103">Fjerne et kanban-job fra planen</span><span class="sxs-lookup"><span data-stu-id="d28bc-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d28bc-104">Denne fremgangsmåde fokuserer på at fjerne et planlagt kanban-procesjob fra tidsplanen ved at gendanne jobstatussen til Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="d28bc-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="d28bc-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="d28bc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d28bc-106">Denne procedure er beregnet til tilsynsførende eller produktionsplanlæggere.</span><span class="sxs-lookup"><span data-stu-id="d28bc-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="d28bc-107">Find et planlagt kanban-job</span><span class="sxs-lookup"><span data-stu-id="d28bc-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="d28bc-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="d28bc-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="d28bc-109">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d28bc-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d28bc-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d28bc-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d28bc-111">Vælg arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="d28bc-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="d28bc-112">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="d28bc-112">Click Select.</span></span>
5. <span data-ttu-id="d28bc-113">Vælg "Planlagt" i feltet Vis jobstatus.</span><span class="sxs-lookup"><span data-stu-id="d28bc-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="d28bc-114">Fjern det planlagte kanban-job fra tidsplanen</span><span class="sxs-lookup"><span data-stu-id="d28bc-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="d28bc-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d28bc-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d28bc-116">Vælg et job, der har statussen Planlagt, for eksempel et job fra 19. december 2012.</span><span class="sxs-lookup"><span data-stu-id="d28bc-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="d28bc-117">Klik på Plan i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d28bc-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="d28bc-118">Klik på Gendan jobstatus.</span><span class="sxs-lookup"><span data-stu-id="d28bc-118">Click Revert job status.</span></span>
4. <span data-ttu-id="d28bc-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d28bc-119">Click OK.</span></span>
    * <span data-ttu-id="d28bc-120">Dette vil gendanne jobbets aktuelle status fra "Planlagt" til "Ikke planlagt" og fjerne det fra procesområdet.</span><span class="sxs-lookup"><span data-stu-id="d28bc-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]