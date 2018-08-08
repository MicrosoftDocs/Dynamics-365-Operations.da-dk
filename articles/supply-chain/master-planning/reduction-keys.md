---
title: "Reduktionsnøgler"
description: "Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle. Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver. Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 3e62431a1fdbeb81dda68297f034ee00adece079
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="reduction-keys"></a><span data-ttu-id="42646-105">Reduktionsnøgler</span><span class="sxs-lookup"><span data-stu-id="42646-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42646-106">Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle.</span><span class="sxs-lookup"><span data-stu-id="42646-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="42646-107">Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver.</span><span class="sxs-lookup"><span data-stu-id="42646-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="42646-108">Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov.</span><span class="sxs-lookup"><span data-stu-id="42646-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="42646-109">Eksempel 1: Budgetreduktionsprincip for Procent - reduktionsnøgle</span><span class="sxs-lookup"><span data-stu-id="42646-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="42646-110">Dette eksempel viser, hvordan en reduktionsnøgle reducerer efterspørgselsprognosebehovet i henhold til de procenter og tidsperioder, der er defineret i reduktionsnøglen.</span><span class="sxs-lookup"><span data-stu-id="42646-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="42646-111">På siden **Reduktionsnøgler** skal du angive følgende linjer.</span><span class="sxs-lookup"><span data-stu-id="42646-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="42646-112">Byttepenge</span><span class="sxs-lookup"><span data-stu-id="42646-112">Change</span></span> | <span data-ttu-id="42646-113">Enhed</span><span class="sxs-lookup"><span data-stu-id="42646-113">Unit</span></span>  | <span data-ttu-id="42646-114">Procent</span><span class="sxs-lookup"><span data-stu-id="42646-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="42646-115">1</span><span class="sxs-lookup"><span data-stu-id="42646-115">1</span></span>    | <span data-ttu-id="42646-116">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-116">Month</span></span> |   <span data-ttu-id="42646-117">100</span><span class="sxs-lookup"><span data-stu-id="42646-117">100</span></span>   |
   |   <span data-ttu-id="42646-118">2</span><span class="sxs-lookup"><span data-stu-id="42646-118">2</span></span>    | <span data-ttu-id="42646-119">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-119">Month</span></span> |   <span data-ttu-id="42646-120">75</span><span class="sxs-lookup"><span data-stu-id="42646-120">75</span></span>    |
   |   <span data-ttu-id="42646-121">3</span><span class="sxs-lookup"><span data-stu-id="42646-121">3</span></span>    | <span data-ttu-id="42646-122">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-122">Month</span></span> |   <span data-ttu-id="42646-123">50</span><span class="sxs-lookup"><span data-stu-id="42646-123">50</span></span>    |
   |   <span data-ttu-id="42646-124">4</span><span class="sxs-lookup"><span data-stu-id="42646-124">4</span></span>    | <span data-ttu-id="42646-125">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-125">Month</span></span> |   <span data-ttu-id="42646-126">25</span><span class="sxs-lookup"><span data-stu-id="42646-126">25</span></span>    |


