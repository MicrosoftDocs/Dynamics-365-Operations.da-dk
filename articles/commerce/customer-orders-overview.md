---
title: Kundeordrer i Modern POS (MPOS)
description: Dette emne indeholder oplysninger om kundeordrer i Modern POS (MPOS). Kundeordrer kaldes også specialordrer. Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
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
ms.openlocfilehash: a6fdc7b8d7ad65c9e4bf1d3b932b62918dea6e77
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710253"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="289f8-105">Kundeordrer i Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="289f8-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="289f8-106">Dette emne indeholder oplysninger om kundeordrer i Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="289f8-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="289f8-107">Kundeordrer kaldes også specialordrer.</span><span class="sxs-lookup"><span data-stu-id="289f8-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="289f8-108">Emnet indeholder en beskrivelse af relaterede parametre og transaktionsflow.</span><span class="sxs-lookup"><span data-stu-id="289f8-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="289f8-109">Med et hav af tilgængelige kanaler i handelsverdenen giver mange detailhandlere mulighed for kundeordrer eller specialordrer for at opfylde forskellige produkt- og opfyldelseskrav.</span><span class="sxs-lookup"><span data-stu-id="289f8-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="289f8-110">Her er nogle typiske scenarier:</span><span class="sxs-lookup"><span data-stu-id="289f8-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="289f8-111">En kunde ønsker, at produkter skal leveres til en bestemt adresse på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="289f8-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="289f8-112">En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.</span><span class="sxs-lookup"><span data-stu-id="289f8-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="289f8-113">En kunde ønsker, at en anden afhenter de produkter, kunden har købt.</span><span class="sxs-lookup"><span data-stu-id="289f8-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="289f8-114">Detailhandlere kan også bruge kundeordrer til at minimere manglende salg, som ellers kan skyldes, at en vare midlertidigt ikke kan leveres, da varerne kan leveres eller afhentes på et andet tidspunkt eller sted.</span><span class="sxs-lookup"><span data-stu-id="289f8-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="289f8-115">Konfigurere kundeordrer</span><span class="sxs-lookup"><span data-stu-id="289f8-115">Set up customer orders</span></span>

<span data-ttu-id="289f8-116">Her er nogle af de parametre, der kan indstilles på siden **Handelsparametre**, for at definere, hvordan kundeordrer opfyldes:</span><span class="sxs-lookup"><span data-stu-id="289f8-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="289f8-117">**Standard indbetalingsprocent** – Angiv det beløb, som kunden skal betale som et depositum, før en ordre kan bekræftes.</span><span class="sxs-lookup"><span data-stu-id="289f8-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="289f8-118">Standardindbetalingsbeløbet beregnes som en procentdel af ordreværdien.</span><span class="sxs-lookup"><span data-stu-id="289f8-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="289f8-119">Afhængigt af rettigheder kan en tilknyttet butik muligvis overstyre beløbet ved hjælp af **Tilsidesæt depositum**.</span><span class="sxs-lookup"><span data-stu-id="289f8-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="289f8-120">**Annulleringsgebyrprocent** – Hvis et gebyr vil blive anvendt, når en kundeordre annulleres, skal du angive beløbet på dette gebyr.</span><span class="sxs-lookup"><span data-stu-id="289f8-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="289f8-121">**Kode for annulleringsgebyr** – Hvis et gebyr vil blive anvendt ved annullering af en kundeordre, afspejles dette gebyr under en gebyrkode på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="289f8-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="289f8-122">Brug denne parameter til at definere annulleringen af gebyrkoden.</span><span class="sxs-lookup"><span data-stu-id="289f8-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="289f8-123">**Kode for leveringsgebyr** – Detailhandlere kan opkræve et ekstra gebyr for levering af varer til en kunde.</span><span class="sxs-lookup"><span data-stu-id="289f8-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="289f8-124">Beløbet for dette leveringsgebyr afspejles under en gebyrkode på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="289f8-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="289f8-125">Brug denne parameter til at knytte leveringsgebyrkoden til forsendelsesgebyrer på kundeordren.</span><span class="sxs-lookup"><span data-stu-id="289f8-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="289f8-126">**Refunder forsendelsesgebyrer** – Angiv, om forsendelsesgebyrer, der er tilknyttet en kundeordre, kan refunderes.</span><span class="sxs-lookup"><span data-stu-id="289f8-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="289f8-127">**Maksimalt beløb uden godkendelse** – Hvis forsendelsesgebyrer kan tilbagebetales, skal du angive det maksimale forsendelsesgebyrbeløb, der kan tilbagebetales på tværs af returordrer.</span><span class="sxs-lookup"><span data-stu-id="289f8-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="289f8-128">Hvis dette beløb overskrides, kræves ledertilsidesættelse for at fortsætte med refusionen.</span><span class="sxs-lookup"><span data-stu-id="289f8-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="289f8-129">For at tage højde for følgende scenarier kan en tilbagebetaling af forsendelsesgebyrer overstige det beløb, der oprindeligt blev betalt:</span><span class="sxs-lookup"><span data-stu-id="289f8-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="289f8-130">Gebyrer anvendes på niveauet for salgsordrehovedet, og når et antal af en produktlinje returneres, kan den maksimale refusion af forsendelsesgebyrer, der er tilladt for produkterne og antallet, ikke bestemmes på måde, der fungerer for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="289f8-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="289f8-131">Forsendelsesgebyrer påløber for hver leveringsforekomst.</span><span class="sxs-lookup"><span data-stu-id="289f8-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="289f8-132">Hvis en kunde returnerer varer flere gange, og forhandlerens politik angiver, at forhandleren skal bære omkostningerne ved returforsendelsesgebyrer, bliver returforsendelsesgebyrerne højere end de faktiske forsendelsesgebyrer.</span><span class="sxs-lookup"><span data-stu-id="289f8-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    

