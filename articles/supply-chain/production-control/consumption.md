---
title: Beregne materialeforbrug
description: Denne artikel indeholder oplysninger om forskellige indstillinger, der er relateret til beregning af materialeforbrug.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8defe5735726e877f37d8595a6aaa7c3d14d226b
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="a7be9-103">Beregne materialeforbrug</span><span class="sxs-lookup"><span data-stu-id="a7be9-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7be9-104">Denne artikel indeholder oplysninger om forskellige indstillinger, der er relateret til beregning af materialeforbrug.</span><span class="sxs-lookup"><span data-stu-id="a7be9-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="a7be9-105">Følgende indstillinger, der er knyttet til beregning af materialeforbruge er tilgængelige på fanerne **Opsætning** og **Trinforbrug** på oversigtspanelet **Linjedetaljer** på siden **Stykliste**.</span><span class="sxs-lookup"><span data-stu-id="a7be9-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="a7be9-106">Variabelt eller konstant forbrug</span><span class="sxs-lookup"><span data-stu-id="a7be9-106">Variable and constant consumption</span></span>
<span data-ttu-id="a7be9-107">I feltet **Forbrug er** kan du vælge, om forbruget skal beregnes som et konstant antal eller et variabelt antal.</span><span class="sxs-lookup"><span data-stu-id="a7be9-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="a7be9-108">Vælg **Konstant**, hvis et fast antal eller volumen kræves til produktionen, uanset det producerede antal.</span><span class="sxs-lookup"><span data-stu-id="a7be9-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="a7be9-109">Vælg **Variabelt**, som er standardindstillingen, hvis den påkrævede materiale i de færdige varer er proportionelt med antallet af færdigvarer, der er produceret.</span><span class="sxs-lookup"><span data-stu-id="a7be9-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="a7be9-110">Beregne forbrug fra en formel</span><span class="sxs-lookup"><span data-stu-id="a7be9-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="a7be9-111">I feltet **Formel** kan du oprette forskellige formler til beregning af materialeforbruget.</span><span class="sxs-lookup"><span data-stu-id="a7be9-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="a7be9-112">Hvis du bruger standardværdien, **Standard**, beregnes forbruger ikke fra en formel.</span><span class="sxs-lookup"><span data-stu-id="a7be9-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="a7be9-113">Følgende formler fungerer sammen med felterne **Højde**, **Bredde**, **Dybde**, **Massefylde** og **Konstant**:</span><span class="sxs-lookup"><span data-stu-id="a7be9-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="a7be9-114">Højde \* Konstant</span><span class="sxs-lookup"><span data-stu-id="a7be9-114">Height \* Constant</span></span>
-   <span data-ttu-id="a7be9-115">Højde \* Bredde \* Konstant</span><span class="sxs-lookup"><span data-stu-id="a7be9-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="a7be9-116">Højde \* Bredde \* Dybde \* Konstant</span><span class="sxs-lookup"><span data-stu-id="a7be9-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="a7be9-117">(Højde \* Bredde \* Dybde/Massefylde) \* Konstant</span><span class="sxs-lookup"><span data-stu-id="a7be9-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="a7be9-118">Afrunding og multipla</span><span class="sxs-lookup"><span data-stu-id="a7be9-118">Rounding up and multiples</span></span>
<span data-ttu-id="a7be9-119">Sammen giver felterne **Afrunding** og **Multipla** dig mulighed for at afrunde materialeforbrugsværdien.</span><span class="sxs-lookup"><span data-stu-id="a7be9-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="a7be9-120">Du kan for eksempel afrunde værdien i overensstemmelse med den materialehåndteringsenhed, hvori råvaren plukkes til produktion.</span><span class="sxs-lookup"><span data-stu-id="a7be9-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="a7be9-121">Følgende indstillinger er tilgængelige i feltet **Afrunding**: **Antal**, **Måling** og **Forbrug**.</span><span class="sxs-lookup"><span data-stu-id="a7be9-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="a7be9-122">Antal</span><span class="sxs-lookup"><span data-stu-id="a7be9-122">Quantity</span></span>

<span data-ttu-id="a7be9-123">Hvis du vælger **Antal** som afrundingsmekanisme, skal antallet være et multiplum af det angivne antal.</span><span class="sxs-lookup"><span data-stu-id="a7be9-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="a7be9-124">Hvis der f.eks. skal bruges hele tal, skal du angive **1** i feltet **Multipla**.</span><span class="sxs-lookup"><span data-stu-id="a7be9-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="a7be9-125">Tal afrundes derefter til et antal, der er delelig med 1.</span><span class="sxs-lookup"><span data-stu-id="a7be9-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="a7be9-126">Mål</span><span class="sxs-lookup"><span data-stu-id="a7be9-126">Measurement</span></span>

