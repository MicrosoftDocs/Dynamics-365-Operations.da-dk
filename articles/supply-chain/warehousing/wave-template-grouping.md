---
title: Bølgeskabelongruppering
description: Gruppering af bølgeskabeloner gør, at systemet kan bruge opsætninger af bøgeskabeloner til at bestemme, baseret på kriterier, du definerer, hvordan den skal opdele frigivne linjer og tildele dem til nye eller eksisterende bølger. Denne funktion kan være nyttig i lagre, hvor bølger oprettes på basis af bestemte kriterier, men hvor lederne foretrækker at oprette bølger automatisk i stedet for manuelt.
author: Mirzaab
manager: tfehr
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4dd188cbd17cfed372283ecb3389633b0c0021eb
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530460"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="602a2-104">Bølgeskabelongruppering</span><span class="sxs-lookup"><span data-stu-id="602a2-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="602a2-105">Gruppering af bølgeskabeloner gør, at systemet kan bruge opsætninger af [bøgeskabeloner](tasks/configure-wave-processing.md) til at bestemme, baseret på kriterier, du definerer, hvordan den skal opdele frigivne linjer og tildele dem til nye eller eksisterende bølger.</span><span class="sxs-lookup"><span data-stu-id="602a2-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="602a2-106">Denne funktion kan være nyttig i lagre, hvor bølger oprettes på basis af bestemte kriterier, men hvor lederne foretrækker at oprette bølger automatisk i stedet for manuelt.</span><span class="sxs-lookup"><span data-stu-id="602a2-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="602a2-107">Det gør det muligt for systemet at føje hver nyligt frigivet forsendelse til den første bølge, der findes, og som har tilsvarende værdier i grupperingsfeltet.</span><span class="sxs-lookup"><span data-stu-id="602a2-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="602a2-108">Hvis der ikke findes et match, opretter systemet en ny bølge til den nye forsendelse.</span><span class="sxs-lookup"><span data-stu-id="602a2-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="602a2-109">Gruppering af bølgeskabeloner understøttes ikke for arbejdstyperne *valg af råmateriale til produktion* eller *kanban-plukning*.</span><span class="sxs-lookup"><span data-stu-id="602a2-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="602a2-110">Det skyldes, at bølgegruppering er baseret på forsendelser, og at disse arbejdstyper ikke bruger forsendelser.</span><span class="sxs-lookup"><span data-stu-id="602a2-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="602a2-111">Slå funktionen til gruppering af bølgeskabeloner til</span><span class="sxs-lookup"><span data-stu-id="602a2-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="602a2-112">Før du kan bruge funktionen *Gruppering af bølgeskabeloner*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="602a2-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="602a2-113">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="602a2-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="602a2-114">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="602a2-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="602a2-115">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="602a2-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="602a2-116">**Funktionsnavn:** *Gruppering af bølgeskabeloner*</span><span class="sxs-lookup"><span data-stu-id="602a2-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="602a2-117">Angiv en bølgeskabelon til at bruge gruppering af bølgeskabeloner</span><span class="sxs-lookup"><span data-stu-id="602a2-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="602a2-118">Hvis du vil gøre gruppering af bølgeskabeloner tilgængelig, skal du følge disse trin til at konfigurere din [bølgeskabelon](tasks/configure-wave-processing.md).</span><span class="sxs-lookup"><span data-stu-id="602a2-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="602a2-119">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="602a2-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="602a2-120">Vælg den bølgeskabelon, der skal konfigureres, i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="602a2-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="602a2-121">Hvis du forbedrer at arbejde via scenariet senere i dette emne ved hjælp af demodata, skal du vælge **62 Standard for forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="602a2-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="602a2-122">Vælg **Rediger** for at sætte siden i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="602a2-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="602a2-123">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="602a2-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="602a2-124">**Automatiser vølgeoprettelse:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="602a2-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="602a2-125">**Tildel til åbne bølger:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="602a2-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="602a2-126">**Udfør behandling af bølgen ved frigivelse til lagerstedet:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="602a2-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="602a2-127">I handlingsruden skal du vælge **Rediger forespørgsel** for at åbne dialogboksen med forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="602a2-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="602a2-128">Gennemgå sorteringskriterierne under fanen sortering i dialogboksen **Forespørgsel**, og sørg for, at der findes en regel, der omfatter det felt, du vil bruge til at gruppere dine bølger.</span><span class="sxs-lookup"><span data-stu-id="602a2-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="602a2-129">Hvis du forbereder at arbejde gennem scenariet med demonstrationsdata, skal du tilføje en række, der har følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="602a2-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="602a2-130">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="602a2-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="602a2-131">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="602a2-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="602a2-132">**Felt:** *Fragttjeneste*</span><span class="sxs-lookup"><span data-stu-id="602a2-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="602a2-133">Når du har valgt denne værdi, får du muligvis vist følgende meddelelse: "Feltet Fragttjeneste er ikke et indeksfelt.</span><span class="sxs-lookup"><span data-stu-id="602a2-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="602a2-134">Vil du tilføje sortering på dette?"</span><span class="sxs-lookup"><span data-stu-id="602a2-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="602a2-135">Vælg **Ja** for at tilføje sortering.</span><span class="sxs-lookup"><span data-stu-id="602a2-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="602a2-136">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="602a2-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="602a2-137">Vælg **OK** for at gemme dine ændringer og lukke forespørgselsdialogboksen.</span><span class="sxs-lookup"><span data-stu-id="602a2-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="602a2-138">Gå til handlingsruden, og vælg **Gruppering af bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="602a2-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="602a2-139">På siden **Gruppering af bølgeskabeloner** skal du markere afkrydsningsfeltet **Gruppér efter** efter for hver række, du vil bruge til at gruppere ordrelinjerne i bølger efter behov.</span><span class="sxs-lookup"><span data-stu-id="602a2-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="602a2-140">Hvis du forbereder at arbejde dig gennem scenariet med demonstrationsdata, skal du markere afkrydsningsfeltet **Gruppér efter** for rækken *Fragttjeneste*.</span><span class="sxs-lookup"><span data-stu-id="602a2-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="602a2-141">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="602a2-141">Select **Save**.</span></span>
1. <span data-ttu-id="602a2-142">Luk siden **Gruppering af bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="602a2-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="602a2-143">Vælg **Gem** for at gemme skabelonen.</span><span class="sxs-lookup"><span data-stu-id="602a2-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="602a2-144">Scenario</span><span class="sxs-lookup"><span data-stu-id="602a2-144">Scenario</span></span>

