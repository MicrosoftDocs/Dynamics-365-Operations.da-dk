---
title: Oversigt over sider med produktdetaljer
description: Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792213"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="73bbe-103">Oversigt over sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="73bbe-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="73bbe-104">Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="73bbe-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="73bbe-105">En PDP viser detaljerede oplysninger om et produkt og gør det muligt for kunderne at vælge produktindstillinger, f.eks. størrelse, stil og farve.</span><span class="sxs-lookup"><span data-stu-id="73bbe-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="73bbe-106">En PDP bør vise alle de produktoplysninger, en kunde har brug for til at kunne træffe en beslutning om køb.</span><span class="sxs-lookup"><span data-stu-id="73bbe-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="73bbe-107">Følgende illustration viser et eksempel på en PDP.</span><span class="sxs-lookup"><span data-stu-id="73bbe-107">The following illustration shows an example of a PDP.</span></span>

![Eksempel på en side med produktdetaljer](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="73bbe-109">Overskrifts- og sidefodsmoduler</span><span class="sxs-lookup"><span data-stu-id="73bbe-109">Header and footer modules</span></span>

<span data-ttu-id="73bbe-110">Den øverste del af en PDP har et sidehoved, der viser alle produktkategorierne og andre sider, som forhandleren ønsker, at kunderne skal gennemse.</span><span class="sxs-lookup"><span data-stu-id="73bbe-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="73bbe-111">Nederst på siden er der en sidefod, der indeholder hurtige links til forskellige emner, som kan have interesse for kunderne.</span><span class="sxs-lookup"><span data-stu-id="73bbe-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="73bbe-112">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="73bbe-112">Buy box module</span></span>

<span data-ttu-id="73bbe-113">Det vigtigste modul på en PDP er modulet med købsfeltet, som vises som det første element i hovedsektionen på siden.</span><span class="sxs-lookup"><span data-stu-id="73bbe-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="73bbe-114">I et købsfeltmodul vises vigtige produktoplysninger, f.eks. produktnavn, produktbeskrivelse, produktpris, produktbilleder og produktvurderinger.</span><span class="sxs-lookup"><span data-stu-id="73bbe-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="73bbe-115">I boksmodulet til køb kan kunden vælge produktindstillinger (f.eks. en størrelse, en stil og en farve) og føje produktet til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="73bbe-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="73bbe-116">Det giver også kunden mulighed for at købe produktet online og plukke det på et lager.</span><span class="sxs-lookup"><span data-stu-id="73bbe-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="73bbe-117">Køb online, og afhent i butikken-modulet bruger integration med Bing Kort-API'er (Application Programming Interfaces) til at finde butikker i nærheden eller butikker på et andet sted, som kunden angiver.</span><span class="sxs-lookup"><span data-stu-id="73bbe-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="73bbe-118">Et boksmodul til køb kræver et produkt-id.</span><span class="sxs-lookup"><span data-stu-id="73bbe-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="73bbe-119">Dette id er afledt af sidekonteksten.</span><span class="sxs-lookup"><span data-stu-id="73bbe-119">This ID is derived from the page context.</span></span> <span data-ttu-id="73bbe-120">Hvis der føjes et boksmodul til køb på en side, hvor sidekonteksten ikke indeholder et produkt-id, gengives oplysningerne ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="73bbe-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="73bbe-121">Modul til produktspecifikationer</span><span class="sxs-lookup"><span data-stu-id="73bbe-121">Product specifications module</span></span>

<span data-ttu-id="73bbe-122">Modulet til produktspecifikationer kan bruges til at vise yderligere oplysninger om produktet.</span><span class="sxs-lookup"><span data-stu-id="73bbe-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="73bbe-123">Disse oplysninger hentes fra produktattributter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="73bbe-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="73bbe-124">I modulet til produktspecifikationer vises alle attributter, hvor egenskaben **synlig** er angivet til **sand**.</span><span class="sxs-lookup"><span data-stu-id="73bbe-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="73bbe-125">Der kræves et produkt-id for at hente produktattributterne.</span><span class="sxs-lookup"><span data-stu-id="73bbe-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="73bbe-126">Anbefalingsmodulet</span><span class="sxs-lookup"><span data-stu-id="73bbe-126">Recommendations module</span></span>

<span data-ttu-id="73bbe-127">Anbefalingsmodulet er et vigtigt modul på en PDP.</span><span class="sxs-lookup"><span data-stu-id="73bbe-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="73bbe-128">Mens kunder søger efter produkter, bør der fremlægges flere produktmuligheder for dem, så de kan finde det rigtige produkt og foretage et køb.</span><span class="sxs-lookup"><span data-stu-id="73bbe-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="73bbe-129">Anbefalinger hjælper kunderne med nemt at finde relateret indhold og fortsætte med at handle.</span><span class="sxs-lookup"><span data-stu-id="73bbe-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="73bbe-130">Der findes forskellige typer af anbefalingslister:</span><span class="sxs-lookup"><span data-stu-id="73bbe-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="73bbe-131">Listen **Personer synes også om** er baseret på maskinel indlæring.</span><span class="sxs-lookup"><span data-stu-id="73bbe-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="73bbe-132">Den bruger transaktionshistorikken fra andre kunder til at give anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="73bbe-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="73bbe-133">Denne liste genereres af anbefalingstjenesten og minder om listetypen "Kunder, der købte dette, købte også...".</span><span class="sxs-lookup"><span data-stu-id="73bbe-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="73bbe-134">Der kræves et produkt-id for at generere denne liste.</span><span class="sxs-lookup"><span data-stu-id="73bbe-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="73bbe-135">Der kan konfigureres en **Relateret**-liste for et produkt i Commerce.</span><span class="sxs-lookup"><span data-stu-id="73bbe-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="73bbe-136">Til en brun rejsetaske i læder kan der f.eks. være konfigureret flere tasker, der er fremstillet af læder eller designet til rejsebrug, på den relaterede liste.</span><span class="sxs-lookup"><span data-stu-id="73bbe-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="73bbe-137">Andre typer af relaterede lister som f.eks. **Tilbehør** og **Mere som dette** kan også konfigureres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="73bbe-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="73bbe-138">Der kræves et produkt-id for at generere denne liste.</span><span class="sxs-lookup"><span data-stu-id="73bbe-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="73bbe-139">Hvis sidekonteksten ikke omfatter et produkt-id, vil listen derfor være tom, hvis den føjes til en startside.</span><span class="sxs-lookup"><span data-stu-id="73bbe-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="73bbe-140">Algoritmisk genererede anbefalingslister, f.eks. **Mest populære**, **Mest solgte** og **Nyt**, kan bruges på PDP'er.</span><span class="sxs-lookup"><span data-stu-id="73bbe-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="73bbe-141">Selvom disse lister ikke er direkte relateret til produktet på PDP, kan de også hjælpe kunderne med at finde produkter, der er interessante for dem.</span><span class="sxs-lookup"><span data-stu-id="73bbe-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="73bbe-142">Disse typer lister kræver ikke et produkt-id.</span><span class="sxs-lookup"><span data-stu-id="73bbe-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="73bbe-143">De er standardlister, der genereres på basis af indkøbsmønstre på tværs af webstedet.</span><span class="sxs-lookup"><span data-stu-id="73bbe-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="73bbe-144">Redaktionelle lister er manuelt fremstillede lister.</span><span class="sxs-lookup"><span data-stu-id="73bbe-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="73bbe-145">En forhandler kan f.eks. manuelt fremstille lister over produkter, der skal vises frem.</span><span class="sxs-lookup"><span data-stu-id="73bbe-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="73bbe-146">Moduler til vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="73bbe-146">Ratings and reviews modules</span></span>

<span data-ttu-id="73bbe-147">Tre moduler kan bruges til at vise og tilføje anmeldelser:</span><span class="sxs-lookup"><span data-stu-id="73bbe-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="73bbe-148">**Anmeldelser** – Modulet indeholder vurderinger og anmeldelser, der er leveret af andre kunder.</span><span class="sxs-lookup"><span data-stu-id="73bbe-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="73bbe-149">Kunderne kan sortere og filtrere anmeldelserne.</span><span class="sxs-lookup"><span data-stu-id="73bbe-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="73bbe-150">Dette modul giver også kunder mulighed for at synes om eller ikke synes om anmeldelser, og de kan rapportere problemer.</span><span class="sxs-lookup"><span data-stu-id="73bbe-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="73bbe-151">**Skriv anmeldelse** – Med dette modul kan kunderne skrive deres egne anmeldelser af et produkt.</span><span class="sxs-lookup"><span data-stu-id="73bbe-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="73bbe-152">**Vurderingshistogram** – Dette modul indeholder et histogram, der viser vurderingstendensen for et produkt.</span><span class="sxs-lookup"><span data-stu-id="73bbe-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="73bbe-153">Du kan finde flere oplysninger under [Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73bbe-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="73bbe-154">Marketingmoduler</span><span class="sxs-lookup"><span data-stu-id="73bbe-154">Marketing modules</span></span>

<span data-ttu-id="73bbe-155">Hvis marketingindhold er entydigt for et bestemt produkt, kan der føjes et marketingmodul til PDP.</span><span class="sxs-lookup"><span data-stu-id="73bbe-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="73bbe-156">Du kan føje marketingmoduler til en PDP ved at "forbedre" siden.</span><span class="sxs-lookup"><span data-stu-id="73bbe-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="73bbe-157">Du kan finde flere oplysninger under [Forbedre en produktside](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="73bbe-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73bbe-158">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="73bbe-158">Additional resources</span></span>

[<span data-ttu-id="73bbe-159">Oversigt over startside</span><span class="sxs-lookup"><span data-stu-id="73bbe-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="73bbe-160">Oversigt over sider til indkøbsvogn og betaling ved kassen</span><span class="sxs-lookup"><span data-stu-id="73bbe-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="73bbe-161">Oversigt over sider til kontostyring</span><span class="sxs-lookup"><span data-stu-id="73bbe-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="73bbe-162">Forbedre en side med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="73bbe-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