<span data-ttu-id="a7be9-127">Typisk ville du vælge **Måling** som afrundingsmekanisme, når råvarer leveres i bestemte dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a7be9-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="a7be9-128">For eksempel et stykke metalrør på 2 meter, der kræves for en færdigvare, og metalrøret gemmes i længder på 4,5 meter.</span><span class="sxs-lookup"><span data-stu-id="a7be9-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="a7be9-129">I dette tilfælde kan afrundingsmekanismen **Måling** bruges til at beregne, hvor mange metalrør, der kræves for at producere et bestemt antal stykker af den færdige vare.</span><span class="sxs-lookup"><span data-stu-id="a7be9-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="a7be9-130">I dette eksempel er feltet **Formel** indstillet til **Højde \* konstant**.</span><span class="sxs-lookup"><span data-stu-id="a7be9-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="a7be9-131">Feltet **Højde** er angivet til **2** for at angive længden af røret, der kræves for færdigvaren.</span><span class="sxs-lookup"><span data-stu-id="a7be9-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="a7be9-132">Feltet **Multiplum** angives til **4,5** for at angive, at røret er plukket i længder på 4,5 meter.</span><span class="sxs-lookup"><span data-stu-id="a7be9-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="a7be9-133">Her er beregningen:</span><span class="sxs-lookup"><span data-stu-id="a7be9-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="a7be9-134">Antal multipla, der kræves til 10 stk. af færdigvaren: 10 ÷ 2 = 5 styk</span><span class="sxs-lookup"><span data-stu-id="a7be9-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="a7be9-135">Samlet forbrug: 4,5 × 5 = 22,5 meter metalrør</span><span class="sxs-lookup"><span data-stu-id="a7be9-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="a7be9-136">Det antages, at 0,5 meter af røret er kasseret for hver fem stykker af rør, der forbruges.</span><span class="sxs-lookup"><span data-stu-id="a7be9-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="a7be9-137">Forbrug</span><span class="sxs-lookup"><span data-stu-id="a7be9-137">Consumption</span></span>

<span data-ttu-id="a7be9-138">Du vælger typisk **Forbrug** som afrundingsmekanisme, når råvaren skal plukkes i hele mængder af en bestemt materialehåndteringsenhed for produktet.</span><span class="sxs-lookup"><span data-stu-id="a7be9-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="a7be9-139">2 quarts maling anvendes f.eks. til at producere et stykke af en færdigvare, og malingen er plukket i bøtter a 25 quarts.</span><span class="sxs-lookup"><span data-stu-id="a7be9-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="a7be9-140">I dette tilfælde kan afrundingsmekanismen **Forbrug** bruges til at afrunde forbrug af bøtter a 25 quarts til hele tal.</span><span class="sxs-lookup"><span data-stu-id="a7be9-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="a7be9-141">Her er beregningen for den mængde af maling, der er påkrævet, hvis der skal produceres 180 stk. færdige varer:</span><span class="sxs-lookup"><span data-stu-id="a7be9-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="a7be9-142">Maling, der skal bruges, uden spild: 180 × 2 = 360 quarts</span><span class="sxs-lookup"><span data-stu-id="a7be9-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="a7be9-143">Antal bøtter: 360 ÷ 25 = 14.4, der afrundes til 15</span><span class="sxs-lookup"><span data-stu-id="a7be9-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="a7be9-144">Maling, der skal bruges, med spild: 15 × 25 = 375 quarts</span><span class="sxs-lookup"><span data-stu-id="a7be9-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="a7be9-145">Trinforbrug</span><span class="sxs-lookup"><span data-stu-id="a7be9-145">Step consumption</span></span>
<span data-ttu-id="a7be9-146">Trinforbrug bruges til at beregne konstant forbrug i antalsintervaller.</span><span class="sxs-lookup"><span data-stu-id="a7be9-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="a7be9-147">Hvis du vælger **Trinforbrug** i feltet **Formel** under fanen **Konfiguration** kan du tilføje oplysninger om trinene under fanen **Trinforbrug**. Den anvendte fastmængde kan konfigureres i intervaller af det producerede antal.</span><span class="sxs-lookup"><span data-stu-id="a7be9-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="a7be9-148">Trinforbrug er f.eks. angivet som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a7be9-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="a7be9-149">Fra serie</span><span class="sxs-lookup"><span data-stu-id="a7be9-149">From series</span></span> | <span data-ttu-id="a7be9-150">Antal</span><span class="sxs-lookup"><span data-stu-id="a7be9-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="a7be9-151">0,00</span><span class="sxs-lookup"><span data-stu-id="a7be9-151">0.00</span></span>        | <span data-ttu-id="a7be9-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="a7be9-152">10.0000</span></span>  |
| <span data-ttu-id="a7be9-153">100,00</span><span class="sxs-lookup"><span data-stu-id="a7be9-153">100.00</span></span>      | <span data-ttu-id="a7be9-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="a7be9-154">20.0000</span></span>  |
| <span data-ttu-id="a7be9-155">200,00</span><span class="sxs-lookup"><span data-stu-id="a7be9-155">200.00</span></span>      | <span data-ttu-id="a7be9-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="a7be9-156">40.0000</span></span>  |

<span data-ttu-id="a7be9-157">Styklistens antal er 1, og produktionsantallet er 110.</span><span class="sxs-lookup"><span data-stu-id="a7be9-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="a7be9-158">Formlen for forbruget er Fra serie (antal) = forbrug.</span><span class="sxs-lookup"><span data-stu-id="a7be9-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="a7be9-159">Da produktionsmængden er 110, falder den ind i "Fra 100-serien."</span><span class="sxs-lookup"><span data-stu-id="a7be9-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="a7be9-160">Antallet er der for 20.</span><span class="sxs-lookup"><span data-stu-id="a7be9-160">Therefore, the quantity is 20.</span></span>




