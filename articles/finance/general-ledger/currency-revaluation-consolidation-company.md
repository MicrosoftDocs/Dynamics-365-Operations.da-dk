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
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014977"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="c8eec-103">Værdiregulering af valuta i et konsolideret regnskab</span><span class="sxs-lookup"><span data-stu-id="c8eec-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8eec-104">Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt.</span><span class="sxs-lookup"><span data-stu-id="c8eec-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="c8eec-105">Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="c8eec-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="c8eec-106">Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene.</span><span class="sxs-lookup"><span data-stu-id="c8eec-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="c8eec-107">Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato.</span><span class="sxs-lookup"><span data-stu-id="c8eec-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="c8eec-108">Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.</span><span class="sxs-lookup"><span data-stu-id="c8eec-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="c8eec-109">Virksomhedsopsætning</span><span class="sxs-lookup"><span data-stu-id="c8eec-109">Company setup</span></span>
-   <span data-ttu-id="c8eec-110">**Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="c8eec-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="c8eec-111">**Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="c8eec-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="c8eec-112">**Realiseret gevinst** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="c8eec-112">**Realized gain** – Ledger account 801500</span></span>
    -   <span data-ttu-id="c8eec-113">**Realiseret tab** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="c8eec-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="c8eec-114">**Urealiseret gevinst** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="c8eec-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="c8eec-115">**Urealiseret tab** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="c8eec-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="c8eec-116">Oprindelige posteringer</span><span class="sxs-lookup"><span data-stu-id="c8eec-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="c8eec-117">Indbetalingsposteringer i USMF</span><span class="sxs-lookup"><span data-stu-id="c8eec-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="c8eec-118">Dato</span><span class="sxs-lookup"><span data-stu-id="c8eec-118">Date</span></span>       | <span data-ttu-id="c8eec-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c8eec-119">Ledger account</span></span>               | <span data-ttu-id="c8eec-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="c8eec-120">Currency</span></span> | <span data-ttu-id="c8eec-121">Beløb</span><span class="sxs-lookup"><span data-stu-id="c8eec-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="c8eec-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-122">10/11/2015</span></span> | <span data-ttu-id="c8eec-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="c8eec-123">110110 – Cash</span></span>                | <span data-ttu-id="c8eec-124">USD</span><span class="sxs-lookup"><span data-stu-id="c8eec-124">USD</span></span>      | <span data-ttu-id="c8eec-125">500</span><span class="sxs-lookup"><span data-stu-id="c8eec-125">500</span></span>    |
| <span data-ttu-id="c8eec-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-126">10/11/2015</span></span> | <span data-ttu-id="c8eec-127">130100 – Debitorer</span><span class="sxs-lookup"><span data-stu-id="c8eec-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="c8eec-128">USD</span><span class="sxs-lookup"><span data-stu-id="c8eec-128">USD</span></span>      | <span data-ttu-id="c8eec-129">-500</span><span class="sxs-lookup"><span data-stu-id="c8eec-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="c8eec-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="c8eec-130">Exchange rates</span></span>

