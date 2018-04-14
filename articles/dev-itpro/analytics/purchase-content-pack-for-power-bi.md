---
title: "Power BI-indhold til købsforbrugsanalyse"
description: "I dette emne beskrives, hvad der skal medtages i Power BI-indhold til Købsforbrugsanalyse. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der bliver brugt til at oprette indholdet."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 37f3b1b4d362bd8b40977648b4aa4387011eea08
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="e6fb6-104">Power BI-indhold til købsforbrugsanalyse</span><span class="sxs-lookup"><span data-stu-id="e6fb6-104">Purchase spend analysis Power BI content</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e6fb6-105">I dette emne beskrives, hvad der skal medtages i Microsoft Power BI-indholdet til **Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="e6fb6-106">Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="e6fb6-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="e6fb6-107">Overview</span></span>

<span data-ttu-id="e6fb6-108">Power BI-indholdet til **Købsforbrugsanalyse** er udviklet til at hjælpe indkøbschefer og ledere, der er ansvarlige for budgetter, med at holde øje med udgifter til køb.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="e6fb6-109">Chefer kan analysere indkøbsudgifter på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="e6fb6-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="e6fb6-110">Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="e6fb6-111">Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="e6fb6-112">Indholdet bruger købstransaktionsdata og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="e6fb6-113">Rapporter fremhæve ændringer i købsforbruget over tid.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="e6fb6-114">Derfor kan rapporterne bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="e6fb6-115">Desuden viser diagrammer købsforbruget til forskellige indkøbskategorier og kreditorgrupper.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="e6fb6-116">Derfor kan kategori- og områdeledere bruge diagrammerne til at identificere ændringer i forbrugsmønsteret.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="e6fb6-117">Adgang til Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="e6fb6-117">Accessing the Power BI content</span></span>
<span data-ttu-id="e6fb6-118">Power BI-indholdet **Købsforbrugsanalyse** vises på siden **Købs- og forbrugsanalyse** (**Indkøb og forsyning** > **Forespørgsler og rapporter** > **Performanceanalyse for indkøb** > **Købs- og forbrugsanalyse**).</span><span class="sxs-lookup"><span data-stu-id="e6fb6-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="e6fb6-119">Metrikker, der er inkluderet i Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="e6fb6-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="e6fb6-120">Power BI-indholdspakken til **Købsforbrugsanalyse** indeholder en rapport, der består af et sæt metrikker.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="e6fb6-121">Disse metrikker visualiseres som diagrammer, felter og tabeller.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="e6fb6-122">I nedenstående tabel vises en oversigt over visualiseringerne.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6fb6-123">Rapportside</span><span class="sxs-lookup"><span data-stu-id="e6fb6-123">Report page</span></span></th>
<th><span data-ttu-id="e6fb6-124">Diagrammer</span><span class="sxs-lookup"><span data-stu-id="e6fb6-124">Charts</span></span></th>
<th><span data-ttu-id="e6fb6-125">Felter</span><span class="sxs-lookup"><span data-stu-id="e6fb6-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6fb6-126">Indkøb efter leverandør</span><span class="sxs-lookup"><span data-stu-id="e6fb6-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="e6fb6-127">Top 10 leverandører efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="e6fb6-128">Samlet indkøb pr. leverandørgruppe/land/navn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="e6fb6-129">Indkøb pr. leverandørgruppe/land/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="e6fb6-130">Gennemsnitsindkøb pr. leverandørgruppe/land/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6fb6-131">Indkøb i alt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-131">Total purchase</span></span></li>
<li><span data-ttu-id="e6fb6-132">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="e6fb6-133">Antal leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-133">Total # vendors</span></span></li>
<li><span data-ttu-id="e6fb6-134">Antal aktive leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6fb6-135">Køb pr. produkt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="e6fb6-136">Køb efter indkøbskategori/produktnavn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="e6fb6-137">Indkøb i alt efter indkøbskategori/produktnavn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="e6fb6-138">Top 10 produkter efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6fb6-139">Antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-139">Total # of products</span></span></li>
<li><span data-ttu-id="e6fb6-140">Antal aktive produkter i alt i procentdel af antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="e6fb6-141">Antal produkter, der udgør for 80 % af indkøbet</span><span class="sxs-lookup"><span data-stu-id="e6fb6-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6fb6-142">Indkøb efter periode\*</span><span class="sxs-lookup"><span data-stu-id="e6fb6-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="e6fb6-143">Indkøb pr. måned/dag (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="e6fb6-144">Afvigelse i akkumuleret indkøb år for år (vandfaldsdiagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="e6fb6-145">Vækst i indkøb i alt år for år (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="e6fb6-146">Indkøbsopgørelse (matrix)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e6fb6-147">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="e6fb6-148">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="e6fb6-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6fb6-149">Indkøb efter leverandørlokalitet</span><span class="sxs-lookup"><span data-stu-id="e6fb6-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="e6fb6-150">Indkøb efter by</span><span class="sxs-lookup"><span data-stu-id="e6fb6-150">Purchase by city</span></span></li>
<li><span data-ttu-id="e6fb6-151">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="e6fb6-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="e6fb6-152">Indkøb efter land</span><span class="sxs-lookup"><span data-stu-id="e6fb6-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6fb6-153">Købsforbrugsanalyse efter tidspunkt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="e6fb6-154">Indkøb indeværende år efter måned/dag (kurvediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="e6fb6-155">Køb indeværende og sidste år (linje- og søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6fb6-156">Købsforbrugsanalyse efter leverandør</span><span class="sxs-lookup"><span data-stu-id="e6fb6-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="e6fb6-157">Indkøb hos top 10 kreditorer i % af indkøb (tragtformet)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="e6fb6-158">Top 10 leverandører med forøget forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="e6fb6-159">Top 10 leverandører med faldende forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e6fb6-160">\* Køb dette og sidste år, og vækst efter indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="e6fb6-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="e6fb6-161">Datamodel og enheder</span><span class="sxs-lookup"><span data-stu-id="e6fb6-161">Data model and entities</span></span>
<span data-ttu-id="e6fb6-162">Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="e6fb6-163">Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="e6fb6-164">Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="e6fb6-165">Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="e6fb6-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="e6fb6-166">De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i indkøbskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="e6fb6-167">For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-167">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="e6fb6-168">Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="e6fb6-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="e6fb6-169">Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdet.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="e6fb6-170">Enhed</span><span class="sxs-lookup"><span data-stu-id="e6fb6-170">Entity</span></span>        | <span data-ttu-id="e6fb6-171">Samlede nøglemålinger</span><span class="sxs-lookup"><span data-stu-id="e6fb6-171">Key aggregate measurements</span></span> | <span data-ttu-id="e6fb6-172">Datakilde</span><span class="sxs-lookup"><span data-stu-id="e6fb6-172">Data source</span></span>                                 | <span data-ttu-id="e6fb6-173">Felt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-173">Field</span></span>              | <span data-ttu-id="e6fb6-174">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="e6fb6-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="e6fb6-175">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="e6fb6-175">Invoice lines</span></span> | <span data-ttu-id="e6fb6-176">Køb</span><span class="sxs-lookup"><span data-stu-id="e6fb6-176">Purchase</span></span>                   | <span data-ttu-id="e6fb6-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="e6fb6-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="e6fb6-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="e6fb6-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="e6fb6-179">Beløbet i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="e6fb6-180">Følgende tabel viser de vigtigste målinger i indholdet, der beregnes fra enheden Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="e6fb6-181">Målepunkt</span><span class="sxs-lookup"><span data-stu-id="e6fb6-181">Measure</span></span>               | <span data-ttu-id="e6fb6-182">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="e6fb6-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fb6-183">Køb indeværende år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-183">Purchase current year</span></span> | <span data-ttu-id="e6fb6-184">Køb indeværende år = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="e6fb6-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="e6fb6-185">Køb sidste år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-185">Purchase last year</span></span>    | <span data-ttu-id="e6fb6-186">Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="e6fb6-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="e6fb6-187">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="e6fb6-187">YOY purchase growth</span></span>   | <span data-ttu-id="e6fb6-188">Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="e6fb6-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="e6fb6-189">Følgende nøgledimensioner i indholdet bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="e6fb6-190">Enhed</span><span class="sxs-lookup"><span data-stu-id="e6fb6-190">Entity</span></span>                 | <span data-ttu-id="e6fb6-191">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="e6fb6-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e6fb6-192">Leverandører</span><span class="sxs-lookup"><span data-stu-id="e6fb6-192">Vendors</span></span>                | <span data-ttu-id="e6fb6-193">Kreditorgrupper, kreditorlande eller -områder, kreditornavn</span><span class="sxs-lookup"><span data-stu-id="e6fb6-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="e6fb6-194">Produkter</span><span class="sxs-lookup"><span data-stu-id="e6fb6-194">Products</span></span>               | <span data-ttu-id="e6fb6-195">Produktnummer, produktnavn, varegruppenavn</span><span class="sxs-lookup"><span data-stu-id="e6fb6-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="e6fb6-196">Indkøbskategorier</span><span class="sxs-lookup"><span data-stu-id="e6fb6-196">Procurement categories</span></span> | <span data-ttu-id="e6fb6-197">Indkøbskategori, indkøbskategorinavne</span><span class="sxs-lookup"><span data-stu-id="e6fb6-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="e6fb6-198">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="e6fb6-198">Legal entities</span></span>         | <span data-ttu-id="e6fb6-199">Navn på juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="e6fb6-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="e6fb6-200">Datoer</span><span class="sxs-lookup"><span data-stu-id="e6fb6-200">Dates</span></span>                  | <span data-ttu-id="e6fb6-201">Datoer, årsforskydning</span><span class="sxs-lookup"><span data-stu-id="e6fb6-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="e6fb6-202">Som standard viser indholdet data for det indeværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="e6fb6-203">Du kan dog ændre datofilteret i rapportens filterafsnit.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="e6fb6-204">Du kan også ændre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="e6fb6-204">You can also change the company filter.</span></span>

