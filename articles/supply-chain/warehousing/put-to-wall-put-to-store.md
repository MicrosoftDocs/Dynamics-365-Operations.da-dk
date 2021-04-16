---
title: Sæt til væg – læg til butik
description: Dette emne indeholder oplysninger om funktionaliteten Sæt til væg – læg til butik. Denne funktionalitet giver dig mulighed for at håndtere scenarier, hvor du skal konsolidere et produkt til et midlertidig lagring til forpakning, der er baseret på konfigurerbare kriterier. Det er med til at reducere pluktiden, da det giver mulighed for at plukke til en enkelt destinations nummerplade og kan bruge flere læg på lager-placeringer end klyngeplukning.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cf34a61d0b3f784b5a424473588d05bf8703635c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823281"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="80803-105">Sæt til væg – læg til butik</span><span class="sxs-lookup"><span data-stu-id="80803-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80803-106">Funktionaliteten *Sæt til væg – læg til butik* giver dig mulighed for at håndtere scenarier, hvor du skal konsolidere et produkt til midlertidig lagring til forpakning, der er baseret på konfigurerbare kriterier.</span><span class="sxs-lookup"><span data-stu-id="80803-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="80803-107">Da denne funktionalitet giver mulighed for at plukke til en enkelt destinations nummerplade og bruge flere læg på-lager-positioner end klyngepluk, vil firmaer, der afsender til butikker eller håndterer små varer, drage fordel af en formindsket plukperiode.</span><span class="sxs-lookup"><span data-stu-id="80803-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="80803-108">Arbejdsgangen i denne funktion dirigerer et direkte plukket produkt til en sorteringslokation til distribution i forskellige typer containere.</span><span class="sxs-lookup"><span data-stu-id="80803-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="80803-109">Generelt indeholder hver enkelt sorteringslokation flere sorteringspositioner.</span><span class="sxs-lookup"><span data-stu-id="80803-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="80803-110">Hver enkelt sorteringsposition tildeles efter de kriterier, der er angivet i forretningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="80803-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="80803-111">Typiske kriterier er den endelige destination, forsendelse eller last.</span><span class="sxs-lookup"><span data-stu-id="80803-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="80803-112">Når et produkt ankommer, fordeles det på hver enkelt sorteringsposition, baseret på det antal, der er knyttet til ordren, destinationen, forsendelsen eller lasten.</span><span class="sxs-lookup"><span data-stu-id="80803-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="80803-113">Når en container er fuld eller fuldført, flyttes den til en midlertidig lagringslokation eller et afsendelsessted, hvor der kan håndteres yderligere, afhængigt af forretningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="80803-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="80803-114">Denne lagerfunktion kaldes også for andre ting, f. eks. læg-på-let og brud åbnes.</span><span class="sxs-lookup"><span data-stu-id="80803-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="80803-115">Aktivere funktionen for udgående sortering</span><span class="sxs-lookup"><span data-stu-id="80803-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="80803-116">Før du kan bruge funktionaliteten *Sæt til væg – læg til butik*, skal funktionen *Udgående sortering* være aktiveret i systemet.</span><span class="sxs-lookup"><span data-stu-id="80803-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="80803-117">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="80803-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="80803-118">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="80803-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="80803-119">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="80803-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="80803-120">**Funktionsnavn:** *Udgående sortering*</span><span class="sxs-lookup"><span data-stu-id="80803-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="80803-121">Funktionen *Udgående sortering* kan bruges sammen med funktionen *Bølgetrinskode for hele organisationen*, hvis den er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="80803-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="80803-122">Du skal også aktivere denne funktion, hvis du vil bruge foruddefinerede koder, der er oprettet i bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="80803-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="80803-123">I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="80803-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="80803-124">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="80803-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="80803-125">**Funktionsnavn:** *Organization wide wave step code*</span><span class="sxs-lookup"><span data-stu-id="80803-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="80803-126">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="80803-126">Setup</span></span>

<span data-ttu-id="80803-127">I denne demonstration bruges standard-Contoso-data og lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="80803-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="80803-128">Nogle tilføjelser, der registreres senere, bruges også.</span><span class="sxs-lookup"><span data-stu-id="80803-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="80803-129">Lokationstype</span><span class="sxs-lookup"><span data-stu-id="80803-129">Location type</span></span>

1. <span data-ttu-id="80803-130">Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationstyper**.</span><span class="sxs-lookup"><span data-stu-id="80803-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="80803-131">Vælg **Ny** i handlingsruden for at oprette en lokationstype til sortering.</span><span class="sxs-lookup"><span data-stu-id="80803-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="80803-132">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-132">Set the following values:</span></span>

    - <span data-ttu-id="80803-133">**Lokationstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="80803-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="80803-134">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="80803-135">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="80803-136">Parametre til lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="80803-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="80803-137">Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.</span><span class="sxs-lookup"><span data-stu-id="80803-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="80803-138">Gå til fanen **Generelt**, og angiv feltet **Sorteringslokationstype** til **SORTER** i oversigtspanelet *Lokationstyper*.</span><span class="sxs-lookup"><span data-stu-id="80803-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="80803-139">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="80803-140">Lokationsprofil</span><span class="sxs-lookup"><span data-stu-id="80803-140">Location profile</span></span>

1. <span data-ttu-id="80803-141">Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="80803-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="80803-142">Vælg **Ny** i handlingsruden for at oprette en lokationsprofil for sorteringslokationen.</span><span class="sxs-lookup"><span data-stu-id="80803-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="80803-143">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="80803-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="80803-144">**Lokationsprofil-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="80803-145">**Navn:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="80803-146">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="80803-147">**Lokationsformat:** *PAKKE*</span><span class="sxs-lookup"><span data-stu-id="80803-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="80803-148">**Lokationstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="80803-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="80803-149">**Brug sporing af nummerplader:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="80803-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="80803-150">**Tillad blandede varer:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="80803-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="80803-151">**Tillad blandede lagerstatusser:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="80803-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="80803-152">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="80803-153">Lokationer</span><span class="sxs-lookup"><span data-stu-id="80803-153">Locations</span></span>

