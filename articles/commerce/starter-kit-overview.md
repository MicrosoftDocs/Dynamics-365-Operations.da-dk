---
title: Modulbibliotek, oversigt
description: Dette emne indeholder en oversigt over modulbiblioteket til Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcb0c2317315308de51d8247d23a930f10c3de6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234287"
---
# <a name="module-library-overview"></a><span data-ttu-id="9767c-103">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="9767c-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9767c-104">Dette emne indeholder en oversigt over modulbiblioteket til Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9767c-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="9767c-105">Dynamics 365 Commerce-modulbiblioteket er en samling af moduler, der kan bruges til at bygge et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="9767c-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="9767c-106">Moduler har både aspekter af brugergrænseflade og funktionsmåder.</span><span class="sxs-lookup"><span data-stu-id="9767c-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="9767c-107">Du kan anvende temaer på modulerne i modulbiblioteket for at ændre deres udseende og funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="9767c-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="9767c-108">Temaerne bruger overlappende typografiark (CSS).</span><span class="sxs-lookup"><span data-stu-id="9767c-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="9767c-109">Der findes et tema for et fiktivt e-handels-websted med navnet "Fabrikam" som en del af modulbiblioteket, der kan bruges som reference.</span><span class="sxs-lookup"><span data-stu-id="9767c-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="9767c-110">Modulbibliotekets moduler</span><span class="sxs-lookup"><span data-stu-id="9767c-110">Module library modules</span></span>

<span data-ttu-id="9767c-111">Følgende typer moduler findes i modulbiblioteket:</span><span class="sxs-lookup"><span data-stu-id="9767c-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="9767c-112">**Containermodul** – Et containermodul er et simpelt modul, der fungerer som vært for andre moduler.</span><span class="sxs-lookup"><span data-stu-id="9767c-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="9767c-113">Det styrer layoutet for de moduler, der ligger i det.</span><span class="sxs-lookup"><span data-stu-id="9767c-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="9767c-114">**Marketingmoduler** – Marketingmoduler omfatter indholdsblok, tekstblok, videoafspiller og karruselmoduler.</span><span class="sxs-lookup"><span data-stu-id="9767c-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="9767c-115">Alle disse moduler kan bruges til at vise indhold.</span><span class="sxs-lookup"><span data-stu-id="9767c-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="9767c-116">De kan placeres på en hvilken som helst side og styres af data fra CMS-indholdsstyringssystemet (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="9767c-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="9767c-117">**Sidehoved- og sidefodsmoduler** – Sidehoved- og sidefodsmoduler vises i sidehovedet og sidefoden på alle webstedssider.</span><span class="sxs-lookup"><span data-stu-id="9767c-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="9767c-118">Disse moduler kan konfigureres efter behov ved hjælp af egenskaber.</span><span class="sxs-lookup"><span data-stu-id="9767c-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="9767c-119">**Søgemoduler** – Produkter kan opdages ved hjælp af søgemodulet i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="9767c-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="9767c-120">Søgeresultaterne vises på siden med søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="9767c-120">Search results appear on the search results page.</span></span> <span data-ttu-id="9767c-121">Der kan også registreres produkter på kategorisider, som er dedikerede sider til hver kategori, der understøttes i kanalens navigationshierarki.</span><span class="sxs-lookup"><span data-stu-id="9767c-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="9767c-122">Desuden kan afgrænsningsmoduler bruges til at filtrere resultater yderligere i søgeresultater og på kategorisider.</span><span class="sxs-lookup"><span data-stu-id="9767c-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="9767c-123">**Sidemoduler for produktdetaljer** – Sider med produktdetaljer bruger flere moduler til at vise produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="9767c-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="9767c-124">I købefeltmodulet kan kunder få vist produkter og føje dem til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="9767c-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="9767c-125">Andre moduler som f.eks. modulet til tekniske specifikationer viser produktoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="9767c-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="9767c-126">Modulet til vurderinger og anmeldelser kan bruges til at se og angive vurderinger.</span><span class="sxs-lookup"><span data-stu-id="9767c-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="9767c-127">**Køb online, afhent i butikken-modulet** – Køb online, afhent i butikken-modulet er integreret med Bing Kort.</span><span class="sxs-lookup"><span data-stu-id="9767c-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="9767c-128">Det kan bruges til at finde butikker i nærheden, hvor kunder kan afhente produkter, som de har købt.</span><span class="sxs-lookup"><span data-stu-id="9767c-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="9767c-129">**Købsmoduler** – Købsmoduler indeholder indkøbsvognsmodulet, som kan bruges til at lægge varer i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="9767c-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="9767c-130">Betalingsmodulet registrerer leveringsadressen, leveringsindstillinger og gavekort, fordelskundeprogram og kreditkortoplysninger, så en ordre kan behandles.</span><span class="sxs-lookup"><span data-stu-id="9767c-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="9767c-131">Når en ordre er afgivet, kan ordrebekræftelsesmodulet bruges til at vise bekræftelsesoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="9767c-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="9767c-132">**Kontostyringsmoduler** – I logonmodulet kan kunder logge på en eksisterende konto, og tilmeldingsmodulet giver dem mulighed for at oprette en ny konto.</span><span class="sxs-lookup"><span data-stu-id="9767c-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="9767c-133">Når en konto er oprettet, kan modulet for ordrehistorik bruges til at få vist de seneste ordrer, og modulet med ordredetaljer kan bruges til at få vist ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="9767c-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="9767c-134">**Anbefalinger-modul** – Anbefalinger vises ved hjælp af modulet til produktplacering.</span><span class="sxs-lookup"><span data-stu-id="9767c-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="9767c-135">Dette modul understøtter algoritmer og redaktionelle lister, der kan vises på alle sider.</span><span class="sxs-lookup"><span data-stu-id="9767c-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9767c-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9767c-136">Additional resources</span></span>

[<span data-ttu-id="9767c-137">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="9767c-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9767c-138">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="9767c-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9767c-139">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="9767c-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9767c-140">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="9767c-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="9767c-141">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="9767c-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="9767c-142">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="9767c-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="9767c-143">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="9767c-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]