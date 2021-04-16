---
title: Skift arbejdspulje på arbejde
description: I dette emne forklares det, hvordan du kan bruge knappen Skift arbejdspulje for arbejdselementer til at ændre arbejdspuljen for eksisterende arbejde.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cdd0a1b6d022c958e00a1ba8fa87a8715ff88ce5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808888"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="da4da-103">Skift arbejdspulje på arbejde</span><span class="sxs-lookup"><span data-stu-id="da4da-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da4da-104">Du kan bruge arbejdspuljer til at organisere arbejde i grupper.</span><span class="sxs-lookup"><span data-stu-id="da4da-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="da4da-105">Du kan f.eks. oprette en arbejdsgruppe til at klassificere arbejde, der opstår på et bestemt lagersted.</span><span class="sxs-lookup"><span data-stu-id="da4da-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="da4da-106">Funktionen *Skift arbejdspulje på arbejde* tilføjer knappen **Skift arbejdspulje** i handlingsruden for arbejdselementer.</span><span class="sxs-lookup"><span data-stu-id="da4da-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="da4da-107">Lagercheferne kan derfor nemt ændre arbejdspuljen for eksisterende arbejde.</span><span class="sxs-lookup"><span data-stu-id="da4da-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="da4da-108">Denne funktion giver cheferne mulighed for hurtigt at reagere på ændringer i lagerstedets produktion, og det er med til at forbedre deres evne til at tilpasse sig skiftende situationer og behovet for at overføre arbejde til en anden arbejdsgruppe.</span><span class="sxs-lookup"><span data-stu-id="da4da-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="da4da-109">Aktivere funktionen Skift arbejdspulje på arbejde</span><span class="sxs-lookup"><span data-stu-id="da4da-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="da4da-110">Før du begynder at konfigurere eller bruge denne funktion, skal du sørge for, at den er tilgængelig i systemet.</span><span class="sxs-lookup"><span data-stu-id="da4da-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="da4da-111">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="da4da-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="da4da-112">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="da4da-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="da4da-113">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="da4da-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="da4da-114">**Funktionsnavn:** *Skift arbejdspulje på arbejde*</span><span class="sxs-lookup"><span data-stu-id="da4da-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="da4da-115">Konfigurere funktionen Skift arbejdspulje på arbejde</span><span class="sxs-lookup"><span data-stu-id="da4da-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="da4da-116">Hvis du vil bruge denne funktion, skal der være konfigureret nogle arbejdspuljer.</span><span class="sxs-lookup"><span data-stu-id="da4da-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="da4da-117">Du kan også oprette arbejdsskabeloner, så de automatisk tildeler en pulje.</span><span class="sxs-lookup"><span data-stu-id="da4da-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="da4da-118">Hvis du vil arbejde i det eksempelscenarie, der er angivet senere i dette emne, skal du konfigurere systemet som beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="da4da-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="da4da-119">Konfigurere arbejdspuljer</span><span class="sxs-lookup"><span data-stu-id="da4da-119">Set up work pools</span></span>

<span data-ttu-id="da4da-120">Med arbejdspuljer kan du organisere arbejdselementer efter type.</span><span class="sxs-lookup"><span data-stu-id="da4da-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="da4da-121">Hvis du vil arbejde med funktionen *Skift arbejdspulje på arbejde*, skal du have mindst to tilgængelige arbejdspuljer.</span><span class="sxs-lookup"><span data-stu-id="da4da-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="da4da-122">Benyt følgende fremgangsmåde for at få vist og tilføje arbejdspuljer.</span><span class="sxs-lookup"><span data-stu-id="da4da-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="da4da-123">Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdspuljer**.</span><span class="sxs-lookup"><span data-stu-id="da4da-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="da4da-124">Hvis du arbejder med demonstrationsdata fra **USMF**-firmaet og gerne vil arbejde dig gennem eksempelscenariet senere i dette emne, skal du tilføje to arbejdspulje, der skal have følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="da4da-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="da4da-125">Arbejdspulje 1:</span><span class="sxs-lookup"><span data-stu-id="da4da-125">Work pool 1:</span></span>

        - <span data-ttu-id="da4da-126">**Arbejdspulje-id:** *Webbutik*</span><span class="sxs-lookup"><span data-stu-id="da4da-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="da4da-127">**Beskrivelse:** *Webbutik*</span><span class="sxs-lookup"><span data-stu-id="da4da-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="da4da-128">Arbejdspulje 2:</span><span class="sxs-lookup"><span data-stu-id="da4da-128">Work pool 2:</span></span>

        - <span data-ttu-id="da4da-129">**Arbejdspulje-id:** *Callcenter*</span><span class="sxs-lookup"><span data-stu-id="da4da-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="da4da-130">**Beskrivelse:** *Callcenter*</span><span class="sxs-lookup"><span data-stu-id="da4da-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="da4da-131">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="da4da-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="da4da-132">Konfigurer arbejdsskabeloner</span><span class="sxs-lookup"><span data-stu-id="da4da-132">Set up work templates</span></span>

