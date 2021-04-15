---
title: Hurtig visning-modul
description: Dette emne omhandler hurtig visning-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d7e88163fd9b8dc4f5636ed29e2c4248aece52bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792165"
---
# <a name="quick-view-module"></a><span data-ttu-id="4bc7a-103">Modul til hurtig visning</span><span class="sxs-lookup"><span data-stu-id="4bc7a-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4bc7a-104">Dette emne omhandler hurtig visning-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4bc7a-105">Modulet Hurtig visning giver brugerne mulighed for hurtigt at få vist produktoplysninger, når de gennemser produkter på en listeside, og føje et eller flere produkter til indkøbsvognen fra listesiden uden at skulle gå til siden med produktoplysninger (PDP).</span><span class="sxs-lookup"><span data-stu-id="4bc7a-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="4bc7a-106">Modulet Hurtig visning indeholder en oversigt over de produktoplysninger, som brugerne skal bruge for at træffe en beslutning om tilføjelse af indkøbsvogn.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="4bc7a-107">Den giver også et link til PDP, så brugerne kan se yderligere produktoplysninger og købsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="4bc7a-108">Modulet Til hurtig visning understøttes af modulerne [produktsamling](product-collection-module-overview.md) og [søgeresultater](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="4bc7a-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bc7a-109">Modulet Hurtig visning er tilgængeligt efter Commerce-version 10.0.17-udgaven.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="4bc7a-110">Følgende illustration viser et eksempel på et hurtig visning-modul på en produktlisteside.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Eksempel på et hurtig visning-modul på en produktlisteside](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="4bc7a-112">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="4bc7a-112">Module properties</span></span>

<span data-ttu-id="4bc7a-113">Modulet Hurtig visning understøtter nogle af de samme funktioner som købsfeltmodulet.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="4bc7a-114">Egenskaberne for et modul til hurtig visning svarer derfor til egenskaberne for et købsfeltmodul.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="4bc7a-115">Egenskab</span><span class="sxs-lookup"><span data-stu-id="4bc7a-115">Property</span></span> | <span data-ttu-id="4bc7a-116">Værdier</span><span class="sxs-lookup"><span data-stu-id="4bc7a-116">Values</span></span> | <span data-ttu-id="4bc7a-117">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4bc7a-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4bc7a-118">Overskriftskode</span><span class="sxs-lookup"><span data-stu-id="4bc7a-118">Heading tag</span></span> | <span data-ttu-id="4bc7a-119">**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**</span><span class="sxs-lookup"><span data-stu-id="4bc7a-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="4bc7a-120">Denne egenskab definerer overskriftskoden for produkttitlen.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="4bc7a-121">Hvis hurtig visning-feltet vises øverst på siden, skal denne egenskab indstilles til **H1** for at overholde tilgængelighedsstandarder.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="4bc7a-122">Tillad brugerdefineret pris</span><span class="sxs-lookup"><span data-stu-id="4bc7a-122">Allow custom price</span></span> | <span data-ttu-id="4bc7a-123">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="4bc7a-123">**True** or **False**</span></span> | <span data-ttu-id="4bc7a-124">Hvis denne egenskab er angivet til **Sand**, kan brugeren angive en brugerdefineret pris.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="4bc7a-125">Minimumpris</span><span class="sxs-lookup"><span data-stu-id="4bc7a-125">Minimum price</span></span> | <span data-ttu-id="4bc7a-126">Heltal</span><span class="sxs-lookup"><span data-stu-id="4bc7a-126">Integer</span></span> | <span data-ttu-id="4bc7a-127">Denne egenskab kan kun anvendes, hvis egenskaben **Tillad brugerdefinerede pris** er angivet til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="4bc7a-128">Den definerer den minimumspris, som brugeren kan angive (f.eks. $1).</span><span class="sxs-lookup"><span data-stu-id="4bc7a-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="4bc7a-129">Maksimumpris</span><span class="sxs-lookup"><span data-stu-id="4bc7a-129">Maximum price</span></span> | <span data-ttu-id="4bc7a-130">Heltal</span><span class="sxs-lookup"><span data-stu-id="4bc7a-130">Integer</span></span> | <span data-ttu-id="4bc7a-131">Denne egenskab kan kun anvendes, hvis egenskaben **Tillad brugerdefinerede pris** er angivet til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="4bc7a-132">Den definerer den maksimumpris, som brugeren kan angive (f.eks. $1,000).</span><span class="sxs-lookup"><span data-stu-id="4bc7a-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="4bc7a-133">Indstillinger til Commerce-webstedsgenerator</span><span class="sxs-lookup"><span data-stu-id="4bc7a-133">Commerce site builder settings</span></span>

<span data-ttu-id="4bc7a-134">Ligesom købsfelt-modulet overholder modulet til hurtig visning indstillingerne ved **Indstillinger for websted \> Udvidelser \> Tilføj produkt til indkøbsvogn**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="4bc7a-135">Indstillingen for siden **Naviger til indkøbsvogn** ignoreres dog, da det ikke er i overensstemmelse med formålet med modulet Til hurtig visning, hvilket er at give brugerne mulighed for at gennemse flere produkter på en listeside og føje dem til indkøbsvognen uden at gå fra listesiden.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="4bc7a-136">Føje et hurtig visning-modul til produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="4bc7a-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="4bc7a-137">Et hurtig visning-modul kan tilføjes til modulerne produktsamling og søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="4bc7a-138">Følg disse trin, hvis du til tilføje et hurtig visning-modul til et produktsamlingsmodul i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4bc7a-139">Gå til **Sider**, og vælg derefter startsiden for Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="4bc7a-140">Gå til **Produktsamling**-modul på startsiden, vælg ellipsen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4bc7a-141">I dialogboksen **Tilføj modul** skal du vælge modulet **Hurtig visning** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4bc7a-142">Vælg **Overskrift** i egenskabsruden i modulet **Hurtig visning**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="4bc7a-143">Angiv feltet **Overskriftsniveau** til **H2** i dialogboksen **Overskrift**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="4bc7a-144">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="4bc7a-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4bc7a-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4bc7a-145">Additional resources</span></span>

[<span data-ttu-id="4bc7a-146">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="4bc7a-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4bc7a-147">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="4bc7a-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4bc7a-148">Produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="4bc7a-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="4bc7a-149">Modul til søgeresultater</span><span class="sxs-lookup"><span data-stu-id="4bc7a-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
