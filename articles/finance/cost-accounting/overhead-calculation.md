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
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208841"
---
# <a name="overhead-calculation"></a><span data-ttu-id="9f504-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f504-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9f504-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="9f504-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="9f504-105">Term definition</span></span>
---------------

<span data-ttu-id="9f504-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="9f504-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="9f504-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="9f504-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="9f504-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="9f504-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="9f504-109">Leje</span><span class="sxs-lookup"><span data-stu-id="9f504-109">Rent</span></span>
-   <span data-ttu-id="9f504-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-110">Electricity</span></span>
-   <span data-ttu-id="9f504-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="9f504-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="9f504-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-112">Overhead calculation overview</span></span>
<span data-ttu-id="9f504-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="9f504-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="9f504-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="9f504-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="9f504-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="9f504-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="9f504-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="9f504-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="9f504-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="9f504-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="9f504-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="9f504-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="9f504-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="9f504-119">Version type</span></span>
-   <span data-ttu-id="9f504-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="9f504-120">Date and time</span></span>
-   <span data-ttu-id="9f504-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="9f504-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="9f504-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="9f504-122">Fiscal year</span></span>
-   <span data-ttu-id="9f504-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="9f504-123">Fiscal period</span></span>

<span data-ttu-id="9f504-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="9f504-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="9f504-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="9f504-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="9f504-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="9f504-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="9f504-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="9f504-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="9f504-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="9f504-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="9f504-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="9f504-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="9f504-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="9f504-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="9f504-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="9f504-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="9f504-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="9f504-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="9f504-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="9f504-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="9f504-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="9f504-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="9f504-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="9f504-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="9f504-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="9f504-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9f504-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="9f504-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="9f504-140">Main account</span></span></th>
<th><span data-ttu-id="9f504-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="9f504-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="9f504-143">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-143">CC099</span></span></td>
<td><span data-ttu-id="9f504-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-144">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-145">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-145">10001</span></span></td>
<td><span data-ttu-id="9f504-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-146">Electricity</span></span></td>
<td><span data-ttu-id="9f504-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="9f504-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="9f504-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="9f504-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="9f504-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="9f504-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="9f504-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="9f504-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="9f504-151">Define the cost behavior rule</span></span>

<span data-ttu-id="9f504-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="9f504-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="9f504-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="9f504-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="9f504-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="9f504-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="9f504-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="9f504-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="9f504-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="9f504-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="9f504-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="9f504-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="9f504-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="9f504-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-160">Journal</span></span></th>
<th><span data-ttu-id="9f504-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="9f504-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9f504-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="9f504-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9f504-163">Version</span><span class="sxs-lookup"><span data-stu-id="9f504-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-164">00001</span><span class="sxs-lookup"><span data-stu-id="9f504-164">00001</span></span></td>
<td><span data-ttu-id="9f504-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="9f504-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="9f504-166">Fiscal</span></span></td>
<td><span data-ttu-id="9f504-167">2017</span><span class="sxs-lookup"><span data-stu-id="9f504-167">2017</span></span></td>
<td><span data-ttu-id="9f504-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="9f504-168">Period 1</span></span></td>
<td><span data-ttu-id="9f504-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="9f504-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9f504-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="9f504-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-173">Cost element</span></span></th>
<th><span data-ttu-id="9f504-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-174">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="9f504-177">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-177">CC099</span></span></td>
<td><span data-ttu-id="9f504-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-178">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-179">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-179">10001</span></span></td>
<td><span data-ttu-id="9f504-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-180">Electricity</span></span></td>
<td><span data-ttu-id="9f504-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="9f504-181">Unclassified</span></span></td>
<td><span data-ttu-id="9f504-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9f504-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="9f504-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-185">Cost element</span></span></th>
<th><span data-ttu-id="9f504-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-186">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-187">Amount</span></span></th>
<th><span data-ttu-id="9f504-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-189">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-189">CC099</span></span></td>
<td><span data-ttu-id="9f504-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-190">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-191">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-191">10001</span></span></td>
<td><span data-ttu-id="9f504-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-192">Electricity</span></span></td>
<td><span data-ttu-id="9f504-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="9f504-193">Unclassified</span></span></td>
<td><span data-ttu-id="9f504-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-194">10,000.00</span></span></td>
<td><span data-ttu-id="9f504-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-196">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-196">CC099</span></span></td>
<td><span data-ttu-id="9f504-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-197">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-198">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-198">10001</span></span></td>
<td><span data-ttu-id="9f504-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-199">Electricity</span></span></td>
<td><span data-ttu-id="9f504-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="9f504-200">Unclassified</span></span></td>
<td><span data-ttu-id="9f504-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-201">-10,000.00</span></span></td>
<td><span data-ttu-id="9f504-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-203">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-203">CC099</span></span></td>
<td><span data-ttu-id="9f504-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-204">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-205">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-205">10001</span></span></td>
<td><span data-ttu-id="9f504-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-206">Electricity</span></span></td>
<td><span data-ttu-id="9f504-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-207">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-208">1,000.00</span></span></td>
<td><span data-ttu-id="9f504-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-210">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-210">CC099</span></span></td>
<td><span data-ttu-id="9f504-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-211">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-212">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-212">10001</span></span></td>
<td><span data-ttu-id="9f504-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-213">Electricity</span></span></td>
<td><span data-ttu-id="9f504-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-214">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-215">9,000.00</span></span></td>
<td><span data-ttu-id="9f504-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="9f504-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="9f504-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="9f504-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="9f504-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="9f504-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="9f504-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="9f504-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="9f504-221">Define the cost distribution rule</span></span>

