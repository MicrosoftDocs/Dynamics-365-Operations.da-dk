---
title: Systembaseret arbejdsrækkefølge
description: Dette emne giver oplysninger om systembaseret arbejdsrækkefølge. Denne funktionalitet gør det muligt at sortere og filtrere de arbejdsordrer, som systemet fremsender til brugere til afvikling. Det er nyttigt i situationer, hvor der kræves yderligere kriterier for at drive plukprocessen på lagerstedet.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017018"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="b58b3-105">Systembaseret arbejdsrækkefølge</span><span class="sxs-lookup"><span data-stu-id="b58b3-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b58b3-106">Systembaseret arbejdsrækkefølge gør det muligt at sortere og filtrere de arbejdsordrer, som systemet fremsender til brugere til afvikling.</span><span class="sxs-lookup"><span data-stu-id="b58b3-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="b58b3-107">Det er nyttigt i situationer, hvor yderligere kriterier (f. eks. leveringstiden, plukzonen, lokationsprofilen eller en kombination af forskellige kriterier) er nødvendige for at drive lagerstedets plukproces.</span><span class="sxs-lookup"><span data-stu-id="b58b3-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="b58b3-108">Denne funktion udvider den aktuelle systembaserede plukfunktionalitet ved at tilføje en systembaseret forespørgselsrækkefølge, hvor brugerne kan angive en sekvens og en eller flere forespørgsler, der evaluerer alle de oprettede arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="b58b3-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="b58b3-109">Det er kun de arbejdsordrer, der opfylder de kriterier, der er angivet i opsætningen af menupunktet i mobilenheden, der registreres og vises.</span><span class="sxs-lookup"><span data-stu-id="b58b3-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="b58b3-110">Denne funktionalitet giver dig derfor mulighed for yderligere optimering af lagerplukprocesser, da den identificerer arbejdsordrer, der opfylder de angivne kriterier, tildeler dem til det korrekte menupunkt i den mobile enhed og viser dem derefter for en arbejder, baseret på et bestemt kompetencesæt, plukudstyr eller et andet krav.</span><span class="sxs-lookup"><span data-stu-id="b58b3-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="b58b3-111">Hvis der er brug for andre kriterier, skal der bruges flere menupunkter i mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="b58b3-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="b58b3-112">Aktivér funktionen Systembaseret arbejdsrækkefølge for hele virksomheden</span><span class="sxs-lookup"><span data-stu-id="b58b3-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="b58b3-113">Før du kan bruge funktionen Systembaseret arbejdsrækkefølge, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="b58b3-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="b58b3-114">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="b58b3-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b58b3-115">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="b58b3-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b58b3-116">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="b58b3-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b58b3-117">**Funktionsnavn:** *Systembaseret arbejdsrækkefølge for hele virksomheden*</span><span class="sxs-lookup"><span data-stu-id="b58b3-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="b58b3-118">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b58b3-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b58b3-119">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="b58b3-119">Make demo data available</span></span>

