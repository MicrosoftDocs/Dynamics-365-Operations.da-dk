---
title: Beregning af moms på finanskladdelinjer
description: Dette emne forklarer, hvordan der beregnes moms for forskellige typer konti (kreditor, debitor, finans og projekt) på finanskladdelinjer.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983591"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="0ff10-103">Beregning af moms på finanskladdelinjer</span><span class="sxs-lookup"><span data-stu-id="0ff10-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ff10-104">Dette emne forklarer, hvordan der beregnes moms for forskellige typer konti (kreditor, debitor, finans og projekt) på finanskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="0ff10-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="0ff10-105">Processen kan opdeles i tre trin:</span><span class="sxs-lookup"><span data-stu-id="0ff10-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="0ff10-106">Fastsætte momsretningen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="0ff10-107">Fastsætte det momsbeløb, der skal gemmes en midlertidig momstabel.</span><span class="sxs-lookup"><span data-stu-id="0ff10-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="0ff10-108">Fastsætte momsbeløbet og kontoen på bilaget.</span><span class="sxs-lookup"><span data-stu-id="0ff10-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="0ff10-109">Fastsætte momsretningen</span><span class="sxs-lookup"><span data-stu-id="0ff10-109">Determine the sales tax direction</span></span>

<span data-ttu-id="0ff10-110">Den måde, som momsretningen fastsættes på, afhænger af kontotypen i bilaget.</span><span class="sxs-lookup"><span data-stu-id="0ff10-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="0ff10-111">Momsretningen bestemmes af kombinationen af kontotype og momskode.</span><span class="sxs-lookup"><span data-stu-id="0ff10-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="0ff10-112">I følgende afsnit beskrives mulighederne mere detaljeret.</span><span class="sxs-lookup"><span data-stu-id="0ff10-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="0ff10-113">Kontotype er Projekt</span><span class="sxs-lookup"><span data-stu-id="0ff10-113">Account type is Project</span></span>

<span data-ttu-id="0ff10-114">Hvis et bilag har en kladdelinje, hvor kontotypen er **Projekt**, anvender alle kladdelinjerne i bilaget samme momsretning.</span><span class="sxs-lookup"><span data-stu-id="0ff10-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="0ff10-115">Følgende illustration viser reglen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-115">The following illustration shows the rule.</span></span> <span data-ttu-id="0ff10-116">Følgende punkter viser de mulige momsretninger for projektkonti.</span><span class="sxs-lookup"><span data-stu-id="0ff10-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="0ff10-117">• Hvis momskoden er importmoms, er momsretningen Importmoms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="0ff10-118">• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.</span><span class="sxs-lookup"><span data-stu-id="0ff10-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0ff10-119">• Hvis momskoden er ekstern moms, er momsretningen Udgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0ff10-120">• Hvis momskoden er modtagermoms, er momsretningen Udgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0ff10-121">Ellers bruges momsretningen Indgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0ff10-122">I følgende diagram vises reglen grafisk.</span><span class="sxs-lookup"><span data-stu-id="0ff10-122">The following diagram illustrates the rule graphically.</span></span>

