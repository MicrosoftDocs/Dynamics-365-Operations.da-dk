---
title: Dobbeltrapportering
description: I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441746"
---
# <a name="dual-reporting"></a><span data-ttu-id="73976-103">Dobbeltrapportering</span><span class="sxs-lookup"><span data-stu-id="73976-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73976-104">I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="73976-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="73976-105">Det er nødvendigt med kendskab til posteringslag i Microsoft Dynamics 365 Finance, og det vil gøre det nemmere at forstå i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="73976-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="73976-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="73976-106">Example</span></span>

<span data-ttu-id="73976-107">Følgende eksempelkonti til en leaseaftale under italiensk lovpligtig rapportering ved hjælp af både likviditetsmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="73976-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="73976-108">Firmaet skal etablere tre kartoteker for at kunne redegøre for både de italienske lovpligtige krav og IFRS 16-krav.</span><span class="sxs-lookup"><span data-stu-id="73976-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="73976-109">Der kræves et kartotek til IFRS 16, et kartotek til lovpligtige krav, og et kartotek til automatisk tilbageføring af lovpligtige bogføringer.</span><span class="sxs-lookup"><span data-stu-id="73976-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="73976-110">Kartotekerne oprettes som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="73976-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="73976-111">**IFRS 16-kartotek**</span><span class="sxs-lookup"><span data-stu-id="73976-111">**IFRS 16 book**</span></span>

<span data-ttu-id="73976-112">IFRS 16-kartoteket er konfigureret, så det overholder IFRS 16-regnskabsstandarden.</span><span class="sxs-lookup"><span data-stu-id="73976-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="73976-113">Alle poster, der er bogført i dette kartotek, bogføres i et brugerdefineret lag.</span><span class="sxs-lookup"><span data-stu-id="73976-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="73976-114">Navn</span><span class="sxs-lookup"><span data-stu-id="73976-114">Name</span></span>                                    | <span data-ttu-id="73976-115">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="73976-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="73976-116">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="73976-116">Book type</span></span>                               | <span data-ttu-id="73976-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="73976-117">IFRS 16</span></span>        |
| <span data-ttu-id="73976-118">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-118">Book description</span></span>                        | <span data-ttu-id="73976-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="73976-119">IFRS 16</span></span>        |
| <span data-ttu-id="73976-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="73976-120">Posting Layer</span></span>                           | <span data-ttu-id="73976-121">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="73976-121">Custom layer 1</span></span> |
| <span data-ttu-id="73976-122">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="73976-122">Lease Type</span></span>                              | <span data-ttu-id="73976-123">Finance</span><span class="sxs-lookup"><span data-stu-id="73976-123">Finance</span></span>        |
| <span data-ttu-id="73976-124">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="73976-124">Accounting Framework</span></span>                    | <span data-ttu-id="73976-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="73976-125">IFRS 16</span></span>        |
| <span data-ttu-id="73976-126">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="73976-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="73976-127">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-127">0.00</span></span>           |
| <span data-ttu-id="73976-128">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="73976-129">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-129">0.00</span></span>           |
| <span data-ttu-id="73976-130">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="73976-130">Short-term threshold</span></span>                    | <span data-ttu-id="73976-131">12</span><span class="sxs-lookup"><span data-stu-id="73976-131">12</span></span>             |
| <span data-ttu-id="73976-132">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="73976-132">Low Value Threshold</span></span>                     | <span data-ttu-id="73976-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-133">5,000.00</span></span>       |
| <span data-ttu-id="73976-134">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-134">Pay to Vendor</span></span>                           | <span data-ttu-id="73976-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="73976-135">No</span></span>             |

<span data-ttu-id="73976-136">**Lovpligtigt kartotek**</span><span class="sxs-lookup"><span data-stu-id="73976-136">**Statutory book**</span></span>

<span data-ttu-id="73976-137">Det lovpligtige kartotek er en kassekladde, hvor firmaet kan redegøre for leasingudgifter som det kontantbeløb, der betales hver måned for leje.</span><span class="sxs-lookup"><span data-stu-id="73976-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="73976-138">Dette kartotek opretter ikke et ROU-aktiv eller en leasingforpligtelse.</span><span class="sxs-lookup"><span data-stu-id="73976-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="73976-139">Navn</span><span class="sxs-lookup"><span data-stu-id="73976-139">Name</span></span>                                    | <span data-ttu-id="73976-140">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="73976-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="73976-141">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="73976-141">Book type</span></span>                               | <span data-ttu-id="73976-142">Lovpligtig</span><span class="sxs-lookup"><span data-stu-id="73976-142">Statutory</span></span>   |
| <span data-ttu-id="73976-143">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-143">Book description</span></span>                        | <span data-ttu-id="73976-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="73976-144">Local GAAP</span></span>  |
| <span data-ttu-id="73976-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="73976-145">Posting Layer</span></span>                           | <span data-ttu-id="73976-146">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-146">Current</span></span>     |
| <span data-ttu-id="73976-147">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="73976-147">Lease Type</span></span>                              | <span data-ttu-id="73976-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="73976-148">Automatic</span></span>   |
| <span data-ttu-id="73976-149">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="73976-149">Accounting Framework</span></span>                    | <span data-ttu-id="73976-150">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="73976-150">Cash basis</span></span>  |
| <span data-ttu-id="73976-151">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="73976-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="73976-152">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-152">0.00</span></span>        |
| <span data-ttu-id="73976-153">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="73976-154">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-154">0.00</span></span>        |
| <span data-ttu-id="73976-155">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="73976-155">Short-term threshold</span></span>                    | <span data-ttu-id="73976-156">0</span><span class="sxs-lookup"><span data-stu-id="73976-156">0</span></span>           |
| <span data-ttu-id="73976-157">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="73976-157">Low Value Threshold</span></span>                     | <span data-ttu-id="73976-158">0</span><span class="sxs-lookup"><span data-stu-id="73976-158">0</span></span>           |
| <span data-ttu-id="73976-159">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-159">Pay to Vendor</span></span>                           | <span data-ttu-id="73976-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="73976-160">No</span></span>          |