1. <span data-ttu-id="80803-154">Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**.</span><span class="sxs-lookup"><span data-stu-id="80803-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="80803-155">Ryd afkrydsningsfeltet **Generér kontrolcifre for lokation**.</span><span class="sxs-lookup"><span data-stu-id="80803-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="80803-156">I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="80803-157">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="80803-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="80803-158">**Lokation:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="80803-159">**Lokationsprofil-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="80803-160">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="80803-161">Pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="80803-161">Packing profiles</span></span>

1. <span data-ttu-id="80803-162">Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Pakningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="80803-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="80803-163">I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="80803-164">**Pakkeprofil-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="80803-165">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="80803-166">**Politik for containerpakning:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="80803-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="80803-167">**Container-id-tilstand:** *Auto*</span><span class="sxs-lookup"><span data-stu-id="80803-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="80803-168">**Containertype:** *PALLE 48 X 48*</span><span class="sxs-lookup"><span data-stu-id="80803-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="80803-169">**Opret automatisk container ved containerlukning:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="80803-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="80803-170">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="80803-171">Bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="80803-171">Wave step codes</span></span>

<span data-ttu-id="80803-172">Hvis du har aktiveret funktionen *Bølgetrinskode for hele organisationen*, skal du konfigurere følgende kode.</span><span class="sxs-lookup"><span data-stu-id="80803-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="80803-173">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinkoder**.</span><span class="sxs-lookup"><span data-stu-id="80803-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="80803-174">I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="80803-175">**Kode for bølgetrin:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="80803-176">**Bølgetrinsbeskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="80803-177">**Bølgetrinstype:** *Sorteringsskabelon*</span><span class="sxs-lookup"><span data-stu-id="80803-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="80803-178">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="80803-179">Skabelon til udgående sortering</span><span class="sxs-lookup"><span data-stu-id="80803-179">Outbound sorting template</span></span>

