---
title: Konsolidere forsendelser, når de frigives til lagerstedet, ved hjælp af automatisk frigivelse af salgsordrer
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den automatiserede procedure til periodisk frigivelse til lagersted.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7102eade4a26f4b4dc08adb395aa7b50a630b9d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243937"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="5b44d-103">Konsolidere forsendelser, når de frigives til lagerstedet, ved hjælp af automatisk frigivelse af salgsordrer</span><span class="sxs-lookup"><span data-stu-id="5b44d-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b44d-104">Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den automatiserede procedure til periodisk frigivelse til lagersted.</span><span class="sxs-lookup"><span data-stu-id="5b44d-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="5b44d-105">Ordrerne vil automatisk blive konsolideret til forsendelser baseret på regler, der er defineret som politikker for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="5b44d-106">I løbet af scenariet opretter du sæt af salgsordrer og frigiver hvert sæt til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="5b44d-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="5b44d-107">Derefter skal du gennemse de forsendelser, der er oprettet eller opdateret under forsendelseskonsolidering, baseret på de konfigurerede politikker.</span><span class="sxs-lookup"><span data-stu-id="5b44d-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="5b44d-108">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="5b44d-108">Make demo data available</span></span>

<span data-ttu-id="5b44d-109">Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5b44d-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5b44d-110">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="5b44d-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="5b44d-111">Konfigurere politikker for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="5b44d-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="5b44d-112">I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="5b44d-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="5b44d-113">Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="5b44d-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="5b44d-114">Oprette salgsordrer til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="5b44d-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="5b44d-115">Start med at oprette en samling salgsordrer, som du kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="5b44d-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="5b44d-116">Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="5b44d-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="5b44d-117">Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.</span><span class="sxs-lookup"><span data-stu-id="5b44d-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="5b44d-118">Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="5b44d-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="5b44d-119">Opret ordresæt 1</span><span class="sxs-lookup"><span data-stu-id="5b44d-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="5b44d-120">Salgsordre 1-1</span><span class="sxs-lookup"><span data-stu-id="5b44d-120">Sales order 1-1</span></span>

1. <span data-ttu-id="5b44d-121">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-122">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b44d-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b44d-123">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="5b44d-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="5b44d-124">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-125">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-126">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="5b44d-127">Salgsordre 1-2</span><span class="sxs-lookup"><span data-stu-id="5b44d-127">Sales order 1-2</span></span>

1. <span data-ttu-id="5b44d-128">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-129">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b44d-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b44d-130">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="5b44d-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="5b44d-131">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-132">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-133">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="5b44d-134">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="5b44d-134">Sales order 1-3</span></span>

1. <span data-ttu-id="5b44d-135">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-136">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b44d-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b44d-137">**Leveringsmåde:** *10*</span><span class="sxs-lookup"><span data-stu-id="5b44d-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="5b44d-138">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-139">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-140">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5b44d-141">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-142">**Varenummer:** *A0002* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-143">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="5b44d-144">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="5b44d-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="5b44d-145">Opret ordresæt 2</span><span class="sxs-lookup"><span data-stu-id="5b44d-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="5b44d-146">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="5b44d-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="5b44d-147">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5b44d-148">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="5b44d-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="5b44d-149">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-150">**Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)</span><span class="sxs-lookup"><span data-stu-id="5b44d-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="5b44d-151">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5b44d-152">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-153">**Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)</span><span class="sxs-lookup"><span data-stu-id="5b44d-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="5b44d-154">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="5b44d-155">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="5b44d-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="5b44d-156">Opret ordresæt 3</span><span class="sxs-lookup"><span data-stu-id="5b44d-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="5b44d-157">Salgsordre 3-1</span><span class="sxs-lookup"><span data-stu-id="5b44d-157">Sales order 3-1</span></span>

