---
title: 'Vejledning: Oprette et prognosegrundlag'
description: En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223956"
---
# <a name="guide-create-a-baseline-forecast"></a><span data-ttu-id="5d8be-103">Vejledning: Oprette et prognosegrundlag</span><span class="sxs-lookup"><span data-stu-id="5d8be-103">Guide: Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d8be-104">En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="5d8be-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="5d8be-105">Denne procedure viser, hvordan du kopierer den historiske efterspørgsel for at oprette et prognosegrundlag for alle produkter ved brug af en varefordelingsnøgle.</span><span class="sxs-lookup"><span data-stu-id="5d8be-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span>

## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="5d8be-106">Oprette en varefordelingsnøgle</span><span class="sxs-lookup"><span data-stu-id="5d8be-106">Set up an item allocation key</span></span>

1. <span data-ttu-id="5d8be-107">Gå til **Varedisponering > Opsætning > Interne planlægningsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-107">Go to **Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="5d8be-108">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="5d8be-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5d8be-109">For eksempel kan du filtrere på feltet *Navn* med værdien *10*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-109">For example, filter on the *Name* field with a value of *10*.</span></span>
    * <span data-ttu-id="5d8be-110">Behovsprognose kører på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="5d8be-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="5d8be-111">Derfor skal du konfigurere alle firmaer, som du generere prognoser for, i en intern planlægningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5d8be-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="5d8be-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5d8be-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5d8be-113">Vælg **Varefordelingsnøgler**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-113">Select **Item allocation keys**.</span></span>
    * <span data-ttu-id="5d8be-114">Vælg alle de varefordelingsnøgler, hvortil du vil oprette prognoser.</span><span class="sxs-lookup"><span data-stu-id="5d8be-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="5d8be-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5d8be-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5d8be-116">Vælg D_Aloc-varefordelingsnøgle.</span><span class="sxs-lookup"><span data-stu-id="5d8be-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="5d8be-117">Vælg **>**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-117">Select **>**.</span></span>
7. <span data-ttu-id="5d8be-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5d8be-118">Close the page.</span></span>
8. <span data-ttu-id="5d8be-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5d8be-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="5d8be-120">Konfigurere parametre til behovsprognoserne</span><span class="sxs-lookup"><span data-stu-id="5d8be-120">Set up the demand forecasting parameters</span></span>

1. <span data-ttu-id="5d8be-121">Gå til **Varedisponering > Opsætning > Behovsprognose > Parametre til behovsprognoser**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-121">Go to **Master planning > Setup > Demand forecasting > Demand forecasting parameters**.</span></span>
2. <span data-ttu-id="5d8be-122">Udvid sektionen **Parametre til prognosealgoritme**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-122">Expand the **Forecast algorithm parameters** section.</span></span>
3. <span data-ttu-id="5d8be-123">Vælg **Kopiér over historisk efterspørgsel** i feltet **Strategi for generering af prognose**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-123">In the **Forecast generation strategy** field, select **Copy over historical demand**.</span></span>
4. <span data-ttu-id="5d8be-124">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-124">Select **Save**.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="5d8be-125">Oprette et prognosegrundlag</span><span class="sxs-lookup"><span data-stu-id="5d8be-125">Create a baseline forecast</span></span>

