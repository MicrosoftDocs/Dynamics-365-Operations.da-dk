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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544049"
---
# <a name="overhead-calculation"></a><span data-ttu-id="76b64-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76b64-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76b64-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="76b64-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="76b64-105">Term definition</span></span>
---------------

<span data-ttu-id="76b64-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="76b64-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="76b64-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="76b64-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="76b64-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="76b64-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="76b64-109">Leje</span><span class="sxs-lookup"><span data-stu-id="76b64-109">Rent</span></span>
-   <span data-ttu-id="76b64-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-110">Electricity</span></span>
-   <span data-ttu-id="76b64-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="76b64-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="76b64-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-112">Overhead calculation overview</span></span>
<span data-ttu-id="76b64-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="76b64-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="76b64-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="76b64-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="76b64-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="76b64-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="76b64-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="76b64-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="76b64-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="76b64-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="76b64-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="76b64-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="76b64-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="76b64-119">Version type</span></span>
-   <span data-ttu-id="76b64-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="76b64-120">Date and time</span></span>
-   <span data-ttu-id="76b64-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="76b64-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="76b64-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="76b64-122">Fiscal year</span></span>
-   <span data-ttu-id="76b64-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="76b64-123">Fiscal period</span></span>

<span data-ttu-id="76b64-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="76b64-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="76b64-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="76b64-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="76b64-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="76b64-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="76b64-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="76b64-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="76b64-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="76b64-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="76b64-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="76b64-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="76b64-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="76b64-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="76b64-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="76b64-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="76b64-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="76b64-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="76b64-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="76b64-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="76b64-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="76b64-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="76b64-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="76b64-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="76b64-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="76b64-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="76b64-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="76b64-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="76b64-140">Main account</span></span></th>
<th><span data-ttu-id="76b64-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="76b64-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="76b64-143">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-143">CC099</span></span></td>
<td><span data-ttu-id="76b64-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-144">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-145">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-145">10001</span></span></td>
<td><span data-ttu-id="76b64-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-146">Electricity</span></span></td>
<td><span data-ttu-id="76b64-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="76b64-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="76b64-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="76b64-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="76b64-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="76b64-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="76b64-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="76b64-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="76b64-151">Define the cost behavior rule</span></span>

<span data-ttu-id="76b64-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="76b64-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="76b64-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="76b64-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="76b64-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="76b64-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="76b64-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="76b64-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="76b64-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="76b64-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="76b64-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="76b64-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="76b64-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="76b64-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-160">Journal</span></span></th>
<th><span data-ttu-id="76b64-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="76b64-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76b64-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="76b64-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76b64-163">Version</span><span class="sxs-lookup"><span data-stu-id="76b64-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-164">00001</span><span class="sxs-lookup"><span data-stu-id="76b64-164">00001</span></span></td>
<td><span data-ttu-id="76b64-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="76b64-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="76b64-166">Fiscal</span></span></td>
<td><span data-ttu-id="76b64-167">2017</span><span class="sxs-lookup"><span data-stu-id="76b64-167">2017</span></span></td>
<td><span data-ttu-id="76b64-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="76b64-168">Period 1</span></span></td>
<td><span data-ttu-id="76b64-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="76b64-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="76b64-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="76b64-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-173">Cost element</span></span></th>
<th><span data-ttu-id="76b64-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-174">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="76b64-177">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-177">CC099</span></span></td>
<td><span data-ttu-id="76b64-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-178">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-179">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-179">10001</span></span></td>
<td><span data-ttu-id="76b64-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-180">Electricity</span></span></td>
<td><span data-ttu-id="76b64-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="76b64-181">Unclassified</span></span></td>
<td><span data-ttu-id="76b64-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76b64-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="76b64-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-185">Cost element</span></span></th>
<th><span data-ttu-id="76b64-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-186">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-187">Amount</span></span></th>
<th><span data-ttu-id="76b64-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-189">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-189">CC099</span></span></td>
<td><span data-ttu-id="76b64-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-190">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-191">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-191">10001</span></span></td>
<td><span data-ttu-id="76b64-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-192">Electricity</span></span></td>
<td><span data-ttu-id="76b64-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="76b64-193">Unclassified</span></span></td>
<td><span data-ttu-id="76b64-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-194">10,000.00</span></span></td>
<td><span data-ttu-id="76b64-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-196">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-196">CC099</span></span></td>
<td><span data-ttu-id="76b64-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-197">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-198">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-198">10001</span></span></td>
<td><span data-ttu-id="76b64-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-199">Electricity</span></span></td>
<td><span data-ttu-id="76b64-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="76b64-200">Unclassified</span></span></td>
<td><span data-ttu-id="76b64-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-201">-10,000.00</span></span></td>
<td><span data-ttu-id="76b64-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-203">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-203">CC099</span></span></td>
<td><span data-ttu-id="76b64-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-204">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-205">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-205">10001</span></span></td>
<td><span data-ttu-id="76b64-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-206">Electricity</span></span></td>
<td><span data-ttu-id="76b64-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-207">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-208">1,000.00</span></span></td>
<td><span data-ttu-id="76b64-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-210">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-210">CC099</span></span></td>
<td><span data-ttu-id="76b64-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-211">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-212">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-212">10001</span></span></td>
<td><span data-ttu-id="76b64-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-213">Electricity</span></span></td>
<td><span data-ttu-id="76b64-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-214">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-215">9,000.00</span></span></td>
<td><span data-ttu-id="76b64-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="76b64-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="76b64-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="76b64-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="76b64-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="76b64-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="76b64-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="76b64-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="76b64-221">Define the cost distribution rule</span></span>

