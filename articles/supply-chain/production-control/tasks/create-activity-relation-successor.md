--- 
title: "Oprette aktivitetsrelation - Efterfølgende"
description: Flowet af aktiviteter i et lean produktionsflow dokumenteres via aktivitetsrelationer.
author: cvocph
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
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 75a76252cc3cb6f3e7516309a7d9a6f2d1934ccd
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-activity-relation-successor"></a><span data-ttu-id="cd064-103">Oprette aktivitetsrelation: Efterfølgende aktivitet</span><span class="sxs-lookup"><span data-stu-id="cd064-103">Create activity relation: Successor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd064-104">Flowet af aktiviteter i et lean produktionsflow dokumenteres via aktivitetsrelationer.</span><span class="sxs-lookup"><span data-stu-id="cd064-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="cd064-105">Denne optagelse viser, hvordan du opretter en aktivitetsrelation.</span><span class="sxs-lookup"><span data-stu-id="cd064-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="cd064-106">Forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="cd064-106">Prerequisites:</span></span>

- <span data-ttu-id="cd064-107">Et produktionsflow og en version i kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="cd064-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="cd064-108">To aktiviteter, der følger efter hinanden i produktionsflowet, er oprettet, men ikke relateret.</span><span class="sxs-lookup"><span data-stu-id="cd064-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="cd064-109">Find produktionsflowversionen</span><span class="sxs-lookup"><span data-stu-id="cd064-109">Find the production flow version</span></span> 
1. <span data-ttu-id="cd064-110">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="cd064-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="cd064-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cd064-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cd064-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd064-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cd064-113">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd064-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="cd064-114">Vælg en kladdeversion på listen.</span><span class="sxs-lookup"><span data-stu-id="cd064-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="cd064-115">Aktivitetsrelationer kan føjes til både kladdeversioner eller aktive versioner af et produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="cd064-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="cd064-116">Åbn den aktivitetsoversigten</span><span class="sxs-lookup"><span data-stu-id="cd064-116">Open the activity overview</span></span>
1. <span data-ttu-id="cd064-117">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cd064-117">Click Activities.</span></span>
    * <span data-ttu-id="cd064-118">Bemærk, at formularen viser alle aktiviteter i produktionsflowet, der er allokeret til versionen af de produktionsflow, du arbejder i.</span><span class="sxs-lookup"><span data-stu-id="cd064-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="cd064-119">Tilføj en efterfølgende aktivitet</span><span class="sxs-lookup"><span data-stu-id="cd064-119">Add a Successor</span></span>
1. <span data-ttu-id="cd064-120">Klik på Tilføj efterfølgende aktivitet.</span><span class="sxs-lookup"><span data-stu-id="cd064-120">Click Add successor.</span></span>
2. <span data-ttu-id="cd064-121">Klik på rullelisten i feltet Aktivitet for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="cd064-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cd064-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="cd064-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cd064-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cd064-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cd064-124">Markér afkrydsningsfeltet Begrænsning.</span><span class="sxs-lookup"><span data-stu-id="cd064-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="cd064-125">Skriv et tal i feltet Begrænsningsværdi.</span><span class="sxs-lookup"><span data-stu-id="cd064-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="cd064-126">Begrænsningstiden er den tid, der skal planlægges mellem den planlagte afslutning af den foregående aktivitet (forfaldsdato og tid) og det planlagte starttidspunkt for den efterfølgende aktivitet.</span><span class="sxs-lookup"><span data-stu-id="cd064-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="cd064-127">Angiv en værdi i feltet Enheder.</span><span class="sxs-lookup"><span data-stu-id="cd064-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="cd064-128">Angiv et tal i feltet Procestidsforhold.</span><span class="sxs-lookup"><span data-stu-id="cd064-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="cd064-129">Hvis begge aktiviteter kører i den samme takt, skal procestidsforholdet være 1.</span><span class="sxs-lookup"><span data-stu-id="cd064-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="cd064-130">Hvis den foregående opgave kører med dobbelt hastighed af den efterfølgende, skal forholdet være 2.</span><span class="sxs-lookup"><span data-stu-id="cd064-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="cd064-131">Procestidsforholdene bruges til at beregne de enkelte procestider for produktionsflowaktiviteterne.</span><span class="sxs-lookup"><span data-stu-id="cd064-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="cd064-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cd064-132">Click OK.</span></span>
10. <span data-ttu-id="cd064-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cd064-133">Close the page.</span></span>
11. <span data-ttu-id="cd064-134">Klik på fanen GridPanel.</span><span class="sxs-lookup"><span data-stu-id="cd064-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="cd064-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cd064-135">Close the page.</span></span>
13. <span data-ttu-id="cd064-136">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="cd064-136">Refresh the page.</span></span>


