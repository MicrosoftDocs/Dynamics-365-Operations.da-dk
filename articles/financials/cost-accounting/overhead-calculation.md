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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "335111"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e5132-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5132-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5132-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="e5132-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="e5132-105">Term definition</span></span>
---------------

<span data-ttu-id="e5132-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="e5132-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e5132-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="e5132-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e5132-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="e5132-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e5132-109">Leje</span><span class="sxs-lookup"><span data-stu-id="e5132-109">Rent</span></span>
-   <span data-ttu-id="e5132-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-110">Electricity</span></span>
-   <span data-ttu-id="e5132-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="e5132-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e5132-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-112">Overhead calculation overview</span></span>
<span data-ttu-id="e5132-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e5132-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e5132-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="e5132-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e5132-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="e5132-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e5132-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e5132-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e5132-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e5132-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e5132-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="e5132-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e5132-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="e5132-119">Version type</span></span>
-   <span data-ttu-id="e5132-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="e5132-120">Date and time</span></span>
-   <span data-ttu-id="e5132-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="e5132-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e5132-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e5132-122">Fiscal year</span></span>
-   <span data-ttu-id="e5132-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="e5132-123">Fiscal period</span></span>

<span data-ttu-id="e5132-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="e5132-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e5132-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="e5132-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e5132-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="e5132-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e5132-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="e5132-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e5132-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="e5132-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e5132-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="e5132-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e5132-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="e5132-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e5132-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e5132-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e5132-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e5132-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="e5132-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e5132-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="e5132-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e5132-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="e5132-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e5132-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="e5132-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e5132-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e5132-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="e5132-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="e5132-140">Main account</span></span></th>
<th><span data-ttu-id="e5132-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="e5132-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e5132-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-143">CC099</span></span></td>
<td><span data-ttu-id="e5132-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-144">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-145">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-145">10001</span></span></td>
<td><span data-ttu-id="e5132-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-146">Electricity</span></span></td>
<td><span data-ttu-id="e5132-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e5132-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="e5132-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e5132-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="e5132-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e5132-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="e5132-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e5132-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="e5132-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e5132-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="e5132-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e5132-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="e5132-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e5132-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="e5132-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e5132-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="e5132-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e5132-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e5132-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="e5132-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e5132-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="e5132-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e5132-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-160">Journal</span></span></th>
<th><span data-ttu-id="e5132-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e5132-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e5132-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e5132-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e5132-163">Version</span><span class="sxs-lookup"><span data-stu-id="e5132-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-164">00001</span><span class="sxs-lookup"><span data-stu-id="e5132-164">00001</span></span></td>
<td><span data-ttu-id="e5132-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e5132-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e5132-166">Fiscal</span></span></td>
<td><span data-ttu-id="e5132-167">2017</span><span class="sxs-lookup"><span data-stu-id="e5132-167">2017</span></span></td>
<td><span data-ttu-id="e5132-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e5132-168">Period 1</span></span></td>
<td><span data-ttu-id="e5132-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e5132-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e5132-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="e5132-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-173">Cost element</span></span></th>
<th><span data-ttu-id="e5132-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e5132-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-177">CC099</span></span></td>
<td><span data-ttu-id="e5132-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-178">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-179">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-179">10001</span></span></td>
<td><span data-ttu-id="e5132-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-180">Electricity</span></span></td>
<td><span data-ttu-id="e5132-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e5132-181">Unclassified</span></span></td>
<td><span data-ttu-id="e5132-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e5132-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e5132-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-185">Cost element</span></span></th>
<th><span data-ttu-id="e5132-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-187">Amount</span></span></th>
<th><span data-ttu-id="e5132-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-189">CC099</span></span></td>
<td><span data-ttu-id="e5132-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-190">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-191">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-191">10001</span></span></td>
<td><span data-ttu-id="e5132-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-192">Electricity</span></span></td>
<td><span data-ttu-id="e5132-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e5132-193">Unclassified</span></span></td>
<td><span data-ttu-id="e5132-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-194">10,000.00</span></span></td>
<td><span data-ttu-id="e5132-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-196">CC099</span></span></td>
<td><span data-ttu-id="e5132-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-197">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-198">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-198">10001</span></span></td>
<td><span data-ttu-id="e5132-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-199">Electricity</span></span></td>
<td><span data-ttu-id="e5132-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e5132-200">Unclassified</span></span></td>
<td><span data-ttu-id="e5132-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e5132-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-203">CC099</span></span></td>
<td><span data-ttu-id="e5132-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-204">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-205">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-205">10001</span></span></td>
<td><span data-ttu-id="e5132-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-206">Electricity</span></span></td>
<td><span data-ttu-id="e5132-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-208">1,000.00</span></span></td>
<td><span data-ttu-id="e5132-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-210">CC099</span></span></td>
<td><span data-ttu-id="e5132-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-211">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-212">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-212">10001</span></span></td>
<td><span data-ttu-id="e5132-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-213">Electricity</span></span></td>
<td><span data-ttu-id="e5132-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-214">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-215">9,000.00</span></span></td>
<td><span data-ttu-id="e5132-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e5132-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e5132-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="e5132-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e5132-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e5132-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="e5132-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e5132-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="e5132-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e5132-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="e5132-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e5132-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="e5132-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e5132-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e5132-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="e5132-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e5132-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="e5132-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e5132-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-228">Cost object</span></span></th>
<th><span data-ttu-id="e5132-229">KWh</span><span class="sxs-lookup"><span data-stu-id="e5132-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-230">CC001</span></span></td>
<td><span data-ttu-id="e5132-231">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-231">HR</span></span></td>
<td><span data-ttu-id="e5132-232">1.000</span><span class="sxs-lookup"><span data-stu-id="e5132-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-233">CC002</span></span></td>
<td><span data-ttu-id="e5132-234">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-234">Finance</span></span></td>
<td><span data-ttu-id="e5132-235">6.000</span><span class="sxs-lookup"><span data-stu-id="e5132-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-236">CC003</span></span></td>
<td><span data-ttu-id="e5132-237">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-237">Assembly</span></span></td>
<td><span data-ttu-id="e5132-238">0</span><span class="sxs-lookup"><span data-stu-id="e5132-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5132-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-240">Cost object</span></span></th>
<th><span data-ttu-id="e5132-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-241">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-244">CC001</span></span></td>
<td><span data-ttu-id="e5132-245">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-245">HR</span></span></td>
<td><span data-ttu-id="e5132-246">1.000</span><span class="sxs-lookup"><span data-stu-id="e5132-246">1,000</span></span></td>
<td><span data-ttu-id="e5132-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e5132-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e5132-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-249">CC002</span></span></td>
<td><span data-ttu-id="e5132-250">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-250">Finance</span></span></td>
<td><span data-ttu-id="e5132-251">6.000</span><span class="sxs-lookup"><span data-stu-id="e5132-251">6,000</span></span></td>
<td><span data-ttu-id="e5132-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e5132-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e5132-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-254">CC003</span></span></td>
<td><span data-ttu-id="e5132-255">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-255">Assembly</span></span></td>
<td><span data-ttu-id="e5132-256">0</span><span class="sxs-lookup"><span data-stu-id="e5132-256">0</span></span></td>
<td><span data-ttu-id="e5132-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e5132-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="e5132-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e5132-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5132-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-261">Cost object</span></span></th>
<th><span data-ttu-id="e5132-262">Formel</span><span class="sxs-lookup"><span data-stu-id="e5132-262">Formula</span></span></th>
<th><span data-ttu-id="e5132-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-263">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-266">CC001</span></span></td>
<td><span data-ttu-id="e5132-267">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-267">HR</span></span></td>
<td><span data-ttu-id="e5132-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e5132-269">1</span><span class="sxs-lookup"><span data-stu-id="e5132-269">1</span></span></td>
<td><span data-ttu-id="e5132-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e5132-271">500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-272">CC002</span></span></td>
<td><span data-ttu-id="e5132-273">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-273">Finance</span></span></td>
<td><span data-ttu-id="e5132-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e5132-275">1</span><span class="sxs-lookup"><span data-stu-id="e5132-275">1</span></span></td>
<td><span data-ttu-id="e5132-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e5132-277">500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-278">CC003</span></span></td>
<td><span data-ttu-id="e5132-279">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-279">Assembly</span></span></td>
<td><span data-ttu-id="e5132-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e5132-281">0</span><span class="sxs-lookup"><span data-stu-id="e5132-281">0</span></span></td>
<td><span data-ttu-id="e5132-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e5132-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e5132-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-285">Journal</span></span></th>
<th><span data-ttu-id="e5132-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e5132-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e5132-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e5132-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e5132-288">Version</span><span class="sxs-lookup"><span data-stu-id="e5132-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-289">00002</span><span class="sxs-lookup"><span data-stu-id="e5132-289">00002</span></span></td>
<td><span data-ttu-id="e5132-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="e5132-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e5132-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e5132-291">Fiscal</span></span></td>
<td><span data-ttu-id="e5132-292">2017</span><span class="sxs-lookup"><span data-stu-id="e5132-292">2017</span></span></td>
<td><span data-ttu-id="e5132-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e5132-293">Period 1</span></span></td>
<td><span data-ttu-id="e5132-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e5132-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e5132-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="e5132-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-298">Cost element</span></span></th>
<th><span data-ttu-id="e5132-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-302">CC099</span></span></td>
<td><span data-ttu-id="e5132-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-303">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-304">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-304">10001</span></span></td>
<td><span data-ttu-id="e5132-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-305">Electricity</span></span></td>
<td><span data-ttu-id="e5132-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-309">CC099</span></span></td>
<td><span data-ttu-id="e5132-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-310">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-311">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-311">10001</span></span></td>
<td><span data-ttu-id="e5132-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-312">Electricity</span></span></td>
<td><span data-ttu-id="e5132-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-313">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e5132-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e5132-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-317">Cost element</span></span></th>
<th><span data-ttu-id="e5132-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-319">Amount</span></span></th>
<th><span data-ttu-id="e5132-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-321">CC099</span></span></td>
<td><span data-ttu-id="e5132-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-322">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-323">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-323">10001</span></span></td>
<td><span data-ttu-id="e5132-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-324">Electricity</span></span></td>
<td><span data-ttu-id="e5132-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e5132-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-328">CC001</span></span></td>
<td><span data-ttu-id="e5132-329">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-329">HR</span></span></td>
<td><span data-ttu-id="e5132-330">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-330">10001</span></span></td>
<td><span data-ttu-id="e5132-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-331">Electricity</span></span></td>
<td><span data-ttu-id="e5132-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-333">500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-333">500.00</span></span></td>
<td><span data-ttu-id="e5132-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-335">CC002</span></span></td>
<td><span data-ttu-id="e5132-336">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-336">Finance</span></span></td>
<td><span data-ttu-id="e5132-337">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-337">10001</span></span></td>
<td><span data-ttu-id="e5132-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-338">Electricity</span></span></td>
<td><span data-ttu-id="e5132-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-340">500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-340">500.00</span></span></td>
<td><span data-ttu-id="e5132-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-342">CC099</span></span></td>
<td><span data-ttu-id="e5132-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="e5132-343">Default cost center</span></span></td>
<td><span data-ttu-id="e5132-344">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-344">10001</span></span></td>
<td><span data-ttu-id="e5132-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-345">Electricity</span></span></td>
<td><span data-ttu-id="e5132-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-346">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="e5132-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e5132-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-349">CC001</span></span></td>
<td><span data-ttu-id="e5132-350">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-350">HR</span></span></td>
<td><span data-ttu-id="e5132-351">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-351">10001</span></span></td>
<td><span data-ttu-id="e5132-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-352">Electricity</span></span></td>
<td><span data-ttu-id="e5132-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-353">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e5132-354">1,285.71</span></span></td>
<td><span data-ttu-id="e5132-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-356">CC002</span></span></td>
<td><span data-ttu-id="e5132-357">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-357">Finance</span></span></td>
<td><span data-ttu-id="e5132-358">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-358">10001</span></span></td>
<td><span data-ttu-id="e5132-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-359">Electricity</span></span></td>
<td><span data-ttu-id="e5132-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-360">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e5132-361">7,714.29</span></span></td>
<td><span data-ttu-id="e5132-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e5132-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e5132-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="e5132-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e5132-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e5132-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e5132-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="e5132-367">Define the overhead rate</span></span>

