---
title: Oprette dynamiske e-handelssider baseret på URL-parametre
description: Dette emne beskriver, hvordan du kan konfigurere en Microsoft Dynamics 365 Commerce-e-handelsside, der kan have dynamisk indhold baseret på URL-parametre.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098617"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="f726c-103">Oprette dynamiske e-handelssider baseret på URL-parametre</span><span class="sxs-lookup"><span data-stu-id="f726c-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f726c-104">Dette emne beskriver, hvordan du kan konfigurere en Microsoft Dynamics 365 Commerce-e-handelsside, der kan have dynamisk indhold baseret på URL-parametre.</span><span class="sxs-lookup"><span data-stu-id="f726c-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="f726c-105">En e-handelsside kan konfigureres til at have forskelligt indhold baseret på et segment i URL-stien.</span><span class="sxs-lookup"><span data-stu-id="f726c-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="f726c-106">Derfor kaldes siden for en dynamisk side.</span><span class="sxs-lookup"><span data-stu-id="f726c-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="f726c-107">Segmentet bruges som parameter til at hente sideindholdet.</span><span class="sxs-lookup"><span data-stu-id="f726c-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="f726c-108">Der oprettes f.eks. en side med navnet **blog\_-fremviser**, som er tilknyttet URL-adressen `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="f726c-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="f726c-109">Denne side kan derefter bruges til at vise forskelligt indhold baseret på det sidste segment i URL-stien.</span><span class="sxs-lookup"><span data-stu-id="f726c-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="f726c-110">Det sidste segment i URL-adressen er f.eks. `https://fabrikam.com/blog/article-1` **artikel-1**.</span><span class="sxs-lookup"><span data-stu-id="f726c-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="f726c-111">Separate brugerdefinerede sider, der tilsidesætter den dynamiske side, kan også tilknyttes segmenter i URL-stien.</span><span class="sxs-lookup"><span data-stu-id="f726c-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="f726c-112">Der oprettes f.eks. en side med navnet **blog\_-oversigt**, som er tilknyttet URL-adressen `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="f726c-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="f726c-113">Når der anmodes om denne URL-adresse, returneres den **blog\_oversigt**-side, der er knyttet til parameteren **/about-this-blog**, i stedet for **blog\_-fremviseren**.</span><span class="sxs-lookup"><span data-stu-id="f726c-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="f726c-114">Funktionerne til modtagelse, hentning og visning af dynamisk sideindhold implementeres ved hjælp af et brugerdefineret modul.</span><span class="sxs-lookup"><span data-stu-id="f726c-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="f726c-115">Du kan finde flere oplysninger i [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="f726c-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="f726c-116">Konfigurere en dynamisk e-handelsside</span><span class="sxs-lookup"><span data-stu-id="f726c-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="f726c-117">Hvis du vil konfigurere en dynamisk e-handelsside, skal du oprette den dynamiske side, oprette den grundlæggende URL-adresse og konfigurere ruten til den dynamiske side.</span><span class="sxs-lookup"><span data-stu-id="f726c-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="f726c-118">Opret den side, der kan vise dynamisk indhold</span><span class="sxs-lookup"><span data-stu-id="f726c-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="f726c-119">Hvis du vil oprette en side, der kan vise dynamisk indhold, skal du følge trinnene i [Tilføj en ny webstedsside](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="f726c-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="f726c-120">Den side, du opretter, kræver implementering af et modul, der bruger det sidste segment i URL-stien til at hente indhold fra en ekstern datakilde.</span><span class="sxs-lookup"><span data-stu-id="f726c-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="f726c-121">Yderligere oplysninger om brugerdefineret moduludvikling finder du i [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="f726c-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="f726c-122">Oprette basis-URL-adressen til den dynamiske side</span><span class="sxs-lookup"><span data-stu-id="f726c-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="f726c-123">Hvis du vil oprette basis-URL-adressen til den dynamiske side i Commerce Site Builder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f726c-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f726c-124">Gå til **URL**-adresser, og vælg **Ny \> Ny URL**-adresse.</span><span class="sxs-lookup"><span data-stu-id="f726c-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="f726c-125">I dialogboksen **Opret ny URL-adresse** vælges **Intern side**.</span><span class="sxs-lookup"><span data-stu-id="f726c-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="f726c-126">Angiv den **URL-sti**, der skal fungere som rod for den dynamiske side (i dette eksempel **/blog**).</span><span class="sxs-lookup"><span data-stu-id="f726c-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="f726c-127">Vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="f726c-127">Then select **Next**.</span></span>
1. <span data-ttu-id="f726c-128">I dialogboksen **Vælg en side** vælges den side, der blev oprettet som dynamisk side, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f726c-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="f726c-129">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="f726c-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="f726c-130">Konfigurere ruten til den dynamiske side</span><span class="sxs-lookup"><span data-stu-id="f726c-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="f726c-131">Hvis du vil konfigurere ruten til den dynamiske side i Commerce Site Builder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f726c-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f726c-132">Gå til **Webstedsindstillinger \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="f726c-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="f726c-133">Under **Parameteriserede URL-stier** skal du vælge **Tilføj** og derefter angive den URL-sti, du angav, da du oprettede URL-adressen (i dette eksempel, **/blog**).</span><span class="sxs-lookup"><span data-stu-id="f726c-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="f726c-134">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="f726c-134">Select **Save and publish**.</span></span>

<span data-ttu-id="f726c-135">Når ruten er konfigureret, returnerer alle anmodninger til den parameteriserede URL-sti den side, der er knyttet til URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="f726c-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="f726c-136">Hvis en anmodning indeholder et yderligere segment, returneres den tilknyttede side, og sideindholdet hentes ved hjælp af segmentet som parameter.</span><span class="sxs-lookup"><span data-stu-id="f726c-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="f726c-137">F.eks. vil `https://fabrikam.com/blog/article-1` returnere **blog\_oversigt**-siden, og sideindholdet vil blive hentet ved hjælp af parameteren **/article-1**.</span><span class="sxs-lookup"><span data-stu-id="f726c-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="f726c-138">Tilsidesætte en parameteriseret URL-adresse med en brugerdefineret side</span><span class="sxs-lookup"><span data-stu-id="f726c-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="f726c-139">Hvis du vil tilsidesætte en parameteriseret URL-adresse med en brugerdefineret side i Commerce Site Builder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f726c-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f726c-140">Gå til **URL**-adresser, og vælg **Ny \> Ny URL**-adresse.</span><span class="sxs-lookup"><span data-stu-id="f726c-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="f726c-141">I dialogboksen **Opret ny URL-adresse** vælges **Intern side**.</span><span class="sxs-lookup"><span data-stu-id="f726c-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="f726c-142">Under **URL-stien** skal du angive den sti, der indeholder det segment, der skal tilsidesættes (i dette eksempel **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="f726c-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="f726c-143">Vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="f726c-143">Then select **Next**.</span></span>
1. <span data-ttu-id="f726c-144">I dialogboksen **Vælg en side** vælges den brugerdefinerede side, og derefter vælges **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f726c-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="f726c-145">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="f726c-145">Select **Publish**.</span></span>
1. <span data-ttu-id="f726c-146">Hvis den brugerdefinerede side endnu ikke er publiceret, skal du gå til **Sider**, vælge den brugerdefinerede side og derefter vælge **Udgiv**.</span><span class="sxs-lookup"><span data-stu-id="f726c-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="f726c-147">Når den brugerdefinerede side er publiceret, vises den i stedet for den dynamiske side, der har parameteriseret indhold.</span><span class="sxs-lookup"><span data-stu-id="f726c-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f726c-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f726c-148">Additional resources</span></span>

[<span data-ttu-id="f726c-149">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="f726c-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="f726c-150">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="f726c-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f726c-151">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="f726c-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="f726c-152">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="f726c-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="f726c-153">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="f726c-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="f726c-154">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="f726c-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="f726c-155">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="f726c-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="f726c-156">Bekræfte tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="f726c-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="f726c-157">Udvidelsesmuligheder for onlinekanal</span><span class="sxs-lookup"><span data-stu-id="f726c-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
