---
title: Understøttelse af to momsvalutaer
description: I dette emne forklares det, hvordan du udvider funktionen vedrørende regnskab for to valutaer på momsområdet og indvirkningen på momsberegning og bogføring
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3f7ca56fef636431e152b2db424f1f972a507721
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212199"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="76a74-103">Understøttelse af to momsvalutaer</span><span class="sxs-lookup"><span data-stu-id="76a74-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="76a74-104">I dette emne forklares det, hvordan du udvider regnskabet for to momsvalutaer og indvirkningen på momsberegning, bogføring og udligninger.</span><span class="sxs-lookup"><span data-stu-id="76a74-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="76a74-105">Funktionen vedrørende to valutaer for Dynamics 365 Finance blev introduceret i version 8.1 (oktober 2018).</span><span class="sxs-lookup"><span data-stu-id="76a74-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="76a74-106">Den ændrer den måde, som regnskabsposter i rapporteringsvalutaen beregnes på.</span><span class="sxs-lookup"><span data-stu-id="76a74-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="76a74-107">I tidligere versioner blev transaktioner omregnet til rapporteringsvalutaen i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="76a74-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="76a74-108">Det samlede transaktionsbeløb blev beregnet i transaktionsvalutaen > transaktionsbeløbet blev omregnet til regnskabsvalutaen > regnskabsvalutabeløbet blev omregnet til rapporteringsvalutaen</span><span class="sxs-lookup"><span data-stu-id="76a74-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="76a74-109">Når funktionen vedrørende to valutaer er aktiveret, blev transaktionerne omregnet til rapporteringsvalutaen i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="76a74-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="76a74-110">Transaktionsvalutabeløb > Rapporteringsvalutabeløb</span><span class="sxs-lookup"><span data-stu-id="76a74-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="76a74-111">Yderligere oplysninger om to valutaer finder du under [To valutaer](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="76a74-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="76a74-112">Som følge af support i forbindelse med dobbelte valutaer er der stillet to nye funktioner i funktionsstyring til rådighed:</span><span class="sxs-lookup"><span data-stu-id="76a74-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="76a74-113">Momskonvertering (ny i version 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="76a74-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="76a74-114">Understøttelse af to momsvalutaer sikrer, at momsen beregnes nøjagtigt i momsvalutaen, og at momsafregningssaldoen beregnes nøjagtigt i både regnskabsvalutaen og rapporteringsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="76a74-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="76a74-115">Omregning af moms</span><span class="sxs-lookup"><span data-stu-id="76a74-115">Sales tax conversion</span></span>

<span data-ttu-id="76a74-116">Parameteren **Momskonvertering** giver to muligheder for at omregne momsbeløb fra transaktionsvaluta til momsvaluta.</span><span class="sxs-lookup"><span data-stu-id="76a74-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="76a74-117">Regnskabsvaluta: Fremgangsmåden er "Beløb i transaktionsvaluta > beløb i regnskabsvaluta > beløb i momsvaluta".</span><span class="sxs-lookup"><span data-stu-id="76a74-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="76a74-118">Regnskabsvalutaens valutakurstype (konfigureret i finansopsætning) vil blive brugt til valutaomregningen.</span><span class="sxs-lookup"><span data-stu-id="76a74-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="76a74-119">Rapporteringsvaluta: Fremgangsmåden er "Beløb i transaktionsvaluta > beløb i rapporteringsvaluta > beløb i momsvaluta".</span><span class="sxs-lookup"><span data-stu-id="76a74-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="76a74-120">Rapporteringsvalutaens valutakurstype (konfigureret i finansopsætning) vil blive brugt til valutaomregningen.</span><span class="sxs-lookup"><span data-stu-id="76a74-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="76a74-121">Eksempel</span><span class="sxs-lookup"><span data-stu-id="76a74-121">Example</span></span>

