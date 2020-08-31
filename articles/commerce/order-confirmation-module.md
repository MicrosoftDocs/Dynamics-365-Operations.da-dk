---
title: Modulet Ordredetaljer
description: Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661166"
---
# <a name="order-details-module"></a><span data-ttu-id="0d8db-103">Modulet Ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="0d8db-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d8db-104">Dette emne omhandler ordredetaljemoduler og beskriver, hvordan du bruger dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d8db-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0d8db-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="0d8db-105">Overview</span></span>

<span data-ttu-id="0d8db-106">Modulet Ordredetaljer bruges til at vise ordrebekræftelsesoplysningerne, når en ordre er afgivet.</span><span class="sxs-lookup"><span data-stu-id="0d8db-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="0d8db-107">Det viser ordrebekræftelses-id, ordrekontaktoplysninger og andre ordreoplysninger, f.eks. de varer, der er købt, betalingsoplysninger og forsendelsesmåde.</span><span class="sxs-lookup"><span data-stu-id="0d8db-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="0d8db-108">Egenskaber for ordredetaljemodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-108">Order details module properties</span></span>

| <span data-ttu-id="0d8db-109">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="0d8db-109">Property name</span></span>  | <span data-ttu-id="0d8db-110">Værdier</span><span class="sxs-lookup"><span data-stu-id="0d8db-110">Values</span></span> | <span data-ttu-id="0d8db-111">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="0d8db-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0d8db-112">Overskrift</span><span class="sxs-lookup"><span data-stu-id="0d8db-112">Heading</span></span>        | <span data-ttu-id="0d8db-113">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="0d8db-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0d8db-114">Ordredetaljemodulet kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="0d8db-114">The order details module can have a heading.</span></span> <span data-ttu-id="0d8db-115">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="0d8db-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0d8db-116">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="0d8db-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0d8db-117">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="0d8db-117">Contact number</span></span> | <span data-ttu-id="0d8db-118">Text</span><span class="sxs-lookup"><span data-stu-id="0d8db-118">Text</span></span> | <span data-ttu-id="0d8db-119">Der kan angives et kontaktnummer for ordrerelaterede spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="0d8db-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="0d8db-120">Moduler, der kan bruges på en side med ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="0d8db-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="0d8db-121">Når du opretter en side med ordredetaljer, kan du tilføje andre relevante moduler udover modulet Ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="0d8db-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="0d8db-122">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="0d8db-122">Here are some examples:</span></span>

- <span data-ttu-id="0d8db-123">**Anbefalingsmodul** – Anbefalingsmodulet kan tilføjes på ordredetaljesiden for at foreslå andre produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="0d8db-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="0d8db-124">**Marketingmoduler** – Ethvert marketingmodul kan føjes til siden Ordredetaljer for at vise marketingindhold.</span><span class="sxs-lookup"><span data-stu-id="0d8db-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="0d8db-125">Føj et ordredetaljemodul til en side</span><span class="sxs-lookup"><span data-stu-id="0d8db-125">Add an order details module to a page</span></span>

<span data-ttu-id="0d8db-126">Hvis du vil føje et ordredetaljemodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="0d8db-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0d8db-127">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="0d8db-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0d8db-128">Angiv navnet **Ordredetaljeskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d8db-129">På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d8db-130">I dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d8db-131">På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d8db-132">I dialogboksen **Tilføj modul** skal du vælge modulet **Ordredetaljer** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d8db-133">Vælg **Gem** og derefter **Vis** for at få vist skabelonen.</span><span class="sxs-lookup"><span data-stu-id="0d8db-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="0d8db-134">Ordredetaljemodulet skal ikke gengives, fordi det kræver ordrebekræftelsesnummerets kontekst.</span><span class="sxs-lookup"><span data-stu-id="0d8db-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="0d8db-135">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="0d8db-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0d8db-136">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="0d8db-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0d8db-137">I dialogboksen **Vælg en skabelon** skal du vælge **Ordredetaljeskabelon**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="0d8db-138">Under **Sidenavn** skal du angive **Ordredetaljeside** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d8db-139">På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d8db-140">I dialogboksen **Tilføj modul** skal du vælge modulet **Ordredetaljer** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d8db-141">Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for ordredetaljemodulet.</span><span class="sxs-lookup"><span data-stu-id="0d8db-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="0d8db-142">Angiv overskriftsteksten **Ordredetaljer** i feltet **Overskriftstekst** i dialogboksen **Overskrift**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d8db-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="0d8db-143">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="0d8db-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0d8db-144">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="0d8db-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d8db-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0d8db-145">Additional resources</span></span>

[<span data-ttu-id="0d8db-146">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0d8db-147">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="0d8db-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0d8db-148">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0d8db-149">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0d8db-150">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0d8db-151">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0d8db-152">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="0d8db-152">Gift card module</span></span>](add-giftcard.md)
