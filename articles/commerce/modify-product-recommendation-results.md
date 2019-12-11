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
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770064"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="5c75b-103">Administrere resultater for AI-ML-baserede produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5c75b-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5c75b-104">I dette emne beskrives, hvordan du kan skræddersy resultater fra produktanbefalinger på basis af kunstig intelligens-maskinel indlæring (AI-ML) til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="5c75b-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="5c75b-105">Når du har aktiveret produktanbefalinger, træder standardindstillingerne i kraft. Disse parametre kan bruges ved mange behov og til mange formål.</span><span class="sxs-lookup"><span data-stu-id="5c75b-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="5c75b-106">Det er bedst at planlægge at bruge tid på at evaluere, om resultaterne opfylder produkternes markedsbevægelse.</span><span class="sxs-lookup"><span data-stu-id="5c75b-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="5c75b-107">Vi foreslår, at du evaluerer resultaterne i nogle dage, før du ændrer parametre efter behov og tester igen.</span><span class="sxs-lookup"><span data-stu-id="5c75b-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="5c75b-108">Om parametre for anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="5c75b-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="5c75b-109">Før du ændrer parametrene, skal du sætte dig ind i, hvordan de påvirker resultaterne nedenfor.</span><span class="sxs-lookup"><span data-stu-id="5c75b-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="5c75b-110">Liste over populære produkter</span><span class="sxs-lookup"><span data-stu-id="5c75b-110">Trending product list</span></span>