<span data-ttu-id="73976-161">**Lovpligtigt tilbageført kartotek**</span><span class="sxs-lookup"><span data-stu-id="73976-161">**Statutory reversal book**</span></span>

<span data-ttu-id="73976-162">Det lovpligtige tilbageførte kartotek konfigureres på samme måde som det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="73976-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="73976-163">Navn</span><span class="sxs-lookup"><span data-stu-id="73976-163">Name</span></span>                                    | <span data-ttu-id="73976-164">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="73976-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="73976-165">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="73976-165">Book type</span></span>                               | <span data-ttu-id="73976-166">Lovpligtig - tilbageført</span><span class="sxs-lookup"><span data-stu-id="73976-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="73976-167">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-167">Book description</span></span>                        | <span data-ttu-id="73976-168">Kartotek, der skal tilbageføre lovpligtigt kartotek</span><span class="sxs-lookup"><span data-stu-id="73976-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="73976-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="73976-169">Posting Layer</span></span>                           | <span data-ttu-id="73976-170">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="73976-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="73976-171">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="73976-171">Lease Type</span></span>                              | <span data-ttu-id="73976-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="73976-172">Automatic</span></span>                      |
| <span data-ttu-id="73976-173">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="73976-173">Accounting Framework</span></span>                    | <span data-ttu-id="73976-174">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="73976-174">Cash basis</span></span>                     |
| <span data-ttu-id="73976-175">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="73976-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="73976-176">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-176">0.00</span></span>                           |
| <span data-ttu-id="73976-177">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="73976-178">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-178">0.00</span></span>                           |
| <span data-ttu-id="73976-179">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="73976-179">Short-term threshold</span></span>                    | <span data-ttu-id="73976-180">0</span><span class="sxs-lookup"><span data-stu-id="73976-180">0</span></span>                              |
| <span data-ttu-id="73976-181">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="73976-181">Low Value Threshold</span></span>                     | <span data-ttu-id="73976-182">0</span><span class="sxs-lookup"><span data-stu-id="73976-182">0</span></span>                              |
| <span data-ttu-id="73976-183">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-183">Pay to Vendor</span></span>                           | <span data-ttu-id="73976-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="73976-184">No</span></span>                             |

<span data-ttu-id="73976-185">I dette eksempel er der oprettet en leasingaftale, der indeholder følgende indstillinger under fanerne **Generelt** og **Betalingsplanlinje**.</span><span class="sxs-lookup"><span data-stu-id="73976-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="73976-186">Fanen **Generelt**</span><span class="sxs-lookup"><span data-stu-id="73976-186">**General tab**</span></span>

| <span data-ttu-id="73976-187">Felt</span><span class="sxs-lookup"><span data-stu-id="73976-187">Field</span></span>                      | <span data-ttu-id="73976-188">Værdi</span><span class="sxs-lookup"><span data-stu-id="73976-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="73976-189">Trinvis lånesats</span><span class="sxs-lookup"><span data-stu-id="73976-189">Incremental borrowing rate</span></span> | <span data-ttu-id="73976-190">5 %</span><span class="sxs-lookup"><span data-stu-id="73976-190">5%</span></span>               |
| <span data-ttu-id="73976-191">Dato for påbegyndelse</span><span class="sxs-lookup"><span data-stu-id="73976-191">Commencement date</span></span>          | <span data-ttu-id="73976-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="73976-192">1/1/2020</span></span>         |
| <span data-ttu-id="73976-193">Leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="73976-193">Lease group</span></span>                | <span data-ttu-id="73976-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="73976-194">Buildings</span></span>        |
| <span data-ttu-id="73976-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="73976-195">Vendor</span></span>                     | <span data-ttu-id="73976-196">1001</span><span class="sxs-lookup"><span data-stu-id="73976-196">1001</span></span>             |
| <span data-ttu-id="73976-197">Aktivets handelsværdi</span><span class="sxs-lookup"><span data-stu-id="73976-197">Fair value of the asset</span></span>    | <span data-ttu-id="73976-198">245,000</span><span class="sxs-lookup"><span data-stu-id="73976-198">245,000</span></span>          |
| <span data-ttu-id="73976-199">Brugstid for aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-199">Asset useful life</span></span>          | <span data-ttu-id="73976-200">120</span><span class="sxs-lookup"><span data-stu-id="73976-200">120</span></span>              |
| <span data-ttu-id="73976-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="73976-201">Annuity type</span></span>               | <span data-ttu-id="73976-202">Almindelig annuitet</span><span class="sxs-lookup"><span data-stu-id="73976-202">Ordinary annuity</span></span> |
| <span data-ttu-id="73976-203">Sammensætningsinterval</span><span class="sxs-lookup"><span data-stu-id="73976-203">Compounding interval</span></span>       | <span data-ttu-id="73976-204">Månedligt</span><span class="sxs-lookup"><span data-stu-id="73976-204">Monthly</span></span>          |

