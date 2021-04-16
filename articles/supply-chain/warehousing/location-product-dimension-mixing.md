---
title: Blanding af produktdimension for lokation
description: Dette emne indeholder oplysninger om blanding af produktdimensioner på lokation. Denne lokationsprofilfunktion hjælper med at forbedre lokationsstyringen, når der bruges produktvarianter eller produkter med dimensioner, f.eks. i modebranchen. Den giver dig mulighed for at bestemme, om konfigurationer, farver, stilarter og størrelser kan blandes for en bestemt lokationsprofil, eller om kun en af disse dimensioner eller en kombination af dem kan placeres på samme lokation.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 28f59052a74b6d8b263c7a8a8b6061f2c4b34c89
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831284"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="06b3f-105">Blanding af produktdimension for lokation</span><span class="sxs-lookup"><span data-stu-id="06b3f-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06b3f-106">Blanding af produktdimensioner på lokation er en lokationsprofilfunktion, der forbedrer lokationsstyringen, når der bruges produktvarianter eller produkter med dimensioner, f.eks. i modebranchen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="06b3f-107">Den giver dig mulighed for at bestemme, om konfigurationer, farver, stilarter og størrelser kan blandes for en bestemt lokationsprofil, eller om kun en af disse dimensioner eller en kombination af dem kan placeres på samme lokation.</span><span class="sxs-lookup"><span data-stu-id="06b3f-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="06b3f-108">Slå funktionen til blanding af produktdimensioner på lokation til</span><span class="sxs-lookup"><span data-stu-id="06b3f-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="06b3f-109">Før du kan bruge funktionen til blanding af produktdimensioner for sted, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="06b3f-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="06b3f-110">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="06b3f-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="06b3f-111">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="06b3f-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="06b3f-112">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="06b3f-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="06b3f-113">**Funktionsnavn:** *Blanding af produktdimensioner på lokation*</span><span class="sxs-lookup"><span data-stu-id="06b3f-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="06b3f-114">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="06b3f-114">Setup</span></span>