<span data-ttu-id="b58b3-120">Hvis du vil arbejde gennem scenariet ved hjælp af de værdier, der vises i dette emne, skal du arbejde på et system, hvor standarddemodata er installeret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="b58b3-121">Derudover skal du vælge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="b58b3-122">I scenariet bruges lagersted *51* fra demodata.</span><span class="sxs-lookup"><span data-stu-id="b58b3-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b58b3-123">Før du frigiver ordrerne til lageret, skal du sørge for, at pluklokationerne har tilstrækkelig lagerbeholdning af alle varerne på ordrerne.</span><span class="sxs-lookup"><span data-stu-id="b58b3-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="b58b3-124">Standard-USMF-data skal understøtte dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="b58b3-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="b58b3-125">Hvis du ikke bruger demodata, skal du gennemse indstillingen **Lokationsvejledning** for at finde ud af, hvilke pluklokationer der skal bruges til salgsordrepluk.</span><span class="sxs-lookup"><span data-stu-id="b58b3-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="b58b3-126">Hvis du skal justere lagerbeholdning, kan du oprette manuelle bevægelser, bruge genopfyldning eller anvende en anden proces.</span><span class="sxs-lookup"><span data-stu-id="b58b3-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="b58b3-127">Opsætning af et mobilenhedsmenupunkt</span><span class="sxs-lookup"><span data-stu-id="b58b3-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="b58b3-128">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b58b3-129">Vælg **Salgspluk – system** på listen over mobilenhedsmenupunkter.</span><span class="sxs-lookup"><span data-stu-id="b58b3-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="b58b3-130">Det påkrævede menupunkt skal findes i forvejen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="b58b3-131">Bekræft følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="b58b3-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="b58b3-132">I oversigtspanelet **Generelt** skal feltet **Styret af** indstilles til *Systembaseret*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="b58b3-133">I oversigtspanelet **Arbejdsklasser** vises følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="b58b3-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="b58b3-134">Arbejdsklasse-id</span><span class="sxs-lookup"><span data-stu-id="b58b3-134">Work class ID</span></span> | <span data-ttu-id="b58b3-135">Arbejdsordretype</span><span class="sxs-lookup"><span data-stu-id="b58b3-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="b58b3-136">Sales</span><span class="sxs-lookup"><span data-stu-id="b58b3-136">Sales</span></span> | <span data-ttu-id="b58b3-137">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="b58b3-137">Sales orders</span></span> |
        | <span data-ttu-id="b58b3-138">Salgsordrepluk</span><span class="sxs-lookup"><span data-stu-id="b58b3-138">SO Pick</span></span> | <span data-ttu-id="b58b3-139">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="b58b3-139">Sales orders</span></span> |