<span data-ttu-id="73976-205">**Betalingsplanlinjer-fane**</span><span class="sxs-lookup"><span data-stu-id="73976-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="73976-206">Felt</span><span class="sxs-lookup"><span data-stu-id="73976-206">Field</span></span>             | <span data-ttu-id="73976-207">Værdi</span><span class="sxs-lookup"><span data-stu-id="73976-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="73976-208">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="73976-208">Start date</span></span>        | <span data-ttu-id="73976-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="73976-209">1/1/2020</span></span>   |
| <span data-ttu-id="73976-210">Periodeinterval</span><span class="sxs-lookup"><span data-stu-id="73976-210">Period interval</span></span>   | <span data-ttu-id="73976-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="73976-211">Months</span></span>     |
| <span data-ttu-id="73976-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="73976-212">Periods</span></span>           | <span data-ttu-id="73976-213">24</span><span class="sxs-lookup"><span data-stu-id="73976-213">24</span></span>         |
| <span data-ttu-id="73976-214">Slutdato</span><span class="sxs-lookup"><span data-stu-id="73976-214">End date</span></span>          | <span data-ttu-id="73976-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="73976-215">12/31/2020</span></span> |
| <span data-ttu-id="73976-216">Betalingshyppighed</span><span class="sxs-lookup"><span data-stu-id="73976-216">Payment frequency</span></span> | <span data-ttu-id="73976-217">Månedligt</span><span class="sxs-lookup"><span data-stu-id="73976-217">Monthly</span></span>    |
| <span data-ttu-id="73976-218">Betalingsbeløb</span><span class="sxs-lookup"><span data-stu-id="73976-218">Payment amount</span></span>    | <span data-ttu-id="73976-219">1.000</span><span class="sxs-lookup"><span data-stu-id="73976-219">1,000</span></span>      |

