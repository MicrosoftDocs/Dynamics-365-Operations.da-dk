---
title: Oprette skabeloner til arbejdstid
description: Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e8e43900fd25f0051124d761dc7b06d4f9313a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006810"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="7d416-103">Oprette skabeloner til arbejdstid</span><span class="sxs-lookup"><span data-stu-id="7d416-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d416-104">Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.</span><span class="sxs-lookup"><span data-stu-id="7d416-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="7d416-105">Denne procedure viser, hvordan du definerer en arbejdstidsskabelon ved hjælp af planlægningsegenskaber for arbejdstider til kategorisering af arbejdstidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="7d416-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="7d416-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="7d416-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="7d416-107">Gå til alle arbejdsområder > Styring af ressourcelivscyklus.</span><span class="sxs-lookup"><span data-stu-id="7d416-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="7d416-108">Klik på Arbejdstidsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="7d416-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="7d416-109">Oprette arbejdstidsskabelon</span><span class="sxs-lookup"><span data-stu-id="7d416-109">Create working time template</span></span>
1. <span data-ttu-id="7d416-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7d416-110">Click New.</span></span>
2. <span data-ttu-id="7d416-111">Indtast en værdi i feltet Arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="7d416-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="7d416-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7d416-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7d416-113">Udvid afsnittet Mandag.</span><span class="sxs-lookup"><span data-stu-id="7d416-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="7d416-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7d416-114">Click Add.</span></span>
6. <span data-ttu-id="7d416-115">Angiv et klokkeslæt i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="7d416-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="7d416-116">Angiv det tidspunkt, hvor arbejdet begynder om morgenen.</span><span class="sxs-lookup"><span data-stu-id="7d416-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="7d416-117">Angiv et klokkeslæt i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="7d416-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="7d416-118">Angiv det tidspunkt, hvor arbejdere har frokostpause.</span><span class="sxs-lookup"><span data-stu-id="7d416-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="7d416-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7d416-119">Click Add.</span></span>
9. <span data-ttu-id="7d416-120">Angiv et klokkeslæt i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="7d416-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="7d416-121">Angiv det tidspunkt, hvor arbejdet genoptages efter frokost.</span><span class="sxs-lookup"><span data-stu-id="7d416-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="7d416-122">Angiv et klokkeslæt i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="7d416-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="7d416-123">Angiv, hvornår arbejdsdagen er slut.</span><span class="sxs-lookup"><span data-stu-id="7d416-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="7d416-124">Replikere arbejdstider til alle ugedage</span><span class="sxs-lookup"><span data-stu-id="7d416-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="7d416-125">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="7d416-125">Click Copy day.</span></span>
    * <span data-ttu-id="7d416-126">Kopier arbejdstidsdefinitionerne fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="7d416-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="7d416-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7d416-127">Click OK.</span></span>
3. <span data-ttu-id="7d416-128">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="7d416-128">Click Copy day.</span></span>
    * <span data-ttu-id="7d416-129">Kopier arbejdstidsdefinitionerne fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="7d416-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="7d416-130">Vælg en indstilling i feltet Til ugedag.</span><span class="sxs-lookup"><span data-stu-id="7d416-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="7d416-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7d416-131">Click OK.</span></span>
6. <span data-ttu-id="7d416-132">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="7d416-132">Click Copy day.</span></span>
    * <span data-ttu-id="7d416-133">Kopier arbejdstidsdefinitionerne fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="7d416-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="7d416-134">Vælg en indstilling i feltet Til ugedag.</span><span class="sxs-lookup"><span data-stu-id="7d416-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="7d416-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7d416-135">Click OK.</span></span>
9. <span data-ttu-id="7d416-136">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="7d416-136">Click Copy day.</span></span>
    * <span data-ttu-id="7d416-137">Kopier arbejdstidsdefinitionerne fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="7d416-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="7d416-138">Vælg en indstilling i feltet Til ugedag.</span><span class="sxs-lookup"><span data-stu-id="7d416-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="7d416-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7d416-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="7d416-140">Definere tidsrubrikker for særlige operationer</span><span class="sxs-lookup"><span data-stu-id="7d416-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="7d416-141">Udvid afsnittet Fredag.</span><span class="sxs-lookup"><span data-stu-id="7d416-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="7d416-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7d416-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7d416-143">Indtast eller vælg en værdi i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="7d416-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="7d416-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7d416-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7d416-145">Indtast eller vælg en værdi i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="7d416-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="7d416-146">Markér dage i weekend som lukket for afhentning</span><span class="sxs-lookup"><span data-stu-id="7d416-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="7d416-147">Udvid afsnittet Lørdag.</span><span class="sxs-lookup"><span data-stu-id="7d416-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="7d416-148">Vælg Ja i feltet Lukket for afhentning.</span><span class="sxs-lookup"><span data-stu-id="7d416-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="7d416-149">Udvid afsnittet Søndag.</span><span class="sxs-lookup"><span data-stu-id="7d416-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="7d416-150">Vælg Ja i feltet Lukket for afhentning.</span><span class="sxs-lookup"><span data-stu-id="7d416-150">Select Yes in the Closed for pickup field.</span></span>