<span data-ttu-id="06b3f-115">Hver lokalitet på lagerstedet skal have tilknyttet en lokalitetsprofil, der beskriver egenskaberne for lokaliteten.</span><span class="sxs-lookup"><span data-stu-id="06b3f-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="06b3f-116">Derfor vil alle lokationer, der bruger samme lokationsprofil, kunne tillade kombinationen af produktdimensioner, efter at den er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="06b3f-117">Konfigurer lokationsprofiler, der tillader blanding af produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="06b3f-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="06b3f-118">Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="06b3f-119">Vælg **MASSE** på listen over lokationsprofiler.</span><span class="sxs-lookup"><span data-stu-id="06b3f-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="06b3f-120">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06b3f-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="06b3f-121">I oversigtspanelet **Generelt** skal du angive indstillingen **Aktivér specifik blanding af produktdimensioner på lokation** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06b3f-122">Du kan kun angive denne indstilling til *Ja*, hvis indstillingen **Tillad blandede varer** er angivet til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="06b3f-123">I oversigtspanelet **Tilladt blanding af produktdimensioner** skal du angive **Størrelse** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="06b3f-124">I det scenarie, der beskrives i dette emne, kan der kun foretages blanding for produkter med forskellige **størrelsesdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="06b3f-125">Der findes dog også andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="06b3f-125">However, other options are also available.</span></span>
1. <span data-ttu-id="06b3f-126">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="06b3f-127">Opret en ny produktmaster og produktvarianter</span><span class="sxs-lookup"><span data-stu-id="06b3f-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="06b3f-128">Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="06b3f-129">Vælg **Ny** i handlingsruden for at oprette en produktmaster.</span><span class="sxs-lookup"><span data-stu-id="06b3f-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="06b3f-130">Angiv følgende værdier i dialogboksen **Nyt produkt**:</span><span class="sxs-lookup"><span data-stu-id="06b3f-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="06b3f-131">**Produkttype:** *Vare*</span><span class="sxs-lookup"><span data-stu-id="06b3f-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="06b3f-132">**Produktundertype:** *Produktmaster*</span><span class="sxs-lookup"><span data-stu-id="06b3f-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="06b3f-133">**Produktnummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="06b3f-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="06b3f-134">**Produktnavn:** *B0001-størrelse*</span><span class="sxs-lookup"><span data-stu-id="06b3f-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="06b3f-135">**Produktdimensionsgruppe:** *Størrelse*</span><span class="sxs-lookup"><span data-stu-id="06b3f-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="06b3f-136">**Konfigurationsteknologi:** *Foruddefineret variant*</span><span class="sxs-lookup"><span data-stu-id="06b3f-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="06b3f-137">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-137">Select **OK**.</span></span>
1. <span data-ttu-id="06b3f-138">Gå til siden **Produktdetaljer** i oversigtspanelet **Generelt**, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="06b3f-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="06b3f-139">**Generér varianter automatisk:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="06b3f-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="06b3f-140">**Størrelsesgruppe:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="06b3f-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="06b3f-141">Hvis du vil have vist de foruddefinerede varianter, skal du vælge **Produktvarianter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06b3f-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="06b3f-142">Siden **Produktvarianter** vises og angiver en liste over varianter fra konfigurationen af størrelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="06b3f-143">Frigive produkter til USMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="06b3f-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="06b3f-144">Vælg **Frigiv produkter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06b3f-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="06b3f-145">På siden **Vælg produkter, der skal frigives**, skal du bekræfte, at produktnummeret *B0001* er på listen og derefter vælge **Næste**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="06b3f-146">Vælg **Næste** for at bekræfte de produktvarianter, der skal frigives.</span><span class="sxs-lookup"><span data-stu-id="06b3f-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="06b3f-147">På siden **Vælg firmaer, der skal frigives til**, skal du vælge *USMF* og derefter vælge **Næste** for at bekræfte valget.</span><span class="sxs-lookup"><span data-stu-id="06b3f-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="06b3f-148">Klik på **Bekræft valg** skal du vælge **Udfør** for at fuldføre frigivelsen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="06b3f-149">Du får vist meddelelsen "Operationen er udført".</span><span class="sxs-lookup"><span data-stu-id="06b3f-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="06b3f-150">Opdatere et frigivet produkt i USMF-firmaet</span><span class="sxs-lookup"><span data-stu-id="06b3f-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="06b3f-151">Kontroller, at du er logget på **USMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="06b3f-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="06b3f-152">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter** for at færdiggøre oprettelse af det frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="06b3f-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="06b3f-153">Find og vælg varenummer *B0001* for at åbne siden **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="06b3f-154">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06b3f-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="06b3f-155">I oversigtspanelet **Generelt** skal du kontrollere, at feltet **Varemodelgruppe** er angivet til *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="06b3f-156">Gå til handlingsruden, og vælg **Dimensionsgrupper** i gruppen **Opsætning** under fanen **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="06b3f-157">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="06b3f-157">Set the following values:</span></span>

    - <span data-ttu-id="06b3f-158">**Lagringsdimensionsgruppe:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="06b3f-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="06b3f-159">**Sporingsdimensionsgruppe:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="06b3f-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="06b3f-160">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-160">Select **OK**.</span></span>
1. <span data-ttu-id="06b3f-161">Gå til handlingsruden, og vælg **Reservationshierarki** i gruppen **Opsætning** under fanen **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="06b3f-162">Angiv feltet **Reservationshierarki** til *Standard*, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="06b3f-163">I oversigtspanelet **Generelt** skal du i sektionen **Administration** bemærke, at dine valg er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="06b3f-164">Angiv **10** i feltet **Pris** i oversigtspanelet *Køb*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="06b3f-165">På oversigtspanelet **Administrer omkostninger** skal du i feltet **Varegruppe** angive *Lyd*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="06b3f-166">Angiv **10** i feltet **Pris** i oversigtspanelet *Køb*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="06b3f-167">I oversigtspanelet **Lager** skal du i feltet **Enhedsseriegruppe-id** angive *ea*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="06b3f-168">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="06b3f-169">Oprette en lokalitetsvejledning</span><span class="sxs-lookup"><span data-stu-id="06b3f-169">Create a location directive</span></span>

