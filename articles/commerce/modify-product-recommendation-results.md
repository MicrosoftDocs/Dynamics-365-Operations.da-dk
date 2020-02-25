---
title: Administrere resultater for AI-ML-baserede produktanbefalinger
description: I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 5da77f71fb2569adc011bb9ee9c8c795d85545f8
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024996"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="deec6-103">Administrere resultater for AI-ML-baserede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="deec6-103">Manage AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="deec6-104">I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="deec6-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="deec6-105">Når du har aktiveret produktanbefalinger, træder standardindstillingerne i kraft. Disse parametre kan bruges ved mange behov og til mange formål.</span><span class="sxs-lookup"><span data-stu-id="deec6-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="deec6-106">Det er bedst at planlægge at bruge tid på at evaluere, om resultaterne opfylder produkternes markedsbevægelse.</span><span class="sxs-lookup"><span data-stu-id="deec6-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="deec6-107">Vi foreslår, at du evaluerer resultaterne i nogle dage, før du ændrer parametre efter behov og tester igen.</span><span class="sxs-lookup"><span data-stu-id="deec6-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="deec6-108">Om parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="deec6-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="deec6-109">Før du ændrer parametrene, skal du sætte dig ind i, hvordan de påvirker resultaterne nedenfor.</span><span class="sxs-lookup"><span data-stu-id="deec6-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="deec6-110">Liste over mest populære produkter</span><span class="sxs-lookup"><span data-stu-id="deec6-110">"Trending" product list</span></span>

<span data-ttu-id="deec6-111">Listen over de mest populære produkter har to parametre, der kan ændres:</span><span class="sxs-lookup"><span data-stu-id="deec6-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Eksempel på standardparametre for liste over mest populære produkter](./media/exampletrendingparameters.png)

1. <span data-ttu-id="deec6-113">**Medtag nye produkter fra de seneste X dage** - Produkter, der er blevet tilføjet inden for det angivne antal dage, før den aktuelle dato kan bruges til at vælge produktkandidater.</span><span class="sxs-lookup"><span data-stu-id="deec6-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="deec6-114">Standardværdien på billedet antyder, at produkter så gamle som 180 dage, kan bruges på listen med populære produkter.</span><span class="sxs-lookup"><span data-stu-id="deec6-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="deec6-115">**Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne.</span><span class="sxs-lookup"><span data-stu-id="deec6-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="deec6-116">Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over populære produkter.</span><span class="sxs-lookup"><span data-stu-id="deec6-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="deec6-117">Liste over mest solgte produkter</span><span class="sxs-lookup"><span data-stu-id="deec6-117">"Best selling" product list</span></span>

