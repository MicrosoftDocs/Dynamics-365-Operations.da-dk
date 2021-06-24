---
title: Beregning af fast omkostning
description: I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187991"
---
# <a name="overhead-calculation"></a><span data-ttu-id="ec672-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec672-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ec672-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="ec672-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="ec672-105">Term definition</span></span>

<span data-ttu-id="ec672-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="ec672-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ec672-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="ec672-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ec672-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="ec672-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ec672-109">Leje</span><span class="sxs-lookup"><span data-stu-id="ec672-109">Rent</span></span>
-   <span data-ttu-id="ec672-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-110">Electricity</span></span>
-   <span data-ttu-id="ec672-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="ec672-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ec672-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-112">Overhead calculation overview</span></span>
<span data-ttu-id="ec672-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="ec672-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ec672-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="ec672-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ec672-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="ec672-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ec672-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ec672-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ec672-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ec672-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ec672-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="ec672-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ec672-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="ec672-119">Version type</span></span>
-   <span data-ttu-id="ec672-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="ec672-120">Date and time</span></span>
-   <span data-ttu-id="ec672-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="ec672-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ec672-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ec672-122">Fiscal year</span></span>
-   <span data-ttu-id="ec672-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="ec672-123">Fiscal period</span></span>

<span data-ttu-id="ec672-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="ec672-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ec672-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="ec672-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ec672-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="ec672-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ec672-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="ec672-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ec672-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ec672-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ec672-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="ec672-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ec672-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="ec672-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ec672-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ec672-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ec672-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ec672-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="ec672-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ec672-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="ec672-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ec672-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="ec672-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ec672-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="ec672-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ec672-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ec672-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="ec672-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="ec672-140">Main account</span></span></th>
<th><span data-ttu-id="ec672-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="ec672-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ec672-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-143">CC099</span></span></td>
<td><span data-ttu-id="ec672-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-144">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-145">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-145">10001</span></span></td>
<td><span data-ttu-id="ec672-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-146">Electricity</span></span></td>
<td><span data-ttu-id="ec672-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ec672-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="ec672-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ec672-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="ec672-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ec672-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="ec672-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ec672-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="ec672-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ec672-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="ec672-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ec672-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="ec672-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ec672-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="ec672-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ec672-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="ec672-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ec672-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ec672-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="ec672-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ec672-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="ec672-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ec672-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-160">Journal</span></span></th>
<th><span data-ttu-id="ec672-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ec672-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ec672-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ec672-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ec672-163">Version</span><span class="sxs-lookup"><span data-stu-id="ec672-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-164">00001</span><span class="sxs-lookup"><span data-stu-id="ec672-164">00001</span></span></td>
<td><span data-ttu-id="ec672-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ec672-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ec672-166">Fiscal</span></span></td>
<td><span data-ttu-id="ec672-167">2017</span><span class="sxs-lookup"><span data-stu-id="ec672-167">2017</span></span></td>
<td><span data-ttu-id="ec672-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ec672-168">Period 1</span></span></td>
<td><span data-ttu-id="ec672-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ec672-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ec672-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="ec672-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-173">Cost element</span></span></th>
<th><span data-ttu-id="ec672-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ec672-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-177">CC099</span></span></td>
<td><span data-ttu-id="ec672-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-178">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-179">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-179">10001</span></span></td>
<td><span data-ttu-id="ec672-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-180">Electricity</span></span></td>
<td><span data-ttu-id="ec672-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ec672-181">Unclassified</span></span></td>
<td><span data-ttu-id="ec672-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ec672-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ec672-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-185">Cost element</span></span></th>
<th><span data-ttu-id="ec672-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-187">Amount</span></span></th>
<th><span data-ttu-id="ec672-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-189">CC099</span></span></td>
<td><span data-ttu-id="ec672-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-190">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-191">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-191">10001</span></span></td>
<td><span data-ttu-id="ec672-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-192">Electricity</span></span></td>
<td><span data-ttu-id="ec672-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ec672-193">Unclassified</span></span></td>
<td><span data-ttu-id="ec672-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-194">10,000.00</span></span></td>
<td><span data-ttu-id="ec672-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-196">CC099</span></span></td>
<td><span data-ttu-id="ec672-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-197">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-198">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-198">10001</span></span></td>
<td><span data-ttu-id="ec672-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-199">Electricity</span></span></td>
<td><span data-ttu-id="ec672-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ec672-200">Unclassified</span></span></td>
<td><span data-ttu-id="ec672-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ec672-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-203">CC099</span></span></td>
<td><span data-ttu-id="ec672-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-204">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-205">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-205">10001</span></span></td>
<td><span data-ttu-id="ec672-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-206">Electricity</span></span></td>
<td><span data-ttu-id="ec672-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-208">1,000.00</span></span></td>
<td><span data-ttu-id="ec672-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-210">CC099</span></span></td>
<td><span data-ttu-id="ec672-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-211">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-212">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-212">10001</span></span></td>
<td><span data-ttu-id="ec672-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-213">Electricity</span></span></td>
<td><span data-ttu-id="ec672-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-214">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-215">9,000.00</span></span></td>
<td><span data-ttu-id="ec672-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ec672-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ec672-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="ec672-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ec672-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ec672-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="ec672-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ec672-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="ec672-221">Define the cost distribution rule</span></span>

