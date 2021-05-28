---
title: Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer
description: I dette emne beskrives yderligere funktioner til beregning og anvendelse af automatiske gebyrer på Commerce-kanalordrer ved hjælp af den avancerede automatiske gebyrfunktion.
author: hhaines
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c36948cc58291b56c1bbe8a3d5c3db52dccc8399
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018600"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="c5fe6-103">Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer</span><span class="sxs-lookup"><span data-stu-id="c5fe6-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c5fe6-104">I dette emne beskrives funktioner til gruppering af automatiske gebyrer på hovedniveau og til forholdsmæssig beregning af dem for handelssalgslinjer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="c5fe6-105">Denne funktionalitet er tilgængelig for transaktioner, der oprettes på POS i Retail version 10.0.1, og salg, der oprettes i et callcenter i Retail version 10.0.2.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="c5fe6-106">Denne funktionalitet er kun tilgængelig, hvis den [avancerede automatiske gebyrfunktion](/dynamics365/unified-operations/retail/omni-auto-charges) er aktiveret ved hjælp af indstillingen på siden **Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-106">This functionality is available only if the [advanced auto-charges](/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="c5fe6-107">Desuden kan den forbedrede beregningsmåde for automatiske gebyrer kun anvendes til salgsordrer, der oprettes gennem handelskanaler (POS, et callcenter og Dynamics e-handelsplatformen).</span><span class="sxs-lookup"><span data-stu-id="c5fe6-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="c5fe6-108">Denne nye funktion giver organisationer større fleksibilitet i den måde, som automatiske gebyrer på hovedniveau beregnes og anvendes i salgstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="c5fe6-109">I versioner af appen, der er ældre end version 10.0.1, beregnes automatiske gebyrer på hovedniveau, som har en bestemt leveringsmåderelation, kun, når der er overensstemmelse med den leveringsmåde, som er defineret i salgsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="c5fe6-110">F.eks. defineres automatiske gebyrer på hovedniveau for levering **99** og leveringsmåden **11**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="c5fe6-111">Der oprettes en salgsordre, og leveringsmåden **99** defineres i ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="c5fe6-112">Men nogle af salgslinjerne er konfigureret, så de sendes ved hjælp af leveringsmåde **11**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="c5fe6-113">I så fald tages kun gebyrer på hovedniveau, der er knyttet til leveringsmåde **99**, i betragtning og anvendes på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="c5fe6-114">I Commerce har gebyrer på hovedniveau en ekstra funktion, som du kan bruge til at definere en [konfiguration af lagdelte gebyrer](/dynamics365/unified-operations/retail/configure-call-center-delivery), der er baseret på ordreværdien.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="c5fe6-115">Eksempelvis hvis ordreværdien er mellem $50,00 og $200,00, kan en organisation eventuelt opkræve et fragtgebyr på $5,00.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="c5fe6-116">Hvis ordreværdien er mellem $200,01 og $500,00, kan fragten dog være $4,00.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="c5fe6-117">Nogle organisationer ønsker fordelene ved beregningen af lagdelte gebyrer, der følger med gebyrer på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="c5fe6-118">Men i scenarier, der består af blandede leveringsmåder, skal de også sikre, at de gebyrer, der beregnes, passer til den leveringsmåde, der er defineret på hver salgslinje.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="c5fe6-119">Du kan nu konfigurere automatiske gebyrer på hovedniveau, så alle leveringsmåder på ordren indgår i beregningen af gebyrer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="c5fe6-120">Denne funktionalitet kræver en mere kompleks beregningslogik til beregning af gebyrer på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="c5fe6-121">Logikken grupperer de varer, der leveres ved hjælp af samme leveringsmåde, og behandler denne gruppe som beregningsgruppen for varerne ved beregning af automatiske gebyrer på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="c5fe6-122">For varer, der har samme leveringsmåde, beregnes automatiske gebyrer ud fra den samlede salgsværdi for varerne.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="c5fe6-123">På denne måde bestemmes det relevante automatiske gebyrniveau.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="c5fe6-124">Når de relevante gebyrer på hovedniveau opnås for de salgslinjer, der sendes ved hjælp af samme leveringsmåde, fordeles de beregnede gebyrer helt ned til salgslinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="c5fe6-125">Da disse gebyrer er på linjeniveau og ikke holdes på hovedniveau, oprettes en mere specifik tilknytning mellem varen og den gebyrværdi, der beregnes for den.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="c5fe6-126">Denne funktionsmåde kan være nyttig ved delvise returneringer, hvor en organisation kun ønsker at tilbagebetale en del af gebyrer i stedet for hele gebyret, når kun nogle af varerne returneres.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="c5fe6-127">Scenarier</span><span class="sxs-lookup"><span data-stu-id="c5fe6-127">Scenarios</span></span>

<span data-ttu-id="c5fe6-128">Følgende to eksempelscenarier skitserer, hvordan disse gebyrer beregnes, både når den nye funktionalitet bruges, og når den ikke bruges.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="c5fe6-129">Scenario 1</span><span class="sxs-lookup"><span data-stu-id="c5fe6-129">Scenario 1</span></span>

<span data-ttu-id="c5fe6-130">Dette scenario beskriver funktionsmåden, når indstillingen **Beregn forholdsmæssigt på matchende salgslinjer** er angivet til **Nej** i opsætningen af automatiske gebyrer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="c5fe6-131">(Funktionsmåden svarer til funktionsmåden for gebyrer på hovedniveau i appversioner, der er ældre end version 10.0.1).</span><span class="sxs-lookup"><span data-stu-id="c5fe6-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="c5fe6-132">I dette scenario har organisationen defineret gebyrer på hovedniveau for leveringsmåderelation **99** og leveringsmåderelation **11**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="c5fe6-133">Ingen automatiske gebyrer er konfigureret for leveringsmåde **21**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![Automatiske gebyrer for leveringsmåde 99, når forholdsmæssig beregning for linjematchning er slået fra](media/99_disabled.png)

![Automatiske gebyrer for leveringsmåde 11, når forholdsmæssig beregning for linjematchning er slået fra](media/11_disabled.png)

<span data-ttu-id="c5fe6-136">Der oprettes en salgsordre i callcenteret, og leveringsmåden indstilles til **99**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="c5fe6-137">Denne ordre indeholder fem varer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-137">This order contains five items.</span></span> <span data-ttu-id="c5fe6-138">To ordrelinjer er konfigureret til at bruge leveringsmåde **99**, to linjer er konfigureret til at bruge leveringsmåde **11**, og én linje er konfigureret til at bruge leveringsmåde **21**, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="c5fe6-139">Post</span><span class="sxs-lookup"><span data-stu-id="c5fe6-139">Item</span></span>  | <span data-ttu-id="c5fe6-140">Linjeantal</span><span class="sxs-lookup"><span data-stu-id="c5fe6-140">Line quantity</span></span> | <span data-ttu-id="c5fe6-141">Leveringstilstand</span><span class="sxs-lookup"><span data-stu-id="c5fe6-141">Delivery mode</span></span> | <span data-ttu-id="c5fe6-142">Pris pr. enhed</span><span class="sxs-lookup"><span data-stu-id="c5fe6-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="c5fe6-143">81331</span><span class="sxs-lookup"><span data-stu-id="c5fe6-143">81331</span></span> | <span data-ttu-id="c5fe6-144">1</span><span class="sxs-lookup"><span data-stu-id="c5fe6-144">1</span></span>             | <span data-ttu-id="c5fe6-145">11</span><span class="sxs-lookup"><span data-stu-id="c5fe6-145">11</span></span>            | <span data-ttu-id="c5fe6-146">$10</span><span class="sxs-lookup"><span data-stu-id="c5fe6-146">$10</span></span>            |
| <span data-ttu-id="c5fe6-147">81332</span><span class="sxs-lookup"><span data-stu-id="c5fe6-147">81332</span></span> | <span data-ttu-id="c5fe6-148">1</span><span class="sxs-lookup"><span data-stu-id="c5fe6-148">1</span></span>             | <span data-ttu-id="c5fe6-149">99</span><span class="sxs-lookup"><span data-stu-id="c5fe6-149">99</span></span>            | <span data-ttu-id="c5fe6-150">$50</span><span class="sxs-lookup"><span data-stu-id="c5fe6-150">$50</span></span>            |
| <span data-ttu-id="c5fe6-151">81333</span><span class="sxs-lookup"><span data-stu-id="c5fe6-151">81333</span></span> | <span data-ttu-id="c5fe6-152">2</span><span class="sxs-lookup"><span data-stu-id="c5fe6-152">2</span></span>             | <span data-ttu-id="c5fe6-153">11</span><span class="sxs-lookup"><span data-stu-id="c5fe6-153">11</span></span>            | <span data-ttu-id="c5fe6-154">$30</span><span class="sxs-lookup"><span data-stu-id="c5fe6-154">$30</span></span>            |
| <span data-ttu-id="c5fe6-155">81334</span><span class="sxs-lookup"><span data-stu-id="c5fe6-155">81334</span></span> | <span data-ttu-id="c5fe6-156">3</span><span class="sxs-lookup"><span data-stu-id="c5fe6-156">3</span></span>             | <span data-ttu-id="c5fe6-157">99</span><span class="sxs-lookup"><span data-stu-id="c5fe6-157">99</span></span>            | <span data-ttu-id="c5fe6-158">$10</span><span class="sxs-lookup"><span data-stu-id="c5fe6-158">$10</span></span>            |
| <span data-ttu-id="c5fe6-159">81334</span><span class="sxs-lookup"><span data-stu-id="c5fe6-159">81334</span></span> | <span data-ttu-id="c5fe6-160">3</span><span class="sxs-lookup"><span data-stu-id="c5fe6-160">3</span></span>             | <span data-ttu-id="c5fe6-161">21</span><span class="sxs-lookup"><span data-stu-id="c5fe6-161">21</span></span>            | <span data-ttu-id="c5fe6-162">$5</span><span class="sxs-lookup"><span data-stu-id="c5fe6-162">$5</span></span>             |

<span data-ttu-id="c5fe6-163">I dette scenario evalueres hele ordren i forhold til tabellen over automatiske gebyrer for leveringsmåde **99**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="c5fe6-164">Hele summen af alle salgslinjer bruges til at bestemme et matchningstrin i konfigurationen af automatiske gebyrer, og dette gebyr anvendes på ordrehovedniveau.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="c5fe6-165">Den samlede ordrebeløb er $165,00 i dette eksempel, og fragtgebyret på $15,00 anvendes i ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="c5fe6-166">Der refereres aldrig til eller anvendes automatiske gebyrer, der er konfigureret for leveringsmåde **11**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="c5fe6-167">I dette scenario, hvis en kunde returnerer nogle af varerne i ordren, og hvis [gebyrkoden konfigureres, så den kan refunderes](/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), anvendes det samlede gebyr på hovedniveau systematisk på refusionen, selvom kun nogle af varerne returneres.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="c5fe6-168">Scenario 2</span><span class="sxs-lookup"><span data-stu-id="c5fe6-168">Scenario 2</span></span>

<span data-ttu-id="c5fe6-169">I dette scenario defineres gebyrer på hovedniveau for leveringsmåderelation **99** og leveringsmåderelation **11**.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="c5fe6-170">Men indstillingen **Beregn forholdsmæssigt på matchende salgslinjer** er angivet til **Ja** for disse tabeller over automatiske gebyrer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![Automatiske gebyrer for leveringsmåde 99, når forholdsmæssig beregning for linjematchning er slået til](media/99_enabled.png)

![Automatiske gebyrer for leveringsmåde 11, når forholdsmæssig beregning for linjematchning er slået til](media/11_enabled.png)

<span data-ttu-id="c5fe6-173">I dette scenario bruges den samme salgsordre, der indeholder fem linjer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="c5fe6-174">Leveringsmåden i ordrehovedet er indstillet til **99**, men leveringsmåden for de enkelte varer på salgsordren er konfigureret som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="c5fe6-175">Post</span><span class="sxs-lookup"><span data-stu-id="c5fe6-175">Item</span></span>  | <span data-ttu-id="c5fe6-176">Linjeantal</span><span class="sxs-lookup"><span data-stu-id="c5fe6-176">Line quantity</span></span> | <span data-ttu-id="c5fe6-177">Leveringstilstand</span><span class="sxs-lookup"><span data-stu-id="c5fe6-177">Delivery mode</span></span> | <span data-ttu-id="c5fe6-178">Pris pr. enhed</span><span class="sxs-lookup"><span data-stu-id="c5fe6-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="c5fe6-179">81331</span><span class="sxs-lookup"><span data-stu-id="c5fe6-179">81331</span></span> | <span data-ttu-id="c5fe6-180">1</span><span class="sxs-lookup"><span data-stu-id="c5fe6-180">1</span></span>             | <span data-ttu-id="c5fe6-181">11</span><span class="sxs-lookup"><span data-stu-id="c5fe6-181">11</span></span>            | <span data-ttu-id="c5fe6-182">$10</span><span class="sxs-lookup"><span data-stu-id="c5fe6-182">$10</span></span>            |
| <span data-ttu-id="c5fe6-183">81332</span><span class="sxs-lookup"><span data-stu-id="c5fe6-183">81332</span></span> | <span data-ttu-id="c5fe6-184">1</span><span class="sxs-lookup"><span data-stu-id="c5fe6-184">1</span></span>             | <span data-ttu-id="c5fe6-185">99</span><span class="sxs-lookup"><span data-stu-id="c5fe6-185">99</span></span>            | <span data-ttu-id="c5fe6-186">$50</span><span class="sxs-lookup"><span data-stu-id="c5fe6-186">$50</span></span>            |
| <span data-ttu-id="c5fe6-187">81333</span><span class="sxs-lookup"><span data-stu-id="c5fe6-187">81333</span></span> | <span data-ttu-id="c5fe6-188">2</span><span class="sxs-lookup"><span data-stu-id="c5fe6-188">2</span></span>             | <span data-ttu-id="c5fe6-189">11</span><span class="sxs-lookup"><span data-stu-id="c5fe6-189">11</span></span>            | <span data-ttu-id="c5fe6-190">$30</span><span class="sxs-lookup"><span data-stu-id="c5fe6-190">$30</span></span>            |
| <span data-ttu-id="c5fe6-191">81334</span><span class="sxs-lookup"><span data-stu-id="c5fe6-191">81334</span></span> | <span data-ttu-id="c5fe6-192">3</span><span class="sxs-lookup"><span data-stu-id="c5fe6-192">3</span></span>             | <span data-ttu-id="c5fe6-193">99</span><span class="sxs-lookup"><span data-stu-id="c5fe6-193">99</span></span>            | <span data-ttu-id="c5fe6-194">$10</span><span class="sxs-lookup"><span data-stu-id="c5fe6-194">$10</span></span>            |
| <span data-ttu-id="c5fe6-195">81334</span><span class="sxs-lookup"><span data-stu-id="c5fe6-195">81334</span></span> | <span data-ttu-id="c5fe6-196">3</span><span class="sxs-lookup"><span data-stu-id="c5fe6-196">3</span></span>             | <span data-ttu-id="c5fe6-197">21</span><span class="sxs-lookup"><span data-stu-id="c5fe6-197">21</span></span>            | <span data-ttu-id="c5fe6-198">$5</span><span class="sxs-lookup"><span data-stu-id="c5fe6-198">$5</span></span>             |

<span data-ttu-id="c5fe6-199">Da konfigurationen af automatiske gebyrer er indstillet til at bliver beregnet forholdsmæssigt til matchende salgslinjer, udfører systemet følgende beregning.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="c5fe6-200">Alle varer, der har samme leveringsmåde, grupperes sammen, og systemet beregner den samlede produktværdi for varerne i gruppen.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="c5fe6-201">**Leveringsmåde 11**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="c5fe6-202">Vare 81331, antal 1 = $10</span><span class="sxs-lookup"><span data-stu-id="c5fe6-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="c5fe6-203">Vare 81333, antal 2 = $60 netto ($30 pr. enhed)</span><span class="sxs-lookup"><span data-stu-id="c5fe6-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="c5fe6-204">**Samlet værdi af produktet for leveringsmåde 11 = $70**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="c5fe6-205">**Leveringsmåde 99**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="c5fe6-206">Vare 81332, antal 1 = $50</span><span class="sxs-lookup"><span data-stu-id="c5fe6-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="c5fe6-207">Vare 81334, antal 3 = $30 netto</span><span class="sxs-lookup"><span data-stu-id="c5fe6-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="c5fe6-208">**Samlet værdi af produktet for leveringsmåde 99 = $80**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="c5fe6-209">**Leveringsmåde 21**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="c5fe6-210">Vare 81334, antal 3 = $15 netto</span><span class="sxs-lookup"><span data-stu-id="c5fe6-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="c5fe6-211">**Samlet værdi af produktet for leveringsmåde 21 = $15**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="c5fe6-212">Systemet søger efter konfigurationen for automatiske gebyrer på hovedniveau, der svarer til debitor- og leveringsmådeindstillingerne for hver gruppe af varer.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="c5fe6-213">Hvis konfigurationen findes, søges der i den niveaudelte konfiguration efter det gebyr, som skal anvendes, baseret på den samlede produktværdi af varer i leveringsmådegruppen.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="c5fe6-214">**Leveringsmåde 11**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="c5fe6-215">Samlet produktværdi = $70</span><span class="sxs-lookup"><span data-stu-id="c5fe6-215">Total product value = $70</span></span>
    - <span data-ttu-id="c5fe6-216">**Gebyrværdi = $7**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-216">**Charge value = $7**</span></span>

    <span data-ttu-id="c5fe6-217">**Leveringsmåde 99**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="c5fe6-218">Samlet produktværdi = $80</span><span class="sxs-lookup"><span data-stu-id="c5fe6-218">Total product value = $80</span></span>
    - <span data-ttu-id="c5fe6-219">**Gebyrværdi = $15**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-219">**Charge value = $15**</span></span>

    <span data-ttu-id="c5fe6-220">**Leveringsmåde 21**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="c5fe6-221">Samlet produktværdi = $15</span><span class="sxs-lookup"><span data-stu-id="c5fe6-221">Total product value = $15</span></span>
    - <span data-ttu-id="c5fe6-222">**Gebyrværdi = $0** (ingen automatiske gebyrer er konfigureret for denne kombination af en kunde og en leveringsmåde).</span><span class="sxs-lookup"><span data-stu-id="c5fe6-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![Gebyrer for leveringsmåde 11 falder inden for det markerede niveau](media/step2mode11.png)

    ![Gebyrer for leveringsmåde 99 falder inden for det markerede niveau](media/step2mode99.png)

3. <span data-ttu-id="c5fe6-225">Systemet beregner den gebyrværdi, der skal anvendes på hver linje baseret på forholdsmæssig beregningslogik, der vurderer den proportionale værdi for linjen i forhold til gruppens samlede produktværdi.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="c5fe6-226">**Leveringsmåde 11**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="c5fe6-227">Gebyrværdi = $7</span><span class="sxs-lookup"><span data-stu-id="c5fe6-227">Charge value = $7</span></span>
    - <span data-ttu-id="c5fe6-228">Gruppeproduktværdi = $70</span><span class="sxs-lookup"><span data-stu-id="c5fe6-228">Group product value = $70</span></span>
    - <span data-ttu-id="c5fe6-229">Værdi for linje 1 = $10 (= 14,2857 % af gruppeværdien)</span><span class="sxs-lookup"><span data-stu-id="c5fe6-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="c5fe6-230">Værdi for linje 3 = $60 (= 85,7143 % af gruppeværdien)</span><span class="sxs-lookup"><span data-stu-id="c5fe6-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="c5fe6-231">**Linjegebyr for linje 1 = $1**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="c5fe6-232">**Linjegebyr for linje 3 = $6**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="c5fe6-233">**Leveringsmåde 99**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="c5fe6-234">Gebyrværdi = $15</span><span class="sxs-lookup"><span data-stu-id="c5fe6-234">Charge value = $15</span></span>
    - <span data-ttu-id="c5fe6-235">Gruppeproduktværdi = $80</span><span class="sxs-lookup"><span data-stu-id="c5fe6-235">Group product value = $80</span></span>
    - <span data-ttu-id="c5fe6-236">Værdi for linje 2 = $50 (= 62,5 % af gruppeværdien)</span><span class="sxs-lookup"><span data-stu-id="c5fe6-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="c5fe6-237">Værdi for linje 4 = $30 (= 37,5 % af gruppeværdien)</span><span class="sxs-lookup"><span data-stu-id="c5fe6-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="c5fe6-238">**Linjegebyr for linje 2 = $9,38**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="c5fe6-239">**Linjegebyr for linje 4 = $5,62**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="c5fe6-240">**Leveringsmåde 21**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="c5fe6-241">Gebyrværdi = $0</span><span class="sxs-lookup"><span data-stu-id="c5fe6-241">Charge value = $0</span></span>
    - <span data-ttu-id="c5fe6-242">Gruppeproduktværdi = $15</span><span class="sxs-lookup"><span data-stu-id="c5fe6-242">Group product value = $15</span></span>
    - <span data-ttu-id="c5fe6-243">Værdi for linje 5 = $15 (= 100 % af gruppeværdien)</span><span class="sxs-lookup"><span data-stu-id="c5fe6-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="c5fe6-244">**Linjegebyr for linje 5 = $0**</span><span class="sxs-lookup"><span data-stu-id="c5fe6-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="c5fe6-245">Derfor tildeles vare 81334 et fragtgebyr på $5,62 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="c5fe6-246">Du kan få vist disse gebyrer på siden **Vedligehold gebyrer** for salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="c5fe6-247">I følgende illustration vises, hvordan denne side ser ud for vare 81334.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-247">The following illustration shows what this page looks like for item 81334.</span></span>

![Forholdsmæssigt beregnede gebyrer på salgslinje for vare 81334](media/proratedlinecharge.png)

<span data-ttu-id="c5fe6-249">Når denne beregningsmetode bruges til en delvis returnering, og hvis gebyrkoden kan refunderes, er det kun en del af det gebyr, som er allokeret til den pågældende linje, der refunderes, når varen er returneret.</span><span class="sxs-lookup"><span data-stu-id="c5fe6-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5fe6-250">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c5fe6-250">Additional resources</span></span>

[<span data-ttu-id="c5fe6-251">Avancerede automatiske gebyrer for omni-kanal</span><span class="sxs-lookup"><span data-stu-id="c5fe6-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="c5fe6-252">Aktivere og konfigurere automatiske gebyrer efter kanal</span><span class="sxs-lookup"><span data-stu-id="c5fe6-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]