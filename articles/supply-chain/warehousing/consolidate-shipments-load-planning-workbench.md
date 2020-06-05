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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 396a038dbf2f4b6835ecbb5fd8cb39a3a3608af7
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383738"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="8708e-103">Konsolidere forsendelser ved at bruge Frigiv til lagersted fra panelet for lastplanlægning</span><span class="sxs-lookup"><span data-stu-id="8708e-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8708e-104">Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet i den samme last, som derefter konsolideres automatisk i forsendelser.</span><span class="sxs-lookup"><span data-stu-id="8708e-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="8708e-105">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="8708e-105">Make demo data available</span></span>

<span data-ttu-id="8708e-106">Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8708e-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8708e-107">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="8708e-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="8708e-108">Konfigurere politikker for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="8708e-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="8708e-109">I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="8708e-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="8708e-110">Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="8708e-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="8708e-111">Oprette salgsordrer til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="8708e-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="8708e-112">Start med at oprette en samling salgsordrer, som du kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="8708e-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="8708e-113">Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="8708e-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="8708e-114">Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.</span><span class="sxs-lookup"><span data-stu-id="8708e-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="8708e-115">Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="8708e-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="8708e-116">Opret ordresæt 1</span><span class="sxs-lookup"><span data-stu-id="8708e-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="8708e-117">Salgsordre 1-1</span><span class="sxs-lookup"><span data-stu-id="8708e-117">Sales order 1-1</span></span>

1. <span data-ttu-id="8708e-118">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8708e-119">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8708e-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8708e-120">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="8708e-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="8708e-121">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-122">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-123">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-124">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="8708e-125">Salgsordre 1-2</span><span class="sxs-lookup"><span data-stu-id="8708e-125">Sales order 1-2</span></span>

1. <span data-ttu-id="8708e-126">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8708e-127">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8708e-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8708e-128">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="8708e-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="8708e-129">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-130">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-131">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-132">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="8708e-133">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="8708e-133">Sales order 1-3</span></span>

1. <span data-ttu-id="8708e-134">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="8708e-135">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8708e-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8708e-136">**Leveringsmåde:** *10*</span><span class="sxs-lookup"><span data-stu-id="8708e-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="8708e-137">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-138">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-139">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-140">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="8708e-141">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-142">**Varenummer:** *A0002* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-143">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="8708e-144">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="8708e-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="8708e-145">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="8708e-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="8708e-146">Opret ordresæt 2</span><span class="sxs-lookup"><span data-stu-id="8708e-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="8708e-147">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="8708e-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="8708e-148">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-149">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="8708e-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="8708e-150">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-151">**Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar*)</span><span class="sxs-lookup"><span data-stu-id="8708e-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="8708e-152">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-153">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="8708e-154">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-155">**Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv*)</span><span class="sxs-lookup"><span data-stu-id="8708e-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="8708e-156">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="8708e-157">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="8708e-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="8708e-158">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="8708e-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="8708e-159">Opret ordresæt 3</span><span class="sxs-lookup"><span data-stu-id="8708e-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="8708e-160">Salgsordrer 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="8708e-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="8708e-161">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-162">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8708e-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8708e-163">**Debitorrekvisition:** *1*</span><span class="sxs-lookup"><span data-stu-id="8708e-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="8708e-164">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-165">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-166">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-167">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="8708e-168">Salgsordrer 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="8708e-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="8708e-169">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-170">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8708e-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8708e-171">**Debitorrekvisition:** *2*</span><span class="sxs-lookup"><span data-stu-id="8708e-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="8708e-172">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-173">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-174">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-175">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="8708e-176">Opret ordresæt 4</span><span class="sxs-lookup"><span data-stu-id="8708e-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="8708e-177">Salgsordrer 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="8708e-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="8708e-178">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-179">**Debitorkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="8708e-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="8708e-180">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-181">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-182">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-183">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="8708e-184">Salgsordrer 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="8708e-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="8708e-185">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-186">**Debitorkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="8708e-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="8708e-187">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-188">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-189">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-190">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="8708e-191">Salgsordrer 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="8708e-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="8708e-192">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-193">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8708e-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8708e-194">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="8708e-194">**Site:** *6*</span></span>
    - <span data-ttu-id="8708e-195">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="8708e-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="8708e-196">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="8708e-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="8708e-197">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-198">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-199">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-200">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="8708e-201">Salgsordrer 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="8708e-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="8708e-202">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8708e-203">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8708e-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8708e-204">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="8708e-204">**Site:** *6*</span></span>
    - <span data-ttu-id="8708e-205">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="8708e-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="8708e-206">**Pulje:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="8708e-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="8708e-207">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8708e-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8708e-208">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="8708e-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8708e-209">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8708e-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8708e-210">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8708e-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="8708e-211">Brug panelet for lastplanlægning til at oprette laster og frigive dem til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="8708e-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="8708e-212">Udfør følgende trin for at oprette en last for hvert ordresæt, du har oprettet i dette scenarie, og frigiv det derefter til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8708e-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="8708e-213">Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="8708e-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="8708e-214">Under fanen **Salgslinjer** kan du finde og vælge alle salgsordrelinjer fra et af de ordresæt, du har oprettet for dette scenario.</span><span class="sxs-lookup"><span data-stu-id="8708e-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="8708e-215">I handlingsruden kan du under fanen **Udbud og efterspørgsel** vælge **Føj \> Til ny last** for at føje de valgte ordrelinjer til en ny last.</span><span class="sxs-lookup"><span data-stu-id="8708e-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="8708e-216">I dialogboksen **Tildeling af lastskabelon** skal du i feltet **Lastskabelon-id** vælge en lastskabelon, f.eks. *Standardlastskabelon*.</span><span class="sxs-lookup"><span data-stu-id="8708e-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="8708e-217">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="8708e-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="8708e-218">I sektionen **Laster** skal du vælge og finde den last, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="8708e-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="8708e-219">Vælg **Frigiv \> Frigiv til lagersted** for at frigive den valgte last til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8708e-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="8708e-220">Gentag denne procedure for de øvrige tre ordresæt, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="8708e-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="8708e-221">Kontrollér forsendelserne</span><span class="sxs-lookup"><span data-stu-id="8708e-221">Verify the shipments</span></span>

