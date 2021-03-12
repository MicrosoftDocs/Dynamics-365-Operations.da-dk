---
title: Aktivere personlige produktanbefalinger
description: Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f535cf0bc3c733426af22cf453ffe97f721f8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000577"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="9a59f-103">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a59f-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a59f-104">Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9a59f-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9a59f-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="9a59f-105">Overview</span></span>

<span data-ttu-id="9a59f-106">I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="9a59f-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="9a59f-107">På denne måde kan personlige anbefalinger indarbejdes i kundeoplevelsen online og på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="9a59f-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="9a59f-108">Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="9a59f-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="9a59f-109">Forudsætninger for personlig tilpasning</span><span class="sxs-lookup"><span data-stu-id="9a59f-109">Personalization prerequisites</span></span>

<span data-ttu-id="9a59f-110">Før du stiller personlige produktanbefalinger til rådighed for kunderne, skal du bemærke, at produktanbefalinger kun understøttes af Commerce-brugere, der har overflyttet deres lager til Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="9a59f-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="9a59f-111">Før kunder kan modtage personlige produktanbefalinger, skal forhandlerne [aktivere produktanbefalinger](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9a59f-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9a59f-112">Når du aktiverer produktanbefalinger, kan du også aktivere personlig tilpasning.</span><span class="sxs-lookup"><span data-stu-id="9a59f-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="9a59f-113">Men hvis du deaktiverer personlig tilpasning, slår du ikke andre typer produktanbefalinger fra.</span><span class="sxs-lookup"><span data-stu-id="9a59f-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="9a59f-114">Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9a59f-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="9a59f-115">Aktivere personlig tilpasning</span><span class="sxs-lookup"><span data-stu-id="9a59f-115">Turn on personalization</span></span>

