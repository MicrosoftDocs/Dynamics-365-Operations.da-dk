---
title: Anvend filtre på en plan
description: I dette emne beskrives det, hvordan du kan anvende filtre på en plan, når funktionen Planlægningsoptimering anvendes.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b5262cc5dc72ffcc50770cf5a2e2dda216d7ff8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212096"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="84671-103">Anvend filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="84671-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84671-104">Når funktionen Planlægningsoptimering bruges, kan du anvende et filter på en plan.</span><span class="sxs-lookup"><span data-stu-id="84671-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="84671-105">**Planfilteret** anvendes altid under en varedisponeringskørsel.</span><span class="sxs-lookup"><span data-stu-id="84671-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="84671-106">Et **Planfilter** er nyttigt, når du vil begrænse en plan til en bestemt varegruppe og sikre dig, at ingen andre varer medtages som en del af den afsluttende varedisponering.</span><span class="sxs-lookup"><span data-stu-id="84671-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="84671-107">Hvis der anvendes et **Planfilter**, og der også anvendes et kørselsfilter under varedisponeringskørslen, er det kun sammenfaldet mellem de to filtre, der medtages i planlægningskørslen.</span><span class="sxs-lookup"><span data-stu-id="84671-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="84671-108">Du kan få adgang til **Planfiltret** fra **Behovsplaner**, når der bruges Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="84671-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="84671-109">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="84671-109">Example scenario</span></span>

<span data-ttu-id="84671-110">Der oprettes et planfilter, der omfatter varer A, B og C. Varedisponering kører derefter i samme plan, men der anvendes forskellige kørselsfiltre:</span><span class="sxs-lookup"><span data-stu-id="84671-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="84671-111">**Kørselsfilter, der indeholder vare D:** Der er ikke planlagt nogen varer, fordi der ikke er noget sammenfald mellem planfilteret og kørselsfilteret.</span><span class="sxs-lookup"><span data-stu-id="84671-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="84671-112">**Kørselsfilter, der omfatter vare A og D:** Kun vare A indgår i planlægningskørslen, fordi vare D ikke indgår i planfilteret.</span><span class="sxs-lookup"><span data-stu-id="84671-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="84671-113">**Kørselsfilter, der omfatter vare B:** Kun vare B indgår i planlægningskørslen, og det forrige planlagte out for vare A bibeholdes.</span><span class="sxs-lookup"><span data-stu-id="84671-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="84671-114">**Kørselsfilter, der omfatter alle varer (tomt filter):** Varerne A, B og C medtages i planlægningskørslen, og den forrige output for planlægning for vare A og B overskrives.</span><span class="sxs-lookup"><span data-stu-id="84671-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="84671-115">Du bør undgå at angive et planfilter på den plan, der er valgt som **Aktuel dynamisk behovsplan** på siden **Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="84671-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="84671-116">Ellers vil funktionaliteten for den dynamiske behovsplan begrænses til de filtrerede elementer.</span><span class="sxs-lookup"><span data-stu-id="84671-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="84671-117">Hvis nettobehovet f.eks. opdateres for en vare, der ikke er en del af planfilteret, vil der ikke blive genereret et resultat.</span><span class="sxs-lookup"><span data-stu-id="84671-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="84671-118">Tilknyttede ressourcer</span><span class="sxs-lookup"><span data-stu-id="84671-118">Related resources</span></span>

[<span data-ttu-id="84671-119">Oversigt over Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="84671-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="84671-120">Introduktion til Planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="84671-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="84671-121">Analyse af om Planlægningsoptimering passer til</span><span class="sxs-lookup"><span data-stu-id="84671-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="84671-122">Få vist planhistorik og planlægningslogs</span><span class="sxs-lookup"><span data-stu-id="84671-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="84671-123">Annullere et planlægningsjob</span><span class="sxs-lookup"><span data-stu-id="84671-123">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]