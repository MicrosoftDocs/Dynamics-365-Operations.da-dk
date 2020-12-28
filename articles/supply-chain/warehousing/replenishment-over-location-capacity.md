---
title: Genopfyldning over lokationskapacitet
description: Dette emne indeholder oplysninger om funktionen Genopfyldning over lokationskapacitet. Denne funktion aktiverer alt genopfyldningsarbejde, der kræves for dagen, der skal oprettes, og styrer tilgængeligheden af genbestillingsarbejdet for at sikre, at plukpladsen ikke løber tør for lager eller overstiger kapaciteten.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425018"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="dc459-104">Genopfyldning over lokationskapacitet</span><span class="sxs-lookup"><span data-stu-id="dc459-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc459-105">Nogle store eller pladsbegrænsende lagersteder skal levere et større antal varer på en dag, end der er plads til på plukpladsen.</span><span class="sxs-lookup"><span data-stu-id="dc459-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="dc459-106">Funktionen *Genopfyldning over lokationskapacitet* aktiverer alt genopfyldningsarbejde, der kræves for dagen, der skal oprettes, og styrer tilgængeligheden af genbestillingsarbejdet for at sikre, at plukpladsen ikke løber tør for lager eller overstiger kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="dc459-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="dc459-107">Funktionen gør det muligt at oprette mere genopfyldningsarbejde, end der er plads til på en lokation, og den blokerer genopfyldningsarbejde i at blive fuldført, når lokationen er fuld.</span><span class="sxs-lookup"><span data-stu-id="dc459-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="dc459-108">Efterhånden som lager på plukpladsen falder under en konfigurerbar grænse, bliver det mere genopfyldningsarbejde tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="dc459-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="dc459-109">Aktivere funktionen Genopfyldning over lokationskapacitet</span><span class="sxs-lookup"><span data-stu-id="dc459-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="dc459-110">Hvis du vil gøre denne funktion tilgængelig, skal du aktivere følgende funktioner i [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rækkefølge):</span><span class="sxs-lookup"><span data-stu-id="dc459-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="dc459-111">Blokering af arbejde i hele organisationen</span><span class="sxs-lookup"><span data-stu-id="dc459-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="dc459-112">Genopfyldning over lokationskapacitet</span><span class="sxs-lookup"><span data-stu-id="dc459-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="dc459-113">Konfigurere funktionen til eksempelscenariet</span><span class="sxs-lookup"><span data-stu-id="dc459-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="dc459-114">Dette afsnit indeholder retningslinjer og et eksempel, der viser, hvordan du kan konfigurere denne funktion og forberede eksempeldata til det eksempelscenario, der er angivet senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="dc459-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="dc459-115">Aktivér eksempeldata</span><span class="sxs-lookup"><span data-stu-id="dc459-115">Enable sample data</span></span>

