---
title: Råbalance - økonomiske rapporter
description: I denne artikel beskrives standardrapporterne til råbalancer. Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd4512b02070415b6228c91b66635815dbacaa2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175341"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="e0ccb-104">Råbalance - økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="e0ccb-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0ccb-105">I denne artikel beskrives standardrapporterne til råbalancer.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="e0ccb-106">Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="e0ccb-107">Standardråbalancerapporter</span><span class="sxs-lookup"><span data-stu-id="e0ccb-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="e0ccb-108">Tre råbalancerapporter er tilgængelige i Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="e0ccb-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="e0ccb-109">Default report</span></span>                                 | <span data-ttu-id="e0ccb-110">Hvad den gør</span><span class="sxs-lookup"><span data-stu-id="e0ccb-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ccb-111">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="e0ccb-112">Leverer oplysninger om saldoen for alle konti og medtager har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="e0ccb-113">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="e0ccb-114">Leverer saldooplysninger for alle konti, og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="e0ccb-115">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="e0ccb-116">Leverer saldooplysninger for alle konti og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="e0ccb-117">Komponenter</span><span class="sxs-lookup"><span data-stu-id="e0ccb-117">Building blocks</span></span>
<span data-ttu-id="e0ccb-118">Råbalance regnskabsrapporter bruger følgende komponenter.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="e0ccb-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="e0ccb-119">Default report</span></span>                                 | <span data-ttu-id="e0ccb-120">Definition af række</span><span class="sxs-lookup"><span data-stu-id="e0ccb-120">Row definition</span></span>          | <span data-ttu-id="e0ccb-121">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="e0ccb-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="e0ccb-122">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="e0ccb-123">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-123">Trial Balance - Default</span></span> | <span data-ttu-id="e0ccb-124">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="e0ccb-125">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="e0ccb-126">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-126">Trial Balance - Default</span></span> | <span data-ttu-id="e0ccb-127">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="e0ccb-128">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="e0ccb-129">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-129">Trial Balance - Default</span></span> | <span data-ttu-id="e0ccb-130">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="e0ccb-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="e0ccb-131">Definition af række</span><span class="sxs-lookup"><span data-stu-id="e0ccb-131">Row definition</span></span>

<span data-ttu-id="e0ccb-132">Rækkedefinitionen, råbalance – standard, indeholder en enkelt række, der henter alle hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="e0ccb-133">Derfor kan alle oprette rapporten uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="e0ccb-134">Når du får vist rapporten, dykker du ind i den enkelte række for at se detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="e0ccb-135">Du kan ændre rækkedefinitionen, så den omfatter flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="e0ccb-136">Følg disse trin for at ændre den råbalancen– standardrækkedefinitionen, så den indeholder rækker for alle konti.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="e0ccb-137">Klik på **Rediger**, og klik derefter på **Indsæt rækker fra dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="e0ccb-138">Med kommandoen **Indsæt rækker fra dimensioner** kan du vælge de dimensioner, du vil have i din rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="e0ccb-139">For denne rækkedefinition skal du bruge **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="e0ccb-140">Sørg for, at **Hovedkonto** indeholder og-tegn (&), og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="e0ccb-141">Rækkedefinitionen indeholder nu alle hovedkonti for den juridiske enhed, der er standard.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="e0ccb-142">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="e0ccb-142">Column definition</span></span>

<span data-ttu-id="e0ccb-143">Hver råbalancerapport bruger en anden kolonnedefinition.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="e0ccb-144">Disse kolonnedefinitioner indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="e0ccb-145">**Detaljeret råbalance – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="e0ccb-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="e0ccb-146">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e0ccb-147">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="e0ccb-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="e0ccb-148">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="e0ccb-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="e0ccb-149">Posteringsdato</span><span class="sxs-lookup"><span data-stu-id="e0ccb-149">Transaction Date</span></span>
        -   <span data-ttu-id="e0ccb-150">Bilag</span><span class="sxs-lookup"><span data-stu-id="e0ccb-150">Voucher</span></span>
        -   <span data-ttu-id="e0ccb-151">Beskrivelse af kladde</span><span class="sxs-lookup"><span data-stu-id="e0ccb-151">Journal Description</span></span>
    -   <span data-ttu-id="e0ccb-152">**FD** – økonomiske data, der kun indeholder debiteringer</span><span class="sxs-lookup"><span data-stu-id="e0ccb-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="e0ccb-153">**FD** – økonomiske data, der kun indeholder krediteringer</span><span class="sxs-lookup"><span data-stu-id="e0ccb-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="e0ccb-154">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="e0ccb-155">**Opsummeret råbalance – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="e0ccb-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="e0ccb-156">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="e0ccb-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="e0ccb-157">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e0ccb-158">**ATTR** – En attribut:</span><span class="sxs-lookup"><span data-stu-id="e0ccb-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="e0ccb-159">Bilag</span><span class="sxs-lookup"><span data-stu-id="e0ccb-159">Voucher</span></span>
    -   <span data-ttu-id="e0ccb-160">**FD** – primosaldo - økonomiske data</span><span class="sxs-lookup"><span data-stu-id="e0ccb-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="e0ccb-161">**FD** – Økonomiske data, der kun indeholder debiteringer</span><span class="sxs-lookup"><span data-stu-id="e0ccb-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="e0ccb-162">**FD** – økonomiske data, der kun indeholder krediteringer</span><span class="sxs-lookup"><span data-stu-id="e0ccb-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="e0ccb-163">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="e0ccb-164">**CALC** – Ultimosaldoen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="e0ccb-165">**Årlig råbalanceoversigt – standard:**</span><span class="sxs-lookup"><span data-stu-id="e0ccb-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="e0ccb-166">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="e0ccb-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="e0ccb-167">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e0ccb-168">**ATTR** – En attribut</span><span class="sxs-lookup"><span data-stu-id="e0ccb-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="e0ccb-169">Bilag</span><span class="sxs-lookup"><span data-stu-id="e0ccb-169">Voucher</span></span>
    -   <span data-ttu-id="e0ccb-170">**FD** – Primosaldoen for økonomiske data for indeværende år</span><span class="sxs-lookup"><span data-stu-id="e0ccb-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="e0ccb-171">**FD** – Økonomiske data, der kun indeholder debiteringer for det indeværende år</span><span class="sxs-lookup"><span data-stu-id="e0ccb-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="e0ccb-172">**FD** – Økonomiske data, der kun indeholder krediteringer for det indeværende år</span><span class="sxs-lookup"><span data-stu-id="e0ccb-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="e0ccb-173">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="e0ccb-174">**CALC** – Ultimosaldoen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="e0ccb-175">**FD** – Økonomiske data, der kun indeholder debiteringer for sidste år</span><span class="sxs-lookup"><span data-stu-id="e0ccb-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="e0ccb-176">**FD** – Økonomiske data, der kun indeholder krediteringer for sidste år</span><span class="sxs-lookup"><span data-stu-id="e0ccb-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="e0ccb-177">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e0ccb-177">Additional resources</span></span>
--------

[<span data-ttu-id="e0ccb-178">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="e0ccb-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="e0ccb-179">Se økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="e0ccb-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="e0ccb-180">Dynamics Financial Reporting-blog</span><span class="sxs-lookup"><span data-stu-id="e0ccb-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



