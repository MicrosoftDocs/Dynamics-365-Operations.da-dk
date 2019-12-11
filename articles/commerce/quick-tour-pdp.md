---
title: Oversigt over sider med produktdetaljer
description: Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697859"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="8cae7-103">Oversigt over sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="8cae7-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8cae7-104">Dette emne indeholder en oversigt over sider med produktdetaljer (PDP'er) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8cae7-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8cae7-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="8cae7-105">Overview</span></span>

<span data-ttu-id="8cae7-106">En PDP viser detaljerede oplysninger om et produkt og gør det muligt for kunderne at vælge produktindstillinger, f.eks. størrelse, stil og farve.</span><span class="sxs-lookup"><span data-stu-id="8cae7-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="8cae7-107">En PDP bør vise alle de produktoplysninger, en kunde har brug for til at kunne træffe en beslutning om køb.</span><span class="sxs-lookup"><span data-stu-id="8cae7-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="8cae7-108">Følgende illustration viser et eksempel på en PDP.</span><span class="sxs-lookup"><span data-stu-id="8cae7-108">The following illustration shows an example of a PDP.</span></span>

![Eksempel på en side med produktdetaljer](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="8cae7-110">Overskrifts- og sidefodsmoduler</span><span class="sxs-lookup"><span data-stu-id="8cae7-110">Header and footer modules</span></span>

<span data-ttu-id="8cae7-111">Den øverste del af en PDP har et sidehoved, der viser alle produktkategorierne og andre sider, som forhandleren ønsker, at kunderne skal gennemse.</span><span class="sxs-lookup"><span data-stu-id="8cae7-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="8cae7-112">Nederst på siden er der en sidefod, der indeholder hurtige links til forskellige emner, som kan have interesse for kunderne.</span><span class="sxs-lookup"><span data-stu-id="8cae7-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="8cae7-113">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="8cae7-113">Buy box module</span></span>

<span data-ttu-id="8cae7-114">Det vigtigste modul på en PDP er boksmodulet til køb.</span><span class="sxs-lookup"><span data-stu-id="8cae7-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="8cae7-115">Det er derfor det første element i hovedsektionen på siden.</span><span class="sxs-lookup"><span data-stu-id="8cae7-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="8cae7-116">Et boksmodul til køb er et container-modul, som er vært for flere forskellige moduler, der indeholder de vigtigste oplysninger om produktet.</span><span class="sxs-lookup"><span data-stu-id="8cae7-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="8cae7-117">Disse oplysninger omfatter produktnavn, produktbilleder, beskrivelse, pris og produktvurderinger.</span><span class="sxs-lookup"><span data-stu-id="8cae7-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="8cae7-118">I boksmodulet til køb kan kunden vælge produktindstillinger (f.eks. en størrelse, en stil og en farve) og føje produktet til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="8cae7-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="8cae7-119">Det giver også kunden mulighed for at købe produktet online og plukke det på et lager.</span><span class="sxs-lookup"><span data-stu-id="8cae7-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="8cae7-120">Køb online, og afhent i butikken-modulet bruger integration med Bing Kort-API'er (Application Programming Interfaces) til at finde butikker i nærheden eller butikker på et andet sted, som kunden angiver.</span><span class="sxs-lookup"><span data-stu-id="8cae7-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="8cae7-121">Et boksmodul til køb kræver et produkt-id.</span><span class="sxs-lookup"><span data-stu-id="8cae7-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="8cae7-122">Dette id er afledt af sidekonteksten.</span><span class="sxs-lookup"><span data-stu-id="8cae7-122">This ID is derived from the page context.</span></span> <span data-ttu-id="8cae7-123">Hvis der føjes et boksmodul til køb på en side, hvor sidekonteksten ikke indeholder et produkt-id, gengives oplysningerne ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="8cae7-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="8cae7-124">Modul til produktspecifikationer</span><span class="sxs-lookup"><span data-stu-id="8cae7-124">Product specifications module</span></span>

<span data-ttu-id="8cae7-125">Modulet til produktspecifikationer kan bruges til at vise yderligere oplysninger om produktet.</span><span class="sxs-lookup"><span data-stu-id="8cae7-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="8cae7-126">Disse oplysninger hentes fra produktattributter i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="8cae7-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="8cae7-127">I modulet til produktspecifikationer vises alle attributter, hvor egenskaben **synlig** er angivet til **sand**.</span><span class="sxs-lookup"><span data-stu-id="8cae7-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="8cae7-128">Der kræves et produkt-id for at hente produktattributterne.</span><span class="sxs-lookup"><span data-stu-id="8cae7-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="8cae7-129">Anbefalingsmodulet</span><span class="sxs-lookup"><span data-stu-id="8cae7-129">Recommendations module</span></span>

<span data-ttu-id="8cae7-130">Anbefalingsmodulet er et vigtigt modul på en PDP.</span><span class="sxs-lookup"><span data-stu-id="8cae7-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="8cae7-131">Mens kunder søger efter produkter, bør der fremlægges flere produktmuligheder for dem, så de kan finde det rigtige produkt og foretage et køb.</span><span class="sxs-lookup"><span data-stu-id="8cae7-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="8cae7-132">Anbefalinger hjælper kunderne med nemt at finde relateret indhold og fortsætte med at handle.</span><span class="sxs-lookup"><span data-stu-id="8cae7-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="8cae7-133">Der findes forskellige typer af anbefalingslister:</span><span class="sxs-lookup"><span data-stu-id="8cae7-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="8cae7-134">Listen **Personer synes også om** er baseret på maskinel indlæring.</span><span class="sxs-lookup"><span data-stu-id="8cae7-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="8cae7-135">Den bruger transaktionshistorikken fra andre kunder til at give anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="8cae7-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="8cae7-136">Denne liste genereres af anbefalingstjenesten og minder om listetypen "Kunder, der købte dette, købte også...".</span><span class="sxs-lookup"><span data-stu-id="8cae7-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="8cae7-137">Der kræves et produkt-id for at generere denne liste.</span><span class="sxs-lookup"><span data-stu-id="8cae7-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="8cae7-138">Der kan konfigureres en **Relateret**-liste for et produkt i Retail.</span><span class="sxs-lookup"><span data-stu-id="8cae7-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="8cae7-139">Til en brun rejsetaske i læder kan der f.eks. være konfigureret flere tasker, der er fremstillet af læder eller designet til rejsebrug, på den relaterede liste.</span><span class="sxs-lookup"><span data-stu-id="8cae7-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="8cae7-140">Andre typer af relaterede lister, som f.eks. **Tilbehør** og **Mere som dette** kan også konfigureres i Retail.</span><span class="sxs-lookup"><span data-stu-id="8cae7-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="8cae7-141">Der kræves et produkt-id for at generere denne liste.</span><span class="sxs-lookup"><span data-stu-id="8cae7-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="8cae7-142">Hvis sidekonteksten ikke omfatter et produkt-id, vil listen derfor være tom, hvis den føjes til en startside.</span><span class="sxs-lookup"><span data-stu-id="8cae7-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="8cae7-143">Algoritmisk genererede anbefalingslister, f.eks. **Mest populære**, **Mest solgte** og **Nyt**, kan bruges på PDP'er.</span><span class="sxs-lookup"><span data-stu-id="8cae7-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="8cae7-144">Selvom disse lister ikke er direkte relateret til produktet på PDP, kan de også hjælpe kunderne med at finde produkter, der er interessante for dem.</span><span class="sxs-lookup"><span data-stu-id="8cae7-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="8cae7-145">Disse typer lister kræver ikke et produkt-id.</span><span class="sxs-lookup"><span data-stu-id="8cae7-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="8cae7-146">De er standardlister, der genereres på basis af indkøbsmønstre på tværs af webstedet.</span><span class="sxs-lookup"><span data-stu-id="8cae7-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="8cae7-147">Redaktionelle lister er manuelt fremstillede lister.</span><span class="sxs-lookup"><span data-stu-id="8cae7-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="8cae7-148">En forhandler kan f.eks. manuelt fremstille lister over produkter, der skal vises frem.</span><span class="sxs-lookup"><span data-stu-id="8cae7-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="8cae7-149">Modulet til vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="8cae7-149">Ratings and reviews module</span></span>

<span data-ttu-id="8cae7-150">Modulet til vurderinger og anmeldelser indeholder vurderinger og anmeldelser, der er leveret af andre kunder.</span><span class="sxs-lookup"><span data-stu-id="8cae7-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="8cae7-151">Det giver også kunden mulighed for at skrive sin egen anmeldelse af produktet.</span><span class="sxs-lookup"><span data-stu-id="8cae7-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="8cae7-152">Desuden indeholder den et histogram, der viser vurderingstendensen for produktet.</span><span class="sxs-lookup"><span data-stu-id="8cae7-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="8cae7-153">Du kan finde flere oplysninger under [Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8cae7-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="8cae7-154">Marketingmoduler</span><span class="sxs-lookup"><span data-stu-id="8cae7-154">Marketing modules</span></span>

<span data-ttu-id="8cae7-155">Hvis marketingindhold er entydigt for et bestemt produkt, kan der føjes et marketingmodul til PDP.</span><span class="sxs-lookup"><span data-stu-id="8cae7-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="8cae7-156">Du kan føje marketingmoduler til en PDP ved at "forbedre" siden.</span><span class="sxs-lookup"><span data-stu-id="8cae7-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="8cae7-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8cae7-157">Additional resources</span></span>

[<span data-ttu-id="8cae7-158">Oversigt over startsiden</span><span class="sxs-lookup"><span data-stu-id="8cae7-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="8cae7-159">Oversigt over standardlandingsside for kategori og side for søgeresultater</span><span class="sxs-lookup"><span data-stu-id="8cae7-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="8cae7-160">Oversigt over sider til indkøbsvogn og betaling ved kassen</span><span class="sxs-lookup"><span data-stu-id="8cae7-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="8cae7-161">Oversigt over sider til kontostyring</span><span class="sxs-lookup"><span data-stu-id="8cae7-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
