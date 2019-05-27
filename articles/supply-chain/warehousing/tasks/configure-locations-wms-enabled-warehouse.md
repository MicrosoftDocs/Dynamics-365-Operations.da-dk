---
title: Konfigurere lokationer på et WMS-aktiveret lagersted
description: Denne vejledning viser, hvordan du konfigurerer lokationsopsætningen for et nyt WMS-aktiveret lagersted (et lagersted, der bruger avancerede lagerstedsstyringsprocesser).
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2be3c7cb33225041872e8b747ba28063f897dae9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563474"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="42135-103">Konfigurere lokationer på et WMS-aktiveret lagersted</span><span class="sxs-lookup"><span data-stu-id="42135-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42135-104">Denne vejledning viser, hvordan du konfigurerer lokationsopsætningen for et nyt WMS-aktiveret lagersted (et lagersted, der bruger avancerede lagerstedsstyringsprocesser).</span><span class="sxs-lookup"><span data-stu-id="42135-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="42135-105">Processen udføres typisk af en lagerchef.</span><span class="sxs-lookup"><span data-stu-id="42135-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="42135-106">Du kan køre denne guide i demofirmaet USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="42135-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="42135-107">En forudsætning er, at du har konfigureret mindst ét websted.</span><span class="sxs-lookup"><span data-stu-id="42135-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="42135-108">Opret et nyt lagersted</span><span class="sxs-lookup"><span data-stu-id="42135-108">Create a new warehouse</span></span>
1. <span data-ttu-id="42135-109">Gå til Lagersteder.</span><span class="sxs-lookup"><span data-stu-id="42135-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="42135-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-110">Click New.</span></span>
3. <span data-ttu-id="42135-111">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="42135-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="42135-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="42135-113">Skriv en værdi i feltet Sted.</span><span class="sxs-lookup"><span data-stu-id="42135-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="42135-114">Vis eller skjul sektionen Lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="42135-115">Angiv indstillingen Brug lagerstedsstyringsprocesser til Ja.</span><span class="sxs-lookup"><span data-stu-id="42135-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="42135-116">Denne indstilling giver dig mulighed at køre avancerede lagerprocesser ved hjælp af lagerstedsarbejde og mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="42135-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="42135-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="42135-118">Definere et lokalitetsformat</span><span class="sxs-lookup"><span data-stu-id="42135-118">Define a location format</span></span>
1. <span data-ttu-id="42135-119">Gå til Lokationsformater.</span><span class="sxs-lookup"><span data-stu-id="42135-119">Go to Location formats.</span></span>
    * <span data-ttu-id="42135-120">Placering-formater er et navngivningssystem, der bruges til at oprette entydige og konsekvent navne for de forskellige placeringpositioner på et lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="42135-121">Det kan være nyttigt at bruge separatorer som en del af placeringsformatet for at gøre det nemmere at identificere komponenter på lokationen som gangnummeret.</span><span class="sxs-lookup"><span data-stu-id="42135-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="42135-122">I dette eksempel skal vi oprette et navn med fire komponenter.</span><span class="sxs-lookup"><span data-stu-id="42135-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="42135-123">Disse kan for eksempel være gang, reol, hylde og placering.</span><span class="sxs-lookup"><span data-stu-id="42135-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="42135-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-124">Click New.</span></span>