1. <span data-ttu-id="5b44d-158">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-159">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="5b44d-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="5b44d-160">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-161">**Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)</span><span class="sxs-lookup"><span data-stu-id="5b44d-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="5b44d-162">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="5b44d-163">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-164">**Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)</span><span class="sxs-lookup"><span data-stu-id="5b44d-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="5b44d-165">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="5b44d-166">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="5b44d-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="5b44d-167">Denne ordre er identisk med de to ordrer, du har oprettet for ordresæt 2.</span><span class="sxs-lookup"><span data-stu-id="5b44d-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="5b44d-168">Men den er angivet som sin egen ordre, fordi du frigiver den på et senere tidspunkt i dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="5b44d-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="5b44d-169">Opret ordresæt 4</span><span class="sxs-lookup"><span data-stu-id="5b44d-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="5b44d-170">Salgsordre 4-1</span><span class="sxs-lookup"><span data-stu-id="5b44d-170">Sales order 4-1</span></span>

1. <span data-ttu-id="5b44d-171">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-172">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b44d-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b44d-173">**Debitorrekvisition:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b44d-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="5b44d-174">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-175">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-176">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="5b44d-177">Opret ordresæt 5</span><span class="sxs-lookup"><span data-stu-id="5b44d-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="5b44d-178">Salgsordrer 5-1 og 5-2</span><span class="sxs-lookup"><span data-stu-id="5b44d-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="5b44d-179">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5b44d-180">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b44d-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b44d-181">**Debitorrekvisition:** *2*</span><span class="sxs-lookup"><span data-stu-id="5b44d-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="5b44d-182">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-183">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-184">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="5b44d-185">Salgsordre 5-3</span><span class="sxs-lookup"><span data-stu-id="5b44d-185">Sales order 5-3</span></span>

