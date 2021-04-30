---
title: Dobbeltrapportering
description: I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881150"
---
# <a name="dual-reporting"></a><span data-ttu-id="b00c8-103">Dobbeltrapportering</span><span class="sxs-lookup"><span data-stu-id="b00c8-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b00c8-104">I dette emne gennemgås et eksempel med, hvordan du kan opfylde kravene til både rapportering af International Financial Reporting Standard (IFRS) og lovpligtig rapportering i aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="b00c8-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="b00c8-105">Det er nødvendigt med kendskab til posteringslag i Microsoft Dynamics 365 Finance, og det vil gøre det nemmere at forstå i eksemplet.</span><span class="sxs-lookup"><span data-stu-id="b00c8-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="b00c8-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b00c8-106">Example</span></span>

<span data-ttu-id="b00c8-107">Følgende eksempelkonti til en leaseaftale under italiensk lovpligtig rapportering ved hjælp af både likviditetsmetoden og IFRS-rapporteringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="b00c8-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="b00c8-108">Firmaet skal etablere tre kartoteker for at kunne redegøre for både de italienske lovpligtige krav og IFRS 16-krav.</span><span class="sxs-lookup"><span data-stu-id="b00c8-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="b00c8-109">Der kræves et kartotek til IFRS 16, et kartotek til lovpligtige krav, og et kartotek til automatisk tilbageføring af lovpligtige bogføringer.</span><span class="sxs-lookup"><span data-stu-id="b00c8-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="b00c8-110">Kartotekerne oprettes som vist i følgende tabeller.</span><span class="sxs-lookup"><span data-stu-id="b00c8-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="b00c8-111">**IFRS 16-kartotek**</span><span class="sxs-lookup"><span data-stu-id="b00c8-111">**IFRS 16 book**</span></span>

<span data-ttu-id="b00c8-112">IFRS 16-kartoteket er konfigureret, så det overholder IFRS 16-regnskabsstandarden.</span><span class="sxs-lookup"><span data-stu-id="b00c8-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="b00c8-113">Alle poster, der er bogført i dette kartotek, bogføres i et brugerdefineret lag.</span><span class="sxs-lookup"><span data-stu-id="b00c8-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="b00c8-114">Navn</span><span class="sxs-lookup"><span data-stu-id="b00c8-114">Name</span></span>                                    | <span data-ttu-id="b00c8-115">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="b00c8-116">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="b00c8-116">Book type</span></span>                               | <span data-ttu-id="b00c8-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="b00c8-117">IFRS 16</span></span>        |
| <span data-ttu-id="b00c8-118">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-118">Book description</span></span>                        | <span data-ttu-id="b00c8-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="b00c8-119">IFRS 16</span></span>        |
| <span data-ttu-id="b00c8-120">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="b00c8-120">Posting Layer</span></span>                           | <span data-ttu-id="b00c8-121">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="b00c8-121">Custom layer 1</span></span> |
| <span data-ttu-id="b00c8-122">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="b00c8-122">Lease Type</span></span>                              | <span data-ttu-id="b00c8-123">Finance</span><span class="sxs-lookup"><span data-stu-id="b00c8-123">Finance</span></span>        |
| <span data-ttu-id="b00c8-124">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="b00c8-124">Accounting Framework</span></span>                    | <span data-ttu-id="b00c8-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="b00c8-125">IFRS 16</span></span>        |
| <span data-ttu-id="b00c8-126">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="b00c8-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="b00c8-127">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-127">0.00</span></span>           |
| <span data-ttu-id="b00c8-128">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="b00c8-129">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-129">0.00</span></span>           |
| <span data-ttu-id="b00c8-130">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="b00c8-130">Short-term threshold</span></span>                    | <span data-ttu-id="b00c8-131">12</span><span class="sxs-lookup"><span data-stu-id="b00c8-131">12</span></span>             |
| <span data-ttu-id="b00c8-132">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="b00c8-132">Low Value Threshold</span></span>                     | <span data-ttu-id="b00c8-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-133">5,000.00</span></span>       |
| <span data-ttu-id="b00c8-134">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-134">Pay to Vendor</span></span>                           | <span data-ttu-id="b00c8-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="b00c8-135">No</span></span>             |

<span data-ttu-id="b00c8-136">**Lovpligtigt kartotek**</span><span class="sxs-lookup"><span data-stu-id="b00c8-136">**Statutory book**</span></span>

<span data-ttu-id="b00c8-137">Det lovpligtige kartotek er en kassekladde, hvor firmaet kan redegøre for leasingudgifter som det kontantbeløb, der betales hver måned for leje.</span><span class="sxs-lookup"><span data-stu-id="b00c8-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="b00c8-138">Dette kartotek opretter ikke et ROU-aktiv eller en leasingforpligtelse.</span><span class="sxs-lookup"><span data-stu-id="b00c8-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="b00c8-139">Navn</span><span class="sxs-lookup"><span data-stu-id="b00c8-139">Name</span></span>                                    | <span data-ttu-id="b00c8-140">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="b00c8-141">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="b00c8-141">Book type</span></span>                               | <span data-ttu-id="b00c8-142">Lovpligtig</span><span class="sxs-lookup"><span data-stu-id="b00c8-142">Statutory</span></span>   |
| <span data-ttu-id="b00c8-143">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-143">Book description</span></span>                        | <span data-ttu-id="b00c8-144">Lokal GAAP</span><span class="sxs-lookup"><span data-stu-id="b00c8-144">Local GAAP</span></span>  |
| <span data-ttu-id="b00c8-145">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="b00c8-145">Posting Layer</span></span>                           | <span data-ttu-id="b00c8-146">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-146">Current</span></span>     |
| <span data-ttu-id="b00c8-147">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="b00c8-147">Lease Type</span></span>                              | <span data-ttu-id="b00c8-148">Automatisk</span><span class="sxs-lookup"><span data-stu-id="b00c8-148">Automatic</span></span>   |
| <span data-ttu-id="b00c8-149">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="b00c8-149">Accounting Framework</span></span>                    | <span data-ttu-id="b00c8-150">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="b00c8-150">Cash basis</span></span>  |
| <span data-ttu-id="b00c8-151">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="b00c8-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="b00c8-152">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-152">0.00</span></span>        |
| <span data-ttu-id="b00c8-153">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="b00c8-154">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-154">0.00</span></span>        |
| <span data-ttu-id="b00c8-155">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="b00c8-155">Short-term threshold</span></span>                    | <span data-ttu-id="b00c8-156">0</span><span class="sxs-lookup"><span data-stu-id="b00c8-156">0</span></span>           |
| <span data-ttu-id="b00c8-157">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="b00c8-157">Low Value Threshold</span></span>                     | <span data-ttu-id="b00c8-158">0</span><span class="sxs-lookup"><span data-stu-id="b00c8-158">0</span></span>           |
| <span data-ttu-id="b00c8-159">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-159">Pay to Vendor</span></span>                           | <span data-ttu-id="b00c8-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="b00c8-160">No</span></span>          |