<span data-ttu-id="73976-220">Hvis du vil redegøre for denne leasingaftale i forbindelse med to strukturer, skal du bruge et aktuelt posteringslag og et brugerdefineret posteringslag.</span><span class="sxs-lookup"><span data-stu-id="73976-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="73976-221">Følgende tabel viser et eksempel på hver kladdepost, der er nødvendig for at repræsentere finanserne i de enkelte rapporteringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="73976-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="73976-222">En detaljeret beskrivelse af de enkelte kladdeposter for den første måned af leasingaftalen tildeles bagefter.</span><span class="sxs-lookup"><span data-stu-id="73976-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="73976-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="73976-224">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="73976-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="73976-225">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="73976-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="73976-226">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="73976-226">Current layer total</span></span></th>
<th><span data-ttu-id="73976-227">Tilbageført kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="73976-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="73976-228">IFRS 16-kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="73976-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="73976-229">Aktuelt lag + brugerdefineret lag i alt</span><span class="sxs-lookup"><span data-stu-id="73976-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73976-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="73976-230">JE-100</span></span></th>
<th><span data-ttu-id="73976-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="73976-231">JE-110</span></span></th>
<th><span data-ttu-id="73976-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="73976-232">JE-120</span></span></th>
<th><span data-ttu-id="73976-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="73976-233">JE-130</span></span></th>
<th><span data-ttu-id="73976-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="73976-234">JE-140</span></span></th>
<th><span data-ttu-id="73976-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="73976-235">JE-150</span></span></th>
<th><span data-ttu-id="73976-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="73976-236">JE-160</span></span></th>
<th><span data-ttu-id="73976-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="73976-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73976-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73976-246">1</span><span class="sxs-lookup"><span data-stu-id="73976-246">1</span></span></td>
<td><span data-ttu-id="73976-247">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="73976-247">Lease expense</span></span></td>
<td><span data-ttu-id="73976-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-249">1,000.00</span></span></td>
<td><span data-ttu-id="73976-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="73976-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-251">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-252">2</span><span class="sxs-lookup"><span data-stu-id="73976-252">2</span></span></td>
<td><span data-ttu-id="73976-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="73976-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="73976-254">3.00</span><span class="sxs-lookup"><span data-stu-id="73976-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-255">3.00</span><span class="sxs-lookup"><span data-stu-id="73976-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-256">3.00</span><span class="sxs-lookup"><span data-stu-id="73976-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-257">3</span><span class="sxs-lookup"><span data-stu-id="73976-257">3</span></span></td>
<td><span data-ttu-id="73976-258">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="73976-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="73976-259">5.00</span><span class="sxs-lookup"><span data-stu-id="73976-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-260">5.00</span><span class="sxs-lookup"><span data-stu-id="73976-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-261">5.00</span><span class="sxs-lookup"><span data-stu-id="73976-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-262">4</span><span class="sxs-lookup"><span data-stu-id="73976-262">4</span></span></td>
<td><span data-ttu-id="73976-263">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-263">Clearing account</span></span></td>
<td><span data-ttu-id="73976-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="73976-264">-1,000.00</span></span></td>
<td><span data-ttu-id="73976-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-266">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-266">0.00</span></span></td>
<td><span data-ttu-id="73976-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="73976-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-269">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-270">5</span><span class="sxs-lookup"><span data-stu-id="73976-270">5</span></span></td>
<td><span data-ttu-id="73976-271">Kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="73976-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-272">-1,008.00</span></span></td>
<td><span data-ttu-id="73976-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="73976-273">1,008.00</span></span></td>
<td><span data-ttu-id="73976-274">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-275">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-276">6</span><span class="sxs-lookup"><span data-stu-id="73976-276">6</span></span></td>
<td><span data-ttu-id="73976-277">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-278">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="73976-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="73976-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-281">7</span><span class="sxs-lookup"><span data-stu-id="73976-281">7</span></span></td>
<td><span data-ttu-id="73976-282">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="73976-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-283">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="73976-284">-22,794.00</span></span></td>
<td><span data-ttu-id="73976-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-285">1,000.00</span></span></td>
<td><span data-ttu-id="73976-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="73976-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="73976-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="73976-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-288">8</span><span class="sxs-lookup"><span data-stu-id="73976-288">8</span></span></td>
<td><span data-ttu-id="73976-289">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="73976-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-290">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-291">94.97</span><span class="sxs-lookup"><span data-stu-id="73976-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="73976-292">94.97</span><span class="sxs-lookup"><span data-stu-id="73976-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-293">9</span><span class="sxs-lookup"><span data-stu-id="73976-293">9</span></span></td>
<td><span data-ttu-id="73976-294">Indløsning</span><span class="sxs-lookup"><span data-stu-id="73976-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-295">-1,008.00</span></span></td>
<td><span data-ttu-id="73976-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-298">10</span><span class="sxs-lookup"><span data-stu-id="73976-298">10</span></span></td>
<td><span data-ttu-id="73976-299">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="73976-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-300">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-301">949.75</span><span class="sxs-lookup"><span data-stu-id="73976-301">949.75</span></span></td>
<td><span data-ttu-id="73976-302">949.75</span><span class="sxs-lookup"><span data-stu-id="73976-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-303">11</span><span class="sxs-lookup"><span data-stu-id="73976-303">11</span></span></td>
<td><span data-ttu-id="73976-304">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="73976-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-305">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="73976-306">-949.75</span></span></td>
<td><span data-ttu-id="73976-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="73976-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73976-308">Som vist i den foregående tabel, skal der rapporteres tre kartoteker under både lovpligtig rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="73976-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="73976-309">I det lovpligtige kartotek registreres leasingbetalingen i henhold til reglerne for kontantregnskab under det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="73976-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="73976-310">Det lovpligtige tilbageførte kartotek tilbagefører de lovpligtige kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="73976-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="73976-311">IFRS 16-kartoteket opretter de kladdeposteringer, der er påkrævet i IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="73976-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="73976-312">Du skal kun angive en leasingaftale én gang.</span><span class="sxs-lookup"><span data-stu-id="73976-312">You must enter a lease only one time.</span></span> <span data-ttu-id="73976-313">Du kan derefter åbne siden **Kartoteker** for at se alle de kartoteker, der er tilknyttet leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="73976-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="73976-314">Når du opretter kartotekerne, skal de alle tre knyttes til samme leasingpost.</span><span class="sxs-lookup"><span data-stu-id="73976-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="73976-315">Den første kladdepostering registrerer leasingudgiften i henhold til det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="73976-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="73976-316">Du kan oprette betalinger enten i en batch eller ved at vælge betalingsplanen i det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="73976-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="73976-317">I dette eksempel er der oprettet følgende kladdepost for det lovpligtige kartotek fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="73976-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="73976-318">Leasingbetaling - 1/31/2020 - JE 100</span><span class="sxs-lookup"><span data-stu-id="73976-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="73976-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-319">Account type</span></span> | <span data-ttu-id="73976-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-320">Account number</span></span> | <span data-ttu-id="73976-321">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-321">Layer</span></span>   | <span data-ttu-id="73976-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-322">Account description</span></span> | <span data-ttu-id="73976-323">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-323">Debit</span></span>    | <span data-ttu-id="73976-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="73976-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-325">Ledger</span></span>       | <span data-ttu-id="73976-326">1</span><span class="sxs-lookup"><span data-stu-id="73976-326">1</span></span>              | <span data-ttu-id="73976-327">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-327">Current</span></span> | <span data-ttu-id="73976-328">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="73976-328">Lease expense</span></span>       | <span data-ttu-id="73976-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-329">1,000.00</span></span> |          |
| <span data-ttu-id="73976-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-330">Ledger</span></span>       | <span data-ttu-id="73976-331">4</span><span class="sxs-lookup"><span data-stu-id="73976-331">4</span></span>              | <span data-ttu-id="73976-332">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-332">Current</span></span> | <span data-ttu-id="73976-333">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-333">Clearing account</span></span>    |          | <span data-ttu-id="73976-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-334">1,000.00</span></span> |

