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
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841483"
---
# <a name="overhead-calculation"></a><span data-ttu-id="ba7e6-103">Beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba7e6-104">I dette emne beskrives de typiske processer til beregning og tildeling af faste omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="ba7e6-105">Definition af begrebet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-105">Term definition</span></span>
---------------

<span data-ttu-id="ba7e6-106">Faste omkostninger er de omkostninger, der er forbundet med at drive et firma, men som ikke direkte kan henføres til nogen specifikke aktiviteter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ba7e6-107">Faste omkostninger giver vigtig understøttelse til generering af aktiviteter, der kan skabe fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ba7e6-108">Følgende er eksempler på faste omkostninger:</span><span class="sxs-lookup"><span data-stu-id="ba7e6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ba7e6-109">Leje</span><span class="sxs-lookup"><span data-stu-id="ba7e6-109">Rent</span></span>
-   <span data-ttu-id="ba7e6-110">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-110">Electricity</span></span>
-   <span data-ttu-id="ba7e6-111">Administrative lønninger</span><span class="sxs-lookup"><span data-stu-id="ba7e6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ba7e6-112">Oversigt over beregning af fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-112">Overhead calculation overview</span></span>
<span data-ttu-id="ba7e6-113">Beregning af faste omkostninger kører politikker for omkostningsregnskab i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ba7e6-114">Hvis politikker for omkostningsregnskab er blevet ændret, eller der er fundet specifikke fejl, kan du køre beregning af faste omkostninger flere gange for den samme regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ba7e6-115">De enkelte kørsler af beregningen af faste omkostninger gemmes og modtager et entydigt versions-ID, som du kan bruge til at sammenligne beregningerne i forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ba7e6-116">De omkostningsposter, der genereres af beregningen af faste omkostninger, modtager en regnskabsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ba7e6-117">Denne regnskabsdato svarer til slutdatoen for den regnskabsperiode, der bruges i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ba7e6-118">Det entydige versions-id består af følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="ba7e6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ba7e6-119">Versionstype</span><span class="sxs-lookup"><span data-stu-id="ba7e6-119">Version type</span></span>
-   <span data-ttu-id="ba7e6-120">Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-120">Date and time</span></span>
-   <span data-ttu-id="ba7e6-121">Finanspost for omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="ba7e6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ba7e6-122">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ba7e6-122">Fiscal year</span></span>
-   <span data-ttu-id="ba7e6-123">Regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-123">Fiscal period</span></span>

