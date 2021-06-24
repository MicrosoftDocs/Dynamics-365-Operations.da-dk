---
title: Foretage manuelle justeringer af prognosegrundlaget
description: I dette emne forklares, hvordan du kan foretage manuelle justeringer af et prognosegrundlag og få vist detaljer om prognosen.
author: roxanadiaconu
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbcdc852bf42038761b4ea19fd7fe7cbfc45f713
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187428"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="7d153-103">Foretage manuelle justeringer af prognosegrundlaget</span><span class="sxs-lookup"><span data-stu-id="7d153-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d153-104">I dette emne forklares, hvordan du kan foretage manuelle justeringer af et prognosegrundlag og få vist detaljer om prognosen.</span><span class="sxs-lookup"><span data-stu-id="7d153-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="7d153-105">Før du foretager manuelle justeringer, er det vigtigt at forstå nogle begreber på forskellige sider.</span><span class="sxs-lookup"><span data-stu-id="7d153-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="7d153-106">Gitter på siden Justeret behovsprognose</span><span class="sxs-lookup"><span data-stu-id="7d153-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="7d153-107">Siden **Justeret behovsprognose** indeholder et gitter, der har følgende struktur:</span><span class="sxs-lookup"><span data-stu-id="7d153-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="7d153-108">Den første kolonne viser varerne, varefordelingsnøgler, virksomheder osv., der er genereret en prognose for.</span><span class="sxs-lookup"><span data-stu-id="7d153-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="7d153-109">Undertitlen på siden indeholder en beskrivelse af de aktuelle prognosedimensioner, der vises i matrixen.</span><span class="sxs-lookup"><span data-stu-id="7d153-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="7d153-110">Hvis undertitlen på siden for eksempel er **firma/websteder/varefordelingsnøgle**, og en af rækkeoverskrifterne i matrixen er **USMF/1/D\_Alloc**, viser rækken budgettet for USMF-firmaet, webstedet 1 og varefordelingsnøglen **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="7d153-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="7d153-111">Efterfølgende kolonnerne repræsenterer de prognosefilsæt, som prognosen er oprettet for.</span><span class="sxs-lookup"><span data-stu-id="7d153-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="7d153-112">Hver enkelt kolonneoverskrift er den første dato i det prognosefilsæt, der vises i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="7d153-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="7d153-113">Værdierne i cellerne repræsenterer prognosen for ét element, varefordelingsnøgle osv. for det specifikke prognosefilsæt.</span><span class="sxs-lookup"><span data-stu-id="7d153-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="7d153-114">Aggregering og de-aggregering af prognose</span><span class="sxs-lookup"><span data-stu-id="7d153-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="7d153-115">Undertitlen på siden viser niveauet af prognoseaggregering.</span><span class="sxs-lookup"><span data-stu-id="7d153-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="7d153-116">Hvis sidens undertitel f.eks. er **Firma/Sted/Fordelingsnøgle/Varenummer/Farve/Størrelse/Konfiguration/Typografi**, er der ingen prognoseaggregering, og prognosen vises på niveauet for varen og dens dimensioner.</span><span class="sxs-lookup"><span data-stu-id="7d153-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="7d153-117">Hvis du vil ændre aggregeringen, skal du bruge siden **Skift prognosedimensioner**, som du kan åbne fra programmenuen.</span><span class="sxs-lookup"><span data-stu-id="7d153-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="7d153-118">Hvis du vil ændre prognosen, skal du klikke i en af de celler, der er tilgængelige, og skrive den justerede prognoseværdi.</span><span class="sxs-lookup"><span data-stu-id="7d153-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="7d153-119">Den redigerede celle bliver straks fed for at angive, at den prognose, som den viser, ikke er den prognose, som den efterspørgsel som behovsprognosetjenesten har oprettet, men er blevet justeret manuelt.</span><span class="sxs-lookup"><span data-stu-id="7d153-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="7d153-120">Hvis du ændrer aggregeringen for at få siden til at vise mere aggregerede data, kan du bruge siden **Behovsprognoselinjer** til at se de individuelle budgetlinjer, der udgør den aggregerede prognose.</span><span class="sxs-lookup"><span data-stu-id="7d153-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="7d153-121">Hvis du f.eks. har genereret prognosen på vareniveauet, men du ved, at behovet for denne vare vil stige på tværs af alle steder på grund af en kampagne eller en lignende hændelse.</span><span class="sxs-lookup"><span data-stu-id="7d153-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="7d153-122">I dette tilfælde kan du angive aggregering til **Firma/Varefordelingsnøgle/Vare** på siden **Skift prognosedimensioner**.</span><span class="sxs-lookup"><span data-stu-id="7d153-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="7d153-123">Du kan justere den globale prognose for varen på tværs af alle steder i matrixen **Justeret behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="7d153-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="7d153-124">Du kan se virkningen af ændringen på alle steder ved at åbne siden **Behovsprognoselinjer**.</span><span class="sxs-lookup"><span data-stu-id="7d153-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="7d153-125">På denne side kan du se en linje for varen for hvert sted, det justerede prognoseantal og det oprindelige prognoseantal.</span><span class="sxs-lookup"><span data-stu-id="7d153-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="7d153-126">Når der foretages justering af prognoseantallet på et aggregeret niveau, bruger systemet vægtet fordeling til at distribuere ændringen mellem de linjer, der skaber aggregeringen.</span><span class="sxs-lookup"><span data-stu-id="7d153-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="7d153-127">Du kan også foretage manuelle justeringer på siden **Behovsprognoselinjer** ved at ændre enten værdien **Samlet antal** eller cellerne **Antal** i de-aggregeringsmatrixen.</span><span class="sxs-lookup"><span data-stu-id="7d153-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="7d153-128">Få vist detaljer om prognosen</span><span class="sxs-lookup"><span data-stu-id="7d153-128">Viewing details of the forecast</span></span>
<span data-ttu-id="7d153-129">Du kan åbne siden **Detaljer om behovsprognose** for at få vist yderligere oplysninger om prognosen.</span><span class="sxs-lookup"><span data-stu-id="7d153-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="7d153-130">Siden **Detaljer om behovsprognose** side viser følgende oplysninger i grafisk format og tabelformat:</span><span class="sxs-lookup"><span data-stu-id="7d153-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="7d153-131">Det historiske behov, som de prognoseforudsigelserne er baseret på.</span><span class="sxs-lookup"><span data-stu-id="7d153-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="7d153-132">Den aktuelle prognose, der bruges ved varedisponering.</span><span class="sxs-lookup"><span data-stu-id="7d153-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="7d153-133">De nye behovsprognoseværdier og de beløb, de justeres for manuelt.</span><span class="sxs-lookup"><span data-stu-id="7d153-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="7d153-134">Konfidensintervallet for prognoseværdierne.</span><span class="sxs-lookup"><span data-stu-id="7d153-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="7d153-135">Den prognosemodel, der blev brugt til at oprette prognosen.</span><span class="sxs-lookup"><span data-stu-id="7d153-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="7d153-136">Hvis du får vist aggregerede data, kan du se listen over alle de metoder, der blev brugt til den aggregerede tidsserie.</span><span class="sxs-lookup"><span data-stu-id="7d153-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="7d153-137">Nøjagtigheden af den interne model (MAPE).</span><span class="sxs-lookup"><span data-stu-id="7d153-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="7d153-138">Du kan få flere oplysninger om prognosenøjagtighed under [Overvåg prognosenøjagtighed](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="7d153-138">For more information about forecast accuracy, see [Monitor forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="7d153-139">**Bemærkninger:**</span><span class="sxs-lookup"><span data-stu-id="7d153-139">**Notes:**</span></span>

