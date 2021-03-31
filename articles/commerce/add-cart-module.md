---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvogn-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5b0ce69f57e6ba691803752280466b41ced7c521
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206481"
---
# <a name="cart-module"></a><span data-ttu-id="d481b-103">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="d481b-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d481b-104">Dette emne omhandler indkøbsvogn-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d481b-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d481b-105">Et indkøbsvognmodul viser de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale.</span><span class="sxs-lookup"><span data-stu-id="d481b-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="d481b-106">Modulet viser også en ordreoversigt, og kunden kan anvende eller fjerne kampagnekoder.</span><span class="sxs-lookup"><span data-stu-id="d481b-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="d481b-107">Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst.</span><span class="sxs-lookup"><span data-stu-id="d481b-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="d481b-108">Den understøtter også et **Tilbage til indkøb**-link.</span><span class="sxs-lookup"><span data-stu-id="d481b-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="d481b-109">Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="d481b-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="d481b-110">I indkøbsvognmodulet gengives data baseret på indkøbsvogn-id'et, som er en browsercookie, der er tilgængelig på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="d481b-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="d481b-111">Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="d481b-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Eksempel på et indkøbsvognmodul på Fabrikam-webstedet](./media/cart2.PNG)

<span data-ttu-id="d481b-113">Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="d481b-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="d481b-114">I dette eksempel er der et ekspeditionsgebyr for et linjeelement.</span><span class="sxs-lookup"><span data-stu-id="d481b-114">In this example, there is a handling fee for a line item.</span></span>

