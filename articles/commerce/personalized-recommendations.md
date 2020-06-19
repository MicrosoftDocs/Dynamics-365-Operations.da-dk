---
title: Aktivere personlige produktanbefalinger
description: Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0e49b4db17ffd792e8dd536a1671773253c74d71
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404134"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="739df-103">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="739df-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="739df-104">Dette emne beskriver, hvordan du stiller personligt tilpassede produktanbefalinger til rådighed for kunder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="739df-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="739df-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="739df-105">Overview</span></span>

<span data-ttu-id="739df-106">I Dynamics 365 Commerce kan detailhandlere gøre personligt tilpassede produktanbefalinger tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="739df-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="739df-107">På denne måde kan personlige anbefalinger indarbejdes i kundeoplevelsen online og på salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="739df-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="739df-108">Når tilpasningsfunktionen er slået til, kan systemet tilknytte en brugers købs- og produktoplysninger for at generere individuelle produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="739df-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="739df-109">Forudsætninger for personlig tilpasning</span><span class="sxs-lookup"><span data-stu-id="739df-109">Personalization prerequisites</span></span>

<span data-ttu-id="739df-110">Før du stiller personlige produktanbefalinger til rådighed for kunderne, skal du bemærke, at produktanbefalinger kun understøttes af Commerce-brugere, der har overflyttet deres lager til Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="739df-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="739df-111">Før kunder kan modtage personlige produktanbefalinger, skal forhandlerne [aktivere produktanbefalinger](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="739df-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="739df-112">Når du aktiverer produktanbefalinger, kan du også aktivere personlig tilpasning.</span><span class="sxs-lookup"><span data-stu-id="739df-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="739df-113">Men hvis du deaktiverer personlig tilpasning, slår du ikke andre typer produktanbefalinger fra.</span><span class="sxs-lookup"><span data-stu-id="739df-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="739df-114">Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="739df-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="739df-115">Aktivere personlig tilpasning</span><span class="sxs-lookup"><span data-stu-id="739df-115">Turn on personalization</span></span>

