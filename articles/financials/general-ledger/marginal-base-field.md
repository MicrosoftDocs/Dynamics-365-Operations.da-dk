---
title: "Momssatser baseret på beregningsgrundlaget og beregningsmåderne"
description: "Denne artikel beskriver, hvordan værdierne i felterne Beregningsgrundlag og Beregningsmetode bestemmer momssatserne for salgs- og købstransaktioner."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: e16e91208cdd6c1a5c904fb763454371b02c71fd
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="44a99-103">Momssatser baseret på beregningsgrundlaget og beregningsmåderne</span><span class="sxs-lookup"><span data-stu-id="44a99-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="44a99-104">Denne artikel beskriver, hvordan værdierne i felterne Beregningsgrundlag og Beregningsmetode bestemmer momssatserne for salgs- og købstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="44a99-104">This article explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="44a99-105">Beregningsgrundlaget for oversigtspanelet Beregning på siden Momskoder bestemmer, hvilke beløb der bruges til at plukke passende momssatser fra satserne på siden Momskodeværdier.</span><span class="sxs-lookup"><span data-stu-id="44a99-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="44a99-106">Beløbstype i feltet Beregningsgrundlag i kombination med metoden i feltet Beregning bestemmer logikken, der skal bruges til at finde de korrekte momssatser for en transaktion.</span><span class="sxs-lookup"><span data-stu-id="44a99-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="44a99-107">Forskellige kombinationer af værdier i disse felter resulterer i meget forskellige momsberegninger, som det fremgår af følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="44a99-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="44a99-108">I eksemplerne bruges de værdier for momsinterval, der er defineret for hver momskode på siden Momskodeværdier.</span><span class="sxs-lookup"><span data-stu-id="44a99-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="44a99-109">Du kan åbne denne side ved at klikke på Momskode &gt; Værdier på siden Momskoder.</span><span class="sxs-lookup"><span data-stu-id="44a99-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="44a99-110">Hvis beregningsgrundlaget for en eller flere af dine momskoder er baseret på linjebeløb eller -enheder, skal værdien i feltet Beregningsmåde på siden Finansparametre indstilles til Linje.</span><span class="sxs-lookup"><span data-stu-id="44a99-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="44a99-111"> Nettobeløb pr. linje</span><span class="sxs-lookup"><span data-stu-id="44a99-111">Net amount per line</span></span>
<span data-ttu-id="44a99-112">Vælg denne indstilling for at bestemme momssatser baseret på nettobeløbet for fakturalinjerne, ekskl. andre afgifter.</span><span class="sxs-lookup"><span data-stu-id="44a99-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="44a99-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44a99-113">Example</span></span>

<span data-ttu-id="44a99-114">Momssatserne er defineret i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="44a99-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="44a99-115">Beløbsinterval</span><span class="sxs-lookup"><span data-stu-id="44a99-115">Amount interval</span></span>    | <span data-ttu-id="44a99-116">Momssats</span><span class="sxs-lookup"><span data-stu-id="44a99-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="44a99-117">0-50</span><span class="sxs-lookup"><span data-stu-id="44a99-117">0 - 50</span></span>             | <span data-ttu-id="44a99-118">30 %</span><span class="sxs-lookup"><span data-stu-id="44a99-118">30%</span></span>      |
| <span data-ttu-id="44a99-119">50-100</span><span class="sxs-lookup"><span data-stu-id="44a99-119">50 - 100</span></span>           | <span data-ttu-id="44a99-120">20 %</span><span class="sxs-lookup"><span data-stu-id="44a99-120">20%</span></span>      |
| <span data-ttu-id="44a99-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="44a99-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="44a99-122">10 %</span><span class="sxs-lookup"><span data-stu-id="44a99-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="44a99-123">Den øvre grænse på nul (0) i det sidste interval betyder, at alle beløb, der er højere end 100, er medtaget i intervallet.</span><span class="sxs-lookup"><span data-stu-id="44a99-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="44a99-124">Beregningsgrundlag: **Nettobeløb pr. linje**</span><span class="sxs-lookup"><span data-stu-id="44a99-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="44a99-125">Beregningsmåde: **Interval**</span><span class="sxs-lookup"><span data-stu-id="44a99-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="44a99-126">Du køber 8 lamper, der hver koster 25,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="44a99-127">Nettobeløbet for fakturalinjen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="44a99-128">Momsen beregnes på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="44a99-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="44a99-129">Samlet moms = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00</span><span class="sxs-lookup"><span data-stu-id="44a99-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="44a99-130">Samlet fakturabeløb = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="44a99-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="44a99-131">**Variation**</span><span class="sxs-lookup"><span data-stu-id="44a99-131">**Variation**</span></span> 