1. <span data-ttu-id="b58b3-140">Vælg **Systembaserede arbejdssekvensforespørgsler** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b58b3-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="b58b3-141">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-141">Select **Edit**.</span></span>
1. <span data-ttu-id="b58b3-142">Slet den eksisterende linje, og bekræft derefter handlingen ved at vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="b58b3-143">Vælg **Ny** i handlingsruden for at oprette en linje.</span><span class="sxs-lookup"><span data-stu-id="b58b3-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="b58b3-144">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b58b3-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b3-145">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b3-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b58b3-146">**Beskrivelsesfelt:** *Arbejdsantal mindre end 20 og faldende*</span><span class="sxs-lookup"><span data-stu-id="b58b3-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="b58b3-147">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-147">Select **Save**.</span></span>
1. <span data-ttu-id="b58b3-148">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b58b3-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="b58b3-149">Under fanen **Joinforbindelser** skal du udvide join-hierarkiet for at få vist tabellen **Arbejdslinjer**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="b58b3-150">Vælg tabeljoinet **Arbejdslinjer**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="b58b3-151">Vælg **Tilføj tabeljoin**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="b58b3-152">Find og vælg den række, der har følgende indstillinger, på den liste, der vises:</span><span class="sxs-lookup"><span data-stu-id="b58b3-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="b58b3-153">**Join-tilstand:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="b58b3-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="b58b3-154">**Relation:** *Lokationer (lokation)*</span><span class="sxs-lookup"><span data-stu-id="b58b3-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="b58b3-155">Vælg **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-155">Select **Select**.</span></span>

    <span data-ttu-id="b58b3-156">Lokationer føjes til tabeljoinet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="b58b3-157">På fanen **Sortering** skal du vælge **Tilføj** for at tilføje en ny linje.</span><span class="sxs-lookup"><span data-stu-id="b58b3-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="b58b3-158">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b58b3-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b3-159">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b58b3-160">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b58b3-161">**Felt:** *Arbejdsantal* (i den viste meddelelsesboks skal du vælge **Ja** for at føje sortering til dette felt).</span><span class="sxs-lookup"><span data-stu-id="b58b3-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="b58b3-162">**Søgeretning:** *Faldende*</span><span class="sxs-lookup"><span data-stu-id="b58b3-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="b58b3-163">Vælg fanen **Område**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="b58b3-164">Hvis der kun skal medtages bestemte arbejdskriterier i rækkefølgen, kan du angive dem under fanen **Område**. I dette eksempel vil du kun medtage det arbejde, hvor antallet er mindre end 20 ea (den laveste måleenhed).</span><span class="sxs-lookup"><span data-stu-id="b58b3-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="b58b3-165">Bemærk, at der allerede er inkluderet nogle linjer.</span><span class="sxs-lookup"><span data-stu-id="b58b3-165">Notice that some lines are already included.</span></span> <span data-ttu-id="b58b3-166">Disse linjer skal ikke fjernes.</span><span class="sxs-lookup"><span data-stu-id="b58b3-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="b58b3-167">Vælg **Tilføj** for at tilføje en linje.</span><span class="sxs-lookup"><span data-stu-id="b58b3-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="b58b3-168">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b58b3-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b3-169">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b58b3-170">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b58b3-171">**Felt:** *Arbejdsantal for lager*</span><span class="sxs-lookup"><span data-stu-id="b58b3-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="b58b3-172">**Kriterier:** *\<20* (mindre end 20)</span><span class="sxs-lookup"><span data-stu-id="b58b3-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="b58b3-173">Vælg **Tilføj** for at tilføje en anden linje.</span><span class="sxs-lookup"><span data-stu-id="b58b3-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="b58b3-174">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b58b3-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b3-175">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="b58b3-176">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="b58b3-177">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="b58b3-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="b58b3-178">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="b58b3-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="b58b3-179">Vælg **Tilføj** for at tilføje en anden linje.</span><span class="sxs-lookup"><span data-stu-id="b58b3-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="b58b3-180">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="b58b3-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b58b3-181">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b58b3-182">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="b58b3-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b58b3-183">**Felt:** *Lokationsprofil-id*</span><span class="sxs-lookup"><span data-stu-id="b58b3-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="b58b3-184">**Kriterier:** *!STADIE*</span><span class="sxs-lookup"><span data-stu-id="b58b3-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="b58b3-185">Sørg for at medtage udråbstegnet ( *!* ) foran *STADIE*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-185">Be sure to include the exclamation point ( *!* ) in front of *STAGE*.</span></span>

1. <span data-ttu-id="b58b3-186">Vælg **OK** for at gemme og lukke forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="b58b3-187">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-187">Select **Save**.</span></span>
1. <span data-ttu-id="b58b3-188">Luk siden for at vende tilbage til siden **Mobilenhedsmenupunkter**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="b58b3-189">Denne opsætning definerer de kriterier, der skal bruges til at føde det kvalificerede arbejde til mobilenhedsmenupunktet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="b58b3-190">Hvis du føjer flere kriterielinjer til forespørgslen, vil systemet bruge den forespørgselslinje, der har det laveste løbenummer først.</span><span class="sxs-lookup"><span data-stu-id="b58b3-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="b58b3-191">Med andre ord vises alt det kvalificerede arbejde for løbenummer 1 for brugeren først og derefter alt arbejde for løbenummer 2.</span><span class="sxs-lookup"><span data-stu-id="b58b3-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="b58b3-192">Hvis et bestemt område og sortering skal bruges sammen, skal de derfor angives i den samme systembaserede arbejdssekvensforespørgsel.</span><span class="sxs-lookup"><span data-stu-id="b58b3-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="b58b3-193">Denne opsætning vil hente alle de ressourcer, der har mindst én linje, hvor antallet er mindre end 20 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="b58b3-194">Hvis arbejdet har en linje, hvor antallet er nøjagtigt 20 ea eller mere end 20 ea, vil det derfor være gyldigt, hvis der også er mindst én linje, hvor antallet er mindre end 20 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="b58b3-195">Lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="b58b3-195">Location directives</span></span>

