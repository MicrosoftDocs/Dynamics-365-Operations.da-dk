---
title: Betalingsmodul
description: Dette emne omhandler betalingsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818320"
---
# <a name="payment-module"></a><span data-ttu-id="53f6a-103">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53f6a-104">Dette emne omhandler betalingsmodulet og forklarer, hvordan du kan konfigurere det i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="53f6a-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="53f6a-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="53f6a-105">Overview</span></span>

<span data-ttu-id="53f6a-106">Betalingsmodulet giver kunderne mulighed for at betale for ordrer med kreditkort eller debetkort.</span><span class="sxs-lookup"><span data-stu-id="53f6a-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="53f6a-107">Integrationen af betalingsfunktioner i dette modul leveres af Dynamics 365-betalingsconnectoren til Adyen.</span><span class="sxs-lookup"><span data-stu-id="53f6a-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="53f6a-108">Du kan finde flere oplysninger om, hvordan du opsætter og konfigurerer betalingsconnectoren i [Dynamics 365-betalingsconnector til Adyen](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="53f6a-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="53f6a-109">Betalingsmodulet er vært for de betalingsoplysninger, der behandles via Adyen i en HTML-indbygget ramme (iFrame).</span><span class="sxs-lookup"><span data-stu-id="53f6a-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="53f6a-110">Betalingsmodulet interagerer med modulet Commerce Scale Unit for at hente Adyens betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="53f6a-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="53f6a-111">Som en del af interaktionen med Commerce Scale Unit kan betalingsmodulet tillade, at faktureringsadresseoplysninger enten vises i iframe eller som et separat modul.</span><span class="sxs-lookup"><span data-stu-id="53f6a-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="53f6a-112">I Fabrikam-temaet vises faktureringsadressen i et separat modul.</span><span class="sxs-lookup"><span data-stu-id="53f6a-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="53f6a-113">Denne fremgangsmåde muliggør fleksibel formatering, fordi adresselinjerne kan gengives, så de ligner linjerne i leveringsadressen.</span><span class="sxs-lookup"><span data-stu-id="53f6a-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="53f6a-114">I betalingsmodulet kan påloggede kunder også gemme deres betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="53f6a-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="53f6a-115">Betalingsoplysningerne og faktureringsadressen gemmes og administreres via Adyen-betalingsconnectoren.</span><span class="sxs-lookup"><span data-stu-id="53f6a-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="53f6a-116">Betalingsmodulet dækker alle ordregebyrer, der ikke allerede er dækket af fordelskundepoint eller et gavekort.</span><span class="sxs-lookup"><span data-stu-id="53f6a-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="53f6a-117">Hvis totalen for en ordre er fuldt dækket af fordelskundepoint eller gavekortkredit, vil betalingsmodulet være skjult, og kunden vil kunne afgive ordren uden at bruge det.</span><span class="sxs-lookup"><span data-stu-id="53f6a-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="53f6a-118">Adyen-betalingsconnectoren understøtter også effektiv kundegodkendelse (SCA).</span><span class="sxs-lookup"><span data-stu-id="53f6a-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="53f6a-119">En del af EU Payment Services-direktivet 2.0 (PSD 2.0) kræver, at onlinekunder godkendes uden for deres onlineindkøbsløsning, når de bruger en elektronisk betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="53f6a-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="53f6a-120">Under betalingsprocessen omdirigeres kunderne til deres banks websted.</span><span class="sxs-lookup"><span data-stu-id="53f6a-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="53f6a-121">Efter godkendelsen omdirigeres de derefter tilbage til flowet for Commerce-betalingen.</span><span class="sxs-lookup"><span data-stu-id="53f6a-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="53f6a-122">Under denne omdirigering vil de oplysninger, som en kunde har angivet i betalingsflowet (f.eks. leveringsadresse, leveringsindstillinger, oplysninger om gavekort og fordelskundeoplysninger) blive bevaret.</span><span class="sxs-lookup"><span data-stu-id="53f6a-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="53f6a-123">Før du kan aktivere denne funktion, skal betalingsconnectoren konfigureres til SCA i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="53f6a-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="53f6a-124">Du kan finde flere oplysninger i [Effektiv kundegodkendelse ved hjælp af Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="53f6a-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="53f6a-125">Følgende illustration viser et eksempel på moduler for gavekort, fordelskunde og betaling på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="53f6a-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Eksempel på moduler for gavekort, fordelskunde og betaling på en betalingsside](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="53f6a-127">Egenskaber for betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-127">Payment module properties</span></span>

| <span data-ttu-id="53f6a-128">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="53f6a-128">Property name</span></span> | <span data-ttu-id="53f6a-129">Værdier</span><span class="sxs-lookup"><span data-stu-id="53f6a-129">Values</span></span> | <span data-ttu-id="53f6a-130">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="53f6a-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="53f6a-131">Overskrift</span><span class="sxs-lookup"><span data-stu-id="53f6a-131">Heading</span></span> | <span data-ttu-id="53f6a-132">Overskriftstekst</span><span class="sxs-lookup"><span data-stu-id="53f6a-132">Heading text</span></span> | <span data-ttu-id="53f6a-133">En valgfri overskrift til betalingsmodulet.</span><span class="sxs-lookup"><span data-stu-id="53f6a-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="53f6a-134">Højden på iFrame.</span><span class="sxs-lookup"><span data-stu-id="53f6a-134">Height of the iframe</span></span> | <span data-ttu-id="53f6a-135">Pixels</span><span class="sxs-lookup"><span data-stu-id="53f6a-135">Pixels</span></span> | <span data-ttu-id="53f6a-136">Højden på iFrame i pixel.</span><span class="sxs-lookup"><span data-stu-id="53f6a-136">The iframe height, in pixels.</span></span> <span data-ttu-id="53f6a-137">Højden kan dog justeres efter behov.</span><span class="sxs-lookup"><span data-stu-id="53f6a-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="53f6a-138">Vis faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="53f6a-138">Show billing address</span></span> | <span data-ttu-id="53f6a-139">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="53f6a-139">**True** or **False**</span></span> | <span data-ttu-id="53f6a-140">Hvis denne egenskab er angivet til **Sand**, vil faktureringsadressen blive betjent af Adyen i betalingsmodulets iFrame.</span><span class="sxs-lookup"><span data-stu-id="53f6a-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="53f6a-141">Hvis den er indstillet til **Falsk**, betjenes faktureringsadressen ikke af Adyen, og en Commerce-bruger skal konfigurere et modul, der viser faktureringsadressen på betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="53f6a-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="53f6a-142">Tilsidesæt betalingstype</span><span class="sxs-lookup"><span data-stu-id="53f6a-142">Payment style override</span></span> | <span data-ttu-id="53f6a-143">Kode for overlappende typografiark (CSS)</span><span class="sxs-lookup"><span data-stu-id="53f6a-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="53f6a-144">Da betalingsmodulet er knyttet til en iframe, er der begrænsede formateringsfunktioner.</span><span class="sxs-lookup"><span data-stu-id="53f6a-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="53f6a-145">Du kan foretage en del formatering ved hjælp af denne egenskab.</span><span class="sxs-lookup"><span data-stu-id="53f6a-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="53f6a-146">Hvis du vil tilsidesætte webstedets typografier, skal du indsætte CSS-koden som værdien for denne egenskab.</span><span class="sxs-lookup"><span data-stu-id="53f6a-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="53f6a-147">Webstedsgeneratorens CSS-tilsidesættelser og -typografier gælder ikke for dette modul.</span><span class="sxs-lookup"><span data-stu-id="53f6a-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="53f6a-148">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="53f6a-148">Billing address</span></span>

<span data-ttu-id="53f6a-149">Betalingsmodulet gør det muligt for kunderne at angive en faktureringsadresse til deres betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="53f6a-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="53f6a-150">De kan også bruge deres leveringsadresse som faktureringsadresse, så betalingsflowet bliver lettere og hurtigere.</span><span class="sxs-lookup"><span data-stu-id="53f6a-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="53f6a-151">Hvis egenskaben **Vis faktureringsadresse** er angivet til **Falsk**, skal betalingsmodulet konfigureres på betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="53f6a-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="53f6a-152">Føje et betalingsmodul til en betalingsside og angive de krævede egenskaber</span><span class="sxs-lookup"><span data-stu-id="53f6a-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="53f6a-153">Et modul til at udføre betalingen kan kun føjes til et betalingsmodul.</span><span class="sxs-lookup"><span data-stu-id="53f6a-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="53f6a-154">Du kan finde flere oplysninger om, hvordan du konfigurerer et betalingsmodul for en betalingsside, under [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="53f6a-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53f6a-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="53f6a-155">Additional resources</span></span>

[<span data-ttu-id="53f6a-156">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="53f6a-157">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="53f6a-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="53f6a-158">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="53f6a-159">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="53f6a-160">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="53f6a-161">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="53f6a-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="53f6a-162">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="53f6a-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="53f6a-163">Dynamics 365-betalingsconnector til Adyen</span><span class="sxs-lookup"><span data-stu-id="53f6a-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="53f6a-164">Effektiv kundegodkendelse (SCA) ved hjælp af Adyen</span><span class="sxs-lookup"><span data-stu-id="53f6a-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