<span data-ttu-id="80803-180">Sorteringsskabelonen styrer, om der oprettes sorteringspositioner, hvilke kriterier der bruges, og andre attributter for sorteringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="80803-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="80803-181">Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Skabelon til udgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="80803-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="80803-182">Vælg **Ny** i handlingsruden for at oprette en sorteringsskabelon.</span><span class="sxs-lookup"><span data-stu-id="80803-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="80803-183">Angiv følgende værdier i hoveddelen for den nye skabelon:</span><span class="sxs-lookup"><span data-stu-id="80803-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="80803-184">**Id for skabelon til udgående sortering:** *Bølgesortering*</span><span class="sxs-lookup"><span data-stu-id="80803-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="80803-185">**Beskrivelse:** *Bølgesortering*</span><span class="sxs-lookup"><span data-stu-id="80803-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="80803-186">**Type af sorteringsskabelon:** *Bølgebehov*</span><span class="sxs-lookup"><span data-stu-id="80803-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="80803-187">Dette felt definerer den proces, som sorteringsskabelonen bruges til.</span><span class="sxs-lookup"><span data-stu-id="80803-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="80803-188">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="80803-188">The following values are available:</span></span>

        - <span data-ttu-id="80803-189">**Bølgebehov** – sorteringsskabelonen bruges til processen *Sæt til væg*.</span><span class="sxs-lookup"><span data-stu-id="80803-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="80803-190">Denne skabelontype bruges til at omgå pakkestationen og behandle lager direkte fra bølgen.</span><span class="sxs-lookup"><span data-stu-id="80803-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="80803-191">Du kan kun bruge denne type, hvis bølgeprocestypen **sortering** er inkluderet i bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="80803-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="80803-192">**Container** – sorteringsskabelonen bruges til processen *Palleopbygning efter pakning*.</span><span class="sxs-lookup"><span data-stu-id="80803-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="80803-193">Denne skabelontype bruges til at behandle containere, der er lukket på den pågældende pakkestation og skal sorteres på paller.</span><span class="sxs-lookup"><span data-stu-id="80803-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="80803-194">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="80803-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="80803-195">**Lokation:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="80803-196">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="80803-197">**Sorter verifikation:** *Positionsscanning*</span><span class="sxs-lookup"><span data-stu-id="80803-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="80803-198">Dette felt definerer den verifikation, der kræves under sorteringen.</span><span class="sxs-lookup"><span data-stu-id="80803-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="80803-199">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="80803-199">The following values are available:</span></span>

        - <span data-ttu-id="80803-200">None</span><span class="sxs-lookup"><span data-stu-id="80803-200">None</span></span>
        - <span data-ttu-id="80803-201">Scanning af id</span><span class="sxs-lookup"><span data-stu-id="80803-201">License plate scan</span></span>
        - <span data-ttu-id="80803-202">Scanning af position</span><span class="sxs-lookup"><span data-stu-id="80803-202">Position scan</span></span>

    - <span data-ttu-id="80803-203">**Opret arbejde lukning af position:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="80803-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="80803-204">Hvis indstillingen er angivet til *Ja*, når positionen er lukket, oprettes arbejde for at flytte lageret til den endelige afsendelseslokation.</span><span class="sxs-lookup"><span data-stu-id="80803-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="80803-205">Hvis den er indstillet til *Nej*, vil lageret straks blive plukket til ordren, når positionen er lukket.</span><span class="sxs-lookup"><span data-stu-id="80803-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="80803-206">**Positionstildeling:** *Manuel*</span><span class="sxs-lookup"><span data-stu-id="80803-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="80803-207">I dette felt defineres typen af positionstildeling.</span><span class="sxs-lookup"><span data-stu-id="80803-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="80803-208">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="80803-208">The following values are available:</span></span>

        - <span data-ttu-id="80803-209">**Manuel** – brugeren skal altid angive, hvilken position lageret skal sorteres til.</span><span class="sxs-lookup"><span data-stu-id="80803-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="80803-210">**Automatisk** – systemet guider automatisk lageret til en position, hvor det kan, baseret på sorteringsskabelonskiftene.</span><span class="sxs-lookup"><span data-stu-id="80803-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="80803-211">**Tildel kriterier for sorteringsposition:** *Brug kun tom position*</span><span class="sxs-lookup"><span data-stu-id="80803-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="80803-212">Dette felt styrer, om lageret, der allerede findes på sorteringspositionen, tages højde for, når der tildeles en position til behovet.</span><span class="sxs-lookup"><span data-stu-id="80803-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="80803-213">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="80803-213">The following values are available:</span></span>

        - <span data-ttu-id="80803-214">**Brug kun tom position** – positioner, der allerede har lager tilknyttet, vil blive taget i betragtning</span><span class="sxs-lookup"><span data-stu-id="80803-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="80803-215">**Antag, at position er tom** – alle de varer, der allerede er på positionen, vil blive ignoreret under tildelingen.</span><span class="sxs-lookup"><span data-stu-id="80803-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="80803-216">Alle tilgængelige positioner vil blive brugt.</span><span class="sxs-lookup"><span data-stu-id="80803-216">All available positions will be used.</span></span>

    - <span data-ttu-id="80803-217">**Kode for bølgetrin:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="80803-218">Hvis funktionen *Bølgetrinskode for hele organisationen* er aktiveret, skal bølgetrinskoden *Sortering* også konfigureres i bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="80803-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="80803-219">**Luk automatisk sorteringsposition:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="80803-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="80803-220">Hvis denne indstilling er angivet til *Ja*, vil sorteringsplaceringen automatisk blive lukket, når alt det arbejde, der kommer til placeringen, er fuldført.</span><span class="sxs-lookup"><span data-stu-id="80803-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="80803-221">**Antal sorteringspositioner:** *3*</span><span class="sxs-lookup"><span data-stu-id="80803-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="80803-222">Dette felt definerer det maksimale antal sorteringspositioner, som systemet opretter.</span><span class="sxs-lookup"><span data-stu-id="80803-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="80803-223">**Sorteringspositionspræfiks:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="80803-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="80803-224">Dette felt definerer det præfiks, som systemet tildeler før positionsnummeret.</span><span class="sxs-lookup"><span data-stu-id="80803-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="80803-225">**Luk automatisk pakningsposition:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="80803-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="80803-226">Hvis denne indstilling er angivet til *Ja*, pakkes lageret på sorteringsplaceringen i en container, når placeringen lukkes.</span><span class="sxs-lookup"><span data-stu-id="80803-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="80803-227">**Pakkeprofil-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="80803-228">Dette felt definerer den pakkeprofil, der skal bruges, når sorteringslokationen pakkes i en container.</span><span class="sxs-lookup"><span data-stu-id="80803-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="80803-229">Gå til handlingsruden, og vælg **Rediger forespørgsel** for at angive de kriterier, der bruges til denne sorteringsskabelon.</span><span class="sxs-lookup"><span data-stu-id="80803-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="80803-230">Vælg forespørgselsdialogboksen skal du under fanen **Sortering** vælge **Ny** for at føje en linje og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="80803-231">**Tabel:** *Lastdetaljer*</span><span class="sxs-lookup"><span data-stu-id="80803-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="80803-232">**Afledt tabel:** *Lastdetaljer*</span><span class="sxs-lookup"><span data-stu-id="80803-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="80803-233">**Felt:** *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="80803-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="80803-234">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="80803-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="80803-235">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80803-235">Select **OK**.</span></span>
1. <span data-ttu-id="80803-236">Du kan få vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?"</span><span class="sxs-lookup"><span data-stu-id="80803-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="80803-237">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80803-237">Select **Yes**.</span></span>

    <span data-ttu-id="80803-238">Knappen **Udgående sorteringsskabelonskift** i handlingsruden bliver tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="80803-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="80803-239">I handlingsruden skal du vælge **Udgående sorteringsskabelonskift**.</span><span class="sxs-lookup"><span data-stu-id="80803-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="80803-240">Vælg afkrydsningsfeltet **Gruppér efter felt** for at gruppere efter forsendelses-id.</span><span class="sxs-lookup"><span data-stu-id="80803-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="80803-241">Denne indstilling vil oprette én sorteringsposition pr. forsendelse, der er en container i bølgen.</span><span class="sxs-lookup"><span data-stu-id="80803-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="80803-242">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80803-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="80803-243">Metoder til bølgeproces</span><span class="sxs-lookup"><span data-stu-id="80803-243">Wave process methods</span></span>

1. <span data-ttu-id="80803-244">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="80803-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="80803-245">Vælg **Genopret metoder** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="80803-246">Metoden **Sortering** føjes til listen over tilgængelige metoder, og bølgeskabelontypen *Forsendelse* er valgt til den.</span><span class="sxs-lookup"><span data-stu-id="80803-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="80803-247">Bølgeskabeloner</span><span class="sxs-lookup"><span data-stu-id="80803-247">Wave templates</span></span>

