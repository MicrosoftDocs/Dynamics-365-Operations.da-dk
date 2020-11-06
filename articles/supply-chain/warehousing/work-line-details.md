---
title: Arbejdslinjedetaljer
description: Dette emne indeholder oplysninger om siden Oplysninger om arbejdslinje, der viser en omfattende, sorterbar og filtrerbar liste over de individuelle arbejdslinjer i systemet.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015889"
---
# <a name="work-line-details"></a><span data-ttu-id="15eab-103">Arbejdslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="15eab-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15eab-104">Siden **Oplysninger om arbejdslinje** viser en omfattende, sorterbar og filtrerbar liste over de individuelle arbejdslinjer i systemet.</span><span class="sxs-lookup"><span data-stu-id="15eab-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="15eab-105">Den indeholder en komplet oversigt over arbejde, der planlægges og udføres på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="15eab-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="15eab-106">Du kan nemt skifte mellem at få vist alle arbejdslinjer og kun få vist åbne arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="15eab-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="15eab-107">De detaljer, der er angivet for hver linje, omfatter arbejdsstatus, varenummer, lokation, arbejdsmængde, last-id og forsendelses-id.</span><span class="sxs-lookup"><span data-stu-id="15eab-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="15eab-108">Aktivér funktionen Oplysninger om arbejdslinje</span><span class="sxs-lookup"><span data-stu-id="15eab-108">Turn on the work line details feature</span></span>

<span data-ttu-id="15eab-109">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="15eab-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="15eab-110">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="15eab-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="15eab-111">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="15eab-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="15eab-112">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="15eab-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="15eab-113">**Funktionsnavn:** *Oplysninger om arbejdslinje*</span><span class="sxs-lookup"><span data-stu-id="15eab-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="15eab-114">Åbne og bruge siden Oplysninger om arbejdslinje</span><span class="sxs-lookup"><span data-stu-id="15eab-114">Open and use the Work line details page</span></span>

<span data-ttu-id="15eab-115">Hvis du vil have vist listen over oplysninger om arbejdslinjer, skal du gå til **Lokationsstyring \> Arbejde \> Oplysninger om arbejdslinje**.</span><span class="sxs-lookup"><span data-stu-id="15eab-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="15eab-116">Herfra kan du udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="15eab-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="15eab-117">Brug feltet **Filtrer** til at søge efter linjer, der har en bestemt værdi, for alle tilgængelige parametre.</span><span class="sxs-lookup"><span data-stu-id="15eab-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="15eab-118">(Tilgængelige parametre omfatter mange parametre, der ikke vises som kolonner i gitteret).</span><span class="sxs-lookup"><span data-stu-id="15eab-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="15eab-119">Brug afkrydsningsfeltet **Vis lukket** for at få vist eller skjule lukkede linjer.</span><span class="sxs-lookup"><span data-stu-id="15eab-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="15eab-120">Vælg **Vis dimensioner** for at åbne dialogboksen **Dimensionsvisning** , hvor du kan vælge at få vist eller skjule forskellige dimensionskolonner i gitteret.</span><span class="sxs-lookup"><span data-stu-id="15eab-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="15eab-121">Vælg en kolonneoverskrift for at åbne en menu, hvor du kan vælge at sortere eller filtrere listen efter værdier i den pågældende kolonne.</span><span class="sxs-lookup"><span data-stu-id="15eab-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="15eab-122">Vælg en arbejdslinje, og vælg derefter **Skift lokation** for at åbne en dialogboks, hvor du kan ændre placeringen for den pågældende arbejdslinje.</span><span class="sxs-lookup"><span data-stu-id="15eab-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="15eab-123">Den lokation, du angiver, tilsidesætter opsætningen af lokationsvejledningen.</span><span class="sxs-lookup"><span data-stu-id="15eab-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="15eab-124">Vælg en arbejdslinje, og vælg derefter **Annuller arbejdslinje** for at åbne en dialogboks, hvor du helt eller delvist kan reducere antallet på den pågældende arbejdslinje.</span><span class="sxs-lookup"><span data-stu-id="15eab-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="15eab-125">Juster antal.</span><span class="sxs-lookup"><span data-stu-id="15eab-125">Adjust quantities.</span></span>
- <span data-ttu-id="15eab-126">Få vist posteringerne bag en vilkårlig arbejdslinje.</span><span class="sxs-lookup"><span data-stu-id="15eab-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="15eab-127">Prøv funktionen</span><span class="sxs-lookup"><span data-stu-id="15eab-127">Try out the feature</span></span>

<span data-ttu-id="15eab-128">Dette afsnit indeholder en demoversion i tre dele, der viser, hvordan du kan arbejde med oplysninger om arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="15eab-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="15eab-129">Gøre eksempeldata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="15eab-129">Make sample data available</span></span>