<span data-ttu-id="9f504-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="9f504-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="9f504-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="9f504-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="9f504-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="9f504-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="9f504-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="9f504-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="9f504-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="9f504-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-228">Cost object</span></span></th>
<th><span data-ttu-id="9f504-229">KWh</span><span class="sxs-lookup"><span data-stu-id="9f504-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-230">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-230">CC001</span></span></td>
<td><span data-ttu-id="9f504-231">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-231">HR</span></span></td>
<td><span data-ttu-id="9f504-232">1.000</span><span class="sxs-lookup"><span data-stu-id="9f504-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-233">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-233">CC002</span></span></td>
<td><span data-ttu-id="9f504-234">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-234">Finance</span></span></td>
<td><span data-ttu-id="9f504-235">6.000</span><span class="sxs-lookup"><span data-stu-id="9f504-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-236">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-236">CC003</span></span></td>
<td><span data-ttu-id="9f504-237">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-237">Assembly</span></span></td>
<td><span data-ttu-id="9f504-238">0</span><span class="sxs-lookup"><span data-stu-id="9f504-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9f504-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-240">Cost object</span></span></th>
<th><span data-ttu-id="9f504-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-241">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-242">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-244">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-244">CC001</span></span></td>
<td><span data-ttu-id="9f504-245">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-245">HR</span></span></td>
<td><span data-ttu-id="9f504-246">1.000</span><span class="sxs-lookup"><span data-stu-id="9f504-246">1,000</span></span></td>
<td><span data-ttu-id="9f504-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9f504-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9f504-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-249">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-249">CC002</span></span></td>
<td><span data-ttu-id="9f504-250">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-250">Finance</span></span></td>
<td><span data-ttu-id="9f504-251">6.000</span><span class="sxs-lookup"><span data-stu-id="9f504-251">6,000</span></span></td>
<td><span data-ttu-id="9f504-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9f504-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9f504-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-254">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-254">CC003</span></span></td>
<td><span data-ttu-id="9f504-255">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-255">Assembly</span></span></td>
<td><span data-ttu-id="9f504-256">0</span><span class="sxs-lookup"><span data-stu-id="9f504-256">0</span></span></td>
<td><span data-ttu-id="9f504-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9f504-258">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="9f504-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="9f504-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9f504-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-261">Cost object</span></span></th>
<th><span data-ttu-id="9f504-262">Formel</span><span class="sxs-lookup"><span data-stu-id="9f504-262">Formula</span></span></th>
<th><span data-ttu-id="9f504-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-263">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-264">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-266">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-266">CC001</span></span></td>
<td><span data-ttu-id="9f504-267">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-267">HR</span></span></td>
<td><span data-ttu-id="9f504-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9f504-269">1</span><span class="sxs-lookup"><span data-stu-id="9f504-269">1</span></span></td>
<td><span data-ttu-id="9f504-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9f504-271">500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-272">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-272">CC002</span></span></td>
<td><span data-ttu-id="9f504-273">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-273">Finance</span></span></td>
<td><span data-ttu-id="9f504-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9f504-275">1</span><span class="sxs-lookup"><span data-stu-id="9f504-275">1</span></span></td>
<td><span data-ttu-id="9f504-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9f504-277">500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-278">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-278">CC003</span></span></td>
<td><span data-ttu-id="9f504-279">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-279">Assembly</span></span></td>
<td><span data-ttu-id="9f504-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9f504-281">0</span><span class="sxs-lookup"><span data-stu-id="9f504-281">0</span></span></td>
<td><span data-ttu-id="9f504-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9f504-283">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9f504-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-285">Journal</span></span></th>
<th><span data-ttu-id="9f504-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="9f504-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9f504-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="9f504-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9f504-288">Version</span><span class="sxs-lookup"><span data-stu-id="9f504-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-289">00002</span><span class="sxs-lookup"><span data-stu-id="9f504-289">00002</span></span></td>
<td><span data-ttu-id="9f504-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="9f504-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="9f504-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="9f504-291">Fiscal</span></span></td>
<td><span data-ttu-id="9f504-292">2017</span><span class="sxs-lookup"><span data-stu-id="9f504-292">2017</span></span></td>
<td><span data-ttu-id="9f504-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="9f504-293">Period 1</span></span></td>
<td><span data-ttu-id="9f504-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="9f504-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9f504-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="9f504-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-298">Cost element</span></span></th>
<th><span data-ttu-id="9f504-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-299">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-302">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-302">CC099</span></span></td>
<td><span data-ttu-id="9f504-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-303">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-304">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-304">10001</span></span></td>
<td><span data-ttu-id="9f504-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-305">Electricity</span></span></td>
<td><span data-ttu-id="9f504-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-306">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-309">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-309">CC099</span></span></td>
<td><span data-ttu-id="9f504-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-310">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-311">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-311">10001</span></span></td>
<td><span data-ttu-id="9f504-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-312">Electricity</span></span></td>
<td><span data-ttu-id="9f504-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-313">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9f504-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="9f504-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-317">Cost element</span></span></th>
<th><span data-ttu-id="9f504-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-318">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-319">Amount</span></span></th>
<th><span data-ttu-id="9f504-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-321">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-321">CC099</span></span></td>
<td><span data-ttu-id="9f504-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-322">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-323">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-323">10001</span></span></td>
<td><span data-ttu-id="9f504-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-324">Electricity</span></span></td>
<td><span data-ttu-id="9f504-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-325">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-326">-1,000.00</span></span></td>
<td><span data-ttu-id="9f504-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-328">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-328">CC001</span></span></td>
<td><span data-ttu-id="9f504-329">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-329">HR</span></span></td>
<td><span data-ttu-id="9f504-330">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-330">10001</span></span></td>
<td><span data-ttu-id="9f504-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-331">Electricity</span></span></td>
<td><span data-ttu-id="9f504-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-332">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-333">500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-333">500.00</span></span></td>
<td><span data-ttu-id="9f504-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-335">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-335">CC002</span></span></td>
<td><span data-ttu-id="9f504-336">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-336">Finance</span></span></td>
<td><span data-ttu-id="9f504-337">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-337">10001</span></span></td>
<td><span data-ttu-id="9f504-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-338">Electricity</span></span></td>
<td><span data-ttu-id="9f504-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-339">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-340">500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-340">500.00</span></span></td>
<td><span data-ttu-id="9f504-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-342">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-342">CC099</span></span></td>
<td><span data-ttu-id="9f504-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="9f504-343">Default cost center</span></span></td>
<td><span data-ttu-id="9f504-344">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-344">10001</span></span></td>
<td><span data-ttu-id="9f504-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-345">Electricity</span></span></td>
<td><span data-ttu-id="9f504-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-346">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="9f504-347">-9,000.00</span></span></td>
<td><span data-ttu-id="9f504-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-349">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-349">CC001</span></span></td>
<td><span data-ttu-id="9f504-350">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-350">HR</span></span></td>
<td><span data-ttu-id="9f504-351">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-351">10001</span></span></td>
<td><span data-ttu-id="9f504-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-352">Electricity</span></span></td>
<td><span data-ttu-id="9f504-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-353">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9f504-354">1,285.71</span></span></td>
<td><span data-ttu-id="9f504-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-356">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-356">CC002</span></span></td>
<td><span data-ttu-id="9f504-357">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-357">Finance</span></span></td>
<td><span data-ttu-id="9f504-358">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-358">10001</span></span></td>
<td><span data-ttu-id="9f504-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-359">Electricity</span></span></td>
<td><span data-ttu-id="9f504-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-360">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9f504-361">7,714.29</span></span></td>
<td><span data-ttu-id="9f504-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="9f504-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="9f504-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="9f504-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="9f504-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="9f504-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="9f504-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="9f504-367">Define the overhead rate</span></span>

