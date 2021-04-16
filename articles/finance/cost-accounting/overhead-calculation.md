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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822897"
---
# <a name="overhead-calculation"></a><span data-ttu-id="df1a9-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df1a9-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="df1a9-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="df1a9-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="df1a9-105">Term definition</span></span>
---------------

<span data-ttu-id="df1a9-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="df1a9-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="df1a9-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="df1a9-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="df1a9-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="df1a9-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="df1a9-109">Leje</span><span class="sxs-lookup"><span data-stu-id="df1a9-109">Rent</span></span>
-   <span data-ttu-id="df1a9-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-110">Electricity</span></span>
-   <span data-ttu-id="df1a9-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="df1a9-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="df1a9-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-112">Overhead calculation overview</span></span>
<span data-ttu-id="df1a9-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="df1a9-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="df1a9-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="df1a9-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="df1a9-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="df1a9-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="df1a9-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="df1a9-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="df1a9-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="df1a9-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="df1a9-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="df1a9-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="df1a9-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="df1a9-119">Version type</span></span>
-   <span data-ttu-id="df1a9-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="df1a9-120">Date and time</span></span>
-   <span data-ttu-id="df1a9-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="df1a9-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="df1a9-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="df1a9-122">Fiscal year</span></span>
-   <span data-ttu-id="df1a9-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="df1a9-123">Fiscal period</span></span>

<span data-ttu-id="df1a9-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="df1a9-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="df1a9-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="df1a9-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="df1a9-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="df1a9-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="df1a9-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="df1a9-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="df1a9-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="df1a9-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="df1a9-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="df1a9-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="df1a9-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="df1a9-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="df1a9-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="df1a9-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="df1a9-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="df1a9-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="df1a9-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="df1a9-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="df1a9-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="df1a9-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="df1a9-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="df1a9-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="df1a9-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="df1a9-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="df1a9-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="df1a9-140">Main account</span></span></th>
<th><span data-ttu-id="df1a9-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="df1a9-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="df1a9-143">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-143">CC099</span></span></td>
<td><span data-ttu-id="df1a9-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-144">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-145">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-145">10001</span></span></td>
<td><span data-ttu-id="df1a9-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-146">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="df1a9-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="df1a9-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="df1a9-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="df1a9-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="df1a9-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="df1a9-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="df1a9-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-151">Define the cost behavior rule</span></span>

<span data-ttu-id="df1a9-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="df1a9-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="df1a9-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="df1a9-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="df1a9-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="df1a9-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="df1a9-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="df1a9-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="df1a9-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="df1a9-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="df1a9-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="df1a9-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="df1a9-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="df1a9-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-160">Journal</span></span></th>
<th><span data-ttu-id="df1a9-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="df1a9-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="df1a9-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="df1a9-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="df1a9-163">Version</span><span class="sxs-lookup"><span data-stu-id="df1a9-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-164">00001</span><span class="sxs-lookup"><span data-stu-id="df1a9-164">00001</span></span></td>
<td><span data-ttu-id="df1a9-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="df1a9-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="df1a9-166">Fiscal</span></span></td>
<td><span data-ttu-id="df1a9-167">2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-167">2017</span></span></td>
<td><span data-ttu-id="df1a9-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="df1a9-168">Period 1</span></span></td>
<td><span data-ttu-id="df1a9-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="df1a9-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="df1a9-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-173">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-174">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="df1a9-177">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-177">CC099</span></span></td>
<td><span data-ttu-id="df1a9-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-178">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-179">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-179">10001</span></span></td>
<td><span data-ttu-id="df1a9-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-180">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="df1a9-181">Unclassified</span></span></td>
<td><span data-ttu-id="df1a9-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="df1a9-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="df1a9-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-185">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-186">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-187">Amount</span></span></th>
<th><span data-ttu-id="df1a9-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-189">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-189">CC099</span></span></td>
<td><span data-ttu-id="df1a9-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-190">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-191">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-191">10001</span></span></td>
<td><span data-ttu-id="df1a9-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-192">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="df1a9-193">Unclassified</span></span></td>
<td><span data-ttu-id="df1a9-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-194">10,000.00</span></span></td>
<td><span data-ttu-id="df1a9-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-196">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-196">CC099</span></span></td>
<td><span data-ttu-id="df1a9-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-197">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-198">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-198">10001</span></span></td>
<td><span data-ttu-id="df1a9-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-199">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="df1a9-200">Unclassified</span></span></td>
<td><span data-ttu-id="df1a9-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-201">-10,000.00</span></span></td>
<td><span data-ttu-id="df1a9-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-203">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-203">CC099</span></span></td>
<td><span data-ttu-id="df1a9-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-204">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-205">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-205">10001</span></span></td>
<td><span data-ttu-id="df1a9-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-206">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-207">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-208">1,000.00</span></span></td>
<td><span data-ttu-id="df1a9-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-210">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-210">CC099</span></span></td>
<td><span data-ttu-id="df1a9-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-211">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-212">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-212">10001</span></span></td>
<td><span data-ttu-id="df1a9-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-213">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-214">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-215">9,000.00</span></span></td>
<td><span data-ttu-id="df1a9-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="df1a9-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="df1a9-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="df1a9-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="df1a9-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="df1a9-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="df1a9-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="df1a9-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="df1a9-221">Define the cost distribution rule</span></span>

