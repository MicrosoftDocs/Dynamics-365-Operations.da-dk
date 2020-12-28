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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa6b98bb41c0845cfa3ab36767f304ad70f46399
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411244"
---
# <a name="gift-card-module"></a><span data-ttu-id="418b4-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="418b4-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="418b4-104">I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="418b4-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="418b4-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="418b4-105">Overview</span></span>

<span data-ttu-id="418b4-106">Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="418b4-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="418b4-107">Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="418b4-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="418b4-108">SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.</span><span class="sxs-lookup"><span data-stu-id="418b4-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="418b4-109">Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="418b4-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="418b4-110">Understøttelse til indløsning af SVS- og Givex-gavekort i betalingsprocessen er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="418b4-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="418b4-111">Der er to tilgængelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="418b4-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="418b4-112">**Gavekort** - Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="418b4-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="418b4-113">**Saldokontrol af gavekort** – Dette modul kan bruges på en hvilken som helst side til at kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="418b4-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="418b4-114">Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="418b4-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="418b4-115">Understøttelse af saldokontrolmodulet til gavekort er tilgængelig i Dynamics 365 Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="418b4-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="418b4-116">Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="418b4-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="418b4-118">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="418b4-118">Module properties</span></span>

- <span data-ttu-id="418b4-119">**Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="418b4-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="418b4-120">Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="418b4-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="418b4-121">Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.</span><span class="sxs-lookup"><span data-stu-id="418b4-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="418b4-122">Understøttede værdier:</span><span class="sxs-lookup"><span data-stu-id="418b4-122">Supported values:</span></span>
-   <span data-ttu-id="418b4-123">Pinkode</span><span class="sxs-lookup"><span data-stu-id="418b4-123">PIN</span></span>
-   <span data-ttu-id="418b4-124">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="418b4-124">Expiration date</span></span>
-   <span data-ttu-id="418b4-125">Pinkode og udløbsdato</span><span class="sxs-lookup"><span data-stu-id="418b4-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="418b4-126">None</span><span class="sxs-lookup"><span data-stu-id="418b4-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="418b4-127">Indstillinger for websted for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="418b4-127">Site settings for gift card modules</span></span>

<span data-ttu-id="418b4-128">I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser** er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="418b4-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="418b4-129">Denne indstilling understøtter tre værdier:</span><span class="sxs-lookup"><span data-stu-id="418b4-129">This setting supports three values:</span></span>
- <span data-ttu-id="418b4-130">**Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="418b4-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="418b4-131">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="418b4-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="418b4-132">**SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="418b4-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="418b4-133">Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="418b4-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="418b4-134">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="418b4-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="418b4-135">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="418b4-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="418b4-136">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.11 og er kun nødvendige, hvis du har brug for understøttelse af SVS- eller Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="418b4-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="418b4-137">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="418b4-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="418b4-138">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="418b4-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="418b4-139">Føje et gavekortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="418b4-139">Add a gift card module to a page</span></span>

<span data-ttu-id="418b4-140">Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="418b4-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="418b4-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="418b4-141">Additional resources</span></span>

[<span data-ttu-id="418b4-142">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="418b4-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="418b4-143">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="418b4-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="418b4-144">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="418b4-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="418b4-145">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="418b4-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="418b4-146">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="418b4-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="418b4-147">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="418b4-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="418b4-148">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="418b4-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="418b4-149">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="418b4-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="418b4-150">Understøttelse af eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="418b4-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="418b4-151">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="418b4-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
