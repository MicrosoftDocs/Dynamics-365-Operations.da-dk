---
title: Forkalkulation af produktionsordre
description: Denne artikel indeholder oplysninger om produktionsforkalkulation. Forkalkulation af produktion giver dig oplysninger om de budgetterede omkostninger til materiale- og kapacitetsforbrug til fremstilling af en vare i det planlagte produktionsordreantal.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 881ba7058a22a98d85730fa1f0aa6c38af7d248c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208153"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="cdc03-104">Forkalkulation af produktionsordre</span><span class="sxs-lookup"><span data-stu-id="cdc03-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdc03-105">Denne artikel indeholder oplysninger om produktionsforkalkulation.</span><span class="sxs-lookup"><span data-stu-id="cdc03-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="cdc03-106">Forkalkulation af produktion giver dig oplysninger om de budgetterede omkostninger til materiale- og kapacitetsforbrug til fremstilling af en vare i det planlagte produktionsordreantal.</span><span class="sxs-lookup"><span data-stu-id="cdc03-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="cdc03-107">Når du opretter en produktionsordre, skal du forkalkulere produktionsomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="cdc03-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="cdc03-108">Formålet er at beregne vare- og ruteforbruget i produktionsprocessen, fordi disse forkalkulationer danner grundlaget for efterfølgende planlægnings- og produktionsprocesser.</span><span class="sxs-lookup"><span data-stu-id="cdc03-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="cdc03-109">Forkalkulation af produktionsomkostninger</span><span class="sxs-lookup"><span data-stu-id="cdc03-109">Production cost estimation</span></span>
<span data-ttu-id="cdc03-110">Forkalkulationer af produktionsomkostninger er baseret på følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="cdc03-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="cdc03-111">Mængden i produktionsordren</span><span class="sxs-lookup"><span data-stu-id="cdc03-111">The quantity on the production order</span></span>
-   <span data-ttu-id="cdc03-112">Komponenterne på produktionsstyklisterne</span><span class="sxs-lookup"><span data-stu-id="cdc03-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="cdc03-113">Ruteplanlægningsoperationer i produktionsruten</span><span class="sxs-lookup"><span data-stu-id="cdc03-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="cdc03-114">De indirekte omkostninger, der gælder for komponenter og operationer</span><span class="sxs-lookup"><span data-stu-id="cdc03-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="cdc03-115">Aktive omkostningsdata pr. beregningsdatoen</span><span class="sxs-lookup"><span data-stu-id="cdc03-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="cdc03-116">Hvis der er en fantomlinjevare på produktionsstyklisterne, afspejler beregningerne fantomets komponenter og ruteoperationer.</span><span class="sxs-lookup"><span data-stu-id="cdc03-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="cdc03-117">Du kan bruge forkalkuleringsopgaven til at genberegne forkalkulerede omkostninger, så de afspejler opdaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="cdc03-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="cdc03-118">De opdaterede oplysninger kan f.eks. være ændringer i mængden på produktionsordren, komponenterne på produktionsstyklisterne, ruteoperationerne i produktionsruten, de indirekte omkostninger, der gælder for disse komponenter og operationer, eller de aktive omkostningsdata pr. beregningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="cdc03-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="cdc03-119">I beregningen af forkalkulerede omkostninger foreslås også en salgspris for produktionsvaren baseret på en beregning af omkostninger plus avance.</span><span class="sxs-lookup"><span data-stu-id="cdc03-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="cdc03-120">Beregningen af forkalkulerede omkostninger kan også gælde for referenceordrer, der afspejler andre produktionsordrer, som er knyttet til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="cdc03-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="cdc03-121">Se de forkalkulerede omkostninger</span><span class="sxs-lookup"><span data-stu-id="cdc03-121">View the estimated costs</span></span>
<span data-ttu-id="cdc03-122">Når du kører forkalkulationen, kan du se resultatet på siden **Prisberegning**.</span><span class="sxs-lookup"><span data-stu-id="cdc03-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="cdc03-123">Forkalkulationen beregner følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="cdc03-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="cdc03-124">**Produktionsomkostninger** – Produktionsomkostninger er den øverste linje i forkalkulationen.</span><span class="sxs-lookup"><span data-stu-id="cdc03-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="cdc03-125">Den viser de samlede omkostninger til kørslen af produktionsordren og den samlede salgspris for produktionen.</span><span class="sxs-lookup"><span data-stu-id="cdc03-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="cdc03-126">Det er summen af alle omkostningslinjer i forkalkulationen.</span><span class="sxs-lookup"><span data-stu-id="cdc03-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="cdc03-127">**Rute-eller ressourceomkostninger** – Rute-eller ressourceomkostninger er omkostninger for produktionsoperationerne.</span><span class="sxs-lookup"><span data-stu-id="cdc03-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="cdc03-128">De omfatter omkostningen for elementer som opstillingstid, operationstid og indirekte omkostninger.</span><span class="sxs-lookup"><span data-stu-id="cdc03-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="cdc03-129">**Materialeomkostninger** – Materialeomkostninger er omkostningerne til og priserne på de styklistekomponenter, der skal bruges til at producere varen.</span><span class="sxs-lookup"><span data-stu-id="cdc03-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="cdc03-130">De er fastlagt og indsat i systemet tidligere.</span><span class="sxs-lookup"><span data-stu-id="cdc03-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="cdc03-131">Andre formål med forkalkulationer</span><span class="sxs-lookup"><span data-stu-id="cdc03-131">Other uses of cost estimation</span></span>
<span data-ttu-id="cdc03-132">En forkalkulation giver dig også følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="cdc03-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="cdc03-133">Brugbare pristilbud</span><span class="sxs-lookup"><span data-stu-id="cdc03-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="cdc03-134">Estimater af rentabiliteten af ordren</span><span class="sxs-lookup"><span data-stu-id="cdc03-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="cdc03-135">Estimater af råvareforbruget</span><span class="sxs-lookup"><span data-stu-id="cdc03-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="cdc03-136">Sammenligninger med omkostningsoplysninger fra tidligere produktioner</span><span class="sxs-lookup"><span data-stu-id="cdc03-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="cdc03-137">Budgetterings- og prognoseoplysninger</span><span class="sxs-lookup"><span data-stu-id="cdc03-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="cdc03-138">Forkalkulationer af den produktionsstørrelse, der kræves for at opretholde en bestemt omkostning.</span><span class="sxs-lookup"><span data-stu-id="cdc03-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]