--- 
title: Konfigurere manuel emballering (kun februar og maj 2016)
description: "Pakningsprocessen gør det muligt at validere og pakke af produkter i containere."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 31b689b6c31563f24892525eed5911af3a35bd51
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="21e68-103">Konfigurere manuel emballering (kun februar og maj 2016)</span><span class="sxs-lookup"><span data-stu-id="21e68-103">Set up manual packing (February & May 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21e68-104">Pakningsprocessen gør det muligt at validere og pakke af produkter i containere.</span><span class="sxs-lookup"><span data-stu-id="21e68-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="21e68-105">I denne proces plukker lagermedarbejdere produkter fra lagerplaceringerne og flytter dem til en pakkestation, hvor de kan kontrollere vareantal og -typer og tildele dem til passende containere.</span><span class="sxs-lookup"><span data-stu-id="21e68-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="21e68-106">Når en container er helt pakket, kan de lukke den og flytte den til forsendelsesområderne, og produkterne er klar til afsendelse.</span><span class="sxs-lookup"><span data-stu-id="21e68-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="21e68-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="21e68-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="21e68-108">Konfigurer lokationsprofiler</span><span class="sxs-lookup"><span data-stu-id="21e68-108">Set up location profiles</span></span>
1. <span data-ttu-id="21e68-109">Gå til Lagerstedsstyring > Konfiguration > Lagersted > Lokationsprofiler.</span><span class="sxs-lookup"><span data-stu-id="21e68-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="21e68-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="21e68-110">Click New.</span></span>
    * <span data-ttu-id="21e68-111">Lokationsprofilen bruges til pakkestationer og indeholder oplysninger om og regler for en lokation.</span><span class="sxs-lookup"><span data-stu-id="21e68-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="21e68-112">Skriv en værdi i feltet Id for lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="21e68-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="21e68-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="21e68-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="21e68-114">Indtast eller vælg en værdi i feltet Lokationsformat.</span><span class="sxs-lookup"><span data-stu-id="21e68-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="21e68-115">Indtast eller vælg en værdi i feltet Lokationstype.</span><span class="sxs-lookup"><span data-stu-id="21e68-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="21e68-116">Vælg Ja i feltet Tillad blandede varer.</span><span class="sxs-lookup"><span data-stu-id="21e68-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="21e68-117">Vælg Ja i feltet Tillad blandede lagerstatusser.</span><span class="sxs-lookup"><span data-stu-id="21e68-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="21e68-118">Vælg Ja i feltet Tilsidesæt regler for batchdage.</span><span class="sxs-lookup"><span data-stu-id="21e68-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="21e68-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21e68-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="21e68-120">Konfigurere lagerstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="21e68-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="21e68-121">Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="21e68-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="21e68-122">Klik på fanen Emballage.</span><span class="sxs-lookup"><span data-stu-id="21e68-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="21e68-123">Indtast eller vælg en værdi i feltet Profil-id for pakkelokation.</span><span class="sxs-lookup"><span data-stu-id="21e68-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="21e68-124">Vælg den lokationsprofil, du vil bruge til pakning.</span><span class="sxs-lookup"><span data-stu-id="21e68-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="21e68-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21e68-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="21e68-126">Konfigurere containertyper</span><span class="sxs-lookup"><span data-stu-id="21e68-126">Set up container types</span></span>
1. <span data-ttu-id="21e68-127">Gå til Lagerstedsstyring > Konfiguration > Containere > Containertyper.</span><span class="sxs-lookup"><span data-stu-id="21e68-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="21e68-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="21e68-128">Click New.</span></span>
    * <span data-ttu-id="21e68-129">Du kan definere de containertyper, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="21e68-129">You can define the types of containers to use.</span></span> <span data-ttu-id="21e68-130">Du kan angive containerens fysiske dimensioner, herunder taravægt, maksimal vægt, maksimal volumen, længde, bredde og vægt.</span><span class="sxs-lookup"><span data-stu-id="21e68-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="21e68-131">Attributterne er brugerdefinerede felter, der gør det muligt at tilføje ekstra dimensioner til containertypen.</span><span class="sxs-lookup"><span data-stu-id="21e68-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="21e68-132">Indtast en værdi i feltet Containertypekode.</span><span class="sxs-lookup"><span data-stu-id="21e68-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="21e68-133">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="21e68-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="21e68-134">Angiv et tal i feltet Taravægt.</span><span class="sxs-lookup"><span data-stu-id="21e68-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="21e68-135">Angiv et tal i feltet Maksimal vægt.</span><span class="sxs-lookup"><span data-stu-id="21e68-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="21e68-136">Angiv et tal i feltet Volumen.</span><span class="sxs-lookup"><span data-stu-id="21e68-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="21e68-137">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="21e68-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="21e68-138">Indtast et tal i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="21e68-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="21e68-139">Indtast et tal i feltet Højde.</span><span class="sxs-lookup"><span data-stu-id="21e68-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="21e68-140">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="21e68-140">Click Save.</span></span>
12. <span data-ttu-id="21e68-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21e68-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="21e68-142">Konfigurere pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="21e68-142">Set up packing profiles</span></span>
1. <span data-ttu-id="21e68-143">Gå til Lagerstedsstyring > Konfiguration > Emballage > Pakkeprofiler.</span><span class="sxs-lookup"><span data-stu-id="21e68-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="21e68-144">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="21e68-144">Click New.</span></span>
3. <span data-ttu-id="21e68-145">Skriv en værdi i feltet Pakkeprofil-id.</span><span class="sxs-lookup"><span data-stu-id="21e68-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="21e68-146">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="21e68-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="21e68-147">Indtast eller vælg en værdi i feltet Profil-id for lukning af container.</span><span class="sxs-lookup"><span data-stu-id="21e68-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="21e68-148">Det er valgfrit at angive et profil-id for containerlukning, og det er standardprofilen for containerlukning for denne pakkeprofil.</span><span class="sxs-lookup"><span data-stu-id="21e68-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="21e68-149">Vælg en indstilling i feltet Tilstanden Container-id.</span><span class="sxs-lookup"><span data-stu-id="21e68-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="21e68-150">Denne indstilling bestemmer, om der automatisk genereres et container-id, når der oprettes en container, eller der oprettes et container-id manuelt.</span><span class="sxs-lookup"><span data-stu-id="21e68-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="21e68-151">Indtast eller vælg en værdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="21e68-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="21e68-152">Containertypen vil blive brugt som standard, når der oprettes en ny container.</span><span class="sxs-lookup"><span data-stu-id="21e68-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="21e68-153">Markér afkrydsningsfeltet Opret automatisk container ved containerlukning.</span><span class="sxs-lookup"><span data-stu-id="21e68-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="21e68-154">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="21e68-154">Click Save.</span></span>
10. <span data-ttu-id="21e68-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21e68-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="21e68-156">Konfigurere profiler for containerlukning</span><span class="sxs-lookup"><span data-stu-id="21e68-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="21e68-157">Gå til Lagerstedsstyring > Konfiguration > Containere > Profiler for lukning af container.</span><span class="sxs-lookup"><span data-stu-id="21e68-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="21e68-158">Containerlukningsprofiler definerer, hvad der sker, når en container er lukket.</span><span class="sxs-lookup"><span data-stu-id="21e68-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="21e68-159">Du kan oprette flere containerlukningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="21e68-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="21e68-160">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="21e68-160">Click New.</span></span>
3. <span data-ttu-id="21e68-161">Skriv en værdi i feltet Profil-id for lukning af container.</span><span class="sxs-lookup"><span data-stu-id="21e68-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="21e68-162">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="21e68-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="21e68-163">Vælg en indstilling i feltet Manifest kl.</span><span class="sxs-lookup"><span data-stu-id="21e68-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="21e68-164">Angiv, om der bruget et manifest ved lukning af containere eller bekræftelse af leverancen.</span><span class="sxs-lookup"><span data-stu-id="21e68-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="21e68-165">Bemærk, at brug af et manifest kræver transportstyring.</span><span class="sxs-lookup"><span data-stu-id="21e68-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="21e68-166">Der skal implementeres et manifest i transportprogrammer, for at det kan fungere.</span><span class="sxs-lookup"><span data-stu-id="21e68-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="21e68-167">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="21e68-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="21e68-168">Indtast eller vælg en værdi i feltet Standardlokation til endelig forsendelse.</span><span class="sxs-lookup"><span data-stu-id="21e68-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="21e68-169">Dette er den lokation, som produkter skal flyttes til, når containerne er lukkede.</span><span class="sxs-lookup"><span data-stu-id="21e68-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="21e68-170">Denne lokation skal have en lokationsprofil, der er defineret i Lagerstedsparametre.</span><span class="sxs-lookup"><span data-stu-id="21e68-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="21e68-171">Indtast eller vælg en værdi i feltet Vægtenhed.</span><span class="sxs-lookup"><span data-stu-id="21e68-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="21e68-172">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="21e68-172">Click Save.</span></span>


