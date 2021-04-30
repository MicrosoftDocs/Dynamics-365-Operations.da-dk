---
title: Leasingbogføringstyper
description: I dette emne beskrives de bogføringstyper, der bruges til aktivleasingtransaktioner.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881126"
---
# <a name="lease-posting-types"></a><span data-ttu-id="43f6e-103">Leasingbogføringstyper</span><span class="sxs-lookup"><span data-stu-id="43f6e-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43f6e-104">I dette emne beskrives de bogføringstyper, der bruges til aktivleasingtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="43f6e-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="43f6e-105">Leasingaktiv</span><span class="sxs-lookup"><span data-stu-id="43f6e-105">Lease asset</span></span>

<span data-ttu-id="43f6e-106">Kontoen er knyttet til ROU-forbrugsretaktivet.</span><span class="sxs-lookup"><span data-stu-id="43f6e-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="43f6e-107">Denne konto debiteres, når en leasingaftale oprindeligt genkendes i henhold til de nye regnskabsstandarder for leasingaftaler, Codification Emne 842 (ASC 842) og International Financial Reporting standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="43f6e-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="43f6e-108">I forbindelse med en ændret leasingaftale kan denne konto enten blive debiteret eller krediteret, afhængigt af om ændringen øger eller reducerer leasingforpligtelsen.</span><span class="sxs-lookup"><span data-stu-id="43f6e-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="43f6e-109">**Eksempler på kladdeposter:** Oprindelig genkendelse</span><span class="sxs-lookup"><span data-stu-id="43f6e-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="43f6e-110">**Debet:** Leasingaktiv xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="43f6e-111">**Kredit:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="43f6e-112">Leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="43f6e-112">Lease liability</span></span>

<span data-ttu-id="43f6e-113">Kontoen er knyttet til den leasginforpligtelse, der forekommer, når betalinger diskonteres i henhold til de nye IFRS 16- og ASC 842-standarder.</span><span class="sxs-lookup"><span data-stu-id="43f6e-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="43f6e-114">Denne konto krediteres, når en leasingaftale i begyndelsen anerkendes under de nye standarder.</span><span class="sxs-lookup"><span data-stu-id="43f6e-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="43f6e-115">Den debiteres for leasingbetalinger og krediteres for renteperiodiseringer.</span><span class="sxs-lookup"><span data-stu-id="43f6e-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="43f6e-116">**Eksempler på kladdeposter:** Oprindelig genkendelse</span><span class="sxs-lookup"><span data-stu-id="43f6e-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="43f6e-117">**Debet:** Leasingaktiv xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="43f6e-118">**Kredit:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="43f6e-119">**Eksempel kladdeposter:** Renteperiodisering</span><span class="sxs-lookup"><span data-stu-id="43f6e-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="43f6e-120">**Debet:** Renteudgift xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="43f6e-121">**Kredit:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="43f6e-122">**Eksempel på kladdeposter:** Leasingbetaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="43f6e-123">**Debet:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-124">**Kredit:** Kreditor-/leasingbetaling xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="43f6e-125">Kortfristet leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="43f6e-125">Short-term lease liability</span></span>

<span data-ttu-id="43f6e-126">Kontoen er tilknyttet den kortfristede leasingforpligtelse, når den kortfristede leasingforpligtelse bogføres som kladdepostering.</span><span class="sxs-lookup"><span data-stu-id="43f6e-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="43f6e-127">Denne konto krediteres på kortsigtede passiver fra amortiseringsplanen på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="43f6e-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="43f6e-128">Det samme beløb debiteres dog den første dag i den næste måned.</span><span class="sxs-lookup"><span data-stu-id="43f6e-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="43f6e-129">**Eksempler på kladdeposter:** Kortfristet leasingforpligtelse</span><span class="sxs-lookup"><span data-stu-id="43f6e-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="43f6e-130">**Debet:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-131">**Kredit:** Kortfristet leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-132">**Debet:** Kortfristet leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-133">**Kredit:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="43f6e-134">Afskrivningsomkostning</span><span class="sxs-lookup"><span data-stu-id="43f6e-134">Depreciation expense</span></span>

