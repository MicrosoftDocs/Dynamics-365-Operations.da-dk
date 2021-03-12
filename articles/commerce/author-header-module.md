---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1373397c4499ed65835bcc71c6fc628ff356e4e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991509"
---
# <a name="header-module"></a><span data-ttu-id="a99af-103">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="a99af-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a99af-104">Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette sidehoveder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a99af-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a99af-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a99af-105">Overview</span></span>

<span data-ttu-id="a99af-106">I Dynamics 365 Commerce konfigureres et sidehoved som et sidefragment, der omfatter modulerne til sidehoved, kampagnebanner og cookie-samtykke.</span><span class="sxs-lookup"><span data-stu-id="a99af-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="a99af-107">Sidehovedmodulet indeholder et websteds logo, links til navigationshierarkiet, links til andre sider på webstedet, et modul til indkøbskurveikon, et hvidlistesymbol, logonindstillinger og søgelinjen.</span><span class="sxs-lookup"><span data-stu-id="a99af-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="a99af-108">Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (med andre ord en stationær enhed eller en mobilenhed).</span><span class="sxs-lookup"><span data-stu-id="a99af-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="a99af-109">På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).</span><span class="sxs-lookup"><span data-stu-id="a99af-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="a99af-110">Det følgende billede viser et eksempel på et sidehovedmodul på en startside.</span><span class="sxs-lookup"><span data-stu-id="a99af-110">The following image shows an example of a header module on a home page.</span></span>

