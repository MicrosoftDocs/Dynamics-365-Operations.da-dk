---
title: Beregning af fast omkostning
description: I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: da-dk
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="5c921-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c921-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5c921-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5c921-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="5c921-105">Term definition</span></span>
---------------

<span data-ttu-id="5c921-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="5c921-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5c921-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="5c921-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5c921-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="5c921-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5c921-109">Leje</span><span class="sxs-lookup"><span data-stu-id="5c921-109">Rent</span></span>
-   <span data-ttu-id="5c921-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-110">Electricity</span></span>
-   <span data-ttu-id="5c921-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="5c921-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5c921-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-112">Overhead calculation overview</span></span>
<span data-ttu-id="5c921-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="5c921-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5c921-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="5c921-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5c921-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="5c921-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5c921-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5c921-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5c921-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5c921-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5c921-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="5c921-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5c921-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="5c921-119">Version type</span></span>
-   <span data-ttu-id="5c921-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="5c921-120">Date and time</span></span>
-   <span data-ttu-id="5c921-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="5c921-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5c921-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5c921-122">Fiscal year</span></span>
-   <span data-ttu-id="5c921-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="5c921-123">Fiscal period</span></span>

<span data-ttu-id="5c921-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="5c921-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5c921-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="5c921-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5c921-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="5c921-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5c921-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="5c921-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5c921-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5c921-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5c921-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="5c921-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5c921-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="5c921-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5c921-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5c921-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5c921-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5c921-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5c921-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5c921-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="5c921-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5c921-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="5c921-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5c921-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="5c921-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5c921-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="5c921-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="5c921-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="5c921-140">Main account</span></span></th>
<th><span data-ttu-id="5c921-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="5c921-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5c921-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-143">CC099</span></span></td>
<td><span data-ttu-id="5c921-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-144">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-145">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-145">10001</span></span></td>
<td><span data-ttu-id="5c921-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-146">Electricity</span></span></td>
<td><span data-ttu-id="5c921-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5c921-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="5c921-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5c921-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="5c921-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5c921-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="5c921-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5c921-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="5c921-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5c921-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="5c921-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5c921-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="5c921-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5c921-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="5c921-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5c921-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="5c921-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5c921-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5c921-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="5c921-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5c921-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="5c921-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5c921-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-160">Journal</span></span></th>
<th><span data-ttu-id="5c921-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5c921-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c921-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5c921-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c921-163">Version</span><span class="sxs-lookup"><span data-stu-id="5c921-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-164">00001</span><span class="sxs-lookup"><span data-stu-id="5c921-164">00001</span></span></td>
<td><span data-ttu-id="5c921-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5c921-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5c921-166">Fiscal</span></span></td>
<td><span data-ttu-id="5c921-167">2017</span><span class="sxs-lookup"><span data-stu-id="5c921-167">2017</span></span></td>
<td><span data-ttu-id="5c921-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5c921-168">Period 1</span></span></td>
<td><span data-ttu-id="5c921-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5c921-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5c921-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="5c921-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-173">Cost element</span></span></th>
<th><span data-ttu-id="5c921-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5c921-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-177">CC099</span></span></td>
<td><span data-ttu-id="5c921-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-178">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-179">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-179">10001</span></span></td>
<td><span data-ttu-id="5c921-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-180">Electricity</span></span></td>
<td><span data-ttu-id="5c921-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5c921-181">Unclassified</span></span></td>
<td><span data-ttu-id="5c921-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c921-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5c921-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-185">Cost element</span></span></th>
<th><span data-ttu-id="5c921-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-187">Amount</span></span></th>
<th><span data-ttu-id="5c921-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-189">CC099</span></span></td>
<td><span data-ttu-id="5c921-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-190">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-191">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-191">10001</span></span></td>
<td><span data-ttu-id="5c921-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-192">Electricity</span></span></td>
<td><span data-ttu-id="5c921-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5c921-193">Unclassified</span></span></td>
<td><span data-ttu-id="5c921-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-194">10,000.00</span></span></td>
<td><span data-ttu-id="5c921-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-196">CC099</span></span></td>
<td><span data-ttu-id="5c921-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-197">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-198">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-198">10001</span></span></td>
<td><span data-ttu-id="5c921-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-199">Electricity</span></span></td>
<td><span data-ttu-id="5c921-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5c921-200">Unclassified</span></span></td>
<td><span data-ttu-id="5c921-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5c921-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-203">CC099</span></span></td>
<td><span data-ttu-id="5c921-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-204">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-205">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-205">10001</span></span></td>
<td><span data-ttu-id="5c921-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-206">Electricity</span></span></td>
<td><span data-ttu-id="5c921-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-208">1,000.00</span></span></td>
<td><span data-ttu-id="5c921-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-210">CC099</span></span></td>
<td><span data-ttu-id="5c921-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-211">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-212">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-212">10001</span></span></td>
<td><span data-ttu-id="5c921-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-213">Electricity</span></span></td>
<td><span data-ttu-id="5c921-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-214">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-215">9,000.00</span></span></td>
<td><span data-ttu-id="5c921-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5c921-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5c921-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="5c921-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5c921-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5c921-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="5c921-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5c921-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="5c921-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5c921-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="5c921-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5c921-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="5c921-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5c921-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5c921-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="5c921-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5c921-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="5c921-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5c921-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-228">Cost object</span></span></th>
<th><span data-ttu-id="5c921-229">KWh</span><span class="sxs-lookup"><span data-stu-id="5c921-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-230">CC001</span></span></td>
<td><span data-ttu-id="5c921-231">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-231">HR</span></span></td>
<td><span data-ttu-id="5c921-232">1.000</span><span class="sxs-lookup"><span data-stu-id="5c921-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-233">CC002</span></span></td>
<td><span data-ttu-id="5c921-234">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-234">Finance</span></span></td>
<td><span data-ttu-id="5c921-235">6.000</span><span class="sxs-lookup"><span data-stu-id="5c921-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-236">CC003</span></span></td>
<td><span data-ttu-id="5c921-237">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-237">Assembly</span></span></td>
<td><span data-ttu-id="5c921-238">0</span><span class="sxs-lookup"><span data-stu-id="5c921-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5c921-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-240">Cost object</span></span></th>
<th><span data-ttu-id="5c921-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-241">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-244">CC001</span></span></td>
<td><span data-ttu-id="5c921-245">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-245">HR</span></span></td>
<td><span data-ttu-id="5c921-246">1.000</span><span class="sxs-lookup"><span data-stu-id="5c921-246">1,000</span></span></td>
<td><span data-ttu-id="5c921-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5c921-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5c921-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-249">CC002</span></span></td>
<td><span data-ttu-id="5c921-250">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-250">Finance</span></span></td>
<td><span data-ttu-id="5c921-251">6.000</span><span class="sxs-lookup"><span data-stu-id="5c921-251">6,000</span></span></td>
<td><span data-ttu-id="5c921-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5c921-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5c921-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-254">CC003</span></span></td>
<td><span data-ttu-id="5c921-255">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-255">Assembly</span></span></td>
<td><span data-ttu-id="5c921-256">0</span><span class="sxs-lookup"><span data-stu-id="5c921-256">0</span></span></td>
<td><span data-ttu-id="5c921-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5c921-258">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="5c921-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5c921-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5c921-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-261">Cost object</span></span></th>
<th><span data-ttu-id="5c921-262">Formel</span><span class="sxs-lookup"><span data-stu-id="5c921-262">Formula</span></span></th>
<th><span data-ttu-id="5c921-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-263">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-266">CC001</span></span></td>
<td><span data-ttu-id="5c921-267">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-267">HR</span></span></td>
<td><span data-ttu-id="5c921-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5c921-269">1</span><span class="sxs-lookup"><span data-stu-id="5c921-269">1</span></span></td>
<td><span data-ttu-id="5c921-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5c921-271">500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-272">CC002</span></span></td>
<td><span data-ttu-id="5c921-273">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-273">Finance</span></span></td>
<td><span data-ttu-id="5c921-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5c921-275">1</span><span class="sxs-lookup"><span data-stu-id="5c921-275">1</span></span></td>
<td><span data-ttu-id="5c921-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5c921-277">500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-278">CC003</span></span></td>
<td><span data-ttu-id="5c921-279">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-279">Assembly</span></span></td>
<td><span data-ttu-id="5c921-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5c921-281">0</span><span class="sxs-lookup"><span data-stu-id="5c921-281">0</span></span></td>
<td><span data-ttu-id="5c921-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5c921-283">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5c921-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-285">Journal</span></span></th>
<th><span data-ttu-id="5c921-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5c921-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c921-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5c921-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c921-288">Version</span><span class="sxs-lookup"><span data-stu-id="5c921-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-289">00002</span><span class="sxs-lookup"><span data-stu-id="5c921-289">00002</span></span></td>
<td><span data-ttu-id="5c921-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="5c921-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5c921-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5c921-291">Fiscal</span></span></td>
<td><span data-ttu-id="5c921-292">2017</span><span class="sxs-lookup"><span data-stu-id="5c921-292">2017</span></span></td>
<td><span data-ttu-id="5c921-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5c921-293">Period 1</span></span></td>
<td><span data-ttu-id="5c921-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5c921-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5c921-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="5c921-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-298">Cost element</span></span></th>
<th><span data-ttu-id="5c921-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-302">CC099</span></span></td>
<td><span data-ttu-id="5c921-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-303">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-304">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-304">10001</span></span></td>
<td><span data-ttu-id="5c921-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-305">Electricity</span></span></td>
<td><span data-ttu-id="5c921-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-309">CC099</span></span></td>
<td><span data-ttu-id="5c921-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-310">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-311">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-311">10001</span></span></td>
<td><span data-ttu-id="5c921-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-312">Electricity</span></span></td>
<td><span data-ttu-id="5c921-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-313">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c921-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5c921-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-317">Cost element</span></span></th>
<th><span data-ttu-id="5c921-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-319">Amount</span></span></th>
<th><span data-ttu-id="5c921-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-321">CC099</span></span></td>
<td><span data-ttu-id="5c921-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-322">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-323">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-323">10001</span></span></td>
<td><span data-ttu-id="5c921-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-324">Electricity</span></span></td>
<td><span data-ttu-id="5c921-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5c921-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-328">CC001</span></span></td>
<td><span data-ttu-id="5c921-329">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-329">HR</span></span></td>
<td><span data-ttu-id="5c921-330">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-330">10001</span></span></td>
<td><span data-ttu-id="5c921-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-331">Electricity</span></span></td>
<td><span data-ttu-id="5c921-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-333">500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-333">500.00</span></span></td>
<td><span data-ttu-id="5c921-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-335">CC002</span></span></td>
<td><span data-ttu-id="5c921-336">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-336">Finance</span></span></td>
<td><span data-ttu-id="5c921-337">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-337">10001</span></span></td>
<td><span data-ttu-id="5c921-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-338">Electricity</span></span></td>
<td><span data-ttu-id="5c921-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-340">500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-340">500.00</span></span></td>
<td><span data-ttu-id="5c921-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-342">CC099</span></span></td>
<td><span data-ttu-id="5c921-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="5c921-343">Default cost center</span></span></td>
<td><span data-ttu-id="5c921-344">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-344">10001</span></span></td>
<td><span data-ttu-id="5c921-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-345">Electricity</span></span></td>
<td><span data-ttu-id="5c921-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-346">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="5c921-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5c921-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-349">CC001</span></span></td>
<td><span data-ttu-id="5c921-350">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-350">HR</span></span></td>
<td><span data-ttu-id="5c921-351">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-351">10001</span></span></td>
<td><span data-ttu-id="5c921-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-352">Electricity</span></span></td>
<td><span data-ttu-id="5c921-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-353">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5c921-354">1,285.71</span></span></td>
<td><span data-ttu-id="5c921-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-356">CC002</span></span></td>
<td><span data-ttu-id="5c921-357">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-357">Finance</span></span></td>
<td><span data-ttu-id="5c921-358">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-358">10001</span></span></td>
<td><span data-ttu-id="5c921-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-359">Electricity</span></span></td>
<td><span data-ttu-id="5c921-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-360">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5c921-361">7,714.29</span></span></td>
<td><span data-ttu-id="5c921-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5c921-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5c921-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="5c921-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5c921-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5c921-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5c921-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="5c921-367">Define the overhead rate</span></span>

