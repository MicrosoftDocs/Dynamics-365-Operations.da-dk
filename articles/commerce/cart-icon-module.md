---
title: Modulet Indkøbskurvikon
description: I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411239"
---
# <a name="cart-icon-module"></a><span data-ttu-id="f3568-103">Modulet Indkøbskurvikon</span><span class="sxs-lookup"><span data-stu-id="f3568-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3568-104">I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3568-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f3568-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="f3568-105">Overview</span></span>

<span data-ttu-id="f3568-106">Modulet Indkøbskurvikon repræsenterer indkøbsvognen i overskriftmodulet på siden, og det viser antallet af varer i en indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="f3568-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="f3568-107">Modulet Indkøbskurvikon viser også en indkøbsvognoversigt (også kaldet en minivogn), når der peges på ikonet for indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="f3568-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="f3568-108">Minivognen giver brugeren en oversigt over varerne i indkøbsvognen uden at skulle navigere til siden med indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="f3568-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="f3568-109">Derudover giver det også brugeren mulighed for at gå direkte til betalingssiden, hvis man er tilfreds med oversigten.</span><span class="sxs-lookup"><span data-stu-id="f3568-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="f3568-110">Det reducerer antallet af sidenavigeringer, og gør betalingen hurtigere.</span><span class="sxs-lookup"><span data-stu-id="f3568-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="f3568-111">Understøttelse af indkøbsvognikonets modul er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="f3568-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="f3568-112">Følgende billede viser et eksempel på et indkøbskurvikonmodul, der viser en minivogn i Fabrikam-hovedet.</span><span class="sxs-lookup"><span data-stu-id="f3568-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Eksempel på et indkøbvognikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="f3568-114">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="f3568-114">Module properties</span></span>

- <span data-ttu-id="f3568-115">**Vis minivogn** – Hvis sand, aktiverer denne egenskab en indkøbsvognoversigt (minivogn), som vises, når man peger på indkøbsvognens ikon.</span><span class="sxs-lookup"><span data-stu-id="f3568-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="f3568-116">Denne funktionalitet understøttes kun ved visning på skrivebordet.</span><span class="sxs-lookup"><span data-stu-id="f3568-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="f3568-117">Føje et indkøbskurvikonmodul til en side</span><span class="sxs-lookup"><span data-stu-id="f3568-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="f3568-118">Hvis du vil tilføje et indkøbsvognikonmodul, skal du se [Overskriftsmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="f3568-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3568-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f3568-119">Additional resources</span></span>

[<span data-ttu-id="f3568-120">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="f3568-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f3568-121">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="f3568-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f3568-122">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="f3568-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f3568-123">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="f3568-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f3568-124">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="f3568-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f3568-125">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="f3568-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f3568-126">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="f3568-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f3568-127">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="f3568-127">Gift card module</span></span>](add-giftcard.md)
