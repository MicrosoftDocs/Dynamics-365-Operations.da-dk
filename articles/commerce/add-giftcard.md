---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797665"
---
# <a name="gift-card-module"></a><span data-ttu-id="daceb-103">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="daceb-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="daceb-104">I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="daceb-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="daceb-105">Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="daceb-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="daceb-106">Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="daceb-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="daceb-107">SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.</span><span class="sxs-lookup"><span data-stu-id="daceb-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="daceb-108">Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="daceb-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="daceb-109">Understøttelse til indløsning af SVS- og Givex-gavekort i betalingsprocessen er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="daceb-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="daceb-110">Der er to tilgængelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="daceb-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="daceb-111">**Gavekort** - Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="daceb-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="daceb-112">**Saldokontrol af gavekort** – Dette modul kan bruges på en hvilken som helst side til at kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="daceb-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="daceb-113">Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="daceb-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="daceb-114">Understøttelse af saldokontrolmodulet til gavekort er tilgængelig i Dynamics 365 Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="daceb-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="daceb-115">Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="daceb-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="daceb-117">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="daceb-117">Module properties</span></span>

- <span data-ttu-id="daceb-118">**Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="daceb-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="daceb-119">Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="daceb-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="daceb-120">Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.</span><span class="sxs-lookup"><span data-stu-id="daceb-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="daceb-121">Understøttede værdier:</span><span class="sxs-lookup"><span data-stu-id="daceb-121">Supported values:</span></span>
-   <span data-ttu-id="daceb-122">Pinkode</span><span class="sxs-lookup"><span data-stu-id="daceb-122">PIN</span></span>
-   <span data-ttu-id="daceb-123">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="daceb-123">Expiration date</span></span>
-   <span data-ttu-id="daceb-124">Pinkode og udløbsdato</span><span class="sxs-lookup"><span data-stu-id="daceb-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="daceb-125">None</span><span class="sxs-lookup"><span data-stu-id="daceb-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="daceb-126">Indstillinger for websted for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="daceb-126">Site settings for gift card modules</span></span>

<span data-ttu-id="daceb-127">I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser** er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="daceb-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="daceb-128">Denne indstilling understøtter tre værdier:</span><span class="sxs-lookup"><span data-stu-id="daceb-128">This setting supports three values:</span></span>
- <span data-ttu-id="daceb-129">**Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="daceb-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="daceb-130">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="daceb-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="daceb-131">**SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="daceb-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="daceb-132">Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="daceb-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="daceb-133">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="daceb-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="daceb-134">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="daceb-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="daceb-135">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.11 og er kun nødvendige, hvis du har brug for understøttelse af SVS- eller Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="daceb-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="daceb-136">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="daceb-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="daceb-137">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="daceb-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="daceb-138">Føje et gavekortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="daceb-138">Add a gift card module to a page</span></span>

<span data-ttu-id="daceb-139">Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="daceb-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="daceb-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="daceb-140">Additional resources</span></span>

[<span data-ttu-id="daceb-141">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="daceb-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="daceb-142">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="daceb-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="daceb-143">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="daceb-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="daceb-144">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="daceb-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="daceb-145">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="daceb-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="daceb-146">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="daceb-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="daceb-147">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="daceb-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="daceb-148">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="daceb-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="daceb-149">Understøttelse af eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="daceb-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="daceb-150">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="daceb-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]