<span data-ttu-id="e5132-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e5132-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e5132-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-370">Cost object</span></span></th>
<th><span data-ttu-id="e5132-371">Timer</span><span class="sxs-lookup"><span data-stu-id="e5132-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-372">Proj 1</span></span></td>
<td><span data-ttu-id="e5132-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-373">Project 1</span></span></td>
<td><span data-ttu-id="e5132-374">3</span><span class="sxs-lookup"><span data-stu-id="e5132-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-375">Proj 2</span></span></td>
<td><span data-ttu-id="e5132-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-376">Project 2</span></span></td>
<td><span data-ttu-id="e5132-377">1</span><span class="sxs-lookup"><span data-stu-id="e5132-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="e5132-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-379">Cost object</span></span></th>
<th><span data-ttu-id="e5132-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-380">Cost element</span></span></th>
<th><span data-ttu-id="e5132-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="e5132-382">Units</span></span></th>
<th><span data-ttu-id="e5132-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="e5132-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-384">CC001</span></span></td>
<td><span data-ttu-id="e5132-385">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-385">HR</span></span></td>
<td><span data-ttu-id="e5132-386">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-386">10001</span></span></td>
<td><span data-ttu-id="e5132-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-387">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-388">1</span><span class="sxs-lookup"><span data-stu-id="e5132-388">1</span></span></td>
<td><span data-ttu-id="e5132-389">10</span><span class="sxs-lookup"><span data-stu-id="e5132-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-391">Cost object</span></span></th>
<th><span data-ttu-id="e5132-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-392">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-393">Cost element</span></span></th>
<th><span data-ttu-id="e5132-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-396">Proj 1</span></span></td>
<td><span data-ttu-id="e5132-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-397">Project 1</span></span></td>
<td><span data-ttu-id="e5132-398">3</span><span class="sxs-lookup"><span data-stu-id="e5132-398">3</span></span></td>
<td><span data-ttu-id="e5132-399">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-399">10001</span></span></td>
<td><span data-ttu-id="e5132-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e5132-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e5132-401">30,00</span><span class="sxs-lookup"><span data-stu-id="e5132-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-402">Proj 2</span></span></td>
<td><span data-ttu-id="e5132-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-403">Project 2</span></span></td>
<td><span data-ttu-id="e5132-404">1</span><span class="sxs-lookup"><span data-stu-id="e5132-404">1</span></span></td>
<td><span data-ttu-id="e5132-405">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-405">10001</span></span></td>
<td><span data-ttu-id="e5132-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e5132-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e5132-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e5132-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e5132-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-409">Journal</span></span></th>
<th><span data-ttu-id="e5132-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e5132-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e5132-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e5132-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e5132-412">Version</span><span class="sxs-lookup"><span data-stu-id="e5132-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-413">00003</span><span class="sxs-lookup"><span data-stu-id="e5132-413">00003</span></span></td>
<td><span data-ttu-id="e5132-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="e5132-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e5132-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e5132-415">Fiscal</span></span></td>
<td><span data-ttu-id="e5132-416">2017</span><span class="sxs-lookup"><span data-stu-id="e5132-416">2017</span></span></td>
<td><span data-ttu-id="e5132-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e5132-417">Period 1</span></span></td>
<td><span data-ttu-id="e5132-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e5132-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e5132-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="e5132-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-421">Cost object</span></span></th>
<th><span data-ttu-id="e5132-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-424">Proj 1</span></span></td>
<td><span data-ttu-id="e5132-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e5132-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e5132-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-428">Proj 2</span></span></td>
<td><span data-ttu-id="e5132-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e5132-430">1,00</span><span class="sxs-lookup"><span data-stu-id="e5132-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e5132-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e5132-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-433">Cost element</span></span></th>
<th><span data-ttu-id="e5132-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-435">Amount</span></span></th>
<th><span data-ttu-id="e5132-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e5132-437">CC0001</span></span></td>
<td><span data-ttu-id="e5132-438">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-438">HR</span></span></td>
<td><span data-ttu-id="e5132-439">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-439">10001</span></span></td>
<td><span data-ttu-id="e5132-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-440">Electricity</span></span></td>
<td><span data-ttu-id="e5132-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-441">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="e5132-442">-30.00</span></span></td>
<td><span data-ttu-id="e5132-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-444">Proj 1</span></span></td>
<td><span data-ttu-id="e5132-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e5132-446">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-446">10001</span></span></td>
<td><span data-ttu-id="e5132-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-447">Electricity</span></span></td>
<td><span data-ttu-id="e5132-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-448">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-449">30,00</span><span class="sxs-lookup"><span data-stu-id="e5132-449">30.00</span></span></td>
<td><span data-ttu-id="e5132-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-451">CC001</span></span></td>
<td><span data-ttu-id="e5132-452">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-452">HR</span></span></td>
<td><span data-ttu-id="e5132-453">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-453">10001</span></span></td>
<td><span data-ttu-id="e5132-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-454">Electricity</span></span></td>
<td><span data-ttu-id="e5132-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-455">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e5132-456">-10.00</span></span></td>
<td><span data-ttu-id="e5132-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-458">Proj 2</span></span></td>
<td><span data-ttu-id="e5132-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e5132-460">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-460">10001</span></span></td>
<td><span data-ttu-id="e5132-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-461">Electricity</span></span></td>
<td><span data-ttu-id="e5132-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-462">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-463">10.00</span><span class="sxs-lookup"><span data-stu-id="e5132-463">10.00</span></span></td>
<td><span data-ttu-id="e5132-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e5132-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e5132-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="e5132-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e5132-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e5132-468">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="e5132-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="e5132-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="e5132-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e5132-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="e5132-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e5132-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="e5132-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e5132-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="e5132-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e5132-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="e5132-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e5132-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e5132-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e5132-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="e5132-475">Define the cost allocation</span></span>

