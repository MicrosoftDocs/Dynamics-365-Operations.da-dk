---
title: Oversigt over standardlandingsside for kategori og side for søgeresultater
description: Dette emne indeholder en oversigt over standardlandingsside for kategori og side for søgeresultater i Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7a40df479bffdc6fdee8f0a7f64fde980cbbdbab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215715"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="fbb39-103">Oversigt over standardlandingsside for kategori og side for søgeresultater</span><span class="sxs-lookup"><span data-stu-id="fbb39-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fbb39-104">Dette emne indeholder en oversigt over standardlandingssiden for kategorier og søgeresultatsiden for e-handel i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fbb39-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="fbb39-105">Standardlandingsside for kategorier</span><span class="sxs-lookup"><span data-stu-id="fbb39-105">Default category landing page</span></span>

<span data-ttu-id="fbb39-106">Standardlandingssiden for kategorier er den side, som brugerne af et websted typisk får vist, når de vælger en kategori i navigationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fbb39-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="fbb39-107">Du kan gennemse kategorisiden, og du kan også sortere og finpudse de kategoriserede produkter.</span><span class="sxs-lookup"><span data-stu-id="fbb39-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Standardlandingsside for kategorier](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="fbb39-109">Øverst på siden findes et sidehoved, der viser alle produktkategorierne og andre sider, som produktchefen har kategoriseret.</span><span class="sxs-lookup"><span data-stu-id="fbb39-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="fbb39-110">Konfigurationen udføres som en del af konfigurationen af kanalnavigationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fbb39-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="fbb39-111">Nederst på startsiden findes en sidefod med hurtige links til forskellige emner, som kan have interesse for kunderne.</span><span class="sxs-lookup"><span data-stu-id="fbb39-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="fbb39-112">Følgende komponenter er vigtige for en kategori:</span><span class="sxs-lookup"><span data-stu-id="fbb39-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="fbb39-113">**Felter til produktplacering** viser de produkter, som produktchefen har defineret i en kategori som et let i konfigurationen af navigationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fbb39-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="fbb39-114">**Oversigt over afgrænsere og valg** er filtre, der viser antal, og som kan bruges til at afgrænse elementer.</span><span class="sxs-lookup"><span data-stu-id="fbb39-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="fbb39-115">Produktchefen konfigurerer dem som en del af konfigurationen af de metadata, der er relateret til kanalkategorier og produktattributter.</span><span class="sxs-lookup"><span data-stu-id="fbb39-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="fbb39-116">**Sorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne.</span><span class="sxs-lookup"><span data-stu-id="fbb39-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="fbb39-117">Følgende sorteringsindstillinger er som standard tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="fbb39-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="fbb39-118">Pris – lav til høj</span><span class="sxs-lookup"><span data-stu-id="fbb39-118">Price – low to high</span></span>
    - <span data-ttu-id="fbb39-119">Pris – høj til lav</span><span class="sxs-lookup"><span data-stu-id="fbb39-119">Price – high to low</span></span>
    - <span data-ttu-id="fbb39-120">Produktnavn – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="fbb39-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="fbb39-121">Produktnavn – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="fbb39-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="fbb39-122">Vurderinger – lav til høj</span><span class="sxs-lookup"><span data-stu-id="fbb39-122">Ratings – low to high</span></span>
    - <span data-ttu-id="fbb39-123">Vurderinger – høj til lav</span><span class="sxs-lookup"><span data-stu-id="fbb39-123">Ratings – high to low</span></span>

- <span data-ttu-id="fbb39-124">**Sideinddeling** lader de besøgende på webstedet flytte fra én side med kategoriserede produktresultater til en anden side.</span><span class="sxs-lookup"><span data-stu-id="fbb39-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="fbb39-125">**Samlet antal** viser det samlede antal produkter, der er defineret i en kategori.</span><span class="sxs-lookup"><span data-stu-id="fbb39-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="fbb39-126">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="fbb39-126">Enrich a category landing page</span></span>

