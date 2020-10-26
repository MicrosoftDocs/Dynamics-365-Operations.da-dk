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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976469"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6439a-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6439a-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="6439a-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6439a-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="6439a-105">Term definition</span></span>
---------------

<span data-ttu-id="6439a-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="6439a-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6439a-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="6439a-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6439a-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="6439a-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6439a-109">Leje</span><span class="sxs-lookup"><span data-stu-id="6439a-109">Rent</span></span>
-   <span data-ttu-id="6439a-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-110">Electricity</span></span>
-   <span data-ttu-id="6439a-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="6439a-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6439a-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-112">Overhead calculation overview</span></span>
<span data-ttu-id="6439a-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="6439a-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6439a-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="6439a-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6439a-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="6439a-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6439a-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="6439a-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6439a-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="6439a-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6439a-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="6439a-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6439a-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="6439a-119">Version type</span></span>
-   <span data-ttu-id="6439a-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="6439a-120">Date and time</span></span>
-   <span data-ttu-id="6439a-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="6439a-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6439a-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="6439a-122">Fiscal year</span></span>
-   <span data-ttu-id="6439a-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="6439a-123">Fiscal period</span></span>

<span data-ttu-id="6439a-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="6439a-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6439a-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="6439a-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6439a-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="6439a-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6439a-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="6439a-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6439a-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="6439a-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6439a-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="6439a-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6439a-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="6439a-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6439a-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6439a-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6439a-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6439a-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="6439a-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6439a-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="6439a-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6439a-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="6439a-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6439a-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="6439a-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6439a-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6439a-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="6439a-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="6439a-140">Main account</span></span></th>
<th><span data-ttu-id="6439a-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="6439a-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6439a-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-143">CC099</span></span></td>
<td><span data-ttu-id="6439a-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-144">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-145">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-145">10001</span></span></td>
<td><span data-ttu-id="6439a-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-146">Electricity</span></span></td>
<td><span data-ttu-id="6439a-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6439a-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="6439a-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6439a-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="6439a-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6439a-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="6439a-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6439a-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="6439a-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6439a-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="6439a-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6439a-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="6439a-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6439a-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="6439a-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6439a-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="6439a-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6439a-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6439a-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="6439a-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6439a-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="6439a-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6439a-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-160">Journal</span></span></th>
<th><span data-ttu-id="6439a-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="6439a-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6439a-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6439a-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6439a-163">Version</span><span class="sxs-lookup"><span data-stu-id="6439a-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-164">00001</span><span class="sxs-lookup"><span data-stu-id="6439a-164">00001</span></span></td>
<td><span data-ttu-id="6439a-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6439a-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="6439a-166">Fiscal</span></span></td>
<td><span data-ttu-id="6439a-167">2017</span><span class="sxs-lookup"><span data-stu-id="6439a-167">2017</span></span></td>
<td><span data-ttu-id="6439a-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="6439a-168">Period 1</span></span></td>
<td><span data-ttu-id="6439a-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="6439a-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6439a-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="6439a-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-173">Cost element</span></span></th>
<th><span data-ttu-id="6439a-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6439a-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-177">CC099</span></span></td>
<td><span data-ttu-id="6439a-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-178">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-179">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-179">10001</span></span></td>
<td><span data-ttu-id="6439a-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-180">Electricity</span></span></td>
<td><span data-ttu-id="6439a-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="6439a-181">Unclassified</span></span></td>
<td><span data-ttu-id="6439a-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6439a-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="6439a-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-185">Cost element</span></span></th>
<th><span data-ttu-id="6439a-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-187">Amount</span></span></th>
<th><span data-ttu-id="6439a-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-189">CC099</span></span></td>
<td><span data-ttu-id="6439a-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-190">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-191">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-191">10001</span></span></td>
<td><span data-ttu-id="6439a-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-192">Electricity</span></span></td>
<td><span data-ttu-id="6439a-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="6439a-193">Unclassified</span></span></td>
<td><span data-ttu-id="6439a-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-194">10,000.00</span></span></td>
<td><span data-ttu-id="6439a-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-196">CC099</span></span></td>
<td><span data-ttu-id="6439a-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-197">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-198">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-198">10001</span></span></td>
<td><span data-ttu-id="6439a-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-199">Electricity</span></span></td>
<td><span data-ttu-id="6439a-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="6439a-200">Unclassified</span></span></td>
<td><span data-ttu-id="6439a-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6439a-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-203">CC099</span></span></td>
<td><span data-ttu-id="6439a-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-204">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-205">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-205">10001</span></span></td>
<td><span data-ttu-id="6439a-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-206">Electricity</span></span></td>
<td><span data-ttu-id="6439a-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-208">1,000.00</span></span></td>
<td><span data-ttu-id="6439a-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-210">CC099</span></span></td>
<td><span data-ttu-id="6439a-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-211">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-212">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-212">10001</span></span></td>
<td><span data-ttu-id="6439a-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-213">Electricity</span></span></td>
<td><span data-ttu-id="6439a-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-214">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-215">9,000.00</span></span></td>
<td><span data-ttu-id="6439a-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="6439a-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6439a-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="6439a-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6439a-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6439a-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="6439a-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6439a-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="6439a-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6439a-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="6439a-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6439a-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="6439a-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6439a-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6439a-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="6439a-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6439a-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="6439a-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6439a-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-228">Cost object</span></span></th>
<th><span data-ttu-id="6439a-229">KWh</span><span class="sxs-lookup"><span data-stu-id="6439a-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-230">CC001</span></span></td>
<td><span data-ttu-id="6439a-231">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-231">HR</span></span></td>
<td><span data-ttu-id="6439a-232">1.000</span><span class="sxs-lookup"><span data-stu-id="6439a-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-233">CC002</span></span></td>
<td><span data-ttu-id="6439a-234">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-234">Finance</span></span></td>
<td><span data-ttu-id="6439a-235">6.000</span><span class="sxs-lookup"><span data-stu-id="6439a-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-236">CC003</span></span></td>
<td><span data-ttu-id="6439a-237">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-237">Assembly</span></span></td>
<td><span data-ttu-id="6439a-238">0</span><span class="sxs-lookup"><span data-stu-id="6439a-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="6439a-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-240">Cost object</span></span></th>
<th><span data-ttu-id="6439a-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-241">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-244">CC001</span></span></td>
<td><span data-ttu-id="6439a-245">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-245">HR</span></span></td>
<td><span data-ttu-id="6439a-246">1.000</span><span class="sxs-lookup"><span data-stu-id="6439a-246">1,000</span></span></td>
<td><span data-ttu-id="6439a-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6439a-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6439a-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-249">CC002</span></span></td>
<td><span data-ttu-id="6439a-250">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-250">Finance</span></span></td>
<td><span data-ttu-id="6439a-251">6.000</span><span class="sxs-lookup"><span data-stu-id="6439a-251">6,000</span></span></td>
<td><span data-ttu-id="6439a-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6439a-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6439a-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-254">CC003</span></span></td>
<td><span data-ttu-id="6439a-255">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-255">Assembly</span></span></td>
<td><span data-ttu-id="6439a-256">0</span><span class="sxs-lookup"><span data-stu-id="6439a-256">0</span></span></td>
<td><span data-ttu-id="6439a-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6439a-258">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="6439a-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6439a-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="6439a-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-261">Cost object</span></span></th>
<th><span data-ttu-id="6439a-262">Formel</span><span class="sxs-lookup"><span data-stu-id="6439a-262">Formula</span></span></th>
<th><span data-ttu-id="6439a-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-263">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-266">CC001</span></span></td>
<td><span data-ttu-id="6439a-267">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-267">HR</span></span></td>
<td><span data-ttu-id="6439a-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6439a-269">1</span><span class="sxs-lookup"><span data-stu-id="6439a-269">1</span></span></td>
<td><span data-ttu-id="6439a-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6439a-271">500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-272">CC002</span></span></td>
<td><span data-ttu-id="6439a-273">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-273">Finance</span></span></td>
<td><span data-ttu-id="6439a-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6439a-275">1</span><span class="sxs-lookup"><span data-stu-id="6439a-275">1</span></span></td>
<td><span data-ttu-id="6439a-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6439a-277">500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-278">CC003</span></span></td>
<td><span data-ttu-id="6439a-279">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-279">Assembly</span></span></td>
<td><span data-ttu-id="6439a-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6439a-281">0</span><span class="sxs-lookup"><span data-stu-id="6439a-281">0</span></span></td>
<td><span data-ttu-id="6439a-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6439a-283">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6439a-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-285">Journal</span></span></th>
<th><span data-ttu-id="6439a-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="6439a-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6439a-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6439a-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6439a-288">Version</span><span class="sxs-lookup"><span data-stu-id="6439a-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-289">00002</span><span class="sxs-lookup"><span data-stu-id="6439a-289">00002</span></span></td>
<td><span data-ttu-id="6439a-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="6439a-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6439a-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="6439a-291">Fiscal</span></span></td>
<td><span data-ttu-id="6439a-292">2017</span><span class="sxs-lookup"><span data-stu-id="6439a-292">2017</span></span></td>
<td><span data-ttu-id="6439a-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="6439a-293">Period 1</span></span></td>
<td><span data-ttu-id="6439a-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="6439a-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6439a-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="6439a-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-298">Cost element</span></span></th>
<th><span data-ttu-id="6439a-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-302">CC099</span></span></td>
<td><span data-ttu-id="6439a-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-303">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-304">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-304">10001</span></span></td>
<td><span data-ttu-id="6439a-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-305">Electricity</span></span></td>
<td><span data-ttu-id="6439a-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-309">CC099</span></span></td>
<td><span data-ttu-id="6439a-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-310">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-311">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-311">10001</span></span></td>
<td><span data-ttu-id="6439a-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-312">Electricity</span></span></td>
<td><span data-ttu-id="6439a-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-313">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6439a-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="6439a-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-317">Cost element</span></span></th>
<th><span data-ttu-id="6439a-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-319">Amount</span></span></th>
<th><span data-ttu-id="6439a-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-321">CC099</span></span></td>
<td><span data-ttu-id="6439a-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-322">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-323">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-323">10001</span></span></td>
<td><span data-ttu-id="6439a-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-324">Electricity</span></span></td>
<td><span data-ttu-id="6439a-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6439a-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-328">CC001</span></span></td>
<td><span data-ttu-id="6439a-329">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-329">HR</span></span></td>
<td><span data-ttu-id="6439a-330">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-330">10001</span></span></td>
<td><span data-ttu-id="6439a-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-331">Electricity</span></span></td>
<td><span data-ttu-id="6439a-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-333">500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-333">500.00</span></span></td>
<td><span data-ttu-id="6439a-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-335">CC002</span></span></td>
<td><span data-ttu-id="6439a-336">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-336">Finance</span></span></td>
<td><span data-ttu-id="6439a-337">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-337">10001</span></span></td>
<td><span data-ttu-id="6439a-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-338">Electricity</span></span></td>
<td><span data-ttu-id="6439a-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-340">500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-340">500.00</span></span></td>
<td><span data-ttu-id="6439a-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-342">CC099</span></span></td>
<td><span data-ttu-id="6439a-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="6439a-343">Default cost center</span></span></td>
<td><span data-ttu-id="6439a-344">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-344">10001</span></span></td>
<td><span data-ttu-id="6439a-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-345">Electricity</span></span></td>
<td><span data-ttu-id="6439a-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-346">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="6439a-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6439a-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-349">CC001</span></span></td>
<td><span data-ttu-id="6439a-350">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-350">HR</span></span></td>
<td><span data-ttu-id="6439a-351">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-351">10001</span></span></td>
<td><span data-ttu-id="6439a-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-352">Electricity</span></span></td>
<td><span data-ttu-id="6439a-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-353">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6439a-354">1,285.71</span></span></td>
<td><span data-ttu-id="6439a-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-356">CC002</span></span></td>
<td><span data-ttu-id="6439a-357">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-357">Finance</span></span></td>
<td><span data-ttu-id="6439a-358">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-358">10001</span></span></td>
<td><span data-ttu-id="6439a-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-359">Electricity</span></span></td>
<td><span data-ttu-id="6439a-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-360">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6439a-361">7,714.29</span></span></td>
<td><span data-ttu-id="6439a-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="6439a-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6439a-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="6439a-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6439a-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6439a-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6439a-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="6439a-367">Define the overhead rate</span></span>

