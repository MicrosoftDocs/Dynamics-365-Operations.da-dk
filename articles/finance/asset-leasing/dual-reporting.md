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
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003175"
---
# <a name="dual-reporting"></a><span data-ttu-id="8b129-103">Dobbeltrapportering</span><span class="sxs-lookup"><span data-stu-id="8b129-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b129-104">I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="8b129-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="8b129-105">Det er nødvendigt med kendskab til posteringslag i Microsoft Dynamics 365 Finance, og det vil gøre det nemmere at forstå i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="8b129-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="8b129-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8b129-106">Example</span></span>

<span data-ttu-id="8b129-107">Følgende eksempelkonti til en leaseaftale under italiensk lovpligtig rapportering ved hjælp af både likviditetsmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="8b129-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="8b129-108">Firmaet skal etablere tre kartoteker for at kunne redegøre for både de italienske lovpligtige krav og IFRS 16-krav.</span><span class="sxs-lookup"><span data-stu-id="8b129-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="8b129-109">Der kræves et kartotek til IFRS 16, et kartotek til lovpligtige krav, og et kartotek til automatisk tilbageføring af lovpligtige bogføringer.</span><span class="sxs-lookup"><span data-stu-id="8b129-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="8b129-110">Kartotekerne oprettes som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="8b129-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="8b129-111">**IFRS 16-kartotek**</span><span class="sxs-lookup"><span data-stu-id="8b129-111">**IFRS 16 book**</span></span>

<span data-ttu-id="8b129-112">IFRS 16-kartoteket er konfigureret, så det overholder IFRS 16-regnskabsstandarden.</span><span class="sxs-lookup"><span data-stu-id="8b129-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="8b129-113">Alle poster, der er bogført i dette kartotek, bogføres i et brugerdefineret lag.</span><span class="sxs-lookup"><span data-stu-id="8b129-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="8b129-114">Navn</span><span class="sxs-lookup"><span data-stu-id="8b129-114">Name</span></span>                                    | <span data-ttu-id="8b129-115">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8b129-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="8b129-116">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="8b129-116">Book type</span></span>                               | <span data-ttu-id="8b129-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8b129-117">IFRS 16</span></span>        |
| <span data-ttu-id="8b129-118">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-118">Book description</span></span>                        | <span data-ttu-id="8b129-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8b129-119">IFRS 16</span></span>        |
| <span data-ttu-id="8b129-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="8b129-120">Posting Layer</span></span>                           | <span data-ttu-id="8b129-121">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="8b129-121">Custom layer 1</span></span> |
| <span data-ttu-id="8b129-122">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="8b129-122">Lease Type</span></span>                              | <span data-ttu-id="8b129-123">Finance</span><span class="sxs-lookup"><span data-stu-id="8b129-123">Finance</span></span>        |
| <span data-ttu-id="8b129-124">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="8b129-124">Accounting Framework</span></span>                    | <span data-ttu-id="8b129-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8b129-125">IFRS 16</span></span>        |
| <span data-ttu-id="8b129-126">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="8b129-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8b129-127">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-127">0.00</span></span>           |
| <span data-ttu-id="8b129-128">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8b129-129">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-129">0.00</span></span>           |
| <span data-ttu-id="8b129-130">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="8b129-130">Short-term threshold</span></span>                    | <span data-ttu-id="8b129-131">12</span><span class="sxs-lookup"><span data-stu-id="8b129-131">12</span></span>             |
| <span data-ttu-id="8b129-132">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="8b129-132">Low Value Threshold</span></span>                     | <span data-ttu-id="8b129-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-133">5,000.00</span></span>       |
| <span data-ttu-id="8b129-134">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-134">Pay to Vendor</span></span>                           | <span data-ttu-id="8b129-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="8b129-135">No</span></span>             |

<span data-ttu-id="8b129-136">**Lovpligtigt kartotek**</span><span class="sxs-lookup"><span data-stu-id="8b129-136">**Statutory book**</span></span>

<span data-ttu-id="8b129-137">Det lovpligtige kartotek er en kassekladde, hvor firmaet kan redegøre for leasingudgifter som det kontantbeløb, der betales hver måned for leje.</span><span class="sxs-lookup"><span data-stu-id="8b129-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="8b129-138">Dette kartotek opretter ikke et ROU-aktiv eller en leasingforpligtelse.</span><span class="sxs-lookup"><span data-stu-id="8b129-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="8b129-139">Navn</span><span class="sxs-lookup"><span data-stu-id="8b129-139">Name</span></span>                                    | <span data-ttu-id="8b129-140">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8b129-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="8b129-141">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="8b129-141">Book type</span></span>                               | <span data-ttu-id="8b129-142">Lovpligtig</span><span class="sxs-lookup"><span data-stu-id="8b129-142">Statutory</span></span>   |
| <span data-ttu-id="8b129-143">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-143">Book description</span></span>                        | <span data-ttu-id="8b129-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="8b129-144">Local GAAP</span></span>  |
| <span data-ttu-id="8b129-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="8b129-145">Posting Layer</span></span>                           | <span data-ttu-id="8b129-146">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-146">Current</span></span>     |
| <span data-ttu-id="8b129-147">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="8b129-147">Lease Type</span></span>                              | <span data-ttu-id="8b129-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="8b129-148">Automatic</span></span>   |
| <span data-ttu-id="8b129-149">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="8b129-149">Accounting Framework</span></span>                    | <span data-ttu-id="8b129-150">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="8b129-150">Cash basis</span></span>  |
| <span data-ttu-id="8b129-151">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="8b129-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8b129-152">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-152">0.00</span></span>        |
| <span data-ttu-id="8b129-153">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8b129-154">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-154">0.00</span></span>        |
| <span data-ttu-id="8b129-155">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="8b129-155">Short-term threshold</span></span>                    | <span data-ttu-id="8b129-156">0</span><span class="sxs-lookup"><span data-stu-id="8b129-156">0</span></span>           |
| <span data-ttu-id="8b129-157">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="8b129-157">Low Value Threshold</span></span>                     | <span data-ttu-id="8b129-158">0</span><span class="sxs-lookup"><span data-stu-id="8b129-158">0</span></span>           |
| <span data-ttu-id="8b129-159">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-159">Pay to Vendor</span></span>                           | <span data-ttu-id="8b129-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="8b129-160">No</span></span>          |

