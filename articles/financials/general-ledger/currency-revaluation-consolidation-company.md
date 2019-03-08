---
title: Værdiregulering af valuta i et konsolideret regnskab
description: Dette emne beskriver, hvordan du revaluerer valuta i et konsolideret regnskab.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "338745"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="f852b-103">Værdiregulering af valuta i et konsolideret regnskab</span><span class="sxs-lookup"><span data-stu-id="f852b-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f852b-104">Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt.</span><span class="sxs-lookup"><span data-stu-id="f852b-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="f852b-105">Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f852b-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="f852b-106">Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene.</span><span class="sxs-lookup"><span data-stu-id="f852b-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="f852b-107">Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato.</span><span class="sxs-lookup"><span data-stu-id="f852b-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="f852b-108">Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.</span><span class="sxs-lookup"><span data-stu-id="f852b-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="f852b-109">Virksomhedsopsætning</span><span class="sxs-lookup"><span data-stu-id="f852b-109">Company setup</span></span>
-   <span data-ttu-id="f852b-110">**Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="f852b-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="f852b-111">**Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="f852b-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="f852b-112">**Realiseret gevinst** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="f852b-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="f852b-113">**Realiseret tab** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="f852b-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f852b-114">**Urealiseret gevinst** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="f852b-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="f852b-115">**Urealiseret tab** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="f852b-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="f852b-116">Oprindelige posteringer</span><span class="sxs-lookup"><span data-stu-id="f852b-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="f852b-117">Indbetalingsposteringer i USMF</span><span class="sxs-lookup"><span data-stu-id="f852b-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="f852b-118">Dato</span><span class="sxs-lookup"><span data-stu-id="f852b-118">Date</span></span>       | <span data-ttu-id="f852b-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f852b-119">Ledger account</span></span>               | <span data-ttu-id="f852b-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="f852b-120">Currency</span></span> | <span data-ttu-id="f852b-121">Beløb</span><span class="sxs-lookup"><span data-stu-id="f852b-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="f852b-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="f852b-122">10/11/2015</span></span> | <span data-ttu-id="f852b-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="f852b-123">110110 – Cash</span></span>                | <span data-ttu-id="f852b-124">USD</span><span class="sxs-lookup"><span data-stu-id="f852b-124">USD</span></span>      | <span data-ttu-id="f852b-125">500</span><span class="sxs-lookup"><span data-stu-id="f852b-125">500</span></span>    |
| <span data-ttu-id="f852b-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="f852b-126">10/11/2015</span></span> | <span data-ttu-id="f852b-127">130100 – Debitorer</span><span class="sxs-lookup"><span data-stu-id="f852b-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="f852b-128">USD</span><span class="sxs-lookup"><span data-stu-id="f852b-128">USD</span></span>      | <span data-ttu-id="f852b-129">-500</span><span class="sxs-lookup"><span data-stu-id="f852b-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="f852b-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="f852b-130">Exchange rates</span></span>

