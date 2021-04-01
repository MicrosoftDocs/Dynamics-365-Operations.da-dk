---
title: Klyngeplacering fuld
description: Dette emne indeholder oplysninger om funktionen Klyngeplacering fuld. Denne funktion er et alternativ til en mere stiv håndhævelse af regler for arbejdspause, når der bruges klyngepluk, da det giver mulighed for større fejlmargener i volumenbegrænsningerne af containere eller transport.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6a7cad070377de58d21a8eb91ee3e1ffaf1c660
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233001"
---
# <a name="cluster-position-full"></a><span data-ttu-id="32dfd-104">Klyngeplacering fuld</span><span class="sxs-lookup"><span data-stu-id="32dfd-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32dfd-105">Funktionen *Klyngeplacering fuld* er et alternativ til en mere stiv håndhævelse af regler for arbejdspause, når der bruges klyngepluk, da det giver mulighed for større fejlmargener i volumenbegrænsningerne af containere eller transport.</span><span class="sxs-lookup"><span data-stu-id="32dfd-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="32dfd-106">I et almindeligt scenarie er det ikke alle varer på en arbejdsordre, der passer ind i en valgt container.</span><span class="sxs-lookup"><span data-stu-id="32dfd-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="32dfd-107">Lagermedarbejdere, der udfører klyngepluk, har få valgmuligheder i dette scenario: De skal enten skifte til en større container eller arbejde sammen med deres overordnede for at kunne finde frem til en anden løsning.</span><span class="sxs-lookup"><span data-stu-id="32dfd-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="32dfd-108">Denne funktion introducerer muligheden for at køre knappen **Fuld** knap på en af arbejdsenhederne i en klynge.</span><span class="sxs-lookup"><span data-stu-id="32dfd-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="32dfd-109">I ældre versioner var denne indstilling kun tilgængelig ved almindeligt ordrepluk, ikke for klyngepluk.</span><span class="sxs-lookup"><span data-stu-id="32dfd-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="32dfd-110">Men denne funktion adskiller sig fra standardknappen **Fuld**, da det resterende arbejde annulleres.</span><span class="sxs-lookup"><span data-stu-id="32dfd-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="32dfd-111">Det foreslås ikke, at brugeren føjer en anden beholder til den samme klynge, og der oprettes ikke automatisk nyt arbejde.</span><span class="sxs-lookup"><span data-stu-id="32dfd-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="32dfd-112">Aktivere funktionen Klyngeplacering fuld</span><span class="sxs-lookup"><span data-stu-id="32dfd-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="32dfd-113">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="32dfd-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="32dfd-114">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="32dfd-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="32dfd-115">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="32dfd-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="32dfd-116">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="32dfd-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="32dfd-117">**Funktionsnavn:** *Klyngeplacering fuld*</span><span class="sxs-lookup"><span data-stu-id="32dfd-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="32dfd-118">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="32dfd-118">Setup</span></span>

<span data-ttu-id="32dfd-119">Dette afsnit indeholder retningslinjer og et eksempel, der viser, hvordan du kan konfigurere og bruge funktionen *Klyngeplacering fuld*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="32dfd-120">Gøre eksempeldata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="32dfd-120">Make sample data available</span></span>

