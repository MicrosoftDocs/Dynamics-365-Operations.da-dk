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
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d753b99b126bf8097e8270f4774db854fa2d279
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240634"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="fb70f-104">Råbalance - økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="fb70f-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb70f-105">I denne artikel beskrives standardrapporterne til råbalancer.</span><span class="sxs-lookup"><span data-stu-id="fb70f-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="fb70f-106">Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="fb70f-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="fb70f-107">Standardråbalancerapporter</span><span class="sxs-lookup"><span data-stu-id="fb70f-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="fb70f-108">Tre råbalancerapporter er tilgængelige i Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="fb70f-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="fb70f-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="fb70f-109">Default report</span></span>                                 | <span data-ttu-id="fb70f-110">Hvad den gør</span><span class="sxs-lookup"><span data-stu-id="fb70f-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb70f-111">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="fb70f-112">Leverer oplysninger om saldoen for alle konti og medtager har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.</span><span class="sxs-lookup"><span data-stu-id="fb70f-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="fb70f-113">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="fb70f-114">Leverer saldooplysninger for alle konti, og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.</span><span class="sxs-lookup"><span data-stu-id="fb70f-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="fb70f-115">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="fb70f-116">Leverer saldooplysninger for alle konti og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år.</span><span class="sxs-lookup"><span data-stu-id="fb70f-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="fb70f-117">Komponenter</span><span class="sxs-lookup"><span data-stu-id="fb70f-117">Building blocks</span></span>
<span data-ttu-id="fb70f-118">Råbalance regnskabsrapporter bruger følgende komponenter.</span><span class="sxs-lookup"><span data-stu-id="fb70f-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="fb70f-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="fb70f-119">Default report</span></span>                                 | <span data-ttu-id="fb70f-120">Definition af række</span><span class="sxs-lookup"><span data-stu-id="fb70f-120">Row definition</span></span>          | <span data-ttu-id="fb70f-121">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="fb70f-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="fb70f-122">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="fb70f-123">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-123">Trial Balance - Default</span></span> | <span data-ttu-id="fb70f-124">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="fb70f-125">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="fb70f-126">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-126">Trial Balance - Default</span></span> | <span data-ttu-id="fb70f-127">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="fb70f-128">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="fb70f-129">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-129">Trial Balance - Default</span></span> | <span data-ttu-id="fb70f-130">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="fb70f-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="fb70f-131">Definition af række</span><span class="sxs-lookup"><span data-stu-id="fb70f-131">Row definition</span></span>

<span data-ttu-id="fb70f-132">Rækkedefinitionen, råbalance – standard, indeholder en enkelt række, der henter alle hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="fb70f-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="fb70f-133">Derfor kan alle oprette rapporten uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="fb70f-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="fb70f-134">Når du får vist rapporten, dykker du ind i den enkelte række for at se detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="fb70f-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="fb70f-135">Du kan ændre rækkedefinitionen, så den omfatter flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="fb70f-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="fb70f-136">Følg disse trin for at ændre den råbalancen– standardrækkedefinitionen, så den indeholder rækker for alle konti.</span><span class="sxs-lookup"><span data-stu-id="fb70f-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="fb70f-137">Klik på **Rediger**, og klik derefter på **Indsæt rækker fra dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="fb70f-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="fb70f-138">Med kommandoen **Indsæt rækker fra dimensioner** kan du vælge de dimensioner, du vil have i din rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="fb70f-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="fb70f-139">For denne rækkedefinition skal du bruge **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="fb70f-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="fb70f-140">Sørg for, at **Hovedkonto** indeholder og-tegn (&), og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb70f-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="fb70f-141">Rækkedefinitionen indeholder nu alle hovedkonti for den juridiske enhed, der er standard.</span><span class="sxs-lookup"><span data-stu-id="fb70f-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="fb70f-142">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="fb70f-142">Column definition</span></span>