## <a name="disable-option-to-pay-later"></a><span data-ttu-id="289f8-133">Deaktivere muligheden for at betale senere</span><span class="sxs-lookup"><span data-stu-id="289f8-133">Disable option to pay later</span></span>

<span data-ttu-id="289f8-134">I Commerce version 10.0.12 og nyere kan forhandlerne fjerne muligheden for at betale senere, når der oprettes en kundeordre i POS.</span><span class="sxs-lookup"><span data-stu-id="289f8-134">In Commerce version 10.0.12 and later, merchants can remove the option to pay later when a customer order is created at the POS.</span></span> <span data-ttu-id="289f8-135">Hvis du vil deaktivere indstillingen, skal du åbne **Funktionalitetsprofil** for den kanal, hvor betaling senere ikke er tilladt, og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="289f8-135">To disable the option, open the **Functionality profile** for the channel that paying later is not allowed in, and then select **Edit**.</span></span> <span data-ttu-id="289f8-136">Under fanen **Generelt** skal du vælge rullelisten for **Kræv betaling for opfyldelse**.</span><span class="sxs-lookup"><span data-stu-id="289f8-136">On the **General** tab, select the dropdown for **Require payment for fulfillment**.</span></span> <span data-ttu-id="289f8-137">Hvis betaling senere ikke skal være tilladt ved POS, skal du vælge **Kort påkrævet** og vælge **Gem**.</span><span class="sxs-lookup"><span data-stu-id="289f8-137">If paying later should not be allowed at the POS, select **Card required** and select **Save**.</span></span> <span data-ttu-id="289f8-138">Kør distributionsplanen **1070** for at synkronisere ændringen til kanalen.</span><span class="sxs-lookup"><span data-stu-id="289f8-138">Run the **1070** distribution schedule to synchronize this change to the channel.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="289f8-139">Transaktionsflow for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="289f8-139">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="289f8-140">Oprette en kundeordre i Modern POS</span><span class="sxs-lookup"><span data-stu-id="289f8-140">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="289f8-141">Føj en kunde til transaktionen.</span><span class="sxs-lookup"><span data-stu-id="289f8-141">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="289f8-142">Føj produkter til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="289f8-142">Add products to the cart.</span></span>
3. <span data-ttu-id="289f8-143">Klik på **Opret kundeordre**, og vælg derefter ordretypen.</span><span class="sxs-lookup"><span data-stu-id="289f8-143">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="289f8-144">Ordretypen kan enten være **Kundeordre** eller **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="289f8-144">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="289f8-145">Klik på **Afsendelse valgt** eller **Send alle** for at levere produkterne til en adresse på debitorkontoen, angive den ønskede afsendelsesdato og forsendelsesgebyrer.</span><span class="sxs-lookup"><span data-stu-id="289f8-145">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="289f8-146">Klik på **Afhent valgte** eller **Afhent alle** for at vælge produkter, der vil blive afhentet fra det aktuelle lager eller et andet lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="289f8-146">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="289f8-147">Opkræv indbetalingsbeløbet, hvis der kræves et depositum.</span><span class="sxs-lookup"><span data-stu-id="289f8-147">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="289f8-148">Rediger en eksisterende kundeordre</span><span class="sxs-lookup"><span data-stu-id="289f8-148">Edit an existing customer order</span></span>