<span data-ttu-id="5c75b-111">Listen med **Mest populære** for produkter har to parametre, der kan ændres: ![Eksempel på standardparametre for tendensliste](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="5c75b-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="5c75b-112">**Medtag nye produkter fra de seneste X dage** - Produkter, der er blevet tilføjet inden for det angivne antal dage, før den aktuelle dato kan bruges til at vælge produktkandidater.</span><span class="sxs-lookup"><span data-stu-id="5c75b-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="5c75b-113">Standardværdien på billedet antyder, at produkter så gamle som 180 dage, kan bruges på listen med populære produkter.</span><span class="sxs-lookup"><span data-stu-id="5c75b-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="5c75b-114">**Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne.</span><span class="sxs-lookup"><span data-stu-id="5c75b-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="5c75b-115">Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over populære produkter.</span><span class="sxs-lookup"><span data-stu-id="5c75b-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="5c75b-116">Liste over bedst sælgende produkter</span><span class="sxs-lookup"><span data-stu-id="5c75b-116">Best selling product list</span></span>

<span data-ttu-id="5c75b-117">Afhængigt af virksomheden kan Bedst sælgende give et andet resultat end Tendens, selvom de begge bruger transaktionsdata til at rangordne produkter.</span><span class="sxs-lookup"><span data-stu-id="5c75b-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="5c75b-118">Da Bedst sælgende ikke har nogen skæring baseret på dato for udvælgelse, kan Bedst sælgende stadig fremhæve meget populære produkter af ældre dato, der muligvis er blevet slettet fra popularitetslisten.</span><span class="sxs-lookup"><span data-stu-id="5c75b-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="5c75b-119">Produktlisten **Bedst sælgende** har én parameter, der kan ændres:</span><span class="sxs-lookup"><span data-stu-id="5c75b-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Eksempel på standardparameter for liste over bedst sælgende](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="5c75b-121">**Medtag salg fra de seneste X dage** - Salgstransaktioner, der er foretaget inden for det angivne antal dage før den aktuelle dato, kan bruges til at vælge produkterne.</span><span class="sxs-lookup"><span data-stu-id="5c75b-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="5c75b-122">Standardværdien ovenfor antyder, at alle køb, der er foretaget af et produkt inden for de seneste 30 dage, bruges til at bestemme produktets placering på listen over bedst sælgende produkter.</span><span class="sxs-lookup"><span data-stu-id="5c75b-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="5c75b-123">Tilføje eller fjerne produkter manuelt fra anbefalingslister</span><span class="sxs-lookup"><span data-stu-id="5c75b-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="5c75b-124">For Ny, Mest populære eller Bedst sælgende</span><span class="sxs-lookup"><span data-stu-id="5c75b-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="5c75b-125">Gå til **Detail** > **Produktanbefalinger** > **Anbefalingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="5c75b-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="5c75b-126">Vælg **Anbefalingslister** på listen over delte detailparametre.</span><span class="sxs-lookup"><span data-stu-id="5c75b-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="5c75b-127">Vælg listen, du vil tilføje eller fjerne produkter fra.</span><span class="sxs-lookup"><span data-stu-id="5c75b-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="5c75b-128">Hvis du vil føje produkter til tabellen, skal du vælge **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="5c75b-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="5c75b-129">Søg i kolonnen Produkt efter et produkt ud fra **Navn** eller **Produktnummer**.
![Eksempel på søgning efter et produkt på listen Ny produkt](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="5c75b-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="5c75b-130">I kolonnen Linjetype skal du vælge en af to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5c75b-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="5c75b-131">**Medtag** – tvinger et produkt op forrest på listen</span><span class="sxs-lookup"><span data-stu-id="5c75b-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="5c75b-132">**Udeluk** – fjerner et produkt, så det ikke bliver vist på listen ![Eksempel på at medtage eller udelukke et produkt fra listen Ny produkt](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="5c75b-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="5c75b-133">Hvis du ændrer **Visningsrækkefølge**, ændres den rækkefølge, som de produkter, der er markeret **medtag**, vises i på listen.</span><span class="sxs-lookup"><span data-stu-id="5c75b-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="5c75b-134">Hvis to produkter har samme værdi for **visningsrækkefølge**, kan den endelige rækkefølge af disse to resultater afvige fra administrationens.</span><span class="sxs-lookup"><span data-stu-id="5c75b-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="5c75b-135">Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="5c75b-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="5c75b-136">For listerne Andre synes også godt om eller Ofte er købt sammen</span><span class="sxs-lookup"><span data-stu-id="5c75b-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="5c75b-137">I forbindelse med listerne **Ofte købt sammen** eller **Andre synes også godt om** bruges maskinel indlæring til at analysere forbrugeres indkøbsmønstre for at anbefale relaterede produkter, der ofte købes sammen, som et produkt med entydig oprindelse.</span><span class="sxs-lookup"><span data-stu-id="5c75b-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="5c75b-138">Et **oprindelsesprodukt** er det produkt, du vil generere resultater for.</span><span class="sxs-lookup"><span data-stu-id="5c75b-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="5c75b-139">I forbindelse med manuel justering af anbefalingslister tilføjer eller fjerner du resultater for dette produkt.</span><span class="sxs-lookup"><span data-stu-id="5c75b-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="5c75b-140">Udfør følgende trin for manuelt at tilføje eller fjerne resultater for et oprindelsesprodukt:</span><span class="sxs-lookup"><span data-stu-id="5c75b-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="5c75b-141">Vælg **Oprindelsesprodukt**.</span><span class="sxs-lookup"><span data-stu-id="5c75b-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="5c75b-142">Søg i kolonnen **Produkt** efter et produkt ud fra **Navn** eller **Produktnummer**.
![Eksempel på søgning efter et produkt på listen Ofte købt sammen](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="5c75b-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="5c75b-143">I kolonnen **Linjetype** skal du vælge en af to indstillinger:</span><span class="sxs-lookup"><span data-stu-id="5c75b-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="5c75b-144">**Medtag** – tvinger et produkt op forrest på listen</span><span class="sxs-lookup"><span data-stu-id="5c75b-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="5c75b-145">**Udeluk** – fjerner et produkt, så det ikke bliver vist på listen</span><span class="sxs-lookup"><span data-stu-id="5c75b-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="5c75b-146">![Eksempel på at medtage eller udelukke et produkt fra listen Ofte købte sammen](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="5c75b-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="5c75b-147">Hvis du vil fjerne produkter fra tabellen, skal du markere den linje, du vil fjerne, og vælge Fjern.</span><span class="sxs-lookup"><span data-stu-id="5c75b-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5c75b-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5c75b-148">Additional resources</span></span>

[<span data-ttu-id="5c75b-149">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5c75b-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5c75b-150">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5c75b-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="5c75b-151">Tilføje lister med produktanbefalinger på sider</span><span class="sxs-lookup"><span data-stu-id="5c75b-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