![Muligheder for momsretning for projektkonti](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="0ff10-124">Kontotype er Kreditor</span><span class="sxs-lookup"><span data-stu-id="0ff10-124">Account type is Vendor</span></span>

<span data-ttu-id="0ff10-125">Hvis et bilag har en kladdelinje, hvor kontotypen er **Kreditor**, anvender alle kladdelinjerne i bilaget samme momsretning.</span><span class="sxs-lookup"><span data-stu-id="0ff10-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="0ff10-126">Følgende punkter viser de mulige momsretninger for kreditorkonti.</span><span class="sxs-lookup"><span data-stu-id="0ff10-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="0ff10-127">• Hvis momskoden er importmoms, er momsretningen Importmoms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="0ff10-128">• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.</span><span class="sxs-lookup"><span data-stu-id="0ff10-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0ff10-129">• Hvis momskoden er ekstern moms, er momsretningen Udgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0ff10-130">• Hvis momskoden er modtagermoms, er momsretningen Udgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0ff10-131">Ellers bruges momsretningen Indgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0ff10-132">I følgende diagram vises reglen grafisk.</span><span class="sxs-lookup"><span data-stu-id="0ff10-132">The following diagram illustrates the rule graphically.</span></span>

![Muligheder for momsretning for kreditorkonti](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="0ff10-134">Kontotype er Debitor</span><span class="sxs-lookup"><span data-stu-id="0ff10-134">Account type is Customer</span></span>

<span data-ttu-id="0ff10-135">Hvis et bilag har en kladdelinje, hvor kontotypen er **Debitor**, anvender alle kladdelinjerne i bilaget samme momsretning.</span><span class="sxs-lookup"><span data-stu-id="0ff10-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="0ff10-136">Følgende punkter viser de mulige momsretninger for debitorkonti.</span><span class="sxs-lookup"><span data-stu-id="0ff10-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="0ff10-137">• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.</span><span class="sxs-lookup"><span data-stu-id="0ff10-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0ff10-138">• Hvis momskoden er ekstern moms, er momsretningen Indgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0ff10-139">• Hvis momskoden er modtagermoms, er momsretningen Indgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0ff10-140">Ellers bruges momsretningen Udgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0ff10-141">I følgende diagram vises reglen grafisk.</span><span class="sxs-lookup"><span data-stu-id="0ff10-141">The following diagram illustrates the rule graphically.</span></span>

![Muligheder for momsretning for debitorkonti](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="0ff10-143">Kontotype er Finans</span><span class="sxs-lookup"><span data-stu-id="0ff10-143">Account type is Ledger</span></span>

<span data-ttu-id="0ff10-144">I følgende illustration vises den regel, der gælder, når et bilag kun har kladdelinjer, hvor kontotypen er **Finans**.</span><span class="sxs-lookup"><span data-stu-id="0ff10-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="0ff10-145">Følgende punkter viser de mulige momsretninger for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="0ff10-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="0ff10-146">• Hvis momskoden er importmoms, er momsretningen Importmoms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="0ff10-147">• Hvis momskoden er momsfrit, er momsretningen Momsfrit køb.</span><span class="sxs-lookup"><span data-stu-id="0ff10-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0ff10-148">Ellers bruges momsretningen Indgående moms, hvis kladdebeløbet er debet (positiv). Hvis kladdebeløbet er kredit (negativt), er momsretningen Udgående moms.</span><span class="sxs-lookup"><span data-stu-id="0ff10-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0ff10-149">I følgende diagram vises reglen grafisk.</span><span class="sxs-lookup"><span data-stu-id="0ff10-149">The following diagram illustrates the rule graphically.</span></span>

![Muligheder for momsretning for finanskonti](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="0ff10-151">Tilsidesætte momsretningen</span><span class="sxs-lookup"><span data-stu-id="0ff10-151">Override the sales tax direction</span></span>

<span data-ttu-id="0ff10-152">Du kan tilsidesætte momsretningen, når bilaget kun indeholder linjer, hvor kontotypen er **Finans**.</span><span class="sxs-lookup"><span data-stu-id="0ff10-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="0ff10-153">Gå til **Finans \> Kontoplan \> Konti \> Hovedkonti**, og vælg oversigtspanelet **Tilsidesættelser af juridisk enhed**.</span><span class="sxs-lookup"><span data-stu-id="0ff10-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="0ff10-154">Fastsætte momsbeløbet</span><span class="sxs-lookup"><span data-stu-id="0ff10-154">Determine the sales tax amount</span></span>

<span data-ttu-id="0ff10-155">I dette afsnit beskrives, hvordan momsbeløbs fortegn beregnes.</span><span class="sxs-lookup"><span data-stu-id="0ff10-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Siden Momstransaktioner](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="0ff10-157">Følgende tabel indeholder den generelle regel til bestemmelse af fortegn på momsbeløb i den midlertidige momstabel.</span><span class="sxs-lookup"><span data-stu-id="0ff10-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="0ff10-158">Kladdelinjebeløb</span><span class="sxs-lookup"><span data-stu-id="0ff10-158">Journal line amount</span></span> | <span data-ttu-id="0ff10-159">Momsretning</span><span class="sxs-lookup"><span data-stu-id="0ff10-159">Sales tax direction</span></span>  | <span data-ttu-id="0ff10-160">Fortegn for momsbeløb</span><span class="sxs-lookup"><span data-stu-id="0ff10-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="0ff10-161">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-161">Positive</span></span>            | <span data-ttu-id="0ff10-162">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-162">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-163">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-163">Positive</span></span>              |
| <span data-ttu-id="0ff10-164">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-164">Positive</span></span>            | <span data-ttu-id="0ff10-165">Udgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-165">Sales Tax Payable</span></span>    | <span data-ttu-id="0ff10-166">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-166">Negative</span></span>              |
| <span data-ttu-id="0ff10-167">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-167">Negative</span></span>            | <span data-ttu-id="0ff10-168">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-168">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-169">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-169">Negative</span></span>              |
| <span data-ttu-id="0ff10-170">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-170">Negative</span></span>            | <span data-ttu-id="0ff10-171">Udgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-171">Sales Tax Payable</span></span>    | <span data-ttu-id="0ff10-172">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-172">Positive</span></span>              |

<span data-ttu-id="0ff10-173">Der findes en særlig regel for bilag, der kun indeholder **Projekt**- eller **Finans**-linjer, når der er valgt en momsgruppe eller varemomsgruppe på **Finans**-linjen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="0ff10-174">Denne regel styres ved at aktivere den uafhængige momsberegningsfunktion for finanskladder.</span><span class="sxs-lookup"><span data-stu-id="0ff10-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="0ff10-175">Når denne funktion er deaktiveret, bruger momsbeløbet i **Finans**-linjen debet- og kreditretningen for **Projekt**-linjen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="0ff10-176">Når denne funktion er aktiveret, bruger momsbeløbet i **Finans**-linjen egen debet- og kreditretning.</span><span class="sxs-lookup"><span data-stu-id="0ff10-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="0ff10-177">I følgende tabeller vises reglen for de enkelte scenarier.</span><span class="sxs-lookup"><span data-stu-id="0ff10-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="0ff10-178">**Regel, når funktionen er slåer til**</span><span class="sxs-lookup"><span data-stu-id="0ff10-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="0ff10-179">Kladdelinjebeløb i projekt</span><span class="sxs-lookup"><span data-stu-id="0ff10-179">Journal line amount of project</span></span> | <span data-ttu-id="0ff10-180">Momsretning</span><span class="sxs-lookup"><span data-stu-id="0ff10-180">Sales tax direction</span></span>  | <span data-ttu-id="0ff10-181">Fortegn for momsbeløb</span><span class="sxs-lookup"><span data-stu-id="0ff10-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="0ff10-182">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-182">Positive</span></span>                       | <span data-ttu-id="0ff10-183">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-183">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-184">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-184">Positive</span></span>              |
| <span data-ttu-id="0ff10-185">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-185">Negative</span></span>                       | <span data-ttu-id="0ff10-186">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-186">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-187">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-187">Negative</span></span>              |

<span data-ttu-id="0ff10-188">**Regel, når funktionen er slåer fra**</span><span class="sxs-lookup"><span data-stu-id="0ff10-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="0ff10-189">Kladdelinjebeløb i finans</span><span class="sxs-lookup"><span data-stu-id="0ff10-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="0ff10-190">Momsretning</span><span class="sxs-lookup"><span data-stu-id="0ff10-190">Sales tax direction</span></span>  | <span data-ttu-id="0ff10-191">Fortegn for momsbeløb</span><span class="sxs-lookup"><span data-stu-id="0ff10-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="0ff10-192">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-192">Positive</span></span>                       | <span data-ttu-id="0ff10-193">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-193">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-194">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-194">Positive</span></span>              |
| <span data-ttu-id="0ff10-195">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-195">Negative</span></span>                       | <span data-ttu-id="0ff10-196">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-196">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-197">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="0ff10-198">Fastsætte momsbeløbet og kontoen på bilaget</span><span class="sxs-lookup"><span data-stu-id="0ff10-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="0ff10-199">Når du bogfører moms, hentes hovedkontoen fra finanskonteringsgruppeprofilen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="0ff10-200">Når moms er indgående, bruger systemet den indgående momskonto, der er angivet i profilen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="0ff10-201">Når udgående moms bruger systemet den udgående momskonto, der er angivet i profilen.</span><span class="sxs-lookup"><span data-stu-id="0ff10-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="0ff10-202">I følgende tabel vises den generiske regel.</span><span class="sxs-lookup"><span data-stu-id="0ff10-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="0ff10-203">Momsretning</span><span class="sxs-lookup"><span data-stu-id="0ff10-203">Sales tax direction</span></span>  | <span data-ttu-id="0ff10-204">Fortegn for momsbeløb</span><span class="sxs-lookup"><span data-stu-id="0ff10-204">Sales tax amount sign</span></span> | <span data-ttu-id="0ff10-205">Momskonto</span><span class="sxs-lookup"><span data-stu-id="0ff10-205">Sales tax account</span></span>      | <span data-ttu-id="0ff10-206">Beløb på bilag</span><span class="sxs-lookup"><span data-stu-id="0ff10-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="0ff10-207">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-207">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-208">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-208">Positive</span></span>              | <span data-ttu-id="0ff10-209">Indgående momskonto</span><span class="sxs-lookup"><span data-stu-id="0ff10-209">Tax Receivable Account</span></span> | <span data-ttu-id="0ff10-210">Positiv (debet)</span><span class="sxs-lookup"><span data-stu-id="0ff10-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="0ff10-211">Indgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-211">Sales Tax Receivable</span></span> | <span data-ttu-id="0ff10-212">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-212">Negative</span></span>              | <span data-ttu-id="0ff10-213">Indgående momskonto</span><span class="sxs-lookup"><span data-stu-id="0ff10-213">Tax Receivable Account</span></span> | <span data-ttu-id="0ff10-214">Negativ (kredit)</span><span class="sxs-lookup"><span data-stu-id="0ff10-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="0ff10-215">Udgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-215">Sales Tax Payable</span></span>    | <span data-ttu-id="0ff10-216">Positiv</span><span class="sxs-lookup"><span data-stu-id="0ff10-216">Positive</span></span>              | <span data-ttu-id="0ff10-217">Udgående momskonto</span><span class="sxs-lookup"><span data-stu-id="0ff10-217">Tax Payable Account</span></span>    | <span data-ttu-id="0ff10-218">Negativ (kredit)</span><span class="sxs-lookup"><span data-stu-id="0ff10-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="0ff10-219">Udgående moms</span><span class="sxs-lookup"><span data-stu-id="0ff10-219">Sales Tax Payable</span></span>    | <span data-ttu-id="0ff10-220">Negativ</span><span class="sxs-lookup"><span data-stu-id="0ff10-220">Negative</span></span>              | <span data-ttu-id="0ff10-221">Udgående momskonto</span><span class="sxs-lookup"><span data-stu-id="0ff10-221">Tax Payable Account</span></span>    | <span data-ttu-id="0ff10-222">Positiv (debet)</span><span class="sxs-lookup"><span data-stu-id="0ff10-222">Positive (Debit)</span></span>  |
