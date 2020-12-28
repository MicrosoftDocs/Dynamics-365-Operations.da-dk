---
title: Udgående sortering
description: Dette emne indeholder oplysninger om udgående sortering. Denne funktion gør det nemmere at håndtere mindre containere og hjælper lagermedarbejderne med bedre at planlægge og organisere pallekapaciteten i lastbilen.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425048"
---
# <a name="outbound-sorting"></a><span data-ttu-id="00cf3-104">Udgående sortering</span><span class="sxs-lookup"><span data-stu-id="00cf3-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00cf3-105">Denne funktion gør det nemmere at håndtere mindre containere og hjælper lagermedarbejderne med bedre at planlægge og organisere pallekapaciteten i lastbilen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="00cf3-106">Når du bruger udgående sortering, kan du sortere pakkede containere til den korrekte palle, når de har været på en pakkestation.</span><span class="sxs-lookup"><span data-stu-id="00cf3-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="00cf3-107">Du kan også opbygge et pakkehierarki.</span><span class="sxs-lookup"><span data-stu-id="00cf3-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="00cf3-108">Med denne funktionalitet kan du opbygge paller fra beholdere, der er pakket via pakkefunktionen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="00cf3-109">Containeren sendes ikke til den endelige afsendelseslokation, fordi den er i det oprindelige emballeringsflow.</span><span class="sxs-lookup"><span data-stu-id="00cf3-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="00cf3-110">I stedet kan arbejderne lukke containeren og flytte den til en sorteringstypelokation.</span><span class="sxs-lookup"><span data-stu-id="00cf3-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="00cf3-111">De kan derefter sortere containere til positioner, der hver har en nummerplade (NP).</span><span class="sxs-lookup"><span data-stu-id="00cf3-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="00cf3-112">Når containerne er blevet sorteret, kan der oprettes arbejde for at sende hele NP'en til det endelige afsendelsesområde eller stadielokation baseret på lokationsvejledninger eller dine egne krav.</span><span class="sxs-lookup"><span data-stu-id="00cf3-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="00cf3-113">Derudover kan den handling, der udføres ved lukning af sorteringspositionen, straks flytte lageret til det endelige afsendelsessted og plukke det til ordren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="00cf3-114">Aktivere funktionen for udgående sortering</span><span class="sxs-lookup"><span data-stu-id="00cf3-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="00cf3-115">Før du kan bruge funktionen, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="00cf3-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="00cf3-116">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="00cf3-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="00cf3-117">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="00cf3-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="00cf3-118">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="00cf3-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="00cf3-119">**Funktionsnavn:** *Udgående sortering*</span><span class="sxs-lookup"><span data-stu-id="00cf3-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="00cf3-120">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="00cf3-120">Setup</span></span>

<span data-ttu-id="00cf3-121">I dette scenarie skal du bruge standarddemodata for **USMF** og lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="00cf3-122">Du skal også udføre den opsætning, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="00cf3-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="00cf3-123">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="00cf3-123">Set up a wave template</span></span>

<span data-ttu-id="00cf3-124">Denne konfiguration behandler automatisk bølgen og opretter arbejde, når en linje er frigivet til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="00cf3-125">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="00cf3-126">Vælg **Lagersted 62** på skabelonlisten.</span><span class="sxs-lookup"><span data-stu-id="00cf3-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="00cf3-127">I oversigtspanelet **Generelt** skal du kontrollere, at indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** er angivet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="00cf3-128">Konfigurere en arbejder</span><span class="sxs-lookup"><span data-stu-id="00cf3-128">Set up a worker</span></span>

<span data-ttu-id="00cf3-129">Pakkestationen betragtes som en lokation.</span><span class="sxs-lookup"><span data-stu-id="00cf3-129">The packing station is considered a location.</span></span> <span data-ttu-id="00cf3-130">De lagermedarbejdere, der logger på ved pakkestationen, kan kun se og arbejde på forsendelser og containere, der er planlagt på den pågældende pakkelokation.</span><span class="sxs-lookup"><span data-stu-id="00cf3-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="00cf3-131">En bruger, der logger på Microsoft Dynamics 365, skal være konfigureret som en arbejder i lokationsstyringen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="00cf3-132">Hvis brugerens navn ikke vises på listen over arbejdsbrugere, skal du benytte følgende fremgangsmåde for at tilføje det.</span><span class="sxs-lookup"><span data-stu-id="00cf3-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="00cf3-133">I disse trin antages det, at brugeren allerede findes i systemet og er blevet tilknyttet som medarbejder eller arbejder i modulet **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="00cf3-134">Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="00cf3-135">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-135">Select **New**.</span></span>
1. <span data-ttu-id="00cf3-136">I feltet **Arbejder** skal du vælge destinationsbrugeren på listen over medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="00cf3-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="00cf3-137">Vælg **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-137">Select **Select**.</span></span>
1. <span data-ttu-id="00cf3-138">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="00cf3-139">Gå til oversigtspanelet **Brugere**, og vælg **Ny** for at oprette en mobilenhedskonto, og angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-140">**Bruger-id:** Angiv et entydigt id.</span><span class="sxs-lookup"><span data-stu-id="00cf3-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="00cf3-141">**Brugernavn:** Angiv et navn til id'et.</span><span class="sxs-lookup"><span data-stu-id="00cf3-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="00cf3-142">**Standardlagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-143">**Menunavn:** *Hoved*</span><span class="sxs-lookup"><span data-stu-id="00cf3-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="00cf3-144">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="00cf3-145">Dialogboksen **Angiv adgangskode** viser, hvor du kan oprette en simpel adgangskode, som brugeren kan bruge til at logge på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="00cf3-146">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-146">Set the following values:</span></span>

    - <span data-ttu-id="00cf3-147">**Adgangskode:** Angiv en enkel adgangskode.</span><span class="sxs-lookup"><span data-stu-id="00cf3-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="00cf3-148">**Bekræft adgangskode:** Angiv den samme adgangskode igen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="00cf3-149">Vælg **Angiv adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-149">Select **Set password**.</span></span>

    <span data-ttu-id="00cf3-150">En besked i Handlingscenter indeholder en meddelelse om, at adgangskoden er angivet for den bruger, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="00cf3-151">Oprette en ny lokationstype</span><span class="sxs-lookup"><span data-stu-id="00cf3-151">Create a location type</span></span>

