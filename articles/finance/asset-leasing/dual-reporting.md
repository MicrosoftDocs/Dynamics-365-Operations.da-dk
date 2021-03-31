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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229544"
---
# <a name="dual-reporting"></a><span data-ttu-id="4030c-103">Dobbeltrapportering</span><span class="sxs-lookup"><span data-stu-id="4030c-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4030c-104">I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="4030c-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="4030c-105">Det er nødvendigt med kendskab til posteringslag i Microsoft Dynamics 365 Finance, og det vil gøre det nemmere at forstå i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="4030c-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="4030c-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4030c-106">Example</span></span>

<span data-ttu-id="4030c-107">Følgende eksempelkonti til en leaseaftale under italiensk lovpligtig rapportering ved hjælp af både likviditetsmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="4030c-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="4030c-108">Firmaet skal etablere tre kartoteker for at kunne redegøre for både de italienske lovpligtige krav og IFRS 16-krav.</span><span class="sxs-lookup"><span data-stu-id="4030c-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="4030c-109">Der kræves et kartotek til IFRS 16, et kartotek til lovpligtige krav, og et kartotek til automatisk tilbageføring af lovpligtige bogføringer.</span><span class="sxs-lookup"><span data-stu-id="4030c-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="4030c-110">Kartotekerne oprettes som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="4030c-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="4030c-111">**IFRS 16-kartotek**</span><span class="sxs-lookup"><span data-stu-id="4030c-111">**IFRS 16 book**</span></span>

<span data-ttu-id="4030c-112">IFRS 16-kartoteket er konfigureret, så det overholder IFRS 16-regnskabsstandarden.</span><span class="sxs-lookup"><span data-stu-id="4030c-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="4030c-113">Alle poster, der er bogført i dette kartotek, bogføres i et brugerdefineret lag.</span><span class="sxs-lookup"><span data-stu-id="4030c-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="4030c-114">Navn</span><span class="sxs-lookup"><span data-stu-id="4030c-114">Name</span></span>                                    | <span data-ttu-id="4030c-115">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4030c-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="4030c-116">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="4030c-116">Book type</span></span>                               | <span data-ttu-id="4030c-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4030c-117">IFRS 16</span></span>        |
| <span data-ttu-id="4030c-118">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-118">Book description</span></span>                        | <span data-ttu-id="4030c-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4030c-119">IFRS 16</span></span>        |
| <span data-ttu-id="4030c-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="4030c-120">Posting Layer</span></span>                           | <span data-ttu-id="4030c-121">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="4030c-121">Custom layer 1</span></span> |
| <span data-ttu-id="4030c-122">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="4030c-122">Lease Type</span></span>                              | <span data-ttu-id="4030c-123">Finance</span><span class="sxs-lookup"><span data-stu-id="4030c-123">Finance</span></span>        |
| <span data-ttu-id="4030c-124">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="4030c-124">Accounting Framework</span></span>                    | <span data-ttu-id="4030c-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="4030c-125">IFRS 16</span></span>        |
| <span data-ttu-id="4030c-126">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="4030c-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4030c-127">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-127">0.00</span></span>           |
| <span data-ttu-id="4030c-128">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4030c-129">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-129">0.00</span></span>           |
| <span data-ttu-id="4030c-130">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="4030c-130">Short-term threshold</span></span>                    | <span data-ttu-id="4030c-131">12</span><span class="sxs-lookup"><span data-stu-id="4030c-131">12</span></span>             |
| <span data-ttu-id="4030c-132">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="4030c-132">Low Value Threshold</span></span>                     | <span data-ttu-id="4030c-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-133">5,000.00</span></span>       |
| <span data-ttu-id="4030c-134">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-134">Pay to Vendor</span></span>                           | <span data-ttu-id="4030c-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="4030c-135">No</span></span>             |

<span data-ttu-id="4030c-136">**Lovpligtigt kartotek**</span><span class="sxs-lookup"><span data-stu-id="4030c-136">**Statutory book**</span></span>

<span data-ttu-id="4030c-137">Det lovpligtige kartotek er en kassekladde, hvor firmaet kan redegøre for leasingudgifter som det kontantbeløb, der betales hver måned for leje.</span><span class="sxs-lookup"><span data-stu-id="4030c-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="4030c-138">Dette kartotek opretter ikke et ROU-aktiv eller en leasingforpligtelse.</span><span class="sxs-lookup"><span data-stu-id="4030c-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="4030c-139">Navn</span><span class="sxs-lookup"><span data-stu-id="4030c-139">Name</span></span>                                    | <span data-ttu-id="4030c-140">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4030c-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="4030c-141">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="4030c-141">Book type</span></span>                               | <span data-ttu-id="4030c-142">Lovpligtig</span><span class="sxs-lookup"><span data-stu-id="4030c-142">Statutory</span></span>   |
| <span data-ttu-id="4030c-143">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-143">Book description</span></span>                        | <span data-ttu-id="4030c-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="4030c-144">Local GAAP</span></span>  |
| <span data-ttu-id="4030c-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="4030c-145">Posting Layer</span></span>                           | <span data-ttu-id="4030c-146">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-146">Current</span></span>     |
| <span data-ttu-id="4030c-147">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="4030c-147">Lease Type</span></span>                              | <span data-ttu-id="4030c-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="4030c-148">Automatic</span></span>   |
| <span data-ttu-id="4030c-149">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="4030c-149">Accounting Framework</span></span>                    | <span data-ttu-id="4030c-150">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="4030c-150">Cash basis</span></span>  |
| <span data-ttu-id="4030c-151">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="4030c-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4030c-152">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-152">0.00</span></span>        |
| <span data-ttu-id="4030c-153">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4030c-154">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-154">0.00</span></span>        |
| <span data-ttu-id="4030c-155">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="4030c-155">Short-term threshold</span></span>                    | <span data-ttu-id="4030c-156">0</span><span class="sxs-lookup"><span data-stu-id="4030c-156">0</span></span>           |
| <span data-ttu-id="4030c-157">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="4030c-157">Low Value Threshold</span></span>                     | <span data-ttu-id="4030c-158">0</span><span class="sxs-lookup"><span data-stu-id="4030c-158">0</span></span>           |
| <span data-ttu-id="4030c-159">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-159">Pay to Vendor</span></span>                           | <span data-ttu-id="4030c-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="4030c-160">No</span></span>          |