3. <span data-ttu-id="42135-125">Skriv en værdi i feltet Lokationsformat.</span><span class="sxs-lookup"><span data-stu-id="42135-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="42135-126">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="42135-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="42135-127">Skriv en værdi i feltet Segmentbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="42135-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="42135-128">Dette beskriver, hvad den første komponent i lokationsnavnet repræsenterer.</span><span class="sxs-lookup"><span data-stu-id="42135-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="42135-129">Det kan for eksempel være Gang.</span><span class="sxs-lookup"><span data-stu-id="42135-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="42135-130">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="42135-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="42135-131">Dette bestemmer, hvor mange tegn denne del af lokationsnavnet må indeholde.</span><span class="sxs-lookup"><span data-stu-id="42135-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="42135-132">Bemærk, at summen af alle komponenterne i navnet, herunder separatorer, ikke må overstige 10 tegn.</span><span class="sxs-lookup"><span data-stu-id="42135-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="42135-133">Skriv en værdi i feltet Separator.</span><span class="sxs-lookup"><span data-stu-id="42135-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="42135-134">Dette bestemmer, hvilket tegn eller symbol der bruges mellem den første og anden komponent i navnet.</span><span class="sxs-lookup"><span data-stu-id="42135-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="42135-135">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-135">Click New.</span></span>
9. <span data-ttu-id="42135-136">Skriv en værdi i feltet Segmentbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="42135-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="42135-137">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="42135-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="42135-138">Skriv en værdi i feltet Separator.</span><span class="sxs-lookup"><span data-stu-id="42135-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="42135-139">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-139">Click New.</span></span>
13. <span data-ttu-id="42135-140">Skriv en værdi i feltet Segmentbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="42135-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="42135-141">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="42135-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="42135-142">Skriv en værdi i feltet Separator.</span><span class="sxs-lookup"><span data-stu-id="42135-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="42135-143">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-143">Click New.</span></span>
17. <span data-ttu-id="42135-144">Skriv en værdi i feltet Segmentbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="42135-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="42135-145">Angiv et tal i feltet Længde.</span><span class="sxs-lookup"><span data-stu-id="42135-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="42135-146">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="42135-146">Click Save.</span></span>
20. <span data-ttu-id="42135-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="42135-148">Definere lokalitetstyper</span><span class="sxs-lookup"><span data-stu-id="42135-148">Define location types</span></span>
1. <span data-ttu-id="42135-149">Gå til Lokationstyper.</span><span class="sxs-lookup"><span data-stu-id="42135-149">Go to Location types.</span></span>
    * <span data-ttu-id="42135-150">Lokationstyper kan bruges til at filtrere indstillinger for at styre de forskellige lagerstedsstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="42135-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="42135-151">Som minimum skal du oprette midlertidige og endelige afsendelseslokationstyper for at definere styring af udgående lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="42135-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="42135-152">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-152">Click New.</span></span>
