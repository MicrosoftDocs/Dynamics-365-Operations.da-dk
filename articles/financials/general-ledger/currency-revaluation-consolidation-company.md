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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839416"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="70d99-103">Værdiregulering af valuta i et konsolideret regnskab</span><span class="sxs-lookup"><span data-stu-id="70d99-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70d99-104">Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt.</span><span class="sxs-lookup"><span data-stu-id="70d99-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="70d99-105">Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="70d99-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="70d99-106">Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene.</span><span class="sxs-lookup"><span data-stu-id="70d99-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="70d99-107">Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato.</span><span class="sxs-lookup"><span data-stu-id="70d99-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="70d99-108">Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.</span><span class="sxs-lookup"><span data-stu-id="70d99-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="70d99-109">Virksomhedsopsætning</span><span class="sxs-lookup"><span data-stu-id="70d99-109">Company setup</span></span>
-   <span data-ttu-id="70d99-110">**Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="70d99-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="70d99-111">**Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.</span><span class="sxs-lookup"><span data-stu-id="70d99-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="70d99-112">**Realiseret gevinst** – Finanskonto 801500</span><span class="sxs-lookup"><span data-stu-id="70d99-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="70d99-113">**Realiseret tab** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="70d99-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="70d99-114">**Urealiseret gevinst** – Finanskonto 801600</span><span class="sxs-lookup"><span data-stu-id="70d99-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="70d99-115">**Urealiseret tab** – Finanskonto 801400</span><span class="sxs-lookup"><span data-stu-id="70d99-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="70d99-116">Oprindelige posteringer</span><span class="sxs-lookup"><span data-stu-id="70d99-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="70d99-117">Indbetalingsposteringer i USMF</span><span class="sxs-lookup"><span data-stu-id="70d99-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="70d99-118">Dato</span><span class="sxs-lookup"><span data-stu-id="70d99-118">Date</span></span>       | <span data-ttu-id="70d99-119">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="70d99-119">Ledger account</span></span>               | <span data-ttu-id="70d99-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="70d99-120">Currency</span></span> | <span data-ttu-id="70d99-121">Beløb</span><span class="sxs-lookup"><span data-stu-id="70d99-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="70d99-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="70d99-122">10/11/2015</span></span> | <span data-ttu-id="70d99-123">110110 – Kontant</span><span class="sxs-lookup"><span data-stu-id="70d99-123">110110 – Cash</span></span>                | <span data-ttu-id="70d99-124">USD</span><span class="sxs-lookup"><span data-stu-id="70d99-124">USD</span></span>      | <span data-ttu-id="70d99-125">500</span><span class="sxs-lookup"><span data-stu-id="70d99-125">500</span></span>    |
| <span data-ttu-id="70d99-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="70d99-126">10/11/2015</span></span> | <span data-ttu-id="70d99-127">130100 – Debitorer</span><span class="sxs-lookup"><span data-stu-id="70d99-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="70d99-128">USD</span><span class="sxs-lookup"><span data-stu-id="70d99-128">USD</span></span>      | <span data-ttu-id="70d99-129">-500</span><span class="sxs-lookup"><span data-stu-id="70d99-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="70d99-130">Valutakurser</span><span class="sxs-lookup"><span data-stu-id="70d99-130">Exchange rates</span></span>