<span data-ttu-id="739df-116">Udfør følgende trin for at aktivere personlig tilpasning.</span><span class="sxs-lookup"><span data-stu-id="739df-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="739df-117">Gå til **Retail og Commerce \> Produktanbefalinger \> Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="739df-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="739df-118">Vælg **Anbefalingslister** på listen over delte Retail-parametre.</span><span class="sxs-lookup"><span data-stu-id="739df-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="739df-119">Angiv indstillingen **Aktivér tilpasning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="739df-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Aktivere tilpasning](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="739df-121">Når du aktiverer personlig tilpasning, startes processen til generering af lister over tilpassede produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="739df-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="739df-122">Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS.</span><span class="sxs-lookup"><span data-stu-id="739df-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="739df-123">Personligt tilpassede lister</span><span class="sxs-lookup"><span data-stu-id="739df-123">Personalized lists</span></span>

<span data-ttu-id="739df-124">Udover at tillade personlig tilpasning af eksisterende maskingenererede lister giver anbefalingstjenesten mulighed for at tilpasse produktregistreringsoplevelsen både online og på POS.</span><span class="sxs-lookup"><span data-stu-id="739df-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="739df-125">Når tilpasning er slået til, kan detailhandlere vise kunderne personlige "Udvalgt til dig"-lister online eller "Anbefalet til kunde"-lister på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="739df-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="739df-126">Desuden kan detailhandlere anvende personlig tilpasning på eksisterende produktanbefalingslister og levere GDPR-baseret framelding (generel forordning om databeskyttelse) til godkendte brugere.</span><span class="sxs-lookup"><span data-stu-id="739df-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="739df-127">Hvis du deaktiverer personlig tilpasning, deaktiverer du også disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="739df-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="739df-128">Online "Udvalgt til dig"-lister</span><span class="sxs-lookup"><span data-stu-id="739df-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="739df-129">Listen "Udvalgt til dig" er en kunstig intelligens-baseret maskinel læring (AI-ML), der viser en godkendt bruger en tilpasset liste over foreslåede produkter.</span><span class="sxs-lookup"><span data-stu-id="739df-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="739df-130">Denne liste er baseret på brugerens omnikanal-indkøbshistorik.</span><span class="sxs-lookup"><span data-stu-id="739df-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="739df-131">Personlige anbefalinger opdateres dynamisk, efterhånden som brugeren foretager flere køb.</span><span class="sxs-lookup"><span data-stu-id="739df-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="739df-132">Denne type liste understøtter også filtrering af kategorier, så detailhandlere kan vise de bedste udvalg baseret på navigationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="739df-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="739df-133">Før listen "Udvalgt til dig" kan vises på en e-handelsside, skal følgende brugerkrav være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="739df-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="739df-134">Brugere skal være logget på.</span><span class="sxs-lookup"><span data-stu-id="739df-134">Users must be signed in.</span></span> <span data-ttu-id="739df-135">Anonyme brugere kan ikke se personligt tilpassede anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="739df-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="739df-136">Brugere skal have mindst ét indkøb på deres konto.</span><span class="sxs-lookup"><span data-stu-id="739df-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="739df-137">Brugerne skal være tilmeldt for at modtage personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="739df-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="739df-138">I følgende illustration vises et eksempel på en liste over "Udvalgt til dig" på en onlinebutiksside.</span><span class="sxs-lookup"><span data-stu-id="739df-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Online Udvalgt til dig-liste](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="739df-140">Listerne "Anbefalet til kunde" på POS</span><span class="sxs-lookup"><span data-stu-id="739df-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="739df-141">For at forbedre deres kundeaktiviteter kan detailhandlere personligt tilpasse eksisterende kundedetaljesider ved at tilføje en kontekstafhængig "Anbefalet til kunde"-liste.</span><span class="sxs-lookup"><span data-stu-id="739df-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="739df-142">I følgende illustration vises et eksempel på en liste over "Anbefalet til kunde" på en POS-klient.</span><span class="sxs-lookup"><span data-stu-id="739df-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Listen Anbefalet til kunde på POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="739df-144">Anvende personlige tilpasninger på eksisterende anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="739df-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="739df-145">Detailhandlere kan anvende personlige tilpasninger på eksisterende anbefalingslister, f.eks. "Nyhed", "Mest populære", "Mest solgte", "Folk kan også godt lide" og "Ofte købt sammen".</span><span class="sxs-lookup"><span data-stu-id="739df-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="739df-146">Når personlig tilpasning anvendes på eksisterende lister, fjernes de varer, som en bruger har købt tidligere, fra listerne.</span><span class="sxs-lookup"><span data-stu-id="739df-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="739df-147">For både anonyme brugere og brugere, der har fravalgt at modtage personlige anbefalinger, vises standardversioner af de eksisterende lister.</span><span class="sxs-lookup"><span data-stu-id="739df-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="739df-148">Derfor behøver detailhandlerne ikke at vedligeholde særskilte sideoplevelser manuelt.</span><span class="sxs-lookup"><span data-stu-id="739df-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="739df-149">En bruger, der er logget på, har f.eks. allerede købt det sorte ur og de brune arbejdsstøvler, der vises på listen "Trending - default" på følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="739df-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="739df-150">Brugeren får derfor vist nye produkter i stedet for disse produkter, som vist på listen "Trending - personalized".</span><span class="sxs-lookup"><span data-stu-id="739df-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Anvende personlig tilpasning](./media/applypersonalization.png)

<span data-ttu-id="739df-152">Hvis du vil anvende tilpasning på en eksisterende anbefalingsliste i Commerce-webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="739df-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="739df-153">Åbn en eksisterende side med webstedsgeneratoren, der indeholder et modul til produktsamling.</span><span class="sxs-lookup"><span data-stu-id="739df-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="739df-154">Vælg produktsamlingsmodulet i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="739df-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="739df-155">Vælg listen under **Produkter** i navigationsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="739df-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="739df-156">Vælg listetypen under **Type** i dialogboksen **Vælg produktlistekonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="739df-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="739df-157">Markér afkrydsningsfeltet **Anvend personlig tilpasning**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="739df-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Anvende personlig tilpasning på en tendensliste](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="739df-159">Gem siden, afslut redigeringen af den, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="739df-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="739df-160">Når siden er publiceret, vil de brugere, der er logget på, se en personligt tilpasset tendensliste.</span><span class="sxs-lookup"><span data-stu-id="739df-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="739df-161">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="739df-161">Additional resources</span></span>

[<span data-ttu-id="739df-162">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="739df-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="739df-163">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="739df-163">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="739df-164">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="739df-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="739df-165">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="739df-165">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="739df-166">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="739df-166">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="739df-167">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="739df-167">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="739df-168">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="739df-168">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="739df-169">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="739df-169">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="739df-170">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="739df-170">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="739df-171">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="739df-171">Product recommendations FAQ</span></span>](faq-recommendations.md)