<span data-ttu-id="80803-248">Rediger den bølgeskabelon, der bruges til sortering af bølgebehov.</span><span class="sxs-lookup"><span data-stu-id="80803-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="80803-249">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="80803-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="80803-250">I feltet **Bølgeskabelontype** skal du vælge *Forsendelse*.</span><span class="sxs-lookup"><span data-stu-id="80803-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="80803-251">Vælg den eksisterende skabelon **62 Forsendelsesstandard**.</span><span class="sxs-lookup"><span data-stu-id="80803-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="80803-252">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="80803-253">I oversigtspanelet **Generelt** skal du foretage følgende ændringer::</span><span class="sxs-lookup"><span data-stu-id="80803-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="80803-254">Angiv indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="80803-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="80803-255">Angiv indstillingen **Tildel til åbne bølger** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="80803-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="80803-256">Gå til oversigtspanelet **Meoder**, og konfigurer metoden **Sortering**:</span><span class="sxs-lookup"><span data-stu-id="80803-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="80803-257">I gitteret **Resterende metoder** skal du vælge **Sortering**.</span><span class="sxs-lookup"><span data-stu-id="80803-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="80803-258">Vælg knappen Højre pil for at flytte **sortering** til gitteret **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="80803-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="80803-259">I gitteret **Valgte metoder** skal du vælge **sortering**.</span><span class="sxs-lookup"><span data-stu-id="80803-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="80803-260">Indstil feltet **Bølgetrinskode** til *Sorter*.</span><span class="sxs-lookup"><span data-stu-id="80803-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="80803-261">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="80803-262">Menupunkter i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="80803-262">Mobile device menu items</span></span>

1. <span data-ttu-id="80803-263">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="80803-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="80803-264">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="80803-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="80803-265">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="80803-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="80803-266">**Navn på menupunkt:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="80803-267">**Titel:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="80803-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="80803-268">**Tilstand:** *Indirekte*</span><span class="sxs-lookup"><span data-stu-id="80803-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="80803-269">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="80803-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="80803-270">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="80803-271">**Aktivitetskode:** *Udgående sortering*</span><span class="sxs-lookup"><span data-stu-id="80803-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="80803-272">**Brug proceslinje:** *Ja* (standardværdi)</span><span class="sxs-lookup"><span data-stu-id="80803-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="80803-273">**Id for skabelon til udgående sortering:** *Bølgesortering*</span><span class="sxs-lookup"><span data-stu-id="80803-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="80803-274">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="80803-275">Menu i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="80803-275">Mobile device menu</span></span>

1. <span data-ttu-id="80803-276">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="80803-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="80803-277">Vælg **Udgående** på listen over menuer.</span><span class="sxs-lookup"><span data-stu-id="80803-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="80803-278">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="80803-279">I gitteret **Tilgængelig menuer og menupunkter** skal du finde og vælge menupunktet **Sorter**, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="80803-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="80803-280">Vælg den højre piletast for at flytte **Sorter** til gitteret **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="80803-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="80803-281">På denne måde føjer du det menupunktet til menuen **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="80803-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="80803-282">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="80803-283">Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="80803-283">Location directives</span></span>

<span data-ttu-id="80803-284">Du skal oprette lokationsdirektiver for at styre det arbejde, der oprettes, efter at sorteringen er udført.</span><span class="sxs-lookup"><span data-stu-id="80803-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="80803-285">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="80803-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="80803-286">I feltet **Arbejdsordretype** skal du vælge *Sorteret lagerplukning*.</span><span class="sxs-lookup"><span data-stu-id="80803-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="80803-287">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="80803-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="80803-288">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="80803-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="80803-289">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="80803-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="80803-290">**Navn:** *Læg til lagerport*</span><span class="sxs-lookup"><span data-stu-id="80803-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="80803-291">I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="80803-292">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="80803-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="80803-293">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="80803-293">**Site:** *6*</span></span>
    - <span data-ttu-id="80803-294">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="80803-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="80803-295">**Vejledningskode:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="80803-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="80803-296">**Flere SKU'er:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="80803-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="80803-297">Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="80803-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="80803-298">I oversigtspanelet **Linjer** skal du vælge **Ny** og derefter indstille følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="80803-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="80803-299">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="80803-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="80803-300">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="80803-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="80803-301">**Fra antal:** *0*</span><span class="sxs-lookup"><span data-stu-id="80803-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="80803-302">**Til antal:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="80803-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="80803-303">Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="80803-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="80803-304">I oversigtspanelet **Handlinger i lokationsvejledninger** skal du vælge **Ny** og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="80803-305">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="80803-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="80803-306">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="80803-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="80803-307">**Navn:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="80803-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="80803-308">Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig i oversigtspanelet **Handlinger i lokationsvejledning**.</span><span class="sxs-lookup"><span data-stu-id="80803-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="80803-309">Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="80803-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="80803-310">Gå til dialogboksen til forespørgselseditoren under fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Lokation*.</span><span class="sxs-lookup"><span data-stu-id="80803-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="80803-311">Angiv feltet **Kriterier** for denne række til *Lagerport*.</span><span class="sxs-lookup"><span data-stu-id="80803-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="80803-312">Vælg **OK** for at bekræfte redigering.</span><span class="sxs-lookup"><span data-stu-id="80803-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="80803-313">Arbejdsklasser</span><span class="sxs-lookup"><span data-stu-id="80803-313">Work classes</span></span>

1. <span data-ttu-id="80803-314">Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="80803-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="80803-315">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="80803-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="80803-316">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="80803-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="80803-317">**Arbejdsklasse-id:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="80803-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="80803-318">**Beskrivelse:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="80803-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="80803-319">**Ordretype:** *Sorteret lagerplukning*</span><span class="sxs-lookup"><span data-stu-id="80803-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="80803-320">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="80803-321">Arbejdsskabeloner</span><span class="sxs-lookup"><span data-stu-id="80803-321">Work templates</span></span>

