---
title: Overføre materialer med kanban-job
description: Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df65ea59be29dbe4eaad30558fcff4394737158f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224924"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="6b8cc-103">Overføre materialer med kanban-job</span><span class="sxs-lookup"><span data-stu-id="6b8cc-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b8cc-104">Denne fremgangsmåde fokuserer på at udtrække et kanban-job for at overføre materialer.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="6b8cc-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6b8cc-106">Denne procedure er beregnet til lagerarbejderen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="6b8cc-107">Vis Overførselsjob</span><span class="sxs-lookup"><span data-stu-id="6b8cc-107">Display transfer jobs</span></span>
1. <span data-ttu-id="6b8cc-108">Gå til Produktionsstyring > Kanban > Kanban-område til overførselsjob.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="6b8cc-109">Udvis eller skjul sektionen Filtre.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="6b8cc-110">I sektionen Filtre kan du angive, hvilke job du vil se ved at filtrere på Produktionsflow, Navn på aktivitet, Fra lagersted og lokalitet og Til lagersted og lokalitet.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="6b8cc-111">Skriv "11" i feltet Fra lagersted.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="6b8cc-112">Skriv "12" i feltet en Til lokalitet.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="6b8cc-113">Start et overførselsjob</span><span class="sxs-lookup"><span data-stu-id="6b8cc-113">Start a transfer job</span></span>
1. <span data-ttu-id="6b8cc-114">Fjern markeringen af den valgte række, hvis der er en, på listen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="6b8cc-115">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="6b8cc-116">Vælg det første job med status som ikke-planlagt.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="6b8cc-117">Kontrollér, at dette er det eneste job, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="6b8cc-118">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-118">Click Start.</span></span>
    * <span data-ttu-id="6b8cc-119">Bemærk, at et ikon angiver, at jobbet er startet.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="6b8cc-120">Vælg et andet overførselsjob, og ret mængde</span><span class="sxs-lookup"><span data-stu-id="6b8cc-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="6b8cc-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b8cc-122">Du kan vælge flere job, men vælg række 5 for nu.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="6b8cc-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6b8cc-124">Kontrollér, at jobbet i det forrige trin er det eneste, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="6b8cc-125">Fravælg alle andre job.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="6b8cc-126">Notér værdien i feltet Jobantal til fremtidig reference</span><span class="sxs-lookup"><span data-stu-id="6b8cc-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="6b8cc-127">Indstil Jobantal til "30".</span><span class="sxs-lookup"><span data-stu-id="6b8cc-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="6b8cc-128">Bemærk advarslen!</span><span class="sxs-lookup"><span data-stu-id="6b8cc-128">Notice the warning!</span></span> <span data-ttu-id="6b8cc-129">Du har ikke tilladelse til at overføre 30.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="6b8cc-130">Du kan kun overføre den oprindelige mængde i overensstemmelse med opsætningen af kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="6b8cc-131">Brug den værdi, der tidligere er noteret i feltet Jobantal</span><span class="sxs-lookup"><span data-stu-id="6b8cc-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="6b8cc-132">Angiv Jobantallet til den forrige værdi.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="6b8cc-133">Start det andet overførselsjob</span><span class="sxs-lookup"><span data-stu-id="6b8cc-133">Start the second transfer job</span></span>
1. <span data-ttu-id="6b8cc-134">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-134">Click Start.</span></span>
    * <span data-ttu-id="6b8cc-135">Dette starter overførslen af jobbet i række 5.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="6b8cc-136">Udfør begge overførselsjob</span><span class="sxs-lookup"><span data-stu-id="6b8cc-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="6b8cc-137">Markér række 4 på listen.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="6b8cc-138">Nu vælges to overførselsjob på række 4 og række 5.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="6b8cc-139">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-139">Click Complete.</span></span>
    * <span data-ttu-id="6b8cc-140">Dette fuldfører overførsel af begge job.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-140">This will complete the transfer of both jobs.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]