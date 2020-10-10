---
title: Opret en variantgruppe
description: Dette emne beskriver, hvordan du opretter en størrelses-, typografi- eller farvevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d9279e1076796bb455429e5ff004c89ec5829e7
ms.sourcegitcommit: 3cc289399e8879b499e31a9559e1031d6ca8570a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885939"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="7e894-103">Opret en variantgruppe</span><span class="sxs-lookup"><span data-stu-id="7e894-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7e894-104">Dette emne beskriver, hvordan du opretter en størrelses-, typografi- eller farvevariantgruppe for et produkt i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7e894-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7e894-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="7e894-105">Overview</span></span>

<span data-ttu-id="7e894-106">Dynamics 365 Commerce understøtter flere varianter for produkter.</span><span class="sxs-lookup"><span data-stu-id="7e894-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="7e894-107">Det er ideelt at konfigurere variantgrupper for forskellige produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="7e894-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="7e894-108">Der kan f.eks. oprettes en størrelsesgruppe for t-shirts med størrelserne extra small, small, medium, large og extra large, eller der oprettes en farvegruppe for at medtage alle de tilgængelige farver for et produkt.</span><span class="sxs-lookup"><span data-stu-id="7e894-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="7e894-109">Variantgrupper skal tilføjes, før der tilføjes produkter.</span><span class="sxs-lookup"><span data-stu-id="7e894-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="7e894-110">I dette emne oprettes og konfigureres en størrelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="7e894-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="7e894-111">Lignende procedurer kan bruges til at tilføje og konfigurere typografigrupper og farvegrupper.</span><span class="sxs-lookup"><span data-stu-id="7e894-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="7e894-112">Oprette en størrelsesgruppe</span><span class="sxs-lookup"><span data-stu-id="7e894-112">Create a size group</span></span>

<span data-ttu-id="7e894-113">Du kan oprette størrelsesgruppe ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7e894-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="7e894-114">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="7e894-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="7e894-115">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7e894-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7e894-116">Angiv et navn til størrelsesgruppen i feltet **Størrelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="7e894-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="7e894-117">Angiv eventuelt en passende beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7e894-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="7e894-118">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7e894-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="7e894-119">Føje attributter til størrelsesgruppen</span><span class="sxs-lookup"><span data-stu-id="7e894-119">Add attributes to the size group</span></span>

<span data-ttu-id="7e894-120">Følg disse trin for at føje attributter til en størrelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="7e894-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="7e894-121">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Variantgrupper \> Størrelsesgrupper** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="7e894-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="7e894-122">Vælg en størrelsesgruppe i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="7e894-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="7e894-123">Vælg **Tilføj** under **Størrelsesgruppelinjer** .</span><span class="sxs-lookup"><span data-stu-id="7e894-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="7e894-124">Angiv en streng, der repræsenterer størrelsen (f.eks. "XL"), i feltet **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="7e894-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="7e894-125">Angiv et navn til størrelsen (f.eks. "Extra Large") i feltet **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="7e894-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="7e894-126">Angiv et nummer, der repræsenterer genopfyldningsvægten, i feltet **Genopfyldningsvægt**.</span><span class="sxs-lookup"><span data-stu-id="7e894-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="7e894-127">Angiv et nummer, der repræsenterer stregkoden, i feltet **Nummer i stregkode**.</span><span class="sxs-lookup"><span data-stu-id="7e894-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="7e894-128">Angiv et nummer, der repræsenterer visningsrækkefølgen, i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="7e894-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="7e894-129">Vælg **Gem** i handlingsruden, når du er færdig med at tilføje størrelser.</span><span class="sxs-lookup"><span data-stu-id="7e894-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="7e894-130">Følgende billede viser et eksempel på en størrelsesgruppe til "størrelser på fritids-t-shirt".</span><span class="sxs-lookup"><span data-stu-id="7e894-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Oprette størrelsesgruppe](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="7e894-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7e894-132">Additional resources</span></span>

[<span data-ttu-id="7e894-133">Oversigt over produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="7e894-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7e894-134">Konfigurere detailprodukter</span><span class="sxs-lookup"><span data-stu-id="7e894-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="7e894-135">Produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="7e894-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