<span data-ttu-id="8b129-161">**Lovpligtigt tilbageført kartotek**</span><span class="sxs-lookup"><span data-stu-id="8b129-161">**Statutory reversal book**</span></span>

<span data-ttu-id="8b129-162">Det lovpligtige tilbageførte kartotek konfigureres på samme måde som det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="8b129-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="8b129-163">Navn</span><span class="sxs-lookup"><span data-stu-id="8b129-163">Name</span></span>                                    | <span data-ttu-id="8b129-164">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8b129-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="8b129-165">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="8b129-165">Book type</span></span>                               | <span data-ttu-id="8b129-166">Lovpligtig - tilbageført</span><span class="sxs-lookup"><span data-stu-id="8b129-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="8b129-167">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-167">Book description</span></span>                        | <span data-ttu-id="8b129-168">Kartotek, der skal tilbageføre lovpligtigt kartotek</span><span class="sxs-lookup"><span data-stu-id="8b129-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="8b129-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="8b129-169">Posting Layer</span></span>                           | <span data-ttu-id="8b129-170">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="8b129-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="8b129-171">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="8b129-171">Lease Type</span></span>                              | <span data-ttu-id="8b129-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="8b129-172">Automatic</span></span>                      |
| <span data-ttu-id="8b129-173">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="8b129-173">Accounting Framework</span></span>                    | <span data-ttu-id="8b129-174">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="8b129-174">Cash basis</span></span>                     |
| <span data-ttu-id="8b129-175">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="8b129-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8b129-176">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-176">0.00</span></span>                           |
| <span data-ttu-id="8b129-177">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8b129-178">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-178">0.00</span></span>                           |
| <span data-ttu-id="8b129-179">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="8b129-179">Short-term threshold</span></span>                    | <span data-ttu-id="8b129-180">0</span><span class="sxs-lookup"><span data-stu-id="8b129-180">0</span></span>                              |
| <span data-ttu-id="8b129-181">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="8b129-181">Low Value Threshold</span></span>                     | <span data-ttu-id="8b129-182">0</span><span class="sxs-lookup"><span data-stu-id="8b129-182">0</span></span>                              |
| <span data-ttu-id="8b129-183">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-183">Pay to Vendor</span></span>                           | <span data-ttu-id="8b129-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="8b129-184">No</span></span>                             |

<span data-ttu-id="8b129-185">I dette eksempel er der oprettet en leasingaftale, der indeholder følgende indstillinger under fanerne **Generelt** og **Betalingsplanlinje**.</span><span class="sxs-lookup"><span data-stu-id="8b129-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="8b129-186">Fanen **Generelt**</span><span class="sxs-lookup"><span data-stu-id="8b129-186">**General tab**</span></span>

| <span data-ttu-id="8b129-187">Felt</span><span class="sxs-lookup"><span data-stu-id="8b129-187">Field</span></span>                      | <span data-ttu-id="8b129-188">Værdi</span><span class="sxs-lookup"><span data-stu-id="8b129-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="8b129-189">Trinvis lånesats</span><span class="sxs-lookup"><span data-stu-id="8b129-189">Incremental borrowing rate</span></span> | <span data-ttu-id="8b129-190">5 %</span><span class="sxs-lookup"><span data-stu-id="8b129-190">5%</span></span>               |
| <span data-ttu-id="8b129-191">Dato for påbegyndelse</span><span class="sxs-lookup"><span data-stu-id="8b129-191">Commencement date</span></span>          | <span data-ttu-id="8b129-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="8b129-192">1/1/2020</span></span>         |
| <span data-ttu-id="8b129-193">Leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="8b129-193">Lease group</span></span>                | <span data-ttu-id="8b129-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="8b129-194">Buildings</span></span>        |
| <span data-ttu-id="8b129-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="8b129-195">Vendor</span></span>                     | <span data-ttu-id="8b129-196">1001</span><span class="sxs-lookup"><span data-stu-id="8b129-196">1001</span></span>             |
| <span data-ttu-id="8b129-197">Aktivets handelsværdi</span><span class="sxs-lookup"><span data-stu-id="8b129-197">Fair value of the asset</span></span>    | <span data-ttu-id="8b129-198">245,000</span><span class="sxs-lookup"><span data-stu-id="8b129-198">245,000</span></span>          |
| <span data-ttu-id="8b129-199">Brugstid for aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-199">Asset useful life</span></span>          | <span data-ttu-id="8b129-200">120</span><span class="sxs-lookup"><span data-stu-id="8b129-200">120</span></span>              |
| <span data-ttu-id="8b129-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="8b129-201">Annuity type</span></span>               | <span data-ttu-id="8b129-202">Almindelig annuitet</span><span class="sxs-lookup"><span data-stu-id="8b129-202">Ordinary annuity</span></span> |
| <span data-ttu-id="8b129-203">Sammensætningsinterval</span><span class="sxs-lookup"><span data-stu-id="8b129-203">Compounding interval</span></span>       | <span data-ttu-id="8b129-204">Månedligt</span><span class="sxs-lookup"><span data-stu-id="8b129-204">Monthly</span></span>          |

