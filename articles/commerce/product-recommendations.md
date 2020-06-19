---
title: Oversigt over produktanbefalinger
description: Dette emne indeholder generelle oplysninger om produktanbefalinger. Produktanbefalinger giver kunderne mulighed for nemt og hurtigt at finde produkter, som de ønsker, og endda produkter, som de oprindeligt ikke havde tænkt sig at købe.
author: Moonma
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
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1b01589322c26b6a7b69d1b992b03603f5f3d29a
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404342"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="3f99a-104">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f99a-105">Microsoft Dynamics 365 Commerce kan bruges til at få vist produktanbefalinger på e-handels-webstedet og POS-enheden.</span><span class="sxs-lookup"><span data-stu-id="3f99a-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="3f99a-106">Produktanbefalinger er varer, som en kunde kan være interesseret i.</span><span class="sxs-lookup"><span data-stu-id="3f99a-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="3f99a-107">Anbefalingerne er baseret på indkøbstendenser fra andre kunder i onlinebutikker og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="3f99a-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="3f99a-108">Produktanbefalinger gør det nemt og hurtigt for kunderne at finde produkter, som de ønsker, mens de har en god oplevelse.</span><span class="sxs-lookup"><span data-stu-id="3f99a-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="3f99a-109">Krydssalg og mersalg kan også bruges til at hjælpe kunder med at finde flere produkter, end de oprindeligt havde tænkt sig at købe.</span><span class="sxs-lookup"><span data-stu-id="3f99a-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="3f99a-110">Når anbefalingerne bruges til at forbedre produktregistrering, kan de skabe flere konverteringsmuligheder, bidrage til at øge salgsindtægterne og endda forbedre kundetilfredshed og -fastholdelse.</span><span class="sxs-lookup"><span data-stu-id="3f99a-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="3f99a-111">I e-handel er produktanbefalingerne baseret på Microsofts anbefalinger fra teknologier for maskinel indlæring i stor målestok.</span><span class="sxs-lookup"><span data-stu-id="3f99a-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="3f99a-112">Anbefalingstjeneste</span><span class="sxs-lookup"><span data-stu-id="3f99a-112">Recommendation service</span></span>

<span data-ttu-id="3f99a-113">Tjenesten Produktanbefalinger anvender kunstig intelligens- og maskinlæringsteknologier (AI-ML) på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3f99a-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="3f99a-114">Data i det format, der kræves af anbefalingstjenesten, udtrækkes fra Commerce-driftsdatabasen og sendes til Azure Data Lake Storage eller til enhedslageret.</span><span class="sxs-lookup"><span data-stu-id="3f99a-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="3f99a-115">Anbefalingstjenesten bruger de lagrede data til at træne anbefalingsmodellerne for listerne **Personer synes også om**, **Ofte købt sammen**, **Nyt**, **Mest solgte** og **Mest populære**.</span><span class="sxs-lookup"><span data-stu-id="3f99a-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="3f99a-116">Scenarier</span><span class="sxs-lookup"><span data-stu-id="3f99a-116">Scenarios</span></span>

<span data-ttu-id="3f99a-117">Produktanbefalinger er tilgængelige for følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="3f99a-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="3f99a-118">**På en butiksside til gennemsyn eller landingsside i e-handel**: Hvis kunder eller butiksansatte besøger en butiks side, kan anbefalingsprogrammet foreslå produkter på de nye lister **Nyt**, **Mest solgte** og **Mest populære**.</span><span class="sxs-lookup"><span data-stu-id="3f99a-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="3f99a-119">**På siden Produktdetaljer:** Hvis kunder eller butiksansatte besøger siden **Produktdetaljer**, foreslår anbefalingsprogrammet yderligere varer, der formentlig også er interessante at købe.</span><span class="sxs-lookup"><span data-stu-id="3f99a-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="3f99a-120">Disse varer vises på listen **Personer synes også om**.</span><span class="sxs-lookup"><span data-stu-id="3f99a-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="3f99a-121">**På siden Transaktion eller ved kassen:** Anbefalingsprogrammet foreslår varer på basis af hele listen med varer i kurven.</span><span class="sxs-lookup"><span data-stu-id="3f99a-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="3f99a-122">Disse varer vises på listen **Ofte købt sammen**.</span><span class="sxs-lookup"><span data-stu-id="3f99a-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="3f99a-123">**Personlige anbefalinger:** Forhandlere kan give logon-kunder en personligt **udvalgt** liste samt nye funktioner, der gør det muligt at tilpasse eksisterende listescenarier efter den pågældende kunde.</span><span class="sxs-lookup"><span data-stu-id="3f99a-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="3f99a-124">Du kan få mere at vide i [Aktivere tilpassede anbefalinger.](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3f99a-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="3f99a-125">Typer af produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-125">Types of product recommendations</span></span>

