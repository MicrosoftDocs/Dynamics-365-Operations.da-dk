---
title: Reduktionsnøgler
description: Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle. Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver. Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2019
ms.locfileid: "770910"
---
# <a name="reduction-keys"></a><span data-ttu-id="9b633-105">Reduktionsnøgler</span><span class="sxs-lookup"><span data-stu-id="9b633-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b633-106">Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle.</span><span class="sxs-lookup"><span data-stu-id="9b633-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="9b633-107">Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver.</span><span class="sxs-lookup"><span data-stu-id="9b633-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="9b633-108">Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov.</span><span class="sxs-lookup"><span data-stu-id="9b633-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="9b633-109">Eksempel 1: Budgetreduktionsprincip for Procent - reduktionsnøgle</span><span class="sxs-lookup"><span data-stu-id="9b633-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="9b633-110">Dette eksempel viser, hvordan en reduktionsnøgle reducerer efterspørgselsprognosebehovet i henhold til de procenter og tidsperioder, der er defineret i reduktionsnøglen.</span><span class="sxs-lookup"><span data-stu-id="9b633-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="9b633-111">På siden **Reduktionsnøgler** skal du angive følgende linjer.</span><span class="sxs-lookup"><span data-stu-id="9b633-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="9b633-112">Byttepenge</span><span class="sxs-lookup"><span data-stu-id="9b633-112">Change</span></span> | <span data-ttu-id="9b633-113">Enhed</span><span class="sxs-lookup"><span data-stu-id="9b633-113">Unit</span></span>  | <span data-ttu-id="9b633-114">Procent</span><span class="sxs-lookup"><span data-stu-id="9b633-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="9b633-115">1</span><span class="sxs-lookup"><span data-stu-id="9b633-115">1</span></span>    | <span data-ttu-id="9b633-116">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-116">Month</span></span> |   <span data-ttu-id="9b633-117">100</span><span class="sxs-lookup"><span data-stu-id="9b633-117">100</span></span>   |
   |   <span data-ttu-id="9b633-118">2</span><span class="sxs-lookup"><span data-stu-id="9b633-118">2</span></span>    | <span data-ttu-id="9b633-119">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-119">Month</span></span> |   <span data-ttu-id="9b633-120">75</span><span class="sxs-lookup"><span data-stu-id="9b633-120">75</span></span>    |
   |   <span data-ttu-id="9b633-121">3</span><span class="sxs-lookup"><span data-stu-id="9b633-121">3</span></span>    | <span data-ttu-id="9b633-122">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-122">Month</span></span> |   <span data-ttu-id="9b633-123">50</span><span class="sxs-lookup"><span data-stu-id="9b633-123">50</span></span>    |
   |   <span data-ttu-id="9b633-124">4</span><span class="sxs-lookup"><span data-stu-id="9b633-124">4</span></span>    | <span data-ttu-id="9b633-125">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-125">Month</span></span> |   <span data-ttu-id="9b633-126">25</span><span class="sxs-lookup"><span data-stu-id="9b633-126">25</span></span>    |