<span data-ttu-id="fbb39-127">Hvis du ønsker, at en landingsside for en kategori skal have en mere skræddersyet oplevelse for en bestemt kategori, kan du "forbedre" kategorilandingssiden for den pågældende kategori.</span><span class="sxs-lookup"><span data-stu-id="fbb39-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="fbb39-128">Du kan f.eks. tilføje en marketingvideo og fortælle om kategorien for at få kundernes opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="fbb39-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="fbb39-129">Du kan finde flere oplysninger under [Forbedre en kategorilandingsside](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="fbb39-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Forbedre en kategorilandingsside](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="fbb39-131">Sider med automatiske forslag og søgeresultater</span><span class="sxs-lookup"><span data-stu-id="fbb39-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="fbb39-132">Brugere af websteder kan udforske et websted ved enten at gå til en kategori fra navigationshierarkiet eller ved at angive et søgeord i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="fbb39-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="fbb39-133">Så snart brugerne går i gang med at skrive i søgefeltet, oplever de den avancerede funktion til automatiske forslag, der foreslår søgeord.</span><span class="sxs-lookup"><span data-stu-id="fbb39-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="fbb39-134">Her er nogle af de typer forslag, der kan vises:</span><span class="sxs-lookup"><span data-stu-id="fbb39-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="fbb39-135">**Nøgleord** bruges til at finde produkter på tværs af alle produkter, der er udvalgt til kanalen.</span><span class="sxs-lookup"><span data-stu-id="fbb39-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="fbb39-136">**Produkter** giver direkte links til siden med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="fbb39-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="fbb39-137">**Søgeforslag for kategoriområde** viser forskellige kategorier og lader brugere søge efter nøgleordet i en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="fbb39-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Avancerede automatiske forslag](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="fbb39-139">Når brugerne vælger et af søgeforslagene for nøgleord eller områdekategori, eller når der ikke er nogen forslag til det søgeord, de angiver, omdirigeres de til en side med søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="fbb39-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="fbb39-140">Brugerne kan derefter gennemse, sortere og finjustere listen over søgeresultater for at finde det ønskede produkt.</span><span class="sxs-lookup"><span data-stu-id="fbb39-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Landingsside for søgeresultater](./media/SearchLanding.png)

<span data-ttu-id="fbb39-142">Følgende komponenter er vigtige for en søgeresultatside:</span><span class="sxs-lookup"><span data-stu-id="fbb39-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="fbb39-143">**Produktplaceringsfelter** viser produkterne til brugerens søgning.</span><span class="sxs-lookup"><span data-stu-id="fbb39-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="fbb39-144">Disse felter sorteres som standard af det skybaserede søgerelevansresultat for brugersøgningen.</span><span class="sxs-lookup"><span data-stu-id="fbb39-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="fbb39-145">**Oversigt over afgrænsere og valg** er filtre, der viser antal, og som kan bruges til at afgrænse elementer.</span><span class="sxs-lookup"><span data-stu-id="fbb39-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="fbb39-146">Produktchefen konfigurerer dem som en del af konfigurationen af metadataene for "kanalkategorier og produktattributter".</span><span class="sxs-lookup"><span data-stu-id="fbb39-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="fbb39-147">**Sorteringsindstillinger** bruges af besøgende på webstedet til at sortere produkterne.</span><span class="sxs-lookup"><span data-stu-id="fbb39-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="fbb39-148">Følgende sorteringsindstillinger er som standard tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="fbb39-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="fbb39-149">Pris – lav til høj</span><span class="sxs-lookup"><span data-stu-id="fbb39-149">Price – low to high</span></span>
    - <span data-ttu-id="fbb39-150">Pris – høj til lav</span><span class="sxs-lookup"><span data-stu-id="fbb39-150">Price – high to low</span></span>
    - <span data-ttu-id="fbb39-151">Produktnavn – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="fbb39-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="fbb39-152">Produktnavn – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="fbb39-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="fbb39-153">Vurderinger – lav til høj</span><span class="sxs-lookup"><span data-stu-id="fbb39-153">Ratings – low to high</span></span>
    - <span data-ttu-id="fbb39-154">Vurderinger – høj til lav</span><span class="sxs-lookup"><span data-stu-id="fbb39-154">Ratings – high to low</span></span>
    - <span data-ttu-id="fbb39-155">Standard</span><span class="sxs-lookup"><span data-stu-id="fbb39-155">Default</span></span>

- <span data-ttu-id="fbb39-156">**Sideinddeling** lader de besøgende på webstedet flytte fra én side med kategoriserede produktresultater til en anden side.</span><span class="sxs-lookup"><span data-stu-id="fbb39-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="fbb39-157">**Samlet antal** viser det samlede antal produkter, der er defineret i en kategori, og som opfylder søgekriterierne.</span><span class="sxs-lookup"><span data-stu-id="fbb39-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="fbb39-158">Disse cloud-aktiverede søgemuligheder er tilgængelige fra og med version 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="fbb39-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="fbb39-159">Kontroller, at der er en post for "ProductSearch.UseAzureSearch, der er indstillet til 'sand' under **Commerce-parametre > Konfigurationsparametre**.</span><span class="sxs-lookup"><span data-stu-id="fbb39-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="fbb39-160">![Konfigurationsparametre for cloud-baseret søgning](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="fbb39-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbb39-161">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fbb39-161">Additional resources</span></span>

[<span data-ttu-id="fbb39-162">Oversigt over skybaseret søgning</span><span class="sxs-lookup"><span data-stu-id="fbb39-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="fbb39-163">Oversigt over startside</span><span class="sxs-lookup"><span data-stu-id="fbb39-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="fbb39-164">Oversigt over sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="fbb39-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="fbb39-165">Oversigt over sider til indkøbsvogn og betaling ved kassen</span><span class="sxs-lookup"><span data-stu-id="fbb39-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="fbb39-166">Oversigt over sider til kontostyring</span><span class="sxs-lookup"><span data-stu-id="fbb39-166">Account management pages overview</span></span>](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]