<span data-ttu-id="b00c8-161">**Lovpligtigt tilbageført kartotek**</span><span class="sxs-lookup"><span data-stu-id="b00c8-161">**Statutory reversal book**</span></span>

<span data-ttu-id="b00c8-162">Det lovpligtige tilbageførte kartotek konfigureres på samme måde som det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="b00c8-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="b00c8-163">Navn</span><span class="sxs-lookup"><span data-stu-id="b00c8-163">Name</span></span>                                    | <span data-ttu-id="b00c8-164">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="b00c8-165">Kartotekstype</span><span class="sxs-lookup"><span data-stu-id="b00c8-165">Book type</span></span>                               | <span data-ttu-id="b00c8-166">Lovpligtig - tilbageført</span><span class="sxs-lookup"><span data-stu-id="b00c8-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="b00c8-167">Bogbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-167">Book description</span></span>                        | <span data-ttu-id="b00c8-168">Kartotek, der skal tilbageføre lovpligtigt kartotek</span><span class="sxs-lookup"><span data-stu-id="b00c8-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="b00c8-169">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="b00c8-169">Posting Layer</span></span>                           | <span data-ttu-id="b00c8-170">Brugerdefineret lag 1</span><span class="sxs-lookup"><span data-stu-id="b00c8-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="b00c8-171">Leasingaftaletype</span><span class="sxs-lookup"><span data-stu-id="b00c8-171">Lease Type</span></span>                              | <span data-ttu-id="b00c8-172">Automatisk</span><span class="sxs-lookup"><span data-stu-id="b00c8-172">Automatic</span></span>                      |
| <span data-ttu-id="b00c8-173">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="b00c8-173">Accounting Framework</span></span>                    | <span data-ttu-id="b00c8-174">Kontantgrundlag</span><span class="sxs-lookup"><span data-stu-id="b00c8-174">Cash basis</span></span>                     |
| <span data-ttu-id="b00c8-175">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="b00c8-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="b00c8-176">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-176">0.00</span></span>                           |
| <span data-ttu-id="b00c8-177">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="b00c8-178">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-178">0.00</span></span>                           |
| <span data-ttu-id="b00c8-179">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="b00c8-179">Short-term threshold</span></span>                    | <span data-ttu-id="b00c8-180">0</span><span class="sxs-lookup"><span data-stu-id="b00c8-180">0</span></span>                              |
| <span data-ttu-id="b00c8-181">Grænse for lav værdi</span><span class="sxs-lookup"><span data-stu-id="b00c8-181">Low Value Threshold</span></span>                     | <span data-ttu-id="b00c8-182">0</span><span class="sxs-lookup"><span data-stu-id="b00c8-182">0</span></span>                              |
| <span data-ttu-id="b00c8-183">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-183">Pay to Vendor</span></span>                           | <span data-ttu-id="b00c8-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="b00c8-184">No</span></span>                             |

<span data-ttu-id="b00c8-185">I dette eksempel er der oprettet en leasingaftale, der indeholder følgende indstillinger under fanerne **Generelt** og **Betalingsplanlinje**.</span><span class="sxs-lookup"><span data-stu-id="b00c8-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="b00c8-186">Fanen **Generelt**</span><span class="sxs-lookup"><span data-stu-id="b00c8-186">**General tab**</span></span>

| <span data-ttu-id="b00c8-187">Felt</span><span class="sxs-lookup"><span data-stu-id="b00c8-187">Field</span></span>                      | <span data-ttu-id="b00c8-188">Værdi</span><span class="sxs-lookup"><span data-stu-id="b00c8-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="b00c8-189">Trinvis lånesats</span><span class="sxs-lookup"><span data-stu-id="b00c8-189">Incremental borrowing rate</span></span> | <span data-ttu-id="b00c8-190">5 %</span><span class="sxs-lookup"><span data-stu-id="b00c8-190">5%</span></span>               |
| <span data-ttu-id="b00c8-191">Dato for påbegyndelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-191">Commencement date</span></span>          | <span data-ttu-id="b00c8-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="b00c8-192">1/1/2020</span></span>         |
| <span data-ttu-id="b00c8-193">Leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="b00c8-193">Lease group</span></span>                | <span data-ttu-id="b00c8-194">Bygninger</span><span class="sxs-lookup"><span data-stu-id="b00c8-194">Buildings</span></span>        |
| <span data-ttu-id="b00c8-195">Leverandør</span><span class="sxs-lookup"><span data-stu-id="b00c8-195">Vendor</span></span>                     | <span data-ttu-id="b00c8-196">1001</span><span class="sxs-lookup"><span data-stu-id="b00c8-196">1001</span></span>             |
| <span data-ttu-id="b00c8-197">Aktivets handelsværdi</span><span class="sxs-lookup"><span data-stu-id="b00c8-197">Fair value of the asset</span></span>    | <span data-ttu-id="b00c8-198">245,000</span><span class="sxs-lookup"><span data-stu-id="b00c8-198">245,000</span></span>          |
| <span data-ttu-id="b00c8-199">Brugstid for aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-199">Asset useful life</span></span>          | <span data-ttu-id="b00c8-200">120</span><span class="sxs-lookup"><span data-stu-id="b00c8-200">120</span></span>              |
| <span data-ttu-id="b00c8-201">Annuitetstype</span><span class="sxs-lookup"><span data-stu-id="b00c8-201">Annuity type</span></span>               | <span data-ttu-id="b00c8-202">Almindelig annuitet</span><span class="sxs-lookup"><span data-stu-id="b00c8-202">Ordinary annuity</span></span> |
| <span data-ttu-id="b00c8-203">Sammensætningsinterval</span><span class="sxs-lookup"><span data-stu-id="b00c8-203">Compounding interval</span></span>       | <span data-ttu-id="b00c8-204">Månedligt</span><span class="sxs-lookup"><span data-stu-id="b00c8-204">Monthly</span></span>          |

