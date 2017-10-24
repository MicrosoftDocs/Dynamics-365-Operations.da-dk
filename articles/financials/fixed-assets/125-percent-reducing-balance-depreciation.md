---
title: 125 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 125 % saldoafskrivning.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 680396bd251cda603dbcd244664fa3421d12e85a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="136c7-103">125 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="136c7-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="136c7-104">Denne artikel indeholder en oversigt over afskrivningsmetoden 125 % saldoafskrivning.</span><span class="sxs-lookup"><span data-stu-id="136c7-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="136c7-105">Når du opretter en afskrivningsprofil for et anlægsaktiv og vælger **125 % saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="136c7-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="136c7-106">Denne procentdel beregnes på basis af aktivets levetid.</span><span class="sxs-lookup"><span data-stu-id="136c7-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="136c7-107">Hvis et aktiv f.eks. har en levetid på fem år, beregnes procentdelen som 25 % (125 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="136c7-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="136c7-108">Hvis du vil oprette en 125 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="136c7-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="136c7-109">Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.</span><span class="sxs-lookup"><span data-stu-id="136c7-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="136c7-110">Vælge et afskrivningsår</span><span class="sxs-lookup"><span data-stu-id="136c7-110">Select a depreciation year</span></span>
<span data-ttu-id="136c7-111">Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="136c7-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="136c7-112">Standardværdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="136c7-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="136c7-113">Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="136c7-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="136c7-114">Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="136c7-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="136c7-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="136c7-115">Calendar</span></span>

<span data-ttu-id="136c7-116">Du kan vælge at beholde standardværdien i feltet **Afskrivningsår**, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="136c7-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="136c7-117">Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="136c7-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="136c7-118">Afskrivningsgrundlaget er typisk bogført nettoværdi minus scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="136c7-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="136c7-119">I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="136c7-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="136c7-120">Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="136c7-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="136c7-121">**Årligt** bogfører et beløb d. 31. december.</span><span class="sxs-lookup"><span data-stu-id="136c7-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="136c7-122">**Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="136c7-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="136c7-123">**Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="136c7-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="136c7-124">**Halvårlig** bogfører et halvårligt beløb sidst i kalenderhalvåret (d. 30. juni og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="136c7-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="136c7-125">**Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.</span><span class="sxs-lookup"><span data-stu-id="136c7-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="136c7-126">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="136c7-126">Fiscal</span></span>

<span data-ttu-id="136c7-127">Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 125 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**.</span><span class="sxs-lookup"><span data-stu-id="136c7-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="136c7-128">Regnskabskalendere oprettes på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="136c7-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="136c7-129">I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli.</span><span class="sxs-lookup"><span data-stu-id="136c7-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="136c7-130">Regnskabsåret kan være længere eller kortere end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="136c7-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="136c7-131">Afskrivningen justeres automatisk for hver periode, og længden på det næste regnskabsår bestemmes af opsætningen af perioder på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="136c7-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="136c7-132">Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="136c7-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="136c7-133">**Årligt** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="136c7-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="136c7-134">**Regnskabsperiode** bogfører det samlede afskrivningsbeløb, der er beregnet for regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="136c7-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="136c7-135">Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="136c7-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="136c7-136">Eksempel på en 125 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="136c7-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="136c7-137">Anskaffelsesomkostning</span><span class="sxs-lookup"><span data-stu-id="136c7-137">Acquisition cost</span></span>               | <span data-ttu-id="136c7-138">11.000</span><span class="sxs-lookup"><span data-stu-id="136c7-138">11,000</span></span> |
| <span data-ttu-id="136c7-139">Restværdi</span><span class="sxs-lookup"><span data-stu-id="136c7-139">Salvage value</span></span>                  | <span data-ttu-id="136c7-140">1.000</span><span class="sxs-lookup"><span data-stu-id="136c7-140">1,000</span></span>  |
| <span data-ttu-id="136c7-141">Afskrivningsgrundlag</span><span class="sxs-lookup"><span data-stu-id="136c7-141">Depreciation base</span></span>              | <span data-ttu-id="136c7-142">10.000</span><span class="sxs-lookup"><span data-stu-id="136c7-142">10,000</span></span> |
| <span data-ttu-id="136c7-143">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="136c7-143">Service life years</span></span>             | <span data-ttu-id="136c7-144">5</span><span class="sxs-lookup"><span data-stu-id="136c7-144">5</span></span>      |
| <span data-ttu-id="136c7-145">Årlig afskrivningsprocent</span><span class="sxs-lookup"><span data-stu-id="136c7-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="136c7-146">25 %</span><span class="sxs-lookup"><span data-stu-id="136c7-146">25%</span></span>    |

<span data-ttu-id="136c7-147">Metoden med 125 % saldoafskrivning dividerer de 125 % med levetiden i år.</span><span class="sxs-lookup"><span data-stu-id="136c7-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="136c7-148">Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.</span><span class="sxs-lookup"><span data-stu-id="136c7-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="136c7-149">Periode</span><span class="sxs-lookup"><span data-stu-id="136c7-149">Period</span></span> | <span data-ttu-id="136c7-150">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="136c7-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="136c7-151">Bogført værdi</span><span class="sxs-lookup"><span data-stu-id="136c7-151">Book value</span></span>                    | <span data-ttu-id="136c7-152">Den bogførte nettoværdi ved årets afslutning</span><span class="sxs-lookup"><span data-stu-id="136c7-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="136c7-153">År 1</span><span class="sxs-lookup"><span data-stu-id="136c7-153">Year 1</span></span> | <span data-ttu-id="136c7-154">(11.000-1.000) x 25 % = 2.500</span><span class="sxs-lookup"><span data-stu-id="136c7-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="136c7-155">(11.000-2.500) = 8.500</span><span class="sxs-lookup"><span data-stu-id="136c7-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="136c7-156">(11.000-1.000-2.500) = 7.500</span><span class="sxs-lookup"><span data-stu-id="136c7-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="136c7-157">År 2</span><span class="sxs-lookup"><span data-stu-id="136c7-157">Year 2</span></span> | <span data-ttu-id="136c7-158">7.500 × 25 % = 1.875</span><span class="sxs-lookup"><span data-stu-id="136c7-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="136c7-159">(8.500-1.875) = 6.625</span><span class="sxs-lookup"><span data-stu-id="136c7-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="136c7-160">(7.500-1.875) = 5.625</span><span class="sxs-lookup"><span data-stu-id="136c7-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="136c7-161">År 3</span><span class="sxs-lookup"><span data-stu-id="136c7-161">Year 3</span></span> | <span data-ttu-id="136c7-162">5.625 × 25 % = 1.406,25</span><span class="sxs-lookup"><span data-stu-id="136c7-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="136c7-163">(6.625-1.406,25) = 5.218,75</span><span class="sxs-lookup"><span data-stu-id="136c7-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="136c7-164">(5.625-1.406,25) = 4.218,75</span><span class="sxs-lookup"><span data-stu-id="136c7-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="136c7-165">Når det beløb, der er beregnet ved hjælp af metoden til 125 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.</span><span class="sxs-lookup"><span data-stu-id="136c7-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




