---
title: Anvendelse af lagerindstillinger
description: Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2c44eb5ece74de15e22180abc6d9d0448ab401b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798883"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="bea1c-103">Anvend lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="bea1c-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bea1c-104">Dette emne dækker lagerindstillinger og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bea1c-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bea1c-105">Lagerindstillinger angiver, om lageret skal kontrolleres, før produkterne føjes til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="bea1c-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="bea1c-106">De definerer også lagerrelaterede marketingsmeddelelser, f.eks. "på lager" og "kun et par tilbage".</span><span class="sxs-lookup"><span data-stu-id="bea1c-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="bea1c-107">Disse indstillinger sikrer, at et produkt ikke kan købes, hvis det ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="bea1c-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="bea1c-108">Dynamics 365 Commerce giver skøn over den disponible tilgængelighed for produkter.</span><span class="sxs-lookup"><span data-stu-id="bea1c-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="bea1c-109">Du kan finde oplysninger om, hvordan det forkalkulerede disponible antal beregnes, i afsnittet [Beregne lagertilgængelighed for detailkanaler](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="bea1c-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="bea1c-110">I Commerce Site Builder kan der defineres lagergrænseværdier og -intervaller for et produkt eller en kategori.</span><span class="sxs-lookup"><span data-stu-id="bea1c-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="bea1c-111">De bestemmer, om lagerbeholdningen kan klassificeres som på lager, lav lagerbeholdning eller udsolgt.</span><span class="sxs-lookup"><span data-stu-id="bea1c-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="bea1c-112">Yderligere oplysninger finder du under [Konfigurere lagerbuffere og lagerniveauer](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="bea1c-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="bea1c-113">Understøttelse af lagergrænseværdier og -områder er tilgængelige i Dynamics 365 Commerce version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="bea1c-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="bea1c-114">Lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="bea1c-114">Inventory settings</span></span>

<span data-ttu-id="bea1c-115">I Commerce er lagerindstillingerne defineret i **Indstillinger for websted \> Udvidelser \> Lagerstyring** i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="bea1c-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="bea1c-116">Der er fire lagerindstillinger, hvoraf en er forældet (frarådes):</span><span class="sxs-lookup"><span data-stu-id="bea1c-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="bea1c-117">**Aktivér kontrol af lagerbeholdning i app** – Denne indstilling slår kontrol af et produktlager til.</span><span class="sxs-lookup"><span data-stu-id="bea1c-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="bea1c-118">Modulerne købefelt, indkøbsvogn og afhentning i butik kontrollerer derefter produktlageret og tillader kun, at der føjes et produkt til indkøbsvognen, hvis lageret er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="bea1c-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="bea1c-119">**Lagerniveau baseret på** – Denne indstilling definerer, hvordan lagerniveauer beregnes.</span><span class="sxs-lookup"><span data-stu-id="bea1c-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="bea1c-120">De tilgængelige værdier er **I alt disponibelt**, **Fysisk disponibelt** og **Grænse for udsolgt**.</span><span class="sxs-lookup"><span data-stu-id="bea1c-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="bea1c-121">I Commerce kan der defineres lagergrænseværdier og -intervaller for de enkelte produkter eller kategorier.</span><span class="sxs-lookup"><span data-stu-id="bea1c-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="bea1c-122">Lager-API'erne returnerer produktlageroplysninger for både egenskaben **I alt disponibelt** og egenskaben **Fysisk disponibelt**.</span><span class="sxs-lookup"><span data-stu-id="bea1c-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="bea1c-123">Forhandleren bestemmer, om værdien for **I alt disponibelt** eller **Fysisk disponibelt** skal bruges til at bestemme lageroptællingen og de tilsvarende intervaller for statusserne på lager og udsolgt.</span><span class="sxs-lookup"><span data-stu-id="bea1c-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="bea1c-124">Værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på** er en gammel (ældre), forældet værdi.</span><span class="sxs-lookup"><span data-stu-id="bea1c-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="bea1c-125">Når den er valgt, bestemmes lageroptællingen ud fra resultaterne af værdien **Disponibelt i alt**, men grænsen defineres af den numeriske indstilling **Grænse for udsolgt**, der beskrives senere.</span><span class="sxs-lookup"><span data-stu-id="bea1c-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="bea1c-126">Tærskelindstillingen gælder for alle produkter på tværs af et e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="bea1c-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="bea1c-127">Hvis lagerbeholdningen ligger under tærskelantallet, anses et produkt for at være udsolgt.</span><span class="sxs-lookup"><span data-stu-id="bea1c-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="bea1c-128">Ellers betragtes det som værende på lager.</span><span class="sxs-lookup"><span data-stu-id="bea1c-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="bea1c-129">Mulighederne for værdien **Grænse for udsolgt** er begrænsede, og det anbefales ikke, at du bruger værdien i version 10.0.12 og senere.</span><span class="sxs-lookup"><span data-stu-id="bea1c-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="bea1c-130">**Lagerintervaller** – Denne indstilling definerer de lagerintervaller, som der vises meddelelser for i webstedsmoduler.</span><span class="sxs-lookup"><span data-stu-id="bea1c-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="bea1c-131">Den kan kun anvendes, hvis enten værdien **I alt disponibelt** eller værdien **Fysisk disponibelt** er valgt for indstillingen **Lagerniveau baseret på**.</span><span class="sxs-lookup"><span data-stu-id="bea1c-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="bea1c-132">De tilgængelige værdier er **Alle**, **Lav lagerbeholdning og udsolgt** og **Udsolgt**.</span><span class="sxs-lookup"><span data-stu-id="bea1c-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="bea1c-133">Når du vælger **Alle**, vises meddelelser for alle lagerintervaller, fra på lager (meddelelsen "Tilgængelig") til udsolgt (meddelelsen "Udsolgt").</span><span class="sxs-lookup"><span data-stu-id="bea1c-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="bea1c-134">Når du vælger **Lav lagerbeholdning og udsolgt**, vises meddelelser for alle lagerintervaller med undtagelse af på lager (meddelelsen "Tilgængelig").</span><span class="sxs-lookup"><span data-stu-id="bea1c-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="bea1c-135">Når du vælger **Udsolgt**, vises kun meddelelsen "Udsolgt".</span><span class="sxs-lookup"><span data-stu-id="bea1c-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="bea1c-136">**Grænse for udsolgt** – Denne gamle numeriske indstilling træder kun i kraft, hvis du vælger værdien **Grænse for udsolgt** for indstillingen **Lagerniveau baseret på**.</span><span class="sxs-lookup"><span data-stu-id="bea1c-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="bea1c-137">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="bea1c-137">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="bea1c-138">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="bea1c-138">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="bea1c-139">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="bea1c-139">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="bea1c-140">Moduler, der bruger lagerindstillinger</span><span class="sxs-lookup"><span data-stu-id="bea1c-140">Modules that use inventory settings</span></span>

<span data-ttu-id="bea1c-141">Modulerne købefelt, ønskeliste, butiksvælger, indkøbsvogn og indkøbsvognikon bruger lagerindstillinger til at vise lagerintervaller og -meddelelser.</span><span class="sxs-lookup"><span data-stu-id="bea1c-141">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="bea1c-142">Følgende billede viser et eksempel på en side med produktdetaljer (PDP), der viser en på lager-meddelelse ("Tilgængelig").</span><span class="sxs-lookup"><span data-stu-id="bea1c-142">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Eksempel på et PDP-modul, der har en på lager-meddelelse](./media/pdp-InStock.png)

<span data-ttu-id="bea1c-144">Følgende billede viser et eksempel på en side med produktdetaljer (PDP), der viser en udsolgt-meddelelse ("Udsolgt").</span><span class="sxs-lookup"><span data-stu-id="bea1c-144">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Eksempel på et PDP-modul, der har en udsolgt-meddelelse](./media/pdp-outofstock.png)

<span data-ttu-id="bea1c-146&quot;>Følgende billede viser et eksempel på en indkøbsvogn, der viser en på lager-meddelelse (&quot;Tilgængelig").</span><span class="sxs-lookup"><span data-stu-id="bea1c-146">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Eksempel på en indkøbsvognmodul, der har en på lager-meddelelse](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="bea1c-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bea1c-148">Additional resources</span></span>

[<span data-ttu-id="bea1c-149">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="bea1c-149">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bea1c-150">Konfigurere lagerbuffere og lagerniveauer</span><span class="sxs-lookup"><span data-stu-id="bea1c-150">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="bea1c-151">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="bea1c-151">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bea1c-152">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="bea1c-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bea1c-153">Kontostyringssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="bea1c-153">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="bea1c-154">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="bea1c-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="bea1c-155">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="bea1c-155">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
