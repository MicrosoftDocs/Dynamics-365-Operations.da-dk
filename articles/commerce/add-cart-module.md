---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621030"
---
# <a name="cart-module"></a><span data-ttu-id="7b427-103">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7b427-104">Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7b427-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7b427-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="7b427-105">Overview</span></span>

<span data-ttu-id="7b427-106">Et indkøbsvognmodul viser de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale.</span><span class="sxs-lookup"><span data-stu-id="7b427-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="7b427-107">Modulet viser også en ordreoversigt, og kunden kan anvende eller fjerne kampagnekoder.</span><span class="sxs-lookup"><span data-stu-id="7b427-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="7b427-108">Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst.</span><span class="sxs-lookup"><span data-stu-id="7b427-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="7b427-109">Den understøtter også et **Tilbage til indkøb**-link.</span><span class="sxs-lookup"><span data-stu-id="7b427-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="7b427-110">Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="7b427-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="7b427-111">I indkøbsvognmodulet gengives data baseret på indkøbsvogn-id'et, som er en browsercookie, der er tilgængelig på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="7b427-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="7b427-112">Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="7b427-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Eksempel på et indkøbvognmodul](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="7b427-114">Egenskaber og pladser i indkøbsvognmodulet</span><span class="sxs-lookup"><span data-stu-id="7b427-114">Cart module properties and slots</span></span>

<span data-ttu-id="7b427-115">Indkøbsvognmodulet har en **Overskrift**-egenskab, der kan angives til værdier som f.eks. **Indkøbspose** og **Varer i indkøbsvognen**.</span><span class="sxs-lookup"><span data-stu-id="7b427-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="7b427-116">Moduler, der kan bruges i et indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="7b427-117">**Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="7b427-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="7b427-118">Meddelelserne styres af CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="7b427-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="7b427-119">Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".</span><span class="sxs-lookup"><span data-stu-id="7b427-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="7b427-120">**Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="7b427-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7b427-121">Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden.</span><span class="sxs-lookup"><span data-stu-id="7b427-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7b427-122">Du kan få flere oplysninger om dette modul i [Butiksvælgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="7b427-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="7b427-123">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="7b427-123">Module properties</span></span>

<span data-ttu-id="7b427-124">De følgende indstillinger for indkøbsvognmodul kan konfigureres under **Indstillinger for websted \> Udvidelser**:</span><span class="sxs-lookup"><span data-stu-id="7b427-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7b427-125">**Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="7b427-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7b427-126">En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.</span><span class="sxs-lookup"><span data-stu-id="7b427-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7b427-127">**Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7b427-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="7b427-128">**Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**.</span><span class="sxs-lookup"><span data-stu-id="7b427-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="7b427-129">Ruten kan konfigureres på webstedsniveau, så detailhandlere kan føre kunden tilbage til startsiden eller en anden side på webstedet.</span><span class="sxs-lookup"><span data-stu-id="7b427-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7b427-130">Enhedsinteraktion i Commerce Scale</span><span class="sxs-lookup"><span data-stu-id="7b427-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7b427-131">Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er.</span><span class="sxs-lookup"><span data-stu-id="7b427-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="7b427-132">Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7b427-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="7b427-133">Føje et indkøbsvognmodul til en side</span><span class="sxs-lookup"><span data-stu-id="7b427-133">Add a cart module to a page</span></span>

<span data-ttu-id="7b427-134">Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7b427-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7b427-135">Gå til **Sidefragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="7b427-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7b427-136">Vælg modulet **Indkøbsvogn** i dialogboksen **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="7b427-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="7b427-137">Under **Sidefragmentsnavn** skal du angive navnet **Indkøbsvognfragment** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b427-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="7b427-138">Vælg **Indkøbsvogn**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="7b427-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="7b427-139">Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.</span><span class="sxs-lookup"><span data-stu-id="7b427-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="7b427-140">På pladsen **Indkøbsvogn** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="7b427-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7b427-141">I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b427-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7b427-142">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="7b427-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7b427-143">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="7b427-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7b427-144">Angiv et navn for skabelonen under **Skabelonnavn** i dialogboksen **Ny skabelon**.</span><span class="sxs-lookup"><span data-stu-id="7b427-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="7b427-145">Vælg pladsen **Brødtekst** i dispositionstræet, vælg ellipsen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="7b427-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="7b427-146">I dialogboksen **Vælg sidefragment** skal du vælge **Indkøbsvognfragmentet** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b427-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7b427-147">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="7b427-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7b427-148">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="7b427-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7b427-149">I dialogboksen **Vælg en skabelon** skal du vælge den skabelon, du har oprettet, angive et sidenavn og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b427-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="7b427-150">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="7b427-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7b427-151">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="7b427-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b427-152">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7b427-152">Additional resources</span></span>

[<span data-ttu-id="7b427-153">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="7b427-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7b427-154">Container-modul</span><span class="sxs-lookup"><span data-stu-id="7b427-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7b427-155">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="7b427-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="7b427-156">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="7b427-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7b427-157">Ikon for indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7b427-158">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7b427-159">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7b427-160">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7b427-161">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="7b427-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="7b427-162">Beregne lagertilgængelighed for detailkanaler</span><span class="sxs-lookup"><span data-stu-id="7b427-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