<span data-ttu-id="5c921-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5c921-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5c921-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-370">Cost object</span></span></th>
<th><span data-ttu-id="5c921-371">Timer</span><span class="sxs-lookup"><span data-stu-id="5c921-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-372">Proj 1</span></span></td>
<td><span data-ttu-id="5c921-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-373">Project 1</span></span></td>
<td><span data-ttu-id="5c921-374">3</span><span class="sxs-lookup"><span data-stu-id="5c921-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-375">Proj 2</span></span></td>
<td><span data-ttu-id="5c921-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-376">Project 2</span></span></td>
<td><span data-ttu-id="5c921-377">1</span><span class="sxs-lookup"><span data-stu-id="5c921-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="5c921-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-379">Cost object</span></span></th>
<th><span data-ttu-id="5c921-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-380">Cost element</span></span></th>
<th><span data-ttu-id="5c921-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="5c921-382">Units</span></span></th>
<th><span data-ttu-id="5c921-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="5c921-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-384">CC001</span></span></td>
<td><span data-ttu-id="5c921-385">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-385">HR</span></span></td>
<td><span data-ttu-id="5c921-386">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-386">10001</span></span></td>
<td><span data-ttu-id="5c921-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-387">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-388">1</span><span class="sxs-lookup"><span data-stu-id="5c921-388">1</span></span></td>
<td><span data-ttu-id="5c921-389">10</span><span class="sxs-lookup"><span data-stu-id="5c921-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-391">Cost object</span></span></th>
<th><span data-ttu-id="5c921-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-392">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-393">Cost element</span></span></th>
<th><span data-ttu-id="5c921-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-396">Proj 1</span></span></td>
<td><span data-ttu-id="5c921-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-397">Project 1</span></span></td>
<td><span data-ttu-id="5c921-398">3</span><span class="sxs-lookup"><span data-stu-id="5c921-398">3</span></span></td>
<td><span data-ttu-id="5c921-399">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-399">10001</span></span></td>
<td><span data-ttu-id="5c921-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5c921-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5c921-401">30,00</span><span class="sxs-lookup"><span data-stu-id="5c921-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-402">Proj 2</span></span></td>
<td><span data-ttu-id="5c921-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-403">Project 2</span></span></td>
<td><span data-ttu-id="5c921-404">1</span><span class="sxs-lookup"><span data-stu-id="5c921-404">1</span></span></td>
<td><span data-ttu-id="5c921-405">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-405">10001</span></span></td>
<td><span data-ttu-id="5c921-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5c921-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5c921-407">10,00</span><span class="sxs-lookup"><span data-stu-id="5c921-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5c921-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-409">Journal</span></span></th>
<th><span data-ttu-id="5c921-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5c921-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c921-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5c921-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c921-412">Version</span><span class="sxs-lookup"><span data-stu-id="5c921-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-413">00003</span><span class="sxs-lookup"><span data-stu-id="5c921-413">00003</span></span></td>
<td><span data-ttu-id="5c921-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="5c921-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5c921-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5c921-415">Fiscal</span></span></td>
<td><span data-ttu-id="5c921-416">2017</span><span class="sxs-lookup"><span data-stu-id="5c921-416">2017</span></span></td>
<td><span data-ttu-id="5c921-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5c921-417">Period 1</span></span></td>
<td><span data-ttu-id="5c921-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5c921-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5c921-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="5c921-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-421">Cost object</span></span></th>
<th><span data-ttu-id="5c921-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-424">Proj 1</span></span></td>
<td><span data-ttu-id="5c921-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5c921-426">3,00</span><span class="sxs-lookup"><span data-stu-id="5c921-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-428">Proj 2</span></span></td>
<td><span data-ttu-id="5c921-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5c921-430">1,00</span><span class="sxs-lookup"><span data-stu-id="5c921-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c921-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5c921-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-433">Cost element</span></span></th>
<th><span data-ttu-id="5c921-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-435">Amount</span></span></th>
<th><span data-ttu-id="5c921-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5c921-437">CC0001</span></span></td>
<td><span data-ttu-id="5c921-438">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-438">HR</span></span></td>
<td><span data-ttu-id="5c921-439">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-439">10001</span></span></td>
<td><span data-ttu-id="5c921-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-440">Electricity</span></span></td>
<td><span data-ttu-id="5c921-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-441">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="5c921-442">-30.00</span></span></td>
<td><span data-ttu-id="5c921-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-444">Proj 1</span></span></td>
<td><span data-ttu-id="5c921-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5c921-446">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-446">10001</span></span></td>
<td><span data-ttu-id="5c921-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-447">Electricity</span></span></td>
<td><span data-ttu-id="5c921-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-448">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-449">30,00</span><span class="sxs-lookup"><span data-stu-id="5c921-449">30.00</span></span></td>
<td><span data-ttu-id="5c921-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-451">CC001</span></span></td>
<td><span data-ttu-id="5c921-452">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-452">HR</span></span></td>
<td><span data-ttu-id="5c921-453">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-453">10001</span></span></td>
<td><span data-ttu-id="5c921-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-454">Electricity</span></span></td>
<td><span data-ttu-id="5c921-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-455">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="5c921-456">-10.00</span></span></td>
<td><span data-ttu-id="5c921-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-458">Proj 2</span></span></td>
<td><span data-ttu-id="5c921-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5c921-460">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-460">10001</span></span></td>
<td><span data-ttu-id="5c921-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-461">Electricity</span></span></td>
<td><span data-ttu-id="5c921-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-462">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-463">10.00</span><span class="sxs-lookup"><span data-stu-id="5c921-463">10.00</span></span></td>
<td><span data-ttu-id="5c921-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="5c921-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5c921-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="5c921-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5c921-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5c921-468">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="5c921-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="5c921-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="5c921-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5c921-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="5c921-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5c921-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="5c921-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5c921-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="5c921-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5c921-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="5c921-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5c921-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5c921-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5c921-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="5c921-475">Define the cost allocation</span></span>