<span data-ttu-id="ba7e6-124">Beregning af faste omkostninger køres uafhængigt af versionen.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ba7e6-125">Derfor kan du beregne Budget-versionen før den faktiske version.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ba7e6-126">Beregning af faste omkostninger består af fire trin, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ba7e6-127">I hvert trin oprettes der et kladdehoved med poster.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ba7e6-128">Dette kladdehoved indeholder inddataene for hvert trin i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ba7e6-129">Politikker og regler anvendes på hver kladdelinje, og der oprettes omkostningsposter som output.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ba7e6-130">Derfor kan dataene altid spores.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ba7e6-131">[![Beregning af fast omkostning](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ba7e6-132">Beregne og fordele den faste omkostning for elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ba7e6-133">I et finansregnskab registreres nogle omkostninger, f.eks. elektricitet, som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ba7e6-134">Derfor er der ikke angivet detaljeret ledelsesmæssig indsigt for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ba7e6-135">I omkostningsregnskabet skal omkostningerne gennemløbe de organisatoriske enheder for at give korrekte ledelsesmæssig viden på tværs af alle afdelinger og niveauer.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ba7e6-136">Denne proces skal være baseret på enten en præcis registrering af forbruget eller en rimelig vurdering.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ba7e6-137">En omkostning for elektricitet kan bogføres i finans som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-138">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-139">Bærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-140">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="ba7e6-140">Main account</span></span></th>
<th><span data-ttu-id="ba7e6-141">Beløb i regnskabsvalutaen</span><span class="sxs-lookup"><span data-stu-id="ba7e6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-142">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-143">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-144">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-144">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-145">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-145">10001</span></span></td>
<td><span data-ttu-id="ba7e6-146">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-146">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ba7e6-148">Trin 1: Behandle beregningen af omkostningsfunktionaliteten</span><span class="sxs-lookup"><span data-stu-id="ba7e6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ba7e6-149">Som standard, når omkostningsposter er importeret fra kildedataene, modtager de klassifikationen **Ikke-klassificerede** for funktionalitet af omkostning i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ba7e6-150">Ved at anvende politikregler for omkostningsfunktionalitet kan du genklassificeres omkostningsposter som enten **Fast omkostning** eller **Variabel omkostning**.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ba7e6-151">Definere reglen for omkostningsfunktionalitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ba7e6-152">I nogle tilfælde er en del af omkostningen et fast gebyr, og de resterende omkostninger er baseret på forbrug.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ba7e6-153">Dette ses ofte på elektricitetsregninger.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ba7e6-154">Når du betaler et bestemt fast gebyr, betaler du for forbrug pr. kilowatttime (kWh).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ba7e6-155">Eksempelvis hvis det faste gebyr er 1.000,00, defineres reglen for omkostningsfunktionalitet sådan:</span><span class="sxs-lookup"><span data-stu-id="ba7e6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ba7e6-156">Fast beløb 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ba7e6-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="ba7e6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ba7e6-158">1000.01 &lt; N = Variabel</span><span class="sxs-lookup"><span data-stu-id="ba7e6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ba7e6-159">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-160">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-160">Journal</span></span></th>
<th><span data-ttu-id="ba7e6-161">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ba7e6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ba7e6-162">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ba7e6-163">Version</span><span class="sxs-lookup"><span data-stu-id="ba7e6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-164">00001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-164">00001</span></span></td>
<td><span data-ttu-id="ba7e6-165">Beregningskladde for funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ba7e6-166">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ba7e6-166">Fiscal</span></span></td>
<td><span data-ttu-id="ba7e6-167">2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-167">2017</span></span></td>
<td><span data-ttu-id="ba7e6-168">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-168">Period 1</span></span></td>
<td><span data-ttu-id="ba7e6-169">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ba7e6-170">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-171">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-172">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-173">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-173">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-174">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-175">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-176">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-177">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-178">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-178">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-179">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-179">10001</span></span></td>
<td><span data-ttu-id="ba7e6-180">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-180">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-181">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ba7e6-181">Unclassified</span></span></td>
<td><span data-ttu-id="ba7e6-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ba7e6-183">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ba7e6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-184">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-185">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-185">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-186">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-187">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-187">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-188">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-189">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-190">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-190">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-191">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-191">10001</span></span></td>
<td><span data-ttu-id="ba7e6-192">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-192">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-193">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ba7e6-193">Unclassified</span></span></td>
<td><span data-ttu-id="ba7e6-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-194">10,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-195">3. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-196">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-197">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-197">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-198">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-198">10001</span></span></td>
<td><span data-ttu-id="ba7e6-199">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-199">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-200">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ba7e6-200">Unclassified</span></span></td>
<td><span data-ttu-id="ba7e6-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-202">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-203">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-204">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-204">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-205">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-205">10001</span></span></td>
<td><span data-ttu-id="ba7e6-206">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-206">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-207">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-208">1,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-209">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-210">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-211">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-211">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-212">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-212">10001</span></span></td>
<td><span data-ttu-id="ba7e6-213">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-213">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-214">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-214">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-215">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-215">9,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-216">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-217">Du kan få flere oplysninger under [Oprette og tildele en politik for omkostningsfunktionalitet til en omkostningskontrolenhed](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ba7e6-218">Trin 2: Behandle beregningen af omkostningsfordelingen</span><span class="sxs-lookup"><span data-stu-id="ba7e6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ba7e6-219">Omkostningsfordeling bruges til at omfordele omkostninger fra ét omkostningsobjekt til et eller flere andre omkostningsobjekter ved at anvende en relevant fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ba7e6-220">Omkostningsfordeling og omkostningstildeling adskiller sig fra hinanden ved, at omkostningsfordeling altid sker på niveauet for det primære omkostningselement i den oprindelige omkostning.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ba7e6-221">Definere reglen for omkostningsdistribution</span><span class="sxs-lookup"><span data-stu-id="ba7e6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="ba7e6-222">I et finansregnskab registreres elektricitetsomkostninger ofte som et engangsbeløb.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ba7e6-223">Denne metode ikke er tilstrækkeligt detaljeret i omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ba7e6-224">Den variable omkostning skal fordeles til de enkelte omkostningsobjekter på et rimeligt grundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ba7e6-225">Den mest logiske fordelingsgrundlag er forbruget af elektricitet (kWh).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ba7e6-226">Der oprettes et statistisk dimensionsmedlem, Elektricitet, og forbruget af elektricitet registreres.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ba7e6-227">Som standard bliver alle statistiske dimensionsmedlemmer tilgængelige som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-228">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-228">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-229">KWh</span><span class="sxs-lookup"><span data-stu-id="ba7e6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-230">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-231">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-231">HR</span></span></td>
<td><span data-ttu-id="ba7e6-232">1.000</span><span class="sxs-lookup"><span data-stu-id="ba7e6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-233">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-234">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-234">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-235">6.000</span><span class="sxs-lookup"><span data-stu-id="ba7e6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-236">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-237">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-237">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-238">0</span><span class="sxs-lookup"><span data-stu-id="ba7e6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-239">Tabellen nedenfor viser resultatet, når elforbrug anvendes som en fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-240">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-240">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-241">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-241">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-242">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-243">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-244">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-245">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-245">HR</span></span></td>
<td><span data-ttu-id="ba7e6-246">1.000</span><span class="sxs-lookup"><span data-stu-id="ba7e6-246">1,000</span></span></td>
<td><span data-ttu-id="ba7e6-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-249">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-250">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-250">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-251">6.000</span><span class="sxs-lookup"><span data-stu-id="ba7e6-251">6,000</span></span></td>
<td><span data-ttu-id="ba7e6-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ba7e6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-254">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-255">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-255">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-256">0</span><span class="sxs-lookup"><span data-stu-id="ba7e6-256">0</span></span></td>
<td><span data-ttu-id="ba7e6-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-259">De faste omkostninger skal fordeles jævnt til de enkelte omkostningsobjekter, der har forbrugt elektricitet.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ba7e6-260">Du kan opnå dette resultat ved hjælp af det statistiske dimensionsmedlem for Elektricitet på en formelfordelingsgrundlag: (Elektricitet &gt; 0,00). I følgende tabel vises resultatet, når elforbruget anvendes som fordelingsgrundlag for variable omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-261">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-261">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-262">Formel</span><span class="sxs-lookup"><span data-stu-id="ba7e6-262">Formula</span></span></th>
<th><span data-ttu-id="ba7e6-263">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-263">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-264">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-265">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-266">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-267">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-267">HR</span></span></td>
<td><span data-ttu-id="ba7e6-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ba7e6-269">1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-269">1</span></span></td>
<td><span data-ttu-id="ba7e6-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-272">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-273">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-273">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ba7e6-275">1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-275">1</span></span></td>
<td><span data-ttu-id="ba7e6-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-278">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-279">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-279">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ba7e6-281">0</span><span class="sxs-lookup"><span data-stu-id="ba7e6-281">0</span></span></td>
<td><span data-ttu-id="ba7e6-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ba7e6-284">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-285">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-285">Journal</span></span></th>
<th><span data-ttu-id="ba7e6-286">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ba7e6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ba7e6-287">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ba7e6-288">Version</span><span class="sxs-lookup"><span data-stu-id="ba7e6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-289">00002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-289">00002</span></span></td>
<td><span data-ttu-id="ba7e6-290">Beregningskladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ba7e6-291">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ba7e6-291">Fiscal</span></span></td>
<td><span data-ttu-id="ba7e6-292">2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-292">2017</span></span></td>
<td><span data-ttu-id="ba7e6-293">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-293">Period 1</span></span></td>
<td><span data-ttu-id="ba7e6-294">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ba7e6-295">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-296">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-297">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-298">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-298">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-299">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-300">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-301">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-302">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-303">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-303">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-304">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-304">10001</span></span></td>
<td><span data-ttu-id="ba7e6-305">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-305">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-306">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-308">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-309">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-310">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-310">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-311">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-311">10001</span></span></td>
<td><span data-ttu-id="ba7e6-312">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-312">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-313">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-313">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-314">9.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ba7e6-315">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ba7e6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-316">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-317">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-317">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-318">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-319">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-319">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-320">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-321">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-322">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-322">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-323">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-323">10001</span></span></td>
<td><span data-ttu-id="ba7e6-324">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-324">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-325">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-327">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-328">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-329">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-329">HR</span></span></td>
<td><span data-ttu-id="ba7e6-330">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-330">10001</span></span></td>
<td><span data-ttu-id="ba7e6-331">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-331">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-332">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-333">500.00</span></span></td>
<td><span data-ttu-id="ba7e6-334">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-335">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-336">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-336">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-337">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-337">10001</span></span></td>
<td><span data-ttu-id="ba7e6-338">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-338">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-339">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-340">500.00</span></span></td>
<td><span data-ttu-id="ba7e6-341">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-342">CC099</span></span></td>
<td><span data-ttu-id="ba7e6-343">Standardbærer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-343">Default cost center</span></span></td>
<td><span data-ttu-id="ba7e6-344">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-344">10001</span></span></td>
<td><span data-ttu-id="ba7e6-345">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-345">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-346">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-346">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="ba7e6-348">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-349">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-350">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-350">HR</span></span></td>
<td><span data-ttu-id="ba7e6-351">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-351">10001</span></span></td>
<td><span data-ttu-id="ba7e6-352">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-352">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-353">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-353">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-354">1,285.71</span></span></td>
<td><span data-ttu-id="ba7e6-355">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-356">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-357">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-357">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-358">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-358">10001</span></span></td>
<td><span data-ttu-id="ba7e6-359">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-359">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-360">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-360">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ba7e6-361">7,714.29</span></span></td>
<td><span data-ttu-id="ba7e6-362">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-363">Du kan få flere oplysninger under [Oprette og tildele en omkostningsfordelingspolitik til en omkostningskontrolenhed](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ba7e6-364">Trin 3: Behandle beregning af faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="ba7e6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ba7e6-365">Satsen for faste omkostninger bruges til at lægge gebyr på et eller flere specifikke omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ba7e6-366">Gebyret er baseret på en foruddefineret omkostningssats og størrelsesordenen fra det tildelte fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ba7e6-367">Definere satsen for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="ba7e6-367">Define the overhead rate</span></span>

