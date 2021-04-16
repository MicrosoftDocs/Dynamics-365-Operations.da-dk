---
title: Modul til søgeresultater
description: Dette emne omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3409e9e99329def55b173eb78cf03db4a6764c92
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794109"
---
# <a name="search-results-module"></a><span data-ttu-id="9e7ba-103">Modul til søgeresultater</span><span class="sxs-lookup"><span data-stu-id="9e7ba-103">Search results module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e7ba-104">Dette emne omhandler søgeresultater-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9e7ba-105">I modulet med søgeresultater returneres resultaterne af produktsøgningen og en liste over relevante forfinere for produkterne.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="9e7ba-106">Du kan bruge Dynamics 365 Commerce-søgeresultatmoduler på websteder til at vise sider i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="9e7ba-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="9e7ba-107">Søgeresultater, der er startet af en brugersøgning</span><span class="sxs-lookup"><span data-stu-id="9e7ba-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="9e7ba-108">Søgeresultater, der viser et bestemt sæt produkter, f.eks. "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="9e7ba-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="9e7ba-109">Lister over produkter, der tilhører en given kategori</span><span class="sxs-lookup"><span data-stu-id="9e7ba-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="9e7ba-110">Yderligere oplysninger om arts- og søgeresultatsider finder du i [oversigtsoversigten over Standardkategorilandingsside og søgeresultater](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9e7ba-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="9e7ba-111">I følgende illustration vises et eksempel på et søge resultater-side for kategori på Fabrikam-webstedet.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Eksempel på en søgeresultatside på Fabrikam-webstedet](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="9e7ba-113">Modulegenskaber til søgeresultater</span><span class="sxs-lookup"><span data-stu-id="9e7ba-113">Search results module properties</span></span>

<span data-ttu-id="9e7ba-114">Følgende tabel indeholder egenskaberne for søgeresultatmoduler sammen med deres værdier og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="9e7ba-115">Egenskab</span><span class="sxs-lookup"><span data-stu-id="9e7ba-115">Property</span></span> | <span data-ttu-id="9e7ba-116">Værdier</span><span class="sxs-lookup"><span data-stu-id="9e7ba-116">Values</span></span> | <span data-ttu-id="9e7ba-117">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9e7ba-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="9e7ba-118">Elementer pr. side</span><span class="sxs-lookup"><span data-stu-id="9e7ba-118">Items per page</span></span> | <span data-ttu-id="9e7ba-119">Heltal</span><span class="sxs-lookup"><span data-stu-id="9e7ba-119">Integer</span></span> | <span data-ttu-id="9e7ba-120">Det antal elementer, der skal vises på hver side.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="9e7ba-121">Tillad at gå tilbage til PDP</span><span class="sxs-lookup"><span data-stu-id="9e7ba-121">Allow back on PDP</span></span> | <span data-ttu-id="9e7ba-122">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e7ba-122">**True** or **False**</span></span> | <span data-ttu-id="9e7ba-123">Hvis denne egenskab er angivet til **Sand**, når en bruger vælger et produkt på siden med søgeresultater, vil den navigation på produktdetaljerne (PDP), der åbnes, vise linket "Tilbage til resultater".</span><span class="sxs-lookup"><span data-stu-id="9e7ba-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="9e7ba-124">Udvid afgrænsninger</span><span class="sxs-lookup"><span data-stu-id="9e7ba-124">Expand Refiners</span></span> | <span data-ttu-id="9e7ba-125">**Alle**, **1**, **2**, **3** eller **4**</span><span class="sxs-lookup"><span data-stu-id="9e7ba-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="9e7ba-126">Det antal af de øverste afgrænsningerne, der skal udvides, når en side indlæses.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="9e7ba-127">Hvis denne egenskab f.eks. er angivet til **3**, udvides de første tre afgrænsninger på siden.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="9e7ba-128">Skjul visning af kategorihierarki</span><span class="sxs-lookup"><span data-stu-id="9e7ba-128">Hide category hierarchy display</span></span> | <span data-ttu-id="9e7ba-129">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e7ba-129">**True** or **False**</span></span> | <span data-ttu-id="9e7ba-130">Hvis denne egenskab er angivet til **Sand**, vil visningen af kategorihierarkiet på siden være skjult.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="9e7ba-131">Denne egenskab skal angives til **Sand**, hvis du bruger [modulet brødkrumme](add-breadcrumb.md) til at få vist kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="9e7ba-132">Inkluder produktattributter i søgeresultater</span><span class="sxs-lookup"><span data-stu-id="9e7ba-132">Include product attributes in search results</span></span> | <span data-ttu-id="9e7ba-133">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e7ba-133">**True** or **False**</span></span> | <span data-ttu-id="9e7ba-134">Hvis denne egenskab er angivet til **Sand**, returneres attributter for produkterne i søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="9e7ba-135">Selvom disse attributter kan vises på et handelswebsted, skal der angives en filtype.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="9e7ba-136">Vis tilknytningspriser</span><span class="sxs-lookup"><span data-stu-id="9e7ba-136">Show affiliation prices</span></span> | <span data-ttu-id="9e7ba-137">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e7ba-137">**True** or **False**</span></span> | <span data-ttu-id="9e7ba-138">Hvis denne egenskab er angivet til **Sand**, vises tilknytningspriserne for produkter i søgeresultaterne, når en bruger, der er logget på, gennemser siden.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="9e7ba-139">I versionen Dynamics 365 Commerce 10.0.16 og senere kan konfigurationen **Vis tilknytningspriser** bruges til at vise tilknytningspriser på siden.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="9e7ba-140">Understøttede moduler</span><span class="sxs-lookup"><span data-stu-id="9e7ba-140">Supported modules</span></span>

