---
title: Lagerstedsallokering
description: Dette emne indeholder oplysninger om lagerstedsallokering. Lagerstedsallokering gør det muligt at konsolidere efterspørgsel efter vare og måleenhed fra ordrer, der har statussen bestilt, reserveret eller frigivet. Den gør det lettere for lagerchefer at planlægge pluklokationer på en intelligent måde, før de frigiver ordrerne til lageret og opretter plukarbejde.
author: mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d9080f192db0c59b4b4bc74468491e86ba0b7471
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530345"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="3a57f-105">Lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="3a57f-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a57f-106">Lagerstedsallokering gør det muligt at konsolidere efterspørgsel efter vare og måleenhed fra ordrer, der har statussen *bestilt*, *reserveret* eller *frigivet*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="3a57f-107">Genereret efterspørgsel kan derefter anvendes på lokationer, der skal bruges til plukning, baseret på antal, enhed, fysiske dimensioner, faste lokationer mv.</span><span class="sxs-lookup"><span data-stu-id="3a57f-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="3a57f-108">Når allokeringsplanen er blevet oprettet, kan genopfyldningsarbejdet oprettes for at bringe den korrekte lagermængde til hver lokation.</span><span class="sxs-lookup"><span data-stu-id="3a57f-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="3a57f-109">Denne funktion gør det lettere for lagerchefer at planlægge pluklokationer på en intelligent måde, før de frigiver ordrerne til lageret og opretter plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="3a57f-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="3a57f-110">Aktivér funktionen til lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="3a57f-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="3a57f-111">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="3a57f-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="3a57f-112">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="3a57f-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3a57f-113">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3a57f-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3a57f-114">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="3a57f-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3a57f-115">**Funktionsnavn:** *Funktion til lagerstedsallokering*</span><span class="sxs-lookup"><span data-stu-id="3a57f-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="3a57f-116">Konfigurere lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="3a57f-116">Set up warehouse slotting</span></span>

<span data-ttu-id="3a57f-117">Hvis du vil bruge lagerstedsallokering, skal du konfigurere følgende elementer i dit system.</span><span class="sxs-lookup"><span data-stu-id="3a57f-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="3a57f-118">Oprette måleenhedsniveauer for allokering</span><span class="sxs-lookup"><span data-stu-id="3a57f-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="3a57f-119">Måleenhedsniveauerne gør det muligt at gruppere flere måleenheder med henblik på allokering.</span><span class="sxs-lookup"><span data-stu-id="3a57f-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="3a57f-120">Hvis der f.eks. plukkes flere størrelser af kasser fra det samme kasseplukområde, kan der oprettes ét niveau for alle størrelserne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="3a57f-121">**Der skal oprettes en linje for hver måleenhed, der skal være en del af niveauet.**</span><span class="sxs-lookup"><span data-stu-id="3a57f-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="3a57f-122">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Måleenhedsniveauer til allokering**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="3a57f-123">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-123">Select **New**.</span></span>
1. <span data-ttu-id="3a57f-124">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="3a57f-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="3a57f-125">**Måleenhedsniveau:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="3a57f-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="3a57f-126">**Beskrivelse:** *Hver kassepalle*</span><span class="sxs-lookup"><span data-stu-id="3a57f-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="3a57f-127">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-127">Select **Save**.</span></span>
1. <span data-ttu-id="3a57f-128">Gå til oversigtspanelet **Måleenheder**, og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3a57f-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3a57f-129">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-130">**Enhed:** *Kasse*</span><span class="sxs-lookup"><span data-stu-id="3a57f-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="3a57f-131">**Beskrivelse:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="3a57f-132">Det udfyldes automatisk, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="3a57f-133">**Enhedsklasse:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="3a57f-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="3a57f-134">Vælg **Ny** for at føje en anden linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3a57f-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="3a57f-135">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-136">**Enhed:** *Styk*</span><span class="sxs-lookup"><span data-stu-id="3a57f-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="3a57f-137">**Beskrivelse:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="3a57f-138">Det udfyldes automatisk, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="3a57f-139">**Enhedsklasse:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="3a57f-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="3a57f-140">Vælg **Ny** for at føje en tredje linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3a57f-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="3a57f-141">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-142">**Enhed:** *PL*</span><span class="sxs-lookup"><span data-stu-id="3a57f-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="3a57f-143">**Beskrivelse:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="3a57f-144">Det udfyldes automatisk, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="3a57f-145">**Enhedsklasse:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="3a57f-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="3a57f-146">Vælg **Gem** for at gemme niveauet.</span><span class="sxs-lookup"><span data-stu-id="3a57f-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="3a57f-147">Oprette en vejledningskode til allokering</span><span class="sxs-lookup"><span data-stu-id="3a57f-147">Create a directive code for slotting</span></span>

