--- 
title: Oprette en ny model for produktkonfiguration
description: "Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 866a4f29723e10eb0a1e1be86d6d4f6da8a69b1c
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="3163f-103">Oprette en ny model for produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3163f-103">Create a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3163f-104">Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter.</span><span class="sxs-lookup"><span data-stu-id="3163f-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="3163f-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="3163f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="3163f-106">Oprette en produktmodel</span><span class="sxs-lookup"><span data-stu-id="3163f-106">Create a product model</span></span>
1. <span data-ttu-id="3163f-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="3163f-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3163f-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="3163f-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="3163f-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3163f-109">Click New.</span></span>
4. <span data-ttu-id="3163f-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3163f-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3163f-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3163f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3163f-112">Vælg en indstilling i feltet Strategi for problemløser.</span><span class="sxs-lookup"><span data-stu-id="3163f-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="3163f-113">Problemløserstrategien bestemmer, hvordan begrænsningerne i en begrænsningsbaseret model til produktkonfiguration behandles.</span><span class="sxs-lookup"><span data-stu-id="3163f-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="3163f-114">Dette valg kan have indflydelse på produktkonfigurationsmodellens ydeevne.</span><span class="sxs-lookup"><span data-stu-id="3163f-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="3163f-115">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3163f-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3163f-116">Rodkomponenten repræsenterer produktkonfigurationsmodellen, men den kan også bruges i andre produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="3163f-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="3163f-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3163f-117">Click OK.</span></span>
9. <span data-ttu-id="3163f-118">I feltet Genbrug konfigurationer skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="3163f-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="3163f-119">Hvis genbrugskonfigurationsparameteren er indstillet til Ja, vil systemet søge efter identiske konfigurationer efter hver konfigurationssession, og genbruge, hvis der findes en nøjagtig match.</span><span class="sxs-lookup"><span data-stu-id="3163f-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="3163f-120">Tilføj attributter</span><span class="sxs-lookup"><span data-stu-id="3163f-120">Add attributes</span></span>
1. <span data-ttu-id="3163f-121">Udvid sektionen Attributter.</span><span class="sxs-lookup"><span data-stu-id="3163f-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="3163f-122">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3163f-122">Click Add.</span></span>
3. <span data-ttu-id="3163f-123">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3163f-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3163f-124">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3163f-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3163f-125">Skriv en værdi i feltet Navn på problemløser.</span><span class="sxs-lookup"><span data-stu-id="3163f-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="3163f-126">Problemløserens navn bruges til løsning af begrænsningsproblemer af variantstyringen.</span><span class="sxs-lookup"><span data-stu-id="3163f-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="3163f-127">Det må ikke indeholde mellemrum eller specialtegn, undtagen _ (understregning).</span><span class="sxs-lookup"><span data-stu-id="3163f-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="3163f-128">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3163f-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3163f-129">Beskrivelsesteksten vises til brugeren af konfigurationen og kan derfor fungere som hjælp til at vælge den rigtige attributværdi.</span><span class="sxs-lookup"><span data-stu-id="3163f-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="3163f-130">Indtast eller vælg en værdi i feltet Attributtype.</span><span class="sxs-lookup"><span data-stu-id="3163f-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="3163f-131">Attributtypen bestemmer, hvilke værdier der er tilgængelige for attributten.</span><span class="sxs-lookup"><span data-stu-id="3163f-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="3163f-132">Marker afkrydsningsfeltet Medtag i genbrug.</span><span class="sxs-lookup"><span data-stu-id="3163f-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="3163f-133">Denne indstilling er kun tilgængelig, når indstillingen Genbrug konfigurationer er valgt.</span><span class="sxs-lookup"><span data-stu-id="3163f-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="3163f-134">Når attributten medtages i genbrugsafkrydsningsfeltet betyder det, at denne attribut medtages, når systemet søger efter et nøjagtigt match.</span><span class="sxs-lookup"><span data-stu-id="3163f-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="3163f-135">Tilføj underkomponenter</span><span class="sxs-lookup"><span data-stu-id="3163f-135">Add subcomponents</span></span>
1. <span data-ttu-id="3163f-136">Vis eller skjul sektionen Underkomponenter.</span><span class="sxs-lookup"><span data-stu-id="3163f-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="3163f-137">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3163f-137">Click Add.</span></span>
3. <span data-ttu-id="3163f-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3163f-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3163f-139">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3163f-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3163f-140">Skriv en værdi i feltet Navn på problemløser.</span><span class="sxs-lookup"><span data-stu-id="3163f-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="3163f-141">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3163f-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="3163f-142">Indtast eller vælg en værdi i feltet Komponent.</span><span class="sxs-lookup"><span data-stu-id="3163f-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="3163f-143">Hver underkomponent skal referere til en komponent-definition.</span><span class="sxs-lookup"><span data-stu-id="3163f-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="3163f-144">Dette design understøtter genanvendelige komponenter og sikrer, at når en komponent er defineret, kan den bruges i mange produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="3163f-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="3163f-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3163f-145">Click Save.</span></span>
9. <span data-ttu-id="3163f-146">Klik på Linjedetaljer i stykliste.</span><span class="sxs-lookup"><span data-stu-id="3163f-146">Click BOM line details.</span></span>
    * <span data-ttu-id="3163f-147">Formularen Linjedetaljer i stykliste gør det muligt for brugeren at vælge de nødvendige egenskaber for underkomponenten.</span><span class="sxs-lookup"><span data-stu-id="3163f-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="3163f-148">Hver egenskab kan gives en fast værdi eller knyttes til en attribut.</span><span class="sxs-lookup"><span data-stu-id="3163f-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="3163f-149">Tilknytning til en attribut medfører, at linjeegenskaben for styklisten få andre værdier, afhængigt af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3163f-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="3163f-150">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="3163f-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="3163f-151">Hver underkomponent repræsenterer konfigurerbare produktmaster med begrænsningsbaseret konfigurationsteknologi.</span><span class="sxs-lookup"><span data-stu-id="3163f-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="3163f-152">Referencen sker via varenummeret.</span><span class="sxs-lookup"><span data-stu-id="3163f-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="3163f-153">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="3163f-153">Select the Set check box.</span></span>
12. <span data-ttu-id="3163f-154">Vælg Ja i feltet Beregning.</span><span class="sxs-lookup"><span data-stu-id="3163f-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="3163f-155">Indstilling af beregning sikrer, at produktet skal medtages, når du kører en omkostningsberegning for produktet.</span><span class="sxs-lookup"><span data-stu-id="3163f-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="3163f-156">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="3163f-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="3163f-157">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="3163f-157">Select the Set check box.</span></span>
15. <span data-ttu-id="3163f-158">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="3163f-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3163f-159">Antalsfeltet, der bestemmer, hvor meget af dette produkt, der forbruges i det konfigurerede produkt.</span><span class="sxs-lookup"><span data-stu-id="3163f-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="3163f-160">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="3163f-160">Select the Set check box.</span></span>
17. <span data-ttu-id="3163f-161">Angiv et nummer i feltet Pr. serie.</span><span class="sxs-lookup"><span data-stu-id="3163f-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="3163f-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3163f-162">Click OK.</span></span>