1. <span data-ttu-id="00cf3-152">Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationstyper**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="00cf3-153">Vælg **Ny** i i handlingsruden for at oprette lokationstype, og angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-154">**Lokationstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="00cf3-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="00cf3-155">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="00cf3-156">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="00cf3-157">Konfigurere parametre for lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="00cf3-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="00cf3-158">Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="00cf3-159">Gå til fanen **Generelt**, og angiv feltet **Sorteringslokationstype** til **SORTER** i oversigtspanelet *Lokationstyper*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="00cf3-160">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="00cf3-161">Konfigurere en lokationsprofil</span><span class="sxs-lookup"><span data-stu-id="00cf3-161">Set up a location profile</span></span>

1. <span data-ttu-id="00cf3-162">Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="00cf3-163">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-164">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="00cf3-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="00cf3-165">**Lokationsprofil-id:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="00cf3-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="00cf3-166">**Navn:** *Sortering*</span><span class="sxs-lookup"><span data-stu-id="00cf3-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="00cf3-167">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-168">**Lokationsformat:** *ASRB* (gang – reol-hylde-beholder)</span><span class="sxs-lookup"><span data-stu-id="00cf3-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="00cf3-169">**Lokationstype:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="00cf3-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="00cf3-170">**Brug sporing af nummerplader:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00cf3-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="00cf3-171">**Tillad blandede varer:** *Ja* (når du angiver denne indstilling til *Ja*, angives indstillingen **Tillad blandede lagerbatchnumre** automatisk til *Ja* og kan ikke ændres uafhængigt.)</span><span class="sxs-lookup"><span data-stu-id="00cf3-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="00cf3-172">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="00cf3-173">Konfigurere en lokation</span><span class="sxs-lookup"><span data-stu-id="00cf3-173">Set up a location</span></span>

1. <span data-ttu-id="00cf3-174">Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="00cf3-175">I hovedet skal du fjerne markeringen i afkrydsningsfeltet **Generér kontrolcifre for lokation**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="00cf3-176">Vælg **Ny** i i handlingsruden for at oprette lokation, og angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-177">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-178">**Lokation:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="00cf3-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="00cf3-179">**Lokationsprofil-id:** *SORTERING*</span><span class="sxs-lookup"><span data-stu-id="00cf3-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="00cf3-180">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="00cf3-181">Oprette en skabelon til udgående sortering</span><span class="sxs-lookup"><span data-stu-id="00cf3-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="00cf3-182">Skabelonen til udgående sortering bestemmer, om der er oprettet arbejde uden for sorteringslokationen, og om sorteringen skal udføres manuelt eller automatisk.</span><span class="sxs-lookup"><span data-stu-id="00cf3-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="00cf3-183">I dette scenario skal du oprette en skabelon til udgående sortering for at oprette paller efter pakkestationen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="00cf3-184">Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Skabelon til udgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="00cf3-185">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-186">Angiv følgende værdier i hoveddelen for den nye skabelon:</span><span class="sxs-lookup"><span data-stu-id="00cf3-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="00cf3-187">**Id for skabelon til udgående sortering:** *AutoArbejde*</span><span class="sxs-lookup"><span data-stu-id="00cf3-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="00cf3-188">**Beskrivelse:** *Oprettelse af automatisk arbejde*</span><span class="sxs-lookup"><span data-stu-id="00cf3-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="00cf3-189">**Skabelontype for udgående sortering:** *Container*</span><span class="sxs-lookup"><span data-stu-id="00cf3-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="00cf3-190">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-191">**Lokation:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="00cf3-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="00cf3-192">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-193">**Sorter verifikation:** *Positionsscanning*</span><span class="sxs-lookup"><span data-stu-id="00cf3-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="00cf3-194">**Opret arbejde lukning af position:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00cf3-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="00cf3-195">Hvis indstillingen er angivet til *Ja*, når positionen er lukket, oprettes arbejde for at flytte lageret til den endelige afsendelseslokation.</span><span class="sxs-lookup"><span data-stu-id="00cf3-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="00cf3-196">Hvis den er indstillet til *Nej*, vil lageret straks blive plukket til ordren, når positionen er lukket.</span><span class="sxs-lookup"><span data-stu-id="00cf3-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="00cf3-197">**Positiontildeling:** *Automatisk*</span><span class="sxs-lookup"><span data-stu-id="00cf3-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="00cf3-198">Hvis dette felt er indstillet til *Manuelt*, skal brugeren altid angive, hvilken position lageret skal sorteres til.</span><span class="sxs-lookup"><span data-stu-id="00cf3-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="00cf3-199">Hvis det er indstillet til *Automatisk*, guider systemet automatisk lageret til en position, hvor det kan, baseret på sorteringsskabelonskiftene.</span><span class="sxs-lookup"><span data-stu-id="00cf3-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="00cf3-200">Vælg **Gem** for at gøre knappen **Rediger forespørgsel** i handlingsruden tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="00cf3-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="00cf3-201">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="00cf3-202">I forespørgselseditor skal du under fanen **Sortering** tilføje en linje, der har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="00cf3-203">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="00cf3-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="00cf3-204">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="00cf3-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="00cf3-205">**Felt:** *Fragttjeneste*</span><span class="sxs-lookup"><span data-stu-id="00cf3-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="00cf3-206">Når du vælger denne værdi, får du muligvis vist følgende meddelelse: "Feltet Fragttjeneste er ikke et indeksfelt.</span><span class="sxs-lookup"><span data-stu-id="00cf3-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="00cf3-207">Vil du tilføje sortering på dette?"</span><span class="sxs-lookup"><span data-stu-id="00cf3-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="00cf3-208">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-208">Select **Yes**.</span></span>

    - <span data-ttu-id="00cf3-209">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="00cf3-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="00cf3-210">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-210">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-211">Du kan få vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?"</span><span class="sxs-lookup"><span data-stu-id="00cf3-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="00cf3-212">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-212">Select **Yes**.</span></span>

    <span data-ttu-id="00cf3-213">Knappen **Udgående sorteringsskabelonskift** i handlingsruden bliver tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="00cf3-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="00cf3-214">I handlingsruden skal du vælge **Udgående sorteringsskabelonskift**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="00cf3-215">I dialogboksen **Kriterier for udgående sortering** skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="00cf3-216">**Referencetabelnavn:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="00cf3-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="00cf3-217">**Referencefeltnavn:** *Fragttjeneste*</span><span class="sxs-lookup"><span data-stu-id="00cf3-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="00cf3-218">**Gruppér efter felt:** Marker dette afkrydsningsfelt for at gruppere forsendelser efter fragtmand.</span><span class="sxs-lookup"><span data-stu-id="00cf3-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="00cf3-219">Vælg **OK** for at gemme dine indstillinger og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="00cf3-220">Konfigurere politik for containerpakning</span><span class="sxs-lookup"><span data-stu-id="00cf3-220">Set up container packing policies</span></span>