<span data-ttu-id="3a57f-148">Du skal vælge den vejledningskode, der skal knyttes til en skabelon.</span><span class="sxs-lookup"><span data-stu-id="3a57f-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="3a57f-149">Gå til **Lokationsstyring \> Opsætning \> Vejledningskoder**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="3a57f-150">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3a57f-151">I feltet **Vejledningskode** skal du angive *Allokering*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="3a57f-152">I feltet **Vejledningsbeskrivelse** skal du angive *Allokering*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="3a57f-153">Konfigurere allokeringsskabeloner</span><span class="sxs-lookup"><span data-stu-id="3a57f-153">Set up slotting templates</span></span>

<span data-ttu-id="3a57f-154">Hver allokeringsskabelon styrer, hvordan lager tilknyttes lokationer for et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="3a57f-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="3a57f-155">Hver skabelon skal indeholde en linje for hver allokeringsspecifikation.</span><span class="sxs-lookup"><span data-stu-id="3a57f-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="3a57f-156">Brug procedurerne i dette afsnit til at konfigurere allokeringsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="3a57f-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="3a57f-157">Gå til **Lagerstedsstyring \> Konfiguration \> Genopfyldning \> Allokeringsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="3a57f-158">Vælg **Ny** for at oprette en skabelon.</span><span class="sxs-lookup"><span data-stu-id="3a57f-158">Select **New** to create a template.</span></span>