<span data-ttu-id="da4da-133">For hver af dine arbejdsskabeloner kan du angive en standardarbejdspulje, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="da4da-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="da4da-134">For hver relevant skabelon kan du tildele en arbejdspulje i kolonnen **Arbejdspulje-id**.</span><span class="sxs-lookup"><span data-stu-id="da4da-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="da4da-135">I dette tilfælde arver alle de arbejdselementer, der genereres ved hjælp af en bestemt skabelon, automatisk den tildelte arbejdspulje.</span><span class="sxs-lookup"><span data-stu-id="da4da-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="da4da-136">Hvis du arbejder med demonstrationsdataene fra **USMF**-firmaet og gerne vil arbejde dig gennem eksempelscenariet senere i dette emne, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="da4da-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="da4da-137">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="da4da-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="da4da-138">Vælg **Rediger** i handlingsruden for at sætte siden i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="da4da-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="da4da-139">Rediger skabelonen ved at angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="da4da-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="da4da-140">**Arbejdsskabelon:** *62 Pluk til pakke*</span><span class="sxs-lookup"><span data-stu-id="da4da-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="da4da-141">**Arbejdspulje-id:** *Webbutik*</span><span class="sxs-lookup"><span data-stu-id="da4da-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="da4da-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="da4da-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="da4da-143">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="da4da-143">Example scenario</span></span>

<span data-ttu-id="da4da-144">Dette scenarie viser, hvordan du kan ændre behandlingsstrømmen for et eksisterende arbejdselement ved at ændre dets arbejdspulje.</span><span class="sxs-lookup"><span data-stu-id="da4da-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="da4da-145">Det bruger demodata fra **USMF**-firmaet og de indstillinger, der blev foreslået tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="da4da-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="da4da-146">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="da4da-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="da4da-147">Bekræft, at der er en tilstrækkelig disponibel lagerbeholdning for varerne *A0001* og *A0002* på lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="da4da-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="da4da-148">Gå til **Lagerstyring \> Forespørgsler og rapporter \> Beholdningsliste**, og rediger de filtre, der vises her:</span><span class="sxs-lookup"><span data-stu-id="da4da-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="da4da-149">Værdien **Lager** begynder med *62*.</span><span class="sxs-lookup"><span data-stu-id="da4da-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="da4da-150">Værdien **Varenummer** er enten *A001* eller *A002*.</span><span class="sxs-lookup"><span data-stu-id="da4da-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="da4da-151">Demodata skal have et antal på 10 pr. stk.</span><span class="sxs-lookup"><span data-stu-id="da4da-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="da4da-152">Derefter skal du oprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="da4da-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="da4da-153">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="da4da-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="da4da-154">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="da4da-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="da4da-155">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="da4da-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="da4da-156">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="da4da-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="da4da-157">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="da4da-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="da4da-158">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="da4da-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="da4da-159">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="da4da-159">The new sales order is opened.</span></span> <span data-ttu-id="da4da-160">Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="da4da-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="da4da-161">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="da4da-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="da4da-162">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="da4da-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="da4da-163">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="da4da-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="da4da-164">Vælg **reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="da4da-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="da4da-165">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="da4da-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="da4da-166">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="da4da-166">Close the page.</span></span>
1. <span data-ttu-id="da4da-167">Gå til oversigtspanelet **Salgsordrelinjer**, vælg **Tilføj linje** for at føje en anden linje til din salgsordre.</span><span class="sxs-lookup"><span data-stu-id="da4da-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="da4da-168">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="da4da-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="da4da-169">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="da4da-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="da4da-170">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="da4da-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="da4da-171">Vælg **reservation** i menuen **Lager** oven over gitteret.</span><span class="sxs-lookup"><span data-stu-id="da4da-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="da4da-172">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="da4da-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="da4da-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="da4da-173">Close the page.</span></span>
1. <span data-ttu-id="da4da-174">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="da4da-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="da4da-175">Du modtager orienterende meddelelser, der viser bølge-id'et og forsendelses-id'et, der blev oprettet fra frigivelsen.</span><span class="sxs-lookup"><span data-stu-id="da4da-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="da4da-176">Notér dig bølge-id'et.</span><span class="sxs-lookup"><span data-stu-id="da4da-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="da4da-177">Gennemse den udgående bølge</span><span class="sxs-lookup"><span data-stu-id="da4da-177">Review the outbound wave</span></span>

