---
title: Oversigt over modulbibliotek
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc52dd8e14bb2e9f2f9c026ee0e058aee4cedcb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411152"
---
# <a name="module-library-overview"></a><span data-ttu-id="b47ab-103">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="b47ab-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b47ab-104">Dette emne indeholder en oversigt over modulbiblioteket til Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b47ab-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

## <a name="overview"></a><span data-ttu-id="b47ab-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="b47ab-105">Overview</span></span>

<span data-ttu-id="b47ab-106">Dynamics 365 Commerce-modulbiblioteket er en samling af moduler, der kan bruges til at bygge et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="b47ab-106">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="b47ab-107">Moduler har både aspekter af brugergrænseflade og funktionsmåder.</span><span class="sxs-lookup"><span data-stu-id="b47ab-107">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="b47ab-108">Du kan anvende temaer på modulerne i modulbiblioteket for at ændre deres udseende og funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="b47ab-108">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="b47ab-109">Temaerne bruger overlappende typografiark (CSS).</span><span class="sxs-lookup"><span data-stu-id="b47ab-109">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="b47ab-110">Der findes et tema for et fiktivt e-handels-websted med navnet "Fabrikam" som en del af modulbiblioteket, der kan bruges som reference.</span><span class="sxs-lookup"><span data-stu-id="b47ab-110">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="b47ab-111">Modulbibliotekets moduler</span><span class="sxs-lookup"><span data-stu-id="b47ab-111">Module library modules</span></span>

<span data-ttu-id="b47ab-112">Følgende typer moduler findes i modulbiblioteket:</span><span class="sxs-lookup"><span data-stu-id="b47ab-112">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="b47ab-113">**Containermodul** – Et containermodul er et simpelt modul, der fungerer som vært for andre moduler.</span><span class="sxs-lookup"><span data-stu-id="b47ab-113">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="b47ab-114">Det styrer layoutet for de moduler, der ligger i det.</span><span class="sxs-lookup"><span data-stu-id="b47ab-114">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="b47ab-115">**Marketingmoduler** – Marketingmoduler omfatter indholdsblok, tekstblok, videoafspiller og karruselmoduler.</span><span class="sxs-lookup"><span data-stu-id="b47ab-115">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="b47ab-116">Alle disse moduler kan bruges til at vise indhold.</span><span class="sxs-lookup"><span data-stu-id="b47ab-116">All these modules can be used to showcase content.</span></span> <span data-ttu-id="b47ab-117">De kan placeres på en hvilken som helst side og styres af data fra CMS-indholdsstyringssystemet (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="b47ab-117">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="b47ab-118">**Sidehoved- og sidefodsmoduler** – Sidehoved- og sidefodsmoduler vises i sidehovedet og sidefoden på alle webstedssider.</span><span class="sxs-lookup"><span data-stu-id="b47ab-118">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="b47ab-119">Disse moduler kan konfigureres efter behov ved hjælp af egenskaber.</span><span class="sxs-lookup"><span data-stu-id="b47ab-119">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="b47ab-120">**Søgemoduler** – Produkter kan opdages ved hjælp af søgemodulet i sidehovedet.</span><span class="sxs-lookup"><span data-stu-id="b47ab-120">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="b47ab-121">Søgeresultaterne vises på siden med søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="b47ab-121">Search results appear on the search results page.</span></span> <span data-ttu-id="b47ab-122">Der kan også registreres produkter på kategorisider, som er dedikerede sider til hver kategori, der understøttes i kanalens navigationshierarki.</span><span class="sxs-lookup"><span data-stu-id="b47ab-122">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="b47ab-123">Desuden kan afgrænsningsmoduler bruges til at filtrere resultater yderligere i søgeresultater og på kategorisider.</span><span class="sxs-lookup"><span data-stu-id="b47ab-123">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="b47ab-124">**Sidemoduler for produktdetaljer** – Sider med produktdetaljer bruger flere moduler til at vise produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b47ab-124">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="b47ab-125">I købefeltmodulet kan kunder få vist produkter og føje dem til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="b47ab-125">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="b47ab-126">Andre moduler som f.eks. modulet til tekniske specifikationer viser produktoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="b47ab-126">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="b47ab-127">Modulet til vurderinger og anmeldelser kan bruges til at se og angive vurderinger.</span><span class="sxs-lookup"><span data-stu-id="b47ab-127">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="b47ab-128">**Køb online, afhent i butikken-modulet** – Køb online, afhent i butikken-modulet er integreret med Bing Kort.</span><span class="sxs-lookup"><span data-stu-id="b47ab-128">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="b47ab-129">Det kan bruges til at finde butikker i nærheden, hvor kunder kan afhente produkter, som de har købt.</span><span class="sxs-lookup"><span data-stu-id="b47ab-129">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="b47ab-130">**Købsmoduler** – Købsmoduler indeholder indkøbsvognsmodulet, som kan bruges til at lægge varer i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="b47ab-130">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="b47ab-131">Betalingsmodulet registrerer leveringsadressen, leveringsindstillinger og gavekort, fordelskundeprogram og kreditkortoplysninger, så en ordre kan behandles.</span><span class="sxs-lookup"><span data-stu-id="b47ab-131">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="b47ab-132">Når en ordre er afgivet, kan ordrebekræftelsesmodulet bruges til at vise bekræftelsesoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="b47ab-132">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="b47ab-133">**Kontostyringsmoduler** – I logonmodulet kan kunder logge på en eksisterende konto, og tilmeldingsmodulet giver dem mulighed for at oprette en ny konto.</span><span class="sxs-lookup"><span data-stu-id="b47ab-133">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="b47ab-134">Når en konto er oprettet, kan modulet for ordrehistorik bruges til at få vist de seneste ordrer, og modulet med ordredetaljer kan bruges til at få vist ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="b47ab-134">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="b47ab-135">**Anbefalinger-modul** – Anbefalinger vises ved hjælp af modulet til produktplacering.</span><span class="sxs-lookup"><span data-stu-id="b47ab-135">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="b47ab-136">Dette modul understøtter algoritmer og redaktionelle lister, der kan vises på alle sider.</span><span class="sxs-lookup"><span data-stu-id="b47ab-136">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b47ab-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b47ab-137">Additional resources</span></span>

[<span data-ttu-id="b47ab-138">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="b47ab-138">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b47ab-139">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="b47ab-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b47ab-140">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="b47ab-140">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b47ab-141">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="b47ab-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b47ab-142">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="b47ab-142">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b47ab-143">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="b47ab-143">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b47ab-144">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="b47ab-144">Footer module</span></span>](author-footer-module.md)
