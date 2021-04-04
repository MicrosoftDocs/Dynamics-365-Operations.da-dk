---
title: Power BI-indhold til købsforbrugsanalyse
description: I dette emne beskrives, hvad der skal medtages i Power BI-indhold til Købsforbrugsanalyse.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559543"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="b2f25-103">Power BI-indhold til købsforbrugsanalyse</span><span class="sxs-lookup"><span data-stu-id="b2f25-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2f25-104">I dette emne beskrives, hvad der skal medtages i **Købsforbrugsanalyse** Microsoft Power BI-indhold.</span><span class="sxs-lookup"><span data-stu-id="b2f25-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="b2f25-105">Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der bruges til at oprette indholdspakken.</span><span class="sxs-lookup"><span data-stu-id="b2f25-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b2f25-106">Overblik</span><span class="sxs-lookup"><span data-stu-id="b2f25-106">Overview</span></span>

<span data-ttu-id="b2f25-107">Power BI-indholdet til **Købsforbrugsanalyse** er udviklet til at hjælpe indkøbschefer og ledere, der er ansvarlige for budgetter, med at holde styr på udgifter til køb.</span><span class="sxs-lookup"><span data-stu-id="b2f25-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="b2f25-108">Chefer kan analysere indkøbsudgifter på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="b2f25-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="b2f25-109">Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)</span><span class="sxs-lookup"><span data-stu-id="b2f25-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="b2f25-110">Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)</span><span class="sxs-lookup"><span data-stu-id="b2f25-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="b2f25-111">Indholdet bruger købstransaktionsdata og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="b2f25-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="b2f25-112">Rapporter fremhæve ændringer i købsforbruget over tid.</span><span class="sxs-lookup"><span data-stu-id="b2f25-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="b2f25-113">Derfor kan rapporterne bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="b2f25-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="b2f25-114">Desuden viser diagrammer købsforbruget til forskellige indkøbskategorier og kreditorgrupper.</span><span class="sxs-lookup"><span data-stu-id="b2f25-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="b2f25-115">Derfor kan kategori- og områdeledere bruge diagrammerne til at identificere ændringer i forbrugsmønsteret.</span><span class="sxs-lookup"><span data-stu-id="b2f25-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b2f25-116">Adgang til Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="b2f25-116">Accessing the Power BI content</span></span>
<span data-ttu-id="b2f25-117">**Power BI-indholdet til Købsforbrugsanalyse** vises på siden **Købs- og forbrugsanalyse** (**Indkøb og forsyning** \> **Forespørgsler og rapporter** \> **Performanceanalyse for indkøb** \> **Købs- og forbrugsanalyse**).</span><span class="sxs-lookup"><span data-stu-id="b2f25-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b2f25-118">Metrikker, der er inkluderet i Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="b2f25-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="b2f25-119">**Power BI-indholdet til købsforbrugsanalyse** indeholder en rapport, der består af et sæt metrikker.</span><span class="sxs-lookup"><span data-stu-id="b2f25-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="b2f25-120">Disse metrikker visualiseres som diagrammer, felter og tabeller.</span><span class="sxs-lookup"><span data-stu-id="b2f25-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="b2f25-121">I nedenstående sektioner vises en oversigt over visualiseringerne.</span><span class="sxs-lookup"><span data-stu-id="b2f25-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="b2f25-122">Rapportsiden Indkøb efter leverandør</span><span class="sxs-lookup"><span data-stu-id="b2f25-122">Purchase by vendor report page</span></span>
<span data-ttu-id="b2f25-123">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="b2f25-123">**Charts**</span></span>
- <span data-ttu-id="b2f25-124">Top 10 leverandører efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="b2f25-125">Samlet indkøb pr. leverandørgruppe/land/område/navn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="b2f25-126">Indkøb pr. leverandørgruppe/land/område/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="b2f25-127">Gennemsnitsindkøb pr. leverandørgruppe/land/område/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="b2f25-128">**Felter**</span><span class="sxs-lookup"><span data-stu-id="b2f25-128">**Tiles**</span></span>
- <span data-ttu-id="b2f25-129">Indkøb i alt</span><span class="sxs-lookup"><span data-stu-id="b2f25-129">Total purchase</span></span>
- <span data-ttu-id="b2f25-130">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="b2f25-130">YOY purchase growth</span></span>
- <span data-ttu-id="b2f25-131">Antal leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="b2f25-131">Total # vendors</span></span>
- <span data-ttu-id="b2f25-132">Antal aktive leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="b2f25-132">Total # of active vendors</span></span>