1. <span data-ttu-id="06b3f-170">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="06b3f-171">I den venstre rude skal du i feltet **Arbejdsordretype** vælge *Indkøbsordrer*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="06b3f-172">Vælg den lokationsvejledning, der hedder *24 PO Direct*, på listen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="06b3f-173">Gå til oversigtspanelet **Handlinger i lokationsvejledning** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="06b3f-174">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="06b3f-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="06b3f-175">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="06b3f-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="06b3f-176">Den nye linje skal være foran den tidligere eksisterende linje.</span><span class="sxs-lookup"><span data-stu-id="06b3f-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="06b3f-177">Hvis du vil foretage ændringen, skal du bruge knapperne **Flyt op** og **Flyt ned** på værktøjslinjen eller ændre **Løbenummerværdi** til *2*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="06b3f-178">**Navn:** *Læg på lager for MASSE-lokationsprofil*</span><span class="sxs-lookup"><span data-stu-id="06b3f-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="06b3f-179">**Anvendelse af fast lokation:** *Faste og ikke-faste lokationer*</span><span class="sxs-lookup"><span data-stu-id="06b3f-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="06b3f-180">**Tillad negativ lagerbeholdning:** *Fjern markeringen i dette afkrydsningsfelt (= Nej)*</span><span class="sxs-lookup"><span data-stu-id="06b3f-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="06b3f-181">**Batch aktiveret:** *Fjern markeringen i dette afkrydsningsfelt (= Nej)*</span><span class="sxs-lookup"><span data-stu-id="06b3f-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="06b3f-182">**Strategi:** *Ingen*</span><span class="sxs-lookup"><span data-stu-id="06b3f-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="06b3f-183">Mens den nye linje stadig er markeret, skal du vælge **Rediger forespørgsel** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="06b3f-184">Vælg forespørgselsdialogboksen skal du under fanen **Interval** vælge **Tilføj** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="06b3f-185">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="06b3f-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="06b3f-186">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="06b3f-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="06b3f-187">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="06b3f-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="06b3f-188">**Felt:** *Lokationsprofil-id*</span><span class="sxs-lookup"><span data-stu-id="06b3f-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="06b3f-189">**Kriterier:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="06b3f-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="06b3f-190">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-190">Select **OK**.</span></span>
1. <span data-ttu-id="06b3f-191">Vælg **Gem** i handlingsruden på siden **Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="06b3f-192">Hvis du i feltet **Strategi** i oversigtspanelet **Handlinger i lokationsvejledning** bruger lokationsstrategien *Konsolider*, vil opsætningen af oversigtspanelet **Tilladt blanding af produktdimensioner** på **Lokationsprofiler** blive tilsidesat, og varer lægges på lager på samme lokation, også selvom denne virkemåde ikke er tilladt af opsætningen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="06b3f-193">Oprette et menupunkt på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="06b3f-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="06b3f-194">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="06b3f-195">Vælg **Ny** i handlingsruden for at oprette et menupunkt, der skal bruges til sortering.</span><span class="sxs-lookup"><span data-stu-id="06b3f-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="06b3f-196">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="06b3f-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="06b3f-197">**Navn på menupunkt:** *Modtagelse af indkøbsordrelinje*</span><span class="sxs-lookup"><span data-stu-id="06b3f-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="06b3f-198">**Titel:** *Modtagelse af indkøbsordrelinje*</span><span class="sxs-lookup"><span data-stu-id="06b3f-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="06b3f-199">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="06b3f-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="06b3f-200">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="06b3f-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="06b3f-201">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="06b3f-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="06b3f-202">**Arbejdsoprettelsesproces:** *Modtagelse og læg på lager for ordrelinje*</span><span class="sxs-lookup"><span data-stu-id="06b3f-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="06b3f-203">**Generer nummerplade:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="06b3f-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="06b3f-204">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="06b3f-205">Konfigurer mobilenhedsmenuen</span><span class="sxs-lookup"><span data-stu-id="06b3f-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="06b3f-206">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="06b3f-207">Vælg **Indgående** på listen over menuer.</span><span class="sxs-lookup"><span data-stu-id="06b3f-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="06b3f-208">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06b3f-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="06b3f-209">På listen **Tilgængelig menuer og menupunkter** skal du finde og vælge menupunktet **Modtagelse af indkøbsordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="06b3f-210">Vælg den højre pileknap for at flytte menupunktet **Modtagelse af indkøbsordrelinje** til listen **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="06b3f-211">På denne måde føjer du det nye menupunkt til den valgte menu.</span><span class="sxs-lookup"><span data-stu-id="06b3f-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="06b3f-212">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="06b3f-213">Scenario</span><span class="sxs-lookup"><span data-stu-id="06b3f-213">Scenario</span></span>