<span data-ttu-id="9e7ba-141">Modulet søgeresultater understøtter [modulet Hurtig visning](quick-view-module.md), som giver brugerne mulighed for at få vist produktoplysninger og føje varer til indkøbsvognen fra en søgeresultater-side.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="9e7ba-142">Føje et modul med søgeresultater til en kategoriside</span><span class="sxs-lookup"><span data-stu-id="9e7ba-142">Add a search results module to a category page</span></span>

<span data-ttu-id="9e7ba-143">Hvis du vil tilføje et søgeresultater-modul til en kategoriside, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="9e7ba-144">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="9e7ba-145">Angiv **Nu skabelon** i dialogboksen, angiv navnet **Søgeresultater**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="9e7ba-146">På pladsen **Brødtekst** skal du vælge ellipsen (...) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9e7ba-147">dI dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9e7ba-148">På pladsen **Hoved** i modulet **Standardside** skal du vælge ellipsen (...) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9e7ba-149">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9e7ba-150">På pladsen **Container** skal du vælge ellipsen (...) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9e7ba-151">I dialogboksen **Tilføj modul** skal du vælge modulet **Brødkrumme** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9e7ba-152">Angiv værdien **1** for **Min. indtræffer** i ruden **Brødkrumme**-egenskaber.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="9e7ba-153">På pladsen **Container** skal du vælge ellipsen (...) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9e7ba-154">I dialogboksen **Tilføj modul** skal du vælge modulet **Søgeresultater** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9e7ba-155">I ruden **Søgeresultater**-egenskaber skal du angive værdien **1** for **Min. indtræffer**, og derefter angive eventuelle andre nødvendige egenskaber for søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="9e7ba-156">Når du angiver disse egenskaber i skabelonen, sikrer du, at eventuelle tilpasninger af en bestemt kategoriside automatisk medtager disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="9e7ba-157">Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere skabelonen.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="9e7ba-158">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="9e7ba-159">I dialogboksen **Vælg en skabelon** skal du vælge den **Søgeresultater**-skabelon, du har oprettet, angive **Kategoriside** for **Sidenavn** og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="9e7ba-160">Da alle værdier er angivet i skabelonen, er siden klar til at blive publiceret.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="9e7ba-161">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="9e7ba-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e7ba-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9e7ba-162">Additional resources</span></span>

[<span data-ttu-id="9e7ba-163">Oversigt over standardlandingsside for kategori og side for søgeresultater</span><span class="sxs-lookup"><span data-stu-id="9e7ba-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="9e7ba-164">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="9e7ba-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9e7ba-165">Hurtig visning-.modul</span><span class="sxs-lookup"><span data-stu-id="9e7ba-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