<span data-ttu-id="43f6e-135">Kontoen er tilknyttet den udgift, der er relateret til afskrivningen af ROU-aktivet under IFRS 16, ASC 842, og finansielle leasingaftaler under IAS 17 og ASC 840.</span><span class="sxs-lookup"><span data-stu-id="43f6e-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="43f6e-136">Denne konto debiteres, når et ROU-aktiv afskrives hver måned.</span><span class="sxs-lookup"><span data-stu-id="43f6e-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="43f6e-137">**Eksempel på kladdeposter:** Afskrivningsperiodisering</span><span class="sxs-lookup"><span data-stu-id="43f6e-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="43f6e-138">**Debet:** Afskrivningsudgift xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="43f6e-139">**Kredit:** Akkumuleret afskrivning xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="43f6e-140">Gevinst/tab ved leasingændring</span><span class="sxs-lookup"><span data-stu-id="43f6e-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="43f6e-141">Kontoen er tilknyttet eventuelle gevinster eller tab, der opstår i forbindelse med leasingændringer.</span><span class="sxs-lookup"><span data-stu-id="43f6e-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="43f6e-142">Der kan opstå en indtægt under en ændring af leasingaftalen, hvis ændringen reducerer leasingforpligtelsen med et beløb, der overstiger ROU-aktivets bærende værdi.</span><span class="sxs-lookup"><span data-stu-id="43f6e-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="43f6e-143">En leasingaftale har f. eks. en aktuel værdi på $150.000 og en bærende værdi af det ROU-aktiv i $100.000.</span><span class="sxs-lookup"><span data-stu-id="43f6e-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="43f6e-144">Leasingaftalen ændres, og denne ændring giver en ny nutidsværdi af de fremtidige minimums leasingbetaling (PVFMLP) på $40.000.</span><span class="sxs-lookup"><span data-stu-id="43f6e-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="43f6e-145">Leasingforpligtelsen debiteres med $110.000 ($150.000 – $40.000).</span><span class="sxs-lookup"><span data-stu-id="43f6e-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="43f6e-146">Da ROU-aktivet kun er $100.000, vil reduktionen på $110.000 reducere aktivet med 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="43f6e-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="43f6e-147">Derfor angiver regnskabsvejledningen, at resten skal konteres til en gevinstkonto.</span><span class="sxs-lookup"><span data-stu-id="43f6e-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="43f6e-148">I dette tilfælde vil den endelige journaloptegnelse være en debitering af leasingforpligtelsen på $110.000, en kreditering til leasingaktivet på $100.000 og en kreditering på gevinstkontoen på $10.000.</span><span class="sxs-lookup"><span data-stu-id="43f6e-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="43f6e-149">**Eksempel på kladdeposter:** Leasingændringer</span><span class="sxs-lookup"><span data-stu-id="43f6e-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="43f6e-150">**Debet:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-151">**Kredit:** Leasingaktiv xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="43f6e-152">**Kredit:** Gevinst xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="43f6e-153">Akkumuleret afskrivning</span><span class="sxs-lookup"><span data-stu-id="43f6e-153">Accumulated depreciation</span></span>

<span data-ttu-id="43f6e-154">Kontoen er tilknyttet ROU-anlægsaktivets konto.</span><span class="sxs-lookup"><span data-stu-id="43f6e-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="43f6e-155">Denne konto krediteres, når der afskrives udgifter.</span><span class="sxs-lookup"><span data-stu-id="43f6e-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="43f6e-156">**Eksempel på kladdeposter:** Afskrivningsperiodisering</span><span class="sxs-lookup"><span data-stu-id="43f6e-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="43f6e-157">**Debet:** Afskrivningsudgift xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="43f6e-158">**Kredit:** Akkumuleret afskrivning xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="43f6e-159">Variabel betaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-159">Variable payment</span></span>

<span data-ttu-id="43f6e-160">Kontoen er knyttet til variable leasingbetalinger, der er produceret af en indeksværdiregulering under ASC 842, ASC 840 og IAS 17-leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="43f6e-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="43f6e-161">I betalingsplanen for leasingaftalen medtages variable betalinger i kolonnen **Variabel betaling**.</span><span class="sxs-lookup"><span data-stu-id="43f6e-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="43f6e-162">Denne konto debiteres, når der oprettes en faktura i forhold til en betalingsplanlinje, der indeholder en variabel betaling.</span><span class="sxs-lookup"><span data-stu-id="43f6e-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="43f6e-163">**Eksempel på kladdeposter:** Leasingbetaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="43f6e-164">**Debet:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-165">**Debet:** Variabel betaling xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="43f6e-166">**Kredit:** Kreditor-/leasingbetaling xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="43f6e-167">Aktiv med udskudt leje (passiv)</span><span class="sxs-lookup"><span data-stu-id="43f6e-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="43f6e-168">Kontoen er knyttet til det udskudte aktiv- eller passivbeløb, der er fremstillet af en leasingaftale til at blive forskudt til lejebehandling.</span><span class="sxs-lookup"><span data-stu-id="43f6e-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="43f6e-169">Denne konto debiteres, når en faktura bogføres i forhold til en udskudt lejebehandling af leasingaftale, hvis betalingsbeløbet er mere end periodens lejeudgifter.</span><span class="sxs-lookup"><span data-stu-id="43f6e-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="43f6e-170">Den krediteres, hvis leasingbetalingen er mindre end den lineære lejeudgifter for perioden.</span><span class="sxs-lookup"><span data-stu-id="43f6e-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="43f6e-171">**Eksempler på kladdeposter:** Leasingbetaling (udskudt rettighed til lejebehandling af leasingaftale)</span><span class="sxs-lookup"><span data-stu-id="43f6e-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="43f6e-172">**Debet:** Leasingudgift xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="43f6e-173">**Kredit:** Leasingaftale med udskudt leje XXX</span><span class="sxs-lookup"><span data-stu-id="43f6e-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="43f6e-174">**Kredit:** Kreditor-/leasingbetaling xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="43f6e-175">Leasingudgift</span><span class="sxs-lookup"><span data-stu-id="43f6e-175">Lease expense</span></span>