<span data-ttu-id="76a74-122">Følgende er et eksempel på en enkelt måde, hvorpå denne funktionalitet kan demonstreres:</span><span class="sxs-lookup"><span data-stu-id="76a74-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="76a74-123">Valutaopsætning for finans og moms</span><span class="sxs-lookup"><span data-stu-id="76a74-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="76a74-124">Transaktionsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-124">Transaction currency</span></span> | <span data-ttu-id="76a74-125">Regnskabsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-125">Accounting currency</span></span> | <span data-ttu-id="76a74-126">Rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-126">Reporting currency</span></span> | <span data-ttu-id="76a74-127">Momsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="76a74-128">EUR</span><span class="sxs-lookup"><span data-stu-id="76a74-128">EUR</span></span>                  | <span data-ttu-id="76a74-129">USD</span><span class="sxs-lookup"><span data-stu-id="76a74-129">USD</span></span>                 | <span data-ttu-id="76a74-130">GBP</span><span class="sxs-lookup"><span data-stu-id="76a74-130">GBP</span></span>                | <span data-ttu-id="76a74-131">GBP</span><span class="sxs-lookup"><span data-stu-id="76a74-131">GBP</span></span>          |

<span data-ttu-id="76a74-132">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="76a74-132">Exchange rate</span></span>

| <span data-ttu-id="76a74-133">Fra valuta</span><span class="sxs-lookup"><span data-stu-id="76a74-133">From currency</span></span> | <span data-ttu-id="76a74-134">Til valuta</span><span class="sxs-lookup"><span data-stu-id="76a74-134">To currency</span></span> | <span data-ttu-id="76a74-135">Faktor</span><span class="sxs-lookup"><span data-stu-id="76a74-135">Factor</span></span> | <span data-ttu-id="76a74-136">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="76a74-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="76a74-137">EUR</span><span class="sxs-lookup"><span data-stu-id="76a74-137">EUR</span></span>           | <span data-ttu-id="76a74-138">USD</span><span class="sxs-lookup"><span data-stu-id="76a74-138">USD</span></span>         | <span data-ttu-id="76a74-139">1</span><span class="sxs-lookup"><span data-stu-id="76a74-139">1</span></span>      | <span data-ttu-id="76a74-140">1.11</span><span class="sxs-lookup"><span data-stu-id="76a74-140">1.11</span></span>          |
| <span data-ttu-id="76a74-141">EUR</span><span class="sxs-lookup"><span data-stu-id="76a74-141">EUR</span></span>           | <span data-ttu-id="76a74-142">GBP</span><span class="sxs-lookup"><span data-stu-id="76a74-142">GBP</span></span>         | <span data-ttu-id="76a74-143">1</span><span class="sxs-lookup"><span data-stu-id="76a74-143">1</span></span>      | <span data-ttu-id="76a74-144">0.83</span><span class="sxs-lookup"><span data-stu-id="76a74-144">0.83</span></span>          |
| <span data-ttu-id="76a74-145">USD</span><span class="sxs-lookup"><span data-stu-id="76a74-145">USD</span></span>           | <span data-ttu-id="76a74-146">GBP</span><span class="sxs-lookup"><span data-stu-id="76a74-146">GBP</span></span>         | <span data-ttu-id="76a74-147">1</span><span class="sxs-lookup"><span data-stu-id="76a74-147">1</span></span>      | <span data-ttu-id="76a74-148">0.75</span><span class="sxs-lookup"><span data-stu-id="76a74-148">0.75</span></span>          |