<span data-ttu-id="4030c-161">**Lovpligtigt tilbageført kartotek**</span><span class="sxs-lookup"><span data-stu-id="4030c-161">**Statutory reversal book**</span></span>

<span data-ttu-id="4030c-162">Det lovpligtige tilbageførte kartotek konfigureres på samme måde som det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="4030c-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="4030c-163">Navn</span><span class="sxs-lookup"><span data-stu-id="4030c-163">Name</span></span>                                    | <span data-ttu-id="4030c-164">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4030c-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="4030c-165">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="4030c-165">Book type</span></span>                               | <span data-ttu-id="4030c-166">Lovpligtig - tilbageført</span><span class="sxs-lookup"><span data-stu-id="4030c-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="4030c-167">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-167">Book description</span></span>                        | <span data-ttu-id="4030c-168">Kartotek, der skal tilbageføre lovpligtigt kartotek</span><span class="sxs-lookup"><span data-stu-id="4030c-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="4030c-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="4030c-169">Posting Layer</span></span>                           | <span data-ttu-id="4030c-170">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="4030c-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="4030c-171">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="4030c-171">Lease Type</span></span>                              | <span data-ttu-id="4030c-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="4030c-172">Automatic</span></span>                      |
| <span data-ttu-id="4030c-173">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="4030c-173">Accounting Framework</span></span>                    | <span data-ttu-id="4030c-174">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="4030c-174">Cash basis</span></span>                     |
| <span data-ttu-id="4030c-175">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="4030c-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="4030c-176">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-176">0.00</span></span>                           |
| <span data-ttu-id="4030c-177">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="4030c-178">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-178">0.00</span></span>                           |
| <span data-ttu-id="4030c-179">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="4030c-179">Short-term threshold</span></span>                    | <span data-ttu-id="4030c-180">0</span><span class="sxs-lookup"><span data-stu-id="4030c-180">0</span></span>                              |
| <span data-ttu-id="4030c-181">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="4030c-181">Low Value Threshold</span></span>                     | <span data-ttu-id="4030c-182">0</span><span class="sxs-lookup"><span data-stu-id="4030c-182">0</span></span>                              |
| <span data-ttu-id="4030c-183">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-183">Pay to Vendor</span></span>                           | <span data-ttu-id="4030c-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="4030c-184">No</span></span>                             |

<span data-ttu-id="4030c-185">I dette eksempel er der oprettet en leasingaftale, der indeholder følgende indstillinger under fanerne **Generelt** og **Betalingsplanlinje**.</span><span class="sxs-lookup"><span data-stu-id="4030c-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="4030c-186">Fanen **Generelt**</span><span class="sxs-lookup"><span data-stu-id="4030c-186">**General tab**</span></span>

| <span data-ttu-id="4030c-187">Felt</span><span class="sxs-lookup"><span data-stu-id="4030c-187">Field</span></span>                      | <span data-ttu-id="4030c-188">Værdi</span><span class="sxs-lookup"><span data-stu-id="4030c-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="4030c-189">Trinvis lånesats</span><span class="sxs-lookup"><span data-stu-id="4030c-189">Incremental borrowing rate</span></span> | <span data-ttu-id="4030c-190">5 %</span><span class="sxs-lookup"><span data-stu-id="4030c-190">5%</span></span>               |
| <span data-ttu-id="4030c-191">Dato for påbegyndelse</span><span class="sxs-lookup"><span data-stu-id="4030c-191">Commencement date</span></span>          | <span data-ttu-id="4030c-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="4030c-192">1/1/2020</span></span>         |
| <span data-ttu-id="4030c-193">Leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="4030c-193">Lease group</span></span>                | <span data-ttu-id="4030c-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="4030c-194">Buildings</span></span>        |
| <span data-ttu-id="4030c-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="4030c-195">Vendor</span></span>                     | <span data-ttu-id="4030c-196">1001</span><span class="sxs-lookup"><span data-stu-id="4030c-196">1001</span></span>             |
| <span data-ttu-id="4030c-197">Aktivets handelsværdi</span><span class="sxs-lookup"><span data-stu-id="4030c-197">Fair value of the asset</span></span>    | <span data-ttu-id="4030c-198">245,000</span><span class="sxs-lookup"><span data-stu-id="4030c-198">245,000</span></span>          |
| <span data-ttu-id="4030c-199">Brugstid for aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-199">Asset useful life</span></span>          | <span data-ttu-id="4030c-200">120</span><span class="sxs-lookup"><span data-stu-id="4030c-200">120</span></span>              |
| <span data-ttu-id="4030c-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="4030c-201">Annuity type</span></span>               | <span data-ttu-id="4030c-202">Almindelig annuitet</span><span class="sxs-lookup"><span data-stu-id="4030c-202">Ordinary annuity</span></span> |
| <span data-ttu-id="4030c-203">Sammensætningsinterval</span><span class="sxs-lookup"><span data-stu-id="4030c-203">Compounding interval</span></span>       | <span data-ttu-id="4030c-204">Månedligt</span><span class="sxs-lookup"><span data-stu-id="4030c-204">Monthly</span></span>          |