<span data-ttu-id="e5132-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5132-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e5132-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e5132-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e5132-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-479">Cost object</span></span></th>
<th><span data-ttu-id="e5132-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="e5132-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-481">CC002</span></span></td>
<td><span data-ttu-id="e5132-482">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-482">Finance</span></span></td>
<td><span data-ttu-id="e5132-483">35</span><span class="sxs-lookup"><span data-stu-id="e5132-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-484">CC003</span></span></td>
<td><span data-ttu-id="e5132-485">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-485">Assembly</span></span></td>
<td><span data-ttu-id="e5132-486">55</span><span class="sxs-lookup"><span data-stu-id="e5132-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-487">CC004</span></span></td>
<td><span data-ttu-id="e5132-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-488">Packaging</span></span></td>
<td><span data-ttu-id="e5132-489">10</span><span class="sxs-lookup"><span data-stu-id="e5132-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e5132-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e5132-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-492">Cost object</span></span></th>
<th><span data-ttu-id="e5132-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="e5132-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-494">CC003</span></span></td>
<td><span data-ttu-id="e5132-495">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-495">Assembly</span></span></td>
<td><span data-ttu-id="e5132-496">65</span><span class="sxs-lookup"><span data-stu-id="e5132-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-497">CC004</span></span></td>
<td><span data-ttu-id="e5132-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-498">Packaging</span></span></td>
<td><span data-ttu-id="e5132-499">35</span><span class="sxs-lookup"><span data-stu-id="e5132-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e5132-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e5132-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-502">Cost object</span></span></th>
<th><span data-ttu-id="e5132-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="e5132-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-504">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-505">Product 1</span></span></td>
<td><span data-ttu-id="e5132-506">60</span><span class="sxs-lookup"><span data-stu-id="e5132-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-507">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-508">Product 2</span></span></td>
<td><span data-ttu-id="e5132-509">20</span><span class="sxs-lookup"><span data-stu-id="e5132-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e5132-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="e5132-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-512">Cost object</span></span></th>
<th><span data-ttu-id="e5132-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="e5132-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-514">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-515">Product 1</span></span></td>
<td><span data-ttu-id="e5132-516">80</span><span class="sxs-lookup"><span data-stu-id="e5132-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-517">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-518">Product 2</span></span></td>
<td><span data-ttu-id="e5132-519">september</span><span class="sxs-lookup"><span data-stu-id="e5132-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e5132-520">I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="e5132-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e5132-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e5132-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e5132-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e5132-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-523">Cost object</span></span></th>
<th><span data-ttu-id="e5132-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-524">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-526">Amount</span></span></th>
<th><span data-ttu-id="e5132-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-528">CC002</span></span></td>
<td><span data-ttu-id="e5132-529">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-529">Finance</span></span></td>
<td><span data-ttu-id="e5132-530">35</span><span class="sxs-lookup"><span data-stu-id="e5132-530">35</span></span></td>
<td><span data-ttu-id="e5132-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e5132-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e5132-532">175.00</span></span></td>
<td><span data-ttu-id="e5132-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-534">CC003</span></span></td>
<td><span data-ttu-id="e5132-535">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-535">Assembly</span></span></td>
<td><span data-ttu-id="e5132-536">55</span><span class="sxs-lookup"><span data-stu-id="e5132-536">55</span></span></td>
<td><span data-ttu-id="e5132-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e5132-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e5132-538">275.00</span></span></td>
<td><span data-ttu-id="e5132-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-540">CC004</span></span></td>
<td><span data-ttu-id="e5132-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-541">Packaging</span></span></td>
<td><span data-ttu-id="e5132-542">10</span><span class="sxs-lookup"><span data-stu-id="e5132-542">10</span></span></td>
<td><span data-ttu-id="e5132-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e5132-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e5132-544">50.00</span></span></td>
<td><span data-ttu-id="e5132-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-546">CC002</span></span></td>
<td><span data-ttu-id="e5132-547">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-547">Finance</span></span></td>
<td><span data-ttu-id="e5132-548">35</span><span class="sxs-lookup"><span data-stu-id="e5132-548">35</span></span></td>
<td><span data-ttu-id="e5132-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e5132-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e5132-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e5132-550">436.00</span></span></td>
<td><span data-ttu-id="e5132-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-552">CC003</span></span></td>
<td><span data-ttu-id="e5132-553">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-553">Assembly</span></span></td>
<td><span data-ttu-id="e5132-554">55</span><span class="sxs-lookup"><span data-stu-id="e5132-554">55</span></span></td>
<td><span data-ttu-id="e5132-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e5132-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e5132-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e5132-556">685.14</span></span></td>
<td><span data-ttu-id="e5132-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-558">CC004</span></span></td>
<td><span data-ttu-id="e5132-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-559">Packaging</span></span></td>
<td><span data-ttu-id="e5132-560">10</span><span class="sxs-lookup"><span data-stu-id="e5132-560">10</span></span></td>
<td><span data-ttu-id="e5132-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e5132-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e5132-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e5132-562">124.57</span></span></td>
<td><span data-ttu-id="e5132-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e5132-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-565">Cost object</span></span></th>
<th><span data-ttu-id="e5132-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-566">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-568">Amount</span></span></th>
<th><span data-ttu-id="e5132-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-570">CC003</span></span></td>
<td><span data-ttu-id="e5132-571">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-571">Assembly</span></span></td>
<td><span data-ttu-id="e5132-572">65</span><span class="sxs-lookup"><span data-stu-id="e5132-572">65</span></span></td>
<td><span data-ttu-id="e5132-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e5132-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e5132-574">438.75</span></span></td>
<td><span data-ttu-id="e5132-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-576">CC004</span></span></td>
<td><span data-ttu-id="e5132-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-577">Packaging</span></span></td>
<td><span data-ttu-id="e5132-578">35</span><span class="sxs-lookup"><span data-stu-id="e5132-578">35</span></span></td>
<td><span data-ttu-id="e5132-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e5132-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e5132-580">236.25</span></span></td>
<td><span data-ttu-id="e5132-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-582">CC003</span></span></td>
<td><span data-ttu-id="e5132-583">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-583">Assembly</span></span></td>
<td><span data-ttu-id="e5132-584">65</span><span class="sxs-lookup"><span data-stu-id="e5132-584">65</span></span></td>
<td><span data-ttu-id="e5132-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e5132-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e5132-586">5,297.69</span></span></td>
<td><span data-ttu-id="e5132-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-588">CC004</span></span></td>
<td><span data-ttu-id="e5132-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-589">Packaging</span></span></td>
<td><span data-ttu-id="e5132-590">35</span><span class="sxs-lookup"><span data-stu-id="e5132-590">35</span></span></td>
<td><span data-ttu-id="e5132-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e5132-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e5132-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e5132-592">2,852.60</span></span></td>
<td><span data-ttu-id="e5132-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e5132-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-595">Cost object</span></span></th>
<th><span data-ttu-id="e5132-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-596">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-598">Amount</span></span></th>
<th><span data-ttu-id="e5132-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-600">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-601">Product 1</span></span></td>
<td><span data-ttu-id="e5132-602">60</span><span class="sxs-lookup"><span data-stu-id="e5132-602">60</span></span></td>
<td><span data-ttu-id="e5132-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e5132-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e5132-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e5132-604">535.31</span></span></td>
<td><span data-ttu-id="e5132-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-606">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-607">Product 2</span></span></td>
<td><span data-ttu-id="e5132-608">20</span><span class="sxs-lookup"><span data-stu-id="e5132-608">20</span></span></td>
<td><span data-ttu-id="e5132-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e5132-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e5132-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e5132-610">178.44</span></span></td>
<td><span data-ttu-id="e5132-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-612">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-613">Product 1</span></span></td>
<td><span data-ttu-id="e5132-614">60</span><span class="sxs-lookup"><span data-stu-id="e5132-614">60</span></span></td>
<td><span data-ttu-id="e5132-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e5132-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e5132-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e5132-616">4,487.12</span></span></td>
<td><span data-ttu-id="e5132-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-618">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-619">Product 2</span></span></td>
<td><span data-ttu-id="e5132-620">20</span><span class="sxs-lookup"><span data-stu-id="e5132-620">20</span></span></td>
<td><span data-ttu-id="e5132-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e5132-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e5132-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e5132-622">1,495.71</span></span></td>
<td><span data-ttu-id="e5132-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e5132-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="e5132-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-625">Cost object</span></span></th>
<th><span data-ttu-id="e5132-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="e5132-626">Magnitude</span></span></th>
<th><span data-ttu-id="e5132-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="e5132-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e5132-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-628">Amount</span></span></th>
<th><span data-ttu-id="e5132-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-630">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-631">Product 1</span></span></td>
<td><span data-ttu-id="e5132-632">80</span><span class="sxs-lookup"><span data-stu-id="e5132-632">80</span></span></td>
<td><span data-ttu-id="e5132-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e5132-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e5132-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e5132-634">241.05</span></span></td>
<td><span data-ttu-id="e5132-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-636">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-637">Product 2</span></span></td>
<td><span data-ttu-id="e5132-638">15</span><span class="sxs-lookup"><span data-stu-id="e5132-638">15</span></span></td>
<td><span data-ttu-id="e5132-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e5132-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e5132-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e5132-640">45.20</span></span></td>
<td><span data-ttu-id="e5132-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-642">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-643">Product 1</span></span></td>
<td><span data-ttu-id="e5132-644">80</span><span class="sxs-lookup"><span data-stu-id="e5132-644">80</span></span></td>
<td><span data-ttu-id="e5132-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e5132-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e5132-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e5132-646">2,507.09</span></span></td>
<td><span data-ttu-id="e5132-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-648">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-649">Product 2</span></span></td>
<td><span data-ttu-id="e5132-650">15</span><span class="sxs-lookup"><span data-stu-id="e5132-650">15</span></span></td>
<td><span data-ttu-id="e5132-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e5132-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e5132-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e5132-652">470.08</span></span></td>
<td><span data-ttu-id="e5132-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e5132-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="e5132-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="e5132-655">Journal</span></span></th>
<th><span data-ttu-id="e5132-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="e5132-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e5132-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="e5132-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e5132-658">Version</span><span class="sxs-lookup"><span data-stu-id="e5132-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-659">00004</span><span class="sxs-lookup"><span data-stu-id="e5132-659">00004</span></span></td>
<td><span data-ttu-id="e5132-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="e5132-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e5132-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="e5132-661">Fiscal</span></span></td>
<td><span data-ttu-id="e5132-662">2017</span><span class="sxs-lookup"><span data-stu-id="e5132-662">2017</span></span></td>
<td><span data-ttu-id="e5132-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="e5132-663">Period 1</span></span></td>
<td><span data-ttu-id="e5132-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="e5132-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e5132-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="e5132-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e5132-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-668">Cost element</span></span></th>
<th><span data-ttu-id="e5132-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-672">CC001</span></span></td>
<td><span data-ttu-id="e5132-673">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-673">HR</span></span></td>
<td><span data-ttu-id="e5132-674">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-674">10001</span></span></td>
<td><span data-ttu-id="e5132-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-675">Electricity</span></span></td>
<td><span data-ttu-id="e5132-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-677">500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-679">CC001</span></span></td>
<td><span data-ttu-id="e5132-680">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-680">HR</span></span></td>
<td><span data-ttu-id="e5132-681">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-681">10001</span></span></td>
<td><span data-ttu-id="e5132-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-682">Electricity</span></span></td>
<td><span data-ttu-id="e5132-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-683">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e5132-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-686">CC002</span></span></td>
<td><span data-ttu-id="e5132-687">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-687">Finance</span></span></td>
<td><span data-ttu-id="e5132-688">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-688">10001</span></span></td>
<td><span data-ttu-id="e5132-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-689">Electricity</span></span></td>
<td><span data-ttu-id="e5132-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e5132-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-693">CC002</span></span></td>
<td><span data-ttu-id="e5132-694">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-694">Finance</span></span></td>
<td><span data-ttu-id="e5132-695">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-695">10001</span></span></td>
<td><span data-ttu-id="e5132-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-696">Electricity</span></span></td>
<td><span data-ttu-id="e5132-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-697">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e5132-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-700">CC003</span></span></td>
<td><span data-ttu-id="e5132-701">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-701">Assembly</span></span></td>
<td><span data-ttu-id="e5132-702">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-702">10001</span></span></td>
<td><span data-ttu-id="e5132-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-703">Electricity</span></span></td>
<td><span data-ttu-id="e5132-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e5132-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-707">CC003</span></span></td>
<td><span data-ttu-id="e5132-708">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-708">Assembly</span></span></td>
<td><span data-ttu-id="e5132-709">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-709">10001</span></span></td>
<td><span data-ttu-id="e5132-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-710">Electricity</span></span></td>
<td><span data-ttu-id="e5132-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-711">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e5132-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-714">CC003</span></span></td>
<td><span data-ttu-id="e5132-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-715">Packaging</span></span></td>
<td><span data-ttu-id="e5132-716">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-716">10001</span></span></td>
<td><span data-ttu-id="e5132-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-717">Electricity</span></span></td>
<td><span data-ttu-id="e5132-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e5132-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-721">CC003</span></span></td>
<td><span data-ttu-id="e5132-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-722">Packaging</span></span></td>
<td><span data-ttu-id="e5132-723">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-723">10001</span></span></td>
<td><span data-ttu-id="e5132-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-724">Electricity</span></span></td>
<td><span data-ttu-id="e5132-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-725">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e5132-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-728">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-729">Product 1</span></span></td>
<td><span data-ttu-id="e5132-730">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-730">10001</span></span></td>
<td><span data-ttu-id="e5132-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-731">Electricity</span></span></td>
<td><span data-ttu-id="e5132-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e5132-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-735">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-736">Product 1</span></span></td>
<td><span data-ttu-id="e5132-737">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-737">10001</span></span></td>
<td><span data-ttu-id="e5132-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-738">Electricity</span></span></td>
<td><span data-ttu-id="e5132-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-739">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e5132-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-742">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-743">Product 1</span></span></td>
<td><span data-ttu-id="e5132-744">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-744">10001</span></span></td>
<td><span data-ttu-id="e5132-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-745">Electricity</span></span></td>
<td><span data-ttu-id="e5132-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e5132-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e5132-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-749">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-750">Product 1</span></span></td>
<td><span data-ttu-id="e5132-751">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-751">10001</span></span></td>
<td><span data-ttu-id="e5132-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-752">Electricity</span></span></td>
<td><span data-ttu-id="e5132-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-753">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e5132-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e5132-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="e5132-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e5132-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e5132-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-757">Cost element</span></span></th>
<th><span data-ttu-id="e5132-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e5132-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="e5132-759">Amount</span></span></th>
<th><span data-ttu-id="e5132-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="e5132-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e5132-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-761">CC001</span></span></td>
<td><span data-ttu-id="e5132-762">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-762">HR</span></span></td>
<td><span data-ttu-id="e5132-763">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-763">10001</span></span></td>
<td><span data-ttu-id="e5132-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-764">Electricity</span></span></td>
<td><span data-ttu-id="e5132-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="e5132-766">-500.00</span></span></td>
<td><span data-ttu-id="e5132-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-768">CC002</span></span></td>
<td><span data-ttu-id="e5132-769">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-769">Finance</span></span></td>
<td><span data-ttu-id="e5132-770">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-770">10001</span></span></td>
<td><span data-ttu-id="e5132-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-771">Electricity</span></span></td>
<td><span data-ttu-id="e5132-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e5132-773">175.00</span></span></td>
<td><span data-ttu-id="e5132-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-775">CC003</span></span></td>
<td><span data-ttu-id="e5132-776">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-776">Assembly</span></span></td>
<td><span data-ttu-id="e5132-777">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-777">10001</span></span></td>
<td><span data-ttu-id="e5132-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-778">Electricity</span></span></td>
<td><span data-ttu-id="e5132-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e5132-780">275.00</span></span></td>
<td><span data-ttu-id="e5132-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-782">CC004</span></span></td>
<td><span data-ttu-id="e5132-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-783">Packaging</span></span></td>
<td><span data-ttu-id="e5132-784">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-784">10001</span></span></td>
<td><span data-ttu-id="e5132-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-785">Electricity</span></span></td>
<td><span data-ttu-id="e5132-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e5132-787">50,00</span></span></td>
<td><span data-ttu-id="e5132-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-789">CC001</span></span></td>
<td><span data-ttu-id="e5132-790">Personale</span><span class="sxs-lookup"><span data-stu-id="e5132-790">HR</span></span></td>
<td><span data-ttu-id="e5132-791">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-791">10001</span></span></td>
<td><span data-ttu-id="e5132-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-792">Electricity</span></span></td>
<td><span data-ttu-id="e5132-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-793">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="e5132-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e5132-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-796">CC002</span></span></td>
<td><span data-ttu-id="e5132-797">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-797">Finance</span></span></td>
<td><span data-ttu-id="e5132-798">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-798">10001</span></span></td>
<td><span data-ttu-id="e5132-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-799">Electricity</span></span></td>
<td><span data-ttu-id="e5132-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-800">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e5132-801">436.00</span></span></td>
<td><span data-ttu-id="e5132-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-803">CC003</span></span></td>
<td><span data-ttu-id="e5132-804">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-804">Assembly</span></span></td>
<td><span data-ttu-id="e5132-805">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-805">10001</span></span></td>
<td><span data-ttu-id="e5132-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-806">Electricity</span></span></td>
<td><span data-ttu-id="e5132-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-807">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e5132-808">685.14</span></span></td>
<td><span data-ttu-id="e5132-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-810">CC004</span></span></td>
<td><span data-ttu-id="e5132-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-811">Packaging</span></span></td>
<td><span data-ttu-id="e5132-812">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-812">10001</span></span></td>
<td><span data-ttu-id="e5132-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-813">Electricity</span></span></td>
<td><span data-ttu-id="e5132-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-814">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e5132-815">124.57</span></span></td>
<td><span data-ttu-id="e5132-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-817">CC002</span></span></td>
<td><span data-ttu-id="e5132-818">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-818">Finance</span></span></td>
<td><span data-ttu-id="e5132-819">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-819">10001</span></span></td>
<td><span data-ttu-id="e5132-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-820">Electricity</span></span></td>
<td><span data-ttu-id="e5132-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="e5132-822">-675.00</span></span></td>
<td><span data-ttu-id="e5132-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-824">CC003</span></span></td>
<td><span data-ttu-id="e5132-825">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-825">Assembly</span></span></td>
<td><span data-ttu-id="e5132-826">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-826">10001</span></span></td>
<td><span data-ttu-id="e5132-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-827">Electricity</span></span></td>
<td><span data-ttu-id="e5132-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e5132-829">438.75</span></span></td>
<td><span data-ttu-id="e5132-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-831">CC004</span></span></td>
<td><span data-ttu-id="e5132-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-832">Packaging</span></span></td>
<td><span data-ttu-id="e5132-833">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-833">10001</span></span></td>
<td><span data-ttu-id="e5132-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-834">Electricity</span></span></td>
<td><span data-ttu-id="e5132-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e5132-836">236.25</span></span></td>
<td><span data-ttu-id="e5132-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-838">CC002</span></span></td>
<td><span data-ttu-id="e5132-839">Finans</span><span class="sxs-lookup"><span data-stu-id="e5132-839">Finance</span></span></td>
<td><span data-ttu-id="e5132-840">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-840">10001</span></span></td>
<td><span data-ttu-id="e5132-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-841">Electricity</span></span></td>
<td><span data-ttu-id="e5132-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-842">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="e5132-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e5132-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-845">CC003</span></span></td>
<td><span data-ttu-id="e5132-846">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-846">Assembly</span></span></td>
<td><span data-ttu-id="e5132-847">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-847">10001</span></span></td>
<td><span data-ttu-id="e5132-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-848">Electricity</span></span></td>
<td><span data-ttu-id="e5132-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-849">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e5132-850">5,297.69</span></span></td>
<td><span data-ttu-id="e5132-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-852">CC004</span></span></td>
<td><span data-ttu-id="e5132-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="e5132-853">Packaging</span></span></td>
<td><span data-ttu-id="e5132-854">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-854">10001</span></span></td>
<td><span data-ttu-id="e5132-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-855">Electricity</span></span></td>
<td><span data-ttu-id="e5132-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-856">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e5132-857">2,852.60</span></span></td>
<td><span data-ttu-id="e5132-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-859">CC003</span></span></td>
<td><span data-ttu-id="e5132-860">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-860">Assembly</span></span></td>
<td><span data-ttu-id="e5132-861">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-861">10001</span></span></td>
<td><span data-ttu-id="e5132-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-862">Electricity</span></span></td>
<td><span data-ttu-id="e5132-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="e5132-864">-713.75</span></span></td>
<td><span data-ttu-id="e5132-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-866">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-867">Product 1</span></span></td>
<td><span data-ttu-id="e5132-868">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-868">10001</span></span></td>
<td><span data-ttu-id="e5132-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-869">Electricity</span></span></td>
<td><span data-ttu-id="e5132-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e5132-871">535.31</span></span></td>
<td><span data-ttu-id="e5132-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-873">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-874">Product 2</span></span></td>
<td><span data-ttu-id="e5132-875">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-875">10001</span></span></td>
<td><span data-ttu-id="e5132-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-876">Electricity</span></span></td>
<td><span data-ttu-id="e5132-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e5132-878">178.44</span></span></td>
<td><span data-ttu-id="e5132-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-880">CC003</span></span></td>
<td><span data-ttu-id="e5132-881">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-881">Assembly</span></span></td>
<td><span data-ttu-id="e5132-882">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-882">10001</span></span></td>
<td><span data-ttu-id="e5132-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-883">Electricity</span></span></td>
<td><span data-ttu-id="e5132-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-884">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="e5132-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e5132-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-887">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-888">Product 1</span></span></td>
<td><span data-ttu-id="e5132-889">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-889">10001</span></span></td>
<td><span data-ttu-id="e5132-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-890">Electricity</span></span></td>
<td><span data-ttu-id="e5132-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-891">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e5132-892">4,487.12</span></span></td>
<td><span data-ttu-id="e5132-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-894">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-895">Product 2</span></span></td>
<td><span data-ttu-id="e5132-896">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-896">10001</span></span></td>
<td><span data-ttu-id="e5132-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-897">Electricity</span></span></td>
<td><span data-ttu-id="e5132-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-898">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e5132-899">1,495.71</span></span></td>
<td><span data-ttu-id="e5132-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-901">CC003</span></span></td>
<td><span data-ttu-id="e5132-902">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-902">Assembly</span></span></td>
<td><span data-ttu-id="e5132-903">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-903">10001</span></span></td>
<td><span data-ttu-id="e5132-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-904">Electricity</span></span></td>
<td><span data-ttu-id="e5132-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="e5132-906">-286.25</span></span></td>
<td><span data-ttu-id="e5132-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-908">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-909">Product 1</span></span></td>
<td><span data-ttu-id="e5132-910">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-910">10001</span></span></td>
<td><span data-ttu-id="e5132-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-911">Electricity</span></span></td>
<td><span data-ttu-id="e5132-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e5132-913">241.05</span></span></td>
<td><span data-ttu-id="e5132-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-915">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-916">Product 2</span></span></td>
<td><span data-ttu-id="e5132-917">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-917">10001</span></span></td>
<td><span data-ttu-id="e5132-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-918">Electricity</span></span></td>
<td><span data-ttu-id="e5132-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e5132-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e5132-920">45.20</span></span></td>
<td><span data-ttu-id="e5132-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-922">CC003</span></span></td>
<td><span data-ttu-id="e5132-923">Samling</span><span class="sxs-lookup"><span data-stu-id="e5132-923">Assembly</span></span></td>
<td><span data-ttu-id="e5132-924">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-924">10001</span></span></td>
<td><span data-ttu-id="e5132-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-925">Electricity</span></span></td>
<td><span data-ttu-id="e5132-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-926">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="e5132-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e5132-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-929">Prod 1</span></span></td>
<td><span data-ttu-id="e5132-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="e5132-930">Product 1</span></span></td>
<td><span data-ttu-id="e5132-931">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-931">10001</span></span></td>
<td><span data-ttu-id="e5132-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-932">Electricity</span></span></td>
<td><span data-ttu-id="e5132-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-933">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e5132-934">2,507.09</span></span></td>
<td><span data-ttu-id="e5132-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e5132-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-936">Prod 2</span></span></td>
<td><span data-ttu-id="e5132-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="e5132-937">Product 2</span></span></td>
<td><span data-ttu-id="e5132-938">10001</span><span class="sxs-lookup"><span data-stu-id="e5132-938">10001</span></span></td>
<td><span data-ttu-id="e5132-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-939">Electricity</span></span></td>
<td><span data-ttu-id="e5132-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-940">Variable cost</span></span></td>
<td><span data-ttu-id="e5132-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e5132-941">470.08</span></span></td>
<td><span data-ttu-id="e5132-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="e5132-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e5132-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="e5132-943">Conclusion</span></span>
<span data-ttu-id="e5132-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="e5132-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e5132-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="e5132-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e5132-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="e5132-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e5132-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="e5132-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e5132-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="e5132-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e5132-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5132-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e5132-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="e5132-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e5132-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e5132-951">CC099</span></span></th>
<th><span data-ttu-id="e5132-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e5132-952">CC001</span></span></th>
<th><span data-ttu-id="e5132-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e5132-953">CC002</span></span></th>
<th><span data-ttu-id="e5132-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e5132-954">CC003</span></span></th>
<th><span data-ttu-id="e5132-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e5132-955">CC004</span></span></th>
<th><span data-ttu-id="e5132-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="e5132-956">Proj 1</span></span></th>
<th><span data-ttu-id="e5132-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="e5132-957">Proj 2</span></span></th>
<th><span data-ttu-id="e5132-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="e5132-958">Prod 1</span></span></th>
<th><span data-ttu-id="e5132-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="e5132-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e5132-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="e5132-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e5132-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e5132-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="e5132-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e5132-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e5132-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e5132-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e5132-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e5132-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="e5132-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-982">000</span><span class="sxs-lookup"><span data-stu-id="e5132-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e5132-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-987">30,00</span><span class="sxs-lookup"><span data-stu-id="e5132-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e5132-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e5132-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e5132-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e5132-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="e5132-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e5132-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="e5132-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e5132-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="e5132-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e5132-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="e5132-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e5132-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="e5132-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e5132-996">Du kan få flere oplysninger under [Omkostningstotaler](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="e5132-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



