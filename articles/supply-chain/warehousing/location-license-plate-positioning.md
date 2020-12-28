---
title: Placering af lokations-id
description: Med placering af nummerplader kan du se, hvor en nummerplade er placeret på en lokation med flere paller, f.eks. en lokation, der bruger en pallereol med dobbeltdybde.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424950"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="a370d-103">Placering af lokations-id</span><span class="sxs-lookup"><span data-stu-id="a370d-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a370d-104">Med placering af nummerplader kan du se, hvor en nummerplade er placeret på en lokation med flere paller, f.eks. en lokation, der bruger en pallereol med dobbeltdybde.</span><span class="sxs-lookup"><span data-stu-id="a370d-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="a370d-105">Funktionen tilføjer et løbenummer til hver nummerplade, der anbringes på en lagerplacering.</span><span class="sxs-lookup"><span data-stu-id="a370d-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="a370d-106">Dette løbenummer bruges til at bestille nummerpladerne på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="a370d-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="a370d-107">Derfor understøtter funktionen intelligente scenarier, hvor kunder anvender et reolsystem og skal vide, hvilken nummerplade der er på forsiden af det af hensyn til plukning.</span><span class="sxs-lookup"><span data-stu-id="a370d-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="a370d-108">Dette emne indeholder et scenarie, der viser, hvordan du kan konfigurere og bruge funktionen.</span><span class="sxs-lookup"><span data-stu-id="a370d-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="a370d-109">Aktivér funktionen til placering af nummerplade på lokation</span><span class="sxs-lookup"><span data-stu-id="a370d-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="a370d-110">Før du kan bruge funktionen til placering af nummerplads på lokation, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="a370d-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="a370d-111">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="a370d-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a370d-112">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="a370d-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a370d-113">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="a370d-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a370d-114">**Funktionsnavn:** *Placering af nummerplade på lokation*</span><span class="sxs-lookup"><span data-stu-id="a370d-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a370d-115">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="a370d-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="a370d-116">Gøre eksempeldata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="a370d-116">Make sample data available</span></span>

<span data-ttu-id="a370d-117">Hvis du vil arbejde gennem dette scenarie ved hjælp af de værdier, der er foreslået, skal du arbejde på et system, hvor eksempeldata er installeret.</span><span class="sxs-lookup"><span data-stu-id="a370d-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="a370d-118">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="a370d-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="a370d-119">Konfigurer funktionen til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="a370d-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="a370d-120">Udfør følgende procedurer for at konfigurere funktionen til *placering af nummerplader på lokation* for det scenarie, der vises i dette emne.</span><span class="sxs-lookup"><span data-stu-id="a370d-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="a370d-121">Lokationsprofiler</span><span class="sxs-lookup"><span data-stu-id="a370d-121">Location profiles</span></span>

<span data-ttu-id="a370d-122">Funktionen skal være aktiveret i lokationsprofilen for hver lokation, hvor den vil blive brugt.</span><span class="sxs-lookup"><span data-stu-id="a370d-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="a370d-123">Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="a370d-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="a370d-124">Vælg **MASSE-06** på listen over lokationsprofiler i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="a370d-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="a370d-125">I oversigtspanelet **Generelt** er der to nye muligheder, der er blevet tilføjet af funktionen.</span><span class="sxs-lookup"><span data-stu-id="a370d-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="a370d-126">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a370d-126">Set the following values:</span></span>

    - <span data-ttu-id="a370d-127">**Aktiver nummerpladeplacering:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a370d-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="a370d-128">Når denne indstilling er angivet til *Ja*, bevares nummerpladeplaceringen for nummerplader på lokationen.</span><span class="sxs-lookup"><span data-stu-id="a370d-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="a370d-129">**Vis NP-position på mobilenhed:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a370d-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="a370d-130">Når denne indstilling er angivet til *Ja*, vises nummerpladens placering for brugere af mobilenheder under justering og optælling.</span><span class="sxs-lookup"><span data-stu-id="a370d-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="a370d-131">Du kan kun ændre indstillingen af denne valgmulighed, når funktionen er slået til.</span><span class="sxs-lookup"><span data-stu-id="a370d-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="a370d-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a370d-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="a370d-133">Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="a370d-133">Location directives</span></span>

