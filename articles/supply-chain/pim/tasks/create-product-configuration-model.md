---
title: Oprette en ny model for produktkonfiguration
description: Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921359"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="7f3bb-103">Oprette en ny model for produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7f3bb-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f3bb-104">Denne procedure viser, hvordan du opretter en produktkonfigurationsmodel og indsætter stamoplysninger som f.eks. attributter og underkomponenter.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="7f3bb-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="7f3bb-106">Oprette en produktmodel</span><span class="sxs-lookup"><span data-stu-id="7f3bb-106">Create a product model</span></span>

1. <span data-ttu-id="7f3bb-107">Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="7f3bb-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-108">Select **New**.</span></span>
1. <span data-ttu-id="7f3bb-109">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7f3bb-110">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="7f3bb-111">Vælg en indstilling i feltet **Strategi for problemløser**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="7f3bb-112">Problemløserstrategien bestemmer, hvordan begrænsningerne i en begrænsningsbaseret model til produktkonfiguration behandles.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="7f3bb-113">Dette valg kan have indflydelse på produktkonfigurationsmodellens ydeevne.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="7f3bb-114">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="7f3bb-115">Rodkomponenten repræsenterer produktkonfigurationsmodellen, men den kan også bruges i andre produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="7f3bb-116">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-116">Select **OK**.</span></span>
1. <span data-ttu-id="7f3bb-117">I feltet **Genbrug konfigurationer** skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="7f3bb-118">Hvis genbrugskonfigurationsparameteren er indstillet til Ja, vil systemet søge efter identiske konfigurationer efter hver konfigurationssession, og genbruge, hvis der findes en nøjagtig match.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="7f3bb-119">Tilføj attributter</span><span class="sxs-lookup"><span data-stu-id="7f3bb-119">Add attributes</span></span>

1. <span data-ttu-id="7f3bb-120">Udvid sektionen **Attributter**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="7f3bb-121">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-121">Select **Add**.</span></span>
3. <span data-ttu-id="7f3bb-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7f3bb-123">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7f3bb-124">Skriv en værdi i feltet **Navn på problemløser**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="7f3bb-125">Problemløserens navn bruges til løsning af begrænsningsproblemer i variantstyringen.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="7f3bb-126">Det må ikke indeholde mellemrum eller specialtegn, undtagen _ (understregning).</span><span class="sxs-lookup"><span data-stu-id="7f3bb-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="7f3bb-127">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="7f3bb-128">Beskrivelsesteksten vises til brugeren af konfigurationen og kan derfor fungere som hjælp til at vælge den rigtige attributværdi.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="7f3bb-129">Indtast eller vælg en værdi i feltet **Attributtype**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="7f3bb-130">Attributtypen bestemmer, hvilke værdier der er tilgængelige for attributten.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="7f3bb-131">Marker afkrydsningsfeltet **Medtag i genbrug**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="7f3bb-132">Denne indstilling er kun tilgængelig, når indstillingen Genbrug konfigurationer er valgt.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="7f3bb-133">Når attributten medtages i genbrugsafkrydsningsfeltet betyder det, at denne attribut medtages, når systemet søger efter et nøjagtigt match.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="7f3bb-134">Tilføj underkomponenter</span><span class="sxs-lookup"><span data-stu-id="7f3bb-134">Add subcomponents</span></span>

1. <span data-ttu-id="7f3bb-135">Udvid sektionen **Underkomponenter**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="7f3bb-136">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-136">Select **Add**.</span></span>
3. <span data-ttu-id="7f3bb-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7f3bb-138">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7f3bb-139">Skriv en værdi i feltet **Navn på problemløser**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="7f3bb-140">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="7f3bb-141">Indtast eller vælg en værdi i feltet **Komponent**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="7f3bb-142">Hver underkomponent skal referere til en komponent-definition.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="7f3bb-143">Dette design understøtter genanvendelige komponenter og sikrer, at når en komponent er defineret, kan den bruges i mange produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="7f3bb-144">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-144">Select **Save**.</span></span>
9. <span data-ttu-id="7f3bb-145">Vælg **Oplysninger om styklistelinjer**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="7f3bb-146">Formularen Linjedetaljer i stykliste gør det muligt for brugeren at vælge de nødvendige egenskaber for underkomponenten.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="7f3bb-147">Hver egenskab kan gives en fast værdi eller knyttes til en attribut.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="7f3bb-148">Tilknytning til en attribut medfører, at linjeegenskaben for styklisten få andre værdier, afhængigt af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="7f3bb-149">Indtast eller vælg en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="7f3bb-150">Hver underkomponent repræsenterer konfigurerbare produktmaster med begrænsningsbaseret konfigurationsteknologi.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="7f3bb-151">Referencen sker via varenummeret.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="7f3bb-152">Marker afkrydsningsfeltet **Indstil**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="7f3bb-153">Vælg **Ja** i feltet **Beregning**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="7f3bb-154">Indstilling af beregning sikrer, at produktet skal medtages, når du kører en omkostningsberegning for produktet.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="7f3bb-155">Vælg fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="7f3bb-156">Marker afkrydsningsfeltet **Indstil**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="7f3bb-157">Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7f3bb-158">Antalsfeltet, der bestemmer, hvor meget af dette produkt, der forbruges i det konfigurerede produkt.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="7f3bb-159">Marker afkrydsningsfeltet **Indstil**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="7f3bb-160">Angiv et nummer i feltet **Pr. serie**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="7f3bb-161">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f3bb-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]