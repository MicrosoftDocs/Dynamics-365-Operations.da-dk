---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261438"
---
# <a name="header-module"></a><span data-ttu-id="262ea-103">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="262ea-104">Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="262ea-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="262ea-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="262ea-105">Overview</span></span>

<span data-ttu-id="262ea-106">I Dynamics 365 Commerce indeholder et sidehoved flere moduler, f.eks. sidehoved, navigationsmenu, søg, kampagnebanner og moduler til cookie-samtykke.</span><span class="sxs-lookup"><span data-stu-id="262ea-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="262ea-107">Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et indkøbskurvsymbol, et hvidlistesymbol, logonindstillinger og søgelinjen.</span><span class="sxs-lookup"><span data-stu-id="262ea-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="262ea-108">Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed).</span><span class="sxs-lookup"><span data-stu-id="262ea-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="262ea-109">På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).</span><span class="sxs-lookup"><span data-stu-id="262ea-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="262ea-110">Egenskaber for et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-110">Properties of a header module</span></span>

<span data-ttu-id="262ea-111">Et sidehovedmodul understøtter egenskaberne **Logo-billede**, **Logo** og **Min konto-link**.</span><span class="sxs-lookup"><span data-stu-id="262ea-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="262ea-112">Egenskaberne **Logo-billede** og **Logo-link** bruges til at definere et logo på siden.</span><span class="sxs-lookup"><span data-stu-id="262ea-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="262ea-113">Du kan finde flere oplysninger under [Tilføj et logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="262ea-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="262ea-114">Egenskaben **Min konto-link** kan bruges til at definere kontosider, som ejeren af webstedet ønsker at vise hurtige links for i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="262ea-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="262ea-115">Moduler, der er tilgængelige i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-115">Modules that are available in a header module</span></span>

<span data-ttu-id="262ea-116">Følgende moduler kan bruges i et sidehovedmodul:</span><span class="sxs-lookup"><span data-stu-id="262ea-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="262ea-117">**Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="262ea-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="262ea-118">Kanalnavigationshierarkiet kan konfigureres i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="262ea-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="262ea-119">Navigationsmenuen indeholder egenskaben **Navigationskilde**, der bruges til at angive navigationsmenupunkter i Detailservere og statiske menupunkter som en kilde.</span><span class="sxs-lookup"><span data-stu-id="262ea-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="262ea-120">Hvis statiske menupunkter angives som kilde, kan der angives relative links til andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="262ea-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="262ea-121">Konfigurerede elementer vises derefter som sidehovednavigation.</span><span class="sxs-lookup"><span data-stu-id="262ea-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="262ea-122">**Søg** – Søgemodulet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter.</span><span class="sxs-lookup"><span data-stu-id="262ea-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="262ea-123">URL-adressen til standardsøgesiden og parametrene for søgeforespørgslen skal angives på **Indstillinger for webside \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="262ea-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="262ea-124">Søgemodulet har egenskaber, du kan bruge til at undertrykke søgeknappen eller -etiketten efter behov.</span><span class="sxs-lookup"><span data-stu-id="262ea-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="262ea-125">Søgemodulet understøtter også indstillinger for automatisk at foreslå, f.eks. produkt-, nøgleords- og kategorisøgeresultater.</span><span class="sxs-lookup"><span data-stu-id="262ea-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="262ea-126">**Indkøbsvognikon** – Indkøbsvognikonmodulet repræsenterer indkøbsvognikonet, som viser antallet af varer i en indkøbsvogn på et givet tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="262ea-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="262ea-127">Du kan få flere oplysninger i [Modulet for indkøbsvognikon](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="262ea-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="262ea-128">Opret et sidehovedmodul for en side</span><span class="sxs-lookup"><span data-stu-id="262ea-128">Create a header module for a page</span></span>

<span data-ttu-id="262ea-129">Følg disse trin for at oprette et sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="262ea-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="262ea-130">Opret et fragment med navnet **Sidehovedfragment**, og føj et containermodul til det.</span><span class="sxs-lookup"><span data-stu-id="262ea-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="262ea-131">Angiv egenskaben **Bredde** til **Fyld container**i egenskabsruden for containermodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="262ea-132">Føj et kampagnebanner og cookie-samtykkemoduler til containermodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="262ea-133">Føj et andet containermodul til fragmentet, og indstil egenskaben **Bredde** til **Fyld container**.</span><span class="sxs-lookup"><span data-stu-id="262ea-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="262ea-134">Føj et sidehovedmodul til det andet containermodul.</span><span class="sxs-lookup"><span data-stu-id="262ea-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="262ea-135">Tilføj et navigationsmenumodul i **Navigationsmenu**pladsen i sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="262ea-136">Konfigurer egenskaberne for navigationsmenumodulet i egenskabsruden for navigationsmenumodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="262ea-137">Tilføj et søgemodul i **Søg**pladsen i sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="262ea-138">Konfigurer egenskaberne for søgemodulet i egenskabsruden for søgemodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="262ea-139">Tilføj et indkøbsvognikonmodul i pladsen **Indkøbsvognikon**.</span><span class="sxs-lookup"><span data-stu-id="262ea-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="262ea-140">Konfigurer egenskaberne for indkøbsvognikonmodulet i egenskabsruden for ikonet for indkøbsvognikonmodulet.</span><span class="sxs-lookup"><span data-stu-id="262ea-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="262ea-141">Hvis indkøbsvognikonet skal vise en minivogn, når der peges på den, skal du vælge **Sand** for **Vis minivogn**.</span><span class="sxs-lookup"><span data-stu-id="262ea-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="262ea-142">Gem sidefragmentet, afslut redigeringen, og udgiv det.</span><span class="sxs-lookup"><span data-stu-id="262ea-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="262ea-143">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="262ea-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="262ea-144">Tilføj det sidehovedfragment, der indeholder sidehovedmodulet af sidehovedet, i **Hoved**pladsen af standardsiden.</span><span class="sxs-lookup"><span data-stu-id="262ea-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="262ea-145">Gem skabelonen, afslut redigeringen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="262ea-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="262ea-146">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="262ea-146">Additional resources</span></span>

[<span data-ttu-id="262ea-147">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="262ea-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="262ea-148">Container-modul</span><span class="sxs-lookup"><span data-stu-id="262ea-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="262ea-149">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="262ea-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="262ea-150">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="262ea-151">Modulet Indkøbskurvikon</span><span class="sxs-lookup"><span data-stu-id="262ea-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="262ea-152">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="262ea-153">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="262ea-154">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="262ea-155">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="262ea-155">Footer module</span></span>](author-footer-module.md)
