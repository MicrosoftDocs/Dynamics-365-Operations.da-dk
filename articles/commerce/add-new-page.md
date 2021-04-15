---
title: Tilføje en ny webstedsside
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer en ny side på et websted i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797545"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="8bcf7-103">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="8bcf7-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8bcf7-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer en ny side på et websted i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8bcf7-105">Når du har oprettet skabeloner og fragmenter til dit websted, er næste trin at starte med at oprette sider, der bruger dem.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="8bcf7-106">For at komme i gang skal du vælge en skabelon eller et layout, et sidenavn og en side-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="8bcf7-107">Skabelon eller layout</span><span class="sxs-lookup"><span data-stu-id="8bcf7-107">Template or layout</span></span>

<span data-ttu-id="8bcf7-108">Du kan enten bruge en skabelon eller et layout til din nye side.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="8bcf7-109">Du kan finde flere oplysninger under [Oversigt over skabeloner og layout](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8bcf7-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="8bcf7-110">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="8bcf7-110">Page name</span></span>

<span data-ttu-id="8bcf7-111">Sidenavnet skal være entydigt for din side.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-111">The page name must be unique to your page.</span></span> <span data-ttu-id="8bcf7-112">Det skal være beskrivende, så du nemt kan finde siden, og så andre personer ved, hvad formålet med siden er.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="8bcf7-113">Vælg sidenavnet med omhu, da det ikke kan ændres senere.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="8bcf7-114">Sidens URL-adresse</span><span class="sxs-lookup"><span data-stu-id="8bcf7-114">Page URL</span></span>

<span data-ttu-id="8bcf7-115">Du kan vælge at angive en URL-adresse til den nye side.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="8bcf7-116">Når du opretter en side, kan du angive en streng, der bruges til at danne en komplet URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="8bcf7-117">Denne streng kaldes også en relativ URL-adresse eller en URL-slug.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="8bcf7-118">Der genereres derefter en komplet URL-adresse ud fra URL-sluggen, og den nye side tildeles til den.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="8bcf7-119">Du kan ændre URL-sluggen senere, før du publicerer siden.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="8bcf7-120">Du kan finde flere oplysninger i [Oprette en side-URL](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="8bcf7-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8bcf7-121">Dynamics 365 Commerce frakobler URL-adresser og indhold.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="8bcf7-122">Med andre ord kan der oprettes en side, der ikke er knyttet til en URL-adresse, og der kan oprettes en URL-adresse, som ikke er knyttet til en side.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="8bcf7-123">Derfor kan der foretages indholdsswapping for en URL-adresse, uden at det kræver nedetid, og omdirigeringer er nemmere at administrere.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="8bcf7-124">Tilføje en ny side</span><span class="sxs-lookup"><span data-stu-id="8bcf7-124">Add a new page</span></span>

<span data-ttu-id="8bcf7-125">Hvis du vil føje en ny side til dit websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="8bcf7-126">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8bcf7-127">Vælg **Ny side**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-127">Select **New Page**.</span></span>
1. <span data-ttu-id="8bcf7-128">I dialogboksen **Ny side** skal du vælge en skabelon og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="8bcf7-129">I feltet **Sidenavn** skal du indtaste et sidenavn (f.eks. **Min nye side**).</span><span class="sxs-lookup"><span data-stu-id="8bcf7-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="8bcf7-130">I feltet **URL-adresse** skal du indtaste en streng (URL-slug) for at fuldføre URL-adressen (f.eks. **minnyeside**).</span><span class="sxs-lookup"><span data-stu-id="8bcf7-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="8bcf7-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-131">Select **OK**.</span></span> <span data-ttu-id="8bcf7-132">Sideeditoren vises.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-132">The page editor appears.</span></span> <span data-ttu-id="8bcf7-133">Bemærk, at der automatisk føjes et sidehoved og en sidefod til siden baseret på den skabelon, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="8bcf7-134">Vælg pladsen **Hoved** i sidedispositionen, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8bcf7-135">Vælg **Container**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="8bcf7-136">Vælg **Flydende container**, vælg ellipseknappen, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8bcf7-137">Vælg **Indholdsrig blok**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="8bcf7-138">Vælg **Indholdsrig blok**, vælg ellipseknappen, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8bcf7-139">Vælg **Element for indholdsrig blok**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="8bcf7-140">I egenskabsruden til højre skal du vælge **Afsnit** og derefter angive **Min testtekst** i feltet.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="8bcf7-141">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8bcf7-142">Angiv **Tilføjet ny side** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="8bcf7-143">Vælg **Eksempel** for at få vist din side.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="8bcf7-144">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="8bcf7-145">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-145">Select **Publish**.</span></span>
1. <span data-ttu-id="8bcf7-146">Vælg **Fabrikam** (eller navnet på dit websted) i navigationsstien (brødkrummer).</span><span class="sxs-lookup"><span data-stu-id="8bcf7-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8bcf7-147">Vælg **URL-adresser** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="8bcf7-148">Find og vælg din URL-adresse (**minnyeside**) på listen.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="8bcf7-149">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8bcf7-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8bcf7-150">Additional resources</span></span>

[<span data-ttu-id="8bcf7-151">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="8bcf7-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="8bcf7-152">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="8bcf7-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8bcf7-153">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="8bcf7-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="8bcf7-154">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="8bcf7-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8bcf7-155">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="8bcf7-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="8bcf7-156">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="8bcf7-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="8bcf7-157">Bekræfte tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="8bcf7-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="8bcf7-158">Oprette dynamiske e-handelssider baseret på URL-parametre</span><span class="sxs-lookup"><span data-stu-id="8bcf7-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
