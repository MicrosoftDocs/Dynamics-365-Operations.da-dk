---
title: Beregning af fast omkostning
description: I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441670"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e7ed2-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7ed2-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e7ed2-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-105">Term definition</span></span>
---------------

<span data-ttu-id="e7ed2-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e7ed2-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e7ed2-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e7ed2-109">Leje</span><span class="sxs-lookup"><span data-stu-id="e7ed2-109">Rent</span></span>
-   <span data-ttu-id="e7ed2-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-110">Electricity</span></span>
-   <span data-ttu-id="e7ed2-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="e7ed2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e7ed2-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-112">Overhead calculation overview</span></span>
<span data-ttu-id="e7ed2-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e7ed2-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e7ed2-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e7ed2-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e7ed2-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e7ed2-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e7ed2-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="e7ed2-119">Version type</span></span>
-   <span data-ttu-id="e7ed2-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-120">Date and time</span></span>
-   <span data-ttu-id="e7ed2-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="e7ed2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e7ed2-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e7ed2-122">Fiscal year</span></span>
-   <span data-ttu-id="e7ed2-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-123">Fiscal period</span></span>

<span data-ttu-id="e7ed2-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e7ed2-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e7ed2-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e7ed2-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e7ed2-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e7ed2-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e7ed2-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e7ed2-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e7ed2-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e7ed2-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e7ed2-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e7ed2-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e7ed2-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e7ed2-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="e7ed2-140">Main account</span></span></th>
<th><span data-ttu-id="e7ed2-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="e7ed2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-143">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-144">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-145">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-145">10001</span></span></td>
<td><span data-ttu-id="e7ed2-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-146">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e7ed2-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="e7ed2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e7ed2-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e7ed2-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e7ed2-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e7ed2-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e7ed2-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e7ed2-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e7ed2-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e7ed2-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e7ed2-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="e7ed2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e7ed2-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="e7ed2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e7ed2-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-160">Journal</span></span></th>
<th><span data-ttu-id="e7ed2-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e7ed2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7ed2-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7ed2-163">Version</span><span class="sxs-lookup"><span data-stu-id="e7ed2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-164">00001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-164">00001</span></span></td>
<td><span data-ttu-id="e7ed2-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e7ed2-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e7ed2-166">Fiscal</span></span></td>
<td><span data-ttu-id="e7ed2-167">2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-167">2017</span></span></td>
<td><span data-ttu-id="e7ed2-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-168">Period 1</span></span></td>
<td><span data-ttu-id="e7ed2-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e7ed2-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-173">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-177">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-178">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-179">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-179">10001</span></span></td>
<td><span data-ttu-id="e7ed2-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-180">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e7ed2-181">Unclassified</span></span></td>
<td><span data-ttu-id="e7ed2-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7ed2-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e7ed2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-185">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-187">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-189">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-190">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-191">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-191">10001</span></span></td>
<td><span data-ttu-id="e7ed2-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-192">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e7ed2-193">Unclassified</span></span></td>
<td><span data-ttu-id="e7ed2-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-194">10,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-196">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-197">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-198">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-198">10001</span></span></td>
<td><span data-ttu-id="e7ed2-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-199">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e7ed2-200">Unclassified</span></span></td>
<td><span data-ttu-id="e7ed2-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-203">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-204">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-205">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-205">10001</span></span></td>
<td><span data-ttu-id="e7ed2-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-206">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-208">1,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-210">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-211">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-212">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-212">10001</span></span></td>
<td><span data-ttu-id="e7ed2-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-213">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-214">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-215">9,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e7ed2-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="e7ed2-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e7ed2-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e7ed2-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e7ed2-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="e7ed2-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e7ed2-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e7ed2-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e7ed2-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e7ed2-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e7ed2-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e7ed2-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-228">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-229">KWh</span><span class="sxs-lookup"><span data-stu-id="e7ed2-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-230">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-231">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-231">HR</span></span></td>
<td><span data-ttu-id="e7ed2-232">1.000</span><span class="sxs-lookup"><span data-stu-id="e7ed2-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-233">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-234">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-234">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-235">6.000</span><span class="sxs-lookup"><span data-stu-id="e7ed2-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-236">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-237">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-237">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-238">0</span><span class="sxs-lookup"><span data-stu-id="e7ed2-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-240">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-241">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-244">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-245">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-245">HR</span></span></td>
<td><span data-ttu-id="e7ed2-246">1.000</span><span class="sxs-lookup"><span data-stu-id="e7ed2-246">1,000</span></span></td>
<td><span data-ttu-id="e7ed2-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-249">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-250">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-250">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-251">6.000</span><span class="sxs-lookup"><span data-stu-id="e7ed2-251">6,000</span></span></td>
<td><span data-ttu-id="e7ed2-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e7ed2-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-254">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-255">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-255">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-256">0</span><span class="sxs-lookup"><span data-stu-id="e7ed2-256">0</span></span></td>
<td><span data-ttu-id="e7ed2-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e7ed2-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-261">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-262">Formel</span><span class="sxs-lookup"><span data-stu-id="e7ed2-262">Formula</span></span></th>
<th><span data-ttu-id="e7ed2-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-263">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-266">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-267">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-267">HR</span></span></td>
<td><span data-ttu-id="e7ed2-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e7ed2-269">1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-269">1</span></span></td>
<td><span data-ttu-id="e7ed2-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-271">500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-272">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-273">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-273">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e7ed2-275">1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-275">1</span></span></td>
<td><span data-ttu-id="e7ed2-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-277">500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-278">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-279">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-279">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e7ed2-281">0</span><span class="sxs-lookup"><span data-stu-id="e7ed2-281">0</span></span></td>
<td><span data-ttu-id="e7ed2-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e7ed2-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-285">Journal</span></span></th>
<th><span data-ttu-id="e7ed2-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e7ed2-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7ed2-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7ed2-288">Version</span><span class="sxs-lookup"><span data-stu-id="e7ed2-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-289">00002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-289">00002</span></span></td>
<td><span data-ttu-id="e7ed2-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e7ed2-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e7ed2-291">Fiscal</span></span></td>
<td><span data-ttu-id="e7ed2-292">2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-292">2017</span></span></td>
<td><span data-ttu-id="e7ed2-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-293">Period 1</span></span></td>
<td><span data-ttu-id="e7ed2-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e7ed2-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-298">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-302">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-303">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-304">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-304">10001</span></span></td>
<td><span data-ttu-id="e7ed2-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-305">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-309">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-310">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-311">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-311">10001</span></span></td>
<td><span data-ttu-id="e7ed2-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-312">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-313">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7ed2-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e7ed2-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-317">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-319">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-321">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-322">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-323">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-323">10001</span></span></td>
<td><span data-ttu-id="e7ed2-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-324">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-328">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-329">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-329">HR</span></span></td>
<td><span data-ttu-id="e7ed2-330">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-330">10001</span></span></td>
<td><span data-ttu-id="e7ed2-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-331">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-333">500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-333">500.00</span></span></td>
<td><span data-ttu-id="e7ed2-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-335">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-336">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-336">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-337">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-337">10001</span></span></td>
<td><span data-ttu-id="e7ed2-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-338">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-340">500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-340">500.00</span></span></td>
<td><span data-ttu-id="e7ed2-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-342">CC099</span></span></td>
<td><span data-ttu-id="e7ed2-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-343">Default cost center</span></span></td>
<td><span data-ttu-id="e7ed2-344">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-344">10001</span></span></td>
<td><span data-ttu-id="e7ed2-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-345">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-346">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e7ed2-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-349">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-350">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-350">HR</span></span></td>
<td><span data-ttu-id="e7ed2-351">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-351">10001</span></span></td>
<td><span data-ttu-id="e7ed2-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-352">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-353">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-354">1,285.71</span></span></td>
<td><span data-ttu-id="e7ed2-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-356">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-357">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-357">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-358">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-358">10001</span></span></td>
<td><span data-ttu-id="e7ed2-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-359">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-360">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e7ed2-361">7,714.29</span></span></td>
<td><span data-ttu-id="e7ed2-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e7ed2-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="e7ed2-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e7ed2-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e7ed2-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e7ed2-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="e7ed2-367">Define the overhead rate</span></span>