<span data-ttu-id="3a57f-159">Derefter skal du konfigurere skabelonhovedet, allokeringsspecifikationerne og lokationsvejledningerne som forklaret i følgende under afsnit.</span><span class="sxs-lookup"><span data-stu-id="3a57f-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="3a57f-160">Oprette en overskrift til allokeringsskabeloner</span><span class="sxs-lookup"><span data-stu-id="3a57f-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="3a57f-161">Angiv følgende værdier i overskriften for skabelonen:</span><span class="sxs-lookup"><span data-stu-id="3a57f-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="3a57f-162">**Allokeringsskabelon:** _61_</span><span class="sxs-lookup"><span data-stu-id="3a57f-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="3a57f-163">**Beskrivelse:** _61_</span><span class="sxs-lookup"><span data-stu-id="3a57f-163">**Description:** _61_</span></span>
    - <span data-ttu-id="3a57f-164">**Efterspørgselstype:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="3a57f-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="3a57f-165">Den eneste efterspørgselstype, der understøttes i øjeblikket, er *Salgsordre*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="3a57f-166">**Efterspørgselsstrategi:** _Bestilt_</span><span class="sxs-lookup"><span data-stu-id="3a57f-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="3a57f-167">Følgende værdier er tilgængelige i dette felt:</span><span class="sxs-lookup"><span data-stu-id="3a57f-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="3a57f-168">**Bestilt** – det fuldt bestilte antal på salgsordren skal betragtes som efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="3a57f-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="3a57f-169">**Reserveret** – det er kun de salgsordrelinjemængder, der er reserveret (fysisk og bestilt), som skal betragtes som efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="3a57f-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="3a57f-170">**Lagersted:** _61_</span><span class="sxs-lookup"><span data-stu-id="3a57f-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="3a57f-171">**Tillad bølgeefterspørgsel at bruge ikke-reserverede antal:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="3a57f-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="3a57f-172">Du kan også angive en forespørgsel for at indsnævre omfanget af den efterspørgsel, der evalueres.</span><span class="sxs-lookup"><span data-stu-id="3a57f-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="3a57f-173">Konfigurere allokeringsspecifikationer for hver skabelon</span><span class="sxs-lookup"><span data-stu-id="3a57f-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="3a57f-174">For hver skabelon, du opretter, skal du udføre disse trin for at tilføje en linje for hver allokeringsspecifikation.</span><span class="sxs-lookup"><span data-stu-id="3a57f-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="3a57f-175">Gå til oversigtspanelet **Detaljer om allokeringsskabelon**, og vælg **Ny** for at oprette en skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="3a57f-176">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-177">**Sekvens:** _1_</span><span class="sxs-lookup"><span data-stu-id="3a57f-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="3a57f-178">**Beskrivelse:** _Fast lokation_</span><span class="sxs-lookup"><span data-stu-id="3a57f-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="3a57f-179">**Minimummængde:** _1_</span><span class="sxs-lookup"><span data-stu-id="3a57f-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="3a57f-180">Dette felt definerer det mindste efterspørgselsantal, der kræves til linjen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="3a57f-181">**Maksimummængde:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="3a57f-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="3a57f-182">Dette felt definerer det maksimale efterspørgselsantal, der er gyldig til linjen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="3a57f-183">**Enhed:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="3a57f-184">Dette felt definerer den måleenhed, som minimum- og maksimumantallet refererer til.</span><span class="sxs-lookup"><span data-stu-id="3a57f-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="3a57f-185">**Måleenhedsniveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="3a57f-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="3a57f-186">Dette felt definerer måleenheden for efterspørgsel, der er gyldig til linjen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="3a57f-187">(Få flere oplysninger i afsnittet i [Oprette måleenhedsniveauer for allokering](#unit-tiers) tidligere i dette emne.)</span><span class="sxs-lookup"><span data-stu-id="3a57f-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="3a57f-188">**Tildel allokeringskriterier:** _Overvej antal_</span><span class="sxs-lookup"><span data-stu-id="3a57f-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="3a57f-189">Følgende værdier er tilgængelige i dette felt:</span><span class="sxs-lookup"><span data-stu-id="3a57f-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="3a57f-190">**Antag tom** – dette system skal antage, at alle lokationer i plukområdet er tomme, og det skal ikke kontrollere disse lokationer med hensyn til lager.</span><span class="sxs-lookup"><span data-stu-id="3a57f-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="3a57f-191">**Overvej antal** – systemet skal kontrollere lokationerne i plukområdet for lager og skal springe lokationer over, der ikke er tomme.</span><span class="sxs-lookup"><span data-stu-id="3a57f-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="3a57f-192">**Vejledningskode:** _Allokering_</span><span class="sxs-lookup"><span data-stu-id="3a57f-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="3a57f-193">Dette felt definerer lokationsvejledningen, der bruges til at finde pluklokationen for genopfyldningsarbejdet.</span><span class="sxs-lookup"><span data-stu-id="3a57f-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="3a57f-194">**Overløbslokation:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="3a57f-195">I dette felt defineres den lokation, som det lager, hvortil der lægges på lager, hvis der ikke kan findes en lokation for antallet, da linjen blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="3a57f-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="3a57f-196">**Tillad brug:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="3a57f-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="3a57f-197">Når denne indstilling er angivet til *Ja*, og hvis det ikke muligt allokere noget efterspørgsel, vil der blive oprettet bevægelsesarbejde for at fjerne lager fra lokationer, hvor der er lager, men hvor der ikke er sket nogen allokering.</span><span class="sxs-lookup"><span data-stu-id="3a57f-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="3a57f-198">Skabelonen køres derefter igen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-198">The template is then run again.</span></span> <span data-ttu-id="3a57f-199">Denne gang ignoreres lageret på lokationerne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="3a57f-200">Denne funktion fungerer bedst, når feltet **Tildel allokeringskriterier** er indstillet til at _Overvej antal_.</span><span class="sxs-lookup"><span data-stu-id="3a57f-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="3a57f-201">**Brug af fast lokation:** _Kun faste lokationer til produktet_</span><span class="sxs-lookup"><span data-stu-id="3a57f-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="3a57f-202">Følgende værdier er tilgængelige i dette felt:</span><span class="sxs-lookup"><span data-stu-id="3a57f-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="3a57f-203">**Faste og ikke-faste lokationer** – systemet skal ikke være begrænset til kun at bruge faste lokationer.</span><span class="sxs-lookup"><span data-stu-id="3a57f-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="3a57f-204">**Kun faste lokationer til produktet** – systemet skal kun allokere til lokationer, der er faste lokationer for produktet.</span><span class="sxs-lookup"><span data-stu-id="3a57f-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="3a57f-205">**Kun faste lokationer til produktvarianten** – systemet skal kun allokere til lokationer, der er faste lokationer for produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="3a57f-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="3a57f-206">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-206">Select **Save**.</span></span>
