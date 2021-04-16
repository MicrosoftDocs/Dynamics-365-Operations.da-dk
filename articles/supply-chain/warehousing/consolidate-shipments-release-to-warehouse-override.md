---
title: Konsolider forsendelser, når politikken for forsendelseskonsolidering tilsidesættes fra siden Frigiv til lager
description: Dette emne viser et scenarie, hvor en eller flere salgslinjer skal frigives til lageret manuelt fra siden Frigiv til lager, og den systemdefinerede politik for forsendelseskonsolidering skal tilsidesættes før frigivelsen.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dcd619ad2906d4224966e2696712ed0e71886eb2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837483"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="a2495-103">Konsolider forsendelser, når politikken for forsendelseskonsolidering tilsidesættes fra siden Frigiv til lager</span><span class="sxs-lookup"><span data-stu-id="a2495-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2495-104">Dette emne viser et scenarie, hvor en eller flere salgslinjer skal frigives til lageret manuelt fra siden **Frigiv til lager**, og den systemdefinerede politik for forsendelseskonsolidering skal tilsidesættes før frigivelsen.</span><span class="sxs-lookup"><span data-stu-id="a2495-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="a2495-105">Der kræves muligvis en tilsidesættelse af politikken for forsendelseskonsolidering, hvis f.eks. en ordre, der ikke normalt konsolideres med åbne forsendelser, skal konsolideres med åbne forsendelser.</span><span class="sxs-lookup"><span data-stu-id="a2495-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="a2495-106">I løbet af scenariet opretter du et sæt salgsordrer og overskriver derefter standardpolitikken for konsolidering af forsendelser, før du frigiver ordrerne til lageret.</span><span class="sxs-lookup"><span data-stu-id="a2495-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="a2495-107">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="a2495-107">Make demo data available</span></span>

<span data-ttu-id="a2495-108">Scenariet i dette emne indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a2495-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a2495-109">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="a2495-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="a2495-110">Konfigurere politikker for forsendelseskonsolidering og produktfiltre</span><span class="sxs-lookup"><span data-stu-id="a2495-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="a2495-111">I det scenarie, der beskrives her, antages det, at du allerede har aktiveret funktionen, udført øvelserne til [Konfigurere politikker for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og oprettet de politikker og andre poster, der er beskrevet der.</span><span class="sxs-lookup"><span data-stu-id="a2495-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="a2495-112">Sørg for at udføre øvelserne, før du fortsætter med dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="a2495-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="a2495-113">Oprette salgsordrer til dette scenarie</span><span class="sxs-lookup"><span data-stu-id="a2495-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="a2495-114">Gå til **Debitor \> Ordrer \> Alle salgsordrer**, og opret tre identiske salgsordrer, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a2495-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a2495-115">**Debitorkonto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a2495-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a2495-116">Tilføj en ordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a2495-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a2495-117">**Varenummer:** *A0001* (en vare, der ikke er tildelt et **Kode 4**-filter)</span><span class="sxs-lookup"><span data-stu-id="a2495-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a2495-118">**Antal:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a2495-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a2495-119">Vælg **Lager \> Reservation**,og vælg derefter **Reserver parti** i handlingsruden for at reservere ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="a2495-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="a2495-120">Frigive salgsordrer fra siden Frigiv til lager</span><span class="sxs-lookup"><span data-stu-id="a2495-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="a2495-121">Udfør følgende trin for at tilsidesætte politikken for forsendelseskonsolidering under frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="a2495-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="a2495-122">Gå til **Lagerstyringssted \> Frigiv til lager \> Frigiv til lager**.</span><span class="sxs-lookup"><span data-stu-id="a2495-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="a2495-123">Vælg den første salgsordre, du har oprettet for dette scenarie, i den øverste rude.</span><span class="sxs-lookup"><span data-stu-id="a2495-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="a2495-124">Vælg **Tilføj** for at føje linjen til frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="a2495-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="a2495-125">Bemærk, at *standardpolitikken* for konsolidering af forsendelse anvendes i den nederste rude.</span><span class="sxs-lookup"><span data-stu-id="a2495-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="a2495-126">Vælg **Vælg ny politik for forsendelseskonsolidering** i nederste rude.</span><span class="sxs-lookup"><span data-stu-id="a2495-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="a2495-127">Vælg en politik, der giver mulighed for konsolidering med andre åbne forsendelser med samme politik.</span><span class="sxs-lookup"><span data-stu-id="a2495-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="a2495-128">Vælg f.eks politikken *Kundeordrenr.*.</span><span class="sxs-lookup"><span data-stu-id="a2495-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="a2495-129">Vælg **Frigiv til lager**.</span><span class="sxs-lookup"><span data-stu-id="a2495-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="a2495-130">Vælg den anden og tredje salgsordre, du har oprettet for dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="a2495-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="a2495-131">Vælg **Tilføj** for at føje linjerne til frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="a2495-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="a2495-132">Bemærk, at *standardpolitikken* anvendes i den nederste rude.</span><span class="sxs-lookup"><span data-stu-id="a2495-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="a2495-133">Vælg den anden linje, og vælg derefter **Kundeordrenr.** i feltet *Vælg ny politik for forsendelseskonsolidering*.</span><span class="sxs-lookup"><span data-stu-id="a2495-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="a2495-134">Vælg **Frigiv til lager** for begge linjer.</span><span class="sxs-lookup"><span data-stu-id="a2495-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="a2495-135">Kontrollér forsendelserne</span><span class="sxs-lookup"><span data-stu-id="a2495-135">Verify the shipments</span></span>

<span data-ttu-id="a2495-136">Der skal være oprettet to forsendelser:</span><span class="sxs-lookup"><span data-stu-id="a2495-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="a2495-137">Den første forsendelse indeholder to linjer og er oprettet ved hjælp af *Kundeordrenr.*-politikken for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="a2495-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="a2495-138">Den anden forsendelse indeholder én linjer og er oprettet ved hjælp af *standardpolitikken* for forsendelseskonsolidering.</span><span class="sxs-lookup"><span data-stu-id="a2495-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="a2495-139">Udfør følgende trin for at gennemse de forsendelser, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="a2495-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="a2495-140">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="a2495-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="a2495-141">Find og vælg den nødvendige forsendelse.</span><span class="sxs-lookup"><span data-stu-id="a2495-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="a2495-142">I feltet **Politik for forsendelseskonsolidering** kan du gennemse den konsolideringspolitik, der blev brugt ved oprettelsen af forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="a2495-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2495-143">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a2495-143">Additional resources</span></span>

- [<span data-ttu-id="a2495-144">Forsendelseskonsolideringspolitikker</span><span class="sxs-lookup"><span data-stu-id="a2495-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="a2495-145">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="a2495-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]