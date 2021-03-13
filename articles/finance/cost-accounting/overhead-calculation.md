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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009512"
---
# <a name="overhead-calculation"></a><span data-ttu-id="d044c-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d044c-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="d044c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="d044c-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="d044c-105">Term definition</span></span>
---------------

<span data-ttu-id="d044c-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="d044c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="d044c-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="d044c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="d044c-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="d044c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="d044c-109">Leje</span><span class="sxs-lookup"><span data-stu-id="d044c-109">Rent</span></span>
-   <span data-ttu-id="d044c-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-110">Electricity</span></span>
-   <span data-ttu-id="d044c-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="d044c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="d044c-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-112">Overhead calculation overview</span></span>
<span data-ttu-id="d044c-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="d044c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="d044c-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="d044c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="d044c-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="d044c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="d044c-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d044c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="d044c-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="d044c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="d044c-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="d044c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="d044c-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="d044c-119">Version type</span></span>
-   <span data-ttu-id="d044c-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="d044c-120">Date and time</span></span>
-   <span data-ttu-id="d044c-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="d044c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="d044c-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d044c-122">Fiscal year</span></span>
-   <span data-ttu-id="d044c-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="d044c-123">Fiscal period</span></span>

<span data-ttu-id="d044c-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="d044c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="d044c-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="d044c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="d044c-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="d044c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="d044c-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="d044c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="d044c-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="d044c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="d044c-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="d044c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="d044c-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="d044c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="d044c-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="d044c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="d044c-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="d044c-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="d044c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="d044c-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="d044c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="d044c-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="d044c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="d044c-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="d044c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="d044c-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="d044c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="d044c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="d044c-140">Main account</span></span></th>
<th><span data-ttu-id="d044c-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="d044c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="d044c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-143">CC099</span></span></td>
<td><span data-ttu-id="d044c-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-144">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-145">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-145">10001</span></span></td>
<td><span data-ttu-id="d044c-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-146">Electricity</span></span></td>
<td><span data-ttu-id="d044c-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="d044c-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="d044c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="d044c-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="d044c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="d044c-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="d044c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="d044c-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="d044c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="d044c-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="d044c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="d044c-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="d044c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="d044c-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="d044c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="d044c-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="d044c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="d044c-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="d044c-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="d044c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="d044c-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="d044c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="d044c-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-160">Journal</span></span></th>
<th><span data-ttu-id="d044c-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="d044c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d044c-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d044c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d044c-163">Version</span><span class="sxs-lookup"><span data-stu-id="d044c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-164">00001</span><span class="sxs-lookup"><span data-stu-id="d044c-164">00001</span></span></td>
<td><span data-ttu-id="d044c-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="d044c-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d044c-166">Fiscal</span></span></td>
<td><span data-ttu-id="d044c-167">2017</span><span class="sxs-lookup"><span data-stu-id="d044c-167">2017</span></span></td>
<td><span data-ttu-id="d044c-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="d044c-168">Period 1</span></span></td>
<td><span data-ttu-id="d044c-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="d044c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d044c-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="d044c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-173">Cost element</span></span></th>
<th><span data-ttu-id="d044c-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="d044c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-177">CC099</span></span></td>
<td><span data-ttu-id="d044c-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-178">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-179">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-179">10001</span></span></td>
<td><span data-ttu-id="d044c-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-180">Electricity</span></span></td>
<td><span data-ttu-id="d044c-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="d044c-181">Unclassified</span></span></td>
<td><span data-ttu-id="d044c-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d044c-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="d044c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-185">Cost element</span></span></th>
<th><span data-ttu-id="d044c-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-187">Amount</span></span></th>
<th><span data-ttu-id="d044c-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-189">CC099</span></span></td>
<td><span data-ttu-id="d044c-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-190">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-191">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-191">10001</span></span></td>
<td><span data-ttu-id="d044c-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-192">Electricity</span></span></td>
<td><span data-ttu-id="d044c-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="d044c-193">Unclassified</span></span></td>
<td><span data-ttu-id="d044c-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-194">10,000.00</span></span></td>
<td><span data-ttu-id="d044c-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-196">CC099</span></span></td>
<td><span data-ttu-id="d044c-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-197">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-198">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-198">10001</span></span></td>
<td><span data-ttu-id="d044c-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-199">Electricity</span></span></td>
<td><span data-ttu-id="d044c-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="d044c-200">Unclassified</span></span></td>
<td><span data-ttu-id="d044c-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="d044c-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-203">CC099</span></span></td>
<td><span data-ttu-id="d044c-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-204">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-205">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-205">10001</span></span></td>
<td><span data-ttu-id="d044c-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-206">Electricity</span></span></td>
<td><span data-ttu-id="d044c-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-208">1,000.00</span></span></td>
<td><span data-ttu-id="d044c-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-210">CC099</span></span></td>
<td><span data-ttu-id="d044c-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-211">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-212">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-212">10001</span></span></td>
<td><span data-ttu-id="d044c-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-213">Electricity</span></span></td>
<td><span data-ttu-id="d044c-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-214">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-215">9,000.00</span></span></td>
<td><span data-ttu-id="d044c-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="d044c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="d044c-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="d044c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="d044c-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="d044c-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="d044c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="d044c-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="d044c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="d044c-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="d044c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="d044c-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="d044c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="d044c-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="d044c-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="d044c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="d044c-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="d044c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="d044c-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-228">Cost object</span></span></th>
<th><span data-ttu-id="d044c-229">KWh</span><span class="sxs-lookup"><span data-stu-id="d044c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-230">CC001</span></span></td>
<td><span data-ttu-id="d044c-231">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-231">HR</span></span></td>
<td><span data-ttu-id="d044c-232">1.000</span><span class="sxs-lookup"><span data-stu-id="d044c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-233">CC002</span></span></td>
<td><span data-ttu-id="d044c-234">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-234">Finance</span></span></td>
<td><span data-ttu-id="d044c-235">6.000</span><span class="sxs-lookup"><span data-stu-id="d044c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-236">CC003</span></span></td>
<td><span data-ttu-id="d044c-237">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-237">Assembly</span></span></td>
<td><span data-ttu-id="d044c-238">0</span><span class="sxs-lookup"><span data-stu-id="d044c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="d044c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-240">Cost object</span></span></th>
<th><span data-ttu-id="d044c-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-241">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-244">CC001</span></span></td>
<td><span data-ttu-id="d044c-245">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-245">HR</span></span></td>
<td><span data-ttu-id="d044c-246">1.000</span><span class="sxs-lookup"><span data-stu-id="d044c-246">1,000</span></span></td>
<td><span data-ttu-id="d044c-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d044c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d044c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-249">CC002</span></span></td>
<td><span data-ttu-id="d044c-250">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-250">Finance</span></span></td>
<td><span data-ttu-id="d044c-251">6.000</span><span class="sxs-lookup"><span data-stu-id="d044c-251">6,000</span></span></td>
<td><span data-ttu-id="d044c-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d044c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d044c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-254">CC003</span></span></td>
<td><span data-ttu-id="d044c-255">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-255">Assembly</span></span></td>
<td><span data-ttu-id="d044c-256">0</span><span class="sxs-lookup"><span data-stu-id="d044c-256">0</span></span></td>
<td><span data-ttu-id="d044c-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d044c-258">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="d044c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="d044c-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="d044c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-261">Cost object</span></span></th>
<th><span data-ttu-id="d044c-262">Formel</span><span class="sxs-lookup"><span data-stu-id="d044c-262">Formula</span></span></th>
<th><span data-ttu-id="d044c-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-263">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-266">CC001</span></span></td>
<td><span data-ttu-id="d044c-267">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-267">HR</span></span></td>
<td><span data-ttu-id="d044c-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d044c-269">1</span><span class="sxs-lookup"><span data-stu-id="d044c-269">1</span></span></td>
<td><span data-ttu-id="d044c-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d044c-271">500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-272">CC002</span></span></td>
<td><span data-ttu-id="d044c-273">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-273">Finance</span></span></td>
<td><span data-ttu-id="d044c-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d044c-275">1</span><span class="sxs-lookup"><span data-stu-id="d044c-275">1</span></span></td>
<td><span data-ttu-id="d044c-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d044c-277">500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-278">CC003</span></span></td>
<td><span data-ttu-id="d044c-279">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-279">Assembly</span></span></td>
<td><span data-ttu-id="d044c-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d044c-281">0</span><span class="sxs-lookup"><span data-stu-id="d044c-281">0</span></span></td>
<td><span data-ttu-id="d044c-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d044c-283">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d044c-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-285">Journal</span></span></th>
<th><span data-ttu-id="d044c-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="d044c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d044c-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d044c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d044c-288">Version</span><span class="sxs-lookup"><span data-stu-id="d044c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-289">00002</span><span class="sxs-lookup"><span data-stu-id="d044c-289">00002</span></span></td>
<td><span data-ttu-id="d044c-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="d044c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="d044c-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d044c-291">Fiscal</span></span></td>
<td><span data-ttu-id="d044c-292">2017</span><span class="sxs-lookup"><span data-stu-id="d044c-292">2017</span></span></td>
<td><span data-ttu-id="d044c-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="d044c-293">Period 1</span></span></td>
<td><span data-ttu-id="d044c-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="d044c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d044c-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="d044c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-298">Cost element</span></span></th>
<th><span data-ttu-id="d044c-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-302">CC099</span></span></td>
<td><span data-ttu-id="d044c-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-303">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-304">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-304">10001</span></span></td>
<td><span data-ttu-id="d044c-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-305">Electricity</span></span></td>
<td><span data-ttu-id="d044c-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-309">CC099</span></span></td>
<td><span data-ttu-id="d044c-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-310">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-311">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-311">10001</span></span></td>
<td><span data-ttu-id="d044c-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-312">Electricity</span></span></td>
<td><span data-ttu-id="d044c-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-313">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d044c-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="d044c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-317">Cost element</span></span></th>
<th><span data-ttu-id="d044c-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-319">Amount</span></span></th>
<th><span data-ttu-id="d044c-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-321">CC099</span></span></td>
<td><span data-ttu-id="d044c-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-322">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-323">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-323">10001</span></span></td>
<td><span data-ttu-id="d044c-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-324">Electricity</span></span></td>
<td><span data-ttu-id="d044c-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="d044c-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-328">CC001</span></span></td>
<td><span data-ttu-id="d044c-329">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-329">HR</span></span></td>
<td><span data-ttu-id="d044c-330">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-330">10001</span></span></td>
<td><span data-ttu-id="d044c-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-331">Electricity</span></span></td>
<td><span data-ttu-id="d044c-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-333">500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-333">500.00</span></span></td>
<td><span data-ttu-id="d044c-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-335">CC002</span></span></td>
<td><span data-ttu-id="d044c-336">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-336">Finance</span></span></td>
<td><span data-ttu-id="d044c-337">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-337">10001</span></span></td>
<td><span data-ttu-id="d044c-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-338">Electricity</span></span></td>
<td><span data-ttu-id="d044c-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-340">500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-340">500.00</span></span></td>
<td><span data-ttu-id="d044c-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-342">CC099</span></span></td>
<td><span data-ttu-id="d044c-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="d044c-343">Default cost center</span></span></td>
<td><span data-ttu-id="d044c-344">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-344">10001</span></span></td>
<td><span data-ttu-id="d044c-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-345">Electricity</span></span></td>
<td><span data-ttu-id="d044c-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-346">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="d044c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="d044c-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-349">CC001</span></span></td>
<td><span data-ttu-id="d044c-350">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-350">HR</span></span></td>
<td><span data-ttu-id="d044c-351">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-351">10001</span></span></td>
<td><span data-ttu-id="d044c-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-352">Electricity</span></span></td>
<td><span data-ttu-id="d044c-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-353">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d044c-354">1,285.71</span></span></td>
<td><span data-ttu-id="d044c-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-356">CC002</span></span></td>
<td><span data-ttu-id="d044c-357">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-357">Finance</span></span></td>
<td><span data-ttu-id="d044c-358">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-358">10001</span></span></td>
<td><span data-ttu-id="d044c-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-359">Electricity</span></span></td>
<td><span data-ttu-id="d044c-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-360">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d044c-361">7,714.29</span></span></td>
<td><span data-ttu-id="d044c-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="d044c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="d044c-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="d044c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="d044c-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="d044c-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="d044c-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="d044c-367">Define the overhead rate</span></span>

