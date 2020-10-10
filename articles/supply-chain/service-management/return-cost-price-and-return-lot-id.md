---
title: Returkostpris og returparti-id
description: I visse tilfælde ønsker du muligvis, at kostprisen for de returnerede produkter er lig med kostprisen for produkterne på det tidspunkt, da du solgte produkterne til kunden. Du kan gøre dette ved hjælp af **Returparti-id**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6206dea0665d479ce8dc6a7526a85414296e6935
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830398"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="94f0a-104">Returkostpris og returparti-id</span><span class="sxs-lookup"><span data-stu-id="94f0a-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="94f0a-105">De kostpriser for produkter, der returneres til lageret, beregnes ved hjælp af de aktuelle kostpriser for produkterne.</span><span class="sxs-lookup"><span data-stu-id="94f0a-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="94f0a-106">I visse tilfælde ønsker du, at kostprisen for de returnerede produkter er lig med kostprisen for produkterne på det tidspunkt, da du solgte produkterne til kunden.</span><span class="sxs-lookup"><span data-stu-id="94f0a-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="94f0a-107">Du kan gøre dette ved hjælp af feltet **Returparti-id** i oversigtspanelet **Linjedetaljer** i formularen **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="94f0a-108">Overvej f.eks. følgende scenario.</span><span class="sxs-lookup"><span data-stu-id="94f0a-108">For example, consider the following scenario.</span></span> <span data-ttu-id="94f0a-109">Du fakturerer en kunde.</span><span class="sxs-lookup"><span data-stu-id="94f0a-109">You invoice a customer.</span></span> <span data-ttu-id="94f0a-110">Kunden returnerer derefter de leverede produkter til dig.</span><span class="sxs-lookup"><span data-stu-id="94f0a-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="94f0a-111">Du returnerer produkterne til lageret.</span><span class="sxs-lookup"><span data-stu-id="94f0a-111">You return the products to stock.</span></span> <span data-ttu-id="94f0a-112">Når du krediterer kunden for de returnerede produkter, beregnes kostpriserne for de pågældende produkter i dette tilfælde ved hjælp af de aktuelle kostpriser for produkterne.</span><span class="sxs-lookup"><span data-stu-id="94f0a-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="94f0a-113">Men hvis du bruger feltet **Returparti-id**, beregnes kostprisen for de returnerede produkter ved hjælp af kostprisen på fakturaen for det oprindelige salg til kunden.</span><span class="sxs-lookup"><span data-stu-id="94f0a-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="94f0a-114">Hvis du vil bruge en anden kostpris end den aktuelle kostpris for returvarer fra en kunde, skal du bruge en af følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="94f0a-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="94f0a-115">Metode 1: Angiv returkostprisen manuelt</span><span class="sxs-lookup"><span data-stu-id="94f0a-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="94f0a-116">Når du føjer varer til en returordre, returneres varerne som standard til lageret til den aktuelle kostpris.</span><span class="sxs-lookup"><span data-stu-id="94f0a-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="94f0a-117">Følg disse trin for at angive en anden returkostpris.</span><span class="sxs-lookup"><span data-stu-id="94f0a-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="94f0a-118">Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="94f0a-119">Klik på **Returordre** i gruppen **Ny** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="94f0a-120">I formularen **Opret returordre** skal du vælge en debitorkonto og derefter klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="94f0a-121">I formularen **Returordre - RMA-nummer: %1, %2** skal du markere en vare og derefter angive et negativ antal feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="94f0a-122">Klik på oversigtspanelet **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="94f0a-123">Angiv en værdi i feltet **Returkostpris** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="94f0a-124">Denne værdi bruges, når varerne returneres til lager.</span><span class="sxs-lookup"><span data-stu-id="94f0a-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="94f0a-125">Hvis du ikke angiver en værdi, bruges den aktuelle kostpris, når varerne returneres til lager.</span><span class="sxs-lookup"><span data-stu-id="94f0a-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="94f0a-126">Metode 2: Automatisk generere kostprisen på baggrund af debitorfakturalinjen</span><span class="sxs-lookup"><span data-stu-id="94f0a-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="94f0a-127">Dette er den foretrukne metode til at oprette returlinjer.</span><span class="sxs-lookup"><span data-stu-id="94f0a-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="94f0a-128">Hvis du vil bruge den kostpris for produkterne, der var aktuel på det tidspunkt, hvor du solgte produkterne til kunden, skal du oprette en returordre og angive en salgslinje, der skal returneres.</span><span class="sxs-lookup"><span data-stu-id="94f0a-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="94f0a-129">Klik på **Salg og marketing** \> **Generelt** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="94f0a-130">Klik på **Returordre** i gruppen **Ny** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="94f0a-131">I formularen **Opret returordre** skal du vælge en debitorkonto og derefter klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="94f0a-132">I formularen **Returordre - RMA-nummer: %1, %2** i **Handlingsrude** skal du klikke på **Find salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="94f0a-133">Vælg den fakturalinje, der skal returneres, i formularen **Find salgsordre**, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="94f0a-134">Værdien fra den oprindelige salgslinje vises i feltet **Returparti-id** under fanen **Generelt** i oversigtspanelet **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="94f0a-135">Desuden vises kostprisværdien fra den oprindelige salgslinje i feltet **Returkostpris**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="94f0a-136">Eksempel på beregning af kostpris</span><span class="sxs-lookup"><span data-stu-id="94f0a-136">Cost calculation example</span></span>

