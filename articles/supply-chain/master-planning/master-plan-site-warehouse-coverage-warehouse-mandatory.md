---
title: Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er obligatorisk.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bc4b54b25edf0f1a47839e8a8253db5a8c595a8f
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="32589-104">Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk</span><span class="sxs-lookup"><span data-stu-id="32589-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="32589-105">I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt.</span><span class="sxs-lookup"><span data-stu-id="32589-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="32589-106">Lagerstedsdimensionen er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="32589-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="32589-107">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="32589-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="32589-108">Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="32589-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="32589-109">Dimensionen for lagerstedet er angivet til tvungen og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="32589-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="32589-110">Dimensionerne for lokation og lagersted er angivet til disponering.</span><span class="sxs-lookup"><span data-stu-id="32589-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="32589-111">Andre dimensioner angives måske også ved behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="32589-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="32589-112">Men de påvirkes ikke af funktionen til flere lokationer.</span><span class="sxs-lookup"><span data-stu-id="32589-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="32589-113">I følgende grafik vises, hvordan varedisponering forløber.</span><span class="sxs-lookup"><span data-stu-id="32589-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="32589-114">De parametre, der henvises til i grafikken, og deres placering er følgende:</span><span class="sxs-lookup"><span data-stu-id="32589-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="32589-115">Lagerstedet er angivet til **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="32589-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="32589-116">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="32589-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="32589-117">I **Overordnet planlægning** oversigtspanelet finder du feltet **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="32589-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="32589-118">Der er defineret varedisponering for varen.</span><span class="sxs-lookup"><span data-stu-id="32589-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="32589-119">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="32589-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="32589-120">Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="32589-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="32589-121">Der er angivet påfyldningsrelationer for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="32589-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="32589-122">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="32589-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="32589-123">Se feltgruppen **Hovedlagersted** i oversigtspanelet **Overordnet planlægning**.</span><span class="sxs-lookup"><span data-stu-id="32589-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="32589-124">Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="32589-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="32589-125">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="32589-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="32589-126">Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="32589-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="32589-127">I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="32589-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Efterspørgselslokalitet og lagerdisponering, lagersted er obligatorisk](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="32589-129">Se også</span><span class="sxs-lookup"><span data-stu-id="32589-129">See also</span></span>
--------

[<span data-ttu-id="32589-130">Varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="32589-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="32589-131">Overordnet planlægning – lokalitetsdisponering, lagersted er obligatorisk</span><span class="sxs-lookup"><span data-stu-id="32589-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="32589-132">Overordnet planlægning – lokalitetsdisponering, lagersted er ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="32589-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="32589-133">Overordnet planlægning – lokations- og lagerdisponering, lagersted er ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="32589-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="32589-134">Overordnet planlægning – sådan bestemmes styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="32589-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




