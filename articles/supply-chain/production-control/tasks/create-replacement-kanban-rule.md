---
title: Oprette en kanban-regel til erstatning
description: Denne procedure drejer sig om at erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ded10b0972f07f4f86ee32cee596c5e30b15ebd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843763"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="12424-103">Oprette en kanban-regel til erstatning</span><span class="sxs-lookup"><span data-stu-id="12424-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12424-104">Denne procedure drejer sig om at erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="12424-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="12424-105">Dette er nyttigt, når ændringer af produktionsflow eller genopfyldningregler skal koordineres og planlægges.</span><span class="sxs-lookup"><span data-stu-id="12424-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="12424-106">Det demodatafirma, der bruges til at oprette proceduren, er USMF.</span><span class="sxs-lookup"><span data-stu-id="12424-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="12424-107">Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen til et nyt produktionsflow eller en ny genopfyldningsregel.</span><span class="sxs-lookup"><span data-stu-id="12424-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="12424-108">Denne opgave erstatter kanban-regel 000022 med en ny regel og øger det maksimale antal fra 48 til 100 for den nye regel.</span><span class="sxs-lookup"><span data-stu-id="12424-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="12424-109">Vælg den kanban-regel, der skal erstattes.</span><span class="sxs-lookup"><span data-stu-id="12424-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="12424-110">Gå til kanban-regler.</span><span class="sxs-lookup"><span data-stu-id="12424-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="12424-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="12424-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="12424-112">Vælg kanban-reglen 000022.</span><span class="sxs-lookup"><span data-stu-id="12424-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="12424-113">Oprette en kanban-regel til erstatning</span><span class="sxs-lookup"><span data-stu-id="12424-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="12424-114">Klik på Erstat kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="12424-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="12424-115">Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="12424-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="12424-116">Vælg en dato i fremtiden, f.eks. en uge fra nu.</span><span class="sxs-lookup"><span data-stu-id="12424-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="12424-117">Dette er den dato og det klokkeslæt, hvor den nye kanban-regel bliver aktiv og erstatter den gamle kanban-regel.</span><span class="sxs-lookup"><span data-stu-id="12424-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="12424-118">Hvis kanban-reglen får en anden sti i produktionsflowet, kan du vælge en anden aktivitet.</span><span class="sxs-lookup"><span data-stu-id="12424-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="12424-119">I denne procedure bevarer vi aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="12424-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="12424-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="12424-120">Click OK.</span></span>
    * <span data-ttu-id="12424-121">Bemærk, at der oprettes en ny kanban-regel som erstatning for kanban-regel 000022.</span><span class="sxs-lookup"><span data-stu-id="12424-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="12424-122">Ikrafttrædelsesdatoen angives i overensstemmelse med den valgte dato, når du udskifter kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="12424-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="12424-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="12424-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="12424-124">Vælg den erstattede kanban-regel 000022.</span><span class="sxs-lookup"><span data-stu-id="12424-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="12424-125">Bemærk, at den erstattede kanban-regel har samme dato som udløbsdatoen, fordi det er den dato, hvor den udløber.</span><span class="sxs-lookup"><span data-stu-id="12424-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="12424-126">Markér række 1 på listen.</span><span class="sxs-lookup"><span data-stu-id="12424-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="12424-127">Vælg den nye kanban-regel øverst på listen.</span><span class="sxs-lookup"><span data-stu-id="12424-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="12424-128">Dette er den kanban-regel, der har det højeste nummer.</span><span class="sxs-lookup"><span data-stu-id="12424-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="12424-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12424-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="12424-130">Klik på kanban-regelnummeret for at åbne kanban-reglen.</span><span class="sxs-lookup"><span data-stu-id="12424-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="12424-131">Ændre maksimumantallet for udskiftning af kanban-regel</span><span class="sxs-lookup"><span data-stu-id="12424-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="12424-132">Angiv Maksimumantal til '100'.</span><span class="sxs-lookup"><span data-stu-id="12424-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="12424-133">Udvid oversigtspanelet Antal for at få vist feltet Maksimalt antal.</span><span class="sxs-lookup"><span data-stu-id="12424-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="12424-134">Hvis du ændrer det maksimale antal til 100, bliver det muligt at behandle op til 100 kanbans.</span><span class="sxs-lookup"><span data-stu-id="12424-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="12424-135">Dette er det sidste trin i denne opgave.</span><span class="sxs-lookup"><span data-stu-id="12424-135">This is the last step in this task.</span></span>  