<span data-ttu-id="4030c-205">**Betalingsplanlinjer-fane**</span><span class="sxs-lookup"><span data-stu-id="4030c-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="4030c-206">Felt</span><span class="sxs-lookup"><span data-stu-id="4030c-206">Field</span></span>             | <span data-ttu-id="4030c-207">Værdi</span><span class="sxs-lookup"><span data-stu-id="4030c-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="4030c-208">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="4030c-208">Start date</span></span>        | <span data-ttu-id="4030c-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="4030c-209">1/1/2020</span></span>   |
| <span data-ttu-id="4030c-210">Periodeinterval</span><span class="sxs-lookup"><span data-stu-id="4030c-210">Period interval</span></span>   | <span data-ttu-id="4030c-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="4030c-211">Months</span></span>     |
| <span data-ttu-id="4030c-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="4030c-212">Periods</span></span>           | <span data-ttu-id="4030c-213">24</span><span class="sxs-lookup"><span data-stu-id="4030c-213">24</span></span>         |
| <span data-ttu-id="4030c-214">Slutdato</span><span class="sxs-lookup"><span data-stu-id="4030c-214">End date</span></span>          | <span data-ttu-id="4030c-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="4030c-215">12/31/2020</span></span> |
| <span data-ttu-id="4030c-216">Betalingshyppighed</span><span class="sxs-lookup"><span data-stu-id="4030c-216">Payment frequency</span></span> | <span data-ttu-id="4030c-217">Månedligt</span><span class="sxs-lookup"><span data-stu-id="4030c-217">Monthly</span></span>    |
| <span data-ttu-id="4030c-218">Betalingsbeløb</span><span class="sxs-lookup"><span data-stu-id="4030c-218">Payment amount</span></span>    | <span data-ttu-id="4030c-219">1.000</span><span class="sxs-lookup"><span data-stu-id="4030c-219">1,000</span></span>      |

