---
title: Lagersøgning i POS
description: Dette emne beskriver de indstillinger, der er tilgængelige for visning af lageroplysninger i salgsstedet (POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: f08906c14f80b07368d88d820acae83cf1157e6c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969945"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="2023f-103">Lagersøgning i POS</span><span class="sxs-lookup"><span data-stu-id="2023f-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2023f-104">Lagersøgning i salgsstedet (POS) hjælper detailhandlere med at opnå flotte resultater i realtid og få indsigt ved at forbinde butikker, salgstedet og administrationen.</span><span class="sxs-lookup"><span data-stu-id="2023f-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="2023f-105">Denne funktion giver en præcis visning af produktlageret i realtid på tværs af butikker og distributionscentre.</span><span class="sxs-lookup"><span data-stu-id="2023f-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="2023f-106">Det hjælper også detailhandlere med at fremme effektiviteten og omkostningsbesparelser ved at forbedre lagerplanlægning i realtid.</span><span class="sxs-lookup"><span data-stu-id="2023f-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="2023f-107">En præcis visning af lageret for hele virksomheden i realtid hjælper lagermedarbejdere med at levere rettidig og fremragende kundeservice.</span><span class="sxs-lookup"><span data-stu-id="2023f-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="2023f-108">Det vigtigste tidspunkt, er det øjeblik, hvor kunden er klar til at træffe en købsbeslutning.</span><span class="sxs-lookup"><span data-stu-id="2023f-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="2023f-109">Det er vigtigt, at kasserere i butikken har lageroplysninger i realtid ved hånden, så de kan garantere præcis produktlevering og afhentning.</span><span class="sxs-lookup"><span data-stu-id="2023f-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="2023f-110">Du kan åbne siden **Lagersøgning** fra arbejdsområdet **Retail Modern POS** eller **Retail Cloud POS**.</span><span class="sxs-lookup"><span data-stu-id="2023f-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Feltet Lagersøgning på POS-startside](media/POSHomepage.png)

<span data-ttu-id="2023f-112">På siden **Lagersøgning** kan du bruge det numeriske tastatur til at angive et produktnummer.</span><span class="sxs-lookup"><span data-stu-id="2023f-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="2023f-113">Du kan derefter få vist det disponible antal for flere butikker og lagersteder.</span><span class="sxs-lookup"><span data-stu-id="2023f-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standardside for lagersøgning](media/InventoryLookUp.png)

