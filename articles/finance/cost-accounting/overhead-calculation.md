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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770798"
---
# <a name="overhead-calculation"></a><span data-ttu-id="88db4-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88db4-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="88db4-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="88db4-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="88db4-105">Term definition</span></span>
---------------

<span data-ttu-id="88db4-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="88db4-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="88db4-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="88db4-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="88db4-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="88db4-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="88db4-109">Leje</span><span class="sxs-lookup"><span data-stu-id="88db4-109">Rent</span></span>
-   <span data-ttu-id="88db4-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-110">Electricity</span></span>
-   <span data-ttu-id="88db4-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="88db4-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="88db4-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-112">Overhead calculation overview</span></span>
<span data-ttu-id="88db4-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="88db4-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="88db4-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="88db4-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="88db4-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="88db4-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="88db4-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="88db4-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="88db4-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88db4-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="88db4-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="88db4-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="88db4-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="88db4-119">Version type</span></span>
-   <span data-ttu-id="88db4-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="88db4-120">Date and time</span></span>
-   <span data-ttu-id="88db4-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="88db4-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="88db4-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="88db4-122">Fiscal year</span></span>
-   <span data-ttu-id="88db4-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="88db4-123">Fiscal period</span></span>

<span data-ttu-id="88db4-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="88db4-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="88db4-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="88db4-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="88db4-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="88db4-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="88db4-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="88db4-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="88db4-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="88db4-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="88db4-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="88db4-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="88db4-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="88db4-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="88db4-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="88db4-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="88db4-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="88db4-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="88db4-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="88db4-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="88db4-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="88db4-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="88db4-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="88db4-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="88db4-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="88db4-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="88db4-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="88db4-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="88db4-140">Main account</span></span></th>
<th><span data-ttu-id="88db4-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="88db4-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="88db4-143">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-143">CC099</span></span></td>
<td><span data-ttu-id="88db4-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-144">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-145">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-145">10001</span></span></td>
<td><span data-ttu-id="88db4-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-146">Electricity</span></span></td>
<td><span data-ttu-id="88db4-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="88db4-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="88db4-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="88db4-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="88db4-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="88db4-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="88db4-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="88db4-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="88db4-151">Define the cost behavior rule</span></span>

<span data-ttu-id="88db4-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="88db4-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="88db4-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="88db4-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="88db4-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="88db4-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="88db4-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="88db4-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="88db4-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="88db4-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="88db4-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="88db4-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="88db4-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="88db4-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-160">Journal</span></span></th>
<th><span data-ttu-id="88db4-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="88db4-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88db4-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="88db4-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88db4-163">Version</span><span class="sxs-lookup"><span data-stu-id="88db4-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-164">00001</span><span class="sxs-lookup"><span data-stu-id="88db4-164">00001</span></span></td>
<td><span data-ttu-id="88db4-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="88db4-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="88db4-166">Fiscal</span></span></td>
<td><span data-ttu-id="88db4-167">2017</span><span class="sxs-lookup"><span data-stu-id="88db4-167">2017</span></span></td>
<td><span data-ttu-id="88db4-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="88db4-168">Period 1</span></span></td>
<td><span data-ttu-id="88db4-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="88db4-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="88db4-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="88db4-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-173">Cost element</span></span></th>
<th><span data-ttu-id="88db4-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-174">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="88db4-177">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-177">CC099</span></span></td>
<td><span data-ttu-id="88db4-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-178">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-179">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-179">10001</span></span></td>
<td><span data-ttu-id="88db4-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-180">Electricity</span></span></td>
<td><span data-ttu-id="88db4-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="88db4-181">Unclassified</span></span></td>
<td><span data-ttu-id="88db4-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88db4-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="88db4-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-185">Cost element</span></span></th>
<th><span data-ttu-id="88db4-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-186">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-187">Amount</span></span></th>
<th><span data-ttu-id="88db4-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-189">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-189">CC099</span></span></td>
<td><span data-ttu-id="88db4-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-190">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-191">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-191">10001</span></span></td>
<td><span data-ttu-id="88db4-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-192">Electricity</span></span></td>
<td><span data-ttu-id="88db4-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="88db4-193">Unclassified</span></span></td>
<td><span data-ttu-id="88db4-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-194">10,000.00</span></span></td>
<td><span data-ttu-id="88db4-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-196">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-196">CC099</span></span></td>
<td><span data-ttu-id="88db4-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-197">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-198">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-198">10001</span></span></td>
<td><span data-ttu-id="88db4-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-199">Electricity</span></span></td>
<td><span data-ttu-id="88db4-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="88db4-200">Unclassified</span></span></td>
<td><span data-ttu-id="88db4-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-201">-10,000.00</span></span></td>
<td><span data-ttu-id="88db4-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-203">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-203">CC099</span></span></td>
<td><span data-ttu-id="88db4-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-204">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-205">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-205">10001</span></span></td>
<td><span data-ttu-id="88db4-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-206">Electricity</span></span></td>
<td><span data-ttu-id="88db4-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-207">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-208">1,000.00</span></span></td>
<td><span data-ttu-id="88db4-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-210">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-210">CC099</span></span></td>
<td><span data-ttu-id="88db4-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-211">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-212">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-212">10001</span></span></td>
<td><span data-ttu-id="88db4-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-213">Electricity</span></span></td>
<td><span data-ttu-id="88db4-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-214">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-215">9,000.00</span></span></td>
<td><span data-ttu-id="88db4-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="88db4-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="88db4-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="88db4-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="88db4-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="88db4-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="88db4-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="88db4-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="88db4-221">Define the cost distribution rule</span></span>