<span data-ttu-id="8b129-205">**Betalingsplanlinjer-fane**</span><span class="sxs-lookup"><span data-stu-id="8b129-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="8b129-206">Felt</span><span class="sxs-lookup"><span data-stu-id="8b129-206">Field</span></span>             | <span data-ttu-id="8b129-207">Værdi</span><span class="sxs-lookup"><span data-stu-id="8b129-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="8b129-208">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="8b129-208">Start date</span></span>        | <span data-ttu-id="8b129-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="8b129-209">1/1/2020</span></span>   |
| <span data-ttu-id="8b129-210">Periodeinterval</span><span class="sxs-lookup"><span data-stu-id="8b129-210">Period interval</span></span>   | <span data-ttu-id="8b129-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="8b129-211">Months</span></span>     |
| <span data-ttu-id="8b129-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="8b129-212">Periods</span></span>           | <span data-ttu-id="8b129-213">24</span><span class="sxs-lookup"><span data-stu-id="8b129-213">24</span></span>         |
| <span data-ttu-id="8b129-214">Slutdato</span><span class="sxs-lookup"><span data-stu-id="8b129-214">End date</span></span>          | <span data-ttu-id="8b129-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="8b129-215">12/31/2020</span></span> |
| <span data-ttu-id="8b129-216">Betalingshyppighed</span><span class="sxs-lookup"><span data-stu-id="8b129-216">Payment frequency</span></span> | <span data-ttu-id="8b129-217">Månedligt</span><span class="sxs-lookup"><span data-stu-id="8b129-217">Monthly</span></span>    |
| <span data-ttu-id="8b129-218">Betalingsbeløb</span><span class="sxs-lookup"><span data-stu-id="8b129-218">Payment amount</span></span>    | <span data-ttu-id="8b129-219">1.000</span><span class="sxs-lookup"><span data-stu-id="8b129-219">1,000</span></span>      |

