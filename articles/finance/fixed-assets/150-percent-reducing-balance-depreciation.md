---
title: 150 % saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden 150 % saldoafskrivning.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4edc868b76d466c41be8036b962730db90eeb68a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249431"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="807ab-103">150 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="807ab-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="807ab-104">Denne artikel indeholder en oversigt over afskrivningsmetoden 150 % saldoafskrivning.</span><span class="sxs-lookup"><span data-stu-id="807ab-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="807ab-105">Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger **150% saldoværdi** i feltet **Metode** på siden **Afskrivningsprofiler**, bliver de anlægsaktiver, der er tildelt afskrivningsprofilen, afskrevet med den samme procent i hver afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="807ab-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="807ab-106">Denne procentdel beregnes på basis af aktivets levetid.</span><span class="sxs-lookup"><span data-stu-id="807ab-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="807ab-107">Hvis et aktiv f.eks. har en levetid på fem år, beregnes procentdelen som 30 % (150 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="807ab-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="807ab-108">Hvis du vil oprette en 150 % saldoafskrivning, skal du også foretage valg i feltet **Afskrivningsår** og feltet **Periodefrekvens** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="807ab-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="807ab-109">Hvilke indstillinger , der er tilgængelige i feltet **Periodefrekvens**, varierer, afhængigt af den værdi der er valgt i feltet **Afskrivningsår**.</span><span class="sxs-lookup"><span data-stu-id="807ab-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="807ab-110">Valg af afskrivningsår</span><span class="sxs-lookup"><span data-stu-id="807ab-110">Selection of depreciation year</span></span>
<span data-ttu-id="807ab-111">Du kan vælge enten **Kalender** eller **Regnskabsår** i feltet **Afskrivningsår** på siden **Afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="807ab-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="807ab-112">Standardværdien er **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="807ab-112">The default value is **Calendar**.</span></span> <span data-ttu-id="807ab-113">Dit valg bestemmer, hvad der kan vælges i feltet **Periodefrekvens**.</span><span class="sxs-lookup"><span data-stu-id="807ab-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="807ab-114">Dette felt definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="807ab-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="807ab-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="807ab-115">Calendar</span></span>

