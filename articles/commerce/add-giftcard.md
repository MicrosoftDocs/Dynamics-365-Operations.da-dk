---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a8428963e105e422dcd048863c17df0926a409ac
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411106"
---
# <a name="gift-card-module"></a><span data-ttu-id="2d1b2-103">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="2d1b2-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d1b2-104">I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2d1b2-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="2d1b2-105">Overview</span></span>

<span data-ttu-id="2d1b2-106">Gavekort er en almindelig form for betaling, og gavekortmodulet kan bruges i modulet til betaling ved kassen til at acceptere gavekort.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="2d1b2-107">Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="2d1b2-108">SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="2d1b2-109">Du kan flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex, i [Support for eksterne gavekort](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="2d1b2-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="2d1b2-110">Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="2d1b2-112">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="2d1b2-112">Module properties</span></span>

- <span data-ttu-id="2d1b2-113">**Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="2d1b2-114">Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="2d1b2-115">Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="2d1b2-116">Understøttede værdier:</span><span class="sxs-lookup"><span data-stu-id="2d1b2-116">Supported values:</span></span>
-   <span data-ttu-id="2d1b2-117">Pinkode</span><span class="sxs-lookup"><span data-stu-id="2d1b2-117">PIN</span></span>
-   <span data-ttu-id="2d1b2-118">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="2d1b2-118">Expiration date</span></span>
-   <span data-ttu-id="2d1b2-119">Pinkode og udløbsdato</span><span class="sxs-lookup"><span data-stu-id="2d1b2-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="2d1b2-120">None</span><span class="sxs-lookup"><span data-stu-id="2d1b2-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="2d1b2-121">Indstillinger for websted for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="2d1b2-121">Site settings for gift card modules</span></span>

<span data-ttu-id="2d1b2-122">I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser**er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="2d1b2-123">Denne indstilling understøtter tre værdier:</span><span class="sxs-lookup"><span data-stu-id="2d1b2-123">This setting supports three values:</span></span>
- <span data-ttu-id="2d1b2-124">**Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="2d1b2-125">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="2d1b2-126">**SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsningen af SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="2d1b2-127">Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="2d1b2-128">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsningen af Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="2d1b2-129">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="2d1b2-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="2d1b2-130">Føje et gavekortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="2d1b2-130">Add a gift card module to a page</span></span>

<span data-ttu-id="2d1b2-131">Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="2d1b2-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d1b2-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2d1b2-132">Additional resources</span></span>

[<span data-ttu-id="2d1b2-133">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="2d1b2-133">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2d1b2-134">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="2d1b2-134">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2d1b2-135">Understøttelse af eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="2d1b2-135">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