2. <span data-ttu-id="9b633-127">Knyt reduktionsnøglen til varedisponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="9b633-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="9b633-128">Vælg **Procent - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="9b633-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="9b633-129">Opret en efterspørgselsprognose på 1000 enheder pr. måned.</span><span class="sxs-lookup"><span data-stu-id="9b633-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="9b633-130">Hvis du kører hovedplanlægning pr. 1. januar, forbruges efterspørgselsprognosebehovet i overensstemmelse med den procentdel, som du konfigurerer på siden **Reduktionsnøgler**.</span><span class="sxs-lookup"><span data-stu-id="9b633-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="9b633-131">Følgende behovsantal overføres til behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="9b633-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="9b633-132">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-132">Month</span></span>                | <span data-ttu-id="9b633-133">Antal krævede enheder</span><span class="sxs-lookup"><span data-stu-id="9b633-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="9b633-134">Januar</span><span class="sxs-lookup"><span data-stu-id="9b633-134">January</span></span>              | <span data-ttu-id="9b633-135">0</span><span class="sxs-lookup"><span data-stu-id="9b633-135">0</span></span>                         |
| <span data-ttu-id="9b633-136">Februar</span><span class="sxs-lookup"><span data-stu-id="9b633-136">February</span></span>             | <span data-ttu-id="9b633-137">250</span><span class="sxs-lookup"><span data-stu-id="9b633-137">250</span></span>                       |
| <span data-ttu-id="9b633-138">Marts</span><span class="sxs-lookup"><span data-stu-id="9b633-138">March</span></span>                | <span data-ttu-id="9b633-139">500</span><span class="sxs-lookup"><span data-stu-id="9b633-139">500</span></span>                       |
| <span data-ttu-id="9b633-140">April</span><span class="sxs-lookup"><span data-stu-id="9b633-140">April</span></span>                | <span data-ttu-id="9b633-141">750</span><span class="sxs-lookup"><span data-stu-id="9b633-141">750</span></span>                       |
| <span data-ttu-id="9b633-142">Maj-december</span><span class="sxs-lookup"><span data-stu-id="9b633-142">May through December</span></span> | <span data-ttu-id="9b633-143">1.000</span><span class="sxs-lookup"><span data-stu-id="9b633-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="9b633-144">Eksempel 2: Posteringer – reduktionsnøgle for budgetreduktionsprincip</span><span class="sxs-lookup"><span data-stu-id="9b633-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="9b633-145">Dette eksempel viser, hvordan de faktiske ordrer, der forekommer i de perioder, der er defineret i reduktionsnøglen, reducerer efterspørgselsprognosebehovet.</span><span class="sxs-lookup"><span data-stu-id="9b633-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="9b633-146">Vælg **Posteringer - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="9b633-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="9b633-147">Der findes følgende salgsordrer pr. 1. januar.</span><span class="sxs-lookup"><span data-stu-id="9b633-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="9b633-148">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-148">Month</span></span>    | <span data-ttu-id="9b633-149">Antal bestilte enheder</span><span class="sxs-lookup"><span data-stu-id="9b633-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="9b633-150">Januar</span><span class="sxs-lookup"><span data-stu-id="9b633-150">January</span></span>  | <span data-ttu-id="9b633-151">956</span><span class="sxs-lookup"><span data-stu-id="9b633-151">956</span></span>                      |
| <span data-ttu-id="9b633-152">Februar</span><span class="sxs-lookup"><span data-stu-id="9b633-152">February</span></span> | <span data-ttu-id="9b633-153">1.176</span><span class="sxs-lookup"><span data-stu-id="9b633-153">1,176</span></span>                    |
| <span data-ttu-id="9b633-154">Marts</span><span class="sxs-lookup"><span data-stu-id="9b633-154">March</span></span>    | <span data-ttu-id="9b633-155">451</span><span class="sxs-lookup"><span data-stu-id="9b633-155">451</span></span>                      |
| <span data-ttu-id="9b633-156">April</span><span class="sxs-lookup"><span data-stu-id="9b633-156">April</span></span>    | <span data-ttu-id="9b633-157">119</span><span class="sxs-lookup"><span data-stu-id="9b633-157">119</span></span>                      |

