---
title: Beregning af fast omkostning
description: I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 936e54c0ef1de449afda2392cd1fbb304eed631b
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="5ec50-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5ec50-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5ec50-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="5ec50-105">Term definition</span></span>
---------------

<span data-ttu-id="5ec50-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="5ec50-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5ec50-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="5ec50-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5ec50-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="5ec50-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5ec50-109">Leje</span><span class="sxs-lookup"><span data-stu-id="5ec50-109">Rent</span></span>
-   <span data-ttu-id="5ec50-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-110">Electricity</span></span>
-   <span data-ttu-id="5ec50-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="5ec50-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5ec50-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-112">Overhead calculation overview</span></span>
<span data-ttu-id="5ec50-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="5ec50-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5ec50-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="5ec50-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5ec50-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="5ec50-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5ec50-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5ec50-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5ec50-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5ec50-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5ec50-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="5ec50-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5ec50-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="5ec50-119">Version type</span></span>
-   <span data-ttu-id="5ec50-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="5ec50-120">Date and time</span></span>
-   <span data-ttu-id="5ec50-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="5ec50-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5ec50-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5ec50-122">Fiscal year</span></span>
-   <span data-ttu-id="5ec50-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="5ec50-123">Fiscal period</span></span>

<span data-ttu-id="5ec50-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="5ec50-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5ec50-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="5ec50-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5ec50-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="5ec50-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5ec50-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="5ec50-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5ec50-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5ec50-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5ec50-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="5ec50-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5ec50-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="5ec50-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5ec50-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5ec50-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5ec50-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5ec50-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5ec50-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5ec50-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="5ec50-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5ec50-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="5ec50-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5ec50-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="5ec50-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5ec50-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="5ec50-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="5ec50-140">Main account</span></span></th>
<th><span data-ttu-id="5ec50-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="5ec50-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5ec50-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-143">CC099</span></span></td>
<td><span data-ttu-id="5ec50-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-144">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-145">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-145">10001</span></span></td>
<td><span data-ttu-id="5ec50-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-146">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5ec50-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="5ec50-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5ec50-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="5ec50-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5ec50-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="5ec50-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5ec50-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5ec50-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="5ec50-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5ec50-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5ec50-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="5ec50-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5ec50-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="5ec50-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5ec50-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5ec50-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="5ec50-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5ec50-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="5ec50-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5ec50-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-160">Journal</span></span></th>
<th><span data-ttu-id="5ec50-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5ec50-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ec50-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5ec50-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ec50-163">Version</span><span class="sxs-lookup"><span data-stu-id="5ec50-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-164">00001</span><span class="sxs-lookup"><span data-stu-id="5ec50-164">00001</span></span></td>
<td><span data-ttu-id="5ec50-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5ec50-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5ec50-166">Fiscal</span></span></td>
<td><span data-ttu-id="5ec50-167">2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-167">2017</span></span></td>
<td><span data-ttu-id="5ec50-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5ec50-168">Period 1</span></span></td>
<td><span data-ttu-id="5ec50-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ec50-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="5ec50-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-173">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5ec50-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-177">CC099</span></span></td>
<td><span data-ttu-id="5ec50-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-178">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-179">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-179">10001</span></span></td>
<td><span data-ttu-id="5ec50-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-180">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5ec50-181">Unclassified</span></span></td>
<td><span data-ttu-id="5ec50-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ec50-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5ec50-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-185">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-187">Amount</span></span></th>
<th><span data-ttu-id="5ec50-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-189">CC099</span></span></td>
<td><span data-ttu-id="5ec50-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-190">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-191">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-191">10001</span></span></td>
<td><span data-ttu-id="5ec50-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-192">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5ec50-193">Unclassified</span></span></td>
<td><span data-ttu-id="5ec50-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-194">10,000.00</span></span></td>
<td><span data-ttu-id="5ec50-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-196">CC099</span></span></td>
<td><span data-ttu-id="5ec50-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-197">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-198">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-198">10001</span></span></td>
<td><span data-ttu-id="5ec50-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-199">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5ec50-200">Unclassified</span></span></td>
<td><span data-ttu-id="5ec50-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5ec50-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-203">CC099</span></span></td>
<td><span data-ttu-id="5ec50-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-204">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-205">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-205">10001</span></span></td>
<td><span data-ttu-id="5ec50-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-206">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-208">1,000.00</span></span></td>
<td><span data-ttu-id="5ec50-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-210">CC099</span></span></td>
<td><span data-ttu-id="5ec50-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-211">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-212">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-212">10001</span></span></td>
<td><span data-ttu-id="5ec50-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-213">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-214">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-215">9,000.00</span></span></td>
<td><span data-ttu-id="5ec50-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-217">Du kan finde detaljerede oplysninger om funktionalitet af omkostninger under Politik for funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="5ec50-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="5ec50-218">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="5ec50-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5ec50-219">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="5ec50-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5ec50-220">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5ec50-221">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="5ec50-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5ec50-222">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="5ec50-222">Define the cost distribution rule</span></span>

