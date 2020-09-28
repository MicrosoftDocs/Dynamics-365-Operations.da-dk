---
title: Råbalance med detaljeret transaktionsrapport
description: I dette emne beskrives standardrapporten til råbalancer. Her beskrives også de komponenter, der er knyttet til denne rapport, og hvordan du kan redigere rapporten, så den passer til virksomhedens behov.
author: v-kiarnd
manager: AnnBe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2019-10-24
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 76b0560499532eb3e97b03a9e797a9168ebcbcdc
ms.sourcegitcommit: d6b17b9bafa84b574a597a560a80e6b7b1852b14
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/12/2020
ms.locfileid: "3799917"
---
# <a name="trial-balance-with-transactional-detail-report"></a><span data-ttu-id="07b8c-104">Råbalance med detaljeret transaktionsrapport</span><span class="sxs-lookup"><span data-stu-id="07b8c-104">Trial balance with transactional detail report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07b8c-105">I dette emne beskrives standardrapporten til råbalancer.</span><span class="sxs-lookup"><span data-stu-id="07b8c-105">This topic describes the default report for trial balances.</span></span> <span data-ttu-id="07b8c-106">Her beskrives også de komponenter, der er knyttet til denne rapport, og hvordan du kan redigere rapporten, så den passer til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="07b8c-106">It also describes the building blocks that are associated with this report and how you can modify the report to fit your business requirements.</span></span>

<span data-ttu-id="07b8c-107">Du kan bruge **Råbalance med detaljeret transaktionsrapport**-rapporten til at få vist detaljer om hver enkelt transaktion for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="07b8c-107">You can use the **Trial balance with transactional detail** report to show the details of each transaction for ledger accounts.</span></span> <span data-ttu-id="07b8c-108">Rapporten indeholder følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="07b8c-108">The report includes the following information:</span></span> 

- <span data-ttu-id="07b8c-109">Startsaldi</span><span class="sxs-lookup"><span data-stu-id="07b8c-109">Opening balances</span></span>
- <span data-ttu-id="07b8c-110">Debet- og kreditbeløb</span><span class="sxs-lookup"><span data-stu-id="07b8c-110">Debits and credits</span></span> 
- <span data-ttu-id="07b8c-111">De resulterende saldi for et datointerval på 31 dage eller derunder</span><span class="sxs-lookup"><span data-stu-id="07b8c-111">The resulting balances for a date range of 31 days or less</span></span>

<span data-ttu-id="07b8c-112">I forbindelse med transaktioner indeholder rapporten følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="07b8c-112">For transactions, the report includes the following information:</span></span> 

- <span data-ttu-id="07b8c-113">Posteringsdato</span><span class="sxs-lookup"><span data-stu-id="07b8c-113">Transaction date</span></span>
- <span data-ttu-id="07b8c-114">Bilagsnummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-114">Voucher number</span></span>
- <span data-ttu-id="07b8c-115">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-115">Account number</span></span>
- <span data-ttu-id="07b8c-116">Dokumentnr.</span><span class="sxs-lookup"><span data-stu-id="07b8c-116">Document number</span></span>
- <span data-ttu-id="07b8c-117">Finansdimension</span><span class="sxs-lookup"><span data-stu-id="07b8c-117">Ledger dimension</span></span>
- <span data-ttu-id="07b8c-118">Finansdimensionsnavn</span><span class="sxs-lookup"><span data-stu-id="07b8c-118">Ledger dimension name</span></span>
- <span data-ttu-id="07b8c-119">Posteringsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="07b8c-119">Transaction description</span></span>
- <span data-ttu-id="07b8c-120">Debet- eller kreditbeløb</span><span class="sxs-lookup"><span data-stu-id="07b8c-120">Debits or credits</span></span>
- <span data-ttu-id="07b8c-121">En løbende saldo for året til dato baseret på det indeværende regnskabsår</span><span class="sxs-lookup"><span data-stu-id="07b8c-121">A running balance for the year to date, based on the current fiscal year</span></span>

<span data-ttu-id="07b8c-122">Du kan bruge råbalance til at identificere fejl i kontosaldi.</span><span class="sxs-lookup"><span data-stu-id="07b8c-122">You can use the trial balance to identify errors for account balances.</span></span> <span data-ttu-id="07b8c-123">Alle konti, der har debetsaldi, skal svare til alle konti, der har kreditsaldi.</span><span class="sxs-lookup"><span data-stu-id="07b8c-123">All accounts that have debit balances should equal all accounts that have credit balances.</span></span> <span data-ttu-id="07b8c-124">Rapporten indeholder oplysninger fra finanskladdens regnskabsposter.</span><span class="sxs-lookup"><span data-stu-id="07b8c-124">The report includes information from the general journal accounting entries.</span></span>

