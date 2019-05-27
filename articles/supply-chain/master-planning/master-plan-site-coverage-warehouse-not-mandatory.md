---
title: Varedisponering for lokalitetsdisponering, lagersted er ikke obligatorisk
description: I dette emne beskrives det, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9475a7fbe40d7feb60c23e0d7164222469dffa75
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552316"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="27ffe-103">Varedisponering for lokalitetsdisponering, lagersted er ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="27ffe-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27ffe-104">I dette emne beskrives det, hvordan en vare med lokationsdimensionen indstillet til disponering bliver planlagt.</span><span class="sxs-lookup"><span data-stu-id="27ffe-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="27ffe-105">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="27ffe-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="27ffe-106">Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="27ffe-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="27ffe-107">Lagerstedsdimensionen er ikke angivet til obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="27ffe-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="27ffe-108">Lagerstedet er måske kendt, men bruges ikke i beregningen i varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="27ffe-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="27ffe-109">Dimensionen for lokationen er angivet til disponering.</span><span class="sxs-lookup"><span data-stu-id="27ffe-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="27ffe-110">Dimensionen for lagerstedet er ikke angivet til disponering.</span><span class="sxs-lookup"><span data-stu-id="27ffe-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="27ffe-111">Udbud og efterspørgsel aggregeres derfor efter lokation og måske også andre disponerede dimensioner.</span><span class="sxs-lookup"><span data-stu-id="27ffe-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="27ffe-112">I følgende grafik vises, hvordan varedisponering forløber.</span><span class="sxs-lookup"><span data-stu-id="27ffe-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="27ffe-113">De parametre, der henvises til i grafikken, og deres placering er følgende:</span><span class="sxs-lookup"><span data-stu-id="27ffe-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="27ffe-114">Der er defineret varedisponering for varen.</span><span class="sxs-lookup"><span data-stu-id="27ffe-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="27ffe-115">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="27ffe-116">Vælg varen, og klik derefter på **Plan &gt; Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="27ffe-117">Der er angivet påfyldningsrelationer for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="27ffe-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="27ffe-118">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="27ffe-119">Se feltgruppen **Hovedlagersted** under fanen **Overordnet planlægning**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="27ffe-120">Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="27ffe-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="27ffe-121">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="27ffe-122">Vælg varen, og klik derefter på **Plan &gt; Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="27ffe-123">I formen **Standardindstillinger for ordre** kan du se feltet **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="27ffe-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Efterspørgsel efter lokalitetsdisponering, lagersted er ikke obligatorisk](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="27ffe-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="27ffe-125">Additional resources</span></span>
--------

[<span data-ttu-id="27ffe-126">Varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="27ffe-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="27ffe-127">Overordnet planlægning – lokalitetsdisponering, lagersted er obligatorisk</span><span class="sxs-lookup"><span data-stu-id="27ffe-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="27ffe-128">Overordnet planlægning – lokations- og lagerdisponering, lagersted er ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="27ffe-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="27ffe-129">Overordnet planlægning – lokations- og lagerdisponering, lagersted er obligatorisk</span><span class="sxs-lookup"><span data-stu-id="27ffe-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="27ffe-130">Varedisponering – Sådan bestemmes styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="27ffe-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