<span data-ttu-id="76b64-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="76b64-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="76b64-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="76b64-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="76b64-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="76b64-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="76b64-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="76b64-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="76b64-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="76b64-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-228">Cost object</span></span></th>
<th><span data-ttu-id="76b64-229">KWh</span><span class="sxs-lookup"><span data-stu-id="76b64-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-230">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-230">CC001</span></span></td>
<td><span data-ttu-id="76b64-231">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-231">HR</span></span></td>
<td><span data-ttu-id="76b64-232">1.000</span><span class="sxs-lookup"><span data-stu-id="76b64-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-233">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-233">CC002</span></span></td>
<td><span data-ttu-id="76b64-234">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-234">Finance</span></span></td>
<td><span data-ttu-id="76b64-235">6.000</span><span class="sxs-lookup"><span data-stu-id="76b64-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-236">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-236">CC003</span></span></td>
<td><span data-ttu-id="76b64-237">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-237">Assembly</span></span></td>
<td><span data-ttu-id="76b64-238">0</span><span class="sxs-lookup"><span data-stu-id="76b64-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76b64-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-240">Cost object</span></span></th>
<th><span data-ttu-id="76b64-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-241">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-242">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-244">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-244">CC001</span></span></td>
<td><span data-ttu-id="76b64-245">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-245">HR</span></span></td>
<td><span data-ttu-id="76b64-246">1.000</span><span class="sxs-lookup"><span data-stu-id="76b64-246">1,000</span></span></td>
<td><span data-ttu-id="76b64-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="76b64-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="76b64-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-249">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-249">CC002</span></span></td>
<td><span data-ttu-id="76b64-250">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-250">Finance</span></span></td>
<td><span data-ttu-id="76b64-251">6.000</span><span class="sxs-lookup"><span data-stu-id="76b64-251">6,000</span></span></td>
<td><span data-ttu-id="76b64-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="76b64-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="76b64-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-254">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-254">CC003</span></span></td>
<td><span data-ttu-id="76b64-255">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-255">Assembly</span></span></td>
<td><span data-ttu-id="76b64-256">0</span><span class="sxs-lookup"><span data-stu-id="76b64-256">0</span></span></td>
<td><span data-ttu-id="76b64-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="76b64-258">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="76b64-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="76b64-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76b64-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-261">Cost object</span></span></th>
<th><span data-ttu-id="76b64-262">Formel</span><span class="sxs-lookup"><span data-stu-id="76b64-262">Formula</span></span></th>
<th><span data-ttu-id="76b64-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-263">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-264">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-266">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-266">CC001</span></span></td>
<td><span data-ttu-id="76b64-267">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-267">HR</span></span></td>
<td><span data-ttu-id="76b64-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="76b64-269">1</span><span class="sxs-lookup"><span data-stu-id="76b64-269">1</span></span></td>
<td><span data-ttu-id="76b64-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="76b64-271">500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-272">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-272">CC002</span></span></td>
<td><span data-ttu-id="76b64-273">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-273">Finance</span></span></td>
<td><span data-ttu-id="76b64-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="76b64-275">1</span><span class="sxs-lookup"><span data-stu-id="76b64-275">1</span></span></td>
<td><span data-ttu-id="76b64-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="76b64-277">500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-278">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-278">CC003</span></span></td>
<td><span data-ttu-id="76b64-279">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-279">Assembly</span></span></td>
<td><span data-ttu-id="76b64-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="76b64-281">0</span><span class="sxs-lookup"><span data-stu-id="76b64-281">0</span></span></td>
<td><span data-ttu-id="76b64-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="76b64-283">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="76b64-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-285">Journal</span></span></th>
<th><span data-ttu-id="76b64-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="76b64-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76b64-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="76b64-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76b64-288">Version</span><span class="sxs-lookup"><span data-stu-id="76b64-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-289">00002</span><span class="sxs-lookup"><span data-stu-id="76b64-289">00002</span></span></td>
<td><span data-ttu-id="76b64-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="76b64-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="76b64-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="76b64-291">Fiscal</span></span></td>
<td><span data-ttu-id="76b64-292">2017</span><span class="sxs-lookup"><span data-stu-id="76b64-292">2017</span></span></td>
<td><span data-ttu-id="76b64-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="76b64-293">Period 1</span></span></td>
<td><span data-ttu-id="76b64-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="76b64-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="76b64-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="76b64-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-298">Cost element</span></span></th>
<th><span data-ttu-id="76b64-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-299">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-302">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-302">CC099</span></span></td>
<td><span data-ttu-id="76b64-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-303">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-304">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-304">10001</span></span></td>
<td><span data-ttu-id="76b64-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-305">Electricity</span></span></td>
<td><span data-ttu-id="76b64-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-306">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-309">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-309">CC099</span></span></td>
<td><span data-ttu-id="76b64-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-310">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-311">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-311">10001</span></span></td>
<td><span data-ttu-id="76b64-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-312">Electricity</span></span></td>
<td><span data-ttu-id="76b64-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-313">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76b64-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="76b64-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-317">Cost element</span></span></th>
<th><span data-ttu-id="76b64-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-318">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-319">Amount</span></span></th>
<th><span data-ttu-id="76b64-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-321">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-321">CC099</span></span></td>
<td><span data-ttu-id="76b64-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-322">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-323">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-323">10001</span></span></td>
<td><span data-ttu-id="76b64-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-324">Electricity</span></span></td>
<td><span data-ttu-id="76b64-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-325">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-326">-1,000.00</span></span></td>
<td><span data-ttu-id="76b64-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-328">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-328">CC001</span></span></td>
<td><span data-ttu-id="76b64-329">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-329">HR</span></span></td>
<td><span data-ttu-id="76b64-330">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-330">10001</span></span></td>
<td><span data-ttu-id="76b64-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-331">Electricity</span></span></td>
<td><span data-ttu-id="76b64-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-332">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-333">500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-333">500.00</span></span></td>
<td><span data-ttu-id="76b64-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-335">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-335">CC002</span></span></td>
<td><span data-ttu-id="76b64-336">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-336">Finance</span></span></td>
<td><span data-ttu-id="76b64-337">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-337">10001</span></span></td>
<td><span data-ttu-id="76b64-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-338">Electricity</span></span></td>
<td><span data-ttu-id="76b64-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-339">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-340">500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-340">500.00</span></span></td>
<td><span data-ttu-id="76b64-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-342">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-342">CC099</span></span></td>
<td><span data-ttu-id="76b64-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="76b64-343">Default cost center</span></span></td>
<td><span data-ttu-id="76b64-344">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-344">10001</span></span></td>
<td><span data-ttu-id="76b64-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-345">Electricity</span></span></td>
<td><span data-ttu-id="76b64-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-346">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="76b64-347">-9,000.00</span></span></td>
<td><span data-ttu-id="76b64-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-349">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-349">CC001</span></span></td>
<td><span data-ttu-id="76b64-350">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-350">HR</span></span></td>
<td><span data-ttu-id="76b64-351">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-351">10001</span></span></td>
<td><span data-ttu-id="76b64-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-352">Electricity</span></span></td>
<td><span data-ttu-id="76b64-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-353">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="76b64-354">1,285.71</span></span></td>
<td><span data-ttu-id="76b64-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-356">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-356">CC002</span></span></td>
<td><span data-ttu-id="76b64-357">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-357">Finance</span></span></td>
<td><span data-ttu-id="76b64-358">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-358">10001</span></span></td>
<td><span data-ttu-id="76b64-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-359">Electricity</span></span></td>
<td><span data-ttu-id="76b64-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-360">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="76b64-361">7,714.29</span></span></td>
<td><span data-ttu-id="76b64-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="76b64-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="76b64-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="76b64-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="76b64-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="76b64-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="76b64-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="76b64-367">Define the overhead rate</span></span>

