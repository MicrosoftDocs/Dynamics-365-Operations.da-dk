---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761075"
---
# <a name="gift-card-module"></a><span data-ttu-id="cec03-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="cec03-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="cec03-104">I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cec03-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cec03-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="cec03-105">Overview</span></span>

<span data-ttu-id="cec03-106">Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="cec03-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="cec03-107">Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="cec03-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="cec03-108">SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.</span><span class="sxs-lookup"><span data-stu-id="cec03-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="cec03-109">Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="cec03-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="cec03-110">Der er to tilgængelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="cec03-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="cec03-111">**Gavekort** - Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="cec03-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="cec03-112">**Saldokontrol af gavekort** – Dette modul kan bruges på en hvilken som helst side til at kontrollere saldoen på et gavekort.</span><span class="sxs-lookup"><span data-stu-id="cec03-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="cec03-113">Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="cec03-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="cec03-114">Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="cec03-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="cec03-116">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="cec03-116">Module properties</span></span>

- <span data-ttu-id="cec03-117">**Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="cec03-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="cec03-118">Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="cec03-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="cec03-119">Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.</span><span class="sxs-lookup"><span data-stu-id="cec03-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="cec03-120">Understøttede værdier:</span><span class="sxs-lookup"><span data-stu-id="cec03-120">Supported values:</span></span>
-   <span data-ttu-id="cec03-121">Pinkode</span><span class="sxs-lookup"><span data-stu-id="cec03-121">PIN</span></span>
-   <span data-ttu-id="cec03-122">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="cec03-122">Expiration date</span></span>
-   <span data-ttu-id="cec03-123">Pinkode og udløbsdato</span><span class="sxs-lookup"><span data-stu-id="cec03-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="cec03-124">None</span><span class="sxs-lookup"><span data-stu-id="cec03-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="cec03-125">Indstillinger for websted for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="cec03-125">Site settings for gift card modules</span></span>

<span data-ttu-id="cec03-126">I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser**er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="cec03-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="cec03-127">Denne indstilling understøtter tre værdier:</span><span class="sxs-lookup"><span data-stu-id="cec03-127">This setting supports three values:</span></span>
- <span data-ttu-id="cec03-128">**Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="cec03-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="cec03-129">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="cec03-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="cec03-130">**SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="cec03-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="cec03-131">Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="cec03-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="cec03-132">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="cec03-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="cec03-133">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="cec03-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="cec03-134">Føje et gavekortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="cec03-134">Add a gift card module to a page</span></span>

<span data-ttu-id="cec03-135">Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="cec03-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cec03-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cec03-136">Additional resources</span></span>

[<span data-ttu-id="cec03-137">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="cec03-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cec03-138">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="cec03-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="cec03-139">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="cec03-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cec03-140">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="cec03-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="cec03-141">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="cec03-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="cec03-142">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="cec03-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="cec03-143">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="cec03-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="cec03-144">Understøttelse af eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="cec03-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