<span data-ttu-id="b00c8-205">**Betalingsplanlinjer-fane**</span><span class="sxs-lookup"><span data-stu-id="b00c8-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="b00c8-206">Felt</span><span class="sxs-lookup"><span data-stu-id="b00c8-206">Field</span></span>             | <span data-ttu-id="b00c8-207">Værdi</span><span class="sxs-lookup"><span data-stu-id="b00c8-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="b00c8-208">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="b00c8-208">Start date</span></span>        | <span data-ttu-id="b00c8-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="b00c8-209">1/1/2020</span></span>   |
| <span data-ttu-id="b00c8-210">Periodeinterval</span><span class="sxs-lookup"><span data-stu-id="b00c8-210">Period interval</span></span>   | <span data-ttu-id="b00c8-211">Måneder</span><span class="sxs-lookup"><span data-stu-id="b00c8-211">Months</span></span>     |
| <span data-ttu-id="b00c8-212">Perioder</span><span class="sxs-lookup"><span data-stu-id="b00c8-212">Periods</span></span>           | <span data-ttu-id="b00c8-213">24</span><span class="sxs-lookup"><span data-stu-id="b00c8-213">24</span></span>         |
| <span data-ttu-id="b00c8-214">Slutdato</span><span class="sxs-lookup"><span data-stu-id="b00c8-214">End date</span></span>          | <span data-ttu-id="b00c8-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="b00c8-215">12/31/2020</span></span> |
| <span data-ttu-id="b00c8-216">Betalingshyppighed</span><span class="sxs-lookup"><span data-stu-id="b00c8-216">Payment frequency</span></span> | <span data-ttu-id="b00c8-217">Månedligt</span><span class="sxs-lookup"><span data-stu-id="b00c8-217">Monthly</span></span>    |
| <span data-ttu-id="b00c8-218">Betalingsbeløb</span><span class="sxs-lookup"><span data-stu-id="b00c8-218">Payment amount</span></span>    | <span data-ttu-id="b00c8-219">1.000</span><span class="sxs-lookup"><span data-stu-id="b00c8-219">1,000</span></span>      |

