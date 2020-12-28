---
title: Navigationsmenumodul
description: Dette emne omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4411216"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="9d93e-103">Navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="9d93e-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d93e-104">Dette emne omhandler navigationsmenumoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d93e-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9d93e-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="9d93e-105">Overview</span></span>

<span data-ttu-id="9d93e-106">Det primære formål med navigationsmenumoduler er at give brugerne af webstedet mulighed for at gennemse produkter og websider i henhold til det kanalnavigationshierarki, der er defineret i Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9d93e-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="9d93e-107">Elementer, der er konfigureret i et navigationsmenumodul, vises som navigation i webstedets sidehoved.</span><span class="sxs-lookup"><span data-stu-id="9d93e-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="9d93e-108">Moduler til navigationsmenuer understøtter også statiske menupunkter med links til andre sider på et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="9d93e-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="9d93e-109">Modulet til genvejsmenuen kan føjes til sidens sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="9d93e-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="9d93e-110">I Fabrikam-temaet viser navigationsmenuen som standard to niveauer.</span><span class="sxs-lookup"><span data-stu-id="9d93e-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="9d93e-111">I Starter-temaet viser navigationsmenuen som standard tre niveauer.</span><span class="sxs-lookup"><span data-stu-id="9d93e-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="9d93e-112">Hvis du vil ændre antallet af niveauer, skal du bruge en visningsudvidelse på temaet.</span><span class="sxs-lookup"><span data-stu-id="9d93e-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="9d93e-113">I følgende illustration vises et eksempel på en navigationsmenu for Fabrikam-webstedet med to niveauer af kategorihierarki og nogle statiske menupunkter.</span><span class="sxs-lookup"><span data-stu-id="9d93e-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="9d93e-114">![Eksempel på et navigationsmenumodul](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="9d93e-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="9d93e-115">Egenskaber for navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="9d93e-115">Navigation menu module properties</span></span>

| <span data-ttu-id="9d93e-116">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="9d93e-116">Property name</span></span>             | <span data-ttu-id="9d93e-117">Værdi</span><span class="sxs-lookup"><span data-stu-id="9d93e-117">Value</span></span>                 | <span data-ttu-id="9d93e-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9d93e-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="9d93e-119">Kildetekst</span><span class="sxs-lookup"><span data-stu-id="9d93e-119">Source</span></span>                  | <span data-ttu-id="9d93e-120">**Detail**, **Manuel oprettelse**, **Detail og manuel oprettelse**</span><span class="sxs-lookup"><span data-stu-id="9d93e-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="9d93e-121">**Detail**-værdien giver mulighed for at få vist kanalnavigationshierarkiet fra Commerce Headquarters i navigationsmenuen.</span><span class="sxs-lookup"><span data-stu-id="9d93e-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="9d93e-122">Værdien af **Manuel oprettelse** tillader, at statiske menupunkter overvåges.</span><span class="sxs-lookup"><span data-stu-id="9d93e-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="9d93e-123">Værdien af **Detail og manuel oprettelse** tillader en blanding af begge dele.</span><span class="sxs-lookup"><span data-stu-id="9d93e-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="9d93e-124">Vise kategoribilleder</span><span class="sxs-lookup"><span data-stu-id="9d93e-124">Show category images</span></span> | <span data-ttu-id="9d93e-125">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9d93e-125">**True** or **False**</span></span>    | <span data-ttu-id="9d93e-126">Når denne egenskab er aktiveret, viser kategoribilleder i den navigationsmenu, som er defineret i Commerce Headquarters for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="9d93e-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="9d93e-127">Tilføjet i Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="9d93e-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="9d93e-128">Aktivere navigationsmenu på flere niveauer</span><span class="sxs-lookup"><span data-stu-id="9d93e-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="9d93e-129">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9d93e-129">**True** or **False**</span></span> | <span data-ttu-id="9d93e-130">Når denne egenskab er aktiveret, kan navigationsmenuen vise flere niveauer i navigationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="9d93e-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="9d93e-131">Denne funktion er tilgængelig i version 10.0.15 af Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d93e-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="9d93e-132">Antal niveauer</span><span class="sxs-lookup"><span data-stu-id="9d93e-132">Number of levels</span></span> | <span data-ttu-id="9d93e-133">heltal</span><span class="sxs-lookup"><span data-stu-id="9d93e-133">integer</span></span> | <span data-ttu-id="9d93e-134">Denne egenskab definerer antallet af niveauer, der skal vises, hvis egenskaben **Aktiver navigationsmenu på flere niveauer** er indstillet til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="9d93e-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="9d93e-135">Statisk menupunkt</span><span class="sxs-lookup"><span data-stu-id="9d93e-135">Static menu item</span></span>| <span data-ttu-id="9d93e-136">Matrix af værdier</span><span class="sxs-lookup"><span data-stu-id="9d93e-136">Array of values</span></span>| <span data-ttu-id="9d93e-137">Statiske menupunkter, der knytter et menupunkts navn til et link til en statisk webside.</span><span class="sxs-lookup"><span data-stu-id="9d93e-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="9d93e-138">Du kan oprette menupunkter under andre menupunkter.</span><span class="sxs-lookup"><span data-stu-id="9d93e-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="9d93e-139">Som standard vises statiske menuer på rodniveau, og de føjes til kanalnavigationshierarkiet, hvis det findes.</span><span class="sxs-lookup"><span data-stu-id="9d93e-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="9d93e-140">Vis rodmenu</span><span class="sxs-lookup"><span data-stu-id="9d93e-140">Show root menu</span></span> | <span data-ttu-id="9d93e-141">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9d93e-141">**True** or **False**</span></span> | <span data-ttu-id="9d93e-142">Når denne egenskab er aktiveret, kan navigationsmenuen defineres under en brugerdefineret rod (f.eks. **Køb nu**).</span><span class="sxs-lookup"><span data-stu-id="9d93e-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="9d93e-143">Denne funktion er tilgængelig i version 10.0.15 af Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9d93e-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="9d93e-144">Rodmenu</span><span class="sxs-lookup"><span data-stu-id="9d93e-144">Root menu</span></span> | <span data-ttu-id="9d93e-145">streng</span><span class="sxs-lookup"><span data-stu-id="9d93e-145">string</span></span> | <span data-ttu-id="9d93e-146">Denne egenskab kan bruges til at definere tekst for en brugerdefineret rod, hvis egenskaben **Vis rodmenu** er indstillet til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="9d93e-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="9d93e-147">I følgende illustration vises et eksempel på et kategoribillede, der vises i navigationsmenuen for Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="9d93e-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="9d93e-148">![Eksempel på et navigationsmenumodul med kategoribilleder](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="9d93e-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="9d93e-149">Tilføje et navigationsmenumodul i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="9d93e-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="9d93e-150">Du kan finde flere oplysninger om, hvordan du føjer et navigationsmenumodul til et sidehovedmodul, under [Sidehovedmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="9d93e-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d93e-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9d93e-151">Additional resources</span></span>

[<span data-ttu-id="9d93e-152">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="9d93e-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9d93e-153">Brødkrummemodul</span><span class="sxs-lookup"><span data-stu-id="9d93e-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="9d93e-154">Webstedsvælgermodul</span><span class="sxs-lookup"><span data-stu-id="9d93e-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="9d93e-155">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="9d93e-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9d93e-156">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="9d93e-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="9d93e-157">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="9d93e-157">Header module</span></span>](author-header-module.md)