2. <span data-ttu-id="42646-127">Knyt reduktionsnøglen til varedisponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="42646-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="42646-128">Vælg **Procent - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="42646-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="42646-129">Opret en efterspørgselsprognose på 1000 enheder pr. måned.</span><span class="sxs-lookup"><span data-stu-id="42646-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="42646-130">Hvis du kører hovedplanlægning pr. 1. januar, forbruges efterspørgselsprognosebehovet i overensstemmelse med den procentdel, som du konfigurerer på siden **Reduktionsnøgler**.</span><span class="sxs-lookup"><span data-stu-id="42646-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="42646-131">Følgende behovsantal overføres til behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="42646-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="42646-132">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-132">Month</span></span>                | <span data-ttu-id="42646-133">Antal krævede enheder</span><span class="sxs-lookup"><span data-stu-id="42646-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="42646-134">Januar</span><span class="sxs-lookup"><span data-stu-id="42646-134">January</span></span>              | <span data-ttu-id="42646-135">0</span><span class="sxs-lookup"><span data-stu-id="42646-135">0</span></span>                         |
| <span data-ttu-id="42646-136">Februar</span><span class="sxs-lookup"><span data-stu-id="42646-136">February</span></span>             | <span data-ttu-id="42646-137">250</span><span class="sxs-lookup"><span data-stu-id="42646-137">250</span></span>                       |
| <span data-ttu-id="42646-138">Marts</span><span class="sxs-lookup"><span data-stu-id="42646-138">March</span></span>                | <span data-ttu-id="42646-139">500</span><span class="sxs-lookup"><span data-stu-id="42646-139">500</span></span>                       |
| <span data-ttu-id="42646-140">April</span><span class="sxs-lookup"><span data-stu-id="42646-140">April</span></span>                | <span data-ttu-id="42646-141">750</span><span class="sxs-lookup"><span data-stu-id="42646-141">750</span></span>                       |
| <span data-ttu-id="42646-142">Maj-december</span><span class="sxs-lookup"><span data-stu-id="42646-142">May through December</span></span> | <span data-ttu-id="42646-143">1.000</span><span class="sxs-lookup"><span data-stu-id="42646-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="42646-144">Eksempel 2: Posteringer – reduktionsnøgle for budgetreduktionsprincip</span><span class="sxs-lookup"><span data-stu-id="42646-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="42646-145">Dette eksempel viser, hvordan de faktiske ordrer, der forekommer i de perioder, der er defineret i reduktionsnøglen, reducerer efterspørgselsprognosebehovet.</span><span class="sxs-lookup"><span data-stu-id="42646-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="42646-146">Vælg **Posteringer - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="42646-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="42646-147">Der findes følgende salgsordrer pr. 1. januar.</span><span class="sxs-lookup"><span data-stu-id="42646-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="42646-148">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-148">Month</span></span>    | <span data-ttu-id="42646-149">Antal bestilte enheder</span><span class="sxs-lookup"><span data-stu-id="42646-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="42646-150">Januar</span><span class="sxs-lookup"><span data-stu-id="42646-150">January</span></span>  | <span data-ttu-id="42646-151">956</span><span class="sxs-lookup"><span data-stu-id="42646-151">956</span></span>                      |
| <span data-ttu-id="42646-152">Februar</span><span class="sxs-lookup"><span data-stu-id="42646-152">February</span></span> | <span data-ttu-id="42646-153">1.176</span><span class="sxs-lookup"><span data-stu-id="42646-153">1,176</span></span>                    |
| <span data-ttu-id="42646-154">Marts</span><span class="sxs-lookup"><span data-stu-id="42646-154">March</span></span>    | <span data-ttu-id="42646-155">451</span><span class="sxs-lookup"><span data-stu-id="42646-155">451</span></span>                      |
| <span data-ttu-id="42646-156">April</span><span class="sxs-lookup"><span data-stu-id="42646-156">April</span></span>    | <span data-ttu-id="42646-157">119</span><span class="sxs-lookup"><span data-stu-id="42646-157">119</span></span>                      |