<span data-ttu-id="6439a-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6439a-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="6439a-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-370">Cost object</span></span></th>
<th><span data-ttu-id="6439a-371">Timer</span><span class="sxs-lookup"><span data-stu-id="6439a-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-372">Proj 1</span></span></td>
<td><span data-ttu-id="6439a-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-373">Project 1</span></span></td>
<td><span data-ttu-id="6439a-374">3</span><span class="sxs-lookup"><span data-stu-id="6439a-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-375">Proj 2</span></span></td>
<td><span data-ttu-id="6439a-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-376">Project 2</span></span></td>
<td><span data-ttu-id="6439a-377">1</span><span class="sxs-lookup"><span data-stu-id="6439a-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="6439a-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-379">Cost object</span></span></th>
<th><span data-ttu-id="6439a-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-380">Cost element</span></span></th>
<th><span data-ttu-id="6439a-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="6439a-382">Units</span></span></th>
<th><span data-ttu-id="6439a-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="6439a-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-384">CC001</span></span></td>
<td><span data-ttu-id="6439a-385">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-385">HR</span></span></td>
<td><span data-ttu-id="6439a-386">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-386">10001</span></span></td>
<td><span data-ttu-id="6439a-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-387">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-388">1</span><span class="sxs-lookup"><span data-stu-id="6439a-388">1</span></span></td>
<td><span data-ttu-id="6439a-389">10</span><span class="sxs-lookup"><span data-stu-id="6439a-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-391">Cost object</span></span></th>
<th><span data-ttu-id="6439a-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-392">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-393">Cost element</span></span></th>
<th><span data-ttu-id="6439a-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-396">Proj 1</span></span></td>
<td><span data-ttu-id="6439a-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-397">Project 1</span></span></td>
<td><span data-ttu-id="6439a-398">3</span><span class="sxs-lookup"><span data-stu-id="6439a-398">3</span></span></td>
<td><span data-ttu-id="6439a-399">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-399">10001</span></span></td>
<td><span data-ttu-id="6439a-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6439a-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6439a-401">30,00</span><span class="sxs-lookup"><span data-stu-id="6439a-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-402">Proj 2</span></span></td>
<td><span data-ttu-id="6439a-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-403">Project 2</span></span></td>
<td><span data-ttu-id="6439a-404">1</span><span class="sxs-lookup"><span data-stu-id="6439a-404">1</span></span></td>
<td><span data-ttu-id="6439a-405">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-405">10001</span></span></td>
<td><span data-ttu-id="6439a-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6439a-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6439a-407">10,00</span><span class="sxs-lookup"><span data-stu-id="6439a-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6439a-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-409">Journal</span></span></th>
<th><span data-ttu-id="6439a-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="6439a-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6439a-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6439a-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6439a-412">Version</span><span class="sxs-lookup"><span data-stu-id="6439a-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-413">00003</span><span class="sxs-lookup"><span data-stu-id="6439a-413">00003</span></span></td>
<td><span data-ttu-id="6439a-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="6439a-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6439a-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="6439a-415">Fiscal</span></span></td>
<td><span data-ttu-id="6439a-416">2017</span><span class="sxs-lookup"><span data-stu-id="6439a-416">2017</span></span></td>
<td><span data-ttu-id="6439a-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="6439a-417">Period 1</span></span></td>
<td><span data-ttu-id="6439a-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="6439a-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6439a-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="6439a-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-421">Cost object</span></span></th>
<th><span data-ttu-id="6439a-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-424">Proj 1</span></span></td>
<td><span data-ttu-id="6439a-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6439a-426">3,00</span><span class="sxs-lookup"><span data-stu-id="6439a-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-428">Proj 2</span></span></td>
<td><span data-ttu-id="6439a-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6439a-430">1,00</span><span class="sxs-lookup"><span data-stu-id="6439a-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6439a-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="6439a-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-433">Cost element</span></span></th>
<th><span data-ttu-id="6439a-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-435">Amount</span></span></th>
<th><span data-ttu-id="6439a-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6439a-437">CC0001</span></span></td>
<td><span data-ttu-id="6439a-438">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-438">HR</span></span></td>
<td><span data-ttu-id="6439a-439">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-439">10001</span></span></td>
<td><span data-ttu-id="6439a-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-440">Electricity</span></span></td>
<td><span data-ttu-id="6439a-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-441">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="6439a-442">-30.00</span></span></td>
<td><span data-ttu-id="6439a-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-444">Proj 1</span></span></td>
<td><span data-ttu-id="6439a-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6439a-446">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-446">10001</span></span></td>
<td><span data-ttu-id="6439a-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-447">Electricity</span></span></td>
<td><span data-ttu-id="6439a-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-448">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-449">30,00</span><span class="sxs-lookup"><span data-stu-id="6439a-449">30.00</span></span></td>
<td><span data-ttu-id="6439a-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-451">CC001</span></span></td>
<td><span data-ttu-id="6439a-452">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-452">HR</span></span></td>
<td><span data-ttu-id="6439a-453">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-453">10001</span></span></td>
<td><span data-ttu-id="6439a-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-454">Electricity</span></span></td>
<td><span data-ttu-id="6439a-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-455">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="6439a-456">-10.00</span></span></td>
<td><span data-ttu-id="6439a-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-458">Proj 2</span></span></td>
<td><span data-ttu-id="6439a-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6439a-460">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-460">10001</span></span></td>
<td><span data-ttu-id="6439a-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-461">Electricity</span></span></td>
<td><span data-ttu-id="6439a-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-462">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-463">10.00</span><span class="sxs-lookup"><span data-stu-id="6439a-463">10.00</span></span></td>
<td><span data-ttu-id="6439a-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="6439a-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6439a-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="6439a-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6439a-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6439a-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="6439a-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="6439a-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="6439a-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6439a-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="6439a-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6439a-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="6439a-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6439a-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="6439a-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6439a-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="6439a-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6439a-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6439a-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6439a-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="6439a-475">Define the cost allocation</span></span>

