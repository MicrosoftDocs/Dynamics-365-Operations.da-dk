---
title: Administrere SEO-metadata
description: I dette emne beskrives, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698343"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="b4f29-103">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="b4f29-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b4f29-104">I dette emne beskrives, hvordan du administrerer SEO-metadata (søgemaskineoptimering) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4f29-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4f29-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b4f29-105">Overview</span></span>

<span data-ttu-id="b4f29-106">SEO-metadata for et websted kan administreres ved hjælp af webstedsoversigter og sidemetadata.</span><span class="sxs-lookup"><span data-stu-id="b4f29-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="b4f29-107">Webstedsoversigter</span><span class="sxs-lookup"><span data-stu-id="b4f29-107">Site maps</span></span>

<span data-ttu-id="b4f29-108">En webstedsoversigt er en maskinlæsbar liste i XML-format over siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="b4f29-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="b4f29-109">Det er meningen, at den skal forbruges af søgemaskiner, så de kan give bedre søgeresultater fra dit websted.</span><span class="sxs-lookup"><span data-stu-id="b4f29-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="b4f29-110">Webstedsoversigter kan bruges manuelt af søgemaskiner eller publiceres i en robots.txt-fil.</span><span class="sxs-lookup"><span data-stu-id="b4f29-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="b4f29-111">Dynamics 365 Commerce understøtter automatisk generering af webstedsoversigter.</span><span class="sxs-lookup"><span data-stu-id="b4f29-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="b4f29-112">Webstedoversigter opdateres automatisk, når sider publiceres og annulleres.</span><span class="sxs-lookup"><span data-stu-id="b4f29-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="b4f29-113">Aktivere generering af webstedsoversigt</span><span class="sxs-lookup"><span data-stu-id="b4f29-113">Turn on site map generation</span></span>

1. <span data-ttu-id="b4f29-114">Log på værktøjet til oprettelse af websider.</span><span class="sxs-lookup"><span data-stu-id="b4f29-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="b4f29-115">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="b4f29-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b4f29-116">Vælg **Administration af websted** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="b4f29-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="b4f29-117">Kontroller, at indstillingen **Oversigter over websted er aktiveret** er slået til.</span><span class="sxs-lookup"><span data-stu-id="b4f29-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="b4f29-118">Sidemetadata</span><span class="sxs-lookup"><span data-stu-id="b4f29-118">Page metadata</span></span>

<span data-ttu-id="b4f29-119">Med Dynamics 365 Commerce kan du administrere SEO-metadata for individuelle sider.</span><span class="sxs-lookup"><span data-stu-id="b4f29-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="b4f29-120">Du kan få vist og redigere disse oplysninger i sektionen **SEO-egenskaber** i en sidecontainer.</span><span class="sxs-lookup"><span data-stu-id="b4f29-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="b4f29-121">Følgende egenskaber for SEO-metadata understøttes:</span><span class="sxs-lookup"><span data-stu-id="b4f29-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="b4f29-122">Stilling</span><span class="sxs-lookup"><span data-stu-id="b4f29-122">Title</span></span>
- <span data-ttu-id="b4f29-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b4f29-123">Description</span></span>
- <span data-ttu-id="b4f29-124">SEO-nøgleord</span><span class="sxs-lookup"><span data-stu-id="b4f29-124">SEO keywords</span></span>
- <span data-ttu-id="b4f29-125">Aria-labels</span><span class="sxs-lookup"><span data-stu-id="b4f29-125">Aria labels</span></span>
- <span data-ttu-id="b4f29-126">noindex</span><span class="sxs-lookup"><span data-stu-id="b4f29-126">noindex</span></span>
- <span data-ttu-id="b4f29-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="b4f29-127">nofollow</span></span>
- <span data-ttu-id="b4f29-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="b4f29-128">noarchive</span></span>
- <span data-ttu-id="b4f29-129">nocache</span><span class="sxs-lookup"><span data-stu-id="b4f29-129">nocache</span></span>
- <span data-ttu-id="b4f29-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="b4f29-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="b4f29-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="b4f29-131">nosnippet</span></span>
- <span data-ttu-id="b4f29-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="b4f29-132">noImageIndex</span></span>
- <span data-ttu-id="b4f29-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="b4f29-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="b4f29-134">Rediger sidemetadata</span><span class="sxs-lookup"><span data-stu-id="b4f29-134">Modify page metadata</span></span>

<span data-ttu-id="b4f29-135">Hvis du vil redigere sidemetadata, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b4f29-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="b4f29-136">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="b4f29-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b4f29-137">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="b4f29-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="b4f29-138">Vælg startsiden for at åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="b4f29-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="b4f29-139">Vælg **Check ud** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b4f29-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="b4f29-140">Udvid **Standardmetatags** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="b4f29-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="b4f29-141">Hvis du vil tilføje en ny metatag, skal du vælge **Tilføj** og derefter angive den pågældende tag i feltet.</span><span class="sxs-lookup"><span data-stu-id="b4f29-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="b4f29-142">Hvis du vil fjerne en eksisterende metatag, skal du vælge skraldespandsymbolet til højre for den.</span><span class="sxs-lookup"><span data-stu-id="b4f29-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="b4f29-143">Vælg **Gem**, og vælg derefter **Tjek ind**.</span><span class="sxs-lookup"><span data-stu-id="b4f29-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="b4f29-144">Angiv **Opdaterede metatags** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4f29-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="b4f29-145">Vælg **Eksempel** for at få vist din side.</span><span class="sxs-lookup"><span data-stu-id="b4f29-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="b4f29-146">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="b4f29-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="b4f29-147">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="b4f29-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4f29-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b4f29-148">Additional resources</span></span>

[<span data-ttu-id="b4f29-149">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="b4f29-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b4f29-150">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="b4f29-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b4f29-151">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="b4f29-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b4f29-152">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="b4f29-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b4f29-153">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="b4f29-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b4f29-154">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="b4f29-154">Enrich a category landing page</span></span>](enrich-category-page.md)