<span data-ttu-id="df1a9-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="df1a9-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="df1a9-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="df1a9-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="df1a9-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="df1a9-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="df1a9-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="df1a9-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="df1a9-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="df1a9-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-228">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-229">KWh</span><span class="sxs-lookup"><span data-stu-id="df1a9-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-230">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-230">CC001</span></span></td>
<td><span data-ttu-id="df1a9-231">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-231">HR</span></span></td>
<td><span data-ttu-id="df1a9-232">1.000</span><span class="sxs-lookup"><span data-stu-id="df1a9-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-233">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-233">CC002</span></span></td>
<td><span data-ttu-id="df1a9-234">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-234">Finance</span></span></td>
<td><span data-ttu-id="df1a9-235">6.000</span><span class="sxs-lookup"><span data-stu-id="df1a9-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-236">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-236">CC003</span></span></td>
<td><span data-ttu-id="df1a9-237">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-237">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-238">0</span><span class="sxs-lookup"><span data-stu-id="df1a9-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="df1a9-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-240">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-241">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-242">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-244">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-244">CC001</span></span></td>
<td><span data-ttu-id="df1a9-245">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-245">HR</span></span></td>
<td><span data-ttu-id="df1a9-246">1.000</span><span class="sxs-lookup"><span data-stu-id="df1a9-246">1,000</span></span></td>
<td><span data-ttu-id="df1a9-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="df1a9-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="df1a9-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-249">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-249">CC002</span></span></td>
<td><span data-ttu-id="df1a9-250">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-250">Finance</span></span></td>
<td><span data-ttu-id="df1a9-251">6.000</span><span class="sxs-lookup"><span data-stu-id="df1a9-251">6,000</span></span></td>
<td><span data-ttu-id="df1a9-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="df1a9-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="df1a9-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-254">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-254">CC003</span></span></td>
<td><span data-ttu-id="df1a9-255">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-255">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-256">0</span><span class="sxs-lookup"><span data-stu-id="df1a9-256">0</span></span></td>
<td><span data-ttu-id="df1a9-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="df1a9-258">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="df1a9-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="df1a9-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="df1a9-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-261">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-262">Formel</span><span class="sxs-lookup"><span data-stu-id="df1a9-262">Formula</span></span></th>
<th><span data-ttu-id="df1a9-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-263">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-264">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-266">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-266">CC001</span></span></td>
<td><span data-ttu-id="df1a9-267">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-267">HR</span></span></td>
<td><span data-ttu-id="df1a9-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="df1a9-269">1</span><span class="sxs-lookup"><span data-stu-id="df1a9-269">1</span></span></td>
<td><span data-ttu-id="df1a9-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="df1a9-271">500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-272">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-272">CC002</span></span></td>
<td><span data-ttu-id="df1a9-273">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-273">Finance</span></span></td>
<td><span data-ttu-id="df1a9-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="df1a9-275">1</span><span class="sxs-lookup"><span data-stu-id="df1a9-275">1</span></span></td>
<td><span data-ttu-id="df1a9-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="df1a9-277">500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-278">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-278">CC003</span></span></td>
<td><span data-ttu-id="df1a9-279">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-279">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="df1a9-281">0</span><span class="sxs-lookup"><span data-stu-id="df1a9-281">0</span></span></td>
<td><span data-ttu-id="df1a9-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="df1a9-283">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="df1a9-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-285">Journal</span></span></th>
<th><span data-ttu-id="df1a9-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="df1a9-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="df1a9-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="df1a9-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="df1a9-288">Version</span><span class="sxs-lookup"><span data-stu-id="df1a9-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-289">00002</span><span class="sxs-lookup"><span data-stu-id="df1a9-289">00002</span></span></td>
<td><span data-ttu-id="df1a9-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="df1a9-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="df1a9-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="df1a9-291">Fiscal</span></span></td>
<td><span data-ttu-id="df1a9-292">2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-292">2017</span></span></td>
<td><span data-ttu-id="df1a9-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="df1a9-293">Period 1</span></span></td>
<td><span data-ttu-id="df1a9-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="df1a9-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="df1a9-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-298">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-299">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-302">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-302">CC099</span></span></td>
<td><span data-ttu-id="df1a9-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-303">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-304">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-304">10001</span></span></td>
<td><span data-ttu-id="df1a9-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-305">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-306">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-309">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-309">CC099</span></span></td>
<td><span data-ttu-id="df1a9-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-310">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-311">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-311">10001</span></span></td>
<td><span data-ttu-id="df1a9-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-312">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-313">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="df1a9-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="df1a9-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-317">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-318">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-319">Amount</span></span></th>
<th><span data-ttu-id="df1a9-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-321">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-321">CC099</span></span></td>
<td><span data-ttu-id="df1a9-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-322">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-323">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-323">10001</span></span></td>
<td><span data-ttu-id="df1a9-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-324">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-325">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-326">-1,000.00</span></span></td>
<td><span data-ttu-id="df1a9-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-328">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-328">CC001</span></span></td>
<td><span data-ttu-id="df1a9-329">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-329">HR</span></span></td>
<td><span data-ttu-id="df1a9-330">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-330">10001</span></span></td>
<td><span data-ttu-id="df1a9-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-331">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-332">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-333">500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-333">500.00</span></span></td>
<td><span data-ttu-id="df1a9-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-335">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-335">CC002</span></span></td>
<td><span data-ttu-id="df1a9-336">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-336">Finance</span></span></td>
<td><span data-ttu-id="df1a9-337">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-337">10001</span></span></td>
<td><span data-ttu-id="df1a9-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-338">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-339">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-340">500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-340">500.00</span></span></td>
<td><span data-ttu-id="df1a9-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-342">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-342">CC099</span></span></td>
<td><span data-ttu-id="df1a9-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="df1a9-343">Default cost center</span></span></td>
<td><span data-ttu-id="df1a9-344">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-344">10001</span></span></td>
<td><span data-ttu-id="df1a9-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-345">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-346">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-347">-9,000.00</span></span></td>
<td><span data-ttu-id="df1a9-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-349">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-349">CC001</span></span></td>
<td><span data-ttu-id="df1a9-350">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-350">HR</span></span></td>
<td><span data-ttu-id="df1a9-351">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-351">10001</span></span></td>
<td><span data-ttu-id="df1a9-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-352">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-353">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="df1a9-354">1,285.71</span></span></td>
<td><span data-ttu-id="df1a9-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-356">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-356">CC002</span></span></td>
<td><span data-ttu-id="df1a9-357">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-357">Finance</span></span></td>
<td><span data-ttu-id="df1a9-358">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-358">10001</span></span></td>
<td><span data-ttu-id="df1a9-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-359">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-360">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="df1a9-361">7,714.29</span></span></td>
<td><span data-ttu-id="df1a9-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="df1a9-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="df1a9-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="df1a9-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="df1a9-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="df1a9-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="df1a9-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="df1a9-367">Define the overhead rate</span></span>

