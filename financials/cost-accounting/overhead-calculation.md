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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: a8c867ba49b95af2816fe8294059307e974c0a81
ms.contentlocale: da-dk
ms.lasthandoff: 09/18/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="b006b-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b006b-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b006b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b006b-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="b006b-105">Term definition</span></span>
---------------

<span data-ttu-id="b006b-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="b006b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b006b-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="b006b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b006b-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="b006b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b006b-109">Leje</span><span class="sxs-lookup"><span data-stu-id="b006b-109">Rent</span></span>
-   <span data-ttu-id="b006b-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-110">Electricity</span></span>
-   <span data-ttu-id="b006b-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="b006b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b006b-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-112">Overhead calculation overview</span></span>
<span data-ttu-id="b006b-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="b006b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b006b-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="b006b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b006b-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="b006b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b006b-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b006b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b006b-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="b006b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b006b-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="b006b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b006b-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="b006b-119">Version type</span></span>
-   <span data-ttu-id="b006b-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="b006b-120">Date and time</span></span>
-   <span data-ttu-id="b006b-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="b006b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b006b-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="b006b-122">Fiscal year</span></span>
-   <span data-ttu-id="b006b-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="b006b-123">Fiscal period</span></span>

<span data-ttu-id="b006b-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="b006b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b006b-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="b006b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b006b-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="b006b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b006b-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="b006b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b006b-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="b006b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b006b-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="b006b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b006b-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="b006b-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="b006b-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b006b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b006b-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b006b-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="b006b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b006b-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="b006b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b006b-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="b006b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b006b-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="b006b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b006b-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="b006b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="b006b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="b006b-140">Main account</span></span></th>
<th><span data-ttu-id="b006b-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="b006b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b006b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-143">CC099</span></span></td>
<td><span data-ttu-id="b006b-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-144">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-145">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-145">10001</span></span></td>
<td><span data-ttu-id="b006b-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-146">Electricity</span></span></td>
<td><span data-ttu-id="b006b-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b006b-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="b006b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b006b-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="b006b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b006b-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="b006b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b006b-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="b006b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b006b-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="b006b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b006b-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="b006b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b006b-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="b006b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b006b-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="b006b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b006b-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b006b-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="b006b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b006b-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="b006b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b006b-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-160">Journal</span></span></th>
<th><span data-ttu-id="b006b-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="b006b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b006b-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b006b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b006b-163">Version</span><span class="sxs-lookup"><span data-stu-id="b006b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-164">00001</span><span class="sxs-lookup"><span data-stu-id="b006b-164">00001</span></span></td>
<td><span data-ttu-id="b006b-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b006b-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="b006b-166">Fiscal</span></span></td>
<td><span data-ttu-id="b006b-167">2017</span><span class="sxs-lookup"><span data-stu-id="b006b-167">2017</span></span></td>
<td><span data-ttu-id="b006b-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="b006b-168">Period 1</span></span></td>
<td><span data-ttu-id="b006b-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="b006b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b006b-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="b006b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-173">Cost element</span></span></th>
<th><span data-ttu-id="b006b-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b006b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-177">CC099</span></span></td>
<td><span data-ttu-id="b006b-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-178">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-179">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-179">10001</span></span></td>
<td><span data-ttu-id="b006b-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-180">Electricity</span></span></td>
<td><span data-ttu-id="b006b-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="b006b-181">Unclassified</span></span></td>
<td><span data-ttu-id="b006b-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b006b-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b006b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-185">Cost element</span></span></th>
<th><span data-ttu-id="b006b-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-187">Amount</span></span></th>
<th><span data-ttu-id="b006b-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-189">CC099</span></span></td>
<td><span data-ttu-id="b006b-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-190">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-191">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-191">10001</span></span></td>
<td><span data-ttu-id="b006b-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-192">Electricity</span></span></td>
<td><span data-ttu-id="b006b-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="b006b-193">Unclassified</span></span></td>
<td><span data-ttu-id="b006b-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-194">10,000.00</span></span></td>
<td><span data-ttu-id="b006b-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-196">CC099</span></span></td>
<td><span data-ttu-id="b006b-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-197">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-198">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-198">10001</span></span></td>
<td><span data-ttu-id="b006b-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-199">Electricity</span></span></td>
<td><span data-ttu-id="b006b-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="b006b-200">Unclassified</span></span></td>
<td><span data-ttu-id="b006b-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b006b-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-203">CC099</span></span></td>
<td><span data-ttu-id="b006b-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-204">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-205">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-205">10001</span></span></td>
<td><span data-ttu-id="b006b-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-206">Electricity</span></span></td>
<td><span data-ttu-id="b006b-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-208">1,000.00</span></span></td>
<td><span data-ttu-id="b006b-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-210">CC099</span></span></td>
<td><span data-ttu-id="b006b-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-211">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-212">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-212">10001</span></span></td>
<td><span data-ttu-id="b006b-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-213">Electricity</span></span></td>
<td><span data-ttu-id="b006b-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-214">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-215">9,000.00</span></span></td>
<td><span data-ttu-id="b006b-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-217">Du kan finde detaljerede oplysninger om funktionalitet af omkostninger under Politik for funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="b006b-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="b006b-218">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="b006b-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b006b-219">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="b006b-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b006b-220">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b006b-221">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="b006b-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b006b-222">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="b006b-222">Define the cost distribution rule</span></span>