<span data-ttu-id="5c921-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5c921-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5c921-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5c921-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5c921-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-479">Cost object</span></span></th>
<th><span data-ttu-id="5c921-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="5c921-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-481">CC002</span></span></td>
<td><span data-ttu-id="5c921-482">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-482">Finance</span></span></td>
<td><span data-ttu-id="5c921-483">35</span><span class="sxs-lookup"><span data-stu-id="5c921-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-484">CC003</span></span></td>
<td><span data-ttu-id="5c921-485">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-485">Assembly</span></span></td>
<td><span data-ttu-id="5c921-486">55</span><span class="sxs-lookup"><span data-stu-id="5c921-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-487">CC004</span></span></td>
<td><span data-ttu-id="5c921-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-488">Packaging</span></span></td>
<td><span data-ttu-id="5c921-489">10</span><span class="sxs-lookup"><span data-stu-id="5c921-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5c921-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5c921-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-492">Cost object</span></span></th>
<th><span data-ttu-id="5c921-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="5c921-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-494">CC003</span></span></td>
<td><span data-ttu-id="5c921-495">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-495">Assembly</span></span></td>
<td><span data-ttu-id="5c921-496">65</span><span class="sxs-lookup"><span data-stu-id="5c921-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-497">CC004</span></span></td>
<td><span data-ttu-id="5c921-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-498">Packaging</span></span></td>
<td><span data-ttu-id="5c921-499">35</span><span class="sxs-lookup"><span data-stu-id="5c921-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5c921-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5c921-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-502">Cost object</span></span></th>
<th><span data-ttu-id="5c921-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="5c921-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-504">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-505">Product 1</span></span></td>
<td><span data-ttu-id="5c921-506">60</span><span class="sxs-lookup"><span data-stu-id="5c921-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-507">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-508">Product 2</span></span></td>
<td><span data-ttu-id="5c921-509">20</span><span class="sxs-lookup"><span data-stu-id="5c921-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5c921-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="5c921-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-512">Cost object</span></span></th>
<th><span data-ttu-id="5c921-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="5c921-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-514">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-515">Product 1</span></span></td>
<td><span data-ttu-id="5c921-516">80</span><span class="sxs-lookup"><span data-stu-id="5c921-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-517">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-518">Product 2</span></span></td>
<td><span data-ttu-id="5c921-519">september</span><span class="sxs-lookup"><span data-stu-id="5c921-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5c921-520">I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="5c921-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5c921-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="5c921-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5c921-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5c921-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-523">Cost object</span></span></th>
<th><span data-ttu-id="5c921-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-524">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-526">Amount</span></span></th>
<th><span data-ttu-id="5c921-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-528">CC002</span></span></td>
<td><span data-ttu-id="5c921-529">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-529">Finance</span></span></td>
<td><span data-ttu-id="5c921-530">35</span><span class="sxs-lookup"><span data-stu-id="5c921-530">35</span></span></td>
<td><span data-ttu-id="5c921-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5c921-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5c921-532">175.00</span></span></td>
<td><span data-ttu-id="5c921-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-534">CC003</span></span></td>
<td><span data-ttu-id="5c921-535">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-535">Assembly</span></span></td>
<td><span data-ttu-id="5c921-536">55</span><span class="sxs-lookup"><span data-stu-id="5c921-536">55</span></span></td>
<td><span data-ttu-id="5c921-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5c921-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5c921-538">275.00</span></span></td>
<td><span data-ttu-id="5c921-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-540">CC004</span></span></td>
<td><span data-ttu-id="5c921-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-541">Packaging</span></span></td>
<td><span data-ttu-id="5c921-542">10</span><span class="sxs-lookup"><span data-stu-id="5c921-542">10</span></span></td>
<td><span data-ttu-id="5c921-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5c921-544">50,00</span><span class="sxs-lookup"><span data-stu-id="5c921-544">50.00</span></span></td>
<td><span data-ttu-id="5c921-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-546">CC002</span></span></td>
<td><span data-ttu-id="5c921-547">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-547">Finance</span></span></td>
<td><span data-ttu-id="5c921-548">35</span><span class="sxs-lookup"><span data-stu-id="5c921-548">35</span></span></td>
<td><span data-ttu-id="5c921-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5c921-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5c921-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5c921-550">436.00</span></span></td>
<td><span data-ttu-id="5c921-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-552">CC003</span></span></td>
<td><span data-ttu-id="5c921-553">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-553">Assembly</span></span></td>
<td><span data-ttu-id="5c921-554">55</span><span class="sxs-lookup"><span data-stu-id="5c921-554">55</span></span></td>
<td><span data-ttu-id="5c921-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5c921-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5c921-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5c921-556">685.14</span></span></td>
<td><span data-ttu-id="5c921-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-558">CC004</span></span></td>
<td><span data-ttu-id="5c921-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-559">Packaging</span></span></td>
<td><span data-ttu-id="5c921-560">10</span><span class="sxs-lookup"><span data-stu-id="5c921-560">10</span></span></td>
<td><span data-ttu-id="5c921-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5c921-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5c921-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5c921-562">124.57</span></span></td>
<td><span data-ttu-id="5c921-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5c921-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-565">Cost object</span></span></th>
<th><span data-ttu-id="5c921-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-566">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-568">Amount</span></span></th>
<th><span data-ttu-id="5c921-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-570">CC003</span></span></td>
<td><span data-ttu-id="5c921-571">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-571">Assembly</span></span></td>
<td><span data-ttu-id="5c921-572">65</span><span class="sxs-lookup"><span data-stu-id="5c921-572">65</span></span></td>
<td><span data-ttu-id="5c921-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5c921-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5c921-574">438.75</span></span></td>
<td><span data-ttu-id="5c921-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-576">CC004</span></span></td>
<td><span data-ttu-id="5c921-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-577">Packaging</span></span></td>
<td><span data-ttu-id="5c921-578">35</span><span class="sxs-lookup"><span data-stu-id="5c921-578">35</span></span></td>
<td><span data-ttu-id="5c921-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5c921-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5c921-580">236.25</span></span></td>
<td><span data-ttu-id="5c921-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-582">CC003</span></span></td>
<td><span data-ttu-id="5c921-583">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-583">Assembly</span></span></td>
<td><span data-ttu-id="5c921-584">65</span><span class="sxs-lookup"><span data-stu-id="5c921-584">65</span></span></td>
<td><span data-ttu-id="5c921-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5c921-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5c921-586">5,297.69</span></span></td>
<td><span data-ttu-id="5c921-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-588">CC004</span></span></td>
<td><span data-ttu-id="5c921-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-589">Packaging</span></span></td>
<td><span data-ttu-id="5c921-590">35</span><span class="sxs-lookup"><span data-stu-id="5c921-590">35</span></span></td>
<td><span data-ttu-id="5c921-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5c921-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5c921-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5c921-592">2,852.60</span></span></td>
<td><span data-ttu-id="5c921-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5c921-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-595">Cost object</span></span></th>
<th><span data-ttu-id="5c921-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-596">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-598">Amount</span></span></th>
<th><span data-ttu-id="5c921-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-600">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-601">Product 1</span></span></td>
<td><span data-ttu-id="5c921-602">60</span><span class="sxs-lookup"><span data-stu-id="5c921-602">60</span></span></td>
<td><span data-ttu-id="5c921-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5c921-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5c921-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5c921-604">535.31</span></span></td>
<td><span data-ttu-id="5c921-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-606">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-607">Product 2</span></span></td>
<td><span data-ttu-id="5c921-608">20</span><span class="sxs-lookup"><span data-stu-id="5c921-608">20</span></span></td>
<td><span data-ttu-id="5c921-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5c921-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5c921-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5c921-610">178.44</span></span></td>
<td><span data-ttu-id="5c921-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-612">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-613">Product 1</span></span></td>
<td><span data-ttu-id="5c921-614">60</span><span class="sxs-lookup"><span data-stu-id="5c921-614">60</span></span></td>
<td><span data-ttu-id="5c921-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5c921-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5c921-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5c921-616">4,487.12</span></span></td>
<td><span data-ttu-id="5c921-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-618">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-619">Product 2</span></span></td>
<td><span data-ttu-id="5c921-620">20</span><span class="sxs-lookup"><span data-stu-id="5c921-620">20</span></span></td>
<td><span data-ttu-id="5c921-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5c921-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5c921-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5c921-622">1,495.71</span></span></td>
<td><span data-ttu-id="5c921-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5c921-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="5c921-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-625">Cost object</span></span></th>
<th><span data-ttu-id="5c921-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="5c921-626">Magnitude</span></span></th>
<th><span data-ttu-id="5c921-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5c921-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5c921-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-628">Amount</span></span></th>
<th><span data-ttu-id="5c921-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-630">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-631">Product 1</span></span></td>
<td><span data-ttu-id="5c921-632">80</span><span class="sxs-lookup"><span data-stu-id="5c921-632">80</span></span></td>
<td><span data-ttu-id="5c921-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5c921-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5c921-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5c921-634">241.05</span></span></td>
<td><span data-ttu-id="5c921-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-636">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-637">Product 2</span></span></td>
<td><span data-ttu-id="5c921-638">15</span><span class="sxs-lookup"><span data-stu-id="5c921-638">15</span></span></td>
<td><span data-ttu-id="5c921-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5c921-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5c921-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5c921-640">45.20</span></span></td>
<td><span data-ttu-id="5c921-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-642">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-643">Product 1</span></span></td>
<td><span data-ttu-id="5c921-644">80</span><span class="sxs-lookup"><span data-stu-id="5c921-644">80</span></span></td>
<td><span data-ttu-id="5c921-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5c921-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5c921-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5c921-646">2,507.09</span></span></td>
<td><span data-ttu-id="5c921-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-648">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-649">Product 2</span></span></td>
<td><span data-ttu-id="5c921-650">15</span><span class="sxs-lookup"><span data-stu-id="5c921-650">15</span></span></td>
<td><span data-ttu-id="5c921-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5c921-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5c921-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5c921-652">470.08</span></span></td>
<td><span data-ttu-id="5c921-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5c921-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="5c921-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="5c921-655">Journal</span></span></th>
<th><span data-ttu-id="5c921-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="5c921-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5c921-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="5c921-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5c921-658">Version</span><span class="sxs-lookup"><span data-stu-id="5c921-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-659">00004</span><span class="sxs-lookup"><span data-stu-id="5c921-659">00004</span></span></td>
<td><span data-ttu-id="5c921-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="5c921-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5c921-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="5c921-661">Fiscal</span></span></td>
<td><span data-ttu-id="5c921-662">2017</span><span class="sxs-lookup"><span data-stu-id="5c921-662">2017</span></span></td>
<td><span data-ttu-id="5c921-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="5c921-663">Period 1</span></span></td>
<td><span data-ttu-id="5c921-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="5c921-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5c921-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="5c921-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5c921-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-668">Cost element</span></span></th>
<th><span data-ttu-id="5c921-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-672">CC001</span></span></td>
<td><span data-ttu-id="5c921-673">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-673">HR</span></span></td>
<td><span data-ttu-id="5c921-674">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-674">10001</span></span></td>
<td><span data-ttu-id="5c921-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-675">Electricity</span></span></td>
<td><span data-ttu-id="5c921-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-677">500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-679">CC001</span></span></td>
<td><span data-ttu-id="5c921-680">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-680">HR</span></span></td>
<td><span data-ttu-id="5c921-681">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-681">10001</span></span></td>
<td><span data-ttu-id="5c921-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-682">Electricity</span></span></td>
<td><span data-ttu-id="5c921-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-683">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5c921-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-686">CC002</span></span></td>
<td><span data-ttu-id="5c921-687">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-687">Finance</span></span></td>
<td><span data-ttu-id="5c921-688">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-688">10001</span></span></td>
<td><span data-ttu-id="5c921-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-689">Electricity</span></span></td>
<td><span data-ttu-id="5c921-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5c921-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-693">CC002</span></span></td>
<td><span data-ttu-id="5c921-694">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-694">Finance</span></span></td>
<td><span data-ttu-id="5c921-695">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-695">10001</span></span></td>
<td><span data-ttu-id="5c921-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-696">Electricity</span></span></td>
<td><span data-ttu-id="5c921-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-697">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5c921-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-700">CC003</span></span></td>
<td><span data-ttu-id="5c921-701">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-701">Assembly</span></span></td>
<td><span data-ttu-id="5c921-702">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-702">10001</span></span></td>
<td><span data-ttu-id="5c921-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-703">Electricity</span></span></td>
<td><span data-ttu-id="5c921-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5c921-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-707">CC003</span></span></td>
<td><span data-ttu-id="5c921-708">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-708">Assembly</span></span></td>
<td><span data-ttu-id="5c921-709">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-709">10001</span></span></td>
<td><span data-ttu-id="5c921-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-710">Electricity</span></span></td>
<td><span data-ttu-id="5c921-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-711">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5c921-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-714">CC003</span></span></td>
<td><span data-ttu-id="5c921-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-715">Packaging</span></span></td>
<td><span data-ttu-id="5c921-716">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-716">10001</span></span></td>
<td><span data-ttu-id="5c921-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-717">Electricity</span></span></td>
<td><span data-ttu-id="5c921-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5c921-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-721">CC003</span></span></td>
<td><span data-ttu-id="5c921-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-722">Packaging</span></span></td>
<td><span data-ttu-id="5c921-723">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-723">10001</span></span></td>
<td><span data-ttu-id="5c921-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-724">Electricity</span></span></td>
<td><span data-ttu-id="5c921-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-725">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5c921-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-728">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-729">Product 1</span></span></td>
<td><span data-ttu-id="5c921-730">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-730">10001</span></span></td>
<td><span data-ttu-id="5c921-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-731">Electricity</span></span></td>
<td><span data-ttu-id="5c921-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5c921-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-735">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-736">Product 1</span></span></td>
<td><span data-ttu-id="5c921-737">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-737">10001</span></span></td>
<td><span data-ttu-id="5c921-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-738">Electricity</span></span></td>
<td><span data-ttu-id="5c921-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-739">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5c921-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-742">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-743">Product 1</span></span></td>
<td><span data-ttu-id="5c921-744">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-744">10001</span></span></td>
<td><span data-ttu-id="5c921-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-745">Electricity</span></span></td>
<td><span data-ttu-id="5c921-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5c921-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5c921-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-749">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-750">Product 1</span></span></td>
<td><span data-ttu-id="5c921-751">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-751">10001</span></span></td>
<td><span data-ttu-id="5c921-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-752">Electricity</span></span></td>
<td><span data-ttu-id="5c921-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-753">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5c921-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5c921-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="5c921-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5c921-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5c921-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-757">Cost element</span></span></th>
<th><span data-ttu-id="5c921-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5c921-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="5c921-759">Amount</span></span></th>
<th><span data-ttu-id="5c921-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="5c921-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5c921-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-761">CC001</span></span></td>
<td><span data-ttu-id="5c921-762">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-762">HR</span></span></td>
<td><span data-ttu-id="5c921-763">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-763">10001</span></span></td>
<td><span data-ttu-id="5c921-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-764">Electricity</span></span></td>
<td><span data-ttu-id="5c921-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="5c921-766">-500.00</span></span></td>
<td><span data-ttu-id="5c921-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-768">CC002</span></span></td>
<td><span data-ttu-id="5c921-769">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-769">Finance</span></span></td>
<td><span data-ttu-id="5c921-770">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-770">10001</span></span></td>
<td><span data-ttu-id="5c921-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-771">Electricity</span></span></td>
<td><span data-ttu-id="5c921-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5c921-773">175.00</span></span></td>
<td><span data-ttu-id="5c921-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-775">CC003</span></span></td>
<td><span data-ttu-id="5c921-776">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-776">Assembly</span></span></td>
<td><span data-ttu-id="5c921-777">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-777">10001</span></span></td>
<td><span data-ttu-id="5c921-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-778">Electricity</span></span></td>
<td><span data-ttu-id="5c921-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5c921-780">275.00</span></span></td>
<td><span data-ttu-id="5c921-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-782">CC004</span></span></td>
<td><span data-ttu-id="5c921-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-783">Packaging</span></span></td>
<td><span data-ttu-id="5c921-784">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-784">10001</span></span></td>
<td><span data-ttu-id="5c921-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-785">Electricity</span></span></td>
<td><span data-ttu-id="5c921-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5c921-787">50,00</span></span></td>
<td><span data-ttu-id="5c921-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-789">CC001</span></span></td>
<td><span data-ttu-id="5c921-790">Personale</span><span class="sxs-lookup"><span data-stu-id="5c921-790">HR</span></span></td>
<td><span data-ttu-id="5c921-791">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-791">10001</span></span></td>
<td><span data-ttu-id="5c921-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-792">Electricity</span></span></td>
<td><span data-ttu-id="5c921-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-793">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="5c921-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5c921-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-796">CC002</span></span></td>
<td><span data-ttu-id="5c921-797">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-797">Finance</span></span></td>
<td><span data-ttu-id="5c921-798">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-798">10001</span></span></td>
<td><span data-ttu-id="5c921-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-799">Electricity</span></span></td>
<td><span data-ttu-id="5c921-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-800">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5c921-801">436.00</span></span></td>
<td><span data-ttu-id="5c921-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-803">CC003</span></span></td>
<td><span data-ttu-id="5c921-804">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-804">Assembly</span></span></td>
<td><span data-ttu-id="5c921-805">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-805">10001</span></span></td>
<td><span data-ttu-id="5c921-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-806">Electricity</span></span></td>
<td><span data-ttu-id="5c921-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-807">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5c921-808">685.14</span></span></td>
<td><span data-ttu-id="5c921-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-810">CC004</span></span></td>
<td><span data-ttu-id="5c921-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-811">Packaging</span></span></td>
<td><span data-ttu-id="5c921-812">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-812">10001</span></span></td>
<td><span data-ttu-id="5c921-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-813">Electricity</span></span></td>
<td><span data-ttu-id="5c921-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-814">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5c921-815">124.57</span></span></td>
<td><span data-ttu-id="5c921-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-817">CC002</span></span></td>
<td><span data-ttu-id="5c921-818">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-818">Finance</span></span></td>
<td><span data-ttu-id="5c921-819">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-819">10001</span></span></td>
<td><span data-ttu-id="5c921-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-820">Electricity</span></span></td>
<td><span data-ttu-id="5c921-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="5c921-822">-675.00</span></span></td>
<td><span data-ttu-id="5c921-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-824">CC003</span></span></td>
<td><span data-ttu-id="5c921-825">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-825">Assembly</span></span></td>
<td><span data-ttu-id="5c921-826">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-826">10001</span></span></td>
<td><span data-ttu-id="5c921-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-827">Electricity</span></span></td>
<td><span data-ttu-id="5c921-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5c921-829">438.75</span></span></td>
<td><span data-ttu-id="5c921-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-831">CC004</span></span></td>
<td><span data-ttu-id="5c921-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-832">Packaging</span></span></td>
<td><span data-ttu-id="5c921-833">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-833">10001</span></span></td>
<td><span data-ttu-id="5c921-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-834">Electricity</span></span></td>
<td><span data-ttu-id="5c921-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5c921-836">236.25</span></span></td>
<td><span data-ttu-id="5c921-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-838">CC002</span></span></td>
<td><span data-ttu-id="5c921-839">Finans</span><span class="sxs-lookup"><span data-stu-id="5c921-839">Finance</span></span></td>
<td><span data-ttu-id="5c921-840">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-840">10001</span></span></td>
<td><span data-ttu-id="5c921-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-841">Electricity</span></span></td>
<td><span data-ttu-id="5c921-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-842">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="5c921-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5c921-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-845">CC003</span></span></td>
<td><span data-ttu-id="5c921-846">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-846">Assembly</span></span></td>
<td><span data-ttu-id="5c921-847">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-847">10001</span></span></td>
<td><span data-ttu-id="5c921-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-848">Electricity</span></span></td>
<td><span data-ttu-id="5c921-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-849">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5c921-850">5,297.69</span></span></td>
<td><span data-ttu-id="5c921-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-852">CC004</span></span></td>
<td><span data-ttu-id="5c921-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="5c921-853">Packaging</span></span></td>
<td><span data-ttu-id="5c921-854">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-854">10001</span></span></td>
<td><span data-ttu-id="5c921-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-855">Electricity</span></span></td>
<td><span data-ttu-id="5c921-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-856">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5c921-857">2,852.60</span></span></td>
<td><span data-ttu-id="5c921-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-859">CC003</span></span></td>
<td><span data-ttu-id="5c921-860">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-860">Assembly</span></span></td>
<td><span data-ttu-id="5c921-861">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-861">10001</span></span></td>
<td><span data-ttu-id="5c921-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-862">Electricity</span></span></td>
<td><span data-ttu-id="5c921-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="5c921-864">-713.75</span></span></td>
<td><span data-ttu-id="5c921-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-866">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-867">Product 1</span></span></td>
<td><span data-ttu-id="5c921-868">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-868">10001</span></span></td>
<td><span data-ttu-id="5c921-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-869">Electricity</span></span></td>
<td><span data-ttu-id="5c921-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5c921-871">535.31</span></span></td>
<td><span data-ttu-id="5c921-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-873">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-874">Product 2</span></span></td>
<td><span data-ttu-id="5c921-875">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-875">10001</span></span></td>
<td><span data-ttu-id="5c921-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-876">Electricity</span></span></td>
<td><span data-ttu-id="5c921-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5c921-878">178.44</span></span></td>
<td><span data-ttu-id="5c921-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-880">CC003</span></span></td>
<td><span data-ttu-id="5c921-881">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-881">Assembly</span></span></td>
<td><span data-ttu-id="5c921-882">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-882">10001</span></span></td>
<td><span data-ttu-id="5c921-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-883">Electricity</span></span></td>
<td><span data-ttu-id="5c921-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-884">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="5c921-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5c921-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-887">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-888">Product 1</span></span></td>
<td><span data-ttu-id="5c921-889">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-889">10001</span></span></td>
<td><span data-ttu-id="5c921-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-890">Electricity</span></span></td>
<td><span data-ttu-id="5c921-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-891">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5c921-892">4,487.12</span></span></td>
<td><span data-ttu-id="5c921-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-894">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-895">Product 2</span></span></td>
<td><span data-ttu-id="5c921-896">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-896">10001</span></span></td>
<td><span data-ttu-id="5c921-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-897">Electricity</span></span></td>
<td><span data-ttu-id="5c921-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-898">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5c921-899">1,495.71</span></span></td>
<td><span data-ttu-id="5c921-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-901">CC003</span></span></td>
<td><span data-ttu-id="5c921-902">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-902">Assembly</span></span></td>
<td><span data-ttu-id="5c921-903">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-903">10001</span></span></td>
<td><span data-ttu-id="5c921-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-904">Electricity</span></span></td>
<td><span data-ttu-id="5c921-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="5c921-906">-286.25</span></span></td>
<td><span data-ttu-id="5c921-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-908">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-909">Product 1</span></span></td>
<td><span data-ttu-id="5c921-910">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-910">10001</span></span></td>
<td><span data-ttu-id="5c921-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-911">Electricity</span></span></td>
<td><span data-ttu-id="5c921-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5c921-913">241.05</span></span></td>
<td><span data-ttu-id="5c921-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-915">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-916">Product 2</span></span></td>
<td><span data-ttu-id="5c921-917">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-917">10001</span></span></td>
<td><span data-ttu-id="5c921-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-918">Electricity</span></span></td>
<td><span data-ttu-id="5c921-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5c921-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5c921-920">45.20</span></span></td>
<td><span data-ttu-id="5c921-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-922">CC003</span></span></td>
<td><span data-ttu-id="5c921-923">Samling</span><span class="sxs-lookup"><span data-stu-id="5c921-923">Assembly</span></span></td>
<td><span data-ttu-id="5c921-924">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-924">10001</span></span></td>
<td><span data-ttu-id="5c921-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-925">Electricity</span></span></td>
<td><span data-ttu-id="5c921-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-926">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="5c921-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5c921-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-929">Prod 1</span></span></td>
<td><span data-ttu-id="5c921-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="5c921-930">Product 1</span></span></td>
<td><span data-ttu-id="5c921-931">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-931">10001</span></span></td>
<td><span data-ttu-id="5c921-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-932">Electricity</span></span></td>
<td><span data-ttu-id="5c921-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-933">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5c921-934">2,507.09</span></span></td>
<td><span data-ttu-id="5c921-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5c921-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-936">Prod 2</span></span></td>
<td><span data-ttu-id="5c921-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="5c921-937">Product 2</span></span></td>
<td><span data-ttu-id="5c921-938">10001</span><span class="sxs-lookup"><span data-stu-id="5c921-938">10001</span></span></td>
<td><span data-ttu-id="5c921-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-939">Electricity</span></span></td>
<td><span data-ttu-id="5c921-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-940">Variable cost</span></span></td>
<td><span data-ttu-id="5c921-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5c921-941">470.08</span></span></td>
<td><span data-ttu-id="5c921-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="5c921-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5c921-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="5c921-943">Conclusion</span></span>
<span data-ttu-id="5c921-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="5c921-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5c921-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="5c921-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5c921-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="5c921-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5c921-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5c921-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5c921-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="5c921-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5c921-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="5c921-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5c921-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="5c921-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5c921-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5c921-951">CC099</span></span></th>
<th><span data-ttu-id="5c921-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5c921-952">CC001</span></span></th>
<th><span data-ttu-id="5c921-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5c921-953">CC002</span></span></th>
<th><span data-ttu-id="5c921-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5c921-954">CC003</span></span></th>
<th><span data-ttu-id="5c921-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5c921-955">CC004</span></span></th>
<th><span data-ttu-id="5c921-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5c921-956">Proj 1</span></span></th>
<th><span data-ttu-id="5c921-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5c921-957">Proj 2</span></span></th>
<th><span data-ttu-id="5c921-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5c921-958">Prod 1</span></span></th>
<th><span data-ttu-id="5c921-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5c921-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5c921-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="5c921-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5c921-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5c921-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="5c921-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-971">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5c921-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-973">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-975">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5c921-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5c921-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5c921-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5c921-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="5c921-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-982">000</span><span class="sxs-lookup"><span data-stu-id="5c921-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-983">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-984">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-985">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5c921-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-987">30,00</span><span class="sxs-lookup"><span data-stu-id="5c921-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-988">10,00</span><span class="sxs-lookup"><span data-stu-id="5c921-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5c921-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5c921-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5c921-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5c921-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5c921-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="5c921-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5c921-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="5c921-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5c921-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="5c921-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5c921-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="5c921-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5c921-996">Du kan få flere oplysninger under [Omkostningstotaler](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="5c921-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