1. <span data-ttu-id="da4da-178">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="da4da-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="da4da-179">Søg efter det bølge-id, der er oprettet ud fra frigivelsen af salgsordren, i gitteret.</span><span class="sxs-lookup"><span data-stu-id="da4da-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="da4da-180">Vælg bølge-id'et for at få vist detaljerne.</span><span class="sxs-lookup"><span data-stu-id="da4da-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="da4da-181">Gå til oversigtspanelet **Bølgelinjer**, og sørg for, at forsendelses-id'et vises for salgsordren.</span><span class="sxs-lookup"><span data-stu-id="da4da-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="da4da-182">Hvis indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** er angivet til *Nej* i opsætningen af forsendelsesbølgeskabelonen, skal du behandle bølgen manuelt ved at vælge **Behandl** under fanen **Bølge** i handlingsruden for at oprette arbejde.</span><span class="sxs-lookup"><span data-stu-id="da4da-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="da4da-183">Kontrollér, at bølgen er blevet behandlet.</span><span class="sxs-lookup"><span data-stu-id="da4da-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="da4da-184">Denne behandling opretter det nødvendige arbejde.</span><span class="sxs-lookup"><span data-stu-id="da4da-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="da4da-185">Få vist oplysninger om arbejde og ændre arbejdspuljen</span><span class="sxs-lookup"><span data-stu-id="da4da-185">View work details and change the work pool</span></span>

<span data-ttu-id="da4da-186">Du kan bruge siden **Arbejdsdetaljer** til at få vist det arbejde, der er oprettet, og til at administrere arbejdspuljen.</span><span class="sxs-lookup"><span data-stu-id="da4da-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="da4da-187">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="da4da-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="da4da-188">Vælg rækken for det arbejde, der netop er oprettet.</span><span class="sxs-lookup"><span data-stu-id="da4da-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="da4da-189">Kolonnen **Ordrenummer** viser nummeret på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="da4da-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="da4da-190">Feltet **Arbejdspulje-id** indstilles til det arbejdspulje-id, der blev konfigureret i arbejdsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="da4da-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="da4da-191">Hvis du ikke kan se feltet **Arbejdspulje-id**, skal du føje kolonnen til gitteret og derefter opdatere siden.</span><span class="sxs-lookup"><span data-stu-id="da4da-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="da4da-192">Hvis du vil ændre den arbejdspulje, der er knyttet til arbejds-id'et, skal du vælge **Skift arbejdspulje-id** under fanen **Arbejde** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="da4da-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="da4da-193">Gå til dialogboksen **Skift arbejdspulje**, og vælg **Callcenter** i feltet **Arbejdspulje-id** i oversigtspanelet *Parametre*.</span><span class="sxs-lookup"><span data-stu-id="da4da-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="da4da-194">Vælg **OK** for at anvende ændringen.</span><span class="sxs-lookup"><span data-stu-id="da4da-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="da4da-195">Bemærk, at værdien i feltet **Arbejdspulje-id** er nu ændret til *Callcenter*.</span><span class="sxs-lookup"><span data-stu-id="da4da-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da4da-196">Når dialogboksen **Skift arbejdspulje** vises, kan feltet **Arbejdspulje-id** være tomt som standard.</span><span class="sxs-lookup"><span data-stu-id="da4da-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="da4da-197">Hvis feltet er tomt, når du vælger **OK** for at anvende ændringer, skal du fjerne arbejdspuljen helt fra arbejdet.</span><span class="sxs-lookup"><span data-stu-id="da4da-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="da4da-198">Ud over at skifte arbejdspulje kan du bruge denne procedure til at føje en arbejdsgruppe til en arbejdsgang, der ikke har en, eller til at fjerne en arbejdspulje fra et arbejdselement, der har en.</span><span class="sxs-lookup"><span data-stu-id="da4da-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]