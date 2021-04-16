---
title: Ordrebekræftelsesmodul
description: Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan bruge dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804571"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="e4f30-103">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4f30-104">Dette emne omhandler ordrebekræftelsesmoduler og beskriver, hvordan du kan bruge dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4f30-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e4f30-105">Ordrebekræftelsesmodulet bruges til at vise ordrebekræftelsesoplysningerne, når en ordre er afgivet.</span><span class="sxs-lookup"><span data-stu-id="e4f30-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="e4f30-106">Det viser ordrebekræftelses-id, ordrekontaktoplysninger og andre ordreoplysninger, f.eks. de varer, der er købt, afhentningsoplysninger og forsendelsesmåde.</span><span class="sxs-lookup"><span data-stu-id="e4f30-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="e4f30-107">Egenskaber for ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-107">Order confirmation module properties</span></span>

| <span data-ttu-id="e4f30-108">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="e4f30-108">Property name</span></span>  | <span data-ttu-id="e4f30-109">Værdier</span><span class="sxs-lookup"><span data-stu-id="e4f30-109">Values</span></span> | <span data-ttu-id="e4f30-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e4f30-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e4f30-111">Overskrift</span><span class="sxs-lookup"><span data-stu-id="e4f30-111">Heading</span></span>        | <span data-ttu-id="e4f30-112">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="e4f30-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e4f30-113">Ordrebekræftelsesmodulet kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="e4f30-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="e4f30-114">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="e4f30-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e4f30-115">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="e4f30-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e4f30-116">Kontaktnummer</span><span class="sxs-lookup"><span data-stu-id="e4f30-116">Contact number</span></span> | <span data-ttu-id="e4f30-117">Text</span><span class="sxs-lookup"><span data-stu-id="e4f30-117">Text</span></span> | <span data-ttu-id="e4f30-118">Der kan angives et kontaktnummer for ordrerelaterede spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="e4f30-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="e4f30-119">Vis oplysninger om tidsinterval for afhentning</span><span class="sxs-lookup"><span data-stu-id="e4f30-119">Show pickup timeslot information</span></span> | <span data-ttu-id="e4f30-120">Sand eller falsk</span><span class="sxs-lookup"><span data-stu-id="e4f30-120">True or False</span></span> | <span data-ttu-id="e4f30-121">Denne egenskab er tilgængelig i Dynamics 365 Commerce 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="e4f30-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="e4f30-122">Hvis sand, vises de afhentede oplysninger om tidsintervallet for afhentningen, hvis de er tilgængelige for en vare, der skal afhentes</span><span class="sxs-lookup"><span data-stu-id="e4f30-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="e4f30-123">Moduler, der kan bruges på en ordrebekræftelsesside</span><span class="sxs-lookup"><span data-stu-id="e4f30-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="e4f30-124">Når du opretter en ordrebekræftelsesside, kan du tilføje andre relevante moduler udover ordrebekræftelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="e4f30-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="e4f30-125">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="e4f30-125">Here are some examples:</span></span>

- <span data-ttu-id="e4f30-126">**Anbefalingsmodul** – Anbefalingsmodulet kan tilføjes på ordrebekræftelsessiden for at foreslå andre produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="e4f30-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="e4f30-127">**Marketingmoduler** – Ethvert marketingmodul kan føjes til ordrebekræftelsessiden for at vise marketingindhold.</span><span class="sxs-lookup"><span data-stu-id="e4f30-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="e4f30-128">Føj et ordrebekræftelsesmodul til en side</span><span class="sxs-lookup"><span data-stu-id="e4f30-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="e4f30-129">Hvis du vil føje et ordrebekræftelsesmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e4f30-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e4f30-130">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="e4f30-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e4f30-131">Angiv navnet **Ordrebekræftelsesskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4f30-132">På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e4f30-133">I dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e4f30-134">På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e4f30-135">I dialogboksen **Tilføj modul** skal du vælge modulet **Ordrebekræftelse** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e4f30-136">Vælg **Gem** og derefter **Vis** for at få vist skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e4f30-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="e4f30-137">Ordrebekræftelsesmodulet bliver ikke gengivet, fordi det kræver ordrebekræftelsesnummerets kontekst.</span><span class="sxs-lookup"><span data-stu-id="e4f30-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="e4f30-138">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="e4f30-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e4f30-139">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="e4f30-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="e4f30-140">I dialogboksen **Vælg en skabelon** skal du vælge **Ordrebekræftelsesskabelon**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="e4f30-141">Under **Sidenavn** skal du angive **Ordrebekræftelsesside** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4f30-142">På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e4f30-143">I dialogboksen **Tilføj modul** skal du vælge modulet **Ordrebekræftelse** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e4f30-144">Vælg **Overskrift** ud for blyantsymbolet i egenskabsruden for ordrebekræftelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="e4f30-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="e4f30-145">Angiv overskriftsteksten **Ordrebekræftelse** i feltet **Overskriftstekst** i dialogboksen **Overskrift**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f30-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="e4f30-146">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="e4f30-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e4f30-147">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="e4f30-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4f30-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e4f30-148">Additional resources</span></span>

[<span data-ttu-id="e4f30-149">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e4f30-150">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="e4f30-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e4f30-151">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e4f30-152">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e4f30-153">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e4f30-154">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e4f30-155">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="e4f30-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="e4f30-156">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="e4f30-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]