<span data-ttu-id="15eab-130">Hvis du vil arbejde gennem denne demo ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="15eab-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="15eab-131">Derudover skal du vælge den juridiske enhed **USMF** , før du starter.</span><span class="sxs-lookup"><span data-stu-id="15eab-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="15eab-132">Du kan også bruge denne demonstration som vejledning, når du arbejder i et produktionssystem.</span><span class="sxs-lookup"><span data-stu-id="15eab-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="15eab-133">Du skal dog erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.</span><span class="sxs-lookup"><span data-stu-id="15eab-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="15eab-134">Kontroller, at scenarieopsætningen indeholder en tilstrækkelig disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="15eab-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="15eab-135">Hvis du arbejder med **USMF** -demodataene, skal du først sikre dig, at systemet er konfigureret, så der er en tilstrækkelig lagerbeholdning på hver af de relevante pluklokationer.</span><span class="sxs-lookup"><span data-stu-id="15eab-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="15eab-136">I denne demo er der en forventning om, at du har den følgende tilgængelige lagerbeholdning:</span><span class="sxs-lookup"><span data-stu-id="15eab-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="15eab-137">**Vare M9200:** 45 ea.</span><span class="sxs-lookup"><span data-stu-id="15eab-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="15eab-138">(eller mere)</span><span class="sxs-lookup"><span data-stu-id="15eab-138">(or more)</span></span>
- <span data-ttu-id="15eab-139">**Vare M9202:** 10 ea.</span><span class="sxs-lookup"><span data-stu-id="15eab-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="15eab-140">(eller mere)</span><span class="sxs-lookup"><span data-stu-id="15eab-140">(or more)</span></span>

<span data-ttu-id="15eab-141">Udfør følgende trin for at kontrollere, om der er tilstrækkelig lager til rådighed, og om det er nødvendigt at foretage justeringer.</span><span class="sxs-lookup"><span data-stu-id="15eab-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="15eab-142">Gå til **Lokationsstyring \> Konfiguration \> Lokationsvejledninger** , og bestem, hvilke pluklokationer der bruges til plukning af salgsordre på lagersted 51.</span><span class="sxs-lookup"><span data-stu-id="15eab-142">Go to **Warehouse management \> Setup \> Location directives** , and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="15eab-143">(Få flere oplysninger under [Styre lagerarbejde ved hjælp af arbejdsskabeloner og lokalitetsdirektiver](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="15eab-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="15eab-144">Kontrollér lagerniveauerne på de relevante lokationer.</span><span class="sxs-lookup"><span data-stu-id="15eab-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="15eab-145">Regulere lagerbeholdning efter behov.</span><span class="sxs-lookup"><span data-stu-id="15eab-145">Adjust inventory as required.</span></span> <span data-ttu-id="15eab-146">Du kan oprette manuelle bevægelser, bruge genopfyldning eller anvende et andet flow til at regulere lagerbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="15eab-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="15eab-147">Del 1: Oprette plukarbejde</span><span class="sxs-lookup"><span data-stu-id="15eab-147">Part 1: Create picking work</span></span>

