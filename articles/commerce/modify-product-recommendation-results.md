---
title: Juster resultater for AI-ML-baserede produktanbefalinger
description: I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc6a793061a3e644599f0882ff163f5f57b2162d
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664948"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="9a7ea-103">Juster resultater for AI-ML-baserede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a7ea-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9a7ea-104">I dette emne beskrives, hvordan du justerer resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="9a7ea-105">Når du har aktiveret produktanbefalinger, træder standardindstillingerne i kraft. Disse parametre kan bruges ved mange behov og til mange formål.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="9a7ea-106">Det er bedst at planlægge at bruge tid på at evaluere, om resultaterne opfylder produkternes markedsbevægelse.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="9a7ea-107">Vi foreslår, at du evaluerer resultaterne i nogle dage, før du ændrer parametre efter behov og tester igen.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="9a7ea-108">Om parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="9a7ea-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="9a7ea-109">Før du ændrer parametrene, skal du sætte dig ind i, hvordan de påvirker resultaterne nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="9a7ea-110">Liste over mest populære produkter</span><span class="sxs-lookup"><span data-stu-id="9a7ea-110">"Trending" product list</span></span>

<span data-ttu-id="9a7ea-111">Listen over de mest populære produkter har to parametre, der kan ændres:</span><span class="sxs-lookup"><span data-stu-id="9a7ea-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Eksempel på standardparametre for liste over mest populære produkter](./media/exampletrendingparameters.png)

1. <span data-ttu-id="9a7ea-113">**Medtag nye produkter fra de seneste X dage** - Produkter, der er blevet tilføjet inden for det angivne antal dage, før den aktuelle dato kan bruges til at vælge produktkandidater.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="9a7ea-114">Standardværdien på billedet antyder, at produkter så gamle som 180 dage, kan bruges på listen med populære produkter.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="9a7ea-115">**Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="9a7ea-116">Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over populære produkter.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="9a7ea-117">Liste over mest solgte produkter</span><span class="sxs-lookup"><span data-stu-id="9a7ea-117">"Best selling" product list</span></span>

<span data-ttu-id="9a7ea-118">Afhængigt af din virksomhed kan listen over mest solgte produkter give et andet resultat end de mest populære produkter, selvom de begge bruger transaktionsdata til at rangordne produkter.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="9a7ea-119">Da Bedst sælgende ikke har nogen skæring baseret på dato for udvælgelse, kan Bedst sælgende stadig fremhæve meget populære produkter af ældre dato, der muligvis er blevet slettet fra popularitetslisten.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="9a7ea-120">Listen over de mest solgte produkter har én parameter, der kan ændres:</span><span class="sxs-lookup"><span data-stu-id="9a7ea-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Eksempel på standardparameter for liste over bedst sælgende](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="9a7ea-122">**Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="9a7ea-123">Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over bedst sælgende produkter.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="9a7ea-124">Tilføje eller fjerne produkter manuelt fra anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="9a7ea-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="9a7ea-125">For listerne Ny, Mest populære eller Mest solgte</span><span class="sxs-lookup"><span data-stu-id="9a7ea-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="9a7ea-126">Gå til **Retail og Commerce** > **Produktanbefalinger** > **Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="9a7ea-127">Vælg **Anbefalingslister** på listen over delte parametre.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="9a7ea-128">Vælg listen, du vil tilføje eller fjerne produkter fra.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="9a7ea-129">Hvis du vil føje produkter til tabellen, skal du vælge **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="9a7ea-130">Søg efter et produkts **Navn** eller **Produktnummer** i produktkolonnen.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Eksempel på søgning efter et produkt på listen Nyt produkt](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="9a7ea-132">I kolonnen Linjetype skal du vælge en af to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="9a7ea-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="9a7ea-133">**Medtag** – tvinger et produkt op forrest på listen</span><span class="sxs-lookup"><span data-stu-id="9a7ea-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="9a7ea-134">**Udeluk** – fjerner et produkt, så det ikke bliver vist på listen</span><span class="sxs-lookup"><span data-stu-id="9a7ea-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Eksempel på, hvordan et produkt medtages eller udelukkes fra listen Nyt produkt](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="9a7ea-136">Hvis du ændrer **Visningsrækkefølge**, ændres den rækkefølge, som de produkter, der er markeret **medtag**, vises i på listen.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="9a7ea-137">Hvis to produkter har samme værdi for **visningsrækkefølge**, kan den endelige rækkefølge af disse to resultater afvige fra administrationens.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="9a7ea-138">Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="9a7ea-139">For listerne "Andre synes også godt om" eller "Ofte købt sammen"</span><span class="sxs-lookup"><span data-stu-id="9a7ea-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="9a7ea-140">I forbindelse med listerne "Ofte købt sammen" eller "Andre synes også godt om" bruges maskinel indlæring til at analysere forbrugeres indkøbsmønstre for at anbefale relaterede produkter, der ofte købes sammen, som et produkt med entydig oprindelse.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="9a7ea-141">Et *oprindelsesprodukt* er det produkt, du vil generere resultater for.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="9a7ea-142">I forbindelse med manuel justering af anbefalingslister tilføjer eller fjerner du resultater for dette produkt.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="9a7ea-143">Udfør følgende trin for manuelt at tilføje eller fjerne resultater for et oprindelsesprodukt:</span><span class="sxs-lookup"><span data-stu-id="9a7ea-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="9a7ea-144">Vælg **Oprindelsesprodukt**.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="9a7ea-145">Søg i kolonnen **Produkt** efter et produkt ud fra **Navn** eller **Produktnummer**.
![Eksempel på søgning efter et produkt på listen Ofte købt sammen](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="9a7ea-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="9a7ea-146">I kolonnen **Linjetype** skal du vælge en af to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="9a7ea-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="9a7ea-147">**Medtag** – tvinger et produkt op forrest på listen</span><span class="sxs-lookup"><span data-stu-id="9a7ea-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="9a7ea-148">**Udeluk** – fjerner et produkt, så det ikke bliver vist på listen</span><span class="sxs-lookup"><span data-stu-id="9a7ea-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="9a7ea-149">![Eksempel på at medtage eller udelukke et produkt fra listen Ofte købte sammen](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="9a7ea-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="9a7ea-150">Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge Fjern.</span><span class="sxs-lookup"><span data-stu-id="9a7ea-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9a7ea-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9a7ea-151">Additional resources</span></span>

[<span data-ttu-id="9a7ea-152">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a7ea-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9a7ea-153">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="9a7ea-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9a7ea-154">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a7ea-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9a7ea-155">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a7ea-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9a7ea-156">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a7ea-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9a7ea-157">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="9a7ea-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9a7ea-158">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="9a7ea-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9a7ea-159">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="9a7ea-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9a7ea-160">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="9a7ea-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9a7ea-161">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="9a7ea-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9a7ea-162">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="9a7ea-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