<span data-ttu-id="76b64-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="76b64-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="76b64-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-370">Cost object</span></span></th>
<th><span data-ttu-id="76b64-371">Timer</span><span class="sxs-lookup"><span data-stu-id="76b64-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-372">Proj 1</span></span></td>
<td><span data-ttu-id="76b64-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-373">Project 1</span></span></td>
<td><span data-ttu-id="76b64-374">3</span><span class="sxs-lookup"><span data-stu-id="76b64-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-375">Proj 2</span></span></td>
<td><span data-ttu-id="76b64-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-376">Project 2</span></span></td>
<td><span data-ttu-id="76b64-377">1</span><span class="sxs-lookup"><span data-stu-id="76b64-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="76b64-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-379">Cost object</span></span></th>
<th><span data-ttu-id="76b64-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-380">Cost element</span></span></th>
<th><span data-ttu-id="76b64-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-381">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="76b64-382">Units</span></span></th>
<th><span data-ttu-id="76b64-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="76b64-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-384">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-384">CC001</span></span></td>
<td><span data-ttu-id="76b64-385">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-385">HR</span></span></td>
<td><span data-ttu-id="76b64-386">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-386">10001</span></span></td>
<td><span data-ttu-id="76b64-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-387">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-388">1</span><span class="sxs-lookup"><span data-stu-id="76b64-388">1</span></span></td>
<td><span data-ttu-id="76b64-389">10</span><span class="sxs-lookup"><span data-stu-id="76b64-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-391">Cost object</span></span></th>
<th><span data-ttu-id="76b64-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-392">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-393">Cost element</span></span></th>
<th><span data-ttu-id="76b64-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-394">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-396">Proj 1</span></span></td>
<td><span data-ttu-id="76b64-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-397">Project 1</span></span></td>
<td><span data-ttu-id="76b64-398">3</span><span class="sxs-lookup"><span data-stu-id="76b64-398">3</span></span></td>
<td><span data-ttu-id="76b64-399">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-399">10001</span></span></td>
<td><span data-ttu-id="76b64-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="76b64-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="76b64-401">30,00</span><span class="sxs-lookup"><span data-stu-id="76b64-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-402">Proj 2</span></span></td>
<td><span data-ttu-id="76b64-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-403">Project 2</span></span></td>
<td><span data-ttu-id="76b64-404">1</span><span class="sxs-lookup"><span data-stu-id="76b64-404">1</span></span></td>
<td><span data-ttu-id="76b64-405">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-405">10001</span></span></td>
<td><span data-ttu-id="76b64-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="76b64-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="76b64-407">10,00</span><span class="sxs-lookup"><span data-stu-id="76b64-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="76b64-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-409">Journal</span></span></th>
<th><span data-ttu-id="76b64-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="76b64-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76b64-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="76b64-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76b64-412">Version</span><span class="sxs-lookup"><span data-stu-id="76b64-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-413">00003</span><span class="sxs-lookup"><span data-stu-id="76b64-413">00003</span></span></td>
<td><span data-ttu-id="76b64-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="76b64-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="76b64-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="76b64-415">Fiscal</span></span></td>
<td><span data-ttu-id="76b64-416">2017</span><span class="sxs-lookup"><span data-stu-id="76b64-416">2017</span></span></td>
<td><span data-ttu-id="76b64-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="76b64-417">Period 1</span></span></td>
<td><span data-ttu-id="76b64-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="76b64-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="76b64-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="76b64-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-421">Cost object</span></span></th>
<th><span data-ttu-id="76b64-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-424">Proj 1</span></span></td>
<td><span data-ttu-id="76b64-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="76b64-426">3,00</span><span class="sxs-lookup"><span data-stu-id="76b64-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-428">Proj 2</span></span></td>
<td><span data-ttu-id="76b64-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="76b64-430">1,00</span><span class="sxs-lookup"><span data-stu-id="76b64-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76b64-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="76b64-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-433">Cost element</span></span></th>
<th><span data-ttu-id="76b64-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-434">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-435">Amount</span></span></th>
<th><span data-ttu-id="76b64-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="76b64-437">CC0001</span></span></td>
<td><span data-ttu-id="76b64-438">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-438">HR</span></span></td>
<td><span data-ttu-id="76b64-439">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-439">10001</span></span></td>
<td><span data-ttu-id="76b64-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-440">Electricity</span></span></td>
<td><span data-ttu-id="76b64-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-441">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="76b64-442">-30.00</span></span></td>
<td><span data-ttu-id="76b64-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-444">Proj 1</span></span></td>
<td><span data-ttu-id="76b64-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="76b64-446">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-446">10001</span></span></td>
<td><span data-ttu-id="76b64-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-447">Electricity</span></span></td>
<td><span data-ttu-id="76b64-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-448">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-449">30,00</span><span class="sxs-lookup"><span data-stu-id="76b64-449">30.00</span></span></td>
<td><span data-ttu-id="76b64-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-451">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-451">CC001</span></span></td>
<td><span data-ttu-id="76b64-452">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-452">HR</span></span></td>
<td><span data-ttu-id="76b64-453">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-453">10001</span></span></td>
<td><span data-ttu-id="76b64-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-454">Electricity</span></span></td>
<td><span data-ttu-id="76b64-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-455">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="76b64-456">-10.00</span></span></td>
<td><span data-ttu-id="76b64-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-458">Proj 2</span></span></td>
<td><span data-ttu-id="76b64-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="76b64-460">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-460">10001</span></span></td>
<td><span data-ttu-id="76b64-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-461">Electricity</span></span></td>
<td><span data-ttu-id="76b64-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-462">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-463">10.00</span><span class="sxs-lookup"><span data-stu-id="76b64-463">10.00</span></span></td>
<td><span data-ttu-id="76b64-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="76b64-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="76b64-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="76b64-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="76b64-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="76b64-468">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="76b64-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="76b64-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="76b64-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="76b64-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="76b64-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="76b64-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="76b64-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="76b64-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="76b64-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="76b64-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="76b64-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="76b64-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="76b64-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="76b64-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="76b64-475">Define the cost allocation</span></span>

