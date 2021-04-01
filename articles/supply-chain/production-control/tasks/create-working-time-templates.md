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
ms.openlocfilehash: 9829e91500abf8cba3f7cbfe2f89863cb2b1f4c4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257357"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="d26fd-103">Oprette skabeloner til arbejdstid</span><span class="sxs-lookup"><span data-stu-id="d26fd-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d26fd-104">Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.</span><span class="sxs-lookup"><span data-stu-id="d26fd-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="d26fd-105">Denne procedure viser, hvordan du definerer en arbejdstidsskabelon ved hjælp af planlægningsegenskaber for arbejdstider til kategorisering af arbejdstidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="d26fd-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="d26fd-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d26fd-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d26fd-107">Gå til alle arbejdsområder > Styring af ressourcelivscyklus.</span><span class="sxs-lookup"><span data-stu-id="d26fd-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="d26fd-108">Klik på Arbejdstidsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="d26fd-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="d26fd-109">Oprette arbejdstidsskabelon</span><span class="sxs-lookup"><span data-stu-id="d26fd-109">Create working time template</span></span>
1. <span data-ttu-id="d26fd-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d26fd-110">Click New.</span></span>
2. <span data-ttu-id="d26fd-111">Indtast en værdi i feltet Arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="d26fd-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="d26fd-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d26fd-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d26fd-113">Udvid afsnittet Mandag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="d26fd-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d26fd-114">Click Add.</span></span>
6. <span data-ttu-id="d26fd-115">Angiv et klokkeslæt i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="d26fd-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="d26fd-116">Angiv det tidspunkt, hvor arbejdet begynder om morgenen.</span><span class="sxs-lookup"><span data-stu-id="d26fd-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="d26fd-117">Angiv et klokkeslæt i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="d26fd-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="d26fd-118">Angiv det tidspunkt, hvor arbejdere har frokostpause.</span><span class="sxs-lookup"><span data-stu-id="d26fd-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="d26fd-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d26fd-119">Click Add.</span></span>
9. <span data-ttu-id="d26fd-120">Angiv et klokkeslæt i feltet Fra.</span><span class="sxs-lookup"><span data-stu-id="d26fd-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="d26fd-121">Angiv det tidspunkt, hvor arbejdet genoptages efter frokost.</span><span class="sxs-lookup"><span data-stu-id="d26fd-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="d26fd-122">Angiv et klokkeslæt i feltet Til.</span><span class="sxs-lookup"><span data-stu-id="d26fd-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="d26fd-123">Angiv, hvornår arbejdsdagen er slut.</span><span class="sxs-lookup"><span data-stu-id="d26fd-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="d26fd-124">Replikere arbejdstider til alle ugedage</span><span class="sxs-lookup"><span data-stu-id="d26fd-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="d26fd-125">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-125">Click Copy day.</span></span>
    * <span data-ttu-id="d26fd-126">Kopier arbejdstidsdefinitionerne fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="d26fd-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d26fd-127">Click OK.</span></span>
3. <span data-ttu-id="d26fd-128">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-128">Click Copy day.</span></span>
    * <span data-ttu-id="d26fd-129">Kopier arbejdstidsdefinitionerne fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="d26fd-130">Vælg en indstilling i feltet Til ugedag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="d26fd-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d26fd-131">Click OK.</span></span>
6. <span data-ttu-id="d26fd-132">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-132">Click Copy day.</span></span>
    * <span data-ttu-id="d26fd-133">Kopier arbejdstidsdefinitionerne fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="d26fd-134">Vælg en indstilling i feltet Til ugedag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="d26fd-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d26fd-135">Click OK.</span></span>
9. <span data-ttu-id="d26fd-136">Klik på Kopier dag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-136">Click Copy day.</span></span>
    * <span data-ttu-id="d26fd-137">Kopier arbejdstidsdefinitionerne fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="d26fd-138">Vælg en indstilling i feltet Til ugedag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="d26fd-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d26fd-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="d26fd-140">Definere tidsrubrikker for særlige operationer</span><span class="sxs-lookup"><span data-stu-id="d26fd-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="d26fd-141">Udvid afsnittet Fredag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="d26fd-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d26fd-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d26fd-143">Indtast eller vælg en værdi i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="d26fd-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="d26fd-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d26fd-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d26fd-145">Indtast eller vælg en værdi i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="d26fd-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="d26fd-146">Markér dage i weekend som lukket for afhentning</span><span class="sxs-lookup"><span data-stu-id="d26fd-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="d26fd-147">Udvid afsnittet Lørdag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="d26fd-148">Vælg Ja i feltet Lukket for afhentning.</span><span class="sxs-lookup"><span data-stu-id="d26fd-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="d26fd-149">Udvid afsnittet Søndag.</span><span class="sxs-lookup"><span data-stu-id="d26fd-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="d26fd-150">Vælg Ja i feltet Lukket for afhentning.</span><span class="sxs-lookup"><span data-stu-id="d26fd-150">Select Yes in the Closed for pickup field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]