---
title: Analyse af om Planlægningsoptimering passer til
description: Dette emne beskriver, hvordan du kan kontrollere den aktuelle opsætning og de nuværende data i forhold til funktionerne i funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208748"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="67b78-103">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="67b78-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67b78-104">Hvis du vil se, hvordan din aktuelle opsætning og data er kompatibel med funktionen Planlægningsoptimering, skal du gå til **Varedisponering** \> **Opsætning** \> **Analyse af om Planlægninsoptimering passer til** og dernæst vælge **Kør analyse**.</span><span class="sxs-lookup"><span data-stu-id="67b78-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="67b78-105">Hvis analysen finder nogen uoverensstemmelser, vises de på samme side.</span><span class="sxs-lookup"><span data-stu-id="67b78-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="67b78-106">(Det kan tage et par minutter at køre analysen).</span><span class="sxs-lookup"><span data-stu-id="67b78-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="67b78-107">Hvis der findes uoverensstemmelser, kan du stadig bruge Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="67b78-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="67b78-108">Resultaterne af tilpasningsanalysen viser kun de steder, hvor planlægningstjenesten ikke kan overholde din aktuelle opsætning.</span><span class="sxs-lookup"><span data-stu-id="67b78-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="67b78-109">Det vil sige, at det vises de steder, hvor nogle processer muligvis bliver ignoreret eller ikke understøttes.</span><span class="sxs-lookup"><span data-stu-id="67b78-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="67b78-110">Analyseresultater: eksempel 1</span><span class="sxs-lookup"><span data-stu-id="67b78-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="67b78-111">**Funktion:** Produktion</span><span class="sxs-lookup"><span data-stu-id="67b78-111">**Feature:** Production</span></span>
- <span data-ttu-id="67b78-112">**Afgang:** Varer med styklisteniveau, der er større end nul: 56</span><span class="sxs-lookup"><span data-stu-id="67b78-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="67b78-113">**Forklaring:** Tilpasningsanalysen fandt 56 varer, der indeholder en styklisteopsætning til produktion.</span><span class="sxs-lookup"><span data-stu-id="67b78-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="67b78-114">Da den aktuelle version af funktionen Planlægningsoptimering ikke understøtter produktion, vil Planlægningsoptimering oprette indkøbsordreforslag i stedet for produktionsordreforslag.</span><span class="sxs-lookup"><span data-stu-id="67b78-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="67b78-115">Der vises også en advarsel om, at de berørte varer vises.</span><span class="sxs-lookup"><span data-stu-id="67b78-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="67b78-116">Analyseresultater: eksempel 2</span><span class="sxs-lookup"><span data-stu-id="67b78-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="67b78-117">**Funktion:** Handlinger</span><span class="sxs-lookup"><span data-stu-id="67b78-117">**Feature:** Actions</span></span>
- <span data-ttu-id="67b78-118">**Afgang:** Disponeringsgrupper med aktiveret handlingsberegning: 6</span><span class="sxs-lookup"><span data-stu-id="67b78-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="67b78-119">**Forklaring:** Tilpasningsanalysen fandt seks disponeringsgrupper, hvor handlingsberegningen er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="67b78-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="67b78-120">Da den aktuelle version af Planlægningsoptimerings ikke understøtter handlinger, vil der ikke blive genereret handlinger ved varedisponering.</span><span class="sxs-lookup"><span data-stu-id="67b78-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="67b78-121">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="67b78-121">Related resources</span></span>

[<span data-ttu-id="67b78-122">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="67b78-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="67b78-123">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="67b78-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="67b78-124">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="67b78-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="67b78-125">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="67b78-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="67b78-126">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="67b78-126">Cancel a planning job</span></span>](cancel-planning-job.md)