<span data-ttu-id="3f99a-126">I følgende tabel beskrives de forskellige typer automatiske produktanbefalinger, der er tilgængelige for detailhandlere med henblik på implementering i deres Dynamics 365 Commerce-løsning via [modulet Produktsamling](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3f99a-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="3f99a-127">Detailhandlende kan også vise personlige resultater for en bruger, der er logget på, hvis webstedets forfatter vælger denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="3f99a-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="3f99a-128">Produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="3f99a-128">Product collection module</span></span>  | <span data-ttu-id="3f99a-129">Type</span><span class="sxs-lookup"><span data-stu-id="3f99a-129">Type</span></span> | <span data-ttu-id="3f99a-130">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="3f99a-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="3f99a-131">Nye</span><span class="sxs-lookup"><span data-stu-id="3f99a-131">New</span></span>                        | <span data-ttu-id="3f99a-132">Algoritmisk</span><span class="sxs-lookup"><span data-stu-id="3f99a-132">Algorithmic</span></span> | <span data-ttu-id="3f99a-133">Dette modul viser en liste over de nyeste produkter, der for nyligt er blevet udvalgt til kanaler og kataloger.</span><span class="sxs-lookup"><span data-stu-id="3f99a-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="3f99a-134">Bedst sælgende</span><span class="sxs-lookup"><span data-stu-id="3f99a-134">Best selling</span></span>               | <span data-ttu-id="3f99a-135">Algoritmisk</span><span class="sxs-lookup"><span data-stu-id="3f99a-135">Algorithmic</span></span> | <span data-ttu-id="3f99a-136">Dette modul viser en liste over produkter, der er rangeret efter det højeste salgsantal.</span><span class="sxs-lookup"><span data-stu-id="3f99a-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="3f99a-137">Tendenser</span><span class="sxs-lookup"><span data-stu-id="3f99a-137">Trending</span></span>                   | <span data-ttu-id="3f99a-138">Algoritmisk</span><span class="sxs-lookup"><span data-stu-id="3f99a-138">Algorithmic</span></span> | <span data-ttu-id="3f99a-139">Dette modul viser en liste over de mest populære produkter i et givet tidsinterval, sorteret efter højeste salg.</span><span class="sxs-lookup"><span data-stu-id="3f99a-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="3f99a-140">Ofte købt sammen</span><span class="sxs-lookup"><span data-stu-id="3f99a-140">Frequently bought together</span></span> | <span data-ttu-id="3f99a-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="3f99a-141">AI-ML</span></span> | <span data-ttu-id="3f99a-142">Dette modul anbefaler en liste over produkter, der ofte købes sammen med indholdet af den aktuelle bruger kurv.</span><span class="sxs-lookup"><span data-stu-id="3f99a-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="3f99a-143">Folk kan også godt lide</span><span class="sxs-lookup"><span data-stu-id="3f99a-143">People also like</span></span>           | <span data-ttu-id="3f99a-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="3f99a-144">AI-ML</span></span> | <span data-ttu-id="3f99a-145">Dette modul anbefaler produkter til et bestemt basisprodukt baseret på forbrugernes købsmønstre.</span><span class="sxs-lookup"><span data-stu-id="3f99a-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="3f99a-146">Muligheder til dig</span><span class="sxs-lookup"><span data-stu-id="3f99a-146">Picks for you</span></span>              | <span data-ttu-id="3f99a-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="3f99a-147">AI-ML</span></span> | <span data-ttu-id="3f99a-148">Dette modul anbefaler en personlig liste over produkter, der er baseret på købsmønstre for den bruger, der er logget på.</span><span class="sxs-lookup"><span data-stu-id="3f99a-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="3f99a-149">For en gæstebruger vil denne liste være skjult.</span><span class="sxs-lookup"><span data-stu-id="3f99a-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="3f99a-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3f99a-150">Additional resources</span></span>

[<span data-ttu-id="3f99a-151">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="3f99a-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="3f99a-152">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3f99a-153">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3f99a-154">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="3f99a-155">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="3f99a-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="3f99a-156">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="3f99a-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3f99a-157">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3f99a-158">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="3f99a-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3f99a-159">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="3f99a-159">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3f99a-160">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="3f99a-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
