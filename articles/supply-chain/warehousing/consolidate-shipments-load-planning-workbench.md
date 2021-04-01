---
title: Konsolidere forsendelser ved at bruge Frigiv til lagersted fra panelet for lastplanlægning
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den samme last, som derefter konsolideres automatisk i forsendelser.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2fd13c2ceb8843b79b9dbc87acf77f219f0244f5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242247"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="34e9a-103">Konsolidere forsendelser ved at bruge Frigiv til lagersted fra panelet for lastplanlægning</span><span class="sxs-lookup"><span data-stu-id="34e9a-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34e9a-104">Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den samme last, som derefter konsolideres automatisk i forsendelser.</span><span class="sxs-lookup"><span data-stu-id="34e9a-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="34e9a-105">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="34e9a-105">Make demo data available</span></span>

<span data-ttu-id="34e9a-106">Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="34e9a-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="34e9a-107">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="34e9a-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="34e9a-108">Konfigurere politikker for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="34e9a-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="34e9a-109">I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="34e9a-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="34e9a-110">Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="34e9a-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="34e9a-111">Oprette salgsordrer til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="34e9a-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="34e9a-112">Start med at oprette en samling salgsordrer, som du kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="34e9a-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="34e9a-113">Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="34e9a-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="34e9a-114">Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.</span><span class="sxs-lookup"><span data-stu-id="34e9a-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="34e9a-115">Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="34e9a-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="34e9a-116">Opret ordresæt 1</span><span class="sxs-lookup"><span data-stu-id="34e9a-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="34e9a-117">Salgsordre 1-1</span><span class="sxs-lookup"><span data-stu-id="34e9a-117">Sales order 1-1</span></span>

1. <span data-ttu-id="34e9a-118">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-119">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="34e9a-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="34e9a-120">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="34e9a-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="34e9a-121">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-122">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-123">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-124">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="34e9a-125">Salgsordre 1-2</span><span class="sxs-lookup"><span data-stu-id="34e9a-125">Sales order 1-2</span></span>

1. <span data-ttu-id="34e9a-126">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-127">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="34e9a-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="34e9a-128">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="34e9a-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="34e9a-129">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-130">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-131">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-132">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="34e9a-133">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="34e9a-133">Sales order 1-3</span></span>

1. <span data-ttu-id="34e9a-134">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-135">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="34e9a-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="34e9a-136">**Leveringsmåde:** *10*</span><span class="sxs-lookup"><span data-stu-id="34e9a-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="34e9a-137">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-138">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-139">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-140">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="34e9a-141">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-142">**Varenummer:** *A0002* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-143">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="34e9a-144">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="34e9a-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="34e9a-145">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="34e9a-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="34e9a-146">Opret ordresæt 2</span><span class="sxs-lookup"><span data-stu-id="34e9a-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="34e9a-147">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="34e9a-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="34e9a-148">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-149">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="34e9a-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="34e9a-150">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-151">**Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)</span><span class="sxs-lookup"><span data-stu-id="34e9a-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="34e9a-152">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-153">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="34e9a-154">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-155">**Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)</span><span class="sxs-lookup"><span data-stu-id="34e9a-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="34e9a-156">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="34e9a-157">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="34e9a-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="34e9a-158">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="34e9a-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="34e9a-159">Opret ordresæt 3</span><span class="sxs-lookup"><span data-stu-id="34e9a-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="34e9a-160">Salgsordrer 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="34e9a-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="34e9a-161">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-162">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="34e9a-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="34e9a-163">**Debitorrekvisition:** *1*</span><span class="sxs-lookup"><span data-stu-id="34e9a-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="34e9a-164">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-165">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-166">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-167">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="34e9a-168">Salgsordrer 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="34e9a-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="34e9a-169">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-170">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="34e9a-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="34e9a-171">**Debitorrekvisition:** *2*</span><span class="sxs-lookup"><span data-stu-id="34e9a-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="34e9a-172">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-173">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-174">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-175">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="34e9a-176">Opret ordresæt 4</span><span class="sxs-lookup"><span data-stu-id="34e9a-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="34e9a-177">Salgsordrer 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="34e9a-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="34e9a-178">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-179">**Debitorkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="34e9a-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="34e9a-180">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-181">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-182">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-183">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="34e9a-184">Salgsordrer 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="34e9a-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="34e9a-185">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-186">**Debitorkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="34e9a-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="34e9a-187">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-188">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-189">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-190">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="34e9a-191">Salgsordrer 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="34e9a-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="34e9a-192">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-193">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="34e9a-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="34e9a-194">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="34e9a-194">**Site:** *6*</span></span>
    - <span data-ttu-id="34e9a-195">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="34e9a-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="34e9a-196">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="34e9a-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="34e9a-197">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-198">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-199">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-200">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="34e9a-201">Salgsordrer 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="34e9a-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="34e9a-202">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e9a-203">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="34e9a-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="34e9a-204">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="34e9a-204">**Site:** *6*</span></span>
    - <span data-ttu-id="34e9a-205">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="34e9a-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="34e9a-206">**Pulje:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="34e9a-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="34e9a-207">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="34e9a-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e9a-208">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="34e9a-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e9a-209">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e9a-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e9a-210">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="34e9a-211">Brug panelet for lastplanlægning til at oprette laster og frigive dem til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="34e9a-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="34e9a-212">Udfør følgende trin for at oprette en last for hvert ordresæt, du har oprettet i dette scenarie, og frigiv det derefter til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="34e9a-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="34e9a-213">Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="34e9a-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="34e9a-214">Under fanen **Salgslinjer** kan du finde og vælge alle salgsordrelinjer fra et af de ordresæt, du har oprettet for dette scenario.</span><span class="sxs-lookup"><span data-stu-id="34e9a-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="34e9a-215">I handlingsruden kan du under fanen **Udbud og efterspørgsel** vælge **Føj \> Til ny last** for at føje de valgte ordrelinjer til en ny last.</span><span class="sxs-lookup"><span data-stu-id="34e9a-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="34e9a-216">I dialogboksen **Tildeling af lastskabelon** skal du i feltet **Lastskabelon-id** vælge en lastskabelon, f.eks. *Standardlastskabelon*.</span><span class="sxs-lookup"><span data-stu-id="34e9a-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="34e9a-217">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="34e9a-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="34e9a-218">I sektionen **Laster** skal du vælge og finde den last, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="34e9a-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="34e9a-219">Vælg **Frigiv \> Frigiv til lagersted** for at frigive den valgte last til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="34e9a-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="34e9a-220">Gentag denne procedure for de øvrige tre ordresæt, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="34e9a-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="34e9a-221">Kontrollér forsendelserne</span><span class="sxs-lookup"><span data-stu-id="34e9a-221">Verify the shipments</span></span>