<span data-ttu-id="b00c8-220">Hvis du vil redegøre for denne leasingaftale i forbindelse med to strukturer, skal du bruge et aktuelt posteringslag og et brugerdefineret posteringslag.</span><span class="sxs-lookup"><span data-stu-id="b00c8-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="b00c8-221">Følgende tabel viser et eksempel på hver kladdepost, der er nødvendig for at repræsentere finanserne i de enkelte rapporteringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="b00c8-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="b00c8-222">En detaljeret beskrivelse af de enkelte kladdeposter for den første måned af leasingaftalen tildeles bagefter.</span><span class="sxs-lookup"><span data-stu-id="b00c8-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="b00c8-223">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="b00c8-224">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="b00c8-225">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="b00c8-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="b00c8-226">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-226">Current layer total</span></span></th>
<th><span data-ttu-id="b00c8-227">Tilbageført kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="b00c8-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="b00c8-228">IFRS 16-kartotek (brugerdefineret lag)</span><span class="sxs-lookup"><span data-stu-id="b00c8-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="b00c8-229">Aktuelt lag + brugerdefineret lag i alt</span><span class="sxs-lookup"><span data-stu-id="b00c8-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b00c8-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="b00c8-230">JE-100</span></span></th>
<th><span data-ttu-id="b00c8-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="b00c8-231">JE-110</span></span></th>
<th><span data-ttu-id="b00c8-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="b00c8-232">JE-120</span></span></th>
<th><span data-ttu-id="b00c8-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="b00c8-233">JE-130</span></span></th>
<th><span data-ttu-id="b00c8-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="b00c8-234">JE-140</span></span></th>
<th><span data-ttu-id="b00c8-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="b00c8-235">JE-150</span></span></th>
<th><span data-ttu-id="b00c8-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="b00c8-236">JE-160</span></span></th>
<th><span data-ttu-id="b00c8-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="b00c8-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b00c8-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b00c8-246">1</span><span class="sxs-lookup"><span data-stu-id="b00c8-246">1</span></span></td>
<td><span data-ttu-id="b00c8-247">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-247">Lease expense</span></span></td>
<td><span data-ttu-id="b00c8-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-249">1,000.00</span></span></td>
<td><span data-ttu-id="b00c8-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-251">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-252">2</span><span class="sxs-lookup"><span data-stu-id="b00c8-252">2</span></span></td>
<td><span data-ttu-id="b00c8-253">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="b00c8-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-254">3.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-255">3.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-256">3.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-257">3</span><span class="sxs-lookup"><span data-stu-id="b00c8-257">3</span></span></td>
<td><span data-ttu-id="b00c8-258">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-259">5.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-260">5.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-261">5.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-262">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-262">4</span></span></td>
<td><span data-ttu-id="b00c8-263">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-263">Clearing account</span></span></td>
<td><span data-ttu-id="b00c8-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-264">-1,000.00</span></span></td>
<td><span data-ttu-id="b00c8-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-266">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-266">0.00</span></span></td>
<td><span data-ttu-id="b00c8-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-269">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-270">5</span><span class="sxs-lookup"><span data-stu-id="b00c8-270">5</span></span></td>
<td><span data-ttu-id="b00c8-271">Kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-272">-1,008.00</span></span></td>
<td><span data-ttu-id="b00c8-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-273">1,008.00</span></span></td>
<td><span data-ttu-id="b00c8-274">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-275">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-276">6</span><span class="sxs-lookup"><span data-stu-id="b00c8-276">6</span></span></td>
<td><span data-ttu-id="b00c8-277">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-278">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="b00c8-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-281">7</span><span class="sxs-lookup"><span data-stu-id="b00c8-281">7</span></span></td>
<td><span data-ttu-id="b00c8-282">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-283">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-284">-22,794.00</span></span></td>
<td><span data-ttu-id="b00c8-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-285">1,000.00</span></span></td>
<td><span data-ttu-id="b00c8-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="b00c8-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="b00c8-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-288">8</span><span class="sxs-lookup"><span data-stu-id="b00c8-288">8</span></span></td>
<td><span data-ttu-id="b00c8-289">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-290">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-291">94.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-292">94.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-293">9</span><span class="sxs-lookup"><span data-stu-id="b00c8-293">9</span></span></td>
<td><span data-ttu-id="b00c8-294">Indløsning</span><span class="sxs-lookup"><span data-stu-id="b00c8-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-295">-1,008.00</span></span></td>
<td><span data-ttu-id="b00c8-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-298">10</span><span class="sxs-lookup"><span data-stu-id="b00c8-298">10</span></span></td>
<td><span data-ttu-id="b00c8-299">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="b00c8-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-300">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-301">949.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-301">949.75</span></span></td>
<td><span data-ttu-id="b00c8-302">949.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-303">11</span><span class="sxs-lookup"><span data-stu-id="b00c8-303">11</span></span></td>
<td><span data-ttu-id="b00c8-304">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="b00c8-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-305">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="b00c8-306">-949.75</span></span></td>
<td><span data-ttu-id="b00c8-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="b00c8-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b00c8-308">Som vist i den foregående tabel, skal der rapporteres tre kartoteker under både lovpligtig rapportering og IFRS-rapportering.</span><span class="sxs-lookup"><span data-stu-id="b00c8-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="b00c8-309">I det lovpligtige kartotek registreres leasingbetalingen i henhold til reglerne for kontantregnskab under det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="b00c8-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="b00c8-310">Det lovpligtige tilbageførte kartotek tilbagefører de lovpligtige kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="b00c8-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="b00c8-311">IFRS 16-kartoteket opretter de kladdeposteringer, der er påkrævet i IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="b00c8-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="b00c8-312">Du skal kun angive en leasingaftale én gang.</span><span class="sxs-lookup"><span data-stu-id="b00c8-312">You must enter a lease only one time.</span></span> <span data-ttu-id="b00c8-313">Du kan derefter åbne siden **Kartoteker** for at se alle de kartoteker, der er tilknyttet leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="b00c8-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="b00c8-314">Når du opretter kartotekerne, skal de alle tre knyttes til samme leasingpost.</span><span class="sxs-lookup"><span data-stu-id="b00c8-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="b00c8-315">Den første kladdepostering registrerer leasingudgiften i henhold til det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="b00c8-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="b00c8-316">Du kan oprette betalinger enten i en batch eller ved at vælge betalingsplanen i det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="b00c8-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="b00c8-317">I dette eksempel er der oprettet følgende kladdepost for det lovpligtige kartotek fra betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="b00c8-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="b00c8-318">Leasingbetaling - 1/31/2020 - JE 100</span><span class="sxs-lookup"><span data-stu-id="b00c8-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="b00c8-319">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-319">Account type</span></span> | <span data-ttu-id="b00c8-320">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-320">Account number</span></span> | <span data-ttu-id="b00c8-321">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-321">Layer</span></span>   | <span data-ttu-id="b00c8-322">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-322">Account description</span></span> | <span data-ttu-id="b00c8-323">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-323">Debit</span></span>    | <span data-ttu-id="b00c8-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="b00c8-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-325">Ledger</span></span>       | <span data-ttu-id="b00c8-326">1</span><span class="sxs-lookup"><span data-stu-id="b00c8-326">1</span></span>              | <span data-ttu-id="b00c8-327">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-327">Current</span></span> | <span data-ttu-id="b00c8-328">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-328">Lease expense</span></span>       | <span data-ttu-id="b00c8-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-329">1,000.00</span></span> |          |
| <span data-ttu-id="b00c8-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-330">Ledger</span></span>       | <span data-ttu-id="b00c8-331">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-331">4</span></span>              | <span data-ttu-id="b00c8-332">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-332">Current</span></span> | <span data-ttu-id="b00c8-333">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-333">Clearing account</span></span>    |          | <span data-ttu-id="b00c8-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-334">1,000.00</span></span> |