1. <span data-ttu-id="00cf3-221">Gå til **Lokationsstyring \> Konfiguration \> Containere \> Politikker for containerpakning**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="00cf3-222">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-223">Angiv følgende værdier i hoveddelen for den nye politik:</span><span class="sxs-lookup"><span data-stu-id="00cf3-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="00cf3-224">**Politik for containerpakning:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-225">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="00cf3-226">I oversigtspanelet **Oversigt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-227">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-228">**Standardlokationen for sortering:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="00cf3-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="00cf3-229">**Vægtenhed:** *kg*</span><span class="sxs-lookup"><span data-stu-id="00cf3-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="00cf3-230">**Politik for containerlukning:** *Automatisk frigivelse*</span><span class="sxs-lookup"><span data-stu-id="00cf3-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="00cf3-231">**Politik for containerfrigivelse:** *Tildel container til position for udgående sortering*</span><span class="sxs-lookup"><span data-stu-id="00cf3-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="00cf3-232">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="00cf3-233">Konfigurere pakkeprofiler</span><span class="sxs-lookup"><span data-stu-id="00cf3-233">Set up packing profiles</span></span>

<span data-ttu-id="00cf3-234">Opret en ny pakkeprofil, der skal bruges sammen med sorteringsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="00cf3-235">Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Pakningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="00cf3-236">Vælg **Ny** i i handlingsruden for at oprette en linje, og angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-237">**Pakkeprofil-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-238">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-239">**Politik for containerpakning:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-240">**Container-id-tilstand:** *Auto*</span><span class="sxs-lookup"><span data-stu-id="00cf3-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="00cf3-241">**Containertype:** *Kasse-Stor*</span><span class="sxs-lookup"><span data-stu-id="00cf3-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="00cf3-242">**Opret automatisk container ved containerlukning:** Ryddet (= *Nej*)</span><span class="sxs-lookup"><span data-stu-id="00cf3-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="00cf3-243">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="00cf3-244">Konfigurere arbejdsklasser</span><span class="sxs-lookup"><span data-stu-id="00cf3-244">Set up work classes</span></span>

<span data-ttu-id="00cf3-245">Konfigurer en arbejdsklasse, der skal bruges sammen med sortering.</span><span class="sxs-lookup"><span data-stu-id="00cf3-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="00cf3-246">Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="00cf3-247">Vælg **Ny** i i handlingsruden for at oprette en arbejdsklasse til sortering, og angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-248">**Arbejdsklasse-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-249">**Beskrivelse:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-250">**Ordretype:** *Sorteret lagerplukning*</span><span class="sxs-lookup"><span data-stu-id="00cf3-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="00cf3-251">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="00cf3-252">Opsætning af mobilenhedsmenupunkter</span><span class="sxs-lookup"><span data-stu-id="00cf3-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="00cf3-253">Konfigurere nyt pallemenupunkt</span><span class="sxs-lookup"><span data-stu-id="00cf3-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="00cf3-254">Opret et menupunkt til mobilenhed for at opbygge paller under sortering.</span><span class="sxs-lookup"><span data-stu-id="00cf3-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="00cf3-255">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="00cf3-256">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-257">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="00cf3-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="00cf3-258">**Navn på menupunkt:** *Palle-build*</span><span class="sxs-lookup"><span data-stu-id="00cf3-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="00cf3-259">**Titel:** *Palle-build*</span><span class="sxs-lookup"><span data-stu-id="00cf3-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="00cf3-260">**Tilstand:** *Indirekte*</span><span class="sxs-lookup"><span data-stu-id="00cf3-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="00cf3-261">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="00cf3-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="00cf3-262">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-263">**Aktivitetskode:** *Udgående sortering*</span><span class="sxs-lookup"><span data-stu-id="00cf3-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="00cf3-264">Når dette felt er angivet til *Udgående sortering*, vises feltet udgående **Skabelon-id for udgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="00cf3-265">**Brug procesvejledning:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00cf3-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="00cf3-266">Når feltet **Aktivitetskode** er angivet til *Udgående sortering*, angives denne indstilling automatisk til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="00cf3-267">**Id for skabelon til udgående sortering:** *AutoArbejde*</span><span class="sxs-lookup"><span data-stu-id="00cf3-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="00cf3-268">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="00cf3-269">Konfigurere nyt lastmenupunkt</span><span class="sxs-lookup"><span data-stu-id="00cf3-269">Set up a new loading menu item</span></span>

<span data-ttu-id="00cf3-270">Derefter skal du oprette et menupunkt, som giver brugerne mulighed for at flytte de sorterede lagervarer til afsendelsesstedet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="00cf3-271">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="00cf3-272">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-273">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="00cf3-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="00cf3-274">**Navn på menupunkt:** *Sortering efter last fra*</span><span class="sxs-lookup"><span data-stu-id="00cf3-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="00cf3-275">**Titel:** *Sortering efter last fra*</span><span class="sxs-lookup"><span data-stu-id="00cf3-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="00cf3-276">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="00cf3-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="00cf3-277">**Brug eksisterende arbejde:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00cf3-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="00cf3-278">I oversigtspanelet **Generelt** skal du indstille feltet **Styret af** til *Brugerstyret*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="00cf3-279">I oversigtspanelet **Arbejdsklasser** skal du vælge **Ny** og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="00cf3-280">**Arbejdsklasse-id:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="00cf3-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="00cf3-281">**Ordretype:** *Sorteret lagerplukning*</span><span class="sxs-lookup"><span data-stu-id="00cf3-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="00cf3-282">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="00cf3-283">Konfigurere mobilenhedsmenuen</span><span class="sxs-lookup"><span data-stu-id="00cf3-283">Set up the mobile device menu</span></span>