<span data-ttu-id="d044c-368">Omkostningsobjektet CC001 Human Resources bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="d044c-369">Et statistisk dimensionsmedlem med navnet Human Resourcesprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="d044c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-370">Cost object</span></span></th>
<th><span data-ttu-id="d044c-371">Timer</span><span class="sxs-lookup"><span data-stu-id="d044c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-372">Proj 1</span></span></td>
<td><span data-ttu-id="d044c-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-373">Project 1</span></span></td>
<td><span data-ttu-id="d044c-374">3</span><span class="sxs-lookup"><span data-stu-id="d044c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-375">Proj 2</span></span></td>
<td><span data-ttu-id="d044c-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-376">Project 2</span></span></td>
<td><span data-ttu-id="d044c-377">1</span><span class="sxs-lookup"><span data-stu-id="d044c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="d044c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-379">Cost object</span></span></th>
<th><span data-ttu-id="d044c-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-380">Cost element</span></span></th>
<th><span data-ttu-id="d044c-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="d044c-382">Units</span></span></th>
<th><span data-ttu-id="d044c-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="d044c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-384">CC001</span></span></td>
<td><span data-ttu-id="d044c-385">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-385">HR</span></span></td>
<td><span data-ttu-id="d044c-386">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-386">10001</span></span></td>
<td><span data-ttu-id="d044c-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-387">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-388">1</span><span class="sxs-lookup"><span data-stu-id="d044c-388">1</span></span></td>
<td><span data-ttu-id="d044c-389">10</span><span class="sxs-lookup"><span data-stu-id="d044c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-391">Cost object</span></span></th>
<th><span data-ttu-id="d044c-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-392">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-393">Cost element</span></span></th>
<th><span data-ttu-id="d044c-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-396">Proj 1</span></span></td>
<td><span data-ttu-id="d044c-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-397">Project 1</span></span></td>
<td><span data-ttu-id="d044c-398">3</span><span class="sxs-lookup"><span data-stu-id="d044c-398">3</span></span></td>
<td><span data-ttu-id="d044c-399">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-399">10001</span></span></td>
<td><span data-ttu-id="d044c-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d044c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d044c-401">30,00</span><span class="sxs-lookup"><span data-stu-id="d044c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-402">Proj 2</span></span></td>
<td><span data-ttu-id="d044c-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-403">Project 2</span></span></td>
<td><span data-ttu-id="d044c-404">1</span><span class="sxs-lookup"><span data-stu-id="d044c-404">1</span></span></td>
<td><span data-ttu-id="d044c-405">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-405">10001</span></span></td>
<td><span data-ttu-id="d044c-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d044c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d044c-407">10,00</span><span class="sxs-lookup"><span data-stu-id="d044c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d044c-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-409">Journal</span></span></th>
<th><span data-ttu-id="d044c-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="d044c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d044c-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d044c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d044c-412">Version</span><span class="sxs-lookup"><span data-stu-id="d044c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-413">00003</span><span class="sxs-lookup"><span data-stu-id="d044c-413">00003</span></span></td>
<td><span data-ttu-id="d044c-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="d044c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="d044c-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d044c-415">Fiscal</span></span></td>
<td><span data-ttu-id="d044c-416">2017</span><span class="sxs-lookup"><span data-stu-id="d044c-416">2017</span></span></td>
<td><span data-ttu-id="d044c-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="d044c-417">Period 1</span></span></td>
<td><span data-ttu-id="d044c-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="d044c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="d044c-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="d044c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-421">Cost object</span></span></th>
<th><span data-ttu-id="d044c-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-424">Proj 1</span></span></td>
<td><span data-ttu-id="d044c-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d044c-426">3,00</span><span class="sxs-lookup"><span data-stu-id="d044c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-428">Proj 2</span></span></td>
<td><span data-ttu-id="d044c-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d044c-430">1,00</span><span class="sxs-lookup"><span data-stu-id="d044c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d044c-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="d044c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-433">Cost element</span></span></th>
<th><span data-ttu-id="d044c-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-435">Amount</span></span></th>
<th><span data-ttu-id="d044c-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="d044c-437">CC0001</span></span></td>
<td><span data-ttu-id="d044c-438">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-438">HR</span></span></td>
<td><span data-ttu-id="d044c-439">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-439">10001</span></span></td>
<td><span data-ttu-id="d044c-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-440">Electricity</span></span></td>
<td><span data-ttu-id="d044c-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-441">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="d044c-442">-30.00</span></span></td>
<td><span data-ttu-id="d044c-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-444">Proj 1</span></span></td>
<td><span data-ttu-id="d044c-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d044c-446">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-446">10001</span></span></td>
<td><span data-ttu-id="d044c-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-447">Electricity</span></span></td>
<td><span data-ttu-id="d044c-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-448">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-449">30,00</span><span class="sxs-lookup"><span data-stu-id="d044c-449">30.00</span></span></td>
<td><span data-ttu-id="d044c-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-451">CC001</span></span></td>
<td><span data-ttu-id="d044c-452">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-452">HR</span></span></td>
<td><span data-ttu-id="d044c-453">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-453">10001</span></span></td>
<td><span data-ttu-id="d044c-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-454">Electricity</span></span></td>
<td><span data-ttu-id="d044c-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-455">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="d044c-456">-10.00</span></span></td>
<td><span data-ttu-id="d044c-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-458">Proj 2</span></span></td>
<td><span data-ttu-id="d044c-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d044c-460">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-460">10001</span></span></td>
<td><span data-ttu-id="d044c-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-461">Electricity</span></span></td>
<td><span data-ttu-id="d044c-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-462">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-463">10.00</span><span class="sxs-lookup"><span data-stu-id="d044c-463">10.00</span></span></td>
<td><span data-ttu-id="d044c-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="d044c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="d044c-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="d044c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="d044c-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="d044c-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="d044c-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="d044c-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="d044c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="d044c-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="d044c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="d044c-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="d044c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="d044c-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="d044c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="d044c-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="d044c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="d044c-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="d044c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="d044c-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="d044c-475">Define the cost allocation</span></span>