<span data-ttu-id="44a99-132">Hvis fakturaen har to linjer og fire varer på hver linje, er nettobeløbet på hver linje 100,00, og momsen beregnes på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="44a99-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="44a99-133">Momslinje 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="44a99-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="44a99-134">Momslinje 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="44a99-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="44a99-135">Moms i alt= 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="44a99-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="44a99-136">Samlet fakturabeløb = 200,00 + 50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="44a99-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="44a99-137"> Nettobeløb pr. enhed</span><span class="sxs-lookup"><span data-stu-id="44a99-137">Net amount per unit</span></span>
<span data-ttu-id="44a99-138">Vælg denne indstilling for at bestemme momssatser baseret på værdien af hver enhed, ekskl. andre afgifter.</span><span class="sxs-lookup"><span data-stu-id="44a99-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="44a99-139">Når et enhedsbaseret beregningsgrundlag vælges, skal også en enhed angives for momskoden.</span><span class="sxs-lookup"><span data-stu-id="44a99-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="44a99-140">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44a99-140">Example</span></span>

<span data-ttu-id="44a99-141">Momssatserne er defineret i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="44a99-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="44a99-142">Beløb</span><span class="sxs-lookup"><span data-stu-id="44a99-142">Amount</span></span>             | <span data-ttu-id="44a99-143">Momssats</span><span class="sxs-lookup"><span data-stu-id="44a99-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="44a99-144">0-50</span><span class="sxs-lookup"><span data-stu-id="44a99-144">0 - 50</span></span>             | <span data-ttu-id="44a99-145">30 %</span><span class="sxs-lookup"><span data-stu-id="44a99-145">30%</span></span>      |
| <span data-ttu-id="44a99-146">50-100</span><span class="sxs-lookup"><span data-stu-id="44a99-146">50 - 100</span></span>           | <span data-ttu-id="44a99-147">20 %</span><span class="sxs-lookup"><span data-stu-id="44a99-147">20%</span></span>      |
| <span data-ttu-id="44a99-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="44a99-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="44a99-149">10 %</span><span class="sxs-lookup"><span data-stu-id="44a99-149">10%</span></span>      |

<span data-ttu-id="44a99-150">Beregningsgrundlag: **Nettobeløb pr. enhed**</span><span class="sxs-lookup"><span data-stu-id="44a99-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="44a99-151">Beregningsmåde: **Hele beløbet**</span><span class="sxs-lookup"><span data-stu-id="44a99-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="44a99-152">Du køber 8 lamper, der hver koster 25,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="44a99-153">Nettobeløbet for fakturalinjen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="44a99-154">Momsen beregnes på følgende måde: Moms pr. enhed = 25,00 x 30 % = 7,50 Samlet moms = 7,50 x 8 enheder = 60,00 Samlet fakturabeløb = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="44a99-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="44a99-155"> Nettobeløb på fakturasaldo</span><span class="sxs-lookup"><span data-stu-id="44a99-155">Net amount of invoice balance</span></span>

<span data-ttu-id="44a99-156">Vælg denne indstilling for at bestemme momssatser ud fra den samlede værdi af fakturaen, ekskl. andre afgifter.</span><span class="sxs-lookup"><span data-stu-id="44a99-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="44a99-157">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44a99-157">Example</span></span>

<span data-ttu-id="44a99-158">Momssatserne er defineret i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="44a99-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="44a99-159">Beløb</span><span class="sxs-lookup"><span data-stu-id="44a99-159">Amount</span></span>            | <span data-ttu-id="44a99-160">Momssats</span><span class="sxs-lookup"><span data-stu-id="44a99-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="44a99-161">0-50</span><span class="sxs-lookup"><span data-stu-id="44a99-161">0 - 50</span></span>            | <span data-ttu-id="44a99-162">30 %</span><span class="sxs-lookup"><span data-stu-id="44a99-162">30%</span></span>      |
| <span data-ttu-id="44a99-163">50-100</span><span class="sxs-lookup"><span data-stu-id="44a99-163">50 - 100</span></span>          | <span data-ttu-id="44a99-164">20 %</span><span class="sxs-lookup"><span data-stu-id="44a99-164">20%</span></span>      |
| <span data-ttu-id="44a99-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="44a99-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="44a99-166">10 %</span><span class="sxs-lookup"><span data-stu-id="44a99-166">10%</span></span>      |