<span data-ttu-id="9b633-158">Hvis du bruger samme efterspørgselsprognose på 1.000 enheder pr. måned anvendes, overføres følgende behovsantal til behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="9b633-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="9b633-159">Måned</span><span class="sxs-lookup"><span data-stu-id="9b633-159">Month</span></span>                | <span data-ttu-id="9b633-160">Antal krævede enheder</span><span class="sxs-lookup"><span data-stu-id="9b633-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="9b633-161">Januar</span><span class="sxs-lookup"><span data-stu-id="9b633-161">January</span></span>              | <span data-ttu-id="9b633-162">44</span><span class="sxs-lookup"><span data-stu-id="9b633-162">44</span></span>                        |
| <span data-ttu-id="9b633-163">Februar</span><span class="sxs-lookup"><span data-stu-id="9b633-163">February</span></span>             | <span data-ttu-id="9b633-164">0</span><span class="sxs-lookup"><span data-stu-id="9b633-164">0</span></span>                         |
| <span data-ttu-id="9b633-165">Marts</span><span class="sxs-lookup"><span data-stu-id="9b633-165">March</span></span>                | <span data-ttu-id="9b633-166">549</span><span class="sxs-lookup"><span data-stu-id="9b633-166">549</span></span>                       |
| <span data-ttu-id="9b633-167">April</span><span class="sxs-lookup"><span data-stu-id="9b633-167">April</span></span>                | <span data-ttu-id="9b633-168">881</span><span class="sxs-lookup"><span data-stu-id="9b633-168">881</span></span>                       |
| <span data-ttu-id="9b633-169">Maj-december</span><span class="sxs-lookup"><span data-stu-id="9b633-169">May through December</span></span> | <span data-ttu-id="9b633-170">1.000</span><span class="sxs-lookup"><span data-stu-id="9b633-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="9b633-171">Eksempel 3: Posteringer – reduktionsprincip for dynamisk budgetperiode</span><span class="sxs-lookup"><span data-stu-id="9b633-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="9b633-172">I de fleste tilfælde konfigureres systemer, så posteringer reducerer efterspørgselsprognose inden for specifikke budgetperioder: uger, måneder og så videre.</span><span class="sxs-lookup"><span data-stu-id="9b633-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="9b633-173">Disse perioder er defineret i reduktionsnøglen.</span><span class="sxs-lookup"><span data-stu-id="9b633-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="9b633-174">Men tiden mellem to linjer i behovsprognosen kan også *omfatte* en periode.</span><span class="sxs-lookup"><span data-stu-id="9b633-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="9b633-175">Opret en behovsprognose for følgende datoer og antal.</span><span class="sxs-lookup"><span data-stu-id="9b633-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="9b633-176">Dato</span><span class="sxs-lookup"><span data-stu-id="9b633-176">Date</span></span>       | <span data-ttu-id="9b633-177">Behovsprognose</span><span class="sxs-lookup"><span data-stu-id="9b633-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="9b633-178">1. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-178">January 1</span></span>  | <span data-ttu-id="9b633-179">1.000</span><span class="sxs-lookup"><span data-stu-id="9b633-179">1,000</span></span>           |
   | <span data-ttu-id="9b633-180">5. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-180">January 5</span></span>  | <span data-ttu-id="9b633-181">500</span><span class="sxs-lookup"><span data-stu-id="9b633-181">500</span></span>             |
   | <span data-ttu-id="9b633-182">12. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-182">January 12</span></span> | <span data-ttu-id="9b633-183">1.000</span><span class="sxs-lookup"><span data-stu-id="9b633-183">1,000</span></span>           |

   <span data-ttu-id="9b633-184">I dette budget er der ikke en klar periode mellem budgetdatoerne: mellem første og anden dato er der et interval på fire dage, og mellem den anden og tredje dato er det et interval på syv dage.</span><span class="sxs-lookup"><span data-stu-id="9b633-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="9b633-185">Disse forskellige intervaller er dynamiske perioder.</span><span class="sxs-lookup"><span data-stu-id="9b633-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="9b633-186">Opret salgsordrelinjer på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="9b633-186">Create sales order lines as follows.</span></span>

   | <span data-ttu-id="9b633-187">Dato</span><span class="sxs-lookup"><span data-stu-id="9b633-187">Date</span></span>                             | <span data-ttu-id="9b633-188">Salgsordremængde</span><span class="sxs-lookup"><span data-stu-id="9b633-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="9b633-189">15. december forrige år</span><span class="sxs-lookup"><span data-stu-id="9b633-189">December 15 in the previous year</span></span> | <span data-ttu-id="9b633-190">500</span><span class="sxs-lookup"><span data-stu-id="9b633-190">500</span></span>                  |
   | <span data-ttu-id="9b633-191">3. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-191">January 3</span></span>                        | <span data-ttu-id="9b633-192">100</span><span class="sxs-lookup"><span data-stu-id="9b633-192">100</span></span>                  |
   | <span data-ttu-id="9b633-193">10. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-193">January 10</span></span>                       | <span data-ttu-id="9b633-194">200</span><span class="sxs-lookup"><span data-stu-id="9b633-194">200</span></span>                  |

