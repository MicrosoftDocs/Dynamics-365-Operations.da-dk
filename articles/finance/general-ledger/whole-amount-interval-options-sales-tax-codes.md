---
title: Indstillinger for beregning af hele beløbet og intervaller for momskoder
description: I denne artikel beskrives indstillingerne for feltet Beregningsmåde for momskoder, og hvordan der beregnes moms for intervaller og hele beløb.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d452ccc94324a695f0d203486fc5fa8fe9db79f6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770545"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="ff68d-103">Indstillinger for beregning af hele beløbet og intervaller for momskoder</span><span class="sxs-lookup"><span data-stu-id="ff68d-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff68d-104">I denne artikel beskrives indstillingerne for feltet Beregningsmåde for momskoder, og hvordan der beregnes moms for intervaller og hele beløb.</span><span class="sxs-lookup"><span data-stu-id="ff68d-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="ff68d-105">Du kan konfigurere, at en momskode skal beregnes på grundlag af hele beløbet eller et intervalbeløb.</span><span class="sxs-lookup"><span data-stu-id="ff68d-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="ff68d-106">På siden Momskoder skal du bruge feltet Beregningsmåde på oversigtspanelet Beregning til at vælge, hvordan en momskode skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="ff68d-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="ff68d-107">Hele beløb – En momssats anvendes på hele det momspligtige beløb.</span><span class="sxs-lookup"><span data-stu-id="ff68d-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="ff68d-108">Interval – Det momspligtige beløb er opdelt i dele, hvor hver del ligger inden for et beløbsinterval, der er underlagt en bestemt momssats.</span><span class="sxs-lookup"><span data-stu-id="ff68d-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="ff68d-109">Den del af beløbet, der ligger inden for et bestemt interval, pålægges moms i henhold til momssatsen for dette interval.</span><span class="sxs-lookup"><span data-stu-id="ff68d-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="ff68d-110">Momsen er summen af de momsbeløb, der beregnes for hvert beløbsinterval.</span><span class="sxs-lookup"><span data-stu-id="ff68d-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="ff68d-111">Indstillingen Interval er kun tilgængelig, når du vælger Linje i en feltet Beregningsmåde i området Moms på siden Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="ff68d-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="ff68d-112">Du angiver Intervaller på siden Momskodeværdier ved at angive minimum- og maksimumgrænsebeløb pr. momssats.</span><span class="sxs-lookup"><span data-stu-id="ff68d-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="ff68d-113">For moms, der skal beregnes af alle momspligtige beløb, uanset den valgte beregningsmetode, skal intervallerne overholde følgende regler:</span><span class="sxs-lookup"><span data-stu-id="ff68d-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="ff68d-114">Første interval skal have en minimumgrænse på nul.</span><span class="sxs-lookup"><span data-stu-id="ff68d-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="ff68d-115">Det sidste interval, der skal have en maksimumgrænse på nul, angiver uendeligt.</span><span class="sxs-lookup"><span data-stu-id="ff68d-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="ff68d-116">Maksimumgrænsen for alle intervaller er minimumgrænsen for det næste interval.</span><span class="sxs-lookup"><span data-stu-id="ff68d-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="ff68d-117">Hvis et beløb er maksimumgrænsen for det forrige interval og minimumgrænsen for det næste interval, gælder momssatsen for det første interval for beløbet.</span><span class="sxs-lookup"><span data-stu-id="ff68d-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="ff68d-118">Hvis et beløb ligger uden for de intervaller, der er defineret af de øvre og nedre grænser, anvendes momssatsen 0.</span><span class="sxs-lookup"><span data-stu-id="ff68d-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="ff68d-119">Eksempel: Beregningsmåden er hele beløbet</span><span class="sxs-lookup"><span data-stu-id="ff68d-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="ff68d-120">På siden Momskodeværdier er momssatserne defineret i følgende intervaller i:</span><span class="sxs-lookup"><span data-stu-id="ff68d-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="ff68d-121">**Minimumsgrænse**</span><span class="sxs-lookup"><span data-stu-id="ff68d-121">**Minimum limit**</span></span> | <span data-ttu-id="ff68d-122">**Maksimumgrænse**</span><span class="sxs-lookup"><span data-stu-id="ff68d-122">**Maximum limit**</span></span> | <span data-ttu-id="ff68d-123">**Momssats**</span><span class="sxs-lookup"><span data-stu-id="ff68d-123">**Tax rate**</span></span> |
| <span data-ttu-id="ff68d-124">0,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-124">0.00</span></span>              | <span data-ttu-id="ff68d-125">50,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-125">50.00</span></span>             | <span data-ttu-id="ff68d-126">30 %</span><span class="sxs-lookup"><span data-stu-id="ff68d-126">30%</span></span>          |
| <span data-ttu-id="ff68d-127">50,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-127">50.00</span></span>             | <span data-ttu-id="ff68d-128">100,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-128">100.00</span></span>            | <span data-ttu-id="ff68d-129">20 %</span><span class="sxs-lookup"><span data-stu-id="ff68d-129">20%</span></span>          |
| <span data-ttu-id="ff68d-130">100,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-130">100.00</span></span>            | <span data-ttu-id="ff68d-131">0,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-131">0.00</span></span>              | <span data-ttu-id="ff68d-132">10 %</span><span class="sxs-lookup"><span data-stu-id="ff68d-132">10%</span></span>          |

