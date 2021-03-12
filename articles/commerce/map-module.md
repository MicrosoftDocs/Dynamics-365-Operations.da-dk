---
title: Kortmodul
description: Dette emne omhandler kortmoduler og beskriver, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e93358a9c76e8eb7bfb4ade4f772dece2aa5f7d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982484"
---
# <a name="map-module"></a><span data-ttu-id="71920-103">Kortmodul</span><span class="sxs-lookup"><span data-stu-id="71920-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="71920-104">Dette emne omhandler kortmoduler og beskriver, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71920-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="71920-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="71920-105">Overview</span></span>

<span data-ttu-id="71920-106">Et kortmodul viser butikkernes placering på et interaktivt kort, der gengives ved hjælp af [Webkontrolelementet Bing Kort V8](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="71920-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="71920-107">Der kræves en Bing Kort-API-nøgle, og den skal føjes til siden med delte parametre for Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="71920-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="71920-108">Kortmoduler indeholder forskellige visninger, f.eks. veje, fra luften og gadeniveau, som brugerne kan vælge for at se kortplaceringer.</span><span class="sxs-lookup"><span data-stu-id="71920-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="71920-109">De giver også mulighed for interaktioner som f.eks. zoom og udnyttelse af brugerens placering.</span><span class="sxs-lookup"><span data-stu-id="71920-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="71920-110">Et kortmodul fungerer sammen med modulet for butiksvælger for at bestemme de geografiske placeringer af butikker, der skal gengives på et kort.</span><span class="sxs-lookup"><span data-stu-id="71920-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="71920-111">Butiksvælger og kortmoduler fungerer interaktivt, når en bruger vælger en butik i et af disse moduler på en webside.</span><span class="sxs-lookup"><span data-stu-id="71920-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="71920-112">Kortmoduler kan udvides til andre scenarier udover interaktion med butiksvælgermoduler.</span><span class="sxs-lookup"><span data-stu-id="71920-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="71920-113">Modultilpasning er dog påkrævet.</span><span class="sxs-lookup"><span data-stu-id="71920-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="71920-114">Kortmodulet er tilgængeligt i Dynamics 365 Commerce version 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="71920-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="71920-115">Det følgende billede viser et eksempel på et kortmodul, der bruges på en side med butiksadresser.</span><span class="sxs-lookup"><span data-stu-id="71920-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Eksempel på et butiksvælgermodul](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="71920-117">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="71920-117">Module properties</span></span>

| <span data-ttu-id="71920-118">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="71920-118">Property name</span></span>             | <span data-ttu-id="71920-119">Værdi</span><span class="sxs-lookup"><span data-stu-id="71920-119">Value</span></span>                 | <span data-ttu-id="71920-120">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="71920-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="71920-121">Overskrift</span><span class="sxs-lookup"><span data-stu-id="71920-121">Heading</span></span> | <span data-ttu-id="71920-122">Tekst</span><span class="sxs-lookup"><span data-stu-id="71920-122">Text</span></span> | <span data-ttu-id="71920-123">Overskrift for modulet.</span><span class="sxs-lookup"><span data-stu-id="71920-123">The heading for the module.</span></span> |
| <span data-ttu-id="71920-124">Indstillinger for opslagsnål: standardikon</span><span class="sxs-lookup"><span data-stu-id="71920-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="71920-125">Billede</span><span class="sxs-lookup"><span data-stu-id="71920-125">Image</span></span> | <span data-ttu-id="71920-126">Det symbolbillede for opslagsnål, der bruges til butikker, som vises på et kort.</span><span class="sxs-lookup"><span data-stu-id="71920-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="71920-127">Indstillinger for opslagsnål: aktivt ikon</span><span class="sxs-lookup"><span data-stu-id="71920-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="71920-128">Billede</span><span class="sxs-lookup"><span data-stu-id="71920-128">Image</span></span> | <span data-ttu-id="71920-129">Det symbolbillede for opslagsnål, der bruges til en butik, der er valgt på et kort.</span><span class="sxs-lookup"><span data-stu-id="71920-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="71920-130">Indstillinger for opslagsnål: standardikonfarve</span><span class="sxs-lookup"><span data-stu-id="71920-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="71920-131">Tegnstreng</span><span class="sxs-lookup"><span data-stu-id="71920-131">Character string</span></span> | <span data-ttu-id="71920-132">Teksten eller den hexadecimale værdi for farven på symboler for opslagsnål på et kort.</span><span class="sxs-lookup"><span data-stu-id="71920-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="71920-133">Indstillinger for opslagsnål: farve på aktivt ikon</span><span class="sxs-lookup"><span data-stu-id="71920-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="71920-134">Tegnstreng</span><span class="sxs-lookup"><span data-stu-id="71920-134">Character string</span></span> | <span data-ttu-id="71920-135">Teksten eller den hexadecimale værdi for farven på symboler for den valgte opslagsnål på et kort.</span><span class="sxs-lookup"><span data-stu-id="71920-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="71920-136">Vis indeks</span><span class="sxs-lookup"><span data-stu-id="71920-136">Show index</span></span> | <span data-ttu-id="71920-137">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="71920-137">**True** or **False**</span></span> | <span data-ttu-id="71920-138">Hvis denne egenskab er indstillet til **Sand**, viser alle symboler på opslagsnål, der indikerer en butik, et indeks.</span><span class="sxs-lookup"><span data-stu-id="71920-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="71920-139">Dette indeks vil svare til indekset i listevisningen, som butiksvælgermodulet viser.</span><span class="sxs-lookup"><span data-stu-id="71920-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="71920-140">Føje tilladte URL-adresser til et websteds direktiver for sikkerhedspolitik</span><span class="sxs-lookup"><span data-stu-id="71920-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="71920-141">For at kortmodulet kan fungere interaktivt med Bing Kort, skal du sikre dig, at følgende tilknytnings-URL-adresser er tilladt pr. dit websteds sikkerhedspolitik for indhold (CSP).</span><span class="sxs-lookup"><span data-stu-id="71920-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="71920-142">Denne opsætning udføres i Commerce-webstedsgeneratoren ved at tilføje tilladte URL-adresser i forskellige CSP-direktiver (f.eks. **img-src**).</span><span class="sxs-lookup"><span data-stu-id="71920-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="71920-143">Du kan finde flere oplysninger under [Sikkerhedspolitik for indhold](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="71920-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="71920-144">Til **connect-src**-direktivet skal du tilføje **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="71920-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="71920-145">Til **img-src**-direktivet skal du tilføje **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="71920-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="71920-146">Til direktivet **script-src** skal du tilføje **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="71920-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="71920-147">Til direktivet **script style-src** skal du tilføje **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="71920-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="71920-148">Føje et kortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="71920-148">Add a map module to a page</span></span>

<span data-ttu-id="71920-149">Du kan finde detaljerede oplysninger om, hvordan du konfigurerer et kortmodul på en side, under [Butiksvælgermodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="71920-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="71920-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="71920-150">Additional resources</span></span>

[<span data-ttu-id="71920-151">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="71920-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="71920-152">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="71920-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="71920-153">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="71920-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="71920-154">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="71920-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="71920-155">Administrere Bing Kort for din organisation</span><span class="sxs-lookup"><span data-stu-id="71920-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="71920-156">Webkontrolelementet Bing Kort V8</span><span class="sxs-lookup"><span data-stu-id="71920-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