<span data-ttu-id="e7ed2-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e7ed2-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-370">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-371">Timer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-372">Proj 1</span></span></td>
<td><span data-ttu-id="e7ed2-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-373">Project 1</span></span></td>
<td><span data-ttu-id="e7ed2-374">3</span><span class="sxs-lookup"><span data-stu-id="e7ed2-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-375">Proj 2</span></span></td>
<td><span data-ttu-id="e7ed2-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-376">Project 2</span></span></td>
<td><span data-ttu-id="e7ed2-377">1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-379">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-380">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="e7ed2-382">Units</span></span></th>
<th><span data-ttu-id="e7ed2-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="e7ed2-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-384">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-385">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-385">HR</span></span></td>
<td><span data-ttu-id="e7ed2-386">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-386">10001</span></span></td>
<td><span data-ttu-id="e7ed2-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-387">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-388">1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-388">1</span></span></td>
<td><span data-ttu-id="e7ed2-389">10</span><span class="sxs-lookup"><span data-stu-id="e7ed2-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-391">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-392">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-393">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-396">Proj 1</span></span></td>
<td><span data-ttu-id="e7ed2-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-397">Project 1</span></span></td>
<td><span data-ttu-id="e7ed2-398">3</span><span class="sxs-lookup"><span data-stu-id="e7ed2-398">3</span></span></td>
<td><span data-ttu-id="e7ed2-399">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-399">10001</span></span></td>
<td><span data-ttu-id="e7ed2-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e7ed2-401">30,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-402">Proj 2</span></span></td>
<td><span data-ttu-id="e7ed2-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-403">Project 2</span></span></td>
<td><span data-ttu-id="e7ed2-404">1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-404">1</span></span></td>
<td><span data-ttu-id="e7ed2-405">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-405">10001</span></span></td>
<td><span data-ttu-id="e7ed2-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e7ed2-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e7ed2-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-409">Journal</span></span></th>
<th><span data-ttu-id="e7ed2-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e7ed2-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7ed2-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7ed2-412">Version</span><span class="sxs-lookup"><span data-stu-id="e7ed2-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-413">00003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-413">00003</span></span></td>
<td><span data-ttu-id="e7ed2-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="e7ed2-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e7ed2-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e7ed2-415">Fiscal</span></span></td>
<td><span data-ttu-id="e7ed2-416">2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-416">2017</span></span></td>
<td><span data-ttu-id="e7ed2-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-417">Period 1</span></span></td>
<td><span data-ttu-id="e7ed2-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e7ed2-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-421">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-424">Proj 1</span></span></td>
<td><span data-ttu-id="e7ed2-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e7ed2-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-428">Proj 2</span></span></td>
<td><span data-ttu-id="e7ed2-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e7ed2-430">1,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7ed2-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e7ed2-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-433">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-435">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-437">CC0001</span></span></td>
<td><span data-ttu-id="e7ed2-438">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-438">HR</span></span></td>
<td><span data-ttu-id="e7ed2-439">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-439">10001</span></span></td>
<td><span data-ttu-id="e7ed2-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-440">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-441">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-442">-30.00</span></span></td>
<td><span data-ttu-id="e7ed2-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-444">Proj 1</span></span></td>
<td><span data-ttu-id="e7ed2-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e7ed2-446">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-446">10001</span></span></td>
<td><span data-ttu-id="e7ed2-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-447">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-448">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-449">30,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-449">30.00</span></span></td>
<td><span data-ttu-id="e7ed2-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-451">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-452">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-452">HR</span></span></td>
<td><span data-ttu-id="e7ed2-453">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-453">10001</span></span></td>
<td><span data-ttu-id="e7ed2-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-454">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-455">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-456">-10.00</span></span></td>
<td><span data-ttu-id="e7ed2-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-458">Proj 2</span></span></td>
<td><span data-ttu-id="e7ed2-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e7ed2-460">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-460">10001</span></span></td>
<td><span data-ttu-id="e7ed2-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-461">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-462">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-463">10.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-463">10.00</span></span></td>
<td><span data-ttu-id="e7ed2-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e7ed2-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="e7ed2-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e7ed2-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e7ed2-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="e7ed2-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e7ed2-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e7ed2-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e7ed2-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e7ed2-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e7ed2-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e7ed2-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="e7ed2-475">Define the cost allocation</span></span>

