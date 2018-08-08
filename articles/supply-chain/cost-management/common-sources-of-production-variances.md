---
title: Almindelige kilder til produktionsafvigelser
description: I denne artikel beskrives forskellige kilder, der er typiske for de enkelte typer afvigelser i produktion.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 50f8cd7904e1d32175edd321fbd6533e985fb324
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="common-sources-of-production-variances"></a><span data-ttu-id="40f69-103">Almindelige kilder til produktionsafvigelser</span><span class="sxs-lookup"><span data-stu-id="40f69-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40f69-104">I denne artikel beskrives forskellige kilder, der er typiske for de enkelte typer afvigelser i produktion.</span><span class="sxs-lookup"><span data-stu-id="40f69-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="40f69-105">Her er nogle typiske kilder til en afvigelse i **partistørrelse**:</span><span class="sxs-lookup"><span data-stu-id="40f69-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="40f69-106">Antallet af gode varer for en produktionsordre er forskelligt fra den beregningsmængde, der bruges i standardomkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="40f69-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="40f69-107">Antallet danner grundlag for amortisering af omkostninger.</span><span class="sxs-lookup"><span data-stu-id="40f69-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="40f69-108">Værdien af konstante omkostninger i produktionsordren er forskellig fra de konstante omkostninger, der bruges til beregning af standardomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="40f69-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="40f69-109">De konstante omkostninger i produktionsordren kan være forskellige af flere årsager.</span><span class="sxs-lookup"><span data-stu-id="40f69-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="40f69-110">For eksempel kan de konstante omkostninger afspejle følgende faktorer:</span><span class="sxs-lookup"><span data-stu-id="40f69-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="40f69-111">Manuelle ændringer af produktionsstyklisten eller ruten</span><span class="sxs-lookup"><span data-stu-id="40f69-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="40f69-112">Valget af en anden styklisteversion eller ruteversion ved oprettelse af produktionsordren</span><span class="sxs-lookup"><span data-stu-id="40f69-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="40f69-113">Planlagte engineering-ændringer i styklisteversionen eller ruteversionen, der er tildelt varen</span><span class="sxs-lookup"><span data-stu-id="40f69-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="40f69-114">Her er nogle typiske kilder til en afvigelse i **produktionspris**:</span><span class="sxs-lookup"><span data-stu-id="40f69-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="40f69-115">Omkostningsarten (og prisen for omkostningsarten) for det rapporterede forbrug af en ruteoperation er forskellig fra den omkostningsart, der bruges i standardomkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="40f69-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="40f69-116">Den aktive omkostning for prisen for omkostningsarten er forskellig fra den pris for omkostningsarten, der bruges i standardomkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="40f69-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="40f69-117">Her er nogle typiske kilder til en afvigelse i **produktionsantal**:</span><span class="sxs-lookup"><span data-stu-id="40f69-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="40f69-118">For stor afgang eller for lille afgang af en materialekomponent.</span><span class="sxs-lookup"><span data-stu-id="40f69-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="40f69-119">For lang eller for kort rapporteret tid for en ruteoperation.</span><span class="sxs-lookup"><span data-stu-id="40f69-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="40f69-120">Du modtager for stort eller lille antal af den overordnede vare i forhold til ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="40f69-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="40f69-121">Men du udsteder komponenter og rapportoperationer helt, baseret på ordreantallet for produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="40f69-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="40f69-122">Her er nogle typiske kilder til en afvigelse i **produktionserstatning**:</span><span class="sxs-lookup"><span data-stu-id="40f69-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="40f69-123">Afgang af en materialekomponent, der ikke er del af produktionsstyklisten.</span><span class="sxs-lookup"><span data-stu-id="40f69-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="40f69-124">Manuel tilføjelse af en komponent på produktionsstyklisten og rapportering af komponenten som Forbrugt.</span><span class="sxs-lookup"><span data-stu-id="40f69-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="40f69-125">Rapportering af en vare som forbrugt uden, at den manuelt føjes til produktionsstyklisten.</span><span class="sxs-lookup"><span data-stu-id="40f69-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="40f69-126">Manuel tilføjelse af en operation til produktionsruten og rapportering af operationen som Forbrugt.</span><span class="sxs-lookup"><span data-stu-id="40f69-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="40f69-127">Valg af en anden styklisteversion ved oprettelse af produktionsordren, eller hvis styklisteversionen er forskellig fra den, der bruges i standardomkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="40f69-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="40f69-128">Valg af en anden ruteversion ved oprettelse af produktionsordren, eller hvis ruteversionen er forskellig fra den, der bruges i standardomkostningsberegningen.</span><span class="sxs-lookup"><span data-stu-id="40f69-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>