<span data-ttu-id="06b3f-214">Dette demonstrationsscenarie viser, hvordan to forskellige produktvarianter kan anbringes på samme lokation, når lokationsprofilen ikke tillader blandede varer, men funktionen *Blanding af produktdimensioner på lokation* er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="06b3f-215">I dette tilfælde skal du bruge varianten **Størrelse** som kriterium.</span><span class="sxs-lookup"><span data-stu-id="06b3f-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="06b3f-216">Før du går i gang, skal du sikre dig, at der er tomme lokationer på lagerstedet *24*, der bruger *MASSE*-lokationsprofilen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="06b3f-217">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="06b3f-217">Create a purchase order</span></span>

<span data-ttu-id="06b3f-218">Du skal oprette en indkøbsordre, der indeholder tre linjer: to linjer for samme produktnummer, men med forskellige varianter af **Størrelse**, og en tredje linje for et andet produkt, der ikke har nogen varianter.</span><span class="sxs-lookup"><span data-stu-id="06b3f-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="06b3f-219">Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="06b3f-220">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="06b3f-221">Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:</span><span class="sxs-lookup"><span data-stu-id="06b3f-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="06b3f-222">**Kreditorkonto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="06b3f-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="06b3f-223">**Lagersted:** *24*</span><span class="sxs-lookup"><span data-stu-id="06b3f-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="06b3f-224">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-224">Select **OK**.</span></span>
1. <span data-ttu-id="06b3f-225">Indkøbsordren oprettes, og der tilføjes en ny linje i oversigtspanelet **Indkøbsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="06b3f-226">Notér dig købsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="06b3f-227">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="06b3f-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="06b3f-228">**Varenummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="06b3f-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="06b3f-229">**Størrelse** *L*</span><span class="sxs-lookup"><span data-stu-id="06b3f-229">**Size** *L*</span></span>
    - <span data-ttu-id="06b3f-230">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="06b3f-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="06b3f-231">Vælg **Tilføj linje** over gitteret for at tilføje en anden indkøbsordrelinje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="06b3f-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="06b3f-232">**Varenummer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="06b3f-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="06b3f-233">**Størrelse** *XL*</span><span class="sxs-lookup"><span data-stu-id="06b3f-233">**Size** *XL*</span></span>
    - <span data-ttu-id="06b3f-234">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="06b3f-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="06b3f-235">Vælg **Tilføj linje** for at tilføje en tredje indkøbsordrelinje, og angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="06b3f-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="06b3f-236">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="06b3f-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="06b3f-237">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="06b3f-237">**Quantity:** *1*</span></span>

<span data-ttu-id="06b3f-238">1. Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="06b3f-239">Modtage indkøbsordrelinjer i mobilappen Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="06b3f-239">Receive purchase order lines in the Warehouse Management mobile app</span></span>

