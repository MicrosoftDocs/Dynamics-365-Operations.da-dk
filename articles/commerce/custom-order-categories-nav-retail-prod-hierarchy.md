---
title: Ændre sorteringsrækkefølgen for merchandisingenheder
description: I dette emne forklares de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 67807c53a6ffc6dd09cc6f0e48218e2ee2de559f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207769"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="be331-103">Ændre sorteringsrækkefølgen for merchandisingenheder</span><span class="sxs-lookup"><span data-stu-id="be331-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="be331-104">Detailhandlere regner produktopdagelse for et primært værktøj til kundeinteraktion på tværs af alle kanaler.</span><span class="sxs-lookup"><span data-stu-id="be331-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="be331-105">Forskellige funktioner kan hjælpe kunderne med at finde produkter på en nem måde.</span><span class="sxs-lookup"><span data-stu-id="be331-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="be331-106">De kan f.eks. gennemse kategorier, søge og filtrere.</span><span class="sxs-lookup"><span data-stu-id="be331-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="be331-107">I dette emne forklares de begreber, der er relateret til styring af visningsrækkefølgen for forskellige merchandising-relaterede enheder.</span><span class="sxs-lookup"><span data-stu-id="be331-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="be331-108">Det forklarer også, hvordan sorteringsrækkefølgen ændres.</span><span class="sxs-lookup"><span data-stu-id="be331-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="be331-109">Overblik</span><span class="sxs-lookup"><span data-stu-id="be331-109">Overview</span></span>

<span data-ttu-id="be331-110">Understøttelsen af sortering af forskellige merchandising-relaterede enheder er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="be331-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="be331-111">Denne understøttelse er nu bedre tilpasset eksisterende kundescenarier, der tidligere krævede udvidelser fra implementeringspartnere.</span><span class="sxs-lookup"><span data-stu-id="be331-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="be331-112">I versioner af Retail, der er ældre end version 10.0.5, var sorteringsrækkefølgen for kategorierne i navigationshierarkiet alfabetisk.</span><span class="sxs-lookup"><span data-stu-id="be331-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="be331-113">Den nye brugerdefinerede funktion til sorteringsrækkefølge gør det muligt for merchandising-chefer at konfigurere sorteringsrækkefølgen for forskellige merchandising-relaterede enheder på tværs af alle slutbrugerklienter.</span><span class="sxs-lookup"><span data-stu-id="be331-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="be331-114">Disse klienter omfatter hovedkontorer og callcentre.</span><span class="sxs-lookup"><span data-stu-id="be331-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="be331-115">Konfigurere visningsrækkefølgen for kategorier i produkthierarkiet</span><span class="sxs-lookup"><span data-stu-id="be331-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="be331-116">Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="be331-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="be331-117">Gå til **Detail og handel \> Produkter og kategorier \> Commerce-produkthierarki**.</span><span class="sxs-lookup"><span data-stu-id="be331-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="be331-118">Klik på **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="be331-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="be331-119">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="be331-119">Click **Edit**.</span></span>
4. <span data-ttu-id="be331-120">Udvid **ALL \> Action Sports** i træet.</span><span class="sxs-lookup"><span data-stu-id="be331-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="be331-121">Udvid **ALL \> Team Sports** i træet.</span><span class="sxs-lookup"><span data-stu-id="be331-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="be331-122">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="be331-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="be331-123">(Tallet kan være negativt).</span><span class="sxs-lookup"><span data-stu-id="be331-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="be331-124">Gentag trin 4 til 6 for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.</span><span class="sxs-lookup"><span data-stu-id="be331-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="be331-125">Visningsrækkefølgen for hierarkiet til kanalnavigation vil blive afspejlet i hovedkontoret for handelsprodukthierarkiet og frigivne produkter efter kategori.</span><span class="sxs-lookup"><span data-stu-id="be331-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Produkhierarki sorteret med negative værdier](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Frigivne produkter efter kategori sorteret på basis af produkthierarkiet](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="be331-128">Konfigurere visningsrækkefølgen for kategorier i navigationshierarki for kanal</span><span class="sxs-lookup"><span data-stu-id="be331-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="be331-129">Før du kan udføre denne procedure, skal demodata være installeret i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="be331-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="be331-130">Gå til **Retail og Commerce \> Produkter og kategorier \> Navigationskategorier for kanal**.</span><span class="sxs-lookup"><span data-stu-id="be331-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="be331-131">Vælg hierarkiet **Fashion navigation** på listen.</span><span class="sxs-lookup"><span data-stu-id="be331-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="be331-132">Klik på **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="be331-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="be331-133">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="be331-133">Click **Edit**.</span></span>
5. <span data-ttu-id="be331-134">Vælg **Fashion \> Womenswear \> Womens Shoes** i træet.</span><span class="sxs-lookup"><span data-stu-id="be331-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="be331-135">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="be331-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="be331-136">Vælg **Fashion \> Womenswear \> Tops** i træet.</span><span class="sxs-lookup"><span data-stu-id="be331-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="be331-137">På samme måde kan du definere sorteringsrækkefølgen for underkategorierne.</span><span class="sxs-lookup"><span data-stu-id="be331-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="be331-138">Vælg **Fashion \> Menswear \> Casual Shirts** i træet.</span><span class="sxs-lookup"><span data-stu-id="be331-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="be331-139">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="be331-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="be331-140">Vælg **Fashion \> Menswear \> Coats & Jackets** i træet.</span><span class="sxs-lookup"><span data-stu-id="be331-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="be331-141">Angiv et tal i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="be331-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="be331-142">Gentag for eventuelle yderligere kategorier, du vil ændre rækkefølgen af.</span><span class="sxs-lookup"><span data-stu-id="be331-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="be331-143">Visningsrækkefølgen i navigationshierarkiet for kanal afspejles i hovedkontoret, kataloget og kanaler.</span><span class="sxs-lookup"><span data-stu-id="be331-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Brugersorteret navigationshierarki for kanal](./media/ChannelNavCustomSorted.png)

![Brugersorteret navigationshierarki for kanal baseret på kanalnavigationshierarkiet](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS med brugerdefinerede sorterede kategorier](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="be331-147">Funktionen for brugerdefineret sorteringsrækkefølge er som standard slået fra.</span><span class="sxs-lookup"><span data-stu-id="be331-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="be331-148">Du kan få mere at vide om, hvordan du aktiverer denne og andre funktioner, under [Administration af funktioner](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="be331-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]