---
title: Aktivere anbefalinger af "Køb tilsvarende beskrivelse"
description: Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende beskrivelse" i Microsoft Dynamics 365 Commerce.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ce01ef1d4b916d955685b4d01dafd3d54d6fcebd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795399"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="42833-103">Aktivér anbefalinger af "Køb tilsvarende beskrivelse"</span><span class="sxs-lookup"><span data-stu-id="42833-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42833-104">Dette emne beskriver, hvordan du aktiverer produktanbefalingerne "Køb tilsvarende beskrivelse" i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42833-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="42833-105">Anbefalingsfunktionen "Køb tilsvarende beskrivelse" i Dynamics 365 Commerce bruger styrkerne i kunstig intelligens og maskinel læring (AI-ML) til at give anbefalinger til produkter, der er beskrivelser, der svarer til det, kunden leder efter.</span><span class="sxs-lookup"><span data-stu-id="42833-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="42833-106">Når du gør anbefalinger af typen "Køb tilsvarende beskrivelse" tilgængelige for alle detailkanaler i Commerce, kan detailhandlerne hjælpe kunderne til nemt at finde det, de ønsker.</span><span class="sxs-lookup"><span data-stu-id="42833-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="42833-107">Anbefalingsfunktionen "Køb tilsvarende beskrivelse" bruger produktafbildninger af rangerede produktnavn og beskrivelse til at finde og anbefale visuelt tilsvarende produkter i en forhandlers produktkatalog.</span><span class="sxs-lookup"><span data-stu-id="42833-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="42833-108">Anbefalinger af typen "Køb tilsvarende beskrivelse" er tilgængelige i både POS- og e-handelsløsninger.</span><span class="sxs-lookup"><span data-stu-id="42833-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="42833-109">Eksempelscenarier</span><span class="sxs-lookup"><span data-stu-id="42833-109">Example scenarios</span></span>

<span data-ttu-id="42833-110">Scenarierne nedenfor viser de typer af anbefalinger, som funktionen "køb tilsvarende beskrivelse" kan indeholde:</span><span class="sxs-lookup"><span data-stu-id="42833-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="42833-111">En kunde får at se et par års kontekster, der ligner hinanden, og modtager et sæt anbefalinger for andre produkter, der har et lignende design i detailbranchen.</span><span class="sxs-lookup"><span data-stu-id="42833-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="42833-112">En kunde bruger anbefalinger i "køb tilsvarende beskrivelse" til at finde kaffemærker, der ligner dem, de tidligere har købt af forhandleren.</span><span class="sxs-lookup"><span data-stu-id="42833-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="42833-113">Konfigurere anbefalinger af "Køb tilsvarende beskrivelse"</span><span class="sxs-lookup"><span data-stu-id="42833-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="42833-114">Produktanbefalinger understøttes kun for Commerce-brugere, som har overført deres lager til Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="42833-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="42833-115">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="42833-115">Prerequisites</span></span>

<span data-ttu-id="42833-116">Før "køb tilsvarende beskrivelse" kan vises til kunder, skal du udføre følgende forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="42833-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="42833-117">[Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="42833-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="42833-118">Bekræft, at medieserveren understøtter HTTPS-kald.</span><span class="sxs-lookup"><span data-stu-id="42833-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="42833-119">Aktivere funktionen med anbefalinger i "Køb tilsvarende beskrivelse"</span><span class="sxs-lookup"><span data-stu-id="42833-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="42833-120">Hvis du vil aktivere anbefalingsfunktionen "Køb tilsvarende beskrivelse" i Commerce Headquarters, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="42833-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="42833-121">I arbejdsområdet **Funktionsstyring** på listen over tilgængelige funktioner skal du søge efter og vælge **Køb tilsvarende beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="42833-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="42833-122">Vælg **Aktivér** i højre rude.</span><span class="sxs-lookup"><span data-stu-id="42833-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="42833-123">Når du aktiverer funktionen, begynder systemet at generere lister over produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="42833-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="42833-124">Der kan gå op til en dag, før disse lister er tilgængelige og synlige online og på POS-terminaler.</span><span class="sxs-lookup"><span data-stu-id="42833-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="42833-125">Hvis du deaktiverer funktionen, påvirkes andre typer produktanbefalinger ikke.</span><span class="sxs-lookup"><span data-stu-id="42833-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="42833-126">Yderligere oplysninger om produktanbefalinger finder du under [Oversigt over produktanbefalinger](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="42833-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="42833-127">Tilføje en knap med Køb tilsvarende beskrivelse til sider med produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="42833-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="42833-128">Når du har aktiveret funktionen "Køb tilsvarende beskrivelse" i Commerce Headquarters, kan en indstilling i Commerce-webstedsgenerator lade detailhandlere føje knappen **Køb tilsvarende beskrivelse** til købefeltet på alle produktoplysningssider (PDP).</span><span class="sxs-lookup"><span data-stu-id="42833-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="42833-129">En kunde, der vælger denne knap, føres til en dedikeret side af typen **Køb tilsvarende beskrivelse**, som returnerer visuelt tilsvarende produkter.</span><span class="sxs-lookup"><span data-stu-id="42833-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="42833-130">Kunden kan bruge vælgere til at filtrere produkterne yderligere.</span><span class="sxs-lookup"><span data-stu-id="42833-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="42833-131">Hvis du vil tilføje knappen **Køb tilsvarende beskrivelse** til en PDP ved hjælp af Commerce-webstedsgenerator, skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="42833-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="42833-132">Åbn en eksisterende side med webstedsgeneratoren, som indeholder et købefeltmodul.</span><span class="sxs-lookup"><span data-stu-id="42833-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="42833-133">Vælg købefeltmodulet i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="42833-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="42833-134">Marker afkrydsningsfeltet **Aktivér link til Køb tilsvarende beskrivelse** i højre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="42833-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="42833-135">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="42833-135">Select **Save**.</span></span>
1. <span data-ttu-id="42833-136">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="42833-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="42833-137">Når siden er udgivet, vil PDP inkludere knappen **Køb tilsvarende beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="42833-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="42833-138">I følgende illustration vises afkrydsningsfeltet **Aktiver link til Køb tilsvarende beskrivelse** og knappen **Køb tilsvarende beskrivelse** i et PDP-eksempel i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="42833-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![I følgende illustration vises afkrydsningsfeltet Aktiver link til Køb tilsvarende beskrivelse og knappen Køb tilsvarende på en PDP i webstedsgeneratoren.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="42833-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="42833-140">Additional resources</span></span>

[<span data-ttu-id="42833-141">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="42833-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="42833-142">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="42833-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="42833-143">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="42833-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="42833-144">Aktivér anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="42833-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="42833-145">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="42833-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="42833-146">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="42833-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="42833-147">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="42833-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]