<span data-ttu-id="94f0a-137">Når du bruger feltet **Returvare-id** på en returordrelinje til at angive returkostprisen, bruges kostprisen på returordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="94f0a-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="94f0a-138">Hvis du kører funktionen til lagerlukning eller genberegning, justeres kostprisen på den oprindelige salgslinje.</span><span class="sxs-lookup"><span data-stu-id="94f0a-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="94f0a-139">Kostprisen på returordrelinjen justeres automatisk til at afspejle samme kostpris pr. styk.</span><span class="sxs-lookup"><span data-stu-id="94f0a-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="94f0a-140">Opret og frigiv et produkt, der kaldes Test.</span><span class="sxs-lookup"><span data-stu-id="94f0a-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="94f0a-141">I formularen **Frigivne produktdetaljer** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="94f0a-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="94f0a-142">På oversigtspanelet **Administrer omkostninger** skal du i feltet **Varegruppe** vælge gruppen **Dele**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="94f0a-143">I oversigtspanelet **Generelt** i feltet **Varemodelgruppe** skal du vælge **DEF**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="94f0a-144">Angiv 10,00 som varens kostpris i feltet **Pris** i oversigtspanelet **Køb**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="94f0a-145">Klik på **Dimensionsgrupper** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="94f0a-146">I feltet **Lagringsdimensionsgruppe** skal du vælge **Kun lokation og lagersted**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="94f0a-147">I feltet **Sporingsdimensionsgruppe** skal du vælge **Ingen aktive sporingsdimensioner**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="94f0a-148">Opret en indkøbsordre på 10 stk. af testvaren til 6,00 pr. stk., og bogfør derefter en faktura for indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="94f0a-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="94f0a-149">Opret en anden indkøbsordre på 10 stk. af testvaren til 8,00 pr. stk., og bogfør derefter en faktura for indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="94f0a-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="94f0a-150">Bogfør en faktura for en salgsordre for at sælge fem stk. af testvaren.</span><span class="sxs-lookup"><span data-stu-id="94f0a-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="94f0a-151">I dette tilfælde er salgsordrelinjen efterkalkuleret til 35,00 (5 stk. \* 7,00, som er den gennemsnitlige kostpris pr. stk.).</span><span class="sxs-lookup"><span data-stu-id="94f0a-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="94f0a-152">Opret en returordre for debitoren.</span><span class="sxs-lookup"><span data-stu-id="94f0a-152">Create a return order for the customer.</span></span> <span data-ttu-id="94f0a-153">Vælg fakturalinjen i formularen **Find salgsordre**, og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="94f0a-154">I formularen **Returordre - RMA-nummer: %1, %2** skal du kontrollere, at der genereres en returordre for at returnere testvaren.</span><span class="sxs-lookup"><span data-stu-id="94f0a-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="94f0a-155">Antallet på returordren er angivet til -5,00.</span><span class="sxs-lookup"><span data-stu-id="94f0a-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="94f0a-156">Feltet **Returparti-id** viser et parti-id.</span><span class="sxs-lookup"><span data-stu-id="94f0a-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="94f0a-157">Dette parti-id er hentet fra den oprindelige salgsordre for den vare, der blev solgt til kunden.</span><span class="sxs-lookup"><span data-stu-id="94f0a-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="94f0a-158">Kostprisværdien fra den oprindelige salgslinje vises i feltet **Returkostpris**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="94f0a-159">Registrer modtagelsen af de returnerede varer.</span><span class="sxs-lookup"><span data-stu-id="94f0a-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="94f0a-160">Bogfør en følgeseddel for de returnerede varer.</span><span class="sxs-lookup"><span data-stu-id="94f0a-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="94f0a-161">Bogfør en faktura for returordren.</span><span class="sxs-lookup"><span data-stu-id="94f0a-161">Post an invoice for the return order.</span></span> <span data-ttu-id="94f0a-162">Vælg en salgsordre, hvor ordretypen er **Returordre**, på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="94f0a-163">Åbn formularen **Lagertransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="94f0a-164">Kontrollér, at returneringen efterkalkuleres til 7,00 pr. stk. ved hjælp af værdien i feltet **Returkostpris**, så totalen er 35,00 i feltet **Kostbeløb**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="94f0a-165">Du kan åbne formularen **Lagertransaktioner** fra formularen **Returordre - RMA-nummer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="94f0a-166">Klik på **Lager** \> **Transaktioner** i gitteret **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="94f0a-167">I Lager- og lokalitetsstyring skal du bruge formularen **Lukning og regulering** til at køre proceduren **3. Luk**.</span><span class="sxs-lookup"><span data-stu-id="94f0a-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="94f0a-168">Denne handling justerer kostprisen på den oprindelige salgslinje, som blev efterkalkuleret fra -35,00 (5 stk. \* 7,00) til -30,00 (5 stk. \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="94f0a-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="94f0a-169">Dette skyldes, at lagermodelgruppen bruger FIFO (First In, First Out), og 6,00 pr. stk. er FIFO-kostprisen fra den første indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="94f0a-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="94f0a-170">Desuden justerer handlingen kostprisen på retursalgslinjen, så den svarer til kostprisen pr. stk. på den oprindelige salgslinje.</span><span class="sxs-lookup"><span data-stu-id="94f0a-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="94f0a-171">Kostprisen på returlinjen justeres derfor fra 35,00 til 30,00.</span><span class="sxs-lookup"><span data-stu-id="94f0a-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




