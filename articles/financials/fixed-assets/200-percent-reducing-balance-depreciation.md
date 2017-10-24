---
title: 200 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 200 % saldoafskrivning.
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
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 46afd002a370a43c9e1d2fb7cc5e61ece9033be9
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="9c59b-103">200 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="9c59b-103">200 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9c59b-104">Denne artikel indeholder en oversigt over afskrivningsmetoden 200 % saldoafskrivning.</span><span class="sxs-lookup"><span data-stu-id="9c59b-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="9c59b-105">Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger **200% saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="9c59b-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="9c59b-106">Denne procentdel beregnes på basis af aktivets levetid.</span><span class="sxs-lookup"><span data-stu-id="9c59b-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="9c59b-107">Hvis et aktiv f.eks. har en levetid på fem år, beregnes procentdelen som 40 % (200 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="9c59b-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="9c59b-108">Denne metode kaldes også for dobbelt saldoafskrivning.</span><span class="sxs-lookup"><span data-stu-id="9c59b-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="9c59b-109">Hvis du vil oprette en 200 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="9c59b-110">Hvilke indstillinger der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi du vælger i feltet **Afskrivningsår**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="9c59b-111">Vælge et afskrivningsår</span><span class="sxs-lookup"><span data-stu-id="9c59b-111">Select a depreciation year</span></span>
<span data-ttu-id="9c59b-112">Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="9c59b-113">Standardværdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="9c59b-114">Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="9c59b-115">Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="9c59b-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="9c59b-116">Kalender</span><span class="sxs-lookup"><span data-stu-id="9c59b-116">Calendar</span></span>

<span data-ttu-id="9c59b-117">Du kan vælge at beholde standardværdien i feltet **Afskrivningsår**, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="9c59b-118">Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="9c59b-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="9c59b-119">Afskrivningen er typisk bogført nettoværdi minus scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="9c59b-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="9c59b-120">I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="9c59b-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="9c59b-121">Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="9c59b-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="9c59b-122">**Årligt** bogfører et beløb d. 31. december.</span><span class="sxs-lookup"><span data-stu-id="9c59b-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="9c59b-123">**Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="9c59b-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="9c59b-124">**Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="9c59b-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="9c59b-125">**Halvårlig** bogfører et halvårligt beløb sidst i kalenderhalvåret (d. 30. juni og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="9c59b-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="9c59b-126">**Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.</span><span class="sxs-lookup"><span data-stu-id="9c59b-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="9c59b-127">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="9c59b-127">Fiscal</span></span>

<span data-ttu-id="9c59b-128">Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 200 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="9c59b-129">Regnskabskalendere oprettes på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="9c59b-130">I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli.</span><span class="sxs-lookup"><span data-stu-id="9c59b-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="9c59b-131">Regnskabsåret kan være længere eller kortere end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="9c59b-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="9c59b-132">Afskrivningen reguleres for hver periode.</span><span class="sxs-lookup"><span data-stu-id="9c59b-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="9c59b-133">Længden på det næste regnskabsår bestemmes af konfigurationen af perioderne på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="9c59b-134">Npr du har valgt **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="9c59b-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="9c59b-135">**Årligt** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="9c59b-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="9c59b-136">**Regnskabsperiode** bogfører det samlede afskrivningsbeløb, der er beregnet for regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="9c59b-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="9c59b-137">Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="9c59b-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="9c59b-138">Eksempel på en 200 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="9c59b-138">Example of 200% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="9c59b-139">Anskaffelsesomkostning</span><span class="sxs-lookup"><span data-stu-id="9c59b-139">Acquisition cost</span></span>               | <span data-ttu-id="9c59b-140">11.000</span><span class="sxs-lookup"><span data-stu-id="9c59b-140">11,000</span></span> |
| <span data-ttu-id="9c59b-141">Restværdi</span><span class="sxs-lookup"><span data-stu-id="9c59b-141">Salvage value</span></span>                  | <span data-ttu-id="9c59b-142">1.000</span><span class="sxs-lookup"><span data-stu-id="9c59b-142">1, 000</span></span> |
| <span data-ttu-id="9c59b-143">Afskrivningsgrundlag</span><span class="sxs-lookup"><span data-stu-id="9c59b-143">Depreciation base</span></span>              | <span data-ttu-id="9c59b-144">10.000</span><span class="sxs-lookup"><span data-stu-id="9c59b-144">10,000</span></span> |
| <span data-ttu-id="9c59b-145">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="9c59b-145">Service life years</span></span>             | <span data-ttu-id="9c59b-146">5</span><span class="sxs-lookup"><span data-stu-id="9c59b-146">5</span></span>      |
| <span data-ttu-id="9c59b-147">Årlig afskrivningsprocent</span><span class="sxs-lookup"><span data-stu-id="9c59b-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="9c59b-148">40 %</span><span class="sxs-lookup"><span data-stu-id="9c59b-148">40%</span></span>    |

<span data-ttu-id="9c59b-149">Metoden med 200 % saldoafskrivning dividerer de 200 % med levetiden i år.</span><span class="sxs-lookup"><span data-stu-id="9c59b-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="9c59b-150">Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.</span><span class="sxs-lookup"><span data-stu-id="9c59b-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="9c59b-151">Periode</span><span class="sxs-lookup"><span data-stu-id="9c59b-151">Period</span></span> | <span data-ttu-id="9c59b-152">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="9c59b-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="9c59b-153">Bogført værdi</span><span class="sxs-lookup"><span data-stu-id="9c59b-153">Book value</span></span>             | <span data-ttu-id="9c59b-154">Den bogførte nettoværdi ved årets afslutning</span><span class="sxs-lookup"><span data-stu-id="9c59b-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="9c59b-155">År 1</span><span class="sxs-lookup"><span data-stu-id="9c59b-155">Year 1</span></span> | <span data-ttu-id="9c59b-156">(11.000 – 1.000) × 40 % = 4.000</span><span class="sxs-lookup"><span data-stu-id="9c59b-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="9c59b-157">11.000-4.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="9c59b-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="9c59b-158">11.000 - 1.000 - 4.000 = 6.000</span><span class="sxs-lookup"><span data-stu-id="9c59b-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="9c59b-159">År 2</span><span class="sxs-lookup"><span data-stu-id="9c59b-159">Year 2</span></span> | <span data-ttu-id="9c59b-160">6.000 × 40 % = 2.400</span><span class="sxs-lookup"><span data-stu-id="9c59b-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="9c59b-161">7.000 - 2.400 = 4.600</span><span class="sxs-lookup"><span data-stu-id="9c59b-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="9c59b-162">6.000 - 2.400 = 3.600</span><span class="sxs-lookup"><span data-stu-id="9c59b-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="9c59b-163">År 3</span><span class="sxs-lookup"><span data-stu-id="9c59b-163">Year 3</span></span> | <span data-ttu-id="9c59b-164">3.600 × 40 % = 1.440</span><span class="sxs-lookup"><span data-stu-id="9c59b-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="9c59b-165">4.600 - 1.440 = 3.160</span><span class="sxs-lookup"><span data-stu-id="9c59b-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="9c59b-166">3.600 - 1.440 = 2.160</span><span class="sxs-lookup"><span data-stu-id="9c59b-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="9c59b-167">Når det beløb, der er beregnet ved hjælp af metoden til 200 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.</span><span class="sxs-lookup"><span data-stu-id="9c59b-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




