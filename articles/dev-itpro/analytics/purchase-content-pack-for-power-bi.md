---
title: "Power BI-indhold til købsforbrugsanalyse"
description: "I dette emne beskrives, hvad der skal medtages i Power BI-indhold til Købsforbrugsanalyse. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der bliver brugt til at oprette indholdet."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6485f36802fc4e327e223f47d65c4bdca11c1609
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="00145-104">Power BI-indhold til købsforbrugsanalyse</span><span class="sxs-lookup"><span data-stu-id="00145-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="00145-105">I dette emne beskrives, hvad der skal medtages i Microsoft Power BI-indholdet til **Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="00145-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="00145-106">Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.</span><span class="sxs-lookup"><span data-stu-id="00145-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="00145-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="00145-107">Overview</span></span>

<span data-ttu-id="00145-108">Power BI-indholdet til **Købsforbrugsanalyse** er udviklet til at hjælpe indkøbschefer og ledere, der er ansvarlige for budgetter, med at holde øje med udgifter til køb.</span><span class="sxs-lookup"><span data-stu-id="00145-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="00145-109">Chefer kan analysere indkøbsudgifter på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="00145-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="00145-110">Køb år til dato (efter kreditorgruppe og individuelle kreditorer, indkøbskategori og individuelle produkter og leverandørlokalitet)</span><span class="sxs-lookup"><span data-stu-id="00145-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="00145-111">Ændring af køb år for-år (efter leverandørgruppe og indkøbskategori)</span><span class="sxs-lookup"><span data-stu-id="00145-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="00145-112">Indholdet bruger købstransaktionsdata og indeholder både en samlet oversigt over alle firmaets købstal og en opdeling af købsforbrug pr. leverandør og vare.</span><span class="sxs-lookup"><span data-stu-id="00145-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="00145-113">Rapporter fremhæve ændringer i købsforbruget over tid.</span><span class="sxs-lookup"><span data-stu-id="00145-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="00145-114">Derfor kan rapporterne bruges til at give ledere besked om positive og negative forbrugstendenser for individuelle leverandører og produkter.</span><span class="sxs-lookup"><span data-stu-id="00145-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="00145-115">Desuden viser diagrammer købsforbruget til forskellige indkøbskategorier og kreditorgrupper.</span><span class="sxs-lookup"><span data-stu-id="00145-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="00145-116">Derfor kan kategori- og områdeledere bruge diagrammerne til at identificere ændringer i forbrugsmønsteret.</span><span class="sxs-lookup"><span data-stu-id="00145-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="00145-117">Adgang til Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="00145-117">Accessing the Power BI content</span></span>
<span data-ttu-id="00145-118">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) vises Power BI-indholdet til **Købsforbrugsanalyse** på siden **Købs- og forbrugsanalyse** (**Indkøb og forsyning** > **Forespørgsler og rapporter** > **Performanceanalyse for indkøb** > **Købs- og forbrugsanalyse**).</span><span class="sxs-lookup"><span data-stu-id="00145-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="00145-119">Metrikker, der er inkluderet i Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="00145-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="00145-120">Power BI-indholdspakken til **Købsforbrugsanalyse** indeholder en rapport, der består af et sæt metrikker.</span><span class="sxs-lookup"><span data-stu-id="00145-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="00145-121">Disse metrikker visualiseres som diagrammer, felter og tabeller.</span><span class="sxs-lookup"><span data-stu-id="00145-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="00145-122">I nedenstående tabel vises en oversigt over visualiseringerne.</span><span class="sxs-lookup"><span data-stu-id="00145-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00145-123">Rapportside</span><span class="sxs-lookup"><span data-stu-id="00145-123">Report page</span></span></th>
<th><span data-ttu-id="00145-124">Diagrammer</span><span class="sxs-lookup"><span data-stu-id="00145-124">Charts</span></span></th>
<th><span data-ttu-id="00145-125">Felter</span><span class="sxs-lookup"><span data-stu-id="00145-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00145-126">Indkøb efter leverandør</span><span class="sxs-lookup"><span data-stu-id="00145-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="00145-127">Top 10 leverandører efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="00145-128">Samlet indkøb pr. leverandørgruppe/land/navn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="00145-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="00145-129">Indkøb pr. leverandørgruppe/land/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="00145-130">Gennemsnitsindkøb pr. leverandørgruppe/land/navn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="00145-131">Indkøb i alt</span><span class="sxs-lookup"><span data-stu-id="00145-131">Total purchase</span></span></li>
<li><span data-ttu-id="00145-132">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="00145-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="00145-133">Antal leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="00145-133">Total # vendors</span></span></li>
<li><span data-ttu-id="00145-134">Antal aktive leverandører i alt</span><span class="sxs-lookup"><span data-stu-id="00145-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00145-135">Køb pr. produkt</span><span class="sxs-lookup"><span data-stu-id="00145-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="00145-136">Køb efter indkøbskategori/produktnavn (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="00145-137">Indkøb i alt efter indkøbskategori/produktnavn (cirkeldiagram)</span><span class="sxs-lookup"><span data-stu-id="00145-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="00145-138">Top 10 produkter efter indkøb (stablet liggende søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="00145-139">Antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="00145-139">Total # of products</span></span></li>
<li><span data-ttu-id="00145-140">Antal aktive produkter i alt i procentdel af antal produkter i alt</span><span class="sxs-lookup"><span data-stu-id="00145-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="00145-141">Antal produkter, der udgør for 80 % af indkøbet</span><span class="sxs-lookup"><span data-stu-id="00145-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00145-142">Indkøb efter periode*</span><span class="sxs-lookup"><span data-stu-id="00145-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="00145-143">Indkøb pr. måned/dag (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="00145-144">Afvigelse i akkumuleret indkøb år for år (vandfaldsdiagram)</span><span class="sxs-lookup"><span data-stu-id="00145-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="00145-145">Vækst i indkøb i alt år for år (søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="00145-146">Indkøbsopgørelse (matrix)</span><span class="sxs-lookup"><span data-stu-id="00145-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="00145-147">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="00145-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="00145-148">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="00145-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00145-149">Indkøb efter leverandørlokalitet</span><span class="sxs-lookup"><span data-stu-id="00145-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="00145-150">Indkøb efter by</span><span class="sxs-lookup"><span data-stu-id="00145-150">Purchase by city</span></span></li>
<li><span data-ttu-id="00145-151">Indkøbsvækst år for år i %</span><span class="sxs-lookup"><span data-stu-id="00145-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="00145-152">Indkøb efter land</span><span class="sxs-lookup"><span data-stu-id="00145-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00145-153">Købsforbrugsanalyse efter tidspunkt</span><span class="sxs-lookup"><span data-stu-id="00145-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="00145-154">Indkøb indeværende år efter måned/dag (kurvediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="00145-155">Køb indeværende og sidste år (linje- og søjlediagram)</span><span class="sxs-lookup"><span data-stu-id="00145-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00145-156">Købsforbrugsanalyse efter leverandør</span><span class="sxs-lookup"><span data-stu-id="00145-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="00145-157">Indkøb hos top 10 kreditorer i % af indkøb (tragtformet)</span><span class="sxs-lookup"><span data-stu-id="00145-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="00145-158">Top 10 leverandører med forøget forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="00145-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="00145-159">Top 10 leverandører med faldende forbrug år for år</span><span class="sxs-lookup"><span data-stu-id="00145-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="00145-160">\* Køb dette og sidste år, og vækst efter indkøbskategori</span><span class="sxs-lookup"><span data-stu-id="00145-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="00145-161">Udvidelse af Power BI-indhold</span><span class="sxs-lookup"><span data-stu-id="00145-161">Extending the Power BI content</span></span>
<span data-ttu-id="00145-162">Når du bruger de indholdspakker, der er tilgængelige i Microsoft Dynamics Lifecycle Services (LCS), kan du levere fremragende analyser til personer, der ikke logger på Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="00145-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="00145-163">Du kan redigere disse indholdspakker, så de omfatter andre rapporter eller grafik, og derefter udgive indholdspakkerne på din Power BI.com-lejer med henblik på analyse.</span><span class="sxs-lookup"><span data-stu-id="00145-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="00145-164">Du kan finde Power BI-indholdet til **Købsforbrugsanalyse** i biblioteket med delte aktiver i LCS.</span><span class="sxs-lookup"><span data-stu-id="00145-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="00145-165">Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="00145-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="00145-166">Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="00145-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="00145-167">Sørg for at downloade **Købsforbrugsanalyse**-indhold, der gælder for den version af Dynamics 365, du bruger.</span><span class="sxs-lookup"><span data-stu-id="00145-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="00145-168">Hvis du bruger Microsoft Dynamics 365 for Operations version 1611, er KB 4011327 en forudsætning for dette Power BI-indhold.</span><span class="sxs-lookup"><span data-stu-id="00145-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="00145-169">Når du logger på LCS, kan du få adgang til KB på https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="00145-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="00145-170">Datamodel og enheder</span><span class="sxs-lookup"><span data-stu-id="00145-170">Data model and entities</span></span>
<span data-ttu-id="00145-171">Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Købsforbrugsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="00145-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="00145-172">Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="00145-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="00145-173">Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser.</span><span class="sxs-lookup"><span data-stu-id="00145-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="00145-174">Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="00145-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="00145-175">De samlede målinger i dette indhold er et undersæt af de samlede målinger, der var tilgængelige i indkøbskuben i Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="00145-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="00145-176">For at forberede kubens samlede målinger i enhedslageret skal du gøre dem installerbare.</span><span class="sxs-lookup"><span data-stu-id="00145-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="00145-177">Du kan finde flere oplysninger i fremgangsmåden for forberedelse af samlede målinger i enhedslager under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="00145-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="00145-178">Følgende samlede nøglemålinger er tilgængelige direkte fra enheden Fakturalinjer og bruges som grundlag for indholdet.</span><span class="sxs-lookup"><span data-stu-id="00145-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="00145-179">Enhed</span><span class="sxs-lookup"><span data-stu-id="00145-179">Entity</span></span>        | <span data-ttu-id="00145-180">Samlede nøglemålinger</span><span class="sxs-lookup"><span data-stu-id="00145-180">Key aggregate measurements</span></span> | <span data-ttu-id="00145-181">Datakilde</span><span class="sxs-lookup"><span data-stu-id="00145-181">Data source</span></span>                                 | <span data-ttu-id="00145-182">Felt</span><span class="sxs-lookup"><span data-stu-id="00145-182">Field</span></span>              | <span data-ttu-id="00145-183">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="00145-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="00145-184">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="00145-184">Invoice lines</span></span> | <span data-ttu-id="00145-185">Køb</span><span class="sxs-lookup"><span data-stu-id="00145-185">Purchase</span></span>                   | <span data-ttu-id="00145-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="00145-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="00145-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="00145-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="00145-188">Beløbet i regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="00145-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="00145-189">Følgende tabel viser de vigtigste målinger i indholdet, der beregnes fra enheden Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="00145-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="00145-190">Målepunkt</span><span class="sxs-lookup"><span data-stu-id="00145-190">Measure</span></span>               | <span data-ttu-id="00145-191">Kalkulation</span><span class="sxs-lookup"><span data-stu-id="00145-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00145-192">Køb indeværende år</span><span class="sxs-lookup"><span data-stu-id="00145-192">Purchase current year</span></span> | <span data-ttu-id="00145-193">Køb indeværende år = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="00145-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="00145-194">Køb sidste år</span><span class="sxs-lookup"><span data-stu-id="00145-194">Purchase last year</span></span>    | <span data-ttu-id="00145-195">Køb sidste år = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="00145-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="00145-196">Indkøbsvækst år for år</span><span class="sxs-lookup"><span data-stu-id="00145-196">YOY purchase growth</span></span>   | <span data-ttu-id="00145-197">Indkøbsvækst år for år = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="00145-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="00145-198">Følgende nøgledimensioner i indholdet bruges som filtre til at skabe udsnit af de samlede målinger, så du kan få større granularitet og dybere analytisk indsigt.</span><span class="sxs-lookup"><span data-stu-id="00145-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="00145-199">Enhed</span><span class="sxs-lookup"><span data-stu-id="00145-199">Entity</span></span>                 | <span data-ttu-id="00145-200">Eksempler på attributter</span><span class="sxs-lookup"><span data-stu-id="00145-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="00145-201">Leverandører</span><span class="sxs-lookup"><span data-stu-id="00145-201">Vendors</span></span>                | <span data-ttu-id="00145-202">Kreditorgrupper, kreditorlande eller -områder, kreditornavn</span><span class="sxs-lookup"><span data-stu-id="00145-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="00145-203">Produkter</span><span class="sxs-lookup"><span data-stu-id="00145-203">Products</span></span>               | <span data-ttu-id="00145-204">Produktnummer, produktnavn, varegruppenavn</span><span class="sxs-lookup"><span data-stu-id="00145-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="00145-205">Indkøbskategorier</span><span class="sxs-lookup"><span data-stu-id="00145-205">Procurement categories</span></span> | <span data-ttu-id="00145-206">Indkøbskategori, indkøbskategorinavne</span><span class="sxs-lookup"><span data-stu-id="00145-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="00145-207">Juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="00145-207">Legal entities</span></span>         | <span data-ttu-id="00145-208">Navn på juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="00145-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="00145-209">Datoer</span><span class="sxs-lookup"><span data-stu-id="00145-209">Dates</span></span>                  | <span data-ttu-id="00145-210">Datoer, årsforskydning</span><span class="sxs-lookup"><span data-stu-id="00145-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="00145-211">Som standard viser indholdet data for det indeværende kalenderår.</span><span class="sxs-lookup"><span data-stu-id="00145-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="00145-212">Du kan dog ændre datofilteret i rapportens filterafsnit.</span><span class="sxs-lookup"><span data-stu-id="00145-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="00145-213">Du kan også ændre firmafilteret.</span><span class="sxs-lookup"><span data-stu-id="00145-213">You can also change the company filter.</span></span>

