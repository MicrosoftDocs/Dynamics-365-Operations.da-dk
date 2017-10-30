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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 285799d70a945c2dae1e3c65296282d5c432a243
ms.contentlocale: da-dk
ms.lasthandoff: 10/30/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="81b0c-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="81b0c-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="81b0c-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="81b0c-105">Term definition</span></span>
---------------

<span data-ttu-id="81b0c-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="81b0c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="81b0c-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="81b0c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="81b0c-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="81b0c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="81b0c-109">Leje</span><span class="sxs-lookup"><span data-stu-id="81b0c-109">Rent</span></span>
-   <span data-ttu-id="81b0c-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-110">Electricity</span></span>
-   <span data-ttu-id="81b0c-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="81b0c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="81b0c-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-112">Overhead calculation overview</span></span>
<span data-ttu-id="81b0c-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="81b0c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="81b0c-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="81b0c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="81b0c-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="81b0c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="81b0c-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="81b0c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="81b0c-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="81b0c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="81b0c-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="81b0c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="81b0c-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="81b0c-119">Version type</span></span>
-   <span data-ttu-id="81b0c-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="81b0c-120">Date and time</span></span>
-   <span data-ttu-id="81b0c-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="81b0c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="81b0c-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="81b0c-122">Fiscal year</span></span>
-   <span data-ttu-id="81b0c-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="81b0c-123">Fiscal period</span></span>

<span data-ttu-id="81b0c-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="81b0c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="81b0c-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="81b0c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="81b0c-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="81b0c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="81b0c-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="81b0c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="81b0c-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="81b0c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="81b0c-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="81b0c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="81b0c-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="81b0c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="81b0c-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="81b0c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="81b0c-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="81b0c-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="81b0c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="81b0c-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="81b0c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="81b0c-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="81b0c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="81b0c-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="81b0c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="81b0c-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="81b0c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="81b0c-140">Main account</span></span></th>
<th><span data-ttu-id="81b0c-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="81b0c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="81b0c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-143">CC099</span></span></td>
<td><span data-ttu-id="81b0c-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-144">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-145">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-145">10001</span></span></td>
<td><span data-ttu-id="81b0c-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-146">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="81b0c-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="81b0c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="81b0c-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="81b0c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="81b0c-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="81b0c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="81b0c-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="81b0c-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="81b0c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="81b0c-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="81b0c-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="81b0c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="81b0c-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="81b0c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="81b0c-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="81b0c-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="81b0c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="81b0c-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="81b0c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="81b0c-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-160">Journal</span></span></th>
<th><span data-ttu-id="81b0c-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="81b0c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="81b0c-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="81b0c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="81b0c-163">Version</span><span class="sxs-lookup"><span data-stu-id="81b0c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-164">00001</span><span class="sxs-lookup"><span data-stu-id="81b0c-164">00001</span></span></td>
<td><span data-ttu-id="81b0c-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="81b0c-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="81b0c-166">Fiscal</span></span></td>
<td><span data-ttu-id="81b0c-167">2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-167">2017</span></span></td>
<td><span data-ttu-id="81b0c-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="81b0c-168">Period 1</span></span></td>
<td><span data-ttu-id="81b0c-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="81b0c-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="81b0c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-173">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="81b0c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-177">CC099</span></span></td>
<td><span data-ttu-id="81b0c-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-178">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-179">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-179">10001</span></span></td>
<td><span data-ttu-id="81b0c-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-180">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="81b0c-181">Unclassified</span></span></td>
<td><span data-ttu-id="81b0c-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="81b0c-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="81b0c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-185">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-187">Amount</span></span></th>
<th><span data-ttu-id="81b0c-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-189">CC099</span></span></td>
<td><span data-ttu-id="81b0c-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-190">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-191">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-191">10001</span></span></td>
<td><span data-ttu-id="81b0c-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-192">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="81b0c-193">Unclassified</span></span></td>
<td><span data-ttu-id="81b0c-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-194">10,000.00</span></span></td>
<td><span data-ttu-id="81b0c-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-196">CC099</span></span></td>
<td><span data-ttu-id="81b0c-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-197">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-198">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-198">10001</span></span></td>
<td><span data-ttu-id="81b0c-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-199">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="81b0c-200">Unclassified</span></span></td>
<td><span data-ttu-id="81b0c-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="81b0c-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-203">CC099</span></span></td>
<td><span data-ttu-id="81b0c-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-204">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-205">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-205">10001</span></span></td>
<td><span data-ttu-id="81b0c-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-206">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-208">1,000.00</span></span></td>
<td><span data-ttu-id="81b0c-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-210">CC099</span></span></td>
<td><span data-ttu-id="81b0c-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-211">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-212">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-212">10001</span></span></td>
<td><span data-ttu-id="81b0c-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-213">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-214">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-215">9,000.00</span></span></td>
<td><span data-ttu-id="81b0c-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-217">Du kan finde detaljerede oplysninger om funktionalitet af omkostninger under Politik for funktionalitet af omkostning.</span><span class="sxs-lookup"><span data-stu-id="81b0c-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="81b0c-218">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="81b0c-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="81b0c-219">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="81b0c-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="81b0c-220">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="81b0c-221">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="81b0c-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="81b0c-222">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="81b0c-222">Define the cost distribution rule</span></span>