<span data-ttu-id="b58b3-196">Hvis du bruger standarddata fra Contoso, kræver forespørgslen til handling i lokationsvejledning ikke ændringer.</span><span class="sxs-lookup"><span data-stu-id="b58b3-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="b58b3-197">Hvis du vil være sikker på, at lokationsvejledninger registrerer varerne på salgsordrerne, når du anvender funktionen i et miljø, der ikke er Contoso, skal du oprette en ny lokalitetsvejledning.</span><span class="sxs-lookup"><span data-stu-id="b58b3-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="b58b3-198">Udfør følgende trin for at kontrollere indstillingerne i demomiljøet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="b58b3-199">Gå til **Lagerstedsstyring** \> **Opsætning** \> **Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="b58b3-200">I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="b58b3-201">Vælg lokationsvejledningen med navnet *51 Pluk*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="b58b3-202">Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg linjen for handlingen **Pluk**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="b58b3-203">Vælg **Rediger forespørgsel** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="b58b3-204">Gennemgå forespørgslen **Område**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="b58b3-205">Find den linje, hvor feltet **Felt** er angivet til *Lokation*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="b58b3-206">Kontroller, at feltet **Afgrænsning** er tomt (dvs. der er ingen begrænsninger).</span><span class="sxs-lookup"><span data-stu-id="b58b3-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="b58b3-207">Scenario</span><span class="sxs-lookup"><span data-stu-id="b58b3-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="b58b3-208">Oprette arbejde med salgsordrepluk</span><span class="sxs-lookup"><span data-stu-id="b58b3-208">Create sales order picking work</span></span>

<span data-ttu-id="b58b3-209">Inden der køres systembaseret plukning, skal der oprettes noget udgående arbejde.</span><span class="sxs-lookup"><span data-stu-id="b58b3-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="b58b3-210">I dette scenarie opretter du fire salgsordrer, der er baseret på de angivne systembaserede arbejdssekvensforespørgsler.</span><span class="sxs-lookup"><span data-stu-id="b58b3-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="b58b3-211">Du kan reservere lagerantal for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="b58b3-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="b58b3-212">Det reserverede lager kan derfor ikke trækkes fra lagerstedet i forbindelse med andre ordrer, medmindre lagerreservationen eller en del af lagerreservationen annulleres.</span><span class="sxs-lookup"><span data-stu-id="b58b3-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="b58b3-213">Du skal derefter frigive hver salgsordre til lagerstedet for at oprette det udgående arbejde.</span><span class="sxs-lookup"><span data-stu-id="b58b3-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="b58b3-214">Salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="b58b3-214">Sales order 1</span></span>

1. <span data-ttu-id="b58b3-215">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b58b3-216">Vælg **Ny** i handlingsruden for at oprette en salgsordre 1.</span><span class="sxs-lookup"><span data-stu-id="b58b3-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="b58b3-217">Angiv følgende værdier i dialogboksen **Opret salgsordre** :</span><span class="sxs-lookup"><span data-stu-id="b58b3-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b58b3-218">Gå til sektionen **Kunde** , indstil feltet **Debitorkonto** til *US-004*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="b58b3-219">I sektionen **Generelt** skal du indstille **Lagersted** til *51*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="b58b3-220">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="b58b3-221">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b58b3-222">Føj en linje til den nye salgsordre, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-223">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="b58b3-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="b58b3-224">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="b58b3-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="b58b3-225">Vælg **reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b58b3-226">På siden **Reservation** skal du vælge **Reserver parti** for at reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="b58b3-227">Luk siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="b58b3-228">I handlingsruden skal du på fanen **Lagersted** vælge **Frigiv til lagersted** for at oprette lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="b58b3-229">Du modtager orienterende meddelelser, der viser bølge-id'et og forsendelses-id'et, der blev oprettet for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b58b3-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="b58b3-230">Salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="b58b3-230">Sales order 2</span></span>