<span data-ttu-id="e7ed2-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e7ed2-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e7ed2-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-479">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="e7ed2-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-481">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-482">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-482">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-483">35</span><span class="sxs-lookup"><span data-stu-id="e7ed2-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-484">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-485">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-485">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-486">55</span><span class="sxs-lookup"><span data-stu-id="e7ed2-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-487">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-488">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-489">10</span><span class="sxs-lookup"><span data-stu-id="e7ed2-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e7ed2-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-492">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="e7ed2-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-494">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-495">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-495">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-496">65</span><span class="sxs-lookup"><span data-stu-id="e7ed2-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-497">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-498">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-499">35</span><span class="sxs-lookup"><span data-stu-id="e7ed2-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e7ed2-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-502">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-504">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-505">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-506">60</span><span class="sxs-lookup"><span data-stu-id="e7ed2-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-507">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-508">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-509">20</span><span class="sxs-lookup"><span data-stu-id="e7ed2-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e7ed2-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-512">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-514">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-515">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-516">80</span><span class="sxs-lookup"><span data-stu-id="e7ed2-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-517">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-518">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-519">15</span><span class="sxs-lookup"><span data-stu-id="e7ed2-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e7ed2-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e7ed2-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e7ed2-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-523">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-524">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-526">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-528">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-529">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-529">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-530">35</span><span class="sxs-lookup"><span data-stu-id="e7ed2-530">35</span></span></td>
<td><span data-ttu-id="e7ed2-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e7ed2-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-532">175.00</span></span></td>
<td><span data-ttu-id="e7ed2-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-534">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-535">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-535">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-536">55</span><span class="sxs-lookup"><span data-stu-id="e7ed2-536">55</span></span></td>
<td><span data-ttu-id="e7ed2-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e7ed2-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-538">275.00</span></span></td>
<td><span data-ttu-id="e7ed2-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-540">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-541">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-542">10</span><span class="sxs-lookup"><span data-stu-id="e7ed2-542">10</span></span></td>
<td><span data-ttu-id="e7ed2-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e7ed2-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-544">50.00</span></span></td>
<td><span data-ttu-id="e7ed2-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-546">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-547">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-547">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-548">35</span><span class="sxs-lookup"><span data-stu-id="e7ed2-548">35</span></span></td>
<td><span data-ttu-id="e7ed2-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e7ed2-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-550">436.00</span></span></td>
<td><span data-ttu-id="e7ed2-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-552">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-553">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-553">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-554">55</span><span class="sxs-lookup"><span data-stu-id="e7ed2-554">55</span></span></td>
<td><span data-ttu-id="e7ed2-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e7ed2-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e7ed2-556">685.14</span></span></td>
<td><span data-ttu-id="e7ed2-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-558">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-559">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-560">10</span><span class="sxs-lookup"><span data-stu-id="e7ed2-560">10</span></span></td>
<td><span data-ttu-id="e7ed2-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e7ed2-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e7ed2-562">124.57</span></span></td>
<td><span data-ttu-id="e7ed2-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-565">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-566">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-568">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-570">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-571">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-571">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-572">65</span><span class="sxs-lookup"><span data-stu-id="e7ed2-572">65</span></span></td>
<td><span data-ttu-id="e7ed2-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e7ed2-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e7ed2-574">438.75</span></span></td>
<td><span data-ttu-id="e7ed2-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-576">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-577">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-578">35</span><span class="sxs-lookup"><span data-stu-id="e7ed2-578">35</span></span></td>
<td><span data-ttu-id="e7ed2-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e7ed2-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e7ed2-580">236.25</span></span></td>
<td><span data-ttu-id="e7ed2-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-582">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-583">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-583">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-584">65</span><span class="sxs-lookup"><span data-stu-id="e7ed2-584">65</span></span></td>
<td><span data-ttu-id="e7ed2-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e7ed2-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e7ed2-586">5,297.69</span></span></td>
<td><span data-ttu-id="e7ed2-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-588">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-589">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-590">35</span><span class="sxs-lookup"><span data-stu-id="e7ed2-590">35</span></span></td>
<td><span data-ttu-id="e7ed2-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e7ed2-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e7ed2-592">2,852.60</span></span></td>
<td><span data-ttu-id="e7ed2-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-595">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-596">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-598">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-600">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-601">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-602">60</span><span class="sxs-lookup"><span data-stu-id="e7ed2-602">60</span></span></td>
<td><span data-ttu-id="e7ed2-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e7ed2-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e7ed2-604">535.31</span></span></td>
<td><span data-ttu-id="e7ed2-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-606">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-607">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-608">20</span><span class="sxs-lookup"><span data-stu-id="e7ed2-608">20</span></span></td>
<td><span data-ttu-id="e7ed2-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e7ed2-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e7ed2-610">178.44</span></span></td>
<td><span data-ttu-id="e7ed2-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-612">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-613">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-614">60</span><span class="sxs-lookup"><span data-stu-id="e7ed2-614">60</span></span></td>
<td><span data-ttu-id="e7ed2-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e7ed2-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e7ed2-616">4,487.12</span></span></td>
<td><span data-ttu-id="e7ed2-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-618">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-619">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-620">20</span><span class="sxs-lookup"><span data-stu-id="e7ed2-620">20</span></span></td>
<td><span data-ttu-id="e7ed2-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e7ed2-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-622">1,495.71</span></span></td>
<td><span data-ttu-id="e7ed2-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7ed2-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-625">Cost object</span></span></th>
<th><span data-ttu-id="e7ed2-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-626">Magnitude</span></span></th>
<th><span data-ttu-id="e7ed2-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e7ed2-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e7ed2-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-628">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-630">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-631">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-632">80</span><span class="sxs-lookup"><span data-stu-id="e7ed2-632">80</span></span></td>
<td><span data-ttu-id="e7ed2-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e7ed2-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e7ed2-634">241.05</span></span></td>
<td><span data-ttu-id="e7ed2-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-636">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-637">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-638">15</span><span class="sxs-lookup"><span data-stu-id="e7ed2-638">15</span></span></td>
<td><span data-ttu-id="e7ed2-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e7ed2-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e7ed2-640">45.20</span></span></td>
<td><span data-ttu-id="e7ed2-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-642">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-643">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-644">80</span><span class="sxs-lookup"><span data-stu-id="e7ed2-644">80</span></span></td>
<td><span data-ttu-id="e7ed2-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e7ed2-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e7ed2-646">2,507.09</span></span></td>
<td><span data-ttu-id="e7ed2-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-648">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-649">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-650">15</span><span class="sxs-lookup"><span data-stu-id="e7ed2-650">15</span></span></td>
<td><span data-ttu-id="e7ed2-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e7ed2-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e7ed2-652">470.08</span></span></td>
<td><span data-ttu-id="e7ed2-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e7ed2-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="e7ed2-655">Journal</span></span></th>
<th><span data-ttu-id="e7ed2-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e7ed2-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e7ed2-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e7ed2-658">Version</span><span class="sxs-lookup"><span data-stu-id="e7ed2-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-659">00004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-659">00004</span></span></td>
<td><span data-ttu-id="e7ed2-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e7ed2-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e7ed2-661">Fiscal</span></span></td>
<td><span data-ttu-id="e7ed2-662">2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-662">2017</span></span></td>
<td><span data-ttu-id="e7ed2-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e7ed2-663">Period 1</span></span></td>
<td><span data-ttu-id="e7ed2-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e7ed2-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="e7ed2-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e7ed2-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-668">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-672">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-673">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-673">HR</span></span></td>
<td><span data-ttu-id="e7ed2-674">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-674">10001</span></span></td>
<td><span data-ttu-id="e7ed2-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-675">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-677">500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-679">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-680">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-680">HR</span></span></td>
<td><span data-ttu-id="e7ed2-681">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-681">10001</span></span></td>
<td><span data-ttu-id="e7ed2-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-682">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-683">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-686">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-687">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-687">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-688">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-688">10001</span></span></td>
<td><span data-ttu-id="e7ed2-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-689">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-693">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-694">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-694">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-695">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-695">10001</span></span></td>
<td><span data-ttu-id="e7ed2-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-696">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-697">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e7ed2-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-700">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-701">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-701">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-702">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-702">10001</span></span></td>
<td><span data-ttu-id="e7ed2-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-703">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e7ed2-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-707">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-708">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-708">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-709">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-709">10001</span></span></td>
<td><span data-ttu-id="e7ed2-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-710">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-711">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e7ed2-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-714">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-715">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-716">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-716">10001</span></span></td>
<td><span data-ttu-id="e7ed2-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-717">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e7ed2-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-721">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-722">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-723">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-723">10001</span></span></td>
<td><span data-ttu-id="e7ed2-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-724">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-725">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e7ed2-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-728">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-729">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-730">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-730">10001</span></span></td>
<td><span data-ttu-id="e7ed2-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-731">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e7ed2-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-735">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-736">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-737">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-737">10001</span></span></td>
<td><span data-ttu-id="e7ed2-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-738">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-739">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e7ed2-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-742">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-743">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-744">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-744">10001</span></span></td>
<td><span data-ttu-id="e7ed2-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-745">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e7ed2-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e7ed2-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-749">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-750">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-751">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-751">10001</span></span></td>
<td><span data-ttu-id="e7ed2-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-752">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-753">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e7ed2-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e7ed2-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e7ed2-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e7ed2-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e7ed2-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-757">Cost element</span></span></th>
<th><span data-ttu-id="e7ed2-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e7ed2-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="e7ed2-759">Amount</span></span></th>
<th><span data-ttu-id="e7ed2-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e7ed2-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e7ed2-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-761">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-762">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-762">HR</span></span></td>
<td><span data-ttu-id="e7ed2-763">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-763">10001</span></span></td>
<td><span data-ttu-id="e7ed2-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-764">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-766">-500.00</span></span></td>
<td><span data-ttu-id="e7ed2-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-768">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-769">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-769">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-770">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-770">10001</span></span></td>
<td><span data-ttu-id="e7ed2-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-771">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-773">175.00</span></span></td>
<td><span data-ttu-id="e7ed2-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-775">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-776">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-776">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-777">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-777">10001</span></span></td>
<td><span data-ttu-id="e7ed2-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-778">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-780">275.00</span></span></td>
<td><span data-ttu-id="e7ed2-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-782">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-783">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-784">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-784">10001</span></span></td>
<td><span data-ttu-id="e7ed2-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-785">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-787">50,00</span></span></td>
<td><span data-ttu-id="e7ed2-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-789">CC001</span></span></td>
<td><span data-ttu-id="e7ed2-790">Personale</span><span class="sxs-lookup"><span data-stu-id="e7ed2-790">HR</span></span></td>
<td><span data-ttu-id="e7ed2-791">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-791">10001</span></span></td>
<td><span data-ttu-id="e7ed2-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-792">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-793">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e7ed2-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-796">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-797">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-797">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-798">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-798">10001</span></span></td>
<td><span data-ttu-id="e7ed2-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-799">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-800">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-801">436.00</span></span></td>
<td><span data-ttu-id="e7ed2-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-803">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-804">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-804">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-805">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-805">10001</span></span></td>
<td><span data-ttu-id="e7ed2-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-806">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-807">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e7ed2-808">685.14</span></span></td>
<td><span data-ttu-id="e7ed2-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-810">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-811">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-812">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-812">10001</span></span></td>
<td><span data-ttu-id="e7ed2-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-813">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-814">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e7ed2-815">124.57</span></span></td>
<td><span data-ttu-id="e7ed2-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-817">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-818">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-818">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-819">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-819">10001</span></span></td>
<td><span data-ttu-id="e7ed2-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-820">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-822">-675.00</span></span></td>
<td><span data-ttu-id="e7ed2-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-824">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-825">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-825">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-826">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-826">10001</span></span></td>
<td><span data-ttu-id="e7ed2-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-827">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e7ed2-829">438.75</span></span></td>
<td><span data-ttu-id="e7ed2-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-831">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-832">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-833">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-833">10001</span></span></td>
<td><span data-ttu-id="e7ed2-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-834">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e7ed2-836">236.25</span></span></td>
<td><span data-ttu-id="e7ed2-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-838">CC002</span></span></td>
<td><span data-ttu-id="e7ed2-839">Finans</span><span class="sxs-lookup"><span data-stu-id="e7ed2-839">Finance</span></span></td>
<td><span data-ttu-id="e7ed2-840">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-840">10001</span></span></td>
<td><span data-ttu-id="e7ed2-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-841">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-842">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="e7ed2-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e7ed2-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-845">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-846">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-846">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-847">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-847">10001</span></span></td>
<td><span data-ttu-id="e7ed2-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-848">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-849">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e7ed2-850">5,297.69</span></span></td>
<td><span data-ttu-id="e7ed2-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-852">CC004</span></span></td>
<td><span data-ttu-id="e7ed2-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="e7ed2-853">Packaging</span></span></td>
<td><span data-ttu-id="e7ed2-854">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-854">10001</span></span></td>
<td><span data-ttu-id="e7ed2-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-855">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-856">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e7ed2-857">2,852.60</span></span></td>
<td><span data-ttu-id="e7ed2-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-859">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-860">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-860">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-861">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-861">10001</span></span></td>
<td><span data-ttu-id="e7ed2-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-862">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="e7ed2-864">-713.75</span></span></td>
<td><span data-ttu-id="e7ed2-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-866">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-867">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-868">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-868">10001</span></span></td>
<td><span data-ttu-id="e7ed2-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-869">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e7ed2-871">535.31</span></span></td>
<td><span data-ttu-id="e7ed2-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-873">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-874">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-875">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-875">10001</span></span></td>
<td><span data-ttu-id="e7ed2-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-876">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e7ed2-878">178.44</span></span></td>
<td><span data-ttu-id="e7ed2-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-880">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-881">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-881">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-882">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-882">10001</span></span></td>
<td><span data-ttu-id="e7ed2-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-883">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-884">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="e7ed2-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e7ed2-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-887">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-888">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-889">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-889">10001</span></span></td>
<td><span data-ttu-id="e7ed2-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-890">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-891">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e7ed2-892">4,487.12</span></span></td>
<td><span data-ttu-id="e7ed2-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-894">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-895">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-896">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-896">10001</span></span></td>
<td><span data-ttu-id="e7ed2-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-897">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-898">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e7ed2-899">1,495.71</span></span></td>
<td><span data-ttu-id="e7ed2-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-901">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-902">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-902">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-903">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-903">10001</span></span></td>
<td><span data-ttu-id="e7ed2-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-904">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="e7ed2-906">-286.25</span></span></td>
<td><span data-ttu-id="e7ed2-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-908">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-909">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-910">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-910">10001</span></span></td>
<td><span data-ttu-id="e7ed2-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-911">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e7ed2-913">241.05</span></span></td>
<td><span data-ttu-id="e7ed2-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-915">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-916">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-917">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-917">10001</span></span></td>
<td><span data-ttu-id="e7ed2-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-918">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e7ed2-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e7ed2-920">45.20</span></span></td>
<td><span data-ttu-id="e7ed2-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-922">CC003</span></span></td>
<td><span data-ttu-id="e7ed2-923">Samling</span><span class="sxs-lookup"><span data-stu-id="e7ed2-923">Assembly</span></span></td>
<td><span data-ttu-id="e7ed2-924">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-924">10001</span></span></td>
<td><span data-ttu-id="e7ed2-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-925">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-926">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="e7ed2-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e7ed2-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-929">Prod 1</span></span></td>
<td><span data-ttu-id="e7ed2-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-930">Product 1</span></span></td>
<td><span data-ttu-id="e7ed2-931">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-931">10001</span></span></td>
<td><span data-ttu-id="e7ed2-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-932">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-933">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e7ed2-934">2,507.09</span></span></td>
<td><span data-ttu-id="e7ed2-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e7ed2-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-936">Prod 2</span></span></td>
<td><span data-ttu-id="e7ed2-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-937">Product 2</span></span></td>
<td><span data-ttu-id="e7ed2-938">10001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-938">10001</span></span></td>
<td><span data-ttu-id="e7ed2-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-939">Electricity</span></span></td>
<td><span data-ttu-id="e7ed2-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-940">Variable cost</span></span></td>
<td><span data-ttu-id="e7ed2-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e7ed2-941">470.08</span></span></td>
<td><span data-ttu-id="e7ed2-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e7ed2-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e7ed2-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="e7ed2-943">Conclusion</span></span>
<span data-ttu-id="e7ed2-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e7ed2-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e7ed2-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e7ed2-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e7ed2-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e7ed2-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e7ed2-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e7ed2-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e7ed2-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e7ed2-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e7ed2-951">CC099</span></span></th>
<th><span data-ttu-id="e7ed2-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e7ed2-952">CC001</span></span></th>
<th><span data-ttu-id="e7ed2-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e7ed2-953">CC002</span></span></th>
<th><span data-ttu-id="e7ed2-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-954">CC003</span></span></th>
<th><span data-ttu-id="e7ed2-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e7ed2-955">CC004</span></span></th>
<th><span data-ttu-id="e7ed2-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-956">Proj 1</span></span></th>
<th><span data-ttu-id="e7ed2-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-957">Proj 2</span></span></th>
<th><span data-ttu-id="e7ed2-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e7ed2-958">Prod 1</span></span></th>
<th><span data-ttu-id="e7ed2-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e7ed2-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e7ed2-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e7ed2-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e7ed2-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e7ed2-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e7ed2-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e7ed2-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e7ed2-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e7ed2-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e7ed2-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-982">000</span><span class="sxs-lookup"><span data-stu-id="e7ed2-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-987">30,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e7ed2-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e7ed2-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e7ed2-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e7ed2-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e7ed2-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e7ed2-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e7ed2-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e7ed2-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e7ed2-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e7ed2-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="e7ed2-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