<span data-ttu-id="2023f-115">Antal, der er **Reserveret** og **Bestilt**, vises også for hver lokation.</span><span class="sxs-lookup"><span data-stu-id="2023f-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="2023f-116">**Reserveret** – Dette antal refererer til værdien **Fysisk reserveret** fra administrationen for det angivne produktnummer på lokationen.</span><span class="sxs-lookup"><span data-stu-id="2023f-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="2023f-117">**Bestilt** – Dette antal refererer til værdien **Bestilt i alt** fra administrationen for det angivne produktnummer på lokationen.</span><span class="sxs-lookup"><span data-stu-id="2023f-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="2023f-118">Lokationer, som oplysninger om disponibel lagerbeholdning vises for</span><span class="sxs-lookup"><span data-stu-id="2023f-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="2023f-119">Listen over lokationer indeholder to typer enheder:</span><span class="sxs-lookup"><span data-stu-id="2023f-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="2023f-120">**Butikker** – Listen viser butikker, der er konfigureret ved hjælp af butikssøgergruppen for den aktuelle butik i hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="2023f-120">**Stores** – The list shows stores that are configured by using the store locator group for the current store in the Headquarters.</span></span>
- <span data-ttu-id="2023f-121">**Distributionscentre** – Forskellige typer distributionscentre (f.eks. lagersteder) kan konfigureres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="2023f-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Commerce.</span></span> <span data-ttu-id="2023f-122">Listen viser dog kun oplysninger om disponibel lagerbeholdning for distributionscentre af typen **Standard**.</span><span class="sxs-lookup"><span data-stu-id="2023f-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2023f-123">Oplysninger om disponibel lagerbeholdning vises ikke for lagersteder af typerne **Transit**, **Karantæne** og **Varer undervejs** for POS.</span><span class="sxs-lookup"><span data-stu-id="2023f-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="2023f-124">På siden **Lagersøgning** kan du få vist disponibel til tilsagn (DTT) for hver butik foruden de aktuelle disponible mængder, reserverede mængder og bestilte mængder.</span><span class="sxs-lookup"><span data-stu-id="2023f-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="2023f-125">Vælg den butik, du vil se DTT-oplysninger for, og vælg derefter **Vis butikkens tilgængelighed**.</span><span class="sxs-lookup"><span data-stu-id="2023f-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP-antal](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="2023f-127">Åbning af dimensionsbaseret matrix for at få vist alle varianter</span><span class="sxs-lookup"><span data-stu-id="2023f-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="2023f-128">På siden **Produktdetaljer** for en produktmaster eller på siden **Lagersøgning** skal du vælge **Vis alle varianter** fra applinjen nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="2023f-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="2023f-129">Visningen **Dimensionsbaseret matrix** for den første start af disse sider viser oplysninger om lagertilgængelighed for alle varianter af et produkt for den aktuelle butik.</span><span class="sxs-lookup"><span data-stu-id="2023f-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="2023f-130">Knappen **Vis alle varianter** er kun tilgængelig for vareproduktmastere med produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="2023f-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="2023f-131">Den er ikke tilgængelig for enkeltstående produkter eller pakker.</span><span class="sxs-lookup"><span data-stu-id="2023f-131">It isn't available for standalone products or kits.</span></span>

![Knappen Vis alle varianter på siden Lagersøgning](media/StandardToMatrix.png)

<span data-ttu-id="2023f-133">Vælg **Vis alle varianter** på siden **Produktdetaljer** for en produktmaster eller på siden **Lagersøgning** uden at vælge en lokation for at gå til visningen **Dimensionsbaseret matrix** for at se oplysninger om lagertilgængeligheden for alle varianter af et produkt for den aktuelle butik.</span><span class="sxs-lookup"><span data-stu-id="2023f-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Visningen Dimensionsbaseret matrix for siden Lagersøgning](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="2023f-135">I den foregående illustration vises dimensionerne i alfabetisk rækkefølge, fordi visningsrækkefølgen for dimensioner ikke var konfigureret for det valgte produkt.</span><span class="sxs-lookup"><span data-stu-id="2023f-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="2023f-136">I visningen **Dimensionsbaseret matrix** omfatter cellerne for produktvarianter en værdi for disponibel lagerbeholdning i nederste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="2023f-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="2023f-137">Følgende tabel forklarer betydningen af de forskellige værdier.</span><span class="sxs-lookup"><span data-stu-id="2023f-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="2023f-138">Beholdningsværdi</span><span class="sxs-lookup"><span data-stu-id="2023f-138">On-hand value</span></span>                            | <span data-ttu-id="2023f-139">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2023f-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="2023f-140">Numerisk værdi, der er større end 0 (nul)</span><span class="sxs-lookup"><span data-stu-id="2023f-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="2023f-141">En variant er frigivet til den valgte lokation, og du kan udføre yderligere handlinger i cellen.</span><span class="sxs-lookup"><span data-stu-id="2023f-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="2023f-142">(Disse handlinger er beskrevet nærmere senere i dette emne.)</span><span class="sxs-lookup"><span data-stu-id="2023f-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="2023f-143">**0** (nul)</span><span class="sxs-lookup"><span data-stu-id="2023f-143">**0** (zero)</span></span>                             | <span data-ttu-id="2023f-144">En variant er blevet frigivet til den valgte lokation, men varen er ikke tilgængelig i den valgte lokation.</span><span class="sxs-lookup"><span data-stu-id="2023f-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="2023f-145">Du kan dog udføre yderligere handlinger i cellen.</span><span class="sxs-lookup"><span data-stu-id="2023f-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="2023f-146">(Disse handlinger er beskrevet nærmere senere i dette emne.)</span><span class="sxs-lookup"><span data-stu-id="2023f-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="2023f-147">**i/t** eller en inaktiv celle</span><span class="sxs-lookup"><span data-stu-id="2023f-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="2023f-148">En variant er blevet frigivet til den valgte lokation, og du kan ikke udføre yderligere handlinger i cellen.</span><span class="sxs-lookup"><span data-stu-id="2023f-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="2023f-149">Du kan også ændre pivot for dimensioner ved at vælge den nye dimension, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="2023f-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Ændring af pivot](media/ChangePivot.png)

![Pivot ændret](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="2023f-152">I de foregående illustrationer er visningsrækkefølgen af dimensioner for det valgte produkt brugerdefineret (ikke-alfabetisk).</span><span class="sxs-lookup"><span data-stu-id="2023f-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="2023f-153">Den er baseret på den visningsrækkefølge for dimensionen, der er angivet i administrationen.</span><span class="sxs-lookup"><span data-stu-id="2023f-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="2023f-154">I visningen **Dimensionsbaseret matrix** kan der udføres flere handlinger for at øge butiksmedarbejderens produktivitet.</span><span class="sxs-lookup"><span data-stu-id="2023f-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="2023f-155">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="2023f-155">Here are some examples:</span></span>

- <span data-ttu-id="2023f-156">Skift af butikslokationen for at søge efter lagertilgængeligheden for alle produktvarianter på andre lokationer.</span><span class="sxs-lookup"><span data-stu-id="2023f-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="2023f-157">Disse lokationer omfatter andre butikker i butikssøgergruppen og distributionscentrene af typen **Standard**.</span><span class="sxs-lookup"><span data-stu-id="2023f-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="2023f-158">Sælg en enkelt produktvariant til en debitor ved hjælp af Cash & Carry, afhentning i butikken eller levering til en adresse.</span><span class="sxs-lookup"><span data-stu-id="2023f-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="2023f-159">Giv debitoren DTT-oplysninger for en individuel produktvariant for en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="2023f-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Yderligere handlinger for variantfelter](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="2023f-161">I den foregående illustration vises dimensionerne i alfabetisk rækkefølge, fordi visningsrækkefølgen for dimensioner ikke var konfigureret for det valgte produkt.</span><span class="sxs-lookup"><span data-stu-id="2023f-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="2023f-162">Følgende tabel indeholder flere oplysninger om yderligere handlinger, der er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="2023f-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="2023f-163">Handling</span><span class="sxs-lookup"><span data-stu-id="2023f-163">Action</span></span>               | <span data-ttu-id="2023f-164">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="2023f-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="2023f-165">Sælg nu</span><span class="sxs-lookup"><span data-stu-id="2023f-165">Sell now</span></span>             | <span data-ttu-id="2023f-166">Føj den valgte varevariant til transaktionen, og omdiriger brugeren til skærmbilledet for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="2023f-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="2023f-167">(Denne handling er ikke tilgængelig, når den valgte lokation er et distributionscenter).</span><span class="sxs-lookup"><span data-stu-id="2023f-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="2023f-168">Afhent i butik</span><span class="sxs-lookup"><span data-stu-id="2023f-168">Pick up in store</span></span>     | <span data-ttu-id="2023f-169">Opret en debitorordre for den produktvariant, som vil blive plukket fra den valgte lokation, og omdiriger brugeren til skærmbilledet for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="2023f-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="2023f-170">(Denne handling er ikke tilgængelig, når den valgte lokation er et distributionscenter).</span><span class="sxs-lookup"><span data-stu-id="2023f-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="2023f-171">Afsend produkt</span><span class="sxs-lookup"><span data-stu-id="2023f-171">Ship product</span></span>         | <span data-ttu-id="2023f-172">Opret en debitorordre for den produktvariant, som vil blive afsendt fra den valgte lokation, og omdiriger brugeren til skærmbilledet for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="2023f-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="2023f-173">Tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="2023f-173">Availability</span></span>         | <span data-ttu-id="2023f-174">Vis DTT-oplysninger for den valgte variantkombination for den valgte lokation.</span><span class="sxs-lookup"><span data-stu-id="2023f-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="2023f-175">Vis alle lokationer</span><span class="sxs-lookup"><span data-stu-id="2023f-175">Show all locations</span></span>   | <span data-ttu-id="2023f-176">Skift til standardvisningen for lagersøgning, og fremhæv oplysninger om lagertilgængeligheden for varevarianten på tværs af alle butikker i butikssøgergruppen, og i distributionscentre af tyden **Standard**.</span><span class="sxs-lookup"><span data-stu-id="2023f-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="2023f-177">Få vist produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="2023f-177">View product details</span></span> | <span data-ttu-id="2023f-178">Omdiriger brugeren til siden **Produktdetaljer** for den tilknyttede produktmaster.</span><span class="sxs-lookup"><span data-stu-id="2023f-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