1. <span data-ttu-id="b58b3-231">Vælg **Ny** i handlingsruden for at oprette en salgsordre 2.</span><span class="sxs-lookup"><span data-stu-id="b58b3-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="b58b3-232">Angiv følgende værdier i dialogboksen **Opret salgsordre** :</span><span class="sxs-lookup"><span data-stu-id="b58b3-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b58b3-233">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b58b3-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b58b3-234">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b3-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b3-235">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="b58b3-236">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b58b3-237">Føj en linje til den nye salgsordre, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-238">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="b58b3-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="b58b3-239">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="b58b3-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="b58b3-240">Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-241">**Varenummer:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="b58b3-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="b58b3-242">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="b58b3-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b58b3-243">Reservér lager for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="b58b3-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="b58b3-244">Frigive ordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="b58b3-245">Salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="b58b3-245">Sales order 3</span></span>

1. <span data-ttu-id="b58b3-246">Vælg **Ny** i handlingsruden for at oprette en salgsordre 3.</span><span class="sxs-lookup"><span data-stu-id="b58b3-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="b58b3-247">Angiv følgende værdier i dialogboksen **Opret salgsordre** :</span><span class="sxs-lookup"><span data-stu-id="b58b3-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b58b3-248">**Debitorkonto:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="b58b3-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="b58b3-249">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b3-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b3-250">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="b58b3-251">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b58b3-252">Føj en linje til den nye salgsordre, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-253">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="b58b3-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="b58b3-254">**Antal:** *7*</span><span class="sxs-lookup"><span data-stu-id="b58b3-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="b58b3-255">Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-256">**Varenummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="b58b3-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="b58b3-257">**Antal:** *8*</span><span class="sxs-lookup"><span data-stu-id="b58b3-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="b58b3-258">Reservér lager for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="b58b3-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="b58b3-259">Frigive ordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="b58b3-260">Salgsordre 4</span><span class="sxs-lookup"><span data-stu-id="b58b3-260">Sales order 4</span></span>

