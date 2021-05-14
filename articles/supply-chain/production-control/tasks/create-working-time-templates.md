---
title: Oprette skabeloner til arbejdstid
description: Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920922"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="c18b1-103">Oprette skabeloner til arbejdstid</span><span class="sxs-lookup"><span data-stu-id="c18b1-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c18b1-104">Arbejdstidsskabeloner definerer arbejdstiderne i hele ugen og bruges til at generere arbejdstider for et bestemt tidsrum.</span><span class="sxs-lookup"><span data-stu-id="c18b1-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="c18b1-105">Denne procedure viser, hvordan du definerer en arbejdstidsskabelon ved hjælp af planlægningsegenskaber for arbejdstider til kategorisering af arbejdstidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="c18b1-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="c18b1-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="c18b1-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="c18b1-107">Gå til **Arbejdsområder > Styring af ressourcelivscyklus**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="c18b1-108">Vælg **Arbejdstidsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="c18b1-109">Oprette arbejdstidsskabelon</span><span class="sxs-lookup"><span data-stu-id="c18b1-109">Create working time template</span></span>

1. <span data-ttu-id="c18b1-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-110">Select **New**.</span></span>
1. <span data-ttu-id="c18b1-111">Indtast en værdi i feltet **Arbejdstidsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="c18b1-112">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="c18b1-113">Udvid sektionen **Mandag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="c18b1-114">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-114">Select **Add**.</span></span>
1. <span data-ttu-id="c18b1-115">Angiv et klokkeslæt i feltet **Fra**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="c18b1-116">Angiv det tidspunkt, hvor arbejdet begynder om morgenen.</span><span class="sxs-lookup"><span data-stu-id="c18b1-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="c18b1-117">Angiv et klokkeslæt i feltet **Til**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="c18b1-118">Angiv det tidspunkt, hvor arbejdere har frokostpause.</span><span class="sxs-lookup"><span data-stu-id="c18b1-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="c18b1-119">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-119">Select **Add**.</span></span>
1. <span data-ttu-id="c18b1-120">Angiv et klokkeslæt i feltet **Fra**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="c18b1-121">Angiv det tidspunkt, hvor arbejdet genoptages efter frokost.</span><span class="sxs-lookup"><span data-stu-id="c18b1-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="c18b1-122">Angiv et klokkeslæt i feltet **Til**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="c18b1-123">Angiv, hvornår arbejdsdagen er slut.</span><span class="sxs-lookup"><span data-stu-id="c18b1-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="c18b1-124">Replikere arbejdstider til alle ugedage</span><span class="sxs-lookup"><span data-stu-id="c18b1-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="c18b1-125">Vælg **Kopiér dag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="c18b1-126">Kopier arbejdstidsdefinitionerne fra mandag til tirsdag.</span><span class="sxs-lookup"><span data-stu-id="c18b1-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="c18b1-127">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-127">Select **OK**.</span></span>
1. <span data-ttu-id="c18b1-128">Vælg **Kopiér dag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="c18b1-129">Kopier arbejdstidsdefinitionerne fra mandag til onsdag.</span><span class="sxs-lookup"><span data-stu-id="c18b1-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="c18b1-130">Vælg en indstilling i feltet **Til ugedag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="c18b1-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-131">Select **OK**.</span></span>
1. <span data-ttu-id="c18b1-132">Vælg **Kopiér dag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="c18b1-133">Kopier arbejdstidsdefinitionerne fra mandag til torsdag.</span><span class="sxs-lookup"><span data-stu-id="c18b1-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="c18b1-134">Vælg en indstilling i feltet **Til ugedag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="c18b1-135">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-135">Select **OK**.</span></span>
1. <span data-ttu-id="c18b1-136">Vælg **Kopiér dag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="c18b1-137">Kopier arbejdstidsdefinitionerne fra mandag til fredag.</span><span class="sxs-lookup"><span data-stu-id="c18b1-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="c18b1-138">Vælg en indstilling i feltet **Til ugedag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="c18b1-139">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="c18b1-140">Definere tidsrubrikker for særlige operationer</span><span class="sxs-lookup"><span data-stu-id="c18b1-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="c18b1-141">Udvid sektionen **Fredag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="c18b1-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c18b1-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="c18b1-143">Indtast eller vælg en værdi i feltet **Egenskab**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="c18b1-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c18b1-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="c18b1-145">Indtast eller vælg en værdi i feltet **Egenskab**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="c18b1-146">Markér dage i weekend som lukket for afhentning</span><span class="sxs-lookup"><span data-stu-id="c18b1-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="c18b1-147">Udvid sektionen **Lørdag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="c18b1-148">Vælg *Ja* i feltet **Lukket for afhentning**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="c18b1-149">Udvid sektionen **Søndag**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="c18b1-150">Vælg *Ja* i feltet **Lukket for afhentning**.</span><span class="sxs-lookup"><span data-stu-id="c18b1-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]