<span data-ttu-id="602a2-145">Dette afsnit indeholder et script, som du kan arbejde med for at finde ud af, hvad funktionen gør, og hvordan du arbejder med den.</span><span class="sxs-lookup"><span data-stu-id="602a2-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="602a2-146">Gøre eksempeldata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="602a2-146">Make sample data available</span></span>

<span data-ttu-id="602a2-147">Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="602a2-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="602a2-148">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="602a2-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="602a2-149">Du kan også bruge dette scenarie som vejledning til brug af funktionen, når du arbejder i et produktionssystem.</span><span class="sxs-lookup"><span data-stu-id="602a2-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="602a2-150">Du skal dog i det tilfælde erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.</span><span class="sxs-lookup"><span data-stu-id="602a2-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="602a2-151">Scenarie: gruppering af bølgeskabeloner</span><span class="sxs-lookup"><span data-stu-id="602a2-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="602a2-152">I dette scenarie vises, hvordan du kan bruge gruppering af bølgeskabeloner til automatisk at oprette flere bølger baseret på grupperingskriterier, der er defineret i en bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="602a2-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="602a2-153">I dette scenarie er bølgeskabelonen konfigureret i systemet, så der oprettes en bølge pr. fragttjeneste.</span><span class="sxs-lookup"><span data-stu-id="602a2-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="602a2-154">Før du går i gang, skal du forberede din bølgeskabelon som beskrevet i afsnittet [Angiv en bølgeskabelon til at bruge gruppering af bølgeskabeloner](#set-up-template) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="602a2-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="602a2-155">Hvis du vil arbejde med demonstrationsdata i dette scenarie, skal du sørge for at bruge de demonstrationsdatasværdier, der er foreslået i den pågældende procedure.</span><span class="sxs-lookup"><span data-stu-id="602a2-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="602a2-156">Denne indstilling vil gruppere dine bølger efter den fragtmand, der er angivet for hver salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="602a2-157">Opret salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="602a2-157">Create sales order 1</span></span>

1. <span data-ttu-id="602a2-158">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="602a2-159">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="602a2-160">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="602a2-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="602a2-161">Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-004*.</span><span class="sxs-lookup"><span data-stu-id="602a2-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="602a2-162">I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.</span><span class="sxs-lookup"><span data-stu-id="602a2-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="602a2-163">Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="602a2-164">Den nye salgsordre åbnes i visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="602a2-165">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="602a2-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="602a2-166">Skift til **overskriftsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="602a2-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="602a2-167">Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="602a2-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="602a2-168">**Fragtmand:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="602a2-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="602a2-169">**Fragttjeneste:** *Air*</span><span class="sxs-lookup"><span data-stu-id="602a2-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="602a2-170">Skift tilbage til visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="602a2-171">Vælg **Tilføj linje** i sektionen **Salgsordrelinjer** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="602a2-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="602a2-172">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="602a2-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="602a2-173">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="602a2-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="602a2-174">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="602a2-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="602a2-175">Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="602a2-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="602a2-176">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="602a2-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="602a2-177">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="602a2-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="602a2-178">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="602a2-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="602a2-179">Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="602a2-180">Noter dig bølge-id-nummeret og forsendelses-id-numrene.</span><span class="sxs-lookup"><span data-stu-id="602a2-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="602a2-181">Få vist den bølge, der er oprettet fra salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="602a2-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="602a2-182">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="602a2-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="602a2-183">Vælg det bølge-id, der blev oprettet fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="602a2-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="602a2-184">Vælg linket for bølge-id'et for at åbne siden med bølgedetaljer.</span><span class="sxs-lookup"><span data-stu-id="602a2-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="602a2-185">Bemærk, at forsendelsen er føjet til oversigtspanelet **Bølgelinjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="602a2-186">Opret salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="602a2-186">Create sales order 2</span></span>

