---
title: Angive forskellige dimensioner for pakning og lagring
description: I dette emne vises, hvordan du kan angive, hvilken proces (pakning, lagring eller indlejret emballage) hver enkelt dimension bruges til.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078246"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="0f8d0-103">Angive forskellige dimensioner for pakning og lagring</span><span class="sxs-lookup"><span data-stu-id="0f8d0-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f8d0-104">Nogle varer er pakket eller lagret på en sådan måde, at du kan få brug for at spore fysiske dimensioner forskelligt for hver af flere forskellige processer.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="0f8d0-105">Funktionen *Emballageproduktdimensioner* gør det muligt at konfigurere en eller flere typer dimensioner for hvert produkt.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="0f8d0-106">Hver dimensionstype indeholder et sæt fysiske målinger (vægt, bredde, dybde og højde) og fastlægger den proces, hvor disse fysiske målingsværdier gælder.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="0f8d0-107">Når denne funktion er aktiveret, understøtter systemet følgende dimensionstyper:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="0f8d0-108">*Lagring* – Lagringsdimensioner bruges sammen med lokationsmængder til at bestemme, hvor mange af hver vare der kan opbevares på forskellige lagersteder.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="0f8d0-109">*Emballage* – Pakkedimensioner bruges under containerisering og den manuelle pakningsproces til at bestemme, hvor mange af hver vare der kan være i forskellige containertyper.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="0f8d0-110">*Indlejret emballage* – Indlejrede emballagedimensioner bruges, når pakkeprocessen indeholder flere niveauer.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="0f8d0-111">*Lagringsdimensioner* understøttes også, selvom funktionen *Emballageproduktdimensioner* ikke er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="0f8d0-112">Du kan konfigurere disse ved hjælp af siden **Fysisk dimension** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="0f8d0-113">Disse dimensioner bruges af alle processer, hvor dimensionerne for pakning og indlejret emballage ikke er angivet.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="0f8d0-114">Dimensioner for *Emballage* og *indlejret emballage* konfigureres ved hjælp af siden **Fysiske produktdimensioner**, som tilføjes, når du aktiverer funktionen *Emballageproduktdimensioner*.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="0f8d0-115">Dette emne indeholder et eksempel på, hvordan denne funktion bruges.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="0f8d0-116">Aktivere funktionen Emballageproduktdimensioner</span><span class="sxs-lookup"><span data-stu-id="0f8d0-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="0f8d0-117">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="0f8d0-118">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="0f8d0-119">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0f8d0-120">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0f8d0-121">**Funktionsnavn:** *Emballageproduktdimensioner*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0f8d0-122">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="0f8d0-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="0f8d0-123">Konfigurere scenariet</span><span class="sxs-lookup"><span data-stu-id="0f8d0-123">Set up the scenario</span></span>

<span data-ttu-id="0f8d0-124">Før du kan køre eksempelscenariet, skal du forberede systemet som beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="0f8d0-125">Aktivere demodata</span><span class="sxs-lookup"><span data-stu-id="0f8d0-125">Enable demo data</span></span>

<span data-ttu-id="0f8d0-126">Hvis du vil arbejde gennem dette scenarie ved hjælp af de demoposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="0f8d0-127">Derudover skal du vælge den juridiske enhed *USMF*, før du starter.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="0f8d0-128">Føje en ny fysisk dimension til et produkt</span><span class="sxs-lookup"><span data-stu-id="0f8d0-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="0f8d0-129">Tilføj en ny fysisk dimension for et produkt på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="0f8d0-130">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0f8d0-131">Vælg produktet med **varenummeret** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="0f8d0-132">I handlingsruden skal du åbne fanen **Styr lager** og vælge **Fysiske produktdimensioner** i gruppen **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="0f8d0-133">Siden **Fysiske produktdimensioner** åbnes.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="0f8d0-134">Gå til handlingsruden, og vælg **Ny** for at føje en ny dimension til gitteret med følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="0f8d0-135">**Fysisk dimensionstype** - *Emballage*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="0f8d0-136">**Fysisk enhed** - *stk.*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="0f8d0-137">**Vægt** - *4*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="0f8d0-138">**Vægtenhed** - *kg*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="0f8d0-139">**Dybde** - *3*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="0f8d0-140">**Højde** - *4*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-140">**Height** - *4*</span></span>
    - <span data-ttu-id="0f8d0-141">**Bredde** - *3*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-141">**Width** - *3*</span></span>
    - <span data-ttu-id="0f8d0-142">**Længde** - *cm*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="0f8d0-143">**Volumenenhed** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="0f8d0-144">Feltet **Volumen** beregnes automatisk ud fra indstillingerne for **Dybde**, **Højde** og **Bredde**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="0f8d0-145">Oprette en ny containertype</span><span class="sxs-lookup"><span data-stu-id="0f8d0-145">Create a new container type</span></span>

