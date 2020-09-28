---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 07d121d5a68970dd29f0e77babda735de12871ca
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761123"
---
# <a name="cart-module"></a><span data-ttu-id="7558a-103">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="7558a-103">Cart module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7558a-104">Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7558a-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7558a-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="7558a-105">Overview</span></span>

<span data-ttu-id="7558a-106">Et indkøbsvognmodul viser de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale.</span><span class="sxs-lookup"><span data-stu-id="7558a-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="7558a-107">Modulet viser også en ordreoversigt, og kunden kan anvende eller fjerne kampagnekoder.</span><span class="sxs-lookup"><span data-stu-id="7558a-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="7558a-108">Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst.</span><span class="sxs-lookup"><span data-stu-id="7558a-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="7558a-109">Den understøtter også et **Tilbage til indkøb**-link.</span><span class="sxs-lookup"><span data-stu-id="7558a-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="7558a-110">Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="7558a-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="7558a-111">I indkøbsvognmodulet gengives data baseret på indkøbsvogn-id'et, som er en browsercookie, der er tilgængelig på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="7558a-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="7558a-112">Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="7558a-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Eksempel på et indkøbvognmodul](./media/cart2.PNG)

<span data-ttu-id="7558a-114">Det følgende billede viser et eksempel på en side med en indkøbsvogn på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="7558a-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="7558a-115">I dette eksempel er der et ekspeditionsgebyr for et linjeelement.</span><span class="sxs-lookup"><span data-stu-id="7558a-115">In this example, there is a handling fee for a line item.</span></span>

![Eksempel på et indkøbvognmodul](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="7558a-117">Egenskaber og pladser i indkøbsvognmodulet</span><span class="sxs-lookup"><span data-stu-id="7558a-117">Cart module properties and slots</span></span>

| <span data-ttu-id="7558a-118">Egenskab</span><span class="sxs-lookup"><span data-stu-id="7558a-118">Property</span></span> | <span data-ttu-id="7558a-119">Værdier</span><span class="sxs-lookup"><span data-stu-id="7558a-119">Values</span></span> | <span data-ttu-id="7558a-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7558a-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="7558a-121">Overskrift</span><span class="sxs-lookup"><span data-stu-id="7558a-121">Heading</span></span> | <span data-ttu-id="7558a-122">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="7558a-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="7558a-123">En overskrift til vognen som f.eks. "Indkøbspose" eller "Varer i din indkøbsvogn".</span><span class="sxs-lookup"><span data-stu-id="7558a-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="7558a-124">Vis fejl for ikke på lager</span><span class="sxs-lookup"><span data-stu-id="7558a-124">Show out of stock errors</span></span> | <span data-ttu-id="7558a-125">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="7558a-125">**True** or **False**</span></span> | <span data-ttu-id="7558a-126">Hvis denne egenskab er angivet til **Sand**, vil der blive vist lagerrelaterede fejl på siden for indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="7558a-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="7558a-127">Det anbefales, at du angiver denne egenskab til **Sand**, hvis der anvendes lagerkontroller på lokationen.</span><span class="sxs-lookup"><span data-stu-id="7558a-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="7558a-128">Vis forsendelsesgebyrer for linjeelementer</span><span class="sxs-lookup"><span data-stu-id="7558a-128">Show shipping charges for line items</span></span> | <span data-ttu-id="7558a-129">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="7558a-129">**True** or **False**</span></span> | <span data-ttu-id="7558a-130">Hvis denne egenskab angives til **Sand**, vil linjeelementer i en indkøbsvogn vise forsendelsesgebyrer, hvis disse oplysninger er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="7558a-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="7558a-131">Denne funktion understøttes ikke i Fabrikam-temaet, da brugere først vælger levering i betalingsflowet.</span><span class="sxs-lookup"><span data-stu-id="7558a-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="7558a-132">Denne funktion kan dog aktiveres i andre arbejdsprocesser, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="7558a-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="7558a-133">Moduler, der kan bruges i et indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="7558a-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="7558a-134">**Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="7558a-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="7558a-135">Meddelelserne styres af CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="7558a-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="7558a-136">Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".</span><span class="sxs-lookup"><span data-stu-id="7558a-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="7558a-137">**Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="7558a-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7558a-138">Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden.</span><span class="sxs-lookup"><span data-stu-id="7558a-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7558a-139">Du kan få flere oplysninger om dette modul i [Butiksvælgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="7558a-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="7558a-140">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="7558a-140">Module properties</span></span>

<span data-ttu-id="7558a-141">De følgende indstillinger for indkøbsvognmodul kan konfigureres under **Indstillinger for websted \> Udvidelser**:</span><span class="sxs-lookup"><span data-stu-id="7558a-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7558a-142">**Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="7558a-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7558a-143">En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.</span><span class="sxs-lookup"><span data-stu-id="7558a-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7558a-144">**Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7558a-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="7558a-145">**Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**.</span><span class="sxs-lookup"><span data-stu-id="7558a-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="7558a-146">Ruten kan konfigureres på webstedsniveau, så detailhandlere kan føre kunden tilbage til startsiden eller en anden side på webstedet.</span><span class="sxs-lookup"><span data-stu-id="7558a-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7558a-147">Enhedsinteraktion i Commerce Scale</span><span class="sxs-lookup"><span data-stu-id="7558a-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7558a-148">Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er.</span><span class="sxs-lookup"><span data-stu-id="7558a-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="7558a-149">Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7558a-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="7558a-150">Føje et indkøbsvognmodul til en side</span><span class="sxs-lookup"><span data-stu-id="7558a-150">Add a cart module to a page</span></span>

<span data-ttu-id="7558a-151">Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7558a-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7558a-152">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="7558a-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7558a-153">Vælg modulet **Indkøbsvogn** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="7558a-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="7558a-154">Under **Fragmentnavn** skal du angive navnet **Indkøbsvognfragment** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7558a-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="7558a-155">Vælg **Indkøbsvogn**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="7558a-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="7558a-156">Vælg blyantsymbolet i ruden Egenskaber til højre. Skriv overskriften i feltet, og vælg derefter markeringssymbolet.</span><span class="sxs-lookup"><span data-stu-id="7558a-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="7558a-157">På pladsen **Indkøbsvogn** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="7558a-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7558a-158">I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7558a-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7558a-159">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="7558a-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7558a-160">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="7558a-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7558a-161">Angiv et navn for skabelonen under **Skabelonnavn** i dialogboksen **Ny skabelon**.</span><span class="sxs-lookup"><span data-stu-id="7558a-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="7558a-162">Vælg pladsen **Brødtekst** i dispositionstræet, vælg ellipsen (**...**), og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="7558a-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="7558a-163">I dialogboksen **Vælg fragment** skal du vælge **Indkøbsvognfragment** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7558a-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7558a-164">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="7558a-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7558a-165">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="7558a-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7558a-166">I dialogboksen **Vælg en skabelon** skal du vælge den skabelon, du har oprettet, angive et sidenavn og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7558a-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="7558a-167">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="7558a-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7558a-168">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="7558a-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7558a-169">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7558a-169">Additional resources</span></span>

[<span data-ttu-id="7558a-170">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="7558a-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7558a-171">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="7558a-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7558a-172">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="7558a-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7558a-173">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="7558a-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7558a-174">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="7558a-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="7558a-175">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="7558a-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7558a-176">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="7558a-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="7558a-177">Beregne lagertilgængelighed for detailkanaler</span><span class="sxs-lookup"><span data-stu-id="7558a-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