3. <span data-ttu-id="42135-153">Indtast en værdi i feltet Lokalitetstype.</span><span class="sxs-lookup"><span data-stu-id="42135-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="42135-154">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="42135-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="42135-155">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="42135-156">Definere lokalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="42135-156">Define location profile</span></span>
1. <span data-ttu-id="42135-157">Gå til Lokationsprofiler.</span><span class="sxs-lookup"><span data-stu-id="42135-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="42135-158">Definitionen af lokationsprofiler er meget vigtigt.</span><span class="sxs-lookup"><span data-stu-id="42135-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="42135-159">Grupperede lokaliteters kapacitet kan styres her, og de politikker, der er relateret til, hvilket lager der gemmes, og hvordan det gemmes.</span><span class="sxs-lookup"><span data-stu-id="42135-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="42135-160">Lokationprofiler kan bruges til at filtrere indstillinger for at styre de forskellige lagerstedsstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="42135-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="42135-161">Som minimum skal du oprette en brugerlokationsprofil for at aktivere lagerstedsstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="42135-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="42135-162">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-162">Click New.</span></span>
3. <span data-ttu-id="42135-163">Skriv en værdi i feltet Id for lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="42135-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="42135-164">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="42135-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="42135-165">Klik på rullelisten i feltet Lokationsformat for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="42135-166">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="42135-167">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="42135-168">Klik på rullelisten i feltet Lokationstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="42135-169">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="42135-170">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="42135-171">Markér eller fjern markeringen i afkrydsningsfeltet Tillad blandede lagerstatusser.</span><span class="sxs-lookup"><span data-stu-id="42135-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="42135-172">Aktiver denne indstilling, hvis du vil tillade blandede lagerstatusværdier på de lokaliteter, der skal grupperes efter denne lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="42135-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="42135-173">Markér eller fjern markeringen i afkrydsningsfeltet Tilsidesæt regler for batchdage.</span><span class="sxs-lookup"><span data-stu-id="42135-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="42135-174">Aktiver denne indstilling for at tilsidesætte reglen for, hvor mange dage lagerbatchudløbsdatoer kan variere, for at tillade blanding af lagerbatches, der ikke overholder denne regel.</span><span class="sxs-lookup"><span data-stu-id="42135-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="42135-175">Marker eller fjern markeringen i afkrydsningsfeltet Tillad cyklusoptælling.</span><span class="sxs-lookup"><span data-stu-id="42135-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="42135-176">Aktiver denne indstilling, hvis du vil tillade behandling af cyklusoptælling på alle de lokaliteter, der skal grupperes efter denne lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="42135-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="42135-177">Vis eller skjul sektionen Dimensioner.</span><span class="sxs-lookup"><span data-stu-id="42135-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="42135-178">Fanen Dimensioner giver dig mulighed for at definere parametre og metoder, så der kan foretages aktivere nøjagtige beregninger af belastkapacitet inden for hver af lokaliteterne.</span><span class="sxs-lookup"><span data-stu-id="42135-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="42135-179">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="42135-180">Aktivér parametre for lagerstedsstyring</span><span class="sxs-lookup"><span data-stu-id="42135-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="42135-181">Gå til Parametre til lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="42135-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="42135-182">For at kunne behandle lagerstedsarbejde skal du angive parametre for brugerlokationsprofilen, den midlertidige lokationstype og den endelige afsendelseslokationstype Så snart, den udgående processen afsluttes på den endelige afsendelseslokationstype, du definerer, opdateres de relaterede udgående transaktioner til 'Plukket'.</span><span class="sxs-lookup"><span data-stu-id="42135-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="42135-183">Vis eller skjul sektionen Lokalitetsprofiler.</span><span class="sxs-lookup"><span data-stu-id="42135-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="42135-184">Klik på rullelisten i feltet Brugerlokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="42135-185">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="42135-186">Vis eller skjul sektionen Lokalitetstyper.</span><span class="sxs-lookup"><span data-stu-id="42135-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="42135-187">Klik på rullelisten i feltet Midlertidig lokalitetstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="42135-188">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="42135-189">Klik på rullelisten i feltet Endelig afsendelseslokalitetstype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="42135-190">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="42135-191">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="42135-192">Definere lagerstedszonegrupper</span><span class="sxs-lookup"><span data-stu-id="42135-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="42135-193">Gå til Lagerstedszonegrupper.</span><span class="sxs-lookup"><span data-stu-id="42135-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="42135-194">Lagerstedszoner kan bruges som filtre for indstillinger for at styre de forskellige lagerstedsstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="42135-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="42135-195">Du skal oprette en zonegruppe, før du kan definere en zone.</span><span class="sxs-lookup"><span data-stu-id="42135-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="42135-196">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-196">Click New.</span></span>
3. <span data-ttu-id="42135-197">Skriv en værdi i feltet Id for zonegruppe.</span><span class="sxs-lookup"><span data-stu-id="42135-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="42135-198">Skriv en værdi i feltet Navn på zonegruppe.</span><span class="sxs-lookup"><span data-stu-id="42135-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="42135-199">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="42135-200">Definere Lagerstedszoner</span><span class="sxs-lookup"><span data-stu-id="42135-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="42135-201">Gå til Zoner.</span><span class="sxs-lookup"><span data-stu-id="42135-201">Go to Zones.</span></span>
2. <span data-ttu-id="42135-202">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-202">Click New.</span></span>
3. <span data-ttu-id="42135-203">Skriv en værdi i feltet Zone-id</span><span class="sxs-lookup"><span data-stu-id="42135-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="42135-204">Skriv en værdi i feltet Navn på zone.</span><span class="sxs-lookup"><span data-stu-id="42135-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="42135-205">Klik på rullelisten i feltet Id for zonegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="42135-206">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="42135-207">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="42135-208">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="42135-209">Oprette lokationer ved hjælp af guiden Konfiguration af lokalitet</span><span class="sxs-lookup"><span data-stu-id="42135-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="42135-210">Gå til guiden Konfiguration af lokalitet.</span><span class="sxs-lookup"><span data-stu-id="42135-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="42135-211">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="42135-212">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="42135-213">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="42135-214">Klik på rullelisten i feltet Zone-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="42135-215">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="42135-216">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="42135-217">Klik på rullelisten i feltet Id for lokalitetsprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="42135-218">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="42135-219">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="42135-220">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="42135-221">Indtast et tal i feltet Fra numnmer.</span><span class="sxs-lookup"><span data-stu-id="42135-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="42135-222">Felterne Fra nummer og Til nummer definerer, hvor mange lokaliteter, der bliver oprettet.</span><span class="sxs-lookup"><span data-stu-id="42135-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="42135-223">Hvis du for eksempel angiver Fra nummer til 1 og Til nummer til 3 for alle fire linjer i lokationsformatet, oprettes 81 lokaliteter (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="42135-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="42135-224">Indtast et tal i feltet Til nummer.</span><span class="sxs-lookup"><span data-stu-id="42135-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="42135-225">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="42135-226">Indtast et tal i feltet Fra numnmer.</span><span class="sxs-lookup"><span data-stu-id="42135-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="42135-227">Indtast et tal i feltet Til nummer.</span><span class="sxs-lookup"><span data-stu-id="42135-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="42135-228">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="42135-229">Indtast et tal i feltet Fra numnmer.</span><span class="sxs-lookup"><span data-stu-id="42135-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="42135-230">Indtast et tal i feltet Til nummer.</span><span class="sxs-lookup"><span data-stu-id="42135-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="42135-231">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="42135-232">Indtast et tal i feltet Fra numnmer.</span><span class="sxs-lookup"><span data-stu-id="42135-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="42135-233">Indtast et tal i feltet Til nummer.</span><span class="sxs-lookup"><span data-stu-id="42135-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="42135-234">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="42135-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="42135-235">Oprette lokaliteter manuelt</span><span class="sxs-lookup"><span data-stu-id="42135-235">Create locations manually</span></span>
1. <span data-ttu-id="42135-236">Gå til Lokaliteter.</span><span class="sxs-lookup"><span data-stu-id="42135-236">Go to Locations.</span></span>
    * <span data-ttu-id="42135-237">Det er nemt manuelt at oprette lokaliteter i lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="42135-238">Lokalitetens navn og profil-ID er obligatoriske værdier.</span><span class="sxs-lookup"><span data-stu-id="42135-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="42135-239">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-239">Click New.</span></span>
3. <span data-ttu-id="42135-240">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="42135-241">Skriv en værdi i feltet Lokalitet.</span><span class="sxs-lookup"><span data-stu-id="42135-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="42135-242">Bemærk, at du opretter en ny lokalitet her, så du skal skrive et nyt entydigt navn i stedet for at vælge et eksisterende navn.</span><span class="sxs-lookup"><span data-stu-id="42135-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="42135-243">Skriv en værdi i feltet Id for lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="42135-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="42135-244">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="42135-245">Definere Kategorier af pakkestørrelse</span><span class="sxs-lookup"><span data-stu-id="42135-245">Define Pack size categories</span></span>
1. <span data-ttu-id="42135-246">Gå til Kategorier af pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="42135-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="42135-247">Kategorier af pakkestørrelse kan bruges til gruppering af varer, der har samme fysiske pakkestørrelser.</span><span class="sxs-lookup"><span data-stu-id="42135-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="42135-248">I dette eksempel bruges pakkestørrelsekategorien til at styre kapaciteten på plukkelokaliteterne inden for en bestemt zone på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="42135-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="42135-249">Bemærk, at pakkestørrelsekategori-id'et skal tildeles til det frigivne produkt for at kunne bruges som en del af behandlingen af grænser for lokationslagring.</span><span class="sxs-lookup"><span data-stu-id="42135-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="42135-250">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-250">Click New.</span></span>
3. <span data-ttu-id="42135-251">Skriv en værdi i feltet Kategori-id for pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="42135-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="42135-252">Skriv en værdi i feltet Kategorinavn på pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="42135-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="42135-253">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="42135-254">Definere grænser for lokalitetslagring</span><span class="sxs-lookup"><span data-stu-id="42135-254">Define location stocking limits</span></span>
1. <span data-ttu-id="42135-255">Gå til Grænser for lokalitetslagring.</span><span class="sxs-lookup"><span data-stu-id="42135-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="42135-256">Grænser for lokationslagring hjælper med til at sikre, at arbejdet ikke oprettes for at anmode om, at lageret skal placeres på en lokalitet, der ikke har den fysiske kapacitet til rumme lageret.</span><span class="sxs-lookup"><span data-stu-id="42135-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="42135-257">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-257">Click New.</span></span>
3. <span data-ttu-id="42135-258">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="42135-259">Skriv en værdi i feltet Id for lokationsprofil.</span><span class="sxs-lookup"><span data-stu-id="42135-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="42135-260">Skriv en værdi i feltet Kategori-id for pakkestørrelse.</span><span class="sxs-lookup"><span data-stu-id="42135-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="42135-261">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="42135-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="42135-262">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="42135-262">Click Save.</span></span>
8. <span data-ttu-id="42135-263">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="42135-264">Definere faste plukpladser</span><span class="sxs-lookup"><span data-stu-id="42135-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="42135-265">Gå til Faste lokationer.</span><span class="sxs-lookup"><span data-stu-id="42135-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="42135-266">Du kan definere de lokaliteter, der skal bruges pr. produkt eller produktvariant.</span><span class="sxs-lookup"><span data-stu-id="42135-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="42135-267">Det er muligt at oprette flere faste lokaliteter til det samme produkt inden for det samme lager.</span><span class="sxs-lookup"><span data-stu-id="42135-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="42135-268">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42135-268">Click New.</span></span>
3. <span data-ttu-id="42135-269">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="42135-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="42135-270">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="42135-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="42135-271">Klik på rullelisten i feltet Lokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42135-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="42135-272">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42135-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="42135-273">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="42135-273">Close the page.</span></span>

