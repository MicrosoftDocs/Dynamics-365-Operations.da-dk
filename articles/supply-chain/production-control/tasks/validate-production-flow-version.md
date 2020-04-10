---
title: Validere et produktionsflow og en version
description: Denne procedure viser, hvordan du opretter et nyt produktionsflow og en første version af lean manufacturing.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dfd5655ecdfa74d75490b0915c4cea609baebe3
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146491"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="0798d-103">Validere et produktionsflow og en version</span><span class="sxs-lookup"><span data-stu-id="0798d-103">Validate a production flow and version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0798d-104">Denne procedure viser, hvordan du opretter et nyt produktionsflow og en første version af lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="0798d-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="0798d-105">Forudsætninger: Produktionsparametre for lean manufacturing og måleenheder for klassen Tid skal defineres.</span><span class="sxs-lookup"><span data-stu-id="0798d-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="0798d-106">Du skal definere en værdistrøm og en produktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0798d-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="0798d-107">Se hvidbøgerne om Lean manufacturing for at blive fortrolig med begreberne produktionsflow og -aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="0798d-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="0798d-108">Denne procedure refererer til den juridiske enhed USMF i demodata.</span><span class="sxs-lookup"><span data-stu-id="0798d-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="0798d-109">Forudsat at den juridiske enhed er konfigureret for Lean manufacturing, kan andre juridiske enheder imidlertid også bruges.</span><span class="sxs-lookup"><span data-stu-id="0798d-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="0798d-110">Oprette et produktionsflow</span><span class="sxs-lookup"><span data-stu-id="0798d-110">Create a production flow</span></span>
1. <span data-ttu-id="0798d-111">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="0798d-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="0798d-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0798d-112">Click New.</span></span>
3. <span data-ttu-id="0798d-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0798d-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0798d-114">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0798d-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0798d-115">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0798d-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0798d-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0798d-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0798d-117">En værdistrøm er en driftsenhed, der spænder over alle værdistrømmens aktiviteter og flow.</span><span class="sxs-lookup"><span data-stu-id="0798d-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="0798d-118">På dette stadium er driftsenheder begrænset til en juridisk enhed og har ikke yderligere funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="0798d-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="0798d-119">Klik på rullelisten i feltet Produktionsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0798d-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0798d-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0798d-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0798d-121">Produktionsgrupper giver mulighed for definition af materiale, arbejdskraft og IGVF-konti for en produktionsproces.</span><span class="sxs-lookup"><span data-stu-id="0798d-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="0798d-122">For at knytte regnskabskonteksten til et produktionsflow skal der vælges en produktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0798d-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="0798d-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0798d-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="0798d-124">Oprette en produktionsflowversion</span><span class="sxs-lookup"><span data-stu-id="0798d-124">Create a production flow version</span></span>
1. <span data-ttu-id="0798d-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0798d-125">Click Add.</span></span>
2. <span data-ttu-id="0798d-126">Angiv dato og klokkeslæt i feltet Udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="0798d-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="0798d-127">Du kan opdatere udløbsdatoen for versionen til enhver tid, selv for aktive versioner.</span><span class="sxs-lookup"><span data-stu-id="0798d-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="0798d-128">Brug udløbet af versionen til at planlægge en udfasning af en version.</span><span class="sxs-lookup"><span data-stu-id="0798d-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="0798d-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0798d-129">Click OK.</span></span>
4. <span data-ttu-id="0798d-130">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0798d-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="0798d-131">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="0798d-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="0798d-132">Vælg Taktenhed.</span><span class="sxs-lookup"><span data-stu-id="0798d-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="0798d-133">Angiv et tal i feltet Gennemsnitlig takttid.</span><span class="sxs-lookup"><span data-stu-id="0798d-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="0798d-134">Definer en gennemsnitlig takttid for taktstyring af produktionsflowversionen.</span><span class="sxs-lookup"><span data-stu-id="0798d-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="0798d-135">Takten defineres som antal pr. periode.</span><span class="sxs-lookup"><span data-stu-id="0798d-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="0798d-136">I det givne eksempel er takttiden 0,2 timer pr. 10 styk.</span><span class="sxs-lookup"><span data-stu-id="0798d-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="0798d-137">Dette svarer til en daglig gennemløbskapacitet på 400 styk for en arbejdstid på 8 timer.</span><span class="sxs-lookup"><span data-stu-id="0798d-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="0798d-138">Skriv et tal i feltet Antal pr. cyklus.</span><span class="sxs-lookup"><span data-stu-id="0798d-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="0798d-139">Udvid eller skjul afsnittet Versionsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="0798d-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="0798d-140">Angiv et tal i feltet Mimimumtakttid.</span><span class="sxs-lookup"><span data-stu-id="0798d-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="0798d-141">Minimumtakttiden skal være mindre end eller lig med den gennemsnitlige takttid.</span><span class="sxs-lookup"><span data-stu-id="0798d-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="0798d-142">Angiv et tal i feltet Maksimumtakttid.</span><span class="sxs-lookup"><span data-stu-id="0798d-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="0798d-143">Maksimumtakttiden skal være større end eller lig med den gennemsnitlige takttid.</span><span class="sxs-lookup"><span data-stu-id="0798d-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="0798d-144">Angiv et antal dage i Periode for faktisk procestid</span><span class="sxs-lookup"><span data-stu-id="0798d-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="0798d-145">Periode for faktisk procestid er det antal dage, hvor jobs aggregeres, fra det faktiske minut bagud for at beregne den faktiske procestid.</span><span class="sxs-lookup"><span data-stu-id="0798d-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="0798d-146">Værdien kan ændres når som helst og bruges kun til beregning af de faktiske procestider.</span><span class="sxs-lookup"><span data-stu-id="0798d-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="0798d-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0798d-147">Click Save.</span></span>