<span data-ttu-id="b2f25-133">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="b2f25-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="b2f25-134">Rapportsiden Køb pr. produkt</span><span class="sxs-lookup"><span data-stu-id="b2f25-134">Purchase by product report page</span></span>

<span data-ttu-id="b2f25-135">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="b2f25-135">**Charts**</span></span>
- <span data-ttu-id="b2f25-136">Køb efter indkøbskategori/produktnavn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="b2f25-137">Indkøb i alt efter indkøbskategori/produktnavn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="b2f25-138">Top 10 produkter efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="b2f25-139">**Felter**</span><span class="sxs-lookup"><span data-stu-id="b2f25-139">**Tiles**</span></span>
- <span data-ttu-id="b2f25-140">Antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="b2f25-140">Total # of products</span></span></li>
- <span data-ttu-id="b2f25-141">Antal aktive produkter i alt i procentdel af antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="b2f25-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="b2f25-142">Antal produkter, der udgør for 80 % af indkøbet</span><span class="sxs-lookup"><span data-stu-id="b2f25-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="b2f25-143">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="b2f25-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="b2f25-144">Rapportsiden Indkøb efter periode</span><span class="sxs-lookup"><span data-stu-id="b2f25-144">Purchase by period report page</span></span>
<span data-ttu-id="b2f25-145">Denne side viser køb dette og sidste år, og vækst efter indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="b2f25-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="b2f25-146">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="b2f25-146">**Charts**</span></span> 
- <span data-ttu-id="b2f25-147">Indkøb pr. måned/dag (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="b2f25-148">Afvigelse i akkumuleret indkøb år for år (vandfaldsdiagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="b2f25-149">Vækst i indkøb i alt år for år (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="b2f25-150">Indkøbsopgørelse (matrix)</span><span class="sxs-lookup"><span data-stu-id="b2f25-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="b2f25-151">**Felter**</span><span class="sxs-lookup"><span data-stu-id="b2f25-151">**Tiles**</span></span>
- <span data-ttu-id="b2f25-152">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="b2f25-152">YOY purchase growth</span></span>
- <span data-ttu-id="b2f25-153">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="b2f25-153">YOY purchase growth %</span></span>

<span data-ttu-id="b2f25-154">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="b2f25-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="b2f25-155">Rapportsiden Indkøb efter leverandørlokalitet</span><span class="sxs-lookup"><span data-stu-id="b2f25-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="b2f25-156">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="b2f25-156">**Charts**</span></span>
- <span data-ttu-id="b2f25-157">Indkøb efter by</span><span class="sxs-lookup"><span data-stu-id="b2f25-157">Purchase by city</span></span>
- <span data-ttu-id="b2f25-158">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="b2f25-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="b2f25-159">Indkøb efter land/område</span><span class="sxs-lookup"><span data-stu-id="b2f25-159">Purchase by country</span></span>

<span data-ttu-id="b2f25-160">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="b2f25-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="b2f25-161">Rapportsiden Købsforbrugsanalyse efter tidspunkt</span><span class="sxs-lookup"><span data-stu-id="b2f25-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="b2f25-162">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="b2f25-162">**Charts**</span></span> 
- <span data-ttu-id="b2f25-163">Indkøb indeværende år efter måned/dag (kurvediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="b2f25-164">Køb indeværende og sidste år (linje- og søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="b2f25-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="b2f25-165">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="b2f25-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="b2f25-166">Rapportsiden Købsforbrugsanalyse efter leverandør</span><span class="sxs-lookup"><span data-stu-id="b2f25-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="b2f25-167">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="b2f25-167">**Charts**</span></span> 
- <span data-ttu-id="b2f25-168">Indkøb hos top 10 kreditorer i % af indkøb (tragtformet)</span><span class="sxs-lookup"><span data-stu-id="b2f25-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="b2f25-169">Top 10 leverandører med forøget forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="b2f25-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="b2f25-170">Top 10 leverandører med faldende forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="b2f25-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="b2f25-171">**Eksempel:** 
</span><span class="sxs-lookup"><span data-stu-id="b2f25-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="b2f25-172">Datamodel og enheder</span><span class="sxs-lookup"><span data-stu-id="b2f25-172">Data model and entities</span></span>
<span data-ttu-id="b2f25-173">Følgende data bruges til at udfylde rapportsiderne i **Power BI-indholdet til Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="b2f25-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="b2f25-174">Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="b2f25-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="b2f25-175">Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser.</span><span class="sxs-lookup"><span data-stu-id="b2f25-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="b2f25-176">Du kan finde flere oplysninger under [Power BI-integration med Enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="b2f25-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="b2f25-177">De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i købskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="b2f25-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="b2f25-178">For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare.</span><span class="sxs-lookup"><span data-stu-id="b2f25-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="b2f25-179">Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager under [Power BI-integration med enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="b2f25-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="b2f25-180">Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdet.</span><span class="sxs-lookup"><span data-stu-id="b2f25-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="b2f25-181">Enhed</span><span class="sxs-lookup"><span data-stu-id="b2f25-181">Entity</span></span>        | <span data-ttu-id="b2f25-182">Samlede nøglemålinger</span><span class="sxs-lookup"><span data-stu-id="b2f25-182">Key aggregate measurements</span></span> | <span data-ttu-id="b2f25-183">Datakilde</span><span class="sxs-lookup"><span data-stu-id="b2f25-183">Data source</span></span>                                 | <span data-ttu-id="b2f25-184">Felt</span><span class="sxs-lookup"><span data-stu-id="b2f25-184">Field</span></span>              | <span data-ttu-id="b2f25-185">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b2f25-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="b2f25-186">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="b2f25-186">Invoice lines</span></span> | <span data-ttu-id="b2f25-187">Køb</span><span class="sxs-lookup"><span data-stu-id="b2f25-187">Purchase</span></span>                   | <span data-ttu-id="b2f25-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="b2f25-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="b2f25-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="b2f25-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="b2f25-190">Beløbet i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="b2f25-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="b2f25-191">Følgende tabel viser de vigtigste målinger i indholdet, der beregnes fra enheden Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="b2f25-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="b2f25-192">Målepunkt</span><span class="sxs-lookup"><span data-stu-id="b2f25-192">Measure</span></span>               | <span data-ttu-id="b2f25-193">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="b2f25-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f25-194">Køb indeværende år</span><span class="sxs-lookup"><span data-stu-id="b2f25-194">Purchase current year</span></span> | <span data-ttu-id="b2f25-195">Køb indeværende år = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="b2f25-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="b2f25-196">Køb sidste år</span><span class="sxs-lookup"><span data-stu-id="b2f25-196">Purchase last year</span></span>    | <span data-ttu-id="b2f25-197">Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="b2f25-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="b2f25-198">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="b2f25-198">YOY purchase growth</span></span>   | <span data-ttu-id="b2f25-199">Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="b2f25-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="b2f25-200">Følgende nøgledimensioner i indholdet bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.</span><span class="sxs-lookup"><span data-stu-id="b2f25-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="b2f25-201">Enhed</span><span class="sxs-lookup"><span data-stu-id="b2f25-201">Entity</span></span>                 | <span data-ttu-id="b2f25-202">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="b2f25-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b2f25-203">Leverandører</span><span class="sxs-lookup"><span data-stu-id="b2f25-203">Vendors</span></span>                | <span data-ttu-id="b2f25-204">Kreditorgrupper, kreditorlande eller -områder, kreditornavn</span><span class="sxs-lookup"><span data-stu-id="b2f25-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="b2f25-205">Produkter</span><span class="sxs-lookup"><span data-stu-id="b2f25-205">Products</span></span>               | <span data-ttu-id="b2f25-206">Produktnummer, produktnavn, varegruppenavn</span><span class="sxs-lookup"><span data-stu-id="b2f25-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="b2f25-207">Indkøbskategorier</span><span class="sxs-lookup"><span data-stu-id="b2f25-207">Procurement categories</span></span> | <span data-ttu-id="b2f25-208">Indkøbskategori, indkøbskategorinavne</span><span class="sxs-lookup"><span data-stu-id="b2f25-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="b2f25-209">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="b2f25-209">Legal entities</span></span>         | <span data-ttu-id="b2f25-210">Navn på juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="b2f25-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="b2f25-211">Datoer</span><span class="sxs-lookup"><span data-stu-id="b2f25-211">Dates</span></span>                  | <span data-ttu-id="b2f25-212">Datoer, årsforskydning</span><span class="sxs-lookup"><span data-stu-id="b2f25-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="b2f25-213">Som standard viser indholdet data for det indeværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="b2f25-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="b2f25-214">Du kan dog ændre datofilteret i rapportens filterafsnit.</span><span class="sxs-lookup"><span data-stu-id="b2f25-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="b2f25-215">Du kan også ændre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="b2f25-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]