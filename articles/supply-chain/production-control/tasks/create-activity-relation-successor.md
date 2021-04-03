---
title: Oprette aktivitetsrelation - Efterfølgende
description: Flowet af aktiviteter i et lean produktionsflow dokumenteres via aktivitetsrelationer.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f10ecb8e579975327440ede6ea383226645c8cf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255295"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="b186e-103">Oprette aktivitetsrelation - Efterfølgende</span><span class="sxs-lookup"><span data-stu-id="b186e-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b186e-104">Flowet af aktiviteter i et lean produktionsflow dokumenteres via aktivitetsrelationer.</span><span class="sxs-lookup"><span data-stu-id="b186e-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="b186e-105">Denne optagelse viser, hvordan du opretter en aktivitetsrelation.</span><span class="sxs-lookup"><span data-stu-id="b186e-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="b186e-106">Forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="b186e-106">Prerequisites:</span></span>

- <span data-ttu-id="b186e-107">Et produktionsflow og en version i kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="b186e-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="b186e-108">To aktiviteter, der følger efter hinanden i produktionsflowet, er oprettet, men ikke relateret.</span><span class="sxs-lookup"><span data-stu-id="b186e-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="b186e-109">Find produktionsflowversionen</span><span class="sxs-lookup"><span data-stu-id="b186e-109">Find the production flow version</span></span> 
1. <span data-ttu-id="b186e-110">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="b186e-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b186e-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b186e-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b186e-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b186e-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b186e-113">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b186e-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b186e-114">Vælg en kladdeversion på listen.</span><span class="sxs-lookup"><span data-stu-id="b186e-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="b186e-115">Aktivitetsrelationer kan føjes til både kladdeversioner eller aktive versioner af et produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="b186e-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="b186e-116">Åbn den aktivitetsoversigten</span><span class="sxs-lookup"><span data-stu-id="b186e-116">Open the activity overview</span></span>
1. <span data-ttu-id="b186e-117">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="b186e-117">Click Activities.</span></span>
    * <span data-ttu-id="b186e-118">Bemærk, at formularen viser alle aktiviteter i produktionsflowet, der er allokeret til versionen af de produktionsflow, du arbejder i.</span><span class="sxs-lookup"><span data-stu-id="b186e-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="b186e-119">Tilføj en efterfølgende aktivitet</span><span class="sxs-lookup"><span data-stu-id="b186e-119">Add a Successor</span></span>
1. <span data-ttu-id="b186e-120">Klik på Tilføj efterfølgende aktivitet.</span><span class="sxs-lookup"><span data-stu-id="b186e-120">Click Add successor.</span></span>
2. <span data-ttu-id="b186e-121">Klik på rullelisten i feltet Aktivitet for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b186e-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b186e-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b186e-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b186e-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b186e-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b186e-124">Markér afkrydsningsfeltet Begrænsning.</span><span class="sxs-lookup"><span data-stu-id="b186e-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="b186e-125">Skriv et tal i feltet Begrænsningsværdi.</span><span class="sxs-lookup"><span data-stu-id="b186e-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="b186e-126">Begrænsningstiden er den tid, der skal planlægges mellem den planlagte afslutning af den foregående aktivitet (forfaldsdato og tid) og det planlagte starttidspunkt for den efterfølgende aktivitet.</span><span class="sxs-lookup"><span data-stu-id="b186e-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="b186e-127">Angiv en værdi i feltet Enheder.</span><span class="sxs-lookup"><span data-stu-id="b186e-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="b186e-128">Angiv et tal i feltet Procestidsforhold.</span><span class="sxs-lookup"><span data-stu-id="b186e-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="b186e-129">Hvis begge aktiviteter kører i den samme takt, skal procestidsforholdet være 1.</span><span class="sxs-lookup"><span data-stu-id="b186e-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="b186e-130">Hvis den foregående opgave kører med dobbelt hastighed af den efterfølgende, skal forholdet være 2.</span><span class="sxs-lookup"><span data-stu-id="b186e-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="b186e-131">Procestidsforholdene bruges til at beregne de enkelte procestider for produktionsflowaktiviteterne.</span><span class="sxs-lookup"><span data-stu-id="b186e-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="b186e-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b186e-132">Click OK.</span></span>
10. <span data-ttu-id="b186e-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b186e-133">Close the page.</span></span>
11. <span data-ttu-id="b186e-134">Klik på fanen GridPanel.</span><span class="sxs-lookup"><span data-stu-id="b186e-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="b186e-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b186e-135">Close the page.</span></span>
13. <span data-ttu-id="b186e-136">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="b186e-136">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]