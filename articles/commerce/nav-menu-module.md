---
title: Navigationsmenumodul
description: Dette emne omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817868"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="6d1c8-103">Navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="6d1c8-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6d1c8-104">Dette emne omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6d1c8-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="6d1c8-105">Overview</span></span>

<span data-ttu-id="6d1c8-106">Det primære formål med navigationsmenumoduler er at give brugerne af webstedet mulighed for at gennemse produkter og websider i henhold til det kanalnavigationshierarki, der er defineret i Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="6d1c8-107">Elementer, der er konfigureret i et navigationsmenumodul, vises som navigation i webstedets sidehoved.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="6d1c8-108">Moduler til navigationsmenuer understøtter også statiske menupunkter med links til andre sider på et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="6d1c8-109">Modulet til genvejsmenuen kan føjes til sidens sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="6d1c8-110">I Fabrikam-temaet viser navigationsmenuen som standard to niveauer.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="6d1c8-111">I Starter-temaet viser navigationsmenuen som standard tre niveauer.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="6d1c8-112">Hvis du vil ændre antallet af niveauer, skal du bruge en visningsudvidelse på temaet.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="6d1c8-113">I følgende illustration vises et eksempel på en navigationsmenu for Fabrikam-webstedet med to niveauer af kategorihierarki og nogle statiske menupunkter.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="6d1c8-114">![Eksempel på et navigationsmenumodul](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="6d1c8-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="6d1c8-115">Egenskaber for navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="6d1c8-115">Navigation menu module properties</span></span>

| <span data-ttu-id="6d1c8-116">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="6d1c8-116">Property name</span></span>             | <span data-ttu-id="6d1c8-117">Værdi</span><span class="sxs-lookup"><span data-stu-id="6d1c8-117">Value</span></span>                 | <span data-ttu-id="6d1c8-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6d1c8-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6d1c8-119">Kildetekst</span><span class="sxs-lookup"><span data-stu-id="6d1c8-119">Source</span></span>                  | <span data-ttu-id="6d1c8-120">**Detail**, **Manuel oprettelse**, **Detail og manuel oprettelse**</span><span class="sxs-lookup"><span data-stu-id="6d1c8-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="6d1c8-121">**Detail**-værdien giver mulighed for at få vist kanalnavigationshierarkiet fra Commerce Headquarters i navigationsmenuen.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="6d1c8-122">Værdien af **Manuel oprettelse** tillader, at statiske menupunkter overvåges.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="6d1c8-123">Værdien af **Detail og manuel oprettelse** tillader en blanding af begge dele.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="6d1c8-124">Vise kategoribilleder</span><span class="sxs-lookup"><span data-stu-id="6d1c8-124">Show category images</span></span> | <span data-ttu-id="6d1c8-125">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="6d1c8-125">**True** or **False**</span></span>    | <span data-ttu-id="6d1c8-126">Når denne egenskab er aktiveret, viser kategoribilleder i den navigationsmenu, som er defineret i Commerce Headquarters for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="6d1c8-127">Tilføjet i Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="6d1c8-128">Statisk menupunkt</span><span class="sxs-lookup"><span data-stu-id="6d1c8-128">Static menu item</span></span>| <span data-ttu-id="6d1c8-129">Matrix af værdier</span><span class="sxs-lookup"><span data-stu-id="6d1c8-129">Array of values</span></span>| <span data-ttu-id="6d1c8-130">Statiske menupunkter, der knytter et menupunkts navn til et link til en statisk webside.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="6d1c8-131">Du kan oprette menupunkter under andre menupunkter.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="6d1c8-132">Som standard vises statiske menuer på rodniveau, og de føjes til kanalnavigationshierarkiet, hvis det findes.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="6d1c8-133">I følgende illustration vises et eksempel på et kategoribillede, der vises i navigationsmenuen for Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="6d1c8-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="6d1c8-134">![Eksempel på et navigationsmenumodul med kategoribilleder](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="6d1c8-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="6d1c8-135">Tilføje et navigationsmenumodul i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="6d1c8-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="6d1c8-136">Du kan finde flere oplysninger om, hvordan du føjer et navigationsmenumodul til et sidehovedmodul, under [Sidehovedmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="6d1c8-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d1c8-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6d1c8-137">Additional resources</span></span>

[<span data-ttu-id="6d1c8-138">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="6d1c8-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6d1c8-139">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="6d1c8-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6d1c8-140">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="6d1c8-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="6d1c8-141">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="6d1c8-141">Header module</span></span>](author-header-module.md)
