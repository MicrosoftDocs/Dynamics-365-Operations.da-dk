---
title: Ordrebekræftelsesmodul
description: Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698320"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="2fb75-103">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2fb75-104">Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2fb75-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2fb75-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="2fb75-105">Overview</span></span>

<span data-ttu-id="2fb75-106">Et ordrebekræftelsesmodul bruges til at vise en bekræftelsesmeddelelse på en ordrebekræftelsesside, når en ordre er afgivet.</span><span class="sxs-lookup"><span data-stu-id="2fb75-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="2fb75-107">Ordrebekræftelsesmodulet viser ordrebekræftelsesnummeret og den kundemailadresse, der blev oplyst under betalingen.</span><span class="sxs-lookup"><span data-stu-id="2fb75-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="2fb75-108">Når en ordre afgives under betalingen, overføres ordrebekræftelsesnummeret og kundens mailadresse til ordrebekræftelsessiden som en forespørgselsstreng i sidens URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2fb75-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="2fb75-109">Ordrebekræftelsesmodulet modtager disse oplysninger og gengiver ordrestatus på ordrebekræftelsessiden.</span><span class="sxs-lookup"><span data-stu-id="2fb75-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="2fb75-110">Ordrebekræftelsesmodulet kræver, at denne sidekontekst angiver ordrens status.</span><span class="sxs-lookup"><span data-stu-id="2fb75-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="2fb75-111">Egenskaber for ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-111">Order confirmation module properties</span></span>

| <span data-ttu-id="2fb75-112">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="2fb75-112">Property name</span></span> | <span data-ttu-id="2fb75-113">Værdier</span><span class="sxs-lookup"><span data-stu-id="2fb75-113">Values</span></span> | <span data-ttu-id="2fb75-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2fb75-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="2fb75-115">Overskrift</span><span class="sxs-lookup"><span data-stu-id="2fb75-115">Heading</span></span>       | <span data-ttu-id="2fb75-116">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="2fb75-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="2fb75-117">Ordrebekræftelsesmodulet kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="2fb75-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="2fb75-118">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="2fb75-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="2fb75-119">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="2fb75-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="2fb75-120">Moduler, der kan bruges i et ordrebekræftelsessidemodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="2fb75-121">**Anbefalinger** – Anbefalingsmodulet kan placeres på ordrebekræftelsessiden for at foreslå andre produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="2fb75-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="2fb75-122">**Marketing** – Marketingmodulet kan føje marketingindhold til ordrebekræftelsessiden.</span><span class="sxs-lookup"><span data-stu-id="2fb75-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="2fb75-123">Oprette et ordrebekræftelsessidemodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="2fb75-124">Opret en sideskabelon med navnet **ordrebekræftelsesskabelon**.</span><span class="sxs-lookup"><span data-stu-id="2fb75-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="2fb75-125">Tilføj et ordrebekræftelsesmodul på **Hoved**-pladsen på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="2fb75-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="2fb75-126">Tilføj et anbefalingsmodul i ordrebekræftelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="2fb75-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="2fb75-127">Gem skabelonen, og se forhåndsvisningen af den.</span><span class="sxs-lookup"><span data-stu-id="2fb75-127">Save and preview the template.</span></span> <span data-ttu-id="2fb75-128">Ordrebekræftelsesmodulet skal ikke gengives, fordi det kræver ordrebekræftelsesnummerets kontekst.</span><span class="sxs-lookup"><span data-stu-id="2fb75-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="2fb75-129">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="2fb75-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="2fb75-130">Brug den ordrebekræftelsesskabelon, som du netop har oprettet, til at oprette en side med navnet **ordrebekræftelsesside**.</span><span class="sxs-lookup"><span data-stu-id="2fb75-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="2fb75-131">Føj standardsiden til sidedispositionen.</span><span class="sxs-lookup"><span data-stu-id="2fb75-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="2fb75-132">Tilføj et sidehovedfragment på pladsen **Sidehoved**.</span><span class="sxs-lookup"><span data-stu-id="2fb75-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="2fb75-133">Tilføj et sidefodsfragment på pladsen **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="2fb75-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="2fb75-134">Tilføj et ordrebekræftelsesmodul på **Hoved**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="2fb75-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="2fb75-135">Tilføj overskriften **Ordrebekræftelse** i egenskabsruden i ordrebekræftelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="2fb75-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="2fb75-136">Tilføj et anbefalingsmodul under ordrebekræftelsesmodulet, og konfigurer det, så det bruger indstillingerne **Ny** og **Bedst sælgende**.</span><span class="sxs-lookup"><span data-stu-id="2fb75-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="2fb75-137">Gem siden, og se en forhåndsvisning af den, check den ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="2fb75-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2fb75-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2fb75-138">Additional resources</span></span>

[<span data-ttu-id="2fb75-139">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="2fb75-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2fb75-140">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="2fb75-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2fb75-141">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2fb75-142">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2fb75-143">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2fb75-144">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2fb75-145">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="2fb75-145">Footer module</span></span>](author-footer-module.md)