-   <span data-ttu-id="7d153-140">Hvis du aktiverer **Oplysninger om valg af prognosemodel for behovsprognose** fra funktionsstyring, kan du vælge de prognosemodeller, der skal medtages for den historiske prognose, på siden **Oplysninger om behovsprognoser**.</span><span class="sxs-lookup"><span data-stu-id="7d153-140">If you enable **Forecast model selection on Demand forecast details** from Feature management, you will be able to select the forecast models to be include, for the historical forecast, on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="7d153-141">De konfidensinterval, der vises i sektionen **Prognose** på siden, der repræsenterer forskellen mellem den øvre grænse for konfidensintervallet og den nedre grænse for konfidensintervallet.</span><span class="sxs-lookup"><span data-stu-id="7d153-141">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="7d153-142">For at få vist værdierne for de øvre og nedre grænser skal du holde markøren over diagrammet i sektionen **Historisk efterspørgsel og prognose grafisk**.</span><span class="sxs-lookup"><span data-stu-id="7d153-142">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="7d153-143">Hvis du bruger behovsprognose med Microsoft Azure Machine Learning, kan du angive det procentvise konfidensniveau, som den generede prognose skal have.</span><span class="sxs-lookup"><span data-stu-id="7d153-143">If you use the Demand forecasting Microsoft Azure Machine Learning, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="7d153-144">Et konfidensinterval består af en række værdier, der fungerer som gode estimater for behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="7d153-144">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="7d153-145">En konfidensinternval på 95 procent angiver, at der er 5 procent risiko for, at behovsprognosen falder uden for konfidensintervalområdet.</span><span class="sxs-lookup"><span data-stu-id="7d153-145">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="7d153-146">Du kan også foretage manuelle justeringer af prognosen på siden **Detaljer om behovsprognose** ved at ændre værdierne i rækken **Prognose** i sektionen **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="7d153-146">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d153-147">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7d153-147">Additional resources</span></span>

[<span data-ttu-id="7d153-148">Overvåge prognosenøjagtighed</span><span class="sxs-lookup"><span data-stu-id="7d153-148">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="7d153-149">Generere et statistisk budgetgrundlag</span><span class="sxs-lookup"><span data-stu-id="7d153-149">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]