<span data-ttu-id="8708e-222">I følgende procedure kan du kontrollere de forsendelser, der er oprettet eller opdateret som resultat af forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="8708e-223">Brug den til at gennemgå de ordresæt, du har oprettet for dette scenario, og gennemse derefter de underafsnit, der følger efter, for at sikre, at du har opnået de forventede resultater.</span><span class="sxs-lookup"><span data-stu-id="8708e-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="8708e-224">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="8708e-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="8708e-225">Find og vælg den nødvendige forsendelse.</span><span class="sxs-lookup"><span data-stu-id="8708e-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="8708e-226">Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="8708e-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="8708e-227">Frigiv ordresæt 1 i en last</span><span class="sxs-lookup"><span data-stu-id="8708e-227">Release order set 1 in one load</span></span>

<span data-ttu-id="8708e-228">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="8708e-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="8708e-229">Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="8708e-230">Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="8708e-231">Frigiv ordresæt 2 i en last</span><span class="sxs-lookup"><span data-stu-id="8708e-231">Release order set 2 in one load</span></span>

<span data-ttu-id="8708e-232">Der skal være oprettet tre forsendelser:</span><span class="sxs-lookup"><span data-stu-id="8708e-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="8708e-233">Den første forsendelse indeholder de *brændfarlige* varer.</span><span class="sxs-lookup"><span data-stu-id="8708e-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="8708e-234">Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.</span><span class="sxs-lookup"><span data-stu-id="8708e-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="8708e-235">Frigiv ordresæt 3 i en last</span><span class="sxs-lookup"><span data-stu-id="8708e-235">Release order set 3 in one load</span></span>

<span data-ttu-id="8708e-236">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="8708e-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="8708e-237">Den første forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *1*.</span><span class="sxs-lookup"><span data-stu-id="8708e-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="8708e-238">Den anden forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *2*.</span><span class="sxs-lookup"><span data-stu-id="8708e-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="8708e-239">Frigiv ordresæt 4 i en last</span><span class="sxs-lookup"><span data-stu-id="8708e-239">Release order set 4 in one load</span></span>

<span data-ttu-id="8708e-240">Der skal være oprettet fire forsendelser:</span><span class="sxs-lookup"><span data-stu-id="8708e-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="8708e-241">Linjer fra to ordrer på kundekonto *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="8708e-242">Linjer fra to ordrer på kundekonto *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="8708e-243">Linjer fra salgsordrer 4-5 og 4-6 for kundekonto *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="8708e-244">Linjer fra salgsordrer 4-7 og 4-8 for kundekonto *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="8708e-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8708e-245">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8708e-245">Additional resources</span></span>

- [<span data-ttu-id="8708e-246">Forsendelseskonsolideringspolitikker</span><span class="sxs-lookup"><span data-stu-id="8708e-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="8708e-247">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="8708e-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