<span data-ttu-id="b00c8-335">En kreditormedarbejder bruger standardfunktionen for Dynamics 365 til at oprette en faktura, der skal betale for leasingaftalen uden for aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="b00c8-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="b00c8-336">I stedet for at vælge **leasingudgift** som debetkonto vælger kreditormedarbejderen en clearingkonto til at generere følgende post.</span><span class="sxs-lookup"><span data-stu-id="b00c8-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="b00c8-337">AP-proces – 31/1/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="b00c8-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="b00c8-338">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-338">Account type</span></span> | <span data-ttu-id="b00c8-339">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-339">Account number</span></span> | <span data-ttu-id="b00c8-340">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-340">Layer</span></span>   | <span data-ttu-id="b00c8-341">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-341">Account description</span></span> | <span data-ttu-id="b00c8-342">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-342">Debit</span></span>    | <span data-ttu-id="b00c8-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="b00c8-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-344">Ledger</span></span>       | <span data-ttu-id="b00c8-345">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-345">4</span></span>              | <span data-ttu-id="b00c8-346">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-346">Current</span></span> | <span data-ttu-id="b00c8-347">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-347">Clearing account</span></span>    | <span data-ttu-id="b00c8-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-348">1,000.00</span></span> |          |
| <span data-ttu-id="b00c8-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-349">Ledger</span></span>       | <span data-ttu-id="b00c8-350">2</span><span class="sxs-lookup"><span data-stu-id="b00c8-350">2</span></span>              | <span data-ttu-id="b00c8-351">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-351">Current</span></span> | <span data-ttu-id="b00c8-352">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="b00c8-352">Bank fee</span></span>            | <span data-ttu-id="b00c8-353">3.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-353">3.00</span></span>     |          |
| <span data-ttu-id="b00c8-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-354">Ledger</span></span>       | <span data-ttu-id="b00c8-355">3</span><span class="sxs-lookup"><span data-stu-id="b00c8-355">3</span></span>              | <span data-ttu-id="b00c8-356">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-356">Current</span></span> | <span data-ttu-id="b00c8-357">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-357">VAT expense</span></span>         | <span data-ttu-id="b00c8-358">5.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-358">5.00</span></span>     |          |
| <span data-ttu-id="b00c8-359">Leverandør</span><span class="sxs-lookup"><span data-stu-id="b00c8-359">Vendor</span></span>       | <span data-ttu-id="b00c8-360">5</span><span class="sxs-lookup"><span data-stu-id="b00c8-360">5</span></span>              | <span data-ttu-id="b00c8-361">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-361">Current</span></span> | <span data-ttu-id="b00c8-362">Kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-362">Accounts payable</span></span>    |          | <span data-ttu-id="b00c8-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-363">1,008.00</span></span> |

<span data-ttu-id="b00c8-364">Når opgørelsen er udstedt til leverandøren, skal du følge den almindelige betalingsproces.</span><span class="sxs-lookup"><span data-stu-id="b00c8-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="b00c8-365">Under denne proces genereres følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="b00c8-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="b00c8-366">Kontant betaling – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="b00c8-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="b00c8-367">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-367">Account type</span></span> | <span data-ttu-id="b00c8-368">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-368">Account number</span></span> | <span data-ttu-id="b00c8-369">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-369">Layer</span></span>   | <span data-ttu-id="b00c8-370">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-370">Account description</span></span> | <span data-ttu-id="b00c8-371">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-371">Debit</span></span>    | <span data-ttu-id="b00c8-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="b00c8-373">Leverandør</span><span class="sxs-lookup"><span data-stu-id="b00c8-373">Vendor</span></span>       | <span data-ttu-id="b00c8-374">5</span><span class="sxs-lookup"><span data-stu-id="b00c8-374">5</span></span>              | <span data-ttu-id="b00c8-375">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-375">Current</span></span> | <span data-ttu-id="b00c8-376">Kreditorer</span><span class="sxs-lookup"><span data-stu-id="b00c8-376">Accounts Payable</span></span>    | <span data-ttu-id="b00c8-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-377">1,008.00</span></span> |          |
| <span data-ttu-id="b00c8-378">Bank</span><span class="sxs-lookup"><span data-stu-id="b00c8-378">Bank</span></span>         | <span data-ttu-id="b00c8-379">9</span><span class="sxs-lookup"><span data-stu-id="b00c8-379">9</span></span>              | <span data-ttu-id="b00c8-380">Løbende</span><span class="sxs-lookup"><span data-stu-id="b00c8-380">Current</span></span> | <span data-ttu-id="b00c8-381">Indløsning</span><span class="sxs-lookup"><span data-stu-id="b00c8-381">Cash</span></span>                |          | <span data-ttu-id="b00c8-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-382">1,008.00</span></span> |

