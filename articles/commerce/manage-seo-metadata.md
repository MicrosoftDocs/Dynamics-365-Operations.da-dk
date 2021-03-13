---
title: Administrere SEO-metadata
description: I dette emne beskrives, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c7cf9e76ffb30ee5c8bba318b2644e67c757bff0
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097409"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="6e5af-103">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="6e5af-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6e5af-104">I dette emne beskrives, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e5af-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e5af-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="6e5af-105">Overview</span></span>

<span data-ttu-id="6e5af-106">SEO-metadata for et websted kan administreres ved hjælp af webstedsoversigter og sidemetadata.</span><span class="sxs-lookup"><span data-stu-id="6e5af-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="6e5af-107">Webstedsoversigter</span><span class="sxs-lookup"><span data-stu-id="6e5af-107">Site maps</span></span>

<span data-ttu-id="6e5af-108">En webstedsoversigt er en maskinlæsbar liste i XML-format over siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="6e5af-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="6e5af-109">Det er meningen, at den skal forbruges af søgemaskiner, så de kan give bedre søgeresultater fra dit websted.</span><span class="sxs-lookup"><span data-stu-id="6e5af-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="6e5af-110">Webstedsoversigter kan bruges manuelt af søgemaskiner eller publiceres i en robots.txt-fil.</span><span class="sxs-lookup"><span data-stu-id="6e5af-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="6e5af-111">Dynamics 365 Commerce understøtter automatisk generering af webstedsoversigter.</span><span class="sxs-lookup"><span data-stu-id="6e5af-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="6e5af-112">Webstedoversigter opdateres automatisk, når sider publiceres og annulleres.</span><span class="sxs-lookup"><span data-stu-id="6e5af-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="6e5af-113">Aktivere generering af webstedsoversigt</span><span class="sxs-lookup"><span data-stu-id="6e5af-113">Turn on site map generation</span></span>

1. <span data-ttu-id="6e5af-114">Log på værktøjet til oprettelse af websider.</span><span class="sxs-lookup"><span data-stu-id="6e5af-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="6e5af-115">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="6e5af-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="6e5af-116">Vælg **Administration af websted** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="6e5af-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="6e5af-117">Kontroller, at indstillingen **Oversigter over websted er aktiveret** er slået til.</span><span class="sxs-lookup"><span data-stu-id="6e5af-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="6e5af-118">Sidemetadata</span><span class="sxs-lookup"><span data-stu-id="6e5af-118">Page metadata</span></span>

<span data-ttu-id="6e5af-119">Med Dynamics 365 Commerce kan du administrere SEO-metadata for individuelle sider.</span><span class="sxs-lookup"><span data-stu-id="6e5af-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="6e5af-120">Du kan få vist og redigere disse oplysninger i sektionen **SEO-egenskaber** i en sidecontainer.</span><span class="sxs-lookup"><span data-stu-id="6e5af-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="6e5af-121">Følgende egenskaber for SEO-metadata understøttes:</span><span class="sxs-lookup"><span data-stu-id="6e5af-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="6e5af-122">Stilling</span><span class="sxs-lookup"><span data-stu-id="6e5af-122">Title</span></span>
- <span data-ttu-id="6e5af-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6e5af-123">Description</span></span>
- <span data-ttu-id="6e5af-124">SEO-nøgleord</span><span class="sxs-lookup"><span data-stu-id="6e5af-124">SEO keywords</span></span>
- <span data-ttu-id="6e5af-125">Aria-labels</span><span class="sxs-lookup"><span data-stu-id="6e5af-125">Aria labels</span></span>
- <span data-ttu-id="6e5af-126">noindex</span><span class="sxs-lookup"><span data-stu-id="6e5af-126">noindex</span></span>
- <span data-ttu-id="6e5af-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="6e5af-127">nofollow</span></span>
- <span data-ttu-id="6e5af-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="6e5af-128">noarchive</span></span>
- <span data-ttu-id="6e5af-129">nocache</span><span class="sxs-lookup"><span data-stu-id="6e5af-129">nocache</span></span>
- <span data-ttu-id="6e5af-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="6e5af-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="6e5af-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="6e5af-131">nosnippet</span></span>
- <span data-ttu-id="6e5af-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="6e5af-132">noImageIndex</span></span>
- <span data-ttu-id="6e5af-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="6e5af-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="6e5af-134">Rediger sidemetadata</span><span class="sxs-lookup"><span data-stu-id="6e5af-134">Modify page metadata</span></span>

<span data-ttu-id="6e5af-135">Hvis du vil redigere sidemetadata, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="6e5af-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="6e5af-136">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="6e5af-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="6e5af-137">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="6e5af-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="6e5af-138">Vælg startsiden for at åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="6e5af-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="6e5af-139">Vælg **Rediger** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="6e5af-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="6e5af-140">Udvid **Standardmetatags** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="6e5af-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="6e5af-141">Hvis du vil tilføje en ny metatag, skal du vælge **Tilføj** og derefter angive den pågældende tag i feltet.</span><span class="sxs-lookup"><span data-stu-id="6e5af-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="6e5af-142">Hvis du vil fjerne en eksisterende metatag, skal du vælge skraldespandsymbolet til højre for den.</span><span class="sxs-lookup"><span data-stu-id="6e5af-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="6e5af-143">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="6e5af-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="6e5af-144">Angiv **Opdaterede metatags** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e5af-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="6e5af-145">Vælg **Eksempel** for at få vist din side.</span><span class="sxs-lookup"><span data-stu-id="6e5af-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="6e5af-146">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="6e5af-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="6e5af-147">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="6e5af-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e5af-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6e5af-148">Additional resources</span></span>

[<span data-ttu-id="6e5af-149">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="6e5af-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="6e5af-150">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="6e5af-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="6e5af-151">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="6e5af-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="6e5af-152">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="6e5af-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="6e5af-153">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="6e5af-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="6e5af-154">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="6e5af-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="6e5af-155">Bekræfte tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="6e5af-155">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="6e5af-156">Oprette dynamiske e-handelssider baseret på URL-parametre</span><span class="sxs-lookup"><span data-stu-id="6e5af-156">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