<span data-ttu-id="df1a9-368">Omkostningsobjektet CC001 Human Resources bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="df1a9-369">Et statistisk dimensionsmedlem med navnet Human Resourcesprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="df1a9-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-370">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-371">Timer</span><span class="sxs-lookup"><span data-stu-id="df1a9-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-372">Proj 1</span></span></td>
<td><span data-ttu-id="df1a9-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-373">Project 1</span></span></td>
<td><span data-ttu-id="df1a9-374">3</span><span class="sxs-lookup"><span data-stu-id="df1a9-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-375">Proj 2</span></span></td>
<td><span data-ttu-id="df1a9-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-376">Project 2</span></span></td>
<td><span data-ttu-id="df1a9-377">1</span><span class="sxs-lookup"><span data-stu-id="df1a9-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="df1a9-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-379">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-380">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-381">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="df1a9-382">Units</span></span></th>
<th><span data-ttu-id="df1a9-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="df1a9-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-384">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-384">CC001</span></span></td>
<td><span data-ttu-id="df1a9-385">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-385">HR</span></span></td>
<td><span data-ttu-id="df1a9-386">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-386">10001</span></span></td>
<td><span data-ttu-id="df1a9-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-387">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-388">1</span><span class="sxs-lookup"><span data-stu-id="df1a9-388">1</span></span></td>
<td><span data-ttu-id="df1a9-389">10</span><span class="sxs-lookup"><span data-stu-id="df1a9-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-391">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-392">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-393">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-394">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-396">Proj 1</span></span></td>
<td><span data-ttu-id="df1a9-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-397">Project 1</span></span></td>
<td><span data-ttu-id="df1a9-398">3</span><span class="sxs-lookup"><span data-stu-id="df1a9-398">3</span></span></td>
<td><span data-ttu-id="df1a9-399">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-399">10001</span></span></td>
<td><span data-ttu-id="df1a9-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="df1a9-401">30,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-402">Proj 2</span></span></td>
<td><span data-ttu-id="df1a9-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-403">Project 2</span></span></td>
<td><span data-ttu-id="df1a9-404">1</span><span class="sxs-lookup"><span data-stu-id="df1a9-404">1</span></span></td>
<td><span data-ttu-id="df1a9-405">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-405">10001</span></span></td>
<td><span data-ttu-id="df1a9-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="df1a9-407">10,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="df1a9-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-409">Journal</span></span></th>
<th><span data-ttu-id="df1a9-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="df1a9-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="df1a9-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="df1a9-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="df1a9-412">Version</span><span class="sxs-lookup"><span data-stu-id="df1a9-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-413">00003</span><span class="sxs-lookup"><span data-stu-id="df1a9-413">00003</span></span></td>
<td><span data-ttu-id="df1a9-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="df1a9-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="df1a9-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="df1a9-415">Fiscal</span></span></td>
<td><span data-ttu-id="df1a9-416">2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-416">2017</span></span></td>
<td><span data-ttu-id="df1a9-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="df1a9-417">Period 1</span></span></td>
<td><span data-ttu-id="df1a9-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="df1a9-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="df1a9-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-421">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-424">Proj 1</span></span></td>
<td><span data-ttu-id="df1a9-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="df1a9-426">3,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-428">Proj 2</span></span></td>
<td><span data-ttu-id="df1a9-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="df1a9-430">1,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="df1a9-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="df1a9-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-433">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-434">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-435">Amount</span></span></th>
<th><span data-ttu-id="df1a9-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="df1a9-437">CC0001</span></span></td>
<td><span data-ttu-id="df1a9-438">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-438">HR</span></span></td>
<td><span data-ttu-id="df1a9-439">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-439">10001</span></span></td>
<td><span data-ttu-id="df1a9-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-440">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-441">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-442">-30.00</span></span></td>
<td><span data-ttu-id="df1a9-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-444">Proj 1</span></span></td>
<td><span data-ttu-id="df1a9-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="df1a9-446">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-446">10001</span></span></td>
<td><span data-ttu-id="df1a9-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-447">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-448">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-449">30,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-449">30.00</span></span></td>
<td><span data-ttu-id="df1a9-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-451">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-451">CC001</span></span></td>
<td><span data-ttu-id="df1a9-452">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-452">HR</span></span></td>
<td><span data-ttu-id="df1a9-453">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-453">10001</span></span></td>
<td><span data-ttu-id="df1a9-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-454">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-455">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-456">-10.00</span></span></td>
<td><span data-ttu-id="df1a9-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-458">Proj 2</span></span></td>
<td><span data-ttu-id="df1a9-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="df1a9-460">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-460">10001</span></span></td>
<td><span data-ttu-id="df1a9-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-461">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-462">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-463">10.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-463">10.00</span></span></td>
<td><span data-ttu-id="df1a9-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="df1a9-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="df1a9-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="df1a9-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="df1a9-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="df1a9-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="df1a9-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="df1a9-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="df1a9-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="df1a9-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="df1a9-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="df1a9-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="df1a9-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="df1a9-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="df1a9-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="df1a9-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="df1a9-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="df1a9-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="df1a9-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="df1a9-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="df1a9-475">Define the cost allocation</span></span>