<span data-ttu-id="8b129-220">Hvis du vil redegøre for denne leasingaftale i forbindelse med to strukturer, skal du bruge et aktuelt posteringslag og et brugerdefineret posteringslag.</span><span class="sxs-lookup"><span data-stu-id="8b129-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="8b129-221">Følgende tabel viser et eksempel på hver kladdepost, der er nødvendig for at repræsentere finanserne i de enkelte rapporteringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="8b129-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="8b129-222">En detaljeret beskrivelse af de enkelte kladdeposter for den første måned af leasingaftalen tildeles bagefter.</span><span class="sxs-lookup"><span data-stu-id="8b129-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="8b129-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="8b129-224">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8b129-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="8b129-225">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="8b129-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8b129-226">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="8b129-226">Current layer total</span></span></th>
<th><span data-ttu-id="8b129-227">Tilbageført kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="8b129-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="8b129-228">IFRS 16-kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="8b129-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8b129-229">Aktuelt lag + brugerdefineret lag i alt</span><span class="sxs-lookup"><span data-stu-id="8b129-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8b129-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="8b129-230">JE-100</span></span></th>
<th><span data-ttu-id="8b129-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="8b129-231">JE-110</span></span></th>
<th><span data-ttu-id="8b129-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="8b129-232">JE-120</span></span></th>
<th><span data-ttu-id="8b129-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="8b129-233">JE-130</span></span></th>
<th><span data-ttu-id="8b129-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="8b129-234">JE-140</span></span></th>
<th><span data-ttu-id="8b129-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="8b129-235">JE-150</span></span></th>
<th><span data-ttu-id="8b129-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="8b129-236">JE-160</span></span></th>
<th><span data-ttu-id="8b129-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="8b129-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8b129-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b129-246">1</span><span class="sxs-lookup"><span data-stu-id="8b129-246">1</span></span></td>
<td><span data-ttu-id="8b129-247">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-247">Lease expense</span></span></td>
<td><span data-ttu-id="8b129-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-249">1,000.00</span></span></td>
<td><span data-ttu-id="8b129-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="8b129-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-251">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-252">2</span><span class="sxs-lookup"><span data-stu-id="8b129-252">2</span></span></td>
<td><span data-ttu-id="8b129-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="8b129-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-254">3.00</span><span class="sxs-lookup"><span data-stu-id="8b129-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-255">3.00</span><span class="sxs-lookup"><span data-stu-id="8b129-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-256">3.00</span><span class="sxs-lookup"><span data-stu-id="8b129-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-257">3</span><span class="sxs-lookup"><span data-stu-id="8b129-257">3</span></span></td>
<td><span data-ttu-id="8b129-258">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-259">5.00</span><span class="sxs-lookup"><span data-stu-id="8b129-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-260">5.00</span><span class="sxs-lookup"><span data-stu-id="8b129-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-261">5.00</span><span class="sxs-lookup"><span data-stu-id="8b129-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-262">4</span><span class="sxs-lookup"><span data-stu-id="8b129-262">4</span></span></td>
<td><span data-ttu-id="8b129-263">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-263">Clearing account</span></span></td>
<td><span data-ttu-id="8b129-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="8b129-264">-1,000.00</span></span></td>
<td><span data-ttu-id="8b129-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-266">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-266">0.00</span></span></td>
<td><span data-ttu-id="8b129-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="8b129-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-269">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-270">5</span><span class="sxs-lookup"><span data-stu-id="8b129-270">5</span></span></td>
<td><span data-ttu-id="8b129-271">Kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-272">-1,008.00</span></span></td>
<td><span data-ttu-id="8b129-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8b129-273">1,008.00</span></span></td>
<td><span data-ttu-id="8b129-274">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-275">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-276">6</span><span class="sxs-lookup"><span data-stu-id="8b129-276">6</span></span></td>
<td><span data-ttu-id="8b129-277">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-278">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="8b129-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8b129-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-281">7</span><span class="sxs-lookup"><span data-stu-id="8b129-281">7</span></span></td>
<td><span data-ttu-id="8b129-282">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="8b129-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-283">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="8b129-284">-22,794.00</span></span></td>
<td><span data-ttu-id="8b129-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-285">1,000.00</span></span></td>
<td><span data-ttu-id="8b129-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="8b129-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="8b129-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-288">8</span><span class="sxs-lookup"><span data-stu-id="8b129-288">8</span></span></td>
<td><span data-ttu-id="8b129-289">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-290">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-291">94.97</span><span class="sxs-lookup"><span data-stu-id="8b129-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-292">94.97</span><span class="sxs-lookup"><span data-stu-id="8b129-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-293">9</span><span class="sxs-lookup"><span data-stu-id="8b129-293">9</span></span></td>
<td><span data-ttu-id="8b129-294">Indløsning</span><span class="sxs-lookup"><span data-stu-id="8b129-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-295">-1,008.00</span></span></td>
<td><span data-ttu-id="8b129-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-298">10</span><span class="sxs-lookup"><span data-stu-id="8b129-298">10</span></span></td>
<td><span data-ttu-id="8b129-299">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="8b129-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-300">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-301">949.75</span><span class="sxs-lookup"><span data-stu-id="8b129-301">949.75</span></span></td>
<td><span data-ttu-id="8b129-302">949.75</span><span class="sxs-lookup"><span data-stu-id="8b129-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-303">11</span><span class="sxs-lookup"><span data-stu-id="8b129-303">11</span></span></td>
<td><span data-ttu-id="8b129-304">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="8b129-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-305">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="8b129-306">-949.75</span></span></td>
<td><span data-ttu-id="8b129-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="8b129-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b129-308">Som vist i den foregående tabel, skal der rapporteres tre kartoteker under både lovpligtig rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="8b129-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="8b129-309">I det lovpligtige kartotek registreres leasingbetalingen i henhold til reglerne for kontantregnskab under det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="8b129-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="8b129-310">Det lovpligtige tilbageførte kartotek tilbagefører de lovpligtige kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="8b129-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="8b129-311">IFRS 16-kartoteket opretter de kladdeposteringer, der er påkrævet i IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="8b129-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="8b129-312">Du skal kun angive en leasingaftale én gang.</span><span class="sxs-lookup"><span data-stu-id="8b129-312">You must enter a lease only one time.</span></span> <span data-ttu-id="8b129-313">Du kan derefter åbne siden **Kartoteker** for at se alle de kartoteker, der er tilknyttet leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="8b129-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="8b129-314">Når du opretter kartotekerne, skal de alle tre knyttes til samme leasingpost.</span><span class="sxs-lookup"><span data-stu-id="8b129-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="8b129-315">Den første kladdepostering registrerer leasingudgiften i henhold til det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="8b129-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="8b129-316">Du kan oprette betalinger enten i en batch eller ved at vælge betalingsplanen i det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="8b129-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="8b129-317">I dette eksempel er der oprettet følgende kladdepost for det lovpligtige kartotek fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="8b129-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="8b129-318">Leasingbetaling - 1/31/2020 - JE 100</span><span class="sxs-lookup"><span data-stu-id="8b129-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="8b129-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-319">Account type</span></span> | <span data-ttu-id="8b129-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-320">Account number</span></span> | <span data-ttu-id="8b129-321">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-321">Layer</span></span>   | <span data-ttu-id="8b129-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-322">Account description</span></span> | <span data-ttu-id="8b129-323">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-323">Debit</span></span>    | <span data-ttu-id="8b129-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8b129-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-325">Ledger</span></span>       | <span data-ttu-id="8b129-326">1</span><span class="sxs-lookup"><span data-stu-id="8b129-326">1</span></span>              | <span data-ttu-id="8b129-327">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-327">Current</span></span> | <span data-ttu-id="8b129-328">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-328">Lease expense</span></span>       | <span data-ttu-id="8b129-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-329">1,000.00</span></span> |          |
| <span data-ttu-id="8b129-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-330">Ledger</span></span>       | <span data-ttu-id="8b129-331">4</span><span class="sxs-lookup"><span data-stu-id="8b129-331">4</span></span>              | <span data-ttu-id="8b129-332">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-332">Current</span></span> | <span data-ttu-id="8b129-333">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-333">Clearing account</span></span>    |          | <span data-ttu-id="8b129-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-334">1,000.00</span></span> |

