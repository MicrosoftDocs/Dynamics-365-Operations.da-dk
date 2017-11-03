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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 506ca3aac7ad271ca7472f3b74627e94d97a74ee
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="a22b5-105">Reduktionsnøgler</span><span class="sxs-lookup"><span data-stu-id="a22b5-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a22b5-106">Denne artikel indeholder eksempler på, hvordan du konfigurerer en reduktionsnøgle.</span><span class="sxs-lookup"><span data-stu-id="a22b5-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="a22b5-107">Den indeholder oplysninger om de forskellige indstillinger for reduktionsnøglen og resultaterne af hver.</span><span class="sxs-lookup"><span data-stu-id="a22b5-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="a22b5-108">Du kan bruge en reduktionsnøgle til at definere, hvordan du kan reducere budgetbehov.</span><span class="sxs-lookup"><span data-stu-id="a22b5-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="a22b5-109">Eksempel 1: Budgetreduktionsprincip for Procent - reduktionsnøgle</span><span class="sxs-lookup"><span data-stu-id="a22b5-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="a22b5-110">Dette eksempel viser, hvordan en reduktionsnøgle reducerer efterspørgselsprognosebehovet i henhold til de procenter og tidsperioder, der er defineret i reduktionsnøglen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="a22b5-111">På siden **Reduktionsnøgler** skal du angive følgende linjer.</span><span class="sxs-lookup"><span data-stu-id="a22b5-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="a22b5-112">Byttepenge</span><span class="sxs-lookup"><span data-stu-id="a22b5-112">Change</span></span> | <span data-ttu-id="a22b5-113">Enhed</span><span class="sxs-lookup"><span data-stu-id="a22b5-113">Unit</span></span>  | <span data-ttu-id="a22b5-114">Procent</span><span class="sxs-lookup"><span data-stu-id="a22b5-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="a22b5-115">1</span><span class="sxs-lookup"><span data-stu-id="a22b5-115">1</span></span>      | <span data-ttu-id="a22b5-116">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-116">Month</span></span> | <span data-ttu-id="a22b5-117">100</span><span class="sxs-lookup"><span data-stu-id="a22b5-117">100</span></span>     |
    | <span data-ttu-id="a22b5-118">2</span><span class="sxs-lookup"><span data-stu-id="a22b5-118">2</span></span>      | <span data-ttu-id="a22b5-119">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-119">Month</span></span> | <span data-ttu-id="a22b5-120">75</span><span class="sxs-lookup"><span data-stu-id="a22b5-120">75</span></span>      |
    | <span data-ttu-id="a22b5-121">3</span><span class="sxs-lookup"><span data-stu-id="a22b5-121">3</span></span>      | <span data-ttu-id="a22b5-122">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-122">Month</span></span> | <span data-ttu-id="a22b5-123">50</span><span class="sxs-lookup"><span data-stu-id="a22b5-123">50</span></span>      |
    | <span data-ttu-id="a22b5-124">4</span><span class="sxs-lookup"><span data-stu-id="a22b5-124">4</span></span>      | <span data-ttu-id="a22b5-125">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-125">Month</span></span> | <span data-ttu-id="a22b5-126">25</span><span class="sxs-lookup"><span data-stu-id="a22b5-126">25</span></span>      |

