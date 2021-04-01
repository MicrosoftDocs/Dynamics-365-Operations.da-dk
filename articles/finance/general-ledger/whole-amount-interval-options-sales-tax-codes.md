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
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0414f835b7797d2ed554f8d9dbd95b2ad47bba43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234111"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="0b947-103">Indstillinger for beregning af hele beløbet og intervaller for momskoder</span><span class="sxs-lookup"><span data-stu-id="0b947-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b947-104">I denne artikel beskrives indstillingerne for feltet Beregningsmåde for momskoder, og hvordan der beregnes moms for intervaller og hele beløb.</span><span class="sxs-lookup"><span data-stu-id="0b947-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="0b947-105">Du kan konfigurere, at en momskode skal beregnes på grundlag af hele beløbet eller et intervalbeløb.</span><span class="sxs-lookup"><span data-stu-id="0b947-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="0b947-106">På siden Momskoder skal du bruge feltet Beregningsmåde på oversigtspanelet Beregning til at vælge, hvordan en momskode skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="0b947-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="0b947-107">Hele beløb – En momssats anvendes på hele det momspligtige beløb.</span><span class="sxs-lookup"><span data-stu-id="0b947-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="0b947-108">Interval – Det momspligtige beløb er opdelt i dele, hvor hver del ligger inden for et beløbsinterval, der er underlagt en bestemt momssats.</span><span class="sxs-lookup"><span data-stu-id="0b947-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="0b947-109">Den del af beløbet, der ligger inden for et bestemt interval, pålægges moms i henhold til momssatsen for dette interval.</span><span class="sxs-lookup"><span data-stu-id="0b947-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="0b947-110">Momsen er summen af de momsbeløb, der beregnes for hvert beløbsinterval.</span><span class="sxs-lookup"><span data-stu-id="0b947-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="0b947-111">Indstillingen Interval er kun tilgængelig, når du vælger Linje i en feltet Beregningsmåde i området Moms på siden Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="0b947-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="0b947-112">Du angiver Intervaller på siden Momskodeværdier ved at angive minimum- og maksimumgrænsebeløb pr. momssats.</span><span class="sxs-lookup"><span data-stu-id="0b947-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="0b947-113">For moms, der skal beregnes af alle momspligtige beløb, uanset den valgte beregningsmetode, skal intervallerne overholde følgende regler:</span><span class="sxs-lookup"><span data-stu-id="0b947-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="0b947-114">Første interval skal have en minimumgrænse på nul.</span><span class="sxs-lookup"><span data-stu-id="0b947-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="0b947-115">Det sidste interval, der skal have en maksimumgrænse på nul, angiver uendeligt.</span><span class="sxs-lookup"><span data-stu-id="0b947-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="0b947-116">Maksimumgrænsen for alle intervaller er minimumgrænsen for det næste interval.</span><span class="sxs-lookup"><span data-stu-id="0b947-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="0b947-117">Hvis et beløb er maksimumgrænsen for det forrige interval og minimumgrænsen for det næste interval, gælder momssatsen for det første interval for beløbet.</span><span class="sxs-lookup"><span data-stu-id="0b947-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="0b947-118">Hvis et beløb ligger uden for de intervaller, der er defineret af de øvre og nedre grænser, anvendes momssatsen 0.</span><span class="sxs-lookup"><span data-stu-id="0b947-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="0b947-119">Eksempel: Beregningsmåden er hele beløbet</span><span class="sxs-lookup"><span data-stu-id="0b947-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="0b947-120">På siden Momskodeværdier er momssatserne defineret i følgende intervaller i:</span><span class="sxs-lookup"><span data-stu-id="0b947-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="0b947-121">**Minimumsgrænse**</span><span class="sxs-lookup"><span data-stu-id="0b947-121">**Minimum limit**</span></span> | <span data-ttu-id="0b947-122">**Maksimumgrænse**</span><span class="sxs-lookup"><span data-stu-id="0b947-122">**Maximum limit**</span></span> | <span data-ttu-id="0b947-123">**Momssats**</span><span class="sxs-lookup"><span data-stu-id="0b947-123">**Tax rate**</span></span> |
| <span data-ttu-id="0b947-124">0,00</span><span class="sxs-lookup"><span data-stu-id="0b947-124">0.00</span></span>              | <span data-ttu-id="0b947-125">50,00</span><span class="sxs-lookup"><span data-stu-id="0b947-125">50.00</span></span>             | <span data-ttu-id="0b947-126">30 %</span><span class="sxs-lookup"><span data-stu-id="0b947-126">30%</span></span>          |
| <span data-ttu-id="0b947-127">50,00</span><span class="sxs-lookup"><span data-stu-id="0b947-127">50.00</span></span>             | <span data-ttu-id="0b947-128">100,00</span><span class="sxs-lookup"><span data-stu-id="0b947-128">100.00</span></span>            | <span data-ttu-id="0b947-129">20 %</span><span class="sxs-lookup"><span data-stu-id="0b947-129">20%</span></span>          |
| <span data-ttu-id="0b947-130">100,00</span><span class="sxs-lookup"><span data-stu-id="0b947-130">100.00</span></span>            | <span data-ttu-id="0b947-131">0,00</span><span class="sxs-lookup"><span data-stu-id="0b947-131">0.00</span></span>              | <span data-ttu-id="0b947-132">10 %</span><span class="sxs-lookup"><span data-stu-id="0b947-132">10%</span></span>          |

