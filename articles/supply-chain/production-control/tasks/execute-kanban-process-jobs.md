---
title: Udføre kanban-procesjob
description: Denne procedure drejer sig om at udføre kanban-procesjob.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62be1f116dfecbc4c6ba11053b94efc874baa3e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "357421"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="8a96f-103">Udføre kanban-procesjob</span><span class="sxs-lookup"><span data-stu-id="8a96f-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a96f-104">Denne procedure drejer sig om at udføre kanban-procesjob.</span><span class="sxs-lookup"><span data-stu-id="8a96f-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="8a96f-105">Det første job er fuldført med det forventede antal og har ingen fejl.</span><span class="sxs-lookup"><span data-stu-id="8a96f-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="8a96f-106">Det andet job er fuldført med fejl.</span><span class="sxs-lookup"><span data-stu-id="8a96f-106">The second job is completed with errors.</span></span> <span data-ttu-id="8a96f-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="8a96f-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8a96f-108">Denne procedure er beregnet til maskinoperatøren.</span><span class="sxs-lookup"><span data-stu-id="8a96f-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="8a96f-109">Vælge et kanban-job</span><span class="sxs-lookup"><span data-stu-id="8a96f-109">Select a kanban job</span></span>
1. <span data-ttu-id="8a96f-110">Gå til Produktionsstyring > Kanban > Kanban-område til procesjob.</span><span class="sxs-lookup"><span data-stu-id="8a96f-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="8a96f-111">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8a96f-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8a96f-112">Klik på rækken med ressourcegruppen 1250.</span><span class="sxs-lookup"><span data-stu-id="8a96f-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="8a96f-113">Dette filtrerer joblisten, så du kun får vist job for arbejdscelle 1250.</span><span class="sxs-lookup"><span data-stu-id="8a96f-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="8a96f-114">Markér den række, der har statussen Planlagt job.</span><span class="sxs-lookup"><span data-stu-id="8a96f-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="8a96f-115">Fuldføre et job med forventet antal</span><span class="sxs-lookup"><span data-stu-id="8a96f-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="8a96f-116">Vis eller skjul sektionen Detaljer.</span><span class="sxs-lookup"><span data-stu-id="8a96f-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="8a96f-117">Denne sektion viser vigtige oplysninger om kortnummer, varenummer, bestilt antal og aktivitetsnavn.</span><span class="sxs-lookup"><span data-stu-id="8a96f-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="8a96f-118">Udvid eller skjul sektionen Produktionsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="8a96f-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="8a96f-119">Denne sektion viser produktionsinstruktioner for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="8a96f-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="8a96f-120">Instruktionerne kan bestå af tekst, billeder, tegninger og andre dokumenter.</span><span class="sxs-lookup"><span data-stu-id="8a96f-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="8a96f-121">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="8a96f-121">Click Start.</span></span>
    * <span data-ttu-id="8a96f-122">Vælg et job, der ikke er fuldført.</span><span class="sxs-lookup"><span data-stu-id="8a96f-122">Select a job that is not completed.</span></span> <span data-ttu-id="8a96f-123">Brug statusikoner i feltet Jobstatus til at få vist jobstatus.</span><span class="sxs-lookup"><span data-stu-id="8a96f-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="8a96f-124">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="8a96f-124">Click Complete.</span></span>
    * <span data-ttu-id="8a96f-125">Jobbet er fuldført med den forventede kvalitet.</span><span class="sxs-lookup"><span data-stu-id="8a96f-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="8a96f-126">Fuldføre et job med fejl</span><span class="sxs-lookup"><span data-stu-id="8a96f-126">Complete a job with errors</span></span>
1. <span data-ttu-id="8a96f-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="8a96f-127">Click Start.</span></span>
    * <span data-ttu-id="8a96f-128">Når et job er fuldført, vælges det næste job på listen automatisk.</span><span class="sxs-lookup"><span data-stu-id="8a96f-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="8a96f-129">Dette er grunden til, at du ikke behøver at vælge et job, før du klikker på Start.</span><span class="sxs-lookup"><span data-stu-id="8a96f-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="8a96f-130">Klik på Produktion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8a96f-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="8a96f-131">Klik på Udført (detaljer).</span><span class="sxs-lookup"><span data-stu-id="8a96f-131">Click Complete (details).</span></span>
4. <span data-ttu-id="8a96f-132">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8a96f-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8a96f-133">Indtast et tal i feltet Antal fejl.</span><span class="sxs-lookup"><span data-stu-id="8a96f-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="8a96f-134">Indtast et tal i feltet Antal gode.</span><span class="sxs-lookup"><span data-stu-id="8a96f-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="8a96f-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8a96f-135">Click OK.</span></span>