2.  <span data-ttu-id="a22b5-127">Knyt reduktionsnøglen til varedisponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="a22b5-128">Vælg **Procent - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a22b5-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="a22b5-129">Opret en efterspørgselsprognose på 1000 enheder pr. måned.</span><span class="sxs-lookup"><span data-stu-id="a22b5-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="a22b5-130">Hvis du kører hovedplanlægning pr. 1. januar, forbruges efterspørgselsprognosebehovet i overensstemmelse med den procentdel, som du konfigurerer på siden **Reduktionsnøgler**.</span><span class="sxs-lookup"><span data-stu-id="a22b5-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="a22b5-131">Følgende behovsantal overføres til behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="a22b5-132">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-132">Month</span></span>                | <span data-ttu-id="a22b5-133">Antal krævede enheder</span><span class="sxs-lookup"><span data-stu-id="a22b5-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="a22b5-134">Januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-134">January</span></span>              | <span data-ttu-id="a22b5-135">0</span><span class="sxs-lookup"><span data-stu-id="a22b5-135">0</span></span>                         |
| <span data-ttu-id="a22b5-136">Februar</span><span class="sxs-lookup"><span data-stu-id="a22b5-136">February</span></span>             | <span data-ttu-id="a22b5-137">250</span><span class="sxs-lookup"><span data-stu-id="a22b5-137">250</span></span>                       |
| <span data-ttu-id="a22b5-138">Marts</span><span class="sxs-lookup"><span data-stu-id="a22b5-138">March</span></span>                | <span data-ttu-id="a22b5-139">500</span><span class="sxs-lookup"><span data-stu-id="a22b5-139">500</span></span>                       |
| <span data-ttu-id="a22b5-140">April</span><span class="sxs-lookup"><span data-stu-id="a22b5-140">April</span></span>                | <span data-ttu-id="a22b5-141">750</span><span class="sxs-lookup"><span data-stu-id="a22b5-141">750</span></span>                       |
| <span data-ttu-id="a22b5-142">Maj-december</span><span class="sxs-lookup"><span data-stu-id="a22b5-142">May through December</span></span> | <span data-ttu-id="a22b5-143">1.000</span><span class="sxs-lookup"><span data-stu-id="a22b5-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="a22b5-144">Eksempel 2: Posteringer – reduktionsnøgle for budgetreduktionsprincip</span><span class="sxs-lookup"><span data-stu-id="a22b5-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="a22b5-145">Dette eksempel viser, hvordan de faktiske ordrer, der forekommer i de perioder, der er defineret i reduktionsnøglen, reducerer efterspørgselsprognosebehovet.</span><span class="sxs-lookup"><span data-stu-id="a22b5-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="a22b5-146">Vælg **Posteringer - reduktionsnøgle** i feltet **Reduktionsprincip** på siden **Behovsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a22b5-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="a22b5-147">Der findes følgende salgsordrer pr. 1. januar.</span><span class="sxs-lookup"><span data-stu-id="a22b5-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="a22b5-148">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-148">Month</span></span>    | <span data-ttu-id="a22b5-149">Antal bestilte enheder</span><span class="sxs-lookup"><span data-stu-id="a22b5-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="a22b5-150">Januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-150">January</span></span>  | <span data-ttu-id="a22b5-151">956</span><span class="sxs-lookup"><span data-stu-id="a22b5-151">956</span></span>                      |
| <span data-ttu-id="a22b5-152">Februar</span><span class="sxs-lookup"><span data-stu-id="a22b5-152">February</span></span> | <span data-ttu-id="a22b5-153">1.176</span><span class="sxs-lookup"><span data-stu-id="a22b5-153">1,176</span></span>                    |
| <span data-ttu-id="a22b5-154">Marts</span><span class="sxs-lookup"><span data-stu-id="a22b5-154">March</span></span>    | <span data-ttu-id="a22b5-155">451</span><span class="sxs-lookup"><span data-stu-id="a22b5-155">451</span></span>                      |
| <span data-ttu-id="a22b5-156">April</span><span class="sxs-lookup"><span data-stu-id="a22b5-156">April</span></span>    | <span data-ttu-id="a22b5-157">119</span><span class="sxs-lookup"><span data-stu-id="a22b5-157">119</span></span>                      |

