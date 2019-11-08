---
title: Momsberegningsmetoderne i feltet Grundlag
description: I denne artikel beskrives indstillingerne i feltet Grundlag på siden Momskoder, og hvordan momsen beregnes ud fra den valgte indstilling for en momskode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
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
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37bb02dfc9cfcb3e2c1dcda446be3945563d6594
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570574"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="bd694-103">Momsberegningsmetoderne i feltet Grundlag</span><span class="sxs-lookup"><span data-stu-id="bd694-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd694-104">I denne artikel beskrives indstillingerne i feltet Grundlag på siden Momskoder, og hvordan momsen beregnes ud fra den valgte indstilling for en momskode.</span><span class="sxs-lookup"><span data-stu-id="bd694-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="bd694-105">For hver momskode, du opretter på siden Momskoder, skal du vælge den beregningsmåde, der skal anvendes for momsgrundlagsbeløbet i feltet Grundlag.</span><span class="sxs-lookup"><span data-stu-id="bd694-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="bd694-106">Procent af nettobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-106">Percentage of net amount</span></span>
<span data-ttu-id="bd694-107">Procentdelen af metoden til beregning af nettobeløb er standardværdien i feltet Grundlag.</span><span class="sxs-lookup"><span data-stu-id="bd694-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="bd694-108">Momsen beregnes som en procentdel af købs- eller salgsbeløbet eksklusive evt. andre omsætningsafgifter.</span><span class="sxs-lookup"><span data-stu-id="bd694-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="bd694-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bd694-109">Example</span></span>

<span data-ttu-id="bd694-110">Momssatsen er 25 %.</span><span class="sxs-lookup"><span data-stu-id="bd694-110">The tax rate is 25%.</span></span> <span data-ttu-id="bd694-111">Fakturalinjen viser et antal på 10 varer til en stykpris på 1,00, og kunden får en linjerabat på 10 %.</span><span class="sxs-lookup"><span data-stu-id="bd694-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="bd694-112">Nettobeløbet: (10 x 1,00) -10 % = 9,00 moms: 9,00 x 25 % = 2,25 samlet beløb: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="bd694-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="bd694-113"> Procent af bruttobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-113">Percentage of gross amount</span></span>
<span data-ttu-id="bd694-114">Hvis du vælger beregningsmetoden Procent af bruttobeløb, beregnes momsen som en procent af bruttosalgsbeløbet.</span><span class="sxs-lookup"><span data-stu-id="bd694-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="bd694-115">Bruttobeløbet er nettobeløbet for linjen plus alle afgifter og gebyrer for linjen, bortset fra skatten, hvor Grundlag = Procent af bruttobeløb.</span><span class="sxs-lookup"><span data-stu-id="bd694-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="bd694-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bd694-116">Example</span></span>

<span data-ttu-id="bd694-117">Momsmyndighederne har pålagt en vare specielle afgifter.</span><span class="sxs-lookup"><span data-stu-id="bd694-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="bd694-118">Afgiftsbeløbene føjes til nettobeløbet, før der beregnes moms.</span><span class="sxs-lookup"><span data-stu-id="bd694-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="bd694-119">Anvend følgende momskoder:</span><span class="sxs-lookup"><span data-stu-id="bd694-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="bd694-120">AFGIFT 1 = 10 % ved hjælp af beregningsmetoden Procent af nettobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="bd694-121">AFGIFT 2 = 20 % ved hjælp af beregningsmetoden Procent af nettobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="bd694-122">MOMS = 25 % ved hjælp af beregningsmetoden Procent af bruttobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="bd694-123">Hvis nettobeløbet er 10,00, er AFGIFT 1 1,00 (10,00 x 10 %) og AFGIFT 2 = 2,00 (10,00 x 20 %).</span><span class="sxs-lookup"><span data-stu-id="bd694-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="bd694-124">Beløbene vil være som følger: Bruttobeløb: Nettobeløb + AFGIFT 1-beløb + AFGIFT 2-beløb (10,00 + 1,00 + 2,00) = 13,00 MOMS = 13,00 x 25 % = 3,25 samlede AFGIFTER og MOMS: 1,00 + 2,00 + 3,25 = 6,25 samlet beløb: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="bd694-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="bd694-125">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="bd694-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd694-126">Kun én skattekode til Grundlag = Procentdel af bruttobeløb kan bruges til en transaktion.</span><span class="sxs-lookup"><span data-stu-id="bd694-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="bd694-127">Hvis der bestemmes mere end én momskode for en transaktion, vises der en fejl om, at der ikke kan beregnes moms.</span><span class="sxs-lookup"><span data-stu-id="bd694-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="bd694-128">Procent af moms</span><span class="sxs-lookup"><span data-stu-id="bd694-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="bd694-129">Når du vælger Procent af moms i feltet Grundlag, beregnes momsen som en procent af den moms, der er valgt i feltet Moms på moms.</span><span class="sxs-lookup"><span data-stu-id="bd694-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="bd694-130">Den moms, der er valgt i feltet Moms på moms, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="bd694-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="bd694-131">Den næste moms beregnes derefter på grundlag af det første momsbeløb.</span><span class="sxs-lookup"><span data-stu-id="bd694-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="bd694-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bd694-132">Example</span></span>