<span data-ttu-id="44a99-167">Beregningsgrundlag: **Nettobeløb på fakturasaldo**</span><span class="sxs-lookup"><span data-stu-id="44a99-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="44a99-168">Beregningsmåde: **Interval** En salgsfaktura har 2 linjer med 4 lamper på hver linje til 25,00 pr. stk.</span><span class="sxs-lookup"><span data-stu-id="44a99-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="44a99-169">Fakturasaldoens nettobeløb er 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="44a99-170">Momsen beregnes på følgende måde: Samlet moms = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Samlet fakturabeløb = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="44a99-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="44a99-171"> Bruttobeløb pr. linje</span><span class="sxs-lookup"><span data-stu-id="44a99-171">Gross amount per line</span></span>

<span data-ttu-id="44a99-172">Vælg denne indstilling for at bestemme momssatser ud fra værdien af linjen, inkl. alle andre afgifter for linjen.</span><span class="sxs-lookup"><span data-stu-id="44a99-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="44a99-173">I en momsgruppe kan du kun have én momskode med dette valg i feltet Beregningsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="44a99-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="44a99-174">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44a99-174">Example</span></span>

<span data-ttu-id="44a99-175">Momssatserne er defineret i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="44a99-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="44a99-176">Beløb</span><span class="sxs-lookup"><span data-stu-id="44a99-176">Amount</span></span>             | <span data-ttu-id="44a99-177">Momssats</span><span class="sxs-lookup"><span data-stu-id="44a99-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="44a99-178">0-50</span><span class="sxs-lookup"><span data-stu-id="44a99-178">0 - 50</span></span>             | <span data-ttu-id="44a99-179">30 %</span><span class="sxs-lookup"><span data-stu-id="44a99-179">30%</span></span>      |
| <span data-ttu-id="44a99-180">50-100</span><span class="sxs-lookup"><span data-stu-id="44a99-180">50 - 100</span></span>           | <span data-ttu-id="44a99-181">20 %</span><span class="sxs-lookup"><span data-stu-id="44a99-181">20%</span></span>      |
| <span data-ttu-id="44a99-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="44a99-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="44a99-183">10 %</span><span class="sxs-lookup"><span data-stu-id="44a99-183">10%</span></span>      |

<span data-ttu-id="44a99-184">Beregningsgrundlag: **Bruttobeløb pr. linje** Beregningsmåde: **Interval** Der er desuden en anden momskode, der beregnes for en særlig afgift på 5,00 på hver lampe.</span><span class="sxs-lookup"><span data-stu-id="44a99-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is an other tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="44a99-185">Afgiften lægges til nettobeløbet før momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="44a99-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="44a99-186">Du køber 8 lamper, der hver koster 25,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="44a99-187">Nettobeløbet for fakturalinjen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="44a99-188">Bruttobeløbet for fakturalinjen er 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="44a99-189">Momsen beregnes på følgende måde: Samlet moms = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="44a99-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="44a99-190">**Variation**</span><span class="sxs-lookup"><span data-stu-id="44a99-190">**Variation**</span></span> 

<span data-ttu-id="44a99-191">Hvis fakturaen oprettes ved hjælp af 2 fakturalinjer med 4 varer på hver linje, er nettobeløbet pr. fakturalinje 100.</span><span class="sxs-lookup"><span data-stu-id="44a99-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="44a99-192">Bruttobeløb (inklusive afgift på 4 x 5,00) pr. fakturalinje er 120,00, og momsen beregnes på følgende måde: Moms for fakturalinje 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Moms for fakturalinje 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Samlet moms = 27,00 + 27,00 = 54,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="44a99-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="44a99-193"> Bruttobeløb pr. enhed</span><span class="sxs-lookup"><span data-stu-id="44a99-193">Gross amount per unit</span></span>

<span data-ttu-id="44a99-194">Vælg denne indstilling for at bestemme momssatser baseret på værdien af enheden, inkl. andre afgifter.</span><span class="sxs-lookup"><span data-stu-id="44a99-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="44a99-195">I en momsgruppe kan du kun have én momskode med dette valg i feltet Beregningsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="44a99-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="44a99-196">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44a99-196">Example</span></span>

