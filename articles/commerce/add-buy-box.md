---
title: Købefeltmodul
description: Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686664"
---
# <a name="buy-box-module"></a><span data-ttu-id="c4baa-103">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c4baa-104">Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c4baa-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c4baa-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="c4baa-105">Overview</span></span>

<span data-ttu-id="c4baa-106">Termen *købefelt* refererer normalt til det område på en produktdetaljeside, der er "over folden", og som omfatter alle de vigtigste oplysninger, der kræves for at foretage et produktkøb.</span><span class="sxs-lookup"><span data-stu-id="c4baa-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="c4baa-107">(et område, der er "over folden", er synligt med det samme, når siden indlæses, så brugerne ikke behøver at rulle ned for at se den).</span><span class="sxs-lookup"><span data-stu-id="c4baa-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="c4baa-108">Et købefeltmodul er en særlig container, der omfatter alle de moduler, som vises i købefeltområdet på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4baa-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="c4baa-109">URL-adressen for siden produktdetaljer indeholder produkt-id'et.</span><span class="sxs-lookup"><span data-stu-id="c4baa-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="c4baa-110">Alle de oplysninger, der kræves for at gengive et købefeltmodul, er afledt af dette produkt-id.</span><span class="sxs-lookup"><span data-stu-id="c4baa-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="c4baa-111">Hvis der ikke er angivet et produkt-ID, gengives købefeltmodulet ikke korrekt på en side.</span><span class="sxs-lookup"><span data-stu-id="c4baa-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="c4baa-112">Derfor kan et købsfeltmodul kun bruges på sider med en produktkontekst.</span><span class="sxs-lookup"><span data-stu-id="c4baa-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="c4baa-113">Hvis du vil bruge den på en side, der ikke har en produktkontekst (f.eks. en startside eller en marketingside), skal du udføre flere tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="c4baa-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="c4baa-114">Det følgende billede viser et eksempel på et købefeltmodul på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4baa-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Eksempel på et købefeltmodul](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="c4baa-116">Egenskaber og pladser i købefeltmodulet</span><span class="sxs-lookup"><span data-stu-id="c4baa-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="c4baa-117">På siden med produktdetaljer er et købefelt opdelt i to områder: et medieområde til venstre og et indholdsområde til højre.</span><span class="sxs-lookup"><span data-stu-id="c4baa-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="c4baa-118">Forholdet mellem bredden af kolonnen med medieområder og bredden af kolonnen med indholdsområder er som standard 2:1.</span><span class="sxs-lookup"><span data-stu-id="c4baa-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="c4baa-119">På mobile enheder er de to områder stablet, så det ene område vises under det andet område.</span><span class="sxs-lookup"><span data-stu-id="c4baa-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="c4baa-120">Du kan bruge temaer til at tilpasse kolonnebredder og stablingsrangering.</span><span class="sxs-lookup"><span data-stu-id="c4baa-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="c4baa-121">I et købsfeltmodul vises titlen, beskrivelsen, prisen og klassifikationen for et produkt.</span><span class="sxs-lookup"><span data-stu-id="c4baa-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="c4baa-122">Kunderne kan også vælge produktvarianter, der har forskellige produktattributter, f.eks. størrelse, typografi og farve.</span><span class="sxs-lookup"><span data-stu-id="c4baa-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="c4baa-123">Når der er valgt en produktvariant, opdateres andre egenskaber i købefeltet (f. eks. produktbeskrivelsen og -billederne), så de afspejler variantoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="c4baa-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="c4baa-124">Der angives en mængdevælger, så debitorer kan angive antallet af varer, der skal købes.</span><span class="sxs-lookup"><span data-stu-id="c4baa-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="c4baa-125">Det maksimale antal, der kan købes, kan defineres i indstillingerne for webstedet.</span><span class="sxs-lookup"><span data-stu-id="c4baa-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="c4baa-126">Fra købsfeltet kan kunderne også udføre handlinger, som f.eks. føje et produkt til indkøbsvognen, føje et produkt til ønskelisten og vælge et afhentningssted.</span><span class="sxs-lookup"><span data-stu-id="c4baa-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="c4baa-127">Disse handlinger kan udføres på et produkt eller en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="c4baa-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="c4baa-128">Hvis du vil føje et produkt til en ønskeliste, skal kunden være logget på.</span><span class="sxs-lookup"><span data-stu-id="c4baa-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="c4baa-129">Temaer kan bruges til at fjerne eller ændre rækkefølgen af købsfeltets produktegenskaber og handlingskontroller.</span><span class="sxs-lookup"><span data-stu-id="c4baa-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="c4baa-130">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="c4baa-130">Module properties</span></span>