<span data-ttu-id="9f504-368">Omkostningsobjektet CC001 Human Resources bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="9f504-369">Et statistisk dimensionsmedlem med navnet Human Resourcesprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="9f504-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-370">Cost object</span></span></th>
<th><span data-ttu-id="9f504-371">Timer</span><span class="sxs-lookup"><span data-stu-id="9f504-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-372">Proj 1</span></span></td>
<td><span data-ttu-id="9f504-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-373">Project 1</span></span></td>
<td><span data-ttu-id="9f504-374">3</span><span class="sxs-lookup"><span data-stu-id="9f504-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-375">Proj 2</span></span></td>
<td><span data-ttu-id="9f504-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-376">Project 2</span></span></td>
<td><span data-ttu-id="9f504-377">1</span><span class="sxs-lookup"><span data-stu-id="9f504-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="9f504-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-379">Cost object</span></span></th>
<th><span data-ttu-id="9f504-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-380">Cost element</span></span></th>
<th><span data-ttu-id="9f504-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-381">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="9f504-382">Units</span></span></th>
<th><span data-ttu-id="9f504-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="9f504-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-384">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-384">CC001</span></span></td>
<td><span data-ttu-id="9f504-385">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-385">HR</span></span></td>
<td><span data-ttu-id="9f504-386">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-386">10001</span></span></td>
<td><span data-ttu-id="9f504-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-387">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-388">1</span><span class="sxs-lookup"><span data-stu-id="9f504-388">1</span></span></td>
<td><span data-ttu-id="9f504-389">10</span><span class="sxs-lookup"><span data-stu-id="9f504-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-391">Cost object</span></span></th>
<th><span data-ttu-id="9f504-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-392">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-393">Cost element</span></span></th>
<th><span data-ttu-id="9f504-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-394">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-396">Proj 1</span></span></td>
<td><span data-ttu-id="9f504-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-397">Project 1</span></span></td>
<td><span data-ttu-id="9f504-398">3</span><span class="sxs-lookup"><span data-stu-id="9f504-398">3</span></span></td>
<td><span data-ttu-id="9f504-399">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-399">10001</span></span></td>
<td><span data-ttu-id="9f504-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9f504-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9f504-401">30,00</span><span class="sxs-lookup"><span data-stu-id="9f504-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-402">Proj 2</span></span></td>
<td><span data-ttu-id="9f504-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-403">Project 2</span></span></td>
<td><span data-ttu-id="9f504-404">1</span><span class="sxs-lookup"><span data-stu-id="9f504-404">1</span></span></td>
<td><span data-ttu-id="9f504-405">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-405">10001</span></span></td>
<td><span data-ttu-id="9f504-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9f504-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9f504-407">10,00</span><span class="sxs-lookup"><span data-stu-id="9f504-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9f504-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-409">Journal</span></span></th>
<th><span data-ttu-id="9f504-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="9f504-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9f504-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="9f504-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9f504-412">Version</span><span class="sxs-lookup"><span data-stu-id="9f504-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-413">00003</span><span class="sxs-lookup"><span data-stu-id="9f504-413">00003</span></span></td>
<td><span data-ttu-id="9f504-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="9f504-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="9f504-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="9f504-415">Fiscal</span></span></td>
<td><span data-ttu-id="9f504-416">2017</span><span class="sxs-lookup"><span data-stu-id="9f504-416">2017</span></span></td>
<td><span data-ttu-id="9f504-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="9f504-417">Period 1</span></span></td>
<td><span data-ttu-id="9f504-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="9f504-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="9f504-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="9f504-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-421">Cost object</span></span></th>
<th><span data-ttu-id="9f504-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-424">Proj 1</span></span></td>
<td><span data-ttu-id="9f504-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9f504-426">3,00</span><span class="sxs-lookup"><span data-stu-id="9f504-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-428">Proj 2</span></span></td>
<td><span data-ttu-id="9f504-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9f504-430">1,00</span><span class="sxs-lookup"><span data-stu-id="9f504-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9f504-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="9f504-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-433">Cost element</span></span></th>
<th><span data-ttu-id="9f504-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-434">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-435">Amount</span></span></th>
<th><span data-ttu-id="9f504-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="9f504-437">CC0001</span></span></td>
<td><span data-ttu-id="9f504-438">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-438">HR</span></span></td>
<td><span data-ttu-id="9f504-439">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-439">10001</span></span></td>
<td><span data-ttu-id="9f504-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-440">Electricity</span></span></td>
<td><span data-ttu-id="9f504-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-441">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="9f504-442">-30.00</span></span></td>
<td><span data-ttu-id="9f504-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-444">Proj 1</span></span></td>
<td><span data-ttu-id="9f504-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9f504-446">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-446">10001</span></span></td>
<td><span data-ttu-id="9f504-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-447">Electricity</span></span></td>
<td><span data-ttu-id="9f504-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-448">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-449">30,00</span><span class="sxs-lookup"><span data-stu-id="9f504-449">30.00</span></span></td>
<td><span data-ttu-id="9f504-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-451">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-451">CC001</span></span></td>
<td><span data-ttu-id="9f504-452">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-452">HR</span></span></td>
<td><span data-ttu-id="9f504-453">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-453">10001</span></span></td>
<td><span data-ttu-id="9f504-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-454">Electricity</span></span></td>
<td><span data-ttu-id="9f504-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-455">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="9f504-456">-10.00</span></span></td>
<td><span data-ttu-id="9f504-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-458">Proj 2</span></span></td>
<td><span data-ttu-id="9f504-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9f504-460">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-460">10001</span></span></td>
<td><span data-ttu-id="9f504-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-461">Electricity</span></span></td>
<td><span data-ttu-id="9f504-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-462">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-463">10.00</span><span class="sxs-lookup"><span data-stu-id="9f504-463">10.00</span></span></td>
<td><span data-ttu-id="9f504-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="9f504-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="9f504-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="9f504-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="9f504-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="9f504-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="9f504-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="9f504-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="9f504-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="9f504-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="9f504-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="9f504-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="9f504-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="9f504-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="9f504-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="9f504-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="9f504-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="9f504-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="9f504-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="9f504-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="9f504-475">Define the cost allocation</span></span>

