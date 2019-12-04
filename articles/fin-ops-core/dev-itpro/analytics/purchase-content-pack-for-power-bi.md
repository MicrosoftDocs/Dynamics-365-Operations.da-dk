---
title: Power BI-indhold til købsforbrugsanalyse
description: I dette emne beskrives, hvad der skal medtages i Power BI-indhold til Købsforbrugsanalyse. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der bliver brugt til at oprette indholdet.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2d31aaf14f6399baca8531707864c48cd2d56ac2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769965"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="8a7a0-104">Power BI-indhold til købsforbrugsanalyse</span><span class="sxs-lookup"><span data-stu-id="8a7a0-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a7a0-105">I dette emne beskrives, hvad der skal medtages i **Microsoft Power BI-indhold til Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="8a7a0-106">Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der bruges til at oprette indholdspakken.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="8a7a0-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="8a7a0-107">Overview</span></span>

<span data-ttu-id="8a7a0-108">Power BI-indholdet til **Købsforbrugsanalyse** er udviklet til at hjælpe indkøbschefer og ledere, der er ansvarlige for budgetter, med at holde styr på udgifter til køb.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="8a7a0-109">Chefer kan analysere indkøbsudgifter på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="8a7a0-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="8a7a0-110">Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="8a7a0-111">Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="8a7a0-112">Indholdet bruger købstransaktionsdata og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="8a7a0-113">Rapporter fremhæve ændringer i købsforbruget over tid.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="8a7a0-114">Derfor kan rapporterne bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="8a7a0-115">Desuden viser diagrammer købsforbruget til forskellige indkøbskategorier og kreditorgrupper.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="8a7a0-116">Derfor kan kategori- og områdeledere bruge diagrammerne til at identificere ændringer i forbrugsmønsteret.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="8a7a0-117">Adgang til Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="8a7a0-117">Accessing the Power BI content</span></span>
<span data-ttu-id="8a7a0-118">**Power BI-indholdet til Købsforbrugsanalyse** vises på siden **Købs- og forbrugsanalyse** (**Indkøb og forsyning** \> **Forespørgsler og rapporter** \> **Performanceanalyse for indkøb** \> **Købs- og forbrugsanalyse**).</span><span class="sxs-lookup"><span data-stu-id="8a7a0-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="8a7a0-119">Metrikker, der er inkluderet i Power BI-indholdet</span><span class="sxs-lookup"><span data-stu-id="8a7a0-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="8a7a0-120">**Power BI-indholdet til købsforbrugsanalyse** indeholder en rapport, der består af et sæt metrikker.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="8a7a0-121">Disse metrikker visualiseres som diagrammer, felter og tabeller.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="8a7a0-122">I nedenstående sektioner vises en oversigt over visualiseringerne.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="8a7a0-123">Rapportsiden Indkøb efter leverandør</span><span class="sxs-lookup"><span data-stu-id="8a7a0-123">Purchase by vendor report page</span></span>
<span data-ttu-id="8a7a0-124">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-124">**Charts**</span></span>
- <span data-ttu-id="8a7a0-125">Top 10 leverandører efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="8a7a0-126">Samlet indkøb pr. leverandørgruppe/land/navn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="8a7a0-127">Indkøb pr. leverandørgruppe/land/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="8a7a0-128">Gennemsnitsindkøb pr. leverandørgruppe/land/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="8a7a0-129">**Felter**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-129">**Tiles**</span></span>
- <span data-ttu-id="8a7a0-130">Indkøb i alt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-130">Total purchase</span></span>
- <span data-ttu-id="8a7a0-131">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-131">YOY purchase growth</span></span>
- <span data-ttu-id="8a7a0-132">Antal leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-132">Total # vendors</span></span>
- <span data-ttu-id="8a7a0-133">Antal aktive leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-133">Total # of active vendors</span></span>

<span data-ttu-id="8a7a0-134">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="8a7a0-135">Rapportsiden Køb pr. produkt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-135">Purchase by product report page</span></span>