<span data-ttu-id="34e9a-222">I følgende procedure kan du kontrollere de forsendelser, der er oprettet eller opdateret som resultat af forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="34e9a-223">Brug den til at gennemgå de ordresæt, du har oprettet for dette scenario, og gennemse derefter de underafsnit, der følger efter, for at sikre, at du har opnået de forventede resultater.</span><span class="sxs-lookup"><span data-stu-id="34e9a-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="34e9a-224">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="34e9a-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="34e9a-225">Find og vælg den nødvendige forsendelse.</span><span class="sxs-lookup"><span data-stu-id="34e9a-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="34e9a-226">Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="34e9a-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="34e9a-227">Frigiv ordresæt 1 i en last</span><span class="sxs-lookup"><span data-stu-id="34e9a-227">Release order set 1 in one load</span></span>

<span data-ttu-id="34e9a-228">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="34e9a-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="34e9a-229">Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="34e9a-230">Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="34e9a-231">Frigiv ordresæt 2 i en last</span><span class="sxs-lookup"><span data-stu-id="34e9a-231">Release order set 2 in one load</span></span>

<span data-ttu-id="34e9a-232">Der skal være oprettet tre forsendelser:</span><span class="sxs-lookup"><span data-stu-id="34e9a-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="34e9a-233">Den første forsendelse indeholder de *brændfarlige* varer.</span><span class="sxs-lookup"><span data-stu-id="34e9a-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="34e9a-234">Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.</span><span class="sxs-lookup"><span data-stu-id="34e9a-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="34e9a-235">Frigiv ordresæt 3 i en last</span><span class="sxs-lookup"><span data-stu-id="34e9a-235">Release order set 3 in one load</span></span>

<span data-ttu-id="34e9a-236">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="34e9a-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="34e9a-237">Den første forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *1*.</span><span class="sxs-lookup"><span data-stu-id="34e9a-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="34e9a-238">Den anden forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *2*.</span><span class="sxs-lookup"><span data-stu-id="34e9a-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="34e9a-239">Frigiv ordresæt 4 i en last</span><span class="sxs-lookup"><span data-stu-id="34e9a-239">Release order set 4 in one load</span></span>

<span data-ttu-id="34e9a-240">Der skal være oprettet fire forsendelser:</span><span class="sxs-lookup"><span data-stu-id="34e9a-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="34e9a-241">Linjer fra to ordrer på kundekonto *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="34e9a-242">Linjer fra to ordrer på kundekonto *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="34e9a-243">Linjer fra salgsordrer 4-5 og 4-6 for kundekonto *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="34e9a-244">Linjer fra salgsordrer 4-7 og 4-8 for kundekonto *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="34e9a-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34e9a-245">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="34e9a-245">Additional resources</span></span>

- [<span data-ttu-id="34e9a-246">Forsendelseskonsolideringspolitikker</span><span class="sxs-lookup"><span data-stu-id="34e9a-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="34e9a-247">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="34e9a-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]