| <span data-ttu-id="f852b-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="f852b-131">From currency</span></span> | <span data-ttu-id="f852b-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="f852b-132">To currency</span></span> | <span data-ttu-id="f852b-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="f852b-133">Start date</span></span> | <span data-ttu-id="f852b-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="f852b-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="f852b-135">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-135">EUR</span></span>           | <span data-ttu-id="f852b-136">USD</span><span class="sxs-lookup"><span data-stu-id="f852b-136">USD</span></span>         | <span data-ttu-id="f852b-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="f852b-137">10/1/2015</span></span>  | <span data-ttu-id="f852b-138">200</span><span class="sxs-lookup"><span data-stu-id="f852b-138">200</span></span>           |
| <span data-ttu-id="f852b-139">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-139">EUR</span></span>           | <span data-ttu-id="f852b-140">USD</span><span class="sxs-lookup"><span data-stu-id="f852b-140">USD</span></span>         | <span data-ttu-id="f852b-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="f852b-141">11/1/2015</span></span>  | <span data-ttu-id="f852b-142">150</span><span class="sxs-lookup"><span data-stu-id="f852b-142">150</span></span>           |
| <span data-ttu-id="f852b-143">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-143">EUR</span></span>           | <span data-ttu-id="f852b-144">USD</span><span class="sxs-lookup"><span data-stu-id="f852b-144">USD</span></span>         | <span data-ttu-id="f852b-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="f852b-145">12/1/2012</span></span>  | <span data-ttu-id="f852b-146">100</span><span class="sxs-lookup"><span data-stu-id="f852b-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="f852b-147">Udføre konsolidering for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="f852b-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f852b-148">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="f852b-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="f852b-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f852b-149">Ledger account</span></span> | <span data-ttu-id="f852b-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="f852b-150">Currency</span></span> | <span data-ttu-id="f852b-151">Beløb</span><span class="sxs-lookup"><span data-stu-id="f852b-151">Amount</span></span> | <span data-ttu-id="f852b-152">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="f852b-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="f852b-153">110110</span><span class="sxs-lookup"><span data-stu-id="f852b-153">110110</span></span>         | <span data-ttu-id="f852b-154">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-154">EUR</span></span>      | <span data-ttu-id="f852b-155">250</span><span class="sxs-lookup"><span data-stu-id="f852b-155">250</span></span>    | <span data-ttu-id="f852b-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f852b-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="f852b-157">130100</span><span class="sxs-lookup"><span data-stu-id="f852b-157">130100</span></span>         | <span data-ttu-id="f852b-158">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-158">EUR</span></span>      | <span data-ttu-id="f852b-159">-250</span><span class="sxs-lookup"><span data-stu-id="f852b-159">-250</span></span>   | <span data-ttu-id="f852b-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="f852b-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="f852b-161">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="f852b-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f852b-162">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="f852b-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="f852b-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f852b-163">Ledger account</span></span> | <span data-ttu-id="f852b-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="f852b-164">Currency</span></span> | <span data-ttu-id="f852b-165">Beløb</span><span class="sxs-lookup"><span data-stu-id="f852b-165">Amount</span></span>  | <span data-ttu-id="f852b-166">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="f852b-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="f852b-167">110110</span><span class="sxs-lookup"><span data-stu-id="f852b-167">110110</span></span>         | <span data-ttu-id="f852b-168">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-168">EUR</span></span>      | <span data-ttu-id="f852b-169">333,33</span><span class="sxs-lookup"><span data-stu-id="f852b-169">333.33</span></span>  | <span data-ttu-id="f852b-170">Oprindeligt beløb på 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f852b-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="f852b-171">130100</span><span class="sxs-lookup"><span data-stu-id="f852b-171">130100</span></span>         | <span data-ttu-id="f852b-172">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-172">EUR</span></span>      | <span data-ttu-id="f852b-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="f852b-173">-333.33</span></span> | <span data-ttu-id="f852b-174">Oprindeligt beløb på -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="f852b-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="f852b-175">801400</span><span class="sxs-lookup"><span data-stu-id="f852b-175">801400</span></span>         | <span data-ttu-id="f852b-176">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-176">EUR</span></span>      | <span data-ttu-id="f852b-177">83,33</span><span class="sxs-lookup"><span data-stu-id="f852b-177">83.33</span></span>   | <span data-ttu-id="f852b-178">333,33-250</span><span class="sxs-lookup"><span data-stu-id="f852b-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="f852b-179">801600</span><span class="sxs-lookup"><span data-stu-id="f852b-179">801600</span></span>         | <span data-ttu-id="f852b-180">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-180">EUR</span></span>      | <span data-ttu-id="f852b-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="f852b-181">-83.33</span></span>  | <span data-ttu-id="f852b-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="f852b-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="f852b-183">Du vil se flere posteringer for rapporteringsvalutabeløbene.</span><span class="sxs-lookup"><span data-stu-id="f852b-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="f852b-184">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 31. december 2015</span><span class="sxs-lookup"><span data-stu-id="f852b-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="f852b-185">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="f852b-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="f852b-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="f852b-186">Ledger account</span></span> | <span data-ttu-id="f852b-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="f852b-187">Currency</span></span> | <span data-ttu-id="f852b-188">Beløb</span><span class="sxs-lookup"><span data-stu-id="f852b-188">Amount</span></span>  | <span data-ttu-id="f852b-189">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="f852b-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="f852b-190">110110</span><span class="sxs-lookup"><span data-stu-id="f852b-190">110110</span></span>         | <span data-ttu-id="f852b-191">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-191">EUR</span></span>      | <span data-ttu-id="f852b-192">500,00</span><span class="sxs-lookup"><span data-stu-id="f852b-192">500.00</span></span>  | <span data-ttu-id="f852b-193">Oprindeligt beløb på 500 × 1 %</span><span class="sxs-lookup"><span data-stu-id="f852b-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="f852b-194">130100</span><span class="sxs-lookup"><span data-stu-id="f852b-194">130100</span></span>         | <span data-ttu-id="f852b-195">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-195">EUR</span></span>      | <span data-ttu-id="f852b-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="f852b-196">-500.00</span></span> | <span data-ttu-id="f852b-197">Oprindeligt beløb på -500 × 1</span><span class="sxs-lookup"><span data-stu-id="f852b-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="f852b-198">801400</span><span class="sxs-lookup"><span data-stu-id="f852b-198">801400</span></span>         | <span data-ttu-id="f852b-199">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-199">EUR</span></span>      | <span data-ttu-id="f852b-200">250</span><span class="sxs-lookup"><span data-stu-id="f852b-200">250</span></span>     | <span data-ttu-id="f852b-201">500-333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="f852b-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="f852b-202">801600</span><span class="sxs-lookup"><span data-stu-id="f852b-202">801600</span></span>         | <span data-ttu-id="f852b-203">EUR</span><span class="sxs-lookup"><span data-stu-id="f852b-203">EUR</span></span>      | <span data-ttu-id="f852b-204">-250</span><span class="sxs-lookup"><span data-stu-id="f852b-204">-250</span></span>    | <span data-ttu-id="f852b-205">-500 – (-333,33) = -166,67-166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="f852b-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





