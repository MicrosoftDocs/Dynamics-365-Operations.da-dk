---
title: Leveringsadressemodul
description: Dette emne omhandler leveringsadressemodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985630"
---
# <a name="shipping-address-module"></a><span data-ttu-id="b932f-103">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="b932f-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b932f-104">Dette emne beskriver leveringsadressemodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b932f-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b932f-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="b932f-105">Overview</span></span>

<span data-ttu-id="b932f-106">Leveringsadressemodulet giver kunder mulighed for at tilføje eller vælge leveringsadressen for en ordre i betalingsflowet.</span><span class="sxs-lookup"><span data-stu-id="b932f-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="b932f-107">Hvis en kunde er logget på, vises adresser, der tidligere er blevet gemt for den pågældende kunde, og kunden kan vælge mellem dem.</span><span class="sxs-lookup"><span data-stu-id="b932f-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="b932f-108">Kunden kan også tilføje en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="b932f-108">The customer can also add a new address.</span></span> <span data-ttu-id="b932f-109">Leveringsadressemodulet bruges til alle varer i en ordre, som kræver levering.</span><span class="sxs-lookup"><span data-stu-id="b932f-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="b932f-110">Der kan angives leveringsadresseformater i Commerce Headquarters for hvert land eller område, og leveringsadressemodulet gennemtvinger de lande/områdespecifikke regler.</span><span class="sxs-lookup"><span data-stu-id="b932f-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="b932f-111">Når kunder angiver en leveringsadresse i betalingsflowet, har de mulighed for at gemme adressen som en primær adresse.</span><span class="sxs-lookup"><span data-stu-id="b932f-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="b932f-112">Denne indstilling vises kun, hvis en kunde er logget på.</span><span class="sxs-lookup"><span data-stu-id="b932f-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="b932f-113">Selvom leveringsadressemodulet ikke indeholder adressevalidering, kan denne funktion implementeres gennem tilpasning.</span><span class="sxs-lookup"><span data-stu-id="b932f-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="b932f-114">Følgende illustration viser et eksempel på et nyt leveringsadressemodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="b932f-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Eksempel på et leveringsadressemodul på en betalingsside](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="b932f-116">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="b932f-116">Module properties</span></span>

| <span data-ttu-id="b932f-117">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="b932f-117">Property name</span></span> | <span data-ttu-id="b932f-118">Værdier</span><span class="sxs-lookup"><span data-stu-id="b932f-118">Values</span></span> | <span data-ttu-id="b932f-119">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="b932f-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b932f-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="b932f-120">Heading</span></span> | <span data-ttu-id="b932f-121">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="b932f-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b932f-122">En valgfri overskrift til leveringsadressemodulet.</span><span class="sxs-lookup"><span data-stu-id="b932f-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="b932f-123">Vis adressetype</span><span class="sxs-lookup"><span data-stu-id="b932f-123">Show address type</span></span> | <span data-ttu-id="b932f-124">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="b932f-124">**True** or **False**</span></span> | <span data-ttu-id="b932f-125">Hvis denne valgfrie egenskab er angivet til **Sand**, vises en adressetype som f.eks **Privat** eller **Virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="b932f-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="b932f-126">Hvis der ikke er angivet en adressetype, vil adressen automatisk blive gemt som **Type**=**Anden**.</span><span class="sxs-lookup"><span data-stu-id="b932f-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="b932f-127">Føje et leveringsadressemodul til en betalingsside og angive de krævede egenskaber</span><span class="sxs-lookup"><span data-stu-id="b932f-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="b932f-128">Et leveringsadressemodul kan kun føjes til et betalignsmodul.</span><span class="sxs-lookup"><span data-stu-id="b932f-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="b932f-129">Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsadressemodulet og føjer det til en betalingsside, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b932f-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b932f-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b932f-130">Additional resources</span></span>

[<span data-ttu-id="b932f-131">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="b932f-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b932f-132">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="b932f-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b932f-133">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="b932f-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b932f-134">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="b932f-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b932f-135">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="b932f-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b932f-136">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="b932f-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b932f-137">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="b932f-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b932f-138">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="b932f-138">Gift card module</span></span>](add-giftcard.md)