<span data-ttu-id="81b0c-223">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="81b0c-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="81b0c-224">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="81b0c-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="81b0c-225">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="81b0c-226">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="81b0c-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="81b0c-227">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="81b0c-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="81b0c-228">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-229">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-229">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-230">KWh</span><span class="sxs-lookup"><span data-stu-id="81b0c-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-231">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-231">CC001</span></span></td>
<td><span data-ttu-id="81b0c-232">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-232">HR</span></span></td>
<td><span data-ttu-id="81b0c-233">1.000</span><span class="sxs-lookup"><span data-stu-id="81b0c-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-234">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-234">CC002</span></span></td>
<td><span data-ttu-id="81b0c-235">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-235">Finance</span></span></td>
<td><span data-ttu-id="81b0c-236">6.000</span><span class="sxs-lookup"><span data-stu-id="81b0c-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-237">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-237">CC003</span></span></td>
<td><span data-ttu-id="81b0c-238">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-238">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-239">0</span><span class="sxs-lookup"><span data-stu-id="81b0c-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-240">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-241">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-241">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-242">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-242">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-243">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-243">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-244">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-245">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-245">CC001</span></span></td>
<td><span data-ttu-id="81b0c-246">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-246">HR</span></span></td>
<td><span data-ttu-id="81b0c-247">1.000</span><span class="sxs-lookup"><span data-stu-id="81b0c-247">1,000</span></span></td>
<td><span data-ttu-id="81b0c-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="81b0c-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="81b0c-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-250">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-250">CC002</span></span></td>
<td><span data-ttu-id="81b0c-251">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-251">Finance</span></span></td>
<td><span data-ttu-id="81b0c-252">6.000</span><span class="sxs-lookup"><span data-stu-id="81b0c-252">6,000</span></span></td>
<td><span data-ttu-id="81b0c-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="81b0c-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="81b0c-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-255">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-255">CC003</span></span></td>
<td><span data-ttu-id="81b0c-256">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-256">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-257">0</span><span class="sxs-lookup"><span data-stu-id="81b0c-257">0</span></span></td>
<td><span data-ttu-id="81b0c-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="81b0c-259">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-260">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="81b0c-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="81b0c-261">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-262">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-262">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-263">Formel</span><span class="sxs-lookup"><span data-stu-id="81b0c-263">Formula</span></span></th>
<th><span data-ttu-id="81b0c-264">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-264">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-265">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-265">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-266">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-267">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-267">CC001</span></span></td>
<td><span data-ttu-id="81b0c-268">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-268">HR</span></span></td>
<td><span data-ttu-id="81b0c-269">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="81b0c-270">1</span><span class="sxs-lookup"><span data-stu-id="81b0c-270">1</span></span></td>
<td><span data-ttu-id="81b0c-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="81b0c-272">500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-273">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-273">CC002</span></span></td>
<td><span data-ttu-id="81b0c-274">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-274">Finance</span></span></td>
<td><span data-ttu-id="81b0c-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="81b0c-276">1</span><span class="sxs-lookup"><span data-stu-id="81b0c-276">1</span></span></td>
<td><span data-ttu-id="81b0c-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="81b0c-278">500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-279">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-279">CC003</span></span></td>
<td><span data-ttu-id="81b0c-280">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-280">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="81b0c-282">0</span><span class="sxs-lookup"><span data-stu-id="81b0c-282">0</span></span></td>
<td><span data-ttu-id="81b0c-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="81b0c-284">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="81b0c-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-286">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-286">Journal</span></span></th>
<th><span data-ttu-id="81b0c-287">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="81b0c-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="81b0c-288">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="81b0c-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="81b0c-289">Version</span><span class="sxs-lookup"><span data-stu-id="81b0c-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-290">00002</span><span class="sxs-lookup"><span data-stu-id="81b0c-290">00002</span></span></td>
<td><span data-ttu-id="81b0c-291">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="81b0c-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="81b0c-292">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="81b0c-292">Fiscal</span></span></td>
<td><span data-ttu-id="81b0c-293">2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-293">2017</span></span></td>
<td><span data-ttu-id="81b0c-294">1. Periode</span><span class="sxs-lookup"><span data-stu-id="81b0c-294">Period 1</span></span></td>
<td><span data-ttu-id="81b0c-295">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="81b0c-296">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="81b0c-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-297">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-298">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-299">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-299">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-300">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-300">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-301">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-302">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-303">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-303">CC099</span></span></td>
<td><span data-ttu-id="81b0c-304">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-304">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-305">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-305">10001</span></span></td>
<td><span data-ttu-id="81b0c-306">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-306">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-307">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-307">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-309">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-310">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-310">CC099</span></span></td>
<td><span data-ttu-id="81b0c-311">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-311">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-312">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-312">10001</span></span></td>
<td><span data-ttu-id="81b0c-313">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-313">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-314">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-314">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-315">9.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="81b0c-316">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="81b0c-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-317">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-318">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-318">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-319">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-319">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-320">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-320">Amount</span></span></th>
<th><span data-ttu-id="81b0c-321">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-322">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-322">CC099</span></span></td>
<td><span data-ttu-id="81b0c-323">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-323">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-324">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-324">10001</span></span></td>
<td><span data-ttu-id="81b0c-325">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-325">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-326">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-326">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-327">-1,000.00</span></span></td>
<td><span data-ttu-id="81b0c-328">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-329">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-329">CC001</span></span></td>
<td><span data-ttu-id="81b0c-330">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-330">HR</span></span></td>
<td><span data-ttu-id="81b0c-331">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-331">10001</span></span></td>
<td><span data-ttu-id="81b0c-332">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-332">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-333">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-333">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-334">500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-334">500.00</span></span></td>
<td><span data-ttu-id="81b0c-335">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-336">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-336">CC002</span></span></td>
<td><span data-ttu-id="81b0c-337">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-337">Finance</span></span></td>
<td><span data-ttu-id="81b0c-338">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-338">10001</span></span></td>
<td><span data-ttu-id="81b0c-339">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-339">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-340">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-340">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-341">500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-341">500.00</span></span></td>
<td><span data-ttu-id="81b0c-342">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-343">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-343">CC099</span></span></td>
<td><span data-ttu-id="81b0c-344">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="81b0c-344">Default cost center</span></span></td>
<td><span data-ttu-id="81b0c-345">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-345">10001</span></span></td>
<td><span data-ttu-id="81b0c-346">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-346">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-347">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-347">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-348">-9,000.00</span></span></td>
<td><span data-ttu-id="81b0c-349">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-350">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-350">CC001</span></span></td>
<td><span data-ttu-id="81b0c-351">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-351">HR</span></span></td>
<td><span data-ttu-id="81b0c-352">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-352">10001</span></span></td>
<td><span data-ttu-id="81b0c-353">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-353">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-354">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-354">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="81b0c-355">1,285.71</span></span></td>
<td><span data-ttu-id="81b0c-356">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-357">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-357">CC002</span></span></td>
<td><span data-ttu-id="81b0c-358">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-358">Finance</span></span></td>
<td><span data-ttu-id="81b0c-359">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-359">10001</span></span></td>
<td><span data-ttu-id="81b0c-360">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-360">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-361">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-361">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="81b0c-362">7,714.29</span></span></td>
<td><span data-ttu-id="81b0c-363">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-364">Du kan finde detaljerede oplysninger om omkostningsfordeling og fordelingsgrundlag under Politik for omkostningsfordeling og Fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="81b0c-365">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="81b0c-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="81b0c-366">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="81b0c-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="81b0c-367">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="81b0c-368">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="81b0c-369">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="81b0c-369">Define the overhead rate</span></span>