<span data-ttu-id="807ab-116">Du kan vælge at beholde standardværdien i feltet **Afskrivningsår**, **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="807ab-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="807ab-117">Indstillingen **Kalender** opdaterer afskrivningsgrundlaget d. 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="807ab-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="807ab-118">Afskrivningsgrundlaget er typisk bogført nettoværdi minus scrapværdi.</span><span class="sxs-lookup"><span data-stu-id="807ab-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="807ab-119">I eksemplerne senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i beregningskolonnen.</span><span class="sxs-lookup"><span data-stu-id="807ab-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="807ab-120">Hvis du vælger **Kalender** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="807ab-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="807ab-121">**Årligt** bogfører et beløb d. 31. december.</span><span class="sxs-lookup"><span data-stu-id="807ab-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="807ab-122">**Månedligt** bogfører et månedligt beløb sidst i hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="807ab-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="807ab-123">**Kvartalsvis** bogfører et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="807ab-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="807ab-124">**Halvårlig** bogfører et halvårligt beløb sidst i kalenderhalvåret (d. 30. juni og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="807ab-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="807ab-125">**Daglig** bogfører afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.</span><span class="sxs-lookup"><span data-stu-id="807ab-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="807ab-126">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="807ab-126">Fiscal</span></span>

<span data-ttu-id="807ab-127">Hvis du vælger **Regnskabsår** i feltet **Afskrivningsår**, beregnes 150 % saldoafskrivning på grundlag af regnskabsåret for den regnskabskalender, der er angivet for modellen eller den regnskabskalender, der er valgt på siden **Finans**.</span><span class="sxs-lookup"><span data-stu-id="807ab-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="807ab-128">Regnskabskalendere oprettes på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="807ab-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="807ab-129">I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli.</span><span class="sxs-lookup"><span data-stu-id="807ab-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="807ab-130">Regnskabsåret kan være længere eller kortere end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="807ab-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="807ab-131">Afskrivningen reguleres for hver periode.</span><span class="sxs-lookup"><span data-stu-id="807ab-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="807ab-132">Længden på det næste regnskabsår bestemmes af konfigurationen af perioderne på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="807ab-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="807ab-133">Hvis du vælger **Regnskabsår** som afskrivningsår, er følgende indstillinger tilgængelige i feltet **Periodefrekvens**:</span><span class="sxs-lookup"><span data-stu-id="807ab-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="807ab-134">**Årlig** bogfører det samlede afskrivningsbeløb, der beregnes for regnskabsåret på den sidste dag i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="807ab-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="807ab-135">**Regnskabsperiode** bogfører det samlede afskrivningsbeløb, der er beregnet for regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="807ab-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="807ab-136">Dette beløb periodiseres for de regnskabsperioder, der er defineret på siden **Regnskabskalendere**.</span><span class="sxs-lookup"><span data-stu-id="807ab-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="807ab-137">Eksempel på en 150 % saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="807ab-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="807ab-138">Anskaffelsesomkostning</span><span class="sxs-lookup"><span data-stu-id="807ab-138">Acquisition cost</span></span>               | <span data-ttu-id="807ab-139">11.000</span><span class="sxs-lookup"><span data-stu-id="807ab-139">11,000</span></span> |
| <span data-ttu-id="807ab-140">Restværdi</span><span class="sxs-lookup"><span data-stu-id="807ab-140">Salvage value</span></span>                  | <span data-ttu-id="807ab-141">1.000</span><span class="sxs-lookup"><span data-stu-id="807ab-141">1,000</span></span>  |
| <span data-ttu-id="807ab-142">Afskrivningsgrundlag</span><span class="sxs-lookup"><span data-stu-id="807ab-142">Depreciation base</span></span>              | <span data-ttu-id="807ab-143">10.000</span><span class="sxs-lookup"><span data-stu-id="807ab-143">10,000</span></span> |
| <span data-ttu-id="807ab-144">Levetid i år</span><span class="sxs-lookup"><span data-stu-id="807ab-144">Service life years</span></span>             | <span data-ttu-id="807ab-145">5</span><span class="sxs-lookup"><span data-stu-id="807ab-145">5</span></span>      |
| <span data-ttu-id="807ab-146">Årlig afskrivningsprocent</span><span class="sxs-lookup"><span data-stu-id="807ab-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="807ab-147">30 %</span><span class="sxs-lookup"><span data-stu-id="807ab-147">30%</span></span>    |

<span data-ttu-id="807ab-148">Metoden med 150 % saldoafskrivning dividerer de 150 % med levetiden i år.</span><span class="sxs-lookup"><span data-stu-id="807ab-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="807ab-149">Denne procent ganges med aktivets bogførte nettoværdi for at beregne årets afskrivningsbeløb.</span><span class="sxs-lookup"><span data-stu-id="807ab-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="807ab-150">Periode</span><span class="sxs-lookup"><span data-stu-id="807ab-150">Period</span></span> | <span data-ttu-id="807ab-151">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="807ab-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="807ab-152">Bogført værdi</span><span class="sxs-lookup"><span data-stu-id="807ab-152">Book value</span></span>             | <span data-ttu-id="807ab-153">Den bogførte nettoværdi ved årets afslutning</span><span class="sxs-lookup"><span data-stu-id="807ab-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="807ab-154">År 1</span><span class="sxs-lookup"><span data-stu-id="807ab-154">Year 1</span></span> | <span data-ttu-id="807ab-155">(11.000 – 1.000) × 30 % = 3.000</span><span class="sxs-lookup"><span data-stu-id="807ab-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="807ab-156">11.000 – 3.000 = 8.000</span><span class="sxs-lookup"><span data-stu-id="807ab-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="807ab-157">11.000 – 1.000 – 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="807ab-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="807ab-158">År 2</span><span class="sxs-lookup"><span data-stu-id="807ab-158">Year 2</span></span> | <span data-ttu-id="807ab-159">7.000 × 30 % = 2.100</span><span class="sxs-lookup"><span data-stu-id="807ab-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="807ab-160">8.000 – 2.100 = 5.900</span><span class="sxs-lookup"><span data-stu-id="807ab-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="807ab-161">7.000 – 2.100 = 4.900</span><span class="sxs-lookup"><span data-stu-id="807ab-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="807ab-162">År 3</span><span class="sxs-lookup"><span data-stu-id="807ab-162">Year 3</span></span> | <span data-ttu-id="807ab-163">4.900 × 30 % = 1.470</span><span class="sxs-lookup"><span data-stu-id="807ab-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="807ab-164">5.900 – 1.470 = 4.430</span><span class="sxs-lookup"><span data-stu-id="807ab-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="807ab-165">4.900 – 1.470 = 3.430</span><span class="sxs-lookup"><span data-stu-id="807ab-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="807ab-166">Når det beløb, der er beregnet ved hjælp af metoden til 150 % saldoafskrivning bliver mindre end det beløb, der skal beregnes ved hjælp af den lineære metode, er der en konvertering til lineær afskrivningsmetode for resten af levetiden.</span><span class="sxs-lookup"><span data-stu-id="807ab-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]