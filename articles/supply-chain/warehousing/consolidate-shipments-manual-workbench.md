---
title: Konsolidere forsendelser ved hjælp af panelet for forsendelseskonsolidering
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet, hvorefter disse senere konsolideres til forsendelser ved hjælp af panelet for forsendelseskonsolidering.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1eec1a8e3a9a2a0f95302e1d6ea68eb90b9a3b93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016810"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="0b7da-103">Konsolidere forsendelser ved hjælp af panelet for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="0b7da-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b7da-104">Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet, hvorefter disse senere konsolideres til forsendelser ved hjælp af panelet for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="0b7da-105">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="0b7da-105">Make demo data available</span></span>

<span data-ttu-id="0b7da-106">Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0b7da-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0b7da-107">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF** , før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="0b7da-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="0b7da-108">Konfigurere politikker for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="0b7da-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="0b7da-109">I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="0b7da-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="0b7da-110">Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="0b7da-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="0b7da-111">Slå funktionen til manuel forsendelseskonsolidering til</span><span class="sxs-lookup"><span data-stu-id="0b7da-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="0b7da-112">Før du kan bruge funktionen *Manuel forsendelseskonsolidering* , skal du slå den til i systemet.</span><span class="sxs-lookup"><span data-stu-id="0b7da-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="0b7da-113">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="0b7da-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="0b7da-114">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0b7da-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0b7da-115">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="0b7da-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0b7da-116">**Funktionsnavn:** *Manuel forsendelseskonsolidering*</span><span class="sxs-lookup"><span data-stu-id="0b7da-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="0b7da-117">Som det blev nævnt i [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md), skal du også aktivere funktionen *Konsolider forsendelse* , før du kan oprette politikker.</span><span class="sxs-lookup"><span data-stu-id="0b7da-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="0b7da-118">Du skal dog allerede have fuldført dette trin.</span><span class="sxs-lookup"><span data-stu-id="0b7da-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="0b7da-119">Oprette salgsordrer til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="0b7da-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="0b7da-120">Start med at oprette en samling salgsordrer, som du kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="0b7da-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="0b7da-121">Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="0b7da-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="0b7da-122">Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.</span><span class="sxs-lookup"><span data-stu-id="0b7da-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="0b7da-123">Gå til **Debitor \> Ordrer \> Alle salgsordrer** , og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="0b7da-123">Go to **Accounts receivable \> Orders \> All sales orders** , and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="0b7da-124">Opret ordresæt 1</span><span class="sxs-lookup"><span data-stu-id="0b7da-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="0b7da-125">Salgsordrer 1-1 og 1-2</span><span class="sxs-lookup"><span data-stu-id="0b7da-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="0b7da-126">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-127">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0b7da-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0b7da-128">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0b7da-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0b7da-129">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-130">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-131">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-132">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-132">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="0b7da-133">Salgsordre 1-3</span><span class="sxs-lookup"><span data-stu-id="0b7da-133">Sales order 1-3</span></span>