<span data-ttu-id="a22b5-158">Hvis du bruger samme efterspørgselsprognose på 1.000 enheder pr. måned anvendes, overføres følgende behovsantal til behovsplanen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="a22b5-159">Måned</span><span class="sxs-lookup"><span data-stu-id="a22b5-159">Month</span></span>                | <span data-ttu-id="a22b5-160">Antal krævede enheder</span><span class="sxs-lookup"><span data-stu-id="a22b5-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="a22b5-161">Januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-161">January</span></span>              | <span data-ttu-id="a22b5-162">44</span><span class="sxs-lookup"><span data-stu-id="a22b5-162">44</span></span>                        |
| <span data-ttu-id="a22b5-163">Februar</span><span class="sxs-lookup"><span data-stu-id="a22b5-163">February</span></span>             | <span data-ttu-id="a22b5-164">0</span><span class="sxs-lookup"><span data-stu-id="a22b5-164">0</span></span>                         |
| <span data-ttu-id="a22b5-165">Marts</span><span class="sxs-lookup"><span data-stu-id="a22b5-165">March</span></span>                | <span data-ttu-id="a22b5-166">549</span><span class="sxs-lookup"><span data-stu-id="a22b5-166">549</span></span>                       |
| <span data-ttu-id="a22b5-167">April</span><span class="sxs-lookup"><span data-stu-id="a22b5-167">April</span></span>                | <span data-ttu-id="a22b5-168">881</span><span class="sxs-lookup"><span data-stu-id="a22b5-168">881</span></span>                       |
| <span data-ttu-id="a22b5-169">Maj-december</span><span class="sxs-lookup"><span data-stu-id="a22b5-169">May through December</span></span> | <span data-ttu-id="a22b5-170">1.000</span><span class="sxs-lookup"><span data-stu-id="a22b5-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="a22b5-171">Eksempel 3: Posteringer – reduktionsprincip for dynamisk budgetperiode</span><span class="sxs-lookup"><span data-stu-id="a22b5-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="a22b5-172">I de fleste tilfælde konfigureres systemer, så posteringer reducerer efterspørgselsprognose inden for specifikke budgetperioder: uger, måneder og så videre.</span><span class="sxs-lookup"><span data-stu-id="a22b5-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="a22b5-173">Disse perioder er defineret i reduktionsnøglen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="a22b5-174">Men tiden mellem to linjer i behovsprognosen kan også *omfatte* en periode.</span><span class="sxs-lookup"><span data-stu-id="a22b5-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="a22b5-175">Opret en behovsprognose for følgende datoer og antal.</span><span class="sxs-lookup"><span data-stu-id="a22b5-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="a22b5-176">Dato</span><span class="sxs-lookup"><span data-stu-id="a22b5-176">Date</span></span>       | <span data-ttu-id="a22b5-177">Behovsprognose</span><span class="sxs-lookup"><span data-stu-id="a22b5-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="a22b5-178">1. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-178">January 1</span></span>  | <span data-ttu-id="a22b5-179">1.000</span><span class="sxs-lookup"><span data-stu-id="a22b5-179">1,000</span></span>           |
    | <span data-ttu-id="a22b5-180">5. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-180">January 5</span></span>  | <span data-ttu-id="a22b5-181">500</span><span class="sxs-lookup"><span data-stu-id="a22b5-181">500</span></span>             |
    | <span data-ttu-id="a22b5-182">12. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-182">January 12</span></span> | <span data-ttu-id="a22b5-183">1.000</span><span class="sxs-lookup"><span data-stu-id="a22b5-183">1,000</span></span>           |

    <span data-ttu-id="a22b5-184">I dette budget er der ikke en klar periode mellem budgetdatoerne: mellem første og anden dato er der et interval på fire dage, og mellem den anden og tredje dato er det et interval på syv dage.</span><span class="sxs-lookup"><span data-stu-id="a22b5-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="a22b5-185">Disse forskellige intervaller er dynamiske perioder.</span><span class="sxs-lookup"><span data-stu-id="a22b5-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="a22b5-186">Opret salgsordrelinjer på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a22b5-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="a22b5-187">Dato</span><span class="sxs-lookup"><span data-stu-id="a22b5-187">Date</span></span>                             | <span data-ttu-id="a22b5-188">Salgsordremængde</span><span class="sxs-lookup"><span data-stu-id="a22b5-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="a22b5-189">15. december forrige år</span><span class="sxs-lookup"><span data-stu-id="a22b5-189">December 15 in the previous year</span></span> | <span data-ttu-id="a22b5-190">500</span><span class="sxs-lookup"><span data-stu-id="a22b5-190">500</span></span>                  |
    | <span data-ttu-id="a22b5-191">3. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-191">January 3</span></span>                        | <span data-ttu-id="a22b5-192">100</span><span class="sxs-lookup"><span data-stu-id="a22b5-192">100</span></span>                  |
    | <span data-ttu-id="a22b5-193">10. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-193">January 10</span></span>                       | <span data-ttu-id="a22b5-194">200</span><span class="sxs-lookup"><span data-stu-id="a22b5-194">200</span></span>                  |