<span data-ttu-id="5ec50-223">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5ec50-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5ec50-224">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="5ec50-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5ec50-225">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5ec50-226">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="5ec50-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5ec50-227">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="5ec50-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5ec50-228">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-229">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-229">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-230">KWh</span><span class="sxs-lookup"><span data-stu-id="5ec50-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-231">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-231">CC001</span></span></td>
<td><span data-ttu-id="5ec50-232">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-232">HR</span></span></td>
<td><span data-ttu-id="5ec50-233">1.000</span><span class="sxs-lookup"><span data-stu-id="5ec50-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-234">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-234">CC002</span></span></td>
<td><span data-ttu-id="5ec50-235">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-235">Finance</span></span></td>
<td><span data-ttu-id="5ec50-236">6.000</span><span class="sxs-lookup"><span data-stu-id="5ec50-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-237">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-237">CC003</span></span></td>
<td><span data-ttu-id="5ec50-238">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-238">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-239">0</span><span class="sxs-lookup"><span data-stu-id="5ec50-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-240">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-241">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-241">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-242">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-242">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-243">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-243">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-244">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-245">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-245">CC001</span></span></td>
<td><span data-ttu-id="5ec50-246">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-246">HR</span></span></td>
<td><span data-ttu-id="5ec50-247">1.000</span><span class="sxs-lookup"><span data-stu-id="5ec50-247">1,000</span></span></td>
<td><span data-ttu-id="5ec50-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ec50-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5ec50-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-250">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-250">CC002</span></span></td>
<td><span data-ttu-id="5ec50-251">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-251">Finance</span></span></td>
<td><span data-ttu-id="5ec50-252">6.000</span><span class="sxs-lookup"><span data-stu-id="5ec50-252">6,000</span></span></td>
<td><span data-ttu-id="5ec50-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ec50-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5ec50-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-255">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-255">CC003</span></span></td>
<td><span data-ttu-id="5ec50-256">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-256">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-257">0</span><span class="sxs-lookup"><span data-stu-id="5ec50-257">0</span></span></td>
<td><span data-ttu-id="5ec50-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ec50-259">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-260">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="5ec50-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5ec50-261">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-262">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-262">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-263">Formel</span><span class="sxs-lookup"><span data-stu-id="5ec50-263">Formula</span></span></th>
<th><span data-ttu-id="5ec50-264">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-264">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-265">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-265">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-266">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-267">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-267">CC001</span></span></td>
<td><span data-ttu-id="5ec50-268">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-268">HR</span></span></td>
<td><span data-ttu-id="5ec50-269">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ec50-270">1</span><span class="sxs-lookup"><span data-stu-id="5ec50-270">1</span></span></td>
<td><span data-ttu-id="5ec50-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ec50-272">500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-273">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-273">CC002</span></span></td>
<td><span data-ttu-id="5ec50-274">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-274">Finance</span></span></td>
<td><span data-ttu-id="5ec50-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ec50-276">1</span><span class="sxs-lookup"><span data-stu-id="5ec50-276">1</span></span></td>
<td><span data-ttu-id="5ec50-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ec50-278">500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-279">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-279">CC003</span></span></td>
<td><span data-ttu-id="5ec50-280">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-280">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ec50-282">0</span><span class="sxs-lookup"><span data-stu-id="5ec50-282">0</span></span></td>
<td><span data-ttu-id="5ec50-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ec50-284">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5ec50-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-286">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-286">Journal</span></span></th>
<th><span data-ttu-id="5ec50-287">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5ec50-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ec50-288">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5ec50-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ec50-289">Version</span><span class="sxs-lookup"><span data-stu-id="5ec50-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-290">00002</span><span class="sxs-lookup"><span data-stu-id="5ec50-290">00002</span></span></td>
<td><span data-ttu-id="5ec50-291">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="5ec50-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5ec50-292">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5ec50-292">Fiscal</span></span></td>
<td><span data-ttu-id="5ec50-293">2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-293">2017</span></span></td>
<td><span data-ttu-id="5ec50-294">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5ec50-294">Period 1</span></span></td>
<td><span data-ttu-id="5ec50-295">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ec50-296">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="5ec50-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-297">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-298">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-299">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-299">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-300">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-300">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-301">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-302">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-303">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-303">CC099</span></span></td>
<td><span data-ttu-id="5ec50-304">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-304">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-305">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-305">10001</span></span></td>
<td><span data-ttu-id="5ec50-306">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-306">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-307">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-307">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-309">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-310">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-310">CC099</span></span></td>
<td><span data-ttu-id="5ec50-311">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-311">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-312">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-312">10001</span></span></td>
<td><span data-ttu-id="5ec50-313">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-313">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-314">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-314">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ec50-316">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5ec50-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-317">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-318">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-318">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-319">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-319">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-320">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-320">Amount</span></span></th>
<th><span data-ttu-id="5ec50-321">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-322">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-322">CC099</span></span></td>
<td><span data-ttu-id="5ec50-323">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-323">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-324">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-324">10001</span></span></td>
<td><span data-ttu-id="5ec50-325">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-325">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-326">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-326">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-327">-1,000.00</span></span></td>
<td><span data-ttu-id="5ec50-328">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-329">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-329">CC001</span></span></td>
<td><span data-ttu-id="5ec50-330">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-330">HR</span></span></td>
<td><span data-ttu-id="5ec50-331">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-331">10001</span></span></td>
<td><span data-ttu-id="5ec50-332">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-332">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-333">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-333">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-334">500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-334">500.00</span></span></td>
<td><span data-ttu-id="5ec50-335">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-336">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-336">CC002</span></span></td>
<td><span data-ttu-id="5ec50-337">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-337">Finance</span></span></td>
<td><span data-ttu-id="5ec50-338">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-338">10001</span></span></td>
<td><span data-ttu-id="5ec50-339">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-339">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-340">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-340">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-341">500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-341">500.00</span></span></td>
<td><span data-ttu-id="5ec50-342">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-343">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-343">CC099</span></span></td>
<td><span data-ttu-id="5ec50-344">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5ec50-344">Default cost center</span></span></td>
<td><span data-ttu-id="5ec50-345">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-345">10001</span></span></td>
<td><span data-ttu-id="5ec50-346">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-346">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-347">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-347">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-348">-9,000.00</span></span></td>
<td><span data-ttu-id="5ec50-349">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-350">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-350">CC001</span></span></td>
<td><span data-ttu-id="5ec50-351">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-351">HR</span></span></td>
<td><span data-ttu-id="5ec50-352">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-352">10001</span></span></td>
<td><span data-ttu-id="5ec50-353">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-353">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-354">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-354">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5ec50-355">1,285.71</span></span></td>
<td><span data-ttu-id="5ec50-356">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-357">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-357">CC002</span></span></td>
<td><span data-ttu-id="5ec50-358">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-358">Finance</span></span></td>
<td><span data-ttu-id="5ec50-359">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-359">10001</span></span></td>
<td><span data-ttu-id="5ec50-360">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-360">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-361">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-361">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5ec50-362">7,714.29</span></span></td>
<td><span data-ttu-id="5ec50-363">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-364">Du kan finde detaljerede oplysninger om omkostningsfordeling og fordelingsgrundlag under Politik for omkostningsfordeling og Fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="5ec50-365">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="5ec50-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5ec50-366">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="5ec50-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5ec50-367">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5ec50-368">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5ec50-369">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="5ec50-369">Define the overhead rate</span></span>