<span data-ttu-id="81b0c-370">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="81b0c-371">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="81b0c-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-372">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-372">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-373">Timer</span><span class="sxs-lookup"><span data-stu-id="81b0c-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-374">Proj 1</span></span></td>
<td><span data-ttu-id="81b0c-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-375">Project 1</span></span></td>
<td><span data-ttu-id="81b0c-376">3</span><span class="sxs-lookup"><span data-stu-id="81b0c-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-377">Proj 2</span></span></td>
<td><span data-ttu-id="81b0c-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-378">Project 2</span></span></td>
<td><span data-ttu-id="81b0c-379">1</span><span class="sxs-lookup"><span data-stu-id="81b0c-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-380">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="81b0c-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-381">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-381">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-382">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-382">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-383">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-383">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-384">Enheder</span><span class="sxs-lookup"><span data-stu-id="81b0c-384">Units</span></span></th>
<th><span data-ttu-id="81b0c-385">Kurs</span><span class="sxs-lookup"><span data-stu-id="81b0c-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-386">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-386">CC001</span></span></td>
<td><span data-ttu-id="81b0c-387">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-387">HR</span></span></td>
<td><span data-ttu-id="81b0c-388">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-388">10001</span></span></td>
<td><span data-ttu-id="81b0c-389">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-389">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-390">1</span><span class="sxs-lookup"><span data-stu-id="81b0c-390">1</span></span></td>
<td><span data-ttu-id="81b0c-391">10</span><span class="sxs-lookup"><span data-stu-id="81b0c-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-392">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-393">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-393">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-394">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-394">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-395">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-395">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-396">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-396">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-397">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-398">Proj 1</span></span></td>
<td><span data-ttu-id="81b0c-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-399">Project 1</span></span></td>
<td><span data-ttu-id="81b0c-400">3</span><span class="sxs-lookup"><span data-stu-id="81b0c-400">3</span></span></td>
<td><span data-ttu-id="81b0c-401">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-401">10001</span></span></td>
<td><span data-ttu-id="81b0c-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="81b0c-403">30,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-404">Proj 2</span></span></td>
<td><span data-ttu-id="81b0c-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-405">Project 2</span></span></td>
<td><span data-ttu-id="81b0c-406">1</span><span class="sxs-lookup"><span data-stu-id="81b0c-406">1</span></span></td>
<td><span data-ttu-id="81b0c-407">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-407">10001</span></span></td>
<td><span data-ttu-id="81b0c-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="81b0c-409">10,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="81b0c-410">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-411">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-411">Journal</span></span></th>
<th><span data-ttu-id="81b0c-412">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="81b0c-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="81b0c-413">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="81b0c-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="81b0c-414">Version</span><span class="sxs-lookup"><span data-stu-id="81b0c-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-415">00003</span><span class="sxs-lookup"><span data-stu-id="81b0c-415">00003</span></span></td>
<td><span data-ttu-id="81b0c-416">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="81b0c-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="81b0c-417">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="81b0c-417">Fiscal</span></span></td>
<td><span data-ttu-id="81b0c-418">2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-418">2017</span></span></td>
<td><span data-ttu-id="81b0c-419">1. Periode</span><span class="sxs-lookup"><span data-stu-id="81b0c-419">Period 1</span></span></td>
<td><span data-ttu-id="81b0c-420">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="81b0c-421">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="81b0c-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-422">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-423">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-423">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-424">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-425">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-426">Proj 1</span></span></td>
<td><span data-ttu-id="81b0c-427">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="81b0c-428">3,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-429">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-430">Proj 2</span></span></td>
<td><span data-ttu-id="81b0c-431">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="81b0c-432">1,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="81b0c-433">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="81b0c-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-434">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-435">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-435">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-436">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-436">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-437">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-437">Amount</span></span></th>
<th><span data-ttu-id="81b0c-438">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="81b0c-439">CC0001</span></span></td>
<td><span data-ttu-id="81b0c-440">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-440">HR</span></span></td>
<td><span data-ttu-id="81b0c-441">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-441">10001</span></span></td>
<td><span data-ttu-id="81b0c-442">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-442">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-443">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-443">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-444">-30.00</span></span></td>
<td><span data-ttu-id="81b0c-445">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-446">Proj 1</span></span></td>
<td><span data-ttu-id="81b0c-447">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="81b0c-448">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-448">10001</span></span></td>
<td><span data-ttu-id="81b0c-449">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-449">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-450">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-450">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-451">30,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-451">30.00</span></span></td>
<td><span data-ttu-id="81b0c-452">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-453">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-453">CC001</span></span></td>
<td><span data-ttu-id="81b0c-454">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-454">HR</span></span></td>
<td><span data-ttu-id="81b0c-455">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-455">10001</span></span></td>
<td><span data-ttu-id="81b0c-456">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-456">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-457">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-457">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-458">-10.00</span></span></td>
<td><span data-ttu-id="81b0c-459">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-460">Proj 2</span></span></td>
<td><span data-ttu-id="81b0c-461">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="81b0c-462">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-462">10001</span></span></td>
<td><span data-ttu-id="81b0c-463">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-463">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-464">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-464">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-465">10,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-465">10.00</span></span></td>
<td><span data-ttu-id="81b0c-466">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-467">Detaljerede oplysninger om politik for satser for faste omkostninger finder du i Politik for sats for faste omkostninger og Fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="81b0c-468">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="81b0c-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="81b0c-469">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="81b0c-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="81b0c-470">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="81b0c-471">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="81b0c-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="81b0c-472">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="81b0c-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="81b0c-473">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="81b0c-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="81b0c-474">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="81b0c-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="81b0c-475">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="81b0c-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="81b0c-476">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="81b0c-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="81b0c-477">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="81b0c-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="81b0c-478">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="81b0c-478">Define the cost allocation</span></span>

