---
title: Kundeordrer i Retail Modern POS (MPOS)
description: Dette emne indeholder oplysninger om kundeordrer i Retail Modern POS (MPOS). Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b54f39cc7896871d77f9371e6197bf6dbaac51de
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553570"
---
# <a name="customer-orders-in-retail-modern-pos-mpos"></a><span data-ttu-id="81da5-105">Kundeordrer i Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="81da5-105">Customer orders in Retail Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81da5-106">Dette emne indeholder oplysninger om kundeordrer i Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="81da5-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="81da5-107">Kundeordrer kaldes også specialordrer.</span><span class="sxs-lookup"><span data-stu-id="81da5-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="81da5-108">Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.</span><span class="sxs-lookup"><span data-stu-id="81da5-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="81da5-109">Med et hav af tilgængelige kanaler i detailverdenen giver mange detailhandlere mulighed for kundeordrer eller specialordrer for at opfylde forskellige produkt- og opfyldelseskrav.</span><span class="sxs-lookup"><span data-stu-id="81da5-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="81da5-110">Her er nogle typiske scenarier:</span><span class="sxs-lookup"><span data-stu-id="81da5-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="81da5-111">En kunde ønsker, at produkter skal leveres til en bestemt adresse på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="81da5-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="81da5-112">En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.</span><span class="sxs-lookup"><span data-stu-id="81da5-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="81da5-113">En kunde ønsker, at en anden afhenter de produkter, kunden har købt.</span><span class="sxs-lookup"><span data-stu-id="81da5-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="81da5-114">Detailhandlere kan også bruge kundeordrer til at minimere manglende salg, som ellers kan skyldes, at en vare midlertidigt ikke kan leveres, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.</span><span class="sxs-lookup"><span data-stu-id="81da5-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="81da5-115">Konfigurere kundeordrer</span><span class="sxs-lookup"><span data-stu-id="81da5-115">Set up customer orders</span></span>

<span data-ttu-id="81da5-116">Her er nogle af de parametre, der kan indstilles på siden **Detailparametre**, for at definere, hvordan kundeordrer opfyldes:</span><span class="sxs-lookup"><span data-stu-id="81da5-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="81da5-117">**Standard indbetalingsprocent** – Angiv det beløb, som kunden skal betale som et depositum, før en ordre kan bekræftes.</span><span class="sxs-lookup"><span data-stu-id="81da5-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="81da5-118">Standardindbetalingsbeløbet beregnes som en procentdel af ordreværdien.</span><span class="sxs-lookup"><span data-stu-id="81da5-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="81da5-119">Afhængigt af rettigheder kan en tilknyttet butik muligvis overstyre beløbet ved hjælp af **Tilsidesæt depositum**.</span><span class="sxs-lookup"><span data-stu-id="81da5-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="81da5-120">**Annulleringsgebyrprocent** – Hvis et gebyr vil blive anvendt, når en kundeordre annulleres, skal du angive beløbet på dette gebyr.</span><span class="sxs-lookup"><span data-stu-id="81da5-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="81da5-121">**Kode for annulleringsgebyr** – Hvis et gebyr vil blive anvendt ved annullering af en kundeordre, afspejles dette gebyr under en gebyrkode på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="81da5-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="81da5-122">Brug denne parameter til at definere annulleringen af gebyrkoden.</span><span class="sxs-lookup"><span data-stu-id="81da5-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="81da5-123">**Kode for leveringsgebyr** – Detailhandlere kan opkræve et ekstra gebyr for levering af varer til en kunde.</span><span class="sxs-lookup"><span data-stu-id="81da5-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="81da5-124">Beløbet for dette leveringsgebyr afspejles under en gebyrkode på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="81da5-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="81da5-125">Brug denne parameter til at knytte leveringsgebyrkoden til forsendelsesgebyrer på kundeordren.</span><span class="sxs-lookup"><span data-stu-id="81da5-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="81da5-126">**Refunder forsendelsesgebyrer** – Angiv, om forsendelsesgebyrer, der er tilknyttet en kundeordre, kan refunderes.</span><span class="sxs-lookup"><span data-stu-id="81da5-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="81da5-127">**Maksimalt beløb uden godkendelse** – Hvis forsendelsesgebyrer kan tilbagebetales, skal du angive det maksimale forsendelsesgebyrbeløb, der kan tilbagebetales på tværs af returordrer.</span><span class="sxs-lookup"><span data-stu-id="81da5-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="81da5-128">Hvis dette beløb overskrides, kræves ledertilsidesættelse for at fortsætte med refusionen.</span><span class="sxs-lookup"><span data-stu-id="81da5-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="81da5-129">For at tage højde for følgende scenarier kan en tilbagebetaling af forsendelsesgebyrer overstige det beløb, der oprindeligt blev betalt:</span><span class="sxs-lookup"><span data-stu-id="81da5-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="81da5-130">Gebyrer anvendes på niveauet for salgsordrehovedet, og når et antal af en produktlinje returneres, kan den maksimale refusion af forsendelsesgebyrer, der er tilladt for produkterne og antallet, ikke bestemmes på måde, der fungerer for alle detailkunder.</span><span class="sxs-lookup"><span data-stu-id="81da5-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    - <span data-ttu-id="81da5-131">Forsendelsesgebyrer påløber for hver leveringsforekomst.</span><span class="sxs-lookup"><span data-stu-id="81da5-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="81da5-132">Hvis en kunde returnerer varer flere gange, og forhandlerens politik angiver, at forhandleren skal bære omkostningerne ved returforsendelsesgebyrer, bliver returforsendelsesgebyrerne højere end de faktiske forsendelsesgebyrer.</span><span class="sxs-lookup"><span data-stu-id="81da5-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="81da5-133">Transaktionsflow for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="81da5-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="81da5-134">Oprette en kundeordre i Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="81da5-134">Create a customer order in Retail Modern POS</span></span>