<span data-ttu-id="00cf3-284">Du skal nu føje de nye menupunkter til mobilenhedsmenuen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="00cf3-285">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="00cf3-286">Vælg menuen **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="00cf3-287">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="00cf3-288">I kolonnen **Tilgængelige menuer og menupunkter** skal du finde og vælge **Palle-build**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="00cf3-289">Vælg den højre piletast for at flytte **Palle-build** til kolonnen **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="00cf3-290">Brug knapperne pil op og pil ned for at placere menupunktet **Palle-build** i den ønskede placering i mobilenhedsmenuen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="00cf3-291">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-291">Select **Save**.</span></span>
1. <span data-ttu-id="00cf3-292">Gentag denne procedure for at føje menupunktet **Sortering efter last fra** til menuen **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="00cf3-293">Konfigurer lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="00cf3-293">Set up location directives</span></span>

<span data-ttu-id="00cf3-294">*Lokalitetsvejledninger* er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser.</span><span class="sxs-lookup"><span data-stu-id="00cf3-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="00cf3-295">Du skal nu oprette en regel for at administrere sorteringsarbejdet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="00cf3-296">Konfigurere vejledning for enkelt varenummer</span><span class="sxs-lookup"><span data-stu-id="00cf3-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="00cf3-297">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="00cf3-298">I ruden til venstre skal du ændre værdien i feltet **Arbejdsordretype** til *Sorteret lagerpluk*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="00cf3-299">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-300">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="00cf3-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="00cf3-301">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="00cf3-302">**Navn:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="00cf3-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="00cf3-303">I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-304">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="00cf3-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="00cf3-305">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="00cf3-305">**Site:** *6*</span></span>
    - <span data-ttu-id="00cf3-306">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-307">**Flere SKU'er:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="00cf3-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="00cf3-308">Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Linjer** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="00cf3-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="00cf3-309">I oversigtspanelet **Linjer** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="00cf3-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="00cf3-310">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="00cf3-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="00cf3-311">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="00cf3-312">**Fra:** *0*</span><span class="sxs-lookup"><span data-stu-id="00cf3-312">**From:** *0*</span></span>
    - <span data-ttu-id="00cf3-313">**Til:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="00cf3-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="00cf3-314">Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Handlinger i lokationsvejledning** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="00cf3-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="00cf3-315">I oversigtspanelet **Handlinger i lokationsvejledninger** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="00cf3-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="00cf3-316">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="00cf3-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="00cf3-317">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="00cf3-318">**Navn:** *Båsedør*</span><span class="sxs-lookup"><span data-stu-id="00cf3-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="00cf3-319">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-319">Select **Save**.</span></span>
1. <span data-ttu-id="00cf3-320">Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="00cf3-321">Gå til forespørgselseditoren under fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Lokation*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="00cf3-322">Angiv feltet **Kriterier** for denne række til *Lagerport*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="00cf3-323">Vælg **OK** for at gemme dine indstillinger og lukke forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="00cf3-324">Konfigurere vejledning for flere varenumre</span><span class="sxs-lookup"><span data-stu-id="00cf3-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="00cf3-325">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="00cf3-326">I ruden til venstre skal du ændre værdien i feltet **Arbejdsordretype** til *Sorteret lagerpluk*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="00cf3-327">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-328">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="00cf3-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="00cf3-329">**Sekvens:** *2*</span><span class="sxs-lookup"><span data-stu-id="00cf3-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="00cf3-330">**Navn:** *Lagerport – flere*</span><span class="sxs-lookup"><span data-stu-id="00cf3-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="00cf3-331">I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-332">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="00cf3-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="00cf3-333">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="00cf3-333">**Site:** *6*</span></span>
    - <span data-ttu-id="00cf3-334">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-335">**Flere varenumre:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="00cf3-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="00cf3-336">Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Linjer** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="00cf3-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="00cf3-337">I oversigtspanelet **Linjer** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="00cf3-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="00cf3-338">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="00cf3-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="00cf3-339">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="00cf3-340">**Fra:** *0*</span><span class="sxs-lookup"><span data-stu-id="00cf3-340">**From:** *0*</span></span>
    - <span data-ttu-id="00cf3-341">**Til:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="00cf3-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="00cf3-342">Vælg **Gem** for at gøre værktøjslinjen i oversigtspanelet **Handlinger i lokationsvejledning** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="00cf3-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="00cf3-343">I oversigtspanelet **Handlinger i lokationsvejledninger** skal du vælge **Ny** og derefter indstille følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="00cf3-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="00cf3-344">Accepter standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="00cf3-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="00cf3-345">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="00cf3-346">**Navn:** *Lagerport – flere*</span><span class="sxs-lookup"><span data-stu-id="00cf3-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="00cf3-347">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-347">Select **Save**.</span></span>
1. <span data-ttu-id="00cf3-348">Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="00cf3-349">Gå til forespørgselseditoren under fanen **Område**, og find den række, hvor feltet **Felt** er indstillet til *Lokation*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="00cf3-350">Angiv feltet **Kriterier** for denne række til *Lagerport*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="00cf3-351">Vælg **OK** for at gemme dine indstillinger og lukke forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="00cf3-352">Konfigurer arbejdsskabeloner</span><span class="sxs-lookup"><span data-stu-id="00cf3-352">Set up work templates</span></span>

1. <span data-ttu-id="00cf3-353">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="00cf3-354">Skift værdien af feltet **Arbejdsordretype** til *Sorteret lagerpluk*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="00cf3-355">Vælg **Ny** i handlingsruden for at oprette en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="00cf3-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="00cf3-356">På fanen **Oversigt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-357">**Sekvens:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="00cf3-358">**Arbejdsskabelon:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="00cf3-359">**Beskrivelse af arbejdsskabelon:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="00cf3-360">Vælg **Gem** for at gøre oversigtspanelet **Arbejdsskabelondetaljer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="00cf3-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="00cf3-361">Gå til oversigtspanelet **Arbejdsskabelondetaljer**, og vælg **Ny** for at tilføje en linje, og indstil derefter følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-362">**Arbejdstype:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="00cf3-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="00cf3-363">**Arbejdsklasse-id:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="00cf3-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="00cf3-364">Vælg **Ny** igen for at tilføje en anden linje, og angiv derefter følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="00cf3-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="00cf3-365">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="00cf3-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="00cf3-366">**Arbejdsklasse-id:** *SORTER*</span><span class="sxs-lookup"><span data-stu-id="00cf3-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="00cf3-367">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="00cf3-368">Scenario</span><span class="sxs-lookup"><span data-stu-id="00cf3-368">Scenario</span></span>