<span data-ttu-id="9a59f-116">Udfør følgende trin for at aktivere personlig tilpasning.</span><span class="sxs-lookup"><span data-stu-id="9a59f-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="9a59f-117">Søg efter **Funktionsstyring** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="9a59f-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="9a59f-118">Vælg **Alle** for at få vist en liste over tilgængelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="9a59f-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="9a59f-119">Skriv **Anbefalinger** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="9a59f-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="9a59f-120">Vælg funktionen **Tilpassede produktanbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="9a59f-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="9a59f-121">Vælg **Aktivér nu** i ruden med egenskaber for **Tilpassede produktanbefalinger**.</span><span class="sxs-lookup"><span data-stu-id="9a59f-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Aktivere tilpasning](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="9a59f-123">Når du aktiverer personlig tilpasning, startes processen til generering af lister over tilpassede produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="9a59f-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="9a59f-124">Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS.</span><span class="sxs-lookup"><span data-stu-id="9a59f-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="9a59f-125">Personligt tilpassede lister</span><span class="sxs-lookup"><span data-stu-id="9a59f-125">Personalized lists</span></span>

<span data-ttu-id="9a59f-126">Udover at tillade personlig tilpasning af eksisterende maskingenererede lister giver anbefalingstjenesten mulighed for at tilpasse produktregistreringsoplevelsen både online og på POS.</span><span class="sxs-lookup"><span data-stu-id="9a59f-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="9a59f-127">Når tilpasning er slået til, kan detailhandlere vise kunderne personlige "Udvalgt til dig"-lister online eller "Anbefalet til kunde"-lister på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="9a59f-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="9a59f-128">Desuden kan detailhandlere anvende personlig tilpasning på eksisterende produktanbefalingslister og levere GDPR-baseret framelding (generel forordning om databeskyttelse) til godkendte brugere.</span><span class="sxs-lookup"><span data-stu-id="9a59f-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="9a59f-129">Hvis du deaktiverer personlig tilpasning, deaktiverer du også disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="9a59f-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="9a59f-130">Online "Udvalgt til dig"-lister</span><span class="sxs-lookup"><span data-stu-id="9a59f-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="9a59f-131">Listen "Udvalgt til dig" er en kunstig intelligens-baseret maskinel læring (AI-ML), der viser en godkendt bruger en tilpasset liste over foreslåede produkter.</span><span class="sxs-lookup"><span data-stu-id="9a59f-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="9a59f-132">Denne liste er baseret på brugerens omnikanal-indkøbshistorik.</span><span class="sxs-lookup"><span data-stu-id="9a59f-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="9a59f-133">Personlige anbefalinger opdateres dynamisk, efterhånden som brugeren foretager flere køb.</span><span class="sxs-lookup"><span data-stu-id="9a59f-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="9a59f-134">Denne type liste understøtter også filtrering af kategorier, så detailhandlere kan vise de bedste udvalg baseret på navigationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="9a59f-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="9a59f-135">Før listen "Udvalgt til dig" kan vises på en e-handelsside, skal følgende brugerkrav være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="9a59f-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="9a59f-136">Brugere skal være logget på.</span><span class="sxs-lookup"><span data-stu-id="9a59f-136">Users must be signed in.</span></span> <span data-ttu-id="9a59f-137">Anonyme brugere kan ikke se personligt tilpassede anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="9a59f-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="9a59f-138">Brugere skal have mindst ét indkøb på deres konto.</span><span class="sxs-lookup"><span data-stu-id="9a59f-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="9a59f-139">Brugerne skal være tilmeldt for at modtage personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="9a59f-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="9a59f-140">I følgende illustration vises et eksempel på en liste over "Udvalgt til dig" på en onlinebutiksside.</span><span class="sxs-lookup"><span data-stu-id="9a59f-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Online Udvalgt til dig-liste](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="9a59f-142">Listerne "Anbefalet til kunde" på POS</span><span class="sxs-lookup"><span data-stu-id="9a59f-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="9a59f-143">For at forbedre deres kundeaktiviteter kan detailhandlere personligt tilpasse eksisterende kundedetaljesider ved at tilføje en kontekstafhængig "Anbefalet til kunde"-liste.</span><span class="sxs-lookup"><span data-stu-id="9a59f-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="9a59f-144">I følgende illustration vises et eksempel på en liste over "Anbefalet til kunde" på en POS-klient.</span><span class="sxs-lookup"><span data-stu-id="9a59f-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Listen Anbefalet til kunde på POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="9a59f-146">Anvende personlige tilpasninger på eksisterende anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="9a59f-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="9a59f-147">Detailhandlere kan anvende personlige tilpasninger på eksisterende anbefalingslister, f.eks. "Nyhed", "Mest populære", "Mest solgte", "Folk kan også godt lide" og "Ofte købt sammen".</span><span class="sxs-lookup"><span data-stu-id="9a59f-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="9a59f-148">Når personlig tilpasning anvendes på eksisterende lister, fjernes de varer, som en bruger har købt tidligere, fra listerne.</span><span class="sxs-lookup"><span data-stu-id="9a59f-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="9a59f-149">For både anonyme brugere og brugere, der har fravalgt at modtage personlige anbefalinger, vises standardversioner af de eksisterende lister.</span><span class="sxs-lookup"><span data-stu-id="9a59f-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="9a59f-150">Derfor behøver detailhandlerne ikke at vedligeholde særskilte sideoplevelser manuelt.</span><span class="sxs-lookup"><span data-stu-id="9a59f-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="9a59f-151">En bruger, der er logget på, har f.eks. allerede købt det sorte ur og de brune arbejdsstøvler, der vises på listen "Trending - default" på følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="9a59f-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="9a59f-152">Brugeren får derfor vist nye produkter i stedet for disse produkter, som vist på listen "Trending - personalized".</span><span class="sxs-lookup"><span data-stu-id="9a59f-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Anvende personlig tilpasning](./media/applypersonalization.png)

<span data-ttu-id="9a59f-154">Hvis du vil anvende tilpasning på en eksisterende anbefalingsliste i Commerce-webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9a59f-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9a59f-155">Åbn en eksisterende side med webstedsgeneratoren, der indeholder et modul til produktsamling.</span><span class="sxs-lookup"><span data-stu-id="9a59f-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="9a59f-156">Vælg produktsamlingsmodulet i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="9a59f-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="9a59f-157">Vælg listen under **Produkter** i navigationsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="9a59f-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="9a59f-158">Vælg listetypen under **Type** i dialogboksen **Vælg produktlistekonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9a59f-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="9a59f-159">Markér afkrydsningsfeltet **Anvend personlig tilpasning**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a59f-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Anvende personlig tilpasning på en tendensliste](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="9a59f-161">Gem siden, afslut redigeringen af den, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="9a59f-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="9a59f-162">Når siden er publiceret, vil de brugere, der er logget på, se en personligt tilpasset tendensliste.</span><span class="sxs-lookup"><span data-stu-id="9a59f-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a59f-163">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9a59f-163">Additional resources</span></span>

[<span data-ttu-id="9a59f-164">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a59f-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9a59f-165">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="9a59f-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9a59f-166">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a59f-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9a59f-167">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="9a59f-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9a59f-168">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a59f-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9a59f-169">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="9a59f-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9a59f-170">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="9a59f-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9a59f-171">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a59f-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9a59f-172">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="9a59f-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9a59f-173">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="9a59f-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9a59f-174">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a59f-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