<span data-ttu-id="ec672-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="ec672-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ec672-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="ec672-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ec672-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ec672-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="ec672-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ec672-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="ec672-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ec672-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-228">Cost object</span></span></th>
<th><span data-ttu-id="ec672-229">KWh</span><span class="sxs-lookup"><span data-stu-id="ec672-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-230">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-230">CC001</span></span></td>
<td><span data-ttu-id="ec672-231">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-231">HR</span></span></td>
<td><span data-ttu-id="ec672-232">1.000</span><span class="sxs-lookup"><span data-stu-id="ec672-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-233">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-233">CC002</span></span></td>
<td><span data-ttu-id="ec672-234">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-234">Finance</span></span></td>
<td><span data-ttu-id="ec672-235">6.000</span><span class="sxs-lookup"><span data-stu-id="ec672-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-236">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-236">CC003</span></span></td>
<td><span data-ttu-id="ec672-237">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-237">Assembly</span></span></td>
<td><span data-ttu-id="ec672-238">0</span><span class="sxs-lookup"><span data-stu-id="ec672-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ec672-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-240">Cost object</span></span></th>
<th><span data-ttu-id="ec672-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-241">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-242">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-244">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-244">CC001</span></span></td>
<td><span data-ttu-id="ec672-245">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-245">HR</span></span></td>
<td><span data-ttu-id="ec672-246">1.000</span><span class="sxs-lookup"><span data-stu-id="ec672-246">1,000</span></span></td>
<td><span data-ttu-id="ec672-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ec672-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ec672-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-249">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-249">CC002</span></span></td>
<td><span data-ttu-id="ec672-250">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-250">Finance</span></span></td>
<td><span data-ttu-id="ec672-251">6.000</span><span class="sxs-lookup"><span data-stu-id="ec672-251">6,000</span></span></td>
<td><span data-ttu-id="ec672-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ec672-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ec672-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-254">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-254">CC003</span></span></td>
<td><span data-ttu-id="ec672-255">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-255">Assembly</span></span></td>
<td><span data-ttu-id="ec672-256">0</span><span class="sxs-lookup"><span data-stu-id="ec672-256">0</span></span></td>
<td><span data-ttu-id="ec672-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ec672-258">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="ec672-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ec672-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ec672-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-261">Cost object</span></span></th>
<th><span data-ttu-id="ec672-262">Formel</span><span class="sxs-lookup"><span data-stu-id="ec672-262">Formula</span></span></th>
<th><span data-ttu-id="ec672-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-263">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-264">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-266">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-266">CC001</span></span></td>
<td><span data-ttu-id="ec672-267">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-267">HR</span></span></td>
<td><span data-ttu-id="ec672-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ec672-269">1</span><span class="sxs-lookup"><span data-stu-id="ec672-269">1</span></span></td>
<td><span data-ttu-id="ec672-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ec672-271">500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-272">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-272">CC002</span></span></td>
<td><span data-ttu-id="ec672-273">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-273">Finance</span></span></td>
<td><span data-ttu-id="ec672-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ec672-275">1</span><span class="sxs-lookup"><span data-stu-id="ec672-275">1</span></span></td>
<td><span data-ttu-id="ec672-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ec672-277">500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-278">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-278">CC003</span></span></td>
<td><span data-ttu-id="ec672-279">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-279">Assembly</span></span></td>
<td><span data-ttu-id="ec672-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ec672-281">0</span><span class="sxs-lookup"><span data-stu-id="ec672-281">0</span></span></td>
<td><span data-ttu-id="ec672-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ec672-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ec672-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-285">Journal</span></span></th>
<th><span data-ttu-id="ec672-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ec672-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ec672-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ec672-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ec672-288">Version</span><span class="sxs-lookup"><span data-stu-id="ec672-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-289">00002</span><span class="sxs-lookup"><span data-stu-id="ec672-289">00002</span></span></td>
<td><span data-ttu-id="ec672-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="ec672-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ec672-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ec672-291">Fiscal</span></span></td>
<td><span data-ttu-id="ec672-292">2017</span><span class="sxs-lookup"><span data-stu-id="ec672-292">2017</span></span></td>
<td><span data-ttu-id="ec672-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ec672-293">Period 1</span></span></td>
<td><span data-ttu-id="ec672-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ec672-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ec672-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="ec672-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-298">Cost element</span></span></th>
<th><span data-ttu-id="ec672-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-299">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-302">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-302">CC099</span></span></td>
<td><span data-ttu-id="ec672-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-303">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-304">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-304">10001</span></span></td>
<td><span data-ttu-id="ec672-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-305">Electricity</span></span></td>
<td><span data-ttu-id="ec672-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-306">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-309">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-309">CC099</span></span></td>
<td><span data-ttu-id="ec672-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-310">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-311">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-311">10001</span></span></td>
<td><span data-ttu-id="ec672-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-312">Electricity</span></span></td>
<td><span data-ttu-id="ec672-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-313">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ec672-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ec672-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-317">Cost element</span></span></th>
<th><span data-ttu-id="ec672-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-318">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-319">Amount</span></span></th>
<th><span data-ttu-id="ec672-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-321">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-321">CC099</span></span></td>
<td><span data-ttu-id="ec672-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-322">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-323">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-323">10001</span></span></td>
<td><span data-ttu-id="ec672-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-324">Electricity</span></span></td>
<td><span data-ttu-id="ec672-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-325">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-326">-1,000.00</span></span></td>
<td><span data-ttu-id="ec672-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-328">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-328">CC001</span></span></td>
<td><span data-ttu-id="ec672-329">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-329">HR</span></span></td>
<td><span data-ttu-id="ec672-330">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-330">10001</span></span></td>
<td><span data-ttu-id="ec672-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-331">Electricity</span></span></td>
<td><span data-ttu-id="ec672-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-332">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-333">500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-333">500.00</span></span></td>
<td><span data-ttu-id="ec672-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-335">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-335">CC002</span></span></td>
<td><span data-ttu-id="ec672-336">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-336">Finance</span></span></td>
<td><span data-ttu-id="ec672-337">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-337">10001</span></span></td>
<td><span data-ttu-id="ec672-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-338">Electricity</span></span></td>
<td><span data-ttu-id="ec672-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-339">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-340">500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-340">500.00</span></span></td>
<td><span data-ttu-id="ec672-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-342">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-342">CC099</span></span></td>
<td><span data-ttu-id="ec672-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ec672-343">Default cost center</span></span></td>
<td><span data-ttu-id="ec672-344">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-344">10001</span></span></td>
<td><span data-ttu-id="ec672-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-345">Electricity</span></span></td>
<td><span data-ttu-id="ec672-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-346">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="ec672-347">-9,000.00</span></span></td>
<td><span data-ttu-id="ec672-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-349">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-349">CC001</span></span></td>
<td><span data-ttu-id="ec672-350">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-350">HR</span></span></td>
<td><span data-ttu-id="ec672-351">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-351">10001</span></span></td>
<td><span data-ttu-id="ec672-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-352">Electricity</span></span></td>
<td><span data-ttu-id="ec672-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-353">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ec672-354">1,285.71</span></span></td>
<td><span data-ttu-id="ec672-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-356">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-356">CC002</span></span></td>
<td><span data-ttu-id="ec672-357">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-357">Finance</span></span></td>
<td><span data-ttu-id="ec672-358">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-358">10001</span></span></td>
<td><span data-ttu-id="ec672-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-359">Electricity</span></span></td>
<td><span data-ttu-id="ec672-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-360">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ec672-361">7,714.29</span></span></td>
<td><span data-ttu-id="ec672-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ec672-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ec672-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="ec672-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ec672-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ec672-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ec672-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="ec672-367">Define the overhead rate</span></span>

