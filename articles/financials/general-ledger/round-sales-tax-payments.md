---
title: Momsafregninger og afrundingsregler
description: I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834992"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="d30e2-103">Momsafregninger og afrundingsregler</span><span class="sxs-lookup"><span data-stu-id="d30e2-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d30e2-104">I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.</span><span class="sxs-lookup"><span data-stu-id="d30e2-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="d30e2-105">Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="d30e2-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="d30e2-106">Dette kan gøres ved at køre processen til udligning og postering af moms på siden Moms.</span><span class="sxs-lookup"><span data-stu-id="d30e2-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="d30e2-107">Moms for en periode udlignes til momskontiene og momssaldoen posteres til momsafregningskontoen.</span><span class="sxs-lookup"><span data-stu-id="d30e2-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="d30e2-108">Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden Moms.</span><span class="sxs-lookup"><span data-stu-id="d30e2-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="d30e2-109">Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.</span><span class="sxs-lookup"><span data-stu-id="d30e2-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="d30e2-110">Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.</span><span class="sxs-lookup"><span data-stu-id="d30e2-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="d30e2-111">Eksempler</span><span class="sxs-lookup"><span data-stu-id="d30e2-111">Examples</span></span>

<span data-ttu-id="d30e2-112">Den samlede moms for en periode viser en kreditsaldo på -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="d30e2-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="d30e2-113">Den juridiske enhed opkrævede mere moms, end den betalte.</span><span class="sxs-lookup"><span data-stu-id="d30e2-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="d30e2-114">Den juridiske enhed skylder derfor penge til skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="d30e2-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="d30e2-115">Den juridiske enhed vil bruge en afrundingsmetode, der afrunder saldoen til nærmeste hele 1,00.</span><span class="sxs-lookup"><span data-stu-id="d30e2-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="d30e2-116">Den bruger, der er ansvarlig for bogføring af moms, udfører følgende trin.</span><span class="sxs-lookup"><span data-stu-id="d30e2-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="d30e2-117">Klik på Moms &gt; Indirekte skatter &gt; Moms &gt; Skattemyndigheder</span><span class="sxs-lookup"><span data-stu-id="d30e2-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="d30e2-118">I oversigtspanelet Generelt skal du vælge Normal i feltet Afrundingsform.</span><span class="sxs-lookup"><span data-stu-id="d30e2-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="d30e2-119">Angiv 1,00 i feltet Afrunding.</span><span class="sxs-lookup"><span data-stu-id="d30e2-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="d30e2-120">Når det er tid til at betale momsen til skattemyndighederne, skal du åbne siden Afregn og bogfør moms.</span><span class="sxs-lookup"><span data-stu-id="d30e2-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="d30e2-121">(Klik på Moms &gt; Opgørelser &gt; Moms &gt; Afregn og bogfør moms).</span><span class="sxs-lookup"><span data-stu-id="d30e2-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="d30e2-122">I momsafregningskontoen afrundes skattetilsvarsbeløbet på 98.765,43 til 98.765.</span><span class="sxs-lookup"><span data-stu-id="d30e2-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="d30e2-123">Følgende tabel viser, hvordan et beløb på 98.765,43 afrundes ved hjælp af hver afrundingsmetode, der er tilgængelig i feltet Afrundingsform på siden Skattemyndigheder.</span><span class="sxs-lookup"><span data-stu-id="d30e2-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="d30e2-124">Indstilling for afrundingsform</span><span class="sxs-lookup"><span data-stu-id="d30e2-124">Rounding form option</span></span>                | <span data-ttu-id="d30e2-125">Afrundingsværdi = 0,01</span><span class="sxs-lookup"><span data-stu-id="d30e2-125">Round-off value = 0.01</span></span> | <span data-ttu-id="d30e2-126">Afrundingsværdi = 0,10</span><span class="sxs-lookup"><span data-stu-id="d30e2-126">Round-off value = 0.10</span></span> | <span data-ttu-id="d30e2-127">Afrundingsværdi = 1,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-127">Round-off value = 1.00</span></span> | <span data-ttu-id="d30e2-128">Afrundingsværdi = 100,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="d30e2-129">Almindelig</span><span class="sxs-lookup"><span data-stu-id="d30e2-129">Normal</span></span>                              | <span data-ttu-id="d30e2-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d30e2-130">98,765.43</span></span>              | <span data-ttu-id="d30e2-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="d30e2-131">98,765.40</span></span>              | <span data-ttu-id="d30e2-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-132">98,765.00</span></span>              | <span data-ttu-id="d30e2-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-133">98,800.00</span></span>                |
| <span data-ttu-id="d30e2-134">Nedad</span><span class="sxs-lookup"><span data-stu-id="d30e2-134">Downward</span></span>                            | <span data-ttu-id="d30e2-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d30e2-135">98,765.43</span></span>              | <span data-ttu-id="d30e2-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="d30e2-136">98,765.40</span></span>              | <span data-ttu-id="d30e2-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-137">98,765.00</span></span>              | <span data-ttu-id="d30e2-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-138">98,700.00</span></span>                |
| <span data-ttu-id="d30e2-139">Oprunding</span><span class="sxs-lookup"><span data-stu-id="d30e2-139">Rounding-up</span></span>                         | <span data-ttu-id="d30e2-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d30e2-140">98,765.43</span></span>              | <span data-ttu-id="d30e2-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="d30e2-141">98,765.50</span></span>              | <span data-ttu-id="d30e2-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-142">98,766.00</span></span>              | <span data-ttu-id="d30e2-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-143">98,800.00</span></span>                |
| <span data-ttu-id="d30e2-144">Egen fordel, for en kreditsaldo</span><span class="sxs-lookup"><span data-stu-id="d30e2-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="d30e2-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="d30e2-145">98,765.43</span></span>              | <span data-ttu-id="d30e2-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="d30e2-146">98,765.40</span></span>              | <span data-ttu-id="d30e2-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-147">98,765.00</span></span>              | <span data-ttu-id="d30e2-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-148">98,700.00</span></span>                |
| <span data-ttu-id="d30e2-149">Egen fordel, for en debetsaldo</span><span class="sxs-lookup"><span data-stu-id="d30e2-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="d30e2-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="d30e2-150">98,765.43</span></span>              | <span data-ttu-id="d30e2-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="d30e2-151">98,765.50</span></span>              | <span data-ttu-id="d30e2-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="d30e2-152">98,766.00</span></span>              | <span data-ttu-id="d30e2-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="d30e2-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="d30e2-154">Ingen afrunding overhovedet, da afrundingen er 0,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="d30e2-155">afrund(1,0151, 0,00) = 1,0151 afrund(1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="d30e2-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="d30e2-156">Normal afrunding og afrundingspræcision er 0,01</span><span class="sxs-lookup"><span data-stu-id="d30e2-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="d30e2-157">Afrunding</span><span class="sxs-lookup"><span data-stu-id="d30e2-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="d30e2-158">Beregningsproces</span><span class="sxs-lookup"><span data-stu-id="d30e2-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="d30e2-159">afrund(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="d30e2-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="d30e2-160">afrund(1,015 / 0,01, 0) = afrund(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="d30e2-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="d30e2-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="d30e2-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="d30e2-162">afrund(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="d30e2-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="d30e2-163">afrund(1,014 / 0,01, 0) = afrund(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="d30e2-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="d30e2-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="d30e2-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="d30e2-165">afrund(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="d30e2-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="d30e2-166">afrund(1,011 / 0,02, 0) = afrund(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="d30e2-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="d30e2-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="d30e2-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="d30e2-168">afrund(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="d30e2-169">afrund(1,009 / 0,02, 0) = afrund(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="d30e2-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="d30e2-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="d30e2-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="d30e2-171">Hvis du vælger Egen fordel, er afrundingen altid til fordel for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="d30e2-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="d30e2-172">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="d30e2-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="d30e2-173">Momsoversigt</span><span class="sxs-lookup"><span data-stu-id="d30e2-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="d30e2-174">Oprette en momsbetaling</span><span class="sxs-lookup"><span data-stu-id="d30e2-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="d30e2-175">Oprette momsposteringer i dokumenter</span><span class="sxs-lookup"><span data-stu-id="d30e2-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="d30e2-176">Vise bogførte momstransaktioner</span><span class="sxs-lookup"><span data-stu-id="d30e2-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="d30e2-177">afrundingsfunktion</span><span class="sxs-lookup"><span data-stu-id="d30e2-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


