---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154011"
---
# <a name="cart-module"></a><span data-ttu-id="a8566-103">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8566-104">Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a8566-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a8566-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a8566-105">Overview</span></span>

<span data-ttu-id="a8566-106">Et indkøbsvognmodul viser de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale.</span><span class="sxs-lookup"><span data-stu-id="a8566-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="a8566-107">Modulet viser også en ordreoversigt, og kunden kan anvende eller fjerne kampagnekoder.</span><span class="sxs-lookup"><span data-stu-id="a8566-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="a8566-108">Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst.</span><span class="sxs-lookup"><span data-stu-id="a8566-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="a8566-109">Den understøtter også et **Tilbage til indkøb**-link.</span><span class="sxs-lookup"><span data-stu-id="a8566-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="a8566-110">Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.</span><span class="sxs-lookup"><span data-stu-id="a8566-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="a8566-111">I indkøbsvognmodulet gengives data baseret på indkøbsvogn-id'et, som er en browsercookie, der er tilgængelig på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="a8566-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="a8566-112">Egenskaber og pladser i indkøbsvognmodulet</span><span class="sxs-lookup"><span data-stu-id="a8566-112">Cart module properties and slots</span></span>

<span data-ttu-id="a8566-113">Indkøbsvognmodulet har en **Overskrift**-egenskab, der kan angives til værdier som f.eks. **Indkøbspose** og **Varer i indkøbsvognen**.</span><span class="sxs-lookup"><span data-stu-id="a8566-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="a8566-114">Moduler, der kan bruges i et indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="a8566-115">**Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="a8566-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="a8566-116">Meddelelserne styres af CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="a8566-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="a8566-117">Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".</span><span class="sxs-lookup"><span data-stu-id="a8566-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="a8566-118">**Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes.</span><span class="sxs-lookup"><span data-stu-id="a8566-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="a8566-119">Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden.</span><span class="sxs-lookup"><span data-stu-id="a8566-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="a8566-120">Yderligere oplysninger om dette modul finder du i [Modulet Butiksvælger](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="a8566-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="a8566-121">Indstillinger for indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-121">Cart module settings</span></span>

<span data-ttu-id="a8566-122">Indkøbsvognmoduler har følgende indstillinger, der kan konfigureres på **Indstillinger for websted \> Udvidelser**:</span><span class="sxs-lookup"><span data-stu-id="a8566-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="a8566-123">**Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="a8566-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="a8566-124">En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.</span><span class="sxs-lookup"><span data-stu-id="a8566-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="a8566-125">**Lagerkontrol** – når værdien er angivet til **Sand**, føjes der først en vare til indkøbsvognen, når købefeltmodulet har sikret, at varen er på lager.</span><span class="sxs-lookup"><span data-stu-id="a8566-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="a8566-126">Denne lagerkontrol udføres for de scenarier, hvor varen skal afsendes, og for scenarier, hvor den afhentes i butikken.</span><span class="sxs-lookup"><span data-stu-id="a8566-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="a8566-127">Hvis værdien er angivet til **Falsk**, udføres der ingen lagerkontrol, før der føjes en vare til indkøbsvognen, og ordren afgives.</span><span class="sxs-lookup"><span data-stu-id="a8566-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="a8566-128">**Lagerbuffer** – Denne egenskab bruges til at angive et buffernummer til lageret.</span><span class="sxs-lookup"><span data-stu-id="a8566-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="a8566-129">Lageret vedligeholdes i realtid, og når mange kunder afgiver ordrer, kan det være vanskeligt at bevare en nøjagtig lageroptælling.</span><span class="sxs-lookup"><span data-stu-id="a8566-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="a8566-130">Når der foretages en lagerkontrol, og lageret er mindre end bufferantallet, behandles produktet, som om det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="a8566-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="a8566-131">Når salg sker hurtigt via flere kanaler, og lageroptællingen ikke er synkroniseret, er der derfor mindre risiko for, at der sælges en vare, som ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="a8566-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="a8566-132">**Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**.</span><span class="sxs-lookup"><span data-stu-id="a8566-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="a8566-133">Ruten kan konfigureres på webstedsniveau, så detailhandlere kan føre kunden tilbage til startsiden eller en anden side på webstedet.</span><span class="sxs-lookup"><span data-stu-id="a8566-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="a8566-134">Enhedsinteraktion i Commerce Scale</span><span class="sxs-lookup"><span data-stu-id="a8566-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="a8566-135">Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er.</span><span class="sxs-lookup"><span data-stu-id="a8566-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="a8566-136">Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a8566-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="a8566-137">Føje et indkøbsvognmodul til en side</span><span class="sxs-lookup"><span data-stu-id="a8566-137">Add a cart module to a page</span></span>

<span data-ttu-id="a8566-138">Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a8566-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a8566-139">Opret et fragment med navnet **Indkøbsvognfragment**, og føj et indkøbsvognmodul til det nye fragment.</span><span class="sxs-lookup"><span data-stu-id="a8566-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="a8566-140">Føj en overskrift til indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="a8566-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="a8566-141">Føj et butiksvælgermodul til indkøbsvognmodulet.</span><span class="sxs-lookup"><span data-stu-id="a8566-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="a8566-142">Gem fragmentet, afslut redigeringen, og publicer fragmentet.</span><span class="sxs-lookup"><span data-stu-id="a8566-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="a8566-143">Opret en skabelon med navnet **Indkøbsvognskabelon**, og tilføj det indkøbsvognfragment, som du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="a8566-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="a8566-144">Gem skabelonen, afslut redigeringen, og publicer skabelonen.</span><span class="sxs-lookup"><span data-stu-id="a8566-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="a8566-145">Opret en side, der bruger den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="a8566-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="a8566-146">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="a8566-146">Save and preview the page.</span></span>
1. <span data-ttu-id="a8566-147">Afslut redigeringen af siden, og publicer derefter siden.</span><span class="sxs-lookup"><span data-stu-id="a8566-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8566-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a8566-148">Additional resources</span></span>

[<span data-ttu-id="a8566-149">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="a8566-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a8566-150">Container-modul</span><span class="sxs-lookup"><span data-stu-id="a8566-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a8566-151">Modulet Butiksvælger</span><span class="sxs-lookup"><span data-stu-id="a8566-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="a8566-152">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="a8566-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a8566-153">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a8566-154">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a8566-155">Overskriftsmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a8566-156">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="a8566-156">Footer module</span></span>](author-footer-module.md)