<span data-ttu-id="ec672-368">Omkostningsobjektet CC001 Human Resources bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ec672-369">Et statistisk dimensionsmedlem med navnet Human Resourcesprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ec672-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-370">Cost object</span></span></th>
<th><span data-ttu-id="ec672-371">Timer</span><span class="sxs-lookup"><span data-stu-id="ec672-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-372">Proj 1</span></span></td>
<td><span data-ttu-id="ec672-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-373">Project 1</span></span></td>
<td><span data-ttu-id="ec672-374">3</span><span class="sxs-lookup"><span data-stu-id="ec672-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-375">Proj 2</span></span></td>
<td><span data-ttu-id="ec672-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-376">Project 2</span></span></td>
<td><span data-ttu-id="ec672-377">1</span><span class="sxs-lookup"><span data-stu-id="ec672-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="ec672-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-379">Cost object</span></span></th>
<th><span data-ttu-id="ec672-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-380">Cost element</span></span></th>
<th><span data-ttu-id="ec672-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-381">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="ec672-382">Units</span></span></th>
<th><span data-ttu-id="ec672-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="ec672-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-384">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-384">CC001</span></span></td>
<td><span data-ttu-id="ec672-385">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-385">HR</span></span></td>
<td><span data-ttu-id="ec672-386">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-386">10001</span></span></td>
<td><span data-ttu-id="ec672-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-387">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-388">1</span><span class="sxs-lookup"><span data-stu-id="ec672-388">1</span></span></td>
<td><span data-ttu-id="ec672-389">10</span><span class="sxs-lookup"><span data-stu-id="ec672-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-391">Cost object</span></span></th>
<th><span data-ttu-id="ec672-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-392">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-393">Cost element</span></span></th>
<th><span data-ttu-id="ec672-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-394">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-396">Proj 1</span></span></td>
<td><span data-ttu-id="ec672-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-397">Project 1</span></span></td>
<td><span data-ttu-id="ec672-398">3</span><span class="sxs-lookup"><span data-stu-id="ec672-398">3</span></span></td>
<td><span data-ttu-id="ec672-399">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-399">10001</span></span></td>
<td><span data-ttu-id="ec672-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ec672-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ec672-401">30,00</span><span class="sxs-lookup"><span data-stu-id="ec672-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-402">Proj 2</span></span></td>
<td><span data-ttu-id="ec672-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-403">Project 2</span></span></td>
<td><span data-ttu-id="ec672-404">1</span><span class="sxs-lookup"><span data-stu-id="ec672-404">1</span></span></td>
<td><span data-ttu-id="ec672-405">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-405">10001</span></span></td>
<td><span data-ttu-id="ec672-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ec672-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ec672-407">10,00</span><span class="sxs-lookup"><span data-stu-id="ec672-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ec672-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-409">Journal</span></span></th>
<th><span data-ttu-id="ec672-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ec672-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ec672-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ec672-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ec672-412">Version</span><span class="sxs-lookup"><span data-stu-id="ec672-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-413">00003</span><span class="sxs-lookup"><span data-stu-id="ec672-413">00003</span></span></td>
<td><span data-ttu-id="ec672-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="ec672-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ec672-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ec672-415">Fiscal</span></span></td>
<td><span data-ttu-id="ec672-416">2017</span><span class="sxs-lookup"><span data-stu-id="ec672-416">2017</span></span></td>
<td><span data-ttu-id="ec672-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ec672-417">Period 1</span></span></td>
<td><span data-ttu-id="ec672-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ec672-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ec672-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="ec672-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-421">Cost object</span></span></th>
<th><span data-ttu-id="ec672-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-424">Proj 1</span></span></td>
<td><span data-ttu-id="ec672-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ec672-426">3,00</span><span class="sxs-lookup"><span data-stu-id="ec672-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-428">Proj 2</span></span></td>
<td><span data-ttu-id="ec672-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ec672-430">1,00</span><span class="sxs-lookup"><span data-stu-id="ec672-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ec672-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ec672-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-433">Cost element</span></span></th>
<th><span data-ttu-id="ec672-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-434">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-435">Amount</span></span></th>
<th><span data-ttu-id="ec672-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="ec672-437">CC0001</span></span></td>
<td><span data-ttu-id="ec672-438">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-438">HR</span></span></td>
<td><span data-ttu-id="ec672-439">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-439">10001</span></span></td>
<td><span data-ttu-id="ec672-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-440">Electricity</span></span></td>
<td><span data-ttu-id="ec672-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-441">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="ec672-442">-30.00</span></span></td>
<td><span data-ttu-id="ec672-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-444">Proj 1</span></span></td>
<td><span data-ttu-id="ec672-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ec672-446">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-446">10001</span></span></td>
<td><span data-ttu-id="ec672-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-447">Electricity</span></span></td>
<td><span data-ttu-id="ec672-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-448">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-449">30,00</span><span class="sxs-lookup"><span data-stu-id="ec672-449">30.00</span></span></td>
<td><span data-ttu-id="ec672-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-451">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-451">CC001</span></span></td>
<td><span data-ttu-id="ec672-452">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-452">HR</span></span></td>
<td><span data-ttu-id="ec672-453">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-453">10001</span></span></td>
<td><span data-ttu-id="ec672-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-454">Electricity</span></span></td>
<td><span data-ttu-id="ec672-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-455">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="ec672-456">-10.00</span></span></td>
<td><span data-ttu-id="ec672-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-458">Proj 2</span></span></td>
<td><span data-ttu-id="ec672-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ec672-460">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-460">10001</span></span></td>
<td><span data-ttu-id="ec672-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-461">Electricity</span></span></td>
<td><span data-ttu-id="ec672-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-462">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-463">10.00</span><span class="sxs-lookup"><span data-stu-id="ec672-463">10.00</span></span></td>
<td><span data-ttu-id="ec672-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="ec672-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ec672-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="ec672-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ec672-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ec672-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="ec672-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="ec672-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="ec672-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ec672-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="ec672-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ec672-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ec672-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ec672-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="ec672-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ec672-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="ec672-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ec672-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ec672-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ec672-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="ec672-475">Define the cost allocation</span></span>

