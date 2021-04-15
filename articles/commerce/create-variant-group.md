---
title: Opret en variantgruppe
description: Dette emne beskriver, hvordan du opretter en størrelses-, typografi- eller farvevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799535"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="6770e-103">Oprette en variantgruppe</span><span class="sxs-lookup"><span data-stu-id="6770e-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6770e-104">Dette emne beskriver, hvordan du opretter en størrelses-, typografi- eller farvevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6770e-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6770e-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="6770e-105">Overview</span></span>

<span data-ttu-id="6770e-106">Dynamics 365 Commerce understøtter flere varianter for produkter.</span><span class="sxs-lookup"><span data-stu-id="6770e-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="6770e-107">Det er ideelt at konfigurere variantgrupper for forskellige produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="6770e-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="6770e-108">Der kan f.eks. oprettes en størrelsesgruppe for t-shirts med størrelserne extra small, small, medium, large og extra large, eller der oprettes en farvegruppe for at medtage alle de tilgængelige farver for et produkt.</span><span class="sxs-lookup"><span data-stu-id="6770e-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="6770e-109">Variantgrupper skal tilføjes, før der tilføjes produkter.</span><span class="sxs-lookup"><span data-stu-id="6770e-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="6770e-110">I dette emne oprettes og konfigureres en størrelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="6770e-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="6770e-111">Lignende procedurer kan bruges til at tilføje og konfigurere typografigrupper og farvegrupper.</span><span class="sxs-lookup"><span data-stu-id="6770e-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="6770e-112">Oprette en størrelsesgruppe</span><span class="sxs-lookup"><span data-stu-id="6770e-112">Create a size group</span></span>

<span data-ttu-id="6770e-113">Du kan oprette størrelsesgruppe ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="6770e-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="6770e-114">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6770e-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="6770e-115">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6770e-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6770e-116">Angiv et navn til størrelsesgruppen i feltet **Størrelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="6770e-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="6770e-117">Angiv eventuelt en passende beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6770e-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="6770e-118">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6770e-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="6770e-119">Føje attributter til størrelsesgruppen</span><span class="sxs-lookup"><span data-stu-id="6770e-119">Add attributes to the size group</span></span>

<span data-ttu-id="6770e-120">Følg disse trin for at føje attributter til en størrelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="6770e-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="6770e-121">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6770e-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="6770e-122">Vælg en størrelsesgruppe i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="6770e-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="6770e-123">Vælg **Tilføj** under **Størrelsesgruppelinjer** .</span><span class="sxs-lookup"><span data-stu-id="6770e-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="6770e-124">Angiv en streng, der repræsenterer størrelsen (f.eks. "XL"), i feltet **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="6770e-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="6770e-125">Angiv et navn til størrelsen (f.eks. "Extra Large") i feltet **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="6770e-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="6770e-126">Angiv et nummer, der repræsenterer genopfyldningsvægten, i feltet **Genopfyldningsvægt**.</span><span class="sxs-lookup"><span data-stu-id="6770e-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="6770e-127">Angiv et nummer, der repræsenterer stregkoden, i feltet **Nummer i stregkode**.</span><span class="sxs-lookup"><span data-stu-id="6770e-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="6770e-128">Angiv et nummer, der repræsenterer visningsrækkefølgen, i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="6770e-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="6770e-129">Vælg **Gem** i handlingsruden, når du er færdig med at tilføje størrelser.</span><span class="sxs-lookup"><span data-stu-id="6770e-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="6770e-130">Følgende billede viser et eksempel på en størrelsesgruppe til "størrelser på fritids-t-shirt".</span><span class="sxs-lookup"><span data-stu-id="6770e-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Oprette størrelsesgruppe](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="6770e-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6770e-132">Additional resources</span></span>

[<span data-ttu-id="6770e-133">Oversigt over produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="6770e-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6770e-134">Konfigurere detailprodukter</span><span class="sxs-lookup"><span data-stu-id="6770e-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="6770e-135">Produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="6770e-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]