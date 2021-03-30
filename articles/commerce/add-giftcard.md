---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206289"
---
# <a name="gift-card-module"></a><span data-ttu-id="18f05-103">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="18f05-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18f05-104">I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18f05-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="18f05-105">Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="18f05-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="18f05-106">Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="18f05-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="18f05-107">SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.</span><span class="sxs-lookup"><span data-stu-id="18f05-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="18f05-108">Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="18f05-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="18f05-109">Understøttelse til indløsning af SVS- og Givex-gavekort i betalingsprocessen er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="18f05-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="18f05-110">Der er to tilgængelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="18f05-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="18f05-111">**Gavekort** - Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="18f05-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="18f05-112">**Saldokontrol af gavekort** – Dette modul kan bruges på en hvilken som helst side til at kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="18f05-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="18f05-113">Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="18f05-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="18f05-114">Understøttelse af saldokontrolmodulet til gavekort er tilgængelig i Dynamics 365 Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="18f05-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="18f05-115">Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="18f05-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="18f05-117">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="18f05-117">Module properties</span></span>

- <span data-ttu-id="18f05-118">**Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="18f05-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="18f05-119">Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="18f05-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="18f05-120">Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.</span><span class="sxs-lookup"><span data-stu-id="18f05-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="18f05-121">Understøttede værdier:</span><span class="sxs-lookup"><span data-stu-id="18f05-121">Supported values:</span></span>
-   <span data-ttu-id="18f05-122">Pinkode</span><span class="sxs-lookup"><span data-stu-id="18f05-122">PIN</span></span>
-   <span data-ttu-id="18f05-123">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="18f05-123">Expiration date</span></span>
-   <span data-ttu-id="18f05-124">Pinkode og udløbsdato</span><span class="sxs-lookup"><span data-stu-id="18f05-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="18f05-125">None</span><span class="sxs-lookup"><span data-stu-id="18f05-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="18f05-126">Indstillinger for websted for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="18f05-126">Site settings for gift card modules</span></span>

<span data-ttu-id="18f05-127">I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser** er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="18f05-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="18f05-128">Denne indstilling understøtter tre værdier:</span><span class="sxs-lookup"><span data-stu-id="18f05-128">This setting supports three values:</span></span>
- <span data-ttu-id="18f05-129">**Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="18f05-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="18f05-130">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="18f05-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="18f05-131">**SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="18f05-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="18f05-132">Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="18f05-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="18f05-133">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="18f05-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="18f05-134">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="18f05-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18f05-135">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.11 og er kun nødvendige, hvis du har brug for understøttelse af SVS- eller Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="18f05-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="18f05-136">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="18f05-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="18f05-137">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="18f05-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="18f05-138">Føje et gavekortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="18f05-138">Add a gift card module to a page</span></span>

<span data-ttu-id="18f05-139">Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="18f05-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18f05-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="18f05-140">Additional resources</span></span>

[<span data-ttu-id="18f05-141">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="18f05-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="18f05-142">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="18f05-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="18f05-143">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="18f05-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="18f05-144">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="18f05-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="18f05-145">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="18f05-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="18f05-146">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="18f05-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="18f05-147">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="18f05-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="18f05-148">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="18f05-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="18f05-149">Understøttelse af eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="18f05-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="18f05-150">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="18f05-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]