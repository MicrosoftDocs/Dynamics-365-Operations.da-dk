---
title: Sidehovedmodul
description: Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697269"
---
# <a name="header-module"></a><span data-ttu-id="86e7c-103">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-103">Header module</span></span>

<span data-ttu-id="86e7c-104">[!include [banner]includes/preview-banner.md] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="86e7c-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="86e7c-105">Dette emne omhandler sidehovedmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86e7c-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86e7c-106">Oversigt</span><span class="sxs-lookup"><span data-stu-id="86e7c-106">Overview</span></span>

<span data-ttu-id="86e7c-107">Et sidehovedmodul er en særlig container, der bruges som vært for alle de moduler, der vises i et sidehoved.</span><span class="sxs-lookup"><span data-stu-id="86e7c-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="86e7c-108">Det kan f.eks. indeholde dit websteds logo, links til navigationshierarkiet, links til andre sider på webstedet og søgepanelet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="86e7c-109">Et sidehovedmodul optimeres automatisk for den enhed, som webstedet vises på (dvs. en stationær enhed eller en mobilenhed).</span><span class="sxs-lookup"><span data-stu-id="86e7c-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="86e7c-110">På en mobilenhed er navigationslinjen f.eks. skjult på **Menu**-knappen (som undertiden kaldes en *hamburgermenu*).</span><span class="sxs-lookup"><span data-stu-id="86e7c-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="86e7c-111">Egenskaber for et sidehoved</span><span class="sxs-lookup"><span data-stu-id="86e7c-111">Properties of a header</span></span>

<span data-ttu-id="86e7c-112">Ligesom generiske containere understøtter et sidehovedmodulet egenskaberne **overskrift** og **bredde**.</span><span class="sxs-lookup"><span data-stu-id="86e7c-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="86e7c-113">Et sidehovedmodul har flere pladser.</span><span class="sxs-lookup"><span data-stu-id="86e7c-113">A header module has multiple slots.</span></span> <span data-ttu-id="86e7c-114">Der er f.eks. pladser til en oplysningsmeddelelse, navigationsmenu, logo, søgepanel, indkøbsvognsikon, ønskelisteikon og kontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="86e7c-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="86e7c-115">Hver plads understøtter et bestemt sæt moduler.</span><span class="sxs-lookup"><span data-stu-id="86e7c-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="86e7c-116">Moduler, der er tilgængelige i et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-116">Modules that are available in a header module</span></span>

