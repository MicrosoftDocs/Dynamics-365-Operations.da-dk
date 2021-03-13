---
title: Ofte stillede spørgsmål om produktanbefalinger
description: Dette emne indeholder oplysninger om processer og værktøjer, du kan bruge til at foretage fejlfinding af problemer, der vedrører produktanbefalinger eller resultaterne af dem.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8eaebaf605cd53ce6848624169c3bbbd2a4281a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009893"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="067f7-103">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="067f7-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="067f7-104">Dette emne indeholder oplysninger om processer og værktøjer, du kan bruge til at foretage fejlfinding af problemer, der vedrører [produktanbefalinger](product-recommendations.md) eller resultaterne af dem.</span><span class="sxs-lookup"><span data-stu-id="067f7-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="067f7-105">Bedste fremgangsmåder</span><span class="sxs-lookup"><span data-stu-id="067f7-105">Best practices</span></span>
<span data-ttu-id="067f7-106">Det er meget vigtigt at udnytte begrebet produktmastere og -varianter.</span><span class="sxs-lookup"><span data-stu-id="067f7-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="067f7-107">Grupperingen af varianter i en overordnet produktmaster udnyttes af listealgoritmerne og tjenesten til at oprette bedre modeller.</span><span class="sxs-lookup"><span data-stu-id="067f7-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="067f7-108">Desuden kan tjenesten kun levere én forekomst af et produkt i stedet for at sætte alle tæt forbundne varianter på en liste.</span><span class="sxs-lookup"><span data-stu-id="067f7-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="067f7-109">Når alle nært relaterede varianter placeres på en liste, kan der forekomme forkerte eller identiske resultater.</span><span class="sxs-lookup"><span data-stu-id="067f7-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="067f7-110">Hvorfor mangler der produkter i mine anbefalingslister?</span><span class="sxs-lookup"><span data-stu-id="067f7-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="067f7-111">Hvis der mangler en vare på en produktanbefalingsliste, kan der typisk være problemer med produktkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="067f7-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="067f7-112">Der kan f.eks. være en forkert produktstartdato eller -slutdato, en dimension kan være fejlkonfigureret, eller produktet er muligvis ikke i det korrekte kanalsortiment osv.</span><span class="sxs-lookup"><span data-stu-id="067f7-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="067f7-113">Hvis der mangler en vare på en anbefalingsliste, der er baseret på kunstig intelligens-maskinel indlæring (AI-ML), er varen muligvis ikke i overensstemmelse med kriterierne for anbefalingslisten, eller der er muligvis ikke nok indkøbstransaktioner på anbefalingslister til at vise den.</span><span class="sxs-lookup"><span data-stu-id="067f7-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="067f7-114">Det anbefales, at du kontrollerer disse trin:</span><span class="sxs-lookup"><span data-stu-id="067f7-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="067f7-115">**Sørg for, at produktanbefalingerne er aktiveret i hovedkontoret.**</span><span class="sxs-lookup"><span data-stu-id="067f7-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="067f7-116">Du kan finde oplysninger om, hvordan du aktiverer denne tjeneste, under [Aktiver produktanbefaler](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="067f7-117">**Sørg for, at nøgleproduktegenskaberne er angivet.**</span><span class="sxs-lookup"><span data-stu-id="067f7-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="067f7-118">Produktsortimenter skal f.eks. være indstillet til **Medtag**.</span><span class="sxs-lookup"><span data-stu-id="067f7-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="067f7-119">**For nyligt udvalgte produkter kan det tage op til tre timer, før produktet begynder at blive vist på den nye liste.**</span><span class="sxs-lookup"><span data-stu-id="067f7-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="067f7-120">**Hvis et produkt stadig ikke vises i Mest populære, Bedst sælgende, Andre synes også godt om eller Ofte købt sammen, vil produktet muligvis ikke have nok transaktioner.**</span><span class="sxs-lookup"><span data-stu-id="067f7-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="067f7-121">I dette tilfælde kan du enten vente på, at der foretages flere transaktioner, opdatere standardparametrene for anbefalingslisten eller bruge manuel indgriben til at redigere resultaterne af produktlisten.</span><span class="sxs-lookup"><span data-stu-id="067f7-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="067f7-122">Du kan finde flere oplysninger om anbefalingsparametre under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="067f7-123">**Kontroller, at produktet opfylder anbefalingskriterierne for listen.**</span><span class="sxs-lookup"><span data-stu-id="067f7-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="067f7-124">Du kan finde flere oplysninger om produktanbefalingsparametre under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="067f7-125">Hvordan kan jeg forhindre, at der returneres dårlige anbefalingsresultater?</span><span class="sxs-lookup"><span data-stu-id="067f7-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="067f7-126">Anbefalingslister kræver en stor mængder transaktioner for at opnå resultater.</span><span class="sxs-lookup"><span data-stu-id="067f7-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="067f7-127">Det er derfor vigtigt, at brugerne leverer fuldstændige historiske transaktionsdata.</span><span class="sxs-lookup"><span data-stu-id="067f7-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="067f7-128">Desuden har produkter, der ikke har nogen transaktioner eller få transaktioner, typisk ikke resultater af typen **Andre synes også godt om** eller **Ofte købt sammen**, og de vises ikke i **Mest populære** eller **Bedst sælgende**-anbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="067f7-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="067f7-129">Denne situation kan ofte forekomme for meget nye produkter eller for gamle produkter, der har et lille antal indkøb.</span><span class="sxs-lookup"><span data-stu-id="067f7-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="067f7-130">Nye populære varer kan nemt overvinde dette problem.</span><span class="sxs-lookup"><span data-stu-id="067f7-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="067f7-131">Det anbefales, at du følger disse trin:</span><span class="sxs-lookup"><span data-stu-id="067f7-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="067f7-132">**Kontroller, at produktet opfylder anbefalingskriterierne for denne liste.**</span><span class="sxs-lookup"><span data-stu-id="067f7-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="067f7-133">Du kan finde flere oplysninger om produktanbefalingsparametre under Redigere resultater for AI-ML-baserede produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="067f7-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="067f7-134">**Hvis produktet er nyt, bør du overveje at redigere en anbefalingsliste, indtil produktet har flere transaktioner.**</span><span class="sxs-lookup"><span data-stu-id="067f7-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="067f7-135">Du kan finde flere oplysninger om, hvordan du redigerer anbefalingslistens resultater under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="067f7-136">**Kontroller, at produktet opfylder anbefalingskriterierne for denne liste.**</span><span class="sxs-lookup"><span data-stu-id="067f7-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="067f7-137">Du kan finde flere oplysninger om produktanbefalingsparametre under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="067f7-138">**Hvis produktet er nyt, bør du overveje at redigere en anbefalingsliste, indtil produktet har flere transaktioner**.</span><span class="sxs-lookup"><span data-stu-id="067f7-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="067f7-139">Du kan finde flere oplysninger om, hvordan du redigerer anbefalingslistens resultater under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="067f7-140">Kan jeg fjerne et produkt, men stadig se det i butikken?</span><span class="sxs-lookup"><span data-stu-id="067f7-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="067f7-141">Du kan justere lister, der genereres algoritmisk, hvis der opstår et forretningsmæssigt behov.</span><span class="sxs-lookup"><span data-stu-id="067f7-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="067f7-142">Men hvis et produkt fjernes fra en anbefalingsliste, vil produktet stadig være synligt i butikken.</span><span class="sxs-lookup"><span data-stu-id="067f7-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="067f7-143">Du kan finde flere oplysninger om, hvordan du redigerer produktanbefalingsresultater under [Administrere resultater for AI-ML-baserede produktanbefalinger](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="067f7-144">Hvis du vil forhindre, at en vare er synlig i butikken, skal du ændre værdien for **Varesortimenter**, til **Udelad**.</span><span class="sxs-lookup"><span data-stu-id="067f7-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="067f7-145">Hvordan føjer jeg en liste til en e-handelsside?</span><span class="sxs-lookup"><span data-stu-id="067f7-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="067f7-146">Du kan finde flere oplysninger om, hvordan du føjer produktanbefalingssider til e-handelswebsteder, under [Tilføje lister med produktanbefalinger på sider](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="067f7-147">Hvordan aktiverer jeg anbefalinger i POS?</span><span class="sxs-lookup"><span data-stu-id="067f7-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="067f7-148">Når du har aktiveret produktanbefalinger, skal du tilføje anbefalingspanelet på kontrolelementets POS-skærm.</span><span class="sxs-lookup"><span data-stu-id="067f7-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="067f7-149">Du kan få flere oplysninger i [Føje et kontrolelement med anbefalinger til posteringsskærmen på POS-enheder](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="067f7-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="067f7-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="067f7-150">Additional resources</span></span>

[<span data-ttu-id="067f7-151">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="067f7-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="067f7-152">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="067f7-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="067f7-153">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="067f7-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="067f7-154">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="067f7-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="067f7-155">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="067f7-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="067f7-156">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="067f7-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="067f7-157">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="067f7-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="067f7-158">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="067f7-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="067f7-159">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="067f7-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="067f7-160">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="067f7-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="067f7-161">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="067f7-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
