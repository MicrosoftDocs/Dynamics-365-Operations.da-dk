---
title: Webstedsvælgermodul
description: Dette emne omhandler webstedsvælgermodulet og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055824"
---
# <a name="site-selector-module"></a><span data-ttu-id="e2fa4-103">Webstedsvælgermodul</span><span class="sxs-lookup"><span data-stu-id="e2fa4-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e2fa4-104">Dette emne omhandler webstedsvælgermodulet og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e2fa4-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="e2fa4-105">Overview</span></span>

<span data-ttu-id="e2fa4-106">Når en virksomhed har forskellige websteder på tværs af markeder, områder og landestandarder, skal webstedsbrugere have en nem metode til at skifte mellem websteder og vælge deres foretrukne indkøbssted.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="e2fa4-107">For at tage højde for dette scenario kan brugere gennemse flere websteder ved at bruge modulet til valg af websted.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="e2fa4-108">Modulet til valg af websted skal konfigureres med listen over websteder (markeder, områder eller landestandarder), som brugerne kan gennemse.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="e2fa4-109">Modulet til valg af websted er tilgængeligt i Dynamics 365 Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="e2fa4-110">I følgende illustration vises et eksempel på et modul til valg af websted, der findes i overskriften på en webside.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Eksempel på et modul til valg af websted i en overskrift på en webside](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="e2fa4-112">Egenskaber for webstedsvælgermodulet</span><span class="sxs-lookup"><span data-stu-id="e2fa4-112">Site selector module properties</span></span>

| <span data-ttu-id="e2fa4-113">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="e2fa4-113">Property name</span></span> | <span data-ttu-id="e2fa4-114">Værdi</span><span class="sxs-lookup"><span data-stu-id="e2fa4-114">Value</span></span>                 | <span data-ttu-id="e2fa4-115">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="e2fa4-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="e2fa4-116">Overskrift</span><span class="sxs-lookup"><span data-stu-id="e2fa4-116">Heading</span></span>       | <span data-ttu-id="e2fa4-117">Tekst</span><span class="sxs-lookup"><span data-stu-id="e2fa4-117">Text</span></span>                  | <span data-ttu-id="e2fa4-118">Overskrift for modulet.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-118">The heading for the module.</span></span> |
| <span data-ttu-id="e2fa4-119">Webstedsindstillinger</span><span class="sxs-lookup"><span data-stu-id="e2fa4-119">Site options</span></span>  | <span data-ttu-id="e2fa4-120">Navn, billede, URL-adresse</span><span class="sxs-lookup"><span data-stu-id="e2fa4-120">Name, Image, URL</span></span>      | <span data-ttu-id="e2fa4-121">Denne egenskab specificerer et navn, et link til webstedets startside og et valgfrit billede, der skal vises for hvert websted, der er medtaget i modulet.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="e2fa4-122">Billedet kan være et flag eller en vis repræsentation af et marked, område eller en landestandard.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="e2fa4-123">Føje et webstedsvælgermodul til en side</span><span class="sxs-lookup"><span data-stu-id="e2fa4-123">Add a site selector module to a page</span></span>

<span data-ttu-id="e2fa4-124">Webstedsvælgermodulet kan føjes til [overskriftsmodulet](author-header-module.md) under pladsen for webstedsvælgeren.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="e2fa4-125">Når det er tilføjet, kan du definere moduloverskriften og indstillinger for webstedet.</span><span class="sxs-lookup"><span data-stu-id="e2fa4-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2fa4-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e2fa4-126">Additional resources</span></span>

[<span data-ttu-id="e2fa4-127">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="e2fa4-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e2fa4-128">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="e2fa4-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e2fa4-129">Brødkrummemodul</span><span class="sxs-lookup"><span data-stu-id="e2fa4-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="e2fa4-130">Navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="e2fa4-130">Navigation menu module</span></span>](nav-menu-module.md)
