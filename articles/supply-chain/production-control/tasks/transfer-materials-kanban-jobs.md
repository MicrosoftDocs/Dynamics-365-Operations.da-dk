---
title: Overføre materialer med kanban-job
description: Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcab5d27d1e5bb2f86910fe083168e7b97c52e2f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148786"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="3933a-103">Overføre materialer med kanban-job</span><span class="sxs-lookup"><span data-stu-id="3933a-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3933a-104">Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer.</span><span class="sxs-lookup"><span data-stu-id="3933a-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="3933a-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="3933a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3933a-106">Denne procedure er beregnet til lagerarbejderen.</span><span class="sxs-lookup"><span data-stu-id="3933a-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="3933a-107">Vis Overførselsjob</span><span class="sxs-lookup"><span data-stu-id="3933a-107">Display transfer jobs</span></span>
1. <span data-ttu-id="3933a-108">Gå til Produktionsstyring > Kanban > Kanban-område til overførselsjob.</span><span class="sxs-lookup"><span data-stu-id="3933a-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="3933a-109">Udvis eller skjul sektionen Filtre.</span><span class="sxs-lookup"><span data-stu-id="3933a-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="3933a-110">I sektionen Filtre kan du angive, hvilke job du vil se ved at filtrere på Produktionsflow, Navn på aktivitet, Fra lagersted og lokalitet og Til lagersted og lokalitet.</span><span class="sxs-lookup"><span data-stu-id="3933a-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="3933a-111">Skriv "11" i feltet Fra lagersted.</span><span class="sxs-lookup"><span data-stu-id="3933a-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="3933a-112">Skriv "12" i feltet en Til lokalitet.</span><span class="sxs-lookup"><span data-stu-id="3933a-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="3933a-113">Start et overførselsjob</span><span class="sxs-lookup"><span data-stu-id="3933a-113">Start a transfer job</span></span>
1. <span data-ttu-id="3933a-114">Fjern markeringen af den valgte række, hvis der er en, på listen.</span><span class="sxs-lookup"><span data-stu-id="3933a-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="3933a-115">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="3933a-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="3933a-116">Vælg det første job med status som ikke-planlagt.</span><span class="sxs-lookup"><span data-stu-id="3933a-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="3933a-117">Kontrollér, at dette er det eneste job, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="3933a-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="3933a-118">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="3933a-118">Click Start.</span></span>
    * <span data-ttu-id="3933a-119">Bemærk, at et ikon angiver, at jobbet er startet.</span><span class="sxs-lookup"><span data-stu-id="3933a-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="3933a-120">Vælg et andet overførselsjob, og ret mængde</span><span class="sxs-lookup"><span data-stu-id="3933a-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="3933a-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3933a-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3933a-122">Du kan vælge flere job, men vælg række 5 for nu.</span><span class="sxs-lookup"><span data-stu-id="3933a-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="3933a-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3933a-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3933a-124">Kontrollér, at jobbet i det forrige trin er det eneste, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="3933a-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="3933a-125">Fravælg alle andre job.</span><span class="sxs-lookup"><span data-stu-id="3933a-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="3933a-126">Notér værdien i feltet Jobantal til fremtidig reference</span><span class="sxs-lookup"><span data-stu-id="3933a-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="3933a-127">Indstil Jobantal til "30".</span><span class="sxs-lookup"><span data-stu-id="3933a-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="3933a-128">Bemærk advarslen!</span><span class="sxs-lookup"><span data-stu-id="3933a-128">Notice the warning!</span></span> <span data-ttu-id="3933a-129">Du har ikke tilladelse til at overføre 30.</span><span class="sxs-lookup"><span data-stu-id="3933a-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="3933a-130">Du kan kun overføre den oprindelige mængde i overensstemmelse med opsætningen af kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="3933a-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="3933a-131">Brug den værdi, der tidligere er noteret i feltet Jobantal</span><span class="sxs-lookup"><span data-stu-id="3933a-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="3933a-132">Angiv Jobantallet til den forrige værdi.</span><span class="sxs-lookup"><span data-stu-id="3933a-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="3933a-133">Start det andet overførselsjob</span><span class="sxs-lookup"><span data-stu-id="3933a-133">Start the second transfer job</span></span>
1. <span data-ttu-id="3933a-134">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="3933a-134">Click Start.</span></span>
    * <span data-ttu-id="3933a-135">Dette starter overførslen af jobbet i række 5.</span><span class="sxs-lookup"><span data-stu-id="3933a-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="3933a-136">Udfør begge overførselsjob</span><span class="sxs-lookup"><span data-stu-id="3933a-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="3933a-137">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="3933a-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="3933a-138">Nu vælges to overførselsjob på række 4 og række 5.</span><span class="sxs-lookup"><span data-stu-id="3933a-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="3933a-139">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="3933a-139">Click Complete.</span></span>
    * <span data-ttu-id="3933a-140">Dette fuldfører overførsel af begge job.</span><span class="sxs-lookup"><span data-stu-id="3933a-140">This will complete the transfer of both jobs.</span></span>  