<span data-ttu-id="9f504-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9f504-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="9f504-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="9f504-478">Et statistisk dimensionsmedlem med navnet Human Resources-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="9f504-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-479">Cost object</span></span></th>
<th><span data-ttu-id="9f504-480">Human Resources-tjenester</span><span class="sxs-lookup"><span data-stu-id="9f504-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-481">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-481">CC002</span></span></td>
<td><span data-ttu-id="9f504-482">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-482">Finance</span></span></td>
<td><span data-ttu-id="9f504-483">35</span><span class="sxs-lookup"><span data-stu-id="9f504-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-484">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-484">CC003</span></span></td>
<td><span data-ttu-id="9f504-485">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-485">Assembly</span></span></td>
<td><span data-ttu-id="9f504-486">55</span><span class="sxs-lookup"><span data-stu-id="9f504-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-487">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-487">CC004</span></span></td>
<td><span data-ttu-id="9f504-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-488">Packaging</span></span></td>
<td><span data-ttu-id="9f504-489">10</span><span class="sxs-lookup"><span data-stu-id="9f504-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="9f504-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="9f504-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-492">Cost object</span></span></th>
<th><span data-ttu-id="9f504-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="9f504-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-494">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-494">CC003</span></span></td>
<td><span data-ttu-id="9f504-495">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-495">Assembly</span></span></td>
<td><span data-ttu-id="9f504-496">65</span><span class="sxs-lookup"><span data-stu-id="9f504-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-497">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-497">CC004</span></span></td>
<td><span data-ttu-id="9f504-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-498">Packaging</span></span></td>
<td><span data-ttu-id="9f504-499">35</span><span class="sxs-lookup"><span data-stu-id="9f504-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="9f504-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="9f504-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-502">Cost object</span></span></th>
<th><span data-ttu-id="9f504-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="9f504-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-504">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-505">Product 1</span></span></td>
<td><span data-ttu-id="9f504-506">60</span><span class="sxs-lookup"><span data-stu-id="9f504-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-507">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-508">Product 2</span></span></td>
<td><span data-ttu-id="9f504-509">20</span><span class="sxs-lookup"><span data-stu-id="9f504-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="9f504-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="9f504-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-512">Cost object</span></span></th>
<th><span data-ttu-id="9f504-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="9f504-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-514">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-515">Product 1</span></span></td>
<td><span data-ttu-id="9f504-516">80</span><span class="sxs-lookup"><span data-stu-id="9f504-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-517">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-518">Product 2</span></span></td>
<td><span data-ttu-id="9f504-519">15</span><span class="sxs-lookup"><span data-stu-id="9f504-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9f504-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="9f504-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="9f504-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="9f504-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="9f504-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="9f504-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-523">Cost object</span></span></th>
<th><span data-ttu-id="9f504-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-524">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-525">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-526">Amount</span></span></th>
<th><span data-ttu-id="9f504-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-528">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-528">CC002</span></span></td>
<td><span data-ttu-id="9f504-529">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-529">Finance</span></span></td>
<td><span data-ttu-id="9f504-530">35</span><span class="sxs-lookup"><span data-stu-id="9f504-530">35</span></span></td>
<td><span data-ttu-id="9f504-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9f504-532">175.00</span><span class="sxs-lookup"><span data-stu-id="9f504-532">175.00</span></span></td>
<td><span data-ttu-id="9f504-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-534">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-534">CC003</span></span></td>
<td><span data-ttu-id="9f504-535">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-535">Assembly</span></span></td>
<td><span data-ttu-id="9f504-536">55</span><span class="sxs-lookup"><span data-stu-id="9f504-536">55</span></span></td>
<td><span data-ttu-id="9f504-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9f504-538">275.00</span><span class="sxs-lookup"><span data-stu-id="9f504-538">275.00</span></span></td>
<td><span data-ttu-id="9f504-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-540">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-540">CC004</span></span></td>
<td><span data-ttu-id="9f504-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-541">Packaging</span></span></td>
<td><span data-ttu-id="9f504-542">10</span><span class="sxs-lookup"><span data-stu-id="9f504-542">10</span></span></td>
<td><span data-ttu-id="9f504-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9f504-544">50,00</span><span class="sxs-lookup"><span data-stu-id="9f504-544">50.00</span></span></td>
<td><span data-ttu-id="9f504-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-546">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-546">CC002</span></span></td>
<td><span data-ttu-id="9f504-547">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-547">Finance</span></span></td>
<td><span data-ttu-id="9f504-548">35</span><span class="sxs-lookup"><span data-stu-id="9f504-548">35</span></span></td>
<td><span data-ttu-id="9f504-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9f504-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9f504-550">436.00</span><span class="sxs-lookup"><span data-stu-id="9f504-550">436.00</span></span></td>
<td><span data-ttu-id="9f504-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-552">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-552">CC003</span></span></td>
<td><span data-ttu-id="9f504-553">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-553">Assembly</span></span></td>
<td><span data-ttu-id="9f504-554">55</span><span class="sxs-lookup"><span data-stu-id="9f504-554">55</span></span></td>
<td><span data-ttu-id="9f504-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9f504-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9f504-556">685.14</span><span class="sxs-lookup"><span data-stu-id="9f504-556">685.14</span></span></td>
<td><span data-ttu-id="9f504-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-558">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-558">CC004</span></span></td>
<td><span data-ttu-id="9f504-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-559">Packaging</span></span></td>
<td><span data-ttu-id="9f504-560">10</span><span class="sxs-lookup"><span data-stu-id="9f504-560">10</span></span></td>
<td><span data-ttu-id="9f504-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9f504-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9f504-562">124.57</span><span class="sxs-lookup"><span data-stu-id="9f504-562">124.57</span></span></td>
<td><span data-ttu-id="9f504-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="9f504-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-565">Cost object</span></span></th>
<th><span data-ttu-id="9f504-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-566">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-567">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-568">Amount</span></span></th>
<th><span data-ttu-id="9f504-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-570">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-570">CC003</span></span></td>
<td><span data-ttu-id="9f504-571">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-571">Assembly</span></span></td>
<td><span data-ttu-id="9f504-572">65</span><span class="sxs-lookup"><span data-stu-id="9f504-572">65</span></span></td>
<td><span data-ttu-id="9f504-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9f504-574">438.75</span><span class="sxs-lookup"><span data-stu-id="9f504-574">438.75</span></span></td>
<td><span data-ttu-id="9f504-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-576">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-576">CC004</span></span></td>
<td><span data-ttu-id="9f504-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-577">Packaging</span></span></td>
<td><span data-ttu-id="9f504-578">35</span><span class="sxs-lookup"><span data-stu-id="9f504-578">35</span></span></td>
<td><span data-ttu-id="9f504-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9f504-580">236.25</span><span class="sxs-lookup"><span data-stu-id="9f504-580">236.25</span></span></td>
<td><span data-ttu-id="9f504-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-582">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-582">CC003</span></span></td>
<td><span data-ttu-id="9f504-583">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-583">Assembly</span></span></td>
<td><span data-ttu-id="9f504-584">65</span><span class="sxs-lookup"><span data-stu-id="9f504-584">65</span></span></td>
<td><span data-ttu-id="9f504-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9f504-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9f504-586">5,297.69</span></span></td>
<td><span data-ttu-id="9f504-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-588">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-588">CC004</span></span></td>
<td><span data-ttu-id="9f504-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-589">Packaging</span></span></td>
<td><span data-ttu-id="9f504-590">35</span><span class="sxs-lookup"><span data-stu-id="9f504-590">35</span></span></td>
<td><span data-ttu-id="9f504-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9f504-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9f504-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9f504-592">2,852.60</span></span></td>
<td><span data-ttu-id="9f504-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="9f504-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-595">Cost object</span></span></th>
<th><span data-ttu-id="9f504-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-596">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-597">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-598">Amount</span></span></th>
<th><span data-ttu-id="9f504-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-600">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-601">Product 1</span></span></td>
<td><span data-ttu-id="9f504-602">60</span><span class="sxs-lookup"><span data-stu-id="9f504-602">60</span></span></td>
<td><span data-ttu-id="9f504-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9f504-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9f504-604">535.31</span><span class="sxs-lookup"><span data-stu-id="9f504-604">535.31</span></span></td>
<td><span data-ttu-id="9f504-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-606">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-607">Product 2</span></span></td>
<td><span data-ttu-id="9f504-608">20</span><span class="sxs-lookup"><span data-stu-id="9f504-608">20</span></span></td>
<td><span data-ttu-id="9f504-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9f504-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9f504-610">178.44</span><span class="sxs-lookup"><span data-stu-id="9f504-610">178.44</span></span></td>
<td><span data-ttu-id="9f504-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-612">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-613">Product 1</span></span></td>
<td><span data-ttu-id="9f504-614">60</span><span class="sxs-lookup"><span data-stu-id="9f504-614">60</span></span></td>
<td><span data-ttu-id="9f504-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9f504-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9f504-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9f504-616">4,487.12</span></span></td>
<td><span data-ttu-id="9f504-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-618">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-619">Product 2</span></span></td>
<td><span data-ttu-id="9f504-620">20</span><span class="sxs-lookup"><span data-stu-id="9f504-620">20</span></span></td>
<td><span data-ttu-id="9f504-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9f504-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9f504-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9f504-622">1,495.71</span></span></td>
<td><span data-ttu-id="9f504-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9f504-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="9f504-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-625">Cost object</span></span></th>
<th><span data-ttu-id="9f504-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="9f504-626">Magnitude</span></span></th>
<th><span data-ttu-id="9f504-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="9f504-627">Allocation factor</span></span></th>
<th><span data-ttu-id="9f504-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-628">Amount</span></span></th>
<th><span data-ttu-id="9f504-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-630">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-631">Product 1</span></span></td>
<td><span data-ttu-id="9f504-632">80</span><span class="sxs-lookup"><span data-stu-id="9f504-632">80</span></span></td>
<td><span data-ttu-id="9f504-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9f504-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9f504-634">241.05</span><span class="sxs-lookup"><span data-stu-id="9f504-634">241.05</span></span></td>
<td><span data-ttu-id="9f504-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-636">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-637">Product 2</span></span></td>
<td><span data-ttu-id="9f504-638">15</span><span class="sxs-lookup"><span data-stu-id="9f504-638">15</span></span></td>
<td><span data-ttu-id="9f504-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9f504-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9f504-640">45.20</span><span class="sxs-lookup"><span data-stu-id="9f504-640">45.20</span></span></td>
<td><span data-ttu-id="9f504-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-642">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-643">Product 1</span></span></td>
<td><span data-ttu-id="9f504-644">80</span><span class="sxs-lookup"><span data-stu-id="9f504-644">80</span></span></td>
<td><span data-ttu-id="9f504-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9f504-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9f504-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9f504-646">2,507.09</span></span></td>
<td><span data-ttu-id="9f504-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-648">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-649">Product 2</span></span></td>
<td><span data-ttu-id="9f504-650">15</span><span class="sxs-lookup"><span data-stu-id="9f504-650">15</span></span></td>
<td><span data-ttu-id="9f504-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9f504-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9f504-652">470.08</span><span class="sxs-lookup"><span data-stu-id="9f504-652">470.08</span></span></td>
<td><span data-ttu-id="9f504-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9f504-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="9f504-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="9f504-655">Journal</span></span></th>
<th><span data-ttu-id="9f504-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="9f504-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9f504-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="9f504-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9f504-658">Version</span><span class="sxs-lookup"><span data-stu-id="9f504-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-659">00004</span><span class="sxs-lookup"><span data-stu-id="9f504-659">00004</span></span></td>
<td><span data-ttu-id="9f504-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="9f504-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="9f504-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="9f504-661">Fiscal</span></span></td>
<td><span data-ttu-id="9f504-662">2017</span><span class="sxs-lookup"><span data-stu-id="9f504-662">2017</span></span></td>
<td><span data-ttu-id="9f504-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="9f504-663">Period 1</span></span></td>
<td><span data-ttu-id="9f504-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="9f504-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="9f504-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="9f504-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f504-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-668">Cost element</span></span></th>
<th><span data-ttu-id="9f504-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-669">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-672">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-672">CC001</span></span></td>
<td><span data-ttu-id="9f504-673">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-673">HR</span></span></td>
<td><span data-ttu-id="9f504-674">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-674">10001</span></span></td>
<td><span data-ttu-id="9f504-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-675">Electricity</span></span></td>
<td><span data-ttu-id="9f504-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-676">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-677">500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-679">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-679">CC001</span></span></td>
<td><span data-ttu-id="9f504-680">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-680">HR</span></span></td>
<td><span data-ttu-id="9f504-681">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-681">10001</span></span></td>
<td><span data-ttu-id="9f504-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-682">Electricity</span></span></td>
<td><span data-ttu-id="9f504-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-683">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="9f504-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-686">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-686">CC002</span></span></td>
<td><span data-ttu-id="9f504-687">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-687">Finance</span></span></td>
<td><span data-ttu-id="9f504-688">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-688">10001</span></span></td>
<td><span data-ttu-id="9f504-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-689">Electricity</span></span></td>
<td><span data-ttu-id="9f504-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-690">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-691">675.00</span><span class="sxs-lookup"><span data-stu-id="9f504-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-693">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-693">CC002</span></span></td>
<td><span data-ttu-id="9f504-694">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-694">Finance</span></span></td>
<td><span data-ttu-id="9f504-695">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-695">10001</span></span></td>
<td><span data-ttu-id="9f504-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-696">Electricity</span></span></td>
<td><span data-ttu-id="9f504-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-697">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="9f504-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-700">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-700">CC003</span></span></td>
<td><span data-ttu-id="9f504-701">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-701">Assembly</span></span></td>
<td><span data-ttu-id="9f504-702">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-702">10001</span></span></td>
<td><span data-ttu-id="9f504-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-703">Electricity</span></span></td>
<td><span data-ttu-id="9f504-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-704">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-705">713.75</span><span class="sxs-lookup"><span data-stu-id="9f504-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-707">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-707">CC003</span></span></td>
<td><span data-ttu-id="9f504-708">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-708">Assembly</span></span></td>
<td><span data-ttu-id="9f504-709">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-709">10001</span></span></td>
<td><span data-ttu-id="9f504-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-710">Electricity</span></span></td>
<td><span data-ttu-id="9f504-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-711">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="9f504-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-714">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-714">CC003</span></span></td>
<td><span data-ttu-id="9f504-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-715">Packaging</span></span></td>
<td><span data-ttu-id="9f504-716">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-716">10001</span></span></td>
<td><span data-ttu-id="9f504-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-717">Electricity</span></span></td>
<td><span data-ttu-id="9f504-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-718">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-719">286.25</span><span class="sxs-lookup"><span data-stu-id="9f504-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-721">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-721">CC003</span></span></td>
<td><span data-ttu-id="9f504-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-722">Packaging</span></span></td>
<td><span data-ttu-id="9f504-723">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-723">10001</span></span></td>
<td><span data-ttu-id="9f504-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-724">Electricity</span></span></td>
<td><span data-ttu-id="9f504-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-725">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="9f504-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-728">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-729">Product 1</span></span></td>
<td><span data-ttu-id="9f504-730">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-730">10001</span></span></td>
<td><span data-ttu-id="9f504-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-731">Electricity</span></span></td>
<td><span data-ttu-id="9f504-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-732">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-733">776.36</span><span class="sxs-lookup"><span data-stu-id="9f504-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-735">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-736">Product 1</span></span></td>
<td><span data-ttu-id="9f504-737">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-737">10001</span></span></td>
<td><span data-ttu-id="9f504-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-738">Electricity</span></span></td>
<td><span data-ttu-id="9f504-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-739">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9f504-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-742">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-743">Product 1</span></span></td>
<td><span data-ttu-id="9f504-744">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-744">10001</span></span></td>
<td><span data-ttu-id="9f504-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-745">Electricity</span></span></td>
<td><span data-ttu-id="9f504-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-746">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-747">223.64</span><span class="sxs-lookup"><span data-stu-id="9f504-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="9f504-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-749">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-750">Product 1</span></span></td>
<td><span data-ttu-id="9f504-751">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-751">10001</span></span></td>
<td><span data-ttu-id="9f504-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-752">Electricity</span></span></td>
<td><span data-ttu-id="9f504-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-753">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9f504-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9f504-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="9f504-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9f504-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9f504-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-757">Cost element</span></span></th>
<th><span data-ttu-id="9f504-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-758">Cost behavior</span></span></th>
<th><span data-ttu-id="9f504-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="9f504-759">Amount</span></span></th>
<th><span data-ttu-id="9f504-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="9f504-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f504-761">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-761">CC001</span></span></td>
<td><span data-ttu-id="9f504-762">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-762">HR</span></span></td>
<td><span data-ttu-id="9f504-763">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-763">10001</span></span></td>
<td><span data-ttu-id="9f504-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-764">Electricity</span></span></td>
<td><span data-ttu-id="9f504-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-765">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="9f504-766">-500.00</span></span></td>
<td><span data-ttu-id="9f504-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-768">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-768">CC002</span></span></td>
<td><span data-ttu-id="9f504-769">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-769">Finance</span></span></td>
<td><span data-ttu-id="9f504-770">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-770">10001</span></span></td>
<td><span data-ttu-id="9f504-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-771">Electricity</span></span></td>
<td><span data-ttu-id="9f504-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-772">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-773">175.00</span><span class="sxs-lookup"><span data-stu-id="9f504-773">175.00</span></span></td>
<td><span data-ttu-id="9f504-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-775">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-775">CC003</span></span></td>
<td><span data-ttu-id="9f504-776">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-776">Assembly</span></span></td>
<td><span data-ttu-id="9f504-777">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-777">10001</span></span></td>
<td><span data-ttu-id="9f504-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-778">Electricity</span></span></td>
<td><span data-ttu-id="9f504-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-779">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-780">275.00</span><span class="sxs-lookup"><span data-stu-id="9f504-780">275.00</span></span></td>
<td><span data-ttu-id="9f504-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-782">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-782">CC004</span></span></td>
<td><span data-ttu-id="9f504-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-783">Packaging</span></span></td>
<td><span data-ttu-id="9f504-784">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-784">10001</span></span></td>
<td><span data-ttu-id="9f504-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-785">Electricity</span></span></td>
<td><span data-ttu-id="9f504-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-786">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-787">50,00</span><span class="sxs-lookup"><span data-stu-id="9f504-787">50,00</span></span></td>
<td><span data-ttu-id="9f504-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-789">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-789">CC001</span></span></td>
<td><span data-ttu-id="9f504-790">Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f504-790">HR</span></span></td>
<td><span data-ttu-id="9f504-791">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-791">10001</span></span></td>
<td><span data-ttu-id="9f504-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-792">Electricity</span></span></td>
<td><span data-ttu-id="9f504-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-793">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="9f504-794">-1,245.71</span></span></td>
<td><span data-ttu-id="9f504-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-796">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-796">CC002</span></span></td>
<td><span data-ttu-id="9f504-797">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-797">Finance</span></span></td>
<td><span data-ttu-id="9f504-798">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-798">10001</span></span></td>
<td><span data-ttu-id="9f504-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-799">Electricity</span></span></td>
<td><span data-ttu-id="9f504-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-800">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-801">436.00</span><span class="sxs-lookup"><span data-stu-id="9f504-801">436.00</span></span></td>
<td><span data-ttu-id="9f504-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-803">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-803">CC003</span></span></td>
<td><span data-ttu-id="9f504-804">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-804">Assembly</span></span></td>
<td><span data-ttu-id="9f504-805">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-805">10001</span></span></td>
<td><span data-ttu-id="9f504-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-806">Electricity</span></span></td>
<td><span data-ttu-id="9f504-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-807">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-808">685.14</span><span class="sxs-lookup"><span data-stu-id="9f504-808">685.14</span></span></td>
<td><span data-ttu-id="9f504-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-810">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-810">CC004</span></span></td>
<td><span data-ttu-id="9f504-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-811">Packaging</span></span></td>
<td><span data-ttu-id="9f504-812">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-812">10001</span></span></td>
<td><span data-ttu-id="9f504-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-813">Electricity</span></span></td>
<td><span data-ttu-id="9f504-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-814">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-815">124.57</span><span class="sxs-lookup"><span data-stu-id="9f504-815">124.57</span></span></td>
<td><span data-ttu-id="9f504-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-817">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-817">CC002</span></span></td>
<td><span data-ttu-id="9f504-818">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-818">Finance</span></span></td>
<td><span data-ttu-id="9f504-819">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-819">10001</span></span></td>
<td><span data-ttu-id="9f504-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-820">Electricity</span></span></td>
<td><span data-ttu-id="9f504-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-821">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="9f504-822">-675.00</span></span></td>
<td><span data-ttu-id="9f504-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-824">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-824">CC003</span></span></td>
<td><span data-ttu-id="9f504-825">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-825">Assembly</span></span></td>
<td><span data-ttu-id="9f504-826">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-826">10001</span></span></td>
<td><span data-ttu-id="9f504-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-827">Electricity</span></span></td>
<td><span data-ttu-id="9f504-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-828">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-829">438.75</span><span class="sxs-lookup"><span data-stu-id="9f504-829">438.75</span></span></td>
<td><span data-ttu-id="9f504-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-831">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-831">CC004</span></span></td>
<td><span data-ttu-id="9f504-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-832">Packaging</span></span></td>
<td><span data-ttu-id="9f504-833">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-833">10001</span></span></td>
<td><span data-ttu-id="9f504-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-834">Electricity</span></span></td>
<td><span data-ttu-id="9f504-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-835">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-836">236.25</span><span class="sxs-lookup"><span data-stu-id="9f504-836">236.25</span></span></td>
<td><span data-ttu-id="9f504-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-838">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-838">CC002</span></span></td>
<td><span data-ttu-id="9f504-839">Finans</span><span class="sxs-lookup"><span data-stu-id="9f504-839">Finance</span></span></td>
<td><span data-ttu-id="9f504-840">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-840">10001</span></span></td>
<td><span data-ttu-id="9f504-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-841">Electricity</span></span></td>
<td><span data-ttu-id="9f504-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-842">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="9f504-843">-8,150.29</span></span></td>
<td><span data-ttu-id="9f504-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-845">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-845">CC003</span></span></td>
<td><span data-ttu-id="9f504-846">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-846">Assembly</span></span></td>
<td><span data-ttu-id="9f504-847">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-847">10001</span></span></td>
<td><span data-ttu-id="9f504-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-848">Electricity</span></span></td>
<td><span data-ttu-id="9f504-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-849">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9f504-850">5,297.69</span></span></td>
<td><span data-ttu-id="9f504-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-852">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-852">CC004</span></span></td>
<td><span data-ttu-id="9f504-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="9f504-853">Packaging</span></span></td>
<td><span data-ttu-id="9f504-854">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-854">10001</span></span></td>
<td><span data-ttu-id="9f504-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-855">Electricity</span></span></td>
<td><span data-ttu-id="9f504-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-856">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9f504-857">2,852.60</span></span></td>
<td><span data-ttu-id="9f504-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-859">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-859">CC003</span></span></td>
<td><span data-ttu-id="9f504-860">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-860">Assembly</span></span></td>
<td><span data-ttu-id="9f504-861">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-861">10001</span></span></td>
<td><span data-ttu-id="9f504-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-862">Electricity</span></span></td>
<td><span data-ttu-id="9f504-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-863">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="9f504-864">-713.75</span></span></td>
<td><span data-ttu-id="9f504-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-866">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-867">Product 1</span></span></td>
<td><span data-ttu-id="9f504-868">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-868">10001</span></span></td>
<td><span data-ttu-id="9f504-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-869">Electricity</span></span></td>
<td><span data-ttu-id="9f504-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-870">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-871">535.31</span><span class="sxs-lookup"><span data-stu-id="9f504-871">535.31</span></span></td>
<td><span data-ttu-id="9f504-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-873">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-874">Product 2</span></span></td>
<td><span data-ttu-id="9f504-875">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-875">10001</span></span></td>
<td><span data-ttu-id="9f504-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-876">Electricity</span></span></td>
<td><span data-ttu-id="9f504-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-877">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-878">178.44</span><span class="sxs-lookup"><span data-stu-id="9f504-878">178.44</span></span></td>
<td><span data-ttu-id="9f504-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-880">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-880">CC003</span></span></td>
<td><span data-ttu-id="9f504-881">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-881">Assembly</span></span></td>
<td><span data-ttu-id="9f504-882">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-882">10001</span></span></td>
<td><span data-ttu-id="9f504-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-883">Electricity</span></span></td>
<td><span data-ttu-id="9f504-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-884">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="9f504-885">-5,982.83</span></span></td>
<td><span data-ttu-id="9f504-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-887">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-888">Product 1</span></span></td>
<td><span data-ttu-id="9f504-889">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-889">10001</span></span></td>
<td><span data-ttu-id="9f504-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-890">Electricity</span></span></td>
<td><span data-ttu-id="9f504-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-891">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9f504-892">4,487.12</span></span></td>
<td><span data-ttu-id="9f504-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-894">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-895">Product 2</span></span></td>
<td><span data-ttu-id="9f504-896">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-896">10001</span></span></td>
<td><span data-ttu-id="9f504-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-897">Electricity</span></span></td>
<td><span data-ttu-id="9f504-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-898">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9f504-899">1,495.71</span></span></td>
<td><span data-ttu-id="9f504-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-901">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-901">CC003</span></span></td>
<td><span data-ttu-id="9f504-902">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-902">Assembly</span></span></td>
<td><span data-ttu-id="9f504-903">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-903">10001</span></span></td>
<td><span data-ttu-id="9f504-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-904">Electricity</span></span></td>
<td><span data-ttu-id="9f504-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-905">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="9f504-906">-286.25</span></span></td>
<td><span data-ttu-id="9f504-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-908">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-909">Product 1</span></span></td>
<td><span data-ttu-id="9f504-910">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-910">10001</span></span></td>
<td><span data-ttu-id="9f504-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-911">Electricity</span></span></td>
<td><span data-ttu-id="9f504-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-912">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-913">241.05</span><span class="sxs-lookup"><span data-stu-id="9f504-913">241.05</span></span></td>
<td><span data-ttu-id="9f504-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-915">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-916">Product 2</span></span></td>
<td><span data-ttu-id="9f504-917">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-917">10001</span></span></td>
<td><span data-ttu-id="9f504-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-918">Electricity</span></span></td>
<td><span data-ttu-id="9f504-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-919">Fixed cost</span></span></td>
<td><span data-ttu-id="9f504-920">45.20</span><span class="sxs-lookup"><span data-stu-id="9f504-920">45.20</span></span></td>
<td><span data-ttu-id="9f504-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-922">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-922">CC003</span></span></td>
<td><span data-ttu-id="9f504-923">Samling</span><span class="sxs-lookup"><span data-stu-id="9f504-923">Assembly</span></span></td>
<td><span data-ttu-id="9f504-924">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-924">10001</span></span></td>
<td><span data-ttu-id="9f504-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-925">Electricity</span></span></td>
<td><span data-ttu-id="9f504-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-926">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="9f504-927">-2,977.17</span></span></td>
<td><span data-ttu-id="9f504-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-929">Prod 1</span></span></td>
<td><span data-ttu-id="9f504-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="9f504-930">Product 1</span></span></td>
<td><span data-ttu-id="9f504-931">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-931">10001</span></span></td>
<td><span data-ttu-id="9f504-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-932">Electricity</span></span></td>
<td><span data-ttu-id="9f504-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-933">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9f504-934">2,507.09</span></span></td>
<td><span data-ttu-id="9f504-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9f504-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-936">Prod 2</span></span></td>
<td><span data-ttu-id="9f504-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="9f504-937">Product 2</span></span></td>
<td><span data-ttu-id="9f504-938">10001</span><span class="sxs-lookup"><span data-stu-id="9f504-938">10001</span></span></td>
<td><span data-ttu-id="9f504-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-939">Electricity</span></span></td>
<td><span data-ttu-id="9f504-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-940">Variable cost</span></span></td>
<td><span data-ttu-id="9f504-941">470.08</span><span class="sxs-lookup"><span data-stu-id="9f504-941">470.08</span></span></td>
<td><span data-ttu-id="9f504-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="9f504-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="9f504-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="9f504-943">Conclusion</span></span>
<span data-ttu-id="9f504-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="9f504-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="9f504-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="9f504-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="9f504-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="9f504-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="9f504-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9f504-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="9f504-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="9f504-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="9f504-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="9f504-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="9f504-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="9f504-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9f504-951">CC099</span><span class="sxs-lookup"><span data-stu-id="9f504-951">CC099</span></span></th>
<th><span data-ttu-id="9f504-952">CC001</span><span class="sxs-lookup"><span data-stu-id="9f504-952">CC001</span></span></th>
<th><span data-ttu-id="9f504-953">CC002</span><span class="sxs-lookup"><span data-stu-id="9f504-953">CC002</span></span></th>
<th><span data-ttu-id="9f504-954">CC003</span><span class="sxs-lookup"><span data-stu-id="9f504-954">CC003</span></span></th>
<th><span data-ttu-id="9f504-955">CC004</span><span class="sxs-lookup"><span data-stu-id="9f504-955">CC004</span></span></th>
<th><span data-ttu-id="9f504-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="9f504-956">Proj 1</span></span></th>
<th><span data-ttu-id="9f504-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="9f504-957">Proj 2</span></span></th>
<th><span data-ttu-id="9f504-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="9f504-958">Prod 1</span></span></th>
<th><span data-ttu-id="9f504-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="9f504-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="9f504-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="9f504-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9f504-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="9f504-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="9f504-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-971">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="9f504-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-973">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-974">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-975">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-976">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-977">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9f504-978">776.36</span><span class="sxs-lookup"><span data-stu-id="9f504-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-979">223.64</span><span class="sxs-lookup"><span data-stu-id="9f504-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="9f504-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="9f504-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-982">000</span><span class="sxs-lookup"><span data-stu-id="9f504-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-983">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-984">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-985">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-986">0,00</span><span class="sxs-lookup"><span data-stu-id="9f504-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-987">30,00</span><span class="sxs-lookup"><span data-stu-id="9f504-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-988">10,00</span><span class="sxs-lookup"><span data-stu-id="9f504-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9f504-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9f504-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9f504-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9f504-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9f504-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="9f504-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="9f504-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="9f504-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="9f504-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="9f504-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="9f504-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="9f504-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="9f504-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="9f504-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]