<span data-ttu-id="00cf3-369">Dette scenarie simulerer en situation, hvor pakkede containere automatisk sorteres til andre placeringer (paller) efter pakkestationen, afhængigt af fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="00cf3-370">Når alle varer fra lasten pakkes og sorteres efter adresse, og pallerne flyttes til lagerporten.</span><span class="sxs-lookup"><span data-stu-id="00cf3-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="00cf3-371">Oprette ordrer og plukarbejde</span><span class="sxs-lookup"><span data-stu-id="00cf3-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="00cf3-372">Opret salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="00cf3-372">Create sales order 1</span></span>

1. <span data-ttu-id="00cf3-373">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="00cf3-374">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-375">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="00cf3-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="00cf3-376">**Debitorkonto:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="00cf3-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="00cf3-377">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="00cf3-378">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="00cf3-379">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="00cf3-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="00cf3-380">Skift til **overskriftsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="00cf3-381">Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="00cf3-382">**Fragtmand:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="00cf3-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="00cf3-383">**Fragttjeneste:** *Air*</span><span class="sxs-lookup"><span data-stu-id="00cf3-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="00cf3-384">Skift til visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="00cf3-385">Hvis en ny tom linje ikke automatisk føjes til gitteret i oversigtspanelet **Salgsordrelinjer**, skal du vælge **Tilføj linje** for at tilføje en.</span><span class="sxs-lookup"><span data-stu-id="00cf3-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="00cf3-386">På den nye ordrelinje skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="00cf3-387">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="00cf3-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="00cf3-388">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="00cf3-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="00cf3-389">Mens den nye ordrelinje stadig er valgt i oversigtspanelet **Salgsordrelinjer**, skal du vælge **Reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="00cf3-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="00cf3-390">På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på den valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="00cf3-391">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="00cf3-392">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="00cf3-393">Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre.</span><span class="sxs-lookup"><span data-stu-id="00cf3-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="00cf3-394">Noter dig bølge-id og forsendelses-id-numrene.</span><span class="sxs-lookup"><span data-stu-id="00cf3-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="00cf3-395">Salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="00cf3-395">Sales order 2</span></span>

1. <span data-ttu-id="00cf3-396">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="00cf3-397">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="00cf3-398">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="00cf3-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="00cf3-399">**Debitorkonto:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="00cf3-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="00cf3-400">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="00cf3-401">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="00cf3-402">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="00cf3-402">The new sales order is opened.</span></span> <span data-ttu-id="00cf3-403">Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="00cf3-404">Indstil følgende værdier på denne ordrelinje:</span><span class="sxs-lookup"><span data-stu-id="00cf3-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="00cf3-405">**Vare:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="00cf3-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="00cf3-406">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="00cf3-407">I oversigtspanelet **Linjedetaljer** under fanen **Levering** skal du angive feltet **Leveringsmåde** til *Flow-STD*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="00cf3-408">I oversigtspanelet **Salgsordrelinjer** skal du vælge **Tilføj linje** og derefter indstille følgende værdier på den anden linje:</span><span class="sxs-lookup"><span data-stu-id="00cf3-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="00cf3-409">**Vare:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="00cf3-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="00cf3-410">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="00cf3-411">I oversigtspanelet **Linjedetaljer** under fanen **Levering** ændre værdien af feltet **Leveringsmåde** til *Luft C-Luft*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="00cf3-412">I oversigtspanelet **Salgsordrelinjer** skal du vælge den første ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="00cf3-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="00cf3-413">Vælg derefter **Reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="00cf3-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="00cf3-414">På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på den valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="00cf3-415">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="00cf3-416">I oversigtspanelet **Salgsordrelinjer** skal du vælge den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="00cf3-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="00cf3-417">Vælg derefter **Reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="00cf3-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="00cf3-418">På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på den valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="00cf3-419">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="00cf3-420">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="00cf3-421">Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre.</span><span class="sxs-lookup"><span data-stu-id="00cf3-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="00cf3-422">Bemærk, at der er oprettet to bølge-numre og to forsendelses-id-numre er blevet oprettet, et for hver leveringsmåde for salgsordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="00cf3-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="00cf3-423">Få arbejds-id'erne fra arbejdsdetaljerne</span><span class="sxs-lookup"><span data-stu-id="00cf3-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="00cf3-424">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="00cf3-425">På siden vises de arbejds-id'er, der er oprettet ud fra salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="00cf3-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="00cf3-426">Brug bølge-id'erne og forsendelses-id'erne fra de salgsordrer, du har oprettet, til at finde arbejds-id'et for hver enkelt bølge og forsendelse.</span><span class="sxs-lookup"><span data-stu-id="00cf3-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="00cf3-427">Noter dig disse arbejds-id'er, fordi du skal bruge dem i de næste trin.</span><span class="sxs-lookup"><span data-stu-id="00cf3-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="00cf3-428">Bemærk, at der er oprettet to arbejds-id'er for den anden salgsordre.</span><span class="sxs-lookup"><span data-stu-id="00cf3-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="00cf3-429">Hvis der plukkes forskellige varer fra forskellige lokationer, genereres der separate arbejds-id'er.</span><span class="sxs-lookup"><span data-stu-id="00cf3-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="00cf3-430">Plukke varer til salgsordrerne</span><span class="sxs-lookup"><span data-stu-id="00cf3-430">Pick items for the sales orders</span></span>