<span data-ttu-id="b00c8-383">På dette tidspunkt har du taget fuld højde for denne leasingaftale under lovpligtige rapporteringskrav og kan generere en råbalance ved hjælp af det aktuelle lag.</span><span class="sxs-lookup"><span data-stu-id="b00c8-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="b00c8-384">Systemet returnerer en råbalance, der har følgende tal.</span><span class="sxs-lookup"><span data-stu-id="b00c8-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="b00c8-385">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="b00c8-386">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="b00c8-387">Lovpligtigt kartotek (aktuelt lag)</span><span class="sxs-lookup"><span data-stu-id="b00c8-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="b00c8-388">Aktuelt samlet lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b00c8-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="b00c8-389">JE-100</span></span></th>
<th><span data-ttu-id="b00c8-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="b00c8-390">JE-110</span></span></th>
<th><span data-ttu-id="b00c8-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="b00c8-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b00c8-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="b00c8-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="b00c8-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b00c8-395">1</span><span class="sxs-lookup"><span data-stu-id="b00c8-395">1</span></span></td>
<td><span data-ttu-id="b00c8-396">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-396">Lease expense</span></span></td>
<td><span data-ttu-id="b00c8-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-399">2</span><span class="sxs-lookup"><span data-stu-id="b00c8-399">2</span></span></td>
<td><span data-ttu-id="b00c8-400">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="b00c8-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-401">3.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-402">3.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-403">3</span><span class="sxs-lookup"><span data-stu-id="b00c8-403">3</span></span></td>
<td><span data-ttu-id="b00c8-404">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-405">5.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-406">5.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-407">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-407">4</span></span></td>
<td><span data-ttu-id="b00c8-408">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-408">Clearing account</span></span></td>
<td><span data-ttu-id="b00c8-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-409">-1,000.00</span></span></td>
<td><span data-ttu-id="b00c8-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-411">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-412">5</span><span class="sxs-lookup"><span data-stu-id="b00c8-412">5</span></span></td>
<td><span data-ttu-id="b00c8-413">Kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="b00c8-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-414">-1,008.00</span></span></td>
<td><span data-ttu-id="b00c8-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-415">1,008.00</span></span></td>
<td><span data-ttu-id="b00c8-416">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-417">6</span><span class="sxs-lookup"><span data-stu-id="b00c8-417">6</span></span></td>
<td><span data-ttu-id="b00c8-418">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-419">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-420">7</span><span class="sxs-lookup"><span data-stu-id="b00c8-420">7</span></span></td>
<td><span data-ttu-id="b00c8-421">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-422">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-423">8</span><span class="sxs-lookup"><span data-stu-id="b00c8-423">8</span></span></td>
<td><span data-ttu-id="b00c8-424">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-425">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-426">9</span><span class="sxs-lookup"><span data-stu-id="b00c8-426">9</span></span></td>
<td><span data-ttu-id="b00c8-427">Indløsning</span><span class="sxs-lookup"><span data-stu-id="b00c8-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-428">-1,008.00</span></span></td>
<td><span data-ttu-id="b00c8-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-430">10</span><span class="sxs-lookup"><span data-stu-id="b00c8-430">10</span></span></td>
<td><span data-ttu-id="b00c8-431">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="b00c8-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-432">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b00c8-433">11</span><span class="sxs-lookup"><span data-stu-id="b00c8-433">11</span></span></td>
<td><span data-ttu-id="b00c8-434">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="b00c8-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="b00c8-435">0,00</span><span class="sxs-lookup"><span data-stu-id="b00c8-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b00c8-436">Hvis du vil bruge IFRS 16-tal til at køre samme råbalance, skal de lovpligtige regnskabskladdeposteringer tilbageføres, og de IFRS 16-journaloptegnelser skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="b00c8-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="b00c8-437">Hvis du vil tilbageføre lovpligtige kladdeposteringer, skal dette eksempel indeholde en lovpligtig tilbageførsel, der har samme opsætning som det lovpligtige kartotek, men en modsat posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="b00c8-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="b00c8-438">Det lovpligtige kartotek har *debiteret* en konto til leasingomkostninger, men det tilbagevendende kartotek vil *kreditere* denne konto.</span><span class="sxs-lookup"><span data-stu-id="b00c8-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="b00c8-439">Disse relationer defineres nemt i bankkonti for aktivleasing på siden **Aktivleasingparametre** (**Aktivleasing \> Konfiguration \> Aktivleasingparametre**).</span><span class="sxs-lookup"><span data-stu-id="b00c8-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="b00c8-440">Når den samme proces, der blev anvendt til det lovpligtige kartotek, bruges i et tilbageført kartotek, oprettes følgende kladdepost.</span><span class="sxs-lookup"><span data-stu-id="b00c8-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="b00c8-441">Forskellen er, at det tilbageførte kartotek registrerer posteringer fra det lovpligtige kartotek.</span><span class="sxs-lookup"><span data-stu-id="b00c8-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="b00c8-442">De tilbageførte posteringer foretages også i det brugerdefinerede lag.</span><span class="sxs-lookup"><span data-stu-id="b00c8-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="b00c8-443">Når der køres en råbalance på det aktuelle lag, medtages der ikke kladdeposteringer til tilbageførsel.</span><span class="sxs-lookup"><span data-stu-id="b00c8-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="b00c8-444">Leasingbetaling - 31/1/2020 - JE 130</span><span class="sxs-lookup"><span data-stu-id="b00c8-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="b00c8-445">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-445">Account type</span></span> | <span data-ttu-id="b00c8-446">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-446">Account number</span></span> | <span data-ttu-id="b00c8-447">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-447">Layer</span></span>  | <span data-ttu-id="b00c8-448">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-448">Account description</span></span> | <span data-ttu-id="b00c8-449">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-449">Debit</span></span>    | <span data-ttu-id="b00c8-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="b00c8-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-451">Ledger</span></span>       | <span data-ttu-id="b00c8-452">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-452">4</span></span>              | <span data-ttu-id="b00c8-453">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-453">Custom</span></span> | <span data-ttu-id="b00c8-454">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-454">Clearing account</span></span>    | <span data-ttu-id="b00c8-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-455">1,000.00</span></span> |          |
| <span data-ttu-id="b00c8-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-456">Ledger</span></span>       | <span data-ttu-id="b00c8-457">1</span><span class="sxs-lookup"><span data-stu-id="b00c8-457">1</span></span>              | <span data-ttu-id="b00c8-458">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-458">Custom</span></span> | <span data-ttu-id="b00c8-459">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-459">Lease expense</span></span>       |          | <span data-ttu-id="b00c8-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-460">1,000.00</span></span> |

<span data-ttu-id="b00c8-461">Nu, hvor du har elimineret lovpligtige kladdeposteringer, skal du reservere alle de kladdeposter, IFRS 16 har brug for, i IFRS 16-kartoteket.</span><span class="sxs-lookup"><span data-stu-id="b00c8-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="b00c8-462">Disse poster omfatter den første anerkendelse af ROU-aktiv og ansvarsforsikring samt posten med renter og afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b00c8-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="b00c8-463">Første indregning – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="b00c8-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="b00c8-464">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-464">Account type</span></span> | <span data-ttu-id="b00c8-465">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-465">Account number</span></span> | <span data-ttu-id="b00c8-466">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-466">Layer</span></span>  | <span data-ttu-id="b00c8-467">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-467">Account description</span></span>      | <span data-ttu-id="b00c8-468">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-468">Debit</span></span>     | <span data-ttu-id="b00c8-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="b00c8-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-470">Ledger</span></span>       | <span data-ttu-id="b00c8-471">6</span><span class="sxs-lookup"><span data-stu-id="b00c8-471">6</span></span>              | <span data-ttu-id="b00c8-472">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-472">Custom</span></span> | <span data-ttu-id="b00c8-473">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-473">ROU Asset</span></span>                | <span data-ttu-id="b00c8-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="b00c8-474">22,793.90</span></span> |           |
| <span data-ttu-id="b00c8-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-475">Ledger</span></span>       | <span data-ttu-id="b00c8-476">7</span><span class="sxs-lookup"><span data-stu-id="b00c8-476">7</span></span>              | <span data-ttu-id="b00c8-477">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-477">Custom</span></span> | <span data-ttu-id="b00c8-478">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-478">Finance lease obligation</span></span> |           | <span data-ttu-id="b00c8-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="b00c8-479">22,793.90</span></span> |

