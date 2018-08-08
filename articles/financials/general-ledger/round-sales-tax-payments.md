---
title: Momsafregninger og afrundingsregler
description: "I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms."
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="8d4ee-103">Momsafregninger og afrundingsregler</span><span class="sxs-lookup"><span data-stu-id="8d4ee-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d4ee-104">I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="8d4ee-105">Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="8d4ee-106">Dette kan gøres ved at køre processen til udligning og postering af moms på siden Moms.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="8d4ee-107">Moms for en periode udlignes til momskontiene og momssaldoen posteres til momsafregningskontoen.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="8d4ee-108">Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden Moms.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="8d4ee-109">Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="8d4ee-110">Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="8d4ee-111">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="8d4ee-111">Example:</span></span>

<span data-ttu-id="8d4ee-112">Den samlede moms for en periode viser en kreditsaldo på -98.765,43.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="8d4ee-113">Den juridiske enhed opkrævede mere moms, end den betalte.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="8d4ee-114">Den juridiske enhed skylder derfor penge til skattemyndighederne.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="8d4ee-115">Den juridiske enhed vil bruge en afrundingsmetode, der afrunder saldoen til nærmeste hele 1,00.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="8d4ee-116">Den bruger, der er ansvarlig for bogføring af moms, udfører følgende trin.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="8d4ee-117">Klik på Moms &gt; Indirekte skatter &gt; Moms &gt; Skattemyndigheder</span><span class="sxs-lookup"><span data-stu-id="8d4ee-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="8d4ee-118">I oversigtspanelet Generelt skal du vælge Normal i feltet Afrundingsform.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="8d4ee-119">Angiv 1,00 i feltet Afrunding.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="8d4ee-120">Når det er tid til at betale momsen til skattemyndighederne, skal du åbne siden Afregn og bogfør moms.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="8d4ee-121">(Klik på Moms &gt; Opgørelser &gt; Moms &gt; Afregn og bogfør moms).</span><span class="sxs-lookup"><span data-stu-id="8d4ee-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="8d4ee-122">I momsafregningskontoen afrundes skattetilsvarsbeløbet på 98.765,43 til 98.765.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="8d4ee-123">Følgende tabel viser, hvordan et beløb på 98.765,43 afrundes ved hjælp af hver afrundingsmetode, der er tilgængelig i feltet Afrundingsform på siden Skattemyndigheder.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="8d4ee-124">Indstilling for afrundingsform</span><span class="sxs-lookup"><span data-stu-id="8d4ee-124">Rounding form option</span></span>                | <span data-ttu-id="8d4ee-125">Afrundingsværdi = 0,01</span><span class="sxs-lookup"><span data-stu-id="8d4ee-125">Round-off value = 0.01</span></span> | <span data-ttu-id="8d4ee-126">Afrundingsværdi = 0,10</span><span class="sxs-lookup"><span data-stu-id="8d4ee-126">Round-off value = 0.10</span></span> | <span data-ttu-id="8d4ee-127">Afrundingsværdi = 1,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-127">Round-off value = 1.00</span></span> | <span data-ttu-id="8d4ee-128">Afrundingsværdi = 100,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="8d4ee-129">Almindelig</span><span class="sxs-lookup"><span data-stu-id="8d4ee-129">Normal</span></span>                              | <span data-ttu-id="8d4ee-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="8d4ee-130">98,765.43</span></span>              | <span data-ttu-id="8d4ee-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="8d4ee-131">98,765.40</span></span>              | <span data-ttu-id="8d4ee-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-132">98,765.00</span></span>              | <span data-ttu-id="8d4ee-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-133">98,800.00</span></span>                |
| <span data-ttu-id="8d4ee-134">Nedad</span><span class="sxs-lookup"><span data-stu-id="8d4ee-134">Downward</span></span>                            | <span data-ttu-id="8d4ee-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="8d4ee-135">98,765.43</span></span>              | <span data-ttu-id="8d4ee-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="8d4ee-136">98,765.40</span></span>              | <span data-ttu-id="8d4ee-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-137">98,765.00</span></span>              | <span data-ttu-id="8d4ee-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-138">98,700.00</span></span>                |
| <span data-ttu-id="8d4ee-139">Oprunding</span><span class="sxs-lookup"><span data-stu-id="8d4ee-139">Rounding-up</span></span>                         | <span data-ttu-id="8d4ee-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="8d4ee-140">98,765.43</span></span>              | <span data-ttu-id="8d4ee-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="8d4ee-141">98,765.50</span></span>              | <span data-ttu-id="8d4ee-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-142">98,766.00</span></span>              | <span data-ttu-id="8d4ee-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-143">98,800.00</span></span>                |
| <span data-ttu-id="8d4ee-144">Egen fordel, for en kreditsaldo</span><span class="sxs-lookup"><span data-stu-id="8d4ee-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="8d4ee-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="8d4ee-145">98,765.43</span></span>              | <span data-ttu-id="8d4ee-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="8d4ee-146">98,765.40</span></span>              | <span data-ttu-id="8d4ee-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-147">98,765.00</span></span>              | <span data-ttu-id="8d4ee-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-148">98,700.00</span></span>                |
| <span data-ttu-id="8d4ee-149">Egen fordel, for en debetsaldo</span><span class="sxs-lookup"><span data-stu-id="8d4ee-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="8d4ee-150">98.765,43</span><span class="sxs-lookup"><span data-stu-id="8d4ee-150">98,765.43</span></span>              | <span data-ttu-id="8d4ee-151">98.765,50</span><span class="sxs-lookup"><span data-stu-id="8d4ee-151">98,765.50</span></span>              | <span data-ttu-id="8d4ee-152">98.766,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-152">98,766.00</span></span>              | <span data-ttu-id="8d4ee-153">98.800,00</span><span class="sxs-lookup"><span data-stu-id="8d4ee-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="8d4ee-154">Hvis du vælger Egen fordel, er afrundingen altid til fordel for den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="8d4ee-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="8d4ee-155">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="8d4ee-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="8d4ee-156">Momsoversigt</span><span class="sxs-lookup"><span data-stu-id="8d4ee-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="8d4ee-157">Oprette en momsbetaling</span><span class="sxs-lookup"><span data-stu-id="8d4ee-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="8d4ee-158">Oprette momsposteringer i dokumenter</span><span class="sxs-lookup"><span data-stu-id="8d4ee-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="8d4ee-159">Vise bogførte momsposteringer</span><span class="sxs-lookup"><span data-stu-id="8d4ee-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