1. <span data-ttu-id="a370d-134">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="a370d-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a370d-135">I venstre rude skal du kontrollere, at feltet **Arbejdsordretype** er angivet til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="a370d-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="a370d-136">På listen over lokationsvejledninger skal du vælge **61 SO Plukliste**.</span><span class="sxs-lookup"><span data-stu-id="a370d-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="a370d-137">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a370d-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a370d-138">I oversigtspanelet **Linjer** skal du vælge den linje, hvor et **løbenummer** har værdien *2*.</span><span class="sxs-lookup"><span data-stu-id="a370d-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="a370d-139">I oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge den linje, der har en værdi for **Navn** med *Vælg for mindre end palle* (den skal være den eneste linje) og ændre værdien for **løbenummer** til *2*.</span><span class="sxs-lookup"><span data-stu-id="a370d-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="a370d-140">Vælg **Ny** over gitteret for at tilføje en linje til en ny handling i lokationsvejledning.</span><span class="sxs-lookup"><span data-stu-id="a370d-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="a370d-141">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="a370d-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a370d-142">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="a370d-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a370d-143">**Navn:** *Plukposition 1*</span><span class="sxs-lookup"><span data-stu-id="a370d-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="a370d-144">Mens den nye linje stadig er markeret, skal du vælge **Rediger forespørgsel** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="a370d-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="a370d-145">Vælg forespørgselseditoren skal du vælge fanen **Joinforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="a370d-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="a370d-146">Udvid tabeljoinet **lokationer** for at få vist joinet med tabellen **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="a370d-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="a370d-147">Udvid tabeljoinet **Lagerdimensioner** for at få vist joinet med tabellen **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="a370d-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="a370d-148">Vælg **Lagerdimensioner**, og vælg derefter **Tilføj tabeljoin**.</span><span class="sxs-lookup"><span data-stu-id="a370d-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="a370d-149">På listen over tabeller, der vises, skal du i kolonnen **Relation** vælge **Nummerplade (nummerplade)**.</span><span class="sxs-lookup"><span data-stu-id="a370d-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="a370d-150">Vælg derefter **Vælg** for at føje en **Nummerplade** til tabeljoinet **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="a370d-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="a370d-151">Mens **Nummerplade** stadig er valgt, skal du vælge **Tilføj tabeljoin**.</span><span class="sxs-lookup"><span data-stu-id="a370d-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="a370d-152">På listen over tabeller, der vises, skal du i kolonnen **Relation** vælge **Placering af nummerplade på lokation (nummerplade)**.</span><span class="sxs-lookup"><span data-stu-id="a370d-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="a370d-153">Vælg derefter **Vælg** for at føje **Placering af nummerplads på lokation** til tabeljoinet **Lagerdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="a370d-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="a370d-154">![Tabeljoinforbindelser](media/LpTableJoin.png "Tabeljoinforbindelser")</span><span class="sxs-lookup"><span data-stu-id="a370d-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="a370d-155">Vælg **OK** for at bekræfte de opdaterede joinforbundne tabeller og lukke forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a370d-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="a370d-156">I oversigtspanelet **Handlinger i lokationsvejledning** skal du vælge **Rediger forespørgsel** igen for at åbne forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a370d-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="a370d-157">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="a370d-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="a370d-158">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="a370d-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a370d-159">**Tabel:** *Placering af nummerplade på lokation*</span><span class="sxs-lookup"><span data-stu-id="a370d-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="a370d-160">**Afledt tabel:** *Placering af nummerplade på lokation*</span><span class="sxs-lookup"><span data-stu-id="a370d-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="a370d-161">**Felt:** *NP-position*</span><span class="sxs-lookup"><span data-stu-id="a370d-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="a370d-162">**Afgrænsning:** *1*</span><span class="sxs-lookup"><span data-stu-id="a370d-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="a370d-163">![Nyt område](media/LpPositionCriteria.png "Nyt område")</span><span class="sxs-lookup"><span data-stu-id="a370d-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="a370d-164">Vælg **OK** for at bekræfte dine ændringer og lukke forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a370d-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="a370d-165">Konfigurer eksempeldata til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="a370d-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="a370d-166">I dette scenarie skal brugeren logge på den Warehouse Mobile App ved hjælp af en arbejder, der er konfigureret til lagersted *61*, for at udføre arbejde.</span><span class="sxs-lookup"><span data-stu-id="a370d-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="a370d-167">Brugeren skal også fuldføre transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a370d-167">The user must also complete transactions.</span></span>

