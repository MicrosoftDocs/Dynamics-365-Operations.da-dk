---
title: Modulet Butiksvælger
description: Dette emne omhandler modulet Butiksvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157334"
---
# <a name="store-selector-module"></a><span data-ttu-id="14baf-103">Modulet Butiksvælger</span><span class="sxs-lookup"><span data-stu-id="14baf-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14baf-104">Dette emne omhandler modulet Butiksvælger og beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="14baf-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="14baf-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="14baf-105">Overview</span></span>

<span data-ttu-id="14baf-106">Et butiksvælgermodul bruges til kundescenariet "Køb online, afhent i butikken" (BOPIS).</span><span class="sxs-lookup"><span data-stu-id="14baf-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="14baf-107">I modulet vises en liste over butikker, hvor et produkt kan afhentes, samt åbningstider og produktbeholdning for hver butik.</span><span class="sxs-lookup"><span data-stu-id="14baf-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="14baf-108">Butiksvælgermodulet kræver en produktkontekst og en søgeplacering, når du vil finde butikker.</span><span class="sxs-lookup"><span data-stu-id="14baf-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="14baf-109">Hvis der ikke findes en søgeplacering, bruges som standard kundens browserplacering, hvis kunden giver samtykke.</span><span class="sxs-lookup"><span data-stu-id="14baf-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="14baf-110">Modulet har et inputfelt, som giver kunden mulighed for at angive et sted (postnummer eller by og stat) for at finde butikker i nærheden.</span><span class="sxs-lookup"><span data-stu-id="14baf-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="14baf-111">Modulet Butiksvælger er integreret med Bing Maps Geocoding-API'en (Application Programming Interface) til at konvertere det sted, som kunden indtastede, til en bredde- og en længdegrad.</span><span class="sxs-lookup"><span data-stu-id="14baf-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="14baf-112">Der kræves en Bing Kort-API-nøgle, og den skal føjes til siden med delte parametre for Commerce i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="14baf-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="14baf-113">Butiksvælgermodulet kan føjes til et købefeltmodul på siden med produktdetaljer (PDP), hvis du vil have vist butikker, hvor et produkt kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="14baf-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="14baf-114">Modulet kan også føjes til et indkøbsvognmodul.</span><span class="sxs-lookup"><span data-stu-id="14baf-114">It can also be added to a cart module.</span></span> <span data-ttu-id="14baf-115">Når butiksvælgermodulet føjes til et indkøbsvognmodul, vises afhentningsindstillinger for de enkelte linjevarer i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="14baf-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="14baf-116">Desuden kan dette modul ved hjælp af brugerdefineret kodning føjes til andre sider eller moduler via udvidelser og tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="14baf-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="14baf-117">Hvis BOPIS-scenariet skal fungere, skal produkterne konfigureres med leveringstilstanden "kundeafhentning".</span><span class="sxs-lookup"><span data-stu-id="14baf-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="14baf-118">Ellers bliver modulet ikke vist på de respektive sider.</span><span class="sxs-lookup"><span data-stu-id="14baf-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="14baf-119">Du kan finde flere oplysninger om, hvordan du kan konfigurere leveringsmåden, i [Konfigurere leveringsmåder](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="14baf-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="14baf-120">Følgende billede viser et eksempel på et butiksvælgermodul, der bruges på en produktoplysningsside (PDP).</span><span class="sxs-lookup"><span data-stu-id="14baf-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Eksempel på et butiksvælgermodul](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="14baf-122">Brug af butiksvælgermodul i e-handel</span><span class="sxs-lookup"><span data-stu-id="14baf-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="14baf-123">Et butiksvælgermodul kan bruges på en side med produktdetaljer (PDP) til at finde butikker i nærheden, hvor et produkt kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="14baf-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="14baf-124">Et butiksvælgermodul kan bruges på en indkøbsvognside til at finde butikker i nærheden, hvor et produkt i indkøbsvognen kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="14baf-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="14baf-125">Egenskaber for modulet Butiksvælger</span><span class="sxs-lookup"><span data-stu-id="14baf-125">Store selector module properties</span></span>

| <span data-ttu-id="14baf-126">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="14baf-126">Property name</span></span>             | <span data-ttu-id="14baf-127">Værdi</span><span class="sxs-lookup"><span data-stu-id="14baf-127">Value</span></span>                 | <span data-ttu-id="14baf-128">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="14baf-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="14baf-129">Søgeradius</span><span class="sxs-lookup"><span data-stu-id="14baf-129">Search radius</span></span> | <span data-ttu-id="14baf-130">Tal</span><span class="sxs-lookup"><span data-stu-id="14baf-130">Number</span></span> | <span data-ttu-id="14baf-131">Definerer søgeradius for butikker, i miles.</span><span class="sxs-lookup"><span data-stu-id="14baf-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="14baf-132">Hvis der ikke er angivet en værdi, bruges standardradiussen på 50 miles.</span><span class="sxs-lookup"><span data-stu-id="14baf-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="14baf-133">Vilkår for brug</span><span class="sxs-lookup"><span data-stu-id="14baf-133">Terms of Service</span></span> | <span data-ttu-id="14baf-134">URL-adresse</span><span class="sxs-lookup"><span data-stu-id="14baf-134">URL</span></span>    |  <span data-ttu-id="14baf-135">URL-adressen til servicebetingelserne skal angives for Bing Kort-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="14baf-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="14baf-136">Føje et butiksvælgermodul til en side</span><span class="sxs-lookup"><span data-stu-id="14baf-136">Add a store selector module to a page</span></span>

<span data-ttu-id="14baf-137">Et butiksvælgermodul skal bruge en produktkontekst, så det kan kun bruges i forbindelse med købefelt- og indkøbsvognmoduler.</span><span class="sxs-lookup"><span data-stu-id="14baf-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="14baf-138">Butiksvælgermoduler fungerer ikke uden for disse moduler.</span><span class="sxs-lookup"><span data-stu-id="14baf-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="14baf-139">Yderligere oplysninger om, hvordan du føjer et butiksvælgermodul til et købefeltmodul, finder du under [Købefeltmodul](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="14baf-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="14baf-140">Oplysninger om, hvordan du føjer et butiksvælgermodul til et indkøbsvognmodul, finder du under [Indkøbsvognmodul](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="14baf-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14baf-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="14baf-141">Additional resources</span></span>

[<span data-ttu-id="14baf-142">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="14baf-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="14baf-143">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="14baf-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="14baf-144">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="14baf-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="14baf-145">Hurtig rundvisning i PDP</span><span class="sxs-lookup"><span data-stu-id="14baf-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="14baf-146">Hurtig rundvisning i Indkøbsvogn og betaling</span><span class="sxs-lookup"><span data-stu-id="14baf-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="14baf-147">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="14baf-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