- <span data-ttu-id="c4baa-131">**Overskriftskode** – Denne egenskab definerer overskriftskoden for produkttitlen.</span><span class="sxs-lookup"><span data-stu-id="c4baa-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="c4baa-132">Hvis købsfeltet vises øverst på siden, skal denne egenskab indstilles til **h1** for at overholde tilgængelighedsstandarder.</span><span class="sxs-lookup"><span data-stu-id="c4baa-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="c4baa-133">Moduler, der kan bruges i et købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="c4baa-134">**Mediegalleri** – dette modul bruges til at vise billeder af et produkt på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4baa-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="c4baa-135">Yderligere oplysninger om dette modul finder du i [Mediegallerimodul](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="c4baa-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="c4baa-136">**Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="c4baa-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="c4baa-137">Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden.</span><span class="sxs-lookup"><span data-stu-id="c4baa-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="c4baa-138">Yderligere oplysninger om dette modul finder du i [Butiksvælgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="c4baa-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="c4baa-139">Indstillinger for købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-139">Buy box module settings</span></span>

<span data-ttu-id="c4baa-140">De følgende indstillinger for købefeltmoduler kan konfigureres under **Indstillinger for websted \> Udvidelser**:</span><span class="sxs-lookup"><span data-stu-id="c4baa-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="c4baa-141">**Grænse for antal linjevarer i indkøbsvogn** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="c4baa-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="c4baa-142">En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.</span><span class="sxs-lookup"><span data-stu-id="c4baa-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="c4baa-143">**Lager** – Du finder oplysninger om, hvordan du anvender lagerindstillinger, under [Anvendelse af lagerindstillinger](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c4baa-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="c4baa-144">**Føj til indkøbsvogn** – Denne egenskab bruges til at angive proceduren, når en vare er føjet til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="c4baa-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="c4baa-145">De mulige værdier er **Naviger til indkøbsvogn**, **Naviger ikke til indkøbsvogn** og **Vis beskeder**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="c4baa-146">Når værdien er angivet til **Naviger til indkøbsvogn**, sendes brugeren til indkøbsvognen, når der er tilføjet en vare.</span><span class="sxs-lookup"><span data-stu-id="c4baa-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="c4baa-147">Når værdien er angivet til **Naviger ikke til indkøbsvogn**, sendes brugeren ikke til siden med indkøbsvognen, når der er tilføjet en vare.</span><span class="sxs-lookup"><span data-stu-id="c4baa-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="c4baa-148">Når værdien er angivet til **Vis beskeder**, får brugerne vist en bekræftelsesmeddelelse og kan fortsætte med at søge på siden produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4baa-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="c4baa-149">Det følgende billede viser et eksempel på en besked med bekræftelse af handlingen "Føjet til indkøbsvogn" på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="c4baa-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Eksempel på et beskedmodul](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="c4baa-151">Enhedsinteraktion i Commerce Scale</span><span class="sxs-lookup"><span data-stu-id="c4baa-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="c4baa-152">Købsfeltmodulet henter produktoplysninger ved hjælp af Commerce Scale Unit-API'er (Application Programming Interfaces).</span><span class="sxs-lookup"><span data-stu-id="c4baa-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="c4baa-153">Produkt-id'et fra siden med produktdetaljer bruges til at hente alle oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c4baa-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="c4baa-154">Føje et købefeltmodul til en side</span><span class="sxs-lookup"><span data-stu-id="c4baa-154">Add a buy box module to a page</span></span>

<span data-ttu-id="c4baa-155">Hvis du vil føje et købefeltmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c4baa-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c4baa-156">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="c4baa-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="c4baa-157">Vælg modulet **Købefelt** i dialogboksen **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="c4baa-158">Under **Sidefragmentnavn** skal du angive navnet **Købefeltfragment** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-159">På pladsen **Media Gallery** i købefeltmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4baa-160">I dialogboksen **Tilføj modul** skal du vælge modulet **Media Gallery** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-161">På pladsen **Butiksvælger** i købefeltmodulet skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4baa-162">I dialogboksen **Tilføj modul** skal du vælge modulet **Butiksvælger** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-163">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="c4baa-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c4baa-164">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="c4baa-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c4baa-165">Angiv **PDP-skabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-166">På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4baa-167">dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-168">Vælg pladsen **Hoved** på standardsiden, vælg ellipsen (**...**) og derefter **Tilføj sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="c4baa-169">I dialogboksen **Vælg sidefragment** skal du vælge det **Købefeltfragment**, som du tidligere har valgt, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-170">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="c4baa-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c4baa-171">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="c4baa-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c4baa-172">Vælg dialogboksen **Vælg en skabelon**, og vælg skabelonen **PDP-skabelon**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="c4baa-173">Under **Sidenavn** skal du angive **PDP-side** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-174">Vælg pladsen **Hoved** på den nye side, vælg ellipsen (**...**), og vælg derefter **Tilføj sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="c4baa-175">I dialogboksen **Vælg sidefragment** skal du vælge det **Købefeltfragment**, som du tidligere har valgt, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4baa-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="c4baa-176">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="c4baa-176">Save and preview the page.</span></span> <span data-ttu-id="c4baa-177">Føj forespørgselsstrengparameteren **?productid=&lt;product id&gt;** til URL-adressen for eksempelsiden.</span><span class="sxs-lookup"><span data-stu-id="c4baa-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="c4baa-178">På denne måde bruges produktkonteksten til at indlæse og gengive eksempelsiden.</span><span class="sxs-lookup"><span data-stu-id="c4baa-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="c4baa-179">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="c4baa-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="c4baa-180">Der vises et købefelt på siden med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4baa-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4baa-181">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c4baa-181">Additional resources</span></span>

[<span data-ttu-id="c4baa-182">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="c4baa-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c4baa-183">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c4baa-184">Mediegallerimodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="c4baa-185">Container-modul</span><span class="sxs-lookup"><span data-stu-id="c4baa-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c4baa-186">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c4baa-187">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="c4baa-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c4baa-188">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c4baa-189">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c4baa-190">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c4baa-191">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="c4baa-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="c4baa-192">Beregne lagertilgængelighed for detailkanaler</span><span class="sxs-lookup"><span data-stu-id="c4baa-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