<span data-ttu-id="4030c-220">Hvis du vil redegøre for denne leasingaftale i forbindelse med to strukturer, skal du bruge et aktuelt posteringslag og et brugerdefineret posteringslag.</span><span class="sxs-lookup"><span data-stu-id="4030c-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="4030c-221">Følgende tabel viser et eksempel på hver kladdepost, der er nødvendig for at repræsentere finanserne i de enkelte rapporteringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="4030c-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="4030c-222">En detaljeret beskrivelse af de enkelte kladdeposter for den første måned af leasingaftalen tildeles bagefter.</span><span class="sxs-lookup"><span data-stu-id="4030c-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="4030c-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="4030c-224">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4030c-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="4030c-225">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="4030c-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4030c-226">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="4030c-226">Current layer total</span></span></th>
<th><span data-ttu-id="4030c-227">Tilbageført kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="4030c-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="4030c-228">IFRS 16-kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="4030c-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4030c-229">Aktuelt lag + brugerdefineret lag i alt</span><span class="sxs-lookup"><span data-stu-id="4030c-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4030c-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="4030c-230">JE-100</span></span></th>
<th><span data-ttu-id="4030c-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="4030c-231">JE-110</span></span></th>
<th><span data-ttu-id="4030c-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="4030c-232">JE-120</span></span></th>
<th><span data-ttu-id="4030c-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="4030c-233">JE-130</span></span></th>
<th><span data-ttu-id="4030c-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="4030c-234">JE-140</span></span></th>
<th><span data-ttu-id="4030c-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="4030c-235">JE-150</span></span></th>
<th><span data-ttu-id="4030c-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="4030c-236">JE-160</span></span></th>
<th><span data-ttu-id="4030c-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="4030c-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4030c-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4030c-246">1</span><span class="sxs-lookup"><span data-stu-id="4030c-246">1</span></span></td>
<td><span data-ttu-id="4030c-247">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-247">Lease expense</span></span></td>
<td><span data-ttu-id="4030c-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-249">1,000.00</span></span></td>
<td><span data-ttu-id="4030c-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4030c-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-251">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-252">2</span><span class="sxs-lookup"><span data-stu-id="4030c-252">2</span></span></td>
<td><span data-ttu-id="4030c-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="4030c-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-254">3.00</span><span class="sxs-lookup"><span data-stu-id="4030c-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-255">3.00</span><span class="sxs-lookup"><span data-stu-id="4030c-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-256">3.00</span><span class="sxs-lookup"><span data-stu-id="4030c-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-257">3</span><span class="sxs-lookup"><span data-stu-id="4030c-257">3</span></span></td>
<td><span data-ttu-id="4030c-258">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-259">5.00</span><span class="sxs-lookup"><span data-stu-id="4030c-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-260">5.00</span><span class="sxs-lookup"><span data-stu-id="4030c-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-261">5.00</span><span class="sxs-lookup"><span data-stu-id="4030c-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-262">4</span><span class="sxs-lookup"><span data-stu-id="4030c-262">4</span></span></td>
<td><span data-ttu-id="4030c-263">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-263">Clearing account</span></span></td>
<td><span data-ttu-id="4030c-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4030c-264">-1,000.00</span></span></td>
<td><span data-ttu-id="4030c-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-266">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-266">0.00</span></span></td>
<td><span data-ttu-id="4030c-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4030c-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-269">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-270">5</span><span class="sxs-lookup"><span data-stu-id="4030c-270">5</span></span></td>
<td><span data-ttu-id="4030c-271">Kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-272">-1,008.00</span></span></td>
<td><span data-ttu-id="4030c-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4030c-273">1,008.00</span></span></td>
<td><span data-ttu-id="4030c-274">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-275">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-276">6</span><span class="sxs-lookup"><span data-stu-id="4030c-276">6</span></span></td>
<td><span data-ttu-id="4030c-277">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-278">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="4030c-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4030c-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-281">7</span><span class="sxs-lookup"><span data-stu-id="4030c-281">7</span></span></td>
<td><span data-ttu-id="4030c-282">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="4030c-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="4030c-284">-22,794.00</span></span></td>
<td><span data-ttu-id="4030c-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-285">1,000.00</span></span></td>
<td><span data-ttu-id="4030c-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="4030c-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="4030c-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-288">8</span><span class="sxs-lookup"><span data-stu-id="4030c-288">8</span></span></td>
<td><span data-ttu-id="4030c-289">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-290">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-291">94.97</span><span class="sxs-lookup"><span data-stu-id="4030c-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-292">94.97</span><span class="sxs-lookup"><span data-stu-id="4030c-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-293">9</span><span class="sxs-lookup"><span data-stu-id="4030c-293">9</span></span></td>
<td><span data-ttu-id="4030c-294">Indløsning</span><span class="sxs-lookup"><span data-stu-id="4030c-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-295">-1,008.00</span></span></td>
<td><span data-ttu-id="4030c-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-298">10</span><span class="sxs-lookup"><span data-stu-id="4030c-298">10</span></span></td>
<td><span data-ttu-id="4030c-299">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="4030c-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-300">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-301">949.75</span><span class="sxs-lookup"><span data-stu-id="4030c-301">949.75</span></span></td>
<td><span data-ttu-id="4030c-302">949.75</span><span class="sxs-lookup"><span data-stu-id="4030c-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-303">11</span><span class="sxs-lookup"><span data-stu-id="4030c-303">11</span></span></td>
<td><span data-ttu-id="4030c-304">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="4030c-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-305">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="4030c-306">-949.75</span></span></td>
<td><span data-ttu-id="4030c-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="4030c-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4030c-308">Som vist i den foregående tabel, skal der rapporteres tre kartoteker under både lovpligtig rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="4030c-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="4030c-309">I det lovpligtige kartotek registreres leasingbetalingen i henhold til reglerne for kontantregnskab under det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="4030c-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="4030c-310">Det lovpligtige tilbageførte kartotek tilbagefører de lovpligtige kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="4030c-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="4030c-311">IFRS 16-kartoteket opretter de kladdeposteringer, der er påkrævet i IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="4030c-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="4030c-312">Du skal kun angive en leasingaftale én gang.</span><span class="sxs-lookup"><span data-stu-id="4030c-312">You must enter a lease only one time.</span></span> <span data-ttu-id="4030c-313">Du kan derefter åbne siden **Kartoteker** for at se alle de kartoteker, der er tilknyttet leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="4030c-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="4030c-314">Når du opretter kartotekerne, skal de alle tre knyttes til samme leasingpost.</span><span class="sxs-lookup"><span data-stu-id="4030c-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="4030c-315">Den første kladdepostering registrerer leasingudgiften i henhold til det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="4030c-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="4030c-316">Du kan oprette betalinger enten i en batch eller ved at vælge betalingsplanen i det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="4030c-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="4030c-317">I dette eksempel er der oprettet følgende kladdepost for det lovpligtige kartotek fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="4030c-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="4030c-318">Leasingbetaling - 1/31/2020 - JE 100</span><span class="sxs-lookup"><span data-stu-id="4030c-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="4030c-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-319">Account type</span></span> | <span data-ttu-id="4030c-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-320">Account number</span></span> | <span data-ttu-id="4030c-321">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-321">Layer</span></span>   | <span data-ttu-id="4030c-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-322">Account description</span></span> | <span data-ttu-id="4030c-323">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-323">Debit</span></span>    | <span data-ttu-id="4030c-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4030c-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-325">Ledger</span></span>       | <span data-ttu-id="4030c-326">1</span><span class="sxs-lookup"><span data-stu-id="4030c-326">1</span></span>              | <span data-ttu-id="4030c-327">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-327">Current</span></span> | <span data-ttu-id="4030c-328">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-328">Lease expense</span></span>       | <span data-ttu-id="4030c-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-329">1,000.00</span></span> |          |
| <span data-ttu-id="4030c-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-330">Ledger</span></span>       | <span data-ttu-id="4030c-331">4</span><span class="sxs-lookup"><span data-stu-id="4030c-331">4</span></span>              | <span data-ttu-id="4030c-332">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-332">Current</span></span> | <span data-ttu-id="4030c-333">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-333">Clearing account</span></span>    |          | <span data-ttu-id="4030c-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-334">1,000.00</span></span> |