| <span data-ttu-id="c8eec-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="c8eec-131">From currency</span></span> | <span data-ttu-id="c8eec-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="c8eec-132">To currency</span></span> | <span data-ttu-id="c8eec-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="c8eec-133">Start date</span></span> | <span data-ttu-id="c8eec-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="c8eec-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="c8eec-135">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-135">EUR</span></span>           | <span data-ttu-id="c8eec-136">USD</span><span class="sxs-lookup"><span data-stu-id="c8eec-136">USD</span></span>         | <span data-ttu-id="c8eec-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-137">10/1/2015</span></span>  | <span data-ttu-id="c8eec-138">200</span><span class="sxs-lookup"><span data-stu-id="c8eec-138">200</span></span>           |
| <span data-ttu-id="c8eec-139">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-139">EUR</span></span>           | <span data-ttu-id="c8eec-140">USD</span><span class="sxs-lookup"><span data-stu-id="c8eec-140">USD</span></span>         | <span data-ttu-id="c8eec-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-141">11/1/2015</span></span>  | <span data-ttu-id="c8eec-142">150</span><span class="sxs-lookup"><span data-stu-id="c8eec-142">150</span></span>           |
| <span data-ttu-id="c8eec-143">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-143">EUR</span></span>           | <span data-ttu-id="c8eec-144">USD</span><span class="sxs-lookup"><span data-stu-id="c8eec-144">USD</span></span>         | <span data-ttu-id="c8eec-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="c8eec-145">12/1/2012</span></span>  | <span data-ttu-id="c8eec-146">100</span><span class="sxs-lookup"><span data-stu-id="c8eec-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="c8eec-147">Udføre konsolidering for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="c8eec-148">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="c8eec-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="c8eec-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c8eec-149">Ledger account</span></span> | <span data-ttu-id="c8eec-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="c8eec-150">Currency</span></span> | <span data-ttu-id="c8eec-151">Beløb</span><span class="sxs-lookup"><span data-stu-id="c8eec-151">Amount</span></span> | <span data-ttu-id="c8eec-152">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="c8eec-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="c8eec-153">110110</span><span class="sxs-lookup"><span data-stu-id="c8eec-153">110110</span></span>         | <span data-ttu-id="c8eec-154">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-154">EUR</span></span>      | <span data-ttu-id="c8eec-155">250</span><span class="sxs-lookup"><span data-stu-id="c8eec-155">250</span></span>    | <span data-ttu-id="c8eec-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="c8eec-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="c8eec-157">130100</span><span class="sxs-lookup"><span data-stu-id="c8eec-157">130100</span></span>         | <span data-ttu-id="c8eec-158">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-158">EUR</span></span>      | <span data-ttu-id="c8eec-159">-250</span><span class="sxs-lookup"><span data-stu-id="c8eec-159">-250</span></span>   | <span data-ttu-id="c8eec-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="c8eec-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="c8eec-161">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="c8eec-162">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="c8eec-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="c8eec-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c8eec-163">Ledger account</span></span> | <span data-ttu-id="c8eec-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="c8eec-164">Currency</span></span> | <span data-ttu-id="c8eec-165">Beløb</span><span class="sxs-lookup"><span data-stu-id="c8eec-165">Amount</span></span>  | <span data-ttu-id="c8eec-166">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="c8eec-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="c8eec-167">110110</span><span class="sxs-lookup"><span data-stu-id="c8eec-167">110110</span></span>         | <span data-ttu-id="c8eec-168">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-168">EUR</span></span>      | <span data-ttu-id="c8eec-169">333,33</span><span class="sxs-lookup"><span data-stu-id="c8eec-169">333.33</span></span>  | <span data-ttu-id="c8eec-170">Oprindeligt beløb på 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="c8eec-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="c8eec-171">130100</span><span class="sxs-lookup"><span data-stu-id="c8eec-171">130100</span></span>         | <span data-ttu-id="c8eec-172">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-172">EUR</span></span>      | <span data-ttu-id="c8eec-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="c8eec-173">-333.33</span></span> | <span data-ttu-id="c8eec-174">Oprindeligt beløb på -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="c8eec-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="c8eec-175">801400</span><span class="sxs-lookup"><span data-stu-id="c8eec-175">801400</span></span>         | <span data-ttu-id="c8eec-176">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-176">EUR</span></span>      | <span data-ttu-id="c8eec-177">83,33</span><span class="sxs-lookup"><span data-stu-id="c8eec-177">83.33</span></span>   | <span data-ttu-id="c8eec-178">333,33-250</span><span class="sxs-lookup"><span data-stu-id="c8eec-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="c8eec-179">801600</span><span class="sxs-lookup"><span data-stu-id="c8eec-179">801600</span></span>         | <span data-ttu-id="c8eec-180">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-180">EUR</span></span>      | <span data-ttu-id="c8eec-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="c8eec-181">-83.33</span></span>  | <span data-ttu-id="c8eec-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="c8eec-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="c8eec-183">Du vil se flere posteringer for rapporteringsvalutabeløbene.</span><span class="sxs-lookup"><span data-stu-id="c8eec-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="c8eec-184">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 31. december 2015</span><span class="sxs-lookup"><span data-stu-id="c8eec-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="c8eec-185">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="c8eec-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="c8eec-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c8eec-186">Ledger account</span></span> | <span data-ttu-id="c8eec-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="c8eec-187">Currency</span></span> | <span data-ttu-id="c8eec-188">Beløb</span><span class="sxs-lookup"><span data-stu-id="c8eec-188">Amount</span></span>  | <span data-ttu-id="c8eec-189">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="c8eec-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="c8eec-190">110110</span><span class="sxs-lookup"><span data-stu-id="c8eec-190">110110</span></span>         | <span data-ttu-id="c8eec-191">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-191">EUR</span></span>      | <span data-ttu-id="c8eec-192">500,00</span><span class="sxs-lookup"><span data-stu-id="c8eec-192">500.00</span></span>  | <span data-ttu-id="c8eec-193">Oprindeligt beløb på 500 × 1 %</span><span class="sxs-lookup"><span data-stu-id="c8eec-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="c8eec-194">130100</span><span class="sxs-lookup"><span data-stu-id="c8eec-194">130100</span></span>         | <span data-ttu-id="c8eec-195">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-195">EUR</span></span>      | <span data-ttu-id="c8eec-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="c8eec-196">-500.00</span></span> | <span data-ttu-id="c8eec-197">Oprindeligt beløb på -500 × 1</span><span class="sxs-lookup"><span data-stu-id="c8eec-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="c8eec-198">801400</span><span class="sxs-lookup"><span data-stu-id="c8eec-198">801400</span></span>         | <span data-ttu-id="c8eec-199">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-199">EUR</span></span>      | <span data-ttu-id="c8eec-200">250</span><span class="sxs-lookup"><span data-stu-id="c8eec-200">250</span></span>     | <span data-ttu-id="c8eec-201">500-333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="c8eec-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="c8eec-202">801600</span><span class="sxs-lookup"><span data-stu-id="c8eec-202">801600</span></span>         | <span data-ttu-id="c8eec-203">EUR</span><span class="sxs-lookup"><span data-stu-id="c8eec-203">EUR</span></span>      | <span data-ttu-id="c8eec-204">-250</span><span class="sxs-lookup"><span data-stu-id="c8eec-204">-250</span></span>    | <span data-ttu-id="c8eec-205">-500 – (-333,33) = -166,67-166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="c8eec-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





