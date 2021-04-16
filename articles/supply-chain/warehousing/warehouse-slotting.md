---
title: Lagerstedsallokering
description: Dette emne indeholder oplysninger om lagerstedsallokering. Lagerstedsallokering gør det muligt at konsolidere efterspørgsel efter vare og måleenhed fra ordrer, der har statussen bestilt, reserveret eller frigivet. Den gør det lettere for lagerchefer at planlægge pluklokationer på en intelligent måde, før de frigiver ordrerne til lageret og opretter plukarbejde.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0dd1f42b7bb337ccb65b7e4bdd9d307d074ae0d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838148"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="b2740-105">Lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="b2740-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2740-106">Der er flere tilgængelige funktioner for lagerstedsallokering, som gør det lettere for lagerchefer at planlægge pluklokationer på en intelligent måde, før de frigiver ordrerne til lagerstedet og opretter plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="b2740-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="b2740-107">Funktionen *Lagerstedsallokering* gør det muligt at konsolidere efterspørgsel efter vare og måleenhed fra ordrer, der har statussen *Bestilt*, *Reserveret* eller *Frigivet*.</span><span class="sxs-lookup"><span data-stu-id="b2740-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="b2740-108">Genereret efterspørgsel kan derefter anvendes på lokationer, der skal bruges til plukning, baseret på antal, enhed, fysiske dimensioner, faste lokationer mv.</span><span class="sxs-lookup"><span data-stu-id="b2740-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="b2740-109">Når allokeringsplanen er blevet oprettet, kan genopfyldningsarbejdet oprettes for at bringe den korrekte lagermængde til hver lokation.</span><span class="sxs-lookup"><span data-stu-id="b2740-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="b2740-110">Med funktionen *Lagerstedallokering for flytteordrer* kan lagerchefer genopfylde plukpladser baseret på efterspørgsel fra flytteordrer, der endnu ikke er frigivet til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b2740-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="b2740-111">Det sikrer, at plukpladser indeholder alle de varer, der kræves til flytteordrerne, når de er frigivet til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b2740-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="b2740-112">Denne funktion kræver, at du også aktiverer funktionen *Lagerstedsallokering*.</span><span class="sxs-lookup"><span data-stu-id="b2740-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="b2740-113">Funktionen *Forbedringer af lagerstedsallokering* tilføjer en indstilling for de skabelonlinjer, der bruges af funktionen *Lagerstedsallokering*.</span><span class="sxs-lookup"><span data-stu-id="b2740-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="b2740-114">Indstillingen gør det muligt for systemet at overveje den eksisterende disponible lagerbeholdning på en mållokation.</span><span class="sxs-lookup"><span data-stu-id="b2740-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="b2740-115">Derfor kan der genereres færre genopfyldninger for allokering.</span><span class="sxs-lookup"><span data-stu-id="b2740-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="b2740-116">Funktionen *Forbedringer af fordeling af lagerstedsallokering* kræver, at du også aktiverer funktionen *Lagerstedsallokering*.</span><span class="sxs-lookup"><span data-stu-id="b2740-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="b2740-117">Den kan evt. bruges sammen med funktionen *Lagerstedsallokering for flytteordrer*.</span><span class="sxs-lookup"><span data-stu-id="b2740-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="b2740-118">Aktivere funktioner til lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="b2740-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="b2740-119">Før du kan bruge disse funktioner, skal de være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="b2740-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="b2740-120">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for funktionerne og aktivere dem, hvis de skal bruges.</span><span class="sxs-lookup"><span data-stu-id="b2740-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="b2740-121">Aktivér følgende funktioner efter behov:</span><span class="sxs-lookup"><span data-stu-id="b2740-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="b2740-122">Brug af slotfunktion på lagersted</span><span class="sxs-lookup"><span data-stu-id="b2740-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="b2740-123">Lagerstedsallokering for flytteordrer</span><span class="sxs-lookup"><span data-stu-id="b2740-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b2740-124">Funktionen *Lagerstedsallokering* skal være aktiveret før denne funktion.</span><span class="sxs-lookup"><span data-stu-id="b2740-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="b2740-125">Forbedringer af fordeling af lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="b2740-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b2740-126">Funktionen *Lagerstedsallokering* skal være aktiveret før denne funktion.</span><span class="sxs-lookup"><span data-stu-id="b2740-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="b2740-127">Konfigurere lagerstedsallokering</span><span class="sxs-lookup"><span data-stu-id="b2740-127">Set up warehouse slotting</span></span>