<span data-ttu-id="6439a-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="6439a-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6439a-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6439a-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="6439a-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-479">Cost object</span></span></th>
<th><span data-ttu-id="6439a-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="6439a-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-481">CC002</span></span></td>
<td><span data-ttu-id="6439a-482">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-482">Finance</span></span></td>
<td><span data-ttu-id="6439a-483">35</span><span class="sxs-lookup"><span data-stu-id="6439a-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-484">CC003</span></span></td>
<td><span data-ttu-id="6439a-485">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-485">Assembly</span></span></td>
<td><span data-ttu-id="6439a-486">55</span><span class="sxs-lookup"><span data-stu-id="6439a-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-487">CC004</span></span></td>
<td><span data-ttu-id="6439a-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-488">Packaging</span></span></td>
<td><span data-ttu-id="6439a-489">10</span><span class="sxs-lookup"><span data-stu-id="6439a-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6439a-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="6439a-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-492">Cost object</span></span></th>
<th><span data-ttu-id="6439a-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="6439a-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-494">CC003</span></span></td>
<td><span data-ttu-id="6439a-495">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-495">Assembly</span></span></td>
<td><span data-ttu-id="6439a-496">65</span><span class="sxs-lookup"><span data-stu-id="6439a-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-497">CC004</span></span></td>
<td><span data-ttu-id="6439a-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-498">Packaging</span></span></td>
<td><span data-ttu-id="6439a-499">35</span><span class="sxs-lookup"><span data-stu-id="6439a-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6439a-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="6439a-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-502">Cost object</span></span></th>
<th><span data-ttu-id="6439a-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="6439a-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-504">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-505">Product 1</span></span></td>
<td><span data-ttu-id="6439a-506">60</span><span class="sxs-lookup"><span data-stu-id="6439a-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-507">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-508">Product 2</span></span></td>
<td><span data-ttu-id="6439a-509">20</span><span class="sxs-lookup"><span data-stu-id="6439a-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6439a-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="6439a-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-512">Cost object</span></span></th>
<th><span data-ttu-id="6439a-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="6439a-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-514">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-515">Product 1</span></span></td>
<td><span data-ttu-id="6439a-516">80</span><span class="sxs-lookup"><span data-stu-id="6439a-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-517">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-518">Product 2</span></span></td>
<td><span data-ttu-id="6439a-519">15</span><span class="sxs-lookup"><span data-stu-id="6439a-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6439a-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="6439a-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6439a-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="6439a-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6439a-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="6439a-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-523">Cost object</span></span></th>
<th><span data-ttu-id="6439a-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-524">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-526">Amount</span></span></th>
<th><span data-ttu-id="6439a-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-528">CC002</span></span></td>
<td><span data-ttu-id="6439a-529">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-529">Finance</span></span></td>
<td><span data-ttu-id="6439a-530">35</span><span class="sxs-lookup"><span data-stu-id="6439a-530">35</span></span></td>
<td><span data-ttu-id="6439a-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6439a-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6439a-532">175.00</span></span></td>
<td><span data-ttu-id="6439a-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-534">CC003</span></span></td>
<td><span data-ttu-id="6439a-535">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-535">Assembly</span></span></td>
<td><span data-ttu-id="6439a-536">55</span><span class="sxs-lookup"><span data-stu-id="6439a-536">55</span></span></td>
<td><span data-ttu-id="6439a-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6439a-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6439a-538">275.00</span></span></td>
<td><span data-ttu-id="6439a-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-540">CC004</span></span></td>
<td><span data-ttu-id="6439a-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-541">Packaging</span></span></td>
<td><span data-ttu-id="6439a-542">10</span><span class="sxs-lookup"><span data-stu-id="6439a-542">10</span></span></td>
<td><span data-ttu-id="6439a-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6439a-544">50,00</span><span class="sxs-lookup"><span data-stu-id="6439a-544">50.00</span></span></td>
<td><span data-ttu-id="6439a-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-546">CC002</span></span></td>
<td><span data-ttu-id="6439a-547">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-547">Finance</span></span></td>
<td><span data-ttu-id="6439a-548">35</span><span class="sxs-lookup"><span data-stu-id="6439a-548">35</span></span></td>
<td><span data-ttu-id="6439a-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6439a-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6439a-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6439a-550">436.00</span></span></td>
<td><span data-ttu-id="6439a-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-552">CC003</span></span></td>
<td><span data-ttu-id="6439a-553">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-553">Assembly</span></span></td>
<td><span data-ttu-id="6439a-554">55</span><span class="sxs-lookup"><span data-stu-id="6439a-554">55</span></span></td>
<td><span data-ttu-id="6439a-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6439a-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6439a-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6439a-556">685.14</span></span></td>
<td><span data-ttu-id="6439a-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-558">CC004</span></span></td>
<td><span data-ttu-id="6439a-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-559">Packaging</span></span></td>
<td><span data-ttu-id="6439a-560">10</span><span class="sxs-lookup"><span data-stu-id="6439a-560">10</span></span></td>
<td><span data-ttu-id="6439a-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6439a-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6439a-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6439a-562">124.57</span></span></td>
<td><span data-ttu-id="6439a-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="6439a-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-565">Cost object</span></span></th>
<th><span data-ttu-id="6439a-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-566">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-568">Amount</span></span></th>
<th><span data-ttu-id="6439a-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-570">CC003</span></span></td>
<td><span data-ttu-id="6439a-571">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-571">Assembly</span></span></td>
<td><span data-ttu-id="6439a-572">65</span><span class="sxs-lookup"><span data-stu-id="6439a-572">65</span></span></td>
<td><span data-ttu-id="6439a-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6439a-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6439a-574">438.75</span></span></td>
<td><span data-ttu-id="6439a-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-576">CC004</span></span></td>
<td><span data-ttu-id="6439a-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-577">Packaging</span></span></td>
<td><span data-ttu-id="6439a-578">35</span><span class="sxs-lookup"><span data-stu-id="6439a-578">35</span></span></td>
<td><span data-ttu-id="6439a-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6439a-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6439a-580">236.25</span></span></td>
<td><span data-ttu-id="6439a-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-582">CC003</span></span></td>
<td><span data-ttu-id="6439a-583">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-583">Assembly</span></span></td>
<td><span data-ttu-id="6439a-584">65</span><span class="sxs-lookup"><span data-stu-id="6439a-584">65</span></span></td>
<td><span data-ttu-id="6439a-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6439a-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6439a-586">5,297.69</span></span></td>
<td><span data-ttu-id="6439a-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-588">CC004</span></span></td>
<td><span data-ttu-id="6439a-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-589">Packaging</span></span></td>
<td><span data-ttu-id="6439a-590">35</span><span class="sxs-lookup"><span data-stu-id="6439a-590">35</span></span></td>
<td><span data-ttu-id="6439a-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6439a-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6439a-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6439a-592">2,852.60</span></span></td>
<td><span data-ttu-id="6439a-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="6439a-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-595">Cost object</span></span></th>
<th><span data-ttu-id="6439a-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-596">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-598">Amount</span></span></th>
<th><span data-ttu-id="6439a-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-600">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-601">Product 1</span></span></td>
<td><span data-ttu-id="6439a-602">60</span><span class="sxs-lookup"><span data-stu-id="6439a-602">60</span></span></td>
<td><span data-ttu-id="6439a-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6439a-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6439a-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6439a-604">535.31</span></span></td>
<td><span data-ttu-id="6439a-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-606">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-607">Product 2</span></span></td>
<td><span data-ttu-id="6439a-608">20</span><span class="sxs-lookup"><span data-stu-id="6439a-608">20</span></span></td>
<td><span data-ttu-id="6439a-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6439a-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6439a-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6439a-610">178.44</span></span></td>
<td><span data-ttu-id="6439a-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-612">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-613">Product 1</span></span></td>
<td><span data-ttu-id="6439a-614">60</span><span class="sxs-lookup"><span data-stu-id="6439a-614">60</span></span></td>
<td><span data-ttu-id="6439a-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6439a-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6439a-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6439a-616">4,487.12</span></span></td>
<td><span data-ttu-id="6439a-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-618">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-619">Product 2</span></span></td>
<td><span data-ttu-id="6439a-620">20</span><span class="sxs-lookup"><span data-stu-id="6439a-620">20</span></span></td>
<td><span data-ttu-id="6439a-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6439a-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6439a-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6439a-622">1,495.71</span></span></td>
<td><span data-ttu-id="6439a-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6439a-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="6439a-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-625">Cost object</span></span></th>
<th><span data-ttu-id="6439a-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="6439a-626">Magnitude</span></span></th>
<th><span data-ttu-id="6439a-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="6439a-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6439a-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-628">Amount</span></span></th>
<th><span data-ttu-id="6439a-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-630">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-631">Product 1</span></span></td>
<td><span data-ttu-id="6439a-632">80</span><span class="sxs-lookup"><span data-stu-id="6439a-632">80</span></span></td>
<td><span data-ttu-id="6439a-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6439a-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6439a-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6439a-634">241.05</span></span></td>
<td><span data-ttu-id="6439a-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-636">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-637">Product 2</span></span></td>
<td><span data-ttu-id="6439a-638">15</span><span class="sxs-lookup"><span data-stu-id="6439a-638">15</span></span></td>
<td><span data-ttu-id="6439a-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6439a-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6439a-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6439a-640">45.20</span></span></td>
<td><span data-ttu-id="6439a-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-642">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-643">Product 1</span></span></td>
<td><span data-ttu-id="6439a-644">80</span><span class="sxs-lookup"><span data-stu-id="6439a-644">80</span></span></td>
<td><span data-ttu-id="6439a-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6439a-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6439a-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6439a-646">2,507.09</span></span></td>
<td><span data-ttu-id="6439a-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-648">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-649">Product 2</span></span></td>
<td><span data-ttu-id="6439a-650">15</span><span class="sxs-lookup"><span data-stu-id="6439a-650">15</span></span></td>
<td><span data-ttu-id="6439a-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6439a-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6439a-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6439a-652">470.08</span></span></td>
<td><span data-ttu-id="6439a-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6439a-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="6439a-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="6439a-655">Journal</span></span></th>
<th><span data-ttu-id="6439a-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="6439a-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6439a-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="6439a-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6439a-658">Version</span><span class="sxs-lookup"><span data-stu-id="6439a-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-659">00004</span><span class="sxs-lookup"><span data-stu-id="6439a-659">00004</span></span></td>
<td><span data-ttu-id="6439a-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="6439a-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6439a-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="6439a-661">Fiscal</span></span></td>
<td><span data-ttu-id="6439a-662">2017</span><span class="sxs-lookup"><span data-stu-id="6439a-662">2017</span></span></td>
<td><span data-ttu-id="6439a-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="6439a-663">Period 1</span></span></td>
<td><span data-ttu-id="6439a-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="6439a-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6439a-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="6439a-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6439a-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-668">Cost element</span></span></th>
<th><span data-ttu-id="6439a-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-672">CC001</span></span></td>
<td><span data-ttu-id="6439a-673">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-673">HR</span></span></td>
<td><span data-ttu-id="6439a-674">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-674">10001</span></span></td>
<td><span data-ttu-id="6439a-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-675">Electricity</span></span></td>
<td><span data-ttu-id="6439a-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-677">500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-679">CC001</span></span></td>
<td><span data-ttu-id="6439a-680">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-680">HR</span></span></td>
<td><span data-ttu-id="6439a-681">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-681">10001</span></span></td>
<td><span data-ttu-id="6439a-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-682">Electricity</span></span></td>
<td><span data-ttu-id="6439a-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-683">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6439a-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-686">CC002</span></span></td>
<td><span data-ttu-id="6439a-687">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-687">Finance</span></span></td>
<td><span data-ttu-id="6439a-688">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-688">10001</span></span></td>
<td><span data-ttu-id="6439a-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-689">Electricity</span></span></td>
<td><span data-ttu-id="6439a-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6439a-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-693">CC002</span></span></td>
<td><span data-ttu-id="6439a-694">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-694">Finance</span></span></td>
<td><span data-ttu-id="6439a-695">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-695">10001</span></span></td>
<td><span data-ttu-id="6439a-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-696">Electricity</span></span></td>
<td><span data-ttu-id="6439a-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-697">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6439a-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-700">CC003</span></span></td>
<td><span data-ttu-id="6439a-701">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-701">Assembly</span></span></td>
<td><span data-ttu-id="6439a-702">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-702">10001</span></span></td>
<td><span data-ttu-id="6439a-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-703">Electricity</span></span></td>
<td><span data-ttu-id="6439a-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6439a-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-707">CC003</span></span></td>
<td><span data-ttu-id="6439a-708">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-708">Assembly</span></span></td>
<td><span data-ttu-id="6439a-709">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-709">10001</span></span></td>
<td><span data-ttu-id="6439a-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-710">Electricity</span></span></td>
<td><span data-ttu-id="6439a-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-711">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6439a-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-714">CC003</span></span></td>
<td><span data-ttu-id="6439a-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-715">Packaging</span></span></td>
<td><span data-ttu-id="6439a-716">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-716">10001</span></span></td>
<td><span data-ttu-id="6439a-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-717">Electricity</span></span></td>
<td><span data-ttu-id="6439a-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6439a-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-721">CC003</span></span></td>
<td><span data-ttu-id="6439a-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-722">Packaging</span></span></td>
<td><span data-ttu-id="6439a-723">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-723">10001</span></span></td>
<td><span data-ttu-id="6439a-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-724">Electricity</span></span></td>
<td><span data-ttu-id="6439a-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-725">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6439a-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-728">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-729">Product 1</span></span></td>
<td><span data-ttu-id="6439a-730">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-730">10001</span></span></td>
<td><span data-ttu-id="6439a-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-731">Electricity</span></span></td>
<td><span data-ttu-id="6439a-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6439a-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-735">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-736">Product 1</span></span></td>
<td><span data-ttu-id="6439a-737">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-737">10001</span></span></td>
<td><span data-ttu-id="6439a-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-738">Electricity</span></span></td>
<td><span data-ttu-id="6439a-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-739">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6439a-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-742">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-743">Product 1</span></span></td>
<td><span data-ttu-id="6439a-744">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-744">10001</span></span></td>
<td><span data-ttu-id="6439a-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-745">Electricity</span></span></td>
<td><span data-ttu-id="6439a-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6439a-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6439a-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-749">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-750">Product 1</span></span></td>
<td><span data-ttu-id="6439a-751">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-751">10001</span></span></td>
<td><span data-ttu-id="6439a-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-752">Electricity</span></span></td>
<td><span data-ttu-id="6439a-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-753">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6439a-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6439a-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="6439a-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6439a-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6439a-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-757">Cost element</span></span></th>
<th><span data-ttu-id="6439a-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6439a-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="6439a-759">Amount</span></span></th>
<th><span data-ttu-id="6439a-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="6439a-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6439a-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-761">CC001</span></span></td>
<td><span data-ttu-id="6439a-762">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-762">HR</span></span></td>
<td><span data-ttu-id="6439a-763">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-763">10001</span></span></td>
<td><span data-ttu-id="6439a-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-764">Electricity</span></span></td>
<td><span data-ttu-id="6439a-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="6439a-766">-500.00</span></span></td>
<td><span data-ttu-id="6439a-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-768">CC002</span></span></td>
<td><span data-ttu-id="6439a-769">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-769">Finance</span></span></td>
<td><span data-ttu-id="6439a-770">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-770">10001</span></span></td>
<td><span data-ttu-id="6439a-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-771">Electricity</span></span></td>
<td><span data-ttu-id="6439a-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6439a-773">175.00</span></span></td>
<td><span data-ttu-id="6439a-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-775">CC003</span></span></td>
<td><span data-ttu-id="6439a-776">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-776">Assembly</span></span></td>
<td><span data-ttu-id="6439a-777">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-777">10001</span></span></td>
<td><span data-ttu-id="6439a-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-778">Electricity</span></span></td>
<td><span data-ttu-id="6439a-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6439a-780">275.00</span></span></td>
<td><span data-ttu-id="6439a-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-782">CC004</span></span></td>
<td><span data-ttu-id="6439a-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-783">Packaging</span></span></td>
<td><span data-ttu-id="6439a-784">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-784">10001</span></span></td>
<td><span data-ttu-id="6439a-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-785">Electricity</span></span></td>
<td><span data-ttu-id="6439a-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6439a-787">50,00</span></span></td>
<td><span data-ttu-id="6439a-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-789">CC001</span></span></td>
<td><span data-ttu-id="6439a-790">Personale</span><span class="sxs-lookup"><span data-stu-id="6439a-790">HR</span></span></td>
<td><span data-ttu-id="6439a-791">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-791">10001</span></span></td>
<td><span data-ttu-id="6439a-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-792">Electricity</span></span></td>
<td><span data-ttu-id="6439a-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-793">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="6439a-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6439a-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-796">CC002</span></span></td>
<td><span data-ttu-id="6439a-797">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-797">Finance</span></span></td>
<td><span data-ttu-id="6439a-798">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-798">10001</span></span></td>
<td><span data-ttu-id="6439a-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-799">Electricity</span></span></td>
<td><span data-ttu-id="6439a-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-800">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6439a-801">436.00</span></span></td>
<td><span data-ttu-id="6439a-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-803">CC003</span></span></td>
<td><span data-ttu-id="6439a-804">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-804">Assembly</span></span></td>
<td><span data-ttu-id="6439a-805">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-805">10001</span></span></td>
<td><span data-ttu-id="6439a-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-806">Electricity</span></span></td>
<td><span data-ttu-id="6439a-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-807">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6439a-808">685.14</span></span></td>
<td><span data-ttu-id="6439a-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-810">CC004</span></span></td>
<td><span data-ttu-id="6439a-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-811">Packaging</span></span></td>
<td><span data-ttu-id="6439a-812">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-812">10001</span></span></td>
<td><span data-ttu-id="6439a-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-813">Electricity</span></span></td>
<td><span data-ttu-id="6439a-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-814">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6439a-815">124.57</span></span></td>
<td><span data-ttu-id="6439a-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-817">CC002</span></span></td>
<td><span data-ttu-id="6439a-818">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-818">Finance</span></span></td>
<td><span data-ttu-id="6439a-819">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-819">10001</span></span></td>
<td><span data-ttu-id="6439a-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-820">Electricity</span></span></td>
<td><span data-ttu-id="6439a-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="6439a-822">-675.00</span></span></td>
<td><span data-ttu-id="6439a-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-824">CC003</span></span></td>
<td><span data-ttu-id="6439a-825">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-825">Assembly</span></span></td>
<td><span data-ttu-id="6439a-826">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-826">10001</span></span></td>
<td><span data-ttu-id="6439a-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-827">Electricity</span></span></td>
<td><span data-ttu-id="6439a-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6439a-829">438.75</span></span></td>
<td><span data-ttu-id="6439a-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-831">CC004</span></span></td>
<td><span data-ttu-id="6439a-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-832">Packaging</span></span></td>
<td><span data-ttu-id="6439a-833">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-833">10001</span></span></td>
<td><span data-ttu-id="6439a-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-834">Electricity</span></span></td>
<td><span data-ttu-id="6439a-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6439a-836">236.25</span></span></td>
<td><span data-ttu-id="6439a-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-838">CC002</span></span></td>
<td><span data-ttu-id="6439a-839">Finans</span><span class="sxs-lookup"><span data-stu-id="6439a-839">Finance</span></span></td>
<td><span data-ttu-id="6439a-840">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-840">10001</span></span></td>
<td><span data-ttu-id="6439a-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-841">Electricity</span></span></td>
<td><span data-ttu-id="6439a-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-842">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="6439a-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6439a-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-845">CC003</span></span></td>
<td><span data-ttu-id="6439a-846">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-846">Assembly</span></span></td>
<td><span data-ttu-id="6439a-847">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-847">10001</span></span></td>
<td><span data-ttu-id="6439a-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-848">Electricity</span></span></td>
<td><span data-ttu-id="6439a-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-849">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6439a-850">5,297.69</span></span></td>
<td><span data-ttu-id="6439a-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-852">CC004</span></span></td>
<td><span data-ttu-id="6439a-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="6439a-853">Packaging</span></span></td>
<td><span data-ttu-id="6439a-854">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-854">10001</span></span></td>
<td><span data-ttu-id="6439a-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-855">Electricity</span></span></td>
<td><span data-ttu-id="6439a-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-856">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6439a-857">2,852.60</span></span></td>
<td><span data-ttu-id="6439a-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-859">CC003</span></span></td>
<td><span data-ttu-id="6439a-860">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-860">Assembly</span></span></td>
<td><span data-ttu-id="6439a-861">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-861">10001</span></span></td>
<td><span data-ttu-id="6439a-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-862">Electricity</span></span></td>
<td><span data-ttu-id="6439a-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="6439a-864">-713.75</span></span></td>
<td><span data-ttu-id="6439a-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-866">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-867">Product 1</span></span></td>
<td><span data-ttu-id="6439a-868">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-868">10001</span></span></td>
<td><span data-ttu-id="6439a-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-869">Electricity</span></span></td>
<td><span data-ttu-id="6439a-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6439a-871">535.31</span></span></td>
<td><span data-ttu-id="6439a-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-873">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-874">Product 2</span></span></td>
<td><span data-ttu-id="6439a-875">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-875">10001</span></span></td>
<td><span data-ttu-id="6439a-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-876">Electricity</span></span></td>
<td><span data-ttu-id="6439a-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6439a-878">178.44</span></span></td>
<td><span data-ttu-id="6439a-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-880">CC003</span></span></td>
<td><span data-ttu-id="6439a-881">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-881">Assembly</span></span></td>
<td><span data-ttu-id="6439a-882">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-882">10001</span></span></td>
<td><span data-ttu-id="6439a-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-883">Electricity</span></span></td>
<td><span data-ttu-id="6439a-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-884">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="6439a-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6439a-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-887">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-888">Product 1</span></span></td>
<td><span data-ttu-id="6439a-889">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-889">10001</span></span></td>
<td><span data-ttu-id="6439a-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-890">Electricity</span></span></td>
<td><span data-ttu-id="6439a-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-891">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6439a-892">4,487.12</span></span></td>
<td><span data-ttu-id="6439a-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-894">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-895">Product 2</span></span></td>
<td><span data-ttu-id="6439a-896">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-896">10001</span></span></td>
<td><span data-ttu-id="6439a-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-897">Electricity</span></span></td>
<td><span data-ttu-id="6439a-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-898">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6439a-899">1,495.71</span></span></td>
<td><span data-ttu-id="6439a-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-901">CC003</span></span></td>
<td><span data-ttu-id="6439a-902">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-902">Assembly</span></span></td>
<td><span data-ttu-id="6439a-903">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-903">10001</span></span></td>
<td><span data-ttu-id="6439a-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-904">Electricity</span></span></td>
<td><span data-ttu-id="6439a-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="6439a-906">-286.25</span></span></td>
<td><span data-ttu-id="6439a-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-908">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-909">Product 1</span></span></td>
<td><span data-ttu-id="6439a-910">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-910">10001</span></span></td>
<td><span data-ttu-id="6439a-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-911">Electricity</span></span></td>
<td><span data-ttu-id="6439a-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6439a-913">241.05</span></span></td>
<td><span data-ttu-id="6439a-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-915">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-916">Product 2</span></span></td>
<td><span data-ttu-id="6439a-917">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-917">10001</span></span></td>
<td><span data-ttu-id="6439a-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-918">Electricity</span></span></td>
<td><span data-ttu-id="6439a-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6439a-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6439a-920">45.20</span></span></td>
<td><span data-ttu-id="6439a-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-922">CC003</span></span></td>
<td><span data-ttu-id="6439a-923">Samling</span><span class="sxs-lookup"><span data-stu-id="6439a-923">Assembly</span></span></td>
<td><span data-ttu-id="6439a-924">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-924">10001</span></span></td>
<td><span data-ttu-id="6439a-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-925">Electricity</span></span></td>
<td><span data-ttu-id="6439a-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-926">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="6439a-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6439a-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-929">Prod 1</span></span></td>
<td><span data-ttu-id="6439a-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="6439a-930">Product 1</span></span></td>
<td><span data-ttu-id="6439a-931">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-931">10001</span></span></td>
<td><span data-ttu-id="6439a-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-932">Electricity</span></span></td>
<td><span data-ttu-id="6439a-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-933">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6439a-934">2,507.09</span></span></td>
<td><span data-ttu-id="6439a-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6439a-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-936">Prod 2</span></span></td>
<td><span data-ttu-id="6439a-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="6439a-937">Product 2</span></span></td>
<td><span data-ttu-id="6439a-938">10001</span><span class="sxs-lookup"><span data-stu-id="6439a-938">10001</span></span></td>
<td><span data-ttu-id="6439a-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-939">Electricity</span></span></td>
<td><span data-ttu-id="6439a-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-940">Variable cost</span></span></td>
<td><span data-ttu-id="6439a-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6439a-941">470.08</span></span></td>
<td><span data-ttu-id="6439a-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="6439a-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6439a-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="6439a-943">Conclusion</span></span>
<span data-ttu-id="6439a-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="6439a-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6439a-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="6439a-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6439a-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="6439a-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6439a-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="6439a-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6439a-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="6439a-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6439a-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="6439a-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6439a-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="6439a-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6439a-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6439a-951">CC099</span></span></th>
<th><span data-ttu-id="6439a-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6439a-952">CC001</span></span></th>
<th><span data-ttu-id="6439a-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6439a-953">CC002</span></span></th>
<th><span data-ttu-id="6439a-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6439a-954">CC003</span></span></th>
<th><span data-ttu-id="6439a-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6439a-955">CC004</span></span></th>
<th><span data-ttu-id="6439a-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6439a-956">Proj 1</span></span></th>
<th><span data-ttu-id="6439a-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6439a-957">Proj 2</span></span></th>
<th><span data-ttu-id="6439a-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6439a-958">Prod 1</span></span></th>
<th><span data-ttu-id="6439a-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6439a-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6439a-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="6439a-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6439a-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6439a-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="6439a-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-971">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6439a-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-973">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-974">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-975">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-976">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-977">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6439a-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6439a-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6439a-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6439a-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="6439a-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-982">000</span><span class="sxs-lookup"><span data-stu-id="6439a-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-983">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-984">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-985">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-986">0,00</span><span class="sxs-lookup"><span data-stu-id="6439a-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-987">30,00</span><span class="sxs-lookup"><span data-stu-id="6439a-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-988">10,00</span><span class="sxs-lookup"><span data-stu-id="6439a-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6439a-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6439a-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6439a-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6439a-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6439a-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="6439a-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6439a-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="6439a-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6439a-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="6439a-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6439a-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="6439a-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6439a-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="6439a-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



