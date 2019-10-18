---
title: Reducer saldoafskrivning
description: Denne artikel indeholder en oversigt over afskrivningsmetoden Saldoafskrivning.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd4a8726ca194de2e5d95128659f3b212eaace5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176954"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="4c0a7-103">Reducer saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="4c0a7-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c0a7-104">Denne artikel indeholder en oversigt over afskrivningsmetoden Saldoafskrivning.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="4c0a7-105">Når du opretter en afskrivningsprofil til et anlægsaktiv og vælger Saldoafskrivning i feltet Metode på siden Afskrivningsprofiler, afskrives der med den samme procent i hver afskrivningsperiode på de aktiver, der har denne afskrivningsprofil tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="4c0a7-106">Hvis du vil oprette afskrivning efter saldoværdimetoden, skal du også angive indstillinger i felterne under fanen Generelt på siden Afskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="4c0a7-107">Først skal du vælge et år i feltet Afskrivningsår.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="4c0a7-108">Ud fra valget vises der forskellige indstillinger i feltet Periodefrekvens, som forklaret i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="4c0a7-109">Du skal også angive en værdi i feltet Procent for afskrivningsprofilen.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="4c0a7-110">Hvis du vælger indstillingen Fuld afskrivning, tages den resterende afskrivning i den sidste afskrivningsperiode, og den kan udgøre et stort beløb.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="4c0a7-111">I nogle lande/områder bruges der ikke en omlægning til lineær afskrivning.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="4c0a7-112">Der kan forekommer omlægninger, når beløbet for den alternative afskrivningsmetode er større end eller lig med beløbet for den primære afskrivningsprofil, og der brugte afskrivningsbeløb er beløbet for den alternative metode.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="4c0a7-113">Fordi et aktiv aldrig bliver fuldt afskrevet på basis af en procentberegning, skal du vælge indstillingen Fuld afskrivning for at afskrive et anlægsaktiv i fuldt omfang.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="4c0a7-114">Vælge et afskrivningsår</span><span class="sxs-lookup"><span data-stu-id="4c0a7-114">Select a depreciation year</span></span>
<span data-ttu-id="4c0a7-115">Du kan vælge enten Kalender eller Regnskabsår i feltet Afskrivningsår på siden Afskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="4c0a7-116">Dit valg bestemmer, hvad der kan vælges i feltet Periodefrekvens.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="4c0a7-117">Standardindstillingen er Kalender.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="4c0a7-118">Kalender</span><span class="sxs-lookup"><span data-stu-id="4c0a7-118">Calendar</span></span>