<span data-ttu-id="73976-335">En kreditormedarbejder bruger standardfunktionen for Dynamics 365 til at oprette en faktura, der skal betale for leasingaftalen uden for aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="73976-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="73976-336">I stedet for at vælge **leasingudgift** som debetkonto vælger kreditormedarbejderen en clearingkonto til at generere følgende post.</span><span class="sxs-lookup"><span data-stu-id="73976-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="73976-337">AP-proces – 31/1/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="73976-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="73976-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-338">Account type</span></span> | <span data-ttu-id="73976-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-339">Account number</span></span> | <span data-ttu-id="73976-340">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-340">Layer</span></span>   | <span data-ttu-id="73976-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-341">Account description</span></span> | <span data-ttu-id="73976-342">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-342">Debit</span></span>    | <span data-ttu-id="73976-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="73976-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-344">Ledger</span></span>       | <span data-ttu-id="73976-345">4</span><span class="sxs-lookup"><span data-stu-id="73976-345">4</span></span>              | <span data-ttu-id="73976-346">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-346">Current</span></span> | <span data-ttu-id="73976-347">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-347">Clearing account</span></span>    | <span data-ttu-id="73976-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-348">1,000.00</span></span> |          |
| <span data-ttu-id="73976-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-349">Ledger</span></span>       | <span data-ttu-id="73976-350">2</span><span class="sxs-lookup"><span data-stu-id="73976-350">2</span></span>              | <span data-ttu-id="73976-351">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-351">Current</span></span> | <span data-ttu-id="73976-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="73976-352">Bank fee</span></span>            | <span data-ttu-id="73976-353">3.00</span><span class="sxs-lookup"><span data-stu-id="73976-353">3.00</span></span>     |          |
| <span data-ttu-id="73976-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-354">Ledger</span></span>       | <span data-ttu-id="73976-355">3</span><span class="sxs-lookup"><span data-stu-id="73976-355">3</span></span>              | <span data-ttu-id="73976-356">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-356">Current</span></span> | <span data-ttu-id="73976-357">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="73976-357">VAT expense</span></span>         | <span data-ttu-id="73976-358">5.00</span><span class="sxs-lookup"><span data-stu-id="73976-358">5.00</span></span>     |          |
| <span data-ttu-id="73976-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="73976-359">Vendor</span></span>       | <span data-ttu-id="73976-360">5</span><span class="sxs-lookup"><span data-stu-id="73976-360">5</span></span>              | <span data-ttu-id="73976-361">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-361">Current</span></span> | <span data-ttu-id="73976-362">Kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-362">Accounts payable</span></span>    |          | <span data-ttu-id="73976-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="73976-363">1,008.00</span></span> |

<span data-ttu-id="73976-364">Når opgørelsen er udstedt til leverandøren, skal du følge den almindelige betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="73976-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="73976-365">Under denne proces genereres følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="73976-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="73976-366">Kontant betaling – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="73976-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="73976-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-367">Account type</span></span> | <span data-ttu-id="73976-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-368">Account number</span></span> | <span data-ttu-id="73976-369">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-369">Layer</span></span>   | <span data-ttu-id="73976-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-370">Account description</span></span> | <span data-ttu-id="73976-371">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-371">Debit</span></span>    | <span data-ttu-id="73976-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="73976-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="73976-373">Vendor</span></span>       | <span data-ttu-id="73976-374">5</span><span class="sxs-lookup"><span data-stu-id="73976-374">5</span></span>              | <span data-ttu-id="73976-375">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-375">Current</span></span> | <span data-ttu-id="73976-376">Kreditorer</span><span class="sxs-lookup"><span data-stu-id="73976-376">Accounts Payable</span></span>    | <span data-ttu-id="73976-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="73976-377">1,008.00</span></span> |          |
| <span data-ttu-id="73976-378">Bank</span><span class="sxs-lookup"><span data-stu-id="73976-378">Bank</span></span>         | <span data-ttu-id="73976-379">9</span><span class="sxs-lookup"><span data-stu-id="73976-379">9</span></span>              | <span data-ttu-id="73976-380">Løbende</span><span class="sxs-lookup"><span data-stu-id="73976-380">Current</span></span> | <span data-ttu-id="73976-381">Indløsning</span><span class="sxs-lookup"><span data-stu-id="73976-381">Cash</span></span>                |          | <span data-ttu-id="73976-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="73976-382">1,008.00</span></span> |