1. <span data-ttu-id="81da5-135">Føj en kunde til transaktionen.</span><span class="sxs-lookup"><span data-stu-id="81da5-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="81da5-136">Føj produkter til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="81da5-136">Add products to the cart.</span></span>
3. <span data-ttu-id="81da5-137">Klik på **Opret kundeordre**, og vælg derefter ordretypen.</span><span class="sxs-lookup"><span data-stu-id="81da5-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="81da5-138">Ordretypen kan enten være **Kundeordre** eller **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="81da5-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="81da5-139">Klik på **Afsendelse valgt** eller **Send alle** for at levere produkterne til en adresse på debitorkontoen, angive den ønskede afsendelsesdato og forsendelsesgebyrer.</span><span class="sxs-lookup"><span data-stu-id="81da5-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="81da5-140">Klik på **Afhent valgte** eller **Afhent alle** for at vælge produkter, der vil blive afhentet fra det aktuelle lager eller et andet lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="81da5-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="81da5-141">Opkræv indbetalingsbeløbet, hvis der kræves et depositum.</span><span class="sxs-lookup"><span data-stu-id="81da5-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="81da5-142">Rediger en eksisterende kundeordre</span><span class="sxs-lookup"><span data-stu-id="81da5-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="81da5-143">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="81da5-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="81da5-144">Find og vælg den ordre, der skal redigeres.</span><span class="sxs-lookup"><span data-stu-id="81da5-144">Find and select the order to edit.</span></span> <span data-ttu-id="81da5-145">Klik på **Rediger** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="81da5-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="81da5-146">Afhente en ordre</span><span class="sxs-lookup"><span data-stu-id="81da5-146">Pick up an order</span></span>

1. <span data-ttu-id="81da5-147">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="81da5-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="81da5-148">Vælg den ordre, der skal afhentes.</span><span class="sxs-lookup"><span data-stu-id="81da5-148">Select the order to pick up.</span></span> <span data-ttu-id="81da5-149">Klik på **Pluk og pakning** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="81da5-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="81da5-150">Klik på **Afhent**.</span><span class="sxs-lookup"><span data-stu-id="81da5-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="81da5-151">Annullere en ordre</span><span class="sxs-lookup"><span data-stu-id="81da5-151">Cancel an order</span></span>

1. <span data-ttu-id="81da5-152">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="81da5-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="81da5-153">Vælg den ordre, der skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="81da5-153">Select the order to cancel.</span></span> <span data-ttu-id="81da5-154">Klik på **Annuller** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="81da5-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="81da5-155">Oprette en returordre</span><span class="sxs-lookup"><span data-stu-id="81da5-155">Create a return order</span></span>

1. <span data-ttu-id="81da5-156">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="81da5-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="81da5-157">Vælg den ordre, der skal returneres, vælg fakturaen for ordren, og vælg derefter produktlinjen for den vare, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="81da5-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="81da5-158">Klik på **Returordre** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="81da5-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="81da5-159">Asynkront transaktionsflow for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="81da5-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="81da5-160">Kundeordrer kan oprettes fra POS-klienten i enten synkron eller asynkron tilstand.</span><span class="sxs-lookup"><span data-stu-id="81da5-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="81da5-161">Aktivere kundeordrer, der skal oprettes i asynkron tilstand</span><span class="sxs-lookup"><span data-stu-id="81da5-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="81da5-162">Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profiler** &gt; **Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="81da5-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="81da5-163">I oversigtspanelet **Generelt** skal du vælge **Ja** for **Opret kundeordre i asynkron tilstand**.</span><span class="sxs-lookup"><span data-stu-id="81da5-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="81da5-164">Når indstillingen **Opret kundeordre i asynkron tilstand** er indstillet til **Ja**, oprettes kundeordrer altid i asynkron tilstand, også selvom Retail Transaction Service (RTS) er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="81da5-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="81da5-165">Hvis du vælger **Nej** for denne indstilling, oprettes kundeordrer altid i synkron tilstand ved hjælp af RTS.</span><span class="sxs-lookup"><span data-stu-id="81da5-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="81da5-166">Når kundeordrer oprettes i asynkron tilstand, hentes de og indsættes i Retail af Pull-job (P).</span><span class="sxs-lookup"><span data-stu-id="81da5-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="81da5-167">De tilsvarende salgsordrer oprettes i Retail, når **Synkroniser ordrer** køres enten manuelt eller via en batchproces.</span><span class="sxs-lookup"><span data-stu-id="81da5-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81da5-168">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="81da5-168">Additional resources</span></span>

[<span data-ttu-id="81da5-169">Hybride kundeordrer</span><span class="sxs-lookup"><span data-stu-id="81da5-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