<span data-ttu-id="a370d-168">Da funktionen *Placering af nummerplade på lokation* tilføjer et nyt id for nummerpladepositioner på en placering, skal du først oprette nogle data for at kunne understøtte scenariet.</span><span class="sxs-lookup"><span data-stu-id="a370d-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="a370d-169">Lav spotoptælling på den første lokation</span><span class="sxs-lookup"><span data-stu-id="a370d-169">Spot-count the first location</span></span>

1. <span data-ttu-id="a370d-170">Åbn Warehouse Mobile App, og log på lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="a370d-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="a370d-171">Gå til **Lager \> Spotoptælling**.</span><span class="sxs-lookup"><span data-stu-id="a370d-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="a370d-172">På siden **Spotoptælling** skal du angive feltet **Lokation** til *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="a370d-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="a370d-173">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-173">Select **OK**.</span></span>

    <span data-ttu-id="a370d-174">På siden vises den lokation, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a370d-174">The page shows the location that you entered.</span></span> <span data-ttu-id="a370d-175">Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a370d-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a370d-176">Vælg **Opdater** for at tilføje en optælling på lokationen.</span><span class="sxs-lookup"><span data-stu-id="a370d-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="a370d-177">På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **Vare** og derefter angive værdien *A0001*.</span><span class="sxs-lookup"><span data-stu-id="a370d-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="a370d-178">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-178">Select **OK**.</span></span>
1. <span data-ttu-id="a370d-179">På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **NP** og derefter angive værdien *LP1001* (eller andre nummerplader efter eget valg).</span><span class="sxs-lookup"><span data-stu-id="a370d-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="a370d-180">Siden **Cyklusoptælling: Tilføj ny NP eller vare** viser **Nummerpladeposition 1**.</span><span class="sxs-lookup"><span data-stu-id="a370d-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="a370d-181">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-181">Select **OK**.</span></span>

    <span data-ttu-id="a370d-182">Du skal nu angive antallet for den vare, der er optalt på nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="a370d-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="a370d-183">Angiv feltet **Antal** til *10*.</span><span class="sxs-lookup"><span data-stu-id="a370d-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="a370d-184">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-184">Select **OK**.</span></span>

    <span data-ttu-id="a370d-185">På siden vises den lokation, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a370d-185">The page shows the location that you entered.</span></span> <span data-ttu-id="a370d-186">Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a370d-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a370d-187">Vælg **Opdater** for at tilføje en anden optælling på lokationen.</span><span class="sxs-lookup"><span data-stu-id="a370d-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="a370d-188">På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **Vare** og derefter angive værdien *A0002*.</span><span class="sxs-lookup"><span data-stu-id="a370d-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="a370d-189">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-189">Select **OK**.</span></span>
1. <span data-ttu-id="a370d-190">På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **NP** og derefter angive værdien *LP1002* (eller andre nummerpladenumre, du vælger, hvis det er forskelligt fra det nummer, du har angivet tidligere).</span><span class="sxs-lookup"><span data-stu-id="a370d-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="a370d-191">Skift nummerpladens placering ved at indstille feltet **NP-position** til *2*.</span><span class="sxs-lookup"><span data-stu-id="a370d-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="a370d-192">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-192">Select **OK**.</span></span>
1. <span data-ttu-id="a370d-193">Angiv det antal af varen, der er optalt på nummerpladen, ved at angive feltet **Antal** til *10*.</span><span class="sxs-lookup"><span data-stu-id="a370d-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="a370d-194">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-194">Select **OK**.</span></span>

    <span data-ttu-id="a370d-195">På siden vises den lokation, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a370d-195">The page shows the location that you entered.</span></span> <span data-ttu-id="a370d-196">Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a370d-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a370d-197">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-197">Select **OK**.</span></span>