<span data-ttu-id="ec672-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ec672-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ec672-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ec672-478">Et statistisk dimensionsmedlem med navnet Human Resources-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ec672-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-479">Cost object</span></span></th>
<th><span data-ttu-id="ec672-480">Human Resources-tjenester</span><span class="sxs-lookup"><span data-stu-id="ec672-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-481">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-481">CC002</span></span></td>
<td><span data-ttu-id="ec672-482">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-482">Finance</span></span></td>
<td><span data-ttu-id="ec672-483">35</span><span class="sxs-lookup"><span data-stu-id="ec672-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-484">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-484">CC003</span></span></td>
<td><span data-ttu-id="ec672-485">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-485">Assembly</span></span></td>
<td><span data-ttu-id="ec672-486">55</span><span class="sxs-lookup"><span data-stu-id="ec672-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-487">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-487">CC004</span></span></td>
<td><span data-ttu-id="ec672-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-488">Packaging</span></span></td>
<td><span data-ttu-id="ec672-489">10</span><span class="sxs-lookup"><span data-stu-id="ec672-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ec672-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ec672-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-492">Cost object</span></span></th>
<th><span data-ttu-id="ec672-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="ec672-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-494">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-494">CC003</span></span></td>
<td><span data-ttu-id="ec672-495">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-495">Assembly</span></span></td>
<td><span data-ttu-id="ec672-496">65</span><span class="sxs-lookup"><span data-stu-id="ec672-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-497">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-497">CC004</span></span></td>
<td><span data-ttu-id="ec672-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-498">Packaging</span></span></td>
<td><span data-ttu-id="ec672-499">35</span><span class="sxs-lookup"><span data-stu-id="ec672-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ec672-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ec672-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-502">Cost object</span></span></th>
<th><span data-ttu-id="ec672-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="ec672-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-504">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-505">Product 1</span></span></td>
<td><span data-ttu-id="ec672-506">60</span><span class="sxs-lookup"><span data-stu-id="ec672-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-507">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-508">Product 2</span></span></td>
<td><span data-ttu-id="ec672-509">20</span><span class="sxs-lookup"><span data-stu-id="ec672-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ec672-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ec672-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-512">Cost object</span></span></th>
<th><span data-ttu-id="ec672-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="ec672-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-514">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-515">Product 1</span></span></td>
<td><span data-ttu-id="ec672-516">80</span><span class="sxs-lookup"><span data-stu-id="ec672-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-517">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-518">Product 2</span></span></td>
<td><span data-ttu-id="ec672-519">15</span><span class="sxs-lookup"><span data-stu-id="ec672-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ec672-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="ec672-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ec672-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="ec672-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="ec672-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ec672-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-523">Cost object</span></span></th>
<th><span data-ttu-id="ec672-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-524">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-525">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-526">Amount</span></span></th>
<th><span data-ttu-id="ec672-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-528">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-528">CC002</span></span></td>
<td><span data-ttu-id="ec672-529">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-529">Finance</span></span></td>
<td><span data-ttu-id="ec672-530">35</span><span class="sxs-lookup"><span data-stu-id="ec672-530">35</span></span></td>
<td><span data-ttu-id="ec672-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ec672-532">175.00</span><span class="sxs-lookup"><span data-stu-id="ec672-532">175.00</span></span></td>
<td><span data-ttu-id="ec672-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-534">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-534">CC003</span></span></td>
<td><span data-ttu-id="ec672-535">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-535">Assembly</span></span></td>
<td><span data-ttu-id="ec672-536">55</span><span class="sxs-lookup"><span data-stu-id="ec672-536">55</span></span></td>
<td><span data-ttu-id="ec672-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ec672-538">275.00</span><span class="sxs-lookup"><span data-stu-id="ec672-538">275.00</span></span></td>
<td><span data-ttu-id="ec672-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-540">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-540">CC004</span></span></td>
<td><span data-ttu-id="ec672-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-541">Packaging</span></span></td>
<td><span data-ttu-id="ec672-542">10</span><span class="sxs-lookup"><span data-stu-id="ec672-542">10</span></span></td>
<td><span data-ttu-id="ec672-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ec672-544">50,00</span><span class="sxs-lookup"><span data-stu-id="ec672-544">50.00</span></span></td>
<td><span data-ttu-id="ec672-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-546">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-546">CC002</span></span></td>
<td><span data-ttu-id="ec672-547">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-547">Finance</span></span></td>
<td><span data-ttu-id="ec672-548">35</span><span class="sxs-lookup"><span data-stu-id="ec672-548">35</span></span></td>
<td><span data-ttu-id="ec672-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ec672-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ec672-550">436.00</span><span class="sxs-lookup"><span data-stu-id="ec672-550">436.00</span></span></td>
<td><span data-ttu-id="ec672-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-552">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-552">CC003</span></span></td>
<td><span data-ttu-id="ec672-553">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-553">Assembly</span></span></td>
<td><span data-ttu-id="ec672-554">55</span><span class="sxs-lookup"><span data-stu-id="ec672-554">55</span></span></td>
<td><span data-ttu-id="ec672-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ec672-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ec672-556">685.14</span><span class="sxs-lookup"><span data-stu-id="ec672-556">685.14</span></span></td>
<td><span data-ttu-id="ec672-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-558">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-558">CC004</span></span></td>
<td><span data-ttu-id="ec672-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-559">Packaging</span></span></td>
<td><span data-ttu-id="ec672-560">10</span><span class="sxs-lookup"><span data-stu-id="ec672-560">10</span></span></td>
<td><span data-ttu-id="ec672-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ec672-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ec672-562">124.57</span><span class="sxs-lookup"><span data-stu-id="ec672-562">124.57</span></span></td>
<td><span data-ttu-id="ec672-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ec672-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-565">Cost object</span></span></th>
<th><span data-ttu-id="ec672-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-566">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-567">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-568">Amount</span></span></th>
<th><span data-ttu-id="ec672-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-570">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-570">CC003</span></span></td>
<td><span data-ttu-id="ec672-571">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-571">Assembly</span></span></td>
<td><span data-ttu-id="ec672-572">65</span><span class="sxs-lookup"><span data-stu-id="ec672-572">65</span></span></td>
<td><span data-ttu-id="ec672-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ec672-574">438.75</span><span class="sxs-lookup"><span data-stu-id="ec672-574">438.75</span></span></td>
<td><span data-ttu-id="ec672-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-576">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-576">CC004</span></span></td>
<td><span data-ttu-id="ec672-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-577">Packaging</span></span></td>
<td><span data-ttu-id="ec672-578">35</span><span class="sxs-lookup"><span data-stu-id="ec672-578">35</span></span></td>
<td><span data-ttu-id="ec672-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ec672-580">236.25</span><span class="sxs-lookup"><span data-stu-id="ec672-580">236.25</span></span></td>
<td><span data-ttu-id="ec672-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-582">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-582">CC003</span></span></td>
<td><span data-ttu-id="ec672-583">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-583">Assembly</span></span></td>
<td><span data-ttu-id="ec672-584">65</span><span class="sxs-lookup"><span data-stu-id="ec672-584">65</span></span></td>
<td><span data-ttu-id="ec672-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ec672-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ec672-586">5,297.69</span></span></td>
<td><span data-ttu-id="ec672-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-588">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-588">CC004</span></span></td>
<td><span data-ttu-id="ec672-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-589">Packaging</span></span></td>
<td><span data-ttu-id="ec672-590">35</span><span class="sxs-lookup"><span data-stu-id="ec672-590">35</span></span></td>
<td><span data-ttu-id="ec672-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ec672-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ec672-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ec672-592">2,852.60</span></span></td>
<td><span data-ttu-id="ec672-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ec672-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-595">Cost object</span></span></th>
<th><span data-ttu-id="ec672-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-596">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-597">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-598">Amount</span></span></th>
<th><span data-ttu-id="ec672-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-600">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-601">Product 1</span></span></td>
<td><span data-ttu-id="ec672-602">60</span><span class="sxs-lookup"><span data-stu-id="ec672-602">60</span></span></td>
<td><span data-ttu-id="ec672-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ec672-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ec672-604">535.31</span><span class="sxs-lookup"><span data-stu-id="ec672-604">535.31</span></span></td>
<td><span data-ttu-id="ec672-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-606">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-607">Product 2</span></span></td>
<td><span data-ttu-id="ec672-608">20</span><span class="sxs-lookup"><span data-stu-id="ec672-608">20</span></span></td>
<td><span data-ttu-id="ec672-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ec672-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ec672-610">178.44</span><span class="sxs-lookup"><span data-stu-id="ec672-610">178.44</span></span></td>
<td><span data-ttu-id="ec672-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-612">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-613">Product 1</span></span></td>
<td><span data-ttu-id="ec672-614">60</span><span class="sxs-lookup"><span data-stu-id="ec672-614">60</span></span></td>
<td><span data-ttu-id="ec672-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ec672-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ec672-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ec672-616">4,487.12</span></span></td>
<td><span data-ttu-id="ec672-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-618">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-619">Product 2</span></span></td>
<td><span data-ttu-id="ec672-620">20</span><span class="sxs-lookup"><span data-stu-id="ec672-620">20</span></span></td>
<td><span data-ttu-id="ec672-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ec672-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ec672-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ec672-622">1,495.71</span></span></td>
<td><span data-ttu-id="ec672-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ec672-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ec672-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-625">Cost object</span></span></th>
<th><span data-ttu-id="ec672-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ec672-626">Magnitude</span></span></th>
<th><span data-ttu-id="ec672-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ec672-627">Allocation factor</span></span></th>
<th><span data-ttu-id="ec672-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-628">Amount</span></span></th>
<th><span data-ttu-id="ec672-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-630">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-631">Product 1</span></span></td>
<td><span data-ttu-id="ec672-632">80</span><span class="sxs-lookup"><span data-stu-id="ec672-632">80</span></span></td>
<td><span data-ttu-id="ec672-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ec672-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ec672-634">241.05</span><span class="sxs-lookup"><span data-stu-id="ec672-634">241.05</span></span></td>
<td><span data-ttu-id="ec672-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-636">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-637">Product 2</span></span></td>
<td><span data-ttu-id="ec672-638">15</span><span class="sxs-lookup"><span data-stu-id="ec672-638">15</span></span></td>
<td><span data-ttu-id="ec672-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ec672-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ec672-640">45.20</span><span class="sxs-lookup"><span data-stu-id="ec672-640">45.20</span></span></td>
<td><span data-ttu-id="ec672-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-642">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-643">Product 1</span></span></td>
<td><span data-ttu-id="ec672-644">80</span><span class="sxs-lookup"><span data-stu-id="ec672-644">80</span></span></td>
<td><span data-ttu-id="ec672-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ec672-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ec672-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ec672-646">2,507.09</span></span></td>
<td><span data-ttu-id="ec672-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-648">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-649">Product 2</span></span></td>
<td><span data-ttu-id="ec672-650">15</span><span class="sxs-lookup"><span data-stu-id="ec672-650">15</span></span></td>
<td><span data-ttu-id="ec672-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ec672-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ec672-652">470.08</span><span class="sxs-lookup"><span data-stu-id="ec672-652">470.08</span></span></td>
<td><span data-ttu-id="ec672-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ec672-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="ec672-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="ec672-655">Journal</span></span></th>
<th><span data-ttu-id="ec672-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ec672-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ec672-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ec672-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ec672-658">Version</span><span class="sxs-lookup"><span data-stu-id="ec672-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-659">00004</span><span class="sxs-lookup"><span data-stu-id="ec672-659">00004</span></span></td>
<td><span data-ttu-id="ec672-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="ec672-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ec672-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ec672-661">Fiscal</span></span></td>
<td><span data-ttu-id="ec672-662">2017</span><span class="sxs-lookup"><span data-stu-id="ec672-662">2017</span></span></td>
<td><span data-ttu-id="ec672-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ec672-663">Period 1</span></span></td>
<td><span data-ttu-id="ec672-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ec672-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ec672-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="ec672-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ec672-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-668">Cost element</span></span></th>
<th><span data-ttu-id="ec672-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-669">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-672">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-672">CC001</span></span></td>
<td><span data-ttu-id="ec672-673">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-673">HR</span></span></td>
<td><span data-ttu-id="ec672-674">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-674">10001</span></span></td>
<td><span data-ttu-id="ec672-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-675">Electricity</span></span></td>
<td><span data-ttu-id="ec672-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-676">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-677">500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-679">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-679">CC001</span></span></td>
<td><span data-ttu-id="ec672-680">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-680">HR</span></span></td>
<td><span data-ttu-id="ec672-681">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-681">10001</span></span></td>
<td><span data-ttu-id="ec672-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-682">Electricity</span></span></td>
<td><span data-ttu-id="ec672-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-683">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ec672-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-686">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-686">CC002</span></span></td>
<td><span data-ttu-id="ec672-687">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-687">Finance</span></span></td>
<td><span data-ttu-id="ec672-688">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-688">10001</span></span></td>
<td><span data-ttu-id="ec672-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-689">Electricity</span></span></td>
<td><span data-ttu-id="ec672-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-690">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-691">675.00</span><span class="sxs-lookup"><span data-stu-id="ec672-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-693">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-693">CC002</span></span></td>
<td><span data-ttu-id="ec672-694">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-694">Finance</span></span></td>
<td><span data-ttu-id="ec672-695">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-695">10001</span></span></td>
<td><span data-ttu-id="ec672-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-696">Electricity</span></span></td>
<td><span data-ttu-id="ec672-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-697">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ec672-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-700">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-700">CC003</span></span></td>
<td><span data-ttu-id="ec672-701">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-701">Assembly</span></span></td>
<td><span data-ttu-id="ec672-702">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-702">10001</span></span></td>
<td><span data-ttu-id="ec672-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-703">Electricity</span></span></td>
<td><span data-ttu-id="ec672-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-704">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-705">713.75</span><span class="sxs-lookup"><span data-stu-id="ec672-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-707">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-707">CC003</span></span></td>
<td><span data-ttu-id="ec672-708">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-708">Assembly</span></span></td>
<td><span data-ttu-id="ec672-709">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-709">10001</span></span></td>
<td><span data-ttu-id="ec672-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-710">Electricity</span></span></td>
<td><span data-ttu-id="ec672-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-711">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ec672-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-714">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-714">CC003</span></span></td>
<td><span data-ttu-id="ec672-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-715">Packaging</span></span></td>
<td><span data-ttu-id="ec672-716">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-716">10001</span></span></td>
<td><span data-ttu-id="ec672-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-717">Electricity</span></span></td>
<td><span data-ttu-id="ec672-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-718">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-719">286.25</span><span class="sxs-lookup"><span data-stu-id="ec672-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-721">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-721">CC003</span></span></td>
<td><span data-ttu-id="ec672-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-722">Packaging</span></span></td>
<td><span data-ttu-id="ec672-723">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-723">10001</span></span></td>
<td><span data-ttu-id="ec672-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-724">Electricity</span></span></td>
<td><span data-ttu-id="ec672-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-725">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ec672-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-728">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-729">Product 1</span></span></td>
<td><span data-ttu-id="ec672-730">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-730">10001</span></span></td>
<td><span data-ttu-id="ec672-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-731">Electricity</span></span></td>
<td><span data-ttu-id="ec672-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-732">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-733">776.36</span><span class="sxs-lookup"><span data-stu-id="ec672-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-735">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-736">Product 1</span></span></td>
<td><span data-ttu-id="ec672-737">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-737">10001</span></span></td>
<td><span data-ttu-id="ec672-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-738">Electricity</span></span></td>
<td><span data-ttu-id="ec672-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-739">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ec672-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-742">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-743">Product 1</span></span></td>
<td><span data-ttu-id="ec672-744">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-744">10001</span></span></td>
<td><span data-ttu-id="ec672-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-745">Electricity</span></span></td>
<td><span data-ttu-id="ec672-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-746">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-747">223.64</span><span class="sxs-lookup"><span data-stu-id="ec672-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="ec672-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-749">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-750">Product 1</span></span></td>
<td><span data-ttu-id="ec672-751">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-751">10001</span></span></td>
<td><span data-ttu-id="ec672-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-752">Electricity</span></span></td>
<td><span data-ttu-id="ec672-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-753">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ec672-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ec672-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ec672-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ec672-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ec672-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-757">Cost element</span></span></th>
<th><span data-ttu-id="ec672-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-758">Cost behavior</span></span></th>
<th><span data-ttu-id="ec672-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="ec672-759">Amount</span></span></th>
<th><span data-ttu-id="ec672-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ec672-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ec672-761">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-761">CC001</span></span></td>
<td><span data-ttu-id="ec672-762">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-762">HR</span></span></td>
<td><span data-ttu-id="ec672-763">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-763">10001</span></span></td>
<td><span data-ttu-id="ec672-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-764">Electricity</span></span></td>
<td><span data-ttu-id="ec672-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-765">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="ec672-766">-500.00</span></span></td>
<td><span data-ttu-id="ec672-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-768">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-768">CC002</span></span></td>
<td><span data-ttu-id="ec672-769">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-769">Finance</span></span></td>
<td><span data-ttu-id="ec672-770">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-770">10001</span></span></td>
<td><span data-ttu-id="ec672-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-771">Electricity</span></span></td>
<td><span data-ttu-id="ec672-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-772">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-773">175.00</span><span class="sxs-lookup"><span data-stu-id="ec672-773">175.00</span></span></td>
<td><span data-ttu-id="ec672-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-775">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-775">CC003</span></span></td>
<td><span data-ttu-id="ec672-776">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-776">Assembly</span></span></td>
<td><span data-ttu-id="ec672-777">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-777">10001</span></span></td>
<td><span data-ttu-id="ec672-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-778">Electricity</span></span></td>
<td><span data-ttu-id="ec672-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-779">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-780">275.00</span><span class="sxs-lookup"><span data-stu-id="ec672-780">275.00</span></span></td>
<td><span data-ttu-id="ec672-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-782">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-782">CC004</span></span></td>
<td><span data-ttu-id="ec672-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-783">Packaging</span></span></td>
<td><span data-ttu-id="ec672-784">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-784">10001</span></span></td>
<td><span data-ttu-id="ec672-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-785">Electricity</span></span></td>
<td><span data-ttu-id="ec672-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-786">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-787">50,00</span><span class="sxs-lookup"><span data-stu-id="ec672-787">50,00</span></span></td>
<td><span data-ttu-id="ec672-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-789">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-789">CC001</span></span></td>
<td><span data-ttu-id="ec672-790">Human Resources</span><span class="sxs-lookup"><span data-stu-id="ec672-790">HR</span></span></td>
<td><span data-ttu-id="ec672-791">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-791">10001</span></span></td>
<td><span data-ttu-id="ec672-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-792">Electricity</span></span></td>
<td><span data-ttu-id="ec672-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-793">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="ec672-794">-1,245.71</span></span></td>
<td><span data-ttu-id="ec672-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-796">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-796">CC002</span></span></td>
<td><span data-ttu-id="ec672-797">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-797">Finance</span></span></td>
<td><span data-ttu-id="ec672-798">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-798">10001</span></span></td>
<td><span data-ttu-id="ec672-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-799">Electricity</span></span></td>
<td><span data-ttu-id="ec672-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-800">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-801">436.00</span><span class="sxs-lookup"><span data-stu-id="ec672-801">436.00</span></span></td>
<td><span data-ttu-id="ec672-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-803">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-803">CC003</span></span></td>
<td><span data-ttu-id="ec672-804">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-804">Assembly</span></span></td>
<td><span data-ttu-id="ec672-805">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-805">10001</span></span></td>
<td><span data-ttu-id="ec672-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-806">Electricity</span></span></td>
<td><span data-ttu-id="ec672-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-807">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-808">685.14</span><span class="sxs-lookup"><span data-stu-id="ec672-808">685.14</span></span></td>
<td><span data-ttu-id="ec672-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-810">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-810">CC004</span></span></td>
<td><span data-ttu-id="ec672-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-811">Packaging</span></span></td>
<td><span data-ttu-id="ec672-812">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-812">10001</span></span></td>
<td><span data-ttu-id="ec672-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-813">Electricity</span></span></td>
<td><span data-ttu-id="ec672-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-814">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-815">124.57</span><span class="sxs-lookup"><span data-stu-id="ec672-815">124.57</span></span></td>
<td><span data-ttu-id="ec672-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-817">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-817">CC002</span></span></td>
<td><span data-ttu-id="ec672-818">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-818">Finance</span></span></td>
<td><span data-ttu-id="ec672-819">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-819">10001</span></span></td>
<td><span data-ttu-id="ec672-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-820">Electricity</span></span></td>
<td><span data-ttu-id="ec672-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-821">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="ec672-822">-675.00</span></span></td>
<td><span data-ttu-id="ec672-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-824">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-824">CC003</span></span></td>
<td><span data-ttu-id="ec672-825">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-825">Assembly</span></span></td>
<td><span data-ttu-id="ec672-826">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-826">10001</span></span></td>
<td><span data-ttu-id="ec672-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-827">Electricity</span></span></td>
<td><span data-ttu-id="ec672-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-828">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-829">438.75</span><span class="sxs-lookup"><span data-stu-id="ec672-829">438.75</span></span></td>
<td><span data-ttu-id="ec672-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-831">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-831">CC004</span></span></td>
<td><span data-ttu-id="ec672-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-832">Packaging</span></span></td>
<td><span data-ttu-id="ec672-833">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-833">10001</span></span></td>
<td><span data-ttu-id="ec672-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-834">Electricity</span></span></td>
<td><span data-ttu-id="ec672-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-835">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-836">236.25</span><span class="sxs-lookup"><span data-stu-id="ec672-836">236.25</span></span></td>
<td><span data-ttu-id="ec672-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-838">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-838">CC002</span></span></td>
<td><span data-ttu-id="ec672-839">Finans</span><span class="sxs-lookup"><span data-stu-id="ec672-839">Finance</span></span></td>
<td><span data-ttu-id="ec672-840">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-840">10001</span></span></td>
<td><span data-ttu-id="ec672-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-841">Electricity</span></span></td>
<td><span data-ttu-id="ec672-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-842">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="ec672-843">-8,150.29</span></span></td>
<td><span data-ttu-id="ec672-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-845">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-845">CC003</span></span></td>
<td><span data-ttu-id="ec672-846">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-846">Assembly</span></span></td>
<td><span data-ttu-id="ec672-847">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-847">10001</span></span></td>
<td><span data-ttu-id="ec672-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-848">Electricity</span></span></td>
<td><span data-ttu-id="ec672-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-849">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ec672-850">5,297.69</span></span></td>
<td><span data-ttu-id="ec672-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-852">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-852">CC004</span></span></td>
<td><span data-ttu-id="ec672-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="ec672-853">Packaging</span></span></td>
<td><span data-ttu-id="ec672-854">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-854">10001</span></span></td>
<td><span data-ttu-id="ec672-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-855">Electricity</span></span></td>
<td><span data-ttu-id="ec672-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-856">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ec672-857">2,852.60</span></span></td>
<td><span data-ttu-id="ec672-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-859">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-859">CC003</span></span></td>
<td><span data-ttu-id="ec672-860">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-860">Assembly</span></span></td>
<td><span data-ttu-id="ec672-861">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-861">10001</span></span></td>
<td><span data-ttu-id="ec672-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-862">Electricity</span></span></td>
<td><span data-ttu-id="ec672-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-863">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="ec672-864">-713.75</span></span></td>
<td><span data-ttu-id="ec672-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-866">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-867">Product 1</span></span></td>
<td><span data-ttu-id="ec672-868">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-868">10001</span></span></td>
<td><span data-ttu-id="ec672-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-869">Electricity</span></span></td>
<td><span data-ttu-id="ec672-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-870">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-871">535.31</span><span class="sxs-lookup"><span data-stu-id="ec672-871">535.31</span></span></td>
<td><span data-ttu-id="ec672-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-873">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-874">Product 2</span></span></td>
<td><span data-ttu-id="ec672-875">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-875">10001</span></span></td>
<td><span data-ttu-id="ec672-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-876">Electricity</span></span></td>
<td><span data-ttu-id="ec672-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-877">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-878">178.44</span><span class="sxs-lookup"><span data-stu-id="ec672-878">178.44</span></span></td>
<td><span data-ttu-id="ec672-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-880">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-880">CC003</span></span></td>
<td><span data-ttu-id="ec672-881">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-881">Assembly</span></span></td>
<td><span data-ttu-id="ec672-882">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-882">10001</span></span></td>
<td><span data-ttu-id="ec672-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-883">Electricity</span></span></td>
<td><span data-ttu-id="ec672-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-884">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="ec672-885">-5,982.83</span></span></td>
<td><span data-ttu-id="ec672-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-887">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-888">Product 1</span></span></td>
<td><span data-ttu-id="ec672-889">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-889">10001</span></span></td>
<td><span data-ttu-id="ec672-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-890">Electricity</span></span></td>
<td><span data-ttu-id="ec672-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-891">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ec672-892">4,487.12</span></span></td>
<td><span data-ttu-id="ec672-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-894">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-895">Product 2</span></span></td>
<td><span data-ttu-id="ec672-896">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-896">10001</span></span></td>
<td><span data-ttu-id="ec672-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-897">Electricity</span></span></td>
<td><span data-ttu-id="ec672-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-898">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ec672-899">1,495.71</span></span></td>
<td><span data-ttu-id="ec672-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-901">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-901">CC003</span></span></td>
<td><span data-ttu-id="ec672-902">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-902">Assembly</span></span></td>
<td><span data-ttu-id="ec672-903">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-903">10001</span></span></td>
<td><span data-ttu-id="ec672-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-904">Electricity</span></span></td>
<td><span data-ttu-id="ec672-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-905">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="ec672-906">-286.25</span></span></td>
<td><span data-ttu-id="ec672-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-908">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-909">Product 1</span></span></td>
<td><span data-ttu-id="ec672-910">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-910">10001</span></span></td>
<td><span data-ttu-id="ec672-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-911">Electricity</span></span></td>
<td><span data-ttu-id="ec672-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-912">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-913">241.05</span><span class="sxs-lookup"><span data-stu-id="ec672-913">241.05</span></span></td>
<td><span data-ttu-id="ec672-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-915">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-916">Product 2</span></span></td>
<td><span data-ttu-id="ec672-917">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-917">10001</span></span></td>
<td><span data-ttu-id="ec672-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-918">Electricity</span></span></td>
<td><span data-ttu-id="ec672-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-919">Fixed cost</span></span></td>
<td><span data-ttu-id="ec672-920">45.20</span><span class="sxs-lookup"><span data-stu-id="ec672-920">45.20</span></span></td>
<td><span data-ttu-id="ec672-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-922">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-922">CC003</span></span></td>
<td><span data-ttu-id="ec672-923">Samling</span><span class="sxs-lookup"><span data-stu-id="ec672-923">Assembly</span></span></td>
<td><span data-ttu-id="ec672-924">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-924">10001</span></span></td>
<td><span data-ttu-id="ec672-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-925">Electricity</span></span></td>
<td><span data-ttu-id="ec672-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-926">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="ec672-927">-2,977.17</span></span></td>
<td><span data-ttu-id="ec672-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-929">Prod 1</span></span></td>
<td><span data-ttu-id="ec672-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ec672-930">Product 1</span></span></td>
<td><span data-ttu-id="ec672-931">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-931">10001</span></span></td>
<td><span data-ttu-id="ec672-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-932">Electricity</span></span></td>
<td><span data-ttu-id="ec672-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-933">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ec672-934">2,507.09</span></span></td>
<td><span data-ttu-id="ec672-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ec672-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-936">Prod 2</span></span></td>
<td><span data-ttu-id="ec672-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ec672-937">Product 2</span></span></td>
<td><span data-ttu-id="ec672-938">10001</span><span class="sxs-lookup"><span data-stu-id="ec672-938">10001</span></span></td>
<td><span data-ttu-id="ec672-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-939">Electricity</span></span></td>
<td><span data-ttu-id="ec672-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-940">Variable cost</span></span></td>
<td><span data-ttu-id="ec672-941">470.08</span><span class="sxs-lookup"><span data-stu-id="ec672-941">470.08</span></span></td>
<td><span data-ttu-id="ec672-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ec672-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ec672-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="ec672-943">Conclusion</span></span>
<span data-ttu-id="ec672-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="ec672-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ec672-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="ec672-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ec672-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="ec672-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ec672-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ec672-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ec672-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ec672-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ec672-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ec672-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ec672-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="ec672-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ec672-951">CC099</span><span class="sxs-lookup"><span data-stu-id="ec672-951">CC099</span></span></th>
<th><span data-ttu-id="ec672-952">CC001</span><span class="sxs-lookup"><span data-stu-id="ec672-952">CC001</span></span></th>
<th><span data-ttu-id="ec672-953">CC002</span><span class="sxs-lookup"><span data-stu-id="ec672-953">CC002</span></span></th>
<th><span data-ttu-id="ec672-954">CC003</span><span class="sxs-lookup"><span data-stu-id="ec672-954">CC003</span></span></th>
<th><span data-ttu-id="ec672-955">CC004</span><span class="sxs-lookup"><span data-stu-id="ec672-955">CC004</span></span></th>
<th><span data-ttu-id="ec672-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ec672-956">Proj 1</span></span></th>
<th><span data-ttu-id="ec672-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ec672-957">Proj 2</span></span></th>
<th><span data-ttu-id="ec672-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ec672-958">Prod 1</span></span></th>
<th><span data-ttu-id="ec672-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ec672-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ec672-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ec672-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ec672-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ec672-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ec672-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-971">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ec672-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-973">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-975">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ec672-978">776.36</span><span class="sxs-lookup"><span data-stu-id="ec672-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-979">223.64</span><span class="sxs-lookup"><span data-stu-id="ec672-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ec672-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ec672-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-982">000</span><span class="sxs-lookup"><span data-stu-id="ec672-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-983">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-984">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-985">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ec672-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-987">30,00</span><span class="sxs-lookup"><span data-stu-id="ec672-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-988">10,00</span><span class="sxs-lookup"><span data-stu-id="ec672-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ec672-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ec672-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ec672-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ec672-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ec672-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ec672-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ec672-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="ec672-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ec672-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="ec672-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ec672-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="ec672-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ec672-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="ec672-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]