---
title: Varedisponering for lokalitetsdisponering, obligatorisk lagersted
description: I dette emne beskrives det, hvordan en vare med lokationen som disponeringsdimension bliver planlagt. Lagerstedet er en obligatorisk dimension.
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a6128900d403c05af611b7636d5768b1c6a0b2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213693"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="b3690-104">Varedisponering for lokalitetsdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="b3690-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3690-105">I dette emne beskrives det, hvordan en vare med lokationen som disponeringsdimension bliver planlagt.</span><span class="sxs-lookup"><span data-stu-id="b3690-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="b3690-106">Lagerstedet er en obligatorisk dimension.</span><span class="sxs-lookup"><span data-stu-id="b3690-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="b3690-107">Dette behovsplanlægningsscenario omfatter følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="b3690-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b3690-108">Lokationsdimensionen er angivet til obligatorisk og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="b3690-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="b3690-109">Denne indstilling kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="b3690-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="b3690-110">Dimensionen for lagerstedet er angivet til tvungen og skal angives på behovsposteringen.</span><span class="sxs-lookup"><span data-stu-id="b3690-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b3690-111">Dimensionen for lokationen er angivet til disponering.</span><span class="sxs-lookup"><span data-stu-id="b3690-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="b3690-112">Der kan også angives andre dimensioner for disponering.</span><span class="sxs-lookup"><span data-stu-id="b3690-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="b3690-113">De påvirkes dog ikke af funktionen til brug af flere lokationer.</span><span class="sxs-lookup"><span data-stu-id="b3690-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="b3690-114">Dimensionen for lagerstedet er ikke angivet til disponering.</span><span class="sxs-lookup"><span data-stu-id="b3690-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="b3690-115">Udbud og efterspørgsel aggregeres derfor efter lokation og måske også andre disponerede dimensioner.</span><span class="sxs-lookup"><span data-stu-id="b3690-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="b3690-116">I følgende grafik vises, hvordan varedisponering forløber.</span><span class="sxs-lookup"><span data-stu-id="b3690-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b3690-117">De parametre, der henvises til i grafikken, og deres placering er følgende:</span><span class="sxs-lookup"><span data-stu-id="b3690-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b3690-118">Der er defineret varedisponering for varen.</span><span class="sxs-lookup"><span data-stu-id="b3690-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="b3690-119">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b3690-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b3690-120">Vælg varen, og klik derefter på **Plan &gt; Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="b3690-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="b3690-121">Der er angivet påfyldningsrelationer for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b3690-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b3690-122">Klik på **Lagerstyring &gt; Opsætning &gt; Lageropdeling &gt; Lagersteder**.</span><span class="sxs-lookup"><span data-stu-id="b3690-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b3690-123">Se feltgruppen **Hovedlagersted** under fanen **Overordnet planlægning**.</span><span class="sxs-lookup"><span data-stu-id="b3690-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b3690-124">Standardordretypen er indstillet til Produktion, Indkøbsordre eller Kanban.</span><span class="sxs-lookup"><span data-stu-id="b3690-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="b3690-125">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b3690-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b3690-126">Vælg varen, og klik derefter på **Plan &gt; Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="b3690-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="b3690-127">I formen **Standardindstillinger for ordre** kan du se **Standardordretype**.</span><span class="sxs-lookup"><span data-stu-id="b3690-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Efterspørgsel efter lokalitetsdisponering, lagersted obligatorisk](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="b3690-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b3690-129">Additional resources</span></span>
--------

[<span data-ttu-id="b3690-130">Oversigt over varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="b3690-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b3690-131">Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="b3690-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b3690-132">Varedisponering for lokalitetsdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="b3690-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b3690-133">Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b3690-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b3690-134">Bestemme styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="b3690-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