<span data-ttu-id="88db4-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="88db4-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="88db4-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="88db4-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="88db4-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="88db4-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="88db4-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="88db4-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="88db4-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="88db4-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-228">Cost object</span></span></th>
<th><span data-ttu-id="88db4-229">KWh</span><span class="sxs-lookup"><span data-stu-id="88db4-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-230">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-230">CC001</span></span></td>
<td><span data-ttu-id="88db4-231">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-231">HR</span></span></td>
<td><span data-ttu-id="88db4-232">1.000</span><span class="sxs-lookup"><span data-stu-id="88db4-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-233">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-233">CC002</span></span></td>
<td><span data-ttu-id="88db4-234">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-234">Finance</span></span></td>
<td><span data-ttu-id="88db4-235">6.000</span><span class="sxs-lookup"><span data-stu-id="88db4-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-236">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-236">CC003</span></span></td>
<td><span data-ttu-id="88db4-237">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-237">Assembly</span></span></td>
<td><span data-ttu-id="88db4-238">0</span><span class="sxs-lookup"><span data-stu-id="88db4-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="88db4-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-240">Cost object</span></span></th>
<th><span data-ttu-id="88db4-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-241">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-242">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-244">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-244">CC001</span></span></td>
<td><span data-ttu-id="88db4-245">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-245">HR</span></span></td>
<td><span data-ttu-id="88db4-246">1.000</span><span class="sxs-lookup"><span data-stu-id="88db4-246">1,000</span></span></td>
<td><span data-ttu-id="88db4-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="88db4-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="88db4-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-249">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-249">CC002</span></span></td>
<td><span data-ttu-id="88db4-250">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-250">Finance</span></span></td>
<td><span data-ttu-id="88db4-251">6.000</span><span class="sxs-lookup"><span data-stu-id="88db4-251">6,000</span></span></td>
<td><span data-ttu-id="88db4-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="88db4-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="88db4-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-254">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-254">CC003</span></span></td>
<td><span data-ttu-id="88db4-255">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-255">Assembly</span></span></td>
<td><span data-ttu-id="88db4-256">0</span><span class="sxs-lookup"><span data-stu-id="88db4-256">0</span></span></td>
<td><span data-ttu-id="88db4-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="88db4-258">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="88db4-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="88db4-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="88db4-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-261">Cost object</span></span></th>
<th><span data-ttu-id="88db4-262">Formel</span><span class="sxs-lookup"><span data-stu-id="88db4-262">Formula</span></span></th>
<th><span data-ttu-id="88db4-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-263">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-264">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-266">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-266">CC001</span></span></td>
<td><span data-ttu-id="88db4-267">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-267">HR</span></span></td>
<td><span data-ttu-id="88db4-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="88db4-269">1</span><span class="sxs-lookup"><span data-stu-id="88db4-269">1</span></span></td>
<td><span data-ttu-id="88db4-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="88db4-271">500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-272">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-272">CC002</span></span></td>
<td><span data-ttu-id="88db4-273">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-273">Finance</span></span></td>
<td><span data-ttu-id="88db4-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="88db4-275">1</span><span class="sxs-lookup"><span data-stu-id="88db4-275">1</span></span></td>
<td><span data-ttu-id="88db4-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="88db4-277">500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-278">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-278">CC003</span></span></td>
<td><span data-ttu-id="88db4-279">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-279">Assembly</span></span></td>
<td><span data-ttu-id="88db4-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="88db4-281">0</span><span class="sxs-lookup"><span data-stu-id="88db4-281">0</span></span></td>
<td><span data-ttu-id="88db4-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="88db4-283">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="88db4-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-285">Journal</span></span></th>
<th><span data-ttu-id="88db4-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="88db4-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88db4-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="88db4-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88db4-288">Version</span><span class="sxs-lookup"><span data-stu-id="88db4-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-289">00002</span><span class="sxs-lookup"><span data-stu-id="88db4-289">00002</span></span></td>
<td><span data-ttu-id="88db4-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="88db4-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="88db4-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="88db4-291">Fiscal</span></span></td>
<td><span data-ttu-id="88db4-292">2017</span><span class="sxs-lookup"><span data-stu-id="88db4-292">2017</span></span></td>
<td><span data-ttu-id="88db4-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="88db4-293">Period 1</span></span></td>
<td><span data-ttu-id="88db4-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="88db4-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="88db4-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="88db4-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-298">Cost element</span></span></th>
<th><span data-ttu-id="88db4-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-299">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-302">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-302">CC099</span></span></td>
<td><span data-ttu-id="88db4-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-303">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-304">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-304">10001</span></span></td>
<td><span data-ttu-id="88db4-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-305">Electricity</span></span></td>
<td><span data-ttu-id="88db4-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-306">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-309">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-309">CC099</span></span></td>
<td><span data-ttu-id="88db4-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-310">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-311">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-311">10001</span></span></td>
<td><span data-ttu-id="88db4-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-312">Electricity</span></span></td>
<td><span data-ttu-id="88db4-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-313">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88db4-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="88db4-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-317">Cost element</span></span></th>
<th><span data-ttu-id="88db4-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-318">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-319">Amount</span></span></th>
<th><span data-ttu-id="88db4-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-321">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-321">CC099</span></span></td>
<td><span data-ttu-id="88db4-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-322">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-323">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-323">10001</span></span></td>
<td><span data-ttu-id="88db4-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-324">Electricity</span></span></td>
<td><span data-ttu-id="88db4-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-325">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-326">-1,000.00</span></span></td>
<td><span data-ttu-id="88db4-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-328">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-328">CC001</span></span></td>
<td><span data-ttu-id="88db4-329">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-329">HR</span></span></td>
<td><span data-ttu-id="88db4-330">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-330">10001</span></span></td>
<td><span data-ttu-id="88db4-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-331">Electricity</span></span></td>
<td><span data-ttu-id="88db4-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-332">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-333">500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-333">500.00</span></span></td>
<td><span data-ttu-id="88db4-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-335">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-335">CC002</span></span></td>
<td><span data-ttu-id="88db4-336">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-336">Finance</span></span></td>
<td><span data-ttu-id="88db4-337">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-337">10001</span></span></td>
<td><span data-ttu-id="88db4-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-338">Electricity</span></span></td>
<td><span data-ttu-id="88db4-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-339">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-340">500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-340">500.00</span></span></td>
<td><span data-ttu-id="88db4-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-342">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-342">CC099</span></span></td>
<td><span data-ttu-id="88db4-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="88db4-343">Default cost center</span></span></td>
<td><span data-ttu-id="88db4-344">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-344">10001</span></span></td>
<td><span data-ttu-id="88db4-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-345">Electricity</span></span></td>
<td><span data-ttu-id="88db4-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-346">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="88db4-347">-9,000.00</span></span></td>
<td><span data-ttu-id="88db4-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-349">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-349">CC001</span></span></td>
<td><span data-ttu-id="88db4-350">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-350">HR</span></span></td>
<td><span data-ttu-id="88db4-351">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-351">10001</span></span></td>
<td><span data-ttu-id="88db4-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-352">Electricity</span></span></td>
<td><span data-ttu-id="88db4-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-353">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="88db4-354">1,285.71</span></span></td>
<td><span data-ttu-id="88db4-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-356">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-356">CC002</span></span></td>
<td><span data-ttu-id="88db4-357">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-357">Finance</span></span></td>
<td><span data-ttu-id="88db4-358">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-358">10001</span></span></td>
<td><span data-ttu-id="88db4-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-359">Electricity</span></span></td>
<td><span data-ttu-id="88db4-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-360">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="88db4-361">7,714.29</span></span></td>
<td><span data-ttu-id="88db4-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="88db4-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="88db4-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="88db4-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="88db4-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="88db4-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="88db4-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="88db4-367">Define the overhead rate</span></span>