1. <span data-ttu-id="b58b3-261">Vælg **Ny** i handlingsruden for at oprette en salgsordre 4.</span><span class="sxs-lookup"><span data-stu-id="b58b3-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="b58b3-262">Angiv følgende værdier i dialogboksen **Opret salgsordre** :</span><span class="sxs-lookup"><span data-stu-id="b58b3-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b58b3-263">**Debitorkonto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="b58b3-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="b58b3-264">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="b58b3-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b58b3-265">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="b58b3-266">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="b58b3-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="b58b3-267">Føj en linje til den nye salgsordre, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-268">**Varenummer:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="b58b3-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="b58b3-269">**Antal:** *25*</span><span class="sxs-lookup"><span data-stu-id="b58b3-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="b58b3-270">Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="b58b3-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="b58b3-271">**Varenummer:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="b58b3-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="b58b3-272">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="b58b3-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="b58b3-273">Reservér lager for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="b58b3-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="b58b3-274">Frigive ordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="b58b3-275">Hent arbejds-id'er for det arbejde, der er oprettet</span><span class="sxs-lookup"><span data-stu-id="b58b3-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="b58b3-276">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b58b3-277">Filtrer på feltet **Lagersted** , så der kun vises arbejde for lagersted *51*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="b58b3-278">Der skal være oprettet fire arbejds-id'er.</span><span class="sxs-lookup"><span data-stu-id="b58b3-278">Four work IDs should have been created.</span></span> <span data-ttu-id="b58b3-279">Noter arbejds-id'et for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="b58b3-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="b58b3-280">Salgsordre-id</span><span class="sxs-lookup"><span data-stu-id="b58b3-280">Sales order ID</span></span> | <span data-ttu-id="b58b3-281">Arbejds-id</span><span class="sxs-lookup"><span data-stu-id="b58b3-281">Work ID</span></span> | <span data-ttu-id="b58b3-282">Arbejdsantal</span><span class="sxs-lookup"><span data-stu-id="b58b3-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="b58b3-283">Salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="b58b3-283">Sales Order 1</span></span> | <span data-ttu-id="b58b3-284">Arbejds-id 1</span><span class="sxs-lookup"><span data-stu-id="b58b3-284">Work ID 1</span></span> | <span data-ttu-id="b58b3-285">20 ea</span><span class="sxs-lookup"><span data-stu-id="b58b3-285">20 ea</span></span> |
    | <span data-ttu-id="b58b3-286">Salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="b58b3-286">Sales Order 2</span></span> | <span data-ttu-id="b58b3-287">Arbejds-id 2</span><span class="sxs-lookup"><span data-stu-id="b58b3-287">Work ID 2</span></span> | <span data-ttu-id="b58b3-288">6 ea (summen af begge linjer)</span><span class="sxs-lookup"><span data-stu-id="b58b3-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="b58b3-289">Salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="b58b3-289">Sales Order 3</span></span> | <span data-ttu-id="b58b3-290">Arbejds-id 3</span><span class="sxs-lookup"><span data-stu-id="b58b3-290">Work ID 3</span></span> | <span data-ttu-id="b58b3-291">15 ea (summen af begge linjer)</span><span class="sxs-lookup"><span data-stu-id="b58b3-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="b58b3-292">Salgsordre 4</span><span class="sxs-lookup"><span data-stu-id="b58b3-292">Sales Order 4</span></span> | <span data-ttu-id="b58b3-293">Arbejds-id 4</span><span class="sxs-lookup"><span data-stu-id="b58b3-293">Work ID 4</span></span> | <span data-ttu-id="b58b3-294">35 ea (summen af begge linjer)</span><span class="sxs-lookup"><span data-stu-id="b58b3-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="b58b3-295">Før du kører processen på mobilenheden, skal du sørge for, at kun det arbejde, du netop har oprettet, har statussen *Åben* for lagersted *51* og arbejdsordretypen *Salgsordre*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="b58b3-296">Ellers kan testresultaterne variere, fordi systembaseret plukning vil omfatte alt berettiget arbejde.</span><span class="sxs-lookup"><span data-stu-id="b58b3-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="b58b3-297">Gå til **Lokationsstyring \> Arbejde \> Udgående \> Åbent salgsarbejde**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="b58b3-298">Gå til gitteret **Åbent salgsarbejde** , filtrer efter feltet **Lagersted** , så kun arbejde for lagersted *51* vises.</span><span class="sxs-lookup"><span data-stu-id="b58b3-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="b58b3-299">Bekræft, at det kun er de fire arbejds-id'er, du har oprettet tidligere, der vises.</span><span class="sxs-lookup"><span data-stu-id="b58b3-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="b58b3-300">Luk siden **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="b58b3-301">Udførelse af mobilenhedsproces</span><span class="sxs-lookup"><span data-stu-id="b58b3-301">Mobile device flow execution</span></span>

<span data-ttu-id="b58b3-302">På basis af opsætningen føder systemet brugeren arbejde, der er sorteret fra det højeste linjeantal til det laveste.</span><span class="sxs-lookup"><span data-stu-id="b58b3-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="b58b3-303">Antallet på hver linje vil være mindre end 20 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="b58b3-304">Husk, at denne opsætning vil hente alle de ressourcer, der har mindst én linje, hvor antallet er mindre end 20 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="b58b3-305">Hvis arbejdet derfor har en anden linje, hvor antallet er nøjagtigt 20 ea. eller mere end 20 ea., vil det også være gyldigt.</span><span class="sxs-lookup"><span data-stu-id="b58b3-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="b58b3-306">Mobilapp</span><span class="sxs-lookup"><span data-stu-id="b58b3-306">Mobile app</span></span>

