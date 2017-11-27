--- 
title: Oprette en baselineprognose
description: "En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel."
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: 6a712077fed4a94ae6ae6ce7ea2cfba8848e5fa5
ms.contentlocale: da-dk
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="2c310-103">Oprette en baselineprognose</span><span class="sxs-lookup"><span data-stu-id="2c310-103">Create a baseline forecast</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c310-104">En produktionsplanlægger kan oprette et prognosegrundlag ved hjælp af prognosemodeller med tidsserier eller ved at kopiere den historiske efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="2c310-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="2c310-105">Denne procedure viser, hvordan du kopierer den historiske efterspørgsel for at oprette et prognosegrundlag for alle produkter ved brug af en varefordelingsnøgle.</span><span class="sxs-lookup"><span data-stu-id="2c310-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="2c310-106">Oprette en varefordelingsnøgle</span><span class="sxs-lookup"><span data-stu-id="2c310-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="2c310-107">Gå til Overordnet planlægning > Opsætning > Interne planlægningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="2c310-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="2c310-108">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="2c310-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2c310-109">For eksempel kan du filtrere på feltet Navn med værdien '10'.</span><span class="sxs-lookup"><span data-stu-id="2c310-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="2c310-110">Behovsprognose kører på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="2c310-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="2c310-111">Derfor skal du konfigurere alle firmaer, som du generere prognoser for, i en intern planlægningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2c310-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="2c310-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2c310-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2c310-113">Klik på Vis varefordelingsnøgler.</span><span class="sxs-lookup"><span data-stu-id="2c310-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="2c310-114">Vælg alle de varefordelingsnøgler, hvortil du vil oprette prognoser.</span><span class="sxs-lookup"><span data-stu-id="2c310-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="2c310-115">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2c310-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2c310-116">Vælg D_Aloc-varefordelingsnøgle.</span><span class="sxs-lookup"><span data-stu-id="2c310-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="2c310-117">Klik på >.</span><span class="sxs-lookup"><span data-stu-id="2c310-117">Click >.</span></span>
7. <span data-ttu-id="2c310-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2c310-118">Close the page.</span></span>
8. <span data-ttu-id="2c310-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="2c310-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="2c310-120">Konfigurer parametre til behovsprognoserne</span><span class="sxs-lookup"><span data-stu-id="2c310-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="2c310-121">Gå til Overordnet planlægning > Opsætning > Behovsprognose > Parametre til behovsprognoser.</span><span class="sxs-lookup"><span data-stu-id="2c310-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="2c310-122">Udvid sektionen Parametre til prognosealgoritme.</span><span class="sxs-lookup"><span data-stu-id="2c310-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="2c310-123">Vælg "Kopiér over historisk efterspørgsel" i feltet Strategi for generering af prognose.</span><span class="sxs-lookup"><span data-stu-id="2c310-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="2c310-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="2c310-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="2c310-125">Oprette en baselineprognose</span><span class="sxs-lookup"><span data-stu-id="2c310-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="2c310-126">Gå til Overordnet planlægning > Prognose > Behovsprognose > Generér statistisk budgetgrundlag.</span><span class="sxs-lookup"><span data-stu-id="2c310-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="2c310-127">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="2c310-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="2c310-128">Hvis du har salgsordrer med start fra 1. januar 2015, skal du angive denne dato.</span><span class="sxs-lookup"><span data-stu-id="2c310-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="2c310-129">Hvis du ikke har det, kan du angive den tidligste dato for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="2c310-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="2c310-130">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="2c310-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="2c310-131">Angiv den sidste dato for dine salgsordrer, f.eks. '31-03-2015'.</span><span class="sxs-lookup"><span data-stu-id="2c310-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="2c310-132">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="2c310-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="2c310-133">Indtast '01-04-2015'.</span><span class="sxs-lookup"><span data-stu-id="2c310-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="2c310-134">Denne dato beregnes automatisk som startdatoen for det næste prognosegruppe.</span><span class="sxs-lookup"><span data-stu-id="2c310-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="2c310-135">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="2c310-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="2c310-136">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="2c310-136">Click Filter.</span></span>
7. <span data-ttu-id="2c310-137">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2c310-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2c310-138">Markér rækken, hvor feltet = intern planlægningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2c310-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="2c310-139">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="2c310-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="2c310-140">Indtast den interne planlægningsgruppe, f.eks. 10, som du brugte i den første opgave.</span><span class="sxs-lookup"><span data-stu-id="2c310-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="2c310-141">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2c310-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2c310-142">Markér rækken, hvor feltet = varefordelingsnøgle.</span><span class="sxs-lookup"><span data-stu-id="2c310-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="2c310-143">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="2c310-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="2c310-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2c310-144">Click OK.</span></span>
12. <span data-ttu-id="2c310-145">Udvid sektionen Avancerede parametre.</span><span class="sxs-lookup"><span data-stu-id="2c310-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="2c310-146">Vælg "Måned" i feltet Prognosegruppe.</span><span class="sxs-lookup"><span data-stu-id="2c310-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="2c310-147">Angiv "3" i feltet Prognosehorisont.</span><span class="sxs-lookup"><span data-stu-id="2c310-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="2c310-148">Angiv "1" i feltet Låsningstidshorisont.</span><span class="sxs-lookup"><span data-stu-id="2c310-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="2c310-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="2c310-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="2c310-150">Visualiser behovsprognosen</span><span class="sxs-lookup"><span data-stu-id="2c310-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="2c310-151">Gå til Overordnet planlægning > Prognose > Behovsprognose > Justeret behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="2c310-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="2c310-152">Vælg cellen i række 1, kolonne 2 i tabellen for aggregeret visning.</span><span class="sxs-lookup"><span data-stu-id="2c310-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="2c310-153">Dette er den anden måned, du har oprettet budget for.</span><span class="sxs-lookup"><span data-stu-id="2c310-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="2c310-154">Angiv QtyCell til "400".</span><span class="sxs-lookup"><span data-stu-id="2c310-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="2c310-155">Angiv et andet tal i cellen end det, der blev prognosticeret, f.eks. 400.</span><span class="sxs-lookup"><span data-stu-id="2c310-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="2c310-156">Du har foretaget en manuel regulering af prognosen.</span><span class="sxs-lookup"><span data-stu-id="2c310-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="2c310-157">Bemærk den grafiske indikator i næste trin.</span><span class="sxs-lookup"><span data-stu-id="2c310-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="2c310-158">Klik på Prognoselinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="2c310-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="2c310-159">Du kan se de nøjagtige værdier, historisk efterspørgsel og prognose på denne side.</span><span class="sxs-lookup"><span data-stu-id="2c310-159">On this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="2c310-160">Du kan også foretage ændringer af prognosen.</span><span class="sxs-lookup"><span data-stu-id="2c310-160">You can make changes to the forecast as well.</span></span>  


