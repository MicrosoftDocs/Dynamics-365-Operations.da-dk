---
title: Råbalance - økonomiske rapporter
description: I denne artikel beskrives standardrapporterne til råbalancer. Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103652"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="f523e-104">Råbalance - økonomiske rapporter</span><span class="sxs-lookup"><span data-stu-id="f523e-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f523e-105">I denne artikel beskrives standardrapporterne til råbalancer.</span><span class="sxs-lookup"><span data-stu-id="f523e-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="f523e-106">Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="f523e-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="f523e-107">Standardråbalancerapporter</span><span class="sxs-lookup"><span data-stu-id="f523e-107">Default trial balance reports</span></span>

<span data-ttu-id="f523e-108">Tre råbalancerapporter er tilgængelige i Økonomirapportering.</span><span class="sxs-lookup"><span data-stu-id="f523e-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="f523e-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="f523e-109">Default report</span></span>                                 | <span data-ttu-id="f523e-110">Hvad den gør</span><span class="sxs-lookup"><span data-stu-id="f523e-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f523e-111">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="f523e-112">Leverer oplysninger om saldoen for alle konti og medtager har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.</span><span class="sxs-lookup"><span data-stu-id="f523e-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="f523e-113">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="f523e-114">Leverer saldooplysninger for alle konti, og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.</span><span class="sxs-lookup"><span data-stu-id="f523e-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="f523e-115">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="f523e-116">Leverer saldooplysninger for alle konti og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år.</span><span class="sxs-lookup"><span data-stu-id="f523e-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="f523e-117">Komponenter</span><span class="sxs-lookup"><span data-stu-id="f523e-117">Building blocks</span></span>
<span data-ttu-id="f523e-118">Råbalance regnskabsrapporter bruger følgende komponenter.</span><span class="sxs-lookup"><span data-stu-id="f523e-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="f523e-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="f523e-119">Default report</span></span>                                 | <span data-ttu-id="f523e-120">Definition af række</span><span class="sxs-lookup"><span data-stu-id="f523e-120">Row definition</span></span>          | <span data-ttu-id="f523e-121">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="f523e-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="f523e-122">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="f523e-123">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-123">Trial Balance - Default</span></span> | <span data-ttu-id="f523e-124">Detaljeret råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="f523e-125">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="f523e-126">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-126">Trial Balance - Default</span></span> | <span data-ttu-id="f523e-127">Råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="f523e-128">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="f523e-129">Råbalance – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-129">Trial Balance - Default</span></span> | <span data-ttu-id="f523e-130">Årlig råbalanceoversigt – standard</span><span class="sxs-lookup"><span data-stu-id="f523e-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="f523e-131">Når du kører rapporten **Råbalance** i Financial Reporting, skal du sørge for at markere afkrydsningsfelterne for **Vis rækker uden beløb** og **Vis rapporter uden aktive rækker** under fanen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f523e-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="f523e-132">Definition af række</span><span class="sxs-lookup"><span data-stu-id="f523e-132">Row definition</span></span>

<span data-ttu-id="f523e-133">Rækkedefinitionen, råbalance – standard, indeholder en enkelt række, der henter alle hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="f523e-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="f523e-134">Derfor kan alle oprette rapporten uden at skulle foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="f523e-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="f523e-135">Når du får vist rapporten, dykker du ind i den enkelte række for at se detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="f523e-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="f523e-136">Du kan ændre rækkedefinitionen, så den omfatter flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="f523e-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="f523e-137">Følg disse trin for at ændre den råbalancen– standardrækkedefinitionen, så den indeholder rækker for alle konti.</span><span class="sxs-lookup"><span data-stu-id="f523e-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="f523e-138">Klik på **Rediger**, og klik derefter på **Indsæt rækker fra dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="f523e-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="f523e-139">Med kommandoen **Indsæt rækker fra dimensioner** kan du vælge de dimensioner, du vil have i din rækkedefinition.</span><span class="sxs-lookup"><span data-stu-id="f523e-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="f523e-140">For denne rækkedefinition skal du bruge **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="f523e-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="f523e-141">Sørg for, at **Hovedkonto** indeholder og-tegn (&), og klik derefter på **OK**.</span><span class="sxs-lookup"><span data-stu-id="f523e-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="f523e-142">Rækkedefinitionen indeholder nu alle hovedkonti for den juridiske enhed, der er standard.</span><span class="sxs-lookup"><span data-stu-id="f523e-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="f523e-143">Kolonnedefinition</span><span class="sxs-lookup"><span data-stu-id="f523e-143">Column definition</span></span>

