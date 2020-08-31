---
title: Leveringsindstillingsmodul
description: Dette emne omhandler leveringsindstillingsmoduler og forklarer, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 60449e9492c8e831b4ec6b2896f1ab471ef9d499
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661194"
---
# <a name="delivery-options-module"></a><span data-ttu-id="26b4f-103">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="26b4f-104">Dette emne omhandler leveringsindstillingsmoduler og forklarer, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26b4f-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="26b4f-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="26b4f-105">Overview</span></span>

<span data-ttu-id="26b4f-106">Leveringsindstillingsmoduler gør det muligt for kunderne at vælge en leveringsmåde, f.eks. forsendelse eller afhentning af deres onlineordre.</span><span class="sxs-lookup"><span data-stu-id="26b4f-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="26b4f-107">Der skal angives en leveringsadresse for at bestemme leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="26b4f-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="26b4f-108">Hvis leveringsadressen ændres, skal leveringsindstillingerne hentes igen.</span><span class="sxs-lookup"><span data-stu-id="26b4f-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="26b4f-109">Hvis en ordre kun omfatter varer, der afhentes i en butik, skjules dette modul automatisk.</span><span class="sxs-lookup"><span data-stu-id="26b4f-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="26b4f-110">Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsmåder, i [Konfiguration af onlinekanaler](channel-setup-online.md) og [Konfigurer leveringsmåder](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="26b4f-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="26b4f-111">Hver leveringsmåde kan være tilknyttet et gebyr.</span><span class="sxs-lookup"><span data-stu-id="26b4f-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="26b4f-112">Du kan få flere oplysninger om, hvordan du konfigurer gebyrer for en onlinebutik, i [Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="26b4f-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="26b4f-113">I Commerce version 10.0.13 er leveringsindstillingsmodulet opdateret til at understøtte funktionerne **Hovedgebyrer uden forholdsberegning** og **Levering som et linjegebyr**.</span><span class="sxs-lookup"><span data-stu-id="26b4f-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="26b4f-114">Hvis forholdsberegning er deaktiveret, forventes det, at e-Commerce-arbejdsprocessen ikke tillader en blandet leveringsmåde for varerne i indkøbsvognen (dvs. at nogle varer er valgt til levering, mens andre er valgt til afhentning).</span><span class="sxs-lookup"><span data-stu-id="26b4f-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="26b4f-115">Funktionen **Hovedgebyrerne uden forholdsberegning** kræver, at flaget **Aktivér ensartet leveringsmåde i kanal** er aktiveret i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="26b4f-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="26b4f-116">Når dette flag er aktiveret, tilskrives der forsendelsesgebyrer enten på hovedniveauet eller linjeniveauet, afhængigt af konfigurationen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="26b4f-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="26b4f-117">Fabrikam-temaet understøtter en blandet leveringsmåde, hvor nogle varer er valgt til levering, men andre er valgt til afhentning.</span><span class="sxs-lookup"><span data-stu-id="26b4f-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="26b4f-118">I denne tilstand anvendes der forholdsberegning til forsendelsesgebyrer for alle varer, der er valgt til leveringsmåden for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="26b4f-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="26b4f-119">For at blandet leveringsmåde kan fungere korrekt, skal du først konfigurere funktionen **Hovedgebyrer med forholdsberegning** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="26b4f-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="26b4f-120">Yderligere oplysninger om denne konfiguration finder du i [Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="26b4f-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="26b4f-121">Hvis der gælder forsendelsesgebyrer for linjeelementer, kan de vises på indkøbslinjen for hver vare.</span><span class="sxs-lookup"><span data-stu-id="26b4f-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="26b4f-122">Denne funktion kræver, at egenskaben **Vis forsendelsesgebyrer på linjeelement** er aktiveret både for indkøbsvognmodulet og betalingsmodulet.</span><span class="sxs-lookup"><span data-stu-id="26b4f-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="26b4f-123">Yderligere oplysninger finder du i [Vognmodul](add-cart-module.md) og [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="26b4f-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="26b4f-124">Følgende illustration viser et eksempel på et leveringsindstillingsmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="26b4f-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Eksempel på et leveringsindstillingsmodul på en betalingsside](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="26b4f-126">Egenskaber for leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-126">Delivery options module properties</span></span>

| <span data-ttu-id="26b4f-127">Egenskab</span><span class="sxs-lookup"><span data-stu-id="26b4f-127">Property</span></span> | <span data-ttu-id="26b4f-128">Værdier</span><span class="sxs-lookup"><span data-stu-id="26b4f-128">Values</span></span> | <span data-ttu-id="26b4f-129">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="26b4f-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="26b4f-130">Overskrift</span><span class="sxs-lookup"><span data-stu-id="26b4f-130">Heading</span></span> | <span data-ttu-id="26b4f-131">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="26b4f-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="26b4f-132">En valgfri overskrift til leveringsindstillingsmodulet.</span><span class="sxs-lookup"><span data-stu-id="26b4f-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="26b4f-133">Brugerdefineret CSS-klassenavn</span><span class="sxs-lookup"><span data-stu-id="26b4f-133">Custom CSS class name</span></span> | <span data-ttu-id="26b4f-134">Tekst</span><span class="sxs-lookup"><span data-stu-id="26b4f-134">Text</span></span> | <span data-ttu-id="26b4f-135">Et brugerdefineret klassenavn for overlappende typografiark (CSS), der bruges til at gengive dette modul, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="26b4f-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="26b4f-136">Indstilling til filtreret leveringstilstand</span><span class="sxs-lookup"><span data-stu-id="26b4f-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="26b4f-137">**Filtrér ikke** eller **Ingen forsendelsestilstand**</span><span class="sxs-lookup"><span data-stu-id="26b4f-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="26b4f-138">En værdi, der angiver, om leveringsindstillingsmodulet skal filtrere alle leveringsmåder, der ikke er forsendelser.</span><span class="sxs-lookup"><span data-stu-id="26b4f-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="26b4f-139">Føje et leveringsindstillingsmodul til en betalingsside og angive de krævede egenskaber</span><span class="sxs-lookup"><span data-stu-id="26b4f-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="26b4f-140">Et leveringsindstillingsmodul kan kun føjes til et betalignsmodul.</span><span class="sxs-lookup"><span data-stu-id="26b4f-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="26b4f-141">Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsindstillingsmodulet og føjer det til en betalingsside, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="26b4f-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26b4f-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="26b4f-142">Additional resources</span></span>

[<span data-ttu-id="26b4f-143">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="26b4f-144">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="26b4f-145">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="26b4f-146">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="26b4f-147">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="26b4f-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="26b4f-148">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="26b4f-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="26b4f-149">Konfiguration af onlinekanal</span><span class="sxs-lookup"><span data-stu-id="26b4f-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="26b4f-150">Avancerede automatiske gebyrer for omni-kanal</span><span class="sxs-lookup"><span data-stu-id="26b4f-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="26b4f-151">Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer</span><span class="sxs-lookup"><span data-stu-id="26b4f-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="26b4f-152">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="26b4f-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