<span data-ttu-id="73976-383">På dette tidspunkt har du taget fuld højde for denne leasingaftale under lovpligtige rapporteringskrav og kan generere en råbalance ved hjælp af det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="73976-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="73976-384">Systemet returnerer en råbalance, der har følgende tal.</span><span class="sxs-lookup"><span data-stu-id="73976-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="73976-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="73976-386">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="73976-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="73976-387">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="73976-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="73976-388">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="73976-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73976-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="73976-389">JE-100</span></span></th>
<th><span data-ttu-id="73976-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="73976-390">JE-110</span></span></th>
<th><span data-ttu-id="73976-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="73976-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73976-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="73976-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="73976-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73976-395">1</span><span class="sxs-lookup"><span data-stu-id="73976-395">1</span></span></td>
<td><span data-ttu-id="73976-396">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="73976-396">Lease expense</span></span></td>
<td><span data-ttu-id="73976-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-399">2</span><span class="sxs-lookup"><span data-stu-id="73976-399">2</span></span></td>
<td><span data-ttu-id="73976-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="73976-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="73976-401">3.00</span><span class="sxs-lookup"><span data-stu-id="73976-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-402">3.00</span><span class="sxs-lookup"><span data-stu-id="73976-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-403">3</span><span class="sxs-lookup"><span data-stu-id="73976-403">3</span></span></td>
<td><span data-ttu-id="73976-404">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="73976-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="73976-405">5.00</span><span class="sxs-lookup"><span data-stu-id="73976-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-406">5.00</span><span class="sxs-lookup"><span data-stu-id="73976-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-407">4</span><span class="sxs-lookup"><span data-stu-id="73976-407">4</span></span></td>
<td><span data-ttu-id="73976-408">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-408">Clearing account</span></span></td>
<td><span data-ttu-id="73976-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="73976-409">-1,000.00</span></span></td>
<td><span data-ttu-id="73976-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="73976-411">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-412">5</span><span class="sxs-lookup"><span data-stu-id="73976-412">5</span></span></td>
<td><span data-ttu-id="73976-413">Kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="73976-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-414">-1,008.00</span></span></td>
<td><span data-ttu-id="73976-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="73976-415">1,008.00</span></span></td>
<td><span data-ttu-id="73976-416">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-417">6</span><span class="sxs-lookup"><span data-stu-id="73976-417">6</span></span></td>
<td><span data-ttu-id="73976-418">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-419">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-420">7</span><span class="sxs-lookup"><span data-stu-id="73976-420">7</span></span></td>
<td><span data-ttu-id="73976-421">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="73976-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-422">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-423">8</span><span class="sxs-lookup"><span data-stu-id="73976-423">8</span></span></td>
<td><span data-ttu-id="73976-424">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="73976-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-425">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-426">9</span><span class="sxs-lookup"><span data-stu-id="73976-426">9</span></span></td>
<td><span data-ttu-id="73976-427">Indløsning</span><span class="sxs-lookup"><span data-stu-id="73976-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-428">-1,008.00</span></span></td>
<td><span data-ttu-id="73976-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="73976-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-430">10</span><span class="sxs-lookup"><span data-stu-id="73976-430">10</span></span></td>
<td><span data-ttu-id="73976-431">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="73976-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-432">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73976-433">11</span><span class="sxs-lookup"><span data-stu-id="73976-433">11</span></span></td>
<td><span data-ttu-id="73976-434">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="73976-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="73976-435">0,00</span><span class="sxs-lookup"><span data-stu-id="73976-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73976-436">Hvis du vil bruge IFRS 16-tal til at køre samme råbalance, skal de lovpligtige regnskabskladdeposteringer tilbageføres, og de IFRS 16-journaloptegnelser skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="73976-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="73976-437">Hvis du vil tilbageføre lovpligtige kladdeposteringer, skal dette eksempel indeholde en lovpligtig tilbageførsel, der har samme opsætning som det lovpligtige kartotek, men en modsat posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="73976-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="73976-438">Det lovpligtige kartotek har *debiteret* en konto til leasingomkostninger, men det tilbagevendende kartotek vil *kreditere* denne konto.</span><span class="sxs-lookup"><span data-stu-id="73976-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="73976-439">Disse relationer defineres nemt i bankkonti for aktivleasing på siden **Aktivleasingparametre** (**Aktivleasing \> Konfiguration \> Aktivleasingparametre**).</span><span class="sxs-lookup"><span data-stu-id="73976-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="73976-440">Når den samme proces, der blev anvendt til det lovpligtige kartotek, bruges i et tilbageført kartotek, oprettes følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="73976-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="73976-441">Forskellen er, at det tilbageførte kartotek registrerer posteringer fra det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="73976-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="73976-442">De tilbageførte posteringer foretages også i det brugerdefinerede lag.</span><span class="sxs-lookup"><span data-stu-id="73976-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="73976-443">Når der køres en råbalance på det aktuelle lag, medtages der ikke kladdeposteringer til tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="73976-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="73976-444">Leasingbetaling - 31/1/2020 - JE 130</span><span class="sxs-lookup"><span data-stu-id="73976-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="73976-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-445">Account type</span></span> | <span data-ttu-id="73976-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-446">Account number</span></span> | <span data-ttu-id="73976-447">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-447">Layer</span></span>  | <span data-ttu-id="73976-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-448">Account description</span></span> | <span data-ttu-id="73976-449">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-449">Debit</span></span>    | <span data-ttu-id="73976-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="73976-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-451">Ledger</span></span>       | <span data-ttu-id="73976-452">4</span><span class="sxs-lookup"><span data-stu-id="73976-452">4</span></span>              | <span data-ttu-id="73976-453">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-453">Custom</span></span> | <span data-ttu-id="73976-454">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-454">Clearing account</span></span>    | <span data-ttu-id="73976-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-455">1,000.00</span></span> |          |
| <span data-ttu-id="73976-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-456">Ledger</span></span>       | <span data-ttu-id="73976-457">1</span><span class="sxs-lookup"><span data-stu-id="73976-457">1</span></span>              | <span data-ttu-id="73976-458">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-458">Custom</span></span> | <span data-ttu-id="73976-459">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="73976-459">Lease expense</span></span>       |          | <span data-ttu-id="73976-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-460">1,000.00</span></span> |

<span data-ttu-id="73976-461">Nu, hvor du har elimineret lovpligtige kladdeposteringer, skal du reservere alle de kladdeposter, IFRS 16 har brug for, i IFRS 16-kartoteket.</span><span class="sxs-lookup"><span data-stu-id="73976-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="73976-462">Disse poster omfatter den første anerkendelse af ROU-aktiv og ansvarsforsikring samt posten med renter og afskrivning.</span><span class="sxs-lookup"><span data-stu-id="73976-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="73976-463">Første indregning – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="73976-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="73976-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-464">Account type</span></span> | <span data-ttu-id="73976-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-465">Account number</span></span> | <span data-ttu-id="73976-466">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-466">Layer</span></span>  | <span data-ttu-id="73976-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-467">Account description</span></span>      | <span data-ttu-id="73976-468">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-468">Debit</span></span>     | <span data-ttu-id="73976-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="73976-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-470">Ledger</span></span>       | <span data-ttu-id="73976-471">6</span><span class="sxs-lookup"><span data-stu-id="73976-471">6</span></span>              | <span data-ttu-id="73976-472">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-472">Custom</span></span> | <span data-ttu-id="73976-473">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-473">ROU Asset</span></span>                | <span data-ttu-id="73976-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="73976-474">22,793.90</span></span> |           |
| <span data-ttu-id="73976-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-475">Ledger</span></span>       | <span data-ttu-id="73976-476">7</span><span class="sxs-lookup"><span data-stu-id="73976-476">7</span></span>              | <span data-ttu-id="73976-477">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-477">Custom</span></span> | <span data-ttu-id="73976-478">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="73976-478">Finance lease obligation</span></span> |           | <span data-ttu-id="73976-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="73976-479">22,793.90</span></span> |