<span data-ttu-id="deec6-118">Afhængigt af din virksomhed kan listen over mest solgte produkter give et andet resultat end de mest populære produkter, selvom de begge bruger transaktionsdata til at rangordne produkter.</span><span class="sxs-lookup"><span data-stu-id="deec6-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="deec6-119">Da Bedst sælgende ikke har nogen skæring baseret på dato for udvælgelse, kan Bedst sælgende stadig fremhæve meget populære produkter af ældre dato, der muligvis er blevet slettet fra popularitetslisten.</span><span class="sxs-lookup"><span data-stu-id="deec6-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="deec6-120">Listen over de mest solgte produkter har én parameter, der kan ændres:</span><span class="sxs-lookup"><span data-stu-id="deec6-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Eksempel på standardparameter for liste over bedst sælgende](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="deec6-122">**Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne.</span><span class="sxs-lookup"><span data-stu-id="deec6-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="deec6-123">Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over bedst sælgende produkter.</span><span class="sxs-lookup"><span data-stu-id="deec6-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="deec6-124">Tilføje eller fjerne produkter manuelt fra anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="deec6-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="deec6-125">For listerne Ny, Mest populære eller Mest solgte</span><span class="sxs-lookup"><span data-stu-id="deec6-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="deec6-126">Gå til **Retail og Commerce** > **Produktanbefalinger** > **Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="deec6-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="deec6-127">Vælg **Anbefalingslister** på listen over delte parametre.</span><span class="sxs-lookup"><span data-stu-id="deec6-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="deec6-128">Vælg listen, du vil tilføje eller fjerne produkter fra.</span><span class="sxs-lookup"><span data-stu-id="deec6-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="deec6-129">Hvis du vil føje produkter til tabellen, skal du vælge **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="deec6-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="deec6-130">Søg efter et produkts **Navn** eller **Produktnummer** i produktkolonnen.</span><span class="sxs-lookup"><span data-stu-id="deec6-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Eksempel på søgning efter et produkt på listen Nyt produkt](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="deec6-132">I kolonnen Linjetype skal du vælge en af to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="deec6-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="deec6-133">**Medtag** – tvinger et produkt op forrest på listen</span><span class="sxs-lookup"><span data-stu-id="deec6-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="deec6-134">**Udeluk** – fjerner et produkt, så det ikke bliver vist på listen</span><span class="sxs-lookup"><span data-stu-id="deec6-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Eksempel på, hvordan et produkt medtages eller udelukkes fra listen Nyt produkt](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="deec6-136">Hvis du ændrer **Visningsrækkefølge**, ændres den rækkefølge, som de produkter, der er markeret **medtag**, vises i på listen.</span><span class="sxs-lookup"><span data-stu-id="deec6-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="deec6-137">Hvis to produkter har samme værdi for **visningsrækkefølge**, kan den endelige rækkefølge af disse to resultater afvige fra administrationens.</span><span class="sxs-lookup"><span data-stu-id="deec6-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="deec6-138">Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="deec6-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="deec6-139">For listerne "Andre synes også godt om" eller "Ofte købt sammen"</span><span class="sxs-lookup"><span data-stu-id="deec6-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="deec6-140">I forbindelse med listerne "Ofte købt sammen" eller "Andre synes også godt om" bruges maskinel indlæring til at analysere forbrugeres indkøbsmønstre for at anbefale relaterede produkter, der ofte købes sammen, som et produkt med entydig oprindelse.</span><span class="sxs-lookup"><span data-stu-id="deec6-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="deec6-141">Et *oprindelsesprodukt* er det produkt, du vil generere resultater for.</span><span class="sxs-lookup"><span data-stu-id="deec6-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="deec6-142">I forbindelse med manuel justering af anbefalingslister tilføjer eller fjerner du resultater for dette produkt.</span><span class="sxs-lookup"><span data-stu-id="deec6-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="deec6-143">Udfør følgende trin for manuelt at tilføje eller fjerne resultater for et oprindelsesprodukt:</span><span class="sxs-lookup"><span data-stu-id="deec6-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="deec6-144">Vælg **Oprindelsesprodukt**.</span><span class="sxs-lookup"><span data-stu-id="deec6-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="deec6-145">Søg i kolonnen **Produkt** efter et produkt ud fra **Navn** eller **Produktnummer**.
![Eksempel på søgning efter et produkt på listen Ofte købt sammen](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="deec6-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="deec6-146">I kolonnen **Linjetype** skal du vælge en af to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="deec6-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="deec6-147">**Medtag** – tvinger et produkt op forrest på listen</span><span class="sxs-lookup"><span data-stu-id="deec6-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="deec6-148">**Udeluk** – fjerner et produkt, så det ikke bliver vist på listen</span><span class="sxs-lookup"><span data-stu-id="deec6-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="deec6-149">![Eksempel på at medtage eller udelukke et produkt fra listen Ofte købte sammen](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="deec6-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="deec6-150">Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge Fjern.</span><span class="sxs-lookup"><span data-stu-id="deec6-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="deec6-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="deec6-151">Additional resources</span></span>

[<span data-ttu-id="deec6-152">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="deec6-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="deec6-153">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="deec6-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="deec6-154">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="deec6-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="deec6-155">Tilføje lister med produktanbefalinger på sider</span><span class="sxs-lookup"><span data-stu-id="deec6-155">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="deec6-156">Oversigt over modulet Produktsamling</span><span class="sxs-lookup"><span data-stu-id="deec6-156">Product collection module overview</span></span>](product-collection-module-overview.md)
