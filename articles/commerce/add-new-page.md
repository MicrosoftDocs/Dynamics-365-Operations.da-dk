---
title: Tilføje en ny webstedsside
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer en ny side på et websted i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1993e58108ad73aad4adf382bb03ec2e62231add
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945599"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="22b9b-103">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="22b9b-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="22b9b-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer en ny side på et websted i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22b9b-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="22b9b-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="22b9b-105">Overview</span></span>

<span data-ttu-id="22b9b-106">Når du har oprettet skabeloner og fragmenter til dit websted, er næste trin at starte med at oprette sider, der bruger dem.</span><span class="sxs-lookup"><span data-stu-id="22b9b-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="22b9b-107">For at komme i gang skal du vælge en skabelon eller et layout, et sidenavn og en side-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="22b9b-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="22b9b-108">Skabelon eller layout</span><span class="sxs-lookup"><span data-stu-id="22b9b-108">Template or layout</span></span>

<span data-ttu-id="22b9b-109">Du kan enten bruge en skabelon eller et layout til din nye side.</span><span class="sxs-lookup"><span data-stu-id="22b9b-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="22b9b-110">Du kan finde flere oplysninger under [Oversigt over skabeloner og layout](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22b9b-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="22b9b-111">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="22b9b-111">Page name</span></span>

<span data-ttu-id="22b9b-112">Sidenavnet skal være entydigt for din side.</span><span class="sxs-lookup"><span data-stu-id="22b9b-112">The page name must be unique to your page.</span></span> <span data-ttu-id="22b9b-113">Det skal være beskrivende, så du nemt kan finde siden, og så andre personer ved, hvad formålet med siden er.</span><span class="sxs-lookup"><span data-stu-id="22b9b-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="22b9b-114">Vælg sidenavnet med omhu, da det ikke kan ændres senere.</span><span class="sxs-lookup"><span data-stu-id="22b9b-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="22b9b-115">Sidens URL-adresse</span><span class="sxs-lookup"><span data-stu-id="22b9b-115">Page URL</span></span>

<span data-ttu-id="22b9b-116">Du kan vælge at angive en URL-adresse til den nye side.</span><span class="sxs-lookup"><span data-stu-id="22b9b-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="22b9b-117">Når du opretter en side, kan du angive en streng, der bruges til at danne en komplet URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="22b9b-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="22b9b-118">Denne streng kaldes også en relativ URL-adresse eller en URL-slug.</span><span class="sxs-lookup"><span data-stu-id="22b9b-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="22b9b-119">Der genereres derefter en komplet URL-adresse ud fra URL-sluggen, og den nye side tildeles til den.</span><span class="sxs-lookup"><span data-stu-id="22b9b-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="22b9b-120">Du kan ændre URL-sluggen senere, før du publicerer siden.</span><span class="sxs-lookup"><span data-stu-id="22b9b-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="22b9b-121">Du kan finde flere oplysninger i [Oprette en side-URL](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="22b9b-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="22b9b-122">Dynamics 365 Commerce frakobler URL-adresser og indhold.</span><span class="sxs-lookup"><span data-stu-id="22b9b-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="22b9b-123">Med andre ord kan der oprettes en side, der ikke er knyttet til en URL-adresse, og der kan oprettes en URL-adresse, som ikke er knyttet til en side.</span><span class="sxs-lookup"><span data-stu-id="22b9b-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="22b9b-124">Derfor kan der foretages indholdsswapping for en URL-adresse, uden at det kræver nedetid, og omdirigeringer er nemmere at administrere.</span><span class="sxs-lookup"><span data-stu-id="22b9b-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="22b9b-125">Tilføje en ny side</span><span class="sxs-lookup"><span data-stu-id="22b9b-125">Add a new page</span></span>

<span data-ttu-id="22b9b-126">Hvis du vil føje en ny side til dit websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="22b9b-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="22b9b-127">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="22b9b-128">Vælg **Ny side**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-128">Select **New Page**.</span></span>
1. <span data-ttu-id="22b9b-129">I dialogboksen **Ny side** skal du vælge en skabelon og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="22b9b-130">I feltet **Sidenavn** skal du indtaste et sidenavn (f.eks. **Min nye side**).</span><span class="sxs-lookup"><span data-stu-id="22b9b-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="22b9b-131">I feltet **URL-adresse** skal du indtaste en streng (URL-slug) for at fuldføre URL-adressen (f.eks. **minnyeside**).</span><span class="sxs-lookup"><span data-stu-id="22b9b-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="22b9b-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-132">Select **OK**.</span></span> <span data-ttu-id="22b9b-133">Sideeditoren vises.</span><span class="sxs-lookup"><span data-stu-id="22b9b-133">The page editor appears.</span></span> <span data-ttu-id="22b9b-134">Bemærk, at der automatisk føjes et sidehoved og en sidefod til siden baseret på den skabelon, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="22b9b-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="22b9b-135">Vælg pladsen **Hoved** i sidedispositionen, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="22b9b-136">Vælg **Container**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="22b9b-137">Vælg **Flydende container**, vælg ellipseknappen, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="22b9b-138">Vælg **Indholdsrig blok**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="22b9b-139">Vælg **Indholdsrig blok**, vælg ellipseknappen, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="22b9b-140">Vælg **Element for indholdsrig blok**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="22b9b-141">I egenskabsruden til højre skal du vælge **Afsnit**og derefter angive **Min testtekst** i feltet.</span><span class="sxs-lookup"><span data-stu-id="22b9b-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="22b9b-142">Vælg **Gem**, og vælg derefter **Tjek ind**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="22b9b-143">Angiv **Tilføjet ny side** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="22b9b-144">Vælg **Eksempel** for at få vist din side.</span><span class="sxs-lookup"><span data-stu-id="22b9b-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="22b9b-145">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="22b9b-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="22b9b-146">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-146">Select **Publish**.</span></span>
1. <span data-ttu-id="22b9b-147">Vælg **Fabrikam** (eller navnet på dit websted) i navigationsstien (brødkrummer).</span><span class="sxs-lookup"><span data-stu-id="22b9b-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="22b9b-148">Vælg **URL-adresser** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="22b9b-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="22b9b-149">Find og vælg din URL-adresse (**minnyeside**) på listen.</span><span class="sxs-lookup"><span data-stu-id="22b9b-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="22b9b-150">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="22b9b-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22b9b-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="22b9b-151">Additional resources</span></span>

[<span data-ttu-id="22b9b-152">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="22b9b-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="22b9b-153">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="22b9b-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="22b9b-154">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="22b9b-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="22b9b-155">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="22b9b-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="22b9b-156">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="22b9b-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="22b9b-157">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="22b9b-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="22b9b-158">Bekræft tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="22b9b-158">Verify page content accessibility</span></span>](verify-accessibility.md)