<span data-ttu-id="b2740-128">Hvis du vil bruge lagerstedsallokering, skal du konfigurere følgende elementer i dit system:</span><span class="sxs-lookup"><span data-stu-id="b2740-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="b2740-129">Måleenhedsniveauer for allokering</span><span class="sxs-lookup"><span data-stu-id="b2740-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="b2740-130">Vejledningskoder</span><span class="sxs-lookup"><span data-stu-id="b2740-130">Directive codes</span></span>
- <span data-ttu-id="b2740-131">Allokeringsskabeloner</span><span class="sxs-lookup"><span data-stu-id="b2740-131">Slotting templates</span></span>
- <span data-ttu-id="b2740-132">Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="b2740-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="b2740-133">Oprette måleenhedsniveauer for allokering</span><span class="sxs-lookup"><span data-stu-id="b2740-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="b2740-134">Måleenhedsniveauerne gør det muligt at gruppere flere måleenheder med henblik på allokering.</span><span class="sxs-lookup"><span data-stu-id="b2740-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="b2740-135">Hvis der f.eks. plukkes flere størrelser af kasser fra det samme kasseplukområde, kan der oprettes ét niveau for alle størrelserne.</span><span class="sxs-lookup"><span data-stu-id="b2740-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="b2740-136">**Der skal oprettes en linje for hver måleenhed, der skal være en del af niveauet.**</span><span class="sxs-lookup"><span data-stu-id="b2740-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="b2740-137">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Måleenhedsniveauer til allokering**.</span><span class="sxs-lookup"><span data-stu-id="b2740-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="b2740-138">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b2740-138">Select **New**.</span></span>
1. <span data-ttu-id="b2740-139">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="b2740-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="b2740-140">**Måleenhedsniveau:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="b2740-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="b2740-141">**Beskrivelse:** *Hver kassepalle*</span><span class="sxs-lookup"><span data-stu-id="b2740-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="b2740-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b2740-142">Select **Save**.</span></span>
1. <span data-ttu-id="b2740-143">Gå til oversigtspanelet **Måleenheder**, og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b2740-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2740-144">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-145">**Enhed:** *Kasse*</span><span class="sxs-lookup"><span data-stu-id="b2740-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="b2740-146">**Beskrivelse:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="b2740-147">Det udfyldes automatisk, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="b2740-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="b2740-148">**Enhedsklasse:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="b2740-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="b2740-149">Vælg **Ny** for at føje en anden linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b2740-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="b2740-150">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-151">**Enhed:** *Styk*</span><span class="sxs-lookup"><span data-stu-id="b2740-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="b2740-152">**Beskrivelse:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="b2740-153">Det udfyldes automatisk, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="b2740-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="b2740-154">**Enhedsklasse:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="b2740-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="b2740-155">Vælg **Ny** for at føje en tredje linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b2740-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="b2740-156">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-157">**Enhed:** *PL*</span><span class="sxs-lookup"><span data-stu-id="b2740-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="b2740-158">**Beskrivelse:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="b2740-159">Det udfyldes automatisk, når du gemmer ændringerne.</span><span class="sxs-lookup"><span data-stu-id="b2740-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="b2740-160">**Enhedsklasse:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="b2740-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="b2740-161">Vælg **Gem** for at gemme niveauet.</span><span class="sxs-lookup"><span data-stu-id="b2740-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="b2740-162">Oprette en vejledningskode til allokering</span><span class="sxs-lookup"><span data-stu-id="b2740-162">Create a directive code for slotting</span></span>

<span data-ttu-id="b2740-163">Du skal vælge den vejledningskode, der skal knyttes til en skabelon.</span><span class="sxs-lookup"><span data-stu-id="b2740-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="b2740-164">Gå til **Lokationsstyring \> Opsætning \> Vejledningskoder**.</span><span class="sxs-lookup"><span data-stu-id="b2740-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="b2740-165">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b2740-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2740-166">I feltet **Vejledningskode** skal du angive *Allokering*.</span><span class="sxs-lookup"><span data-stu-id="b2740-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="b2740-167">I feltet **Vejledningsbeskrivelse** skal du angive *Allokering*.</span><span class="sxs-lookup"><span data-stu-id="b2740-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="b2740-168">Konfigurere allokeringsskabeloner</span><span class="sxs-lookup"><span data-stu-id="b2740-168">Set up slotting templates</span></span>

