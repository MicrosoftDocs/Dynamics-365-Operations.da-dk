---
title: Konfigurer manuel pakning (februar 2016 og maj 2016)
description: Pakningsprocessen gør det muligt at validere og pakke af produkter i containere.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2843c42474fcd4afbbc2cd7753c0d06cfe467dbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810360"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="f7d0c-103">Konfigurer manuel pakning (februar 2016 og maj 2016)</span><span class="sxs-lookup"><span data-stu-id="f7d0c-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7d0c-104">Pakningsprocessen gør det muligt at validere og pakke af produkter i containere.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="f7d0c-105">I denne proces plukker lagermedarbejdere produkter fra lagerplaceringerne og flytter dem til en pakkestation, hvor de kan kontrollere vareantal og -typer og tildele dem til passende containere.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="f7d0c-106">Når en container er helt pakket, kan de lukke den og flytte den til forsendelsesområderne, og produkterne er klar til afsendelse.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="f7d0c-107">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f7d0c-108">Denne procedure gælder kun for februar 2016- og maj 2016-versionerne af Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="f7d0c-109">Konfigurer lokationsprofiler</span><span class="sxs-lookup"><span data-stu-id="f7d0c-109">Set up location profiles</span></span>
1. <span data-ttu-id="f7d0c-110">Gå til Lagerstedsstyring > Konfiguration > Lagersted > Lokationsprofiler.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="f7d0c-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-111">Click New.</span></span>
    * <span data-ttu-id="f7d0c-112">Lokationsprofilen bruges til pakkestationer og indeholder oplysninger om og regler for en lokation.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="f7d0c-113">Skriv en værdi i feltet Id for lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="f7d0c-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f7d0c-115">Indtast eller vælg en værdi i feltet Lokationsformat.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="f7d0c-116">Indtast eller vælg en værdi i feltet Lokationstype.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="f7d0c-117">Vælg Ja i feltet Tillad blandede varer.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="f7d0c-118">Vælg Ja i feltet Tillad blandede lagerstatusser.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="f7d0c-119">Vælg Ja i feltet Tilsidesæt regler for batchdage.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="f7d0c-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="f7d0c-121">Konfigurere lagerstyringsparametre</span><span class="sxs-lookup"><span data-stu-id="f7d0c-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="f7d0c-122">Gå til Lagerstedsstyring > Opsætning > Parametre til lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="f7d0c-123">Klik på fanen Emballage.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="f7d0c-124">Indtast eller vælg en værdi i feltet Profil-id for pakkelokation.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d0c-125">Vælg den lokationsprofil, du vil bruge til pakning.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="f7d0c-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="f7d0c-127">Konfigurere containertyper</span><span class="sxs-lookup"><span data-stu-id="f7d0c-127">Set up container types</span></span>
1. <span data-ttu-id="f7d0c-128">Gå til Lagerstedsstyring > Konfiguration > Containere > Containertyper.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="f7d0c-129">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-129">Click New.</span></span>
    * <span data-ttu-id="f7d0c-130">Du kan definere de containertyper, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-130">You can define the types of containers to use.</span></span> <span data-ttu-id="f7d0c-131">Du kan angive containerens fysiske dimensioner, herunder taravægt, maksimal vægt, maksimal volumen, længde, bredde og vægt.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="f7d0c-132">Attributterne er brugerdefinerede felter, der gør det muligt at tilføje ekstra dimensioner til containertypen.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="f7d0c-133">Indtast en værdi i feltet Containertypekode.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="f7d0c-134">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d0c-135">Angiv et tal i feltet Taravægt.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="f7d0c-136">Angiv et tal i feltet Maksimal vægt.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="f7d0c-137">Angiv et tal i feltet Volumen.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="f7d0c-138">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="f7d0c-139">Indtast et tal i feltet Bredde.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="f7d0c-140">Indtast et tal i feltet Højde.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="f7d0c-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-141">Click Save.</span></span>
12. <span data-ttu-id="f7d0c-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="f7d0c-143">Konfigurere pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="f7d0c-143">Set up packing profiles</span></span>
1. <span data-ttu-id="f7d0c-144">Gå til Lagerstedsstyring > Konfiguration > Emballage > Pakkeprofiler.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="f7d0c-145">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-145">Click New.</span></span>
3. <span data-ttu-id="f7d0c-146">Skriv en værdi i feltet Pakkeprofil-id.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="f7d0c-147">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d0c-148">Indtast eller vælg en værdi i feltet Profil-id for lukning af container.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d0c-149">Det er valgfrit at angive et profil-id for containerlukning, og det er standardprofilen for containerlukning for denne pakkeprofil.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="f7d0c-150">Vælg en indstilling i feltet Tilstanden Container-id.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="f7d0c-151">Denne indstilling bestemmer, om der automatisk genereres et container-id, når der oprettes en container, eller der oprettes et container-id manuelt.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="f7d0c-152">Indtast eller vælg en værdi i feltet Containertype.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d0c-153">Containertypen vil blive brugt som standard, når der oprettes en ny container.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="f7d0c-154">Markér afkrydsningsfeltet Opret automatisk container ved containerlukning.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="f7d0c-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-155">Click Save.</span></span>
10. <span data-ttu-id="f7d0c-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="f7d0c-157">Konfigurere profiler for containerlukning</span><span class="sxs-lookup"><span data-stu-id="f7d0c-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="f7d0c-158">Gå til Lagerstedsstyring > Konfiguration > Containere > Profiler for lukning af container.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="f7d0c-159">Containerlukningsprofiler definerer, hvad der sker, når en container er lukket.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="f7d0c-160">Du kan oprette flere containerlukningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="f7d0c-161">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-161">Click New.</span></span>
3. <span data-ttu-id="f7d0c-162">Skriv en værdi i feltet Profil-id for lukning af container.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="f7d0c-163">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d0c-164">Vælg en indstilling i feltet Manifest kl.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="f7d0c-165">Angiv, om der bruget et manifest ved lukning af containere eller bekræftelse af leverancen.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="f7d0c-166">Bemærk, at brug af et manifest kræver transportstyring.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="f7d0c-167">Der skal implementeres et manifest i transportprogrammer, for at det kan fungere.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="f7d0c-168">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="f7d0c-169">Indtast eller vælg en værdi i feltet Standardlokation til endelig forsendelse.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d0c-170">Dette er den lokation, som produkter skal flyttes til, når containerne er lukkede.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="f7d0c-171">Denne lokation skal have en lokationsprofil, der er defineret i Lagerstedsparametre.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="f7d0c-172">Indtast eller vælg en værdi i feltet Vægtenhed.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="f7d0c-173">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f7d0c-173">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]