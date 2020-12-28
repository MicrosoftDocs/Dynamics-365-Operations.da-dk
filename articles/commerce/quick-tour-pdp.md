---
title: Oversigt over sider med produktdetaljer
description: Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411185"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="fda9b-103">Oversigt over sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="fda9b-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fda9b-104">Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fda9b-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fda9b-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="fda9b-105">Overview</span></span>

<span data-ttu-id="fda9b-106">En PDP viser detaljerede oplysninger om et produkt og gør det muligt for kunderne at vælge produktindstillinger, f.eks. størrelse, stil og farve.</span><span class="sxs-lookup"><span data-stu-id="fda9b-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="fda9b-107">En PDP bør vise alle de produktoplysninger, en kunde har brug for til at kunne træffe en beslutning om køb.</span><span class="sxs-lookup"><span data-stu-id="fda9b-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="fda9b-108">Følgende illustration viser et eksempel på en PDP.</span><span class="sxs-lookup"><span data-stu-id="fda9b-108">The following illustration shows an example of a PDP.</span></span>

![Eksempel på en side med produktdetaljer](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="fda9b-110">Overskrifts- og sidefodsmoduler</span><span class="sxs-lookup"><span data-stu-id="fda9b-110">Header and footer modules</span></span>

<span data-ttu-id="fda9b-111">Den øverste del af en PDP har et sidehoved, der viser alle produktkategorierne og andre sider, som forhandleren ønsker, at kunderne skal gennemse.</span><span class="sxs-lookup"><span data-stu-id="fda9b-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="fda9b-112">Nederst på siden er der en sidefod, der indeholder hurtige links til forskellige emner, som kan have interesse for kunderne.</span><span class="sxs-lookup"><span data-stu-id="fda9b-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="fda9b-113">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="fda9b-113">Buy box module</span></span>

<span data-ttu-id="fda9b-114">Det vigtigste modul på en PDP er modulet med købsfeltet, som vises som det første element i hovedsektionen på siden.</span><span class="sxs-lookup"><span data-stu-id="fda9b-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="fda9b-115">I et købsfeltmodul vises vigtige produktoplysninger, f.eks. produktnavn, produktbeskrivelse, produktpris, produktbilleder og produktvurderinger.</span><span class="sxs-lookup"><span data-stu-id="fda9b-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="fda9b-116">I boksmodulet til køb kan kunden vælge produktindstillinger (f.eks. en størrelse, en stil og en farve) og føje produktet til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="fda9b-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="fda9b-117">Det giver også kunden mulighed for at købe produktet online og plukke det på et lager.</span><span class="sxs-lookup"><span data-stu-id="fda9b-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="fda9b-118">Køb online, og afhent i butikken-modulet bruger integration med Bing Kort-API'er (Application Programming Interfaces) til at finde butikker i nærheden eller butikker på et andet sted, som kunden angiver.</span><span class="sxs-lookup"><span data-stu-id="fda9b-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="fda9b-119">Et boksmodul til køb kræver et produkt-id.</span><span class="sxs-lookup"><span data-stu-id="fda9b-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="fda9b-120">Dette id er afledt af sidekonteksten.</span><span class="sxs-lookup"><span data-stu-id="fda9b-120">This ID is derived from the page context.</span></span> <span data-ttu-id="fda9b-121">Hvis der føjes et boksmodul til køb på en side, hvor sidekonteksten ikke indeholder et produkt-id, gengives oplysningerne ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="fda9b-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="fda9b-122">Modul til produktspecifikationer</span><span class="sxs-lookup"><span data-stu-id="fda9b-122">Product specifications module</span></span>

<span data-ttu-id="fda9b-123">Modulet til produktspecifikationer kan bruges til at vise yderligere oplysninger om produktet.</span><span class="sxs-lookup"><span data-stu-id="fda9b-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="fda9b-124">Disse oplysninger hentes fra produktattributter i Commerce.</span><span class="sxs-lookup"><span data-stu-id="fda9b-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="fda9b-125">I modulet til produktspecifikationer vises alle attributter, hvor egenskaben **synlig** er angivet til **sand**.</span><span class="sxs-lookup"><span data-stu-id="fda9b-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="fda9b-126">Der kræves et produkt-id for at hente produktattributterne.</span><span class="sxs-lookup"><span data-stu-id="fda9b-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="fda9b-127">Anbefalingsmodulet</span><span class="sxs-lookup"><span data-stu-id="fda9b-127">Recommendations module</span></span>

<span data-ttu-id="fda9b-128">Anbefalingsmodulet er et vigtigt modul på en PDP.</span><span class="sxs-lookup"><span data-stu-id="fda9b-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="fda9b-129">Mens kunder søger efter produkter, bør der fremlægges flere produktmuligheder for dem, så de kan finde det rigtige produkt og foretage et køb.</span><span class="sxs-lookup"><span data-stu-id="fda9b-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="fda9b-130">Anbefalinger hjælper kunderne med nemt at finde relateret indhold og fortsætte med at handle.</span><span class="sxs-lookup"><span data-stu-id="fda9b-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="fda9b-131">Der findes forskellige typer af anbefalingslister:</span><span class="sxs-lookup"><span data-stu-id="fda9b-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="fda9b-132">Listen **Personer synes også om** er baseret på maskinel indlæring.</span><span class="sxs-lookup"><span data-stu-id="fda9b-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="fda9b-133">Den bruger transaktionshistorikken fra andre kunder til at give anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="fda9b-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="fda9b-134">Denne liste genereres af anbefalingstjenesten og minder om listetypen "Kunder, der købte dette, købte også...".</span><span class="sxs-lookup"><span data-stu-id="fda9b-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="fda9b-135">Der kræves et produkt-id for at generere denne liste.</span><span class="sxs-lookup"><span data-stu-id="fda9b-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="fda9b-136">Der kan konfigureres en **Relateret**-liste for et produkt i Commerce.</span><span class="sxs-lookup"><span data-stu-id="fda9b-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="fda9b-137">Til en brun rejsetaske i læder kan der f.eks. være konfigureret flere tasker, der er fremstillet af læder eller designet til rejsebrug, på den relaterede liste.</span><span class="sxs-lookup"><span data-stu-id="fda9b-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="fda9b-138">Andre typer af relaterede lister som f.eks. **Tilbehør** og **Mere som dette** kan også konfigureres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="fda9b-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="fda9b-139">Der kræves et produkt-id for at generere denne liste.</span><span class="sxs-lookup"><span data-stu-id="fda9b-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="fda9b-140">Hvis sidekonteksten ikke omfatter et produkt-id, vil listen derfor være tom, hvis den føjes til en startside.</span><span class="sxs-lookup"><span data-stu-id="fda9b-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="fda9b-141">Algoritmisk genererede anbefalingslister, f.eks. **Mest populære**, **Mest solgte** og **Nyt**, kan bruges på PDP'er.</span><span class="sxs-lookup"><span data-stu-id="fda9b-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="fda9b-142">Selvom disse lister ikke er direkte relateret til produktet på PDP, kan de også hjælpe kunderne med at finde produkter, der er interessante for dem.</span><span class="sxs-lookup"><span data-stu-id="fda9b-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="fda9b-143">Disse typer lister kræver ikke et produkt-id.</span><span class="sxs-lookup"><span data-stu-id="fda9b-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="fda9b-144">De er standardlister, der genereres på basis af indkøbsmønstre på tværs af webstedet.</span><span class="sxs-lookup"><span data-stu-id="fda9b-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="fda9b-145">Redaktionelle lister er manuelt fremstillede lister.</span><span class="sxs-lookup"><span data-stu-id="fda9b-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="fda9b-146">En forhandler kan f.eks. manuelt fremstille lister over produkter, der skal vises frem.</span><span class="sxs-lookup"><span data-stu-id="fda9b-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="fda9b-147">Moduler til vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="fda9b-147">Ratings and reviews modules</span></span>

<span data-ttu-id="fda9b-148">Tre moduler kan bruges til at vise og tilføje anmeldelser:</span><span class="sxs-lookup"><span data-stu-id="fda9b-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="fda9b-149">**Anmeldelser** – Modulet indeholder vurderinger og anmeldelser, der er leveret af andre kunder.</span><span class="sxs-lookup"><span data-stu-id="fda9b-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="fda9b-150">Kunderne kan sortere og filtrere anmeldelserne.</span><span class="sxs-lookup"><span data-stu-id="fda9b-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="fda9b-151">Dette modul giver også kunder mulighed for at synes om eller ikke synes om anmeldelser, og de kan rapportere problemer.</span><span class="sxs-lookup"><span data-stu-id="fda9b-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="fda9b-152">**Skriv anmeldelse** – Med dette modul kan kunderne skrive deres egne anmeldelser af et produkt.</span><span class="sxs-lookup"><span data-stu-id="fda9b-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="fda9b-153">**Vurderingshistogram** – Dette modul indeholder et histogram, der viser vurderingstendensen for et produkt.</span><span class="sxs-lookup"><span data-stu-id="fda9b-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="fda9b-154">Du kan finde flere oplysninger under [Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fda9b-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="fda9b-155">Marketingmoduler</span><span class="sxs-lookup"><span data-stu-id="fda9b-155">Marketing modules</span></span>

<span data-ttu-id="fda9b-156">Hvis marketingindhold er entydigt for et bestemt produkt, kan der føjes et marketingmodul til PDP.</span><span class="sxs-lookup"><span data-stu-id="fda9b-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="fda9b-157">Du kan føje marketingmoduler til en PDP ved at "forbedre" siden.</span><span class="sxs-lookup"><span data-stu-id="fda9b-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="fda9b-158">Du kan finde flere oplysninger under [Forbedre en produktside](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="fda9b-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fda9b-159">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fda9b-159">Additional resources</span></span>

[<span data-ttu-id="fda9b-160">Oversigt over startside</span><span class="sxs-lookup"><span data-stu-id="fda9b-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="fda9b-161">Oversigt over sider til indkøbsvogn og betaling ved kassen</span><span class="sxs-lookup"><span data-stu-id="fda9b-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="fda9b-162">Oversigt over sider til kontostyring</span><span class="sxs-lookup"><span data-stu-id="fda9b-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="fda9b-163">Forbedre en side med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="fda9b-163">Enrich a product details page</span></span>](enrich-product-page.md)