<span data-ttu-id="8b129-335">En kreditormedarbejder bruger standardfunktionen for Dynamics 365 til at oprette en faktura, der skal betale for leasingaftalen uden for aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="8b129-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="8b129-336">I stedet for at vælge **leasingudgift** som debetkonto vælger kreditormedarbejderen en clearingkonto til at generere følgende post.</span><span class="sxs-lookup"><span data-stu-id="8b129-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="8b129-337">AP-proces – 31/1/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="8b129-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="8b129-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-338">Account type</span></span> | <span data-ttu-id="8b129-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-339">Account number</span></span> | <span data-ttu-id="8b129-340">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-340">Layer</span></span>   | <span data-ttu-id="8b129-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-341">Account description</span></span> | <span data-ttu-id="8b129-342">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-342">Debit</span></span>    | <span data-ttu-id="8b129-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8b129-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-344">Ledger</span></span>       | <span data-ttu-id="8b129-345">4</span><span class="sxs-lookup"><span data-stu-id="8b129-345">4</span></span>              | <span data-ttu-id="8b129-346">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-346">Current</span></span> | <span data-ttu-id="8b129-347">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-347">Clearing account</span></span>    | <span data-ttu-id="8b129-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-348">1,000.00</span></span> |          |
| <span data-ttu-id="8b129-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-349">Ledger</span></span>       | <span data-ttu-id="8b129-350">2</span><span class="sxs-lookup"><span data-stu-id="8b129-350">2</span></span>              | <span data-ttu-id="8b129-351">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-351">Current</span></span> | <span data-ttu-id="8b129-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="8b129-352">Bank fee</span></span>            | <span data-ttu-id="8b129-353">3.00</span><span class="sxs-lookup"><span data-stu-id="8b129-353">3.00</span></span>     |          |
| <span data-ttu-id="8b129-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-354">Ledger</span></span>       | <span data-ttu-id="8b129-355">3</span><span class="sxs-lookup"><span data-stu-id="8b129-355">3</span></span>              | <span data-ttu-id="8b129-356">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-356">Current</span></span> | <span data-ttu-id="8b129-357">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-357">VAT expense</span></span>         | <span data-ttu-id="8b129-358">5.00</span><span class="sxs-lookup"><span data-stu-id="8b129-358">5.00</span></span>     |          |
| <span data-ttu-id="8b129-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="8b129-359">Vendor</span></span>       | <span data-ttu-id="8b129-360">5</span><span class="sxs-lookup"><span data-stu-id="8b129-360">5</span></span>              | <span data-ttu-id="8b129-361">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-361">Current</span></span> | <span data-ttu-id="8b129-362">Kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-362">Accounts payable</span></span>    |          | <span data-ttu-id="8b129-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8b129-363">1,008.00</span></span> |

<span data-ttu-id="8b129-364">Når opgørelsen er udstedt til leverandøren, skal du følge den almindelige betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="8b129-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="8b129-365">Under denne proces genereres følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="8b129-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="8b129-366">Kontant betaling – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="8b129-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="8b129-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-367">Account type</span></span> | <span data-ttu-id="8b129-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-368">Account number</span></span> | <span data-ttu-id="8b129-369">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-369">Layer</span></span>   | <span data-ttu-id="8b129-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-370">Account description</span></span> | <span data-ttu-id="8b129-371">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-371">Debit</span></span>    | <span data-ttu-id="8b129-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8b129-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="8b129-373">Vendor</span></span>       | <span data-ttu-id="8b129-374">5</span><span class="sxs-lookup"><span data-stu-id="8b129-374">5</span></span>              | <span data-ttu-id="8b129-375">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-375">Current</span></span> | <span data-ttu-id="8b129-376">Kreditorer</span><span class="sxs-lookup"><span data-stu-id="8b129-376">Accounts Payable</span></span>    | <span data-ttu-id="8b129-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8b129-377">1,008.00</span></span> |          |
| <span data-ttu-id="8b129-378">Bank</span><span class="sxs-lookup"><span data-stu-id="8b129-378">Bank</span></span>         | <span data-ttu-id="8b129-379">9</span><span class="sxs-lookup"><span data-stu-id="8b129-379">9</span></span>              | <span data-ttu-id="8b129-380">Løbende</span><span class="sxs-lookup"><span data-stu-id="8b129-380">Current</span></span> | <span data-ttu-id="8b129-381">Indløsning</span><span class="sxs-lookup"><span data-stu-id="8b129-381">Cash</span></span>                |          | <span data-ttu-id="8b129-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8b129-382">1,008.00</span></span> |

