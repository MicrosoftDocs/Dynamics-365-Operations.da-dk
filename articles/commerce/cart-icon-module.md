---
title: Modulet Indkøbskurvikon
description: I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 6771a84118504cd5c8e44302380eb970e4658902
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411083"
---
# <a name="cart-icon-module"></a><span data-ttu-id="01794-103">Modulet Indkøbskurvikon</span><span class="sxs-lookup"><span data-stu-id="01794-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01794-104">I dette emne dækkes modulet for indkøbskurvikonet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="01794-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="01794-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="01794-105">Overview</span></span>

<span data-ttu-id="01794-106">Modulet Indkøbskurvikon repræsenterer indkøbsvognen i overskriftmodulet på siden, og det viser antallet af varer i en indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="01794-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="01794-107">Modulet Indkøbskurvikon viser også en indkøbsvognoversigt (også kaldet en minivogn), når der peges på ikonet for indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="01794-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="01794-108">Minivognen giver brugeren en oversigt over varerne i indkøbsvognen uden at skulle navigere til siden med indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="01794-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="01794-109">Derudover giver det også brugeren mulighed for at gå direkte til betalingssiden, hvis man er tilfreds med oversigten.</span><span class="sxs-lookup"><span data-stu-id="01794-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="01794-110">Det reducerer antallet af sidenavigeringer, og gør betalingen hurtigere.</span><span class="sxs-lookup"><span data-stu-id="01794-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="01794-111">Følgende billede viser et eksempel på et indkøbskurvikonmodul, der viser en minivogn i Fabrikam-hovedet.</span><span class="sxs-lookup"><span data-stu-id="01794-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Eksempel på et indkøbvognikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="01794-113">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="01794-113">Module properties</span></span>

- <span data-ttu-id="01794-114">**Vis minivogn** – Hvis sand, aktiverer denne egenskab en indkøbsvognoversigt (minivogn), som vises, når man peger på indkøbsvognens ikon.</span><span class="sxs-lookup"><span data-stu-id="01794-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="01794-115">Denne funktionalitet understøttes kun ved visning på skrivebordet.</span><span class="sxs-lookup"><span data-stu-id="01794-115">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="01794-116">Føje et indkøbskurvikonmodul til en side</span><span class="sxs-lookup"><span data-stu-id="01794-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="01794-117">Hvis du vil tilføje et indkøbsvognikonmodul, skal du se [Overskriftsmodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="01794-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="01794-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="01794-118">Additional resources</span></span>

[<span data-ttu-id="01794-119">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="01794-119">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="01794-120">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="01794-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="01794-121">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="01794-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="01794-122">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="01794-122">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="01794-123">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="01794-123">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="01794-124">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="01794-124">Footer module</span></span>](author-footer-module.md)