1. <span data-ttu-id="b58b3-307">Log på lagerstedsappen som en bruger på lagersted *51*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="b58b3-308">Gå til **Udgående \> Salgsplukning – System**.</span><span class="sxs-lookup"><span data-stu-id="b58b3-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="b58b3-309">Pluktrinnet for arbejds-id *4* vises.</span><span class="sxs-lookup"><span data-stu-id="b58b3-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="b58b3-310">Dette arbejds-id vises først på grund af opsætningen af den systembaserede forespørgselsrækkefølge, hvor du angav, at arbejdet skal sorteres baseret på faldende linjeantal i arbejdet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="b58b3-311">Afslut den krævede plukning, og læg den på lager for at lukke arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="b58b3-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="b58b3-312">Derefter vises arbejds-id *3*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="b58b3-313">En af dens arbejdslinjer er den næste i rækkefølgen baseret på linjeantallet i arbejdet.</span><span class="sxs-lookup"><span data-stu-id="b58b3-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="b58b3-314">Afslut plukningen, og læg den på lager for at lukke arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="b58b3-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="b58b3-315">Derefter vises arbejds-id *2*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="b58b3-316">Dette arbejdes pluklinje er den næste i rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="b58b3-317">Afslut plukningen, og læg den på lager for at lukke arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="b58b3-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="b58b3-318">Der bør ikke vises yderligere arbejde for dig.</span><span class="sxs-lookup"><span data-stu-id="b58b3-318">No further work should be presented to you.</span></span> <span data-ttu-id="b58b3-319">Arbejds-id *1* er ikke gyldigt for dette mobilenhedsmenupunkt, fordi forespørgslen angiver, at arbejdsoverskrifter kun tages i betragtning, hvis antallet på arbejdslinjerne er mindre end 20 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="b58b3-320">Tip!</span><span class="sxs-lookup"><span data-stu-id="b58b3-320">Tips</span></span>

<span data-ttu-id="b58b3-321">De systembaserede arbejdsrækkefølgeforespørgsler er *inklusive*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="b58b3-322">Det er vigtigt, at du husker dette i forbindelse med nogle af opsætningerne.</span><span class="sxs-lookup"><span data-stu-id="b58b3-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="b58b3-323">Du ønsker f. eks., at et bestemt menupunkt kun skal behandle arbejde, hvor arbejdsenheden er *ea* , og du angiver denne begrænsning under fanen **Område** i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-323">For example, you want a specific menu item to process only work where the work unit is *ea* , and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="b58b3-324">I dette tilfælde vil alle de opgaver, hvor mindst én arbejdslinje har arbejdsenheden indstillet til *ea* , blive overført til arbejderen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="b58b3-325">Dette arbejde kan derfor også omfatte arbejde, hvor arbejdslinjer har en anden arbejdsenhed end *ea* (f.eks. *kasse* eller *palle* ).</span><span class="sxs-lookup"><span data-stu-id="b58b3-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet* ).</span></span> <span data-ttu-id="b58b3-326">Forespørgslen udelader kun det arbejde, hvor ingen linjer for arbejdslinjen er angivet til *ea*.</span><span class="sxs-lookup"><span data-stu-id="b58b3-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="b58b3-327">I eksemplet med dette scenarie blev arbejds-id *4* derfor også hentet af forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="b58b3-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="b58b3-328">Da den blev oprettet, blev der tilføjet to linjer: en til 25 ea og en anden til 10 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="b58b3-329">Arbejdet blev stadig vist for brugeren, fordi mindst én arbejdslinje har et antal på mindre end 20 ea.</span><span class="sxs-lookup"><span data-stu-id="b58b3-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="b58b3-330">Afhængigt af scenariet kan du forhindre dette ved at bruge arbejdspauser.</span><span class="sxs-lookup"><span data-stu-id="b58b3-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
