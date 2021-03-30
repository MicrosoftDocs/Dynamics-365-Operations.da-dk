---
title: Værdiregulering af valuta i et konsolideret regnskab
description: Dette emne beskriver, hvordan du revaluerer valuta i et konsolideret regnskab.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212223"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="5464f-103">Værdiregulering af valuta i et konsolideret regnskab</span><span class="sxs-lookup"><span data-stu-id="5464f-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5464f-104">Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt.</span><span class="sxs-lookup"><span data-stu-id="5464f-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="5464f-105">Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="5464f-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="5464f-106">Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene.</span><span class="sxs-lookup"><span data-stu-id="5464f-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="5464f-107">Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato.</span><span class="sxs-lookup"><span data-stu-id="5464f-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="5464f-108">Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.</span><span class="sxs-lookup"><span data-stu-id="5464f-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="5464f-109">Virksomhedsopsætning</span><span class="sxs-lookup"><span data-stu-id="5464f-109">Company setup</span></span>
-   <span data-ttu-id="5464f-110">**Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="5464f-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="5464f-111">**Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="5464f-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="5464f-112">**Realiseret gevinst** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="5464f-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="5464f-113">**Realiseret tab** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="5464f-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5464f-114">**Urealiseret gevinst** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="5464f-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5464f-115">**Urealiseret tab** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="5464f-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="5464f-116">Oprindelige posteringer</span><span class="sxs-lookup"><span data-stu-id="5464f-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="5464f-117">Indbetalingsposteringer i USMF</span><span class="sxs-lookup"><span data-stu-id="5464f-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="5464f-118">Dato</span><span class="sxs-lookup"><span data-stu-id="5464f-118">Date</span></span>       | <span data-ttu-id="5464f-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="5464f-119">Ledger account</span></span>               | <span data-ttu-id="5464f-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="5464f-120">Currency</span></span> | <span data-ttu-id="5464f-121">Beløb</span><span class="sxs-lookup"><span data-stu-id="5464f-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="5464f-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="5464f-122">10/11/2015</span></span> | <span data-ttu-id="5464f-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="5464f-123">110110 – Cash</span></span>                | <span data-ttu-id="5464f-124">USD</span><span class="sxs-lookup"><span data-stu-id="5464f-124">USD</span></span>      | <span data-ttu-id="5464f-125">500</span><span class="sxs-lookup"><span data-stu-id="5464f-125">500</span></span>    |
| <span data-ttu-id="5464f-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="5464f-126">10/11/2015</span></span> | <span data-ttu-id="5464f-127">130100 – Debitorer</span><span class="sxs-lookup"><span data-stu-id="5464f-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="5464f-128">USD</span><span class="sxs-lookup"><span data-stu-id="5464f-128">USD</span></span>      | <span data-ttu-id="5464f-129">-500</span><span class="sxs-lookup"><span data-stu-id="5464f-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="5464f-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="5464f-130">Exchange rates</span></span>

