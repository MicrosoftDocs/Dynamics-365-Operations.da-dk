---
title: Momsafregninger og afrundingsregler
description: I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8d7e402614b35a77a0283d31377a073b0a6b357
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990183"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="94f8f-103">Momsafregninger og afrundingsregler</span><span class="sxs-lookup"><span data-stu-id="94f8f-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94f8f-104">I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.</span><span class="sxs-lookup"><span data-stu-id="94f8f-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="94f8f-105">Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="94f8f-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="94f8f-106">Dette kan gøres ved at køre processen til udligning og postering af moms på siden Moms.</span><span class="sxs-lookup"><span data-stu-id="94f8f-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="94f8f-107">Moms for en periode udlignes til momskontiene og momssaldoen posteres til momsafregningskontoen.</span><span class="sxs-lookup"><span data-stu-id="94f8f-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="94f8f-108">Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden Moms.</span><span class="sxs-lookup"><span data-stu-id="94f8f-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="94f8f-109">Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.</span><span class="sxs-lookup"><span data-stu-id="94f8f-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="94f8f-110">Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.</span><span class="sxs-lookup"><span data-stu-id="94f8f-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="94f8f-111">Eksempler</span><span class="sxs-lookup"><span data-stu-id="94f8f-111">Examples</span></span>

<span data-ttu-id="94f8f-112">Den samlede moms for en periode viser en kreditsaldo på -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="94f8f-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="94f8f-113">Den juridiske enhed opkrævede mere moms, end den betalte.</span><span class="sxs-lookup"><span data-stu-id="94f8f-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="94f8f-114">Den juridiske enhed skylder derfor penge til skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="94f8f-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="94f8f-115">Den juridiske enhed vil bruge en afrundingsmetode, der afrunder saldoen til nærmeste hele 1,00.</span><span class="sxs-lookup"><span data-stu-id="94f8f-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="94f8f-116">Den bruger, der er ansvarlig for bogføring af moms, udfører følgende trin.</span><span class="sxs-lookup"><span data-stu-id="94f8f-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="94f8f-117">Klik på **Moms** > **Indirekte skatter** > **Moms** > **Momsmyndigheder**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="94f8f-118">I oversigtspanelet **Generelt** skal du vælge **Normal** i feltet **Afrundingsform**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="94f8f-119">Angiv 1,00 i feltet **Afrunding**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="94f8f-120">Når det er tid til at betale momsen til skattemyndighederne, skal du gå til **Moms** > **Erklæringer** > **Moms** > **Afregn og bogfør moms**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="94f8f-121">I momsafregningskontoen kan du se, at skattetilsvarsbeløbet på **98.765,43** er afrundet til **98.765**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="94f8f-122">Følgende tabel viser, hvordan et beløb på 98.765,43 afrundes ved hjælp af hver afrundingsmetode, der er tilgængelig i feltet **Afrundingsform** på siden **Skattemyndigheder**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="94f8f-123">Hvis afrundingsværdien er angivet til 0,00, gælder følgende:</span><span class="sxs-lookup"><span data-stu-id="94f8f-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="94f8f-124">Ved normal afrunding er afrundingsfunktionen den samme som for **Afrunding = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="94f8f-125">I forbindelse med **Indstilling for afrundingsform**, **Nedad**, **Oprunding** og **Egen fordel** er funktionsmåden den samme som for **Afrunding = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="94f8f-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="94f8f-126">Indstilling for afrundingsform</span><span class="sxs-lookup"><span data-stu-id="94f8f-126">Rounding form option</span></span>                | <span data-ttu-id="94f8f-127">Afrundingsværdi = 0,01</span><span class="sxs-lookup"><span data-stu-id="94f8f-127">Round-off value = 0.01</span></span> | <span data-ttu-id="94f8f-128">Afrundingsværdi = 0,10</span><span class="sxs-lookup"><span data-stu-id="94f8f-128">Round-off value = 0.10</span></span> | <span data-ttu-id="94f8f-129">Afrundingsværdi = 1,00</span><span class="sxs-lookup"><span data-stu-id="94f8f-129">Round-off value = 1.00</span></span> | <span data-ttu-id="94f8f-130">Afrundingsværdi = 100,00</span><span class="sxs-lookup"><span data-stu-id="94f8f-130">Round-off value = 100.00</span></span> | <span data-ttu-id="94f8f-131">Afrundingsværdi = 0,00</span><span class="sxs-lookup"><span data-stu-id="94f8f-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="94f8f-132">Normal</span><span class="sxs-lookup"><span data-stu-id="94f8f-132">Normal</span></span>                              | <span data-ttu-id="94f8f-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="94f8f-133">98,765.43</span></span>              | <span data-ttu-id="94f8f-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="94f8f-134">98,765.40</span></span>              | <span data-ttu-id="94f8f-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-135">98,765.00</span></span>              | <span data-ttu-id="94f8f-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-136">98,800.00</span></span>                | <span data-ttu-id="94f8f-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="94f8f-137">98,765.43</span></span>                |
| <span data-ttu-id="94f8f-138">Nedad</span><span class="sxs-lookup"><span data-stu-id="94f8f-138">Downward</span></span>                            | <span data-ttu-id="94f8f-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="94f8f-139">98,765.43</span></span>              | <span data-ttu-id="94f8f-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="94f8f-140">98,765.40</span></span>              | <span data-ttu-id="94f8f-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-141">98,765.00</span></span>              | <span data-ttu-id="94f8f-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-142">98,700.00</span></span>                | <span data-ttu-id="94f8f-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-143">98,765.00</span></span>                |
| <span data-ttu-id="94f8f-144">Oprunding</span><span class="sxs-lookup"><span data-stu-id="94f8f-144">Rounding-up</span></span>                         | <span data-ttu-id="94f8f-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="94f8f-145">98,765.43</span></span>              | <span data-ttu-id="94f8f-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="94f8f-146">98,765.50</span></span>              | <span data-ttu-id="94f8f-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-147">98,766.00</span></span>              | <span data-ttu-id="94f8f-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-148">98,800.00</span></span>                | <span data-ttu-id="94f8f-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-149">98,766.00</span></span>                |
| <span data-ttu-id="94f8f-150">Egen fordel, for en kreditsaldo</span><span class="sxs-lookup"><span data-stu-id="94f8f-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="94f8f-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="94f8f-151">98,765.43</span></span>              | <span data-ttu-id="94f8f-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="94f8f-152">98,765.40</span></span>              | <span data-ttu-id="94f8f-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-153">98,765.00</span></span>              | <span data-ttu-id="94f8f-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-154">98,700.00</span></span>                | <span data-ttu-id="94f8f-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-155">98,765.00</span></span>                |
| <span data-ttu-id="94f8f-156">Egen fordel, for en debetsaldo</span><span class="sxs-lookup"><span data-stu-id="94f8f-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="94f8f-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="94f8f-157">98,765.43</span></span>              | <span data-ttu-id="94f8f-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="94f8f-158">98,765.50</span></span>              | <span data-ttu-id="94f8f-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-159">98,766.00</span></span>              | <span data-ttu-id="94f8f-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-160">98,800.00</span></span>                | <span data-ttu-id="94f8f-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="94f8f-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="94f8f-162">Normal afrunding og afrundingspræcision er 0,01</span><span class="sxs-lookup"><span data-stu-id="94f8f-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="94f8f-163">Afrunding</span><span class="sxs-lookup"><span data-stu-id="94f8f-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="94f8f-164">Beregningsproces</span><span class="sxs-lookup"><span data-stu-id="94f8f-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="94f8f-165">afrund(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="94f8f-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="94f8f-166">afrund(1,015 / 0,01, 0) = afrund(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="94f8f-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="94f8f-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="94f8f-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="94f8f-168">afrund(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="94f8f-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="94f8f-169">afrund(1,014 / 0,01, 0) = afrund(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="94f8f-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="94f8f-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="94f8f-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="94f8f-171">afrund(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="94f8f-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="94f8f-172">afrund(1,011 / 0,02, 0) = afrund(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="94f8f-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="94f8f-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="94f8f-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="94f8f-174">afrund(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="94f8f-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="94f8f-175">afrund(1,009 / 0,02, 0) = afrund(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="94f8f-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="94f8f-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="94f8f-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="94f8f-177">Hvis du vælger Egen fordel, er afrundingen altid til fordel for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="94f8f-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="94f8f-178">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="94f8f-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="94f8f-179">Momsoversigt</span><span class="sxs-lookup"><span data-stu-id="94f8f-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="94f8f-180">Oprette en momsbetaling</span><span class="sxs-lookup"><span data-stu-id="94f8f-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="94f8f-181">Oprette momstransaktioner på dokumenter</span><span class="sxs-lookup"><span data-stu-id="94f8f-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="94f8f-182">Vise bogførte momstransaktioner</span><span class="sxs-lookup"><span data-stu-id="94f8f-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="94f8f-183">afrundingsfunktion</span><span class="sxs-lookup"><span data-stu-id="94f8f-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