<span data-ttu-id="bd694-133">Anvend følgende momskoder:</span><span class="sxs-lookup"><span data-stu-id="bd694-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="bd694-134">AFGIFT 1 = 10 % ved hjælp af metoden Procent af nettobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="bd694-135">AFGIFT 2 = 20 % ved hjælp af metoden Procent af moms med Afgift 1 i feltet Moms på moms</span><span class="sxs-lookup"><span data-stu-id="bd694-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="bd694-136">MOMS = 25 % ved hjælp af metoden Procent af bruttobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="bd694-137">Nettobeløb: 10,00 AFGIFT 1: 10,00 x 10 % = 1,00 AFGIFT 2: 1,00 x 20 % = 0,20 Bruttobeløb: 10,00 + 1,00 + 0,20 = 11,20 MOMS: 11,20 x 25 % = 2,80 Samlet AFGIFT og MOMS: 1,00 + 0,20 + 2,80 = 4,00 Samlet beløb: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="bd694-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="bd694-138">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="bd694-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd694-139">Moms på moms-beregninger på flere niveauer er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="bd694-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="bd694-140">En moms kan ikke beregnes ud fra en moms, der allerede er beregnet ud fra en anden moms.</span><span class="sxs-lookup"><span data-stu-id="bd694-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="bd694-141">Flere moms på moms-koder på et enkelt niveau kan beregnes for en transaktion.</span><span class="sxs-lookup"><span data-stu-id="bd694-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="bd694-142"> Beløb pr. enhed</span><span class="sxs-lookup"><span data-stu-id="bd694-142">Amount per unit</span></span>
<span data-ttu-id="bd694-143">Når du vælger Beløb pr. enhed i feltet Grundlag, beregnes momsen som et fast beløb pr. enhed, multipliceret med det antal, der er angivet på dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="bd694-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="bd694-144">Der skal vælges en enhed i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="bd694-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="bd694-145">Beløb pr. enhed angives på siden Momskodeværdier.</span><span class="sxs-lookup"><span data-stu-id="bd694-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="bd694-146">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bd694-146">Example</span></span>

<span data-ttu-id="bd694-147">Momskode er sat op som: kr. 1,20 pr. enhed = kasse på salgsfakturalinje 25 kasser med en vare solgt Moms beregnes som 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="bd694-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="bd694-148">**Bemærk!**</span><span class="sxs-lookup"><span data-stu-id="bd694-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd694-149">Hvis transaktionen angives i en anden enhed end den enhed, der er angivet for momskoden, omregnes den automatisk på grundlag af de enhedsomregninger, der er angivet på siden Enhedsomregninger.</span><span class="sxs-lookup"><span data-stu-id="bd694-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="bd694-150"> Beløb pr. enhed, ekstra indstilling</span><span class="sxs-lookup"><span data-stu-id="bd694-150">Amount per unit, additional option</span></span>

<span data-ttu-id="bd694-151">Under fanen Beregning kan du vælge, om moms for et beløb pr. enhed skal beregnes før andre momskoder og føjes til nettobeløbet før andre momskoder, hvis Grundlag = Procent af nettobeløb beregnes.</span><span class="sxs-lookup"><span data-stu-id="bd694-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="bd694-152">Eksempler</span><span class="sxs-lookup"><span data-stu-id="bd694-152">Examples</span></span>

<span data-ttu-id="bd694-153">Antag, at vi beregner 2 momskoder for en transaktion.</span><span class="sxs-lookup"><span data-stu-id="bd694-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="bd694-154">AFGIFT: Grundlag = beløb pr. enhed og en moms, værdien er angivet til 5,00 pr. enhed = styk</span><span class="sxs-lookup"><span data-stu-id="bd694-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="bd694-155">MOMS: Grundlag = som vist i eksemplerne nedenfor, er værdien angivet til 25 %</span><span class="sxs-lookup"><span data-stu-id="bd694-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="bd694-156">Vi sælger 1 styk af en vare til en enhedspris på 10,00</span><span class="sxs-lookup"><span data-stu-id="bd694-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="bd694-157">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="bd694-157">Example 1</span></span>

