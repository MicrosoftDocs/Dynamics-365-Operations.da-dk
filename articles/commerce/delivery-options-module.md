---
title: Leveringsindstillingsmodul
description: Dette emne omhandler leveringsindstillingsmoduler og forklarer, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
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
ms.openlocfilehash: 12b0281a27dcf5f567bcd6be5530fa8e26a4ae99
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937476"
---
# <a name="delivery-options-module"></a><span data-ttu-id="33e3c-103">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="33e3c-104">Dette emne omhandler leveringsindstillingsmoduler og forklarer, hvordan du kan konfigurere dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="33e3c-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="33e3c-105">Leveringsindstillingsmoduler gør det muligt for kunderne at vælge en leveringsmåde, f.eks. forsendelse eller afhentning af deres onlineordre.</span><span class="sxs-lookup"><span data-stu-id="33e3c-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="33e3c-106">Der skal angives en leveringsadresse for at bestemme leveringsmåden.</span><span class="sxs-lookup"><span data-stu-id="33e3c-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="33e3c-107">Hvis leveringsadressen ændres, skal leveringsindstillingerne hentes igen.</span><span class="sxs-lookup"><span data-stu-id="33e3c-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="33e3c-108">Hvis en ordre kun omfatter varer, der afhentes i en butik, skjules dette modul automatisk.</span><span class="sxs-lookup"><span data-stu-id="33e3c-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="33e3c-109">Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsmåder, i [Konfiguration af onlinekanaler](channel-setup-online.md) og [Konfigurer leveringsmåder](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="33e3c-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="33e3c-110">Hver leveringsmåde kan være tilknyttet et gebyr.</span><span class="sxs-lookup"><span data-stu-id="33e3c-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="33e3c-111">Du kan få flere oplysninger om, hvordan du konfigurer gebyrer for en onlinebutik, i [Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="33e3c-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="33e3c-112">I Commerce version 10.0.13 er leveringsindstillingsmodulet opdateret til at understøtte funktionerne **Hovedgebyrer uden forholdsberegning** og **Levering som et linjegebyr**.</span><span class="sxs-lookup"><span data-stu-id="33e3c-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="33e3c-113">Hvis forholdsberegning er deaktiveret, forventes det, at e-Commerce-arbejdsprocessen ikke tillader en blandet leveringsmåde for varerne i indkøbsvognen (dvs. at nogle varer er valgt til levering, mens andre er valgt til afhentning).</span><span class="sxs-lookup"><span data-stu-id="33e3c-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="33e3c-114">Funktionen **Hovedgebyrerne uden forholdsberegning** kræver, at flaget **Aktivér ensartet leveringsmåde i kanal** er aktiveret i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="33e3c-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="33e3c-115">Når funktionens flag er aktiveret, tilskrives der forsendelsesgebyrer enten på hovedniveauet eller linjeniveauet, afhængigt af konfigurationen i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="33e3c-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="33e3c-116">Fabrikam-temaet understøtter en blandet leveringsmåde, hvor nogle varer er valgt til levering, men andre er valgt til afhentning.</span><span class="sxs-lookup"><span data-stu-id="33e3c-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="33e3c-117">I denne tilstand anvendes der forholdsberegning til forsendelsesgebyrer for alle varer, der er valgt til leveringsmåden for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="33e3c-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="33e3c-118">For at blandet leveringsmåde kan fungere korrekt, skal du først konfigurere funktionen **Hovedgebyrer med forholdsberegning** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="33e3c-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="33e3c-119">Yderligere oplysninger om denne konfiguration finder du i [Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="33e3c-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="33e3c-120">Hvis der gælder forsendelsesgebyrer for linjeelementer, kan de vises på indkøbslinjen for hver vare.</span><span class="sxs-lookup"><span data-stu-id="33e3c-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="33e3c-121">Denne funktion kræver, at egenskaben **Vis forsendelsesgebyrer på linjeelement** er aktiveret både for indkøbsvognmodulet og betalingsmodulet.</span><span class="sxs-lookup"><span data-stu-id="33e3c-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="33e3c-122">Yderligere oplysninger finder du i [Vognmodul](add-cart-module.md) og [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="33e3c-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="33e3c-123">Følgende illustration viser et eksempel på et leveringsindstillingsmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="33e3c-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Eksempel på et leveringsindstillingsmodul på en betalingsside](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="33e3c-125">Egenskaber for leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-125">Delivery options module properties</span></span>