<span data-ttu-id="0f8d0-146">Gå til **Lokationsstyring \> Opsætning \> Containere \> Containertyper**, og opret en ny post med følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="0f8d0-147">**Containertypekode** - *Lav kasse*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="0f8d0-148">**Beskrivelse** - *Lav kasse*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="0f8d0-149">**Maksimal nettovægt** - *50*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="0f8d0-150">**Volumen** - *144*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-150">**Volume** - *144*</span></span>
- <span data-ttu-id="0f8d0-151">**Længde** - *6*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-151">**Length** - *6*</span></span>
- <span data-ttu-id="0f8d0-152">**Bredde** - *6*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-152">**Width** - *6*</span></span>
- <span data-ttu-id="0f8d0-153">**Højde** - *4*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="0f8d0-154">Oprette en containergruppe</span><span class="sxs-lookup"><span data-stu-id="0f8d0-154">Create a container group</span></span>

<span data-ttu-id="0f8d0-155">Gå til **Lokationsstyring \> Opsætning \> Containere \> Containergrupper**, og opret en ny post med følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="0f8d0-156">**Containergruppe-id** - *Lav kasse*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="0f8d0-157">**Beskrivelse** - *Lav kasse*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="0f8d0-158">Føj en ny linje til sektionen **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="0f8d0-159">Angiv **Containertype** til *Lav kasse*.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="0f8d0-160">Konfigurere en containerbuildskabelon</span><span class="sxs-lookup"><span data-stu-id="0f8d0-160">Set up a container build template</span></span>

<span data-ttu-id="0f8d0-161">Gå til **Lokationsstyring \> Konfiguration \> Containere \> Skabeloner til containerbygning**, og vælg **Kasser**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="0f8d0-162">Skift **Containergruppe-id** til *Lav kasse*.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="0f8d0-163">Køre scenariet</span><span class="sxs-lookup"><span data-stu-id="0f8d0-163">Run the scenario</span></span>

<span data-ttu-id="0f8d0-164">Når du har forberedt systemet som beskrevet i forrige afsnit, er du klar til at køre scenariet som beskrevet i næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="0f8d0-165">Oprette en salgsordre og oprette en forsendelse</span><span class="sxs-lookup"><span data-stu-id="0f8d0-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="0f8d0-166">I denne proces opretter du en forsendelse, der er baseret på varens *emballagedimensioner*, for hvilken højden er mindre end 3.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="0f8d0-167">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0f8d0-168">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0f8d0-169">Angiv følgende værdier i dialogboksen **Opret salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0f8d0-170">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0f8d0-171">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="0f8d0-172">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="0f8d0-173">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-173">The new sales order is opened.</span></span> <span data-ttu-id="0f8d0-174">Den skal omfatte en ny tom linje i gitteret i oversigtspanelet **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0f8d0-175">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="0f8d0-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="0f8d0-176">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="0f8d0-177">**Antal:** *5*</span><span class="sxs-lookup"><span data-stu-id="0f8d0-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="0f8d0-178">Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="0f8d0-179">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="0f8d0-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-180">Close the page.</span></span>
1. <span data-ttu-id="0f8d0-181">I handlingsruden skal du åbne fanen **Lagersted** og vælge **Frigiv til lagersted** for at oprette lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="0f8d0-182">I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted \> Forsendelsesoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="0f8d0-183">Åbn fanen **Transport** i handlingsruden, og vælg **Vis containere**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="0f8d0-184">Bekræft, at varen blev pakket containere i de to *Lav kasse*-containere.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="0f8d0-185">Anbringe en vare til lagring</span><span class="sxs-lookup"><span data-stu-id="0f8d0-185">Place an item into storage</span></span>

1. <span data-ttu-id="0f8d0-186">Åbn mobilenheden, log på lagersted 63, og gå til **Lager \> Reguler ind**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="0f8d0-187">Angiv **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="0f8d0-188">Lav en ny nummerplade med **Vare** = *A0001* og **Antal** = *1 stk.*.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="0f8d0-189">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-189">Select **OK**.</span></span> <span data-ttu-id="0f8d0-190">Du modtager fejlen "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span><span class="sxs-lookup"><span data-stu-id="0f8d0-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="0f8d0-191">Det skyldes, at produktets *lagringstypedimensioner* er større end de dimensioner, der er angivet i lokationsprofilen.</span><span class="sxs-lookup"><span data-stu-id="0f8d0-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>
