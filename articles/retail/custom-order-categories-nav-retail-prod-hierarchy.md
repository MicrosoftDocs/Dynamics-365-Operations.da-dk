---
title: Ændre sorteringsrækkefølgen for merchandisingenheder
description: I dette emne forklares de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder i Microsoft Dynamics 365 for Retail.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866155"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="b21d5-103">Ændre sorteringsrækkefølgen for merchandisingenheder</span><span class="sxs-lookup"><span data-stu-id="b21d5-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b21d5-104">Detailhandlere regner produktopdagelse for et primært værktøj til kundeinteraktion på tværs af alle detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="b21d5-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="b21d5-105">Forskellige funktioner kan hjælpe kunderne med at finde produkter på en nem måde.</span><span class="sxs-lookup"><span data-stu-id="b21d5-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="b21d5-106">De kan f.eks. gennemse kategorier, søge og filtrere.</span><span class="sxs-lookup"><span data-stu-id="b21d5-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="b21d5-107">I dette emne forklares de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder.</span><span class="sxs-lookup"><span data-stu-id="b21d5-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="b21d5-108">Det forklarer også, hvordan sorteringsrækkefølgen ændres.</span><span class="sxs-lookup"><span data-stu-id="b21d5-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="b21d5-109">Overblik</span><span class="sxs-lookup"><span data-stu-id="b21d5-109">Overview</span></span>

<span data-ttu-id="b21d5-110">Understøttelsen af sortering af forskellige merchandising-relaterede enheder er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="b21d5-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="b21d5-111">Denne understøttelse er nu bedre tilpasset eksisterende kundescenarier, der tidligere krævede udvidelser fra implementeringspartnere.</span><span class="sxs-lookup"><span data-stu-id="b21d5-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="b21d5-112">I versioner af Microsoft Dynamics 365 for Retail, der er ældre end version 10.0.5, var sorteringsrækkefølgen for kategorierne i navigationshierarkiet alfabetisk.</span><span class="sxs-lookup"><span data-stu-id="b21d5-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="b21d5-113">Den nye brugerdefinerede funktion til sorteringsrækkefølge gør det muligt for merchandising-chefer at konfigurere sorteringsrækkefølgen for forskellige merchandising-relaterede enheder på tværs af alle slutbrugerklienter.</span><span class="sxs-lookup"><span data-stu-id="b21d5-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="b21d5-114">Disse klienter omfatter hovedkontorer og callcentre.</span><span class="sxs-lookup"><span data-stu-id="b21d5-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="b21d5-115">Konfigurere visningsrækkefølgen for kategorier i detailprodukthierarkiet</span><span class="sxs-lookup"><span data-stu-id="b21d5-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="b21d5-116">Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="b21d5-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="b21d5-117">Gå til **Retail \> Produkter og kategorier \> Detailprodukthierarki**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="b21d5-118">Klik på **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="b21d5-119">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-119">Click **Edit**.</span></span>
4. <span data-ttu-id="b21d5-120">Udvid **ALL \> Action Sports** i træet.</span><span class="sxs-lookup"><span data-stu-id="b21d5-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="b21d5-121">Udvid **ALL \> Team Sports** i træet.</span><span class="sxs-lookup"><span data-stu-id="b21d5-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="b21d5-122">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="b21d5-123">(Tallet kan være negativt).</span><span class="sxs-lookup"><span data-stu-id="b21d5-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="b21d5-124">Gentag trin 4 til 6 for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.</span><span class="sxs-lookup"><span data-stu-id="b21d5-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="b21d5-125">Visningsrækkefølgen for hierarkiet til kanalnavigation vil blive afspejlet i hovedkontoret for detailprodukthierarkiet og frigivne produkter efter kategori.</span><span class="sxs-lookup"><span data-stu-id="b21d5-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![Detailprodukthierarki sorteret med negative værdier](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Frigivne produkter efter kategori sorteret på basis af detailprodukthierarkiet](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="b21d5-128">Konfigurere visningsrækkefølgen for kategorier i navigationshierarki for kanal</span><span class="sxs-lookup"><span data-stu-id="b21d5-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="b21d5-129">Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="b21d5-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="b21d5-130">Gå til **Detail \> Produkter og kategorier \> Navigationskategorier for kanal**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="b21d5-131">Vælg hierarkiet **Fashion navigation** på listen.</span><span class="sxs-lookup"><span data-stu-id="b21d5-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="b21d5-132">Klik på **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="b21d5-133">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-133">Click **Edit**.</span></span>
5. <span data-ttu-id="b21d5-134">Vælg **Fashion \> Womenswear \> Womens Shoes** i træet.</span><span class="sxs-lookup"><span data-stu-id="b21d5-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="b21d5-135">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="b21d5-136">Vælg **Fashion \> Womenswear \> Tops** i træet.</span><span class="sxs-lookup"><span data-stu-id="b21d5-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="b21d5-137">På samme måde kan du definere sorteringsrækkefølgen for underkategorierne.</span><span class="sxs-lookup"><span data-stu-id="b21d5-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="b21d5-138">Vælg **Fashion \> Menswear \> Casual Shirts** i træet.</span><span class="sxs-lookup"><span data-stu-id="b21d5-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="b21d5-139">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="b21d5-140">Vælg **Fashion \> Menswear \> Coats & Jackets** i træet.</span><span class="sxs-lookup"><span data-stu-id="b21d5-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="b21d5-141">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="b21d5-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="b21d5-142">Gentag for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.</span><span class="sxs-lookup"><span data-stu-id="b21d5-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="b21d5-143">Visningsrækkefølgen i navigationshierarkiet for kanal afspejles i hovedkontoret, kataloget og detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="b21d5-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![Brugersorteret navigationshierarki for kanal](./media/ChannelNavCustomSorted.png)

![Brugersorteret navigationshierarki for kanal baseret på kanalnavigationshierarkiet](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS med brugerdefinerede sorterede kategorier](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="b21d5-147">Funktionen for brugerdefineret sorteringsrækkefølge er som standard slået fra.</span><span class="sxs-lookup"><span data-stu-id="b21d5-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="b21d5-148">Du kan få mere at vide om, hvordan du aktiverer denne og andre funktioner, under [Administration af funktioner](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="b21d5-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