1. <span data-ttu-id="602a2-187">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="602a2-188">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="602a2-189">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="602a2-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="602a2-190">Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-005*.</span><span class="sxs-lookup"><span data-stu-id="602a2-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="602a2-191">I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.</span><span class="sxs-lookup"><span data-stu-id="602a2-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="602a2-192">Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="602a2-193">Den nye salgsordre åbnes i visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="602a2-194">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="602a2-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="602a2-195">Skift til **overskriftsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="602a2-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="602a2-196">Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="602a2-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="602a2-197">**Fragtmand:** *Flower moving*</span><span class="sxs-lookup"><span data-stu-id="602a2-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="602a2-198">**Fragttjeneste:** *Std*</span><span class="sxs-lookup"><span data-stu-id="602a2-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="602a2-199">Skift tilbage til visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="602a2-200">Vælg **Tilføj linje** i sektionen **Salgsordrelinjer** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="602a2-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="602a2-201">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="602a2-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="602a2-202">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="602a2-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="602a2-203">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="602a2-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="602a2-204">Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="602a2-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="602a2-205">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="602a2-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="602a2-206">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="602a2-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="602a2-207">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="602a2-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="602a2-208">Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="602a2-209">Noter dig bølge-id-nummeret og forsendelses-id-numrene.</span><span class="sxs-lookup"><span data-stu-id="602a2-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="602a2-210">Bemærk, at bølge-id'et ikke er det samme som bølge-id'et for den første salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="602a2-211">Få vist den bølge, der er oprettet fra salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="602a2-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="602a2-212">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="602a2-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="602a2-213">Vælg det bølge-id, der blev oprettet fra den anden salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="602a2-214">Vælg linket for bølge-id'et for at åbne siden med bølgedetaljer.</span><span class="sxs-lookup"><span data-stu-id="602a2-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="602a2-215">Bemærk, at forsendelsen er føjet til oversigtspanelet **Bølgelinjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="602a2-216">Der blev oprettet en ny bølge til denne forsendelse, fordi den bruger en anden fragttjeneste end den første salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="602a2-217">Opret salgsordre 3</span><span class="sxs-lookup"><span data-stu-id="602a2-217">Create sales order 3</span></span>

1. <span data-ttu-id="602a2-218">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="602a2-219">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="602a2-220">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="602a2-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="602a2-221">Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til *US-006*.</span><span class="sxs-lookup"><span data-stu-id="602a2-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="602a2-222">I oversigtspanelet **Generelt** skal du indstille **Lagersted** til *62*.</span><span class="sxs-lookup"><span data-stu-id="602a2-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="602a2-223">Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen **Opret salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="602a2-224">Den nye salgsordre åbnes i visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="602a2-225">Notér dig salgsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="602a2-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="602a2-226">Skift til **overskriftsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="602a2-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="602a2-227">Gå til oversigtspanelet **Levering** i sektionen **Transport**, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="602a2-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="602a2-228">**Fragtmand:** *Air Cargo*</span><span class="sxs-lookup"><span data-stu-id="602a2-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="602a2-229">**Fragttjeneste:** *Air*</span><span class="sxs-lookup"><span data-stu-id="602a2-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="602a2-230">Skift tilbage til visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="602a2-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="602a2-231">Vælg **Tilføj linje** i sektionen **Salgsordrelinjer** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="602a2-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="602a2-232">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="602a2-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="602a2-233">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="602a2-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="602a2-234">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="602a2-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="602a2-235">Vælg den nye ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="602a2-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="602a2-236">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="602a2-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="602a2-237">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="602a2-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="602a2-238">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="602a2-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="602a2-239">Du modtager en informativ meddelelse, der viser forsendelsen og bølgen for denne ordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="602a2-240">Noter dig bølge-id-nummeret og forsendelses-id-numrene.</span><span class="sxs-lookup"><span data-stu-id="602a2-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="602a2-241">Forsendelsen er tildelt den eksisterende bølge fra den første salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="602a2-242">Få vist bølgen for salgsordre 1 og 3</span><span class="sxs-lookup"><span data-stu-id="602a2-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="602a2-243">Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.</span><span class="sxs-lookup"><span data-stu-id="602a2-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="602a2-244">Vælg det bølge-id, der blev oprettet fra den tredje salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="602a2-245">Vælg linket for bølge-id'et for at åbne siden med bølgedetaljer.</span><span class="sxs-lookup"><span data-stu-id="602a2-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="602a2-246">Bemærk, at forsendelsen er føjet til oversigtspanelet **Bølgelinjer** sammen med forsendelsen for den første salgsordre.</span><span class="sxs-lookup"><span data-stu-id="602a2-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>