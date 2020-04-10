---
title: Planlægge en produktionsordre med grov- og finplanlægning
description: Dette emne drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2181a84aea08aac0ddb202f7211dbda6330a3d49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148831"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="aa2ca-103">Planlægge en produktionsordre med grov- og finplanlægning</span><span class="sxs-lookup"><span data-stu-id="aa2ca-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa2ca-104">Dette emne drejer sig om planlægning af en produktionsordre med grovplanlægning og finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="aa2ca-105">Der oprettes ingen job med grovplanlægning, kun job med finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="aa2ca-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="aa2ca-107">Denne procedure er beregnet til produktionslederen, produktionsplanlæggeren eller den produktionstilsynsførende, der arbejder i et dedikeret produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="aa2ca-108">Oprette en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="aa2ca-108">Create a production order</span></span>
1. <span data-ttu-id="aa2ca-109">Gå i navigationsruden til **Moduler > Produktionsstyring > Produktionsordrer > Alle produktionsordrer**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="aa2ca-110">Vælg **Ny produktionsordre**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-110">Select **New production order**.</span></span>
3. <span data-ttu-id="aa2ca-111">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="aa2ca-112">Vælg varenummer **D0001**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="aa2ca-113">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="aa2ca-114">Grovplanlægge for en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="aa2ca-115">Marker den række, der netop er oprettet.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="aa2ca-116">Vælg **Planlæg** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="aa2ca-117">Vælg **Grovplanlægge**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="aa2ca-118">Vælg **Fremad fra planlægningsdato** i feltet **Planlægningsvej**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="aa2ca-119">Angiv en dato i feltet **Planlægningsdato**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="aa2ca-120">Vælg en dato i fremtiden, for eksempel i dag plus en uge.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="aa2ca-121">Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="aa2ca-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-122">Select **OK**.</span></span>
7. <span data-ttu-id="aa2ca-123">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-123">In the list, mark the selected row.</span></span> <span data-ttu-id="aa2ca-124">Bemærk, at status ændres til **Planlagt**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="aa2ca-125">Vælg **Alle job**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-125">Select **All jobs**.</span></span> <span data-ttu-id="aa2ca-126">Bemærk, at der ikke oprettes nogen job til grovplanlægning.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="aa2ca-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="aa2ca-128">Finplanlægge for en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="aa2ca-129">Vælg **Planlæg** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="aa2ca-130">Vælg **Finplanlægge**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="aa2ca-131">Vælg **Fremad fra planlægningsdato** i feltet **Planlægningsvej**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="aa2ca-132">Angiv en dato i feltet **Planlægningsdato**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="aa2ca-133">Vælg en dato i fremtiden, for eksempel i dag plus en uge.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="aa2ca-134">Med den valgte planlægningsvej planlægges produktionsordren fremad fra denne dato.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="aa2ca-135">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-135">Select **OK**.</span></span>
6. <span data-ttu-id="aa2ca-136">Vælg **Produktionsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="aa2ca-137">Vælg **Alle job**.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-137">Select **All jobs**.</span></span> <span data-ttu-id="aa2ca-138">Bemærk, at der baseret på den aktive rute oprettes fem jo med finplanlægning.</span><span class="sxs-lookup"><span data-stu-id="aa2ca-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

