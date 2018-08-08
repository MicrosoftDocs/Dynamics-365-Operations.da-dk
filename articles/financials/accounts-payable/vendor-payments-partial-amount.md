---
title: "Kreditorbetalinger af et delvist beløb"
description: "Du kan somme tider skulle foretage en betaling, der er mindre end fakturabeløbet, til en kreditor. I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2644e0a27eff3e45ddcddb89c9aac9230190788f
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="4446c-104">Kreditorbetalinger af et delvist beløb</span><span class="sxs-lookup"><span data-stu-id="4446c-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4446c-105">Du kan somme tider skulle foretage en betaling, der er mindre end fakturabeløbet, til en kreditor.</span><span class="sxs-lookup"><span data-stu-id="4446c-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="4446c-106">I denne artikel beskrives de forskellige indstillinger til håndtering af denne situation.</span><span class="sxs-lookup"><span data-stu-id="4446c-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="4446c-107">De tilgængelige indstillinger afhænger af forretningsbehovene og konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4446c-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="4446c-108">Kasserabatbeløb</span><span class="sxs-lookup"><span data-stu-id="4446c-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="4446c-109">En kreditor kan tilbyde dig en kasserabat, hvis du betaler en faktura før forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="4446c-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="4446c-110">Du kan f.eks. en oprette en faktura på 100,00, der specificerer en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage.</span><span class="sxs-lookup"><span data-stu-id="4446c-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="4446c-111">Forfaldsdatoen er 30 dage.</span><span class="sxs-lookup"><span data-stu-id="4446c-111">The due date terms are 30 days.</span></span> <span data-ttu-id="4446c-112">Hvis et betalingsforslag bruger kasserabatten som et kriterium for at vælge en faktura, og hvis forslaget køres på eller før datoen for kasserabat, udvælges fakturaen til betaling, og der oprettes betalingen af 98,00.</span><span class="sxs-lookup"><span data-stu-id="4446c-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="4446c-113">En kasserabat kan også tages fra en engangsbetaling, der er oprettet manuelt.</span><span class="sxs-lookup"><span data-stu-id="4446c-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="4446c-114">Delvise betalinger med kasserabatter</span><span class="sxs-lookup"><span data-stu-id="4446c-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="4446c-115">Når du foretager en delvis betaling, har du måske til hensigt at foretage en yderligere delbetaling, så fakturaen udlignes helt.</span><span class="sxs-lookup"><span data-stu-id="4446c-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="4446c-116">For at medtage en kasserabat for en delbetaling skal du angive indstillingen **Beregn kasserabatter for delvise betalinger** til **Ja** på siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="4446c-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="4446c-117">Du modtager f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt.</span><span class="sxs-lookup"><span data-stu-id="4446c-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="4446c-118">Der er bogført en faktura på 100,00.</span><span class="sxs-lookup"><span data-stu-id="4446c-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="4446c-119">Hvis du foretager en betaling på 49,00 inden for 10 dage, angiver du en debitering på 49,00 i en betalingskladde.</span><span class="sxs-lookup"><span data-stu-id="4446c-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="4446c-120">Når du udligner den delvise betaling på siden **Udlign åbne posteringer**, vises **1,00** i feltet **Kasserabatbeløb, der skal medtages**.</span><span class="sxs-lookup"><span data-stu-id="4446c-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="4446c-121">Hvis du indtaster en delvis betaling og lader det fulde fakturabeløb stå i feltet **Beløb, der skal udlignes** beregnes feltet **Kasserabatbeløb, der skal medtages** automatisk, når posteringerne bogføres.</span><span class="sxs-lookup"><span data-stu-id="4446c-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="4446c-122">Kreditnotaer med kasserabatter</span><span class="sxs-lookup"><span data-stu-id="4446c-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="4446c-123">Du kan evt. returnere nogle af varerne på en faktura, hvorefter du modtager en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="4446c-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="4446c-124">Hvis der tidligere er medtaget en kasserabat på en original faktura, kan du fratrække værdien af rabatten og modtage en refundering på det rigtige beløb.</span><span class="sxs-lookup"><span data-stu-id="4446c-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="4446c-125">Hvis indstillingen **Beregn kasserabatter for kreditnotaer** er angivet til **Ja** på siden **Kreditorparametre**, beregnes rabatten automatisk for kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="4446c-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="4446c-126">Du modtager f.eks. en kasserabat på 2 %, hvis fakturaen betales inden for 10 dage efter, at den er udstedt.</span><span class="sxs-lookup"><span data-stu-id="4446c-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="4446c-127">Der er bogført en faktura på 100,00.</span><span class="sxs-lookup"><span data-stu-id="4446c-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="4446c-128">Hvis du returnerer varerne, og du modtager en kreditnota, kan du indtaste kreditnotaen for det fulde beløb for den oprindelige faktura 100,00 sammen med de 2 procent kasserabat, der er også defineret i kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="4446c-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="4446c-129">Når du ser en kreditnota på siden **Udlign transaktioner**, vises **98,00** i feltet **Beløb, der skal udlignes**, og **-2,00** vises i feltet **Kasserabatbeløb**.</span><span class="sxs-lookup"><span data-stu-id="4446c-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="4446c-130">Rabatbeløbet bogføres på en kasserabatkonto.</span><span class="sxs-lookup"><span data-stu-id="4446c-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="4446c-131">Overbetaling/underbetalingsbeløb</span><span class="sxs-lookup"><span data-stu-id="4446c-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="4446c-132">Du foretager eventuelt en delbetaling, hvor beløbet, der stadig skal udlignes, er meget lille.</span><span class="sxs-lookup"><span data-stu-id="4446c-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="4446c-133">For eksempel er kreditorfakturaen for 1.000,00, og du betaler 999.90.</span><span class="sxs-lookup"><span data-stu-id="4446c-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="4446c-134">Hvis det resterende beløb er mindre end det beløb, der er angiver for over- eller underbetalinger på siden **Kreditorparametre**, bogføres differencen automatisk på en overbetalings/underbetalingsfinanskonto.</span><span class="sxs-lookup"><span data-stu-id="4446c-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="4446c-135">Du kan finde flere oplysninger i [Oversigt over kreditorbetalinger](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4446c-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

