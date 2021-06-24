---
title: Varedisponering for lokations- og lagerdisponering, lagersted er ikke obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt. Lagerstedsdimensionen er ikke obligatorisk.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6b9814a0a5a069d945c7888da17348ecfe4d4a7
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187524"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="291b0-104">Varedisponering for lokations- og lagerdisponering, lagersted er ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="291b0-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="291b0-105">I dette emne beskrives det, hvordan en vare med lokation og lagersted som disponeringsdimensioner bliver planlagt.</span><span class="sxs-lookup"><span data-stu-id="291b0-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="291b0-106">Lagerstedsdimensionen er ikke obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="291b0-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="291b0-107">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="291b0-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="291b0-108">Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="291b0-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="291b0-109">Denne indstilling kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="291b0-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="291b0-110">Lagerstedsdimensionen er ikke angivet til obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="291b0-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="291b0-111">Lagerstedet er måske kendt, men bruges ikke i beregningen i varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="291b0-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="291b0-112">Lokations- og lagerstedsdimensioner angives ved behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="291b0-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="291b0-113">Andre dimensioner angives måske også ved behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="291b0-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="291b0-114">Men de påvirkes ikke af funktionen til flere lokationer.</span><span class="sxs-lookup"><span data-stu-id="291b0-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="291b0-115">I følgende grafik vises, hvordan varedisponering forløber.</span><span class="sxs-lookup"><span data-stu-id="291b0-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="291b0-116">De parametre, der henvises til i grafikken, og deres placering er følgende:</span><span class="sxs-lookup"><span data-stu-id="291b0-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="291b0-117">Lagerstedet er angivet til Manuel.</span><span class="sxs-lookup"><span data-stu-id="291b0-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="291b0-118">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="291b0-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="291b0-119">I **Overordnet planlægning** oversigtspanelet finder du feltet **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="291b0-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="291b0-120">Der er defineret varedisponering for varen.</span><span class="sxs-lookup"><span data-stu-id="291b0-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="291b0-121">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="291b0-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="291b0-122">Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="291b0-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="291b0-123">Der er angivet påfyldningsrelationer for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="291b0-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="291b0-124">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="291b0-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="291b0-125">Se feltgruppen **Hovedlagersted** i oversigtspanelet **Overordnet planlægning**.</span><span class="sxs-lookup"><span data-stu-id="291b0-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="291b0-126">Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="291b0-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="291b0-127">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="291b0-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="291b0-128">Vælg varen, og derefter skal du i Handlingsrude under fanen **Plan** klikke på **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="291b0-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="291b0-129">I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="291b0-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Efterspørgsel efter lokalitet og lagersted, lagersted er ikke obligatorisk](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a><span data-ttu-id="291b0-131">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="291b0-131">Additional resources</span></span>

[<span data-ttu-id="291b0-132">Oversigt over varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="291b0-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="291b0-133">Varedisponering for lokalitetsdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="291b0-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="291b0-134">Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="291b0-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="291b0-135">Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="291b0-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="291b0-136">Bestemme styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="291b0-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]