<span data-ttu-id="ba7e6-368">Omkostningsobjektet CC001 Personale bidrager til en række interne projekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ba7e6-369">Et statistisk dimensionsmedlem med navnet Personaleprojekter oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-370">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-370">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-371">Timer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-372">Proj 1</span></span></td>
<td><span data-ttu-id="ba7e6-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-373">Project 1</span></span></td>
<td><span data-ttu-id="ba7e6-374">3</span><span class="sxs-lookup"><span data-stu-id="ba7e6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-375">Proj 2</span></span></td>
<td><span data-ttu-id="ba7e6-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-376">Project 2</span></span></td>
<td><span data-ttu-id="ba7e6-377">1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-378">En foruddefineret omkostningssats for de omkostningsprojektbidrag, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-379">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-379">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-380">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-380">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-381">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-382">Enheder</span><span class="sxs-lookup"><span data-stu-id="ba7e6-382">Units</span></span></th>
<th><span data-ttu-id="ba7e6-383">Kurs</span><span class="sxs-lookup"><span data-stu-id="ba7e6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-384">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-385">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-385">HR</span></span></td>
<td><span data-ttu-id="ba7e6-386">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-386">10001</span></span></td>
<td><span data-ttu-id="ba7e6-387">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-387">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-388">1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-388">1</span></span></td>
<td><span data-ttu-id="ba7e6-389">10</span><span class="sxs-lookup"><span data-stu-id="ba7e6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-390">Tabellen nedenfor viser resultatet, når personaleprojekterne anvendes som fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-391">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-391">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-392">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-392">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-393">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-393">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-394">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-395">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-396">Proj 1</span></span></td>
<td><span data-ttu-id="ba7e6-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-397">Project 1</span></span></td>
<td><span data-ttu-id="ba7e6-398">3</span><span class="sxs-lookup"><span data-stu-id="ba7e6-398">3</span></span></td>
<td><span data-ttu-id="ba7e6-399">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-399">10001</span></span></td>
<td><span data-ttu-id="ba7e6-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ba7e6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-402">Proj 2</span></span></td>
<td><span data-ttu-id="ba7e6-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-403">Project 2</span></span></td>
<td><span data-ttu-id="ba7e6-404">1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-404">1</span></span></td>
<td><span data-ttu-id="ba7e6-405">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-405">10001</span></span></td>
<td><span data-ttu-id="ba7e6-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ba7e6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ba7e6-408">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-409">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-409">Journal</span></span></th>
<th><span data-ttu-id="ba7e6-410">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ba7e6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ba7e6-411">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ba7e6-412">Version</span><span class="sxs-lookup"><span data-stu-id="ba7e6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-413">00003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-413">00003</span></span></td>
<td><span data-ttu-id="ba7e6-414">Beregningskladde for satser for faste omkostninger</span><span class="sxs-lookup"><span data-stu-id="ba7e6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ba7e6-415">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ba7e6-415">Fiscal</span></span></td>
<td><span data-ttu-id="ba7e6-416">2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-416">2017</span></span></td>
<td><span data-ttu-id="ba7e6-417">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-417">Period 1</span></span></td>
<td><span data-ttu-id="ba7e6-418">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ba7e6-419">Kladdeposteringer (kladdeposteringer for beregning af faste omkostninger)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-420">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-421">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-421">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-422">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-423">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-424">Proj 1</span></span></td>
<td><span data-ttu-id="ba7e6-425">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ba7e6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-427">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-428">Proj 2</span></span></td>
<td><span data-ttu-id="ba7e6-429">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ba7e6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ba7e6-431">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ba7e6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-432">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-433">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-433">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-434">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-435">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-435">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-436">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-437">CC0001</span></span></td>
<td><span data-ttu-id="ba7e6-438">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-438">HR</span></span></td>
<td><span data-ttu-id="ba7e6-439">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-439">10001</span></span></td>
<td><span data-ttu-id="ba7e6-440">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-440">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-441">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-441">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-442">-30.00</span></span></td>
<td><span data-ttu-id="ba7e6-443">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-444">Proj 1</span></span></td>
<td><span data-ttu-id="ba7e6-445">Internt proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ba7e6-446">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-446">10001</span></span></td>
<td><span data-ttu-id="ba7e6-447">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-447">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-448">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-448">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-449">30.00</span></span></td>
<td><span data-ttu-id="ba7e6-450">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-451">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-452">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-452">HR</span></span></td>
<td><span data-ttu-id="ba7e6-453">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-453">10001</span></span></td>
<td><span data-ttu-id="ba7e6-454">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-454">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-455">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-455">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-456">-10.00</span></span></td>
<td><span data-ttu-id="ba7e6-457">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-458">Proj 2</span></span></td>
<td><span data-ttu-id="ba7e6-459">Internt proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ba7e6-460">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-460">10001</span></span></td>
<td><span data-ttu-id="ba7e6-461">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-461">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-462">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-462">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-463">10.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-463">10.00</span></span></td>
<td><span data-ttu-id="ba7e6-464">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-465">Du kan få flere oplysninger under [Udfør beregning af fast omkostning](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ba7e6-466">Trin 4: Behandle beregningen af omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="ba7e6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ba7e6-467">Fordeling bruges til at fordele saldoen for et omkostningsobjekt til andre omkostningsobjekter ved at anvende et fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ba7e6-468">Finance and Operations understøtter den gensidige fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="ba7e6-469">I den gensidig fordelingsmetode anerkendes de gensidige tjenester, som ekstra omkostningsobjekter udveksler, fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ba7e6-470">Systemet bestemmer automatisk den rigtige rækkefølge, som tildelingerne skal udføre i.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ba7e6-471">Saldoen for et omkostningsobjekt tildeles af et enkelt fordelingsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ba7e6-472">Tildelinger på tværs af omkostningsobjektdimensioner og deres respektive medlemmer understøttes.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ba7e6-473">Fordelingsrækkefølgen styres af omkostningskontrolenheden.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ba7e6-474">[![Reciprok metode](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ba7e6-475">Definere omkostningstildelingen</span><span class="sxs-lookup"><span data-stu-id="ba7e6-475">Define the cost allocation</span></span>

<span data-ttu-id="ba7e6-476">Her er et enkelt eksempel, der forklarer, hvordan du kan spore strømmen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ba7e6-477">Omkostningsobjektet CC001 personale bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ba7e6-478">Et statistisk dimensionsmedlem med navnet Personale-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-479">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-479">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-480">Personale-tjenester</span><span class="sxs-lookup"><span data-stu-id="ba7e6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-481">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-482">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-482">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-483">35</span><span class="sxs-lookup"><span data-stu-id="ba7e6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-484">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-485">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-485">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-486">55</span><span class="sxs-lookup"><span data-stu-id="ba7e6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-487">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-488">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-488">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-489">10</span><span class="sxs-lookup"><span data-stu-id="ba7e6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-490">Omkostningsobjektet CC002 Finans bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ba7e6-491">Et statistisk dimensionsmedlem med navnet Finans-tjenester oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-492">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-492">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-493">Finans-tjenester</span><span class="sxs-lookup"><span data-stu-id="ba7e6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-494">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-495">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-495">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-496">65</span><span class="sxs-lookup"><span data-stu-id="ba7e6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-497">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-498">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-498">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-499">35</span><span class="sxs-lookup"><span data-stu-id="ba7e6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-500">Omkostningsobjektet CC003 Assembly bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ba7e6-501">Et statistisk dimensionsmedlem med navnet Assembly oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-502">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-502">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-503">Assembly-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-504">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-505">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-505">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-506">60</span><span class="sxs-lookup"><span data-stu-id="ba7e6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-507">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-508">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-508">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-509">20</span><span class="sxs-lookup"><span data-stu-id="ba7e6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-510">Omkostningsobjektet CC004 Emballage bidrager til flere omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ba7e6-511">Et statistisk dimensionsmedlem med navnet Emballage oprettes for at måle den anvendte mængde.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-512">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-512">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-513">Emballage-tjenester (timer)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-514">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-515">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-515">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-516">80</span><span class="sxs-lookup"><span data-stu-id="ba7e6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-517">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-518">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-518">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-519">september</span><span class="sxs-lookup"><span data-stu-id="ba7e6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ba7e6-520">I Finance and Operations kan statistiske foranstaltninger som f.eks. de produktionstimer, som et produkt forbruger, udledes af kildedataene.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ba7e6-521">Du kan finde flere oplysninger under [Skabelon til providere af statistiske målinger](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="ba7e6-522">Tabellen nedenfor viser resultatet, når personaletjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-523">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-523">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-524">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-524">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-525">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-526">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-526">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-527">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-528">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-529">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-529">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-530">35</span><span class="sxs-lookup"><span data-stu-id="ba7e6-530">35</span></span></td>
<td><span data-ttu-id="ba7e6-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ba7e6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-532">175.00</span></span></td>
<td><span data-ttu-id="ba7e6-533">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-534">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-535">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-535">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-536">55</span><span class="sxs-lookup"><span data-stu-id="ba7e6-536">55</span></span></td>
<td><span data-ttu-id="ba7e6-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ba7e6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-538">275.00</span></span></td>
<td><span data-ttu-id="ba7e6-539">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-540">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-541">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-541">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-542">10</span><span class="sxs-lookup"><span data-stu-id="ba7e6-542">10</span></span></td>
<td><span data-ttu-id="ba7e6-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ba7e6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-544">50.00</span></span></td>
<td><span data-ttu-id="ba7e6-545">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-546">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-547">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-547">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-548">35</span><span class="sxs-lookup"><span data-stu-id="ba7e6-548">35</span></span></td>
<td><span data-ttu-id="ba7e6-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ba7e6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-550">436.00</span></span></td>
<td><span data-ttu-id="ba7e6-551">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-552">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-553">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-553">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-554">55</span><span class="sxs-lookup"><span data-stu-id="ba7e6-554">55</span></span></td>
<td><span data-ttu-id="ba7e6-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ba7e6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="ba7e6-556">685.14</span></span></td>
<td><span data-ttu-id="ba7e6-557">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-558">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-559">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-559">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-560">10</span><span class="sxs-lookup"><span data-stu-id="ba7e6-560">10</span></span></td>
<td><span data-ttu-id="ba7e6-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ba7e6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="ba7e6-562">124.57</span></span></td>
<td><span data-ttu-id="ba7e6-563">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-564">Tabellen nedenfor viser resultatet, når Finans-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-565">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-565">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-566">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-566">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-567">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-568">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-568">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-569">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-570">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-571">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-571">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-572">65</span><span class="sxs-lookup"><span data-stu-id="ba7e6-572">65</span></span></td>
<td><span data-ttu-id="ba7e6-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ba7e6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="ba7e6-574">438.75</span></span></td>
<td><span data-ttu-id="ba7e6-575">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-576">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-577">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-577">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-578">35</span><span class="sxs-lookup"><span data-stu-id="ba7e6-578">35</span></span></td>
<td><span data-ttu-id="ba7e6-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ba7e6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="ba7e6-580">236.25</span></span></td>
<td><span data-ttu-id="ba7e6-581">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-582">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-583">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-583">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-584">65</span><span class="sxs-lookup"><span data-stu-id="ba7e6-584">65</span></span></td>
<td><span data-ttu-id="ba7e6-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ba7e6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ba7e6-586">5,297.69</span></span></td>
<td><span data-ttu-id="ba7e6-587">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-588">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-589">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-589">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-590">35</span><span class="sxs-lookup"><span data-stu-id="ba7e6-590">35</span></span></td>
<td><span data-ttu-id="ba7e6-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ba7e6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ba7e6-592">2,852.60</span></span></td>
<td><span data-ttu-id="ba7e6-593">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-594">Tabellen nedenfor viser resultatet, når Assembly-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-595">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-595">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-596">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-596">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-597">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-598">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-598">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-599">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-600">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-601">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-601">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-602">60</span><span class="sxs-lookup"><span data-stu-id="ba7e6-602">60</span></span></td>
<td><span data-ttu-id="ba7e6-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ba7e6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="ba7e6-604">535.31</span></span></td>
<td><span data-ttu-id="ba7e6-605">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-606">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-607">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-607">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-608">20</span><span class="sxs-lookup"><span data-stu-id="ba7e6-608">20</span></span></td>
<td><span data-ttu-id="ba7e6-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ba7e6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="ba7e6-610">178.44</span></span></td>
<td><span data-ttu-id="ba7e6-611">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-612">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-613">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-613">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-614">60</span><span class="sxs-lookup"><span data-stu-id="ba7e6-614">60</span></span></td>
<td><span data-ttu-id="ba7e6-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ba7e6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ba7e6-616">4,487.12</span></span></td>
<td><span data-ttu-id="ba7e6-617">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-618">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-619">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-619">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-620">20</span><span class="sxs-lookup"><span data-stu-id="ba7e6-620">20</span></span></td>
<td><span data-ttu-id="ba7e6-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ba7e6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-622">1,495.71</span></span></td>
<td><span data-ttu-id="ba7e6-623">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ba7e6-624">Tabellen nedenfor viser resultatet, når Emballage-tjenester anvendes som fordelingsgrundlag for samlede omkostninger (faste omkostninger og variable omkostninger).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-625">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-625">Cost object</span></span></th>
<th><span data-ttu-id="ba7e6-626">Størrelsesorden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-626">Magnitude</span></span></th>
<th><span data-ttu-id="ba7e6-627">Fordelingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ba7e6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="ba7e6-628">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-628">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-629">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-630">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-631">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-631">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-632">80</span><span class="sxs-lookup"><span data-stu-id="ba7e6-632">80</span></span></td>
<td><span data-ttu-id="ba7e6-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ba7e6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="ba7e6-634">241.05</span></span></td>
<td><span data-ttu-id="ba7e6-635">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-636">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-637">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-637">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-638">15</span><span class="sxs-lookup"><span data-stu-id="ba7e6-638">15</span></span></td>
<td><span data-ttu-id="ba7e6-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ba7e6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="ba7e6-640">45.20</span></span></td>
<td><span data-ttu-id="ba7e6-641">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-642">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-643">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-643">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-644">80</span><span class="sxs-lookup"><span data-stu-id="ba7e6-644">80</span></span></td>
<td><span data-ttu-id="ba7e6-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ba7e6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ba7e6-646">2,507.09</span></span></td>
<td><span data-ttu-id="ba7e6-647">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-648">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-649">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-649">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-650">15</span><span class="sxs-lookup"><span data-stu-id="ba7e6-650">15</span></span></td>
<td><span data-ttu-id="ba7e6-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ba7e6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="ba7e6-652">470.08</span></span></td>
<td><span data-ttu-id="ba7e6-653">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ba7e6-654">Kladdeposteringer (kladdeposteringer for omkostningsobjektsaldo)</span><span class="sxs-lookup"><span data-stu-id="ba7e6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-655">Kladden</span><span class="sxs-lookup"><span data-stu-id="ba7e6-655">Journal</span></span></th>
<th><span data-ttu-id="ba7e6-656">Kladdetype</span><span class="sxs-lookup"><span data-stu-id="ba7e6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ba7e6-657">Regnskabskalenderperiode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ba7e6-658">Version</span><span class="sxs-lookup"><span data-stu-id="ba7e6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-659">00004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-659">00004</span></span></td>
<td><span data-ttu-id="ba7e6-660">Kladde for omkostningsfordeling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ba7e6-661">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="ba7e6-661">Fiscal</span></span></td>
<td><span data-ttu-id="ba7e6-662">2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-662">2017</span></span></td>
<td><span data-ttu-id="ba7e6-663">1. Periode</span><span class="sxs-lookup"><span data-stu-id="ba7e6-663">Period 1</span></span></td>
<td><span data-ttu-id="ba7e6-664">Beregning af fast omkostning / 02-01-2017 23:51:00 / Finans /2017 / periode 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ba7e6-665">kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="ba7e6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba7e6-666">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-667">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-668">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-668">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-669">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-670">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-671">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-672">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-673">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-673">HR</span></span></td>
<td><span data-ttu-id="ba7e6-674">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-674">10001</span></span></td>
<td><span data-ttu-id="ba7e6-675">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-675">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-676">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-678">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-679">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-680">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-680">HR</span></span></td>
<td><span data-ttu-id="ba7e6-681">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-681">10001</span></span></td>
<td><span data-ttu-id="ba7e6-682">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-682">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-683">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-683">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-685">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-686">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-687">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-687">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-688">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-688">10001</span></span></td>
<td><span data-ttu-id="ba7e6-689">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-689">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-690">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-692">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-693">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-694">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-694">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-695">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-695">10001</span></span></td>
<td><span data-ttu-id="ba7e6-696">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-696">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-697">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-697">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ba7e6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-699">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-700">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-701">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-701">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-702">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-702">10001</span></span></td>
<td><span data-ttu-id="ba7e6-703">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-703">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-704">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="ba7e6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-706">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-707">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-708">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-708">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-709">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-709">10001</span></span></td>
<td><span data-ttu-id="ba7e6-710">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-710">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-711">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-711">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ba7e6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-713">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-714">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-715">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-715">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-716">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-716">10001</span></span></td>
<td><span data-ttu-id="ba7e6-717">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-717">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-718">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="ba7e6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-720">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-721">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-722">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-722">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-723">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-723">10001</span></span></td>
<td><span data-ttu-id="ba7e6-724">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-724">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-725">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-725">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ba7e6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-727">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-728">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-729">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-729">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-730">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-730">10001</span></span></td>
<td><span data-ttu-id="ba7e6-731">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-731">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-732">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="ba7e6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-734">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-735">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-736">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-736">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-737">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-737">10001</span></span></td>
<td><span data-ttu-id="ba7e6-738">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-738">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-739">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-739">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ba7e6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-741">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-742">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-743">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-743">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-744">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-744">10001</span></span></td>
<td><span data-ttu-id="ba7e6-745">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-745">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-746">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="ba7e6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-748">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="ba7e6-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-749">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-750">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-750">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-751">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-751">10001</span></span></td>
<td><span data-ttu-id="ba7e6-752">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-752">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-753">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-753">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ba7e6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ba7e6-755">Omkostningsposter</span><span class="sxs-lookup"><span data-stu-id="ba7e6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ba7e6-756">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ba7e6-757">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-757">Cost element</span></span></th>
<th><span data-ttu-id="ba7e6-758">Funktionalitet af omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="ba7e6-759">Beløb</span><span class="sxs-lookup"><span data-stu-id="ba7e6-759">Amount</span></span></th>
<th><span data-ttu-id="ba7e6-760">Regnskabsdato</span><span class="sxs-lookup"><span data-stu-id="ba7e6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba7e6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-761">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-762">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-762">HR</span></span></td>
<td><span data-ttu-id="ba7e6-763">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-763">10001</span></span></td>
<td><span data-ttu-id="ba7e6-764">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-764">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-765">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-766">-500.00</span></span></td>
<td><span data-ttu-id="ba7e6-767">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-768">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-769">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-769">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-770">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-770">10001</span></span></td>
<td><span data-ttu-id="ba7e6-771">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-771">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-772">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-773">175.00</span></span></td>
<td><span data-ttu-id="ba7e6-774">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-775">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-776">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-776">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-777">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-777">10001</span></span></td>
<td><span data-ttu-id="ba7e6-778">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-778">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-779">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-780">275.00</span></span></td>
<td><span data-ttu-id="ba7e6-781">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-782">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-783">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-783">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-784">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-784">10001</span></span></td>
<td><span data-ttu-id="ba7e6-785">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-785">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-786">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-787">50,00</span></span></td>
<td><span data-ttu-id="ba7e6-788">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-789">CC001</span></span></td>
<td><span data-ttu-id="ba7e6-790">Personale</span><span class="sxs-lookup"><span data-stu-id="ba7e6-790">HR</span></span></td>
<td><span data-ttu-id="ba7e6-791">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-791">10001</span></span></td>
<td><span data-ttu-id="ba7e6-792">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-792">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-793">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-793">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="ba7e6-795">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-796">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-797">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-797">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-798">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-798">10001</span></span></td>
<td><span data-ttu-id="ba7e6-799">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-799">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-800">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-800">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-801">436.00</span></span></td>
<td><span data-ttu-id="ba7e6-802">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-803">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-804">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-804">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-805">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-805">10001</span></span></td>
<td><span data-ttu-id="ba7e6-806">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-806">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-807">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-807">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="ba7e6-808">685.14</span></span></td>
<td><span data-ttu-id="ba7e6-809">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-810">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-811">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-811">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-812">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-812">10001</span></span></td>
<td><span data-ttu-id="ba7e6-813">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-813">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-814">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-814">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="ba7e6-815">124.57</span></span></td>
<td><span data-ttu-id="ba7e6-816">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-817">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-818">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-818">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-819">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-819">10001</span></span></td>
<td><span data-ttu-id="ba7e6-820">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-820">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-821">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-822">-675.00</span></span></td>
<td><span data-ttu-id="ba7e6-823">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-824">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-825">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-825">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-826">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-826">10001</span></span></td>
<td><span data-ttu-id="ba7e6-827">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-827">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-828">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="ba7e6-829">438.75</span></span></td>
<td><span data-ttu-id="ba7e6-830">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-831">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-832">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-832">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-833">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-833">10001</span></span></td>
<td><span data-ttu-id="ba7e6-834">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-834">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-835">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="ba7e6-836">236.25</span></span></td>
<td><span data-ttu-id="ba7e6-837">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-838">CC002</span></span></td>
<td><span data-ttu-id="ba7e6-839">Finans</span><span class="sxs-lookup"><span data-stu-id="ba7e6-839">Finance</span></span></td>
<td><span data-ttu-id="ba7e6-840">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-840">10001</span></span></td>
<td><span data-ttu-id="ba7e6-841">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-841">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-842">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-842">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="ba7e6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="ba7e6-844">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-845">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-846">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-846">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-847">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-847">10001</span></span></td>
<td><span data-ttu-id="ba7e6-848">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-848">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-849">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-849">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ba7e6-850">5,297.69</span></span></td>
<td><span data-ttu-id="ba7e6-851">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-852">CC004</span></span></td>
<td><span data-ttu-id="ba7e6-853">Emballage</span><span class="sxs-lookup"><span data-stu-id="ba7e6-853">Packaging</span></span></td>
<td><span data-ttu-id="ba7e6-854">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-854">10001</span></span></td>
<td><span data-ttu-id="ba7e6-855">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-855">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-856">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-856">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ba7e6-857">2,852.60</span></span></td>
<td><span data-ttu-id="ba7e6-858">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-859">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-860">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-860">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-861">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-861">10001</span></span></td>
<td><span data-ttu-id="ba7e6-862">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-862">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-863">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="ba7e6-864">-713.75</span></span></td>
<td><span data-ttu-id="ba7e6-865">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-866">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-867">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-867">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-868">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-868">10001</span></span></td>
<td><span data-ttu-id="ba7e6-869">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-869">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-870">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="ba7e6-871">535.31</span></span></td>
<td><span data-ttu-id="ba7e6-872">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-873">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-874">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-874">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-875">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-875">10001</span></span></td>
<td><span data-ttu-id="ba7e6-876">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-876">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-877">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="ba7e6-878">178.44</span></span></td>
<td><span data-ttu-id="ba7e6-879">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-880">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-881">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-881">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-882">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-882">10001</span></span></td>
<td><span data-ttu-id="ba7e6-883">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-883">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-884">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-884">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="ba7e6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="ba7e6-886">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-887">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-888">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-888">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-889">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-889">10001</span></span></td>
<td><span data-ttu-id="ba7e6-890">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-890">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-891">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-891">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ba7e6-892">4,487.12</span></span></td>
<td><span data-ttu-id="ba7e6-893">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-894">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-895">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-895">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-896">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-896">10001</span></span></td>
<td><span data-ttu-id="ba7e6-897">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-897">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-898">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-898">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ba7e6-899">1,495.71</span></span></td>
<td><span data-ttu-id="ba7e6-900">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-901">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-902">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-902">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-903">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-903">10001</span></span></td>
<td><span data-ttu-id="ba7e6-904">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-904">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-905">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="ba7e6-906">-286.25</span></span></td>
<td><span data-ttu-id="ba7e6-907">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-908">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-909">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-909">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-910">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-910">10001</span></span></td>
<td><span data-ttu-id="ba7e6-911">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-911">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-912">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="ba7e6-913">241.05</span></span></td>
<td><span data-ttu-id="ba7e6-914">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-915">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-916">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-916">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-917">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-917">10001</span></span></td>
<td><span data-ttu-id="ba7e6-918">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-918">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-919">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="ba7e6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="ba7e6-920">45.20</span></span></td>
<td><span data-ttu-id="ba7e6-921">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-922">CC003</span></span></td>
<td><span data-ttu-id="ba7e6-923">Samling</span><span class="sxs-lookup"><span data-stu-id="ba7e6-923">Assembly</span></span></td>
<td><span data-ttu-id="ba7e6-924">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-924">10001</span></span></td>
<td><span data-ttu-id="ba7e6-925">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-925">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-926">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-926">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="ba7e6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="ba7e6-928">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-929">Prod 1</span></span></td>
<td><span data-ttu-id="ba7e6-930">Produkt 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-930">Product 1</span></span></td>
<td><span data-ttu-id="ba7e6-931">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-931">10001</span></span></td>
<td><span data-ttu-id="ba7e6-932">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-932">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-933">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-933">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ba7e6-934">2,507.09</span></span></td>
<td><span data-ttu-id="ba7e6-935">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ba7e6-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-936">Prod 2</span></span></td>
<td><span data-ttu-id="ba7e6-937">Produkt 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-937">Product 2</span></span></td>
<td><span data-ttu-id="ba7e6-938">10001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-938">10001</span></span></td>
<td><span data-ttu-id="ba7e6-939">Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-939">Electricity</span></span></td>
<td><span data-ttu-id="ba7e6-940">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-940">Variable cost</span></span></td>
<td><span data-ttu-id="ba7e6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="ba7e6-941">470.08</span></span></td>
<td><span data-ttu-id="ba7e6-942">31. januar 2017</span><span class="sxs-lookup"><span data-stu-id="ba7e6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ba7e6-943">Konklusion</span><span class="sxs-lookup"><span data-stu-id="ba7e6-943">Conclusion</span></span>
<span data-ttu-id="ba7e6-944">I Finansregnskab bogføres en omkostning på 10.000,00 for elektricitet til et dummy-bærer-id.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ba7e6-945">Derfor kan bogholdere se, at disse omkostninger skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ba7e6-946">I Omkostningsregnskab passerer omkostningerne på tværs af afdelinger og niveauer, baseret på de politikker og regler, der anvendes.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ba7e6-947">Hver omkostning er knyttet et fordelingsgrundlag, der giver den bedste vurdering af fordelingen af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ba7e6-948">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ba7e6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ba7e6-949">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ba7e6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ba7e6-950">Samlet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ba7e6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="ba7e6-951">CC099</span></span></th>
<th><span data-ttu-id="ba7e6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="ba7e6-952">CC001</span></span></th>
<th><span data-ttu-id="ba7e6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="ba7e6-953">CC002</span></span></th>
<th><span data-ttu-id="ba7e6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="ba7e6-954">CC003</span></span></th>
<th><span data-ttu-id="ba7e6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="ba7e6-955">CC004</span></span></th>
<th><span data-ttu-id="ba7e6-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-956">Proj 1</span></span></th>
<th><span data-ttu-id="ba7e6-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-957">Proj 2</span></span></th>
<th><span data-ttu-id="ba7e6-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ba7e6-958">Prod 1</span></span></th>
<th><span data-ttu-id="ba7e6-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ba7e6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ba7e6-960">10001 Elektricitet</span><span class="sxs-lookup"><span data-stu-id="ba7e6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ba7e6-970">Ikke-klassificerede</span><span class="sxs-lookup"><span data-stu-id="ba7e6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ba7e6-972">Fast omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="ba7e6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="ba7e6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ba7e6-981">Variabel omkostning</span><span class="sxs-lookup"><span data-stu-id="ba7e6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-982">000</span><span class="sxs-lookup"><span data-stu-id="ba7e6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="ba7e6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ba7e6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ba7e6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ba7e6-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ba7e6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ba7e6-992">Dette emne viser, hvordan et primært omkostningselement, 10001 Elektricitet, flyder gennem omkostningsobjekter.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ba7e6-993">Derfor tildeles disse faste omkostninger til det laveste niveau i organisationen.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ba7e6-994">Det vil sige, at omkostningsobjekter på laveste niveau bærer omkostningen.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ba7e6-995">Hvis du har brug for en visuel tilførsel af omkostningen mellem omkostningsobjekter, kan du bruge politikreglerne for omkostningsakkumuleringen til at visualisere strømmen af omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="ba7e6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ba7e6-996">Du kan få flere oplysninger under [Omkostningstotaler](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="ba7e6-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