<span data-ttu-id="8b129-383">På dette tidspunkt har du taget fuld højde for denne leasingaftale under lovpligtige rapporteringskrav og kan generere en råbalance ved hjælp af det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="8b129-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="8b129-384">Systemet returnerer en råbalance, der har følgende tal.</span><span class="sxs-lookup"><span data-stu-id="8b129-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="8b129-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="8b129-386">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8b129-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="8b129-387">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="8b129-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8b129-388">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="8b129-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8b129-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="8b129-389">JE-100</span></span></th>
<th><span data-ttu-id="8b129-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="8b129-390">JE-110</span></span></th>
<th><span data-ttu-id="8b129-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="8b129-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8b129-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8b129-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8b129-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8b129-395">1</span><span class="sxs-lookup"><span data-stu-id="8b129-395">1</span></span></td>
<td><span data-ttu-id="8b129-396">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-396">Lease expense</span></span></td>
<td><span data-ttu-id="8b129-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-399">2</span><span class="sxs-lookup"><span data-stu-id="8b129-399">2</span></span></td>
<td><span data-ttu-id="8b129-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="8b129-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-401">3.00</span><span class="sxs-lookup"><span data-stu-id="8b129-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-402">3.00</span><span class="sxs-lookup"><span data-stu-id="8b129-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-403">3</span><span class="sxs-lookup"><span data-stu-id="8b129-403">3</span></span></td>
<td><span data-ttu-id="8b129-404">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-405">5.00</span><span class="sxs-lookup"><span data-stu-id="8b129-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-406">5.00</span><span class="sxs-lookup"><span data-stu-id="8b129-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-407">4</span><span class="sxs-lookup"><span data-stu-id="8b129-407">4</span></span></td>
<td><span data-ttu-id="8b129-408">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-408">Clearing account</span></span></td>
<td><span data-ttu-id="8b129-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="8b129-409">-1,000.00</span></span></td>
<td><span data-ttu-id="8b129-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-411">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-412">5</span><span class="sxs-lookup"><span data-stu-id="8b129-412">5</span></span></td>
<td><span data-ttu-id="8b129-413">Kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="8b129-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-414">-1,008.00</span></span></td>
<td><span data-ttu-id="8b129-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8b129-415">1,008.00</span></span></td>
<td><span data-ttu-id="8b129-416">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-417">6</span><span class="sxs-lookup"><span data-stu-id="8b129-417">6</span></span></td>
<td><span data-ttu-id="8b129-418">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-419">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-420">7</span><span class="sxs-lookup"><span data-stu-id="8b129-420">7</span></span></td>
<td><span data-ttu-id="8b129-421">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="8b129-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-422">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-423">8</span><span class="sxs-lookup"><span data-stu-id="8b129-423">8</span></span></td>
<td><span data-ttu-id="8b129-424">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-425">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-426">9</span><span class="sxs-lookup"><span data-stu-id="8b129-426">9</span></span></td>
<td><span data-ttu-id="8b129-427">Indløsning</span><span class="sxs-lookup"><span data-stu-id="8b129-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-428">-1,008.00</span></span></td>
<td><span data-ttu-id="8b129-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="8b129-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-430">10</span><span class="sxs-lookup"><span data-stu-id="8b129-430">10</span></span></td>
<td><span data-ttu-id="8b129-431">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="8b129-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-432">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8b129-433">11</span><span class="sxs-lookup"><span data-stu-id="8b129-433">11</span></span></td>
<td><span data-ttu-id="8b129-434">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="8b129-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8b129-435">0,00</span><span class="sxs-lookup"><span data-stu-id="8b129-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8b129-436">Hvis du vil bruge IFRS 16-tal til at køre samme råbalance, skal de lovpligtige regnskabskladdeposteringer tilbageføres, og de IFRS 16-journaloptegnelser skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="8b129-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="8b129-437">Hvis du vil tilbageføre lovpligtige kladdeposteringer, skal dette eksempel indeholde en lovpligtig tilbageførsel, der har samme opsætning som det lovpligtige kartotek, men en modsat posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="8b129-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="8b129-438">Det lovpligtige kartotek har *debiteret* en konto til leasingomkostninger, men det tilbagevendende kartotek vil *kreditere* denne konto.</span><span class="sxs-lookup"><span data-stu-id="8b129-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="8b129-439">Disse relationer defineres nemt i bankkonti for aktivleasing på siden **Aktivleasingparametre** (**Aktivleasing \> Konfiguration \> Aktivleasingparametre**).</span><span class="sxs-lookup"><span data-stu-id="8b129-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="8b129-440">Når den samme proces, der blev anvendt til det lovpligtige kartotek, bruges i et tilbageført kartotek, oprettes følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="8b129-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="8b129-441">Forskellen er, at det tilbageførte kartotek registrerer posteringer fra det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="8b129-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="8b129-442">De tilbageførte posteringer foretages også i det brugerdefinerede lag.</span><span class="sxs-lookup"><span data-stu-id="8b129-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="8b129-443">Når der køres en råbalance på det aktuelle lag, medtages der ikke kladdeposteringer til tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="8b129-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="8b129-444">Leasingbetaling - 31/1/2020 - JE 130</span><span class="sxs-lookup"><span data-stu-id="8b129-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="8b129-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-445">Account type</span></span> | <span data-ttu-id="8b129-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-446">Account number</span></span> | <span data-ttu-id="8b129-447">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-447">Layer</span></span>  | <span data-ttu-id="8b129-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-448">Account description</span></span> | <span data-ttu-id="8b129-449">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-449">Debit</span></span>    | <span data-ttu-id="8b129-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="8b129-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-451">Ledger</span></span>       | <span data-ttu-id="8b129-452">4</span><span class="sxs-lookup"><span data-stu-id="8b129-452">4</span></span>              | <span data-ttu-id="8b129-453">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-453">Custom</span></span> | <span data-ttu-id="8b129-454">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-454">Clearing account</span></span>    | <span data-ttu-id="8b129-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-455">1,000.00</span></span> |          |
| <span data-ttu-id="8b129-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-456">Ledger</span></span>       | <span data-ttu-id="8b129-457">1</span><span class="sxs-lookup"><span data-stu-id="8b129-457">1</span></span>              | <span data-ttu-id="8b129-458">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-458">Custom</span></span> | <span data-ttu-id="8b129-459">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-459">Lease expense</span></span>       |          | <span data-ttu-id="8b129-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-460">1,000.00</span></span> |

<span data-ttu-id="8b129-461">Nu, hvor du har elimineret lovpligtige kladdeposteringer, skal du reservere alle de kladdeposter, IFRS 16 har brug for, i IFRS 16-kartoteket.</span><span class="sxs-lookup"><span data-stu-id="8b129-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="8b129-462">Disse poster omfatter den første anerkendelse af ROU-aktiv og ansvarsforsikring samt posten med renter og afskrivning.</span><span class="sxs-lookup"><span data-stu-id="8b129-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="8b129-463">Første indregning – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="8b129-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="8b129-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-464">Account type</span></span> | <span data-ttu-id="8b129-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-465">Account number</span></span> | <span data-ttu-id="8b129-466">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-466">Layer</span></span>  | <span data-ttu-id="8b129-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-467">Account description</span></span>      | <span data-ttu-id="8b129-468">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-468">Debit</span></span>     | <span data-ttu-id="8b129-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="8b129-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-470">Ledger</span></span>       | <span data-ttu-id="8b129-471">6</span><span class="sxs-lookup"><span data-stu-id="8b129-471">6</span></span>              | <span data-ttu-id="8b129-472">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-472">Custom</span></span> | <span data-ttu-id="8b129-473">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-473">ROU Asset</span></span>                | <span data-ttu-id="8b129-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8b129-474">22,793.90</span></span> |           |
| <span data-ttu-id="8b129-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-475">Ledger</span></span>       | <span data-ttu-id="8b129-476">7</span><span class="sxs-lookup"><span data-stu-id="8b129-476">7</span></span>              | <span data-ttu-id="8b129-477">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-477">Custom</span></span> | <span data-ttu-id="8b129-478">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="8b129-478">Finance lease obligation</span></span> |           | <span data-ttu-id="8b129-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8b129-479">22,793.90</span></span> |