<span data-ttu-id="df1a9-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="df1a9-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="df1a9-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="df1a9-478">Et statistisk dimensionsmedlem med navnet Human Resources-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="df1a9-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-479">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-480">Human Resources-tjenester</span><span class="sxs-lookup"><span data-stu-id="df1a9-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-481">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-481">CC002</span></span></td>
<td><span data-ttu-id="df1a9-482">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-482">Finance</span></span></td>
<td><span data-ttu-id="df1a9-483">35</span><span class="sxs-lookup"><span data-stu-id="df1a9-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-484">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-484">CC003</span></span></td>
<td><span data-ttu-id="df1a9-485">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-485">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-486">55</span><span class="sxs-lookup"><span data-stu-id="df1a9-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-487">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-487">CC004</span></span></td>
<td><span data-ttu-id="df1a9-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-488">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-489">10</span><span class="sxs-lookup"><span data-stu-id="df1a9-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="df1a9-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="df1a9-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-492">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="df1a9-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-494">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-494">CC003</span></span></td>
<td><span data-ttu-id="df1a9-495">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-495">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-496">65</span><span class="sxs-lookup"><span data-stu-id="df1a9-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-497">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-497">CC004</span></span></td>
<td><span data-ttu-id="df1a9-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-498">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-499">35</span><span class="sxs-lookup"><span data-stu-id="df1a9-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="df1a9-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="df1a9-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-502">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="df1a9-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-504">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-505">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-506">60</span><span class="sxs-lookup"><span data-stu-id="df1a9-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-507">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-508">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-509">20</span><span class="sxs-lookup"><span data-stu-id="df1a9-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="df1a9-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="df1a9-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-512">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="df1a9-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-514">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-515">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-516">80</span><span class="sxs-lookup"><span data-stu-id="df1a9-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-517">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-518">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-519">15</span><span class="sxs-lookup"><span data-stu-id="df1a9-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="df1a9-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="df1a9-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="df1a9-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="df1a9-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="df1a9-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="df1a9-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-523">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-524">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-525">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-526">Amount</span></span></th>
<th><span data-ttu-id="df1a9-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-528">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-528">CC002</span></span></td>
<td><span data-ttu-id="df1a9-529">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-529">Finance</span></span></td>
<td><span data-ttu-id="df1a9-530">35</span><span class="sxs-lookup"><span data-stu-id="df1a9-530">35</span></span></td>
<td><span data-ttu-id="df1a9-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="df1a9-532">175.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-532">175.00</span></span></td>
<td><span data-ttu-id="df1a9-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-534">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-534">CC003</span></span></td>
<td><span data-ttu-id="df1a9-535">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-535">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-536">55</span><span class="sxs-lookup"><span data-stu-id="df1a9-536">55</span></span></td>
<td><span data-ttu-id="df1a9-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="df1a9-538">275.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-538">275.00</span></span></td>
<td><span data-ttu-id="df1a9-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-540">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-540">CC004</span></span></td>
<td><span data-ttu-id="df1a9-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-541">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-542">10</span><span class="sxs-lookup"><span data-stu-id="df1a9-542">10</span></span></td>
<td><span data-ttu-id="df1a9-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="df1a9-544">50,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-544">50.00</span></span></td>
<td><span data-ttu-id="df1a9-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-546">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-546">CC002</span></span></td>
<td><span data-ttu-id="df1a9-547">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-547">Finance</span></span></td>
<td><span data-ttu-id="df1a9-548">35</span><span class="sxs-lookup"><span data-stu-id="df1a9-548">35</span></span></td>
<td><span data-ttu-id="df1a9-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="df1a9-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="df1a9-550">436.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-550">436.00</span></span></td>
<td><span data-ttu-id="df1a9-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-552">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-552">CC003</span></span></td>
<td><span data-ttu-id="df1a9-553">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-553">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-554">55</span><span class="sxs-lookup"><span data-stu-id="df1a9-554">55</span></span></td>
<td><span data-ttu-id="df1a9-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="df1a9-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="df1a9-556">685.14</span><span class="sxs-lookup"><span data-stu-id="df1a9-556">685.14</span></span></td>
<td><span data-ttu-id="df1a9-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-558">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-558">CC004</span></span></td>
<td><span data-ttu-id="df1a9-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-559">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-560">10</span><span class="sxs-lookup"><span data-stu-id="df1a9-560">10</span></span></td>
<td><span data-ttu-id="df1a9-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="df1a9-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="df1a9-562">124.57</span><span class="sxs-lookup"><span data-stu-id="df1a9-562">124.57</span></span></td>
<td><span data-ttu-id="df1a9-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="df1a9-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-565">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-566">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-567">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-568">Amount</span></span></th>
<th><span data-ttu-id="df1a9-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-570">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-570">CC003</span></span></td>
<td><span data-ttu-id="df1a9-571">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-571">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-572">65</span><span class="sxs-lookup"><span data-stu-id="df1a9-572">65</span></span></td>
<td><span data-ttu-id="df1a9-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="df1a9-574">438.75</span><span class="sxs-lookup"><span data-stu-id="df1a9-574">438.75</span></span></td>
<td><span data-ttu-id="df1a9-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-576">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-576">CC004</span></span></td>
<td><span data-ttu-id="df1a9-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-577">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-578">35</span><span class="sxs-lookup"><span data-stu-id="df1a9-578">35</span></span></td>
<td><span data-ttu-id="df1a9-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="df1a9-580">236.25</span><span class="sxs-lookup"><span data-stu-id="df1a9-580">236.25</span></span></td>
<td><span data-ttu-id="df1a9-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-582">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-582">CC003</span></span></td>
<td><span data-ttu-id="df1a9-583">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-583">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-584">65</span><span class="sxs-lookup"><span data-stu-id="df1a9-584">65</span></span></td>
<td><span data-ttu-id="df1a9-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="df1a9-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="df1a9-586">5,297.69</span></span></td>
<td><span data-ttu-id="df1a9-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-588">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-588">CC004</span></span></td>
<td><span data-ttu-id="df1a9-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-589">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-590">35</span><span class="sxs-lookup"><span data-stu-id="df1a9-590">35</span></span></td>
<td><span data-ttu-id="df1a9-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="df1a9-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="df1a9-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="df1a9-592">2,852.60</span></span></td>
<td><span data-ttu-id="df1a9-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="df1a9-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-595">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-596">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-597">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-598">Amount</span></span></th>
<th><span data-ttu-id="df1a9-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-600">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-601">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-602">60</span><span class="sxs-lookup"><span data-stu-id="df1a9-602">60</span></span></td>
<td><span data-ttu-id="df1a9-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="df1a9-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="df1a9-604">535.31</span><span class="sxs-lookup"><span data-stu-id="df1a9-604">535.31</span></span></td>
<td><span data-ttu-id="df1a9-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-606">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-607">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-608">20</span><span class="sxs-lookup"><span data-stu-id="df1a9-608">20</span></span></td>
<td><span data-ttu-id="df1a9-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="df1a9-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="df1a9-610">178.44</span><span class="sxs-lookup"><span data-stu-id="df1a9-610">178.44</span></span></td>
<td><span data-ttu-id="df1a9-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-612">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-613">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-614">60</span><span class="sxs-lookup"><span data-stu-id="df1a9-614">60</span></span></td>
<td><span data-ttu-id="df1a9-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="df1a9-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="df1a9-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="df1a9-616">4,487.12</span></span></td>
<td><span data-ttu-id="df1a9-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-618">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-619">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-620">20</span><span class="sxs-lookup"><span data-stu-id="df1a9-620">20</span></span></td>
<td><span data-ttu-id="df1a9-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="df1a9-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="df1a9-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="df1a9-622">1,495.71</span></span></td>
<td><span data-ttu-id="df1a9-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="df1a9-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="df1a9-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-625">Cost object</span></span></th>
<th><span data-ttu-id="df1a9-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="df1a9-626">Magnitude</span></span></th>
<th><span data-ttu-id="df1a9-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="df1a9-627">Allocation factor</span></span></th>
<th><span data-ttu-id="df1a9-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-628">Amount</span></span></th>
<th><span data-ttu-id="df1a9-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-630">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-631">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-632">80</span><span class="sxs-lookup"><span data-stu-id="df1a9-632">80</span></span></td>
<td><span data-ttu-id="df1a9-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="df1a9-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="df1a9-634">241.05</span><span class="sxs-lookup"><span data-stu-id="df1a9-634">241.05</span></span></td>
<td><span data-ttu-id="df1a9-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-636">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-637">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-638">15</span><span class="sxs-lookup"><span data-stu-id="df1a9-638">15</span></span></td>
<td><span data-ttu-id="df1a9-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="df1a9-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="df1a9-640">45.20</span><span class="sxs-lookup"><span data-stu-id="df1a9-640">45.20</span></span></td>
<td><span data-ttu-id="df1a9-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-642">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-643">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-644">80</span><span class="sxs-lookup"><span data-stu-id="df1a9-644">80</span></span></td>
<td><span data-ttu-id="df1a9-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="df1a9-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="df1a9-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="df1a9-646">2,507.09</span></span></td>
<td><span data-ttu-id="df1a9-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-648">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-649">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-650">15</span><span class="sxs-lookup"><span data-stu-id="df1a9-650">15</span></span></td>
<td><span data-ttu-id="df1a9-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="df1a9-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="df1a9-652">470.08</span><span class="sxs-lookup"><span data-stu-id="df1a9-652">470.08</span></span></td>
<td><span data-ttu-id="df1a9-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="df1a9-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="df1a9-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="df1a9-655">Journal</span></span></th>
<th><span data-ttu-id="df1a9-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="df1a9-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="df1a9-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="df1a9-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="df1a9-658">Version</span><span class="sxs-lookup"><span data-stu-id="df1a9-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-659">00004</span><span class="sxs-lookup"><span data-stu-id="df1a9-659">00004</span></span></td>
<td><span data-ttu-id="df1a9-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="df1a9-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="df1a9-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="df1a9-661">Fiscal</span></span></td>
<td><span data-ttu-id="df1a9-662">2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-662">2017</span></span></td>
<td><span data-ttu-id="df1a9-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="df1a9-663">Period 1</span></span></td>
<td><span data-ttu-id="df1a9-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="df1a9-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="df1a9-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="df1a9-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-668">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-669">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-672">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-672">CC001</span></span></td>
<td><span data-ttu-id="df1a9-673">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-673">HR</span></span></td>
<td><span data-ttu-id="df1a9-674">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-674">10001</span></span></td>
<td><span data-ttu-id="df1a9-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-675">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-676">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-677">500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-679">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-679">CC001</span></span></td>
<td><span data-ttu-id="df1a9-680">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-680">HR</span></span></td>
<td><span data-ttu-id="df1a9-681">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-681">10001</span></span></td>
<td><span data-ttu-id="df1a9-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-682">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-683">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="df1a9-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-686">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-686">CC002</span></span></td>
<td><span data-ttu-id="df1a9-687">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-687">Finance</span></span></td>
<td><span data-ttu-id="df1a9-688">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-688">10001</span></span></td>
<td><span data-ttu-id="df1a9-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-689">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-690">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-691">675.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-693">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-693">CC002</span></span></td>
<td><span data-ttu-id="df1a9-694">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-694">Finance</span></span></td>
<td><span data-ttu-id="df1a9-695">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-695">10001</span></span></td>
<td><span data-ttu-id="df1a9-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-696">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-697">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="df1a9-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-700">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-700">CC003</span></span></td>
<td><span data-ttu-id="df1a9-701">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-701">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-702">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-702">10001</span></span></td>
<td><span data-ttu-id="df1a9-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-703">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-704">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-705">713.75</span><span class="sxs-lookup"><span data-stu-id="df1a9-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-707">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-707">CC003</span></span></td>
<td><span data-ttu-id="df1a9-708">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-708">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-709">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-709">10001</span></span></td>
<td><span data-ttu-id="df1a9-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-710">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-711">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="df1a9-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-714">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-714">CC003</span></span></td>
<td><span data-ttu-id="df1a9-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-715">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-716">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-716">10001</span></span></td>
<td><span data-ttu-id="df1a9-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-717">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-718">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-719">286.25</span><span class="sxs-lookup"><span data-stu-id="df1a9-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-721">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-721">CC003</span></span></td>
<td><span data-ttu-id="df1a9-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-722">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-723">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-723">10001</span></span></td>
<td><span data-ttu-id="df1a9-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-724">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-725">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="df1a9-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-728">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-729">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-730">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-730">10001</span></span></td>
<td><span data-ttu-id="df1a9-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-731">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-732">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-733">776.36</span><span class="sxs-lookup"><span data-stu-id="df1a9-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-735">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-736">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-737">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-737">10001</span></span></td>
<td><span data-ttu-id="df1a9-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-738">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-739">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="df1a9-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-742">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-743">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-744">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-744">10001</span></span></td>
<td><span data-ttu-id="df1a9-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-745">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-746">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-747">223.64</span><span class="sxs-lookup"><span data-stu-id="df1a9-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="df1a9-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-749">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-750">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-751">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-751">10001</span></span></td>
<td><span data-ttu-id="df1a9-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-752">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-753">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="df1a9-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="df1a9-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="df1a9-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="df1a9-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="df1a9-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-757">Cost element</span></span></th>
<th><span data-ttu-id="df1a9-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-758">Cost behavior</span></span></th>
<th><span data-ttu-id="df1a9-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="df1a9-759">Amount</span></span></th>
<th><span data-ttu-id="df1a9-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="df1a9-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="df1a9-761">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-761">CC001</span></span></td>
<td><span data-ttu-id="df1a9-762">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-762">HR</span></span></td>
<td><span data-ttu-id="df1a9-763">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-763">10001</span></span></td>
<td><span data-ttu-id="df1a9-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-764">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-765">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-766">-500.00</span></span></td>
<td><span data-ttu-id="df1a9-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-768">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-768">CC002</span></span></td>
<td><span data-ttu-id="df1a9-769">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-769">Finance</span></span></td>
<td><span data-ttu-id="df1a9-770">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-770">10001</span></span></td>
<td><span data-ttu-id="df1a9-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-771">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-772">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-773">175.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-773">175.00</span></span></td>
<td><span data-ttu-id="df1a9-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-775">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-775">CC003</span></span></td>
<td><span data-ttu-id="df1a9-776">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-776">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-777">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-777">10001</span></span></td>
<td><span data-ttu-id="df1a9-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-778">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-779">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-780">275.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-780">275.00</span></span></td>
<td><span data-ttu-id="df1a9-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-782">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-782">CC004</span></span></td>
<td><span data-ttu-id="df1a9-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-783">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-784">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-784">10001</span></span></td>
<td><span data-ttu-id="df1a9-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-785">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-786">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-787">50,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-787">50,00</span></span></td>
<td><span data-ttu-id="df1a9-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-789">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-789">CC001</span></span></td>
<td><span data-ttu-id="df1a9-790">Human Resources</span><span class="sxs-lookup"><span data-stu-id="df1a9-790">HR</span></span></td>
<td><span data-ttu-id="df1a9-791">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-791">10001</span></span></td>
<td><span data-ttu-id="df1a9-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-792">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-793">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="df1a9-794">-1,245.71</span></span></td>
<td><span data-ttu-id="df1a9-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-796">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-796">CC002</span></span></td>
<td><span data-ttu-id="df1a9-797">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-797">Finance</span></span></td>
<td><span data-ttu-id="df1a9-798">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-798">10001</span></span></td>
<td><span data-ttu-id="df1a9-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-799">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-800">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-801">436.00</span><span class="sxs-lookup"><span data-stu-id="df1a9-801">436.00</span></span></td>
<td><span data-ttu-id="df1a9-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-803">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-803">CC003</span></span></td>
<td><span data-ttu-id="df1a9-804">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-804">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-805">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-805">10001</span></span></td>
<td><span data-ttu-id="df1a9-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-806">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-807">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-808">685.14</span><span class="sxs-lookup"><span data-stu-id="df1a9-808">685.14</span></span></td>
<td><span data-ttu-id="df1a9-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-810">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-810">CC004</span></span></td>
<td><span data-ttu-id="df1a9-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-811">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-812">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-812">10001</span></span></td>
<td><span data-ttu-id="df1a9-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-813">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-814">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-815">124.57</span><span class="sxs-lookup"><span data-stu-id="df1a9-815">124.57</span></span></td>
<td><span data-ttu-id="df1a9-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-817">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-817">CC002</span></span></td>
<td><span data-ttu-id="df1a9-818">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-818">Finance</span></span></td>
<td><span data-ttu-id="df1a9-819">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-819">10001</span></span></td>
<td><span data-ttu-id="df1a9-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-820">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-821">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-822">-675.00</span></span></td>
<td><span data-ttu-id="df1a9-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-824">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-824">CC003</span></span></td>
<td><span data-ttu-id="df1a9-825">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-825">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-826">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-826">10001</span></span></td>
<td><span data-ttu-id="df1a9-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-827">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-828">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-829">438.75</span><span class="sxs-lookup"><span data-stu-id="df1a9-829">438.75</span></span></td>
<td><span data-ttu-id="df1a9-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-831">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-831">CC004</span></span></td>
<td><span data-ttu-id="df1a9-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-832">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-833">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-833">10001</span></span></td>
<td><span data-ttu-id="df1a9-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-834">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-835">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-836">236.25</span><span class="sxs-lookup"><span data-stu-id="df1a9-836">236.25</span></span></td>
<td><span data-ttu-id="df1a9-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-838">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-838">CC002</span></span></td>
<td><span data-ttu-id="df1a9-839">Finans</span><span class="sxs-lookup"><span data-stu-id="df1a9-839">Finance</span></span></td>
<td><span data-ttu-id="df1a9-840">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-840">10001</span></span></td>
<td><span data-ttu-id="df1a9-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-841">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-842">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="df1a9-843">-8,150.29</span></span></td>
<td><span data-ttu-id="df1a9-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-845">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-845">CC003</span></span></td>
<td><span data-ttu-id="df1a9-846">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-846">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-847">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-847">10001</span></span></td>
<td><span data-ttu-id="df1a9-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-848">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-849">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="df1a9-850">5,297.69</span></span></td>
<td><span data-ttu-id="df1a9-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-852">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-852">CC004</span></span></td>
<td><span data-ttu-id="df1a9-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="df1a9-853">Packaging</span></span></td>
<td><span data-ttu-id="df1a9-854">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-854">10001</span></span></td>
<td><span data-ttu-id="df1a9-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-855">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-856">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="df1a9-857">2,852.60</span></span></td>
<td><span data-ttu-id="df1a9-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-859">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-859">CC003</span></span></td>
<td><span data-ttu-id="df1a9-860">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-860">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-861">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-861">10001</span></span></td>
<td><span data-ttu-id="df1a9-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-862">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-863">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="df1a9-864">-713.75</span></span></td>
<td><span data-ttu-id="df1a9-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-866">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-867">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-868">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-868">10001</span></span></td>
<td><span data-ttu-id="df1a9-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-869">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-870">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-871">535.31</span><span class="sxs-lookup"><span data-stu-id="df1a9-871">535.31</span></span></td>
<td><span data-ttu-id="df1a9-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-873">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-874">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-875">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-875">10001</span></span></td>
<td><span data-ttu-id="df1a9-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-876">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-877">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-878">178.44</span><span class="sxs-lookup"><span data-stu-id="df1a9-878">178.44</span></span></td>
<td><span data-ttu-id="df1a9-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-880">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-880">CC003</span></span></td>
<td><span data-ttu-id="df1a9-881">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-881">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-882">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-882">10001</span></span></td>
<td><span data-ttu-id="df1a9-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-883">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-884">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="df1a9-885">-5,982.83</span></span></td>
<td><span data-ttu-id="df1a9-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-887">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-888">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-889">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-889">10001</span></span></td>
<td><span data-ttu-id="df1a9-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-890">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-891">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="df1a9-892">4,487.12</span></span></td>
<td><span data-ttu-id="df1a9-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-894">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-895">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-896">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-896">10001</span></span></td>
<td><span data-ttu-id="df1a9-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-897">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-898">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="df1a9-899">1,495.71</span></span></td>
<td><span data-ttu-id="df1a9-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-901">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-901">CC003</span></span></td>
<td><span data-ttu-id="df1a9-902">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-902">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-903">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-903">10001</span></span></td>
<td><span data-ttu-id="df1a9-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-904">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-905">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="df1a9-906">-286.25</span></span></td>
<td><span data-ttu-id="df1a9-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-908">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-909">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-910">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-910">10001</span></span></td>
<td><span data-ttu-id="df1a9-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-911">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-912">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-913">241.05</span><span class="sxs-lookup"><span data-stu-id="df1a9-913">241.05</span></span></td>
<td><span data-ttu-id="df1a9-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-915">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-916">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-917">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-917">10001</span></span></td>
<td><span data-ttu-id="df1a9-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-918">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-919">Fixed cost</span></span></td>
<td><span data-ttu-id="df1a9-920">45.20</span><span class="sxs-lookup"><span data-stu-id="df1a9-920">45.20</span></span></td>
<td><span data-ttu-id="df1a9-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-922">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-922">CC003</span></span></td>
<td><span data-ttu-id="df1a9-923">Samling</span><span class="sxs-lookup"><span data-stu-id="df1a9-923">Assembly</span></span></td>
<td><span data-ttu-id="df1a9-924">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-924">10001</span></span></td>
<td><span data-ttu-id="df1a9-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-925">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-926">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="df1a9-927">-2,977.17</span></span></td>
<td><span data-ttu-id="df1a9-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-929">Prod 1</span></span></td>
<td><span data-ttu-id="df1a9-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-930">Product 1</span></span></td>
<td><span data-ttu-id="df1a9-931">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-931">10001</span></span></td>
<td><span data-ttu-id="df1a9-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-932">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-933">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="df1a9-934">2,507.09</span></span></td>
<td><span data-ttu-id="df1a9-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="df1a9-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-936">Prod 2</span></span></td>
<td><span data-ttu-id="df1a9-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-937">Product 2</span></span></td>
<td><span data-ttu-id="df1a9-938">10001</span><span class="sxs-lookup"><span data-stu-id="df1a9-938">10001</span></span></td>
<td><span data-ttu-id="df1a9-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-939">Electricity</span></span></td>
<td><span data-ttu-id="df1a9-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-940">Variable cost</span></span></td>
<td><span data-ttu-id="df1a9-941">470.08</span><span class="sxs-lookup"><span data-stu-id="df1a9-941">470.08</span></span></td>
<td><span data-ttu-id="df1a9-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="df1a9-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="df1a9-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="df1a9-943">Conclusion</span></span>
<span data-ttu-id="df1a9-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="df1a9-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="df1a9-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="df1a9-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="df1a9-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="df1a9-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="df1a9-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="df1a9-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="df1a9-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="df1a9-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="df1a9-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="df1a9-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="df1a9-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="df1a9-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="df1a9-951">CC099</span><span class="sxs-lookup"><span data-stu-id="df1a9-951">CC099</span></span></th>
<th><span data-ttu-id="df1a9-952">CC001</span><span class="sxs-lookup"><span data-stu-id="df1a9-952">CC001</span></span></th>
<th><span data-ttu-id="df1a9-953">CC002</span><span class="sxs-lookup"><span data-stu-id="df1a9-953">CC002</span></span></th>
<th><span data-ttu-id="df1a9-954">CC003</span><span class="sxs-lookup"><span data-stu-id="df1a9-954">CC003</span></span></th>
<th><span data-ttu-id="df1a9-955">CC004</span><span class="sxs-lookup"><span data-stu-id="df1a9-955">CC004</span></span></th>
<th><span data-ttu-id="df1a9-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-956">Proj 1</span></span></th>
<th><span data-ttu-id="df1a9-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-957">Proj 2</span></span></th>
<th><span data-ttu-id="df1a9-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="df1a9-958">Prod 1</span></span></th>
<th><span data-ttu-id="df1a9-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="df1a9-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="df1a9-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="df1a9-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="df1a9-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="df1a9-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-971">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="df1a9-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-973">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-974">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-975">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-976">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-977">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-978">776.36</span><span class="sxs-lookup"><span data-stu-id="df1a9-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-979">223.64</span><span class="sxs-lookup"><span data-stu-id="df1a9-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="df1a9-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="df1a9-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-982">000</span><span class="sxs-lookup"><span data-stu-id="df1a9-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-983">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-984">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-985">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-986">0,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-987">30,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-988">10,00</span><span class="sxs-lookup"><span data-stu-id="df1a9-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="df1a9-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="df1a9-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="df1a9-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="df1a9-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="df1a9-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="df1a9-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="df1a9-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="df1a9-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="df1a9-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="df1a9-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="df1a9-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="df1a9-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="df1a9-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="df1a9-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]