<span data-ttu-id="76b64-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76b64-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="76b64-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="76b64-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="76b64-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-479">Cost object</span></span></th>
<th><span data-ttu-id="76b64-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="76b64-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-481">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-481">CC002</span></span></td>
<td><span data-ttu-id="76b64-482">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-482">Finance</span></span></td>
<td><span data-ttu-id="76b64-483">35</span><span class="sxs-lookup"><span data-stu-id="76b64-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-484">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-484">CC003</span></span></td>
<td><span data-ttu-id="76b64-485">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-485">Assembly</span></span></td>
<td><span data-ttu-id="76b64-486">55</span><span class="sxs-lookup"><span data-stu-id="76b64-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-487">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-487">CC004</span></span></td>
<td><span data-ttu-id="76b64-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-488">Packaging</span></span></td>
<td><span data-ttu-id="76b64-489">10</span><span class="sxs-lookup"><span data-stu-id="76b64-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="76b64-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="76b64-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-492">Cost object</span></span></th>
<th><span data-ttu-id="76b64-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="76b64-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-494">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-494">CC003</span></span></td>
<td><span data-ttu-id="76b64-495">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-495">Assembly</span></span></td>
<td><span data-ttu-id="76b64-496">65</span><span class="sxs-lookup"><span data-stu-id="76b64-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-497">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-497">CC004</span></span></td>
<td><span data-ttu-id="76b64-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-498">Packaging</span></span></td>
<td><span data-ttu-id="76b64-499">35</span><span class="sxs-lookup"><span data-stu-id="76b64-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="76b64-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="76b64-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-502">Cost object</span></span></th>
<th><span data-ttu-id="76b64-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="76b64-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-504">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-505">Product 1</span></span></td>
<td><span data-ttu-id="76b64-506">60</span><span class="sxs-lookup"><span data-stu-id="76b64-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-507">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-508">Product 2</span></span></td>
<td><span data-ttu-id="76b64-509">20</span><span class="sxs-lookup"><span data-stu-id="76b64-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="76b64-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="76b64-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-512">Cost object</span></span></th>
<th><span data-ttu-id="76b64-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="76b64-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-514">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-515">Product 1</span></span></td>
<td><span data-ttu-id="76b64-516">80</span><span class="sxs-lookup"><span data-stu-id="76b64-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-517">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-518">Product 2</span></span></td>
<td><span data-ttu-id="76b64-519">september</span><span class="sxs-lookup"><span data-stu-id="76b64-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="76b64-520">I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="76b64-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="76b64-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="76b64-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="76b64-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="76b64-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-523">Cost object</span></span></th>
<th><span data-ttu-id="76b64-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-524">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-525">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-526">Amount</span></span></th>
<th><span data-ttu-id="76b64-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-528">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-528">CC002</span></span></td>
<td><span data-ttu-id="76b64-529">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-529">Finance</span></span></td>
<td><span data-ttu-id="76b64-530">35</span><span class="sxs-lookup"><span data-stu-id="76b64-530">35</span></span></td>
<td><span data-ttu-id="76b64-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="76b64-532">175.00</span><span class="sxs-lookup"><span data-stu-id="76b64-532">175.00</span></span></td>
<td><span data-ttu-id="76b64-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-534">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-534">CC003</span></span></td>
<td><span data-ttu-id="76b64-535">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-535">Assembly</span></span></td>
<td><span data-ttu-id="76b64-536">55</span><span class="sxs-lookup"><span data-stu-id="76b64-536">55</span></span></td>
<td><span data-ttu-id="76b64-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="76b64-538">275.00</span><span class="sxs-lookup"><span data-stu-id="76b64-538">275.00</span></span></td>
<td><span data-ttu-id="76b64-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-540">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-540">CC004</span></span></td>
<td><span data-ttu-id="76b64-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-541">Packaging</span></span></td>
<td><span data-ttu-id="76b64-542">10</span><span class="sxs-lookup"><span data-stu-id="76b64-542">10</span></span></td>
<td><span data-ttu-id="76b64-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="76b64-544">50,00</span><span class="sxs-lookup"><span data-stu-id="76b64-544">50.00</span></span></td>
<td><span data-ttu-id="76b64-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-546">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-546">CC002</span></span></td>
<td><span data-ttu-id="76b64-547">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-547">Finance</span></span></td>
<td><span data-ttu-id="76b64-548">35</span><span class="sxs-lookup"><span data-stu-id="76b64-548">35</span></span></td>
<td><span data-ttu-id="76b64-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="76b64-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="76b64-550">436.00</span><span class="sxs-lookup"><span data-stu-id="76b64-550">436.00</span></span></td>
<td><span data-ttu-id="76b64-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-552">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-552">CC003</span></span></td>
<td><span data-ttu-id="76b64-553">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-553">Assembly</span></span></td>
<td><span data-ttu-id="76b64-554">55</span><span class="sxs-lookup"><span data-stu-id="76b64-554">55</span></span></td>
<td><span data-ttu-id="76b64-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="76b64-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="76b64-556">685.14</span><span class="sxs-lookup"><span data-stu-id="76b64-556">685.14</span></span></td>
<td><span data-ttu-id="76b64-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-558">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-558">CC004</span></span></td>
<td><span data-ttu-id="76b64-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-559">Packaging</span></span></td>
<td><span data-ttu-id="76b64-560">10</span><span class="sxs-lookup"><span data-stu-id="76b64-560">10</span></span></td>
<td><span data-ttu-id="76b64-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="76b64-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="76b64-562">124.57</span><span class="sxs-lookup"><span data-stu-id="76b64-562">124.57</span></span></td>
<td><span data-ttu-id="76b64-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="76b64-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-565">Cost object</span></span></th>
<th><span data-ttu-id="76b64-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-566">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-567">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-568">Amount</span></span></th>
<th><span data-ttu-id="76b64-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-570">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-570">CC003</span></span></td>
<td><span data-ttu-id="76b64-571">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-571">Assembly</span></span></td>
<td><span data-ttu-id="76b64-572">65</span><span class="sxs-lookup"><span data-stu-id="76b64-572">65</span></span></td>
<td><span data-ttu-id="76b64-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="76b64-574">438.75</span><span class="sxs-lookup"><span data-stu-id="76b64-574">438.75</span></span></td>
<td><span data-ttu-id="76b64-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-576">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-576">CC004</span></span></td>
<td><span data-ttu-id="76b64-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-577">Packaging</span></span></td>
<td><span data-ttu-id="76b64-578">35</span><span class="sxs-lookup"><span data-stu-id="76b64-578">35</span></span></td>
<td><span data-ttu-id="76b64-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="76b64-580">236.25</span><span class="sxs-lookup"><span data-stu-id="76b64-580">236.25</span></span></td>
<td><span data-ttu-id="76b64-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-582">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-582">CC003</span></span></td>
<td><span data-ttu-id="76b64-583">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-583">Assembly</span></span></td>
<td><span data-ttu-id="76b64-584">65</span><span class="sxs-lookup"><span data-stu-id="76b64-584">65</span></span></td>
<td><span data-ttu-id="76b64-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="76b64-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="76b64-586">5,297.69</span></span></td>
<td><span data-ttu-id="76b64-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-588">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-588">CC004</span></span></td>
<td><span data-ttu-id="76b64-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-589">Packaging</span></span></td>
<td><span data-ttu-id="76b64-590">35</span><span class="sxs-lookup"><span data-stu-id="76b64-590">35</span></span></td>
<td><span data-ttu-id="76b64-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="76b64-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="76b64-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="76b64-592">2,852.60</span></span></td>
<td><span data-ttu-id="76b64-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="76b64-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-595">Cost object</span></span></th>
<th><span data-ttu-id="76b64-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-596">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-597">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-598">Amount</span></span></th>
<th><span data-ttu-id="76b64-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-600">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-601">Product 1</span></span></td>
<td><span data-ttu-id="76b64-602">60</span><span class="sxs-lookup"><span data-stu-id="76b64-602">60</span></span></td>
<td><span data-ttu-id="76b64-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="76b64-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="76b64-604">535.31</span><span class="sxs-lookup"><span data-stu-id="76b64-604">535.31</span></span></td>
<td><span data-ttu-id="76b64-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-606">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-607">Product 2</span></span></td>
<td><span data-ttu-id="76b64-608">20</span><span class="sxs-lookup"><span data-stu-id="76b64-608">20</span></span></td>
<td><span data-ttu-id="76b64-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="76b64-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="76b64-610">178.44</span><span class="sxs-lookup"><span data-stu-id="76b64-610">178.44</span></span></td>
<td><span data-ttu-id="76b64-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-612">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-613">Product 1</span></span></td>
<td><span data-ttu-id="76b64-614">60</span><span class="sxs-lookup"><span data-stu-id="76b64-614">60</span></span></td>
<td><span data-ttu-id="76b64-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="76b64-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="76b64-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="76b64-616">4,487.12</span></span></td>
<td><span data-ttu-id="76b64-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-618">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-619">Product 2</span></span></td>
<td><span data-ttu-id="76b64-620">20</span><span class="sxs-lookup"><span data-stu-id="76b64-620">20</span></span></td>
<td><span data-ttu-id="76b64-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="76b64-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="76b64-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="76b64-622">1,495.71</span></span></td>
<td><span data-ttu-id="76b64-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76b64-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="76b64-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-625">Cost object</span></span></th>
<th><span data-ttu-id="76b64-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="76b64-626">Magnitude</span></span></th>
<th><span data-ttu-id="76b64-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="76b64-627">Allocation factor</span></span></th>
<th><span data-ttu-id="76b64-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-628">Amount</span></span></th>
<th><span data-ttu-id="76b64-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-630">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-631">Product 1</span></span></td>
<td><span data-ttu-id="76b64-632">80</span><span class="sxs-lookup"><span data-stu-id="76b64-632">80</span></span></td>
<td><span data-ttu-id="76b64-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="76b64-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="76b64-634">241.05</span><span class="sxs-lookup"><span data-stu-id="76b64-634">241.05</span></span></td>
<td><span data-ttu-id="76b64-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-636">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-637">Product 2</span></span></td>
<td><span data-ttu-id="76b64-638">15</span><span class="sxs-lookup"><span data-stu-id="76b64-638">15</span></span></td>
<td><span data-ttu-id="76b64-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="76b64-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="76b64-640">45.20</span><span class="sxs-lookup"><span data-stu-id="76b64-640">45.20</span></span></td>
<td><span data-ttu-id="76b64-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-642">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-643">Product 1</span></span></td>
<td><span data-ttu-id="76b64-644">80</span><span class="sxs-lookup"><span data-stu-id="76b64-644">80</span></span></td>
<td><span data-ttu-id="76b64-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="76b64-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="76b64-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="76b64-646">2,507.09</span></span></td>
<td><span data-ttu-id="76b64-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-648">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-649">Product 2</span></span></td>
<td><span data-ttu-id="76b64-650">15</span><span class="sxs-lookup"><span data-stu-id="76b64-650">15</span></span></td>
<td><span data-ttu-id="76b64-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="76b64-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="76b64-652">470.08</span><span class="sxs-lookup"><span data-stu-id="76b64-652">470.08</span></span></td>
<td><span data-ttu-id="76b64-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="76b64-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="76b64-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="76b64-655">Journal</span></span></th>
<th><span data-ttu-id="76b64-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="76b64-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76b64-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="76b64-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76b64-658">Version</span><span class="sxs-lookup"><span data-stu-id="76b64-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-659">00004</span><span class="sxs-lookup"><span data-stu-id="76b64-659">00004</span></span></td>
<td><span data-ttu-id="76b64-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="76b64-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="76b64-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="76b64-661">Fiscal</span></span></td>
<td><span data-ttu-id="76b64-662">2017</span><span class="sxs-lookup"><span data-stu-id="76b64-662">2017</span></span></td>
<td><span data-ttu-id="76b64-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="76b64-663">Period 1</span></span></td>
<td><span data-ttu-id="76b64-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="76b64-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="76b64-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="76b64-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76b64-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-668">Cost element</span></span></th>
<th><span data-ttu-id="76b64-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-669">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-672">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-672">CC001</span></span></td>
<td><span data-ttu-id="76b64-673">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-673">HR</span></span></td>
<td><span data-ttu-id="76b64-674">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-674">10001</span></span></td>
<td><span data-ttu-id="76b64-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-675">Electricity</span></span></td>
<td><span data-ttu-id="76b64-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-676">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-677">500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-679">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-679">CC001</span></span></td>
<td><span data-ttu-id="76b64-680">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-680">HR</span></span></td>
<td><span data-ttu-id="76b64-681">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-681">10001</span></span></td>
<td><span data-ttu-id="76b64-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-682">Electricity</span></span></td>
<td><span data-ttu-id="76b64-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-683">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="76b64-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-686">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-686">CC002</span></span></td>
<td><span data-ttu-id="76b64-687">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-687">Finance</span></span></td>
<td><span data-ttu-id="76b64-688">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-688">10001</span></span></td>
<td><span data-ttu-id="76b64-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-689">Electricity</span></span></td>
<td><span data-ttu-id="76b64-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-690">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-691">675.00</span><span class="sxs-lookup"><span data-stu-id="76b64-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-693">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-693">CC002</span></span></td>
<td><span data-ttu-id="76b64-694">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-694">Finance</span></span></td>
<td><span data-ttu-id="76b64-695">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-695">10001</span></span></td>
<td><span data-ttu-id="76b64-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-696">Electricity</span></span></td>
<td><span data-ttu-id="76b64-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-697">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="76b64-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-700">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-700">CC003</span></span></td>
<td><span data-ttu-id="76b64-701">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-701">Assembly</span></span></td>
<td><span data-ttu-id="76b64-702">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-702">10001</span></span></td>
<td><span data-ttu-id="76b64-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-703">Electricity</span></span></td>
<td><span data-ttu-id="76b64-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-704">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-705">713.75</span><span class="sxs-lookup"><span data-stu-id="76b64-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-707">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-707">CC003</span></span></td>
<td><span data-ttu-id="76b64-708">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-708">Assembly</span></span></td>
<td><span data-ttu-id="76b64-709">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-709">10001</span></span></td>
<td><span data-ttu-id="76b64-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-710">Electricity</span></span></td>
<td><span data-ttu-id="76b64-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-711">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="76b64-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-714">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-714">CC003</span></span></td>
<td><span data-ttu-id="76b64-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-715">Packaging</span></span></td>
<td><span data-ttu-id="76b64-716">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-716">10001</span></span></td>
<td><span data-ttu-id="76b64-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-717">Electricity</span></span></td>
<td><span data-ttu-id="76b64-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-718">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-719">286.25</span><span class="sxs-lookup"><span data-stu-id="76b64-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-721">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-721">CC003</span></span></td>
<td><span data-ttu-id="76b64-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-722">Packaging</span></span></td>
<td><span data-ttu-id="76b64-723">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-723">10001</span></span></td>
<td><span data-ttu-id="76b64-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-724">Electricity</span></span></td>
<td><span data-ttu-id="76b64-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-725">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="76b64-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-728">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-729">Product 1</span></span></td>
<td><span data-ttu-id="76b64-730">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-730">10001</span></span></td>
<td><span data-ttu-id="76b64-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-731">Electricity</span></span></td>
<td><span data-ttu-id="76b64-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-732">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-733">776.36</span><span class="sxs-lookup"><span data-stu-id="76b64-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-735">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-736">Product 1</span></span></td>
<td><span data-ttu-id="76b64-737">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-737">10001</span></span></td>
<td><span data-ttu-id="76b64-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-738">Electricity</span></span></td>
<td><span data-ttu-id="76b64-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-739">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="76b64-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-742">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-743">Product 1</span></span></td>
<td><span data-ttu-id="76b64-744">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-744">10001</span></span></td>
<td><span data-ttu-id="76b64-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-745">Electricity</span></span></td>
<td><span data-ttu-id="76b64-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-746">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-747">223.64</span><span class="sxs-lookup"><span data-stu-id="76b64-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="76b64-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-749">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-750">Product 1</span></span></td>
<td><span data-ttu-id="76b64-751">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-751">10001</span></span></td>
<td><span data-ttu-id="76b64-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-752">Electricity</span></span></td>
<td><span data-ttu-id="76b64-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-753">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="76b64-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76b64-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="76b64-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76b64-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76b64-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-757">Cost element</span></span></th>
<th><span data-ttu-id="76b64-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-758">Cost behavior</span></span></th>
<th><span data-ttu-id="76b64-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="76b64-759">Amount</span></span></th>
<th><span data-ttu-id="76b64-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="76b64-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76b64-761">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-761">CC001</span></span></td>
<td><span data-ttu-id="76b64-762">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-762">HR</span></span></td>
<td><span data-ttu-id="76b64-763">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-763">10001</span></span></td>
<td><span data-ttu-id="76b64-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-764">Electricity</span></span></td>
<td><span data-ttu-id="76b64-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-765">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="76b64-766">-500.00</span></span></td>
<td><span data-ttu-id="76b64-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-768">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-768">CC002</span></span></td>
<td><span data-ttu-id="76b64-769">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-769">Finance</span></span></td>
<td><span data-ttu-id="76b64-770">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-770">10001</span></span></td>
<td><span data-ttu-id="76b64-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-771">Electricity</span></span></td>
<td><span data-ttu-id="76b64-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-772">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-773">175.00</span><span class="sxs-lookup"><span data-stu-id="76b64-773">175.00</span></span></td>
<td><span data-ttu-id="76b64-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-775">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-775">CC003</span></span></td>
<td><span data-ttu-id="76b64-776">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-776">Assembly</span></span></td>
<td><span data-ttu-id="76b64-777">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-777">10001</span></span></td>
<td><span data-ttu-id="76b64-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-778">Electricity</span></span></td>
<td><span data-ttu-id="76b64-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-779">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-780">275.00</span><span class="sxs-lookup"><span data-stu-id="76b64-780">275.00</span></span></td>
<td><span data-ttu-id="76b64-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-782">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-782">CC004</span></span></td>
<td><span data-ttu-id="76b64-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-783">Packaging</span></span></td>
<td><span data-ttu-id="76b64-784">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-784">10001</span></span></td>
<td><span data-ttu-id="76b64-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-785">Electricity</span></span></td>
<td><span data-ttu-id="76b64-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-786">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-787">50,00</span><span class="sxs-lookup"><span data-stu-id="76b64-787">50,00</span></span></td>
<td><span data-ttu-id="76b64-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-789">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-789">CC001</span></span></td>
<td><span data-ttu-id="76b64-790">Personale</span><span class="sxs-lookup"><span data-stu-id="76b64-790">HR</span></span></td>
<td><span data-ttu-id="76b64-791">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-791">10001</span></span></td>
<td><span data-ttu-id="76b64-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-792">Electricity</span></span></td>
<td><span data-ttu-id="76b64-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-793">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="76b64-794">-1,245.71</span></span></td>
<td><span data-ttu-id="76b64-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-796">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-796">CC002</span></span></td>
<td><span data-ttu-id="76b64-797">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-797">Finance</span></span></td>
<td><span data-ttu-id="76b64-798">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-798">10001</span></span></td>
<td><span data-ttu-id="76b64-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-799">Electricity</span></span></td>
<td><span data-ttu-id="76b64-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-800">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-801">436.00</span><span class="sxs-lookup"><span data-stu-id="76b64-801">436.00</span></span></td>
<td><span data-ttu-id="76b64-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-803">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-803">CC003</span></span></td>
<td><span data-ttu-id="76b64-804">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-804">Assembly</span></span></td>
<td><span data-ttu-id="76b64-805">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-805">10001</span></span></td>
<td><span data-ttu-id="76b64-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-806">Electricity</span></span></td>
<td><span data-ttu-id="76b64-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-807">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-808">685.14</span><span class="sxs-lookup"><span data-stu-id="76b64-808">685.14</span></span></td>
<td><span data-ttu-id="76b64-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-810">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-810">CC004</span></span></td>
<td><span data-ttu-id="76b64-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-811">Packaging</span></span></td>
<td><span data-ttu-id="76b64-812">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-812">10001</span></span></td>
<td><span data-ttu-id="76b64-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-813">Electricity</span></span></td>
<td><span data-ttu-id="76b64-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-814">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-815">124.57</span><span class="sxs-lookup"><span data-stu-id="76b64-815">124.57</span></span></td>
<td><span data-ttu-id="76b64-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-817">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-817">CC002</span></span></td>
<td><span data-ttu-id="76b64-818">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-818">Finance</span></span></td>
<td><span data-ttu-id="76b64-819">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-819">10001</span></span></td>
<td><span data-ttu-id="76b64-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-820">Electricity</span></span></td>
<td><span data-ttu-id="76b64-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-821">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="76b64-822">-675.00</span></span></td>
<td><span data-ttu-id="76b64-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-824">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-824">CC003</span></span></td>
<td><span data-ttu-id="76b64-825">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-825">Assembly</span></span></td>
<td><span data-ttu-id="76b64-826">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-826">10001</span></span></td>
<td><span data-ttu-id="76b64-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-827">Electricity</span></span></td>
<td><span data-ttu-id="76b64-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-828">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-829">438.75</span><span class="sxs-lookup"><span data-stu-id="76b64-829">438.75</span></span></td>
<td><span data-ttu-id="76b64-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-831">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-831">CC004</span></span></td>
<td><span data-ttu-id="76b64-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-832">Packaging</span></span></td>
<td><span data-ttu-id="76b64-833">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-833">10001</span></span></td>
<td><span data-ttu-id="76b64-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-834">Electricity</span></span></td>
<td><span data-ttu-id="76b64-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-835">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-836">236.25</span><span class="sxs-lookup"><span data-stu-id="76b64-836">236.25</span></span></td>
<td><span data-ttu-id="76b64-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-838">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-838">CC002</span></span></td>
<td><span data-ttu-id="76b64-839">Finans</span><span class="sxs-lookup"><span data-stu-id="76b64-839">Finance</span></span></td>
<td><span data-ttu-id="76b64-840">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-840">10001</span></span></td>
<td><span data-ttu-id="76b64-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-841">Electricity</span></span></td>
<td><span data-ttu-id="76b64-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-842">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="76b64-843">-8,150.29</span></span></td>
<td><span data-ttu-id="76b64-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-845">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-845">CC003</span></span></td>
<td><span data-ttu-id="76b64-846">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-846">Assembly</span></span></td>
<td><span data-ttu-id="76b64-847">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-847">10001</span></span></td>
<td><span data-ttu-id="76b64-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-848">Electricity</span></span></td>
<td><span data-ttu-id="76b64-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-849">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="76b64-850">5,297.69</span></span></td>
<td><span data-ttu-id="76b64-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-852">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-852">CC004</span></span></td>
<td><span data-ttu-id="76b64-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="76b64-853">Packaging</span></span></td>
<td><span data-ttu-id="76b64-854">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-854">10001</span></span></td>
<td><span data-ttu-id="76b64-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-855">Electricity</span></span></td>
<td><span data-ttu-id="76b64-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-856">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="76b64-857">2,852.60</span></span></td>
<td><span data-ttu-id="76b64-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-859">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-859">CC003</span></span></td>
<td><span data-ttu-id="76b64-860">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-860">Assembly</span></span></td>
<td><span data-ttu-id="76b64-861">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-861">10001</span></span></td>
<td><span data-ttu-id="76b64-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-862">Electricity</span></span></td>
<td><span data-ttu-id="76b64-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-863">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="76b64-864">-713.75</span></span></td>
<td><span data-ttu-id="76b64-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-866">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-867">Product 1</span></span></td>
<td><span data-ttu-id="76b64-868">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-868">10001</span></span></td>
<td><span data-ttu-id="76b64-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-869">Electricity</span></span></td>
<td><span data-ttu-id="76b64-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-870">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-871">535.31</span><span class="sxs-lookup"><span data-stu-id="76b64-871">535.31</span></span></td>
<td><span data-ttu-id="76b64-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-873">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-874">Product 2</span></span></td>
<td><span data-ttu-id="76b64-875">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-875">10001</span></span></td>
<td><span data-ttu-id="76b64-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-876">Electricity</span></span></td>
<td><span data-ttu-id="76b64-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-877">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-878">178.44</span><span class="sxs-lookup"><span data-stu-id="76b64-878">178.44</span></span></td>
<td><span data-ttu-id="76b64-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-880">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-880">CC003</span></span></td>
<td><span data-ttu-id="76b64-881">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-881">Assembly</span></span></td>
<td><span data-ttu-id="76b64-882">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-882">10001</span></span></td>
<td><span data-ttu-id="76b64-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-883">Electricity</span></span></td>
<td><span data-ttu-id="76b64-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-884">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="76b64-885">-5,982.83</span></span></td>
<td><span data-ttu-id="76b64-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-887">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-888">Product 1</span></span></td>
<td><span data-ttu-id="76b64-889">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-889">10001</span></span></td>
<td><span data-ttu-id="76b64-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-890">Electricity</span></span></td>
<td><span data-ttu-id="76b64-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-891">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="76b64-892">4,487.12</span></span></td>
<td><span data-ttu-id="76b64-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-894">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-895">Product 2</span></span></td>
<td><span data-ttu-id="76b64-896">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-896">10001</span></span></td>
<td><span data-ttu-id="76b64-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-897">Electricity</span></span></td>
<td><span data-ttu-id="76b64-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-898">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="76b64-899">1,495.71</span></span></td>
<td><span data-ttu-id="76b64-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-901">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-901">CC003</span></span></td>
<td><span data-ttu-id="76b64-902">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-902">Assembly</span></span></td>
<td><span data-ttu-id="76b64-903">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-903">10001</span></span></td>
<td><span data-ttu-id="76b64-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-904">Electricity</span></span></td>
<td><span data-ttu-id="76b64-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-905">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="76b64-906">-286.25</span></span></td>
<td><span data-ttu-id="76b64-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-908">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-909">Product 1</span></span></td>
<td><span data-ttu-id="76b64-910">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-910">10001</span></span></td>
<td><span data-ttu-id="76b64-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-911">Electricity</span></span></td>
<td><span data-ttu-id="76b64-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-912">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-913">241.05</span><span class="sxs-lookup"><span data-stu-id="76b64-913">241.05</span></span></td>
<td><span data-ttu-id="76b64-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-915">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-916">Product 2</span></span></td>
<td><span data-ttu-id="76b64-917">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-917">10001</span></span></td>
<td><span data-ttu-id="76b64-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-918">Electricity</span></span></td>
<td><span data-ttu-id="76b64-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-919">Fixed cost</span></span></td>
<td><span data-ttu-id="76b64-920">45.20</span><span class="sxs-lookup"><span data-stu-id="76b64-920">45.20</span></span></td>
<td><span data-ttu-id="76b64-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-922">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-922">CC003</span></span></td>
<td><span data-ttu-id="76b64-923">Samling</span><span class="sxs-lookup"><span data-stu-id="76b64-923">Assembly</span></span></td>
<td><span data-ttu-id="76b64-924">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-924">10001</span></span></td>
<td><span data-ttu-id="76b64-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-925">Electricity</span></span></td>
<td><span data-ttu-id="76b64-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-926">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="76b64-927">-2,977.17</span></span></td>
<td><span data-ttu-id="76b64-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-929">Prod 1</span></span></td>
<td><span data-ttu-id="76b64-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="76b64-930">Product 1</span></span></td>
<td><span data-ttu-id="76b64-931">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-931">10001</span></span></td>
<td><span data-ttu-id="76b64-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-932">Electricity</span></span></td>
<td><span data-ttu-id="76b64-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-933">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="76b64-934">2,507.09</span></span></td>
<td><span data-ttu-id="76b64-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76b64-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-936">Prod 2</span></span></td>
<td><span data-ttu-id="76b64-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="76b64-937">Product 2</span></span></td>
<td><span data-ttu-id="76b64-938">10001</span><span class="sxs-lookup"><span data-stu-id="76b64-938">10001</span></span></td>
<td><span data-ttu-id="76b64-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-939">Electricity</span></span></td>
<td><span data-ttu-id="76b64-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-940">Variable cost</span></span></td>
<td><span data-ttu-id="76b64-941">470.08</span><span class="sxs-lookup"><span data-stu-id="76b64-941">470.08</span></span></td>
<td><span data-ttu-id="76b64-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="76b64-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="76b64-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="76b64-943">Conclusion</span></span>
<span data-ttu-id="76b64-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="76b64-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="76b64-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="76b64-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="76b64-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="76b64-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="76b64-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="76b64-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="76b64-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="76b64-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="76b64-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="76b64-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="76b64-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="76b64-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="76b64-951">CC099</span><span class="sxs-lookup"><span data-stu-id="76b64-951">CC099</span></span></th>
<th><span data-ttu-id="76b64-952">CC001</span><span class="sxs-lookup"><span data-stu-id="76b64-952">CC001</span></span></th>
<th><span data-ttu-id="76b64-953">CC002</span><span class="sxs-lookup"><span data-stu-id="76b64-953">CC002</span></span></th>
<th><span data-ttu-id="76b64-954">CC003</span><span class="sxs-lookup"><span data-stu-id="76b64-954">CC003</span></span></th>
<th><span data-ttu-id="76b64-955">CC004</span><span class="sxs-lookup"><span data-stu-id="76b64-955">CC004</span></span></th>
<th><span data-ttu-id="76b64-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="76b64-956">Proj 1</span></span></th>
<th><span data-ttu-id="76b64-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="76b64-957">Proj 2</span></span></th>
<th><span data-ttu-id="76b64-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="76b64-958">Prod 1</span></span></th>
<th><span data-ttu-id="76b64-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="76b64-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="76b64-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="76b64-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="76b64-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="76b64-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="76b64-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-971">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="76b64-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-973">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-974">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-975">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-976">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-977">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="76b64-978">776.36</span><span class="sxs-lookup"><span data-stu-id="76b64-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-979">223.64</span><span class="sxs-lookup"><span data-stu-id="76b64-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="76b64-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="76b64-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-982">000</span><span class="sxs-lookup"><span data-stu-id="76b64-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-983">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-984">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-985">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-986">0,00</span><span class="sxs-lookup"><span data-stu-id="76b64-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-987">30,00</span><span class="sxs-lookup"><span data-stu-id="76b64-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-988">10,00</span><span class="sxs-lookup"><span data-stu-id="76b64-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="76b64-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="76b64-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76b64-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="76b64-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="76b64-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="76b64-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="76b64-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="76b64-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="76b64-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="76b64-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="76b64-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="76b64-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="76b64-996">Du kan få flere oplysninger under [Omkostningstotaler](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="76b64-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