<span data-ttu-id="f523e-144">Hver råbalancerapport bruger en anden kolonnedefinition.</span><span class="sxs-lookup"><span data-stu-id="f523e-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="f523e-145">Disse kolonnedefinitioner indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="f523e-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="f523e-146">**Detaljeret råbalance – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="f523e-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="f523e-147">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="f523e-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f523e-148">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="f523e-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f523e-149">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="f523e-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="f523e-150">Posteringsdato</span><span class="sxs-lookup"><span data-stu-id="f523e-150">Transaction Date</span></span>
        -   <span data-ttu-id="f523e-151">Bilag</span><span class="sxs-lookup"><span data-stu-id="f523e-151">Voucher</span></span>
        -   <span data-ttu-id="f523e-152">Beskrivelse af kladde</span><span class="sxs-lookup"><span data-stu-id="f523e-152">Journal Description</span></span>
    -   <span data-ttu-id="f523e-153">**FD** – økonomiske data, der kun indeholder debiteringer</span><span class="sxs-lookup"><span data-stu-id="f523e-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="f523e-154">**FD** – økonomiske data, der kun indeholder krediteringer</span><span class="sxs-lookup"><span data-stu-id="f523e-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="f523e-155">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="f523e-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="f523e-156">**Opsummeret råbalance – standardkolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="f523e-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="f523e-157">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="f523e-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f523e-158">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="f523e-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f523e-159">**ATTR** – En attribut:</span><span class="sxs-lookup"><span data-stu-id="f523e-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="f523e-160">Bilag</span><span class="sxs-lookup"><span data-stu-id="f523e-160">Voucher</span></span>
    -   <span data-ttu-id="f523e-161">**FD** – primosaldo - økonomiske data</span><span class="sxs-lookup"><span data-stu-id="f523e-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="f523e-162">**FD** – Økonomiske data, der kun indeholder debiteringer</span><span class="sxs-lookup"><span data-stu-id="f523e-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="f523e-163">**FD** – økonomiske data, der kun indeholder krediteringer</span><span class="sxs-lookup"><span data-stu-id="f523e-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="f523e-164">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="f523e-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="f523e-165">**CALC** – Ultimosaldoen</span><span class="sxs-lookup"><span data-stu-id="f523e-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="f523e-166">**Årlig råbalanceoversigt – standard:**</span><span class="sxs-lookup"><span data-stu-id="f523e-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="f523e-167">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="f523e-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f523e-168">**DESC** – En beskrivelse af rækkedefinitionen</span><span class="sxs-lookup"><span data-stu-id="f523e-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f523e-169">**ATTR** – En attribut</span><span class="sxs-lookup"><span data-stu-id="f523e-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="f523e-170">Bilag</span><span class="sxs-lookup"><span data-stu-id="f523e-170">Voucher</span></span>
    -   <span data-ttu-id="f523e-171">**FD** – Primosaldoen for økonomiske data for indeværende år</span><span class="sxs-lookup"><span data-stu-id="f523e-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="f523e-172">**FD** – Økonomiske data, der kun indeholder debiteringer for det indeværende år</span><span class="sxs-lookup"><span data-stu-id="f523e-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="f523e-173">**FD** – Økonomiske data, der kun indeholder krediteringer for det indeværende år</span><span class="sxs-lookup"><span data-stu-id="f523e-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="f523e-174">**CALC** – Nettodifferencen</span><span class="sxs-lookup"><span data-stu-id="f523e-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="f523e-175">**CALC** – Ultimosaldoen</span><span class="sxs-lookup"><span data-stu-id="f523e-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="f523e-176">**FD** – Økonomiske data, der kun indeholder debiteringer for sidste år</span><span class="sxs-lookup"><span data-stu-id="f523e-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="f523e-177">**FD** – Økonomiske data, der kun indeholder krediteringer for sidste år</span><span class="sxs-lookup"><span data-stu-id="f523e-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f523e-178">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f523e-178">Additional resources</span></span>

[<span data-ttu-id="f523e-179">Oversigt over økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="f523e-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="f523e-180">Vise økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="f523e-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="f523e-181">Dynamics Financial Reporting-blog</span><span class="sxs-lookup"><span data-stu-id="f523e-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
