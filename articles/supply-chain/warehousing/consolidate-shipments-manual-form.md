---
title: Konsolidere forsendelser manuelt ved hjælp af siden Konsolider forsendelser
description: Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet og derefter konsolideres senere ved hjælp af siden Konsolider forsendelser.
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
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983008"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="f2fa2-103">Konsolidere forsendelser manuelt ved hjælp af siden Konsolider forsendelser</span><span class="sxs-lookup"><span data-stu-id="f2fa2-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2fa2-104">Dette emne viser et scenarie, hvor der frigives flere ordrer til lagerstedet og derefter konsolideres senere ved hjælp af siden **Konsolider forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="f2fa2-105">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="f2fa2-105">Make demo data available</span></span>

<span data-ttu-id="f2fa2-106">Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f2fa2-107">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="f2fa2-108">Konfigurere politikker for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="f2fa2-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="f2fa2-109">I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="f2fa2-110">Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="f2fa2-111">Oprette salgsordrer til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="f2fa2-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="f2fa2-112">Start med at oprette en samling salgsordrer, som du kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="f2fa2-113">Du skal arbejde med et lagersted, der er aktiveret til avancerede lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="f2fa2-114">Medmindre der udtrykkeligt er angivet et andet lagersted, skal det samme lagersted anvendes til hvert af følgende sæt ordrer.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="f2fa2-115">Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret en samling af salgsordrer, der har de indstillinger, der er beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="f2fa2-116">Oprette salgsordre 1 og 2</span><span class="sxs-lookup"><span data-stu-id="f2fa2-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="f2fa2-117">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f2fa2-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f2fa2-118">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f2fa2-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f2fa2-119">**Pulje:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="f2fa2-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="f2fa2-120">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f2fa2-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f2fa2-121">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="f2fa2-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f2fa2-122">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f2fa2-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f2fa2-123">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="f2fa2-124">Oprette salgsordre 3 og 4</span><span class="sxs-lookup"><span data-stu-id="f2fa2-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="f2fa2-125">Opret to identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f2fa2-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f2fa2-126">**Debitorkonto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f2fa2-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f2fa2-127">**Pulje:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="f2fa2-128">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="f2fa2-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f2fa2-129">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="f2fa2-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f2fa2-130">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f2fa2-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f2fa2-131">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="f2fa2-132">Frigive ordrerne til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="f2fa2-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="f2fa2-133">Udfør følgende trin for at frigive hver salgsordre, du har oprettet i dette scenarie, til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="f2fa2-134">Gå til **Debitor \> Ordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f2fa2-135">Find og vælg den salgsordre, der skal frigives.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="f2fa2-136">I handlingsruden skal du på fanen **Lagersted** vælge **Handlinger \> Frigiv til lagersted** for at at frigive den valgte salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="f2fa2-137">Gentag denne procedure for hver anden salgsordre, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="f2fa2-138">Konsolider forsendelser</span><span class="sxs-lookup"><span data-stu-id="f2fa2-138">Consolidate shipments</span></span>

1. <span data-ttu-id="f2fa2-139">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="f2fa2-140">Find og vælg en forsendelse, der blev oprettet, da salgsordre 1 blev frigivet på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="f2fa2-141">(Dens felt **Politik for forsendelseskonsolidering** skal angives til *Ordrepulje*.)</span><span class="sxs-lookup"><span data-stu-id="f2fa2-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="f2fa2-142">I handlingsruden skal du på fanen **Forsendelser** vælge **Forsendelser \> Konsolider forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="f2fa2-143">Kontrollér de forsendelser, der foreslås til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="f2fa2-144">Der bør kun foreslås én forsendelse, der har samme politik, til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="f2fa2-145">Luk siden **Forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="f2fa2-146">Find og vælg en forsendelse, der blev oprettet, da salgsordre 3 blev frigivet på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="f2fa2-147">(Dens felt **Politik for forsendelseskonsolidering** skal angives til *Standard*.)</span><span class="sxs-lookup"><span data-stu-id="f2fa2-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="f2fa2-148">I handlingsruden skal du på fanen **Forsendelser** vælge **Forsendelser \> Konsolider forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="f2fa2-149">Kontrollér, at ingen forsendelser er blevet foreslået til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="f2fa2-150">Vælg **Vis filtre**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="f2fa2-151">I ruden **Filtre** skal du du fjerne filtret **Ordrenummer** og derefter vælge **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="f2fa2-152">Kontrollér de forsendelser, der foreslås til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="f2fa2-153">Der bør kun foreslås én forsendelse, der har samme politik, til konsolidering.</span><span class="sxs-lookup"><span data-stu-id="f2fa2-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2fa2-154">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f2fa2-154">Additional resources</span></span>

- [<span data-ttu-id="f2fa2-155">Forsendelseskonsolideringspolitikker</span><span class="sxs-lookup"><span data-stu-id="f2fa2-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="f2fa2-156">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="f2fa2-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)