<span data-ttu-id="ff68d-133">Momsen beregnes af hele det momspligtige beløb.</span><span class="sxs-lookup"><span data-stu-id="ff68d-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="ff68d-134">Momspligtigt beløb (pris)</span><span class="sxs-lookup"><span data-stu-id="ff68d-134">Taxable amount (price)</span></span> | <span data-ttu-id="ff68d-135">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="ff68d-135">Calculation</span></span>    | <span data-ttu-id="ff68d-136">Moms</span><span class="sxs-lookup"><span data-stu-id="ff68d-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="ff68d-137">35,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-137">35.00</span></span>                  | <span data-ttu-id="ff68d-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ff68d-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="ff68d-139">10,50</span><span class="sxs-lookup"><span data-stu-id="ff68d-139">10.50</span></span>     |
| <span data-ttu-id="ff68d-140">50,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-140">50.00</span></span>                  | <span data-ttu-id="ff68d-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ff68d-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="ff68d-142">15,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-142">15.00</span></span>     |
| <span data-ttu-id="ff68d-143">85,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-143">85.00</span></span>                  | <span data-ttu-id="ff68d-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="ff68d-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="ff68d-145">17,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-145">17.00</span></span>     |
| <span data-ttu-id="ff68d-146">305,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-146">305.00</span></span>                 | <span data-ttu-id="ff68d-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="ff68d-147">305.00 \* 0.10</span></span> | <span data-ttu-id="ff68d-148">30,50</span><span class="sxs-lookup"><span data-stu-id="ff68d-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="ff68d-149">Eksempel: Beregningsmåde er interval</span><span class="sxs-lookup"><span data-stu-id="ff68d-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="ff68d-150">På siden Værdier er momssatserne defineret i følgende intervaller:</span><span class="sxs-lookup"><span data-stu-id="ff68d-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="ff68d-151">**Minimumsgrænse**</span><span class="sxs-lookup"><span data-stu-id="ff68d-151">**Minimum limit**</span></span> | <span data-ttu-id="ff68d-152">**Maksimumgrænse**</span><span class="sxs-lookup"><span data-stu-id="ff68d-152">**Maximum limit**</span></span> | <span data-ttu-id="ff68d-153">**Momssats**</span><span class="sxs-lookup"><span data-stu-id="ff68d-153">**Tax rate**</span></span> |
| <span data-ttu-id="ff68d-154">0,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-154">0.00</span></span>              | <span data-ttu-id="ff68d-155">50,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-155">50.00</span></span>             | <span data-ttu-id="ff68d-156">30 %</span><span class="sxs-lookup"><span data-stu-id="ff68d-156">30%</span></span>          |
| <span data-ttu-id="ff68d-157">50,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-157">50.00</span></span>             | <span data-ttu-id="ff68d-158">100,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-158">100.00</span></span>            | <span data-ttu-id="ff68d-159">20 %</span><span class="sxs-lookup"><span data-stu-id="ff68d-159">20%</span></span>          |
| <span data-ttu-id="ff68d-160">100,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-160">100.00</span></span>            | <span data-ttu-id="ff68d-161">0,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-161">0.00</span></span>              | <span data-ttu-id="ff68d-162">10 %</span><span class="sxs-lookup"><span data-stu-id="ff68d-162">10%</span></span>          |

<span data-ttu-id="ff68d-163">Momsen er summen af de momsbeløb, der beregnes for hvert beløbsinterval.</span><span class="sxs-lookup"><span data-stu-id="ff68d-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="ff68d-164">Momspligtigt beløb (pris)</span><span class="sxs-lookup"><span data-stu-id="ff68d-164">Taxable amount (price)</span></span> | <span data-ttu-id="ff68d-165">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="ff68d-165">Calculation</span></span>                                                               | <span data-ttu-id="ff68d-166">Moms</span><span class="sxs-lookup"><span data-stu-id="ff68d-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ff68d-167">35,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-167">35.00</span></span>                  | <span data-ttu-id="ff68d-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ff68d-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="ff68d-169">10,50</span><span class="sxs-lookup"><span data-stu-id="ff68d-169">10.50</span></span>     |
| <span data-ttu-id="ff68d-170">50,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-170">50.00</span></span>                  | <span data-ttu-id="ff68d-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ff68d-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="ff68d-172">15,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-172">15.00</span></span>     |
| <span data-ttu-id="ff68d-173">85,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-173">85.00</span></span>                  | <span data-ttu-id="ff68d-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="ff68d-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="ff68d-175">22,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-175">22.00</span></span>     |
| <span data-ttu-id="ff68d-176">305,00</span><span class="sxs-lookup"><span data-stu-id="ff68d-176">305.00</span></span>                 | <span data-ttu-id="ff68d-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="ff68d-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="ff68d-178">45.50</span><span class="sxs-lookup"><span data-stu-id="ff68d-178">45.50</span></span>     |



<span data-ttu-id="ff68d-179">Du kan finde flere oplysninger i [Momssatser baseret på beregningsgrundlaget og felter for beregningsmetoder](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="ff68d-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