| <span data-ttu-id="33e3c-126">Egenskab</span><span class="sxs-lookup"><span data-stu-id="33e3c-126">Property</span></span> | <span data-ttu-id="33e3c-127">Værdier</span><span class="sxs-lookup"><span data-stu-id="33e3c-127">Values</span></span> | <span data-ttu-id="33e3c-128">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="33e3c-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="33e3c-129">Overskrift</span><span class="sxs-lookup"><span data-stu-id="33e3c-129">Heading</span></span> | <span data-ttu-id="33e3c-130">Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="33e3c-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="33e3c-131">En valgfri overskrift til leveringsindstillingsmodulet.</span><span class="sxs-lookup"><span data-stu-id="33e3c-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="33e3c-132">Brugerdefineret CSS-klassenavn</span><span class="sxs-lookup"><span data-stu-id="33e3c-132">Custom CSS class name</span></span> | <span data-ttu-id="33e3c-133">Tekst</span><span class="sxs-lookup"><span data-stu-id="33e3c-133">Text</span></span> | <span data-ttu-id="33e3c-134">Et brugerdefineret klassenavn for overlappende typografiark (CSS), der bruges til at gengive dette modul, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="33e3c-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="33e3c-135">Indstilling til filtreret leveringstilstand</span><span class="sxs-lookup"><span data-stu-id="33e3c-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="33e3c-136">**Filtrér ikke** eller **Ingen forsendelsestilstand**</span><span class="sxs-lookup"><span data-stu-id="33e3c-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="33e3c-137">En værdi, der angiver, om leveringsindstillingsmodulet skal filtrere alle leveringsmåder, der ikke er forsendelser.</span><span class="sxs-lookup"><span data-stu-id="33e3c-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="33e3c-138">Vælge en leveringsindstilling automatisk</span><span class="sxs-lookup"><span data-stu-id="33e3c-138">Auto select a delivery option</span></span> | <span data-ttu-id="33e3c-139">**Filtrer ikke**, **Vælg leveringsindstilling automatisk og vis oversigt**, eller **Vælg leveringsindstilling automatisk og vis ikke oversigt**</span><span class="sxs-lookup"><span data-stu-id="33e3c-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="33e3c-140">Denne egenskab anvender automatisk den første tilgængelige leveringsindstilling i betalingstrinnet, uden at brugeren skal vælge den.</span><span class="sxs-lookup"><span data-stu-id="33e3c-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="33e3c-141">Den skal kun bruges, hvis der er en tilgængelig leveringsindstilling.</span><span class="sxs-lookup"><span data-stu-id="33e3c-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="33e3c-142">Denne egenskab understøttes fra frigivelsen af Commerce version 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="33e3c-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="33e3c-143">Føje et leveringsindstillingsmodul til en betalingsside og angive de krævede egenskaber</span><span class="sxs-lookup"><span data-stu-id="33e3c-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="33e3c-144">Et leveringsindstillingsmodul kan kun føjes til et betalignsmodul.</span><span class="sxs-lookup"><span data-stu-id="33e3c-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="33e3c-145">Du kan finde flere oplysninger om, hvordan du konfigurerer leveringsindstillingsmodulet og føjer det til en betalingsside, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="33e3c-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33e3c-146">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="33e3c-146">Additional resources</span></span>

[<span data-ttu-id="33e3c-147">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="33e3c-148">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="33e3c-149">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="33e3c-150">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="33e3c-151">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="33e3c-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="33e3c-152">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="33e3c-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="33e3c-153">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="33e3c-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="33e3c-154">Konfiguration af onlinekanal</span><span class="sxs-lookup"><span data-stu-id="33e3c-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="33e3c-155">Avancerede automatiske gebyrer for omni-kanal</span><span class="sxs-lookup"><span data-stu-id="33e3c-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="33e3c-156">Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer</span><span class="sxs-lookup"><span data-stu-id="33e3c-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="33e3c-157">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="33e3c-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