<span data-ttu-id="44a99-197">Momssatserne er defineret i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="44a99-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="44a99-198">Beløb</span><span class="sxs-lookup"><span data-stu-id="44a99-198">Amount</span></span>             | <span data-ttu-id="44a99-199">Momssats</span><span class="sxs-lookup"><span data-stu-id="44a99-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="44a99-200">0-50</span><span class="sxs-lookup"><span data-stu-id="44a99-200">0 - 50</span></span>             | <span data-ttu-id="44a99-201">30 %</span><span class="sxs-lookup"><span data-stu-id="44a99-201">30%</span></span>      |
| <span data-ttu-id="44a99-202">50-100</span><span class="sxs-lookup"><span data-stu-id="44a99-202">50 - 100</span></span>           | <span data-ttu-id="44a99-203">20 %</span><span class="sxs-lookup"><span data-stu-id="44a99-203">20%</span></span>      |
| <span data-ttu-id="44a99-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="44a99-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="44a99-205">10 %</span><span class="sxs-lookup"><span data-stu-id="44a99-205">10%</span></span>      |

<span data-ttu-id="44a99-206">Beregningsgrundlag: **Bruttobeløb pr. enhed** Der er en særlig afgift på 5,00 på hver lampe.</span><span class="sxs-lookup"><span data-stu-id="44a99-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="44a99-207">Afgiften lægges til nettobeløbet før momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="44a99-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="44a99-208">Du køber 8 lamper, der hver koster 25,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="44a99-209">Bruttobeløb pr. enhed er 30,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="44a99-210">Momsen beregnes på følgende måde: Moms pr. enhed = 30 x 30 % = 9,00 Samlet moms = 9,00 x 8 = 72,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="44a99-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="44a99-211"> Fakturatotal inkl. andre momsbeløb</span><span class="sxs-lookup"><span data-stu-id="44a99-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="44a99-212">Vælg denne indstilling for at bestemme momssatser ud fra den samlede værdi af fakturaen, inkl. andre afgifter.</span><span class="sxs-lookup"><span data-stu-id="44a99-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="44a99-213">I en momsgruppe kan du kun have én momskode med dette valg i feltet Beregningsgrundlag</span><span class="sxs-lookup"><span data-stu-id="44a99-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="44a99-214">Eksempel</span><span class="sxs-lookup"><span data-stu-id="44a99-214">Example</span></span>

<span data-ttu-id="44a99-215">Momssatserne er defineret i følgende intervaller.</span><span class="sxs-lookup"><span data-stu-id="44a99-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="44a99-216">Beløb</span><span class="sxs-lookup"><span data-stu-id="44a99-216">Amount</span></span>             | <span data-ttu-id="44a99-217">Momssats</span><span class="sxs-lookup"><span data-stu-id="44a99-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="44a99-218">0-50</span><span class="sxs-lookup"><span data-stu-id="44a99-218">0 - 50</span></span>             | <span data-ttu-id="44a99-219">30 %</span><span class="sxs-lookup"><span data-stu-id="44a99-219">30%</span></span>      |
| <span data-ttu-id="44a99-220">50-100</span><span class="sxs-lookup"><span data-stu-id="44a99-220">50 - 100</span></span>           | <span data-ttu-id="44a99-221">20 %</span><span class="sxs-lookup"><span data-stu-id="44a99-221">20%</span></span>      |
| <span data-ttu-id="44a99-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="44a99-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="44a99-223">10 %</span><span class="sxs-lookup"><span data-stu-id="44a99-223">10%</span></span>      |

<span data-ttu-id="44a99-224">Beregningsgrundlag: **Fakturatotal inkl. andre momsbeløb** Beregningsmåde: **Interval** </span><span class="sxs-lookup"><span data-stu-id="44a99-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="44a99-225">Der er en særlig afgift på hver lampe på 5,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="44a99-226">Afgiften lægges til nettobeløbet før momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="44a99-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="44a99-227">Du køber 8 lamper, der hver koster 25,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="44a99-228">Nettobeløbet for fakturaen er 200,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="44a99-229">Bruttobeløbet for fakturaen er 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="44a99-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="44a99-230">Momsen beregnes på følgende måde: Samlet moms = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Samlet afgift = 5,00 x 8 = 40,00 Samlet fakturabeløb = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="44a99-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="44a99-231">Du kan finde flere oplysninger under [Indstillinger for beregning af hele beløbet og intervaller for momskoder](whole-amount-interval-options-sales-tax-codes.md) og [Momsberegningsmetoderne i feltet Grundlag](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="44a99-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>