<span data-ttu-id="9b633-195">Budgettet reduceres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="9b633-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="9b633-196">Den første salgsordre er ikke inden for en periode, så det reducerer ikke et budget.</span><span class="sxs-lookup"><span data-stu-id="9b633-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="9b633-197">Den anden salgsordre ligger mellem d. 1-5. januar, så det vil reducere budgettet for den 1. januar med 100.</span><span class="sxs-lookup"><span data-stu-id="9b633-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="9b633-198">Den tredje salgsordre ligger mellem d. 5-12. januar, så det vil reducere budgettet for den 5. januar med 200.</span><span class="sxs-lookup"><span data-stu-id="9b633-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="9b633-199">Der oprettes følgende ordreforslaget for at imødekomme budgettet.</span><span class="sxs-lookup"><span data-stu-id="9b633-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="9b633-200">Dato for behovsprognose</span><span class="sxs-lookup"><span data-stu-id="9b633-200">Demand forecast date</span></span> | <span data-ttu-id="9b633-201">Reduceret antal</span><span class="sxs-lookup"><span data-stu-id="9b633-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="9b633-202">1. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-202">January 1</span></span>            | <span data-ttu-id="9b633-203">900</span><span class="sxs-lookup"><span data-stu-id="9b633-203">900</span></span>              |
| <span data-ttu-id="9b633-204">5. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-204">January 5</span></span>            | <span data-ttu-id="9b633-205">300</span><span class="sxs-lookup"><span data-stu-id="9b633-205">300</span></span>              |
| <span data-ttu-id="9b633-206">12. januar</span><span class="sxs-lookup"><span data-stu-id="9b633-206">January 12</span></span>           | <span data-ttu-id="9b633-207">1.000</span><span class="sxs-lookup"><span data-stu-id="9b633-207">1,000</span></span>            |

<span data-ttu-id="9b633-208">Her er en oversigt over reduktionen **Posteringer - dynamisk periode**:</span><span class="sxs-lookup"><span data-stu-id="9b633-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="9b633-209">Budgetbehovet reduceres via de faktiske ordreposteringer, der forekommer i den dynamiske periode.</span><span class="sxs-lookup"><span data-stu-id="9b633-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="9b633-210">Den dynamiske periode dækker de aktuelle budgetdatoer og slutter ved starten af det næste budget.</span><span class="sxs-lookup"><span data-stu-id="9b633-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="9b633-211">Til denne metode hverken bruges eller kræves en reduktionsnøgle.</span><span class="sxs-lookup"><span data-stu-id="9b633-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="9b633-212">Når denne indstilling bruges, forekommer følgende funktionsmåde:</span><span class="sxs-lookup"><span data-stu-id="9b633-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="9b633-213">Hvis budgettet reduceres helt, bliver budgetbehovet for det aktuelle budget 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="9b633-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="9b633-214">Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.</span><span class="sxs-lookup"><span data-stu-id="9b633-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="9b633-215">Tidshorisonter medtages i beregningen af budgetreduktionen.</span><span class="sxs-lookup"><span data-stu-id="9b633-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="9b633-216">Positive dage medtages i beregningen af budgetreduktionen.</span><span class="sxs-lookup"><span data-stu-id="9b633-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="9b633-217">Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.</span><span class="sxs-lookup"><span data-stu-id="9b633-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="9b633-218">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9b633-218">Additional resources</span></span>
--------

[<span data-ttu-id="9b633-219">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="9b633-219">Master plans</span></span>](master-plans.md)