<span data-ttu-id="a370d-198">Arbejde er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="a370d-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="a370d-199">Lav spotoptælling på den anden lokation</span><span class="sxs-lookup"><span data-stu-id="a370d-199">Spot-count the second location</span></span>

1. <span data-ttu-id="a370d-200">På siden **Spotoptælling** skal du angive feltet **Lokation** til *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="a370d-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="a370d-201">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-201">Select **OK**.</span></span>

    <span data-ttu-id="a370d-202">På siden vises den lokation, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a370d-202">The page shows the location that you entered.</span></span> <span data-ttu-id="a370d-203">Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a370d-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a370d-204">Vælg **Opdater** for at tilføje en optælling på lokationen.</span><span class="sxs-lookup"><span data-stu-id="a370d-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="a370d-205">På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **Vare** og derefter angive værdien *A0002*.</span><span class="sxs-lookup"><span data-stu-id="a370d-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="a370d-206">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-206">Select **OK**.</span></span>
1. <span data-ttu-id="a370d-207">På siden **Cyklusoptælling: Tilføj ny NP eller vare** skal du vælge feltet **NP** og derefter angive værdien *LP1003* (eller andre nummerpladenumre, du vælger, hvis det er forskelligt fra begge de nummerpladenumre, du har angivet i den forrige procedure).</span><span class="sxs-lookup"><span data-stu-id="a370d-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="a370d-208">Siden **Cyklusoptælling: Tilføj ny NP eller vare** viser **Nummerpladeposition 1**.</span><span class="sxs-lookup"><span data-stu-id="a370d-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="a370d-209">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-209">Select **OK**.</span></span>
1. <span data-ttu-id="a370d-210">Angiv det antal af varen, der er optalt på nummerpladen, ved at angive feltet **Antal** til *10*.</span><span class="sxs-lookup"><span data-stu-id="a370d-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="a370d-211">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-211">Select **OK**.</span></span>

    <span data-ttu-id="a370d-212">På siden vises den lokation, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a370d-212">The page shows the location that you entered.</span></span> <span data-ttu-id="a370d-213">Den viser også følgende meddelelse: "lokation er fuldført, vil du tilføje ny NP eller vare?"</span><span class="sxs-lookup"><span data-stu-id="a370d-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="a370d-214">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-214">Select **OK**.</span></span>