<span data-ttu-id="a22b5-195">Budgettet reduceres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="a22b5-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="a22b5-196">Den første salgsordre er ikke inden for en periode, så det reducerer ikke et budget.</span><span class="sxs-lookup"><span data-stu-id="a22b5-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="a22b5-197">Den anden salgsordre ligger mellem d. 1-5. januar, så det vil reducere budgettet for den 1. januar med 100.</span><span class="sxs-lookup"><span data-stu-id="a22b5-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="a22b5-198">Den tredje salgsordre ligger mellem d. 5-12. januar, så det vil reducere budgettet for den 5. januar med 200.</span><span class="sxs-lookup"><span data-stu-id="a22b5-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="a22b5-199">Der oprettes følgende ordreforslaget for at imødekomme budgettet.</span><span class="sxs-lookup"><span data-stu-id="a22b5-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="a22b5-200">Dato for behovsprognose</span><span class="sxs-lookup"><span data-stu-id="a22b5-200">Demand forecast date</span></span> | <span data-ttu-id="a22b5-201">Reduceret antal</span><span class="sxs-lookup"><span data-stu-id="a22b5-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="a22b5-202">1. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-202">January 1</span></span>            | <span data-ttu-id="a22b5-203">900</span><span class="sxs-lookup"><span data-stu-id="a22b5-203">900</span></span>              |
| <span data-ttu-id="a22b5-204">5. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-204">January 5</span></span>            | <span data-ttu-id="a22b5-205">300</span><span class="sxs-lookup"><span data-stu-id="a22b5-205">300</span></span>              |
| <span data-ttu-id="a22b5-206">12. januar</span><span class="sxs-lookup"><span data-stu-id="a22b5-206">January 12</span></span>           | <span data-ttu-id="a22b5-207">1.000</span><span class="sxs-lookup"><span data-stu-id="a22b5-207">1,000</span></span>            |

<span data-ttu-id="a22b5-208">Her er en oversigt over reduktionen **Posteringer - dynamisk periode**:</span><span class="sxs-lookup"><span data-stu-id="a22b5-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="a22b5-209">Budgetbehovet reduceres via de faktiske ordreposteringer, der forekommer i den dynamiske periode.</span><span class="sxs-lookup"><span data-stu-id="a22b5-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="a22b5-210">Den dynamiske periode dækker de aktuelle budgetdatoer og slutter ved starten af det næste budget.</span><span class="sxs-lookup"><span data-stu-id="a22b5-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="a22b5-211">Til denne metode hverken bruges eller kræves en reduktionsnøgle.</span><span class="sxs-lookup"><span data-stu-id="a22b5-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="a22b5-212">Når denne indstilling bruges, forekommer følgende funktionsmåde:</span><span class="sxs-lookup"><span data-stu-id="a22b5-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="a22b5-213">Hvis budgettet reduceres helt, bliver budgetbehovet for det aktuelle budget 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="a22b5-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="a22b5-214">Hvis der ikke er noget fremtidigt budget, bliver budgetbehovet fra det sidst angivne budget reduceret.</span><span class="sxs-lookup"><span data-stu-id="a22b5-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="a22b5-215">Tidshorisonter medtages i beregningen af budgetreduktionen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="a22b5-216">Positive dage medtages i beregningen af budgetreduktionen.</span><span class="sxs-lookup"><span data-stu-id="a22b5-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="a22b5-217">Hvis de faktiske ordreposteringer overstiger budgetbehovet, overføres de resterende posteringer ikke til den næste budgetperiode.</span><span class="sxs-lookup"><span data-stu-id="a22b5-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="a22b5-218">Se også</span><span class="sxs-lookup"><span data-stu-id="a22b5-218">See also</span></span>
--------

[<span data-ttu-id="a22b5-219">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="a22b5-219">Master plans</span></span>](master-plans.md)