1. <span data-ttu-id="3a57f-207">Vælg **Ny** for at oprette en linje for anden skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="3a57f-208">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-209">**Sekvens:** _2_</span><span class="sxs-lookup"><span data-stu-id="3a57f-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="3a57f-210">**Beskrivelse:** _Andet_</span><span class="sxs-lookup"><span data-stu-id="3a57f-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="3a57f-211">**Minimumantal:** _1_</span><span class="sxs-lookup"><span data-stu-id="3a57f-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="3a57f-212">**Maksimumantal:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="3a57f-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="3a57f-213">**Enhed:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="3a57f-214">**Måleenhedsniveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="3a57f-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="3a57f-215">**Tildel allokeringskriterier:** _Overvej antal_</span><span class="sxs-lookup"><span data-stu-id="3a57f-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="3a57f-216">**Vejledningskode:** _Allokering_</span><span class="sxs-lookup"><span data-stu-id="3a57f-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="3a57f-217">**Overløbslokation:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="3a57f-218">**Tillad brug:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="3a57f-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="3a57f-219">**Brug faste lokationer:** _Faste og ikke-faste lokationer_</span><span class="sxs-lookup"><span data-stu-id="3a57f-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="3a57f-220">I forespørgslen til den anden linje skal du nu angive de kriterier, der bruges til at bestemme, hvilke lokationer efterspørgslen for den linje kan allokeres til.</span><span class="sxs-lookup"><span data-stu-id="3a57f-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="3a57f-221">Vælg den linje, hvor feltet **Rækkefølge** er angivet til *2*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="3a57f-222">Vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="3a57f-223">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3a57f-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="3a57f-224">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-225">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="3a57f-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="3a57f-226">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="3a57f-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="3a57f-227">**Felt:** *Lokationsprofil-id*</span><span class="sxs-lookup"><span data-stu-id="3a57f-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="3a57f-228">**Kriterier:** *Pluk-06* (Vælg det dobbelte plustegn \[**++**\] i feltet for at udvide listen og vælg derefter *Pluk-06* - *Pluklokation 6*.)</span><span class="sxs-lookup"><span data-stu-id="3a57f-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="3a57f-229">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="3a57f-230">Konfigurer lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="3a57f-230">Set up location directives</span></span>

