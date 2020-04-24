---
title: Modulet Indkøbskurvikon
description: I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261558"
---
# <a name="cart-icon-module"></a><span data-ttu-id="09e10-103">Modulet Indkøbskurvikon</span><span class="sxs-lookup"><span data-stu-id="09e10-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09e10-104">I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09e10-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="09e10-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="09e10-105">Overview</span></span>

<span data-ttu-id="09e10-106">Modulet Indkøbskurvikon repræsenterer indkøbsvognen i overskriftmodulet på siden, og det viser antallet af varer i en indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="09e10-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="09e10-107">Modulet Indkøbskurvikon viser også en indkøbsvognoversigt (også kaldet en minivogn), når der peges på ikonet for indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="09e10-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="09e10-108">Minivognen giver brugeren en oversigt over varerne i indkøbsvognen uden at skulle navigere til siden med indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="09e10-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="09e10-109">Derudover giver det også brugeren mulighed for at gå direkte til betalingssiden, hvis man er tilfreds med oversigten.</span><span class="sxs-lookup"><span data-stu-id="09e10-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="09e10-110">Det reducerer antallet af sidenavigeringer, og gør betalingen hurtigere.</span><span class="sxs-lookup"><span data-stu-id="09e10-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="09e10-111">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="09e10-111">Module properties</span></span>

- <span data-ttu-id="09e10-112">**Vis minivogn** – Hvis sand, aktiverer denne egenskab en indkøbsvognoversigt (minivogn), som vises, når man peger på indkøbsvognens ikon.</span><span class="sxs-lookup"><span data-stu-id="09e10-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="09e10-113">Denne funktionalitet understøttes kun ved visning på skrivebordet.</span><span class="sxs-lookup"><span data-stu-id="09e10-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="09e10-114">Føje et indkøbskurvikonmodul til en side</span><span class="sxs-lookup"><span data-stu-id="09e10-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="09e10-115">Hvis du vil tilføje et indkøbsvognikonmodul, skal du se [Overskriftsmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="09e10-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="09e10-116">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="09e10-116">Additional resources</span></span>

[<span data-ttu-id="09e10-117">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="09e10-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="09e10-118">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="09e10-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="09e10-119">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="09e10-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="09e10-120">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="09e10-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="09e10-121">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="09e10-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="09e10-122">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="09e10-122">Footer module</span></span>](author-footer-module.md)