<span data-ttu-id="15eab-148">Før du begynder at oprette arbejdet, skal du kontrollere, at lagerstedet er konfigureret til at reagere på anmodninger på en bestemt måde.</span><span class="sxs-lookup"><span data-stu-id="15eab-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="15eab-149">Benyt følgende fremgangsmåde for at oprette noget plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="15eab-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="15eab-150">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="15eab-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="15eab-151">Vælg **Ny** for at åbne dialogboksen **Opret salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="15eab-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="15eab-152">Angiv følgende værdier i dialogboksen **Opret salgsordre** :</span><span class="sxs-lookup"><span data-stu-id="15eab-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="15eab-153">Gå til oversigtspanelet **Kunde** , indstil feltet **Kundekonto** til _US-001_.</span><span class="sxs-lookup"><span data-stu-id="15eab-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="15eab-154">I oversigtspanelet **Generelt** skal du indstille **Lagersted** til _51_.</span><span class="sxs-lookup"><span data-stu-id="15eab-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="15eab-155">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="15eab-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="15eab-156">Din nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="15eab-156">Your new sales order is opened.</span></span> <span data-ttu-id="15eab-157">Den omfatter en ny, tom række i gitteret **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="15eab-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="15eab-158">Angiv følgende værdier på denne ordrelinje:</span><span class="sxs-lookup"><span data-stu-id="15eab-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="15eab-159">**Varenummer:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="15eab-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="15eab-160">**Antal:** _20_</span><span class="sxs-lookup"><span data-stu-id="15eab-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="15eab-161">**Enhed:** _Styk_</span><span class="sxs-lookup"><span data-stu-id="15eab-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="15eab-162">Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** for at åbne siden **Reservation**.</span><span class="sxs-lookup"><span data-stu-id="15eab-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="15eab-163">På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="15eab-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="15eab-164">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="15eab-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="15eab-165">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="15eab-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="15eab-166">Systemet opretter en forsendelse, føjer den til en ny last og opretter det nødvendige arbejde.</span><span class="sxs-lookup"><span data-stu-id="15eab-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="15eab-167">Opret endnu en salgsordre for den samme debitorkonto og det lagersted, som du brugte til den første ordre.</span><span class="sxs-lookup"><span data-stu-id="15eab-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="15eab-168">Føj følgende to ordrelinjer til denne ordre:</span><span class="sxs-lookup"><span data-stu-id="15eab-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="15eab-169">**Linje 1:** Indstil feltet **Varenummer** til _M9200_ , feltet **Antal** til _25_ og feltet **Enhed** til _EA_.</span><span class="sxs-lookup"><span data-stu-id="15eab-169">**Line 1:** Set the **Item number** field to _M9200_ , the **Quantity** field to _25_ , and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="15eab-170">**Linje 2:** Indstil feltet **Varenummer** til _M9202_ , feltet **Antal** til _10_ og feltet **Enhed** til _EA_.</span><span class="sxs-lookup"><span data-stu-id="15eab-170">**Line 2:** Set the **Item number** field to _M9202_ , the **Quantity** field to _10_ , and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="15eab-171">Gentag trin 6 til 8 for at reservere lageret for hver ordrelinje (en ad gangen), og gentag derefter trin 9 for at frigive ordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="15eab-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="15eab-172">Del 2: Ændre lokationen for en arbejdslinje</span><span class="sxs-lookup"><span data-stu-id="15eab-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="15eab-173">Gå til **Lagerstedsstyring \> Arbejde \> Oplysninger om arbejdslinje**.</span><span class="sxs-lookup"><span data-stu-id="15eab-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="15eab-174">Find og vælg en af de arbejdslinjer, du har oprettet for denne demo.</span><span class="sxs-lookup"><span data-stu-id="15eab-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="15eab-175">Vælg **Skift lokation** for at åbne dialogboksen **Vælg ny lokation**.</span><span class="sxs-lookup"><span data-stu-id="15eab-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="15eab-176">Gå til dialogboksen **Vælg ny lokation** i feltet **Lokation** , og vælg en ny lokation for arbejdslinjen.</span><span class="sxs-lookup"><span data-stu-id="15eab-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="15eab-177">Vælg **OK** for at anvende din ændring, og luk dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="15eab-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15eab-178">Du kan kun sende lokationsændringer, hvis den nye lokation har tilstrækkeligt lager til rådighed (til et pluk), eller hvis dens lokationstype kan valideres (til placer).</span><span class="sxs-lookup"><span data-stu-id="15eab-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="15eab-179">Del 3: Ændre antallet på en arbejdslinje eller annullere en arbejdslinje</span><span class="sxs-lookup"><span data-stu-id="15eab-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="15eab-180">Gå til **Lagerstedsstyring \> Arbejde \> Oplysninger om arbejdslinje**.</span><span class="sxs-lookup"><span data-stu-id="15eab-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="15eab-181">Find og vælg en af de arbejdslinjer, du har oprettet for denne demo.</span><span class="sxs-lookup"><span data-stu-id="15eab-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="15eab-182">Bemærk, at du kun kan annullere eller ændre antal for arbejdslinjer, hvis arbejdstypen er _pluk_.</span><span class="sxs-lookup"><span data-stu-id="15eab-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="15eab-183">Vælg **Annuller arbejdslinje** for at åbne dialogboksen **Antal, der skal annulleres**.</span><span class="sxs-lookup"><span data-stu-id="15eab-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="15eab-184">I dialogboksen **Antal, der skal annulleres** skal du ændre værdien i feltet **Antal** for at angive det antal, der skal *trækkes fra* det antal, der aktuelt er angivet for linjen.</span><span class="sxs-lookup"><span data-stu-id="15eab-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="15eab-185">Feltet **Antal** viser som standard det samlede antal.</span><span class="sxs-lookup"><span data-stu-id="15eab-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="15eab-186">Hvis du annullerer det samlede antal, ændres værdien for **Arbejdsstatus** til _Annulleret_ , men feltet **Arbejdsantal** vil stadig vise den oprindelige værdi.</span><span class="sxs-lookup"><span data-stu-id="15eab-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_ , but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="15eab-187">Hvis du blot annuller en del af antallet, opdateres feltet **Arbejdsantal** for at vise den nye værdi, men værdien **Arbejdsstatus** ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="15eab-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="15eab-188">Vælg **OK** for at anvende din ændring, og luk dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="15eab-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15eab-189">Hvis du kun vil annullere en del af antallet for en arbejdslinje, skal du også fjerne det forældede antal fra lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="15eab-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="15eab-190">Hvis ikke, medmindre underlevering er konfigureret korrekt, kan lastlinjen ikke leveres/bekræftes.</span><span class="sxs-lookup"><span data-stu-id="15eab-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>