<span data-ttu-id="3a57f-231">Der skal oprettes mindst én lokationsvejledning, der understøtter allokeringspluk.</span><span class="sxs-lookup"><span data-stu-id="3a57f-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="3a57f-232">Brug procedurerne i dette afsnit til at oprette en ny *lokationsvejledning for genopfyldning* til allokeringspluk.</span><span class="sxs-lookup"><span data-stu-id="3a57f-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="3a57f-233">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3a57f-234">I den venstre rude skal du i feltet **Arbejdsordretype** vælge *Genopfyldning*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="3a57f-235">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3a57f-236">I overskriften for den nye lokationsvejledning skal du i feltet **Navn** angive *61 Allokeringspluk*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="3a57f-237">Konfigurere oversigtspanelet Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="3a57f-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="3a57f-238">I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="3a57f-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="3a57f-239">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="3a57f-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="3a57f-240">**Arbejdstype:** _Pluk_</span><span class="sxs-lookup"><span data-stu-id="3a57f-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="3a57f-241">**Lokation:** _6_</span><span class="sxs-lookup"><span data-stu-id="3a57f-241">**Site:** _6_</span></span>
    - <span data-ttu-id="3a57f-242">**Lagersted:** _61_</span><span class="sxs-lookup"><span data-stu-id="3a57f-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="3a57f-243">**Vejledningskode:** _Allokering_</span><span class="sxs-lookup"><span data-stu-id="3a57f-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="3a57f-244">Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="3a57f-245">Konfigurere oversigtspanelet Linjer</span><span class="sxs-lookup"><span data-stu-id="3a57f-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="3a57f-246">I oversigtspanelet **Linjer** skal du vælge **Ny** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="3a57f-247">Angiv følgende værdier på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-247">On the new line, set the following values.</span></span> <span data-ttu-id="3a57f-248">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="3a57f-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="3a57f-249">**Fra antal:** _0_</span><span class="sxs-lookup"><span data-stu-id="3a57f-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="3a57f-250">**Til antal:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="3a57f-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="3a57f-251">Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="3a57f-252">Konfigurere oversigtspanelet Handlinger i lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="3a57f-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="3a57f-253">Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="3a57f-254">Angiv følgende værdier på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-254">On the new line, set the following values.</span></span> <span data-ttu-id="3a57f-255">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="3a57f-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="3a57f-256">**Navn:** _Masse_</span><span class="sxs-lookup"><span data-stu-id="3a57f-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="3a57f-257">**Strategi:** _Ingen_</span><span class="sxs-lookup"><span data-stu-id="3a57f-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="3a57f-258">Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="3a57f-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="3a57f-259">Rediger forespørgslen</span><span class="sxs-lookup"><span data-stu-id="3a57f-259">Edit the query</span></span>

1. <span data-ttu-id="3a57f-260">Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="3a57f-261">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3a57f-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="3a57f-262">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-263">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="3a57f-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="3a57f-264">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="3a57f-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="3a57f-265">**Felt:** *Zone-id*</span><span class="sxs-lookup"><span data-stu-id="3a57f-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="3a57f-266">**Kriterier:** *Masse* (Vælg det dobbelte plustegn \[**++**\] i feltet for at udvide listen og vælg derefter *Masse*.)</span><span class="sxs-lookup"><span data-stu-id="3a57f-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="3a57f-267">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="3a57f-268">Scenario</span><span class="sxs-lookup"><span data-stu-id="3a57f-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="3a57f-269">Konfigurere scenariet</span><span class="sxs-lookup"><span data-stu-id="3a57f-269">Set up the scenario</span></span>

<span data-ttu-id="3a57f-270">I dette scenarie skal du bruge de indbyggede eksempeldata og oprette de poster, der er beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="3a57f-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="3a57f-271">Brug af USMF-eksempeldata</span><span class="sxs-lookup"><span data-stu-id="3a57f-271">Use the USMF sample data</span></span>

<span data-ttu-id="3a57f-272">Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="3a57f-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="3a57f-273">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="3a57f-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="3a57f-274">Oprette efterspørgsel</span><span class="sxs-lookup"><span data-stu-id="3a57f-274">Create demand</span></span>