<span data-ttu-id="d044c-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="d044c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="d044c-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="d044c-478">Et statistisk dimensionsmedlem med navnet Human Resources-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="d044c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-479">Cost object</span></span></th>
<th><span data-ttu-id="d044c-480">Human Resources-tjenester</span><span class="sxs-lookup"><span data-stu-id="d044c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-481">CC002</span></span></td>
<td><span data-ttu-id="d044c-482">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-482">Finance</span></span></td>
<td><span data-ttu-id="d044c-483">35</span><span class="sxs-lookup"><span data-stu-id="d044c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-484">CC003</span></span></td>
<td><span data-ttu-id="d044c-485">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-485">Assembly</span></span></td>
<td><span data-ttu-id="d044c-486">55</span><span class="sxs-lookup"><span data-stu-id="d044c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-487">CC004</span></span></td>
<td><span data-ttu-id="d044c-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-488">Packaging</span></span></td>
<td><span data-ttu-id="d044c-489">10</span><span class="sxs-lookup"><span data-stu-id="d044c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="d044c-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="d044c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-492">Cost object</span></span></th>
<th><span data-ttu-id="d044c-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="d044c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-494">CC003</span></span></td>
<td><span data-ttu-id="d044c-495">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-495">Assembly</span></span></td>
<td><span data-ttu-id="d044c-496">65</span><span class="sxs-lookup"><span data-stu-id="d044c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-497">CC004</span></span></td>
<td><span data-ttu-id="d044c-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-498">Packaging</span></span></td>
<td><span data-ttu-id="d044c-499">35</span><span class="sxs-lookup"><span data-stu-id="d044c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="d044c-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="d044c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-502">Cost object</span></span></th>
<th><span data-ttu-id="d044c-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="d044c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-504">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-505">Product 1</span></span></td>
<td><span data-ttu-id="d044c-506">60</span><span class="sxs-lookup"><span data-stu-id="d044c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-507">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-508">Product 2</span></span></td>
<td><span data-ttu-id="d044c-509">20</span><span class="sxs-lookup"><span data-stu-id="d044c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="d044c-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="d044c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-512">Cost object</span></span></th>
<th><span data-ttu-id="d044c-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="d044c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-514">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-515">Product 1</span></span></td>
<td><span data-ttu-id="d044c-516">80</span><span class="sxs-lookup"><span data-stu-id="d044c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-517">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-518">Product 2</span></span></td>
<td><span data-ttu-id="d044c-519">15</span><span class="sxs-lookup"><span data-stu-id="d044c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d044c-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="d044c-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="d044c-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="d044c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="d044c-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="d044c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-523">Cost object</span></span></th>
<th><span data-ttu-id="d044c-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-524">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-526">Amount</span></span></th>
<th><span data-ttu-id="d044c-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-528">CC002</span></span></td>
<td><span data-ttu-id="d044c-529">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-529">Finance</span></span></td>
<td><span data-ttu-id="d044c-530">35</span><span class="sxs-lookup"><span data-stu-id="d044c-530">35</span></span></td>
<td><span data-ttu-id="d044c-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d044c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="d044c-532">175.00</span></span></td>
<td><span data-ttu-id="d044c-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-534">CC003</span></span></td>
<td><span data-ttu-id="d044c-535">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-535">Assembly</span></span></td>
<td><span data-ttu-id="d044c-536">55</span><span class="sxs-lookup"><span data-stu-id="d044c-536">55</span></span></td>
<td><span data-ttu-id="d044c-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d044c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="d044c-538">275.00</span></span></td>
<td><span data-ttu-id="d044c-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-540">CC004</span></span></td>
<td><span data-ttu-id="d044c-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-541">Packaging</span></span></td>
<td><span data-ttu-id="d044c-542">10</span><span class="sxs-lookup"><span data-stu-id="d044c-542">10</span></span></td>
<td><span data-ttu-id="d044c-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d044c-544">50,00</span><span class="sxs-lookup"><span data-stu-id="d044c-544">50.00</span></span></td>
<td><span data-ttu-id="d044c-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-546">CC002</span></span></td>
<td><span data-ttu-id="d044c-547">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-547">Finance</span></span></td>
<td><span data-ttu-id="d044c-548">35</span><span class="sxs-lookup"><span data-stu-id="d044c-548">35</span></span></td>
<td><span data-ttu-id="d044c-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="d044c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d044c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="d044c-550">436.00</span></span></td>
<td><span data-ttu-id="d044c-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-552">CC003</span></span></td>
<td><span data-ttu-id="d044c-553">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-553">Assembly</span></span></td>
<td><span data-ttu-id="d044c-554">55</span><span class="sxs-lookup"><span data-stu-id="d044c-554">55</span></span></td>
<td><span data-ttu-id="d044c-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="d044c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d044c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="d044c-556">685.14</span></span></td>
<td><span data-ttu-id="d044c-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-558">CC004</span></span></td>
<td><span data-ttu-id="d044c-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-559">Packaging</span></span></td>
<td><span data-ttu-id="d044c-560">10</span><span class="sxs-lookup"><span data-stu-id="d044c-560">10</span></span></td>
<td><span data-ttu-id="d044c-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="d044c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d044c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="d044c-562">124.57</span></span></td>
<td><span data-ttu-id="d044c-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="d044c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-565">Cost object</span></span></th>
<th><span data-ttu-id="d044c-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-566">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-568">Amount</span></span></th>
<th><span data-ttu-id="d044c-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-570">CC003</span></span></td>
<td><span data-ttu-id="d044c-571">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-571">Assembly</span></span></td>
<td><span data-ttu-id="d044c-572">65</span><span class="sxs-lookup"><span data-stu-id="d044c-572">65</span></span></td>
<td><span data-ttu-id="d044c-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d044c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="d044c-574">438.75</span></span></td>
<td><span data-ttu-id="d044c-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-576">CC004</span></span></td>
<td><span data-ttu-id="d044c-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-577">Packaging</span></span></td>
<td><span data-ttu-id="d044c-578">35</span><span class="sxs-lookup"><span data-stu-id="d044c-578">35</span></span></td>
<td><span data-ttu-id="d044c-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d044c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="d044c-580">236.25</span></span></td>
<td><span data-ttu-id="d044c-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-582">CC003</span></span></td>
<td><span data-ttu-id="d044c-583">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-583">Assembly</span></span></td>
<td><span data-ttu-id="d044c-584">65</span><span class="sxs-lookup"><span data-stu-id="d044c-584">65</span></span></td>
<td><span data-ttu-id="d044c-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d044c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d044c-586">5,297.69</span></span></td>
<td><span data-ttu-id="d044c-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-588">CC004</span></span></td>
<td><span data-ttu-id="d044c-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-589">Packaging</span></span></td>
<td><span data-ttu-id="d044c-590">35</span><span class="sxs-lookup"><span data-stu-id="d044c-590">35</span></span></td>
<td><span data-ttu-id="d044c-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d044c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d044c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d044c-592">2,852.60</span></span></td>
<td><span data-ttu-id="d044c-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="d044c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-595">Cost object</span></span></th>
<th><span data-ttu-id="d044c-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-596">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-598">Amount</span></span></th>
<th><span data-ttu-id="d044c-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-600">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-601">Product 1</span></span></td>
<td><span data-ttu-id="d044c-602">60</span><span class="sxs-lookup"><span data-stu-id="d044c-602">60</span></span></td>
<td><span data-ttu-id="d044c-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d044c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d044c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="d044c-604">535.31</span></span></td>
<td><span data-ttu-id="d044c-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-606">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-607">Product 2</span></span></td>
<td><span data-ttu-id="d044c-608">20</span><span class="sxs-lookup"><span data-stu-id="d044c-608">20</span></span></td>
<td><span data-ttu-id="d044c-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d044c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d044c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="d044c-610">178.44</span></span></td>
<td><span data-ttu-id="d044c-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-612">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-613">Product 1</span></span></td>
<td><span data-ttu-id="d044c-614">60</span><span class="sxs-lookup"><span data-stu-id="d044c-614">60</span></span></td>
<td><span data-ttu-id="d044c-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d044c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d044c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d044c-616">4,487.12</span></span></td>
<td><span data-ttu-id="d044c-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-618">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-619">Product 2</span></span></td>
<td><span data-ttu-id="d044c-620">20</span><span class="sxs-lookup"><span data-stu-id="d044c-620">20</span></span></td>
<td><span data-ttu-id="d044c-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d044c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d044c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d044c-622">1,495.71</span></span></td>
<td><span data-ttu-id="d044c-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d044c-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="d044c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-625">Cost object</span></span></th>
<th><span data-ttu-id="d044c-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="d044c-626">Magnitude</span></span></th>
<th><span data-ttu-id="d044c-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="d044c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="d044c-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-628">Amount</span></span></th>
<th><span data-ttu-id="d044c-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-630">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-631">Product 1</span></span></td>
<td><span data-ttu-id="d044c-632">80</span><span class="sxs-lookup"><span data-stu-id="d044c-632">80</span></span></td>
<td><span data-ttu-id="d044c-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d044c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d044c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="d044c-634">241.05</span></span></td>
<td><span data-ttu-id="d044c-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-636">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-637">Product 2</span></span></td>
<td><span data-ttu-id="d044c-638">15</span><span class="sxs-lookup"><span data-stu-id="d044c-638">15</span></span></td>
<td><span data-ttu-id="d044c-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d044c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d044c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="d044c-640">45.20</span></span></td>
<td><span data-ttu-id="d044c-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-642">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-643">Product 1</span></span></td>
<td><span data-ttu-id="d044c-644">80</span><span class="sxs-lookup"><span data-stu-id="d044c-644">80</span></span></td>
<td><span data-ttu-id="d044c-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d044c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d044c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d044c-646">2,507.09</span></span></td>
<td><span data-ttu-id="d044c-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-648">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-649">Product 2</span></span></td>
<td><span data-ttu-id="d044c-650">15</span><span class="sxs-lookup"><span data-stu-id="d044c-650">15</span></span></td>
<td><span data-ttu-id="d044c-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d044c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d044c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="d044c-652">470.08</span></span></td>
<td><span data-ttu-id="d044c-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d044c-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="d044c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="d044c-655">Journal</span></span></th>
<th><span data-ttu-id="d044c-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="d044c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d044c-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="d044c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d044c-658">Version</span><span class="sxs-lookup"><span data-stu-id="d044c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-659">00004</span><span class="sxs-lookup"><span data-stu-id="d044c-659">00004</span></span></td>
<td><span data-ttu-id="d044c-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="d044c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="d044c-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="d044c-661">Fiscal</span></span></td>
<td><span data-ttu-id="d044c-662">2017</span><span class="sxs-lookup"><span data-stu-id="d044c-662">2017</span></span></td>
<td><span data-ttu-id="d044c-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="d044c-663">Period 1</span></span></td>
<td><span data-ttu-id="d044c-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="d044c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="d044c-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="d044c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d044c-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-668">Cost element</span></span></th>
<th><span data-ttu-id="d044c-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-672">CC001</span></span></td>
<td><span data-ttu-id="d044c-673">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-673">HR</span></span></td>
<td><span data-ttu-id="d044c-674">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-674">10001</span></span></td>
<td><span data-ttu-id="d044c-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-675">Electricity</span></span></td>
<td><span data-ttu-id="d044c-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-677">500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-679">CC001</span></span></td>
<td><span data-ttu-id="d044c-680">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-680">HR</span></span></td>
<td><span data-ttu-id="d044c-681">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-681">10001</span></span></td>
<td><span data-ttu-id="d044c-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-682">Electricity</span></span></td>
<td><span data-ttu-id="d044c-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-683">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="d044c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-686">CC002</span></span></td>
<td><span data-ttu-id="d044c-687">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-687">Finance</span></span></td>
<td><span data-ttu-id="d044c-688">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-688">10001</span></span></td>
<td><span data-ttu-id="d044c-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-689">Electricity</span></span></td>
<td><span data-ttu-id="d044c-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="d044c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-693">CC002</span></span></td>
<td><span data-ttu-id="d044c-694">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-694">Finance</span></span></td>
<td><span data-ttu-id="d044c-695">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-695">10001</span></span></td>
<td><span data-ttu-id="d044c-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-696">Electricity</span></span></td>
<td><span data-ttu-id="d044c-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-697">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="d044c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-700">CC003</span></span></td>
<td><span data-ttu-id="d044c-701">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-701">Assembly</span></span></td>
<td><span data-ttu-id="d044c-702">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-702">10001</span></span></td>
<td><span data-ttu-id="d044c-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-703">Electricity</span></span></td>
<td><span data-ttu-id="d044c-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="d044c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-707">CC003</span></span></td>
<td><span data-ttu-id="d044c-708">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-708">Assembly</span></span></td>
<td><span data-ttu-id="d044c-709">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-709">10001</span></span></td>
<td><span data-ttu-id="d044c-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-710">Electricity</span></span></td>
<td><span data-ttu-id="d044c-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-711">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="d044c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-714">CC003</span></span></td>
<td><span data-ttu-id="d044c-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-715">Packaging</span></span></td>
<td><span data-ttu-id="d044c-716">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-716">10001</span></span></td>
<td><span data-ttu-id="d044c-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-717">Electricity</span></span></td>
<td><span data-ttu-id="d044c-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="d044c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-721">CC003</span></span></td>
<td><span data-ttu-id="d044c-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-722">Packaging</span></span></td>
<td><span data-ttu-id="d044c-723">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-723">10001</span></span></td>
<td><span data-ttu-id="d044c-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-724">Electricity</span></span></td>
<td><span data-ttu-id="d044c-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-725">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="d044c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-728">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-729">Product 1</span></span></td>
<td><span data-ttu-id="d044c-730">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-730">10001</span></span></td>
<td><span data-ttu-id="d044c-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-731">Electricity</span></span></td>
<td><span data-ttu-id="d044c-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="d044c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-735">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-736">Product 1</span></span></td>
<td><span data-ttu-id="d044c-737">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-737">10001</span></span></td>
<td><span data-ttu-id="d044c-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-738">Electricity</span></span></td>
<td><span data-ttu-id="d044c-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-739">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d044c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-742">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-743">Product 1</span></span></td>
<td><span data-ttu-id="d044c-744">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-744">10001</span></span></td>
<td><span data-ttu-id="d044c-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-745">Electricity</span></span></td>
<td><span data-ttu-id="d044c-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="d044c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="d044c-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-749">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-750">Product 1</span></span></td>
<td><span data-ttu-id="d044c-751">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-751">10001</span></span></td>
<td><span data-ttu-id="d044c-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-752">Electricity</span></span></td>
<td><span data-ttu-id="d044c-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-753">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d044c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d044c-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="d044c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d044c-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d044c-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-757">Cost element</span></span></th>
<th><span data-ttu-id="d044c-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="d044c-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="d044c-759">Amount</span></span></th>
<th><span data-ttu-id="d044c-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="d044c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d044c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-761">CC001</span></span></td>
<td><span data-ttu-id="d044c-762">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-762">HR</span></span></td>
<td><span data-ttu-id="d044c-763">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-763">10001</span></span></td>
<td><span data-ttu-id="d044c-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-764">Electricity</span></span></td>
<td><span data-ttu-id="d044c-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="d044c-766">-500.00</span></span></td>
<td><span data-ttu-id="d044c-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-768">CC002</span></span></td>
<td><span data-ttu-id="d044c-769">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-769">Finance</span></span></td>
<td><span data-ttu-id="d044c-770">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-770">10001</span></span></td>
<td><span data-ttu-id="d044c-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-771">Electricity</span></span></td>
<td><span data-ttu-id="d044c-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="d044c-773">175.00</span></span></td>
<td><span data-ttu-id="d044c-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-775">CC003</span></span></td>
<td><span data-ttu-id="d044c-776">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-776">Assembly</span></span></td>
<td><span data-ttu-id="d044c-777">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-777">10001</span></span></td>
<td><span data-ttu-id="d044c-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-778">Electricity</span></span></td>
<td><span data-ttu-id="d044c-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="d044c-780">275.00</span></span></td>
<td><span data-ttu-id="d044c-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-782">CC004</span></span></td>
<td><span data-ttu-id="d044c-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-783">Packaging</span></span></td>
<td><span data-ttu-id="d044c-784">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-784">10001</span></span></td>
<td><span data-ttu-id="d044c-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-785">Electricity</span></span></td>
<td><span data-ttu-id="d044c-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="d044c-787">50,00</span></span></td>
<td><span data-ttu-id="d044c-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-789">CC001</span></span></td>
<td><span data-ttu-id="d044c-790">Human Resources</span><span class="sxs-lookup"><span data-stu-id="d044c-790">HR</span></span></td>
<td><span data-ttu-id="d044c-791">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-791">10001</span></span></td>
<td><span data-ttu-id="d044c-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-792">Electricity</span></span></td>
<td><span data-ttu-id="d044c-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-793">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="d044c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="d044c-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-796">CC002</span></span></td>
<td><span data-ttu-id="d044c-797">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-797">Finance</span></span></td>
<td><span data-ttu-id="d044c-798">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-798">10001</span></span></td>
<td><span data-ttu-id="d044c-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-799">Electricity</span></span></td>
<td><span data-ttu-id="d044c-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-800">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="d044c-801">436.00</span></span></td>
<td><span data-ttu-id="d044c-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-803">CC003</span></span></td>
<td><span data-ttu-id="d044c-804">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-804">Assembly</span></span></td>
<td><span data-ttu-id="d044c-805">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-805">10001</span></span></td>
<td><span data-ttu-id="d044c-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-806">Electricity</span></span></td>
<td><span data-ttu-id="d044c-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-807">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="d044c-808">685.14</span></span></td>
<td><span data-ttu-id="d044c-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-810">CC004</span></span></td>
<td><span data-ttu-id="d044c-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-811">Packaging</span></span></td>
<td><span data-ttu-id="d044c-812">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-812">10001</span></span></td>
<td><span data-ttu-id="d044c-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-813">Electricity</span></span></td>
<td><span data-ttu-id="d044c-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-814">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="d044c-815">124.57</span></span></td>
<td><span data-ttu-id="d044c-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-817">CC002</span></span></td>
<td><span data-ttu-id="d044c-818">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-818">Finance</span></span></td>
<td><span data-ttu-id="d044c-819">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-819">10001</span></span></td>
<td><span data-ttu-id="d044c-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-820">Electricity</span></span></td>
<td><span data-ttu-id="d044c-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="d044c-822">-675.00</span></span></td>
<td><span data-ttu-id="d044c-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-824">CC003</span></span></td>
<td><span data-ttu-id="d044c-825">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-825">Assembly</span></span></td>
<td><span data-ttu-id="d044c-826">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-826">10001</span></span></td>
<td><span data-ttu-id="d044c-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-827">Electricity</span></span></td>
<td><span data-ttu-id="d044c-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="d044c-829">438.75</span></span></td>
<td><span data-ttu-id="d044c-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-831">CC004</span></span></td>
<td><span data-ttu-id="d044c-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-832">Packaging</span></span></td>
<td><span data-ttu-id="d044c-833">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-833">10001</span></span></td>
<td><span data-ttu-id="d044c-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-834">Electricity</span></span></td>
<td><span data-ttu-id="d044c-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="d044c-836">236.25</span></span></td>
<td><span data-ttu-id="d044c-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-838">CC002</span></span></td>
<td><span data-ttu-id="d044c-839">Finans</span><span class="sxs-lookup"><span data-stu-id="d044c-839">Finance</span></span></td>
<td><span data-ttu-id="d044c-840">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-840">10001</span></span></td>
<td><span data-ttu-id="d044c-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-841">Electricity</span></span></td>
<td><span data-ttu-id="d044c-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-842">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="d044c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="d044c-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-845">CC003</span></span></td>
<td><span data-ttu-id="d044c-846">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-846">Assembly</span></span></td>
<td><span data-ttu-id="d044c-847">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-847">10001</span></span></td>
<td><span data-ttu-id="d044c-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-848">Electricity</span></span></td>
<td><span data-ttu-id="d044c-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-849">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d044c-850">5,297.69</span></span></td>
<td><span data-ttu-id="d044c-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-852">CC004</span></span></td>
<td><span data-ttu-id="d044c-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="d044c-853">Packaging</span></span></td>
<td><span data-ttu-id="d044c-854">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-854">10001</span></span></td>
<td><span data-ttu-id="d044c-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-855">Electricity</span></span></td>
<td><span data-ttu-id="d044c-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-856">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d044c-857">2,852.60</span></span></td>
<td><span data-ttu-id="d044c-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-859">CC003</span></span></td>
<td><span data-ttu-id="d044c-860">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-860">Assembly</span></span></td>
<td><span data-ttu-id="d044c-861">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-861">10001</span></span></td>
<td><span data-ttu-id="d044c-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-862">Electricity</span></span></td>
<td><span data-ttu-id="d044c-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="d044c-864">-713.75</span></span></td>
<td><span data-ttu-id="d044c-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-866">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-867">Product 1</span></span></td>
<td><span data-ttu-id="d044c-868">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-868">10001</span></span></td>
<td><span data-ttu-id="d044c-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-869">Electricity</span></span></td>
<td><span data-ttu-id="d044c-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="d044c-871">535.31</span></span></td>
<td><span data-ttu-id="d044c-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-873">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-874">Product 2</span></span></td>
<td><span data-ttu-id="d044c-875">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-875">10001</span></span></td>
<td><span data-ttu-id="d044c-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-876">Electricity</span></span></td>
<td><span data-ttu-id="d044c-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="d044c-878">178.44</span></span></td>
<td><span data-ttu-id="d044c-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-880">CC003</span></span></td>
<td><span data-ttu-id="d044c-881">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-881">Assembly</span></span></td>
<td><span data-ttu-id="d044c-882">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-882">10001</span></span></td>
<td><span data-ttu-id="d044c-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-883">Electricity</span></span></td>
<td><span data-ttu-id="d044c-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-884">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="d044c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="d044c-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-887">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-888">Product 1</span></span></td>
<td><span data-ttu-id="d044c-889">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-889">10001</span></span></td>
<td><span data-ttu-id="d044c-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-890">Electricity</span></span></td>
<td><span data-ttu-id="d044c-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-891">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d044c-892">4,487.12</span></span></td>
<td><span data-ttu-id="d044c-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-894">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-895">Product 2</span></span></td>
<td><span data-ttu-id="d044c-896">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-896">10001</span></span></td>
<td><span data-ttu-id="d044c-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-897">Electricity</span></span></td>
<td><span data-ttu-id="d044c-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-898">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d044c-899">1,495.71</span></span></td>
<td><span data-ttu-id="d044c-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-901">CC003</span></span></td>
<td><span data-ttu-id="d044c-902">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-902">Assembly</span></span></td>
<td><span data-ttu-id="d044c-903">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-903">10001</span></span></td>
<td><span data-ttu-id="d044c-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-904">Electricity</span></span></td>
<td><span data-ttu-id="d044c-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="d044c-906">-286.25</span></span></td>
<td><span data-ttu-id="d044c-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-908">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-909">Product 1</span></span></td>
<td><span data-ttu-id="d044c-910">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-910">10001</span></span></td>
<td><span data-ttu-id="d044c-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-911">Electricity</span></span></td>
<td><span data-ttu-id="d044c-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="d044c-913">241.05</span></span></td>
<td><span data-ttu-id="d044c-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-915">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-916">Product 2</span></span></td>
<td><span data-ttu-id="d044c-917">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-917">10001</span></span></td>
<td><span data-ttu-id="d044c-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-918">Electricity</span></span></td>
<td><span data-ttu-id="d044c-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="d044c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="d044c-920">45.20</span></span></td>
<td><span data-ttu-id="d044c-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-922">CC003</span></span></td>
<td><span data-ttu-id="d044c-923">Samling</span><span class="sxs-lookup"><span data-stu-id="d044c-923">Assembly</span></span></td>
<td><span data-ttu-id="d044c-924">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-924">10001</span></span></td>
<td><span data-ttu-id="d044c-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-925">Electricity</span></span></td>
<td><span data-ttu-id="d044c-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-926">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="d044c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="d044c-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-929">Prod 1</span></span></td>
<td><span data-ttu-id="d044c-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="d044c-930">Product 1</span></span></td>
<td><span data-ttu-id="d044c-931">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-931">10001</span></span></td>
<td><span data-ttu-id="d044c-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-932">Electricity</span></span></td>
<td><span data-ttu-id="d044c-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-933">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d044c-934">2,507.09</span></span></td>
<td><span data-ttu-id="d044c-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d044c-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-936">Prod 2</span></span></td>
<td><span data-ttu-id="d044c-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="d044c-937">Product 2</span></span></td>
<td><span data-ttu-id="d044c-938">10001</span><span class="sxs-lookup"><span data-stu-id="d044c-938">10001</span></span></td>
<td><span data-ttu-id="d044c-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-939">Electricity</span></span></td>
<td><span data-ttu-id="d044c-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-940">Variable cost</span></span></td>
<td><span data-ttu-id="d044c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="d044c-941">470.08</span></span></td>
<td><span data-ttu-id="d044c-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="d044c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="d044c-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="d044c-943">Conclusion</span></span>
<span data-ttu-id="d044c-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="d044c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="d044c-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="d044c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="d044c-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="d044c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="d044c-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="d044c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="d044c-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="d044c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="d044c-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="d044c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="d044c-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="d044c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d044c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="d044c-951">CC099</span></span></th>
<th><span data-ttu-id="d044c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="d044c-952">CC001</span></span></th>
<th><span data-ttu-id="d044c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="d044c-953">CC002</span></span></th>
<th><span data-ttu-id="d044c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="d044c-954">CC003</span></span></th>
<th><span data-ttu-id="d044c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="d044c-955">CC004</span></span></th>
<th><span data-ttu-id="d044c-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="d044c-956">Proj 1</span></span></th>
<th><span data-ttu-id="d044c-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="d044c-957">Proj 2</span></span></th>
<th><span data-ttu-id="d044c-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="d044c-958">Prod 1</span></span></th>
<th><span data-ttu-id="d044c-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="d044c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="d044c-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="d044c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d044c-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="d044c-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="d044c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-971">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="d044c-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-973">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-975">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d044c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="d044c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="d044c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="d044c-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="d044c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-982">000</span><span class="sxs-lookup"><span data-stu-id="d044c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-983">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-984">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-985">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="d044c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-987">30,00</span><span class="sxs-lookup"><span data-stu-id="d044c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-988">10,00</span><span class="sxs-lookup"><span data-stu-id="d044c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d044c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d044c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d044c-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="d044c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d044c-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="d044c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="d044c-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="d044c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="d044c-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="d044c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="d044c-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="d044c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="d044c-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="d044c-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