![Eksempel på et sidehovedmodul](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="a99af-112">Egenskaber for et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="a99af-112">Properties of a header module</span></span>

<span data-ttu-id="a99af-113">Et sidehovedmodul understøtter egenskaberne **Logo-billede**, **Logo** og **Min konto-link**.</span><span class="sxs-lookup"><span data-stu-id="a99af-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="a99af-114">Egenskaberne **Logo-billede** og **Logo-link** bruges til at definere et logo på siden.</span><span class="sxs-lookup"><span data-stu-id="a99af-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="a99af-115">Du kan finde flere oplysninger under [Tilføj et logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="a99af-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="a99af-116">Egenskaben **Min konto-link** kan bruges til at definere kontosider, som ejeren af webstedet ønsker at vise hurtige links for i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="a99af-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="a99af-117">Moduler, der er tilgængelige i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="a99af-117">Modules that are available within a header module</span></span>

<span data-ttu-id="a99af-118">Følgende moduler kan bruges i et sidehovedmodul:</span><span class="sxs-lookup"><span data-stu-id="a99af-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="a99af-119">**Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="a99af-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="a99af-120">Du kan finde flere oplysninger i [Navigationsmenumodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="a99af-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="a99af-121">**Søg** – Søgemodulet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter.</span><span class="sxs-lookup"><span data-stu-id="a99af-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="a99af-122">URL-adressen til standardsøgesiden og parametrene for søgeforespørgslen skal angives på **Indstillinger for webside \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="a99af-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="a99af-123">Søgemodulet har egenskaber, du kan bruge til at undertrykke søgeknappen eller -etiketten efter behov.</span><span class="sxs-lookup"><span data-stu-id="a99af-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="a99af-124">Søgemodulet understøtter også indstillinger for automatisk at foreslå, f.eks. produkt-, nøgleords- og kategorisøgeresultater.</span><span class="sxs-lookup"><span data-stu-id="a99af-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="a99af-125">**Indkøbsvognikon** – Indkøbsvognikonmodulet repræsenterer indkøbsvognikonet, som viser antallet af varer i en indkøbsvogn på et givet tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="a99af-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="a99af-126">Du kan få flere oplysninger i [Modulet for indkøbsvognikon](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="a99af-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="a99af-127">**Webstedsvælger**- Med webstedsvælgermodulet kan brugere gennemse forskellige foruddefinerede websteder baseret på marked, områder og landestandarder.</span><span class="sxs-lookup"><span data-stu-id="a99af-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="a99af-128">Du kan få flere oplysninger under [Webstedsvælgermodul](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="a99af-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="a99af-129">**Butiksvælger** - Butiksvælgermodulet kan medtages på et overskriftmoduls butiksvælgerplads.</span><span class="sxs-lookup"><span data-stu-id="a99af-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="a99af-130">Det giver brugere mulighed for at søge efter og finde butikker i nærheden.</span><span class="sxs-lookup"><span data-stu-id="a99af-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="a99af-131">Brugerne kan også angive en foretrukken butik.</span><span class="sxs-lookup"><span data-stu-id="a99af-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="a99af-132">Butikken vil derefter blive vist i overskriften.</span><span class="sxs-lookup"><span data-stu-id="a99af-132">That store will then be shown in the header.</span></span> <span data-ttu-id="a99af-133">Når butiksvælgermodulet er inkluderet i overskriftsmodulet, skal egenskaben **Tilstand** være angivet til **Find butikker**.</span><span class="sxs-lookup"><span data-stu-id="a99af-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="a99af-134">Du kan få flere oplysninger under [Butiksvælgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="a99af-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="a99af-135">Understøttelse af indkøbsvognikonets modul i overskriftsmoduler er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="a99af-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="a99af-136">Understøttelse af webstedsvælgermodulet i overskriftsmoduler er tilgængelig i Dynamics 365 Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="a99af-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="a99af-137">Understøttelse af butiksvælgermodulet i overskriftsmoduler er tilgængelig i Dynamics 365 Commerce version 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="a99af-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="a99af-138">Oprette et sidehovedfragment for en side</span><span class="sxs-lookup"><span data-stu-id="a99af-138">Create a header fragment for a page</span></span>

<span data-ttu-id="a99af-139">Følg disse trin for at oprette et sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="a99af-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="a99af-140">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="a99af-140">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="a99af-141">I dialogboksen **Nyt fragment** skal du vælge modulet **Container**, angive et navn for fragmentet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="a99af-142">Vælg pladsen **Standardcontainer**, og angiv derefter egenskaben **Bredde** til **Udfyld skærm** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="a99af-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="a99af-143">På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a99af-143">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a99af-144">I dialogboksen **Tilføj modul** skal du vælge modulerne **Cookie-samtykke**, **Sidehoved** og **Kampagnebanner**. Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-144">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="a99af-145">Vælg **Tilføj meddelelse** i ruden Egenskaber i modulet **Kampagnebanner**, og vælg derefter **Meddelelse**.</span><span class="sxs-lookup"><span data-stu-id="a99af-145">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="a99af-146">Tilføj tekst og links i kampagneindholdet i dialogboksen **Meddelelse**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="a99af-147">Tilføj og Konfigurer tekst og et link til websiden om beskyttelse af personlige oplysninger i ruden Egenskaber i modulet **Cookie-samtykke**.</span><span class="sxs-lookup"><span data-stu-id="a99af-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="a99af-148">På pladsen **Navigationsmenu** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a99af-148">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a99af-149">I dialogboksen **Tilføj modul** skal du vælge modulet **Navigationsmenu** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a99af-150">Vælg **Detailserver** under **Kilde til navigationsmenu** i egenskabsruden for modulet navigationsmenu.</span><span class="sxs-lookup"><span data-stu-id="a99af-150">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="a99af-151">Vælg **Tilføj menupunkt** i egenskabsruden for modulet navigationsmenu under **Statiske menupunkter**, og vælg derefter **Menupunkt**.</span><span class="sxs-lookup"><span data-stu-id="a99af-151">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="a99af-152">Angiv "Kontakt" i dialogboksen **Menupunkt** under **Menupunkttekst**.</span><span class="sxs-lookup"><span data-stu-id="a99af-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="a99af-153">Vælg **Tilføj et link** under **Linkdestination for menupunkt** i dialogboksen **Menupunkt**.</span><span class="sxs-lookup"><span data-stu-id="a99af-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="a99af-154">Vælg URL-adressen til websiden "Kontakt" i dialogboksen **Tilføj et link**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="a99af-155">Vælg **OK** i dialogboksen **Menupunkt**.</span><span class="sxs-lookup"><span data-stu-id="a99af-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="a99af-156">På pladsen **Søg** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a99af-156">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a99af-157">I dialogboksen **Tilføj modul** skal du vælge modulet **Søg** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a99af-158">Konfigurer egenskaberne som påkrævet i egenskabsruden for søgemodulet.</span><span class="sxs-lookup"><span data-stu-id="a99af-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="a99af-159">På pladsen **Indkøbskurvikon** i sidehovedmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="a99af-159">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a99af-160">I dialogboksen **Tilføj modul** skal du vælge modulet **Indkøbskurvikon** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a99af-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a99af-161">Konfigurer egenskaberne som påkrævet i egenskabsruden for indkøbskurvikonmodulet.</span><span class="sxs-lookup"><span data-stu-id="a99af-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="a99af-162">Hvis du ønsker, at indkøbsvognen skal vise en indkøbsvognoversigt (også kaldet en minivogn), når brugerne bevæger dig hen over den, skal du vælge **Vis minivogn**.</span><span class="sxs-lookup"><span data-stu-id="a99af-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="a99af-163">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="a99af-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="a99af-164">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="a99af-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="a99af-165">På pladsen **Sidehoved** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="a99af-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="a99af-166">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="a99af-166">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a99af-167">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a99af-167">Additional resources</span></span>

[<span data-ttu-id="a99af-168">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="a99af-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a99af-169">Container-modul</span><span class="sxs-lookup"><span data-stu-id="a99af-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a99af-170">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="a99af-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a99af-171">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="a99af-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="a99af-172">Navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="a99af-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="a99af-173">Samtykke til cookie</span><span class="sxs-lookup"><span data-stu-id="a99af-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="a99af-174">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="a99af-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="a99af-175">Webstedsvælgermodul</span><span class="sxs-lookup"><span data-stu-id="a99af-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="a99af-176">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="a99af-176">Store selector module</span></span>](store-selector.md)