<span data-ttu-id="dc459-116">Hvis du vil arbejde dig gennem [eksempelscenariet](#example-scenario) ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="dc459-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="dc459-117">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="dc459-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="dc459-118">Lokationsprofil</span><span class="sxs-lookup"><span data-stu-id="dc459-118">Location profile</span></span>

<span data-ttu-id="dc459-119">Aktivér funktionen til genopfyldning over kapacitet på lokationsprofilen.</span><span class="sxs-lookup"><span data-stu-id="dc459-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="dc459-120">Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="dc459-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="dc459-121">Vælg **PICK-06** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="dc459-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="dc459-122">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dc459-123">I oversigtspanelet **Genopfyldning** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="dc459-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="dc459-124">**Overstiger lokationskapacitet:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dc459-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="dc459-125">Når indstillingen er aktiveret, kan den maksimale kapacitet for lokationen overskrides med genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="dc459-126">Dette aktiverer også andre felter i oversigtspanelet **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="dc459-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="dc459-127">**Grænsetype for arbejdstilgængelighed:** *Antal*</span><span class="sxs-lookup"><span data-stu-id="dc459-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="dc459-128">Dette felt definerer den metode, der bruges til at bestemme, hvornår der skal frigives mere arbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="dc459-129">Du kan frigive enten procentsats eller antal:</span><span class="sxs-lookup"><span data-stu-id="dc459-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="dc459-130">*Procent* – Vælg denne indstilling for at bruge den procentvise kapacitet, der er baseret på lagergrænser eller volumenmålinger.</span><span class="sxs-lookup"><span data-stu-id="dc459-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="dc459-131">Hvis du vælger denne indstilling , aktiveres feltet **Overløbsprocent**, og det deaktiverer de to relaterede felter af typen antal, **Overløbsantal** og **Overløbsenhed**.</span><span class="sxs-lookup"><span data-stu-id="dc459-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="dc459-132">Du kan bruge denne indstilling, hvis plukpladserne bruger volumenmålinger.</span><span class="sxs-lookup"><span data-stu-id="dc459-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="dc459-133">Hvis denne indstilling er valgt, skal du angive feltet **Overløbsprocent** til den procentdel, hvor der skal være mere tilgængeligt genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="dc459-134">*Antal* – Vælg denne indstilling for at bruge en bestemt antalsværdi.</span><span class="sxs-lookup"><span data-stu-id="dc459-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="dc459-135">Hvis du vælger denne indstilling , deaktiveres feltet **Overløbsprocent**, og det aktiverer felterne **Overløbsantal** og **Overløbsenhed**.</span><span class="sxs-lookup"><span data-stu-id="dc459-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="dc459-136">Brug denne indstilling, når du ikke bruger volumenmålinger til de pladser, der genopfyldes, eller når du har ensartede mængder, der skal tilføres mere lager på pladsen.</span><span class="sxs-lookup"><span data-stu-id="dc459-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="dc459-137">Hvis denne indstilling er valgt, skal du angive felterne **Overløbsantal** og **Overløbsenhed** til det antal og den enhed, hvor mere genopfyldningsarbejde skal være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="dc459-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="dc459-138">**Overløb i antal:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="dc459-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="dc459-139">Dette felt definerer det antal, hvormed pladsen overløber.</span><span class="sxs-lookup"><span data-stu-id="dc459-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="dc459-140">Arbejde vil være tilgængeligt, når summen af lagerbeholdningen på pladsen og arbejdsantallet er under denne værdi.</span><span class="sxs-lookup"><span data-stu-id="dc459-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="dc459-141">En eventuel genopfyldning over denne værdi blokeres og skal ophæves manuelt.</span><span class="sxs-lookup"><span data-stu-id="dc459-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="dc459-142">Grænser for lokalitetslagring tages i betragtning ved beregning af arbejdsantallet.</span><span class="sxs-lookup"><span data-stu-id="dc459-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="dc459-143">**Overløbsenhed:** *PL*</span><span class="sxs-lookup"><span data-stu-id="dc459-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="dc459-144">I dette felt defineres den enhed, der er knyttet til overløbsantallet.</span><span class="sxs-lookup"><span data-stu-id="dc459-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="dc459-145">I dette tilfælde gøres der mere genopfyldningsarbejde tilgængeligt, når lokationen kommer ned på 0,65 palle (PL).</span><span class="sxs-lookup"><span data-stu-id="dc459-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="dc459-146">**Overløb i procent**</span><span class="sxs-lookup"><span data-stu-id="dc459-146">**Overflow percentage**</span></span>

        <span data-ttu-id="dc459-147">Dette felt definerer den procent, hvormed pladsen overløber.</span><span class="sxs-lookup"><span data-stu-id="dc459-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="dc459-148">Arbejde vil være tilgængeligt, når summen af lagerbeholdningen på pladsen og arbejdsantallet er under denne procent.</span><span class="sxs-lookup"><span data-stu-id="dc459-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="dc459-149">En eventuel arbejdsmængde i procent for arbejdet ved genopfyldning over denne værdi blokeres og skal ophæves manuelt.</span><span class="sxs-lookup"><span data-stu-id="dc459-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="dc459-150">Grænser for lokalitetslagring tages i betragtning ved beregning af arbejdsantallet i procent.</span><span class="sxs-lookup"><span data-stu-id="dc459-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="dc459-151">Hvis der ikke er defineret grænser for lokationslagring, beregnes procenten af arbejdsmængden efter volumen, hvis der er defineret volumenbegrænsninger på lokationsprofilen.</span><span class="sxs-lookup"><span data-stu-id="dc459-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc459-152">Hvis du bruger demodataene til den juridiske enhed **USMF** og tidligere har aktiveret funktionen *Placering af lokations-id*, skal du deaktivere indstillingen **Aktivér placering af id** for lokationsprofilen **MASSE-06** for at fuldføre de mobile trin i eksempelscenariet.</span><span class="sxs-lookup"><span data-stu-id="dc459-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="dc459-153">Kode for bølgetrin</span><span class="sxs-lookup"><span data-stu-id="dc459-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="dc459-154">Hvis du vil oprette en bølgetrinkode som beskrevet her, skal du muligvis først bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere funktionen med navnet *Bølgetrinkode for hele organisationen*.</span><span class="sxs-lookup"><span data-stu-id="dc459-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="dc459-155">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinkoder**.</span><span class="sxs-lookup"><span data-stu-id="dc459-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="dc459-156">Vælg **Ny**, og angiv derefter følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="dc459-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="dc459-157">**Kode for bølgetrin:** *Genopfyld*</span><span class="sxs-lookup"><span data-stu-id="dc459-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="dc459-158">**Bølgetrinsbeskrivelse:** *Genopfyldning*</span><span class="sxs-lookup"><span data-stu-id="dc459-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="dc459-159">**Bølgetrinstype:** *Genopfyldning*</span><span class="sxs-lookup"><span data-stu-id="dc459-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="dc459-160">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc459-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="dc459-161">Genopfyldningsskabelon</span><span class="sxs-lookup"><span data-stu-id="dc459-161">Replenishment template</span></span>

<span data-ttu-id="dc459-162">Genopfyldningsskabeloner er et sæt regler, der styrer, hvornår og hvordan en lokation skal genopfyldes.</span><span class="sxs-lookup"><span data-stu-id="dc459-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="dc459-163">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="dc459-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="dc459-164">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dc459-165">Vælg den linje, hvor feltet **Genopfyldningsskabelon** er angivet til **Genopfyldning af behov** i sektionen *Oversigt*.</span><span class="sxs-lookup"><span data-stu-id="dc459-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="dc459-166">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="dc459-166">Set the following values:</span></span>

    - <span data-ttu-id="dc459-167">**Kode for bølgetrin:** *Genopfyld*</span><span class="sxs-lookup"><span data-stu-id="dc459-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="dc459-168">**Tillad bølgeefterspørgsel at bruge ikke-reserverede antal:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="dc459-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="dc459-169">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc459-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="dc459-170">Bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="dc459-170">Wave template</span></span>

1. <span data-ttu-id="dc459-171">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="dc459-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="dc459-172">I venstre rude skal du angive feltet **Bølgeskabelontype** til *Forsendelse*.</span><span class="sxs-lookup"><span data-stu-id="dc459-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="dc459-173">Vælg skabelonen **61 Forsendelse** på listen.</span><span class="sxs-lookup"><span data-stu-id="dc459-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="dc459-174">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="dc459-175">Brug oversigtspanelet **Generelt** til at angive indstillingen **Automatiser frigivelse af genopfyldningsarbejde** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="dc459-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="dc459-176">Angiv denne indstilling til *Ja* for at oprette behovsbaseret genopfyldningsarbejde og frigive det automatisk.</span><span class="sxs-lookup"><span data-stu-id="dc459-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="dc459-177">Du skal føje genbestillingsbølgemetoden til bølgeskabelonen og oprette en genbestillingsskabelon af typen **Bølgebehov**.</span><span class="sxs-lookup"><span data-stu-id="dc459-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="dc459-178">Konfigurer en genopfyldningsskabelon på siden **Genopfyldningsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="dc459-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="dc459-179">Hvis du vil konfigurere en genopfyldningsskabelon, skal du føje genopfyldningsmetoden til bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="dc459-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="dc459-180">Find følgende linje i kolonnen **Valgte metoder** i oversigtspanelet **Metoder**:</span><span class="sxs-lookup"><span data-stu-id="dc459-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="dc459-181">**Metodenavn:** *Genopfyld*</span><span class="sxs-lookup"><span data-stu-id="dc459-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="dc459-182">**Navn:** *Genopfyldning*</span><span class="sxs-lookup"><span data-stu-id="dc459-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="dc459-183">Indstil feltet **Kode for bølgetrin** for denne linje til *Genopfyld*.</span><span class="sxs-lookup"><span data-stu-id="dc459-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="dc459-184">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc459-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="dc459-185">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="dc459-185">Example scenario</span></span>

<span data-ttu-id="dc459-186">Når du har gjort alle de tidligere nævnte eksempeldata tilgængelige og konfigureret dem, kan du arbejde gennem dette scenario for at afprøve funktionen *Genopfyldning over lokationskapacitet*.</span><span class="sxs-lookup"><span data-stu-id="dc459-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="dc459-187">De værdier, der vises i dette scenarie, forudsætter, at du arbejder med standarddemodataene, at du har valgt **USMF** som juridisk enhed, og at du har forberedt de eksempelposter, der er beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="dc459-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="dc459-188">Dette scenario fungerer også som et eksempel, der viser, hvordan funktionen kan bruges i en produktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="dc459-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="dc459-189">Opret genopfyldningsarbejde</span><span class="sxs-lookup"><span data-stu-id="dc459-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="dc459-190">Opret salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="dc459-190">Create sales order 1</span></span>

1. <span data-ttu-id="dc459-191">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="dc459-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dc459-192">I handlingsruden skal du vælge **Ny** for at åbne dialogboksen Opret ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="dc459-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="dc459-193">I dialogboksen skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="dc459-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="dc459-194">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="dc459-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="dc459-195">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="dc459-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="dc459-196">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc459-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="dc459-197">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="dc459-197">The new sales order is opened.</span></span> <span data-ttu-id="dc459-198">Den indeholder en ny tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="dc459-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dc459-199">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="dc459-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="dc459-200">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="dc459-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="dc459-201">**Antal:** *40*</span><span class="sxs-lookup"><span data-stu-id="dc459-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="dc459-202">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="dc459-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="dc459-203">På siden **Reservation** skal du vælge **Reservér parti**.</span><span class="sxs-lookup"><span data-stu-id="dc459-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="dc459-204">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc459-204">Close the page.</span></span>
1. <span data-ttu-id="dc459-205">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="dc459-206">Du modtager orienterende meddelelser, der viser bølgen og forsendelses-id'et, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="dc459-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="dc459-207">Der oprettes også en genopfyldningsbølge.</span><span class="sxs-lookup"><span data-stu-id="dc459-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="dc459-208">Du får også vist en advarselsmeddelelse om, at "Arbejde-id XXXX ikke kan ophæves, fordi det ikke har fuldført genopfyldningsarbejde".</span><span class="sxs-lookup"><span data-stu-id="dc459-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="dc459-209">Opret salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="dc459-209">Create sales order 2</span></span>

1. <span data-ttu-id="dc459-210">I handlingsruden på siden **Alle salgsordrer** skal du vælge **Ny** for at åbne dialogboksen Opret ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="dc459-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="dc459-211">I dialogboksen skal du angive følgende værdi:</span><span class="sxs-lookup"><span data-stu-id="dc459-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="dc459-212">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="dc459-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="dc459-213">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="dc459-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="dc459-214">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc459-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="dc459-215">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="dc459-215">The new sales order is opened.</span></span> <span data-ttu-id="dc459-216">Den indeholder en ny tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="dc459-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dc459-217">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="dc459-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="dc459-218">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="dc459-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="dc459-219">**Antal:** *60*</span><span class="sxs-lookup"><span data-stu-id="dc459-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="dc459-220">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="dc459-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="dc459-221">På siden **Reservation** skal du vælge **Reservér parti**.</span><span class="sxs-lookup"><span data-stu-id="dc459-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="dc459-222">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc459-222">Close the page.</span></span>
1. <span data-ttu-id="dc459-223">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="dc459-224">Du modtager orienterende meddelelser, der viser bølgen og forsendelses-id'et, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="dc459-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="dc459-225">Der oprettes også en genopfyldningsbølge.</span><span class="sxs-lookup"><span data-stu-id="dc459-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="dc459-226">Du får også vist en advarselsmeddelelse om, at "Arbejde-id XXXX ikke kan ophæves, fordi det ikke har fuldført genopfyldningsarbejde".</span><span class="sxs-lookup"><span data-stu-id="dc459-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="dc459-227">Opret salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="dc459-227">Create sales order 3</span></span>

1. <span data-ttu-id="dc459-228">I handlingsruden på siden **Alle salgsordrer** skal du vælge **Ny** for at åbne dialogboksen Opret ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="dc459-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="dc459-229">I dialogboksen skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="dc459-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="dc459-230">**Debitorkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="dc459-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="dc459-231">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="dc459-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="dc459-232">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc459-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="dc459-233">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="dc459-233">The new sales order is opened.</span></span> <span data-ttu-id="dc459-234">Den indeholder en ny tom linje i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="dc459-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dc459-235">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="dc459-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="dc459-236">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="dc459-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="dc459-237">**Antal:** *30*</span><span class="sxs-lookup"><span data-stu-id="dc459-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="dc459-238">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="dc459-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="dc459-239">På siden **Reservation** skal du vælge **Reservér parti**.</span><span class="sxs-lookup"><span data-stu-id="dc459-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="dc459-240">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc459-240">Close the page.</span></span>
1. <span data-ttu-id="dc459-241">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="dc459-242">Du modtager orienterende meddelelser, der viser bølgen og forsendelses-id'et, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="dc459-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="dc459-243">Der oprettes også en genopfyldningsbølge.</span><span class="sxs-lookup"><span data-stu-id="dc459-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="dc459-244">Du får også vist en advarselsmeddelelse om, at "Arbejde-id XXXX ikke kan ophæves, fordi det ikke har fuldført genopfyldningsarbejde".</span><span class="sxs-lookup"><span data-stu-id="dc459-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="dc459-245">Se arbejdsdetaljer</span><span class="sxs-lookup"><span data-stu-id="dc459-245">View work details</span></span>

1. <span data-ttu-id="dc459-246">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="dc459-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="dc459-247">Filtrer **Lagersted**-kolonnen for lagerstedet **61** i sektionen *Oversigt*.</span><span class="sxs-lookup"><span data-stu-id="dc459-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="dc459-248">Du bør se, at der er oprettet syv arbejds-id'er for de tre behovssalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="dc459-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="dc459-249">Tre af de syv arbejds-id'er har en **Arbejdsordretype**-værdi for *Genopfyldning*, og fire har en **Arbejdsordretype**-værdi for *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="dc459-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="dc459-250">Alle tre arbejds-id'er, der har **Arbejdsordretype**-værdien *Genopfyldning*, har samme *Pluk* og *Læg på lager*-placeringer i afsnittet **Linjer**:</span><span class="sxs-lookup"><span data-stu-id="dc459-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="dc459-251">**Pluk:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="dc459-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="dc459-252">**Læg på lager:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="dc459-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="dc459-253">Der er oprettet to arbejds-id'er for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dc459-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="dc459-254">Notér arbejds-id'erne for salgsordrene.</span><span class="sxs-lookup"><span data-stu-id="dc459-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="dc459-255">Afhængigt af de disponible antal kan de arbejdsantal, der oprettes, variere en smule.</span><span class="sxs-lookup"><span data-stu-id="dc459-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="dc459-256">De overordnede arbejdsoverskrifter, der oprettes, skal dog svare til dette scenarieeksempel.</span><span class="sxs-lookup"><span data-stu-id="dc459-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="dc459-257">Id for disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="dc459-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="dc459-258">Senere i dette scenario skal du bruge appen Lagersted (eller en emulator), hvor du skal identificere id'et for at fuldføre pluk- og genopfyldningsscenarierne.</span><span class="sxs-lookup"><span data-stu-id="dc459-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="dc459-259">Du kan finde de id'er, du skal bruge, senere ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="dc459-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="dc459-260">Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.</span><span class="sxs-lookup"><span data-stu-id="dc459-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="dc459-261">Vælg knappen **Vis filtre** for at åbne filterruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="dc459-262">Angiv følgende filtreringskriterier for at få id'erne til scenariet.</span><span class="sxs-lookup"><span data-stu-id="dc459-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="dc459-263">Brug filteret *begynder med*.</span><span class="sxs-lookup"><span data-stu-id="dc459-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="dc459-264">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="dc459-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="dc459-265">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="dc459-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="dc459-266">Vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="dc459-266">Select **Apply**.</span></span>
1. <span data-ttu-id="dc459-267">Vælg **Dimensioner** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc459-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="dc459-268">Vælg alle værdierne i sektionen **Lagringsdimensioner** i dialogboksen **Dimensionsvisning**.</span><span class="sxs-lookup"><span data-stu-id="dc459-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="dc459-269">I afsnittet **Transaktioner** skal du vælge **Varenummer** og **Antal \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="dc459-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="dc459-270">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc459-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="dc459-271">**Beholdning**-gitteret viser id-numrene for varen *T0100* på hver lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="dc459-272">Notér dig det id, der findes på hver lokation, da du skal bruge disse oplysninger senere.</span><span class="sxs-lookup"><span data-stu-id="dc459-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="dc459-273">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc459-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="dc459-274">Procestrin</span><span class="sxs-lookup"><span data-stu-id="dc459-274">Process steps</span></span>

<span data-ttu-id="dc459-275">Du skal udføre genopfyldning af lagerstedet for de første to arbejds-id'er.</span><span class="sxs-lookup"><span data-stu-id="dc459-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="dc459-276">Arbejdet på det tredje genopfyldningsarbejde blokeres, indtil lagerniveauet på plukpladsen falder under grænsen.</span><span class="sxs-lookup"><span data-stu-id="dc459-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="dc459-277">Opfyldning</span><span class="sxs-lookup"><span data-stu-id="dc459-277">Replenishment</span></span>

1. <span data-ttu-id="dc459-278">Log på lagerstedsappen som en bruger på lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="dc459-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="dc459-279">(Angiv *61* som bruger-id og *1* som adgangskode).</span><span class="sxs-lookup"><span data-stu-id="dc459-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="dc459-280">Gå til **Lager \> Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="dc459-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="dc459-281">Du bliver bedt om at fuldføre det første genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="dc459-282">Varenummeret, antallet og pluklokationen vises.</span><span class="sxs-lookup"><span data-stu-id="dc459-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="dc459-283">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="dc459-284">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="dc459-285">Systemet opretter et id-nummer til målet for det nye id til den plukkede vare.</span><span class="sxs-lookup"><span data-stu-id="dc459-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="dc459-286">Vælg **OK** for at bekræfte værdien.</span><span class="sxs-lookup"><span data-stu-id="dc459-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="dc459-287">Der vises et læg på lager-arbejde, som beder brugeren om at anbringe en mål-id'et på genopfyldningspladsen.</span><span class="sxs-lookup"><span data-stu-id="dc459-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="dc459-288">Pladsen *Læg på lager* skal være **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="dc459-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="dc459-289">Bekræft læg på lager-oplysningerne, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="dc459-290">Du får vist meddelelsen "Arbejde fuldført", og detaljerne i den næste plukopgave til genopfyldning vises: varenummeret, antallet og lokationen, der skal plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="dc459-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="dc459-291">Plukpladsen vil være den samme som den første genopfyldningsplads.</span><span class="sxs-lookup"><span data-stu-id="dc459-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="dc459-292">Derfor vil id'et være det samme nummer, der blev brugt til den første arbejdsopgave for genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="dc459-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="dc459-293">Gentag de foregående trin for at fuldføre genopfyldningsarbejdet for den anden arbejdsopgave.</span><span class="sxs-lookup"><span data-stu-id="dc459-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="dc459-294">Antallet og mål-id'et licens vil være forskellig fra antallet og mål-id'et for den første arbejdsopgave.</span><span class="sxs-lookup"><span data-stu-id="dc459-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="dc459-295">Når det andet genopfyldningsarbejde er fuldført, vises meddelelsen "Arbejde fuldført".</span><span class="sxs-lookup"><span data-stu-id="dc459-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="dc459-296">Din mobilenhed informerer dig også om, at der ikke er noget arbejde tilgængeligt, også selvom noget genopfyldningsarbejde resterer.</span><span class="sxs-lookup"><span data-stu-id="dc459-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="dc459-297">Dette problem opstår, fordi genopfyldningsarbejdet har tilgængelighedsstatussen *På hold* og derfor er markeret som **Blokeret**.</span><span class="sxs-lookup"><span data-stu-id="dc459-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="dc459-298">*På hold*-status blev udløst, fordi lokationsprofilen for den plukplads, som arbejdet tildeles, har en **Overløbsantals**-værdi på *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="dc459-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="dc459-299">De to tidligere opgaver for genopfyldningsarbejde har udfyldt lokationen næsten til dens overløbsgrænse for vare *T0100*.</span><span class="sxs-lookup"><span data-stu-id="dc459-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="dc459-300">(Enhedsomregningen for varen er *1 PL = 100 hver*). Derfor vil det resterende genopfyldningsarbejde medføre, at lokationen overskrider dens overløbsgrænse.</span><span class="sxs-lookup"><span data-stu-id="dc459-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="dc459-301">Indtil der er plukket tilstrækkeligt med lagervarer fra lokationen, så de kommer under grænsen for arbejdsfrigivelsen i menupunktet for mobilenheden, forbliver dette genopfyldningsarbejde blokeret.</span><span class="sxs-lookup"><span data-stu-id="dc459-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="dc459-302">Salgsordrepluk</span><span class="sxs-lookup"><span data-stu-id="dc459-302">Sales order pick</span></span>

<span data-ttu-id="dc459-303">Før den resterende genopfyldningsarbejdsopgave kan fuldføres, skal plukpladsen tømmes for lager til et niveau, hvor blokering af det resterende genopfyldningsarbejde kan ophæves.</span><span class="sxs-lookup"><span data-stu-id="dc459-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="dc459-304">Det vil sige, at summen af antallet af disponible lagerbeholdninger på lokationen og genopfyldningsantallet ikke overstiger værdien af **Overløbsantal**.</span><span class="sxs-lookup"><span data-stu-id="dc459-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="dc459-305">Når denne sum er mindre end overløbsantallet, fjernes spærringen af det resterende genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="dc459-306">Log på lagerstedsappen som en bruger på lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="dc459-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="dc459-307">(Angiv *61* som bruger-id og *1* som adgangskode).</span><span class="sxs-lookup"><span data-stu-id="dc459-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="dc459-308">Gå til **Udgående \> Salgsplukning**.</span><span class="sxs-lookup"><span data-stu-id="dc459-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="dc459-309">Angiv første arbejds-id for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dc459-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="dc459-310">Se arbejds-id'erne for de salgsordrer, du har noteret tidligere, på siden **Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="dc459-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="dc459-311">Det arbejds-id, du angiver her, genererer plukarbejde for et antal på 10 hver fra to forskellige lokationer.</span><span class="sxs-lookup"><span data-stu-id="dc459-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="dc459-312">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-312">Select **OK**.</span></span>

    <span data-ttu-id="dc459-313">Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra for den første lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="dc459-314">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="dc459-315">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="dc459-316">Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra for den næste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="dc459-317">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="dc459-318">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="dc459-319">**Salgsordrer: Læg på lager**-siden giver dig besked på at lægge begge fuldførte plukarbejder til den udgående lokation for midlertidig lagring.</span><span class="sxs-lookup"><span data-stu-id="dc459-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="dc459-320">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-320">Select **OK**.</span></span>

    <span data-ttu-id="dc459-321">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc459-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="dc459-322">Angiv andet arbejds-id for salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="dc459-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="dc459-323">Der er kun én plukopgave for dette arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="dc459-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="dc459-324">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-324">Select **OK**.</span></span>

    <span data-ttu-id="dc459-325">Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="dc459-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="dc459-326">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="dc459-327">Det id, du angiver, vil være et af de systemgenererede id'er fra arbejdsopgaverne for genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="dc459-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="dc459-328">Hvis du vil være sikker på, at du indlæser det korrekte id, skal du kontrollere lageret på siden **Beholdningsliste** for varen, lokationen og antallet.</span><span class="sxs-lookup"><span data-stu-id="dc459-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="dc459-329">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="dc459-330">Bekræft instruktionerne til læg på lager-opgaven på den udgående midlertidige lagring.</span><span class="sxs-lookup"><span data-stu-id="dc459-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="dc459-331">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-331">Select **OK**.</span></span>

    <span data-ttu-id="dc459-332">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc459-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="dc459-333">Salgsordre 2 er spærret for pluk, fordi genopfyldningsopgaven, som den er knyttet til, ikke er fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc459-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="dc459-334">Der er i øjeblikket stadig et antal på 30 hver på plukpladsen, og genopfyldningsantallet for salgsordre 2 er 60 hver.</span><span class="sxs-lookup"><span data-stu-id="dc459-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="dc459-335">Summen af disponibel lagerbeholdning og genopfyldningslageret (90 hver) overskrider overløbsantallet på 0,65 PL (eller 65 hver).</span><span class="sxs-lookup"><span data-stu-id="dc459-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="dc459-336">Salgsordre 3 skal plukkes, før genopfyldningsarbejdet kan fuldføres.</span><span class="sxs-lookup"><span data-stu-id="dc459-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="dc459-337">Angiv arbejds-id for salgsordre 3.</span><span class="sxs-lookup"><span data-stu-id="dc459-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="dc459-338">Der er kun én plukopgave for dette arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="dc459-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="dc459-339">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-339">Select **OK**.</span></span>

    <span data-ttu-id="dc459-340">Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="dc459-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="dc459-341">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="dc459-342">Det id, du angiver, vil være et af de systemgenererede id'er fra arbejdsopgaverne for genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="dc459-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="dc459-343">Hvis du vil være sikker på, at du indlæser det korrekte id, skal du kontrollere lageret på siden **Beholdningsliste** for varen, lokationen og antallet.</span><span class="sxs-lookup"><span data-stu-id="dc459-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="dc459-344">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="dc459-345">Bekræft instruktionerne til læg på lager-opgaven på den udgående midlertidige lagring.</span><span class="sxs-lookup"><span data-stu-id="dc459-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="dc459-346">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-346">Select **OK**.</span></span>

    <span data-ttu-id="dc459-347">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc459-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="dc459-348">Så snart summen af det disponible antal på plukpladsen og opfyldningsantallet er under grænsen, vil du kunne behandle det resterende genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="dc459-349">Vend tilbage til siden **Arbejdsdetaljer**, og bemærk, at tilgængeligheden af genopfyldningsarbejde for det sidste stykke genopfyldning (for salgsordre 2) er *Åben*, fordi der nu er tilstrækkelig plads på lokationen til at acceptere genopfyldningen.</span><span class="sxs-lookup"><span data-stu-id="dc459-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="dc459-350">Du kan nu behandle dette genopfyldningsarbejde via mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="dc459-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="dc459-351">Gå til **Lager \> Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="dc459-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="dc459-352">Du bliver bedt om at fuldføre det resterende genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="dc459-353">Varenummeret, antallet og pluklokationen vises.</span><span class="sxs-lookup"><span data-stu-id="dc459-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="dc459-354">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="dc459-355">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="dc459-356">Systemet opretter et id-nummer til målet for det nye id til den plukkede vare.</span><span class="sxs-lookup"><span data-stu-id="dc459-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="dc459-357">Vælg **OK** for at bekræfte værdien.</span><span class="sxs-lookup"><span data-stu-id="dc459-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="dc459-358">Der vises et læg på lager-arbejde, som beder brugeren om at anbringe en mål-id'et på genopfyldningspladsen.</span><span class="sxs-lookup"><span data-stu-id="dc459-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="dc459-359">Pladsen *Læg på lager* skal være **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="dc459-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="dc459-360">Bekræft læg på lager-oplysningerne, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="dc459-361">Du modtager meddelelsen "Arbejde fuldført" og "Der er intet tilgængeligt arbejde".</span><span class="sxs-lookup"><span data-stu-id="dc459-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="dc459-362">Du kan nu plukke salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="dc459-362">You can now pick sales order 2.</span></span> <span data-ttu-id="dc459-363">Spærringen blev ophævet, da genopfyldningsarbejdet, der er knyttet til salgsordren, blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc459-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="dc459-364">Angiv arbejds-id for salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="dc459-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="dc459-365">Der er kun én plukopgave for dette arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="dc459-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="dc459-366">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-366">Select **OK**.</span></span>

    <span data-ttu-id="dc459-367">Opgavesiden **Salgsordrer: pluk** viser det varenummer, det antal og den lokation, der skal plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="dc459-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="dc459-368">I feltet **LP** skal du angive id-nummeret for varen på den viste lokation.</span><span class="sxs-lookup"><span data-stu-id="dc459-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="dc459-369">Det id, du angiver, vil være et af de systemgenererede id'er fra arbejdsopgaven for genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="dc459-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="dc459-370">Hvis du vil være sikker på, at du indlæser det korrekte id, skal du kontrollere lageret på siden **Beholdningsliste** for varen, lokationen og antallet.</span><span class="sxs-lookup"><span data-stu-id="dc459-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="dc459-371">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="dc459-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="dc459-372">Bekræft instruktionerne til læg på lager-opgaven på den udgående midlertidige lagring.</span><span class="sxs-lookup"><span data-stu-id="dc459-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="dc459-373">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc459-373">Select **OK**.</span></span>

    <span data-ttu-id="dc459-374">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc459-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="dc459-375">Noter og tip</span><span class="sxs-lookup"><span data-stu-id="dc459-375">Notes and tips</span></span>

- <span data-ttu-id="dc459-376">Denne funktionalitet fungerer sammen med alle former for genopfyldning: bølgebehov, minimum/maksimum, lastbaseret behov og allokering.</span><span class="sxs-lookup"><span data-stu-id="dc459-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="dc459-377">Du kan manuelt tilsidesætte genopfyldningsarbejdets tilgængelighed for hver arbejdsoverskrift fra siden **Arbejdsdetaljer**, hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="dc459-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="dc459-378">Når systemet angiver genopfyldningsarbejdets tilgængelighed, tages der højde for ethvert lager, der allerede findes på lokationen, før et arbejde fuldføres.</span><span class="sxs-lookup"><span data-stu-id="dc459-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="dc459-379">Hvert stykke af salgsordrearbejdet er knyttet til et bestemt genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="dc459-380">Der findes ingen tilsvarende funktionalitet for tilgængeligt salgsarbejde.</span><span class="sxs-lookup"><span data-stu-id="dc459-380">There is no corresponding sales work availability functionality.</span></span>
