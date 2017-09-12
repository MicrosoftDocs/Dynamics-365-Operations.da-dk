---
title: "Værdiregulering af valuta i et konsolideret regnskab"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="42ddc-102">Værdiregulering af valuta i et konsolideret regnskab</span><span class="sxs-lookup"><span data-stu-id="42ddc-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="42ddc-103">Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt.</span><span class="sxs-lookup"><span data-stu-id="42ddc-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="42ddc-104">Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="42ddc-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="42ddc-105">Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene.</span><span class="sxs-lookup"><span data-stu-id="42ddc-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="42ddc-106">Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato.</span><span class="sxs-lookup"><span data-stu-id="42ddc-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="42ddc-107">Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.</span><span class="sxs-lookup"><span data-stu-id="42ddc-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="42ddc-108">Virksomhedsopsætning</span><span class="sxs-lookup"><span data-stu-id="42ddc-108">Company setup</span></span>
-   <span data-ttu-id="42ddc-109">**Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="42ddc-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="42ddc-110">**Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="42ddc-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="42ddc-111">**Realiseret gevinst** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="42ddc-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="42ddc-112">**Realiseret tab** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="42ddc-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="42ddc-113">**Urealiseret gevinst** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="42ddc-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="42ddc-114">**Urealiseret tab** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="42ddc-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="42ddc-115">Oprindelige posteringer</span><span class="sxs-lookup"><span data-stu-id="42ddc-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="42ddc-116">Indbetalingsposteringer i USMF</span><span class="sxs-lookup"><span data-stu-id="42ddc-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="42ddc-117">Dato</span><span class="sxs-lookup"><span data-stu-id="42ddc-117">Date</span></span>       | <span data-ttu-id="42ddc-118">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="42ddc-118">Ledger account</span></span>               | <span data-ttu-id="42ddc-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="42ddc-119">Currency</span></span> | <span data-ttu-id="42ddc-120">Beløb</span><span class="sxs-lookup"><span data-stu-id="42ddc-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="42ddc-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-121">10/11/2015</span></span> | <span data-ttu-id="42ddc-122">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="42ddc-122">110110 – Cash</span></span>                | <span data-ttu-id="42ddc-123">USD</span><span class="sxs-lookup"><span data-stu-id="42ddc-123">USD</span></span>      | <span data-ttu-id="42ddc-124">500</span><span class="sxs-lookup"><span data-stu-id="42ddc-124">500</span></span>    |
| <span data-ttu-id="42ddc-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-125">10/11/2015</span></span> | <span data-ttu-id="42ddc-126">130100 – Debitorer</span><span class="sxs-lookup"><span data-stu-id="42ddc-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="42ddc-127">USD</span><span class="sxs-lookup"><span data-stu-id="42ddc-127">USD</span></span>      | <span data-ttu-id="42ddc-128">-500</span><span class="sxs-lookup"><span data-stu-id="42ddc-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="42ddc-129">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="42ddc-129">Exchange rates</span></span>
| <span data-ttu-id="42ddc-130">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="42ddc-130">From currency</span></span> | <span data-ttu-id="42ddc-131">Til valuta</span><span class="sxs-lookup"><span data-stu-id="42ddc-131">To currency</span></span> | <span data-ttu-id="42ddc-132">Startdato</span><span class="sxs-lookup"><span data-stu-id="42ddc-132">Start date</span></span> | <span data-ttu-id="42ddc-133">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="42ddc-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="42ddc-134">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-134">EUR</span></span>           | <span data-ttu-id="42ddc-135">USD</span><span class="sxs-lookup"><span data-stu-id="42ddc-135">USD</span></span>         | <span data-ttu-id="42ddc-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-136">10/1/2015</span></span>  | <span data-ttu-id="42ddc-137">200</span><span class="sxs-lookup"><span data-stu-id="42ddc-137">200</span></span>           |
| <span data-ttu-id="42ddc-138">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-138">EUR</span></span>           | <span data-ttu-id="42ddc-139">USD</span><span class="sxs-lookup"><span data-stu-id="42ddc-139">USD</span></span>         | <span data-ttu-id="42ddc-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-140">11/1/2015</span></span>  | <span data-ttu-id="42ddc-141">150</span><span class="sxs-lookup"><span data-stu-id="42ddc-141">150</span></span>           |
| <span data-ttu-id="42ddc-142">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-142">EUR</span></span>           | <span data-ttu-id="42ddc-143">USD</span><span class="sxs-lookup"><span data-stu-id="42ddc-143">USD</span></span>         | <span data-ttu-id="42ddc-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="42ddc-144">12/1/2012</span></span>  | <span data-ttu-id="42ddc-145">100</span><span class="sxs-lookup"><span data-stu-id="42ddc-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="42ddc-146">Udføre konsolidering for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="42ddc-147">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="42ddc-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="42ddc-148">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="42ddc-148">Ledger account</span></span> | <span data-ttu-id="42ddc-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="42ddc-149">Currency</span></span> | <span data-ttu-id="42ddc-150">Beløb</span><span class="sxs-lookup"><span data-stu-id="42ddc-150">Amount</span></span> | <span data-ttu-id="42ddc-151">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="42ddc-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="42ddc-152">110110</span><span class="sxs-lookup"><span data-stu-id="42ddc-152">110110</span></span>         | <span data-ttu-id="42ddc-153">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-153">EUR</span></span>      | <span data-ttu-id="42ddc-154">250</span><span class="sxs-lookup"><span data-stu-id="42ddc-154">250</span></span>    | <span data-ttu-id="42ddc-155">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="42ddc-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="42ddc-156">130100</span><span class="sxs-lookup"><span data-stu-id="42ddc-156">130100</span></span>         | <span data-ttu-id="42ddc-157">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-157">EUR</span></span>      | <span data-ttu-id="42ddc-158">-250</span><span class="sxs-lookup"><span data-stu-id="42ddc-158">-250</span></span>   | <span data-ttu-id="42ddc-159">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="42ddc-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="42ddc-160">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="42ddc-161">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="42ddc-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="42ddc-162">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="42ddc-162">Ledger account</span></span> | <span data-ttu-id="42ddc-163">Valuta</span><span class="sxs-lookup"><span data-stu-id="42ddc-163">Currency</span></span> | <span data-ttu-id="42ddc-164">Beløb</span><span class="sxs-lookup"><span data-stu-id="42ddc-164">Amount</span></span>  | <span data-ttu-id="42ddc-165">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="42ddc-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="42ddc-166">110110</span><span class="sxs-lookup"><span data-stu-id="42ddc-166">110110</span></span>         | <span data-ttu-id="42ddc-167">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-167">EUR</span></span>      | <span data-ttu-id="42ddc-168">333,33</span><span class="sxs-lookup"><span data-stu-id="42ddc-168">333.33</span></span>  | <span data-ttu-id="42ddc-169">Oprindeligt beløb på 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="42ddc-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="42ddc-170">130100</span><span class="sxs-lookup"><span data-stu-id="42ddc-170">130100</span></span>         | <span data-ttu-id="42ddc-171">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-171">EUR</span></span>      | <span data-ttu-id="42ddc-172">-333,33</span><span class="sxs-lookup"><span data-stu-id="42ddc-172">-333.33</span></span> | <span data-ttu-id="42ddc-173">Oprindeligt beløb på -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="42ddc-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="42ddc-174">801400</span><span class="sxs-lookup"><span data-stu-id="42ddc-174">801400</span></span>         | <span data-ttu-id="42ddc-175">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-175">EUR</span></span>      | <span data-ttu-id="42ddc-176">83,33</span><span class="sxs-lookup"><span data-stu-id="42ddc-176">83.33</span></span>   | <span data-ttu-id="42ddc-177">333,33-250</span><span class="sxs-lookup"><span data-stu-id="42ddc-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="42ddc-178">801600</span><span class="sxs-lookup"><span data-stu-id="42ddc-178">801600</span></span>         | <span data-ttu-id="42ddc-179">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-179">EUR</span></span>      | <span data-ttu-id="42ddc-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="42ddc-180">-83.33</span></span>  | <span data-ttu-id="42ddc-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="42ddc-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="42ddc-182">Du vil se flere posteringer for rapporteringsvalutabeløbene.</span><span class="sxs-lookup"><span data-stu-id="42ddc-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="42ddc-183">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 31. december 2015</span><span class="sxs-lookup"><span data-stu-id="42ddc-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="42ddc-184">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="42ddc-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="42ddc-185">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="42ddc-185">Ledger account</span></span> | <span data-ttu-id="42ddc-186">Valuta</span><span class="sxs-lookup"><span data-stu-id="42ddc-186">Currency</span></span> | <span data-ttu-id="42ddc-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="42ddc-187">Amount</span></span>  | <span data-ttu-id="42ddc-188">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="42ddc-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="42ddc-189">110110</span><span class="sxs-lookup"><span data-stu-id="42ddc-189">110110</span></span>         | <span data-ttu-id="42ddc-190">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-190">EUR</span></span>      | <span data-ttu-id="42ddc-191">500,00</span><span class="sxs-lookup"><span data-stu-id="42ddc-191">500.00</span></span>  | <span data-ttu-id="42ddc-192">Oprindeligt beløb på 500 × 1 %</span><span class="sxs-lookup"><span data-stu-id="42ddc-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="42ddc-193">130100</span><span class="sxs-lookup"><span data-stu-id="42ddc-193">130100</span></span>         | <span data-ttu-id="42ddc-194">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-194">EUR</span></span>      | <span data-ttu-id="42ddc-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="42ddc-195">-500.00</span></span> | <span data-ttu-id="42ddc-196">Oprindeligt beløb på -500 × 1</span><span class="sxs-lookup"><span data-stu-id="42ddc-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="42ddc-197">801400</span><span class="sxs-lookup"><span data-stu-id="42ddc-197">801400</span></span>         | <span data-ttu-id="42ddc-198">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-198">EUR</span></span>      | <span data-ttu-id="42ddc-199">250</span><span class="sxs-lookup"><span data-stu-id="42ddc-199">250</span></span>     | <span data-ttu-id="42ddc-200">500-333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="42ddc-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="42ddc-201">801600</span><span class="sxs-lookup"><span data-stu-id="42ddc-201">801600</span></span>         | <span data-ttu-id="42ddc-202">EUR</span><span class="sxs-lookup"><span data-stu-id="42ddc-202">EUR</span></span>      | <span data-ttu-id="42ddc-203">-250</span><span class="sxs-lookup"><span data-stu-id="42ddc-203">-250</span></span>    | <span data-ttu-id="42ddc-204">-500 – (-333,33) = -166,67-166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="42ddc-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