<span data-ttu-id="8b129-480">Leasingbetalingen bogføres på samme måde som andre leasingbetalinger.</span><span class="sxs-lookup"><span data-stu-id="8b129-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="8b129-481">Årsagen til brug af clearing kontoen er at sikre, at kontant kun krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="8b129-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="8b129-482">Leasingbetaling - 31/1/2020 - JE 150</span><span class="sxs-lookup"><span data-stu-id="8b129-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="8b129-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-483">Account type</span></span> | <span data-ttu-id="8b129-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-484">Account number</span></span> | <span data-ttu-id="8b129-485">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-485">Layer</span></span>  | <span data-ttu-id="8b129-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-486">Account description</span></span>      | <span data-ttu-id="8b129-487">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-487">Debit</span></span>    | <span data-ttu-id="8b129-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="8b129-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-489">Ledger</span></span>       | <span data-ttu-id="8b129-490">7</span><span class="sxs-lookup"><span data-stu-id="8b129-490">7</span></span>              | <span data-ttu-id="8b129-491">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-491">Custom</span></span> | <span data-ttu-id="8b129-492">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="8b129-492">Finance lease obligation</span></span> | <span data-ttu-id="8b129-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-493">1,000.00</span></span> |          |
| <span data-ttu-id="8b129-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-494">Ledger</span></span>       | <span data-ttu-id="8b129-495">4</span><span class="sxs-lookup"><span data-stu-id="8b129-495">4</span></span>              | <span data-ttu-id="8b129-496">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-496">Custom</span></span> | <span data-ttu-id="8b129-497">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-497">Clearing account</span></span>         |          | <span data-ttu-id="8b129-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8b129-498">1,000.00</span></span> |

<span data-ttu-id="8b129-499">Renteudgiftskladdeposten genereres fra planen for passiv afskrivning.</span><span class="sxs-lookup"><span data-stu-id="8b129-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="8b129-500">Renteudgift – 31/1/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="8b129-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="8b129-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-501">Account type</span></span> | <span data-ttu-id="8b129-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-502">Account number</span></span> | <span data-ttu-id="8b129-503">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-503">Layer</span></span>  | <span data-ttu-id="8b129-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-504">Account description</span></span>      | <span data-ttu-id="8b129-505">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-505">Debit</span></span> | <span data-ttu-id="8b129-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="8b129-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-507">Ledger</span></span>       | <span data-ttu-id="8b129-508">8</span><span class="sxs-lookup"><span data-stu-id="8b129-508">8</span></span>              | <span data-ttu-id="8b129-509">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-509">Custom</span></span> | <span data-ttu-id="8b129-510">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-510">Interest expense</span></span>         | <span data-ttu-id="8b129-511">94.97</span><span class="sxs-lookup"><span data-stu-id="8b129-511">94.97</span></span> |        |
| <span data-ttu-id="8b129-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-512">Ledger</span></span>       | <span data-ttu-id="8b129-513">7</span><span class="sxs-lookup"><span data-stu-id="8b129-513">7</span></span>              | <span data-ttu-id="8b129-514">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-514">Custom</span></span> | <span data-ttu-id="8b129-515">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="8b129-515">Finance lease obligation</span></span> |       | <span data-ttu-id="8b129-516">94.97</span><span class="sxs-lookup"><span data-stu-id="8b129-516">94.97</span></span>  |

<span data-ttu-id="8b129-517">Afskrivningsudgiftskladdeposten genereres fra planen for aktivafskrivning.</span><span class="sxs-lookup"><span data-stu-id="8b129-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="8b129-518">Afskrivningsudgift – 31/1/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="8b129-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="8b129-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="8b129-519">Account type</span></span> | <span data-ttu-id="8b129-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-520">Account number</span></span> | <span data-ttu-id="8b129-521">Lag</span><span class="sxs-lookup"><span data-stu-id="8b129-521">Layer</span></span>  | <span data-ttu-id="8b129-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b129-522">Account description</span></span>      | <span data-ttu-id="8b129-523">Debet</span><span class="sxs-lookup"><span data-stu-id="8b129-523">Debit</span></span>  | <span data-ttu-id="8b129-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="8b129-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="8b129-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-525">Ledger</span></span>       | <span data-ttu-id="8b129-526">10</span><span class="sxs-lookup"><span data-stu-id="8b129-526">10</span></span>             | <span data-ttu-id="8b129-527">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-527">Custom</span></span> | <span data-ttu-id="8b129-528">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="8b129-528">Depreciation expense</span></span>     | <span data-ttu-id="8b129-529">949.75</span><span class="sxs-lookup"><span data-stu-id="8b129-529">949.75</span></span> |        |
| <span data-ttu-id="8b129-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="8b129-530">Ledger</span></span>       | <span data-ttu-id="8b129-531">11</span><span class="sxs-lookup"><span data-stu-id="8b129-531">11</span></span>             | <span data-ttu-id="8b129-532">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="8b129-532">Custom</span></span> | <span data-ttu-id="8b129-533">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="8b129-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="8b129-534">949.75</span><span class="sxs-lookup"><span data-stu-id="8b129-534">949.75</span></span> |