1. <span data-ttu-id="289f8-149">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="289f8-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="289f8-150">Find og vælg den ordre, der skal redigeres.</span><span class="sxs-lookup"><span data-stu-id="289f8-150">Find and select the order to edit.</span></span> <span data-ttu-id="289f8-151">Klik på **Rediger** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="289f8-151">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="289f8-152">Afhente en ordre</span><span class="sxs-lookup"><span data-stu-id="289f8-152">Pick up an order</span></span>

1. <span data-ttu-id="289f8-153">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="289f8-153">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="289f8-154">Vælg den ordre, der skal afhentes.</span><span class="sxs-lookup"><span data-stu-id="289f8-154">Select the order to pick up.</span></span> <span data-ttu-id="289f8-155">Klik på **Pluk og pakning** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="289f8-155">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="289f8-156">Klik på **Afhent**.</span><span class="sxs-lookup"><span data-stu-id="289f8-156">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="289f8-157">Annullere en ordre</span><span class="sxs-lookup"><span data-stu-id="289f8-157">Cancel an order</span></span>

1. <span data-ttu-id="289f8-158">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="289f8-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="289f8-159">Vælg den ordre, der skal annulleres.</span><span class="sxs-lookup"><span data-stu-id="289f8-159">Select the order to cancel.</span></span> <span data-ttu-id="289f8-160">Klik på **Annuller** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="289f8-160">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="289f8-161">Oprette en returordre</span><span class="sxs-lookup"><span data-stu-id="289f8-161">Create a return order</span></span>

1. <span data-ttu-id="289f8-162">Klik på **Find en ordre** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="289f8-162">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="289f8-163">Vælg den ordre, der skal returneres, vælg fakturaen for ordren, og vælg derefter produktlinjen for den vare, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="289f8-163">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="289f8-164">Klik på **Returordre** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="289f8-164">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="289f8-165">Asynkront transaktionsflow for kundeordrer</span><span class="sxs-lookup"><span data-stu-id="289f8-165">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="289f8-166">Kundeordrer kan oprettes fra POS-klienten i enten synkron eller asynkron tilstand.</span><span class="sxs-lookup"><span data-stu-id="289f8-166">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="289f8-167">Aktivere kundeordrer, der skal oprettes i asynkron tilstand</span><span class="sxs-lookup"><span data-stu-id="289f8-167">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="289f8-168">Klik på **Retail og Commerce** &gt; **Konfiguration af kanal** &gt; **POS-opsætning** &gt; **POS-profil** &gt; **Funktionalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="289f8-168">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="289f8-169">I oversigtspanelet **Generelt** skal du vælge **Ja** for **Opret kundeordre i asynkron tilstand**.</span><span class="sxs-lookup"><span data-stu-id="289f8-169">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="289f8-170">Når indstillingen **Opret kundeordre i asynkron tilstand** er indstillet til **Ja**, oprettes kundeordrer altid i asynkron tilstand, også selvom Retail Transaction Service (RTS) er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="289f8-170">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="289f8-171">Hvis du vælger **Nej** for denne indstilling, oprettes kundeordrer altid i synkron tilstand ved hjælp af RTS.</span><span class="sxs-lookup"><span data-stu-id="289f8-171">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="289f8-172">Når kundeordrer oprettes i asynkron tilstand, hentes de og indsættes i Commerce af Pull-job (P).</span><span class="sxs-lookup"><span data-stu-id="289f8-172">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="289f8-173">De tilsvarende salgsordrer oprettes, når **Synkroniser ordrer** køres enten manuelt eller via en batchproces.</span><span class="sxs-lookup"><span data-stu-id="289f8-173">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="289f8-174">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="289f8-174">Additional resources</span></span>

[<span data-ttu-id="289f8-175">Hybride kundeordrer</span><span class="sxs-lookup"><span data-stu-id="289f8-175">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