<span data-ttu-id="00cf3-431">Fuldfør det oprettede arbejde ved at bruge mobilenheden til at flytte varerne til pakkestationen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="00cf3-432">På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).</span><span class="sxs-lookup"><span data-stu-id="00cf3-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="00cf3-433">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="00cf3-434">I menuen **Udgående** skal du vælge **Salgspluk**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="00cf3-435">I feltet **Id** skal du angive det arbejds-id, der er oprettet for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="00cf3-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="00cf3-436">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-436">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-437">På siden **Salgsordrer – pluk** skal du angive et mål-NO, der blev oprettet til salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="00cf3-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="00cf3-438">Bemærk, at pluklokation (*batch-001*), vare (*A0001*) og antal (*2 stk.*) vises.</span><span class="sxs-lookup"><span data-stu-id="00cf3-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="00cf3-439">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-439">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-440">Gennemse oplysningerne på siden **Salgsordrer – læg på lager**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="00cf3-441">Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *Pakke*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="00cf3-442">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-442">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-443">På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde fuldført", hvilket angiver, at arbejds-id'et fra salgsordre 1 er blevet fuldført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="00cf3-444">Du skal nu plukke salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="00cf3-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="00cf3-445">I feltet **Id** skal du angive det arbejds-id, der er oprettet for salgsordre 2, hvor linje 1 har varen *A0001*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="00cf3-446">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-446">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-447">På siden **Salgsordrer – pluk** skal du angive en mål-NP.</span><span class="sxs-lookup"><span data-stu-id="00cf3-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="00cf3-448">Bemærk, at pluklokation (*batch-001*), vare (*A0001*) og antal (*1 stk.*) vises.</span><span class="sxs-lookup"><span data-stu-id="00cf3-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="00cf3-449">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-449">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-450">Gennemse oplysningerne på siden **Salgsordrer – læg på lager**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="00cf3-451">Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *Pakke*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="00cf3-452">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-452">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-453">På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde er fuldført".</span><span class="sxs-lookup"><span data-stu-id="00cf3-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="00cf3-454">Denne meddelelse angiver, at arbejds-id'et fra linje 1 i salgsordre 2 er fuldført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="00cf3-455">I feltet **Id** skal du angive det arbejds-id, der er oprettet for salgsordre 2, hvor linje 2 har varen *A0002*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="00cf3-456">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-456">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-457">På siden **Salgsordrer – pluk** skal du angive en mål-NP.</span><span class="sxs-lookup"><span data-stu-id="00cf3-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="00cf3-458">Bemærk, at pluklokation (*batch-002*), vare (*A0001*) og antal (*1 stk.*) vises.</span><span class="sxs-lookup"><span data-stu-id="00cf3-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="00cf3-459">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-459">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-460">Gennemse oplysningerne på siden **Salgsordrer – læg på lager**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="00cf3-461">Feltet **Lok** skal angive, at de plukkede varer skal placeres på lokationen *Pakke*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="00cf3-462">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-462">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-463">På siden **Scan et arbejds-id/nummerplade-id** modtager du en meddelelse om, at "Arbejde er fuldført".</span><span class="sxs-lookup"><span data-stu-id="00cf3-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="00cf3-464">Denne meddelelse angiver, at arbejds-id'et fra linje 2 i salgsordre 2 er fuldført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="00cf3-465">Pakke salgsordrer i containere</span><span class="sxs-lookup"><span data-stu-id="00cf3-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="00cf3-466">Pakke salgsordre 1 i containere</span><span class="sxs-lookup"><span data-stu-id="00cf3-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="00cf3-467">Gå til **Lokationsstyring \> Pakning og containerisering \> Pakke**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="00cf3-468">Dialogboksen **Vælg pakkestation** vises.</span><span class="sxs-lookup"><span data-stu-id="00cf3-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="00cf3-469">Som standard skal feltet **Arbejder** angives til navnet på den arbejder, som du konfigurerede tidligere.</span><span class="sxs-lookup"><span data-stu-id="00cf3-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="00cf3-470">Angiv følgende værdier for at få vist og arbejde med forsendelser og containere, der er planlagt på den specifikke pakkelokation:</span><span class="sxs-lookup"><span data-stu-id="00cf3-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="00cf3-471">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="00cf3-471">**Site:** *6*</span></span>
    - <span data-ttu-id="00cf3-472">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="00cf3-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="00cf3-473">**Lokation:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="00cf3-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="00cf3-474">**Pakkeprofil-id:** *Sorter*</span><span class="sxs-lookup"><span data-stu-id="00cf3-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="00cf3-475">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="00cf3-476">Gå til siden **Pakke**, og angiv mål-NP'en for salgsordre 1 i feltet **Nummerplade eller forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="00cf3-477">Vælg derefter tasten **Tabulator** eller **Retur** på tastaturet for at gå ud af feltet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="00cf3-478">Gå til handlingsruden, og vælg **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="00cf3-479">Accepter alle standardindstillinger, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="00cf3-480">Notér dig container-id'et.</span><span class="sxs-lookup"><span data-stu-id="00cf3-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="00cf3-481">I oversigtspanelet **Varepakning** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-482">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="00cf3-483">**Id:** Vare *A0001*</span><span class="sxs-lookup"><span data-stu-id="00cf3-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="00cf3-484">Gå til handlingsruden, og vælg **Luk container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="00cf3-485">I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="00cf3-486">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-486">Select **OK**.</span></span> <span data-ttu-id="00cf3-487">Containeren flyttes til lokationen *SORTER* og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="00cf3-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="00cf3-488">Opret en anden container for at føje den anden vare fra NP'en til salgsordre 1 til en ny container.</span><span class="sxs-lookup"><span data-stu-id="00cf3-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="00cf3-489">Gå til handlingsruden, og vælg **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="00cf3-490">Accepter alle standardindstillinger, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="00cf3-491">Notér dig container-id'et.</span><span class="sxs-lookup"><span data-stu-id="00cf3-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="00cf3-492">I oversigtspanelet **Varepakning** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-493">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="00cf3-494">**Id:** Vare *A0001*</span><span class="sxs-lookup"><span data-stu-id="00cf3-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="00cf3-495">Gå til handlingsruden, og vælg **Luk container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="00cf3-496">I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="00cf3-497">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-497">Select **OK**.</span></span> <span data-ttu-id="00cf3-498">Containeren flyttes til lokationen *SORTER* og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="00cf3-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="00cf3-499">Pakke salgsordre 2 i containere</span><span class="sxs-lookup"><span data-stu-id="00cf3-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="00cf3-500">Gå til siden **Pakke**, og angiv mål-NP'en for linje 1 i salgsordre 2 i feltet **Nummerplade eller forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="00cf3-501">Vælg derefter tasten **Tabulator** eller **Retur** på tastaturet for at gå ud af feltet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="00cf3-502">Gå til handlingsruden, og vælg **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="00cf3-503">Accepter alle standardindstillinger, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="00cf3-504">Notér dig container-id'et.</span><span class="sxs-lookup"><span data-stu-id="00cf3-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="00cf3-505">I oversigtspanelet **Varepakning** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-506">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="00cf3-507">**Id:** Vare *A0001*</span><span class="sxs-lookup"><span data-stu-id="00cf3-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="00cf3-508">Gå til handlingsruden, og vælg **Luk container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="00cf3-509">I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="00cf3-510">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-510">Select **OK**.</span></span> <span data-ttu-id="00cf3-511">Containeren flyttes til lokationen *SORTER* og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="00cf3-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="00cf3-512">I feltet **Nummerplade eller forsendelse** skal du angive mål-NP for linje i salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="00cf3-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="00cf3-513">Vælg derefter tasten **Tabulator** eller **Retur** på tastaturet for at gå ud af feltet.</span><span class="sxs-lookup"><span data-stu-id="00cf3-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="00cf3-514">Gå til handlingsruden, og vælg **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="00cf3-515">Accepter alle standardindstillinger, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="00cf3-516">Notér dig container-id'et.</span><span class="sxs-lookup"><span data-stu-id="00cf3-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="00cf3-517">I oversigtspanelet **Varepakning** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="00cf3-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="00cf3-518">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="00cf3-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="00cf3-519">**Id-felt:** Vare *A0002*</span><span class="sxs-lookup"><span data-stu-id="00cf3-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="00cf3-520">Gå til handlingsruden, og vælg **Luk container**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="00cf3-521">I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at få systemet til at opdatere feltet **Bruttovægt**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="00cf3-522">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-522">Select **OK**.</span></span> <span data-ttu-id="00cf3-523">Containeren flyttes til lokationen *SORTER* og er klar til sortering.</span><span class="sxs-lookup"><span data-stu-id="00cf3-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="00cf3-524">Hvis du vil have vist containerdetaljerne, skal du gå til **Lokationsstyring \> Pakning og containerisering \> Containere** og søge efter det container-id, der blev oprettet under pakning.</span><span class="sxs-lookup"><span data-stu-id="00cf3-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="00cf3-525">Sortere containerne</span><span class="sxs-lookup"><span data-stu-id="00cf3-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00cf3-526">Når du åbner menupunktet **Palle-build** i mobilappen for at udføre udgående sortering, vises en knap med teksten **Fuld**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="00cf3-527">*Brug ikke knappen **Fuld** til at sortere eller lukke positionen.*</span><span class="sxs-lookup"><span data-stu-id="00cf3-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="00cf3-528">Knappen **Fuld** er som standard tilgængelig og kan ikke deaktiveres eller fjernes fra siden.</span><span class="sxs-lookup"><span data-stu-id="00cf3-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="00cf3-529">Den bruges ikke til den funktionen *Udgående sortering*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="00cf3-530">Sortere den første beholder</span><span class="sxs-lookup"><span data-stu-id="00cf3-530">Sort the first container</span></span>

