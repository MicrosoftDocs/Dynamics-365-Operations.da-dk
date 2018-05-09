--- 
title: "Overføre materialer med kanban-job (kun februar 2016)"
description: "Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e28ed504a945c162635c414bd156571a41faffe9
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="bc1fd-103">Overføre materialer med kanban-job (kun februar 2016)</span><span class="sxs-lookup"><span data-stu-id="bc1fd-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc1fd-104">Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="bc1fd-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bc1fd-106">Denne procedure er beregnet til lagerarbejderen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="bc1fd-107">Vis Overførselsjob</span><span class="sxs-lookup"><span data-stu-id="bc1fd-107">Display transfer jobs</span></span>
1. <span data-ttu-id="bc1fd-108">Gå til Produktionsstyring > Kanban > Kanban-område til overførselsjob.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="bc1fd-109">Udvis eller skjul sektionen Filtre.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="bc1fd-110">I sektionen Filtre kan du angive, hvilke job du vil se ved at filtrere på Produktionsflow, Navn på aktivitet, Fra lagersted og lokalitet og Til lagersted og lokalitet.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="bc1fd-111">Skriv "11" i feltet Fra lagersted.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="bc1fd-112">Skriv "12" i feltet en Til lokalitet.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="bc1fd-113">Start et overførselsjob</span><span class="sxs-lookup"><span data-stu-id="bc1fd-113">Start a transfer job</span></span>
1. <span data-ttu-id="bc1fd-114">Fjern markeringen af den valgte række, hvis der er en, på listen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="bc1fd-115">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="bc1fd-116">Vælg det første job med status som ikke-planlagt.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="bc1fd-117">Kontrollér, at dette er det eneste job, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="bc1fd-118">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-118">Click Start.</span></span>
    * <span data-ttu-id="bc1fd-119">Bemærk, at et ikon angiver, at jobbet er startet.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="bc1fd-120">Vælg et andet overførselsjob, og ret mængde</span><span class="sxs-lookup"><span data-stu-id="bc1fd-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="bc1fd-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bc1fd-122">Du kan vælge flere job, men vælg række 5 for nu.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="bc1fd-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bc1fd-124">Kontrollér, at jobbet i det forrige trin er det eneste, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="bc1fd-125">Fravælg alle andre job.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="bc1fd-126">Notér værdien i feltet Jobantal til fremtidig reference</span><span class="sxs-lookup"><span data-stu-id="bc1fd-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="bc1fd-127">Indstil Jobantal til "30".</span><span class="sxs-lookup"><span data-stu-id="bc1fd-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="bc1fd-128">Bemærk advarslen!</span><span class="sxs-lookup"><span data-stu-id="bc1fd-128">Notice the warning!</span></span> <span data-ttu-id="bc1fd-129">Du har ikke tilladelse til at overføre 30.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="bc1fd-130">Du kan kun overføre den oprindelige mængde i overensstemmelse med opsætningen af kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="bc1fd-131">Brug den værdi, der tidligere er noteret i feltet Jobantal</span><span class="sxs-lookup"><span data-stu-id="bc1fd-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="bc1fd-132">Angiv Jobantallet til den forrige værdi.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="bc1fd-133">Start det andet overførselsjob</span><span class="sxs-lookup"><span data-stu-id="bc1fd-133">Start the second transfer job</span></span>
1. <span data-ttu-id="bc1fd-134">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-134">Click Start.</span></span>
    * <span data-ttu-id="bc1fd-135">Dette starter overførslen af jobbet i række 5.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="bc1fd-136">Udfør begge overførselsjob</span><span class="sxs-lookup"><span data-stu-id="bc1fd-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="bc1fd-137">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="bc1fd-138">Nu vælges to overførselsjob på række 4 og række 5.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="bc1fd-139">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-139">Click Complete.</span></span>
    * <span data-ttu-id="bc1fd-140">Dette fuldfører overførsel af begge job.</span><span class="sxs-lookup"><span data-stu-id="bc1fd-140">This will complete the transfer of both jobs.</span></span>  