<span data-ttu-id="b2740-169">Hver allokeringsskabelon styrer, hvordan lager tilknyttes lokationer for et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="b2740-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="b2740-170">Hver skabelon skal indeholde en linje for hver allokeringsspecifikation.</span><span class="sxs-lookup"><span data-stu-id="b2740-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="b2740-171">Brug procedurerne i dette afsnit til at konfigurere allokeringsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="b2740-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="b2740-172">Gå til **Lagerstedsstyring \> Konfiguration \> Genopfyldning \> Allokeringsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="b2740-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="b2740-173">Vælg **Ny** for at oprette en skabelon.</span><span class="sxs-lookup"><span data-stu-id="b2740-173">Select **New** to create a template.</span></span>

<span data-ttu-id="b2740-174">Derefter skal du konfigurere skabelonhovedet, allokeringsspecifikationerne og lokationsvejledningerne som forklaret i følgende under afsnit.</span><span class="sxs-lookup"><span data-stu-id="b2740-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="b2740-175">Opsætningen af allokering af flytteordrer minder om opsætningen af allokering af salgsordrer, men feltet **Behovstype** er angivet til *Flytteordrer* i stedet for *Salgsordre*.</span><span class="sxs-lookup"><span data-stu-id="b2740-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="b2740-176">Oprette en overskrift til en allokeringsskabelon for salgsordre</span><span class="sxs-lookup"><span data-stu-id="b2740-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="b2740-177">Angiv følgende værdier i overskriften for skabelonen:</span><span class="sxs-lookup"><span data-stu-id="b2740-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="b2740-178">**Allokeringsskabelon:** _61_</span><span class="sxs-lookup"><span data-stu-id="b2740-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="b2740-179">**Beskrivelse:** _61_</span><span class="sxs-lookup"><span data-stu-id="b2740-179">**Description:** _61_</span></span>
    - <span data-ttu-id="b2740-180">**Efterspørgselstype:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="b2740-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="b2740-181">I øjeblikket er *Salgsordrer* og *Flytteordrer* de eneste efterspørgselstyper, der understøttes.</span><span class="sxs-lookup"><span data-stu-id="b2740-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="b2740-182">Du kan kun vælge *Flytteordrer*, hvis funktionen *Lagerstedsallokering for flytteordrer* er slået til.</span><span class="sxs-lookup"><span data-stu-id="b2740-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="b2740-183">**Efterspørgselsstrategi:** _Bestilt_</span><span class="sxs-lookup"><span data-stu-id="b2740-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="b2740-184">Følgende værdier er tilgængelige i dette felt:</span><span class="sxs-lookup"><span data-stu-id="b2740-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="b2740-185">**Bestilt** – det fuldt bestilte antal på salgsordren skal betragtes som efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="b2740-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="b2740-186">**Reserveret** – det er kun de salgsordrelinjemængder, der er reserveret (fysisk og bestilt), som skal betragtes som efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="b2740-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="b2740-187">**Frigivet** – Det frigivne antal skal betragtes som efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="b2740-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="b2740-188">**Lagersted:** _61_</span><span class="sxs-lookup"><span data-stu-id="b2740-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="b2740-189">**Tillad bølgeefterspørgsel at bruge ikke-reserverede antal:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="b2740-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="b2740-190">Du kan også angive en forespørgsel for at indsnævre omfanget af den efterspørgsel, der evalueres.</span><span class="sxs-lookup"><span data-stu-id="b2740-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="b2740-191">Konfigurere allokeringsspecifikationer for hver skabelon</span><span class="sxs-lookup"><span data-stu-id="b2740-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="b2740-192">For hver slagsordreskabelon, du opretter, skal du udføre disse trin for at tilføje en linje for hver allokeringsspecifikation.</span><span class="sxs-lookup"><span data-stu-id="b2740-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="b2740-193">Gå til oversigtspanelet **Detaljer om allokeringsskabelon**, og vælg **Ny** for at oprette en skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="b2740-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="b2740-194">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-195">**Sekvens:** _1_</span><span class="sxs-lookup"><span data-stu-id="b2740-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="b2740-196">**Beskrivelse:** _Fast lokation_</span><span class="sxs-lookup"><span data-stu-id="b2740-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="b2740-197">**Minimummængde:** _1_</span><span class="sxs-lookup"><span data-stu-id="b2740-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="b2740-198">Dette felt definerer det mindste efterspørgselsantal, der kræves til linjen.</span><span class="sxs-lookup"><span data-stu-id="b2740-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="b2740-199">**Maksimummængde:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="b2740-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="b2740-200">Dette felt definerer det maksimale efterspørgselsantal, der er gyldig til linjen.</span><span class="sxs-lookup"><span data-stu-id="b2740-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="b2740-201">**Enhed:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="b2740-202">Dette felt definerer den måleenhed, som minimum- og maksimumantallet refererer til.</span><span class="sxs-lookup"><span data-stu-id="b2740-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="b2740-203">**Måleenhedsniveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="b2740-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="b2740-204">Dette felt definerer måleenheden for efterspørgsel, der er gyldig til linjen.</span><span class="sxs-lookup"><span data-stu-id="b2740-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="b2740-205">(Få flere oplysninger i afsnittet i [Oprette måleenhedsniveauer for allokering](#unit-tiers) tidligere i dette emne.)</span><span class="sxs-lookup"><span data-stu-id="b2740-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="b2740-206">**Tildel allokeringskriterier:** _Overvej antal_</span><span class="sxs-lookup"><span data-stu-id="b2740-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="b2740-207">Følgende værdier er tilgængelige i dette felt:</span><span class="sxs-lookup"><span data-stu-id="b2740-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="b2740-208">**Antag tom** – dette system skal antage, at alle lokationer i plukområdet er tomme, og det skal ikke kontrollere disse lokationer med hensyn til lager.</span><span class="sxs-lookup"><span data-stu-id="b2740-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="b2740-209">**Overvej antal** – systemet skal kontrollere lokationerne i plukområdet for lager og skal springe lokationer over, der ikke er tomme.</span><span class="sxs-lookup"><span data-stu-id="b2740-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="b2740-210">**Overvej beholdningen** – Systemet skal kontrollere, om en bestemt lokation indeholder ikke-reserverede antal for varen på behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="b2740-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="b2740-211">Hvis antallet er stort nok til at opfylde mindst én enhed af behovslinjen, reduceres den genererede allokeringsplan med det disponible antal.</span><span class="sxs-lookup"><span data-stu-id="b2740-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="b2740-212">Hvis behovet f.eks. er 10 kasser, og én kasse er disponibel, vil det fundne behov være ni kasser.</span><span class="sxs-lookup"><span data-stu-id="b2740-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="b2740-213">Hvis behovet er 10 kasser, og én af hver er disponibel, vil det fundne behov være ti kasser.</span><span class="sxs-lookup"><span data-stu-id="b2740-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="b2740-214">Denne værdi er kun tilgængelig, når funktionen *Forbedringer af fordeling af lagerstedsallokering* er slået til.</span><span class="sxs-lookup"><span data-stu-id="b2740-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="b2740-215">**Vejledningskode:** _Allokering_</span><span class="sxs-lookup"><span data-stu-id="b2740-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="b2740-216">Dette felt definerer lokationsvejledningen, der bruges til at finde pluklokationen for genopfyldningsarbejdet.</span><span class="sxs-lookup"><span data-stu-id="b2740-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="b2740-217">**Overløbslokation:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="b2740-218">I dette felt defineres den lokation, som det lager, hvortil der lægges på lager, hvis der ikke kan findes en lokation for antallet, da linjen blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="b2740-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="b2740-219">**Tillad brug:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="b2740-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="b2740-220">Når denne indstilling er angivet til *Ja*, og hvis det ikke muligt allokere noget efterspørgsel, vil der blive oprettet bevægelsesarbejde for at fjerne lager fra lokationer, hvor der er lager, men hvor der ikke er sket nogen allokering.</span><span class="sxs-lookup"><span data-stu-id="b2740-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="b2740-221">Skabelonen køres derefter igen.</span><span class="sxs-lookup"><span data-stu-id="b2740-221">The template is then run again.</span></span> <span data-ttu-id="b2740-222">Denne gang ignoreres lageret på lokationerne.</span><span class="sxs-lookup"><span data-stu-id="b2740-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="b2740-223">Denne funktion fungerer bedst, når feltet **Tildel allokeringskriterier** er indstillet til at _Overvej antal_.</span><span class="sxs-lookup"><span data-stu-id="b2740-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="b2740-224">**Brug af fast lokation:** _Kun faste lokationer til produktet_</span><span class="sxs-lookup"><span data-stu-id="b2740-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="b2740-225">Følgende værdier er tilgængelige i dette felt:</span><span class="sxs-lookup"><span data-stu-id="b2740-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="b2740-226">**Faste og ikke-faste lokationer** – systemet skal ikke være begrænset til kun at bruge faste lokationer.</span><span class="sxs-lookup"><span data-stu-id="b2740-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="b2740-227">**Kun faste lokationer til produktet** – systemet skal kun allokere til lokationer, der er faste lokationer for produktet.</span><span class="sxs-lookup"><span data-stu-id="b2740-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="b2740-228">**Kun faste lokationer til produktvarianten** – systemet skal kun allokere til lokationer, der er faste lokationer for produktvarianten.</span><span class="sxs-lookup"><span data-stu-id="b2740-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="b2740-229">Hvis allokeringsskabelonen indeholder mindst én linje, hvor feltet **Tildel allokeringskriterier** er angivet til *Overvej beholdning*, er afvigelser fra krav ikke længere tilladt for nogen af linjerne i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="b2740-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="b2740-230">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b2740-230">Select **Save**.</span></span>
1. <span data-ttu-id="b2740-231">Vælg **Ny** for at oprette en linje for anden skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="b2740-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="b2740-232">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-233">**Sekvens:** _2_</span><span class="sxs-lookup"><span data-stu-id="b2740-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="b2740-234">**Beskrivelse:** _Andet_</span><span class="sxs-lookup"><span data-stu-id="b2740-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="b2740-235">**Minimumantal:** _1_</span><span class="sxs-lookup"><span data-stu-id="b2740-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="b2740-236">**Maksimumantal:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="b2740-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="b2740-237">**Enhed:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2740-238">**Måleenhedsniveau:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="b2740-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="b2740-239">**Tildel allokeringskriterier:** _Overvej antal_</span><span class="sxs-lookup"><span data-stu-id="b2740-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="b2740-240">**Vejledningskode:** _Allokering_</span><span class="sxs-lookup"><span data-stu-id="b2740-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="b2740-241">**Overløbslokation:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="b2740-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="b2740-242">**Tillad brug:** _Ja_</span><span class="sxs-lookup"><span data-stu-id="b2740-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="b2740-243">**Brug faste lokationer:** _Faste og ikke-faste lokationer_</span><span class="sxs-lookup"><span data-stu-id="b2740-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="b2740-244">I forespørgslen til den anden linje skal du nu angive de kriterier, der bruges til at bestemme, hvilke lokationer efterspørgslen for den linje kan allokeres til.</span><span class="sxs-lookup"><span data-stu-id="b2740-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="b2740-245">Vælg den linje, hvor feltet **Rækkefølge** er angivet til *2*.</span><span class="sxs-lookup"><span data-stu-id="b2740-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="b2740-246">Vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="b2740-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="b2740-247">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b2740-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2740-248">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-249">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="b2740-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b2740-250">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="b2740-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b2740-251">**Felt:** *Lokationsprofil-id*</span><span class="sxs-lookup"><span data-stu-id="b2740-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="b2740-252">**Kriterier:** *Pluk-06* (Vælg det dobbelte plustegn \[**++**\] i feltet for at udvide listen og vælg derefter *Pluk-06* - *Pluklokation 6*.)</span><span class="sxs-lookup"><span data-stu-id="b2740-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="b2740-253">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2740-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="b2740-254">Konfigurer lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="b2740-254">Set up location directives</span></span>

<span data-ttu-id="b2740-255">Der skal oprettes mindst én lokationsvejledning, der understøtter allokeringspluk.</span><span class="sxs-lookup"><span data-stu-id="b2740-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="b2740-256">Brug procedurerne i dette afsnit til at oprette en ny *lokationsvejledning for genopfyldning* til allokeringspluk.</span><span class="sxs-lookup"><span data-stu-id="b2740-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="b2740-257">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="b2740-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b2740-258">I den venstre rude skal du i feltet **Arbejdsordretype** vælge *Genopfyldning*.</span><span class="sxs-lookup"><span data-stu-id="b2740-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="b2740-259">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b2740-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b2740-260">I overskriften for den nye lokationsvejledning skal du i feltet **Navn** angive *61 Allokeringspluk*.</span><span class="sxs-lookup"><span data-stu-id="b2740-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="b2740-261">Feltet **Løbenummer** accepterer standardværdien.</span><span class="sxs-lookup"><span data-stu-id="b2740-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="b2740-262">Konfigurere oversigtspanelet Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="b2740-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="b2740-263">I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="b2740-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="b2740-264">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="b2740-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b2740-265">**Arbejdstype:** _Pluk_</span><span class="sxs-lookup"><span data-stu-id="b2740-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="b2740-266">**Lokation:** _6_</span><span class="sxs-lookup"><span data-stu-id="b2740-266">**Site:** _6_</span></span>
    - <span data-ttu-id="b2740-267">**Lagersted:** _61_</span><span class="sxs-lookup"><span data-stu-id="b2740-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="b2740-268">**Vejledningskode:** _Allokering_</span><span class="sxs-lookup"><span data-stu-id="b2740-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="b2740-269">Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="b2740-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="b2740-270">Konfigurere oversigtspanelet Linjer</span><span class="sxs-lookup"><span data-stu-id="b2740-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="b2740-271">I oversigtspanelet **Linjer** skal du vælge **Ny** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="b2740-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="b2740-272">Angiv følgende værdier på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="b2740-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="b2740-273">**Fra antal:** _0_</span><span class="sxs-lookup"><span data-stu-id="b2740-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="b2740-274">**Til antal:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="b2740-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="b2740-275">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="b2740-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="b2740-276">Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="b2740-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="b2740-277">Konfigurere oversigtspanelet Handlinger i lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="b2740-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="b2740-278">Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="b2740-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="b2740-279">Angiv følgende værdier på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="b2740-279">On the new line, set the following values.</span></span> <span data-ttu-id="b2740-280">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="b2740-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b2740-281">**Løbenummer:** Accepter standardværdien.</span><span class="sxs-lookup"><span data-stu-id="b2740-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b2740-282">**Navn:** _Masse_</span><span class="sxs-lookup"><span data-stu-id="b2740-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="b2740-283">**Strategi:** _Ingen_</span><span class="sxs-lookup"><span data-stu-id="b2740-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="b2740-284">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="b2740-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="b2740-285">Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="b2740-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="b2740-286">Rediger forespørgslen</span><span class="sxs-lookup"><span data-stu-id="b2740-286">Edit the query</span></span>

1. <span data-ttu-id="b2740-287">Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="b2740-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="b2740-288">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b2740-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b2740-289">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b2740-290">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="b2740-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b2740-291">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="b2740-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b2740-292">**Felt:** *Zone-id*</span><span class="sxs-lookup"><span data-stu-id="b2740-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="b2740-293">**Kriterier:** *Masse* (Vælg det dobbelte plustegn \[**++**\] i feltet for at udvide listen og vælg derefter *Masse*.)</span><span class="sxs-lookup"><span data-stu-id="b2740-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="b2740-294">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2740-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b2740-295">Scenario</span><span class="sxs-lookup"><span data-stu-id="b2740-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="b2740-296">Konfigurere scenariet</span><span class="sxs-lookup"><span data-stu-id="b2740-296">Set up the scenario</span></span>

<span data-ttu-id="b2740-297">I dette scenarie skal du bruge de indbyggede eksempeldata og oprette de poster, der er beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="b2740-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="b2740-298">Brug af USMF-eksempeldata</span><span class="sxs-lookup"><span data-stu-id="b2740-298">Use the USMF sample data</span></span>

<span data-ttu-id="b2740-299">Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="b2740-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b2740-300">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="b2740-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="b2740-301">Oprette efterspørgsel</span><span class="sxs-lookup"><span data-stu-id="b2740-301">Create demand</span></span>

<span data-ttu-id="b2740-302">Udfør følgende trin for at oprette den efterspørgsel, du vil anvende allokering på.</span><span class="sxs-lookup"><span data-stu-id="b2740-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="b2740-303">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b2740-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="b2740-304">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="b2740-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b2740-305">Gå til dialogboksen **Opret salgsordre**, og vælg **US-007** i feltet _Debitorkonto_.</span><span class="sxs-lookup"><span data-stu-id="b2740-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="b2740-306">Vælg _61_ i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="b2740-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="b2740-307">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2740-307">Select **OK**.</span></span>
1. <span data-ttu-id="b2740-308">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="b2740-308">The new sales order is opened.</span></span> <span data-ttu-id="b2740-309">Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="b2740-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2740-310">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2740-311">**Vare:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="b2740-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="b2740-312">**Antal:** _20_</span><span class="sxs-lookup"><span data-stu-id="b2740-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="b2740-313">Vælg **Tilføj linje** for at tilføje en ny linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b2740-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="b2740-314">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="b2740-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="b2740-315">**Antal:** _8_</span><span class="sxs-lookup"><span data-stu-id="b2740-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="b2740-316">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b2740-316">Select **Save**.</span></span>
1. <span data-ttu-id="b2740-317">Vælg **Ny** for at oprette en anden salgsordre.</span><span class="sxs-lookup"><span data-stu-id="b2740-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="b2740-318">Gå til dialogboksen **Opret salgsordre**, og vælg **US-008** i feltet _Debitorkonto_.</span><span class="sxs-lookup"><span data-stu-id="b2740-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="b2740-319">Vælg _61_ i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="b2740-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="b2740-320">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="b2740-320">The new sales order is opened.</span></span> <span data-ttu-id="b2740-321">Den indeholder en tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="b2740-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b2740-322">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="b2740-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="b2740-323">**Vare:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="b2740-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="b2740-324">**Antal:** _1_</span><span class="sxs-lookup"><span data-stu-id="b2740-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="b2740-325">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b2740-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="b2740-326">Gennemgå et typisk allokeringsscenarie</span><span class="sxs-lookup"><span data-stu-id="b2740-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="b2740-327">Når alle de nødvendige elementer er på plads, som beskrevet i forrige afsnit, er du klar til at afprøve funktionen ved at gå gennem hver enkelt øvelse i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="b2740-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="b2740-328">Generér behov</span><span class="sxs-lookup"><span data-stu-id="b2740-328">Generate demand</span></span>

1. <span data-ttu-id="b2740-329">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Allokeringsskabeloner**, og vælg den allokeringsskabelon, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="b2740-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="b2740-330">Vælg **Opret efterspørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b2740-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="b2740-331">Denne kommando evaluerer al efterspørgsel, der findes i systemet, og som svarer til allokeringsskabelonforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="b2740-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="b2740-332">Den samlede efterspørgsel i alle ordrer konsolideres derefter til én linje pr. antal/måleenhed.</span><span class="sxs-lookup"><span data-stu-id="b2740-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="b2740-333">Der vises en orienterende meddelelse, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="b2740-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="b2740-334">Allokeringsbehov</span><span class="sxs-lookup"><span data-stu-id="b2740-334">Slotting demand</span></span>

<span data-ttu-id="b2740-335">*Allokeringsefterspørgslen* viser resultater af efterspørgselsoprettelsen baseret på konfigurationen af allokeringsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="b2740-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="b2740-336">Vælg **Allokeringsefterspørgsel** i handlingsruden for at få vist resultaterne fra kommandoen **Opret efterspørgsel**.</span><span class="sxs-lookup"><span data-stu-id="b2740-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="b2740-337">Linjerne i allokeringsbehovet kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="b2740-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="b2740-338">Du kan slette en linje, tilføje en ny linje eller redigere linjedetaljerne.</span><span class="sxs-lookup"><span data-stu-id="b2740-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="b2740-339">Du kan redigere efterspørgslen manuelt, eller du kan importere den fra et eksternt system ved hjælp af datastyring.</span><span class="sxs-lookup"><span data-stu-id="b2740-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="b2740-340">Uanset hvad der er i allokeringsefterspørgslen bruges det i næste trin, uanset hvor den kommer fra.</span><span class="sxs-lookup"><span data-stu-id="b2740-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="b2740-341">Find behov</span><span class="sxs-lookup"><span data-stu-id="b2740-341">Locate demand</span></span>

<span data-ttu-id="b2740-342">Når efterspørgslen er oprettet, skal du bruge kommandoen **Find efterspørgsel** til at oprette *allokeringsplanen*.</span><span class="sxs-lookup"><span data-stu-id="b2740-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="b2740-343">Vælg **Find efterspørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b2740-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="b2740-344">Allokeringsprocessen kører.</span><span class="sxs-lookup"><span data-stu-id="b2740-344">The slotting process runs.</span></span> <span data-ttu-id="b2740-345">Der vises en orienterende meddelelse, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="b2740-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="b2740-346">Allokeringsplan</span><span class="sxs-lookup"><span data-stu-id="b2740-346">Slotting plan</span></span>

<span data-ttu-id="b2740-347">Allokeringsplan viser den lokation, som hver vare/hvert antal er tildelt til, om der er brugt overløb, om at der er oprettet et arbejde, og hvilken skabelonlinje der blev brugt.</span><span class="sxs-lookup"><span data-stu-id="b2740-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="b2740-348">*Alle efterspørgsler, der ikke kunne allokeres, fremhæves med rødt.*</span><span class="sxs-lookup"><span data-stu-id="b2740-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="b2740-349">I handlingsruden skal du vælge **Allokeringsplan** for at få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="b2740-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="b2740-350">Processerne **Generér efterspørgsel**, **Find behov** og **Kør genopfyldning** kører nu i en sandkasse.</span><span class="sxs-lookup"><span data-stu-id="b2740-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="b2740-351">(Disse processer er tilgængelige i handlingsruden på siden **Allokeringsskabeloner**).</span><span class="sxs-lookup"><span data-stu-id="b2740-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="b2740-352">Processerne **Generér behov**, **Find behov** og **Kør genopfyldning** har en lås for at sikre, at de ikke kan udløses samtidig.</span><span class="sxs-lookup"><span data-stu-id="b2740-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="b2740-353">Ellers kunne de data, der bruges, blive slettet.</span><span class="sxs-lookup"><span data-stu-id="b2740-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="b2740-354">Processerne **Generér behov** og **Find behov** viser en advarsel, hvis kørslen ikke genererede poster, eller hvis posterne mangler oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b2740-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="b2740-355">Når du vælger **Allokeringsplan**, har siden ikke knappen **Ny**, **Rediger** eller **Slet** i handlingsruden, fordi datakilden ikke kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="b2740-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="b2740-356">Når du vælger **Kør genopfyldning**, validerer systemet de valgte allokeringsskabeloner og processer.</span><span class="sxs-lookup"><span data-stu-id="b2740-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="b2740-357">Oprette genopfyldning</span><span class="sxs-lookup"><span data-stu-id="b2740-357">Create replenishment</span></span>

<span data-ttu-id="b2740-358">Når allokeringsplanen er blevet oprettet, skal du oprette et *genopfyldningsarbejde* baseret på planen.</span><span class="sxs-lookup"><span data-stu-id="b2740-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="b2740-359">Vælg **Kør genopfyldning** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b2740-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="b2740-360">Der vises en orienterende meddelelse, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="b2740-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="b2740-361">Denne meddelelse angiver det antal overskrifter, der er oprettet for arbejdsopbygnings-id'et.</span><span class="sxs-lookup"><span data-stu-id="b2740-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="b2740-362">Lokationsvejledninger, der bruges, identificeres ud fra den vejledningskode, der er angivet på hver skabelonlinje.</span><span class="sxs-lookup"><span data-stu-id="b2740-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="b2740-363">Tip!</span><span class="sxs-lookup"><span data-stu-id="b2740-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="b2740-364">Konfigurere automatisk allokering</span><span class="sxs-lookup"><span data-stu-id="b2740-364">Set up automatic slotting</span></span>

<span data-ttu-id="b2740-365">Når alle de påkrævede elementer er på plads, kan du konfigurere, at allokerings skal køre automatisk, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b2740-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="b2740-366">Gå til **Lokationsstyring \> Genopfyldning \> Kør allokering**.</span><span class="sxs-lookup"><span data-stu-id="b2740-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="b2740-367">Angiv de allokeringstrin, der skal køres.</span><span class="sxs-lookup"><span data-stu-id="b2740-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="b2740-368">Markér ét eller flere af følgende allokeringstrin:</span><span class="sxs-lookup"><span data-stu-id="b2740-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="b2740-369">Generér behov</span><span class="sxs-lookup"><span data-stu-id="b2740-369">Generate demand</span></span>
    - <span data-ttu-id="b2740-370">Find behov</span><span class="sxs-lookup"><span data-stu-id="b2740-370">Locate demand</span></span>
    - <span data-ttu-id="b2740-371">Opret genopfyldningsarbejde</span><span class="sxs-lookup"><span data-stu-id="b2740-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2740-372">Allokeringstrinnene er progressive.</span><span class="sxs-lookup"><span data-stu-id="b2740-372">The slotting steps are progressive.</span></span> <span data-ttu-id="b2740-373">Hvis du vil vælge *Find efterspørgsel*, skal du først vælge *Opret efterspørgsel*.</span><span class="sxs-lookup"><span data-stu-id="b2740-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="b2740-374">Angiv den allokeringsskabelon, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="b2740-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="b2740-375">Angiv, at gentagelsen skal køres automatisk, hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="b2740-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="b2740-376">Med hensyn til øvelserne i scenariet skal du **ikke** konfigurere automatisk allokering.</span><span class="sxs-lookup"><span data-stu-id="b2740-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]