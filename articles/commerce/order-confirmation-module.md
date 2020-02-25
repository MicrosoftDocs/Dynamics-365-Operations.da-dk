---
title: Modulet Ordredetaljer
description: Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026011"
---
# <a name="order-details-module"></a><span data-ttu-id="b645f-103">Modulet Ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="b645f-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b645f-104">Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b645f-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b645f-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b645f-105">Overview</span></span>

<span data-ttu-id="b645f-106">Modulet Ordredetaljer bruges til at vise ordrebekræftelsesoplysningerne, når en ordre er afgivet.</span><span class="sxs-lookup"><span data-stu-id="b645f-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="b645f-107">Det viser ordrebekræftelses-id, ordrekontaktoplysninger og andre ordreoplysninger, f.eks. de varer, der er købt, betalingsoplysninger og forsendelsesmåde.</span><span class="sxs-lookup"><span data-stu-id="b645f-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="b645f-108">Egenskaber for ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="b645f-108">Order confirmation module properties</span></span>

| <span data-ttu-id="b645f-109">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="b645f-109">Property name</span></span>  | <span data-ttu-id="b645f-110">Værdier</span><span class="sxs-lookup"><span data-stu-id="b645f-110">Values</span></span> | <span data-ttu-id="b645f-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b645f-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b645f-112">Overskrift</span><span class="sxs-lookup"><span data-stu-id="b645f-112">Heading</span></span>        | <span data-ttu-id="b645f-113">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="b645f-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b645f-114">Ordrebekræftelsesmodulet kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="b645f-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="b645f-115">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="b645f-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="b645f-116">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="b645f-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="b645f-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="b645f-117">Contact number</span></span> | <span data-ttu-id="b645f-118">Text</span><span class="sxs-lookup"><span data-stu-id="b645f-118">Text</span></span> | <span data-ttu-id="b645f-119">Der kan angives et kontaktnummer for ordrerelaterede spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="b645f-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="b645f-120">Moduler, der kan bruges på en side med ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="b645f-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="b645f-121">Når du opretter en side med ordredetaljer, kan du tilføje andre relevante moduler udover modulet Ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="b645f-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="b645f-122">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="b645f-122">Here are some examples:</span></span>

- <span data-ttu-id="b645f-123">**Anbefalingsmodul** – Anbefalingsmodulet kan tilføjes på ordredetaljesiden for at foreslå andre produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="b645f-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="b645f-124">**Marketingmoduler** – Ethvert marketingmodul kan føjes til siden Ordredetaljer for at vise marketingindhold.</span><span class="sxs-lookup"><span data-stu-id="b645f-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="b645f-125">Oprette et sidemodul med ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="b645f-125">Create an order details page module</span></span>

1. <span data-ttu-id="b645f-126">Opret en sideskabelon med navnet **Ordredetaljeskabelon**.</span><span class="sxs-lookup"><span data-stu-id="b645f-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="b645f-127">Tilføj et ordredetaljemodul på **Hoved**-pladsen på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="b645f-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="b645f-128">Tilføj et anbefalingsmodul i ordredetaljemodulet.</span><span class="sxs-lookup"><span data-stu-id="b645f-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="b645f-129">Gem skabelonen, og se forhåndsvisningen af den.</span><span class="sxs-lookup"><span data-stu-id="b645f-129">Save and preview the template.</span></span> <span data-ttu-id="b645f-130">Ordredetaljemodulet skal ikke gengives, fordi det kræver ordrebekræftelsesnummerets kontekst.</span><span class="sxs-lookup"><span data-stu-id="b645f-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="b645f-131">Afslut redigeringen af skabelonen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="b645f-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="b645f-132">Brug den ordredetaljeskabelon, som du netop har oprettet, til at oprette en side med navnet **ordredetaljeside**.</span><span class="sxs-lookup"><span data-stu-id="b645f-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="b645f-133">Føj standardsiden til sidedispositionen.</span><span class="sxs-lookup"><span data-stu-id="b645f-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="b645f-134">Tilføj et sidehovedfragment på pladsen **Sidehoved**.</span><span class="sxs-lookup"><span data-stu-id="b645f-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="b645f-135">Tilføj et sidefodsfragment på pladsen **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="b645f-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="b645f-136">Tilføj et ordredetaljemodul på **Hoved**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="b645f-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="b645f-137">Tilføj overskriften **Ordredetaljer** i egenskabsruden i ordredetaljemodulet.</span><span class="sxs-lookup"><span data-stu-id="b645f-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="b645f-138">Tilføj et anbefalingsmodul under ordredetaljemodulet, og konfigurer det, så det bruger indstillingerne **Ny** og **Bedst sælgende**.</span><span class="sxs-lookup"><span data-stu-id="b645f-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="b645f-139">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="b645f-139">Save and preview the page.</span></span>
1. <span data-ttu-id="b645f-140">Afslut redigeringen af siden, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="b645f-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b645f-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b645f-141">Additional resources</span></span>

[<span data-ttu-id="b645f-142">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="b645f-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b645f-143">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="b645f-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b645f-144">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="b645f-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b645f-145">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="b645f-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b645f-146">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="b645f-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b645f-147">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="b645f-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b645f-148">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="b645f-148">Footer module</span></span>](author-footer-module.md)