<span data-ttu-id="b00c8-480">Leasingbetalingen bogføres på samme måde som andre leasingbetalinger.</span><span class="sxs-lookup"><span data-stu-id="b00c8-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="b00c8-481">Årsagen til brug af clearing kontoen er at sikre, at kontant kun krediteres én gang.</span><span class="sxs-lookup"><span data-stu-id="b00c8-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="b00c8-482">Leasingbetaling - 31/1/2020 - JE 150</span><span class="sxs-lookup"><span data-stu-id="b00c8-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="b00c8-483">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-483">Account type</span></span> | <span data-ttu-id="b00c8-484">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-484">Account number</span></span> | <span data-ttu-id="b00c8-485">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-485">Layer</span></span>  | <span data-ttu-id="b00c8-486">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-486">Account description</span></span>      | <span data-ttu-id="b00c8-487">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-487">Debit</span></span>    | <span data-ttu-id="b00c8-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="b00c8-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-489">Ledger</span></span>       | <span data-ttu-id="b00c8-490">7</span><span class="sxs-lookup"><span data-stu-id="b00c8-490">7</span></span>              | <span data-ttu-id="b00c8-491">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-491">Custom</span></span> | <span data-ttu-id="b00c8-492">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-492">Finance lease obligation</span></span> | <span data-ttu-id="b00c8-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-493">1,000.00</span></span> |          |
| <span data-ttu-id="b00c8-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-494">Ledger</span></span>       | <span data-ttu-id="b00c8-495">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-495">4</span></span>              | <span data-ttu-id="b00c8-496">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-496">Custom</span></span> | <span data-ttu-id="b00c8-497">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-497">Clearing account</span></span>         |          | <span data-ttu-id="b00c8-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-498">1,000.00</span></span> |

<span data-ttu-id="b00c8-499">Renteudgiftskladdeposten genereres fra planen for passiv afskrivning.</span><span class="sxs-lookup"><span data-stu-id="b00c8-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="b00c8-500">Renteudgift – 31/1/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="b00c8-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="b00c8-501">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-501">Account type</span></span> | <span data-ttu-id="b00c8-502">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-502">Account number</span></span> | <span data-ttu-id="b00c8-503">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-503">Layer</span></span>  | <span data-ttu-id="b00c8-504">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-504">Account description</span></span>      | <span data-ttu-id="b00c8-505">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-505">Debit</span></span> | <span data-ttu-id="b00c8-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="b00c8-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-507">Ledger</span></span>       | <span data-ttu-id="b00c8-508">8</span><span class="sxs-lookup"><span data-stu-id="b00c8-508">8</span></span>              | <span data-ttu-id="b00c8-509">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-509">Custom</span></span> | <span data-ttu-id="b00c8-510">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-510">Interest expense</span></span>         | <span data-ttu-id="b00c8-511">94.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-511">94.97</span></span> |        |
| <span data-ttu-id="b00c8-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-512">Ledger</span></span>       | <span data-ttu-id="b00c8-513">7</span><span class="sxs-lookup"><span data-stu-id="b00c8-513">7</span></span>              | <span data-ttu-id="b00c8-514">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-514">Custom</span></span> | <span data-ttu-id="b00c8-515">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-515">Finance lease obligation</span></span> |       | <span data-ttu-id="b00c8-516">94.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-516">94.97</span></span>  |

<span data-ttu-id="b00c8-517">Afskrivningsudgiftskladdeposten genereres fra planen for aktivafskrivning.</span><span class="sxs-lookup"><span data-stu-id="b00c8-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="b00c8-518">Afskrivningsudgift – 31/1/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="b00c8-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="b00c8-519">Kontotype</span><span class="sxs-lookup"><span data-stu-id="b00c8-519">Account type</span></span> | <span data-ttu-id="b00c8-520">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-520">Account number</span></span> | <span data-ttu-id="b00c8-521">Lag</span><span class="sxs-lookup"><span data-stu-id="b00c8-521">Layer</span></span>  | <span data-ttu-id="b00c8-522">Kontobeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-522">Account description</span></span>      | <span data-ttu-id="b00c8-523">Debet</span><span class="sxs-lookup"><span data-stu-id="b00c8-523">Debit</span></span>  | <span data-ttu-id="b00c8-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="b00c8-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="b00c8-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-525">Ledger</span></span>       | <span data-ttu-id="b00c8-526">10</span><span class="sxs-lookup"><span data-stu-id="b00c8-526">10</span></span>             | <span data-ttu-id="b00c8-527">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-527">Custom</span></span> | <span data-ttu-id="b00c8-528">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="b00c8-528">Depreciation expense</span></span>     | <span data-ttu-id="b00c8-529">949.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-529">949.75</span></span> |        |
| <span data-ttu-id="b00c8-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="b00c8-530">Ledger</span></span>       | <span data-ttu-id="b00c8-531">11</span><span class="sxs-lookup"><span data-stu-id="b00c8-531">11</span></span>             | <span data-ttu-id="b00c8-532">Brugerdefineret</span><span class="sxs-lookup"><span data-stu-id="b00c8-532">Custom</span></span> | <span data-ttu-id="b00c8-533">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="b00c8-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="b00c8-534">949.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-534">949.75</span></span> |

