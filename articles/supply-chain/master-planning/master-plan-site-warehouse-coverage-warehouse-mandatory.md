---
title: Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er obligatorisk.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92160b45590245e2b1caab6732d1b0aaeaabd208
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975914"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="b3f9d-104">Varedisponering for lokations- og lagerdisponering, lagersted er obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3f9d-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3f9d-105">I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="b3f9d-106">Lagerstedsdimensionen er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="b3f9d-107">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="b3f9d-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b3f9d-108">Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b3f9d-109">Dimensionen for lagerstedet er angivet til tvungen og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b3f9d-110">Dimensionerne for lokation og lagersted er angivet til disponering.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="b3f9d-111">Andre dimensioner angives måske også ved behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="b3f9d-112">Men de påvirkes ikke af funktionen til flere lokationer.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="b3f9d-113">I følgende grafik vises, hvordan varedisponering forløber.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b3f9d-114">De parametre, der henvises til i grafikken, og deres placering er følgende:</span><span class="sxs-lookup"><span data-stu-id="b3f9d-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b3f9d-115">Lagerstedet er angivet til **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="b3f9d-116">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b3f9d-117">I **Overordnet planlægning** oversigtspanelet finder du feltet **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="b3f9d-118">Der er defineret varedisponering for varen.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="b3f9d-119">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b3f9d-120">Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="b3f9d-121">Der er angivet påfyldningsrelationer for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b3f9d-122">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b3f9d-123">Se feltgruppen **Hovedlagersted** i oversigtspanelet **Overordnet planlægning**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b3f9d-124">Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="b3f9d-125">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b3f9d-126">Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="b3f9d-127">I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="b3f9d-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Efterspørgselslokalitet og lagerdisponering, lagersted er obligatorisk](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="b3f9d-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b3f9d-129">Additional resources</span></span>
--------

[<span data-ttu-id="b3f9d-130">Oversigt over varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="b3f9d-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b3f9d-131">Varedisponering for lokalitetsdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="b3f9d-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b3f9d-132">Varedisponering for lokalitetsdisponering, lagersted ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3f9d-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b3f9d-133">Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3f9d-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b3f9d-134">Bestemme styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="b3f9d-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