1. <span data-ttu-id="5d8be-126">Gå til **Varedisponering > Prognose > Behovsprognose > Generér statistisk budgetgrundlag**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-126">Go to **Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast**.</span></span>
2. <span data-ttu-id="5d8be-127">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-127">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5d8be-128">Hvis du har salgsordrer med start fra 1. januar 2015, skal du angive denne dato.</span><span class="sxs-lookup"><span data-stu-id="5d8be-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="5d8be-129">Hvis du ikke har det, kan du angive den tidligste dato for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="5d8be-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="5d8be-130">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-130">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="5d8be-131">Angiv den sidste dato for dine salgsordrer, f.eks. *31-03-2015*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-131">Enter the last date of your sales orders, for example *2015-03-31*.</span></span>  
4. <span data-ttu-id="5d8be-132">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-132">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="5d8be-133">Indtast *01-04-2015*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-133">Enter *2015-04-01*.</span></span> <span data-ttu-id="5d8be-134">Denne dato beregnes automatisk som startdatoen for det næste prognosegruppe.</span><span class="sxs-lookup"><span data-stu-id="5d8be-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="5d8be-135">Udvid sektionen **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-135">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="5d8be-136">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-136">Select **Filter**.</span></span>
7. <span data-ttu-id="5d8be-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5d8be-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5d8be-138">Markér rækken, hvor **Felt** = *Intern planlægningsgruppe*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-138">Mark the row where **Field** = *Intercompany planning group*.</span></span>  
8. <span data-ttu-id="5d8be-139">Skriv en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-139">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="5d8be-140">Indtast den interne planlægningsgruppe (f.eks. *10*), som du brugte i den første opgave.</span><span class="sxs-lookup"><span data-stu-id="5d8be-140">Type the intercompany planning group (for example, *10*) that you used in the first task.</span></span>  
9. <span data-ttu-id="5d8be-141">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5d8be-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5d8be-142">Markér rækken, hvor **Felt** = *Varefordelingsnøgle*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-142">Select the row where **Field** = *Item allocation key*.</span></span>  
10. <span data-ttu-id="5d8be-143">Skriv en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-143">In the **Criteria** field, type a value.</span></span>
11. <span data-ttu-id="5d8be-144">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-144">Select **OK**.</span></span>
12. <span data-ttu-id="5d8be-145">Udvid sektionen **Avancerede parametre**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-145">Expand the **Advanced parameters** section.</span></span>
13. <span data-ttu-id="5d8be-146">Vælg **Måned** i feltet *Prognosegruppe*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-146">In the **Forecast bucket** field, select *Month*.</span></span>
14. <span data-ttu-id="5d8be-147">Angiv **3** i feltet *Prognosehorisont*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-147">In the **Forecast horizon** field, enter *3*.</span></span>
15. <span data-ttu-id="5d8be-148">Angiv **1** i feltet *Låsningstidshorisont*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-148">In the **Freeze time fence** field, enter *1*.</span></span>
16. <span data-ttu-id="5d8be-149">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-149">Select **OK**.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="5d8be-150">Visualiser behovsprognosen</span><span class="sxs-lookup"><span data-stu-id="5d8be-150">Visualize the demand forecast</span></span>

1. <span data-ttu-id="5d8be-151">Gå til **Varedisponering > Prognose > Behovsprognose > Justeret behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-151">Go to **Master planning > Forecasting > Demand forecasting > Adjusted demand forecast**.</span></span>
2. <span data-ttu-id="5d8be-152">Vælg cellen i række 1, kolonne 2 i tabellen for aggregeret visning.</span><span class="sxs-lookup"><span data-stu-id="5d8be-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="5d8be-153">Dette er den anden måned, du har oprettet budget for.</span><span class="sxs-lookup"><span data-stu-id="5d8be-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="5d8be-154">Angiv **QtyCell** til *400*.</span><span class="sxs-lookup"><span data-stu-id="5d8be-154">Set **QtyCell** to *400*.</span></span>
    * <span data-ttu-id="5d8be-155">Angiv et andet tal i cellen end det, der blev prognosticeret, f.eks. 400.</span><span class="sxs-lookup"><span data-stu-id="5d8be-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="5d8be-156">Du har foretaget en manuel regulering af prognosen.</span><span class="sxs-lookup"><span data-stu-id="5d8be-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="5d8be-157">Bemærk den grafiske indikator i næste trin.</span><span class="sxs-lookup"><span data-stu-id="5d8be-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="5d8be-158">Vælg **Prognoselinjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="5d8be-158">Select **Forecast line details**.</span></span>
    * <span data-ttu-id="5d8be-159">Du kan se de nøjagtige værdier, historisk efterspørgsel og prognose på denne side.</span><span class="sxs-lookup"><span data-stu-id="5d8be-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="5d8be-160">Du kan også foretage ændringer af prognosen.</span><span class="sxs-lookup"><span data-stu-id="5d8be-160">You can make changes to the forecast as well.</span></span>  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]