<span data-ttu-id="b006b-223">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="b006b-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b006b-224">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="b006b-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b006b-225">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b006b-226">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="b006b-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b006b-227">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="b006b-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b006b-228">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-229">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-229">Cost object</span></span></th>
<th><span data-ttu-id="b006b-230">KWh</span><span class="sxs-lookup"><span data-stu-id="b006b-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-231">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-231">CC001</span></span></td>
<td><span data-ttu-id="b006b-232">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-232">HR</span></span></td>
<td><span data-ttu-id="b006b-233">1.000</span><span class="sxs-lookup"><span data-stu-id="b006b-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-234">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-234">CC002</span></span></td>
<td><span data-ttu-id="b006b-235">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-235">Finance</span></span></td>
<td><span data-ttu-id="b006b-236">6.000</span><span class="sxs-lookup"><span data-stu-id="b006b-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-237">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-237">CC003</span></span></td>
<td><span data-ttu-id="b006b-238">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-238">Assembly</span></span></td>
<td><span data-ttu-id="b006b-239">0</span><span class="sxs-lookup"><span data-stu-id="b006b-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-240">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b006b-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-241">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-241">Cost object</span></span></th>
<th><span data-ttu-id="b006b-242">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-242">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-243">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-243">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-244">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-245">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-245">CC001</span></span></td>
<td><span data-ttu-id="b006b-246">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-246">HR</span></span></td>
<td><span data-ttu-id="b006b-247">1.000</span><span class="sxs-lookup"><span data-stu-id="b006b-247">1,000</span></span></td>
<td><span data-ttu-id="b006b-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b006b-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b006b-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-250">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-250">CC002</span></span></td>
<td><span data-ttu-id="b006b-251">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-251">Finance</span></span></td>
<td><span data-ttu-id="b006b-252">6.000</span><span class="sxs-lookup"><span data-stu-id="b006b-252">6,000</span></span></td>
<td><span data-ttu-id="b006b-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b006b-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b006b-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-255">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-255">CC003</span></span></td>
<td><span data-ttu-id="b006b-256">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-256">Assembly</span></span></td>
<td><span data-ttu-id="b006b-257">0</span><span class="sxs-lookup"><span data-stu-id="b006b-257">0</span></span></td>
<td><span data-ttu-id="b006b-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b006b-259">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-260">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="b006b-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b006b-261">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b006b-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-262">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-262">Cost object</span></span></th>
<th><span data-ttu-id="b006b-263">Formel</span><span class="sxs-lookup"><span data-stu-id="b006b-263">Formula</span></span></th>
<th><span data-ttu-id="b006b-264">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-264">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-265">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-265">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-266">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-267">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-267">CC001</span></span></td>
<td><span data-ttu-id="b006b-268">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-268">HR</span></span></td>
<td><span data-ttu-id="b006b-269">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b006b-270">1</span><span class="sxs-lookup"><span data-stu-id="b006b-270">1</span></span></td>
<td><span data-ttu-id="b006b-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b006b-272">500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-273">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-273">CC002</span></span></td>
<td><span data-ttu-id="b006b-274">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-274">Finance</span></span></td>
<td><span data-ttu-id="b006b-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b006b-276">1</span><span class="sxs-lookup"><span data-stu-id="b006b-276">1</span></span></td>
<td><span data-ttu-id="b006b-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b006b-278">500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-279">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-279">CC003</span></span></td>
<td><span data-ttu-id="b006b-280">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-280">Assembly</span></span></td>
<td><span data-ttu-id="b006b-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b006b-282">0</span><span class="sxs-lookup"><span data-stu-id="b006b-282">0</span></span></td>
<td><span data-ttu-id="b006b-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b006b-284">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b006b-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-286">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-286">Journal</span></span></th>
<th><span data-ttu-id="b006b-287">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="b006b-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b006b-288">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b006b-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b006b-289">Version</span><span class="sxs-lookup"><span data-stu-id="b006b-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-290">00002</span><span class="sxs-lookup"><span data-stu-id="b006b-290">00002</span></span></td>
<td><span data-ttu-id="b006b-291">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="b006b-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b006b-292">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="b006b-292">Fiscal</span></span></td>
<td><span data-ttu-id="b006b-293">2017</span><span class="sxs-lookup"><span data-stu-id="b006b-293">2017</span></span></td>
<td><span data-ttu-id="b006b-294">1. Periode</span><span class="sxs-lookup"><span data-stu-id="b006b-294">Period 1</span></span></td>
<td><span data-ttu-id="b006b-295">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="b006b-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b006b-296">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="b006b-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-297">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-298">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-299">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-299">Cost element</span></span></th>
<th><span data-ttu-id="b006b-300">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-300">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-301">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-302">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-303">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-303">CC099</span></span></td>
<td><span data-ttu-id="b006b-304">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-304">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-305">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-305">10001</span></span></td>
<td><span data-ttu-id="b006b-306">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-306">Electricity</span></span></td>
<td><span data-ttu-id="b006b-307">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-307">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-309">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-310">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-310">CC099</span></span></td>
<td><span data-ttu-id="b006b-311">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-311">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-312">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-312">10001</span></span></td>
<td><span data-ttu-id="b006b-313">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-313">Electricity</span></span></td>
<td><span data-ttu-id="b006b-314">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-314">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b006b-316">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b006b-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-317">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-318">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-318">Cost element</span></span></th>
<th><span data-ttu-id="b006b-319">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-319">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-320">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-320">Amount</span></span></th>
<th><span data-ttu-id="b006b-321">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-322">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-322">CC099</span></span></td>
<td><span data-ttu-id="b006b-323">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-323">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-324">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-324">10001</span></span></td>
<td><span data-ttu-id="b006b-325">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-325">Electricity</span></span></td>
<td><span data-ttu-id="b006b-326">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-326">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-327">-1,000.00</span></span></td>
<td><span data-ttu-id="b006b-328">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-329">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-329">CC001</span></span></td>
<td><span data-ttu-id="b006b-330">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-330">HR</span></span></td>
<td><span data-ttu-id="b006b-331">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-331">10001</span></span></td>
<td><span data-ttu-id="b006b-332">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-332">Electricity</span></span></td>
<td><span data-ttu-id="b006b-333">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-333">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-334">500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-334">500.00</span></span></td>
<td><span data-ttu-id="b006b-335">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-336">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-336">CC002</span></span></td>
<td><span data-ttu-id="b006b-337">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-337">Finance</span></span></td>
<td><span data-ttu-id="b006b-338">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-338">10001</span></span></td>
<td><span data-ttu-id="b006b-339">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-339">Electricity</span></span></td>
<td><span data-ttu-id="b006b-340">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-340">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-341">500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-341">500.00</span></span></td>
<td><span data-ttu-id="b006b-342">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-343">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-343">CC099</span></span></td>
<td><span data-ttu-id="b006b-344">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="b006b-344">Default cost center</span></span></td>
<td><span data-ttu-id="b006b-345">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-345">10001</span></span></td>
<td><span data-ttu-id="b006b-346">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-346">Electricity</span></span></td>
<td><span data-ttu-id="b006b-347">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-347">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="b006b-348">-9,000.00</span></span></td>
<td><span data-ttu-id="b006b-349">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-350">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-350">CC001</span></span></td>
<td><span data-ttu-id="b006b-351">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-351">HR</span></span></td>
<td><span data-ttu-id="b006b-352">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-352">10001</span></span></td>
<td><span data-ttu-id="b006b-353">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-353">Electricity</span></span></td>
<td><span data-ttu-id="b006b-354">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-354">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b006b-355">1,285.71</span></span></td>
<td><span data-ttu-id="b006b-356">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-357">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-357">CC002</span></span></td>
<td><span data-ttu-id="b006b-358">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-358">Finance</span></span></td>
<td><span data-ttu-id="b006b-359">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-359">10001</span></span></td>
<td><span data-ttu-id="b006b-360">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-360">Electricity</span></span></td>
<td><span data-ttu-id="b006b-361">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-361">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b006b-362">7,714.29</span></span></td>
<td><span data-ttu-id="b006b-363">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-364">Du kan finde detaljerede oplysninger om omkostningsfordeling og fordelingsgrundlag under Politik for omkostningsfordeling og Fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="b006b-365">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="b006b-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b006b-366">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="b006b-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b006b-367">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b006b-368">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b006b-369">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="b006b-369">Define the overhead rate</span></span>

