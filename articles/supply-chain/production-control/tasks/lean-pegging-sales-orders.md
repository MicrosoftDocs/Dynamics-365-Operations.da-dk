---
title: Om udligning fra salgsordrer
description: Denne procedure fokuserer på validering af udligningstræet fra en salgslinje, hvor varen produceres med kanbans.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5142fe552147a9b2988a8828ba1206fad9e252e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146738"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="0bdb6-103">Om udligning fra salgsordrer</span><span class="sxs-lookup"><span data-stu-id="0bdb6-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0bdb6-104">Denne procedure fokuserer på validering af udligningstræet fra en salgslinje, hvor varen produceres med kanbans.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="0bdb6-105">Efter validering af udligningstræet, er alle kanban-job planlagt.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="0bdb6-106">Dette er nyttigt for ordrescenarier, hvor ordretageren skal sikre, at produktionen kan påbegyndes straks.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="0bdb6-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0bdb6-108">Denne procedure er beregnet til den avancerede ordretager, der arbejder i en lean virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="0bdb6-109">Oprette en salgsordre for en kanban-kontrolleret vare</span><span class="sxs-lookup"><span data-stu-id="0bdb6-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="0bdb6-110">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="0bdb6-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-111">Click New.</span></span>
3. <span data-ttu-id="0bdb6-112">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="0bdb6-113">Brug US-001.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-113">Use US-001.</span></span>  
4. <span data-ttu-id="0bdb6-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-114">Click OK.</span></span>
5. <span data-ttu-id="0bdb6-115">Skriv 'L0001' i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="0bdb6-116">Angiv antallet til '30'.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="0bdb6-117">Det er vigtigt, at mængden er større end 24 for at udløse hændelsens kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="0bdb6-118">Åbne et udligningstræ</span><span class="sxs-lookup"><span data-stu-id="0bdb6-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="0bdb6-119">Klik på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-119">Click Product and supply.</span></span>
2. <span data-ttu-id="0bdb6-120">Klik på Vis udligningstræ.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="0bdb6-121">Bemærk, at udligningstræet viser alle niveauer af udligning, der er nødvendige for salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="0bdb6-122">I dette tilfælde er der to niveauer af kanbans og alle de nødvendige komponenter.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="0bdb6-123">Planlæg udligningstræet</span><span class="sxs-lookup"><span data-stu-id="0bdb6-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="0bdb6-124">I træet vælg "Salgslinje 000832\Kanban 000558".</span><span class="sxs-lookup"><span data-stu-id="0bdb6-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="0bdb6-125">Udvid sektionen Kanban-job.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="0bdb6-126">Bemærk, at jobstatus for kanban-jobbet er Ikke planlagt.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="0bdb6-127">Klik på Planlæg hele udligningstræet.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="0bdb6-128">Dette vil planlægge alle kanban-job i udligningstræet, ændre jobstatus fra ikke-planlagt til planlagt.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="0bdb6-129">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-129">Refresh the page.</span></span>
    * <span data-ttu-id="0bdb6-130">Bemærk, at den pågældende kanban jobstatus blev ændret fra Ikke planlagt til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="0bdb6-131">Vælg "Salgslinje 000832\Kanban 000558\Afgang for L0001\Kanban 000559" i træet.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="0bdb6-132">Jobbet for den anden kanban er også planlagt, fordi hele udligningstræet er planlagt.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="0bdb6-133">Bemærk, at den pågældende kanbanjobstatus blev ændret fra Ikke planlagt til Planlagt.</span><span class="sxs-lookup"><span data-stu-id="0bdb6-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