<span data-ttu-id="3a57f-275">Udfør følgende trin for at oprette den efterspørgsel, du vil anvende allokering på.</span><span class="sxs-lookup"><span data-stu-id="3a57f-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="3a57f-276">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="3a57f-277">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3a57f-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3a57f-278">Gå til dialogboksen **Opret salgsordre**, og vælg **US-007** i feltet _Debitorkonto_.</span><span class="sxs-lookup"><span data-stu-id="3a57f-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="3a57f-279">Vælg _61_ i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="3a57f-280">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-280">Select **OK**.</span></span>
1. <span data-ttu-id="3a57f-281">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="3a57f-281">The new sales order is opened.</span></span> <span data-ttu-id="3a57f-282">Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3a57f-283">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-284">**Vare:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="3a57f-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="3a57f-285">**Antal:** _20_</span><span class="sxs-lookup"><span data-stu-id="3a57f-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="3a57f-286">Vælg **Tilføj linje** for at tilføje en ny linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="3a57f-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="3a57f-287">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="3a57f-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="3a57f-288">**Antal:** _8_</span><span class="sxs-lookup"><span data-stu-id="3a57f-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="3a57f-289">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-289">Select **Save**.</span></span>
1. <span data-ttu-id="3a57f-290">Vælg **Ny** for at oprette en anden salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3a57f-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="3a57f-291">Gå til dialogboksen **Opret salgsordre**, og vælg **US-008** i feltet _Debitorkonto_.</span><span class="sxs-lookup"><span data-stu-id="3a57f-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="3a57f-292">Vælg _61_ i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="3a57f-293">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="3a57f-293">The new sales order is opened.</span></span> <span data-ttu-id="3a57f-294">Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3a57f-295">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="3a57f-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="3a57f-296">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="3a57f-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="3a57f-297">**Antal:** _1_</span><span class="sxs-lookup"><span data-stu-id="3a57f-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="3a57f-298">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="3a57f-299">Gennemgå et typisk allokeringsscenarie</span><span class="sxs-lookup"><span data-stu-id="3a57f-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="3a57f-300">Når alle de nødvendige elementer er på plads, som beskrevet i forrige afsnit, er du klar til at afprøve funktionen ved at gå gennem hver enkelt øvelse i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="3a57f-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="3a57f-301">Generér behov</span><span class="sxs-lookup"><span data-stu-id="3a57f-301">Generate demand</span></span>

1. <span data-ttu-id="3a57f-302">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Allokeringsskabeloner**, og vælg den allokeringsskabelon, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="3a57f-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="3a57f-303">Vælg **Opret efterspørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3a57f-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="3a57f-304">Denne kommando evaluerer al efterspørgsel, der findes i systemet, og som svarer til allokeringsskabelonforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="3a57f-305">Den samlede efterspørgsel i alle ordrer konsolideres derefter til én linje pr. antal/måleenhed.</span><span class="sxs-lookup"><span data-stu-id="3a57f-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="3a57f-306">Der vises en orienterende meddelelse, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3a57f-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="3a57f-307">Allokeringsbehov</span><span class="sxs-lookup"><span data-stu-id="3a57f-307">Slotting demand</span></span>

<span data-ttu-id="3a57f-308">*Allokeringsefterspørgslen* viser resultater af efterspørgselsoprettelsen baseret på konfigurationen af allokeringsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="3a57f-309">Vælg **Allokeringsefterspørgsel** i handlingsruden for at få vist resultaterne fra kommandoen **Opret efterspørgsel**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="3a57f-310">Linjerne i allokeringsbehovet kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="3a57f-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="3a57f-311">Du kan slette en linje, tilføje en ny linje eller redigere linjedetaljerne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="3a57f-312">Du kan redigere efterspørgslen manuelt, eller du kan importere den fra et eksternt system ved hjælp af datastyring.</span><span class="sxs-lookup"><span data-stu-id="3a57f-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="3a57f-313">Uanset hvad der er i allokeringsefterspørgslen bruges det i næste trin, uanset hvor den kommer fra.</span><span class="sxs-lookup"><span data-stu-id="3a57f-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="3a57f-314">Find behov</span><span class="sxs-lookup"><span data-stu-id="3a57f-314">Locate demand</span></span>

