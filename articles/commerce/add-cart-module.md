---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025430"
---
# <a name="cart-module"></a><span data-ttu-id="f469b-103">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f469b-104">Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f469b-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f469b-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f469b-105">Overview</span></span>

<span data-ttu-id="f469b-106">Et indkøbsvognmodul bruges til at få vist de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale.</span><span class="sxs-lookup"><span data-stu-id="f469b-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="f469b-107">Det omfatter f.eks. alle de varer, der er føjet til indkøbsvognen og en ordreoversigt.</span><span class="sxs-lookup"><span data-stu-id="f469b-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="f469b-108">Det giver også kunden mulighed for at anvende eller fjerne kampagnekoder.</span><span class="sxs-lookup"><span data-stu-id="f469b-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="f469b-109">Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst.</span><span class="sxs-lookup"><span data-stu-id="f469b-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="f469b-110">Den understøtter også et **Tilbage til indkøb**-link.</span><span class="sxs-lookup"><span data-stu-id="f469b-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="f469b-111">Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="f469b-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="f469b-112">Indkøbsvognmodulet gengiver data på basis af indkøbsvogn-id'et.</span><span class="sxs-lookup"><span data-stu-id="f469b-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="f469b-113">Indkøbsvogn-id'et er en browsercookie, der er tilgængelig på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="f469b-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="f469b-114">Egenskaber og pladser i indkøbsvognmodulet</span><span class="sxs-lookup"><span data-stu-id="f469b-114">Cart module properties and slots</span></span>

<span data-ttu-id="f469b-115">Indkøbsvognmodulet har en **Overskrift**-egenskab, der kan angives til værdier som f.eks. **Indkøbspose** og **Varer i indkøbsvognen**.</span><span class="sxs-lookup"><span data-stu-id="f469b-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="f469b-116">Moduler, der kan bruges i et indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="f469b-117">**Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="f469b-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="f469b-118">Meddelelserne styres af CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="f469b-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="f469b-119">Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".</span><span class="sxs-lookup"><span data-stu-id="f469b-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="f469b-120">**Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="f469b-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="f469b-121">Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden.</span><span class="sxs-lookup"><span data-stu-id="f469b-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="f469b-122">Modulet Butiksvælger er integreret med Bing Maps Geocoding-API'en (Application Programming Interface) til at konvertere det sted, som kunden indtastede, til en bredde- og en længdegrad.</span><span class="sxs-lookup"><span data-stu-id="f469b-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="f469b-123">Der kræves en Bing Maps-API-nøgle, og den skal føjes til den delte Retail-parameterside i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="f469b-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="f469b-124">Dette modul understøtter to egenskaber **Søgeradius** og **Link til vilkår for tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="f469b-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="f469b-125">Egenskaben **Søgeradius** definerer søgeradiussen for butikker, i miles.</span><span class="sxs-lookup"><span data-stu-id="f469b-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="f469b-126">Hvis der ikke er angivet en værdi, bruges standardradiussen, som er 50 miles.</span><span class="sxs-lookup"><span data-stu-id="f469b-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="f469b-127">Hvis Bing Maps eller en ekstern tjeneste bruges, kan egenskaben for **Link til vilkår for tjeneste** bruges til at angive et link til servicebetingelserne.</span><span class="sxs-lookup"><span data-stu-id="f469b-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="f469b-128">Tjenesten Bing Maps kræver et link til et serviceprogram.</span><span class="sxs-lookup"><span data-stu-id="f469b-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="f469b-129">Indstillinger for indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-129">Cart module settings</span></span>

<span data-ttu-id="f469b-130">Indkøbsvognmoduler har følgende indstillinger, der kan konfigureres på **Indstillinger for websted \> Udvidelser**:</span><span class="sxs-lookup"><span data-stu-id="f469b-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="f469b-131">**Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="f469b-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="f469b-132">En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.</span><span class="sxs-lookup"><span data-stu-id="f469b-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="f469b-133">**Lagerkontrol** – når værdien er angivet til **Sand**, føjes der først en vare til indkøbsvognen, når købefeltmodulet har sikret, at varen er på lager.</span><span class="sxs-lookup"><span data-stu-id="f469b-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="f469b-134">Denne lagerkontrol udføres både for de scenarier, hvor varen skal afsendes, og for scenarier, hvor den afhentes i butikken.</span><span class="sxs-lookup"><span data-stu-id="f469b-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="f469b-135">Hvis værdien er angivet til **Falsk**, udføres der ingen lagerkontrol, før der føjes en vare til indkøbsvognen, og ordren afgives.</span><span class="sxs-lookup"><span data-stu-id="f469b-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="f469b-136">**Lagerbuffer** – Denne egenskab bruges til at angive et buffernummer til lageret.</span><span class="sxs-lookup"><span data-stu-id="f469b-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="f469b-137">Lageret vedligeholdes i realtid, og når mange kunder afgiver ordrer, kan det være vanskeligt at bevare en nøjagtig lageroptælling.</span><span class="sxs-lookup"><span data-stu-id="f469b-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="f469b-138">Når der foretages en lagerkontrol, og lageret er mindre end bufferantallet, behandles produktet, som om det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="f469b-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="f469b-139">Når salg sker hurtigt via flere kanaler, og lageroptællingen ikke er synkroniseret, er der derfor mindre risiko for, at der sælges en vare, som ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="f469b-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="f469b-140">**Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**.</span><span class="sxs-lookup"><span data-stu-id="f469b-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="f469b-141">Denne rute kan konfigureres på webstedsniveau.</span><span class="sxs-lookup"><span data-stu-id="f469b-141">This route can be configured at the site level.</span></span> <span data-ttu-id="f469b-142">Detailhandlere kan bruge denne konfiguration til at føre kunden tilbage til startsiden eller en anden side på webstedet.</span><span class="sxs-lookup"><span data-stu-id="f469b-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="f469b-143">Enhedsinteraktion i Commerce Scale</span><span class="sxs-lookup"><span data-stu-id="f469b-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="f469b-144">Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er.</span><span class="sxs-lookup"><span data-stu-id="f469b-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="f469b-145">Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f469b-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="f469b-146">Føje et indkøbsvognmodul til en side</span><span class="sxs-lookup"><span data-stu-id="f469b-146">Add a cart module to a page</span></span>

<span data-ttu-id="f469b-147">Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f469b-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f469b-148">Opret et fragment med navnet **Indkøbsvognfragment**, og føj et indkøbsvognmodul til det.</span><span class="sxs-lookup"><span data-stu-id="f469b-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="f469b-149">Føj en overskrift til indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="f469b-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="f469b-150">Føj et butiksvælgermodul til indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="f469b-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="f469b-151">Gem fragmentet, afslut redigeringen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="f469b-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="f469b-152">Opret en skabelon med navnet **Indkøbsvognskabelon**, og føj det indkøbsvognfragment, som du netop har oprettet, til det.</span><span class="sxs-lookup"><span data-stu-id="f469b-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="f469b-153">Gem skabelonen, afslut redigeringen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="f469b-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="f469b-154">Opret en side, der bruger den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="f469b-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="f469b-155">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="f469b-155">Save and preview the page.</span></span>
1. <span data-ttu-id="f469b-156">Afslut redigeringen af siden, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="f469b-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f469b-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f469b-157">Additional resources</span></span>

[<span data-ttu-id="f469b-158">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="f469b-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f469b-159">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="f469b-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f469b-160">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f469b-161">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f469b-162">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f469b-163">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f469b-164">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f469b-164">Footer module</span></span>](author-footer-module.md)