1. <span data-ttu-id="06b3f-240">Log på mobilappen Lokationsstyring som en bruger, der er aktiveret til lagersted *24*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-240">Sign in to the Warehouse Management mobile app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="06b3f-241">Vælg menuen **Indgående**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="06b3f-242">Vælg **Modtagelse af indkøbsordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="06b3f-243">Vælg feltet **IO-num**, angiv derefter indkøbsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="06b3f-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="06b3f-244">Bekræft angivelsen ved at vælge knappen Bekræft (✔) nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="06b3f-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="06b3f-245">Angiv linjenummeret fra den indkøbsordre, der modtages.</span><span class="sxs-lookup"><span data-stu-id="06b3f-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="06b3f-246">Marker feltet **LINJENUM**, og brug derefter det numeriske tastatur til at angive *1*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="06b3f-247">Bekræft indtastningen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-247">Confirm your entry.</span></span>
1. <span data-ttu-id="06b3f-248">Angiv det antal, der skal modtages.</span><span class="sxs-lookup"><span data-stu-id="06b3f-248">Enter the quantity to receive.</span></span> <span data-ttu-id="06b3f-249">Vælg knappen plustegn (**+**) to gange for at øge værdien i feltet **Antal** til *2*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="06b3f-250">Registrer din indtastning ved at vælge knappen (✔) nederst på siden, og bekræft derefter angivelsen ved at vælge knappen (✔) igen.</span><span class="sxs-lookup"><span data-stu-id="06b3f-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="06b3f-251">Få vist oplysningerne på siden **Indkøbsordrer: Læg på lager**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="06b3f-252">Denne side viser det arbejde, der er oprettet for læg på lager-handlingen (arbejde 1).</span><span class="sxs-lookup"><span data-stu-id="06b3f-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="06b3f-253">Den lokation, hvor den modtagne vare skal lægges på lager, nummerpladen, varen, størrelsen og antallet på den linje i opgaven **Modtagelse indkøbsordrelinje**, som modtager den opgave, du netop har udført, vises.</span><span class="sxs-lookup"><span data-stu-id="06b3f-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="06b3f-254">Bekræft læg på lager-arbejdet.</span><span class="sxs-lookup"><span data-stu-id="06b3f-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="06b3f-255">Gentag trin 4 til 11 for indkøbsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="06b3f-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="06b3f-256">I trin 8 skal du dog angive et antal på *1*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="06b3f-257">Der oprettes et nyt læg på lager-arbejde (arbejde 2) for samme lokation som arbejde 1.</span><span class="sxs-lookup"><span data-stu-id="06b3f-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="06b3f-258">Gentag trin 4 til 11 igen for indkøbsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="06b3f-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="06b3f-259">I trin 8 skal du angive et resterende antal på *1*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="06b3f-260">Der oprettes et nyt læg på lager-arbejde (arbejde 3) for samme lokation som arbejde 1 og 2.</span><span class="sxs-lookup"><span data-stu-id="06b3f-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="06b3f-261">Dette virkemåde opstår, fordi lokationsvejledningen *Konsolider* bruges, og oversigtspanelet **Tilladt blanding af produktdimensioner** i *Masse*-opsætningen af **Lokationsprofiler** tillader, at varianten **Størrelse** kan blandes på en lokation.</span><span class="sxs-lookup"><span data-stu-id="06b3f-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="06b3f-262">Gentag trin 4 til 11 for indkøbsordrelinje 3.</span><span class="sxs-lookup"><span data-stu-id="06b3f-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="06b3f-263">I trin 8 skal du angive et antal på *1* for varenummer *A0001*.</span><span class="sxs-lookup"><span data-stu-id="06b3f-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="06b3f-264">Der oprettes et nyt læg på lager-arbejde (arbejde 4) for en anden lokation end den lokation, der bruges til indkøbsordrelinje nr. 1 og 2.</span><span class="sxs-lookup"><span data-stu-id="06b3f-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="06b3f-265">Denne virkemåde opstår, fordi lokationsprofilen ikke tillader blandede produkter, men den giver mulighed for blandede dimensioner af samme produktmaster.</span><span class="sxs-lookup"><span data-stu-id="06b3f-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="06b3f-266">Vælg menuknappen øverst på siden (kaldes også hamburger eller hamburgerknappen), og vælg derefter **Annuller** for at afslutte **Modtagelse af indkøbsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="06b3f-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="06b3f-267">Du kan gentage dette scenarie, men denne gang skal du angive **Størrelse** - *Nej* under oversigtspanelet **Tillad blanding af produktdimensioner** på *Masse* **Lokationsprofiler**, så ingen af produktdimensionerne kan blandes.</span><span class="sxs-lookup"><span data-stu-id="06b3f-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="06b3f-268">Hvis du i dette tilfælde modtager indkøbsordren, vil de enkelte produktvarianter blive lagt på lager på en ny lokation.</span><span class="sxs-lookup"><span data-stu-id="06b3f-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]