<span data-ttu-id="3a57f-315">Når efterspørgslen er oprettet, skal du bruge kommandoen **Find efterspørgsel** til at oprette *allokeringsplanen*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="3a57f-316">Vælg **Find efterspørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3a57f-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="3a57f-317">Allokeringsprocessen kører.</span><span class="sxs-lookup"><span data-stu-id="3a57f-317">The slotting process runs.</span></span> <span data-ttu-id="3a57f-318">Der vises en orienterende meddelelse, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3a57f-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="3a57f-319">Allokeringsplan</span><span class="sxs-lookup"><span data-stu-id="3a57f-319">Slotting plan</span></span>

<span data-ttu-id="3a57f-320">Allokeringsplan viser den lokation, som hver vare/hvert antal er tildelt til, om der er brugt overløb, om at der er oprettet et arbejde, og hvilken skabelonlinje der blev brugt.</span><span class="sxs-lookup"><span data-stu-id="3a57f-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="3a57f-321">**Alle efterspørgsler, der ikke kunne allokeres, fremhæves med rødt.**</span><span class="sxs-lookup"><span data-stu-id="3a57f-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="3a57f-322">I handlingsruden skal du vælge **Allokeringsplan** for at få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="3a57f-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="3a57f-323">Oprette genopfyldning</span><span class="sxs-lookup"><span data-stu-id="3a57f-323">Create replenishment</span></span>

<span data-ttu-id="3a57f-324">Når allokeringsplanen er blevet oprettet, skal du oprette et *genopfyldningsarbejde* baseret på planen.</span><span class="sxs-lookup"><span data-stu-id="3a57f-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="3a57f-325">Vælg **Kør genopfyldning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3a57f-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="3a57f-326">Der vises en orienterende meddelelse, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3a57f-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="3a57f-327">Denne meddelelse angiver det antal overskrifter, der er oprettet for arbejdsopbygnings-id'et.</span><span class="sxs-lookup"><span data-stu-id="3a57f-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="3a57f-328">Lokationsvejledninger, der bruges, identificeres ud fra den vejledningskode, der er angivet på hver skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="3a57f-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="3a57f-329">Tip!</span><span class="sxs-lookup"><span data-stu-id="3a57f-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="3a57f-330">Konfigurere automatisk allokering</span><span class="sxs-lookup"><span data-stu-id="3a57f-330">Set up automatic slotting</span></span>

<span data-ttu-id="3a57f-331">Når alle de påkrævede elementer er på plads, kan du konfigurere, at allokerings skal køre automatisk, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3a57f-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="3a57f-332">Gå til **Lokationsstyring \> Genopfyldning \> Kør allokering**.</span><span class="sxs-lookup"><span data-stu-id="3a57f-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="3a57f-333">Angiv de allokeringstrin, der skal køres.</span><span class="sxs-lookup"><span data-stu-id="3a57f-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="3a57f-334">Markér ét eller flere af følgende allokeringstrin:</span><span class="sxs-lookup"><span data-stu-id="3a57f-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="3a57f-335">Generér behov</span><span class="sxs-lookup"><span data-stu-id="3a57f-335">Generate demand</span></span>
    - <span data-ttu-id="3a57f-336">Find behov</span><span class="sxs-lookup"><span data-stu-id="3a57f-336">Locate demand</span></span>
    - <span data-ttu-id="3a57f-337">Opret genopfyldningsarbejde</span><span class="sxs-lookup"><span data-stu-id="3a57f-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a57f-338">Allokeringstrinnene er progressive.</span><span class="sxs-lookup"><span data-stu-id="3a57f-338">The slotting steps are progressive.</span></span> <span data-ttu-id="3a57f-339">Hvis du vil vælge *Find efterspørgsel*, skal du først vælge *Opret efterspørgsel*.</span><span class="sxs-lookup"><span data-stu-id="3a57f-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="3a57f-340">Angiv den allokeringsskabelon, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="3a57f-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="3a57f-341">Angiv, at gentagelsen skal køres automatisk, hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="3a57f-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="3a57f-342">Med hensyn til øvelserne i scenariet skal du **ikke** konfigurere automatisk allokering.</span><span class="sxs-lookup"><span data-stu-id="3a57f-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