<span data-ttu-id="43f6e-176">Kontoen er tilknyttet leasingudgift, hvis leasingen klassificeres som en rettighed til at opnå en udskudt lejebehandling af leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="43f6e-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="43f6e-177">Denne konto debiteres, når en faktura bogføres i forhold til en leasingaftale til udskudt lejebehandling.</span><span class="sxs-lookup"><span data-stu-id="43f6e-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="43f6e-178">**Eksempler på kladdeposter:** Leasingbetaling (udskudt rettighed til lejebehandling af leasingaftale)</span><span class="sxs-lookup"><span data-stu-id="43f6e-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="43f6e-179">**Debet:** Leasingudgift xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="43f6e-180">**Kredit:** Leasingaftale med udskudt leje XXX</span><span class="sxs-lookup"><span data-stu-id="43f6e-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="43f6e-181">**Kredit:** Kreditor-/leasingbetaling xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="43f6e-182">Udgift til værdiforringelse</span><span class="sxs-lookup"><span data-stu-id="43f6e-182">Impairment expense</span></span>

<span data-ttu-id="43f6e-183">Kontoen bogføres i forhold til, når en leasingaftale er forringet.</span><span class="sxs-lookup"><span data-stu-id="43f6e-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="43f6e-184">Denne konto debiteres, mens ROU-aktivkonto krediteres direkte.</span><span class="sxs-lookup"><span data-stu-id="43f6e-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="43f6e-185">**Eksempel på kladdeposter:** Leasingbetaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="43f6e-186">**Debet:** Udgift til værdiforringelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="43f6e-187">**Kredit:** ROU-aktiv xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="43f6e-188">Leasingbetaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-188">Lease payment</span></span>

<span data-ttu-id="43f6e-189">Kontoen bogføres i forhold til parameteren **Betal til kreditor** er deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="43f6e-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="43f6e-190">Denne konto krediteres i stedet for kreditoren, hvis parameteren er deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="43f6e-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="43f6e-191">**Eksempel på kladdeposter:** Leasingbetaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="43f6e-192">**Debet:** Leasingforpligtelse xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="43f6e-193">**Kredit:** Leasingaftalebetaling xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="43f6e-194">Udgiftstypeposteringer</span><span class="sxs-lookup"><span data-stu-id="43f6e-194">Expense type postings</span></span>

<span data-ttu-id="43f6e-195">Den konto, der er valgt for hver udgiftstype, debiteres, når der genereres en betaling for den pågældende udgiftstype.</span><span class="sxs-lookup"><span data-stu-id="43f6e-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="43f6e-196">Den konto, der er angivet for udgiftstypen **Forsikring**, debiteres f. eks., når en faktura- eller betalingskladdepost oprettes ud fra planlægningen af det udførende omkostningsskema for forsikringsudgifter.</span><span class="sxs-lookup"><span data-stu-id="43f6e-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="43f6e-197">**Eksempel på kladdeposter:** Forsikringsbetaling</span><span class="sxs-lookup"><span data-stu-id="43f6e-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="43f6e-198">**Debet:** Forsikringsudgiftstypekonto xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="43f6e-199">**Kredit:** Modkonto xxx</span><span class="sxs-lookup"><span data-stu-id="43f6e-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="43f6e-200">Modkontoen vælges på leasingniveau på linjerne for betalingsplanen for driftsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="43f6e-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="43f6e-201">Denne modkonto kan knyttes til kreditoren eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="43f6e-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