1. <span data-ttu-id="00cf3-531">På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).</span><span class="sxs-lookup"><span data-stu-id="00cf3-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="00cf3-532">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="00cf3-533">I menuen **Udgående** skal du vælge **Palle-build**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="00cf3-534">Angiv det første container-id, der er knyttet til salgsordre 1, i feltet **NP/con**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="00cf3-535">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-535">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-536">Da der ikke findes nogen sorteringspositioner i øjeblikket, skal du angive en.</span><span class="sxs-lookup"><span data-stu-id="00cf3-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="00cf3-537">I feltet **Sorteringsposition-id** skal du angive *SP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="00cf3-538">Da der i øjeblikket ikke er knyttet en NP til sorteringsplaceringen *SP01*, skal du angive en.</span><span class="sxs-lookup"><span data-stu-id="00cf3-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="00cf3-539">I feltet **NP** skal du angive *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="00cf3-540">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-540">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-541">Da validering af sorteringsposition er slået til, skal du angive id'et for for sorteringspositionen igen.</span><span class="sxs-lookup"><span data-stu-id="00cf3-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="00cf3-542">I feltet **Sorteringsposition-id** skal du angive *SP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="00cf3-543">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-543">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-544">Du modtager en meddelelse om, at "arbejde er fuldført".</span><span class="sxs-lookup"><span data-stu-id="00cf3-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="00cf3-545">Hvis du vil have vist sorteringspositionen og NP'en på den, skal du gå til **Lokationsstyring \> Pakning og containerisering \> Positionstildelinger for udgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="00cf3-546">Siden **Positionstildelinger for udgående sortering** vises alle de sorteringspositioner, der aktuelt er aktive.</span><span class="sxs-lookup"><span data-stu-id="00cf3-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="00cf3-547">I feltet **Sorteringspositionstransaktioner** vises den NP, der er knyttet til hver enkelt sorteringsposition, og de containere, der findes i sorteringsposition.</span><span class="sxs-lookup"><span data-stu-id="00cf3-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="00cf3-548">Bemærk, at der aktuelt findes én sorteringsposition, og at oversigtspanelet **Kriterier for sorteringsposition** viser et kriterium for **Forsendelsessted – fragtmand fly**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="00cf3-549">Sortere de resterende containerne</span><span class="sxs-lookup"><span data-stu-id="00cf3-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="00cf3-550">På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).</span><span class="sxs-lookup"><span data-stu-id="00cf3-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="00cf3-551">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="00cf3-552">I menuen **Udgående** skal du vælge **Palle-build**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="00cf3-553">Angiv det andet container-id, der er knyttet til salgsordre 1, i feltet **NP/con**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="00cf3-554">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-554">Select **OK**.</span></span> <span data-ttu-id="00cf3-555">Da sorteringsskabelonen er indstillet til automatisk sortering, og der allerede findes en sorteringsposition med overensstemmende kriterier, bliver du automatisk dirigeret til den korrekte sorteringsposition.</span><span class="sxs-lookup"><span data-stu-id="00cf3-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="00cf3-556">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-556">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-557">Bekræft sorteringspositions-id'et for at angive, at lageret er på det korrekte sted.</span><span class="sxs-lookup"><span data-stu-id="00cf3-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="00cf3-558">I feltet **Sorteringsposition-id** skal du angive *SP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="00cf3-559">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-559">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-560">Arbejdet er fuldført på den anden container fra salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="00cf3-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="00cf3-561">Du skal nu sortere de øvrige containere fra salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="00cf3-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="00cf3-562">Angiv container-id'et for containeren fra salgsordre 2, der indeholder vare **A0001**, i feltet *NP/con*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="00cf3-563">Da fragttjenesten er anderledes, bliver du bedt om at angive en ny sorteringsposition og tildele en NP til denne position.</span><span class="sxs-lookup"><span data-stu-id="00cf3-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="00cf3-564">Brug sorteringsposition *SP02* og NP *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="00cf3-565">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-565">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-566">Bekræft sorteringspositionen ved at angive *SP02* i feltet **Sorteringsposition-id**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="00cf3-567">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-567">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-568">Arbejdet på containeren er udført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="00cf3-569">Angiv container-id'et for den resterende container fra salgsordre 2, der indeholder vare **A0002**, i feltet *NP/con*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="00cf3-570">Da fragttjenesten er den samme som fragttjenesten for salgsordre 1, vil systemet vise den eksisterende sorteringsposition, der har de samme kriterier.</span><span class="sxs-lookup"><span data-stu-id="00cf3-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="00cf3-571">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-571">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-572">Bekræft sorteringspositionen ved at angive *SP01* i feltet **Sorteringsposition-id**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="00cf3-573">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-573">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-574">Arbejdet på containeren er udført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="00cf3-575">Luk positionerne for udgående sortering</span><span class="sxs-lookup"><span data-stu-id="00cf3-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="00cf3-576">Når alle lagre er sorteret, skal positionen lukkes, før der kan oprettes et arbejde.</span><span class="sxs-lookup"><span data-stu-id="00cf3-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="00cf3-577">Der oprettes sorteret lagerpluk for at føre lageret til lagerporten.</span><span class="sxs-lookup"><span data-stu-id="00cf3-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="00cf3-578">Lukke en position fra mobilenheden</span><span class="sxs-lookup"><span data-stu-id="00cf3-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="00cf3-579">På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).</span><span class="sxs-lookup"><span data-stu-id="00cf3-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="00cf3-580">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="00cf3-581">I menuen **Udgående** skal du vælge **Palle-build**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="00cf3-582">I feltet **NP/con** skal du angive et container-id, der blev sorteret til sorteringsposition *SP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="00cf3-583">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-583">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-584">Du får vist følgende meddelelse: "Containeren er allerede sorteret til position SP01.</span><span class="sxs-lookup"><span data-stu-id="00cf3-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="00cf3-585">Vil du lukke positionen?"</span><span class="sxs-lookup"><span data-stu-id="00cf3-585">Close the position?"</span></span> <span data-ttu-id="00cf3-586">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-586">Select **Close**.</span></span>

    <span data-ttu-id="00cf3-587">Arbejde er fuldført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="00cf3-588">Luk en position fra positionstildeling for udgående sortering</span><span class="sxs-lookup"><span data-stu-id="00cf3-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="00cf3-589">Gå til **Lagerlokation \> Pakning og containerisering \> Positonstildelinger for udgående sortering**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="00cf3-590">I den venstre kolonne skal du vælge **SP02**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="00cf3-591">Denne position for udgående sortering er den, du vil lukke.</span><span class="sxs-lookup"><span data-stu-id="00cf3-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="00cf3-592">Gå til handlingsruden, og vælg **Luk position**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="00cf3-593">Posten med sorteringspositionen er lukket og vises ikke længere.</span><span class="sxs-lookup"><span data-stu-id="00cf3-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="00cf3-594">Marker afkrydsningsfeltet **Vis lukket** for at få vist alle lukkede positionsposter.</span><span class="sxs-lookup"><span data-stu-id="00cf3-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="00cf3-595">Sorteret lagerplukning</span><span class="sxs-lookup"><span data-stu-id="00cf3-595">Sorted inventory picking</span></span>