1. <span data-ttu-id="80803-322">Gå til **Lokationsstyring \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="80803-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="80803-323">I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="80803-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="80803-324">I gitteret skal du vælge arbejdsskabelonen **62 Pluk til pakning**.</span><span class="sxs-lookup"><span data-stu-id="80803-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="80803-325">Vælg **Opgaveoverskriften skifter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="80803-326">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="80803-327">På den linje, hvor feltet **feltnavn** er angivet til *Forsendelses-id*, skal du rydde afkrydsningsfeltet **Gruppér efter dette felt**.</span><span class="sxs-lookup"><span data-stu-id="80803-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="80803-328">Vælg **Gem**, og luk derefter dialogboksen **Opgaveoverskriften skifter**.</span><span class="sxs-lookup"><span data-stu-id="80803-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="80803-329">I feltet **Arbejdsordretype** skal du vælge *Sorteret lagerplukning*.</span><span class="sxs-lookup"><span data-stu-id="80803-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="80803-330">Vælg **Ny** for at oprette en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="80803-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="80803-331">I sektionen **Oversigt** kan du angive følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="80803-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="80803-332">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="80803-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="80803-333">**Arbejdsskabelon:** *Sorteret pluk*</span><span class="sxs-lookup"><span data-stu-id="80803-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="80803-334">**Beskrivelse af arbejdsskabelon:** *Sorteret pluk*</span><span class="sxs-lookup"><span data-stu-id="80803-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="80803-335">Vælg **Gem** for at gøre sektionen **Arbejdsskabelondetaljer** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="80803-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="80803-336">I sektionen **Arbejdsskabelondetaljer** skal du oprette to linjer.</span><span class="sxs-lookup"><span data-stu-id="80803-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="80803-337">Vælg **Ny**, og vælg derefter følgende værdier for linje 1:</span><span class="sxs-lookup"><span data-stu-id="80803-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="80803-338">**Arbejdstype:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="80803-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="80803-339">**Obligatorisk:** Valgt (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="80803-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="80803-340">**Arbejdsklasse-id:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="80803-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="80803-341">Vælg **Ny** igen, og vælg derefter følgende værdier for linje 2:</span><span class="sxs-lookup"><span data-stu-id="80803-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="80803-342">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="80803-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="80803-343">**Obligatorisk:** Valgt (= *Ja*)</span><span class="sxs-lookup"><span data-stu-id="80803-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="80803-344">**Arbejdsklasse-id:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="80803-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="80803-345">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="80803-346">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="80803-346">Example scenario</span></span>

<span data-ttu-id="80803-347">Dette scenarie simulerer en situation, hvor lagerstedet opbevarer små varer på lokationer og skal pakke dem i kasser, før de leveres, og hvor pakkestationens funktionalitet ikke er korrekt.</span><span class="sxs-lookup"><span data-stu-id="80803-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="80803-348">Medarbejdere plukker ordrer for flere kunder og forskellige adresser samtidigt for at øge plukhastigheden.</span><span class="sxs-lookup"><span data-stu-id="80803-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="80803-349">Når plukningen er fuldført, ankommer arbejderne til sorteringspositionen, hvor de plukkede varer kan sorteres til den rigtige kasse baseret på de krævede kriterier.</span><span class="sxs-lookup"><span data-stu-id="80803-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="80803-350">I dette eksempel bruges forsendelses-id'et til at bestemme det rette felt, da hver forsendelse har en særskilt adresse.</span><span class="sxs-lookup"><span data-stu-id="80803-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="80803-351">Når alle varer fra lasten er pakket og sorteret efter forsendelse, flyttes boksene til det midlertidige lagringsområde og bliver derefter læsset på en lastbil.</span><span class="sxs-lookup"><span data-stu-id="80803-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="80803-352">Før du starter scenariet, skal du sikre dig, at alle standardlagerfunktioner er konfigureret korrekt for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="80803-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="80803-353">Standard-Contoso-lagersted *62* bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="80803-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="80803-354">Standardkonfigurationer er ikke blevet ændret, ud over hvad der er beskrevet i opsætningen.</span><span class="sxs-lookup"><span data-stu-id="80803-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="80803-355">Oprette efterspørgsel</span><span class="sxs-lookup"><span data-stu-id="80803-355">Create demand</span></span>

<span data-ttu-id="80803-356">Før du kan få vist funktionaliteten, skal du oprette et behov.</span><span class="sxs-lookup"><span data-stu-id="80803-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="80803-357">I dette scenarie skal du oprette tre salgsordrer for tre forskellige debitorer for at simulere forskellige leveringsadresser.</span><span class="sxs-lookup"><span data-stu-id="80803-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="80803-358">På denne måde kan du oprette tre separate forsendelser.</span><span class="sxs-lookup"><span data-stu-id="80803-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="80803-359">Før du opretter salgsordrer og forsendelser, skal du sikre, at pluklokationerne har tilstrækkelig lagerbeholdning til alle varerne på ordrerne.</span><span class="sxs-lookup"><span data-stu-id="80803-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="80803-360">Gennemse indstillingerne i lokationsvejledning for at bekræfte de pluklokationer, der skal bruges til salgsordrepluk.</span><span class="sxs-lookup"><span data-stu-id="80803-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="80803-361">Hvis du skal justere lagerbeholdning, kan du oprette manuelle bevægelser, bruge genopfyldning eller anvende en anden proces.</span><span class="sxs-lookup"><span data-stu-id="80803-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="80803-362">Reserver derefter lageret.</span><span class="sxs-lookup"><span data-stu-id="80803-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="80803-363">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="80803-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="80803-364">Vælg **Ny** for at oprette en salgsordre for ordre 1.</span><span class="sxs-lookup"><span data-stu-id="80803-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="80803-365">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="80803-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="80803-366">**Kunde:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="80803-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="80803-367">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="80803-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="80803-368">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80803-368">Select **OK**.</span></span>
1. <span data-ttu-id="80803-369">Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="80803-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="80803-370">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-370">Set the following values:</span></span>

    - <span data-ttu-id="80803-371">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80803-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="80803-372">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="80803-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="80803-373">Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="80803-374">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="80803-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="80803-375">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="80803-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="80803-376">Gentag følgende fremgangsmåde for hver salgslinje på ordren for at reservere lager for den:</span><span class="sxs-lookup"><span data-stu-id="80803-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="80803-377">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Reservation** i menuen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="80803-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="80803-378">På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="80803-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="80803-379">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-379">Select **Save**.</span></span>

