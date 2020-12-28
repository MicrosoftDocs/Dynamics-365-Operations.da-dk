---
title: Aktivrtr anbefalinger af "Køb tilsvarende"
description: Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende" i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411153"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="34f45-103">Aktivrtr anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="34f45-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34f45-104">Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende" i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34f45-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34f45-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="34f45-105">Overview</span></span>

<span data-ttu-id="34f45-106">Anbefalingsfunktionen "Køb tilsvarende" i Dynamics 365 Commerce bruger styrkerne i kunstig intelligens og maskinel læring (AI-ML) til at give anbefalinger af visuelt tilsvarende produkter til kunder.</span><span class="sxs-lookup"><span data-stu-id="34f45-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="34f45-107">Når du gør anbefalinger af typen "Køb tilsvarende" tilgængelige for alle detailkanaler i Commerce, kan detailhandlerne øge kundetilfredsheden ved at hjælpe kunderne til nemt at finde det, de ønsker.</span><span class="sxs-lookup"><span data-stu-id="34f45-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="34f45-108">Anbefalingsfunktionen "Køb tilsvarende" bruger produktafbildninger af rangerede produktvarianter til at finde og anbefale visuelt tilsvarende produkter i en forhandlers produktkatalog.</span><span class="sxs-lookup"><span data-stu-id="34f45-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="34f45-109">Anbefalinger af typen "Køb tilsvarende" er tilgængelige i både POS- og e-handelsløsninger.</span><span class="sxs-lookup"><span data-stu-id="34f45-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="34f45-110">Eksempelscenarier</span><span class="sxs-lookup"><span data-stu-id="34f45-110">Example scenarios</span></span>

- <span data-ttu-id="34f45-111">En kunde ser en sortstribet sweater og får en anbefaling afl en lignende sweater i rødt.</span><span class="sxs-lookup"><span data-stu-id="34f45-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="34f45-112">Kunden vælger det anbefalede produkt i stedet for det oprindeligt viste produkt og modtager derefter anbefalinger af lignende produkter i rødt.</span><span class="sxs-lookup"><span data-stu-id="34f45-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="34f45-113">En kunde bruger anbefalinger af typen "Køb tilsvarende" til at finde frem til matchende ørenringe til en ringe, som kunden er interesseret i at købe.</span><span class="sxs-lookup"><span data-stu-id="34f45-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="34f45-114">Aktivere anbefalinger af typen "Køb tilsvarende" i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="34f45-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="34f45-115">Produktanbefalinger understøttes kun for Commerce-brugere, som har overført deres lager til Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="34f45-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="34f45-116">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="34f45-116">Prerequisites</span></span>

<span data-ttu-id="34f45-117">Før detailhandlere kan begynde at vise anbefalingerne "Køb tilsvarende" til kunderne, kræves to forudgående trin:</span><span class="sxs-lookup"><span data-stu-id="34f45-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="34f45-118">[Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="34f45-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="34f45-119">Bekræft, at medieserveren understøtter HTTPS-kald.</span><span class="sxs-lookup"><span data-stu-id="34f45-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="34f45-120">For at anbefalingsfunktionen kan få adgang til produktbillederne, skal detailhandlerne oprette URL-adresser for produkterne.</span><span class="sxs-lookup"><span data-stu-id="34f45-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="34f45-121">Hvis du vil oprette URL-adresser for produkter i Commerce Headquarters, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="34f45-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="34f45-122">Gå til **Produktbilleder**.</span><span class="sxs-lookup"><span data-stu-id="34f45-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="34f45-123">Gå til handlingsruden, og vælg **Definer medieskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="34f45-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="34f45-124">Vælg **Opret URL-adresser** under **URL-adresser for medier** i egenskabsruden **Definer medieskabelon**.</span><span class="sxs-lookup"><span data-stu-id="34f45-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="34f45-125">Når du aktiverer anbefalingsfunktionen "Køb tilsvarende", starter processen for oprettelse af produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="34f45-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="34f45-126">Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS-terminaler.</span><span class="sxs-lookup"><span data-stu-id="34f45-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="34f45-127">Hvis du vil aktivere anbefalingsfunktionen "Køb tilsvarende" i Commerce Headquarters, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="34f45-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="34f45-128">Gå til **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="34f45-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="34f45-129">På listen over tilgængelige funktioner kan du søge efter og vælge **Køb tilsvarende**.</span><span class="sxs-lookup"><span data-stu-id="34f45-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="34f45-130">I højre rude skal du vælge **Aktivér** for at aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="34f45-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="34f45-131">I følgende illustration vises funktionen **Køb tilsvarende** på siden **Funktionsstyring** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="34f45-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Funktionen Køb tilsvarende på siden Funktionsstyring i Commerce Headquarters](./media/enableshopsimilarlooks.png)