<span data-ttu-id="5ec50-370">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5ec50-371">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5ec50-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-372">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-372">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-373">Timer</span><span class="sxs-lookup"><span data-stu-id="5ec50-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-374">Proj 1</span></span></td>
<td><span data-ttu-id="5ec50-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-375">Project 1</span></span></td>
<td><span data-ttu-id="5ec50-376">3</span><span class="sxs-lookup"><span data-stu-id="5ec50-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-377">Proj 2</span></span></td>
<td><span data-ttu-id="5ec50-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-378">Project 2</span></span></td>
<td><span data-ttu-id="5ec50-379">1</span><span class="sxs-lookup"><span data-stu-id="5ec50-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-380">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="5ec50-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-381">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-381">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-382">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-382">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-383">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-383">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-384">Enheder</span><span class="sxs-lookup"><span data-stu-id="5ec50-384">Units</span></span></th>
<th><span data-ttu-id="5ec50-385">Kurs</span><span class="sxs-lookup"><span data-stu-id="5ec50-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-386">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-386">CC001</span></span></td>
<td><span data-ttu-id="5ec50-387">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-387">HR</span></span></td>
<td><span data-ttu-id="5ec50-388">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-388">10001</span></span></td>
<td><span data-ttu-id="5ec50-389">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-389">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-390">1</span><span class="sxs-lookup"><span data-stu-id="5ec50-390">1</span></span></td>
<td><span data-ttu-id="5ec50-391">10</span><span class="sxs-lookup"><span data-stu-id="5ec50-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-392">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-393">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-393">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-394">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-394">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-395">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-395">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-396">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-396">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-397">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-398">Proj 1</span></span></td>
<td><span data-ttu-id="5ec50-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-399">Project 1</span></span></td>
<td><span data-ttu-id="5ec50-400">3</span><span class="sxs-lookup"><span data-stu-id="5ec50-400">3</span></span></td>
<td><span data-ttu-id="5ec50-401">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-401">10001</span></span></td>
<td><span data-ttu-id="5ec50-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5ec50-403">30,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-404">Proj 2</span></span></td>
<td><span data-ttu-id="5ec50-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-405">Project 2</span></span></td>
<td><span data-ttu-id="5ec50-406">1</span><span class="sxs-lookup"><span data-stu-id="5ec50-406">1</span></span></td>
<td><span data-ttu-id="5ec50-407">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-407">10001</span></span></td>
<td><span data-ttu-id="5ec50-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5ec50-409">10,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5ec50-410">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-411">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-411">Journal</span></span></th>
<th><span data-ttu-id="5ec50-412">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5ec50-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ec50-413">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5ec50-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ec50-414">Version</span><span class="sxs-lookup"><span data-stu-id="5ec50-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-415">00003</span><span class="sxs-lookup"><span data-stu-id="5ec50-415">00003</span></span></td>
<td><span data-ttu-id="5ec50-416">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="5ec50-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5ec50-417">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5ec50-417">Fiscal</span></span></td>
<td><span data-ttu-id="5ec50-418">2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-418">2017</span></span></td>
<td><span data-ttu-id="5ec50-419">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5ec50-419">Period 1</span></span></td>
<td><span data-ttu-id="5ec50-420">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5ec50-421">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="5ec50-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-422">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-423">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-423">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-424">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-425">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-426">Proj 1</span></span></td>
<td><span data-ttu-id="5ec50-427">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5ec50-428">3,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-429">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-430">Proj 2</span></span></td>
<td><span data-ttu-id="5ec50-431">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5ec50-432">1,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ec50-433">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5ec50-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-434">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-435">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-435">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-436">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-436">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-437">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-437">Amount</span></span></th>
<th><span data-ttu-id="5ec50-438">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="5ec50-439">CC0001</span></span></td>
<td><span data-ttu-id="5ec50-440">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-440">HR</span></span></td>
<td><span data-ttu-id="5ec50-441">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-441">10001</span></span></td>
<td><span data-ttu-id="5ec50-442">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-442">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-443">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-443">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-444">-30.00</span></span></td>
<td><span data-ttu-id="5ec50-445">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-446">Proj 1</span></span></td>
<td><span data-ttu-id="5ec50-447">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5ec50-448">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-448">10001</span></span></td>
<td><span data-ttu-id="5ec50-449">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-449">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-450">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-450">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-451">30,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-451">30.00</span></span></td>
<td><span data-ttu-id="5ec50-452">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-453">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-453">CC001</span></span></td>
<td><span data-ttu-id="5ec50-454">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-454">HR</span></span></td>
<td><span data-ttu-id="5ec50-455">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-455">10001</span></span></td>
<td><span data-ttu-id="5ec50-456">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-456">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-457">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-457">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-458">-10.00</span></span></td>
<td><span data-ttu-id="5ec50-459">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-460">Proj 2</span></span></td>
<td><span data-ttu-id="5ec50-461">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5ec50-462">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-462">10001</span></span></td>
<td><span data-ttu-id="5ec50-463">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-463">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-464">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-464">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-465">10,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-465">10.00</span></span></td>
<td><span data-ttu-id="5ec50-466">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-467">Detaljerede oplysninger om politik for satser for faste omkostninger finder du i Politik for sats for faste omkostninger og Fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="5ec50-468">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="5ec50-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5ec50-469">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="5ec50-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5ec50-470">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5ec50-471">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="5ec50-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="5ec50-472">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="5ec50-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5ec50-473">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="5ec50-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5ec50-474">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5ec50-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5ec50-475">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="5ec50-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5ec50-476">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="5ec50-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5ec50-477">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5ec50-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5ec50-478">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="5ec50-478">Define the cost allocation</span></span>