<span data-ttu-id="8a7a0-136">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-136">**Charts**</span></span>
- <span data-ttu-id="8a7a0-137">Køb efter indkøbskategori/produktnavn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="8a7a0-138">Indkøb i alt efter indkøbskategori/produktnavn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="8a7a0-139">Top 10 produkter efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="8a7a0-140">**Felter**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-140">**Tiles**</span></span>
- <span data-ttu-id="8a7a0-141">Antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-141">Total # of products</span></span></li>
- <span data-ttu-id="8a7a0-142">Antal aktive produkter i alt i procentdel af antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="8a7a0-143">Antal produkter, der udgør for 80 % af indkøbet</span><span class="sxs-lookup"><span data-stu-id="8a7a0-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="8a7a0-144">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="8a7a0-145">Rapportsiden Indkøb efter periode</span><span class="sxs-lookup"><span data-stu-id="8a7a0-145">Purchase by period report page</span></span>
<span data-ttu-id="8a7a0-146">Denne side viser køb dette og sidste år, og vækst efter indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="8a7a0-147">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-147">**Charts**</span></span> 
- <span data-ttu-id="8a7a0-148">Indkøb pr. måned/dag (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="8a7a0-149">Afvigelse i akkumuleret indkøb år for år (vandfaldsdiagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="8a7a0-150">Vækst i indkøb i alt år for år (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="8a7a0-151">Indkøbsopgørelse (matrix)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="8a7a0-152">**Felter**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-152">**Tiles**</span></span>
- <span data-ttu-id="8a7a0-153">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-153">YOY purchase growth</span></span>
- <span data-ttu-id="8a7a0-154">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="8a7a0-154">YOY purchase growth %</span></span>

<span data-ttu-id="8a7a0-155">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="8a7a0-156">Rapportsiden Indkøb efter leverandørlokalitet</span><span class="sxs-lookup"><span data-stu-id="8a7a0-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="8a7a0-157">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-157">**Charts**</span></span>
- <span data-ttu-id="8a7a0-158">Indkøb efter by</span><span class="sxs-lookup"><span data-stu-id="8a7a0-158">Purchase by city</span></span>
- <span data-ttu-id="8a7a0-159">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="8a7a0-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="8a7a0-160">Indkøb efter land</span><span class="sxs-lookup"><span data-stu-id="8a7a0-160">Purchase by country</span></span>

<span data-ttu-id="8a7a0-161">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="8a7a0-162">Rapportsiden Købsforbrugsanalyse efter tidspunkt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="8a7a0-163">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-163">**Charts**</span></span> 
- <span data-ttu-id="8a7a0-164">Indkøb indeværende år efter måned/dag (kurvediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="8a7a0-165">Køb indeværende og sidste år (linje- og søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="8a7a0-166">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="8a7a0-167">Rapportsiden Købsforbrugsanalyse efter leverandør</span><span class="sxs-lookup"><span data-stu-id="8a7a0-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="8a7a0-168">**Diagrammer**</span><span class="sxs-lookup"><span data-stu-id="8a7a0-168">**Charts**</span></span> 
- <span data-ttu-id="8a7a0-169">Indkøb hos top 10 kreditorer i % af indkøb (tragtformet)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="8a7a0-170">Top 10 leverandører med forøget forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="8a7a0-171">Top 10 leverandører med faldende forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="8a7a0-172">**Eksempel:** 
</span><span class="sxs-lookup"><span data-stu-id="8a7a0-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="8a7a0-173">Datamodel og enheder</span><span class="sxs-lookup"><span data-stu-id="8a7a0-173">Data model and entities</span></span>
<span data-ttu-id="8a7a0-174">Følgende data bruges til at udfylde rapportsiderne i **Power BI-indholdet til Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="8a7a0-175">Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="8a7a0-176">Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="8a7a0-177">Du kan finde flere oplysninger under [Power BI-integration med Enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="8a7a0-177">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="8a7a0-178">De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i købskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="8a7a0-179">For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="8a7a0-180">Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager under [Power BI-integration med enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="8a7a0-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="8a7a0-181">Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdet.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="8a7a0-182">Enhed</span><span class="sxs-lookup"><span data-stu-id="8a7a0-182">Entity</span></span>        | <span data-ttu-id="8a7a0-183">Samlede nøglemålinger</span><span class="sxs-lookup"><span data-stu-id="8a7a0-183">Key aggregate measurements</span></span> | <span data-ttu-id="8a7a0-184">Datakilde</span><span class="sxs-lookup"><span data-stu-id="8a7a0-184">Data source</span></span>                                 | <span data-ttu-id="8a7a0-185">Felt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-185">Field</span></span>              | <span data-ttu-id="8a7a0-186">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8a7a0-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="8a7a0-187">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="8a7a0-187">Invoice lines</span></span> | <span data-ttu-id="8a7a0-188">Køb</span><span class="sxs-lookup"><span data-stu-id="8a7a0-188">Purchase</span></span>                   | <span data-ttu-id="8a7a0-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="8a7a0-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="8a7a0-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="8a7a0-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="8a7a0-191">Beløbet i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="8a7a0-192">Følgende tabel viser de vigtigste målinger i indholdet, der beregnes fra enheden Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="8a7a0-193">Målepunkt</span><span class="sxs-lookup"><span data-stu-id="8a7a0-193">Measure</span></span>               | <span data-ttu-id="8a7a0-194">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="8a7a0-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7a0-195">Køb indeværende år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-195">Purchase current year</span></span> | <span data-ttu-id="8a7a0-196">Køb indeværende år = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="8a7a0-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="8a7a0-197">Køb sidste år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-197">Purchase last year</span></span>    | <span data-ttu-id="8a7a0-198">Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="8a7a0-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="8a7a0-199">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="8a7a0-199">YOY purchase growth</span></span>   | <span data-ttu-id="8a7a0-200">Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="8a7a0-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="8a7a0-201">Følgende nøgledimensioner i indholdet bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="8a7a0-202">Enhed</span><span class="sxs-lookup"><span data-stu-id="8a7a0-202">Entity</span></span>                 | <span data-ttu-id="8a7a0-203">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="8a7a0-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="8a7a0-204">Leverandører</span><span class="sxs-lookup"><span data-stu-id="8a7a0-204">Vendors</span></span>                | <span data-ttu-id="8a7a0-205">Kreditorgrupper, kreditorlande eller -områder, kreditornavn</span><span class="sxs-lookup"><span data-stu-id="8a7a0-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="8a7a0-206">Produkter</span><span class="sxs-lookup"><span data-stu-id="8a7a0-206">Products</span></span>               | <span data-ttu-id="8a7a0-207">Produktnummer, produktnavn, varegruppenavn</span><span class="sxs-lookup"><span data-stu-id="8a7a0-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="8a7a0-208">Indkøbskategorier</span><span class="sxs-lookup"><span data-stu-id="8a7a0-208">Procurement categories</span></span> | <span data-ttu-id="8a7a0-209">Indkøbskategori, indkøbskategorinavne</span><span class="sxs-lookup"><span data-stu-id="8a7a0-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="8a7a0-210">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="8a7a0-210">Legal entities</span></span>         | <span data-ttu-id="8a7a0-211">Navn på juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="8a7a0-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="8a7a0-212">Datoer</span><span class="sxs-lookup"><span data-stu-id="8a7a0-212">Dates</span></span>                  | <span data-ttu-id="8a7a0-213">Datoer, årsforskydning</span><span class="sxs-lookup"><span data-stu-id="8a7a0-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="8a7a0-214">Som standard viser indholdet data for det indeværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="8a7a0-215">Du kan dog ændre datofilteret i rapportens filterafsnit.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="8a7a0-216">Du kan også ændre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="8a7a0-216">You can also change the company filter.</span></span>