<span data-ttu-id="4c0a7-119">Indstillingen Kalender opdaterer afskrivningsgrundlaget (typisk bogført nettoværdi minus scrapværdi) d. 1. januar hvert år.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="4c0a7-120">I saldoværdieksemplet senere i dette emne er afskrivningsgrundlaget tælleren i det første udtryk i beregningen i kolonnen Beregning.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="4c0a7-121">Hvis du vælger Kalender, kan du vælge mellem følgende indstillinger i feltet Periodefrekvens, der definerer datoer og beløb for periodiseringen af afskrivningsposteringerne i hele kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="4c0a7-122">Ved Årligt bogføres d. 31. december.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="4c0a7-123">Ved Månedligt bogføres et månedligt beløb sidst i hver kalendermåned.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="4c0a7-124">Ved Kvartalsvis bogføres et kvartalsmæssigt beløb sidst i hvert kalenderkvartal (d. 31. marts, d. 30. juni, d. 30. september og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="4c0a7-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="4c0a7-125">Ved Halvårlig bogføres et halvårligt beløb sidst i hvert kalenderhalvår (d. 30. juni og d. 31. december).</span><span class="sxs-lookup"><span data-stu-id="4c0a7-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="4c0a7-126">Ved Dagligt bogføres afskrivningsbeløbet for afskrivningsmetoden dagligt ved hjælp af en postering for hver dag.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="4c0a7-127">Hvis du f.eks. vælger Årligt, bogføres den årlige afskrivning kun én gang, nemlig d. 31. december hvert år.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="4c0a7-128">Hvis du vælger Månedligt, bogføres den månedlige afskrivning hver måned med 1/12 af det årlige afskrivningsbeløb.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="4c0a7-129">Regnskabsår</span><span class="sxs-lookup"><span data-stu-id="4c0a7-129">Fiscal</span></span>

<span data-ttu-id="4c0a7-130">Hvis du vælger Regnskab i feltet Afskrivningsår, bruges den lineære afskrivningsmetode.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="4c0a7-131">Den beregnes baseret på det regnskabsår, der er angivet på siden Regnskabskalendere for den regnskabskalender, der er valgt på siden Finans.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="4c0a7-132">I forbindelse med regnskabsåret fra d. 1. juli til og med d. 30. juni starter afskrivningsberegningen f.eks. d. 1. juli.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="4c0a7-133">Regnskabsåret kan være længere eller kortere end 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="4c0a7-134">Afskrivningen reguleres for hver regnskabsperiode.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="4c0a7-135">Længden på regnskabsåret er baseret på de regnskabsperioder, du angiver, når du opretter et nyt regnskabsår på siden Regnskabskalendere.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="4c0a7-136">Hvis du vælger Regnskab, kan du vælge mellem følgende indstillinger i feltet Periodefrekvens:</span><span class="sxs-lookup"><span data-stu-id="4c0a7-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="4c0a7-137">Ved Årligt bogføres det samlede afskrivningsbeløb, der beregnes for regnskabsåret som ét beløb på den sidste dag i regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="4c0a7-138">Ved Regnskabsperiode bogføres det samlede afskrivningsbeløb, der beregnes for regnskabsåret, der periodiseres for de regnskabsperioder, der er defineret for den regnskabskalender, der er valgt på siden Finans, eller for den regnskabskalender, der er valgt for bogen for et anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="4c0a7-139">Eksempel på saldoafskrivning</span><span class="sxs-lookup"><span data-stu-id="4c0a7-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="4c0a7-140">Det antages, at anskaffelsesprisen for anlægsaktivet er 11.000, at scrapværdien er 1.000, og at afskrivningsprocentsatsen er 30.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="4c0a7-141">Når metoden Saldoværdi benyttes, beregnes der 30 % af afskrivningsgrundlaget (bogført nettoværdi minus scrapværdi) ved slutningen af den forrige afskrivningsperiode.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="4c0a7-142">Afskrivning i de første tre år er vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="4c0a7-143">Periode</span><span class="sxs-lookup"><span data-stu-id="4c0a7-143">Period</span></span> | <span data-ttu-id="4c0a7-144">Beregning af det årlige afskrivningsbeløb</span><span class="sxs-lookup"><span data-stu-id="4c0a7-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="4c0a7-145">Den bogførte nettoværdi ved årets afslutning</span><span class="sxs-lookup"><span data-stu-id="4c0a7-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="4c0a7-146">År 1</span><span class="sxs-lookup"><span data-stu-id="4c0a7-146">Year 1</span></span> | <span data-ttu-id="4c0a7-147">(11.000 - 1.000) \* 30 % = 3.000</span><span class="sxs-lookup"><span data-stu-id="4c0a7-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="4c0a7-148">(11.000 - 1.000) - 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="4c0a7-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="4c0a7-149">År 2</span><span class="sxs-lookup"><span data-stu-id="4c0a7-149">Year 2</span></span> | <span data-ttu-id="4c0a7-150">(7.000 - 1.000) \* 30 % = 1.800</span><span class="sxs-lookup"><span data-stu-id="4c0a7-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="4c0a7-151">(7.000 - 1.800) = 5.200</span><span class="sxs-lookup"><span data-stu-id="4c0a7-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="4c0a7-152">År 3</span><span class="sxs-lookup"><span data-stu-id="4c0a7-152">Year 3</span></span> | <span data-ttu-id="4c0a7-153">(5.200 - 1.000) \* 30 % = 1.260</span><span class="sxs-lookup"><span data-stu-id="4c0a7-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="4c0a7-154">(5.200 - 1.260) = 3.940</span><span class="sxs-lookup"><span data-stu-id="4c0a7-154">(5,200 - 1,260) = 3,940</span></span>               |


-





