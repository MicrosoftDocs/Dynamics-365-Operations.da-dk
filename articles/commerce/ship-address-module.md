---
title: Leveringsadressemodul
description: Dette emne omhandler leveringsadressemodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795423"
---
# <a name="shipping-address-module"></a><span data-ttu-id="8391f-103">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="8391f-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8391f-104">Dette emne omhandler leveringsadressemodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8391f-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8391f-105">Leveringsadressemodulet giver kunder mulighed for at tilføje eller vælge leveringsadressen for en ordre i betalingsflowet.</span><span class="sxs-lookup"><span data-stu-id="8391f-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="8391f-106">Hvis en kunde er logget på, vises adresser, der tidligere er blevet gemt for den pågældende kunde, og kunden kan vælge mellem dem.</span><span class="sxs-lookup"><span data-stu-id="8391f-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="8391f-107">Kunden kan også tilføje en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="8391f-107">The customer can also add a new address.</span></span> <span data-ttu-id="8391f-108">Leveringsadressemodulet bruges til alle varer i en ordre, som kræver levering.</span><span class="sxs-lookup"><span data-stu-id="8391f-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="8391f-109">Der kan angives leveringsadresseformater i Commerce Headquarters for hvert land eller område, og leveringsadressemodulet gennemtvinger de lande/områdespecifikke regler.</span><span class="sxs-lookup"><span data-stu-id="8391f-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="8391f-110">Når kunder angiver en leveringsadresse i betalingsflowet, har de mulighed for at gemme adressen som en primær adresse.</span><span class="sxs-lookup"><span data-stu-id="8391f-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="8391f-111">Denne indstilling vises kun, hvis en kunde er logget på.</span><span class="sxs-lookup"><span data-stu-id="8391f-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="8391f-112">Selvom leveringsadressemodulet ikke indeholder adressevalidering, kan denne funktion implementeres gennem tilpasning.</span><span class="sxs-lookup"><span data-stu-id="8391f-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="8391f-113">Følgende illustration viser et eksempel på et nyt leveringsadressemodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="8391f-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Eksempel på et leveringsadressemodul på en betalingsside](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="8391f-115">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="8391f-115">Module properties</span></span>

| <span data-ttu-id="8391f-116">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="8391f-116">Property name</span></span> | <span data-ttu-id="8391f-117">Værdier</span><span class="sxs-lookup"><span data-stu-id="8391f-117">Values</span></span> | <span data-ttu-id="8391f-118">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="8391f-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8391f-119">Overskrift</span><span class="sxs-lookup"><span data-stu-id="8391f-119">Heading</span></span> | <span data-ttu-id="8391f-120">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="8391f-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="8391f-121">En valgfri overskrift til leveringsadressemodulet.</span><span class="sxs-lookup"><span data-stu-id="8391f-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="8391f-122">Vis adressetype</span><span class="sxs-lookup"><span data-stu-id="8391f-122">Show address type</span></span> | <span data-ttu-id="8391f-123">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="8391f-123">**True** or **False**</span></span> | <span data-ttu-id="8391f-124">Hvis denne valgfrie egenskab er angivet til **Sand**, vises en adressetype som f.eks **Privat** eller **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="8391f-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="8391f-125">Hvis der ikke er angivet en adressetype, vil adressen automatisk blive gemt som **Type**=**Anden**.</span><span class="sxs-lookup"><span data-stu-id="8391f-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="8391f-126">Aktivér automatisk forslag</span><span class="sxs-lookup"><span data-stu-id="8391f-126">Enable auto suggestion</span></span>| <span data-ttu-id="8391f-127">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="8391f-127">**True** or **False**</span></span> | <span data-ttu-id="8391f-128">Hvis denne valgfrie egenskab er angivet til **Sand**, vises der automatiske adresseforslag.</span><span class="sxs-lookup"><span data-stu-id="8391f-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="8391f-129">Disse forslag drives af Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="8391f-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="8391f-130">Du kan finde oplysninger om, hvordan du konfigurerer Bing Maps-integration for dit websted, i [modulet Butiksvælger](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="8391f-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="8391f-131">Denne funktion er tilgængelig pr. Commerce version 10.0.15-udgaven.</span><span class="sxs-lookup"><span data-stu-id="8391f-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="8391f-132">Indstillinger til automatiske forslag</span><span class="sxs-lookup"><span data-stu-id="8391f-132">Auto suggest options</span></span>| <span data-ttu-id="8391f-133">Et nummer</span><span class="sxs-lookup"><span data-stu-id="8391f-133">A number</span></span>| <span data-ttu-id="8391f-134">Hvis automatiske adresseforslag er aktiveret, kan du angive yderligere indstillinger, f.eks. det maksimale antal forslag, der skal gives.</span><span class="sxs-lookup"><span data-stu-id="8391f-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="8391f-135">Føje et leveringsadressemodul til en betalingsside og angive de krævede egenskaber</span><span class="sxs-lookup"><span data-stu-id="8391f-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="8391f-136">Et leveringsadressemodul kan kun føjes til et betalignsmodul.</span><span class="sxs-lookup"><span data-stu-id="8391f-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="8391f-137">Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsadressemodulet og føjer det til en betalingsside, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="8391f-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8391f-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8391f-138">Additional resources</span></span>

[<span data-ttu-id="8391f-139">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="8391f-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8391f-140">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="8391f-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8391f-141">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="8391f-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8391f-142">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="8391f-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8391f-143">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="8391f-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8391f-144">Modul til afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="8391f-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="8391f-145">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="8391f-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8391f-146">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="8391f-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="8391f-147">Butiksvælgermodul</span><span class="sxs-lookup"><span data-stu-id="8391f-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]