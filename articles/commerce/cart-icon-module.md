---
title: Modulet Indkøbskurvikon
description: I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793075"
---
# <a name="cart-icon-module"></a><span data-ttu-id="74d92-103">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="74d92-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74d92-104">I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74d92-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="74d92-105">Modulet Indkøbskurvikon repræsenterer indkøbsvognen i overskriftmodulet på siden, og det viser antallet af varer i en indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="74d92-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="74d92-106">Modulet Indkøbskurvikon viser også en indkøbsvognoversigt (også kaldet en minivogn), når der peges på ikonet for indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="74d92-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="74d92-107">Minivognen giver brugeren en oversigt over varerne i indkøbsvognen uden at skulle navigere til siden med indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="74d92-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="74d92-108">Derudover giver det også brugeren mulighed for at gå direkte til betalingssiden, hvis man er tilfreds med oversigten.</span><span class="sxs-lookup"><span data-stu-id="74d92-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="74d92-109">Det reducerer antallet af sidenavigeringer, og gør betalingen hurtigere.</span><span class="sxs-lookup"><span data-stu-id="74d92-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="74d92-110">Understøttelse af indkøbsvognikonets modul er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="74d92-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="74d92-111">Følgende billede viser et eksempel på et indkøbskurvikonmodul, der viser en minivogn i Fabrikam-hovedet.</span><span class="sxs-lookup"><span data-stu-id="74d92-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Eksempel på et indkøbvognikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="74d92-113">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="74d92-113">Module properties</span></span>

- <span data-ttu-id="74d92-114">**Vis minivogn** – Hvis sand, aktiverer denne egenskab en indkøbsvognoversigt (minivogn), som vises, når man peger på indkøbsvognens ikon.</span><span class="sxs-lookup"><span data-stu-id="74d92-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="74d92-115">Denne funktionalitet understøttes kun ved visning på skrivebordet.</span><span class="sxs-lookup"><span data-stu-id="74d92-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="74d92-116">Føje et indkøbskurvikonmodul til en side</span><span class="sxs-lookup"><span data-stu-id="74d92-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="74d92-117">Hvis du vil tilføje et indkøbsvognikonmodul, skal du se [Overskriftsmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="74d92-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74d92-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="74d92-118">Additional resources</span></span>

[<span data-ttu-id="74d92-119">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="74d92-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="74d92-120">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="74d92-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="74d92-121">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="74d92-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="74d92-122">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="74d92-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="74d92-123">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="74d92-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="74d92-124">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="74d92-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="74d92-125">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="74d92-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="74d92-126">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="74d92-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]