<span data-ttu-id="5ec50-479">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5ec50-480">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5ec50-481">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5ec50-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-482">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-482">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-483">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="5ec50-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-484">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-484">CC002</span></span></td>
<td><span data-ttu-id="5ec50-485">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-485">Finance</span></span></td>
<td><span data-ttu-id="5ec50-486">35</span><span class="sxs-lookup"><span data-stu-id="5ec50-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-487">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-487">CC003</span></span></td>
<td><span data-ttu-id="5ec50-488">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-488">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-489">55</span><span class="sxs-lookup"><span data-stu-id="5ec50-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-490">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-490">CC004</span></span></td>
<td><span data-ttu-id="5ec50-491">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-491">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-492">10</span><span class="sxs-lookup"><span data-stu-id="5ec50-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-493">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5ec50-494">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5ec50-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-495">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-495">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-496">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="5ec50-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-497">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-497">CC003</span></span></td>
<td><span data-ttu-id="5ec50-498">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-498">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-499">65</span><span class="sxs-lookup"><span data-stu-id="5ec50-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-500">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-500">CC004</span></span></td>
<td><span data-ttu-id="5ec50-501">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-501">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-502">35</span><span class="sxs-lookup"><span data-stu-id="5ec50-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-503">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5ec50-504">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5ec50-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-505">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-505">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-506">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="5ec50-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-507">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-508">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-509">60</span><span class="sxs-lookup"><span data-stu-id="5ec50-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-510">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-511">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-512">20</span><span class="sxs-lookup"><span data-stu-id="5ec50-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-513">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5ec50-514">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5ec50-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-515">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-515">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-516">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="5ec50-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-517">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-518">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-519">80</span><span class="sxs-lookup"><span data-stu-id="5ec50-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-520">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-521">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-522">15</span><span class="sxs-lookup"><span data-stu-id="5ec50-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-523">**Bemærk!** I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="5ec50-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5ec50-524">Du kan finde mere detaljerede oplysninger om providere af statistiske målinger under Skabeloner til providere af statistiske målinger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="5ec50-525">(Bemærk, at dette emne ikke er færdigt endnu, men kommer snart). Tabellen nedenfor viser resultatet, når HR tjenester anvendes som tildelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5ec50-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-526">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-526">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-527">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-527">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-528">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-528">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-529">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-529">Amount</span></span></th>
<th><span data-ttu-id="5ec50-530">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-531">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-531">CC002</span></span></td>
<td><span data-ttu-id="5ec50-532">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-532">Finance</span></span></td>
<td><span data-ttu-id="5ec50-533">35</span><span class="sxs-lookup"><span data-stu-id="5ec50-533">35</span></span></td>
<td><span data-ttu-id="5ec50-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ec50-535">175.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-535">175.00</span></span></td>
<td><span data-ttu-id="5ec50-536">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-537">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-537">CC003</span></span></td>
<td><span data-ttu-id="5ec50-538">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-538">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-539">55</span><span class="sxs-lookup"><span data-stu-id="5ec50-539">55</span></span></td>
<td><span data-ttu-id="5ec50-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ec50-541">275.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-541">275.00</span></span></td>
<td><span data-ttu-id="5ec50-542">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-543">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-543">CC004</span></span></td>
<td><span data-ttu-id="5ec50-544">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-544">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-545">10</span><span class="sxs-lookup"><span data-stu-id="5ec50-545">10</span></span></td>
<td><span data-ttu-id="5ec50-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ec50-547">50,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-547">50.00</span></span></td>
<td><span data-ttu-id="5ec50-548">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-549">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-549">CC002</span></span></td>
<td><span data-ttu-id="5ec50-550">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-550">Finance</span></span></td>
<td><span data-ttu-id="5ec50-551">35</span><span class="sxs-lookup"><span data-stu-id="5ec50-551">35</span></span></td>
<td><span data-ttu-id="5ec50-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ec50-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ec50-553">436.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-553">436.00</span></span></td>
<td><span data-ttu-id="5ec50-554">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-555">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-555">CC003</span></span></td>
<td><span data-ttu-id="5ec50-556">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-556">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-557">55</span><span class="sxs-lookup"><span data-stu-id="5ec50-557">55</span></span></td>
<td><span data-ttu-id="5ec50-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ec50-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ec50-559">685.14</span><span class="sxs-lookup"><span data-stu-id="5ec50-559">685.14</span></span></td>
<td><span data-ttu-id="5ec50-560">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-561">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-561">CC004</span></span></td>
<td><span data-ttu-id="5ec50-562">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-562">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-563">10</span><span class="sxs-lookup"><span data-stu-id="5ec50-563">10</span></span></td>
<td><span data-ttu-id="5ec50-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ec50-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ec50-565">124.57</span><span class="sxs-lookup"><span data-stu-id="5ec50-565">124.57</span></span></td>
<td><span data-ttu-id="5ec50-566">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-567">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5ec50-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-568">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-568">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-569">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-569">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-570">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-570">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-571">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-571">Amount</span></span></th>
<th><span data-ttu-id="5ec50-572">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-573">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-573">CC003</span></span></td>
<td><span data-ttu-id="5ec50-574">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-574">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-575">65</span><span class="sxs-lookup"><span data-stu-id="5ec50-575">65</span></span></td>
<td><span data-ttu-id="5ec50-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5ec50-577">438.75</span><span class="sxs-lookup"><span data-stu-id="5ec50-577">438.75</span></span></td>
<td><span data-ttu-id="5ec50-578">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-579">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-579">CC004</span></span></td>
<td><span data-ttu-id="5ec50-580">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-580">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-581">35</span><span class="sxs-lookup"><span data-stu-id="5ec50-581">35</span></span></td>
<td><span data-ttu-id="5ec50-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5ec50-583">236.25</span><span class="sxs-lookup"><span data-stu-id="5ec50-583">236.25</span></span></td>
<td><span data-ttu-id="5ec50-584">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-585">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-585">CC003</span></span></td>
<td><span data-ttu-id="5ec50-586">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-586">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-587">65</span><span class="sxs-lookup"><span data-stu-id="5ec50-587">65</span></span></td>
<td><span data-ttu-id="5ec50-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5ec50-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5ec50-589">5,297.69</span></span></td>
<td><span data-ttu-id="5ec50-590">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-591">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-591">CC004</span></span></td>
<td><span data-ttu-id="5ec50-592">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-592">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-593">35</span><span class="sxs-lookup"><span data-stu-id="5ec50-593">35</span></span></td>
<td><span data-ttu-id="5ec50-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5ec50-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5ec50-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5ec50-595">2,852.60</span></span></td>
<td><span data-ttu-id="5ec50-596">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-597">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5ec50-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-598">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-598">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-599">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-599">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-600">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-600">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-601">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-601">Amount</span></span></th>
<th><span data-ttu-id="5ec50-602">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-603">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-604">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-605">60</span><span class="sxs-lookup"><span data-stu-id="5ec50-605">60</span></span></td>
<td><span data-ttu-id="5ec50-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5ec50-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5ec50-607">535.31</span><span class="sxs-lookup"><span data-stu-id="5ec50-607">535.31</span></span></td>
<td><span data-ttu-id="5ec50-608">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-609">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-610">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-611">20</span><span class="sxs-lookup"><span data-stu-id="5ec50-611">20</span></span></td>
<td><span data-ttu-id="5ec50-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5ec50-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5ec50-613">178.44</span><span class="sxs-lookup"><span data-stu-id="5ec50-613">178.44</span></span></td>
<td><span data-ttu-id="5ec50-614">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-615">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-616">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-617">60</span><span class="sxs-lookup"><span data-stu-id="5ec50-617">60</span></span></td>
<td><span data-ttu-id="5ec50-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5ec50-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5ec50-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5ec50-619">4,487.12</span></span></td>
<td><span data-ttu-id="5ec50-620">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-621">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-622">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-623">20</span><span class="sxs-lookup"><span data-stu-id="5ec50-623">20</span></span></td>
<td><span data-ttu-id="5ec50-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5ec50-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5ec50-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5ec50-625">1,495.71</span></span></td>
<td><span data-ttu-id="5ec50-626">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ec50-627">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5ec50-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-628">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-628">Cost object</span></span></th>
<th><span data-ttu-id="5ec50-629">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5ec50-629">Magnitude</span></span></th>
<th><span data-ttu-id="5ec50-630">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5ec50-630">Allocation factor</span></span></th>
<th><span data-ttu-id="5ec50-631">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-631">Amount</span></span></th>
<th><span data-ttu-id="5ec50-632">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-633">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-634">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-635">80</span><span class="sxs-lookup"><span data-stu-id="5ec50-635">80</span></span></td>
<td><span data-ttu-id="5ec50-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5ec50-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5ec50-637">241.05</span><span class="sxs-lookup"><span data-stu-id="5ec50-637">241.05</span></span></td>
<td><span data-ttu-id="5ec50-638">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-639">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-640">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-641">15</span><span class="sxs-lookup"><span data-stu-id="5ec50-641">15</span></span></td>
<td><span data-ttu-id="5ec50-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5ec50-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5ec50-643">45.20</span><span class="sxs-lookup"><span data-stu-id="5ec50-643">45.20</span></span></td>
<td><span data-ttu-id="5ec50-644">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-645">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-646">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-647">80</span><span class="sxs-lookup"><span data-stu-id="5ec50-647">80</span></span></td>
<td><span data-ttu-id="5ec50-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5ec50-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5ec50-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5ec50-649">2,507.09</span></span></td>
<td><span data-ttu-id="5ec50-650">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-651">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-652">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-653">15</span><span class="sxs-lookup"><span data-stu-id="5ec50-653">15</span></span></td>
<td><span data-ttu-id="5ec50-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5ec50-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5ec50-655">470.08</span><span class="sxs-lookup"><span data-stu-id="5ec50-655">470.08</span></span></td>
<td><span data-ttu-id="5ec50-656">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ec50-657">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="5ec50-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-658">Kladden</span><span class="sxs-lookup"><span data-stu-id="5ec50-658">Journal</span></span></th>
<th><span data-ttu-id="5ec50-659">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5ec50-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ec50-660">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5ec50-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ec50-661">Version</span><span class="sxs-lookup"><span data-stu-id="5ec50-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-662">00004</span><span class="sxs-lookup"><span data-stu-id="5ec50-662">00004</span></span></td>
<td><span data-ttu-id="5ec50-663">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="5ec50-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5ec50-664">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5ec50-664">Fiscal</span></span></td>
<td><span data-ttu-id="5ec50-665">2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-665">2017</span></span></td>
<td><span data-ttu-id="5ec50-666">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5ec50-666">Period 1</span></span></td>
<td><span data-ttu-id="5ec50-667">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5ec50-668">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="5ec50-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ec50-669">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-670">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-671">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-671">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-672">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-672">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-673">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-674">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-675">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-675">CC001</span></span></td>
<td><span data-ttu-id="5ec50-676">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-676">HR</span></span></td>
<td><span data-ttu-id="5ec50-677">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-677">10001</span></span></td>
<td><span data-ttu-id="5ec50-678">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-678">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-679">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-679">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-680">500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-681">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-682">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-682">CC001</span></span></td>
<td><span data-ttu-id="5ec50-683">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-683">HR</span></span></td>
<td><span data-ttu-id="5ec50-684">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-684">10001</span></span></td>
<td><span data-ttu-id="5ec50-685">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-685">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-686">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-686">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ec50-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-688">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-689">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-689">CC002</span></span></td>
<td><span data-ttu-id="5ec50-690">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-690">Finance</span></span></td>
<td><span data-ttu-id="5ec50-691">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-691">10001</span></span></td>
<td><span data-ttu-id="5ec50-692">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-692">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-693">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-693">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-694">675.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-695">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-696">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-696">CC002</span></span></td>
<td><span data-ttu-id="5ec50-697">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-697">Finance</span></span></td>
<td><span data-ttu-id="5ec50-698">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-698">10001</span></span></td>
<td><span data-ttu-id="5ec50-699">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-699">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-700">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-700">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5ec50-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-702">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-703">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-703">CC003</span></span></td>
<td><span data-ttu-id="5ec50-704">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-704">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-705">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-705">10001</span></span></td>
<td><span data-ttu-id="5ec50-706">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-706">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-707">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-707">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-708">713.75</span><span class="sxs-lookup"><span data-stu-id="5ec50-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-709">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-710">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-710">CC003</span></span></td>
<td><span data-ttu-id="5ec50-711">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-711">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-712">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-712">10001</span></span></td>
<td><span data-ttu-id="5ec50-713">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-713">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-714">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-714">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5ec50-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-716">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-717">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-717">CC003</span></span></td>
<td><span data-ttu-id="5ec50-718">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-718">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-719">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-719">10001</span></span></td>
<td><span data-ttu-id="5ec50-720">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-720">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-721">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-721">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-722">286.25</span><span class="sxs-lookup"><span data-stu-id="5ec50-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-723">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-724">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-724">CC003</span></span></td>
<td><span data-ttu-id="5ec50-725">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-725">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-726">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-726">10001</span></span></td>
<td><span data-ttu-id="5ec50-727">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-727">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-728">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-728">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5ec50-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-730">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-731">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-732">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-733">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-733">10001</span></span></td>
<td><span data-ttu-id="5ec50-734">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-734">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-735">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-735">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-736">776.36</span><span class="sxs-lookup"><span data-stu-id="5ec50-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-737">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-738">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-739">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-740">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-740">10001</span></span></td>
<td><span data-ttu-id="5ec50-741">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-741">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-742">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-742">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5ec50-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-744">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-745">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-746">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-747">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-747">10001</span></span></td>
<td><span data-ttu-id="5ec50-748">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-748">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-749">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-749">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-750">223.64</span><span class="sxs-lookup"><span data-stu-id="5ec50-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-751">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ec50-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-752">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-753">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-754">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-754">10001</span></span></td>
<td><span data-ttu-id="5ec50-755">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-755">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-756">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-756">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5ec50-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ec50-758">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5ec50-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ec50-759">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ec50-760">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-760">Cost element</span></span></th>
<th><span data-ttu-id="5ec50-761">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-761">Cost behavior</span></span></th>
<th><span data-ttu-id="5ec50-762">Beløb</span><span class="sxs-lookup"><span data-stu-id="5ec50-762">Amount</span></span></th>
<th><span data-ttu-id="5ec50-763">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5ec50-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ec50-764">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-764">CC001</span></span></td>
<td><span data-ttu-id="5ec50-765">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-765">HR</span></span></td>
<td><span data-ttu-id="5ec50-766">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-766">10001</span></span></td>
<td><span data-ttu-id="5ec50-767">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-767">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-768">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-768">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-769">-500.00</span></span></td>
<td><span data-ttu-id="5ec50-770">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-771">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-771">CC002</span></span></td>
<td><span data-ttu-id="5ec50-772">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-772">Finance</span></span></td>
<td><span data-ttu-id="5ec50-773">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-773">10001</span></span></td>
<td><span data-ttu-id="5ec50-774">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-774">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-775">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-775">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-776">175.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-776">175.00</span></span></td>
<td><span data-ttu-id="5ec50-777">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-778">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-778">CC003</span></span></td>
<td><span data-ttu-id="5ec50-779">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-779">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-780">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-780">10001</span></span></td>
<td><span data-ttu-id="5ec50-781">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-781">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-782">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-782">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-783">275.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-783">275.00</span></span></td>
<td><span data-ttu-id="5ec50-784">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-785">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-785">CC004</span></span></td>
<td><span data-ttu-id="5ec50-786">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-786">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-787">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-787">10001</span></span></td>
<td><span data-ttu-id="5ec50-788">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-788">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-789">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-789">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-790">50,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-790">50,00</span></span></td>
<td><span data-ttu-id="5ec50-791">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-792">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-792">CC001</span></span></td>
<td><span data-ttu-id="5ec50-793">Personale</span><span class="sxs-lookup"><span data-stu-id="5ec50-793">HR</span></span></td>
<td><span data-ttu-id="5ec50-794">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-794">10001</span></span></td>
<td><span data-ttu-id="5ec50-795">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-795">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-796">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-796">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ec50-797">-1,245.71</span></span></td>
<td><span data-ttu-id="5ec50-798">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-799">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-799">CC002</span></span></td>
<td><span data-ttu-id="5ec50-800">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-800">Finance</span></span></td>
<td><span data-ttu-id="5ec50-801">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-801">10001</span></span></td>
<td><span data-ttu-id="5ec50-802">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-802">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-803">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-803">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-804">436.00</span><span class="sxs-lookup"><span data-stu-id="5ec50-804">436.00</span></span></td>
<td><span data-ttu-id="5ec50-805">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-806">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-806">CC003</span></span></td>
<td><span data-ttu-id="5ec50-807">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-807">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-808">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-808">10001</span></span></td>
<td><span data-ttu-id="5ec50-809">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-809">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-810">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-810">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-811">685.14</span><span class="sxs-lookup"><span data-stu-id="5ec50-811">685.14</span></span></td>
<td><span data-ttu-id="5ec50-812">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-813">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-813">CC004</span></span></td>
<td><span data-ttu-id="5ec50-814">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-814">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-815">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-815">10001</span></span></td>
<td><span data-ttu-id="5ec50-816">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-816">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-817">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-817">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-818">124.57</span><span class="sxs-lookup"><span data-stu-id="5ec50-818">124.57</span></span></td>
<td><span data-ttu-id="5ec50-819">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-820">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-820">CC002</span></span></td>
<td><span data-ttu-id="5ec50-821">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-821">Finance</span></span></td>
<td><span data-ttu-id="5ec50-822">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-822">10001</span></span></td>
<td><span data-ttu-id="5ec50-823">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-823">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-824">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-824">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-825">-675.00</span></span></td>
<td><span data-ttu-id="5ec50-826">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-827">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-827">CC003</span></span></td>
<td><span data-ttu-id="5ec50-828">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-828">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-829">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-829">10001</span></span></td>
<td><span data-ttu-id="5ec50-830">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-830">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-831">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-831">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-832">438.75</span><span class="sxs-lookup"><span data-stu-id="5ec50-832">438.75</span></span></td>
<td><span data-ttu-id="5ec50-833">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-834">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-834">CC004</span></span></td>
<td><span data-ttu-id="5ec50-835">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-835">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-836">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-836">10001</span></span></td>
<td><span data-ttu-id="5ec50-837">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-837">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-838">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-838">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-839">236.25</span><span class="sxs-lookup"><span data-stu-id="5ec50-839">236.25</span></span></td>
<td><span data-ttu-id="5ec50-840">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-841">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-841">CC002</span></span></td>
<td><span data-ttu-id="5ec50-842">Finans</span><span class="sxs-lookup"><span data-stu-id="5ec50-842">Finance</span></span></td>
<td><span data-ttu-id="5ec50-843">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-843">10001</span></span></td>
<td><span data-ttu-id="5ec50-844">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-844">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-845">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-845">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="5ec50-846">-8,150.29</span></span></td>
<td><span data-ttu-id="5ec50-847">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-848">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-848">CC003</span></span></td>
<td><span data-ttu-id="5ec50-849">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-849">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-850">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-850">10001</span></span></td>
<td><span data-ttu-id="5ec50-851">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-851">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-852">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-852">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5ec50-853">5,297.69</span></span></td>
<td><span data-ttu-id="5ec50-854">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-855">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-855">CC004</span></span></td>
<td><span data-ttu-id="5ec50-856">Emballage</span><span class="sxs-lookup"><span data-stu-id="5ec50-856">Packaging</span></span></td>
<td><span data-ttu-id="5ec50-857">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-857">10001</span></span></td>
<td><span data-ttu-id="5ec50-858">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-858">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-859">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-859">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5ec50-860">2,852.60</span></span></td>
<td><span data-ttu-id="5ec50-861">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-862">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-862">CC003</span></span></td>
<td><span data-ttu-id="5ec50-863">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-863">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-864">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-864">10001</span></span></td>
<td><span data-ttu-id="5ec50-865">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-865">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-866">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-866">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="5ec50-867">-713.75</span></span></td>
<td><span data-ttu-id="5ec50-868">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-869">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-870">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-871">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-871">10001</span></span></td>
<td><span data-ttu-id="5ec50-872">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-872">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-873">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-873">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-874">535.31</span><span class="sxs-lookup"><span data-stu-id="5ec50-874">535.31</span></span></td>
<td><span data-ttu-id="5ec50-875">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-876">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-877">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-878">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-878">10001</span></span></td>
<td><span data-ttu-id="5ec50-879">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-879">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-880">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-880">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-881">178.44</span><span class="sxs-lookup"><span data-stu-id="5ec50-881">178.44</span></span></td>
<td><span data-ttu-id="5ec50-882">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-883">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-883">CC003</span></span></td>
<td><span data-ttu-id="5ec50-884">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-884">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-885">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-885">10001</span></span></td>
<td><span data-ttu-id="5ec50-886">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-886">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-887">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-887">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="5ec50-888">-5,982.83</span></span></td>
<td><span data-ttu-id="5ec50-889">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-890">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-891">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-892">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-892">10001</span></span></td>
<td><span data-ttu-id="5ec50-893">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-893">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-894">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-894">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5ec50-895">4,487.12</span></span></td>
<td><span data-ttu-id="5ec50-896">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-897">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-898">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-899">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-899">10001</span></span></td>
<td><span data-ttu-id="5ec50-900">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-900">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-901">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-901">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5ec50-902">1,495.71</span></span></td>
<td><span data-ttu-id="5ec50-903">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-904">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-904">CC003</span></span></td>
<td><span data-ttu-id="5ec50-905">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-905">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-906">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-906">10001</span></span></td>
<td><span data-ttu-id="5ec50-907">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-907">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-908">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-908">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="5ec50-909">-286.25</span></span></td>
<td><span data-ttu-id="5ec50-910">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-911">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-912">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-913">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-913">10001</span></span></td>
<td><span data-ttu-id="5ec50-914">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-914">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-915">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-915">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-916">241.05</span><span class="sxs-lookup"><span data-stu-id="5ec50-916">241.05</span></span></td>
<td><span data-ttu-id="5ec50-917">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-918">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-919">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-920">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-920">10001</span></span></td>
<td><span data-ttu-id="5ec50-921">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-921">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-922">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-922">Fixed cost</span></span></td>
<td><span data-ttu-id="5ec50-923">45.20</span><span class="sxs-lookup"><span data-stu-id="5ec50-923">45.20</span></span></td>
<td><span data-ttu-id="5ec50-924">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-925">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-925">CC003</span></span></td>
<td><span data-ttu-id="5ec50-926">Samling</span><span class="sxs-lookup"><span data-stu-id="5ec50-926">Assembly</span></span></td>
<td><span data-ttu-id="5ec50-927">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-927">10001</span></span></td>
<td><span data-ttu-id="5ec50-928">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-928">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-929">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-929">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="5ec50-930">-2,977.17</span></span></td>
<td><span data-ttu-id="5ec50-931">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-932">Prod 1</span></span></td>
<td><span data-ttu-id="5ec50-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-933">Product 1</span></span></td>
<td><span data-ttu-id="5ec50-934">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-934">10001</span></span></td>
<td><span data-ttu-id="5ec50-935">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-935">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-936">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-936">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5ec50-937">2,507.09</span></span></td>
<td><span data-ttu-id="5ec50-938">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ec50-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-939">Prod 2</span></span></td>
<td><span data-ttu-id="5ec50-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-940">Product 2</span></span></td>
<td><span data-ttu-id="5ec50-941">10001</span><span class="sxs-lookup"><span data-stu-id="5ec50-941">10001</span></span></td>
<td><span data-ttu-id="5ec50-942">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-942">Electricity</span></span></td>
<td><span data-ttu-id="5ec50-943">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-943">Variable cost</span></span></td>
<td><span data-ttu-id="5ec50-944">470.08</span><span class="sxs-lookup"><span data-stu-id="5ec50-944">470.08</span></span></td>
<td><span data-ttu-id="5ec50-945">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5ec50-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5ec50-946">Konklusion</span><span class="sxs-lookup"><span data-stu-id="5ec50-946">Conclusion</span></span>
<span data-ttu-id="5ec50-947">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="5ec50-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5ec50-948">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="5ec50-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5ec50-949">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="5ec50-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5ec50-950">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5ec50-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5ec50-951">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5ec50-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5ec50-952">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5ec50-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5ec50-953">Samlet</span><span class="sxs-lookup"><span data-stu-id="5ec50-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5ec50-954">CC099</span><span class="sxs-lookup"><span data-stu-id="5ec50-954">CC099</span></span></th>
<th><span data-ttu-id="5ec50-955">CC001</span><span class="sxs-lookup"><span data-stu-id="5ec50-955">CC001</span></span></th>
<th><span data-ttu-id="5ec50-956">CC002</span><span class="sxs-lookup"><span data-stu-id="5ec50-956">CC002</span></span></th>
<th><span data-ttu-id="5ec50-957">CC003</span><span class="sxs-lookup"><span data-stu-id="5ec50-957">CC003</span></span></th>
<th><span data-ttu-id="5ec50-958">CC004</span><span class="sxs-lookup"><span data-stu-id="5ec50-958">CC004</span></span></th>
<th><span data-ttu-id="5ec50-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-959">Proj 1</span></span></th>
<th><span data-ttu-id="5ec50-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-960">Proj 2</span></span></th>
<th><span data-ttu-id="5ec50-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ec50-961">Prod 1</span></span></th>
<th><span data-ttu-id="5ec50-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ec50-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5ec50-963">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5ec50-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5ec50-973">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5ec50-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-974">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5ec50-975">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-978">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-979">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-980">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-981">776.36</span><span class="sxs-lookup"><span data-stu-id="5ec50-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-982">223.64</span><span class="sxs-lookup"><span data-stu-id="5ec50-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5ec50-984">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5ec50-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-985">000</span><span class="sxs-lookup"><span data-stu-id="5ec50-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-987">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-988">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-989">0,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-990">30,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-991">10,00</span><span class="sxs-lookup"><span data-stu-id="5ec50-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5ec50-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5ec50-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ec50-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ec50-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5ec50-995">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5ec50-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5ec50-996">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="5ec50-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5ec50-997">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="5ec50-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5ec50-998">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="5ec50-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5ec50-999">Du kan finde flere oplysninger under Politik for omkostningstotaler.</span><span class="sxs-lookup"><span data-stu-id="5ec50-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="5ec50-1000">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="5ec50-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