1. <span data-ttu-id="0b7da-134">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-135">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0b7da-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0b7da-136">**Leveringsmåde:** *10*</span><span class="sxs-lookup"><span data-stu-id="0b7da-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="0b7da-137">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-138">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-139">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-140">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-140">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="0b7da-141">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-142">**Varenummer:** *A0002* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-143">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="0b7da-144">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0b7da-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0b7da-145">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="0b7da-145">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="0b7da-146">Opret ordresæt 2</span><span class="sxs-lookup"><span data-stu-id="0b7da-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="0b7da-147">Salgsordrer 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="0b7da-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="0b7da-148">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-149">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="0b7da-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="0b7da-150">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0b7da-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0b7da-151">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-152">**Varenummer:** *M9200* (en vare, hvor filtret **Kode 4** er indstillet til *Brændbar* )</span><span class="sxs-lookup"><span data-stu-id="0b7da-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable* )</span></span>
    - <span data-ttu-id="0b7da-153">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-154">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-154">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="0b7da-155">Tilføj en anden ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-156">**Varenummer:** *M9201* (en vare, hvor filtret **Kode 4** er indstillet til *Eksplosiv* )</span><span class="sxs-lookup"><span data-stu-id="0b7da-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive* )</span></span>
    - <span data-ttu-id="0b7da-157">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="0b7da-158">**Leveringsmåde:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="0b7da-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="0b7da-159">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="0b7da-159">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="0b7da-160">Opret ordresæt 3</span><span class="sxs-lookup"><span data-stu-id="0b7da-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="0b7da-161">Salgsordrer 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="0b7da-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="0b7da-162">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-163">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0b7da-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0b7da-164">**Debitorrekvisition:** *1*</span><span class="sxs-lookup"><span data-stu-id="0b7da-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="0b7da-165">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-166">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-167">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-168">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-168">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="0b7da-169">Salgsordrer 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="0b7da-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="0b7da-170">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-171">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0b7da-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0b7da-172">**Debitorrekvisition:** *2*</span><span class="sxs-lookup"><span data-stu-id="0b7da-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="0b7da-173">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-174">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-175">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-176">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-176">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="0b7da-177">Opret ordresæt 4</span><span class="sxs-lookup"><span data-stu-id="0b7da-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="0b7da-178">Salgsordrer 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="0b7da-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="0b7da-179">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-180">**Debitorkonto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="0b7da-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="0b7da-181">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-182">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-183">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-184">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-184">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="0b7da-185">Salgsordrer 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="0b7da-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="0b7da-186">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-187">**Debitorkonto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="0b7da-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="0b7da-188">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-189">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-190">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-191">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-191">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="0b7da-192">Salgsordrer 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="0b7da-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="0b7da-193">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-194">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0b7da-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0b7da-195">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="0b7da-195">**Site:** *6*</span></span>
    - <span data-ttu-id="0b7da-196">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="0b7da-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="0b7da-197">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="0b7da-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="0b7da-198">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-199">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-200">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-201">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-201">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="0b7da-202">Salgsordrer 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="0b7da-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="0b7da-203">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="0b7da-204">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0b7da-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0b7da-205">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="0b7da-205">**Site:** *6*</span></span>
    - <span data-ttu-id="0b7da-206">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="0b7da-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="0b7da-207">**Pulje:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="0b7da-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="0b7da-208">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0b7da-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="0b7da-209">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4** -filter)</span><span class="sxs-lookup"><span data-stu-id="0b7da-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="0b7da-210">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0b7da-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="0b7da-211">Vælg **Lager \> Reservation** ,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-211">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="0b7da-212">Frigive ordrerne til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="0b7da-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="0b7da-213">Udfør følgende trin for at frigive hver salgsordre, du har oprettet i dette scenarie, til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="0b7da-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="0b7da-214">Gå til **Debitor \> Ordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0b7da-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0b7da-215">Find og vælg den salgsordre, der skal frigives.</span><span class="sxs-lookup"><span data-stu-id="0b7da-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="0b7da-216">I handlingsruden skal du på fanen **Lagersted** vælge **Handlinger \> Frigiv til lagersted** for at at frigive den valgte salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0b7da-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="0b7da-217">Gentag denne procedure for hver anden salgsordre, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="0b7da-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="0b7da-218">Konsolidere forsendelserne ved hjælp af panelet for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="0b7da-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="0b7da-219">Gå til **Lagerstyringssted \> Frigiv til lagersted \> Frigiv til forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="0b7da-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="0b7da-220">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0b7da-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="0b7da-221">Gå til dialogboksen for forespørgselseditor, og vælg **Tilføj** på fanen **Område** for at tilføje en række, der har følgende indstillinger, til gitteret:</span><span class="sxs-lookup"><span data-stu-id="0b7da-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="0b7da-222">**Tabel:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="0b7da-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="0b7da-223">**Felt:** *Salgsordre*</span><span class="sxs-lookup"><span data-stu-id="0b7da-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="0b7da-224">**Kriterier:** Angiv en kommasepareret liste over salgsordrenumrene for hvert ordresæt, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="0b7da-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="0b7da-225">Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b7da-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="0b7da-226">Vælg **Konsolider forsendelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0b7da-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="0b7da-227">Vælg alle forsendelserne, og vælg derefter **Konsolider** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0b7da-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="0b7da-228">Kontrollér forsendelserne</span><span class="sxs-lookup"><span data-stu-id="0b7da-228">Verify the shipments</span></span>