<span data-ttu-id="76a74-149">Beregning af momsbeløb ved forskellige parameterindstillinger</span><span class="sxs-lookup"><span data-stu-id="76a74-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="76a74-150">Momsbeløb = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="76a74-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="76a74-151">Omregningsparametre for moms</span><span class="sxs-lookup"><span data-stu-id="76a74-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="76a74-152">Transaktionsvaluta (EUR)</span><span class="sxs-lookup"><span data-stu-id="76a74-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="76a74-153">Regnskabsvaluta (USD)</span><span class="sxs-lookup"><span data-stu-id="76a74-153">Accounting currency (USD)</span></span> | <span data-ttu-id="76a74-154">Rapporteringsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="76a74-155">Momsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="76a74-156">Regnskabsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-156">Accounting currency</span></span>             | <span data-ttu-id="76a74-157">100</span><span class="sxs-lookup"><span data-stu-id="76a74-157">100</span></span>                        | <span data-ttu-id="76a74-158">111</span><span class="sxs-lookup"><span data-stu-id="76a74-158">111</span></span>                       | <span data-ttu-id="76a74-159">83</span><span class="sxs-lookup"><span data-stu-id="76a74-159">83</span></span>                       | <span data-ttu-id="76a74-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="76a74-160">**83.25**</span></span>          |
| <span data-ttu-id="76a74-161">Rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-161">Reporting currency</span></span>              | <span data-ttu-id="76a74-162">100</span><span class="sxs-lookup"><span data-stu-id="76a74-162">100</span></span>                        | <span data-ttu-id="76a74-163">111</span><span class="sxs-lookup"><span data-stu-id="76a74-163">111</span></span>                       | <span data-ttu-id="76a74-164">83</span><span class="sxs-lookup"><span data-stu-id="76a74-164">83</span></span>                       | <span data-ttu-id="76a74-165">**83**</span><span class="sxs-lookup"><span data-stu-id="76a74-165">**83**</span></span>             |

<span data-ttu-id="76a74-166">Dette parameter kan konfigureres på grundlag af overholdelsesbehovet fra skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="76a74-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="76a74-167">Overvejelser omkring opgradering</span><span class="sxs-lookup"><span data-stu-id="76a74-167">Upgrade Consideration</span></span>

<span data-ttu-id="76a74-168">Denne funktion gælder kun for nye transaktioner.</span><span class="sxs-lookup"><span data-stu-id="76a74-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="76a74-169">For så vidt angår momstransaktioner, der allerede er blevet gemt i tabellen TAXTRANS, men som endnu ikke er blevet udlignet, vil systemet ikke genberegne momsbeløbet i momsvalutaen, fordi valutakursen på tidspunktet, hvor momsen skal bogføres, allerede mangler.</span><span class="sxs-lookup"><span data-stu-id="76a74-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="76a74-170">Hvis du vil undgå ovenstående, anbefales det, at du ændrer denne parameterværdi i en ny (ren) momsafregningsperiode, der ikke indeholder nogen ikke-udlignede momstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="76a74-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="76a74-171">Hvis du vil ændre denne værdi midt i en momsafregningsperiode, skal du køre programmet "Udligning og bogføring af moms" for den aktuelle momsafregningsperiode, før du ændrer denne parameterværdi.</span><span class="sxs-lookup"><span data-stu-id="76a74-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="76a74-172">Spor momsbeløbet i rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="76a74-173">Der blev føjet tre nye felter til de momsrelaterede tabeller for at spore beløb i rapporteringsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="76a74-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="76a74-174">Disse felter findes i TAXUNCOMMITTED- og TAXTRANS-tabellerne:</span><span class="sxs-lookup"><span data-stu-id="76a74-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="76a74-175">TaxAmountRep: momsbeløb i rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="76a74-176">TaxBaseAmountRep: grundbeløbet i rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="76a74-177">TaxInCostPriceRep: ikke-fradragsberettiget beløb i rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="76a74-178">Hvis momsen kun er gemt i tabellen TAXUNCOMMITTED, men ikke bogført endnu, vil systemet beregne momsbeløbet i rapporteringsvalutaen på bogføringstidspunktet og gemme det i TAXTRANS-tabellen.</span><span class="sxs-lookup"><span data-stu-id="76a74-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="76a74-179">Denne version omfatter ikke ændringer i rapporter og formularer, der viser momsbeløbet i rapporteringsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="76a74-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="76a74-180">Ændringer i rapporter og formularer vil blive leveret i den kommende udgivelse.</span><span class="sxs-lookup"><span data-stu-id="76a74-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="76a74-181">Automatisk saldo for momsafregning i rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="76a74-182">Hvis momsafregningen ikke er afstemt i rapporteringsvalutaen af en bestemt grund, f.eks. fordi fremgangsmåden for omregning af moms er "Regnskabsvaluta" eller valutakursen ændres i en enkelt momsafregningsperiode, vil systemet automatisk oprette regnskabsposter, der skal regulere afvigelse i momsbeløbet og modposteres i henhold til den realiserede vekselgevinst/tabskonto, der konfigureres i finansopsætningen.</span><span class="sxs-lookup"><span data-stu-id="76a74-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="76a74-183">Hvis du bruger eksemplet ovenfor til at demonstrere denne funktion, skal du gå ud fra, at dataene i tabellen TAXTRANS på bogføringstidspunktet er som følger.</span><span class="sxs-lookup"><span data-stu-id="76a74-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="76a74-184">Omregningsparametre for moms</span><span class="sxs-lookup"><span data-stu-id="76a74-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="76a74-185">Transaktionsvaluta (EUR)</span><span class="sxs-lookup"><span data-stu-id="76a74-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="76a74-186">Regnskabsvaluta (USD)</span><span class="sxs-lookup"><span data-stu-id="76a74-186">Accounting currency (USD)</span></span> | <span data-ttu-id="76a74-187">Rapporteringsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="76a74-188">Momsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="76a74-189">Regnskabsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-189">Accounting currency</span></span>             | <span data-ttu-id="76a74-190">100</span><span class="sxs-lookup"><span data-stu-id="76a74-190">100</span></span>                        | <span data-ttu-id="76a74-191">111</span><span class="sxs-lookup"><span data-stu-id="76a74-191">111</span></span>                       | <span data-ttu-id="76a74-192">83</span><span class="sxs-lookup"><span data-stu-id="76a74-192">83</span></span>                       | <span data-ttu-id="76a74-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="76a74-193">**83.25**</span></span>          |
| <span data-ttu-id="76a74-194">Rapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="76a74-194">Reporting currency</span></span>              | <span data-ttu-id="76a74-195">100</span><span class="sxs-lookup"><span data-stu-id="76a74-195">100</span></span>                        | <span data-ttu-id="76a74-196">111</span><span class="sxs-lookup"><span data-stu-id="76a74-196">111</span></span>                       | <span data-ttu-id="76a74-197">83</span><span class="sxs-lookup"><span data-stu-id="76a74-197">83</span></span>                       | <span data-ttu-id="76a74-198">**83**</span><span class="sxs-lookup"><span data-stu-id="76a74-198">**83**</span></span>             |

