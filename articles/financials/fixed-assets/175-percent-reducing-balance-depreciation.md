---
title: 175 procent saldoafskrivning
description: Dette emne indeholder en oversigt over afskrivningsmetoden 175 % saldoafskrivning.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8f78eb06930eab26d300fba6fd28333a5ce39cf8
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="11c56-103">175 procent saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="11c56-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11c56-104">Dette emne indeholder en oversigt over afskrivningsmetoden 175 % saldoafskrivning.</span><span class="sxs-lookup"><span data-stu-id="11c56-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="11c56-105">Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger **175 % saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="11c56-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="11c56-106">Hvis du vil oprette en 175 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="11c56-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="11c56-107">Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.</span><span class="sxs-lookup"><span data-stu-id="11c56-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="11c56-108">Vælge et afskrivningsår</span><span class="sxs-lookup"><span data-stu-id="11c56-108">Select a depreciation year</span></span>
<span data-ttu-id="11c56-109">Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="11c56-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="11c56-110">Standardværdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="11c56-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="11c56-111">Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="11c56-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="11c56-112">Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="11c56-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="11c56-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="11c56-113">Calendar</span></span>

<span data-ttu-id="11c56-114">Du kan vælge at beholde standardværdien i feltet **Afskrivningsår**, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="11c56-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="11c56-115">Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="11c56-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="11c56-116">Afskrivningsgrundlaget er typisk bogført nettoværdi minus scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="11c56-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="11c56-117">I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="11c56-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="11c56-118">Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="11c56-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="11c56-119">**Årligt** bogfører et beløb d. 31. december.</span><span class="sxs-lookup"><span data-stu-id="11c56-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="11c56-120">**Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="11c56-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="11c56-121">**Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="11c56-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="11c56-122">**Halvårlig** bogfører et halvårligt beløb sidst i kalenderhalvåret (d. 30. juni og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="11c56-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="11c56-123">**Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.</span><span class="sxs-lookup"><span data-stu-id="11c56-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="11c56-124">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="11c56-124">Fiscal</span></span>

<span data-ttu-id="11c56-125">Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 175 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**.</span><span class="sxs-lookup"><span data-stu-id="11c56-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="11c56-126">Regnskabskalendere oprettes på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="11c56-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="11c56-127">Yderligere oplysninger finder du under [Regnskabskalendere, regnskabsår og perioder](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="11c56-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="11c56-128">I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli.</span><span class="sxs-lookup"><span data-stu-id="11c56-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="11c56-129">Regnskabsåret kan være længere eller kortere end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="11c56-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="11c56-130">Afskrivningen justeres automatisk for hver periode, og længden på det næste regnskabsår bestemmes af opsætningen af perioder på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="11c56-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="11c56-131">Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="11c56-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="11c56-132">**Årlig** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret på den sidste dag i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="11c56-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="11c56-133">**Regnskabsperiode** beregner det samlede afskrivningsbeløb for regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="11c56-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="11c56-134">Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="11c56-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="11c56-135">Eksempel på en 175 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="11c56-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="11c56-136">Anskaffelsesomkostning</span><span class="sxs-lookup"><span data-stu-id="11c56-136">Acquisition cost</span></span>               | <span data-ttu-id="11c56-137">11.000</span><span class="sxs-lookup"><span data-stu-id="11c56-137">11,000</span></span> |
| <span data-ttu-id="11c56-138">Restværdi</span><span class="sxs-lookup"><span data-stu-id="11c56-138">Salvage value</span></span>                  | <span data-ttu-id="11c56-139">1.000</span><span class="sxs-lookup"><span data-stu-id="11c56-139">1,000</span></span>  |
| <span data-ttu-id="11c56-140">Afskrivningsgrundlag</span><span class="sxs-lookup"><span data-stu-id="11c56-140">Depreciation base</span></span>              | <span data-ttu-id="11c56-141">10.000</span><span class="sxs-lookup"><span data-stu-id="11c56-141">10,000</span></span> |
| <span data-ttu-id="11c56-142">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="11c56-142">Service life years</span></span>             | <span data-ttu-id="11c56-143">5</span><span class="sxs-lookup"><span data-stu-id="11c56-143">5</span></span>      |
| <span data-ttu-id="11c56-144">Årlig afskrivningsprocent</span><span class="sxs-lookup"><span data-stu-id="11c56-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="11c56-145">35 %</span><span class="sxs-lookup"><span data-stu-id="11c56-145">35%</span></span>    |

<span data-ttu-id="11c56-146">Metoden med 175 % saldoafskrivning dividerer de 175 % med levetiden i år.</span><span class="sxs-lookup"><span data-stu-id="11c56-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="11c56-147">Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.</span><span class="sxs-lookup"><span data-stu-id="11c56-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="11c56-148">Periode</span><span class="sxs-lookup"><span data-stu-id="11c56-148">Period</span></span> | <span data-ttu-id="11c56-149">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="11c56-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="11c56-150">Bogført værdi</span><span class="sxs-lookup"><span data-stu-id="11c56-150">Book value</span></span>                  | <span data-ttu-id="11c56-151">Den bogførte nettoværdi ved årets afslutning</span><span class="sxs-lookup"><span data-stu-id="11c56-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="11c56-152">År 1</span><span class="sxs-lookup"><span data-stu-id="11c56-152">Year 1</span></span> | <span data-ttu-id="11c56-153">(11.000 – 1.000) × 35 % = 3.500</span><span class="sxs-lookup"><span data-stu-id="11c56-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="11c56-154">11.000 – 3.500 = 7.500</span><span class="sxs-lookup"><span data-stu-id="11c56-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="11c56-155">11.000 – 1.000 – 3.500 = 6.500</span><span class="sxs-lookup"><span data-stu-id="11c56-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="11c56-156">År 2</span><span class="sxs-lookup"><span data-stu-id="11c56-156">Year 2</span></span> | <span data-ttu-id="11c56-157">6.500 × 35 % = 2.275</span><span class="sxs-lookup"><span data-stu-id="11c56-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="11c56-158">7.500 – 2.275 = 5.225</span><span class="sxs-lookup"><span data-stu-id="11c56-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="11c56-159">6.500 – 2.275 = 4.225</span><span class="sxs-lookup"><span data-stu-id="11c56-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="11c56-160">År 3</span><span class="sxs-lookup"><span data-stu-id="11c56-160">Year 3</span></span> | <span data-ttu-id="11c56-161">4.225 × 35 % = 1.478,75</span><span class="sxs-lookup"><span data-stu-id="11c56-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="11c56-162">5.225 – 1.478,75 = 3.746,25</span><span class="sxs-lookup"><span data-stu-id="11c56-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="11c56-163">4.225 – 1.478,75 = 2.746,25</span><span class="sxs-lookup"><span data-stu-id="11c56-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="11c56-164">Når det beløb, der er beregnet ved hjælp af metoden til 175 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.</span><span class="sxs-lookup"><span data-stu-id="11c56-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