<span data-ttu-id="42646-158">Hvis du bruger samme efterspørgselsprognose på 1.000 enheder pr. måned anvendes, overføres følgende behovsantal til behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="42646-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="42646-159">Måned</span><span class="sxs-lookup"><span data-stu-id="42646-159">Month</span></span>                | <span data-ttu-id="42646-160">Antal krævede enheder</span><span class="sxs-lookup"><span data-stu-id="42646-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="42646-161">Januar</span><span class="sxs-lookup"><span data-stu-id="42646-161">January</span></span>              | <span data-ttu-id="42646-162">44</span><span class="sxs-lookup"><span data-stu-id="42646-162">44</span></span>                        |
| <span data-ttu-id="42646-163">Februar</span><span class="sxs-lookup"><span data-stu-id="42646-163">February</span></span>             | <span data-ttu-id="42646-164">0</span><span class="sxs-lookup"><span data-stu-id="42646-164">0</span></span>                         |
| <span data-ttu-id="42646-165">Marts</span><span class="sxs-lookup"><span data-stu-id="42646-165">March</span></span>                | <span data-ttu-id="42646-166">549</span><span class="sxs-lookup"><span data-stu-id="42646-166">549</span></span>                       |
| <span data-ttu-id="42646-167">April</span><span class="sxs-lookup"><span data-stu-id="42646-167">April</span></span>                | <span data-ttu-id="42646-168">881</span><span class="sxs-lookup"><span data-stu-id="42646-168">881</span></span>                       |
| <span data-ttu-id="42646-169">Maj-december</span><span class="sxs-lookup"><span data-stu-id="42646-169">May through December</span></span> | <span data-ttu-id="42646-170">1.000</span><span class="sxs-lookup"><span data-stu-id="42646-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="42646-171">Eksempel 3: Posteringer – reduktionsprincip for dynamisk budgetperiode</span><span class="sxs-lookup"><span data-stu-id="42646-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="42646-172">I de fleste tilfælde konfigureres systemer, så posteringer reducerer efterspørgselsprognose inden for specifikke budgetperioder: uger, måneder og så videre.</span><span class="sxs-lookup"><span data-stu-id="42646-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="42646-173">Disse perioder er defineret i reduktionsnøglen.</span><span class="sxs-lookup"><span data-stu-id="42646-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="42646-174">Men tiden mellem to linjer i behovsprognosen kan også *omfatte* en periode.</span><span class="sxs-lookup"><span data-stu-id="42646-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="42646-175">Opret en behovsprognose for følgende datoer og antal.</span><span class="sxs-lookup"><span data-stu-id="42646-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="42646-176">Dato</span><span class="sxs-lookup"><span data-stu-id="42646-176">Date</span></span>       | <span data-ttu-id="42646-177">Behovsprognose</span><span class="sxs-lookup"><span data-stu-id="42646-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="42646-178">1. januar</span><span class="sxs-lookup"><span data-stu-id="42646-178">January 1</span></span>  | <span data-ttu-id="42646-179">1.000</span><span class="sxs-lookup"><span data-stu-id="42646-179">1,000</span></span>           |
   | <span data-ttu-id="42646-180">5. januar</span><span class="sxs-lookup"><span data-stu-id="42646-180">January 5</span></span>  | <span data-ttu-id="42646-181">500</span><span class="sxs-lookup"><span data-stu-id="42646-181">500</span></span>             |
   | <span data-ttu-id="42646-182">12. januar</span><span class="sxs-lookup"><span data-stu-id="42646-182">January 12</span></span> | <span data-ttu-id="42646-183">1.000</span><span class="sxs-lookup"><span data-stu-id="42646-183">1,000</span></span>           |

   <span data-ttu-id="42646-184">I dette budget er der ikke en klar periode mellem budgetdatoerne: mellem første og anden dato er der et interval på fire dage, og mellem den anden og tredje dato er det et interval på syv dage.</span><span class="sxs-lookup"><span data-stu-id="42646-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="42646-185">Disse forskellige intervaller er dynamiske perioder.</span><span class="sxs-lookup"><span data-stu-id="42646-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="42646-186">Opret salgsordrelinjer på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="42646-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="42646-187">Dato</span><span class="sxs-lookup"><span data-stu-id="42646-187">Date</span></span>                             | <span data-ttu-id="42646-188">Salgsordremængde</span><span class="sxs-lookup"><span data-stu-id="42646-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="42646-189">15. december forrige år</span><span class="sxs-lookup"><span data-stu-id="42646-189">December 15 in the previous year</span></span> | <span data-ttu-id="42646-190">500</span><span class="sxs-lookup"><span data-stu-id="42646-190">500</span></span>                  |
   | <span data-ttu-id="42646-191">3. januar</span><span class="sxs-lookup"><span data-stu-id="42646-191">January 3</span></span>                        | <span data-ttu-id="42646-192">100</span><span class="sxs-lookup"><span data-stu-id="42646-192">100</span></span>                  |
   | <span data-ttu-id="42646-193">10. januar</span><span class="sxs-lookup"><span data-stu-id="42646-193">January 10</span></span>                       | <span data-ttu-id="42646-194">200</span><span class="sxs-lookup"><span data-stu-id="42646-194">200</span></span>                  |

