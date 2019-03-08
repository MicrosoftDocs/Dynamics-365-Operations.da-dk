---
title: Ændre kanban-regler for et procesjob
description: Denne procedure drejer sig om ændring af den brugte kanban-regel for en bestemt kanban.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "314940"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="785b7-103">Ændre kanban-regler for et procesjob</span><span class="sxs-lookup"><span data-stu-id="785b7-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="785b7-104">Denne procedure drejer sig om ændring af den brugte kanban-regel for en bestemt kanban.</span><span class="sxs-lookup"><span data-stu-id="785b7-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="785b7-105">Dette er nyttigt til belastningsudjævning af ressourcer eller i tilfælde af nedbrud.</span><span class="sxs-lookup"><span data-stu-id="785b7-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="785b7-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="785b7-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="785b7-107">Denne procedure er beregnet til planlæggeren, der arbejder på en lean manufacturing-virksomhed og er ansvarlig for værdistrømmen.</span><span class="sxs-lookup"><span data-stu-id="785b7-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="785b7-108">Kopiere kanban-regel</span><span class="sxs-lookup"><span data-stu-id="785b7-108">Copy kanban rule</span></span>
1. <span data-ttu-id="785b7-109">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="785b7-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="785b7-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="785b7-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="785b7-111">Vælg hændelses-kanban-regel 000022 for L0001.</span><span class="sxs-lookup"><span data-stu-id="785b7-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="785b7-112">Klik på Dupliker kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="785b7-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="785b7-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="785b7-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="785b7-114">Redigere kanban-regel</span><span class="sxs-lookup"><span data-stu-id="785b7-114">Change kanban rule</span></span>
1. <span data-ttu-id="785b7-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="785b7-115">Close the page.</span></span>
2. <span data-ttu-id="785b7-116">Gå til Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="785b7-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="785b7-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="785b7-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="785b7-118">Vælg linjen med Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="785b7-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="785b7-119">Klik på Brug en anden kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="785b7-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="785b7-120">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="785b7-120">Click Next.</span></span>
6. <span data-ttu-id="785b7-121">Indtast eller vælg en værdi i feltet Kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="785b7-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="785b7-122">Vælg den kanban-regel, der blev oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="785b7-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="785b7-123">Dette er kanban-reglen med det højeste nummer.</span><span class="sxs-lookup"><span data-stu-id="785b7-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="785b7-124">Klik på Finish.</span><span class="sxs-lookup"><span data-stu-id="785b7-124">Click Finish.</span></span>
    * <span data-ttu-id="785b7-125">Kanban-jobbet bruger nu en anden kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="785b7-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="785b7-126">Dette kan være nyttigt ved belastningsudjævning af arbejdsceller.</span><span class="sxs-lookup"><span data-stu-id="785b7-126">This can be useful to level load work cells.</span></span>  