<span data-ttu-id="4030c-335">En kreditormedarbejder bruger standardfunktionen for Dynamics 365 til at oprette en faktura, der skal betale for leasingaftalen uden for aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="4030c-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="4030c-336">I stedet for at vælge **leasingudgift** som debetkonto vælger kreditormedarbejderen en clearingkonto til at generere følgende post.</span><span class="sxs-lookup"><span data-stu-id="4030c-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="4030c-337">AP-proces – 31/1/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="4030c-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="4030c-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-338">Account type</span></span> | <span data-ttu-id="4030c-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-339">Account number</span></span> | <span data-ttu-id="4030c-340">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-340">Layer</span></span>   | <span data-ttu-id="4030c-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-341">Account description</span></span> | <span data-ttu-id="4030c-342">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-342">Debit</span></span>    | <span data-ttu-id="4030c-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4030c-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-344">Ledger</span></span>       | <span data-ttu-id="4030c-345">4</span><span class="sxs-lookup"><span data-stu-id="4030c-345">4</span></span>              | <span data-ttu-id="4030c-346">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-346">Current</span></span> | <span data-ttu-id="4030c-347">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-347">Clearing account</span></span>    | <span data-ttu-id="4030c-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-348">1,000.00</span></span> |          |
| <span data-ttu-id="4030c-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-349">Ledger</span></span>       | <span data-ttu-id="4030c-350">2</span><span class="sxs-lookup"><span data-stu-id="4030c-350">2</span></span>              | <span data-ttu-id="4030c-351">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-351">Current</span></span> | <span data-ttu-id="4030c-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="4030c-352">Bank fee</span></span>            | <span data-ttu-id="4030c-353">3.00</span><span class="sxs-lookup"><span data-stu-id="4030c-353">3.00</span></span>     |          |
| <span data-ttu-id="4030c-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-354">Ledger</span></span>       | <span data-ttu-id="4030c-355">3</span><span class="sxs-lookup"><span data-stu-id="4030c-355">3</span></span>              | <span data-ttu-id="4030c-356">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-356">Current</span></span> | <span data-ttu-id="4030c-357">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-357">VAT expense</span></span>         | <span data-ttu-id="4030c-358">5.00</span><span class="sxs-lookup"><span data-stu-id="4030c-358">5.00</span></span>     |          |
| <span data-ttu-id="4030c-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="4030c-359">Vendor</span></span>       | <span data-ttu-id="4030c-360">5</span><span class="sxs-lookup"><span data-stu-id="4030c-360">5</span></span>              | <span data-ttu-id="4030c-361">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-361">Current</span></span> | <span data-ttu-id="4030c-362">Kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-362">Accounts payable</span></span>    |          | <span data-ttu-id="4030c-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4030c-363">1,008.00</span></span> |

<span data-ttu-id="4030c-364">Når opgørelsen er udstedt til leverandøren, skal du følge den almindelige betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="4030c-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="4030c-365">Under denne proces genereres følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="4030c-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="4030c-366">Kontant betaling – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="4030c-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="4030c-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-367">Account type</span></span> | <span data-ttu-id="4030c-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-368">Account number</span></span> | <span data-ttu-id="4030c-369">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-369">Layer</span></span>   | <span data-ttu-id="4030c-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-370">Account description</span></span> | <span data-ttu-id="4030c-371">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-371">Debit</span></span>    | <span data-ttu-id="4030c-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="4030c-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="4030c-373">Vendor</span></span>       | <span data-ttu-id="4030c-374">5</span><span class="sxs-lookup"><span data-stu-id="4030c-374">5</span></span>              | <span data-ttu-id="4030c-375">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-375">Current</span></span> | <span data-ttu-id="4030c-376">Kreditorer</span><span class="sxs-lookup"><span data-stu-id="4030c-376">Accounts Payable</span></span>    | <span data-ttu-id="4030c-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4030c-377">1,008.00</span></span> |          |
| <span data-ttu-id="4030c-378">Bank</span><span class="sxs-lookup"><span data-stu-id="4030c-378">Bank</span></span>         | <span data-ttu-id="4030c-379">9</span><span class="sxs-lookup"><span data-stu-id="4030c-379">9</span></span>              | <span data-ttu-id="4030c-380">Løbende</span><span class="sxs-lookup"><span data-stu-id="4030c-380">Current</span></span> | <span data-ttu-id="4030c-381">Indløsning</span><span class="sxs-lookup"><span data-stu-id="4030c-381">Cash</span></span>                |          | <span data-ttu-id="4030c-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4030c-382">1,008.00</span></span> |