| <span data-ttu-id="5464f-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="5464f-131">From currency</span></span> | <span data-ttu-id="5464f-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="5464f-132">To currency</span></span> | <span data-ttu-id="5464f-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="5464f-133">Start date</span></span> | <span data-ttu-id="5464f-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="5464f-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="5464f-135">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-135">EUR</span></span>           | <span data-ttu-id="5464f-136">USD</span><span class="sxs-lookup"><span data-stu-id="5464f-136">USD</span></span>         | <span data-ttu-id="5464f-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="5464f-137">10/1/2015</span></span>  | <span data-ttu-id="5464f-138">200</span><span class="sxs-lookup"><span data-stu-id="5464f-138">200</span></span>           |
| <span data-ttu-id="5464f-139">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-139">EUR</span></span>           | <span data-ttu-id="5464f-140">USD</span><span class="sxs-lookup"><span data-stu-id="5464f-140">USD</span></span>         | <span data-ttu-id="5464f-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="5464f-141">11/1/2015</span></span>  | <span data-ttu-id="5464f-142">150</span><span class="sxs-lookup"><span data-stu-id="5464f-142">150</span></span>           |
| <span data-ttu-id="5464f-143">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-143">EUR</span></span>           | <span data-ttu-id="5464f-144">USD</span><span class="sxs-lookup"><span data-stu-id="5464f-144">USD</span></span>         | <span data-ttu-id="5464f-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="5464f-145">12/1/2012</span></span>  | <span data-ttu-id="5464f-146">100</span><span class="sxs-lookup"><span data-stu-id="5464f-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="5464f-147">Udføre konsolidering for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="5464f-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5464f-148">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="5464f-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="5464f-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="5464f-149">Ledger account</span></span> | <span data-ttu-id="5464f-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="5464f-150">Currency</span></span> | <span data-ttu-id="5464f-151">Beløb</span><span class="sxs-lookup"><span data-stu-id="5464f-151">Amount</span></span> | <span data-ttu-id="5464f-152">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="5464f-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="5464f-153">110110</span><span class="sxs-lookup"><span data-stu-id="5464f-153">110110</span></span>         | <span data-ttu-id="5464f-154">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-154">EUR</span></span>      | <span data-ttu-id="5464f-155">250</span><span class="sxs-lookup"><span data-stu-id="5464f-155">250</span></span>    | <span data-ttu-id="5464f-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="5464f-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="5464f-157">130100</span><span class="sxs-lookup"><span data-stu-id="5464f-157">130100</span></span>         | <span data-ttu-id="5464f-158">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-158">EUR</span></span>      | <span data-ttu-id="5464f-159">-250</span><span class="sxs-lookup"><span data-stu-id="5464f-159">-250</span></span>   | <span data-ttu-id="5464f-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="5464f-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="5464f-161">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="5464f-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5464f-162">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="5464f-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="5464f-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="5464f-163">Ledger account</span></span> | <span data-ttu-id="5464f-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="5464f-164">Currency</span></span> | <span data-ttu-id="5464f-165">Beløb</span><span class="sxs-lookup"><span data-stu-id="5464f-165">Amount</span></span>  | <span data-ttu-id="5464f-166">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="5464f-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="5464f-167">110110</span><span class="sxs-lookup"><span data-stu-id="5464f-167">110110</span></span>         | <span data-ttu-id="5464f-168">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-168">EUR</span></span>      | <span data-ttu-id="5464f-169">333,33</span><span class="sxs-lookup"><span data-stu-id="5464f-169">333.33</span></span>  | <span data-ttu-id="5464f-170">Oprindeligt beløb på 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="5464f-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="5464f-171">130100</span><span class="sxs-lookup"><span data-stu-id="5464f-171">130100</span></span>         | <span data-ttu-id="5464f-172">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-172">EUR</span></span>      | <span data-ttu-id="5464f-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="5464f-173">-333.33</span></span> | <span data-ttu-id="5464f-174">Oprindeligt beløb på -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="5464f-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="5464f-175">801400</span><span class="sxs-lookup"><span data-stu-id="5464f-175">801400</span></span>         | <span data-ttu-id="5464f-176">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-176">EUR</span></span>      | <span data-ttu-id="5464f-177">83,33</span><span class="sxs-lookup"><span data-stu-id="5464f-177">83.33</span></span>   | <span data-ttu-id="5464f-178">333,33-250</span><span class="sxs-lookup"><span data-stu-id="5464f-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="5464f-179">801600</span><span class="sxs-lookup"><span data-stu-id="5464f-179">801600</span></span>         | <span data-ttu-id="5464f-180">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-180">EUR</span></span>      | <span data-ttu-id="5464f-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="5464f-181">-83.33</span></span>  | <span data-ttu-id="5464f-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="5464f-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="5464f-183">Du vil se flere posteringer for rapporteringsvalutabeløbene.</span><span class="sxs-lookup"><span data-stu-id="5464f-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="5464f-184">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 31. december 2015</span><span class="sxs-lookup"><span data-stu-id="5464f-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5464f-185">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="5464f-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="5464f-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="5464f-186">Ledger account</span></span> | <span data-ttu-id="5464f-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="5464f-187">Currency</span></span> | <span data-ttu-id="5464f-188">Beløb</span><span class="sxs-lookup"><span data-stu-id="5464f-188">Amount</span></span>  | <span data-ttu-id="5464f-189">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="5464f-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="5464f-190">110110</span><span class="sxs-lookup"><span data-stu-id="5464f-190">110110</span></span>         | <span data-ttu-id="5464f-191">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-191">EUR</span></span>      | <span data-ttu-id="5464f-192">500,00</span><span class="sxs-lookup"><span data-stu-id="5464f-192">500.00</span></span>  | <span data-ttu-id="5464f-193">Oprindeligt beløb på 500 × 1 %</span><span class="sxs-lookup"><span data-stu-id="5464f-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="5464f-194">130100</span><span class="sxs-lookup"><span data-stu-id="5464f-194">130100</span></span>         | <span data-ttu-id="5464f-195">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-195">EUR</span></span>      | <span data-ttu-id="5464f-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="5464f-196">-500.00</span></span> | <span data-ttu-id="5464f-197">Oprindeligt beløb på -500 × 1</span><span class="sxs-lookup"><span data-stu-id="5464f-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="5464f-198">801400</span><span class="sxs-lookup"><span data-stu-id="5464f-198">801400</span></span>         | <span data-ttu-id="5464f-199">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-199">EUR</span></span>      | <span data-ttu-id="5464f-200">250</span><span class="sxs-lookup"><span data-stu-id="5464f-200">250</span></span>     | <span data-ttu-id="5464f-201">500-333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="5464f-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="5464f-202">801600</span><span class="sxs-lookup"><span data-stu-id="5464f-202">801600</span></span>         | <span data-ttu-id="5464f-203">EUR</span><span class="sxs-lookup"><span data-stu-id="5464f-203">EUR</span></span>      | <span data-ttu-id="5464f-204">-250</span><span class="sxs-lookup"><span data-stu-id="5464f-204">-250</span></span>    | <span data-ttu-id="5464f-205">-500 – (-333,33) = -166,67-166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="5464f-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]