---
title: Gendan status for kanban-job
description: Denne procedure fokuserer på at vende tilbage til en forkert kanban-jobstatus.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ace8ff57b91828eb055658af5c8ecc50064ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831908"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="4efc2-103">Gendan status for kanban-job</span><span class="sxs-lookup"><span data-stu-id="4efc2-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4efc2-104">Denne procedure fokuserer på at vende tilbage til en forkert kanban-jobstatus.</span><span class="sxs-lookup"><span data-stu-id="4efc2-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="4efc2-105">Dette er nyttigt i tilfælde af, at maskinoperatøren opdaterer det forkerte job eller angiver forkert status ved en fejltagelse.</span><span class="sxs-lookup"><span data-stu-id="4efc2-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="4efc2-106">I denne procedure er et kanban-job registreret som fremstillet ved en fejltagelse, og status er tilbageført.</span><span class="sxs-lookup"><span data-stu-id="4efc2-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="4efc2-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="4efc2-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4efc2-108">Denne procedure er beregnet til den tilsynsførende eller maskinoperatøren, der arbejder i en virksomhed med lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="4efc2-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="4efc2-109">Åbn procesområdet for arbejdscellen.</span><span class="sxs-lookup"><span data-stu-id="4efc2-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="4efc2-110">Gå til Kanban-område til procesjob.</span><span class="sxs-lookup"><span data-stu-id="4efc2-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="4efc2-111">Indtast eller vælg en værdi i feltet Arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="4efc2-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="4efc2-112">Vælg arbejdscelle 1260.</span><span class="sxs-lookup"><span data-stu-id="4efc2-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="4efc2-113">Klargøre kanban-job</span><span class="sxs-lookup"><span data-stu-id="4efc2-113">Prepare kanban job</span></span>
1. <span data-ttu-id="4efc2-114">Klik på Klargør.</span><span class="sxs-lookup"><span data-stu-id="4efc2-114">Click Prepare.</span></span>
    * <span data-ttu-id="4efc2-115">Hvis du ikke kan klikke på Forbered, fordi det er nedtonet, skal du sørge for, at det valgte kanban-job har statussen Planlagt, som angives af det tomme kanban-ikon.</span><span class="sxs-lookup"><span data-stu-id="4efc2-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="4efc2-116">Hvis Forbered mislykkes, skal du kontrollere, at alle materialer på pluklisten, er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="4efc2-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="4efc2-117">Vælg det klargjorte job på listen.</span><span class="sxs-lookup"><span data-stu-id="4efc2-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="4efc2-118">Vælg det første job, du lige har klargjort.</span><span class="sxs-lookup"><span data-stu-id="4efc2-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="4efc2-119">Bemærk, at jobstatus er forberedt, hvilket er angivet med en trekant i kanban-ikonet.</span><span class="sxs-lookup"><span data-stu-id="4efc2-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="4efc2-120">Tilbageføre status for det forberedte kanban-job</span><span class="sxs-lookup"><span data-stu-id="4efc2-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="4efc2-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4efc2-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4efc2-122">Vælg det første job, der blev klargjort.</span><span class="sxs-lookup"><span data-stu-id="4efc2-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="4efc2-123">Klik på Produktion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4efc2-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="4efc2-124">Klik på Genindlæs status.</span><span class="sxs-lookup"><span data-stu-id="4efc2-124">Click Revert status.</span></span>
    * <span data-ttu-id="4efc2-125">Du kan bruge en alternativ kanban-regel, når følgende betingelser er opfyldt: - Genopfyldningsstrategien er den samme for begge regler.</span><span class="sxs-lookup"><span data-stu-id="4efc2-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="4efc2-126">- Versionen af produktionsflowet er den samme for begge regler.</span><span class="sxs-lookup"><span data-stu-id="4efc2-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="4efc2-127">- Det produkt, der leveres, er det samme for begge regler.</span><span class="sxs-lookup"><span data-stu-id="4efc2-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="4efc2-128">- Enhver downstream-aktivitet, der er konfigureret for den sidste aktivitet i kanban-reglerne, skal være den samme for begge regler.</span><span class="sxs-lookup"><span data-stu-id="4efc2-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="4efc2-129">- De samme angivne lagerdimensioner skal være konfigureret til begge regler.</span><span class="sxs-lookup"><span data-stu-id="4efc2-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="4efc2-130">- Status for materialehåndteringsenheden skal være Ikke-tildelt.</span><span class="sxs-lookup"><span data-stu-id="4efc2-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="4efc2-131">- Konfigurationen for hændelses-kanbans skal være den samme.</span><span class="sxs-lookup"><span data-stu-id="4efc2-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="4efc2-132">Sørg for, at den nye status er Planlagt.</span><span class="sxs-lookup"><span data-stu-id="4efc2-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="4efc2-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4efc2-133">Click OK.</span></span>
5. <span data-ttu-id="4efc2-134">Fjern markeringen af den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4efc2-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="4efc2-135">Vælg det samme job.</span><span class="sxs-lookup"><span data-stu-id="4efc2-135">Select the same job.</span></span>  
    * <span data-ttu-id="4efc2-136">Bemærk, at jobstatus for kanban-jobbet er ført tilbage til Planlagt, hvilket angives med et tomt kanban-ikon.</span><span class="sxs-lookup"><span data-stu-id="4efc2-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]