| <span data-ttu-id="70d99-131">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="70d99-131">From currency</span></span> | <span data-ttu-id="70d99-132">Til valuta</span><span class="sxs-lookup"><span data-stu-id="70d99-132">To currency</span></span> | <span data-ttu-id="70d99-133">Startdato</span><span class="sxs-lookup"><span data-stu-id="70d99-133">Start date</span></span> | <span data-ttu-id="70d99-134">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="70d99-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="70d99-135">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-135">EUR</span></span>           | <span data-ttu-id="70d99-136">USD</span><span class="sxs-lookup"><span data-stu-id="70d99-136">USD</span></span>         | <span data-ttu-id="70d99-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="70d99-137">10/1/2015</span></span>  | <span data-ttu-id="70d99-138">200</span><span class="sxs-lookup"><span data-stu-id="70d99-138">200</span></span>           |
| <span data-ttu-id="70d99-139">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-139">EUR</span></span>           | <span data-ttu-id="70d99-140">USD</span><span class="sxs-lookup"><span data-stu-id="70d99-140">USD</span></span>         | <span data-ttu-id="70d99-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="70d99-141">11/1/2015</span></span>  | <span data-ttu-id="70d99-142">150</span><span class="sxs-lookup"><span data-stu-id="70d99-142">150</span></span>           |
| <span data-ttu-id="70d99-143">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-143">EUR</span></span>           | <span data-ttu-id="70d99-144">USD</span><span class="sxs-lookup"><span data-stu-id="70d99-144">USD</span></span>         | <span data-ttu-id="70d99-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="70d99-145">12/1/2012</span></span>  | <span data-ttu-id="70d99-146">100</span><span class="sxs-lookup"><span data-stu-id="70d99-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="70d99-147">Udføre konsolidering for oktober 2015</span><span class="sxs-lookup"><span data-stu-id="70d99-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="70d99-148">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="70d99-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="70d99-149">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="70d99-149">Ledger account</span></span> | <span data-ttu-id="70d99-150">Valuta</span><span class="sxs-lookup"><span data-stu-id="70d99-150">Currency</span></span> | <span data-ttu-id="70d99-151">Beløb</span><span class="sxs-lookup"><span data-stu-id="70d99-151">Amount</span></span> | <span data-ttu-id="70d99-152">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="70d99-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="70d99-153">110110</span><span class="sxs-lookup"><span data-stu-id="70d99-153">110110</span></span>         | <span data-ttu-id="70d99-154">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-154">EUR</span></span>      | <span data-ttu-id="70d99-155">250</span><span class="sxs-lookup"><span data-stu-id="70d99-155">250</span></span>    | <span data-ttu-id="70d99-156">500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="70d99-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="70d99-157">130100</span><span class="sxs-lookup"><span data-stu-id="70d99-157">130100</span></span>         | <span data-ttu-id="70d99-158">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-158">EUR</span></span>      | <span data-ttu-id="70d99-159">-250</span><span class="sxs-lookup"><span data-stu-id="70d99-159">-250</span></span>   | <span data-ttu-id="70d99-160">-500 USD × 50 %</span><span class="sxs-lookup"><span data-stu-id="70d99-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="70d99-161">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 30. november 2015</span><span class="sxs-lookup"><span data-stu-id="70d99-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="70d99-162">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="70d99-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="70d99-163">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="70d99-163">Ledger account</span></span> | <span data-ttu-id="70d99-164">Valuta</span><span class="sxs-lookup"><span data-stu-id="70d99-164">Currency</span></span> | <span data-ttu-id="70d99-165">Beløb</span><span class="sxs-lookup"><span data-stu-id="70d99-165">Amount</span></span>  | <span data-ttu-id="70d99-166">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="70d99-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="70d99-167">110110</span><span class="sxs-lookup"><span data-stu-id="70d99-167">110110</span></span>         | <span data-ttu-id="70d99-168">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-168">EUR</span></span>      | <span data-ttu-id="70d99-169">333,33</span><span class="sxs-lookup"><span data-stu-id="70d99-169">333.33</span></span>  | <span data-ttu-id="70d99-170">Oprindeligt beløb på 500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="70d99-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="70d99-171">130100</span><span class="sxs-lookup"><span data-stu-id="70d99-171">130100</span></span>         | <span data-ttu-id="70d99-172">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-172">EUR</span></span>      | <span data-ttu-id="70d99-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="70d99-173">-333.33</span></span> | <span data-ttu-id="70d99-174">Oprindeligt beløb på -500 × 66,6667 %</span><span class="sxs-lookup"><span data-stu-id="70d99-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="70d99-175">801400</span><span class="sxs-lookup"><span data-stu-id="70d99-175">801400</span></span>         | <span data-ttu-id="70d99-176">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-176">EUR</span></span>      | <span data-ttu-id="70d99-177">83,33</span><span class="sxs-lookup"><span data-stu-id="70d99-177">83.33</span></span>   | <span data-ttu-id="70d99-178">333,33-250</span><span class="sxs-lookup"><span data-stu-id="70d99-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="70d99-179">801600</span><span class="sxs-lookup"><span data-stu-id="70d99-179">801600</span></span>         | <span data-ttu-id="70d99-180">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-180">EUR</span></span>      | <span data-ttu-id="70d99-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="70d99-181">-83.33</span></span>  | <span data-ttu-id="70d99-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="70d99-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="70d99-183">Du vil se flere posteringer for rapporteringsvalutabeløbene.</span><span class="sxs-lookup"><span data-stu-id="70d99-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="70d99-184">Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 31. december 2015</span><span class="sxs-lookup"><span data-stu-id="70d99-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="70d99-185">Saldiene i det konsoliderede regnskab</span><span class="sxs-lookup"><span data-stu-id="70d99-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="70d99-186">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="70d99-186">Ledger account</span></span> | <span data-ttu-id="70d99-187">Valuta</span><span class="sxs-lookup"><span data-stu-id="70d99-187">Currency</span></span> | <span data-ttu-id="70d99-188">Beløb</span><span class="sxs-lookup"><span data-stu-id="70d99-188">Amount</span></span>  | <span data-ttu-id="70d99-189">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="70d99-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="70d99-190">110110</span><span class="sxs-lookup"><span data-stu-id="70d99-190">110110</span></span>         | <span data-ttu-id="70d99-191">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-191">EUR</span></span>      | <span data-ttu-id="70d99-192">500,00</span><span class="sxs-lookup"><span data-stu-id="70d99-192">500.00</span></span>  | <span data-ttu-id="70d99-193">Oprindeligt beløb på 500 × 1 %</span><span class="sxs-lookup"><span data-stu-id="70d99-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="70d99-194">130100</span><span class="sxs-lookup"><span data-stu-id="70d99-194">130100</span></span>         | <span data-ttu-id="70d99-195">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-195">EUR</span></span>      | <span data-ttu-id="70d99-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="70d99-196">-500.00</span></span> | <span data-ttu-id="70d99-197">Oprindeligt beløb på -500 × 1</span><span class="sxs-lookup"><span data-stu-id="70d99-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="70d99-198">801400</span><span class="sxs-lookup"><span data-stu-id="70d99-198">801400</span></span>         | <span data-ttu-id="70d99-199">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-199">EUR</span></span>      | <span data-ttu-id="70d99-200">250</span><span class="sxs-lookup"><span data-stu-id="70d99-200">250</span></span>     | <span data-ttu-id="70d99-201">500-333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="70d99-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="70d99-202">801600</span><span class="sxs-lookup"><span data-stu-id="70d99-202">801600</span></span>         | <span data-ttu-id="70d99-203">EUR</span><span class="sxs-lookup"><span data-stu-id="70d99-203">EUR</span></span>      | <span data-ttu-id="70d99-204">-250</span><span class="sxs-lookup"><span data-stu-id="70d99-204">-250</span></span>    | <span data-ttu-id="70d99-205">-500 – (-333,33) = -166,67-166,67 + (-83,33) = -250</span><span class="sxs-lookup"><span data-stu-id="70d99-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





