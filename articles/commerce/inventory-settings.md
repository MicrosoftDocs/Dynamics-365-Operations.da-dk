---
title: Anvendelse af lagerindstillinger
description: Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7d25fd62efca52dd2d60ed3435104c3507a1d19
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817603"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="b5b0a-103">Anvendelse af lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="b5b0a-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5b0a-104">Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5b0a-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="b5b0a-105">Overview</span></span>

<span data-ttu-id="b5b0a-106">Lagerindstillinger angiver, om lageret skal kontrolleres, før produkterne føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="b5b0a-107">De definerer også lagerrelaterede marketingsmeddelelser, f.eks. "på lager" og "kun et par tilbage".</span><span class="sxs-lookup"><span data-stu-id="b5b0a-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="b5b0a-108">Disse indstillinger sikrer, at et produkt ikke kan købes, hvis det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="b5b0a-109">Dynamics 365 Commerce giver skøn over den disponible tilgængelighed for produkter.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="b5b0a-110">Du kan finde oplysninger om, hvordan det forkalkulerede disponible antal beregnes, i afsnittet [Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="b5b0a-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="b5b0a-111">I Commerce Site Builder kan der defineres lagergrænseværdier og -intervaller for et produkt eller en kategori.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="b5b0a-112">De bestemmer, om lagerbeholdningen kan klassificeres som på lager, lav lagerbeholdning eller udsolgt.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="b5b0a-113">Yderligere oplysninger finder du under [Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b5b0a-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b5b0a-114">Understøttelse af lagergrænseværdier og -områder er tilgængelige i Dynamics 365 Commerce version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="b5b0a-115">Lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="b5b0a-115">Inventory settings</span></span>

<span data-ttu-id="b5b0a-116">I Commerce er lagerindstillingerne defineret i **Indstillinger for websted \> Udvidelser \> Lagerstyring** i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="b5b0a-117">Der er fire lagerindstillinger, hvoraf en er forældet (frarådes):</span><span class="sxs-lookup"><span data-stu-id="b5b0a-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="b5b0a-118">**Aktivér lagerkontrol på app** – Denne indstilling slår kontrol af et produktlager til.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-118">**Enable inventory check on app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="b5b0a-119">Modulerne købefelt, indkøbsvogn og afhentning i butik kontrollerer derefter produktlageret og tillader kun, at der føjes et produkt til indkøbsvognen, hvis lageret er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="b5b0a-120">**Lagerniveau baseret på** – Denne indstilling definerer, hvordan lagerniveauer beregnes.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="b5b0a-121">De tilgængelige værdier er **I alt disponibelt**, **Fysisk disponibelt** og **Grænse for udsolgt**.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="b5b0a-122">I Commerce kan der defineres lagergrænseværdier og -intervaller for de enkelte produkter eller kategorier.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="b5b0a-123">Lager-API'erne returnerer produktlageroplysninger for både egenskaben **I alt disponibelt** og egenskaben **Fysisk disponibelt**.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="b5b0a-124">Forhandleren bestemmer, om værdien for **I alt disponibelt** eller **Fysisk disponibelt** skal bruges til at bestemme lageroptællingen og de tilsvarende intervaller for statusserne på lager og udsolgt.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="b5b0a-125">Værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på** er en gammel (ældre), forældet værdi.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="b5b0a-126">Når den er valgt, bestemmes lageroptællingen ud fra resultaterne af værdien **Disponibelt i alt**, men grænsen defineres af den numeriske indstilling **Grænse for udsolgt**, der beskrives senere.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="b5b0a-127">Tærskelindstillingen gælder for alle produkter på tværs af et e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-127">This threshold setting applies to all products across an e-Commerce site.</span></span> <span data-ttu-id="b5b0a-128">Hvis lagerbeholdningen ligger under tærskelantallet, anses et produkt for at være udsolgt.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="b5b0a-129">Ellers betragtes det som værende på lager.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="b5b0a-130">Mulighederne for værdien **Grænse for udsolgt** er begrænsede, og det anbefales ikke, at du bruger værdien i version 10.0.12 og senere.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="b5b0a-131">**Lagerintervaller** – Denne indstilling definerer de lagerintervaller, som der vises meddelelser for i webstedsmoduler.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="b5b0a-132">Den kan kun anvendes, hvis enten værdien **I alt disponibelt** eller værdien **Fysisk disponibelt** er valgt for indstillingen **Lagerniveau baseret på**.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="b5b0a-133">De tilgængelige værdier er **Alle**, **Lav lagerbeholdning og udsolgt** og **Udsolgt**.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="b5b0a-134">Når du vælger **Alle**, vises meddelelser for alle lagerintervaller, fra på lager (meddelelsen "Tilgængelig") til udsolgt (meddelelsen "Udsolgt").</span><span class="sxs-lookup"><span data-stu-id="b5b0a-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="b5b0a-135">Når du vælger **Lav lagerbeholdning og udsolgt**, vises meddelelser for alle lagerintervaller med undtagelse af på lager (meddelelsen "Tilgængelig").</span><span class="sxs-lookup"><span data-stu-id="b5b0a-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="b5b0a-136">Når du vælger **Udsolgt**, vises kun meddelelsen "Udsolgt".</span><span class="sxs-lookup"><span data-stu-id="b5b0a-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="b5b0a-137">**Grænse for udsolgt** – Denne gamle numeriske indstilling træder kun i kraft, hvis du vælger værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på**.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="b5b0a-138">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="b5b0a-139">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b5b0a-140">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="b5b0a-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="b5b0a-141">Moduler, der bruger lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="b5b0a-141">Modules that use inventory settings</span></span>

<span data-ttu-id="b5b0a-142">Modulerne købefelt, ønskeliste, butiksvælger, indkøbsvogn og indkøbsvognikon bruger lagerindstillinger til at vise lagerintervaller og -meddelelser.</span><span class="sxs-lookup"><span data-stu-id="b5b0a-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="b5b0a-143">Følgende billede viser et eksempel på en side med produktdetaljer (PDP), der viser en på lager-meddelelse ("Tilgængelig").</span><span class="sxs-lookup"><span data-stu-id="b5b0a-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Eksempel på et PDP-modul, der har en på lager-meddelelse](./media/pdp-InStock.png)

<span data-ttu-id="b5b0a-145">Følgende billede viser et eksempel på en side med produktdetaljer (PDP), der viser en udsolgt-meddelelse ("Udsolgt").</span><span class="sxs-lookup"><span data-stu-id="b5b0a-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Eksempel på et PDP-modul, der har en udsolgt-meddelelse](./media/pdp-outofstock.png)

<span data-ttu-id="b5b0a-147">Følgende billede viser et eksempel på en indkøbsvogn, der viser en på lager-meddelelse ("Tilgængelig").</span><span class="sxs-lookup"><span data-stu-id="b5b0a-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Eksempel på en indkøbsvognmodul, der har en på lager-meddelelse](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="b5b0a-149">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b5b0a-149">Additional resources</span></span>

[<span data-ttu-id="b5b0a-150">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="b5b0a-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b5b0a-151">Konfigurere lagerbuffere og lagerniveauer</span><span class="sxs-lookup"><span data-stu-id="b5b0a-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="b5b0a-152">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="b5b0a-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b5b0a-153">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="b5b0a-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b5b0a-154">Kontostyringssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="b5b0a-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="b5b0a-155">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="b5b0a-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b5b0a-156">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="b5b0a-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