<span data-ttu-id="4030c-383">På dette tidspunkt har du taget fuld højde for denne leasingaftale under lovpligtige rapporteringskrav og kan generere en råbalance ved hjælp af det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="4030c-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="4030c-384">Systemet returnerer en råbalance, der har følgende tal.</span><span class="sxs-lookup"><span data-stu-id="4030c-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="4030c-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="4030c-386">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4030c-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="4030c-387">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="4030c-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="4030c-388">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="4030c-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4030c-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="4030c-389">JE-100</span></span></th>
<th><span data-ttu-id="4030c-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="4030c-390">JE-110</span></span></th>
<th><span data-ttu-id="4030c-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="4030c-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4030c-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="4030c-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="4030c-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4030c-395">1</span><span class="sxs-lookup"><span data-stu-id="4030c-395">1</span></span></td>
<td><span data-ttu-id="4030c-396">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-396">Lease expense</span></span></td>
<td><span data-ttu-id="4030c-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-399">2</span><span class="sxs-lookup"><span data-stu-id="4030c-399">2</span></span></td>
<td><span data-ttu-id="4030c-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="4030c-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-401">3.00</span><span class="sxs-lookup"><span data-stu-id="4030c-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-402">3.00</span><span class="sxs-lookup"><span data-stu-id="4030c-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-403">3</span><span class="sxs-lookup"><span data-stu-id="4030c-403">3</span></span></td>
<td><span data-ttu-id="4030c-404">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-405">5.00</span><span class="sxs-lookup"><span data-stu-id="4030c-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-406">5.00</span><span class="sxs-lookup"><span data-stu-id="4030c-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-407">4</span><span class="sxs-lookup"><span data-stu-id="4030c-407">4</span></span></td>
<td><span data-ttu-id="4030c-408">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-408">Clearing account</span></span></td>
<td><span data-ttu-id="4030c-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4030c-409">-1,000.00</span></span></td>
<td><span data-ttu-id="4030c-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-411">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-412">5</span><span class="sxs-lookup"><span data-stu-id="4030c-412">5</span></span></td>
<td><span data-ttu-id="4030c-413">Kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="4030c-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-414">-1,008.00</span></span></td>
<td><span data-ttu-id="4030c-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="4030c-415">1,008.00</span></span></td>
<td><span data-ttu-id="4030c-416">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-417">6</span><span class="sxs-lookup"><span data-stu-id="4030c-417">6</span></span></td>
<td><span data-ttu-id="4030c-418">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-419">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-420">7</span><span class="sxs-lookup"><span data-stu-id="4030c-420">7</span></span></td>
<td><span data-ttu-id="4030c-421">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="4030c-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-422">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-423">8</span><span class="sxs-lookup"><span data-stu-id="4030c-423">8</span></span></td>
<td><span data-ttu-id="4030c-424">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-425">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-426">9</span><span class="sxs-lookup"><span data-stu-id="4030c-426">9</span></span></td>
<td><span data-ttu-id="4030c-427">Indløsning</span><span class="sxs-lookup"><span data-stu-id="4030c-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-428">-1,008.00</span></span></td>
<td><span data-ttu-id="4030c-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="4030c-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-430">10</span><span class="sxs-lookup"><span data-stu-id="4030c-430">10</span></span></td>
<td><span data-ttu-id="4030c-431">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="4030c-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-432">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4030c-433">11</span><span class="sxs-lookup"><span data-stu-id="4030c-433">11</span></span></td>
<td><span data-ttu-id="4030c-434">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="4030c-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="4030c-435">0,00</span><span class="sxs-lookup"><span data-stu-id="4030c-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4030c-436">Hvis du vil bruge IFRS 16-tal til at køre samme råbalance, skal de lovpligtige regnskabskladdeposteringer tilbageføres, og de IFRS 16-journaloptegnelser skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="4030c-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="4030c-437">Hvis du vil tilbageføre lovpligtige kladdeposteringer, skal dette eksempel indeholde en lovpligtig tilbageførsel, der har samme opsætning som det lovpligtige kartotek, men en modsat posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="4030c-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="4030c-438">Det lovpligtige kartotek har *debiteret* en konto til leasingomkostninger, men det tilbagevendende kartotek vil *kreditere* denne konto.</span><span class="sxs-lookup"><span data-stu-id="4030c-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="4030c-439">Disse relationer defineres nemt i bankkonti for aktivleasing på siden **Aktivleasingparametre** (**Aktivleasing \> Konfiguration \> Aktivleasingparametre**).</span><span class="sxs-lookup"><span data-stu-id="4030c-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="4030c-440">Når den samme proces, der blev anvendt til det lovpligtige kartotek, bruges i et tilbageført kartotek, oprettes følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="4030c-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="4030c-441">Forskellen er, at det tilbageførte kartotek registrerer posteringer fra det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="4030c-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="4030c-442">De tilbageførte posteringer foretages også i det brugerdefinerede lag.</span><span class="sxs-lookup"><span data-stu-id="4030c-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="4030c-443">Når der køres en råbalance på det aktuelle lag, medtages der ikke kladdeposteringer til tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="4030c-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="4030c-444">Leasingbetaling - 31/1/2020 - JE 130</span><span class="sxs-lookup"><span data-stu-id="4030c-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="4030c-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-445">Account type</span></span> | <span data-ttu-id="4030c-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-446">Account number</span></span> | <span data-ttu-id="4030c-447">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-447">Layer</span></span>  | <span data-ttu-id="4030c-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-448">Account description</span></span> | <span data-ttu-id="4030c-449">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-449">Debit</span></span>    | <span data-ttu-id="4030c-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="4030c-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-451">Ledger</span></span>       | <span data-ttu-id="4030c-452">4</span><span class="sxs-lookup"><span data-stu-id="4030c-452">4</span></span>              | <span data-ttu-id="4030c-453">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-453">Custom</span></span> | <span data-ttu-id="4030c-454">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-454">Clearing account</span></span>    | <span data-ttu-id="4030c-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-455">1,000.00</span></span> |          |
| <span data-ttu-id="4030c-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-456">Ledger</span></span>       | <span data-ttu-id="4030c-457">1</span><span class="sxs-lookup"><span data-stu-id="4030c-457">1</span></span>              | <span data-ttu-id="4030c-458">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-458">Custom</span></span> | <span data-ttu-id="4030c-459">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-459">Lease expense</span></span>       |          | <span data-ttu-id="4030c-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-460">1,000.00</span></span> |

<span data-ttu-id="4030c-461">Nu, hvor du har elimineret lovpligtige kladdeposteringer, skal du reservere alle de kladdeposter, IFRS 16 har brug for, i IFRS 16-kartoteket.</span><span class="sxs-lookup"><span data-stu-id="4030c-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="4030c-462">Disse poster omfatter den første anerkendelse af ROU-aktiv og ansvarsforsikring samt posten med renter og afskrivning.</span><span class="sxs-lookup"><span data-stu-id="4030c-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="4030c-463">Første indregning – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="4030c-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="4030c-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-464">Account type</span></span> | <span data-ttu-id="4030c-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-465">Account number</span></span> | <span data-ttu-id="4030c-466">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-466">Layer</span></span>  | <span data-ttu-id="4030c-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-467">Account description</span></span>      | <span data-ttu-id="4030c-468">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-468">Debit</span></span>     | <span data-ttu-id="4030c-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="4030c-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-470">Ledger</span></span>       | <span data-ttu-id="4030c-471">6</span><span class="sxs-lookup"><span data-stu-id="4030c-471">6</span></span>              | <span data-ttu-id="4030c-472">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-472">Custom</span></span> | <span data-ttu-id="4030c-473">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-473">ROU Asset</span></span>                | <span data-ttu-id="4030c-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4030c-474">22,793.90</span></span> |           |
| <span data-ttu-id="4030c-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-475">Ledger</span></span>       | <span data-ttu-id="4030c-476">7</span><span class="sxs-lookup"><span data-stu-id="4030c-476">7</span></span>              | <span data-ttu-id="4030c-477">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-477">Custom</span></span> | <span data-ttu-id="4030c-478">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="4030c-478">Finance lease obligation</span></span> |           | <span data-ttu-id="4030c-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="4030c-479">22,793.90</span></span> |