<span data-ttu-id="fb70f-143">Hver råbalancerapport bruger en anden kolonnedefinition.</span><span class="sxs-lookup"><span data-stu-id="fb70f-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="fb70f-144">Disse kolonnedefinitioner indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="fb70f-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="fb70f-145">**Detaljeret råbalance – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="fb70f-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="fb70f-146">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="fb70f-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="fb70f-147">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="fb70f-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="fb70f-148">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="fb70f-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="fb70f-149">Posteringsdato</span><span class="sxs-lookup"><span data-stu-id="fb70f-149">Transaction Date</span></span>
        -   <span data-ttu-id="fb70f-150">Bilag</span><span class="sxs-lookup"><span data-stu-id="fb70f-150">Voucher</span></span>
        -   <span data-ttu-id="fb70f-151">Beskrivelse af kladde</span><span class="sxs-lookup"><span data-stu-id="fb70f-151">Journal Description</span></span>
    -   <span data-ttu-id="fb70f-152">**FD** – økonomiske data, der kun indeholder debiteringer</span><span class="sxs-lookup"><span data-stu-id="fb70f-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="fb70f-153">**FD** – økonomiske data, der kun indeholder krediteringer</span><span class="sxs-lookup"><span data-stu-id="fb70f-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="fb70f-154">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="fb70f-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="fb70f-155">**Opsummeret råbalance – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="fb70f-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="fb70f-156">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="fb70f-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="fb70f-157">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="fb70f-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="fb70f-158">**ATTR** – En attribut:</span><span class="sxs-lookup"><span data-stu-id="fb70f-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="fb70f-159">Bilag</span><span class="sxs-lookup"><span data-stu-id="fb70f-159">Voucher</span></span>
    -   <span data-ttu-id="fb70f-160">**FD** – primosaldo - økonomiske data</span><span class="sxs-lookup"><span data-stu-id="fb70f-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="fb70f-161">**FD** – Økonomiske data, der kun indeholder debiteringer</span><span class="sxs-lookup"><span data-stu-id="fb70f-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="fb70f-162">**FD** – økonomiske data, der kun indeholder krediteringer</span><span class="sxs-lookup"><span data-stu-id="fb70f-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="fb70f-163">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="fb70f-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="fb70f-164">**CALC** – Ultimosaldoen</span><span class="sxs-lookup"><span data-stu-id="fb70f-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="fb70f-165">**Årlig råbalanceoversigt – standard:**</span><span class="sxs-lookup"><span data-stu-id="fb70f-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="fb70f-166">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="fb70f-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="fb70f-167">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="fb70f-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="fb70f-168">**ATTR** – En attribut</span><span class="sxs-lookup"><span data-stu-id="fb70f-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="fb70f-169">Bilag</span><span class="sxs-lookup"><span data-stu-id="fb70f-169">Voucher</span></span>
    -   <span data-ttu-id="fb70f-170">**FD** – Primosaldoen for økonomiske data for indeværende år</span><span class="sxs-lookup"><span data-stu-id="fb70f-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="fb70f-171">**FD** – Økonomiske data, der kun indeholder debiteringer for det indeværende år</span><span class="sxs-lookup"><span data-stu-id="fb70f-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="fb70f-172">**FD** – Økonomiske data, der kun indeholder krediteringer for det indeværende år</span><span class="sxs-lookup"><span data-stu-id="fb70f-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="fb70f-173">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="fb70f-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="fb70f-174">**CALC** – Ultimosaldoen</span><span class="sxs-lookup"><span data-stu-id="fb70f-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="fb70f-175">**FD** – Økonomiske data, der kun indeholder debiteringer for sidste år</span><span class="sxs-lookup"><span data-stu-id="fb70f-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="fb70f-176">**FD** – Økonomiske data, der kun indeholder krediteringer for sidste år</span><span class="sxs-lookup"><span data-stu-id="fb70f-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="fb70f-177">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fb70f-177">Additional resources</span></span>
--------

[<span data-ttu-id="fb70f-178">Oversigt over økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="fb70f-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="fb70f-179">Vise økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="fb70f-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="fb70f-180">Dynamics Financial Reporting-blog</span><span class="sxs-lookup"><span data-stu-id="fb70f-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]