<span data-ttu-id="0b7da-229">I følgende procedure kan du kontrollere de forsendelser, der er oprettet eller opdateret som resultat af forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="0b7da-230">Brug den til at gennemgå de ordresæt, du har oprettet for dette scenario, og gennemse derefter de underafsnit, der følger efter, for at sikre, at du har opnået de forventede resultater.</span><span class="sxs-lookup"><span data-stu-id="0b7da-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="0b7da-231">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="0b7da-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="0b7da-232">Find og vælg den nødvendige forsendelse.</span><span class="sxs-lookup"><span data-stu-id="0b7da-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="0b7da-233">Hvis der blev brugt en forsendelsespolitik, da forsendelsen blev oprettet eller opdateret, burde du kunne se den i feltet **Politik for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="0b7da-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="0b7da-234">Relaterede forsendelser for ordresæt 1</span><span class="sxs-lookup"><span data-stu-id="0b7da-234">Related shipments for order set 1</span></span>

<span data-ttu-id="0b7da-235">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="0b7da-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="0b7da-236">Den første forsendelse indeholder tre linjer og er oprettet ved hjælp af politikken *Kundetilstand* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="0b7da-237">Den anden forsendelse, der ikke bruger transportmåden *Flytransport* til levering, blev oprettet ved hjælp af politikken *Kundeordrenr.* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="0b7da-238">Relaterede forsendelser for ordresæt 2</span><span class="sxs-lookup"><span data-stu-id="0b7da-238">Related shipments for order set 2</span></span>

<span data-ttu-id="0b7da-239">Der skal være oprettet tre forsendelser:</span><span class="sxs-lookup"><span data-stu-id="0b7da-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="0b7da-240">Den første forsendelse indeholder *brændfarlige* varer.</span><span class="sxs-lookup"><span data-stu-id="0b7da-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="0b7da-241">Hver af de to andre forsendelser indeholder én linje med den *eksplosive* vare.</span><span class="sxs-lookup"><span data-stu-id="0b7da-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="0b7da-242">Relaterede forsendelser for ordresæt 3</span><span class="sxs-lookup"><span data-stu-id="0b7da-242">Related shipments for order set 3</span></span>

<span data-ttu-id="0b7da-243">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="0b7da-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="0b7da-244">Den første forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *1*.</span><span class="sxs-lookup"><span data-stu-id="0b7da-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="0b7da-245">Den anden forsendelse indeholder ordrelinjer fra den salgsordre, hvor feltet **Debitorrekvisition** er angivet til *2*.</span><span class="sxs-lookup"><span data-stu-id="0b7da-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="0b7da-246">Relaterede forsendelser for ordresæt 4</span><span class="sxs-lookup"><span data-stu-id="0b7da-246">Related shipments for order set 4</span></span>

<span data-ttu-id="0b7da-247">Der skal være oprettet fire forsendelser:</span><span class="sxs-lookup"><span data-stu-id="0b7da-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="0b7da-248">Linjer fra to ordrer på kunde *US-003* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="0b7da-249">Linjer fra to ordrer på kunde *US-004* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="0b7da-250">Linjer fra salgsordrer 4-5 og 4-6 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Ordrepulje* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="0b7da-251">Linjer fra salgsordrer 4-7 og 4-8 for kunden *US-007* blev grupperet i én forsendelse ved hjælp af politikken *Krydsordre* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="0b7da-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b7da-252">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0b7da-252">Additional resources</span></span>

- [<span data-ttu-id="0b7da-253">Forsendelseskonsolideringspolitikker</span><span class="sxs-lookup"><span data-stu-id="0b7da-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="0b7da-254">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="0b7da-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