<span data-ttu-id="b006b-370">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b006b-371">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="b006b-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-372">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-372">Cost object</span></span></th>
<th><span data-ttu-id="b006b-373">Timer</span><span class="sxs-lookup"><span data-stu-id="b006b-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-374">Proj 1</span></span></td>
<td><span data-ttu-id="b006b-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-375">Project 1</span></span></td>
<td><span data-ttu-id="b006b-376">3</span><span class="sxs-lookup"><span data-stu-id="b006b-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-377">Proj 2</span></span></td>
<td><span data-ttu-id="b006b-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-378">Project 2</span></span></td>
<td><span data-ttu-id="b006b-379">1</span><span class="sxs-lookup"><span data-stu-id="b006b-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-380">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="b006b-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-381">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-381">Cost object</span></span></th>
<th><span data-ttu-id="b006b-382">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-382">Cost element</span></span></th>
<th><span data-ttu-id="b006b-383">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-383">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-384">Enheder</span><span class="sxs-lookup"><span data-stu-id="b006b-384">Units</span></span></th>
<th><span data-ttu-id="b006b-385">Kurs</span><span class="sxs-lookup"><span data-stu-id="b006b-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-386">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-386">CC001</span></span></td>
<td><span data-ttu-id="b006b-387">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-387">HR</span></span></td>
<td><span data-ttu-id="b006b-388">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-388">10001</span></span></td>
<td><span data-ttu-id="b006b-389">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-389">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-390">1</span><span class="sxs-lookup"><span data-stu-id="b006b-390">1</span></span></td>
<td><span data-ttu-id="b006b-391">10</span><span class="sxs-lookup"><span data-stu-id="b006b-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-392">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-393">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-393">Cost object</span></span></th>
<th><span data-ttu-id="b006b-394">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-394">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-395">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-395">Cost element</span></span></th>
<th><span data-ttu-id="b006b-396">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-396">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-397">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-398">Proj 1</span></span></td>
<td><span data-ttu-id="b006b-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-399">Project 1</span></span></td>
<td><span data-ttu-id="b006b-400">3</span><span class="sxs-lookup"><span data-stu-id="b006b-400">3</span></span></td>
<td><span data-ttu-id="b006b-401">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-401">10001</span></span></td>
<td><span data-ttu-id="b006b-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b006b-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b006b-403">30,00</span><span class="sxs-lookup"><span data-stu-id="b006b-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-404">Proj 2</span></span></td>
<td><span data-ttu-id="b006b-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-405">Project 2</span></span></td>
<td><span data-ttu-id="b006b-406">1</span><span class="sxs-lookup"><span data-stu-id="b006b-406">1</span></span></td>
<td><span data-ttu-id="b006b-407">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-407">10001</span></span></td>
<td><span data-ttu-id="b006b-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b006b-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b006b-409">10,00</span><span class="sxs-lookup"><span data-stu-id="b006b-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b006b-410">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-411">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-411">Journal</span></span></th>
<th><span data-ttu-id="b006b-412">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="b006b-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b006b-413">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b006b-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b006b-414">Version</span><span class="sxs-lookup"><span data-stu-id="b006b-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-415">00003</span><span class="sxs-lookup"><span data-stu-id="b006b-415">00003</span></span></td>
<td><span data-ttu-id="b006b-416">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="b006b-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b006b-417">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="b006b-417">Fiscal</span></span></td>
<td><span data-ttu-id="b006b-418">2017</span><span class="sxs-lookup"><span data-stu-id="b006b-418">2017</span></span></td>
<td><span data-ttu-id="b006b-419">1. Periode</span><span class="sxs-lookup"><span data-stu-id="b006b-419">Period 1</span></span></td>
<td><span data-ttu-id="b006b-420">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="b006b-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b006b-421">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="b006b-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-422">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-423">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-423">Cost object</span></span></th>
<th><span data-ttu-id="b006b-424">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-425">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-426">Proj 1</span></span></td>
<td><span data-ttu-id="b006b-427">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b006b-428">3,00</span><span class="sxs-lookup"><span data-stu-id="b006b-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-429">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-430">Proj 2</span></span></td>
<td><span data-ttu-id="b006b-431">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b006b-432">1,00</span><span class="sxs-lookup"><span data-stu-id="b006b-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b006b-433">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b006b-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-434">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-435">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-435">Cost element</span></span></th>
<th><span data-ttu-id="b006b-436">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-436">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-437">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-437">Amount</span></span></th>
<th><span data-ttu-id="b006b-438">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="b006b-439">CC0001</span></span></td>
<td><span data-ttu-id="b006b-440">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-440">HR</span></span></td>
<td><span data-ttu-id="b006b-441">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-441">10001</span></span></td>
<td><span data-ttu-id="b006b-442">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-442">Electricity</span></span></td>
<td><span data-ttu-id="b006b-443">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-443">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="b006b-444">-30.00</span></span></td>
<td><span data-ttu-id="b006b-445">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-446">Proj 1</span></span></td>
<td><span data-ttu-id="b006b-447">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b006b-448">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-448">10001</span></span></td>
<td><span data-ttu-id="b006b-449">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-449">Electricity</span></span></td>
<td><span data-ttu-id="b006b-450">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-450">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-451">30,00</span><span class="sxs-lookup"><span data-stu-id="b006b-451">30.00</span></span></td>
<td><span data-ttu-id="b006b-452">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-453">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-453">CC001</span></span></td>
<td><span data-ttu-id="b006b-454">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-454">HR</span></span></td>
<td><span data-ttu-id="b006b-455">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-455">10001</span></span></td>
<td><span data-ttu-id="b006b-456">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-456">Electricity</span></span></td>
<td><span data-ttu-id="b006b-457">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-457">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="b006b-458">-10.00</span></span></td>
<td><span data-ttu-id="b006b-459">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-460">Proj 2</span></span></td>
<td><span data-ttu-id="b006b-461">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b006b-462">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-462">10001</span></span></td>
<td><span data-ttu-id="b006b-463">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-463">Electricity</span></span></td>
<td><span data-ttu-id="b006b-464">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-464">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-465">10,00</span><span class="sxs-lookup"><span data-stu-id="b006b-465">10.00</span></span></td>
<td><span data-ttu-id="b006b-466">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-467">Detaljerede oplysninger om politik for satser for faste omkostninger finder du i Politik for sats for faste omkostninger og Fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="b006b-468">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="b006b-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b006b-469">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="b006b-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b006b-470">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b006b-471">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="b006b-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="b006b-472">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="b006b-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b006b-473">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="b006b-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b006b-474">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="b006b-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b006b-475">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="b006b-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b006b-476">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="b006b-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="b006b-477">[![Reciprok metode](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="b006b-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b006b-478">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="b006b-478">Define the cost allocation</span></span>

<span data-ttu-id="b006b-479">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b006b-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b006b-480">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b006b-481">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="b006b-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-482">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-482">Cost object</span></span></th>
<th><span data-ttu-id="b006b-483">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="b006b-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-484">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-484">CC002</span></span></td>
<td><span data-ttu-id="b006b-485">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-485">Finance</span></span></td>
<td><span data-ttu-id="b006b-486">35</span><span class="sxs-lookup"><span data-stu-id="b006b-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-487">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-487">CC003</span></span></td>
<td><span data-ttu-id="b006b-488">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-488">Assembly</span></span></td>
<td><span data-ttu-id="b006b-489">55</span><span class="sxs-lookup"><span data-stu-id="b006b-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-490">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-490">CC004</span></span></td>
<td><span data-ttu-id="b006b-491">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-491">Packaging</span></span></td>
<td><span data-ttu-id="b006b-492">10</span><span class="sxs-lookup"><span data-stu-id="b006b-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-493">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b006b-494">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="b006b-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-495">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-495">Cost object</span></span></th>
<th><span data-ttu-id="b006b-496">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="b006b-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-497">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-497">CC003</span></span></td>
<td><span data-ttu-id="b006b-498">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-498">Assembly</span></span></td>
<td><span data-ttu-id="b006b-499">65</span><span class="sxs-lookup"><span data-stu-id="b006b-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-500">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-500">CC004</span></span></td>
<td><span data-ttu-id="b006b-501">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-501">Packaging</span></span></td>
<td><span data-ttu-id="b006b-502">35</span><span class="sxs-lookup"><span data-stu-id="b006b-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-503">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b006b-504">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="b006b-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-505">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-505">Cost object</span></span></th>
<th><span data-ttu-id="b006b-506">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="b006b-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-507">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-508">Product 1</span></span></td>
<td><span data-ttu-id="b006b-509">60</span><span class="sxs-lookup"><span data-stu-id="b006b-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-510">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-511">Product 2</span></span></td>
<td><span data-ttu-id="b006b-512">20</span><span class="sxs-lookup"><span data-stu-id="b006b-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-513">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b006b-514">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="b006b-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-515">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-515">Cost object</span></span></th>
<th><span data-ttu-id="b006b-516">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="b006b-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-517">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-518">Product 1</span></span></td>
<td><span data-ttu-id="b006b-519">80</span><span class="sxs-lookup"><span data-stu-id="b006b-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-520">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-521">Product 2</span></span></td>
<td><span data-ttu-id="b006b-522">15</span><span class="sxs-lookup"><span data-stu-id="b006b-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-523">**Bemærk!** I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="b006b-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b006b-524">Du kan finde mere detaljerede oplysninger om providere af statistiske målinger under Skabeloner til providere af statistiske målinger.</span><span class="sxs-lookup"><span data-stu-id="b006b-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="b006b-525">(Bemærk, at dette emne ikke er færdigt endnu, men kommer snart). Tabellen nedenfor viser resultatet, når HR tjenester anvendes som tildelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="b006b-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-526">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-526">Cost object</span></span></th>
<th><span data-ttu-id="b006b-527">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-527">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-528">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-528">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-529">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-529">Amount</span></span></th>
<th><span data-ttu-id="b006b-530">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-531">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-531">CC002</span></span></td>
<td><span data-ttu-id="b006b-532">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-532">Finance</span></span></td>
<td><span data-ttu-id="b006b-533">35</span><span class="sxs-lookup"><span data-stu-id="b006b-533">35</span></span></td>
<td><span data-ttu-id="b006b-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b006b-535">175.00</span><span class="sxs-lookup"><span data-stu-id="b006b-535">175.00</span></span></td>
<td><span data-ttu-id="b006b-536">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-537">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-537">CC003</span></span></td>
<td><span data-ttu-id="b006b-538">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-538">Assembly</span></span></td>
<td><span data-ttu-id="b006b-539">55</span><span class="sxs-lookup"><span data-stu-id="b006b-539">55</span></span></td>
<td><span data-ttu-id="b006b-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b006b-541">275.00</span><span class="sxs-lookup"><span data-stu-id="b006b-541">275.00</span></span></td>
<td><span data-ttu-id="b006b-542">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-543">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-543">CC004</span></span></td>
<td><span data-ttu-id="b006b-544">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-544">Packaging</span></span></td>
<td><span data-ttu-id="b006b-545">10</span><span class="sxs-lookup"><span data-stu-id="b006b-545">10</span></span></td>
<td><span data-ttu-id="b006b-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b006b-547">50,00</span><span class="sxs-lookup"><span data-stu-id="b006b-547">50.00</span></span></td>
<td><span data-ttu-id="b006b-548">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-549">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-549">CC002</span></span></td>
<td><span data-ttu-id="b006b-550">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-550">Finance</span></span></td>
<td><span data-ttu-id="b006b-551">35</span><span class="sxs-lookup"><span data-stu-id="b006b-551">35</span></span></td>
<td><span data-ttu-id="b006b-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b006b-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b006b-553">436.00</span><span class="sxs-lookup"><span data-stu-id="b006b-553">436.00</span></span></td>
<td><span data-ttu-id="b006b-554">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-555">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-555">CC003</span></span></td>
<td><span data-ttu-id="b006b-556">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-556">Assembly</span></span></td>
<td><span data-ttu-id="b006b-557">55</span><span class="sxs-lookup"><span data-stu-id="b006b-557">55</span></span></td>
<td><span data-ttu-id="b006b-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b006b-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b006b-559">685.14</span><span class="sxs-lookup"><span data-stu-id="b006b-559">685.14</span></span></td>
<td><span data-ttu-id="b006b-560">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-561">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-561">CC004</span></span></td>
<td><span data-ttu-id="b006b-562">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-562">Packaging</span></span></td>
<td><span data-ttu-id="b006b-563">10</span><span class="sxs-lookup"><span data-stu-id="b006b-563">10</span></span></td>
<td><span data-ttu-id="b006b-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b006b-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b006b-565">124.57</span><span class="sxs-lookup"><span data-stu-id="b006b-565">124.57</span></span></td>
<td><span data-ttu-id="b006b-566">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-567">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="b006b-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-568">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-568">Cost object</span></span></th>
<th><span data-ttu-id="b006b-569">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-569">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-570">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-570">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-571">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-571">Amount</span></span></th>
<th><span data-ttu-id="b006b-572">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-573">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-573">CC003</span></span></td>
<td><span data-ttu-id="b006b-574">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-574">Assembly</span></span></td>
<td><span data-ttu-id="b006b-575">65</span><span class="sxs-lookup"><span data-stu-id="b006b-575">65</span></span></td>
<td><span data-ttu-id="b006b-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b006b-577">438.75</span><span class="sxs-lookup"><span data-stu-id="b006b-577">438.75</span></span></td>
<td><span data-ttu-id="b006b-578">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-579">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-579">CC004</span></span></td>
<td><span data-ttu-id="b006b-580">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-580">Packaging</span></span></td>
<td><span data-ttu-id="b006b-581">35</span><span class="sxs-lookup"><span data-stu-id="b006b-581">35</span></span></td>
<td><span data-ttu-id="b006b-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b006b-583">236.25</span><span class="sxs-lookup"><span data-stu-id="b006b-583">236.25</span></span></td>
<td><span data-ttu-id="b006b-584">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-585">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-585">CC003</span></span></td>
<td><span data-ttu-id="b006b-586">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-586">Assembly</span></span></td>
<td><span data-ttu-id="b006b-587">65</span><span class="sxs-lookup"><span data-stu-id="b006b-587">65</span></span></td>
<td><span data-ttu-id="b006b-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b006b-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b006b-589">5,297.69</span></span></td>
<td><span data-ttu-id="b006b-590">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-591">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-591">CC004</span></span></td>
<td><span data-ttu-id="b006b-592">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-592">Packaging</span></span></td>
<td><span data-ttu-id="b006b-593">35</span><span class="sxs-lookup"><span data-stu-id="b006b-593">35</span></span></td>
<td><span data-ttu-id="b006b-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b006b-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b006b-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b006b-595">2,852.60</span></span></td>
<td><span data-ttu-id="b006b-596">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-597">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="b006b-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-598">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-598">Cost object</span></span></th>
<th><span data-ttu-id="b006b-599">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-599">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-600">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-600">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-601">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-601">Amount</span></span></th>
<th><span data-ttu-id="b006b-602">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-603">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-604">Product 1</span></span></td>
<td><span data-ttu-id="b006b-605">60</span><span class="sxs-lookup"><span data-stu-id="b006b-605">60</span></span></td>
<td><span data-ttu-id="b006b-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b006b-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b006b-607">535.31</span><span class="sxs-lookup"><span data-stu-id="b006b-607">535.31</span></span></td>
<td><span data-ttu-id="b006b-608">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-609">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-610">Product 2</span></span></td>
<td><span data-ttu-id="b006b-611">20</span><span class="sxs-lookup"><span data-stu-id="b006b-611">20</span></span></td>
<td><span data-ttu-id="b006b-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b006b-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b006b-613">178.44</span><span class="sxs-lookup"><span data-stu-id="b006b-613">178.44</span></span></td>
<td><span data-ttu-id="b006b-614">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-615">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-616">Product 1</span></span></td>
<td><span data-ttu-id="b006b-617">60</span><span class="sxs-lookup"><span data-stu-id="b006b-617">60</span></span></td>
<td><span data-ttu-id="b006b-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b006b-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b006b-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b006b-619">4,487.12</span></span></td>
<td><span data-ttu-id="b006b-620">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-621">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-622">Product 2</span></span></td>
<td><span data-ttu-id="b006b-623">20</span><span class="sxs-lookup"><span data-stu-id="b006b-623">20</span></span></td>
<td><span data-ttu-id="b006b-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b006b-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b006b-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b006b-625">1,495.71</span></span></td>
<td><span data-ttu-id="b006b-626">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b006b-627">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="b006b-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-628">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-628">Cost object</span></span></th>
<th><span data-ttu-id="b006b-629">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="b006b-629">Magnitude</span></span></th>
<th><span data-ttu-id="b006b-630">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="b006b-630">Allocation factor</span></span></th>
<th><span data-ttu-id="b006b-631">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-631">Amount</span></span></th>
<th><span data-ttu-id="b006b-632">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-633">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-634">Product 1</span></span></td>
<td><span data-ttu-id="b006b-635">80</span><span class="sxs-lookup"><span data-stu-id="b006b-635">80</span></span></td>
<td><span data-ttu-id="b006b-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b006b-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b006b-637">241.05</span><span class="sxs-lookup"><span data-stu-id="b006b-637">241.05</span></span></td>
<td><span data-ttu-id="b006b-638">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-639">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-640">Product 2</span></span></td>
<td><span data-ttu-id="b006b-641">15</span><span class="sxs-lookup"><span data-stu-id="b006b-641">15</span></span></td>
<td><span data-ttu-id="b006b-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b006b-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b006b-643">45.20</span><span class="sxs-lookup"><span data-stu-id="b006b-643">45.20</span></span></td>
<td><span data-ttu-id="b006b-644">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-645">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-646">Product 1</span></span></td>
<td><span data-ttu-id="b006b-647">80</span><span class="sxs-lookup"><span data-stu-id="b006b-647">80</span></span></td>
<td><span data-ttu-id="b006b-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b006b-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b006b-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b006b-649">2,507.09</span></span></td>
<td><span data-ttu-id="b006b-650">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-651">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-652">Product 2</span></span></td>
<td><span data-ttu-id="b006b-653">15</span><span class="sxs-lookup"><span data-stu-id="b006b-653">15</span></span></td>
<td><span data-ttu-id="b006b-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b006b-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b006b-655">470.08</span><span class="sxs-lookup"><span data-stu-id="b006b-655">470.08</span></span></td>
<td><span data-ttu-id="b006b-656">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b006b-657">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="b006b-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-658">Kladden</span><span class="sxs-lookup"><span data-stu-id="b006b-658">Journal</span></span></th>
<th><span data-ttu-id="b006b-659">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="b006b-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b006b-660">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="b006b-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b006b-661">Version</span><span class="sxs-lookup"><span data-stu-id="b006b-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-662">00004</span><span class="sxs-lookup"><span data-stu-id="b006b-662">00004</span></span></td>
<td><span data-ttu-id="b006b-663">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="b006b-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b006b-664">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="b006b-664">Fiscal</span></span></td>
<td><span data-ttu-id="b006b-665">2017</span><span class="sxs-lookup"><span data-stu-id="b006b-665">2017</span></span></td>
<td><span data-ttu-id="b006b-666">1. Periode</span><span class="sxs-lookup"><span data-stu-id="b006b-666">Period 1</span></span></td>
<td><span data-ttu-id="b006b-667">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="b006b-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b006b-668">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="b006b-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b006b-669">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-670">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-671">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-671">Cost element</span></span></th>
<th><span data-ttu-id="b006b-672">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-672">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-673">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-674">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-675">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-675">CC001</span></span></td>
<td><span data-ttu-id="b006b-676">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-676">HR</span></span></td>
<td><span data-ttu-id="b006b-677">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-677">10001</span></span></td>
<td><span data-ttu-id="b006b-678">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-678">Electricity</span></span></td>
<td><span data-ttu-id="b006b-679">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-679">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-680">500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-681">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-682">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-682">CC001</span></span></td>
<td><span data-ttu-id="b006b-683">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-683">HR</span></span></td>
<td><span data-ttu-id="b006b-684">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-684">10001</span></span></td>
<td><span data-ttu-id="b006b-685">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-685">Electricity</span></span></td>
<td><span data-ttu-id="b006b-686">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-686">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b006b-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-688">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-689">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-689">CC002</span></span></td>
<td><span data-ttu-id="b006b-690">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-690">Finance</span></span></td>
<td><span data-ttu-id="b006b-691">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-691">10001</span></span></td>
<td><span data-ttu-id="b006b-692">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-692">Electricity</span></span></td>
<td><span data-ttu-id="b006b-693">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-693">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-694">675.00</span><span class="sxs-lookup"><span data-stu-id="b006b-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-695">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-696">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-696">CC002</span></span></td>
<td><span data-ttu-id="b006b-697">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-697">Finance</span></span></td>
<td><span data-ttu-id="b006b-698">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-698">10001</span></span></td>
<td><span data-ttu-id="b006b-699">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-699">Electricity</span></span></td>
<td><span data-ttu-id="b006b-700">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-700">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b006b-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-702">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-703">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-703">CC003</span></span></td>
<td><span data-ttu-id="b006b-704">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-704">Assembly</span></span></td>
<td><span data-ttu-id="b006b-705">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-705">10001</span></span></td>
<td><span data-ttu-id="b006b-706">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-706">Electricity</span></span></td>
<td><span data-ttu-id="b006b-707">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-707">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-708">713.75</span><span class="sxs-lookup"><span data-stu-id="b006b-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-709">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-710">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-710">CC003</span></span></td>
<td><span data-ttu-id="b006b-711">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-711">Assembly</span></span></td>
<td><span data-ttu-id="b006b-712">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-712">10001</span></span></td>
<td><span data-ttu-id="b006b-713">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-713">Electricity</span></span></td>
<td><span data-ttu-id="b006b-714">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-714">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b006b-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-716">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-717">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-717">CC003</span></span></td>
<td><span data-ttu-id="b006b-718">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-718">Packaging</span></span></td>
<td><span data-ttu-id="b006b-719">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-719">10001</span></span></td>
<td><span data-ttu-id="b006b-720">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-720">Electricity</span></span></td>
<td><span data-ttu-id="b006b-721">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-721">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-722">286.25</span><span class="sxs-lookup"><span data-stu-id="b006b-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-723">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-724">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-724">CC003</span></span></td>
<td><span data-ttu-id="b006b-725">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-725">Packaging</span></span></td>
<td><span data-ttu-id="b006b-726">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-726">10001</span></span></td>
<td><span data-ttu-id="b006b-727">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-727">Electricity</span></span></td>
<td><span data-ttu-id="b006b-728">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-728">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b006b-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-730">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-731">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-732">Product 1</span></span></td>
<td><span data-ttu-id="b006b-733">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-733">10001</span></span></td>
<td><span data-ttu-id="b006b-734">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-734">Electricity</span></span></td>
<td><span data-ttu-id="b006b-735">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-735">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-736">776.36</span><span class="sxs-lookup"><span data-stu-id="b006b-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-737">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-738">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-739">Product 1</span></span></td>
<td><span data-ttu-id="b006b-740">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-740">10001</span></span></td>
<td><span data-ttu-id="b006b-741">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-741">Electricity</span></span></td>
<td><span data-ttu-id="b006b-742">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-742">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b006b-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-744">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-745">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-746">Product 1</span></span></td>
<td><span data-ttu-id="b006b-747">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-747">10001</span></span></td>
<td><span data-ttu-id="b006b-748">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-748">Electricity</span></span></td>
<td><span data-ttu-id="b006b-749">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-749">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-750">223.64</span><span class="sxs-lookup"><span data-stu-id="b006b-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-751">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="b006b-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-752">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-753">Product 1</span></span></td>
<td><span data-ttu-id="b006b-754">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-754">10001</span></span></td>
<td><span data-ttu-id="b006b-755">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-755">Electricity</span></span></td>
<td><span data-ttu-id="b006b-756">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-756">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b006b-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b006b-758">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="b006b-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b006b-759">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b006b-760">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-760">Cost element</span></span></th>
<th><span data-ttu-id="b006b-761">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-761">Cost behavior</span></span></th>
<th><span data-ttu-id="b006b-762">Beløb</span><span class="sxs-lookup"><span data-stu-id="b006b-762">Amount</span></span></th>
<th><span data-ttu-id="b006b-763">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="b006b-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b006b-764">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-764">CC001</span></span></td>
<td><span data-ttu-id="b006b-765">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-765">HR</span></span></td>
<td><span data-ttu-id="b006b-766">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-766">10001</span></span></td>
<td><span data-ttu-id="b006b-767">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-767">Electricity</span></span></td>
<td><span data-ttu-id="b006b-768">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-768">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="b006b-769">-500.00</span></span></td>
<td><span data-ttu-id="b006b-770">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-771">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-771">CC002</span></span></td>
<td><span data-ttu-id="b006b-772">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-772">Finance</span></span></td>
<td><span data-ttu-id="b006b-773">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-773">10001</span></span></td>
<td><span data-ttu-id="b006b-774">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-774">Electricity</span></span></td>
<td><span data-ttu-id="b006b-775">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-775">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-776">175.00</span><span class="sxs-lookup"><span data-stu-id="b006b-776">175.00</span></span></td>
<td><span data-ttu-id="b006b-777">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-778">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-778">CC003</span></span></td>
<td><span data-ttu-id="b006b-779">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-779">Assembly</span></span></td>
<td><span data-ttu-id="b006b-780">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-780">10001</span></span></td>
<td><span data-ttu-id="b006b-781">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-781">Electricity</span></span></td>
<td><span data-ttu-id="b006b-782">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-782">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-783">275.00</span><span class="sxs-lookup"><span data-stu-id="b006b-783">275.00</span></span></td>
<td><span data-ttu-id="b006b-784">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-785">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-785">CC004</span></span></td>
<td><span data-ttu-id="b006b-786">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-786">Packaging</span></span></td>
<td><span data-ttu-id="b006b-787">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-787">10001</span></span></td>
<td><span data-ttu-id="b006b-788">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-788">Electricity</span></span></td>
<td><span data-ttu-id="b006b-789">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-789">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-790">50,00</span><span class="sxs-lookup"><span data-stu-id="b006b-790">50,00</span></span></td>
<td><span data-ttu-id="b006b-791">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-792">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-792">CC001</span></span></td>
<td><span data-ttu-id="b006b-793">Personale</span><span class="sxs-lookup"><span data-stu-id="b006b-793">HR</span></span></td>
<td><span data-ttu-id="b006b-794">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-794">10001</span></span></td>
<td><span data-ttu-id="b006b-795">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-795">Electricity</span></span></td>
<td><span data-ttu-id="b006b-796">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-796">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="b006b-797">-1,245.71</span></span></td>
<td><span data-ttu-id="b006b-798">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-799">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-799">CC002</span></span></td>
<td><span data-ttu-id="b006b-800">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-800">Finance</span></span></td>
<td><span data-ttu-id="b006b-801">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-801">10001</span></span></td>
<td><span data-ttu-id="b006b-802">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-802">Electricity</span></span></td>
<td><span data-ttu-id="b006b-803">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-803">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-804">436.00</span><span class="sxs-lookup"><span data-stu-id="b006b-804">436.00</span></span></td>
<td><span data-ttu-id="b006b-805">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-806">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-806">CC003</span></span></td>
<td><span data-ttu-id="b006b-807">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-807">Assembly</span></span></td>
<td><span data-ttu-id="b006b-808">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-808">10001</span></span></td>
<td><span data-ttu-id="b006b-809">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-809">Electricity</span></span></td>
<td><span data-ttu-id="b006b-810">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-810">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-811">685.14</span><span class="sxs-lookup"><span data-stu-id="b006b-811">685.14</span></span></td>
<td><span data-ttu-id="b006b-812">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-813">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-813">CC004</span></span></td>
<td><span data-ttu-id="b006b-814">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-814">Packaging</span></span></td>
<td><span data-ttu-id="b006b-815">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-815">10001</span></span></td>
<td><span data-ttu-id="b006b-816">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-816">Electricity</span></span></td>
<td><span data-ttu-id="b006b-817">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-817">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-818">124.57</span><span class="sxs-lookup"><span data-stu-id="b006b-818">124.57</span></span></td>
<td><span data-ttu-id="b006b-819">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-820">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-820">CC002</span></span></td>
<td><span data-ttu-id="b006b-821">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-821">Finance</span></span></td>
<td><span data-ttu-id="b006b-822">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-822">10001</span></span></td>
<td><span data-ttu-id="b006b-823">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-823">Electricity</span></span></td>
<td><span data-ttu-id="b006b-824">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-824">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="b006b-825">-675.00</span></span></td>
<td><span data-ttu-id="b006b-826">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-827">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-827">CC003</span></span></td>
<td><span data-ttu-id="b006b-828">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-828">Assembly</span></span></td>
<td><span data-ttu-id="b006b-829">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-829">10001</span></span></td>
<td><span data-ttu-id="b006b-830">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-830">Electricity</span></span></td>
<td><span data-ttu-id="b006b-831">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-831">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-832">438.75</span><span class="sxs-lookup"><span data-stu-id="b006b-832">438.75</span></span></td>
<td><span data-ttu-id="b006b-833">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-834">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-834">CC004</span></span></td>
<td><span data-ttu-id="b006b-835">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-835">Packaging</span></span></td>
<td><span data-ttu-id="b006b-836">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-836">10001</span></span></td>
<td><span data-ttu-id="b006b-837">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-837">Electricity</span></span></td>
<td><span data-ttu-id="b006b-838">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-838">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-839">236.25</span><span class="sxs-lookup"><span data-stu-id="b006b-839">236.25</span></span></td>
<td><span data-ttu-id="b006b-840">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-841">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-841">CC002</span></span></td>
<td><span data-ttu-id="b006b-842">Finans</span><span class="sxs-lookup"><span data-stu-id="b006b-842">Finance</span></span></td>
<td><span data-ttu-id="b006b-843">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-843">10001</span></span></td>
<td><span data-ttu-id="b006b-844">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-844">Electricity</span></span></td>
<td><span data-ttu-id="b006b-845">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-845">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="b006b-846">-8,150.29</span></span></td>
<td><span data-ttu-id="b006b-847">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-848">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-848">CC003</span></span></td>
<td><span data-ttu-id="b006b-849">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-849">Assembly</span></span></td>
<td><span data-ttu-id="b006b-850">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-850">10001</span></span></td>
<td><span data-ttu-id="b006b-851">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-851">Electricity</span></span></td>
<td><span data-ttu-id="b006b-852">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-852">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b006b-853">5,297.69</span></span></td>
<td><span data-ttu-id="b006b-854">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-855">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-855">CC004</span></span></td>
<td><span data-ttu-id="b006b-856">Emballage</span><span class="sxs-lookup"><span data-stu-id="b006b-856">Packaging</span></span></td>
<td><span data-ttu-id="b006b-857">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-857">10001</span></span></td>
<td><span data-ttu-id="b006b-858">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-858">Electricity</span></span></td>
<td><span data-ttu-id="b006b-859">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-859">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b006b-860">2,852.60</span></span></td>
<td><span data-ttu-id="b006b-861">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-862">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-862">CC003</span></span></td>
<td><span data-ttu-id="b006b-863">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-863">Assembly</span></span></td>
<td><span data-ttu-id="b006b-864">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-864">10001</span></span></td>
<td><span data-ttu-id="b006b-865">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-865">Electricity</span></span></td>
<td><span data-ttu-id="b006b-866">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-866">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="b006b-867">-713.75</span></span></td>
<td><span data-ttu-id="b006b-868">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-869">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-870">Product 1</span></span></td>
<td><span data-ttu-id="b006b-871">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-871">10001</span></span></td>
<td><span data-ttu-id="b006b-872">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-872">Electricity</span></span></td>
<td><span data-ttu-id="b006b-873">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-873">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-874">535.31</span><span class="sxs-lookup"><span data-stu-id="b006b-874">535.31</span></span></td>
<td><span data-ttu-id="b006b-875">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-876">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-877">Product 2</span></span></td>
<td><span data-ttu-id="b006b-878">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-878">10001</span></span></td>
<td><span data-ttu-id="b006b-879">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-879">Electricity</span></span></td>
<td><span data-ttu-id="b006b-880">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-880">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-881">178.44</span><span class="sxs-lookup"><span data-stu-id="b006b-881">178.44</span></span></td>
<td><span data-ttu-id="b006b-882">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-883">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-883">CC003</span></span></td>
<td><span data-ttu-id="b006b-884">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-884">Assembly</span></span></td>
<td><span data-ttu-id="b006b-885">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-885">10001</span></span></td>
<td><span data-ttu-id="b006b-886">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-886">Electricity</span></span></td>
<td><span data-ttu-id="b006b-887">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-887">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="b006b-888">-5,982.83</span></span></td>
<td><span data-ttu-id="b006b-889">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-890">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-891">Product 1</span></span></td>
<td><span data-ttu-id="b006b-892">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-892">10001</span></span></td>
<td><span data-ttu-id="b006b-893">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-893">Electricity</span></span></td>
<td><span data-ttu-id="b006b-894">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-894">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b006b-895">4,487.12</span></span></td>
<td><span data-ttu-id="b006b-896">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-897">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-898">Product 2</span></span></td>
<td><span data-ttu-id="b006b-899">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-899">10001</span></span></td>
<td><span data-ttu-id="b006b-900">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-900">Electricity</span></span></td>
<td><span data-ttu-id="b006b-901">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-901">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b006b-902">1,495.71</span></span></td>
<td><span data-ttu-id="b006b-903">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-904">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-904">CC003</span></span></td>
<td><span data-ttu-id="b006b-905">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-905">Assembly</span></span></td>
<td><span data-ttu-id="b006b-906">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-906">10001</span></span></td>
<td><span data-ttu-id="b006b-907">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-907">Electricity</span></span></td>
<td><span data-ttu-id="b006b-908">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-908">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="b006b-909">-286.25</span></span></td>
<td><span data-ttu-id="b006b-910">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-911">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-912">Product 1</span></span></td>
<td><span data-ttu-id="b006b-913">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-913">10001</span></span></td>
<td><span data-ttu-id="b006b-914">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-914">Electricity</span></span></td>
<td><span data-ttu-id="b006b-915">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-915">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-916">241.05</span><span class="sxs-lookup"><span data-stu-id="b006b-916">241.05</span></span></td>
<td><span data-ttu-id="b006b-917">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-918">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-919">Product 2</span></span></td>
<td><span data-ttu-id="b006b-920">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-920">10001</span></span></td>
<td><span data-ttu-id="b006b-921">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-921">Electricity</span></span></td>
<td><span data-ttu-id="b006b-922">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-922">Fixed cost</span></span></td>
<td><span data-ttu-id="b006b-923">45.20</span><span class="sxs-lookup"><span data-stu-id="b006b-923">45.20</span></span></td>
<td><span data-ttu-id="b006b-924">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-925">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-925">CC003</span></span></td>
<td><span data-ttu-id="b006b-926">Samling</span><span class="sxs-lookup"><span data-stu-id="b006b-926">Assembly</span></span></td>
<td><span data-ttu-id="b006b-927">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-927">10001</span></span></td>
<td><span data-ttu-id="b006b-928">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-928">Electricity</span></span></td>
<td><span data-ttu-id="b006b-929">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-929">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="b006b-930">-2,977.17</span></span></td>
<td><span data-ttu-id="b006b-931">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-932">Prod 1</span></span></td>
<td><span data-ttu-id="b006b-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="b006b-933">Product 1</span></span></td>
<td><span data-ttu-id="b006b-934">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-934">10001</span></span></td>
<td><span data-ttu-id="b006b-935">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-935">Electricity</span></span></td>
<td><span data-ttu-id="b006b-936">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-936">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b006b-937">2,507.09</span></span></td>
<td><span data-ttu-id="b006b-938">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b006b-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-939">Prod 2</span></span></td>
<td><span data-ttu-id="b006b-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="b006b-940">Product 2</span></span></td>
<td><span data-ttu-id="b006b-941">10001</span><span class="sxs-lookup"><span data-stu-id="b006b-941">10001</span></span></td>
<td><span data-ttu-id="b006b-942">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-942">Electricity</span></span></td>
<td><span data-ttu-id="b006b-943">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-943">Variable cost</span></span></td>
<td><span data-ttu-id="b006b-944">470.08</span><span class="sxs-lookup"><span data-stu-id="b006b-944">470.08</span></span></td>
<td><span data-ttu-id="b006b-945">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="b006b-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b006b-946">Konklusion</span><span class="sxs-lookup"><span data-stu-id="b006b-946">Conclusion</span></span>
<span data-ttu-id="b006b-947">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="b006b-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b006b-948">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="b006b-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b006b-949">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="b006b-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b006b-950">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b006b-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b006b-951">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="b006b-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b006b-952">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b006b-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b006b-953">Samlet</span><span class="sxs-lookup"><span data-stu-id="b006b-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b006b-954">CC099</span><span class="sxs-lookup"><span data-stu-id="b006b-954">CC099</span></span></th>
<th><span data-ttu-id="b006b-955">CC001</span><span class="sxs-lookup"><span data-stu-id="b006b-955">CC001</span></span></th>
<th><span data-ttu-id="b006b-956">CC002</span><span class="sxs-lookup"><span data-stu-id="b006b-956">CC002</span></span></th>
<th><span data-ttu-id="b006b-957">CC003</span><span class="sxs-lookup"><span data-stu-id="b006b-957">CC003</span></span></th>
<th><span data-ttu-id="b006b-958">CC004</span><span class="sxs-lookup"><span data-stu-id="b006b-958">CC004</span></span></th>
<th><span data-ttu-id="b006b-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b006b-959">Proj 1</span></span></th>
<th><span data-ttu-id="b006b-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b006b-960">Proj 2</span></span></th>
<th><span data-ttu-id="b006b-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b006b-961">Prod 1</span></span></th>
<th><span data-ttu-id="b006b-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b006b-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b006b-963">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="b006b-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b006b-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b006b-973">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="b006b-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b006b-975">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-978">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-979">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-980">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b006b-981">776.36</span><span class="sxs-lookup"><span data-stu-id="b006b-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-982">223.64</span><span class="sxs-lookup"><span data-stu-id="b006b-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b006b-984">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="b006b-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-985">000</span><span class="sxs-lookup"><span data-stu-id="b006b-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-987">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-988">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-989">0,00</span><span class="sxs-lookup"><span data-stu-id="b006b-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-990">30,00</span><span class="sxs-lookup"><span data-stu-id="b006b-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-991">10,00</span><span class="sxs-lookup"><span data-stu-id="b006b-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b006b-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b006b-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b006b-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b006b-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b006b-995">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="b006b-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b006b-996">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="b006b-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b006b-997">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="b006b-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b006b-998">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="b006b-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b006b-999">Du kan finde flere oplysninger under Politik for omkostningstotaler.</span><span class="sxs-lookup"><span data-stu-id="b006b-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="b006b-1000">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="b006b-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