<span data-ttu-id="88db4-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="88db4-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="88db4-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-370">Cost object</span></span></th>
<th><span data-ttu-id="88db4-371">Timer</span><span class="sxs-lookup"><span data-stu-id="88db4-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-372">Proj 1</span></span></td>
<td><span data-ttu-id="88db4-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-373">Project 1</span></span></td>
<td><span data-ttu-id="88db4-374">3</span><span class="sxs-lookup"><span data-stu-id="88db4-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-375">Proj 2</span></span></td>
<td><span data-ttu-id="88db4-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-376">Project 2</span></span></td>
<td><span data-ttu-id="88db4-377">1</span><span class="sxs-lookup"><span data-stu-id="88db4-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="88db4-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-379">Cost object</span></span></th>
<th><span data-ttu-id="88db4-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-380">Cost element</span></span></th>
<th><span data-ttu-id="88db4-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-381">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="88db4-382">Units</span></span></th>
<th><span data-ttu-id="88db4-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="88db4-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-384">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-384">CC001</span></span></td>
<td><span data-ttu-id="88db4-385">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-385">HR</span></span></td>
<td><span data-ttu-id="88db4-386">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-386">10001</span></span></td>
<td><span data-ttu-id="88db4-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-387">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-388">1</span><span class="sxs-lookup"><span data-stu-id="88db4-388">1</span></span></td>
<td><span data-ttu-id="88db4-389">10</span><span class="sxs-lookup"><span data-stu-id="88db4-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-391">Cost object</span></span></th>
<th><span data-ttu-id="88db4-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-392">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-393">Cost element</span></span></th>
<th><span data-ttu-id="88db4-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-394">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-396">Proj 1</span></span></td>
<td><span data-ttu-id="88db4-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-397">Project 1</span></span></td>
<td><span data-ttu-id="88db4-398">3</span><span class="sxs-lookup"><span data-stu-id="88db4-398">3</span></span></td>
<td><span data-ttu-id="88db4-399">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-399">10001</span></span></td>
<td><span data-ttu-id="88db4-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="88db4-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="88db4-401">30,00</span><span class="sxs-lookup"><span data-stu-id="88db4-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-402">Proj 2</span></span></td>
<td><span data-ttu-id="88db4-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-403">Project 2</span></span></td>
<td><span data-ttu-id="88db4-404">1</span><span class="sxs-lookup"><span data-stu-id="88db4-404">1</span></span></td>
<td><span data-ttu-id="88db4-405">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-405">10001</span></span></td>
<td><span data-ttu-id="88db4-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="88db4-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="88db4-407">10,00</span><span class="sxs-lookup"><span data-stu-id="88db4-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="88db4-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-409">Journal</span></span></th>
<th><span data-ttu-id="88db4-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="88db4-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88db4-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="88db4-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88db4-412">Version</span><span class="sxs-lookup"><span data-stu-id="88db4-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-413">00003</span><span class="sxs-lookup"><span data-stu-id="88db4-413">00003</span></span></td>
<td><span data-ttu-id="88db4-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="88db4-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="88db4-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="88db4-415">Fiscal</span></span></td>
<td><span data-ttu-id="88db4-416">2017</span><span class="sxs-lookup"><span data-stu-id="88db4-416">2017</span></span></td>
<td><span data-ttu-id="88db4-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="88db4-417">Period 1</span></span></td>
<td><span data-ttu-id="88db4-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="88db4-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="88db4-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="88db4-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-421">Cost object</span></span></th>
<th><span data-ttu-id="88db4-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-424">Proj 1</span></span></td>
<td><span data-ttu-id="88db4-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="88db4-426">3,00</span><span class="sxs-lookup"><span data-stu-id="88db4-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-428">Proj 2</span></span></td>
<td><span data-ttu-id="88db4-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="88db4-430">1,00</span><span class="sxs-lookup"><span data-stu-id="88db4-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88db4-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="88db4-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-433">Cost element</span></span></th>
<th><span data-ttu-id="88db4-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-434">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-435">Amount</span></span></th>
<th><span data-ttu-id="88db4-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="88db4-437">CC0001</span></span></td>
<td><span data-ttu-id="88db4-438">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-438">HR</span></span></td>
<td><span data-ttu-id="88db4-439">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-439">10001</span></span></td>
<td><span data-ttu-id="88db4-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-440">Electricity</span></span></td>
<td><span data-ttu-id="88db4-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-441">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="88db4-442">-30.00</span></span></td>
<td><span data-ttu-id="88db4-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-444">Proj 1</span></span></td>
<td><span data-ttu-id="88db4-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="88db4-446">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-446">10001</span></span></td>
<td><span data-ttu-id="88db4-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-447">Electricity</span></span></td>
<td><span data-ttu-id="88db4-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-448">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-449">30,00</span><span class="sxs-lookup"><span data-stu-id="88db4-449">30.00</span></span></td>
<td><span data-ttu-id="88db4-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-451">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-451">CC001</span></span></td>
<td><span data-ttu-id="88db4-452">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-452">HR</span></span></td>
<td><span data-ttu-id="88db4-453">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-453">10001</span></span></td>
<td><span data-ttu-id="88db4-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-454">Electricity</span></span></td>
<td><span data-ttu-id="88db4-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-455">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="88db4-456">-10.00</span></span></td>
<td><span data-ttu-id="88db4-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-458">Proj 2</span></span></td>
<td><span data-ttu-id="88db4-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="88db4-460">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-460">10001</span></span></td>
<td><span data-ttu-id="88db4-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-461">Electricity</span></span></td>
<td><span data-ttu-id="88db4-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-462">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-463">10.00</span><span class="sxs-lookup"><span data-stu-id="88db4-463">10.00</span></span></td>
<td><span data-ttu-id="88db4-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="88db4-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="88db4-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="88db4-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="88db4-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="88db4-468">Finance understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="88db4-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="88db4-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="88db4-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="88db4-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="88db4-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="88db4-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="88db4-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="88db4-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="88db4-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="88db4-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="88db4-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="88db4-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="88db4-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="88db4-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="88db4-475">Define the cost allocation</span></span>