1. <span data-ttu-id="80803-380">Vælg **Ny** for at oprette en salgsordre for ordre 2.</span><span class="sxs-lookup"><span data-stu-id="80803-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="80803-381">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="80803-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="80803-382">**Kunde:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="80803-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="80803-383">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="80803-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="80803-384">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80803-384">Select **OK**.</span></span>
1. <span data-ttu-id="80803-385">Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="80803-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="80803-386">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-386">Set the following values:</span></span>

    - <span data-ttu-id="80803-387">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80803-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="80803-388">**Antal:** *7*</span><span class="sxs-lookup"><span data-stu-id="80803-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="80803-389">Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="80803-390">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="80803-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="80803-391">**Antal:** *3*</span><span class="sxs-lookup"><span data-stu-id="80803-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="80803-392">Gentag følgende fremgangsmåde for hver salgslinje på ordren for at reservere lager for den:</span><span class="sxs-lookup"><span data-stu-id="80803-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="80803-393">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Reservation** i menuen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="80803-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="80803-394">På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="80803-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="80803-395">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-395">Select **Save**.</span></span>

1. <span data-ttu-id="80803-396">Vælg **Ny** for at oprette en salgsordre for ordre 3.</span><span class="sxs-lookup"><span data-stu-id="80803-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="80803-397">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="80803-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="80803-398">**Kunde:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="80803-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="80803-399">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="80803-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="80803-400">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80803-400">Select **OK**.</span></span>
1. <span data-ttu-id="80803-401">Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="80803-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="80803-402">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="80803-402">Set the following values:</span></span>

    - <span data-ttu-id="80803-403">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80803-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="80803-404">**Antal:** *8*</span><span class="sxs-lookup"><span data-stu-id="80803-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="80803-405">Følg disse trin for at reservere lager for salgslinjen:</span><span class="sxs-lookup"><span data-stu-id="80803-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="80803-406">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Reservation** i menuen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="80803-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="80803-407">På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="80803-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="80803-408">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80803-408">Select **Save**.</span></span>

<span data-ttu-id="80803-409">Gennemfør følgende procedure for at frigive hver salgsordre til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="80803-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="80803-410">Der vil blive oprettet tre forskellige forsendelser.</span><span class="sxs-lookup"><span data-stu-id="80803-410">Three different shipments will be created.</span></span> <span data-ttu-id="80803-411">Du skal derefter tilføje alle tre forsendelser til en ny bølge.</span><span class="sxs-lookup"><span data-stu-id="80803-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="80803-412">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="80803-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="80803-413">Vælg den første salgsordre, du har oprettet, i gitteret.</span><span class="sxs-lookup"><span data-stu-id="80803-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="80803-414">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="80803-415">Du modtager en orienterende meddelelse, der viser bølge-id'et og forsendelses-id'et, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="80803-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="80803-416">Gentag de forrige trin for at frigive salgsordrer 2 og 3 til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="80803-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="80803-417">Bemærk, at den oplysningsmeddelelse, du modtager, angiver, at der er føjet en forsendelse til den bølge, der blev oprettet, da du frigav salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="80803-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="80803-418">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="80803-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="80803-419">Vælg det bølge-id, der er oprettet ud fra frigivelsen af salgsordrerne, for at åbne siden **Bølger**.</span><span class="sxs-lookup"><span data-stu-id="80803-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="80803-420">På denne side vises bølgeoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="80803-420">This page shows the wave details.</span></span> <span data-ttu-id="80803-421">I oversigtspanelet **Bølgelinjer** vises de forsendelser, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="80803-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="80803-422">Du skal nu oprette arbejde for at hente varer fra pluklokationerne til sorteringslokationen.</span><span class="sxs-lookup"><span data-stu-id="80803-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="80803-423">Vælg **Behandl** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="80803-424">Ved bølgebehandling vil sorteringsmetoden bruge sorteringsskabelonen til at tildele lageret til sorteringspositioner.</span><span class="sxs-lookup"><span data-stu-id="80803-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="80803-425">Når bølgebehandling er fuldført, modtager du en orienterende meddelelser, der angiver, at den pågældende bølge er poseret, og at arbejdet er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="80803-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="80803-426">I handlingsruden skal du under fanen **Fane** i gruppen **Relaterede oplysninger** vælge **Arbejde** for at få vist det arbejde, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="80803-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="80803-427">Notér dig arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="80803-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="80803-428">Gå til **Lagerlokation \> Pakning og containerisering \> Positonstildelinger for udgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="80803-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="80803-429">I kolonnen til venstre kan du få vist den udgående sorteringsposition, der er oprettet for de enkelte forsendelser.</span><span class="sxs-lookup"><span data-stu-id="80803-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="80803-430">I oversigtspanelet **Kriterier for sorteringsposition** kan du få vist forsendelses-id'et for den pågældende position.</span><span class="sxs-lookup"><span data-stu-id="80803-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="80803-431">Der er blevet oprettet et arbejds-id for at hente lageret fra pluklokationerne til sorteringslokationen.</span><span class="sxs-lookup"><span data-stu-id="80803-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="80803-432">Før du kan fuldføre arbejdet, skal du bruge det arbejds-id, der blev oprettet under bølgebehandling.</span><span class="sxs-lookup"><span data-stu-id="80803-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="80803-433">Salgsordrepluk til sorteringslokationen</span><span class="sxs-lookup"><span data-stu-id="80803-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="80803-434">Log på mobilappen som en arbejder på lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="80803-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="80803-435">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="80803-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="80803-436">I menuen **Udgående** skal du vælge **Salgspluk**.</span><span class="sxs-lookup"><span data-stu-id="80803-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="80803-437">Vælg feltet **Id**, og angiv derefter arbejds-id'et fra bølgeprocessen.</span><span class="sxs-lookup"><span data-stu-id="80803-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="80803-438">Bekræft indtastningen.</span><span class="sxs-lookup"><span data-stu-id="80803-438">Confirm your entry.</span></span>

    <span data-ttu-id="80803-439">Derefter bedes du angive en destinationsnummerplade (NP).</span><span class="sxs-lookup"><span data-stu-id="80803-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="80803-440">Bemærk, at linje 1 fra salgsordre 1 er den, der skal plukkes og føjes til destinationsnummerpladen.</span><span class="sxs-lookup"><span data-stu-id="80803-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="80803-441">Varenummeret, antallet, varebeskrivelsen og pluklokationen vises.</span><span class="sxs-lookup"><span data-stu-id="80803-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="80803-442">I feltet **Mål-NP** skal du angive et nummerplade-id.</span><span class="sxs-lookup"><span data-stu-id="80803-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="80803-443">Du skal vælge alle linjer, der er oprettet ud fra den behandlede bølge, på samme nummerplade.</span><span class="sxs-lookup"><span data-stu-id="80803-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="80803-444">Bekræft indtastningen.</span><span class="sxs-lookup"><span data-stu-id="80803-444">Confirm your entry.</span></span>

    <span data-ttu-id="80803-445">Mobilappen indeholder nu en serie af **Pluk**-sider, der peger på pluklokationen og på varen og det antal, der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="80803-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="80803-446">Når den plukkede vare føjes til nummerpladen, skal du bekræfte plukarbejdet.</span><span class="sxs-lookup"><span data-stu-id="80803-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="80803-447">Den sidste side er det arbejde, der skal placere de plukkede varer på sorteringslokationen.</span><span class="sxs-lookup"><span data-stu-id="80803-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="80803-448">Bekræft det første plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="80803-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="80803-449">Det næste plukarbejde vises.</span><span class="sxs-lookup"><span data-stu-id="80803-449">The next pick work is shown.</span></span> <span data-ttu-id="80803-450">Bekræft plukningen.</span><span class="sxs-lookup"><span data-stu-id="80803-450">Confirm the pick.</span></span>
