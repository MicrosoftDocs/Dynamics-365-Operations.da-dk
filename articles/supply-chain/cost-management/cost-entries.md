---
title: Omkostningsposter
description: "Denne artikel indeholder oplysninger om omkostningsposter, og hvornår de er oprettet. En omkostningspost er en post, der registrerer antallet og omkostningen for en given hændelse."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d8a443d03f8eb2d6ff44d869964b47b6569ce4c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="cost-entries"></a><span data-ttu-id="b9364-104">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b9364-104">Cost entries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b9364-105">Denne artikel indeholder oplysninger om omkostningsposter, og hvornår de er oprettet.</span><span class="sxs-lookup"><span data-stu-id="b9364-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="b9364-106">En omkostningspost er en post, der registrerer antallet og omkostningen for en given hændelse.</span><span class="sxs-lookup"><span data-stu-id="b9364-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="b9364-107">Omkostningsposter er akkumuleringer af lagertransaktioner, der er registreret på aktive økonomiske lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="b9364-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="b9364-108">Eksempler</span><span class="sxs-lookup"><span data-stu-id="b9364-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="b9364-109">Eksempel 1: Der er ikke oprettet omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b9364-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="b9364-110">Der er registreret en overførselsjournalhændelse.</span><span class="sxs-lookup"><span data-stu-id="b9364-110">A transfer journal event is registered.</span></span> <span data-ttu-id="b9364-111">Hændelsen overfører et eksemplar af vare A fra lokalitet A til lokalitet B. Lagerdimensionens lokalitet betragtes ikke som en del af omkostningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="b9364-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="b9364-112">Hændelsen opretter derfor to lagerposteringer og ingen omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="b9364-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="b9364-113">Eksempel 2: Der er oprettet omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b9364-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="b9364-114">Der er registreret en overførselsjournalhændelse.</span><span class="sxs-lookup"><span data-stu-id="b9364-114">A transfer journal event is registered.</span></span> <span data-ttu-id="b9364-115">Hændelsen overfører ét eksemplar af vare A fra websted 1 til websted 2.</span><span class="sxs-lookup"><span data-stu-id="b9364-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="b9364-116">Lagerdimensionen for lokationen betragtes som en del af omkostningsobjektet.</span><span class="sxs-lookup"><span data-stu-id="b9364-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="b9364-117">Hændelsen opretter derfor to lagerposteringer og to omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="b9364-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="b9364-118">Eksempel 3: Der oprettes én omkostningspost</span><span class="sxs-lookup"><span data-stu-id="b9364-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="b9364-119">Hændelsens produktkvittering registreres for en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="b9364-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="b9364-120">Hændelsen registrerer 100 styk af vare A til en enhedsomkostning på 10,00 amerikanske dollar (USD).</span><span class="sxs-lookup"><span data-stu-id="b9364-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="b9364-121">Da vare A bruger et serienummer til at spore formålet med lagerstyring, oprettes der et entydigt serienummer for hver vare, der modtages.</span><span class="sxs-lookup"><span data-stu-id="b9364-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="b9364-122">Hændelsen opretter derfor 100 lagerposteringer og én omkostningspost.</span><span class="sxs-lookup"><span data-stu-id="b9364-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="b9364-123">Siden Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b9364-123">Cost entries page</span></span>
<span data-ttu-id="b9364-124">På den nye side **Omkostningsposter** kan du få vist og styre registreringer af mængder og omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b9364-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="b9364-125">Siden supplerer siderne **Lagertransaktion** og **Lagerudligning**.</span><span class="sxs-lookup"><span data-stu-id="b9364-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="b9364-126">Poster registreres i kronologisk rækkefølge for en hændelse.</span><span class="sxs-lookup"><span data-stu-id="b9364-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="b9364-127">Derfor kan du hurtigt finde og styre de akkumulerede omkostninger for en bestemt hændelse eller alle hændelser, der er relateret til et dokument.</span><span class="sxs-lookup"><span data-stu-id="b9364-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="b9364-128">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="b9364-128">Here is an example:</span></span>