<span data-ttu-id="a370d-215">Arbejde er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="a370d-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="a370d-216">Arbejdsdetaljer</span><span class="sxs-lookup"><span data-stu-id="a370d-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="a370d-217">Lav spotoptælling via cyklusoptælling af arbejde i mobilappen i Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a370d-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="a370d-218">Arbejdet kræver, at optællingerne accepteres, før de bogføres til lageret.</span><span class="sxs-lookup"><span data-stu-id="a370d-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="a370d-219">Log på Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a370d-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="a370d-220">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a370d-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="a370d-221">På fanen **Oversigt** skal du se efter de linjer, der har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a370d-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="a370d-222">**Arbejdsordretype:** *Cyklusoptælling*</span><span class="sxs-lookup"><span data-stu-id="a370d-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="a370d-223">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="a370d-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a370d-224">**Arbejdsstatus:** *Afventer gennemsyn*</span><span class="sxs-lookup"><span data-stu-id="a370d-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="a370d-225">Der skal være oprettet to arbejds-id'er for disse linjer.</span><span class="sxs-lookup"><span data-stu-id="a370d-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="a370d-226">Optællingerne for begge disse arbejds-id'er skal accepteres.</span><span class="sxs-lookup"><span data-stu-id="a370d-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="a370d-227">I gitteret skal du vælge det første arbejds-id for arbejdsordretypen *Cyklusoptælling*.</span><span class="sxs-lookup"><span data-stu-id="a370d-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="a370d-228">Gå til handlingsrunde og vælg **Cyklusoptælling** i gruppen **Arbejde** under fanen **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a370d-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="a370d-229">Der vises to linjer, én for hver vare og nummerplade.</span><span class="sxs-lookup"><span data-stu-id="a370d-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="a370d-230">Værdierne i felterne **Optalt antal**, **Lokation**, **Nummerplade** og **Vare** skal svare til de optællingsposter, du har oprettet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="a370d-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="a370d-231">Hvis et eller flere af disse felter ikke er synlige, skal du vælge **Vis dimensioner** i handlingsruden for at føje dem til gitteret.</span><span class="sxs-lookup"><span data-stu-id="a370d-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="a370d-232">Vælg begge linjer.</span><span class="sxs-lookup"><span data-stu-id="a370d-232">Select both lines.</span></span>
1. <span data-ttu-id="a370d-233">Vælg **Accepter antal** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a370d-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="a370d-234">Du får vist meddelelse om "kladdebogføring".</span><span class="sxs-lookup"><span data-stu-id="a370d-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="a370d-235">Vælg **Meddelelsesdetaljer** for at få vist det bogførte kladdenummer.</span><span class="sxs-lookup"><span data-stu-id="a370d-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="a370d-236">Luk meddelelsesdetaljerne.</span><span class="sxs-lookup"><span data-stu-id="a370d-236">Close the message details.</span></span>
1. <span data-ttu-id="a370d-237">Opdater siden **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a370d-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="a370d-238">Det første arbejds-id er lukket og vises ikke længere.</span><span class="sxs-lookup"><span data-stu-id="a370d-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="a370d-239">Hvis du vil have vist lukket arbejde, skal du markere afkrydsningsfeltet **Vis lukket** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="a370d-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="a370d-240">Du accepterer nu arbejdet for nummerpladen på lokationen *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="a370d-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="a370d-241">På fanen **Oversigt** skal du vælge det andet arbejds-id for arbejdsordretypen *Cyklusoptælling*.</span><span class="sxs-lookup"><span data-stu-id="a370d-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="a370d-242">Gå til handlingsrunde og vælg **Cyklusoptælling** i gruppen **Arbejde** under fanen **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a370d-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="a370d-243">Der vises en linje for varen og nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="a370d-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="a370d-244">Værdierne i felterne **Optalt antal**, **Lokation**, **Nummerplade** og **Vare** skal svare til de optællingsposter, du har oprettet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="a370d-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="a370d-245">Vælg linjen.</span><span class="sxs-lookup"><span data-stu-id="a370d-245">Select the line.</span></span>
1. <span data-ttu-id="a370d-246">Vælg **Accepter antal** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a370d-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="a370d-247">Du får vist meddelelse om "kladdebogføring".</span><span class="sxs-lookup"><span data-stu-id="a370d-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="a370d-248">Vælg **Meddelelsesdetaljer** for at få vist det bogførte kladdenummer.</span><span class="sxs-lookup"><span data-stu-id="a370d-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="a370d-249">Luk meddelelsesdetaljerne.</span><span class="sxs-lookup"><span data-stu-id="a370d-249">Close the message details.</span></span>
1. <span data-ttu-id="a370d-250">Opdater siden **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a370d-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="a370d-251">Det andet arbejds-id er lukket og vises ikke længere.</span><span class="sxs-lookup"><span data-stu-id="a370d-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="a370d-252">Hvis du vil have vist lukket arbejde, skal du markere afkrydsningsfeltet **Vis lukket** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="a370d-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="a370d-253">Disponibel efter lokation</span><span class="sxs-lookup"><span data-stu-id="a370d-253">On-hand by location</span></span>

