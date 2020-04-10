---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025647"
---
# <a name="header-module"></a><span data-ttu-id="04d50-103">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="04d50-104">Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="04d50-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="04d50-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="04d50-105">Overview</span></span>

<span data-ttu-id="04d50-106">I Dynamics 365 Commerce indeholder et sidehoved flere moduler, f.eks. sidehoved, navigationsmenu, søg, kampagnebanner og moduler til cookie-samtykke.</span><span class="sxs-lookup"><span data-stu-id="04d50-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="04d50-107">Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et indkøbskurvsymbol, et hvidlistesymbol, logonindstillinger og søgelinjen.</span><span class="sxs-lookup"><span data-stu-id="04d50-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="04d50-108">Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed).</span><span class="sxs-lookup"><span data-stu-id="04d50-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="04d50-109">På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).</span><span class="sxs-lookup"><span data-stu-id="04d50-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="04d50-110">Egenskaber for et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-110">Properties of a header module</span></span>

<span data-ttu-id="04d50-111">Et sidehovedmodul understøtter egenskaberne **Logo-billede**, **Logo** og **Min konto-link**.</span><span class="sxs-lookup"><span data-stu-id="04d50-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="04d50-112">Egenskaberne **Logo-billede** og **Logo-link** bruges til at definere et logo på siden.</span><span class="sxs-lookup"><span data-stu-id="04d50-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="04d50-113">Du kan finde flere oplysninger under [Tilføj et logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="04d50-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="04d50-114">Egenskaben **Min konto-link** kan bruges til at definere kontosider, som ejeren af webstedet ønsker at vise hurtige links for i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="04d50-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="04d50-115">Moduler, der er tilgængelige i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-115">Modules that are available in a header module</span></span>

<span data-ttu-id="04d50-116">Følgende moduler kan bruges i et sidehovedmodul:</span><span class="sxs-lookup"><span data-stu-id="04d50-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="04d50-117">**Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="04d50-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="04d50-118">Kanalnavigationshierarkiet kan konfigureres i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="04d50-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="04d50-119">Navigationsmenuen indeholder egenskaben **Navigationskilde**, der bruges til at angive navigationsmenupunkter i Detailservere og statiske menupunkter som en kilde.</span><span class="sxs-lookup"><span data-stu-id="04d50-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="04d50-120">Hvis statiske menupunkter angives som kilde, kan der angives relative links til andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="04d50-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="04d50-121">Konfigurerede elementer vises derefter som sidehovednavigation.</span><span class="sxs-lookup"><span data-stu-id="04d50-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="04d50-122">**Søg** – Søgemodulet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter.</span><span class="sxs-lookup"><span data-stu-id="04d50-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="04d50-123">URL-adressen til standardsøgesiden og parametrene for søgeforespørgslen skal angives på **Indstillinger for webside \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="04d50-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="04d50-124">Søgemodulet har egenskaber, du kan bruge til at undertrykke søgeknappen eller -etiketten efter behov.</span><span class="sxs-lookup"><span data-stu-id="04d50-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="04d50-125">Søgemodulet understøtter også indstillinger for automatisk at foreslå, f.eks. produkt-, nøgleords- og kategorisøgeresultater.</span><span class="sxs-lookup"><span data-stu-id="04d50-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="04d50-126">Opret et sidehovedmodul for en side</span><span class="sxs-lookup"><span data-stu-id="04d50-126">Create a header module for a page</span></span>

<span data-ttu-id="04d50-127">Følg disse trin for at oprette et sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="04d50-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="04d50-128">Opret et fragment med navnet **Sidehovedfragment**, og føj et containermodul til det.</span><span class="sxs-lookup"><span data-stu-id="04d50-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="04d50-129">Angiv egenskaben **Bredde** til **Fyld container**i egenskabsruden for containermodulet.</span><span class="sxs-lookup"><span data-stu-id="04d50-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="04d50-130">Føj kampagnebanner og cookie-samtykkemoduler til containermodulet.</span><span class="sxs-lookup"><span data-stu-id="04d50-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="04d50-131">Føj et andet containermodul til fragmentet, og indstil egenskaben **Bredde** til **Fyld container**.</span><span class="sxs-lookup"><span data-stu-id="04d50-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="04d50-132">Føj et sidehovedmodul til det andet containermodul.</span><span class="sxs-lookup"><span data-stu-id="04d50-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="04d50-133">Tilføj et navigationsmenumodul i **Navigationsmenu**pladsen i sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="04d50-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="04d50-134">Konfigurer egenskaberne for navigationsmenumodulet i egenskabsruden for navigationsmenumodulet.</span><span class="sxs-lookup"><span data-stu-id="04d50-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="04d50-135">Tilføj et søgemodul i **Søg**pladsen i sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="04d50-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="04d50-136">Konfigurer egenskaberne for søgemodulet i egenskabsruden for søgemodulet.</span><span class="sxs-lookup"><span data-stu-id="04d50-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="04d50-137">Gem sidefragmentet, afslut redigeringen, og udgiv det.</span><span class="sxs-lookup"><span data-stu-id="04d50-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="04d50-138">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="04d50-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="04d50-139">Tilføj det sidehovedfragment, der indeholder sidehovedmodulet af sidehovedet, i **Hoved**pladsen af standardsiden.</span><span class="sxs-lookup"><span data-stu-id="04d50-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="04d50-140">Gem skabelonen, afslut redigeringen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="04d50-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04d50-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="04d50-141">Additional resources</span></span>

[<span data-ttu-id="04d50-142">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="04d50-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="04d50-143">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="04d50-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="04d50-144">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="04d50-145">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="04d50-146">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="04d50-147">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="04d50-148">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="04d50-149">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="04d50-149">Footer module</span></span>](author-footer-module.md)