<span data-ttu-id="8b129-535">Når alle disse kladdeposteringer er oprettet og bogført, vises følgende værdier for "brugerdefineret lag 1".</span><span class="sxs-lookup"><span data-stu-id="8b129-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="8b129-536">Bemærk, at den sidste kolonne indeholder bankgebyret, momsudgiften og reduktionen af kontanter fra det foregående lag, men ikke de lovpligtige rapporteringskladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="8b129-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="8b129-537">Derfor opnås ægte Dual Reporting-funktioner.</span><span class="sxs-lookup"><span data-stu-id="8b129-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="8b129-538">På dette tidspunkt har firmaet kun brug for sin råbalance, og kombinerer det aktuelle lag og det brugerdefinerede lag for at oprette en IFRS-råbalance.</span><span class="sxs-lookup"><span data-stu-id="8b129-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="8b129-539">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="8b129-539">Account No</span></span> | <span data-ttu-id="8b129-540">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8b129-540">Description</span></span>              | <span data-ttu-id="8b129-541">Lovpligtigt kartotek\-Aktuelt lag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-542">Lovpligtigt kartotek\-Aktuelt lag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-543">Lovpligtigt kartotek\-Aktuelt lag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-544">Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="8b129-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="8b129-545">Tilbageført kartotek\-Brugerdefineret lag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-546">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-547">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-548">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-549">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8b129-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="8b129-550">Brugerdefineret lag \+ Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="8b129-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="8b129-551">1</span><span class="sxs-lookup"><span data-stu-id="8b129-551">1</span></span>          | <span data-ttu-id="8b129-552">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-552">Lease expense</span></span>            | <span data-ttu-id="8b129-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="8b129-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-554">1,000\.00</span></span>               |   | <span data-ttu-id="8b129-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="8b129-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="8b129-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-556">0\.00</span></span>                                   |
| <span data-ttu-id="8b129-557">2</span><span class="sxs-lookup"><span data-stu-id="8b129-557">2</span></span>          | <span data-ttu-id="8b129-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="8b129-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="8b129-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="8b129-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8b129-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-561">3\.00</span></span>                                   |
| <span data-ttu-id="8b129-562">3</span><span class="sxs-lookup"><span data-stu-id="8b129-562">3</span></span>          | <span data-ttu-id="8b129-563">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="8b129-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="8b129-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8b129-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-566">5\.00</span></span>                                   |
| <span data-ttu-id="8b129-567">4</span><span class="sxs-lookup"><span data-stu-id="8b129-567">4</span></span>          | <span data-ttu-id="8b129-568">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="8b129-568">Clearing account</span></span>         | <span data-ttu-id="8b129-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="8b129-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="8b129-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-571">0\.00</span></span>                   |   | <span data-ttu-id="8b129-572">1.000</span><span class="sxs-lookup"><span data-stu-id="8b129-572">1,000</span></span>                                           |                                                | <span data-ttu-id="8b129-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="8b129-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="8b129-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-574">0\.00</span></span>                                   |
| <span data-ttu-id="8b129-575">5</span><span class="sxs-lookup"><span data-stu-id="8b129-575">5</span></span>          | <span data-ttu-id="8b129-576">Kreditor</span><span class="sxs-lookup"><span data-stu-id="8b129-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="8b129-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="8b129-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-578">1,008\.00</span></span>                                         | <span data-ttu-id="8b129-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8b129-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-580">0\.00</span></span>                                   |
| <span data-ttu-id="8b129-581">6</span><span class="sxs-lookup"><span data-stu-id="8b129-581">6</span></span>          | <span data-ttu-id="8b129-582">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="8b129-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="8b129-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="8b129-584">22,794</span><span class="sxs-lookup"><span data-stu-id="8b129-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="8b129-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="8b129-585">22,793\.90</span></span>                              |
| <span data-ttu-id="8b129-586">7</span><span class="sxs-lookup"><span data-stu-id="8b129-586">7</span></span>          | <span data-ttu-id="8b129-587">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="8b129-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="8b129-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="8b129-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="8b129-589">\-22,794</span></span>                                       | <span data-ttu-id="8b129-590">1.000</span><span class="sxs-lookup"><span data-stu-id="8b129-590">1,000</span></span>                                          | <span data-ttu-id="8b129-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="8b129-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="8b129-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="8b129-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="8b129-593">8</span><span class="sxs-lookup"><span data-stu-id="8b129-593">8</span></span>          | <span data-ttu-id="8b129-594">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="8b129-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="8b129-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="8b129-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="8b129-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="8b129-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="8b129-597">94\.97</span></span>                                  |
| <span data-ttu-id="8b129-598">9</span><span class="sxs-lookup"><span data-stu-id="8b129-598">9</span></span>          | <span data-ttu-id="8b129-599">Indløsning</span><span class="sxs-lookup"><span data-stu-id="8b129-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="8b129-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="8b129-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8b129-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="8b129-603">10</span><span class="sxs-lookup"><span data-stu-id="8b129-603">10</span></span>         | <span data-ttu-id="8b129-604">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="8b129-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="8b129-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="8b129-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="8b129-606">949\.75</span></span>                                        | <span data-ttu-id="8b129-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="8b129-607">949\.75</span></span>                                 |
| <span data-ttu-id="8b129-608">11</span><span class="sxs-lookup"><span data-stu-id="8b129-608">11</span></span>         | <span data-ttu-id="8b129-609">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="8b129-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="8b129-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="8b129-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="8b129-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="8b129-611">\-949\.75</span></span>                                      | <span data-ttu-id="8b129-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="8b129-612">\-949\.75</span></span>                               |