<span data-ttu-id="07b8c-125">Du kan filtrere dataene efter et af følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="07b8c-125">You can filter the data by any of the following items:</span></span>

- <span data-ttu-id="07b8c-126">Bogførte posteringer</span><span class="sxs-lookup"><span data-stu-id="07b8c-126">Posted transactions</span></span>
- <span data-ttu-id="07b8c-127">Ventende transaktioner (disse transaktioner omfatter alle transaktioner, der ikke er bogført).</span><span class="sxs-lookup"><span data-stu-id="07b8c-127">Pending transactions (These transactions include all transactions that aren't posted.)</span></span> 
- <span data-ttu-id="07b8c-128">Alle transaktioner</span><span class="sxs-lookup"><span data-stu-id="07b8c-128">All transactions</span></span> 

<span data-ttu-id="07b8c-129">Hvis transaktionerne omfatter økonomiske dimensioner, vises disse oplysninger under en finanskonto i rapporten.</span><span class="sxs-lookup"><span data-stu-id="07b8c-129">If the transactions include financial dimensions, the report shows that information under a ledger account.</span></span> <span data-ttu-id="07b8c-130">Ellers grupperes oplysningerne for økonomiske dimensioner øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="07b8c-130">Otherwise, information for financial dimensions is grouped at the top of the page.</span></span> 

<span data-ttu-id="07b8c-131">I øjeblikket eksporteres rapporten direkte til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="07b8c-131">Currently, the report is exported directly to Microsoft Excel.</span></span> 

## <a name="transaction-information-on-the-report"></a><span data-ttu-id="07b8c-132">Transaktionsoplysninger i rapporten</span><span class="sxs-lookup"><span data-stu-id="07b8c-132">Transaction information on the report</span></span>

<span data-ttu-id="07b8c-133">Afhængigt af transaktionstypen, f.eks. en avanceret finanspost (ALE) eller en indkøbsordre, vises følgende yderligere oplysninger i rapporten.</span><span class="sxs-lookup"><span data-stu-id="07b8c-133">Depending on the type of transaction, such as an advanced ledger entry (ALE) or purchase order, the following additional information appears on the report.</span></span>

<table> 
<thead>
<tr>
<th><span data-ttu-id="07b8c-134">Konteringstype</span><span class="sxs-lookup"><span data-stu-id="07b8c-134">Transaction type</span></span></th>
<th><span data-ttu-id="07b8c-135">Yderligere dokumentoplysninger</span><span class="sxs-lookup"><span data-stu-id="07b8c-135">Additional document information</span></span></th>
<th><span data-ttu-id="07b8c-136">Yderligere beskrivelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="07b8c-136">Additional description information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<ul>
<li><span data-ttu-id="07b8c-137">ALE-bilag</span><span class="sxs-lookup"><span data-stu-id="07b8c-137">ALE voucher</span></span></li>
<li><span data-ttu-id="07b8c-138">Fordelingsregel</span><span class="sxs-lookup"><span data-stu-id="07b8c-138">Allocation rule</span></span></li>
<li><span data-ttu-id="07b8c-139">Overførsel af finanskladde</span><span class="sxs-lookup"><span data-stu-id="07b8c-139">General journal transfer</span></span></li>
<li><span data-ttu-id="07b8c-140">Kladden</span><span class="sxs-lookup"><span data-stu-id="07b8c-140">Journal</span></span></li>
</ul>
</td>
<td><span data-ttu-id="07b8c-141">ALE-nummer eller finanskladdenummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-141">ALE number or general journal number</span></span></td>
<td><span data-ttu-id="07b8c-142">Beskrivelse af linjeelement</span><span class="sxs-lookup"><span data-stu-id="07b8c-142">Line item description</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-143">Ingen data</span><span class="sxs-lookup"><span data-stu-id="07b8c-143">No data</span></span></td>
<td><span data-ttu-id="07b8c-144">Beskrivelse af overskrift i ALE eller finanskladde</span><span class="sxs-lookup"><span data-stu-id="07b8c-144">ALE or general journal header description</span></span></td>
</tr>
<tr>
<td>
<ul>
<li><span data-ttu-id="07b8c-145">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="07b8c-145">Invoice voucher</span></span></li>
<li><span data-ttu-id="07b8c-146">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="07b8c-146">Credit note voucher</span></span></li>
</ul>
</td>
<td><span data-ttu-id="07b8c-147">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-147">Invoice number</span></span></td>
<td><span data-ttu-id="07b8c-148">Kreditornummer og kreditornavn</span><span class="sxs-lookup"><span data-stu-id="07b8c-148">Vendor number and Vendor name</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-149">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="07b8c-149">Invoice date</span></span></td>
<td><span data-ttu-id="07b8c-150">Beskrivelse af linjeelement</span><span class="sxs-lookup"><span data-stu-id="07b8c-150">Line item description</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-151">Ingen data</span><span class="sxs-lookup"><span data-stu-id="07b8c-151">No data</span></span></td>
<td><span data-ttu-id="07b8c-152">Indkøbsordrenummer og/eller PA-nummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-152">Purchase order number and/or PA number</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07b8c-153">Betalingsbilag for kreditor</span><span class="sxs-lookup"><span data-stu-id="07b8c-153">Accounts payable (AP) payment voucher</span></span></td>
<td><span data-ttu-id="07b8c-154">Checknummer eller nummer på elektronisk pengeoverførsel</span><span class="sxs-lookup"><span data-stu-id="07b8c-154">Check number or electronic funds transfer (EFT) number</span></span></td>
<td><span data-ttu-id="07b8c-155">Kreditornummer – kreditornavn for "skal betales" eller faktureringskonto</span><span class="sxs-lookup"><span data-stu-id="07b8c-155">Vendor number – Vendor name for the "pay to" or invoice account</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-156">Checkdato, elektronisk pengeoverførselsdato eller udligningsdato</span><span class="sxs-lookup"><span data-stu-id="07b8c-156">Check date, EFT date, or settlement date</span></span></td>
<td><span data-ttu-id="07b8c-157">Kreditornummer og kreditornavn for den oprindelige ordrekonto</span><span class="sxs-lookup"><span data-stu-id="07b8c-157">Vendor number and Vendor name for the original order account</span></span></td>
</tr>
<tr>
<td>
<ul>
<li><span data-ttu-id="07b8c-158">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="07b8c-158">Free text credit note</span></span></li>
<li><span data-ttu-id="07b8c-159">Fritekstfakturabilag</span><span class="sxs-lookup"><span data-stu-id="07b8c-159">Free text invoice voucher</span></span></li>
</ul>
</td>
<td><span data-ttu-id="07b8c-160">Nummer på fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="07b8c-160">Free text invoice number</span></span></td>
<td><span data-ttu-id="07b8c-161">Kundenummer og kundenavn</span><span class="sxs-lookup"><span data-stu-id="07b8c-161">Customer number and Customer name</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-162">Faktureringskode</span><span class="sxs-lookup"><span data-stu-id="07b8c-162">Billing code</span></span></td>
<td><span data-ttu-id="07b8c-163">Beskrivelse af linjeelement i fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="07b8c-163">Free text invoice line item description</span></span><br>
<span data-ttu-id="07b8c-164">(Feltet <strong>Beskrivelse</strong> i oversigtspanelet <strong>Fakturalinjer</strong> på siden <strong>Fritekstfakturaer</strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-164">(<strong>Description</strong> field on the <strong>Invoice lines</strong> FastTab of the <strong>Free text invoices</strong> page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07b8c-165">Betalingsbilag for debitor (AR)</span><span class="sxs-lookup"><span data-stu-id="07b8c-165">Accounts receivable (AR) payment voucher</span></span></td>
<td><span data-ttu-id="07b8c-166">Kladdebatchnummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-166">Journal batch number</span></span><br>
<span data-ttu-id="07b8c-167">(Feltet <strong>Kladdebatchnummer</strong> under fanen <strong>Oversigt</strong> på siden <strong>Betalingskladde</strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-167">(<strong>Journal batch number</strong> field on the <strong>Overview</strong> tab of the <strong>Payment journal</strong> page)</span></span></td>
<td><span data-ttu-id="07b8c-168">Kundenummer – kundenavn</span><span class="sxs-lookup"><span data-stu-id="07b8c-168">Customer number – Customer name</span></span><br>
<span data-ttu-id="07b8c-169">(Felterne <strong>Konto</strong> og <strong>Kontonavn</strong> under fanen <strong>Oversigt</strong> på siden <strong>Kladdebilag</strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-169">(<strong>Account</strong> and <strong>Account name</strong> fields on the <strong>Overview</strong> tab of the <strong>Journal voucher</strong> page)</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-170">Betalingsreference</span><span class="sxs-lookup"><span data-stu-id="07b8c-170">Payment reference</span></span></td>
<td><span data-ttu-id="07b8c-171">Betegnelse for linjen.</span><span class="sxs-lookup"><span data-stu-id="07b8c-171">Line description</span></span><br>
<span data-ttu-id="07b8c-172">(Feltet <strong>Beskrivelse</strong> under fanen <strong>Oversigt</strong> på siden <strong>Kladdebilag</strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-172">(<strong>Description</strong> field on the <strong>Overview</strong> tab of the <strong>Journal voucher</strong> page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07b8c-173">Budgetposteringer</span><span class="sxs-lookup"><span data-stu-id="07b8c-173">Budget register entries</span></span></td>
<td><span data-ttu-id="07b8c-174">Budgetregisterpostens nummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-174">Budget register entry number</span></span></td>
<td><span data-ttu-id="07b8c-175">Beskrivelse af budgetregisterpost</span><span class="sxs-lookup"><span data-stu-id="07b8c-175">Budget register entry description</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-176">Budgetkode</span><span class="sxs-lookup"><span data-stu-id="07b8c-176">Budget code</span></span></td>
<td><span data-ttu-id="07b8c-177">Årsagskode – Beskrivelse af overskrift for budgetregisterpost</span><span class="sxs-lookup"><span data-stu-id="07b8c-177">Reason code – Budget register entry header description</span></span><br>
<span data-ttu-id="07b8c-178">(Feltet <strong>Kommentar</strong> i oversigtspanelet <strong>Oplysninger om budgetkontoposter</strong> på siden <strong>Budgetpost</strong> eller <strong>Budgetregisterpost </strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-178">(<strong>Comment</strong> field on the <strong>Budget account entry details</strong> FastTab on the <strong>Budget entry</strong> page or the <strong>Budget register entry</strong> page)</span></span></td>
</tr>
<tr>
<td>
<ul>
<li><span data-ttu-id="07b8c-179">Indkøbsordrebekræftelse</span><span class="sxs-lookup"><span data-stu-id="07b8c-179">Purchase order confirmation</span></span></li>
<li><span data-ttu-id="07b8c-180">Bekræftelsesbilag på indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="07b8c-180">Purchase order confirmation voucher</span></span></li>
</ul>
</td>
<td><span data-ttu-id="07b8c-181">Indkøbsordrenummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-181">Purchase order number</span></span></td>
<td><span data-ttu-id="07b8c-182">Beskrivelse af linjeelement</span><span class="sxs-lookup"><span data-stu-id="07b8c-182">Line item description</span></span><br>
<span data-ttu-id="07b8c-183">(Feltet <strong>Tekst</strong> i oversigtspanelet <strong>Linjedetaljer</strong> på siden <strong>Indkøbsordre</strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-183">(<strong>Text</strong> field on the <strong>Line details</strong> FastTab of the <strong>Purchase order</strong> page)</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-184">Nummer på indkøbsordrelinje</span><span class="sxs-lookup"><span data-stu-id="07b8c-184">Purchase order line number</span></span></td>
<td><span data-ttu-id="07b8c-185">Indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="07b8c-185">Procurement category</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07b8c-186">Indkøbsrekvisitionsbilag</span><span class="sxs-lookup"><span data-stu-id="07b8c-186">Purchase requisition voucher</span></span></td>
<td><span data-ttu-id="07b8c-187">Indkøbsrekvisitionsnummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-187">Purchase requisition number</span></span></td>
<td><span data-ttu-id="07b8c-188">Navn på indkøbsrekvisition</span><span class="sxs-lookup"><span data-stu-id="07b8c-188">Purchase requisition name</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-189">Indkøbsrekvisitionslinjenummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-189">Purchase requisition line number</span></span></td>
<td><span data-ttu-id="07b8c-190">Beskrivelse af indkøbsrekvisitionslinje</span><span class="sxs-lookup"><span data-stu-id="07b8c-190">Purchase requisition line description</span></span><br>
<span data-ttu-id="07b8c-191">(Feltet <strong>Produktnavn</strong> i oversigtspanelet <strong>Indkøbsrekvisitionslinjer</strong> på siden <strong>Indkøbsrekvisition</strong>)</span><span class="sxs-lookup"><span data-stu-id="07b8c-191">(<strong>Product name</strong> field on the <strong>Purchase requisition lines</strong> FastTab of the <strong>Purchase requisition</strong> page)</span></span></td>
</tr>
<tr>
<td>
<ul>
<li><span data-ttu-id="07b8c-192">Projektfakturabilag</span><span class="sxs-lookup"><span data-stu-id="07b8c-192">Project invoice voucher</span></span></li>
<li><span data-ttu-id="07b8c-193">Projektfaktura</span><span class="sxs-lookup"><span data-stu-id="07b8c-193">Project invoice</span></span></li>
</ul>
</td>
<td><span data-ttu-id="07b8c-194">Projektfakturanummer</span><span class="sxs-lookup"><span data-stu-id="07b8c-194">Project invoice number</span></span></td>
<td><span data-ttu-id="07b8c-195">Fakturakonto og kontonavn</span><span class="sxs-lookup"><span data-stu-id="07b8c-195">Invoice account and Account name</span></span></td>
</tr>
<tr>
<td></td>
<td><span data-ttu-id="07b8c-196">Finansieringskilde</span><span class="sxs-lookup"><span data-stu-id="07b8c-196">Funding source</span></span></td>
<td><span data-ttu-id="07b8c-197">Projekt-id og projektnavn</span><span class="sxs-lookup"><span data-stu-id="07b8c-197">Project ID and Project name</span></span></td>
</tr>
</tbody>
</table>