<span data-ttu-id="34f45-133">Når de foregående opgaver er udført, forbedres POS-klienter automatisk med et kontekstafhængigt panel for **Køb tilsvarende produkter**.</span><span class="sxs-lookup"><span data-stu-id="34f45-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="34f45-134">Hvis du vælger **Vis flere**, kan brugere af POS-terminalen føres til en dedikeret side af typen "Køb tilsvarende", der kan filtreres yderligere.</span><span class="sxs-lookup"><span data-stu-id="34f45-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="34f45-135">Hvis du deaktiverer funktionen "Køb tilsvarende", påvirkes ingen andre typer produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="34f45-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="34f45-136">Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="34f45-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="34f45-137">Tilføje en knap for Køb tilsvarende til produktdetaljesider ved hjælp af Commerce-webstedsgenerator</span><span class="sxs-lookup"><span data-stu-id="34f45-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="34f45-138">Når du har aktiveret funktionen "Køb tilsvarende" i Commerce Headquarters, kan en indstilling i Commerce-webstedsgenerator lade detailhandlere føje knappen **Køb tilsvarende** til købefeltet på alle produktoplysningssider (PDP).</span><span class="sxs-lookup"><span data-stu-id="34f45-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="34f45-139">En kunde, der vælger denne knap, føres til en dedikeret side af typen "Køb tilsvarende", som returnerer visuelt tilsvarende produkter.</span><span class="sxs-lookup"><span data-stu-id="34f45-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="34f45-140">Her kan kunden bruge vælgere til at filtrere produkterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="34f45-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="34f45-141">Hvis du vil tilføje knappen **Køb tilsvarende** til en PDP ved hjælp af Commerce-webstedsgenerator, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="34f45-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="34f45-142">Åbn en eksisterende side med webstedsgeneratoren, som indeholder et købefeltmodul.</span><span class="sxs-lookup"><span data-stu-id="34f45-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="34f45-143">Vælg købefeltmodulet i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="34f45-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="34f45-144">Marker afkrydsningsfeltet **Aktivér link til Køb tilsvarende** i højre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="34f45-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="34f45-145">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="34f45-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="34f45-146">Når siden er udgivet, vil PDP medtage knappen **Køb tilsvarende**.</span><span class="sxs-lookup"><span data-stu-id="34f45-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="34f45-147">I følgende illustration vises afkrydsningsfeltet **Aktiver link til Køb tilsvarende** og knappen **Køb tilsvarende** i et PDP-eksempel i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="34f45-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![I følgende illustration vises afkrydsningsfeltet Aktiver link til Køb tilsvarende og knappen Køb tilsvarende på en PDP i webstedsgeneratoren.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="34f45-149">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="34f45-149">Additional resources</span></span>

[<span data-ttu-id="34f45-150">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="34f45-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="34f45-151">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="34f45-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="34f45-152">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="34f45-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="34f45-153">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="34f45-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="34f45-154">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="34f45-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="34f45-155">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="34f45-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="34f45-156">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="34f45-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="34f45-157">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="34f45-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="34f45-158">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="34f45-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="34f45-159">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="34f45-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