<span data-ttu-id="4030c-480">Leasingbetalingen bogføres på samme måde som andre leasingbetalinger.</span><span class="sxs-lookup"><span data-stu-id="4030c-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="4030c-481">Årsagen til brug af clearing kontoen er at sikre, at kontant kun krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="4030c-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="4030c-482">Leasingbetaling - 31/1/2020 - JE 150</span><span class="sxs-lookup"><span data-stu-id="4030c-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="4030c-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-483">Account type</span></span> | <span data-ttu-id="4030c-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-484">Account number</span></span> | <span data-ttu-id="4030c-485">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-485">Layer</span></span>  | <span data-ttu-id="4030c-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-486">Account description</span></span>      | <span data-ttu-id="4030c-487">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-487">Debit</span></span>    | <span data-ttu-id="4030c-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="4030c-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-489">Ledger</span></span>       | <span data-ttu-id="4030c-490">7</span><span class="sxs-lookup"><span data-stu-id="4030c-490">7</span></span>              | <span data-ttu-id="4030c-491">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-491">Custom</span></span> | <span data-ttu-id="4030c-492">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="4030c-492">Finance lease obligation</span></span> | <span data-ttu-id="4030c-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-493">1,000.00</span></span> |          |
| <span data-ttu-id="4030c-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-494">Ledger</span></span>       | <span data-ttu-id="4030c-495">4</span><span class="sxs-lookup"><span data-stu-id="4030c-495">4</span></span>              | <span data-ttu-id="4030c-496">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-496">Custom</span></span> | <span data-ttu-id="4030c-497">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-497">Clearing account</span></span>         |          | <span data-ttu-id="4030c-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4030c-498">1,000.00</span></span> |

<span data-ttu-id="4030c-499">Renteudgiftskladdeposten genereres fra planen for passiv afskrivning.</span><span class="sxs-lookup"><span data-stu-id="4030c-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="4030c-500">Renteudgift – 31/1/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="4030c-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="4030c-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-501">Account type</span></span> | <span data-ttu-id="4030c-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-502">Account number</span></span> | <span data-ttu-id="4030c-503">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-503">Layer</span></span>  | <span data-ttu-id="4030c-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-504">Account description</span></span>      | <span data-ttu-id="4030c-505">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-505">Debit</span></span> | <span data-ttu-id="4030c-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="4030c-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-507">Ledger</span></span>       | <span data-ttu-id="4030c-508">8</span><span class="sxs-lookup"><span data-stu-id="4030c-508">8</span></span>              | <span data-ttu-id="4030c-509">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-509">Custom</span></span> | <span data-ttu-id="4030c-510">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-510">Interest expense</span></span>         | <span data-ttu-id="4030c-511">94.97</span><span class="sxs-lookup"><span data-stu-id="4030c-511">94.97</span></span> |        |
| <span data-ttu-id="4030c-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-512">Ledger</span></span>       | <span data-ttu-id="4030c-513">7</span><span class="sxs-lookup"><span data-stu-id="4030c-513">7</span></span>              | <span data-ttu-id="4030c-514">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-514">Custom</span></span> | <span data-ttu-id="4030c-515">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="4030c-515">Finance lease obligation</span></span> |       | <span data-ttu-id="4030c-516">94.97</span><span class="sxs-lookup"><span data-stu-id="4030c-516">94.97</span></span>  |

<span data-ttu-id="4030c-517">Afskrivningsudgiftskladdeposten genereres fra planen for aktivafskrivning.</span><span class="sxs-lookup"><span data-stu-id="4030c-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="4030c-518">Afskrivningsudgift – 31/1/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="4030c-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="4030c-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="4030c-519">Account type</span></span> | <span data-ttu-id="4030c-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-520">Account number</span></span> | <span data-ttu-id="4030c-521">Lag</span><span class="sxs-lookup"><span data-stu-id="4030c-521">Layer</span></span>  | <span data-ttu-id="4030c-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4030c-522">Account description</span></span>      | <span data-ttu-id="4030c-523">Debet</span><span class="sxs-lookup"><span data-stu-id="4030c-523">Debit</span></span>  | <span data-ttu-id="4030c-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="4030c-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="4030c-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-525">Ledger</span></span>       | <span data-ttu-id="4030c-526">10</span><span class="sxs-lookup"><span data-stu-id="4030c-526">10</span></span>             | <span data-ttu-id="4030c-527">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-527">Custom</span></span> | <span data-ttu-id="4030c-528">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="4030c-528">Depreciation expense</span></span>     | <span data-ttu-id="4030c-529">949.75</span><span class="sxs-lookup"><span data-stu-id="4030c-529">949.75</span></span> |        |
| <span data-ttu-id="4030c-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="4030c-530">Ledger</span></span>       | <span data-ttu-id="4030c-531">11</span><span class="sxs-lookup"><span data-stu-id="4030c-531">11</span></span>             | <span data-ttu-id="4030c-532">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="4030c-532">Custom</span></span> | <span data-ttu-id="4030c-533">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="4030c-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="4030c-534">949.75</span><span class="sxs-lookup"><span data-stu-id="4030c-534">949.75</span></span> |