<span data-ttu-id="81b0c-479">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="81b0c-480">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="81b0c-481">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="81b0c-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-482">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-482">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-483">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="81b0c-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-484">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-484">CC002</span></span></td>
<td><span data-ttu-id="81b0c-485">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-485">Finance</span></span></td>
<td><span data-ttu-id="81b0c-486">35</span><span class="sxs-lookup"><span data-stu-id="81b0c-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-487">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-487">CC003</span></span></td>
<td><span data-ttu-id="81b0c-488">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-488">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-489">55</span><span class="sxs-lookup"><span data-stu-id="81b0c-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-490">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-490">CC004</span></span></td>
<td><span data-ttu-id="81b0c-491">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-491">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-492">10</span><span class="sxs-lookup"><span data-stu-id="81b0c-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-493">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="81b0c-494">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="81b0c-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-495">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-495">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-496">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="81b0c-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-497">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-497">CC003</span></span></td>
<td><span data-ttu-id="81b0c-498">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-498">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-499">65</span><span class="sxs-lookup"><span data-stu-id="81b0c-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-500">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-500">CC004</span></span></td>
<td><span data-ttu-id="81b0c-501">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-501">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-502">35</span><span class="sxs-lookup"><span data-stu-id="81b0c-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-503">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="81b0c-504">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="81b0c-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-505">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-505">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-506">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="81b0c-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-507">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-508">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-508">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-509">60</span><span class="sxs-lookup"><span data-stu-id="81b0c-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-510">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-511">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-511">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-512">20</span><span class="sxs-lookup"><span data-stu-id="81b0c-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-513">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="81b0c-514">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="81b0c-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-515">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-515">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-516">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="81b0c-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-517">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-518">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-518">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-519">80</span><span class="sxs-lookup"><span data-stu-id="81b0c-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-520">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-521">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-521">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-522">15</span><span class="sxs-lookup"><span data-stu-id="81b0c-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-523">**Bemærk!** I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="81b0c-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="81b0c-524">Du kan finde mere detaljerede oplysninger om providere af statistiske målinger under Skabeloner til providere af statistiske målinger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="81b0c-525">(Bemærk, at dette emne ikke er færdigt endnu, men kommer snart). Tabellen nedenfor viser resultatet, når HR tjenester anvendes som tildelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="81b0c-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-526">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-526">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-527">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-527">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-528">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-528">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-529">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-529">Amount</span></span></th>
<th><span data-ttu-id="81b0c-530">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-531">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-531">CC002</span></span></td>
<td><span data-ttu-id="81b0c-532">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-532">Finance</span></span></td>
<td><span data-ttu-id="81b0c-533">35</span><span class="sxs-lookup"><span data-stu-id="81b0c-533">35</span></span></td>
<td><span data-ttu-id="81b0c-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="81b0c-535">175.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-535">175.00</span></span></td>
<td><span data-ttu-id="81b0c-536">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-537">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-537">CC003</span></span></td>
<td><span data-ttu-id="81b0c-538">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-538">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-539">55</span><span class="sxs-lookup"><span data-stu-id="81b0c-539">55</span></span></td>
<td><span data-ttu-id="81b0c-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="81b0c-541">275.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-541">275.00</span></span></td>
<td><span data-ttu-id="81b0c-542">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-543">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-543">CC004</span></span></td>
<td><span data-ttu-id="81b0c-544">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-544">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-545">10</span><span class="sxs-lookup"><span data-stu-id="81b0c-545">10</span></span></td>
<td><span data-ttu-id="81b0c-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="81b0c-547">50,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-547">50.00</span></span></td>
<td><span data-ttu-id="81b0c-548">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-549">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-549">CC002</span></span></td>
<td><span data-ttu-id="81b0c-550">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-550">Finance</span></span></td>
<td><span data-ttu-id="81b0c-551">35</span><span class="sxs-lookup"><span data-stu-id="81b0c-551">35</span></span></td>
<td><span data-ttu-id="81b0c-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="81b0c-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="81b0c-553">436.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-553">436.00</span></span></td>
<td><span data-ttu-id="81b0c-554">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-555">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-555">CC003</span></span></td>
<td><span data-ttu-id="81b0c-556">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-556">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-557">55</span><span class="sxs-lookup"><span data-stu-id="81b0c-557">55</span></span></td>
<td><span data-ttu-id="81b0c-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="81b0c-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="81b0c-559">685.14</span><span class="sxs-lookup"><span data-stu-id="81b0c-559">685.14</span></span></td>
<td><span data-ttu-id="81b0c-560">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-561">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-561">CC004</span></span></td>
<td><span data-ttu-id="81b0c-562">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-562">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-563">10</span><span class="sxs-lookup"><span data-stu-id="81b0c-563">10</span></span></td>
<td><span data-ttu-id="81b0c-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="81b0c-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="81b0c-565">124.57</span><span class="sxs-lookup"><span data-stu-id="81b0c-565">124.57</span></span></td>
<td><span data-ttu-id="81b0c-566">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-567">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="81b0c-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-568">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-568">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-569">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-569">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-570">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-570">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-571">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-571">Amount</span></span></th>
<th><span data-ttu-id="81b0c-572">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-573">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-573">CC003</span></span></td>
<td><span data-ttu-id="81b0c-574">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-574">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-575">65</span><span class="sxs-lookup"><span data-stu-id="81b0c-575">65</span></span></td>
<td><span data-ttu-id="81b0c-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="81b0c-577">438.75</span><span class="sxs-lookup"><span data-stu-id="81b0c-577">438.75</span></span></td>
<td><span data-ttu-id="81b0c-578">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-579">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-579">CC004</span></span></td>
<td><span data-ttu-id="81b0c-580">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-580">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-581">35</span><span class="sxs-lookup"><span data-stu-id="81b0c-581">35</span></span></td>
<td><span data-ttu-id="81b0c-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="81b0c-583">236.25</span><span class="sxs-lookup"><span data-stu-id="81b0c-583">236.25</span></span></td>
<td><span data-ttu-id="81b0c-584">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-585">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-585">CC003</span></span></td>
<td><span data-ttu-id="81b0c-586">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-586">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-587">65</span><span class="sxs-lookup"><span data-stu-id="81b0c-587">65</span></span></td>
<td><span data-ttu-id="81b0c-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="81b0c-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="81b0c-589">5,297.69</span></span></td>
<td><span data-ttu-id="81b0c-590">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-591">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-591">CC004</span></span></td>
<td><span data-ttu-id="81b0c-592">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-592">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-593">35</span><span class="sxs-lookup"><span data-stu-id="81b0c-593">35</span></span></td>
<td><span data-ttu-id="81b0c-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="81b0c-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="81b0c-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="81b0c-595">2,852.60</span></span></td>
<td><span data-ttu-id="81b0c-596">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-597">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="81b0c-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-598">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-598">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-599">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-599">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-600">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-600">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-601">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-601">Amount</span></span></th>
<th><span data-ttu-id="81b0c-602">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-603">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-604">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-604">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-605">60</span><span class="sxs-lookup"><span data-stu-id="81b0c-605">60</span></span></td>
<td><span data-ttu-id="81b0c-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="81b0c-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="81b0c-607">535.31</span><span class="sxs-lookup"><span data-stu-id="81b0c-607">535.31</span></span></td>
<td><span data-ttu-id="81b0c-608">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-609">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-610">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-610">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-611">20</span><span class="sxs-lookup"><span data-stu-id="81b0c-611">20</span></span></td>
<td><span data-ttu-id="81b0c-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="81b0c-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="81b0c-613">178.44</span><span class="sxs-lookup"><span data-stu-id="81b0c-613">178.44</span></span></td>
<td><span data-ttu-id="81b0c-614">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-615">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-616">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-616">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-617">60</span><span class="sxs-lookup"><span data-stu-id="81b0c-617">60</span></span></td>
<td><span data-ttu-id="81b0c-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="81b0c-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="81b0c-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="81b0c-619">4,487.12</span></span></td>
<td><span data-ttu-id="81b0c-620">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-621">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-622">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-622">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-623">20</span><span class="sxs-lookup"><span data-stu-id="81b0c-623">20</span></span></td>
<td><span data-ttu-id="81b0c-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="81b0c-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="81b0c-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="81b0c-625">1,495.71</span></span></td>
<td><span data-ttu-id="81b0c-626">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81b0c-627">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="81b0c-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-628">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-628">Cost object</span></span></th>
<th><span data-ttu-id="81b0c-629">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="81b0c-629">Magnitude</span></span></th>
<th><span data-ttu-id="81b0c-630">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="81b0c-630">Allocation factor</span></span></th>
<th><span data-ttu-id="81b0c-631">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-631">Amount</span></span></th>
<th><span data-ttu-id="81b0c-632">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-633">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-634">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-634">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-635">80</span><span class="sxs-lookup"><span data-stu-id="81b0c-635">80</span></span></td>
<td><span data-ttu-id="81b0c-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="81b0c-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="81b0c-637">241.05</span><span class="sxs-lookup"><span data-stu-id="81b0c-637">241.05</span></span></td>
<td><span data-ttu-id="81b0c-638">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-639">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-640">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-640">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-641">15</span><span class="sxs-lookup"><span data-stu-id="81b0c-641">15</span></span></td>
<td><span data-ttu-id="81b0c-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="81b0c-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="81b0c-643">45.20</span><span class="sxs-lookup"><span data-stu-id="81b0c-643">45.20</span></span></td>
<td><span data-ttu-id="81b0c-644">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-645">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-646">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-646">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-647">80</span><span class="sxs-lookup"><span data-stu-id="81b0c-647">80</span></span></td>
<td><span data-ttu-id="81b0c-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="81b0c-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="81b0c-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="81b0c-649">2,507.09</span></span></td>
<td><span data-ttu-id="81b0c-650">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-651">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-652">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-652">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-653">15</span><span class="sxs-lookup"><span data-stu-id="81b0c-653">15</span></span></td>
<td><span data-ttu-id="81b0c-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="81b0c-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="81b0c-655">470.08</span><span class="sxs-lookup"><span data-stu-id="81b0c-655">470.08</span></span></td>
<td><span data-ttu-id="81b0c-656">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="81b0c-657">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="81b0c-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-658">Kladden</span><span class="sxs-lookup"><span data-stu-id="81b0c-658">Journal</span></span></th>
<th><span data-ttu-id="81b0c-659">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="81b0c-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="81b0c-660">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="81b0c-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="81b0c-661">Version</span><span class="sxs-lookup"><span data-stu-id="81b0c-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-662">00004</span><span class="sxs-lookup"><span data-stu-id="81b0c-662">00004</span></span></td>
<td><span data-ttu-id="81b0c-663">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="81b0c-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="81b0c-664">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="81b0c-664">Fiscal</span></span></td>
<td><span data-ttu-id="81b0c-665">2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-665">2017</span></span></td>
<td><span data-ttu-id="81b0c-666">1. Periode</span><span class="sxs-lookup"><span data-stu-id="81b0c-666">Period 1</span></span></td>
<td><span data-ttu-id="81b0c-667">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="81b0c-668">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="81b0c-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="81b0c-669">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-670">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-671">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-671">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-672">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-672">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-673">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-674">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-675">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-675">CC001</span></span></td>
<td><span data-ttu-id="81b0c-676">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-676">HR</span></span></td>
<td><span data-ttu-id="81b0c-677">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-677">10001</span></span></td>
<td><span data-ttu-id="81b0c-678">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-678">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-679">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-679">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-680">500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-681">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-682">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-682">CC001</span></span></td>
<td><span data-ttu-id="81b0c-683">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-683">HR</span></span></td>
<td><span data-ttu-id="81b0c-684">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-684">10001</span></span></td>
<td><span data-ttu-id="81b0c-685">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-685">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-686">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-686">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="81b0c-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-688">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-689">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-689">CC002</span></span></td>
<td><span data-ttu-id="81b0c-690">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-690">Finance</span></span></td>
<td><span data-ttu-id="81b0c-691">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-691">10001</span></span></td>
<td><span data-ttu-id="81b0c-692">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-692">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-693">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-693">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-694">675.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-695">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-696">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-696">CC002</span></span></td>
<td><span data-ttu-id="81b0c-697">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-697">Finance</span></span></td>
<td><span data-ttu-id="81b0c-698">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-698">10001</span></span></td>
<td><span data-ttu-id="81b0c-699">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-699">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-700">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-700">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="81b0c-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-702">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-703">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-703">CC003</span></span></td>
<td><span data-ttu-id="81b0c-704">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-704">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-705">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-705">10001</span></span></td>
<td><span data-ttu-id="81b0c-706">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-706">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-707">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-707">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-708">713.75</span><span class="sxs-lookup"><span data-stu-id="81b0c-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-709">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-710">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-710">CC003</span></span></td>
<td><span data-ttu-id="81b0c-711">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-711">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-712">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-712">10001</span></span></td>
<td><span data-ttu-id="81b0c-713">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-713">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-714">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-714">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="81b0c-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-716">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-717">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-717">CC003</span></span></td>
<td><span data-ttu-id="81b0c-718">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-718">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-719">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-719">10001</span></span></td>
<td><span data-ttu-id="81b0c-720">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-720">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-721">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-721">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-722">286.25</span><span class="sxs-lookup"><span data-stu-id="81b0c-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-723">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-724">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-724">CC003</span></span></td>
<td><span data-ttu-id="81b0c-725">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-725">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-726">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-726">10001</span></span></td>
<td><span data-ttu-id="81b0c-727">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-727">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-728">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-728">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="81b0c-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-730">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-731">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-732">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-732">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-733">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-733">10001</span></span></td>
<td><span data-ttu-id="81b0c-734">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-734">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-735">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-735">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-736">776.36</span><span class="sxs-lookup"><span data-stu-id="81b0c-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-737">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-738">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-739">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-739">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-740">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-740">10001</span></span></td>
<td><span data-ttu-id="81b0c-741">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-741">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-742">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-742">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="81b0c-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-744">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-745">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-746">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-746">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-747">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-747">10001</span></span></td>
<td><span data-ttu-id="81b0c-748">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-748">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-749">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-749">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-750">223.64</span><span class="sxs-lookup"><span data-stu-id="81b0c-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-751">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="81b0c-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-752">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-753">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-753">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-754">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-754">10001</span></span></td>
<td><span data-ttu-id="81b0c-755">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-755">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-756">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-756">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="81b0c-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="81b0c-758">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="81b0c-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="81b0c-759">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="81b0c-760">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-760">Cost element</span></span></th>
<th><span data-ttu-id="81b0c-761">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-761">Cost behavior</span></span></th>
<th><span data-ttu-id="81b0c-762">Beløb</span><span class="sxs-lookup"><span data-stu-id="81b0c-762">Amount</span></span></th>
<th><span data-ttu-id="81b0c-763">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="81b0c-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81b0c-764">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-764">CC001</span></span></td>
<td><span data-ttu-id="81b0c-765">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-765">HR</span></span></td>
<td><span data-ttu-id="81b0c-766">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-766">10001</span></span></td>
<td><span data-ttu-id="81b0c-767">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-767">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-768">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-768">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-769">-500.00</span></span></td>
<td><span data-ttu-id="81b0c-770">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-771">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-771">CC002</span></span></td>
<td><span data-ttu-id="81b0c-772">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-772">Finance</span></span></td>
<td><span data-ttu-id="81b0c-773">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-773">10001</span></span></td>
<td><span data-ttu-id="81b0c-774">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-774">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-775">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-775">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-776">175.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-776">175.00</span></span></td>
<td><span data-ttu-id="81b0c-777">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-778">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-778">CC003</span></span></td>
<td><span data-ttu-id="81b0c-779">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-779">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-780">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-780">10001</span></span></td>
<td><span data-ttu-id="81b0c-781">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-781">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-782">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-782">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-783">275.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-783">275.00</span></span></td>
<td><span data-ttu-id="81b0c-784">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-785">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-785">CC004</span></span></td>
<td><span data-ttu-id="81b0c-786">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-786">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-787">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-787">10001</span></span></td>
<td><span data-ttu-id="81b0c-788">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-788">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-789">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-789">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-790">50,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-790">50,00</span></span></td>
<td><span data-ttu-id="81b0c-791">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-792">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-792">CC001</span></span></td>
<td><span data-ttu-id="81b0c-793">Personale</span><span class="sxs-lookup"><span data-stu-id="81b0c-793">HR</span></span></td>
<td><span data-ttu-id="81b0c-794">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-794">10001</span></span></td>
<td><span data-ttu-id="81b0c-795">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-795">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-796">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-796">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="81b0c-797">-1,245.71</span></span></td>
<td><span data-ttu-id="81b0c-798">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-799">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-799">CC002</span></span></td>
<td><span data-ttu-id="81b0c-800">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-800">Finance</span></span></td>
<td><span data-ttu-id="81b0c-801">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-801">10001</span></span></td>
<td><span data-ttu-id="81b0c-802">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-802">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-803">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-803">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-804">436.00</span><span class="sxs-lookup"><span data-stu-id="81b0c-804">436.00</span></span></td>
<td><span data-ttu-id="81b0c-805">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-806">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-806">CC003</span></span></td>
<td><span data-ttu-id="81b0c-807">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-807">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-808">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-808">10001</span></span></td>
<td><span data-ttu-id="81b0c-809">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-809">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-810">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-810">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-811">685.14</span><span class="sxs-lookup"><span data-stu-id="81b0c-811">685.14</span></span></td>
<td><span data-ttu-id="81b0c-812">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-813">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-813">CC004</span></span></td>
<td><span data-ttu-id="81b0c-814">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-814">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-815">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-815">10001</span></span></td>
<td><span data-ttu-id="81b0c-816">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-816">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-817">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-817">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-818">124.57</span><span class="sxs-lookup"><span data-stu-id="81b0c-818">124.57</span></span></td>
<td><span data-ttu-id="81b0c-819">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-820">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-820">CC002</span></span></td>
<td><span data-ttu-id="81b0c-821">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-821">Finance</span></span></td>
<td><span data-ttu-id="81b0c-822">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-822">10001</span></span></td>
<td><span data-ttu-id="81b0c-823">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-823">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-824">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-824">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-825">-675.00</span></span></td>
<td><span data-ttu-id="81b0c-826">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-827">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-827">CC003</span></span></td>
<td><span data-ttu-id="81b0c-828">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-828">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-829">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-829">10001</span></span></td>
<td><span data-ttu-id="81b0c-830">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-830">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-831">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-831">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-832">438.75</span><span class="sxs-lookup"><span data-stu-id="81b0c-832">438.75</span></span></td>
<td><span data-ttu-id="81b0c-833">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-834">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-834">CC004</span></span></td>
<td><span data-ttu-id="81b0c-835">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-835">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-836">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-836">10001</span></span></td>
<td><span data-ttu-id="81b0c-837">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-837">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-838">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-838">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-839">236.25</span><span class="sxs-lookup"><span data-stu-id="81b0c-839">236.25</span></span></td>
<td><span data-ttu-id="81b0c-840">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-841">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-841">CC002</span></span></td>
<td><span data-ttu-id="81b0c-842">Finans</span><span class="sxs-lookup"><span data-stu-id="81b0c-842">Finance</span></span></td>
<td><span data-ttu-id="81b0c-843">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-843">10001</span></span></td>
<td><span data-ttu-id="81b0c-844">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-844">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-845">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-845">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="81b0c-846">-8,150.29</span></span></td>
<td><span data-ttu-id="81b0c-847">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-848">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-848">CC003</span></span></td>
<td><span data-ttu-id="81b0c-849">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-849">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-850">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-850">10001</span></span></td>
<td><span data-ttu-id="81b0c-851">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-851">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-852">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-852">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="81b0c-853">5,297.69</span></span></td>
<td><span data-ttu-id="81b0c-854">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-855">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-855">CC004</span></span></td>
<td><span data-ttu-id="81b0c-856">Emballage</span><span class="sxs-lookup"><span data-stu-id="81b0c-856">Packaging</span></span></td>
<td><span data-ttu-id="81b0c-857">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-857">10001</span></span></td>
<td><span data-ttu-id="81b0c-858">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-858">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-859">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-859">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="81b0c-860">2,852.60</span></span></td>
<td><span data-ttu-id="81b0c-861">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-862">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-862">CC003</span></span></td>
<td><span data-ttu-id="81b0c-863">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-863">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-864">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-864">10001</span></span></td>
<td><span data-ttu-id="81b0c-865">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-865">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-866">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-866">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="81b0c-867">-713.75</span></span></td>
<td><span data-ttu-id="81b0c-868">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-869">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-870">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-870">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-871">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-871">10001</span></span></td>
<td><span data-ttu-id="81b0c-872">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-872">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-873">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-873">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-874">535.31</span><span class="sxs-lookup"><span data-stu-id="81b0c-874">535.31</span></span></td>
<td><span data-ttu-id="81b0c-875">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-876">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-877">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-877">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-878">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-878">10001</span></span></td>
<td><span data-ttu-id="81b0c-879">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-879">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-880">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-880">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-881">178.44</span><span class="sxs-lookup"><span data-stu-id="81b0c-881">178.44</span></span></td>
<td><span data-ttu-id="81b0c-882">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-883">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-883">CC003</span></span></td>
<td><span data-ttu-id="81b0c-884">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-884">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-885">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-885">10001</span></span></td>
<td><span data-ttu-id="81b0c-886">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-886">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-887">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-887">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="81b0c-888">-5,982.83</span></span></td>
<td><span data-ttu-id="81b0c-889">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-890">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-891">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-891">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-892">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-892">10001</span></span></td>
<td><span data-ttu-id="81b0c-893">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-893">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-894">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-894">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="81b0c-895">4,487.12</span></span></td>
<td><span data-ttu-id="81b0c-896">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-897">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-898">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-898">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-899">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-899">10001</span></span></td>
<td><span data-ttu-id="81b0c-900">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-900">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-901">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-901">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="81b0c-902">1,495.71</span></span></td>
<td><span data-ttu-id="81b0c-903">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-904">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-904">CC003</span></span></td>
<td><span data-ttu-id="81b0c-905">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-905">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-906">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-906">10001</span></span></td>
<td><span data-ttu-id="81b0c-907">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-907">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-908">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-908">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="81b0c-909">-286.25</span></span></td>
<td><span data-ttu-id="81b0c-910">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-911">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-912">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-912">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-913">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-913">10001</span></span></td>
<td><span data-ttu-id="81b0c-914">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-914">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-915">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-915">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-916">241.05</span><span class="sxs-lookup"><span data-stu-id="81b0c-916">241.05</span></span></td>
<td><span data-ttu-id="81b0c-917">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-918">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-919">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-919">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-920">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-920">10001</span></span></td>
<td><span data-ttu-id="81b0c-921">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-921">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-922">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-922">Fixed cost</span></span></td>
<td><span data-ttu-id="81b0c-923">45.20</span><span class="sxs-lookup"><span data-stu-id="81b0c-923">45.20</span></span></td>
<td><span data-ttu-id="81b0c-924">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-925">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-925">CC003</span></span></td>
<td><span data-ttu-id="81b0c-926">Samling</span><span class="sxs-lookup"><span data-stu-id="81b0c-926">Assembly</span></span></td>
<td><span data-ttu-id="81b0c-927">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-927">10001</span></span></td>
<td><span data-ttu-id="81b0c-928">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-928">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-929">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-929">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="81b0c-930">-2,977.17</span></span></td>
<td><span data-ttu-id="81b0c-931">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-932">Prod 1</span></span></td>
<td><span data-ttu-id="81b0c-933">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-933">Product 1</span></span></td>
<td><span data-ttu-id="81b0c-934">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-934">10001</span></span></td>
<td><span data-ttu-id="81b0c-935">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-935">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-936">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-936">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="81b0c-937">2,507.09</span></span></td>
<td><span data-ttu-id="81b0c-938">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81b0c-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-939">Prod 2</span></span></td>
<td><span data-ttu-id="81b0c-940">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-940">Product 2</span></span></td>
<td><span data-ttu-id="81b0c-941">10001</span><span class="sxs-lookup"><span data-stu-id="81b0c-941">10001</span></span></td>
<td><span data-ttu-id="81b0c-942">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-942">Electricity</span></span></td>
<td><span data-ttu-id="81b0c-943">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-943">Variable cost</span></span></td>
<td><span data-ttu-id="81b0c-944">470.08</span><span class="sxs-lookup"><span data-stu-id="81b0c-944">470.08</span></span></td>
<td><span data-ttu-id="81b0c-945">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="81b0c-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="81b0c-946">Konklusion</span><span class="sxs-lookup"><span data-stu-id="81b0c-946">Conclusion</span></span>
<span data-ttu-id="81b0c-947">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="81b0c-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="81b0c-948">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="81b0c-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="81b0c-949">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="81b0c-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="81b0c-950">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="81b0c-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="81b0c-951">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="81b0c-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="81b0c-952">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="81b0c-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="81b0c-953">Samlet</span><span class="sxs-lookup"><span data-stu-id="81b0c-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="81b0c-954">CC099</span><span class="sxs-lookup"><span data-stu-id="81b0c-954">CC099</span></span></th>
<th><span data-ttu-id="81b0c-955">CC001</span><span class="sxs-lookup"><span data-stu-id="81b0c-955">CC001</span></span></th>
<th><span data-ttu-id="81b0c-956">CC002</span><span class="sxs-lookup"><span data-stu-id="81b0c-956">CC002</span></span></th>
<th><span data-ttu-id="81b0c-957">CC003</span><span class="sxs-lookup"><span data-stu-id="81b0c-957">CC003</span></span></th>
<th><span data-ttu-id="81b0c-958">CC004</span><span class="sxs-lookup"><span data-stu-id="81b0c-958">CC004</span></span></th>
<th><span data-ttu-id="81b0c-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-959">Proj 1</span></span></th>
<th><span data-ttu-id="81b0c-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-960">Proj 2</span></span></th>
<th><span data-ttu-id="81b0c-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="81b0c-961">Prod 1</span></span></th>
<th><span data-ttu-id="81b0c-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="81b0c-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="81b0c-963">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="81b0c-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="81b0c-973">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="81b0c-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="81b0c-975">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-978">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-979">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-980">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-981">776.36</span><span class="sxs-lookup"><span data-stu-id="81b0c-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-982">223.64</span><span class="sxs-lookup"><span data-stu-id="81b0c-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="81b0c-984">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="81b0c-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-985">000</span><span class="sxs-lookup"><span data-stu-id="81b0c-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-987">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-988">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-989">0,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-990">30,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-991">10,00</span><span class="sxs-lookup"><span data-stu-id="81b0c-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="81b0c-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="81b0c-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="81b0c-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="81b0c-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="81b0c-995">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="81b0c-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="81b0c-996">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="81b0c-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="81b0c-997">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="81b0c-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="81b0c-998">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="81b0c-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="81b0c-999">Du kan finde flere oplysninger under Politik for omkostningstotaler.</span><span class="sxs-lookup"><span data-stu-id="81b0c-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="81b0c-1000">(Bemærk, at dette emne endnu ikke er færdigt, men det kommer snart).</span><span class="sxs-lookup"><span data-stu-id="81b0c-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