<span data-ttu-id="73976-480">Leasingbetalingen bogføres på samme måde som andre leasingbetalinger.</span><span class="sxs-lookup"><span data-stu-id="73976-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="73976-481">Årsagen til brug af clearing kontoen er at sikre, at kontant kun krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="73976-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="73976-482">Leasingbetaling - 31/1/2020 - JE 150</span><span class="sxs-lookup"><span data-stu-id="73976-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="73976-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-483">Account type</span></span> | <span data-ttu-id="73976-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-484">Account number</span></span> | <span data-ttu-id="73976-485">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-485">Layer</span></span>  | <span data-ttu-id="73976-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-486">Account description</span></span>      | <span data-ttu-id="73976-487">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-487">Debit</span></span>    | <span data-ttu-id="73976-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="73976-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-489">Ledger</span></span>       | <span data-ttu-id="73976-490">7</span><span class="sxs-lookup"><span data-stu-id="73976-490">7</span></span>              | <span data-ttu-id="73976-491">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-491">Custom</span></span> | <span data-ttu-id="73976-492">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="73976-492">Finance lease obligation</span></span> | <span data-ttu-id="73976-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-493">1,000.00</span></span> |          |
| <span data-ttu-id="73976-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-494">Ledger</span></span>       | <span data-ttu-id="73976-495">4</span><span class="sxs-lookup"><span data-stu-id="73976-495">4</span></span>              | <span data-ttu-id="73976-496">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-496">Custom</span></span> | <span data-ttu-id="73976-497">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-497">Clearing account</span></span>         |          | <span data-ttu-id="73976-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="73976-498">1,000.00</span></span> |

<span data-ttu-id="73976-499">Renteudgiftskladdeposten genereres fra planen for passiv afskrivning.</span><span class="sxs-lookup"><span data-stu-id="73976-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="73976-500">Renteudgift – 31/1/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="73976-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="73976-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-501">Account type</span></span> | <span data-ttu-id="73976-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-502">Account number</span></span> | <span data-ttu-id="73976-503">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-503">Layer</span></span>  | <span data-ttu-id="73976-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-504">Account description</span></span>      | <span data-ttu-id="73976-505">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-505">Debit</span></span> | <span data-ttu-id="73976-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="73976-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-507">Ledger</span></span>       | <span data-ttu-id="73976-508">8</span><span class="sxs-lookup"><span data-stu-id="73976-508">8</span></span>              | <span data-ttu-id="73976-509">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-509">Custom</span></span> | <span data-ttu-id="73976-510">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="73976-510">Interest expense</span></span>         | <span data-ttu-id="73976-511">94.97</span><span class="sxs-lookup"><span data-stu-id="73976-511">94.97</span></span> |        |
| <span data-ttu-id="73976-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-512">Ledger</span></span>       | <span data-ttu-id="73976-513">7</span><span class="sxs-lookup"><span data-stu-id="73976-513">7</span></span>              | <span data-ttu-id="73976-514">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-514">Custom</span></span> | <span data-ttu-id="73976-515">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="73976-515">Finance lease obligation</span></span> |       | <span data-ttu-id="73976-516">94.97</span><span class="sxs-lookup"><span data-stu-id="73976-516">94.97</span></span>  |

<span data-ttu-id="73976-517">Afskrivningsudgiftskladdeposten genereres fra planen for aktivafskrivning.</span><span class="sxs-lookup"><span data-stu-id="73976-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="73976-518">Afskrivningsudgift – 31/1/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="73976-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="73976-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="73976-519">Account type</span></span> | <span data-ttu-id="73976-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-520">Account number</span></span> | <span data-ttu-id="73976-521">Lag</span><span class="sxs-lookup"><span data-stu-id="73976-521">Layer</span></span>  | <span data-ttu-id="73976-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="73976-522">Account description</span></span>      | <span data-ttu-id="73976-523">Debet</span><span class="sxs-lookup"><span data-stu-id="73976-523">Debit</span></span>  | <span data-ttu-id="73976-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="73976-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="73976-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-525">Ledger</span></span>       | <span data-ttu-id="73976-526">10</span><span class="sxs-lookup"><span data-stu-id="73976-526">10</span></span>             | <span data-ttu-id="73976-527">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-527">Custom</span></span> | <span data-ttu-id="73976-528">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="73976-528">Depreciation expense</span></span>     | <span data-ttu-id="73976-529">949.75</span><span class="sxs-lookup"><span data-stu-id="73976-529">949.75</span></span> |        |
| <span data-ttu-id="73976-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="73976-530">Ledger</span></span>       | <span data-ttu-id="73976-531">11</span><span class="sxs-lookup"><span data-stu-id="73976-531">11</span></span>             | <span data-ttu-id="73976-532">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="73976-532">Custom</span></span> | <span data-ttu-id="73976-533">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="73976-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="73976-534">949.75</span><span class="sxs-lookup"><span data-stu-id="73976-534">949.75</span></span> |