![Eksempel på et indkøbsvognmodul med et ekspeditionsgebyr for et linjeelement](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="d481b-116">Egenskaber og pladser i indkøbsvognmodulet</span><span class="sxs-lookup"><span data-stu-id="d481b-116">Cart module properties and slots</span></span>

| <span data-ttu-id="d481b-117">Egenskab</span><span class="sxs-lookup"><span data-stu-id="d481b-117">Property</span></span> | <span data-ttu-id="d481b-118">Værdier</span><span class="sxs-lookup"><span data-stu-id="d481b-118">Values</span></span> | <span data-ttu-id="d481b-119">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="d481b-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d481b-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="d481b-120">Heading</span></span> | <span data-ttu-id="d481b-121">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="d481b-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d481b-122">En overskrift til vognen som f.eks. "Indkøbspose" eller "Varer i din indkøbsvogn".</span><span class="sxs-lookup"><span data-stu-id="d481b-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="d481b-123">Vis fejl for ikke på lager</span><span class="sxs-lookup"><span data-stu-id="d481b-123">Show out of stock errors</span></span> | <span data-ttu-id="d481b-124">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="d481b-124">**True** or **False**</span></span> | <span data-ttu-id="d481b-125">Hvis denne egenskab er angivet til **Sand**, vil der blive vist lagerrelaterede fejl på siden for indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="d481b-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="d481b-126">Det anbefales, at du angiver denne egenskab til **Sand**, hvis der anvendes lagerkontroller på lokationen.</span><span class="sxs-lookup"><span data-stu-id="d481b-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="d481b-127">Vis forsendelsesgebyrer for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="d481b-127">Show shipping charges for line items</span></span> | <span data-ttu-id="d481b-128">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="d481b-128">**True** or **False**</span></span> | <span data-ttu-id="d481b-129">Hvis denne egenskab angives til **Sand**, vil linjeelementer i en indkøbsvogn vise forsendelsesgebyrer, hvis disse oplysninger er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="d481b-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="d481b-130">Denne funktion understøttes ikke i Fabrikam-temaet, da brugere først vælger levering i betalingsflowet.</span><span class="sxs-lookup"><span data-stu-id="d481b-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="d481b-131">Denne funktion kan dog aktiveres i andre arbejdsprocesser, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="d481b-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="d481b-132">Vis tilgængelige opprioriteringer</span><span class="sxs-lookup"><span data-stu-id="d481b-132">Show available promotions</span></span>| <span data-ttu-id="d481b-133">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="d481b-133">**True** or **False**</span></span> | <span data-ttu-id="d481b-134">Hvis denne egenskab er angivet til **Sand**, viser indkøbsvognen tilgængelige kampagner baseret på varerne i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="d481b-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="d481b-135">Denne egenskab er tilgængelig i version 10.0.16 af Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d481b-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="d481b-136">Moduler, der kan bruges i et indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="d481b-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="d481b-137">**Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="d481b-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="d481b-138">Meddelelserne styres af CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="d481b-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="d481b-139">Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".</span><span class="sxs-lookup"><span data-stu-id="d481b-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="d481b-140">**Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="d481b-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="d481b-141">Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden.</span><span class="sxs-lookup"><span data-stu-id="d481b-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="d481b-142">Du kan få flere oplysninger om dette modul i [Butiksvælgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d481b-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="d481b-143">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="d481b-143">Module properties</span></span>

<span data-ttu-id="d481b-144">De følgende indstillinger for indkøbsvognmodul kan konfigureres under **Indstillinger for websted \> Udvidelser**:</span><span class="sxs-lookup"><span data-stu-id="d481b-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="d481b-145">**Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="d481b-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="d481b-146">En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.</span><span class="sxs-lookup"><span data-stu-id="d481b-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="d481b-147">**Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d481b-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="d481b-148">**Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**.</span><span class="sxs-lookup"><span data-stu-id="d481b-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="d481b-149">Ruten kan konfigureres på webstedsniveau, så detailhandlere kan føre kunden tilbage til startsiden eller en anden side på webstedet.</span><span class="sxs-lookup"><span data-stu-id="d481b-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d481b-150">I Dynamics 365 Commerce version 10.0.14 og senere samles varerne i indkøbsvognen ud fra de indstillinger, der er defineret i online funktionalitetsprofilen for onlinebutikken i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d481b-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="d481b-151">Du kan finde flere oplysninger om, hvordan du opretter en online funktionalitetsprofil og angiver de egenskaber, der kræves til aggregering, i afsnittet [Oprette en online funktionalitetsprofil](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="d481b-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="d481b-152">Enhedsinteraktion i Commerce Scale</span><span class="sxs-lookup"><span data-stu-id="d481b-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="d481b-153">Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er.</span><span class="sxs-lookup"><span data-stu-id="d481b-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="d481b-154">Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="d481b-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="d481b-155">Føje et indkøbsvognmodul til en side</span><span class="sxs-lookup"><span data-stu-id="d481b-155">Add a cart module to a page</span></span>

<span data-ttu-id="d481b-156">Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d481b-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d481b-157">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="d481b-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d481b-158">Vælg modulet **Indkøbsvogn** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="d481b-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="d481b-159">Under **Fragmentnavn** skal du angive navnet **Indkøbsvognfragment** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="d481b-160">Vælg **Indkøbsvogn**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="d481b-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="d481b-161">Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.</span><span class="sxs-lookup"><span data-stu-id="d481b-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="d481b-162">På pladsen **Indkøbsvogn** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="d481b-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d481b-163">I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d481b-164">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="d481b-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d481b-165">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="d481b-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d481b-166">Angiv et navn for skabelonen under **Skabelonnavn** i dialogboksen **Ny skabelon**.</span><span class="sxs-lookup"><span data-stu-id="d481b-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="d481b-167">Vælg pladsen **Brødtekst** i dispositionstræet, vælg ellipsen (**...**), og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="d481b-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d481b-168">I dialogboksen **Vælg fragment** skal du vælge **Indkøbsvognfragment** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d481b-169">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="d481b-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d481b-170">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="d481b-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d481b-171">I dialogboksen **Vælg en skabelon** skal du vælge den skabelon, du har oprettet, angive et sidenavn og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="d481b-172">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="d481b-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d481b-173">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="d481b-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d481b-174">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d481b-174">Additional resources</span></span>

[<span data-ttu-id="d481b-175">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="d481b-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d481b-176">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="d481b-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d481b-177">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="d481b-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d481b-178">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="d481b-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d481b-179">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="d481b-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d481b-180">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="d481b-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d481b-181">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="d481b-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d481b-182">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="d481b-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="d481b-183">Beregne lagertilgængelighed for detailkanaler</span><span class="sxs-lookup"><span data-stu-id="d481b-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="d481b-184">Oprette en onlinefunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="d481b-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]