<span data-ttu-id="0b947-133">Momsen beregnes af hele det momspligtige beløb.</span><span class="sxs-lookup"><span data-stu-id="0b947-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="0b947-134">Momspligtigt beløb (pris)</span><span class="sxs-lookup"><span data-stu-id="0b947-134">Taxable amount (price)</span></span> | <span data-ttu-id="0b947-135">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="0b947-135">Calculation</span></span>    | <span data-ttu-id="0b947-136">Moms</span><span class="sxs-lookup"><span data-stu-id="0b947-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="0b947-137">35,00</span><span class="sxs-lookup"><span data-stu-id="0b947-137">35.00</span></span>                  | <span data-ttu-id="0b947-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="0b947-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="0b947-139">10,50</span><span class="sxs-lookup"><span data-stu-id="0b947-139">10.50</span></span>     |
| <span data-ttu-id="0b947-140">50,00</span><span class="sxs-lookup"><span data-stu-id="0b947-140">50.00</span></span>                  | <span data-ttu-id="0b947-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="0b947-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="0b947-142">15,00</span><span class="sxs-lookup"><span data-stu-id="0b947-142">15.00</span></span>     |
| <span data-ttu-id="0b947-143">85,00</span><span class="sxs-lookup"><span data-stu-id="0b947-143">85.00</span></span>                  | <span data-ttu-id="0b947-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="0b947-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="0b947-145">17,00</span><span class="sxs-lookup"><span data-stu-id="0b947-145">17.00</span></span>     |
| <span data-ttu-id="0b947-146">305,00</span><span class="sxs-lookup"><span data-stu-id="0b947-146">305.00</span></span>                 | <span data-ttu-id="0b947-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="0b947-147">305.00 \* 0.10</span></span> | <span data-ttu-id="0b947-148">30,50</span><span class="sxs-lookup"><span data-stu-id="0b947-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="0b947-149">Eksempel: Beregningsmåde er interval</span><span class="sxs-lookup"><span data-stu-id="0b947-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="0b947-150">På siden Værdier er momssatserne defineret i følgende intervaller:</span><span class="sxs-lookup"><span data-stu-id="0b947-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="0b947-151">**Minimumsgrænse**</span><span class="sxs-lookup"><span data-stu-id="0b947-151">**Minimum limit**</span></span> | <span data-ttu-id="0b947-152">**Maksimumgrænse**</span><span class="sxs-lookup"><span data-stu-id="0b947-152">**Maximum limit**</span></span> | <span data-ttu-id="0b947-153">**Momssats**</span><span class="sxs-lookup"><span data-stu-id="0b947-153">**Tax rate**</span></span> |
| <span data-ttu-id="0b947-154">0,00</span><span class="sxs-lookup"><span data-stu-id="0b947-154">0.00</span></span>              | <span data-ttu-id="0b947-155">50,00</span><span class="sxs-lookup"><span data-stu-id="0b947-155">50.00</span></span>             | <span data-ttu-id="0b947-156">30 %</span><span class="sxs-lookup"><span data-stu-id="0b947-156">30%</span></span>          |
| <span data-ttu-id="0b947-157">50,00</span><span class="sxs-lookup"><span data-stu-id="0b947-157">50.00</span></span>             | <span data-ttu-id="0b947-158">100,00</span><span class="sxs-lookup"><span data-stu-id="0b947-158">100.00</span></span>            | <span data-ttu-id="0b947-159">20 %</span><span class="sxs-lookup"><span data-stu-id="0b947-159">20%</span></span>          |
| <span data-ttu-id="0b947-160">100,00</span><span class="sxs-lookup"><span data-stu-id="0b947-160">100.00</span></span>            | <span data-ttu-id="0b947-161">0,00</span><span class="sxs-lookup"><span data-stu-id="0b947-161">0.00</span></span>              | <span data-ttu-id="0b947-162">10 %</span><span class="sxs-lookup"><span data-stu-id="0b947-162">10%</span></span>          |

<span data-ttu-id="0b947-163">Momsen er summen af de momsbeløb, der beregnes for hvert beløbsinterval.</span><span class="sxs-lookup"><span data-stu-id="0b947-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="0b947-164">Momspligtigt beløb (pris)</span><span class="sxs-lookup"><span data-stu-id="0b947-164">Taxable amount (price)</span></span> | <span data-ttu-id="0b947-165">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="0b947-165">Calculation</span></span>                                                               | <span data-ttu-id="0b947-166">Moms</span><span class="sxs-lookup"><span data-stu-id="0b947-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0b947-167">35,00</span><span class="sxs-lookup"><span data-stu-id="0b947-167">35.00</span></span>                  | <span data-ttu-id="0b947-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="0b947-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="0b947-169">10,50</span><span class="sxs-lookup"><span data-stu-id="0b947-169">10.50</span></span>     |
| <span data-ttu-id="0b947-170">50,00</span><span class="sxs-lookup"><span data-stu-id="0b947-170">50.00</span></span>                  | <span data-ttu-id="0b947-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="0b947-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="0b947-172">15,00</span><span class="sxs-lookup"><span data-stu-id="0b947-172">15.00</span></span>     |
| <span data-ttu-id="0b947-173">85,00</span><span class="sxs-lookup"><span data-stu-id="0b947-173">85.00</span></span>                  | <span data-ttu-id="0b947-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="0b947-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="0b947-175">22,00</span><span class="sxs-lookup"><span data-stu-id="0b947-175">22.00</span></span>     |
| <span data-ttu-id="0b947-176">305,00</span><span class="sxs-lookup"><span data-stu-id="0b947-176">305.00</span></span>                 | <span data-ttu-id="0b947-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="0b947-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="0b947-178">45.50</span><span class="sxs-lookup"><span data-stu-id="0b947-178">45.50</span></span>     |



<span data-ttu-id="0b947-179">Du kan finde flere oplysninger i [Momssatser baseret på beregningsgrundlaget og felter for beregningsmetoder](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="0b947-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]