-   <span data-ttu-id="b9364-129">En produktkvitteringshændelsen er registreret for vare A. Et hundrede stykker er modtaget til en enhedskostpris på USD 10,00.</span><span class="sxs-lookup"><span data-stu-id="b9364-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="b9364-130">Et par dage efter, at fakturahændelsen er registreret, stiger omkostningen til 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="b9364-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="b9364-131">Det samlede beløb er derfor 1.100 USD.</span><span class="sxs-lookup"><span data-stu-id="b9364-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="b9364-132">Der oprettes endnu et bilag for at tage højde for forskellen på 100 USD.</span><span class="sxs-lookup"><span data-stu-id="b9364-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="b9364-133">Et par dage senere registreres et tillæg på 15,00 USD til dækning af transportomkostningerne på indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="b9364-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="b9364-134">Bilag</span><span class="sxs-lookup"><span data-stu-id="b9364-134">Voucher</span></span> | <span data-ttu-id="b9364-135">Dato</span><span class="sxs-lookup"><span data-stu-id="b9364-135">Date</span></span>       | <span data-ttu-id="b9364-136">Reference</span><span class="sxs-lookup"><span data-stu-id="b9364-136">Reference</span></span>      | <span data-ttu-id="b9364-137">Tal</span><span class="sxs-lookup"><span data-stu-id="b9364-137">Number</span></span> | <span data-ttu-id="b9364-138">Parti-id</span><span class="sxs-lookup"><span data-stu-id="b9364-138">Lot ID</span></span>  | <span data-ttu-id="b9364-139">Mængde</span><span class="sxs-lookup"><span data-stu-id="b9364-139">Quantity</span></span> | <span data-ttu-id="b9364-140">Beløb</span><span class="sxs-lookup"><span data-stu-id="b9364-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="b9364-141">00001</span><span class="sxs-lookup"><span data-stu-id="b9364-141">00001</span></span>   | <span data-ttu-id="b9364-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="b9364-142">01-01-2015</span></span> | <span data-ttu-id="b9364-143">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="b9364-143">Purchase order</span></span> | <span data-ttu-id="b9364-144">100001</span><span class="sxs-lookup"><span data-stu-id="b9364-144">100001</span></span> | <span data-ttu-id="b9364-145">0000101</span><span class="sxs-lookup"><span data-stu-id="b9364-145">0000101</span></span> | <span data-ttu-id="b9364-146">100,00</span><span class="sxs-lookup"><span data-stu-id="b9364-146">100.00</span></span>   | <span data-ttu-id="b9364-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="b9364-147">1000.00</span></span> |
| <span data-ttu-id="b9364-148">00002</span><span class="sxs-lookup"><span data-stu-id="b9364-148">00002</span></span>   | <span data-ttu-id="b9364-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="b9364-149">20-01-2015</span></span> | <span data-ttu-id="b9364-150">Indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="b9364-150">Purchase order</span></span> | <span data-ttu-id="b9364-151">100001</span><span class="sxs-lookup"><span data-stu-id="b9364-151">100001</span></span> | <span data-ttu-id="b9364-152">0000101</span><span class="sxs-lookup"><span data-stu-id="b9364-152">0000101</span></span> |          | <span data-ttu-id="b9364-153">100,00</span><span class="sxs-lookup"><span data-stu-id="b9364-153">100.00</span></span>  |
| <span data-ttu-id="b9364-154">00003</span><span class="sxs-lookup"><span data-stu-id="b9364-154">00003</span></span>   | <span data-ttu-id="b9364-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="b9364-155">31-01-2015</span></span> | <span data-ttu-id="b9364-156">Tilpasning</span><span class="sxs-lookup"><span data-stu-id="b9364-156">Adjustment</span></span>     | <span data-ttu-id="b9364-157">100001</span><span class="sxs-lookup"><span data-stu-id="b9364-157">100001</span></span> | <span data-ttu-id="b9364-158">0000101</span><span class="sxs-lookup"><span data-stu-id="b9364-158">0000101</span></span> |          | <span data-ttu-id="b9364-159">15,00</span><span class="sxs-lookup"><span data-stu-id="b9364-159">15.00</span></span>   |

<span data-ttu-id="b9364-160">Siden **Omkostningsposter** gør det muligt at filtrere efter dokument-id og dokumentdato.</span><span class="sxs-lookup"><span data-stu-id="b9364-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9364-161">Omkostningsposter er kun tilgængelige for [omkostningsobjekter](cost-object.md) eller frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="b9364-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="see-also"></a><span data-ttu-id="b9364-162">Se også</span><span class="sxs-lookup"><span data-stu-id="b9364-162">See also</span></span>
--------

[<span data-ttu-id="b9364-163">Omkostningsobjekter</span><span class="sxs-lookup"><span data-stu-id="b9364-163">Cost objects</span></span>](cost-object.md)