<span data-ttu-id="76a74-199">Når du kører momsafregningsprogrammet ved månedsafslutning, vil regnskabsbogføringen være følgende:.</span><span class="sxs-lookup"><span data-stu-id="76a74-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="76a74-200">Scenarie: omberegning af momsbeløb = "Regnskabsvaluta"</span><span class="sxs-lookup"><span data-stu-id="76a74-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="76a74-201">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="76a74-201">Main account</span></span>           | <span data-ttu-id="76a74-202">Transaktionsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="76a74-203">Regnskabsvaluta (USD)</span><span class="sxs-lookup"><span data-stu-id="76a74-203">Accounting currency (USD)</span></span> | <span data-ttu-id="76a74-204">Rapporteringsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="76a74-205">Udgående/indgående moms</span><span class="sxs-lookup"><span data-stu-id="76a74-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="76a74-206">-83,25</span><span class="sxs-lookup"><span data-stu-id="76a74-206">-83.25</span></span>                     | <span data-ttu-id="76a74-207">-111</span><span class="sxs-lookup"><span data-stu-id="76a74-207">-111</span></span>                      | <span data-ttu-id="76a74-208">-83,25</span><span class="sxs-lookup"><span data-stu-id="76a74-208">-83.25</span></span>                   |
| <span data-ttu-id="76a74-209">Momsafregning</span><span class="sxs-lookup"><span data-stu-id="76a74-209">Tax Settlement</span></span>         | <span data-ttu-id="76a74-210">83.25</span><span class="sxs-lookup"><span data-stu-id="76a74-210">83.25</span></span>                      | <span data-ttu-id="76a74-211">111</span><span class="sxs-lookup"><span data-stu-id="76a74-211">111</span></span>                       | <span data-ttu-id="76a74-212">83.25</span><span class="sxs-lookup"><span data-stu-id="76a74-212">83.25</span></span>                    |
| <span data-ttu-id="76a74-213">Realiseret gevinst/tab</span><span class="sxs-lookup"><span data-stu-id="76a74-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="76a74-214">0</span><span class="sxs-lookup"><span data-stu-id="76a74-214">0</span></span>                          | <span data-ttu-id="76a74-215">0</span><span class="sxs-lookup"><span data-stu-id="76a74-215">0</span></span>                         | <span data-ttu-id="76a74-216">-0,25</span><span class="sxs-lookup"><span data-stu-id="76a74-216">-0.25</span></span>                    |
| <span data-ttu-id="76a74-217">Udgående/indgående moms</span><span class="sxs-lookup"><span data-stu-id="76a74-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="76a74-218">0</span><span class="sxs-lookup"><span data-stu-id="76a74-218">0</span></span>                          | <span data-ttu-id="76a74-219">0</span><span class="sxs-lookup"><span data-stu-id="76a74-219">0</span></span>                         | <span data-ttu-id="76a74-220">0.25</span><span class="sxs-lookup"><span data-stu-id="76a74-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="76a74-221">Scenarie: omberegning af momsbeløb = "Rapporteringsvaluta"</span><span class="sxs-lookup"><span data-stu-id="76a74-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="76a74-222">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="76a74-222">Main account</span></span>           | <span data-ttu-id="76a74-223">Transaktionsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="76a74-224">Regnskabsvaluta (USD)</span><span class="sxs-lookup"><span data-stu-id="76a74-224">Accounting currency (USD)</span></span> | <span data-ttu-id="76a74-225">Rapporteringsvaluta (GBP)</span><span class="sxs-lookup"><span data-stu-id="76a74-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="76a74-226">Udgående/indgående moms</span><span class="sxs-lookup"><span data-stu-id="76a74-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="76a74-227">-83</span><span class="sxs-lookup"><span data-stu-id="76a74-227">-83</span></span>                        | <span data-ttu-id="76a74-228">-110,67</span><span class="sxs-lookup"><span data-stu-id="76a74-228">-110.67</span></span>                   | <span data-ttu-id="76a74-229">-83</span><span class="sxs-lookup"><span data-stu-id="76a74-229">-83</span></span>                      |
| <span data-ttu-id="76a74-230">Momsafregning</span><span class="sxs-lookup"><span data-stu-id="76a74-230">Tax Settlement</span></span>         | <span data-ttu-id="76a74-231">83</span><span class="sxs-lookup"><span data-stu-id="76a74-231">83</span></span>                         | <span data-ttu-id="76a74-232">110.67</span><span class="sxs-lookup"><span data-stu-id="76a74-232">110.67</span></span>                    | <span data-ttu-id="76a74-233">83</span><span class="sxs-lookup"><span data-stu-id="76a74-233">83</span></span>                       |
| <span data-ttu-id="76a74-234">Realiseret gevinst/tab</span><span class="sxs-lookup"><span data-stu-id="76a74-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="76a74-235">0</span><span class="sxs-lookup"><span data-stu-id="76a74-235">0</span></span>                          | <span data-ttu-id="76a74-236">0.33</span><span class="sxs-lookup"><span data-stu-id="76a74-236">0.33</span></span>                      | <span data-ttu-id="76a74-237">0</span><span class="sxs-lookup"><span data-stu-id="76a74-237">0</span></span>                        |
| <span data-ttu-id="76a74-238">Udgående/indgående moms</span><span class="sxs-lookup"><span data-stu-id="76a74-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="76a74-239">0</span><span class="sxs-lookup"><span data-stu-id="76a74-239">0</span></span>                          | <span data-ttu-id="76a74-240">-0,33</span><span class="sxs-lookup"><span data-stu-id="76a74-240">-0.33</span></span>                     | <span data-ttu-id="76a74-241">0</span><span class="sxs-lookup"><span data-stu-id="76a74-241">0</span></span>                        |



<span data-ttu-id="76a74-242">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="76a74-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="76a74-243">Dobbelt valuta</span><span class="sxs-lookup"><span data-stu-id="76a74-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="76a74-244">Momsoversigt</span><span class="sxs-lookup"><span data-stu-id="76a74-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]