<span data-ttu-id="42646-195">Budgettet reduceres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="42646-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="42646-196">Den første salgsordre er ikke inden for en periode, så det reducerer ikke et budget.</span><span class="sxs-lookup"><span data-stu-id="42646-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="42646-197">Den anden salgsordre ligger mellem d. 1-5. januar, så det vil reducere budgettet for den 1. januar med 100.</span><span class="sxs-lookup"><span data-stu-id="42646-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="42646-198">Den tredje salgsordre ligger mellem d. 5-12. januar, så det vil reducere budgettet for den 5. januar med 200.</span><span class="sxs-lookup"><span data-stu-id="42646-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="42646-199">Der oprettes følgende ordreforslaget for at imødekomme budgettet.</span><span class="sxs-lookup"><span data-stu-id="42646-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="42646-200">Dato for behovsprognose</span><span class="sxs-lookup"><span data-stu-id="42646-200">Demand forecast date</span></span> | <span data-ttu-id="42646-201">Reduceret antal</span><span class="sxs-lookup"><span data-stu-id="42646-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="42646-202">1. januar</span><span class="sxs-lookup"><span data-stu-id="42646-202">January 1</span></span>            | <span data-ttu-id="42646-203">900</span><span class="sxs-lookup"><span data-stu-id="42646-203">900</span></span>              |
| <span data-ttu-id="42646-204">5. januar</span><span class="sxs-lookup"><span data-stu-id="42646-204">January 5</span></span>            | <span data-ttu-id="42646-205">300</span><span class="sxs-lookup"><span data-stu-id="42646-205">300</span></span>              |
| <span data-ttu-id="42646-206">12. januar</span><span class="sxs-lookup"><span data-stu-id="42646-206">January 12</span></span>           | <span data-ttu-id="42646-207">1.000</span><span class="sxs-lookup"><span data-stu-id="42646-207">1,000</span></span>            |

<span data-ttu-id="42646-208">Her er en oversigt over reduktionen **Posteringer - dynamisk periode**:</span><span class="sxs-lookup"><span data-stu-id="42646-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="42646-209">Budgetbehovet reduceres via de faktiske ordreposteringer, der forekommer i den dynamiske periode.</span><span class="sxs-lookup"><span data-stu-id="42646-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="42646-210">Den dynamiske periode dækker de aktuelle budgetdatoer og slutter ved starten af det næste budget.</span><span class="sxs-lookup"><span data-stu-id="42646-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="42646-211">Til denne metode hverken bruges eller kræves en reduktionsnøgle.</span><span class="sxs-lookup"><span data-stu-id="42646-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="42646-212">Når denne indstilling bruges, forekommer følgende funktionsmåde:</span><span class="sxs-lookup"><span data-stu-id="42646-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="42646-213">Hvis budgettet reduceres helt, bliver budgetbehovet for det aktuelle budget 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="42646-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="42646-214">Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.</span><span class="sxs-lookup"><span data-stu-id="42646-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="42646-215">Tidshorisonter medtages i beregningen af budgetreduktionen.</span><span class="sxs-lookup"><span data-stu-id="42646-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="42646-216">Positive dage medtages i beregningen af budgetreduktionen.</span><span class="sxs-lookup"><span data-stu-id="42646-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="42646-217">Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.</span><span class="sxs-lookup"><span data-stu-id="42646-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="42646-218">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="42646-218">Additional resources</span></span>
--------

[<span data-ttu-id="42646-219">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="42646-219">Master plans</span></span>](master-plans.md)