<span data-ttu-id="73976-535">Når alle disse kladdeposteringer er oprettet og bogført, vises følgende værdier for "brugerdefineret lag 1".</span><span class="sxs-lookup"><span data-stu-id="73976-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="73976-536">Bemærk, at den sidste kolonne indeholder bankgebyret, momsudgiften og reduktionen af kontanter fra det foregående lag, men ikke de lovpligtige rapporteringskladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="73976-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="73976-537">Derfor opnås ægte Dual Reporting-funktioner.</span><span class="sxs-lookup"><span data-stu-id="73976-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="73976-538">På dette tidspunkt har firmaet kun brug for sin råbalance, og kombinerer det aktuelle lag og det brugerdefinerede lag for at oprette en IFRS-råbalance.</span><span class="sxs-lookup"><span data-stu-id="73976-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="73976-539">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="73976-539">Account No</span></span> | <span data-ttu-id="73976-540">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="73976-540">Description</span></span>              | <span data-ttu-id="73976-541">Lovpligtigt kartotek\-Aktuelt lag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-542">Lovpligtigt kartotek\-Aktuelt lag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-543">Lovpligtigt kartotek\-Aktuelt lag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-544">Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="73976-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="73976-545">Tilbageført kartotek\-Brugerdefineret lag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-546">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-547">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-548">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-549">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="73976-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="73976-550">Brugerdefineret lag \+ Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="73976-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="73976-551">1</span><span class="sxs-lookup"><span data-stu-id="73976-551">1</span></span>          | <span data-ttu-id="73976-552">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="73976-552">Lease expense</span></span>            | <span data-ttu-id="73976-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="73976-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="73976-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="73976-554">1,000\.00</span></span>               |   | <span data-ttu-id="73976-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="73976-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="73976-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-556">0\.00</span></span>                                   |
| <span data-ttu-id="73976-557">2</span><span class="sxs-lookup"><span data-stu-id="73976-557">2</span></span>          | <span data-ttu-id="73976-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="73976-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="73976-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="73976-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="73976-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="73976-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="73976-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="73976-561">3\.00</span></span>                                   |
| <span data-ttu-id="73976-562">3</span><span class="sxs-lookup"><span data-stu-id="73976-562">3</span></span>          | <span data-ttu-id="73976-563">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="73976-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="73976-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="73976-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="73976-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="73976-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="73976-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="73976-566">5\.00</span></span>                                   |
| <span data-ttu-id="73976-567">4</span><span class="sxs-lookup"><span data-stu-id="73976-567">4</span></span>          | <span data-ttu-id="73976-568">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="73976-568">Clearing account</span></span>         | <span data-ttu-id="73976-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="73976-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="73976-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="73976-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="73976-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-571">0\.00</span></span>                   |   | <span data-ttu-id="73976-572">1.000</span><span class="sxs-lookup"><span data-stu-id="73976-572">1,000</span></span>                                           |                                                | <span data-ttu-id="73976-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="73976-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="73976-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-574">0\.00</span></span>                                   |
| <span data-ttu-id="73976-575">5</span><span class="sxs-lookup"><span data-stu-id="73976-575">5</span></span>          | <span data-ttu-id="73976-576">Kreditor</span><span class="sxs-lookup"><span data-stu-id="73976-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="73976-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="73976-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="73976-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="73976-578">1,008\.00</span></span>                                         | <span data-ttu-id="73976-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="73976-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-580">0\.00</span></span>                                   |
| <span data-ttu-id="73976-581">6</span><span class="sxs-lookup"><span data-stu-id="73976-581">6</span></span>          | <span data-ttu-id="73976-582">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="73976-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="73976-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="73976-584">22,794</span><span class="sxs-lookup"><span data-stu-id="73976-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="73976-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="73976-585">22,793\.90</span></span>                              |
| <span data-ttu-id="73976-586">7</span><span class="sxs-lookup"><span data-stu-id="73976-586">7</span></span>          | <span data-ttu-id="73976-587">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="73976-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="73976-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="73976-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="73976-589">\-22,794</span></span>                                       | <span data-ttu-id="73976-590">1.000</span><span class="sxs-lookup"><span data-stu-id="73976-590">1,000</span></span>                                          | <span data-ttu-id="73976-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="73976-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="73976-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="73976-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="73976-593">8</span><span class="sxs-lookup"><span data-stu-id="73976-593">8</span></span>          | <span data-ttu-id="73976-594">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="73976-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="73976-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="73976-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="73976-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="73976-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="73976-597">94\.97</span></span>                                  |
| <span data-ttu-id="73976-598">9</span><span class="sxs-lookup"><span data-stu-id="73976-598">9</span></span>          | <span data-ttu-id="73976-599">Indløsning</span><span class="sxs-lookup"><span data-stu-id="73976-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="73976-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="73976-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="73976-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="73976-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="73976-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="73976-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="73976-603">10</span><span class="sxs-lookup"><span data-stu-id="73976-603">10</span></span>         | <span data-ttu-id="73976-604">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="73976-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="73976-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="73976-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="73976-606">949\.75</span></span>                                        | <span data-ttu-id="73976-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="73976-607">949\.75</span></span>                                 |
| <span data-ttu-id="73976-608">11</span><span class="sxs-lookup"><span data-stu-id="73976-608">11</span></span>         | <span data-ttu-id="73976-609">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="73976-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="73976-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="73976-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="73976-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="73976-611">\-949\.75</span></span>                                      | <span data-ttu-id="73976-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="73976-612">\-949\.75</span></span>                               |