1. <span data-ttu-id="80803-451">Fortsæt for at bekræfte det resterende plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="80803-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="80803-452">Det sidste trin er at fuldføre læg på lager-arbejde.</span><span class="sxs-lookup"><span data-stu-id="80803-452">The last step is to complete the put work.</span></span> <span data-ttu-id="80803-453">Bekræft læg på lager-aktiviteten til sorteringslokationen.</span><span class="sxs-lookup"><span data-stu-id="80803-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="80803-454">Du modtager en meddelelse om, at "arbejde er fuldført".</span><span class="sxs-lookup"><span data-stu-id="80803-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="80803-455">Afslut **Salgsplukning** på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="80803-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="80803-456">Sortering/sæt til væg</span><span class="sxs-lookup"><span data-stu-id="80803-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="80803-457">Nu, hvor alt lager er blevet placeret på sorteringslokationen, og at det skal sorteres til den korrekte sorteringsposition.</span><span class="sxs-lookup"><span data-stu-id="80803-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="80803-458">Log på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="80803-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="80803-459">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="80803-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="80803-460">I menuen **Udgående** skal du vælge **Sorter** for at begynde at sortere varerne.</span><span class="sxs-lookup"><span data-stu-id="80803-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="80803-461">I feltet **NP/CON** skal du angive destinationsnummerpladen for det plukkede salgsordrearbejde.</span><span class="sxs-lookup"><span data-stu-id="80803-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="80803-462">Bekræft indtastningen.</span><span class="sxs-lookup"><span data-stu-id="80803-462">Confirm your entry.</span></span>
1. <span data-ttu-id="80803-463">Angiv det varenummer, der skal sorteres først.</span><span class="sxs-lookup"><span data-stu-id="80803-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="80803-464">Systemet bestemmer den første sorteringsposition, der skal vises.</span><span class="sxs-lookup"><span data-stu-id="80803-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="80803-465">Bekræft sorteringspositionen.</span><span class="sxs-lookup"><span data-stu-id="80803-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="80803-466">Du bliver bedt om at tildele en nummerplade til sorteringspositionen.</span><span class="sxs-lookup"><span data-stu-id="80803-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="80803-467">Vælg feltet **NP**, angiv et id-nummer, og bekræft derefter indtastningen.</span><span class="sxs-lookup"><span data-stu-id="80803-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="80803-468">Da sorteringspositionen er relateret til forsendelses-id'et, sorterer du de plukkede varer til en nummerplade, der er specifik for den udgående leverance og salgsordre.</span><span class="sxs-lookup"><span data-stu-id="80803-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="80803-469">På næste side vises vare-id, antal, sorteringspositions-id og id-numrene for "fra" (pluk) og "til" (sortering).</span><span class="sxs-lookup"><span data-stu-id="80803-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="80803-470">Oplysningerne på denne side giver dig besked på at sortere den angivne vare og antallet fra pluknummerpladen til sorteringsnummerpladen.</span><span class="sxs-lookup"><span data-stu-id="80803-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="80803-471">Bekræft sorteringspositionen.</span><span class="sxs-lookup"><span data-stu-id="80803-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="80803-472">Sorter varer i den første sorteringsposition.</span><span class="sxs-lookup"><span data-stu-id="80803-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="80803-473">Når du er færdig, sender systemet dig til den næste sorteringsposition.</span><span class="sxs-lookup"><span data-stu-id="80803-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="80803-474">Gentag denne fremgangsmåde for alle plukkede linjer i arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="80803-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="80803-475">Du skal også bruge denne fremgangsmåde, når der er flere pluklinjer med samme varenummer.</span><span class="sxs-lookup"><span data-stu-id="80803-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="80803-476">Efterhånden som du gentager denne proces for alle varer, evaluerer systemet kriterierne fra den næste scannede vare (arbejdslinje) og bestemmer, hvilken sorteringsposition den skal lægges til.</span><span class="sxs-lookup"><span data-stu-id="80803-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="80803-477">Du bliver automatisk bedt om at placere varen på den korrekte sorteringsposition.</span><span class="sxs-lookup"><span data-stu-id="80803-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="80803-478">Afhængigt af bekræftelsesopsætningen bliver du også bedt om at bekræfte denne handling ved at angive positionsnummeret eller id-nummeret.</span><span class="sxs-lookup"><span data-stu-id="80803-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80803-479">Hvis automatisk sortering er slået til, er manuel tilsidesættelse ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="80803-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="80803-480">Når du er færdig, skal du i Microsoft Dynamics 365 Supply Chain Management åbne siden **Tildelinger af udgående sorteringsposition** for at gennemse statussen for positionerne.</span><span class="sxs-lookup"><span data-stu-id="80803-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="80803-481">Hvis positionerne lukkes automatisk, skal du vælge **Vis lukkede** for at få vist de lukkede positioner.</span><span class="sxs-lookup"><span data-stu-id="80803-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="80803-482">Bemærk, at transaktioner for sorteringspositioner vises.</span><span class="sxs-lookup"><span data-stu-id="80803-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="80803-483">Varen og det antal, der er behandlet gennem positionen, vises.</span><span class="sxs-lookup"><span data-stu-id="80803-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="80803-484">Når du opretter skabelonen for udgående sortering, skal du angive indstillingen til **Luk sorteringsposition automatisk** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="80803-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="80803-485">Derfor lukkes positionen automatisk, når den sidste forventede lagerbeholdning er sat til den.</span><span class="sxs-lookup"><span data-stu-id="80803-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="80803-486">Sorteringspositionerne er i statussen **Lukket**, og der er oprettet arbejde for at flytte det sorterede lager til lokationen *Lagerport*.</span><span class="sxs-lookup"><span data-stu-id="80803-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="80803-487">Fuldfør det sorterede lagerplukarbejde for at flytte lageret til afsendelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="80803-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="80803-488">Når lageret er klart, skal du sende og bekræfte det.</span><span class="sxs-lookup"><span data-stu-id="80803-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="80803-489">I forbindelse med sorteret lagerplukarbejde, der skal behandles korrekt, er der et menupunkt i mobilenheder, der har et arbejdsklasse-id, hvor feltet **Arbejdsordretype** er angivet til *Sorteret lagerpluk*, der skal bruges til flytnings- og læsningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="80803-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="80803-490">Lukke en position manuelt (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="80803-490">Manually close a position (optional)</span></span>

<span data-ttu-id="80803-491">Hvis sorteringspositionerne skal lukkes manuelt, skal indstillingen **Luk sorteringsposition automatisk** for skabelon til udgående sortering angives til *Nej*, og lukningen skal foretages, før lageret kan flyttes til lagerportområdet.</span><span class="sxs-lookup"><span data-stu-id="80803-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="80803-492">Positioner kan lukkes på flere forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="80803-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="80803-493">Via mobilappen Lokationsstyring:</span><span class="sxs-lookup"><span data-stu-id="80803-493">Via the Warehouse Management mobile app:</span></span>

    - <span data-ttu-id="80803-494">Brugeren kan scanne en af de varer, der allerede findes på positionen, og derefter vælge **Luk** for at lukke positionen.</span><span class="sxs-lookup"><span data-stu-id="80803-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="80803-495">Hvis brugeren scanner en container, der allerede er sorteret til container, vises en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="80803-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="80803-496">Brugeren kan dog stadig fortsætte med at lukke positionen.</span><span class="sxs-lookup"><span data-stu-id="80803-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="80803-497">På siden **Tildelinger af udgående sorteringsposition** i Microsoft Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="80803-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="80803-498">Brugeren kan vælge den udgående sorteringspositionspost og derefter vælge **Luk position** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80803-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="80803-499">Tip!</span><span class="sxs-lookup"><span data-stu-id="80803-499">Tips</span></span>

- <span data-ttu-id="80803-500">Varer kan ikke flyttes mellem positioner, når de er blevet tildelt til én.</span><span class="sxs-lookup"><span data-stu-id="80803-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="80803-501">Systemet evaluerer, hvor mange af hver vare der skal gå til en bestemt position.</span><span class="sxs-lookup"><span data-stu-id="80803-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="80803-502">Sorteringsskabeloner kan konfigureres til automatisk at oprette containere, når positionerne er lukket.</span><span class="sxs-lookup"><span data-stu-id="80803-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="80803-503">Denne fremgangsmåde opretter en standardcontainer-id-struktur, der er baseret på den angivne pakkeprofil.</span><span class="sxs-lookup"><span data-stu-id="80803-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80803-504">Når der er oprettet et overførselsarbejde ud fra sorteringspositionen, må du ikke annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="80803-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="80803-505">Ellers vil positionen og containerne i den blive slettet fra systemet og ikke være tilgængelig til viderebehandling.</span><span class="sxs-lookup"><span data-stu-id="80803-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="80803-506">Lageret vil også blive fjernet.</span><span class="sxs-lookup"><span data-stu-id="80803-506">The inventory will also be removed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]