1. <span data-ttu-id="5b44d-186">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-187">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5b44d-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5b44d-188">**Debitorrekvisition:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b44d-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="5b44d-189">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-190">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-191">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="5b44d-192">Opret ordresæt 6</span><span class="sxs-lookup"><span data-stu-id="5b44d-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="5b44d-193">Salgsordrer 6-1 og 6-2</span><span class="sxs-lookup"><span data-stu-id="5b44d-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="5b44d-194">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5b44d-195">**Debitorkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="5b44d-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="5b44d-196">**Debitorrekvisition:** *2*</span><span class="sxs-lookup"><span data-stu-id="5b44d-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="5b44d-197">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-198">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-199">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="5b44d-200">Salgsordrer 6-3 og 6-4</span><span class="sxs-lookup"><span data-stu-id="5b44d-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="5b44d-201">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5b44d-202">**Debitorkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="5b44d-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="5b44d-203">**Debitorrekvisition:** *1*</span><span class="sxs-lookup"><span data-stu-id="5b44d-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="5b44d-204">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-205">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-206">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="5b44d-207">Salgsordrer 6-5 og 6-6</span><span class="sxs-lookup"><span data-stu-id="5b44d-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="5b44d-208">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5b44d-209">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="5b44d-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="5b44d-210">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="5b44d-210">**Site:** *6*</span></span>
    - <span data-ttu-id="5b44d-211">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="5b44d-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="5b44d-212">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="5b44d-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="5b44d-213">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-214">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-215">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="5b44d-216">Salgsordrer 6-7 og 6-8</span><span class="sxs-lookup"><span data-stu-id="5b44d-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="5b44d-217">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="5b44d-218">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="5b44d-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="5b44d-219">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="5b44d-219">**Site:** *6*</span></span>
    - <span data-ttu-id="5b44d-220">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="5b44d-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="5b44d-221">**Pulje:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="5b44d-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="5b44d-222">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5b44d-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="5b44d-223">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="5b44d-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="5b44d-224">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="5b44d-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="5b44d-225">Automatisk frigivelse af salgsordrer til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="5b44d-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="5b44d-226">For hvert sæt af salgsordrer, du har oprettet tidligere, fuldfører du en procedure for automatisk frigivelse til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="5b44d-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="5b44d-227">I hvert enkelt tilfælde kan du arbejde via [den procedure for frigivelse til lager](#release-procedure), der angives her.</span><span class="sxs-lookup"><span data-stu-id="5b44d-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="5b44d-228">Grundlæggende procedure for frigivelse til lager</span><span class="sxs-lookup"><span data-stu-id="5b44d-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="5b44d-229">For hvert sæt af salgsordrer, du har oprettet tidligere, skal du fuldføre de tre fremgangsmåder, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="5b44d-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="5b44d-230">Opdater den bølgeskabelon, der vil blive brugt under frigivelse</span><span class="sxs-lookup"><span data-stu-id="5b44d-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="5b44d-231">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="5b44d-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5b44d-232">Indstil feltet **Bølgeskabelontype** til *Forsendelse*.</span><span class="sxs-lookup"><span data-stu-id="5b44d-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="5b44d-233">Find og vælg den bølgeskabelon, der er knyttet til det lagersted, du har brugt i de ordresæt, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="5b44d-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="5b44d-234">Hvis du f.eks. brugte lagerstedet *24*, skal du vælge bølgeskabelonen **24 Standard for forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="5b44d-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="5b44d-235">Hvis du brugte lagerstedet *61*, skal du vælge bølgeskabelonen **61 Forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="5b44d-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="5b44d-236">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5b44d-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5b44d-237">Angiv indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="5b44d-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="5b44d-238">Frigiv til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="5b44d-238">Release to the warehouse</span></span>

1. <span data-ttu-id="5b44d-239">Gå til **Lagerstedsstyring \> Frigiv til lagersted \> Automatisk frigivelse af salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5b44d-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="5b44d-240">Angiv feltet **Antal til frigivelse** til *Alle*.</span><span class="sxs-lookup"><span data-stu-id="5b44d-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="5b44d-241">Gå til oversigtspanelet **Poster, der skal indgå**, og vælg **Filter** for at åbne forespørgselsdialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5b44d-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="5b44d-242">Gå til fanen **Område**, og vælg **Tilføj** for at tilføje en række, der har følgende indstillinger, til gitteret:</span><span class="sxs-lookup"><span data-stu-id="5b44d-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="5b44d-243">**Tabel:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="5b44d-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="5b44d-244">**Afledt tabel:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="5b44d-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="5b44d-245">**Felt:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="5b44d-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="5b44d-246">**Kriterier:** Angiv en kommasepareret liste over salgsordrenumrene fra det ønskede ordresæt.</span><span class="sxs-lookup"><span data-stu-id="5b44d-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="5b44d-247">Vælg **OK** for at gemme forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="5b44d-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="5b44d-248">Vælg **OK** for at starte proceduren *Automatisk frigivelse til lagersted*.</span><span class="sxs-lookup"><span data-stu-id="5b44d-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="5b44d-249">Gennemse den forsendelse, der er oprettet eller opdateret</span><span class="sxs-lookup"><span data-stu-id="5b44d-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="5b44d-250">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="5b44d-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="5b44d-251">Find og vælg den nødvendige forsendelse.</span><span class="sxs-lookup"><span data-stu-id="5b44d-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="5b44d-252">Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="5b44d-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="5b44d-253">Frigiv salgsordrer fra ordresæt 1</span><span class="sxs-lookup"><span data-stu-id="5b44d-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="5b44d-254">Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 1.</span><span class="sxs-lookup"><span data-stu-id="5b44d-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="5b44d-255">Når du er færdig, burde du kunne se, at der er oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="5b44d-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="5b44d-256">Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="5b44d-257">Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="5b44d-258">Frigiv salgsordrer fra ordresæt 2</span><span class="sxs-lookup"><span data-stu-id="5b44d-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="5b44d-259">Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 2.</span><span class="sxs-lookup"><span data-stu-id="5b44d-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="5b44d-260">Når du er færdig, burde du kunne se, at der er oprettet tre forsendelser:</span><span class="sxs-lookup"><span data-stu-id="5b44d-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="5b44d-261">Den første forsendelse indeholder *brændfarlige* varer.</span><span class="sxs-lookup"><span data-stu-id="5b44d-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="5b44d-262">Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.</span><span class="sxs-lookup"><span data-stu-id="5b44d-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="5b44d-263">Frigiv salgsordrer fra ordresæt 3</span><span class="sxs-lookup"><span data-stu-id="5b44d-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="5b44d-264">Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 3.</span><span class="sxs-lookup"><span data-stu-id="5b44d-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="5b44d-265">Når du er færdig, burde du kunne se, at følgende handlinger er sket:</span><span class="sxs-lookup"><span data-stu-id="5b44d-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="5b44d-266">En eksisterende forsendelse (den forsendelse, der blev oprettet, da ordresæt 2 blev frigivet til lagerstedet) blev opdateret.</span><span class="sxs-lookup"><span data-stu-id="5b44d-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="5b44d-267">Der er tilføjet en linje , hvor varen *brændbar* blev tilføjet.</span><span class="sxs-lookup"><span data-stu-id="5b44d-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="5b44d-268">Der blev oprettet en ny forsendelse, som indeholder varen *Eksplosiv*.</span><span class="sxs-lookup"><span data-stu-id="5b44d-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="5b44d-269">Frigiv salgsordrer fra ordresæt 4</span><span class="sxs-lookup"><span data-stu-id="5b44d-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="5b44d-270">Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 4.</span><span class="sxs-lookup"><span data-stu-id="5b44d-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="5b44d-271">Når du er færdig, burde du kunne se, at en eksisterende forsendelse (hvor feltet **Debitorrekvisition** er angivet til *1*) blev opdateret.</span><span class="sxs-lookup"><span data-stu-id="5b44d-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="5b44d-272">Der blev føjet en ny linje til den.</span><span class="sxs-lookup"><span data-stu-id="5b44d-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="5b44d-273">Frigiv salgsordrer fra ordresæt 5</span><span class="sxs-lookup"><span data-stu-id="5b44d-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="5b44d-274">Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 5.</span><span class="sxs-lookup"><span data-stu-id="5b44d-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="5b44d-275">Når du er færdig, burde du kunne se, at følgende handlinger er sket:</span><span class="sxs-lookup"><span data-stu-id="5b44d-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="5b44d-276">En eksisterende forsendelse (hvor feltet **Debitorrekvisition** er angivet til *1*) blev opdateret.</span><span class="sxs-lookup"><span data-stu-id="5b44d-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="5b44d-277">En linje fra salgsordren 5-3 (hvor feltet **Debitorrekvisition** er angivet til *1*) blev føjet til den.</span><span class="sxs-lookup"><span data-stu-id="5b44d-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="5b44d-278">Der blev oprettet en ny forsendelse, hvor linjerne fra salgsordrerne 5-1 og 5-2 er grupperet i én forsendelse.</span><span class="sxs-lookup"><span data-stu-id="5b44d-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="5b44d-279">Frigiv salgsordrer fra ordresæt 6</span><span class="sxs-lookup"><span data-stu-id="5b44d-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="5b44d-280">Følg den [grundlæggende procedure for frigivelse til lager](#release-procedure) for at frigive salgsordrerne fra ordresæt 6.</span><span class="sxs-lookup"><span data-stu-id="5b44d-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="5b44d-281">Når du er færdig, burde du kunne se, at der er oprettet fire forsendelser:</span><span class="sxs-lookup"><span data-stu-id="5b44d-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="5b44d-282">Linjer fra to ordrer på kunde *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="5b44d-283">Linjer fra to ordrer på kunde *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="5b44d-284">Linjer fra salgsordrer 6-5 og 6-6 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="5b44d-285">Linjer fra salgsordrer 6-7 og 6-8 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="5b44d-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b44d-286">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5b44d-286">Additional resources</span></span>

- [<span data-ttu-id="5b44d-287">Forsendelseskonsolideringspolitikker</span><span class="sxs-lookup"><span data-stu-id="5b44d-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="5b44d-288">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="5b44d-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]