<span data-ttu-id="88db4-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="88db4-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="88db4-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="88db4-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="88db4-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-479">Cost object</span></span></th>
<th><span data-ttu-id="88db4-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="88db4-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-481">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-481">CC002</span></span></td>
<td><span data-ttu-id="88db4-482">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-482">Finance</span></span></td>
<td><span data-ttu-id="88db4-483">35</span><span class="sxs-lookup"><span data-stu-id="88db4-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-484">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-484">CC003</span></span></td>
<td><span data-ttu-id="88db4-485">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-485">Assembly</span></span></td>
<td><span data-ttu-id="88db4-486">55</span><span class="sxs-lookup"><span data-stu-id="88db4-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-487">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-487">CC004</span></span></td>
<td><span data-ttu-id="88db4-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-488">Packaging</span></span></td>
<td><span data-ttu-id="88db4-489">10</span><span class="sxs-lookup"><span data-stu-id="88db4-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="88db4-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="88db4-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-492">Cost object</span></span></th>
<th><span data-ttu-id="88db4-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="88db4-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-494">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-494">CC003</span></span></td>
<td><span data-ttu-id="88db4-495">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-495">Assembly</span></span></td>
<td><span data-ttu-id="88db4-496">65</span><span class="sxs-lookup"><span data-stu-id="88db4-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-497">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-497">CC004</span></span></td>
<td><span data-ttu-id="88db4-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-498">Packaging</span></span></td>
<td><span data-ttu-id="88db4-499">35</span><span class="sxs-lookup"><span data-stu-id="88db4-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="88db4-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="88db4-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-502">Cost object</span></span></th>
<th><span data-ttu-id="88db4-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="88db4-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-504">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-505">Product 1</span></span></td>
<td><span data-ttu-id="88db4-506">60</span><span class="sxs-lookup"><span data-stu-id="88db4-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-507">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-508">Product 2</span></span></td>
<td><span data-ttu-id="88db4-509">20</span><span class="sxs-lookup"><span data-stu-id="88db4-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="88db4-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="88db4-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-512">Cost object</span></span></th>
<th><span data-ttu-id="88db4-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="88db4-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-514">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-515">Product 1</span></span></td>
<td><span data-ttu-id="88db4-516">80</span><span class="sxs-lookup"><span data-stu-id="88db4-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-517">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-518">Product 2</span></span></td>
<td><span data-ttu-id="88db4-519">15</span><span class="sxs-lookup"><span data-stu-id="88db4-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="88db4-520">Statistiske målinger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="88db4-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="88db4-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="88db4-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="88db4-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="88db4-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-523">Cost object</span></span></th>
<th><span data-ttu-id="88db4-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-524">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-525">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-526">Amount</span></span></th>
<th><span data-ttu-id="88db4-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-528">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-528">CC002</span></span></td>
<td><span data-ttu-id="88db4-529">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-529">Finance</span></span></td>
<td><span data-ttu-id="88db4-530">35</span><span class="sxs-lookup"><span data-stu-id="88db4-530">35</span></span></td>
<td><span data-ttu-id="88db4-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="88db4-532">175.00</span><span class="sxs-lookup"><span data-stu-id="88db4-532">175.00</span></span></td>
<td><span data-ttu-id="88db4-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-534">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-534">CC003</span></span></td>
<td><span data-ttu-id="88db4-535">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-535">Assembly</span></span></td>
<td><span data-ttu-id="88db4-536">55</span><span class="sxs-lookup"><span data-stu-id="88db4-536">55</span></span></td>
<td><span data-ttu-id="88db4-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="88db4-538">275.00</span><span class="sxs-lookup"><span data-stu-id="88db4-538">275.00</span></span></td>
<td><span data-ttu-id="88db4-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-540">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-540">CC004</span></span></td>
<td><span data-ttu-id="88db4-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-541">Packaging</span></span></td>
<td><span data-ttu-id="88db4-542">10</span><span class="sxs-lookup"><span data-stu-id="88db4-542">10</span></span></td>
<td><span data-ttu-id="88db4-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="88db4-544">50,00</span><span class="sxs-lookup"><span data-stu-id="88db4-544">50.00</span></span></td>
<td><span data-ttu-id="88db4-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-546">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-546">CC002</span></span></td>
<td><span data-ttu-id="88db4-547">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-547">Finance</span></span></td>
<td><span data-ttu-id="88db4-548">35</span><span class="sxs-lookup"><span data-stu-id="88db4-548">35</span></span></td>
<td><span data-ttu-id="88db4-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="88db4-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="88db4-550">436.00</span><span class="sxs-lookup"><span data-stu-id="88db4-550">436.00</span></span></td>
<td><span data-ttu-id="88db4-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-552">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-552">CC003</span></span></td>
<td><span data-ttu-id="88db4-553">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-553">Assembly</span></span></td>
<td><span data-ttu-id="88db4-554">55</span><span class="sxs-lookup"><span data-stu-id="88db4-554">55</span></span></td>
<td><span data-ttu-id="88db4-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="88db4-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="88db4-556">685.14</span><span class="sxs-lookup"><span data-stu-id="88db4-556">685.14</span></span></td>
<td><span data-ttu-id="88db4-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-558">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-558">CC004</span></span></td>
<td><span data-ttu-id="88db4-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-559">Packaging</span></span></td>
<td><span data-ttu-id="88db4-560">10</span><span class="sxs-lookup"><span data-stu-id="88db4-560">10</span></span></td>
<td><span data-ttu-id="88db4-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="88db4-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="88db4-562">124.57</span><span class="sxs-lookup"><span data-stu-id="88db4-562">124.57</span></span></td>
<td><span data-ttu-id="88db4-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="88db4-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-565">Cost object</span></span></th>
<th><span data-ttu-id="88db4-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-566">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-567">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-568">Amount</span></span></th>
<th><span data-ttu-id="88db4-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-570">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-570">CC003</span></span></td>
<td><span data-ttu-id="88db4-571">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-571">Assembly</span></span></td>
<td><span data-ttu-id="88db4-572">65</span><span class="sxs-lookup"><span data-stu-id="88db4-572">65</span></span></td>
<td><span data-ttu-id="88db4-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="88db4-574">438.75</span><span class="sxs-lookup"><span data-stu-id="88db4-574">438.75</span></span></td>
<td><span data-ttu-id="88db4-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-576">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-576">CC004</span></span></td>
<td><span data-ttu-id="88db4-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-577">Packaging</span></span></td>
<td><span data-ttu-id="88db4-578">35</span><span class="sxs-lookup"><span data-stu-id="88db4-578">35</span></span></td>
<td><span data-ttu-id="88db4-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="88db4-580">236.25</span><span class="sxs-lookup"><span data-stu-id="88db4-580">236.25</span></span></td>
<td><span data-ttu-id="88db4-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-582">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-582">CC003</span></span></td>
<td><span data-ttu-id="88db4-583">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-583">Assembly</span></span></td>
<td><span data-ttu-id="88db4-584">65</span><span class="sxs-lookup"><span data-stu-id="88db4-584">65</span></span></td>
<td><span data-ttu-id="88db4-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="88db4-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="88db4-586">5,297.69</span></span></td>
<td><span data-ttu-id="88db4-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-588">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-588">CC004</span></span></td>
<td><span data-ttu-id="88db4-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-589">Packaging</span></span></td>
<td><span data-ttu-id="88db4-590">35</span><span class="sxs-lookup"><span data-stu-id="88db4-590">35</span></span></td>
<td><span data-ttu-id="88db4-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="88db4-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="88db4-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="88db4-592">2,852.60</span></span></td>
<td><span data-ttu-id="88db4-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="88db4-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-595">Cost object</span></span></th>
<th><span data-ttu-id="88db4-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-596">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-597">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-598">Amount</span></span></th>
<th><span data-ttu-id="88db4-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-600">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-601">Product 1</span></span></td>
<td><span data-ttu-id="88db4-602">60</span><span class="sxs-lookup"><span data-stu-id="88db4-602">60</span></span></td>
<td><span data-ttu-id="88db4-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="88db4-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="88db4-604">535.31</span><span class="sxs-lookup"><span data-stu-id="88db4-604">535.31</span></span></td>
<td><span data-ttu-id="88db4-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-606">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-607">Product 2</span></span></td>
<td><span data-ttu-id="88db4-608">20</span><span class="sxs-lookup"><span data-stu-id="88db4-608">20</span></span></td>
<td><span data-ttu-id="88db4-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="88db4-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="88db4-610">178.44</span><span class="sxs-lookup"><span data-stu-id="88db4-610">178.44</span></span></td>
<td><span data-ttu-id="88db4-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-612">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-613">Product 1</span></span></td>
<td><span data-ttu-id="88db4-614">60</span><span class="sxs-lookup"><span data-stu-id="88db4-614">60</span></span></td>
<td><span data-ttu-id="88db4-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="88db4-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="88db4-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="88db4-616">4,487.12</span></span></td>
<td><span data-ttu-id="88db4-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-618">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-619">Product 2</span></span></td>
<td><span data-ttu-id="88db4-620">20</span><span class="sxs-lookup"><span data-stu-id="88db4-620">20</span></span></td>
<td><span data-ttu-id="88db4-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="88db4-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="88db4-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="88db4-622">1,495.71</span></span></td>
<td><span data-ttu-id="88db4-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88db4-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="88db4-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-625">Cost object</span></span></th>
<th><span data-ttu-id="88db4-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="88db4-626">Magnitude</span></span></th>
<th><span data-ttu-id="88db4-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="88db4-627">Allocation factor</span></span></th>
<th><span data-ttu-id="88db4-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-628">Amount</span></span></th>
<th><span data-ttu-id="88db4-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-630">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-631">Product 1</span></span></td>
<td><span data-ttu-id="88db4-632">80</span><span class="sxs-lookup"><span data-stu-id="88db4-632">80</span></span></td>
<td><span data-ttu-id="88db4-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="88db4-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="88db4-634">241.05</span><span class="sxs-lookup"><span data-stu-id="88db4-634">241.05</span></span></td>
<td><span data-ttu-id="88db4-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-636">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-637">Product 2</span></span></td>
<td><span data-ttu-id="88db4-638">15</span><span class="sxs-lookup"><span data-stu-id="88db4-638">15</span></span></td>
<td><span data-ttu-id="88db4-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="88db4-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="88db4-640">45.20</span><span class="sxs-lookup"><span data-stu-id="88db4-640">45.20</span></span></td>
<td><span data-ttu-id="88db4-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-642">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-643">Product 1</span></span></td>
<td><span data-ttu-id="88db4-644">80</span><span class="sxs-lookup"><span data-stu-id="88db4-644">80</span></span></td>
<td><span data-ttu-id="88db4-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="88db4-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="88db4-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="88db4-646">2,507.09</span></span></td>
<td><span data-ttu-id="88db4-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-648">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-649">Product 2</span></span></td>
<td><span data-ttu-id="88db4-650">15</span><span class="sxs-lookup"><span data-stu-id="88db4-650">15</span></span></td>
<td><span data-ttu-id="88db4-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="88db4-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="88db4-652">470.08</span><span class="sxs-lookup"><span data-stu-id="88db4-652">470.08</span></span></td>
<td><span data-ttu-id="88db4-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="88db4-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="88db4-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="88db4-655">Journal</span></span></th>
<th><span data-ttu-id="88db4-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="88db4-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88db4-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="88db4-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88db4-658">Version</span><span class="sxs-lookup"><span data-stu-id="88db4-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-659">00004</span><span class="sxs-lookup"><span data-stu-id="88db4-659">00004</span></span></td>
<td><span data-ttu-id="88db4-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="88db4-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="88db4-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="88db4-661">Fiscal</span></span></td>
<td><span data-ttu-id="88db4-662">2017</span><span class="sxs-lookup"><span data-stu-id="88db4-662">2017</span></span></td>
<td><span data-ttu-id="88db4-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="88db4-663">Period 1</span></span></td>
<td><span data-ttu-id="88db4-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="88db4-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="88db4-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="88db4-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88db4-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-668">Cost element</span></span></th>
<th><span data-ttu-id="88db4-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-669">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-672">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-672">CC001</span></span></td>
<td><span data-ttu-id="88db4-673">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-673">HR</span></span></td>
<td><span data-ttu-id="88db4-674">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-674">10001</span></span></td>
<td><span data-ttu-id="88db4-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-675">Electricity</span></span></td>
<td><span data-ttu-id="88db4-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-676">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-677">500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-679">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-679">CC001</span></span></td>
<td><span data-ttu-id="88db4-680">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-680">HR</span></span></td>
<td><span data-ttu-id="88db4-681">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-681">10001</span></span></td>
<td><span data-ttu-id="88db4-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-682">Electricity</span></span></td>
<td><span data-ttu-id="88db4-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-683">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="88db4-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-686">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-686">CC002</span></span></td>
<td><span data-ttu-id="88db4-687">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-687">Finance</span></span></td>
<td><span data-ttu-id="88db4-688">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-688">10001</span></span></td>
<td><span data-ttu-id="88db4-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-689">Electricity</span></span></td>
<td><span data-ttu-id="88db4-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-690">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-691">675.00</span><span class="sxs-lookup"><span data-stu-id="88db4-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-693">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-693">CC002</span></span></td>
<td><span data-ttu-id="88db4-694">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-694">Finance</span></span></td>
<td><span data-ttu-id="88db4-695">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-695">10001</span></span></td>
<td><span data-ttu-id="88db4-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-696">Electricity</span></span></td>
<td><span data-ttu-id="88db4-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-697">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="88db4-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-700">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-700">CC003</span></span></td>
<td><span data-ttu-id="88db4-701">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-701">Assembly</span></span></td>
<td><span data-ttu-id="88db4-702">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-702">10001</span></span></td>
<td><span data-ttu-id="88db4-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-703">Electricity</span></span></td>
<td><span data-ttu-id="88db4-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-704">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-705">713.75</span><span class="sxs-lookup"><span data-stu-id="88db4-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-707">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-707">CC003</span></span></td>
<td><span data-ttu-id="88db4-708">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-708">Assembly</span></span></td>
<td><span data-ttu-id="88db4-709">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-709">10001</span></span></td>
<td><span data-ttu-id="88db4-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-710">Electricity</span></span></td>
<td><span data-ttu-id="88db4-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-711">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="88db4-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-714">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-714">CC003</span></span></td>
<td><span data-ttu-id="88db4-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-715">Packaging</span></span></td>
<td><span data-ttu-id="88db4-716">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-716">10001</span></span></td>
<td><span data-ttu-id="88db4-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-717">Electricity</span></span></td>
<td><span data-ttu-id="88db4-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-718">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-719">286.25</span><span class="sxs-lookup"><span data-stu-id="88db4-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-721">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-721">CC003</span></span></td>
<td><span data-ttu-id="88db4-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-722">Packaging</span></span></td>
<td><span data-ttu-id="88db4-723">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-723">10001</span></span></td>
<td><span data-ttu-id="88db4-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-724">Electricity</span></span></td>
<td><span data-ttu-id="88db4-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-725">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="88db4-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-728">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-729">Product 1</span></span></td>
<td><span data-ttu-id="88db4-730">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-730">10001</span></span></td>
<td><span data-ttu-id="88db4-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-731">Electricity</span></span></td>
<td><span data-ttu-id="88db4-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-732">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-733">776.36</span><span class="sxs-lookup"><span data-stu-id="88db4-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-735">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-736">Product 1</span></span></td>
<td><span data-ttu-id="88db4-737">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-737">10001</span></span></td>
<td><span data-ttu-id="88db4-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-738">Electricity</span></span></td>
<td><span data-ttu-id="88db4-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-739">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="88db4-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-742">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-743">Product 1</span></span></td>
<td><span data-ttu-id="88db4-744">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-744">10001</span></span></td>
<td><span data-ttu-id="88db4-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-745">Electricity</span></span></td>
<td><span data-ttu-id="88db4-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-746">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-747">223.64</span><span class="sxs-lookup"><span data-stu-id="88db4-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="88db4-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-749">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-750">Product 1</span></span></td>
<td><span data-ttu-id="88db4-751">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-751">10001</span></span></td>
<td><span data-ttu-id="88db4-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-752">Electricity</span></span></td>
<td><span data-ttu-id="88db4-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-753">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="88db4-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88db4-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="88db4-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88db4-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88db4-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-757">Cost element</span></span></th>
<th><span data-ttu-id="88db4-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-758">Cost behavior</span></span></th>
<th><span data-ttu-id="88db4-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="88db4-759">Amount</span></span></th>
<th><span data-ttu-id="88db4-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="88db4-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88db4-761">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-761">CC001</span></span></td>
<td><span data-ttu-id="88db4-762">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-762">HR</span></span></td>
<td><span data-ttu-id="88db4-763">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-763">10001</span></span></td>
<td><span data-ttu-id="88db4-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-764">Electricity</span></span></td>
<td><span data-ttu-id="88db4-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-765">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="88db4-766">-500.00</span></span></td>
<td><span data-ttu-id="88db4-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-768">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-768">CC002</span></span></td>
<td><span data-ttu-id="88db4-769">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-769">Finance</span></span></td>
<td><span data-ttu-id="88db4-770">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-770">10001</span></span></td>
<td><span data-ttu-id="88db4-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-771">Electricity</span></span></td>
<td><span data-ttu-id="88db4-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-772">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-773">175.00</span><span class="sxs-lookup"><span data-stu-id="88db4-773">175.00</span></span></td>
<td><span data-ttu-id="88db4-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-775">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-775">CC003</span></span></td>
<td><span data-ttu-id="88db4-776">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-776">Assembly</span></span></td>
<td><span data-ttu-id="88db4-777">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-777">10001</span></span></td>
<td><span data-ttu-id="88db4-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-778">Electricity</span></span></td>
<td><span data-ttu-id="88db4-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-779">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-780">275.00</span><span class="sxs-lookup"><span data-stu-id="88db4-780">275.00</span></span></td>
<td><span data-ttu-id="88db4-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-782">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-782">CC004</span></span></td>
<td><span data-ttu-id="88db4-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-783">Packaging</span></span></td>
<td><span data-ttu-id="88db4-784">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-784">10001</span></span></td>
<td><span data-ttu-id="88db4-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-785">Electricity</span></span></td>
<td><span data-ttu-id="88db4-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-786">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-787">50,00</span><span class="sxs-lookup"><span data-stu-id="88db4-787">50,00</span></span></td>
<td><span data-ttu-id="88db4-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-789">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-789">CC001</span></span></td>
<td><span data-ttu-id="88db4-790">Personale</span><span class="sxs-lookup"><span data-stu-id="88db4-790">HR</span></span></td>
<td><span data-ttu-id="88db4-791">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-791">10001</span></span></td>
<td><span data-ttu-id="88db4-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-792">Electricity</span></span></td>
<td><span data-ttu-id="88db4-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-793">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="88db4-794">-1,245.71</span></span></td>
<td><span data-ttu-id="88db4-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-796">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-796">CC002</span></span></td>
<td><span data-ttu-id="88db4-797">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-797">Finance</span></span></td>
<td><span data-ttu-id="88db4-798">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-798">10001</span></span></td>
<td><span data-ttu-id="88db4-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-799">Electricity</span></span></td>
<td><span data-ttu-id="88db4-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-800">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-801">436.00</span><span class="sxs-lookup"><span data-stu-id="88db4-801">436.00</span></span></td>
<td><span data-ttu-id="88db4-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-803">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-803">CC003</span></span></td>
<td><span data-ttu-id="88db4-804">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-804">Assembly</span></span></td>
<td><span data-ttu-id="88db4-805">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-805">10001</span></span></td>
<td><span data-ttu-id="88db4-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-806">Electricity</span></span></td>
<td><span data-ttu-id="88db4-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-807">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-808">685.14</span><span class="sxs-lookup"><span data-stu-id="88db4-808">685.14</span></span></td>
<td><span data-ttu-id="88db4-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-810">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-810">CC004</span></span></td>
<td><span data-ttu-id="88db4-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-811">Packaging</span></span></td>
<td><span data-ttu-id="88db4-812">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-812">10001</span></span></td>
<td><span data-ttu-id="88db4-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-813">Electricity</span></span></td>
<td><span data-ttu-id="88db4-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-814">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-815">124.57</span><span class="sxs-lookup"><span data-stu-id="88db4-815">124.57</span></span></td>
<td><span data-ttu-id="88db4-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-817">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-817">CC002</span></span></td>
<td><span data-ttu-id="88db4-818">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-818">Finance</span></span></td>
<td><span data-ttu-id="88db4-819">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-819">10001</span></span></td>
<td><span data-ttu-id="88db4-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-820">Electricity</span></span></td>
<td><span data-ttu-id="88db4-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-821">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="88db4-822">-675.00</span></span></td>
<td><span data-ttu-id="88db4-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-824">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-824">CC003</span></span></td>
<td><span data-ttu-id="88db4-825">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-825">Assembly</span></span></td>
<td><span data-ttu-id="88db4-826">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-826">10001</span></span></td>
<td><span data-ttu-id="88db4-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-827">Electricity</span></span></td>
<td><span data-ttu-id="88db4-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-828">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-829">438.75</span><span class="sxs-lookup"><span data-stu-id="88db4-829">438.75</span></span></td>
<td><span data-ttu-id="88db4-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-831">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-831">CC004</span></span></td>
<td><span data-ttu-id="88db4-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-832">Packaging</span></span></td>
<td><span data-ttu-id="88db4-833">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-833">10001</span></span></td>
<td><span data-ttu-id="88db4-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-834">Electricity</span></span></td>
<td><span data-ttu-id="88db4-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-835">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-836">236.25</span><span class="sxs-lookup"><span data-stu-id="88db4-836">236.25</span></span></td>
<td><span data-ttu-id="88db4-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-838">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-838">CC002</span></span></td>
<td><span data-ttu-id="88db4-839">Finans</span><span class="sxs-lookup"><span data-stu-id="88db4-839">Finance</span></span></td>
<td><span data-ttu-id="88db4-840">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-840">10001</span></span></td>
<td><span data-ttu-id="88db4-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-841">Electricity</span></span></td>
<td><span data-ttu-id="88db4-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-842">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="88db4-843">-8,150.29</span></span></td>
<td><span data-ttu-id="88db4-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-845">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-845">CC003</span></span></td>
<td><span data-ttu-id="88db4-846">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-846">Assembly</span></span></td>
<td><span data-ttu-id="88db4-847">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-847">10001</span></span></td>
<td><span data-ttu-id="88db4-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-848">Electricity</span></span></td>
<td><span data-ttu-id="88db4-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-849">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="88db4-850">5,297.69</span></span></td>
<td><span data-ttu-id="88db4-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-852">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-852">CC004</span></span></td>
<td><span data-ttu-id="88db4-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="88db4-853">Packaging</span></span></td>
<td><span data-ttu-id="88db4-854">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-854">10001</span></span></td>
<td><span data-ttu-id="88db4-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-855">Electricity</span></span></td>
<td><span data-ttu-id="88db4-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-856">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="88db4-857">2,852.60</span></span></td>
<td><span data-ttu-id="88db4-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-859">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-859">CC003</span></span></td>
<td><span data-ttu-id="88db4-860">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-860">Assembly</span></span></td>
<td><span data-ttu-id="88db4-861">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-861">10001</span></span></td>
<td><span data-ttu-id="88db4-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-862">Electricity</span></span></td>
<td><span data-ttu-id="88db4-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-863">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="88db4-864">-713.75</span></span></td>
<td><span data-ttu-id="88db4-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-866">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-867">Product 1</span></span></td>
<td><span data-ttu-id="88db4-868">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-868">10001</span></span></td>
<td><span data-ttu-id="88db4-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-869">Electricity</span></span></td>
<td><span data-ttu-id="88db4-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-870">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-871">535.31</span><span class="sxs-lookup"><span data-stu-id="88db4-871">535.31</span></span></td>
<td><span data-ttu-id="88db4-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-873">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-874">Product 2</span></span></td>
<td><span data-ttu-id="88db4-875">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-875">10001</span></span></td>
<td><span data-ttu-id="88db4-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-876">Electricity</span></span></td>
<td><span data-ttu-id="88db4-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-877">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-878">178.44</span><span class="sxs-lookup"><span data-stu-id="88db4-878">178.44</span></span></td>
<td><span data-ttu-id="88db4-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-880">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-880">CC003</span></span></td>
<td><span data-ttu-id="88db4-881">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-881">Assembly</span></span></td>
<td><span data-ttu-id="88db4-882">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-882">10001</span></span></td>
<td><span data-ttu-id="88db4-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-883">Electricity</span></span></td>
<td><span data-ttu-id="88db4-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-884">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="88db4-885">-5,982.83</span></span></td>
<td><span data-ttu-id="88db4-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-887">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-888">Product 1</span></span></td>
<td><span data-ttu-id="88db4-889">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-889">10001</span></span></td>
<td><span data-ttu-id="88db4-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-890">Electricity</span></span></td>
<td><span data-ttu-id="88db4-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-891">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="88db4-892">4,487.12</span></span></td>
<td><span data-ttu-id="88db4-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-894">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-895">Product 2</span></span></td>
<td><span data-ttu-id="88db4-896">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-896">10001</span></span></td>
<td><span data-ttu-id="88db4-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-897">Electricity</span></span></td>
<td><span data-ttu-id="88db4-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-898">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="88db4-899">1,495.71</span></span></td>
<td><span data-ttu-id="88db4-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-901">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-901">CC003</span></span></td>
<td><span data-ttu-id="88db4-902">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-902">Assembly</span></span></td>
<td><span data-ttu-id="88db4-903">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-903">10001</span></span></td>
<td><span data-ttu-id="88db4-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-904">Electricity</span></span></td>
<td><span data-ttu-id="88db4-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-905">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="88db4-906">-286.25</span></span></td>
<td><span data-ttu-id="88db4-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-908">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-909">Product 1</span></span></td>
<td><span data-ttu-id="88db4-910">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-910">10001</span></span></td>
<td><span data-ttu-id="88db4-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-911">Electricity</span></span></td>
<td><span data-ttu-id="88db4-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-912">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-913">241.05</span><span class="sxs-lookup"><span data-stu-id="88db4-913">241.05</span></span></td>
<td><span data-ttu-id="88db4-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-915">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-916">Product 2</span></span></td>
<td><span data-ttu-id="88db4-917">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-917">10001</span></span></td>
<td><span data-ttu-id="88db4-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-918">Electricity</span></span></td>
<td><span data-ttu-id="88db4-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-919">Fixed cost</span></span></td>
<td><span data-ttu-id="88db4-920">45.20</span><span class="sxs-lookup"><span data-stu-id="88db4-920">45.20</span></span></td>
<td><span data-ttu-id="88db4-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-922">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-922">CC003</span></span></td>
<td><span data-ttu-id="88db4-923">Samling</span><span class="sxs-lookup"><span data-stu-id="88db4-923">Assembly</span></span></td>
<td><span data-ttu-id="88db4-924">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-924">10001</span></span></td>
<td><span data-ttu-id="88db4-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-925">Electricity</span></span></td>
<td><span data-ttu-id="88db4-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-926">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="88db4-927">-2,977.17</span></span></td>
<td><span data-ttu-id="88db4-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-929">Prod 1</span></span></td>
<td><span data-ttu-id="88db4-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="88db4-930">Product 1</span></span></td>
<td><span data-ttu-id="88db4-931">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-931">10001</span></span></td>
<td><span data-ttu-id="88db4-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-932">Electricity</span></span></td>
<td><span data-ttu-id="88db4-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-933">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="88db4-934">2,507.09</span></span></td>
<td><span data-ttu-id="88db4-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88db4-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-936">Prod 2</span></span></td>
<td><span data-ttu-id="88db4-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="88db4-937">Product 2</span></span></td>
<td><span data-ttu-id="88db4-938">10001</span><span class="sxs-lookup"><span data-stu-id="88db4-938">10001</span></span></td>
<td><span data-ttu-id="88db4-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-939">Electricity</span></span></td>
<td><span data-ttu-id="88db4-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-940">Variable cost</span></span></td>
<td><span data-ttu-id="88db4-941">470.08</span><span class="sxs-lookup"><span data-stu-id="88db4-941">470.08</span></span></td>
<td><span data-ttu-id="88db4-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="88db4-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="88db4-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="88db4-943">Conclusion</span></span>
<span data-ttu-id="88db4-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="88db4-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="88db4-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="88db4-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="88db4-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="88db4-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="88db4-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="88db4-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="88db4-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="88db4-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="88db4-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="88db4-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="88db4-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="88db4-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="88db4-951">CC099</span><span class="sxs-lookup"><span data-stu-id="88db4-951">CC099</span></span></th>
<th><span data-ttu-id="88db4-952">CC001</span><span class="sxs-lookup"><span data-stu-id="88db4-952">CC001</span></span></th>
<th><span data-ttu-id="88db4-953">CC002</span><span class="sxs-lookup"><span data-stu-id="88db4-953">CC002</span></span></th>
<th><span data-ttu-id="88db4-954">CC003</span><span class="sxs-lookup"><span data-stu-id="88db4-954">CC003</span></span></th>
<th><span data-ttu-id="88db4-955">CC004</span><span class="sxs-lookup"><span data-stu-id="88db4-955">CC004</span></span></th>
<th><span data-ttu-id="88db4-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="88db4-956">Proj 1</span></span></th>
<th><span data-ttu-id="88db4-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="88db4-957">Proj 2</span></span></th>
<th><span data-ttu-id="88db4-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="88db4-958">Prod 1</span></span></th>
<th><span data-ttu-id="88db4-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="88db4-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="88db4-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="88db4-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="88db4-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="88db4-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="88db4-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-971">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="88db4-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-973">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-974">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-975">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-976">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-977">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="88db4-978">776.36</span><span class="sxs-lookup"><span data-stu-id="88db4-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-979">223.64</span><span class="sxs-lookup"><span data-stu-id="88db4-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="88db4-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="88db4-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-982">000</span><span class="sxs-lookup"><span data-stu-id="88db4-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-983">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-984">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-985">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-986">0,00</span><span class="sxs-lookup"><span data-stu-id="88db4-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-987">30,00</span><span class="sxs-lookup"><span data-stu-id="88db4-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-988">10,00</span><span class="sxs-lookup"><span data-stu-id="88db4-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="88db4-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="88db4-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88db4-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="88db4-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="88db4-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="88db4-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="88db4-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="88db4-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="88db4-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="88db4-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="88db4-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="88db4-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="88db4-996">Du kan finde flere oplysninger i [Politikken for omkostningsakkumulering og beregning af indirekte omkostninger](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="88db4-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