<span data-ttu-id="bd694-158">MOMS: Grundlag = metoden Procent af bruttobeløb. Indstillingen Beregn før moms har ingen virkning, fordi MOMS beregnes som en procentdel af bruttobeløbet.</span><span class="sxs-lookup"><span data-stu-id="bd694-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="bd694-159">AFGIFT: 1 x 5,00 = 5,00 Bruttobeløb: 10,00 + 5,00 = 15,00 MOMS: 15,00 x 25 % = 3,75 Samlet moms: 5,00 + 3,75 = 8,75 Samlet beløb: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="bd694-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="bd694-160">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="bd694-160">Example 2</span></span>

<span data-ttu-id="bd694-161">MOMS: Grundlag = Procent af nettobeløb. Indstillingen Beregn før moms er ikke valgt til beregning af AFGIFT.</span><span class="sxs-lookup"><span data-stu-id="bd694-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="bd694-162">Nettobeløb: 10,00 AFGIFT: 1 x 5,00 = 5,00 MOMS: 10,00 x 25 % = 2,50 Samlet moms: 5,00 + 2,50 = 7,50 Samlet beløb: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="bd694-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="bd694-163">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="bd694-163">Example 3</span></span>

<span data-ttu-id="bd694-164">MOMS: Grundlag = Procent af nettobeløb. Indstillingen Beregn før moms er valgt til beregning af AFGIFT.</span><span class="sxs-lookup"><span data-stu-id="bd694-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="bd694-165">Nettobeløb: 10,00 AFGIFT: 1 x 5,00 = 5,00 MOMS: (10,00 + 5,00) x 25 % = 3,75 Samlet moms: 5,00 + 3,75 = 8,75 Samlet beløb: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="bd694-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="bd694-166">Eksempel 4</span><span class="sxs-lookup"><span data-stu-id="bd694-166">Example 4</span></span>

<span data-ttu-id="bd694-167">Resultatet af Eksempel 3 og Eksempel 1 er det samme, da der kun er én afgift.</span><span class="sxs-lookup"><span data-stu-id="bd694-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="bd694-168">Antag, at du har to AFGIFTER, og kun én af dem er inkluderet i nettobeløbet for beregning af moms: AFGIFT 1: 5,00, ved hjælp af metoden Beløb pr. enhed og indstillingen Beregn før moms valgt AFGIFT 2: 2,50, ved hjælp af metoden Beløb pr. enhed, og indstillingen Beregn før moms er ikke valgt Moms: 25 %, ved hjælp af metoden Procent af nettobeløb Nettobeløb: 10,00 AFGIFT 1: 1 x 5,00 = 5,00 AFGIFT 2: 1 x 2,50 = 2,50 Nettebeløb, der skal beregnes moms af: 10,00 + 5,00 = 15,00 MOMS: 15,00 x 25 % = 3,75 Samlet moms herunder afgifter: 5,00 + 2,50 + 3,75 = 11,25 Samlet beløb: 10,00 + 11,25 = 21,25 MOMSEN på 25 % beregnes for summen af nettobeløb (10,00) + AFGIFT 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="bd694-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="bd694-169">AFGIFT 2 føjes til afgiftsbeløbet, når momsen er beregnet.</span><span class="sxs-lookup"><span data-stu-id="bd694-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="bd694-170"> Beregnet procent af nettobeløb</span><span class="sxs-lookup"><span data-stu-id="bd694-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="bd694-171">Beregnet procent af nettobeløb håndterer momsberegning forskelligt, afhængigt af indstillingen af parameteren for Beløb inkl. moms for dokumentet eller kladden.</span><span class="sxs-lookup"><span data-stu-id="bd694-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="bd694-172">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="bd694-172">Example 1</span></span>

<span data-ttu-id="bd694-173">Dokument/kladde er angivet til Beløb inkl. moms = Ja Beløb på transaktionslinje: 10,00 Momssats: 25 % Moms: transaktionslinjebeløbet x momssats (10,00 x 25 %) = 2,50 Momsgrundlagsbeløb (oprindelsesbeløb): transaktionslinjebeløbet - moms (10,00 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="bd694-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="bd694-174">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="bd694-174">Example 2</span></span>

<span data-ttu-id="bd694-175">Dokument/kladde er angivet til Beløb inkl. moms = Nej Beløb på transaktionslinje: 10,00 Momssats: 25 % Moms: transaktionslinjebeløbet x momssats / (100 - momssats) (10,00 x 25 %) / (100 % - 25 %) = 3,33 Momsgrundlagsbeløb (oprindelsesbeløb): transaktionslinjebeløbet = 10,00</span><span class="sxs-lookup"><span data-stu-id="bd694-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="bd694-176">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bd694-176">Additional resources</span></span>
--------

[<span data-ttu-id="bd694-177">Bestemmelse af momssatser baseret på beregningsgrundlaget og felter for beregningsmåde</span><span class="sxs-lookup"><span data-stu-id="bd694-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="bd694-178">Indstillinger for beregning af hele beløbet og intervaller for momskoder</span><span class="sxs-lookup"><span data-stu-id="bd694-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



