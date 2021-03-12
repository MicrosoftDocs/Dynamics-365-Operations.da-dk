---
title: Få mere end den beregnede rabat til en kreditorbetaling
description: Denne artikel fører dig gennem en situation, hvor en kasserabat anvendes for et beløb, der er større end den rabat, der oprindeligt blev brugt på fakturaen. Denne situation kan opstå, hvis en organisation har en aftale med leverandøren om at betale et mindre beløb på fakturaen.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ee74bad071d546724f6ffe336bbe3bdf47e2a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971897"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="87369-104">Få mere end den beregnede rabat til en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="87369-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87369-105">Denne artikel fører dig gennem en situation, hvor en kasserabat anvendes for et beløb, der er større end den rabat, der oprindeligt blev brugt på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="87369-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="87369-106">Denne situation kan opstå, hvis en organisation har en aftale med leverandøren om at betale et mindre beløb på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="87369-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="87369-107">Leverandøren 3051 giver Fabrikam en kasserabat på 4 %, hvis en faktura betales i løbet af syv dage.</span><span class="sxs-lookup"><span data-stu-id="87369-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="87369-108">Den 29. juni angiver April en faktura på 1.000,00.</span><span class="sxs-lookup"><span data-stu-id="87369-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="87369-109">Kreditoren tillader, at April medtager en rabat på 60,00 i stedet for standardrabatten på 40,00, der er tilgængelig for denne faktura.</span><span class="sxs-lookup"><span data-stu-id="87369-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="87369-110">April registrerer en engangsbetaling ved hjælp af kreditorbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="87369-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="87369-111">Hun angiver kreditoren for betalingen og åbner derefter siden **Udlign transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="87369-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="87369-112">Hun markerer fakturaen og ændrer værdien i feltet **Kasserabatbeløb** til **60,00**.</span><span class="sxs-lookup"><span data-stu-id="87369-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="87369-113">Foretag afmærkning</span><span class="sxs-lookup"><span data-stu-id="87369-113">Mark</span></span>     | <span data-ttu-id="87369-114">Anvend kasserabat</span><span class="sxs-lookup"><span data-stu-id="87369-114">Use cash discount</span></span> | <span data-ttu-id="87369-115">Bilag</span><span class="sxs-lookup"><span data-stu-id="87369-115">Voucher</span></span>   | <span data-ttu-id="87369-116">Konto</span><span class="sxs-lookup"><span data-stu-id="87369-116">Account</span></span> | <span data-ttu-id="87369-117">Dato</span><span class="sxs-lookup"><span data-stu-id="87369-117">Date</span></span>      | <span data-ttu-id="87369-118">Forfaldsdato</span><span class="sxs-lookup"><span data-stu-id="87369-118">Due date</span></span>  | <span data-ttu-id="87369-119">Faktura</span><span class="sxs-lookup"><span data-stu-id="87369-119">Invoice</span></span> | <span data-ttu-id="87369-120">Beløb i transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="87369-120">Amount in transaction currency</span></span> | <span data-ttu-id="87369-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="87369-121">Currency</span></span> | <span data-ttu-id="87369-122">Beløb, der skal udlignes</span><span class="sxs-lookup"><span data-stu-id="87369-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="87369-123">Markeret</span><span class="sxs-lookup"><span data-stu-id="87369-123">Selected</span></span> | <span data-ttu-id="87369-124">Almindelig</span><span class="sxs-lookup"><span data-stu-id="87369-124">Normal</span></span>            | <span data-ttu-id="87369-125">Fak-10040</span><span class="sxs-lookup"><span data-stu-id="87369-125">Inv-10040</span></span> | <span data-ttu-id="87369-126">3051</span><span class="sxs-lookup"><span data-stu-id="87369-126">3051</span></span>    | <span data-ttu-id="87369-127">29-6-2015</span><span class="sxs-lookup"><span data-stu-id="87369-127">6/29/2015</span></span> | <span data-ttu-id="87369-128">29-7-2015</span><span class="sxs-lookup"><span data-stu-id="87369-128">7/29/2015</span></span> | <span data-ttu-id="87369-129">10040</span><span class="sxs-lookup"><span data-stu-id="87369-129">10040</span></span>   | <span data-ttu-id="87369-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="87369-130">1,000.00</span></span>                       | <span data-ttu-id="87369-131">USD</span><span class="sxs-lookup"><span data-stu-id="87369-131">USD</span></span>      | <span data-ttu-id="87369-132">940,00</span><span class="sxs-lookup"><span data-stu-id="87369-132">940.00</span></span>           |

<span data-ttu-id="87369-133">Rabatoplysninger vises nederst på siden **Udlign transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="87369-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="87369-134">Kasserabatdato</span><span class="sxs-lookup"><span data-stu-id="87369-134">Cash discount date</span></span>           | <span data-ttu-id="87369-135">12-7-2015</span><span class="sxs-lookup"><span data-stu-id="87369-135">7/12/2015</span></span> |
| <span data-ttu-id="87369-136">Kasserabatbeløb</span><span class="sxs-lookup"><span data-stu-id="87369-136">Cash discount amount</span></span>         | <span data-ttu-id="87369-137">60,00</span><span class="sxs-lookup"><span data-stu-id="87369-137">60.00</span></span>     |
| <span data-ttu-id="87369-138">Anvend kasserabat</span><span class="sxs-lookup"><span data-stu-id="87369-138">Use cash discount</span></span>            | <span data-ttu-id="87369-139">Almindelig</span><span class="sxs-lookup"><span data-stu-id="87369-139">Normal</span></span>    |
| <span data-ttu-id="87369-140">Medtaget kasserabat</span><span class="sxs-lookup"><span data-stu-id="87369-140">Cash discount taken</span></span>          | <span data-ttu-id="87369-141">0,00</span><span class="sxs-lookup"><span data-stu-id="87369-141">0.00</span></span>      |
| <span data-ttu-id="87369-142">Kasserabatbeløb, der skal medtages</span><span class="sxs-lookup"><span data-stu-id="87369-142">Cash discount amount to take</span></span> | <span data-ttu-id="87369-143">60,00</span><span class="sxs-lookup"><span data-stu-id="87369-143">60.00</span></span>     |

<span data-ttu-id="87369-144">Derefter bogfører April betalingskladden.</span><span class="sxs-lookup"><span data-stu-id="87369-144">April posts the payment journal.</span></span> <span data-ttu-id="87369-145">Fakturaen udlignes fuldt ud med en betaling på 940,00 og en rabat på 60,00.</span><span class="sxs-lookup"><span data-stu-id="87369-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