1. <span data-ttu-id="a370d-254">Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Disponibel efter lokation**.</span><span class="sxs-lookup"><span data-stu-id="a370d-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="a370d-255">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="a370d-255">Set the following values:</span></span>

    - <span data-ttu-id="a370d-256">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="a370d-256">**Site:** *6*</span></span>
    - <span data-ttu-id="a370d-257">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="a370d-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a370d-258">**Opdater på tværs af lokationer:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="a370d-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="a370d-259">Bemærk, at lokationen *01A01R1S1B* har to nummerplader:</span><span class="sxs-lookup"><span data-stu-id="a370d-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="a370d-260">**A0001**, hvor feltet **NP-position** er indstillet til *1*</span><span class="sxs-lookup"><span data-stu-id="a370d-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="a370d-261">**A0002**, hvor feltet **NP-position** er indstillet til *2*</span><span class="sxs-lookup"><span data-stu-id="a370d-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="a370d-262">Bemærk, at lokationen *01A01R1S2B* har én nummerplade:</span><span class="sxs-lookup"><span data-stu-id="a370d-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="a370d-263">**A0002**, hvor feltet **NP-position** er indstillet til *1*</span><span class="sxs-lookup"><span data-stu-id="a370d-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="a370d-264">Salgsordrescenarie</span><span class="sxs-lookup"><span data-stu-id="a370d-264">Sales order scenario</span></span>

<span data-ttu-id="a370d-265">Nu, hvor funktionen *Placering af nummerplade på lokation* er oprettet, og lageret er blevet gemt, skal du oprette en salgsordre for at generere plukarbejde, der anviser, at lagermedarbejderen skal plukke varen *A0002* fra det lagersted, hvor palle-id'et er i position *1*.</span><span class="sxs-lookup"><span data-stu-id="a370d-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="a370d-266">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a370d-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a370d-267">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a370d-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a370d-268">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="a370d-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a370d-269">**Debitorkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="a370d-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="a370d-270">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="a370d-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a370d-271">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a370d-271">Select **OK**.</span></span>
1. <span data-ttu-id="a370d-272">Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="a370d-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a370d-273">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="a370d-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="a370d-274">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a370d-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="a370d-275">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="a370d-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="a370d-276">Vælg **reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="a370d-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a370d-277">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret til ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a370d-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="a370d-278">Luk siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="a370d-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="a370d-279">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a370d-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a370d-280">Du modtager en orienterende meddelelse, der angiver bølge-id'et og forsendelses-id'et, der blev oprettet for ordren.</span><span class="sxs-lookup"><span data-stu-id="a370d-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="a370d-281">I oversigtspanelet **Salgsordrelinjer** skal du i menuen **Lager** over gitteret vælge **Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a370d-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="a370d-282">Siden **Arbejde** vises og viser det arbejde, der er oprettet for salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a370d-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="a370d-283">Noter det arbejds-id, der vises.</span><span class="sxs-lookup"><span data-stu-id="a370d-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="a370d-284">Salgsplukscenarie</span><span class="sxs-lookup"><span data-stu-id="a370d-284">Sales picking scenario</span></span>

1. <span data-ttu-id="a370d-285">Åbn mobilappen, og log på lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="a370d-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="a370d-286">Gå til **Udgående \> Salgsplukning**.</span><span class="sxs-lookup"><span data-stu-id="a370d-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="a370d-287">Vælg feltet **Id** på siden **Scan et arbejds-id/nummerplade-id**, og angiv derefter arbejds-id'et fra salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="a370d-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="a370d-288">Bemærk, at plukarbejdet dirigerer dig til at plukke vare *A0002* fra lokation *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="a370d-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="a370d-289">Du modtager denne instruktion, fordi vare *A0002* er på en licensnummerplade i position *1* på den pågældende lokation.</span><span class="sxs-lookup"><span data-stu-id="a370d-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="a370d-290">![Placering 1-lokation](media/LocationLicensePlatePositioning.png "Placering 1-lokation")</span><span class="sxs-lookup"><span data-stu-id="a370d-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="a370d-291">Angiv det nummerplade-id, du har oprettet for lokationen, og følg derefter vejledningen for at plukke salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a370d-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
