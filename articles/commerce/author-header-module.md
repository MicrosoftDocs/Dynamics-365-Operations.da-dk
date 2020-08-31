---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686616"
---
# <a name="header-module"></a><span data-ttu-id="f1ab8-103">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1ab8-104">Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f1ab8-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f1ab8-105">Overview</span></span>

<span data-ttu-id="f1ab8-106">I Dynamics 365 Commerce indeholder et sidehoved flere moduler, f.eks. sidehoved, navigationsmenu, søg, kampagnebanner og moduler til cookie-samtykke.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="f1ab8-107">Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et indkøbskurvsymbol, et hvidlistesymbol, logonindstillinger og søgelinjen.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="f1ab8-108">Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed).</span><span class="sxs-lookup"><span data-stu-id="f1ab8-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="f1ab8-109">På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).</span><span class="sxs-lookup"><span data-stu-id="f1ab8-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="f1ab8-110">Det følgende billede viser et eksempel på et sidehovedmodul på en startside.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-110">The following image shows an example of a header module on a home page.</span></span>

![Eksempel på et sidehovedmodul](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="f1ab8-112">Egenskaber for et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-112">Properties of a header module</span></span>

<span data-ttu-id="f1ab8-113">Et sidehovedmodul understøtter egenskaberne **Logo-billede**, **Logo** og **Min konto-link**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="f1ab8-114">Egenskaberne **Logo-billede** og **Logo-link** bruges til at definere et logo på siden.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="f1ab8-115">Du kan finde flere oplysninger under [Tilføj et logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="f1ab8-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="f1ab8-116">Egenskaben **Min konto-link** kan bruges til at definere kontosider, som ejeren af webstedet ønsker at vise hurtige links for i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="f1ab8-117">Moduler, der er tilgængelige i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-117">Modules that are available in a header module</span></span>

<span data-ttu-id="f1ab8-118">Følgende moduler kan bruges i et sidehovedmodul:</span><span class="sxs-lookup"><span data-stu-id="f1ab8-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="f1ab8-119">**Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="f1ab8-120">Kanalnavigationshierarkiet kan konfigureres i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f1ab8-121">Navigationsmenuen indeholder egenskaben **Navigationskilde**, der bruges til at angive navigationsmenupunkter i Detailservere og statiske menupunkter som en kilde.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="f1ab8-122">Hvis statiske menupunkter angives som kilde, kan der angives relative links til andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="f1ab8-123">Konfigurerede elementer vises derefter som sidehovednavigation.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="f1ab8-124">**Søg** – Søgemodulet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="f1ab8-125">URL-adressen til standardsøgesiden og parametrene for søgeforespørgslen skal angives på **Indstillinger for webside \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="f1ab8-126">Søgemodulet har egenskaber, du kan bruge til at undertrykke søgeknappen eller -etiketten efter behov.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="f1ab8-127">Søgemodulet understøtter også indstillinger for automatisk at foreslå, f.eks. produkt-, nøgleords- og kategorisøgeresultater.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="f1ab8-128">**Indkøbsvognikon** – Indkøbsvognikonmodulet repræsenterer indkøbsvognikonet, som viser antallet af varer i en indkøbsvogn på et givet tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="f1ab8-129">Du kan få flere oplysninger i [Modulet for indkøbsvognikon](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="f1ab8-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="f1ab8-130">Opret et sidehovedmodul for en side</span><span class="sxs-lookup"><span data-stu-id="f1ab8-130">Create a header module for a page</span></span>

<span data-ttu-id="f1ab8-131">Følg disse trin for at oprette et sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="f1ab8-132">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f1ab8-133">I dialogboksen **Nyt sidefragment** skal du vælge modulet **Container**, angive et navn for sidefragmentet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-134">Vælg pladsen **Standardcontainer**, og angiv derefter egenskaben **Bredde** til **Udfyld container**, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f1ab8-135">På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1ab8-136">I dialogboksen **Tilføj modul** skal du vælge modulerne **Kampagnebanner** og **Cookie-samtykke**. Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-137">På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1ab8-138">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-139">Vælg pladsen **Container**, og angiv derefter egenskaben **Bredde** til **Udfyld container**, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f1ab8-140">På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1ab8-141">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidehoved** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-142">På pladsen **Navigationsmenu** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1ab8-143">I dialogboksen **Tilføj modul** skal du vælge modulet **Navigationsmenu** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-144">Konfigurer egenskaberne som påkrævet i egenskabsruden for navigationsmenumodulet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="f1ab8-145">På pladsen **Søg** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1ab8-146">I dialogboksen **Tilføj modul** skal du vælge modulet **Søg** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-147">Konfigurer egenskaberne som påkrævet i egenskabsruden for søgemodulet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="f1ab8-148">På pladsen **Indkøbskurvikon** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1ab8-149">I dialogboksen **Tilføj modul** skal du vælge modulet **Indkøbskurvikon** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1ab8-150">Konfigurer egenskaberne som påkrævet i egenskabsruden for indkøbskurvikonmodulet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="f1ab8-151">Hvis du ønsker, at indkøbsvognen skal vise en indkøbsvognoversigt (også kaldet en minivogn), når brugerne bevæger dig hen over den, skal du vælge **Vis minivogn**.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="f1ab8-152">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f1ab8-153">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f1ab8-154">På pladsen **Sidehoved** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f1ab8-155">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="f1ab8-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1ab8-156">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f1ab8-156">Additional resources</span></span>

[<span data-ttu-id="f1ab8-157">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="f1ab8-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f1ab8-158">Container-modul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f1ab8-159">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="f1ab8-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f1ab8-160">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f1ab8-161">Modulet Indkøbskurvikon</span><span class="sxs-lookup"><span data-stu-id="f1ab8-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f1ab8-162">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f1ab8-163">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f1ab8-164">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f1ab8-165">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f1ab8-165">Footer module</span></span>](author-footer-module.md)