<span data-ttu-id="b00c8-535">Når alle disse kladdeposteringer er oprettet og bogført, vises følgende værdier for "brugerdefineret lag 1".</span><span class="sxs-lookup"><span data-stu-id="b00c8-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="b00c8-536">Bemærk, at den sidste kolonne indeholder bankgebyret, momsudgiften og reduktionen af kontanter fra det foregående lag, men ikke de lovpligtige rapporteringskladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="b00c8-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="b00c8-537">Derfor opnås ægte Dual Reporting-funktioner.</span><span class="sxs-lookup"><span data-stu-id="b00c8-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="b00c8-538">På dette tidspunkt har firmaet kun brug for sin råbalance, og kombinerer det aktuelle lag og det brugerdefinerede lag for at oprette en IFRS-råbalance.</span><span class="sxs-lookup"><span data-stu-id="b00c8-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="b00c8-539">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="b00c8-539">Account No</span></span> | <span data-ttu-id="b00c8-540">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-540">Description</span></span>              | <span data-ttu-id="b00c8-541">Lovpligtigt kartotek\-Aktuelt lag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-542">Lovpligtigt kartotek\-Aktuelt lag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-543">Lovpligtigt kartotek\-Aktuelt lag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-544">Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="b00c8-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="b00c8-545">Tilbageført kartotek\-Brugerdefineret lag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-546">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-547">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-548">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-549">IFRS 16 kartotek\-Brugerdefineret lag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="b00c8-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="b00c8-550">Brugerdefineret lag \+ Aktuelt lag \- I alt</span><span class="sxs-lookup"><span data-stu-id="b00c8-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="b00c8-551">1</span><span class="sxs-lookup"><span data-stu-id="b00c8-551">1</span></span>          | <span data-ttu-id="b00c8-552">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-552">Lease expense</span></span>            | <span data-ttu-id="b00c8-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="b00c8-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-554">1,000\.00</span></span>               |   | <span data-ttu-id="b00c8-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="b00c8-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="b00c8-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-556">0\.00</span></span>                                   |
| <span data-ttu-id="b00c8-557">2</span><span class="sxs-lookup"><span data-stu-id="b00c8-557">2</span></span>          | <span data-ttu-id="b00c8-558">Bankgebyr</span><span class="sxs-lookup"><span data-stu-id="b00c8-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="b00c8-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="b00c8-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="b00c8-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-561">3\.00</span></span>                                   |
| <span data-ttu-id="b00c8-562">3</span><span class="sxs-lookup"><span data-stu-id="b00c8-562">3</span></span>          | <span data-ttu-id="b00c8-563">Momsudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="b00c8-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="b00c8-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="b00c8-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-566">5\.00</span></span>                                   |
| <span data-ttu-id="b00c8-567">4</span><span class="sxs-lookup"><span data-stu-id="b00c8-567">4</span></span>          | <span data-ttu-id="b00c8-568">Clearingkonto</span><span class="sxs-lookup"><span data-stu-id="b00c8-568">Clearing account</span></span>         | <span data-ttu-id="b00c8-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="b00c8-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="b00c8-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-571">0\.00</span></span>                   |   | <span data-ttu-id="b00c8-572">1.000</span><span class="sxs-lookup"><span data-stu-id="b00c8-572">1,000</span></span>                                           |                                                | <span data-ttu-id="b00c8-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="b00c8-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="b00c8-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-574">0\.00</span></span>                                   |
| <span data-ttu-id="b00c8-575">5</span><span class="sxs-lookup"><span data-stu-id="b00c8-575">5</span></span>          | <span data-ttu-id="b00c8-576">Kreditor</span><span class="sxs-lookup"><span data-stu-id="b00c8-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="b00c8-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="b00c8-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-578">1,008\.00</span></span>                                         | <span data-ttu-id="b00c8-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="b00c8-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-580">0\.00</span></span>                                   |
| <span data-ttu-id="b00c8-581">6</span><span class="sxs-lookup"><span data-stu-id="b00c8-581">6</span></span>          | <span data-ttu-id="b00c8-582">ROU-aktiv</span><span class="sxs-lookup"><span data-stu-id="b00c8-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="b00c8-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="b00c8-584">22,794</span><span class="sxs-lookup"><span data-stu-id="b00c8-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="b00c8-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="b00c8-585">22,793\.90</span></span>                              |
| <span data-ttu-id="b00c8-586">7</span><span class="sxs-lookup"><span data-stu-id="b00c8-586">7</span></span>          | <span data-ttu-id="b00c8-587">Finansiel leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="b00c8-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="b00c8-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="b00c8-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="b00c8-589">\-22,794</span></span>                                       | <span data-ttu-id="b00c8-590">1.000</span><span class="sxs-lookup"><span data-stu-id="b00c8-590">1,000</span></span>                                          | <span data-ttu-id="b00c8-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="b00c8-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="b00c8-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="b00c8-593">8</span><span class="sxs-lookup"><span data-stu-id="b00c8-593">8</span></span>          | <span data-ttu-id="b00c8-594">Renteudgift</span><span class="sxs-lookup"><span data-stu-id="b00c8-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="b00c8-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="b00c8-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="b00c8-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="b00c8-597">94\.97</span></span>                                  |
| <span data-ttu-id="b00c8-598">9</span><span class="sxs-lookup"><span data-stu-id="b00c8-598">9</span></span>          | <span data-ttu-id="b00c8-599">Indløsning</span><span class="sxs-lookup"><span data-stu-id="b00c8-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="b00c8-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="b00c8-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="b00c8-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="b00c8-603">10</span><span class="sxs-lookup"><span data-stu-id="b00c8-603">10</span></span>         | <span data-ttu-id="b00c8-604">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="b00c8-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="b00c8-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="b00c8-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-606">949\.75</span></span>                                        | <span data-ttu-id="b00c8-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-607">949\.75</span></span>                                 |
| <span data-ttu-id="b00c8-608">11</span><span class="sxs-lookup"><span data-stu-id="b00c8-608">11</span></span>         | <span data-ttu-id="b00c8-609">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="b00c8-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="b00c8-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="b00c8-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="b00c8-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-611">\-949\.75</span></span>                                      | <span data-ttu-id="b00c8-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="b00c8-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