<span data-ttu-id="00cf3-596">Du skal fuldføre arbejdet med sorteret lagerpluk.</span><span class="sxs-lookup"><span data-stu-id="00cf3-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="00cf3-597">Når den er fuldført, plukkes lageret til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="00cf3-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="00cf3-598">På dette tidspunkt gælder alle andre lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="00cf3-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="00cf3-599">På mobilenheden skal du logge på lagerstedet *62* ved hjælp af det bruger-id, du har oprettet til dette scenarie (eller bruger-id'et for en eksisterende bruger af demodata).</span><span class="sxs-lookup"><span data-stu-id="00cf3-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="00cf3-600">I hovedmenuen skal du vælge **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="00cf3-601">I menuen **Udgående** skal du vælge **Sortering efter last fra**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="00cf3-602">Angiv destinationens-NP-id fra den første sorteringsposition, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="00cf3-603">Angiv feltet **Id** til *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="00cf3-604">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-604">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-605">Siden **Sorteret lagerpluk: pluk** viser det plukarbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="00cf3-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="00cf3-606">Pluk fra lokationen *SORTER* og mål-NP *PLP01*, der har flere varer og et antal på *3*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="00cf3-607">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-607">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-608">Siden **Sorteret lagerpluk: læg på lager** viser det læg på lager-arbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="00cf3-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="00cf3-609">Læg på lager til lokationen *Lagerport* og mål-NP *PLP01*, der har flere varer og et antal på *3*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="00cf3-610">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-610">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-611">Arbejde er fuldført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-611">Work is completed.</span></span>

1. <span data-ttu-id="00cf3-612">Angiv destinationsnummerplade-id'et fra den anden sorteringsposition, *SP02*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="00cf3-613">Angiv feltet **Id** til *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="00cf3-614">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-614">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-615">Siden **Sorteret lagerpluk: pluk** viser det plukarbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="00cf3-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="00cf3-616">Pluk fra lokationen *SORTER* og mål-NP *PLP02*, der har flere varer og et antal på *1*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="00cf3-617">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-617">Select **OK**.</span></span>
1. <span data-ttu-id="00cf3-618">Siden **Sorteret lagerpluk: læg på lager** viser det læg på lager-arbejde, der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="00cf3-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="00cf3-619">Læg på lager til lokationen *Lagerport* og mål-NP *PLP02*, der har flere varer og et antal på *1*.</span><span class="sxs-lookup"><span data-stu-id="00cf3-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="00cf3-620">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="00cf3-620">Select **OK**.</span></span>

    <span data-ttu-id="00cf3-621">Arbejde er fuldført.</span><span class="sxs-lookup"><span data-stu-id="00cf3-621">Work is completed.</span></span>

<span data-ttu-id="00cf3-622">Fra dette tidspunkt gælder alle andre lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="00cf3-622">From this point forward, all other warehouse processes apply.</span></span>