<span data-ttu-id="32dfd-121">Hvis du vil arbejde dig gennem [eksempelscenariet](#example-scenario) ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="32dfd-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="32dfd-122">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="32dfd-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="32dfd-123">Du kan også bruge dette eksempelscenarie som vejledning til brug af funktionen i et produktionssystem.</span><span class="sxs-lookup"><span data-stu-id="32dfd-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="32dfd-124">I dette tilfælde skal du dog erstatte dine egne værdier for hver af de indstillinger, der beskrives her.</span><span class="sxs-lookup"><span data-stu-id="32dfd-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="32dfd-125">Klyngeprofiler</span><span class="sxs-lookup"><span data-stu-id="32dfd-125">Cluster profiles</span></span>

<span data-ttu-id="32dfd-126">Du skal angive, om klynge-id'er skal genereres automatisk, hvor mange placeringer der bruges, når klynger afbrydes, og hvordan plukarbejdet skal sættes i sekvens og kontrolleres.</span><span class="sxs-lookup"><span data-stu-id="32dfd-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="32dfd-127">Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Klyngeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="32dfd-128">Vælg posten **Opret klynge** i listeruden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="32dfd-129">I oversigtspanelet **Generelt** skal du kontrollere følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="32dfd-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="32dfd-130">**Generér klynge-id:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="32dfd-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="32dfd-131">**Aktivér placeringer:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="32dfd-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="32dfd-132">**Antal placeringer:** *2*</span><span class="sxs-lookup"><span data-stu-id="32dfd-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="32dfd-133">**Navn på placering:** *Numerisk*</span><span class="sxs-lookup"><span data-stu-id="32dfd-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="32dfd-134">**Bryd klynge på:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="32dfd-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="32dfd-135">**Sortér bekræftelsestype:** *Scanning af placering*</span><span class="sxs-lookup"><span data-stu-id="32dfd-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="32dfd-136">I oversigtspanelet **Klyngesortering**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="32dfd-137">Gitteret skal være tomt (dvs. det må ikke indeholde linjer).</span><span class="sxs-lookup"><span data-stu-id="32dfd-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="32dfd-138">Arbejdsskabeloner</span><span class="sxs-lookup"><span data-stu-id="32dfd-138">Work templates</span></span>

<span data-ttu-id="32dfd-139">Definer, hvordan du opretter plukarbejde til klyngepluk.</span><span class="sxs-lookup"><span data-stu-id="32dfd-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="32dfd-140">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="32dfd-141">Angiv feltet **Arbejdsordretype** til *Salgsordrer* øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="32dfd-142">Kontrollér, at følgende arbejdsskabeloner fra demonstrationsdataene vises.</span><span class="sxs-lookup"><span data-stu-id="32dfd-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="32dfd-143">Hvis de ikke er tilgængelige, kan du ikke fuldføre scenariet.</span><span class="sxs-lookup"><span data-stu-id="32dfd-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="32dfd-144">61 Salgsordrestadie</span><span class="sxs-lookup"><span data-stu-id="32dfd-144">61 SO Stage</span></span>
    - <span data-ttu-id="32dfd-145">61 Klyngepluk for slagsordre</span><span class="sxs-lookup"><span data-stu-id="32dfd-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="32dfd-146">Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="32dfd-146">Location directives</span></span>

<span data-ttu-id="32dfd-147">Du skal angive, hvor varerne plukkes fra, og hvor de skal placeres.</span><span class="sxs-lookup"><span data-stu-id="32dfd-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="32dfd-148">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="32dfd-149">Indstil feltet **Arbejdsordretype** i listeoverskriften til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="32dfd-150">Kontrollér, at følgende salgsordredirektiver fra demonstrationsdataene vises.</span><span class="sxs-lookup"><span data-stu-id="32dfd-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="32dfd-151">Hvis de ikke er tilgængelige, kan du ikke fuldføre scenariet.</span><span class="sxs-lookup"><span data-stu-id="32dfd-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="32dfd-152">61 Klyngepluk</span><span class="sxs-lookup"><span data-stu-id="32dfd-152">61 Cluster pick</span></span>
    - <span data-ttu-id="32dfd-153">61 Plukordre for slagsordre</span><span class="sxs-lookup"><span data-stu-id="32dfd-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="32dfd-154">Menupunkter i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="32dfd-154">Mobile device menu items</span></span>

<span data-ttu-id="32dfd-155">Du skal konfigurere et menupunkt på en mobilenhed til at bruge eksisterende arbejde, der er pålagt ved hjælp af klyngepluk.</span><span class="sxs-lookup"><span data-stu-id="32dfd-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="32dfd-156">I mobilenhedens menupunkt til klyngepluk skal parameteren **Tillad opdeling af arbejde** være slået til, og arbejdsklassen *Salgsordrepluk* skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="32dfd-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="32dfd-157">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="32dfd-158">Vælg posten **Opret klyngepluk** i listeruden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="32dfd-159">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="32dfd-160">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="32dfd-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="32dfd-161">**Ledet af:** *Klyngepluk*</span><span class="sxs-lookup"><span data-stu-id="32dfd-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="32dfd-162">**Generer nummerplade:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="32dfd-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="32dfd-163">**Tillad opdeling af arbejde:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="32dfd-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="32dfd-164">**Klyngeprofil-id:** *Opret klynge*</span><span class="sxs-lookup"><span data-stu-id="32dfd-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="32dfd-165">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="32dfd-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="32dfd-166">I oversigtspanelet **Arbejdsklasser** skal du tilføje følgende to linjer efter behov:</span><span class="sxs-lookup"><span data-stu-id="32dfd-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="32dfd-167">Linje 1 (findes som regel i demonstrationsdata):</span><span class="sxs-lookup"><span data-stu-id="32dfd-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="32dfd-168">**Arbejdsklasse-id:** *Salg*</span><span class="sxs-lookup"><span data-stu-id="32dfd-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="32dfd-169">**Arbejdsordretype:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="32dfd-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="32dfd-170">Linje 2 (findes sikkert ikke i demonstrationsdata):</span><span class="sxs-lookup"><span data-stu-id="32dfd-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="32dfd-171">**Arbejdsklasse-id:** *Salgsordrepluk*</span><span class="sxs-lookup"><span data-stu-id="32dfd-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="32dfd-172">**Arbejdsordretype:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="32dfd-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="32dfd-173">Gå til **Konfiguration af arbejdsbekræftelse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="32dfd-174">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-174">Select **Edit**.</span></span>
1. <span data-ttu-id="32dfd-175">Angiv følgende værdier på linjen i gitteret.</span><span class="sxs-lookup"><span data-stu-id="32dfd-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="32dfd-176">**Arbejdstype** - *Pluk*</span><span class="sxs-lookup"><span data-stu-id="32dfd-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="32dfd-177">**Produktbekræftelse** - *Markér afkrydsningsfeltet*</span><span class="sxs-lookup"><span data-stu-id="32dfd-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="32dfd-178">Vælg **Gem** i handlingsruden, og luk siden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="32dfd-179">Opret plukarbejde</span><span class="sxs-lookup"><span data-stu-id="32dfd-179">Create picking work</span></span>

<span data-ttu-id="32dfd-180">Før du kan starte klyngepluk, skal du oprette udgående arbejde.</span><span class="sxs-lookup"><span data-stu-id="32dfd-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="32dfd-181">Den klyngeprofil, du oprettede tidligere, angiver to klyngeplaceringer.</span><span class="sxs-lookup"><span data-stu-id="32dfd-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="32dfd-182">Derfor skal der oprettes mindst to arbejds-id'er til salgsordrepluk.</span><span class="sxs-lookup"><span data-stu-id="32dfd-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="32dfd-183">I dette scenarie sker der transaktioner på lagersted *61*, og de bruger varerne *L0101* og *T0100*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="32dfd-184">Demodataene skal have en tilstrækkelig disponibel lagerbeholdning af disse varer.</span><span class="sxs-lookup"><span data-stu-id="32dfd-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="32dfd-185">Kontrollér, at du har tilstrækkeligt lager til at fuldføre transaktionerne.</span><span class="sxs-lookup"><span data-stu-id="32dfd-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="32dfd-186">Opret salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="32dfd-186">Create sales order 1</span></span>

1. <span data-ttu-id="32dfd-187">Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="32dfd-188">Vælg **Ny** for at oprette salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="32dfd-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="32dfd-189">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="32dfd-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="32dfd-190">**Debitorkonto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="32dfd-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="32dfd-191">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="32dfd-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="32dfd-192">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-192">Select **OK**.</span></span>
1. <span data-ttu-id="32dfd-193">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="32dfd-193">The new sales order is opened.</span></span> <span data-ttu-id="32dfd-194">I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="32dfd-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="32dfd-195">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="32dfd-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="32dfd-196">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="32dfd-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="32dfd-197">I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.</span><span class="sxs-lookup"><span data-stu-id="32dfd-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="32dfd-198">I oversigtspanelet **Salgsordrelinjer** skal du tilføje endnu en linje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="32dfd-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="32dfd-199">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="32dfd-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="32dfd-200">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="32dfd-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="32dfd-201">I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.</span><span class="sxs-lookup"><span data-stu-id="32dfd-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="32dfd-202">Udfør følgende trin for hver linje, du netop har tilføjet, for at reservere lager:</span><span class="sxs-lookup"><span data-stu-id="32dfd-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="32dfd-203">Markér den linje, du vil reservere.</span><span class="sxs-lookup"><span data-stu-id="32dfd-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="32dfd-204">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="32dfd-205">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="32dfd-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="32dfd-206">Luk siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="32dfd-207">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="32dfd-208">Når frigivelsen er fuldført, modtager du orienterende meddelelser, der viser bølgen og last-id'et, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="32dfd-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="32dfd-209">Opret salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="32dfd-209">Create sales order 2</span></span>

1. <span data-ttu-id="32dfd-210">Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="32dfd-211">Vælg **Ny** for at oprette salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="32dfd-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="32dfd-212">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="32dfd-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="32dfd-213">**Debitorkonto:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="32dfd-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="32dfd-214">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="32dfd-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="32dfd-215">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-215">Select **OK**.</span></span>
1. <span data-ttu-id="32dfd-216">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="32dfd-216">The new sales order is opened.</span></span> <span data-ttu-id="32dfd-217">I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="32dfd-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="32dfd-218">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="32dfd-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="32dfd-219">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="32dfd-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="32dfd-220">I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.</span><span class="sxs-lookup"><span data-stu-id="32dfd-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="32dfd-221">I oversigtspanelet **Salgsordrelinjer** skal du tilføje endnu en linje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="32dfd-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="32dfd-222">**Varenummer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="32dfd-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="32dfd-223">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="32dfd-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="32dfd-224">I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** angive feltet **Bekræftet afsendelsesdato** til dags dato.</span><span class="sxs-lookup"><span data-stu-id="32dfd-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="32dfd-225">Udfør følgende trin for hver linje, du netop har tilføjet, for at reservere lager:</span><span class="sxs-lookup"><span data-stu-id="32dfd-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="32dfd-226">Markér den linje, du vil reservere.</span><span class="sxs-lookup"><span data-stu-id="32dfd-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="32dfd-227">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="32dfd-228">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="32dfd-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="32dfd-229">Luk siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="32dfd-230">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="32dfd-231">Når frigivelsen er fuldført, modtager du orienterende meddelelser, der viser bølgen og last-id'et, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="32dfd-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="32dfd-232">Hent arbejds-id'er og id-numre</span><span class="sxs-lookup"><span data-stu-id="32dfd-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="32dfd-233">Der skal være oprettet to arbejds-id'er, som hver især har to pluklinjer.</span><span class="sxs-lookup"><span data-stu-id="32dfd-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="32dfd-234">Udfør følgende trin for at finde arbejds-id'erne og id-tildelingerne.</span><span class="sxs-lookup"><span data-stu-id="32dfd-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="32dfd-235">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="32dfd-236">Søg i gitteret **Oversigt** efter de to salgsordrer, du netop har oprettet, i kolonnen **Ordrenummer**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="32dfd-237">Notér dig arbejds-id'et for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="32dfd-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="32dfd-238">Markér rækken for hver salgsordre for at få vist relaterede oplysninger i **Linjer**-gitteret.</span><span class="sxs-lookup"><span data-stu-id="32dfd-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="32dfd-239">Notér dig den lokation, som de enkelte varer skal plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="32dfd-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="32dfd-240">Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="32dfd-241">I handlingsruden skal du vælge **Dimensioner** for at åbne dialogboksen **Dimensionsvisning**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="32dfd-242">Sørg for, at afkrydsningsfelterne **Id** **Lagersted** og **Varenummer** er markeret, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="32dfd-243">I **Filter**-ruden skal du angive følgende filtre:</span><span class="sxs-lookup"><span data-stu-id="32dfd-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="32dfd-244">**Varenummer** – **er enten** – *L0101* eller *T100*</span><span class="sxs-lookup"><span data-stu-id="32dfd-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="32dfd-245">**Lagersted** – **begynder med** – *61*</span><span class="sxs-lookup"><span data-stu-id="32dfd-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="32dfd-246">Notér dit de viste værdier af **Id**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="32dfd-247">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="32dfd-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="32dfd-248">Udførelse af mobilenhedsproces – Konfiguration af arbejdsbekræftelse for produktet</span><span class="sxs-lookup"><span data-stu-id="32dfd-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="32dfd-249">Log på lagerstedsappen som en bruger på lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="32dfd-250">Gå til **Udgående \> Opret klyngepluk**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="32dfd-251">Siden **OPGAVE: Tildel arbejde til klynge** vises.</span><span class="sxs-lookup"><span data-stu-id="32dfd-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="32dfd-252">Angiv arbejds-id'et for salgsordre 1 for at tildele det klyngeplacering 1.</span><span class="sxs-lookup"><span data-stu-id="32dfd-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="32dfd-253">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-254">Angiv arbejds-id'et for salgsordre 2 for at tildele det klyngeplacering 2.</span><span class="sxs-lookup"><span data-stu-id="32dfd-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="32dfd-255">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="32dfd-256">Siden **OPGAVE: Opret klyngepluk: Pluk** vises, og der står *Vare L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="32dfd-257">Da klyngeprofilen angav antallet af placeringer til 2, vil systemet automatisk henvise til det første konsoliderede pluk: to paller (PL) af vare *L0101*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="32dfd-258">Du kan når som helst under følgende trin vælge fanen **Detaljer** for at få vist flere oplysninger om opgaven, f.eks. plukpladsen.</span><span class="sxs-lookup"><span data-stu-id="32dfd-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="32dfd-259">Angiv feltet **VARE** til *L0101*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="32dfd-260">Dette bekræfter det varenummer, der kræves til dette menupunkt (du har konfigureret dette tidligere ved at vælge **Konfiguration af arbejdsbekræftelse** på siden **Menupunkt på mobilenhed**, da du oprettede dette menupunkt).</span><span class="sxs-lookup"><span data-stu-id="32dfd-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="32dfd-261">Angiv det id-nummer, der er knyttet til varen på den lokation, der plukkes fra.</span><span class="sxs-lookup"><span data-stu-id="32dfd-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="32dfd-262">Du skal vælge to paller.</span><span class="sxs-lookup"><span data-stu-id="32dfd-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="32dfd-263">Indstil feltet **LP** til *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="32dfd-264">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="32dfd-265">Siden **OPGAVE: Sortér: Opret klyngepluk** vises.</span><span class="sxs-lookup"><span data-stu-id="32dfd-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="32dfd-266">Her skal du sortere de to plukkede paller i en plukplacering.</span><span class="sxs-lookup"><span data-stu-id="32dfd-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="32dfd-267">Denne placering kan være en transportkasse eller container, der bruges til at adskille det plukkede lager efter salgsordre.</span><span class="sxs-lookup"><span data-stu-id="32dfd-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="32dfd-268">Se de detaljer, der vises for varen (*L0101*) og antal (*20* hver), som skal sorteres i position 1 (for salgsordre 1).</span><span class="sxs-lookup"><span data-stu-id="32dfd-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="32dfd-269">Indstil feltet **POSITIONSNAVN** til *1*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="32dfd-270">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-271">Se de detaljer, der vises for varen (*L0101*) og antal (*20* hver), som skal sorteres i position 2 (for salgsordre 2).</span><span class="sxs-lookup"><span data-stu-id="32dfd-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="32dfd-272">Indstil feltet **POSITIONSNAVN** til *2*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="32dfd-273">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="32dfd-274">Siden **OPGAVE: Opret klyngepluk: Pluk** vises, og der står *Vare T0100 7 hver*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="32dfd-275">I dette scenario kan position 1 ikke acceptere det fulde antal varer, der skal plukkes for at opfylde salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="32dfd-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="32dfd-276">En position skal være markeret som fuld.</span><span class="sxs-lookup"><span data-stu-id="32dfd-276">A position must be marked as full.</span></span> <span data-ttu-id="32dfd-277">I dette scenario skal du foretage et delvist pluk af den anden vare.</span><span class="sxs-lookup"><span data-stu-id="32dfd-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="32dfd-278">Den anden vare plukkes delvist til position 1, og der oprettes nyt arbejde for at plukke det resterende antal for at opfylde ordren.</span><span class="sxs-lookup"><span data-stu-id="32dfd-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="32dfd-279">Vælg menuknappen (kaldes også hamburger eller hamburgerknappen), og vælg derefter **Position fuld**.</span><span class="sxs-lookup"><span data-stu-id="32dfd-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="32dfd-280">Identificer den position, der er fuld, og vælg *1*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="32dfd-281">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-282">Angiv det plukantal, der stadig kan plukkes til position 1.</span><span class="sxs-lookup"><span data-stu-id="32dfd-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="32dfd-283">Systemet kan bestemme, hvilket varenummer der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="32dfd-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="32dfd-284">Angiv *2*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-284">Enter *2*.</span></span>
1. <span data-ttu-id="32dfd-285">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-286">Bekræft varenummeret for at fuldføre plukningen af den resterende vare på position 2.</span><span class="sxs-lookup"><span data-stu-id="32dfd-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="32dfd-287">Angiv feltet **VARE** til *T0100*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="32dfd-288">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-289">Angiv det id, som varen plukkes fra, ved at indstille feltet **LP** til *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="32dfd-290">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-291">Se de detaljer, der vises for varen (*T0100*) og antal (*2* hver), som skal sorteres i position 2 (for salgsordre 2).</span><span class="sxs-lookup"><span data-stu-id="32dfd-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="32dfd-292">Indstil feltet **POSITIONSNAVN** til *2*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="32dfd-293">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="32dfd-294">Se de detaljer, der vises for varen (*T0100*) og antal (*2* hver), som skal sorteres i position 1 (for salgsordre 1).</span><span class="sxs-lookup"><span data-stu-id="32dfd-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="32dfd-295">Indstil feltet **POSITIONSNAVN** til *1*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="32dfd-296">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="32dfd-297">Siden **OPGAVE: Opret klyngepluk: Læg på lager** vises.</span><span class="sxs-lookup"><span data-stu-id="32dfd-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="32dfd-298">I dette scenario er klyngeplukket fuldført, og brugeren dirigeres til at lægge de plukkede varer på lager fra position 1 og position 2 på lokationen for midlertidig lagring *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="32dfd-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="32dfd-299">Gennemgå oplysningerne på siden.</span><span class="sxs-lookup"><span data-stu-id="32dfd-299">Review the information on the page.</span></span> <span data-ttu-id="32dfd-300">De viser, at der vil blive lagt et samlet antal af *44* på lokationen for midlertidig lagring.</span><span class="sxs-lookup"><span data-stu-id="32dfd-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="32dfd-301">Vælg **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="32dfd-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="32dfd-302">Du modtager en meddelelse om "Klynge er fuldført".</span><span class="sxs-lookup"><span data-stu-id="32dfd-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="32dfd-303">Du kan nu bruge menupunktet **Salgspluk** til at plukke det resterende antal.</span><span class="sxs-lookup"><span data-stu-id="32dfd-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="32dfd-304">Derefter kan du bruge menupunktet **Salgslastning** til at flytte varerne fra den midlertidige lagring til læsserampen.</span><span class="sxs-lookup"><span data-stu-id="32dfd-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]