<span data-ttu-id="4030c-535">Når alle disse kladdeposteringer er oprettet og bogført, vises følgende værdier for "brugerdefineret lag 1".</span><span class="sxs-lookup"><span data-stu-id="4030c-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="4030c-536">Bemærk, at den sidste kolonne indeholder bankgebyret, momsudgiften og reduktionen af kontanter fra det foregående lag, men ikke de lovpligtige rapporteringskladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="4030c-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="4030c-537">Derfor opnås ægte Dual Reporting-funktioner.</span><span class="sxs-lookup"><span data-stu-id="4030c-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="4030c-538">På dette tidspunkt har firmaet kun brug for sin råbalance, og kombinerer det aktuelle lag og det brugerdefinerede lag for at oprette en IFRS-råbalance.</span><span class="sxs-lookup"><span data-stu-id="4030c-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="4030c-539">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="4030c-539">Account No</span></span> | <span data-ttu-id="4030c-540">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4030c-540">Description</span></span>              | <span data-ttu-id="4030c-541">Lovpligtigt kartotek\-Aktuelt lag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-542">Lovpligtigt kartotek\-Aktuelt lag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-543">Lovpligtigt kartotek\-Aktuelt lag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-544">Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="4030c-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="4030c-545">Tilbageført kartotek\-Brugerdefineret lag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-546">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-547">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-548">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-549">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="4030c-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="4030c-550">Brugerdefineret lag \+ Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="4030c-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="4030c-551">1</span><span class="sxs-lookup"><span data-stu-id="4030c-551">1</span></span>          | <span data-ttu-id="4030c-552">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-552">Lease expense</span></span>            | <span data-ttu-id="4030c-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="4030c-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-554">1,000\.00</span></span>               |   | <span data-ttu-id="4030c-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="4030c-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="4030c-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-556">0\.00</span></span>                                   |
| <span data-ttu-id="4030c-557">2</span><span class="sxs-lookup"><span data-stu-id="4030c-557">2</span></span>          | <span data-ttu-id="4030c-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="4030c-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="4030c-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="4030c-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4030c-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-561">3\.00</span></span>                                   |
| <span data-ttu-id="4030c-562">3</span><span class="sxs-lookup"><span data-stu-id="4030c-562">3</span></span>          | <span data-ttu-id="4030c-563">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="4030c-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="4030c-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4030c-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-566">5\.00</span></span>                                   |
| <span data-ttu-id="4030c-567">4</span><span class="sxs-lookup"><span data-stu-id="4030c-567">4</span></span>          | <span data-ttu-id="4030c-568">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="4030c-568">Clearing account</span></span>         | <span data-ttu-id="4030c-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="4030c-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="4030c-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-571">0\.00</span></span>                   |   | <span data-ttu-id="4030c-572">1.000</span><span class="sxs-lookup"><span data-stu-id="4030c-572">1,000</span></span>                                           |                                                | <span data-ttu-id="4030c-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="4030c-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="4030c-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-574">0\.00</span></span>                                   |
| <span data-ttu-id="4030c-575">5</span><span class="sxs-lookup"><span data-stu-id="4030c-575">5</span></span>          | <span data-ttu-id="4030c-576">Kreditor</span><span class="sxs-lookup"><span data-stu-id="4030c-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="4030c-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="4030c-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-578">1,008\.00</span></span>                                         | <span data-ttu-id="4030c-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4030c-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-580">0\.00</span></span>                                   |
| <span data-ttu-id="4030c-581">6</span><span class="sxs-lookup"><span data-stu-id="4030c-581">6</span></span>          | <span data-ttu-id="4030c-582">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="4030c-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="4030c-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="4030c-584">22,794</span><span class="sxs-lookup"><span data-stu-id="4030c-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="4030c-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="4030c-585">22,793\.90</span></span>                              |
| <span data-ttu-id="4030c-586">7</span><span class="sxs-lookup"><span data-stu-id="4030c-586">7</span></span>          | <span data-ttu-id="4030c-587">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="4030c-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="4030c-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="4030c-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="4030c-589">\-22,794</span></span>                                       | <span data-ttu-id="4030c-590">1.000</span><span class="sxs-lookup"><span data-stu-id="4030c-590">1,000</span></span>                                          | <span data-ttu-id="4030c-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="4030c-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="4030c-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="4030c-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="4030c-593">8</span><span class="sxs-lookup"><span data-stu-id="4030c-593">8</span></span>          | <span data-ttu-id="4030c-594">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="4030c-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="4030c-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="4030c-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="4030c-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="4030c-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="4030c-597">94\.97</span></span>                                  |
| <span data-ttu-id="4030c-598">9</span><span class="sxs-lookup"><span data-stu-id="4030c-598">9</span></span>          | <span data-ttu-id="4030c-599">Indløsning</span><span class="sxs-lookup"><span data-stu-id="4030c-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="4030c-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="4030c-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="4030c-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="4030c-603">10</span><span class="sxs-lookup"><span data-stu-id="4030c-603">10</span></span>         | <span data-ttu-id="4030c-604">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="4030c-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="4030c-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="4030c-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="4030c-606">949\.75</span></span>                                        | <span data-ttu-id="4030c-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="4030c-607">949\.75</span></span>                                 |
| <span data-ttu-id="4030c-608">11</span><span class="sxs-lookup"><span data-stu-id="4030c-608">11</span></span>         | <span data-ttu-id="4030c-609">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="4030c-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="4030c-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="4030c-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="4030c-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="4030c-611">\-949\.75</span></span>                                      | <span data-ttu-id="4030c-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="4030c-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]