<span data-ttu-id="86e7c-117">Følgende moduler kan bruges i et sidehovedmodul:</span><span class="sxs-lookup"><span data-stu-id="86e7c-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="86e7c-118">**Navigationsmenu** – Navigationsmenuen repræsenterer hierarkiet for kanalnavigation og andre statiske navigationslinks.</span><span class="sxs-lookup"><span data-stu-id="86e7c-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="86e7c-119">Kanalnavigationshierarkiet kan konfigureres i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="86e7c-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="86e7c-120">Konfigurerede elementer vises derefter som sidehovednavigation.</span><span class="sxs-lookup"><span data-stu-id="86e7c-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="86e7c-121">Desuden kan statiske navigationslinks konfigureres, og der kan angives relative links til andre sider på e-handelsstedet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="86e7c-122">Selve sidehovedet kan justeres til venstre, højre eller i midten.</span><span class="sxs-lookup"><span data-stu-id="86e7c-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="86e7c-123">**Indkøbsvogn** – Indkøbsvogn-ikonet er et særligt ikon, der repræsenterer indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="86e7c-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="86e7c-124">Det vises i sidehovedet og angiver antallet af varer i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="86e7c-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="86e7c-125">Et link til siden med indkøbsvognen skal ledsage indkøbsvognikonet, så kunderne kan blive omdirigeret til indkøbsvognen, når de bruger ikonet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="86e7c-126">**Ønskelisteikon** – Ønskelisteikonet vises i sidehovedet og angiver det antal varer, der er føjet til kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="86e7c-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="86e7c-127">Et link til siden med ønskelisten skal ledsage dette ikon, så kunderne kan blive omdirigeret til ønskelistesiden, når de bruger ikonet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="86e7c-128">**Logonmodul** – Logonmodulet vises i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="86e7c-129">Her kan kunderne enten logge på deres konto eller tilmelde sig en konto.</span><span class="sxs-lookup"><span data-stu-id="86e7c-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="86e7c-130">Hvis kunden allerede er logget på, kan modulet konfigureres til at vise links til kontosiden, ordrehistoriksiden eller en anden side.</span><span class="sxs-lookup"><span data-stu-id="86e7c-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="86e7c-131">**Logomodul** – Dette modul viser det logo, der repræsenterer detailhandleren og varemærket.</span><span class="sxs-lookup"><span data-stu-id="86e7c-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="86e7c-132">Det er et billede, der har et link.</span><span class="sxs-lookup"><span data-stu-id="86e7c-132">It's an image that has a link.</span></span> <span data-ttu-id="86e7c-133">Linket konfigureres typisk, så det har en omdirigering til startsiden, og derfor kan kunderne hurtigt vende tilbage til startsiden fra en hvilken som helst side på webstedet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="86e7c-134">**Påmindelse** – Der vises en påmindelse i sidehovedet, og den bruges til at vise en indbygget meddelelse, der gælder for alle sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="86e7c-135">En påmindelse kan være en meddelelse som f.eks. "Det årlige udsalgs slutter om to dage".</span><span class="sxs-lookup"><span data-stu-id="86e7c-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="86e7c-136">**Søgepanel** – Søgepanelet giver brugerne mulighed for at angive søgeord, så de kan søge efter produkter.</span><span class="sxs-lookup"><span data-stu-id="86e7c-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="86e7c-137">Modulet skal konfigureres med URL-adressen til siden med søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="86e7c-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="86e7c-138">Parameteren for forespørgselsstrengen kan konfigureres (standardværdien er **"q"**).</span><span class="sxs-lookup"><span data-stu-id="86e7c-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="86e7c-139">Søgepanelet har en plads til automatiske forslag, hvor modulet med automatiske forslag skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="86e7c-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="86e7c-140">**Automatiske forslag** – Modulet til automatiske forslag viser automatisk resultatforslag.</span><span class="sxs-lookup"><span data-stu-id="86e7c-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="86e7c-141">Disse resultater kan være nøgleord, produkter eller kategorier, hvor søgeordet indgår i.</span><span class="sxs-lookup"><span data-stu-id="86e7c-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="86e7c-142">Oprette et sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-142">Create a header module</span></span>

<span data-ttu-id="86e7c-143">Følg disse trin for at oprette et sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="86e7c-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="86e7c-144">Opret et sidefragment, der indeholder et sidehovedmodul.</span><span class="sxs-lookup"><span data-stu-id="86e7c-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="86e7c-145">Tilføj moduler på pladserne i sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="86e7c-146">Opdater indstillingerne for de enkelte moduler.</span><span class="sxs-lookup"><span data-stu-id="86e7c-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="86e7c-147">Gem sidefragmentet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="86e7c-148">Tjek siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="86e7c-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="86e7c-149">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="86e7c-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="86e7c-150">På standardsiden skal du føje det sidefragment, der indeholder sidehovedmodulet, til sidehovedet på hovedpladsen.</span><span class="sxs-lookup"><span data-stu-id="86e7c-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="86e7c-151">Gem skabelonen.</span><span class="sxs-lookup"><span data-stu-id="86e7c-151">Save the template.</span></span> 
1. <span data-ttu-id="86e7c-152">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="86e7c-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86e7c-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="86e7c-153">Additional resources</span></span>

[<span data-ttu-id="86e7c-154">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="86e7c-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="86e7c-155">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="86e7c-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="86e7c-156">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="86e7c-157">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="86e7c-158">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="86e7c-159">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="86e7c-160">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="86e7c-161">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="86e7c-161">Footer module</span></span>](author-footer-module.md)
