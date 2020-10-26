---
title: Gemme, få vist og udgive en side
description: Dette emne beskriver, hvordan du gemmer, ser forhåndsvisning af og udgiver en side i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: db4866b22060b764fdde3e4a44e99e969133c0a0
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961604"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="cb5b3-103">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="cb5b3-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb5b3-104">Dette emne beskriver, hvordan du gemmer, ser forhåndsvisning af og udgiver en side i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="cb5b3-105">Gemme en side</span><span class="sxs-lookup"><span data-stu-id="cb5b3-105">Save a page</span></span>

<span data-ttu-id="cb5b3-106">Hvis du vil gemme en side, skal du selv have den tjekket ud til dig selv og åbnet den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="cb5b3-107">Vælg **Rediger** på kommandolinjen for at tjekke siden ud.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-107">To check out a page, select **Edit** on the command bar.</span></span> <span data-ttu-id="cb5b3-108">Du bør gemme den straks efter, at du har redigeret den, for at sikre, at ændringerne bevares.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-108">After you've finished editing a page, you should immediately save it to ensure that your changes are stored.</span></span>

<span data-ttu-id="cb5b3-109">Når du gemmer en side, er ændringerne kun synlige for dig.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-109">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="cb5b3-110">Gemmehandlingen er primært beregnet til at gemme ændringer, mens siden endnu ikke er klar til at blive tjekket ind.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-110">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="cb5b3-111">Når du er færdig med at redigere siden, anbefales du at tjekke den ind, så ændringerne bliver synlige for andre.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-111">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="cb5b3-112">På dette tidspunkt kan siden også være tjekket ud af andre brugere, der skal redigere den.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-112">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="cb5b3-113">Se forhåndsvisning af en side</span><span class="sxs-lookup"><span data-stu-id="cb5b3-113">Preview a page</span></span>

<span data-ttu-id="cb5b3-114">Oprettelsesværktøjet indeholder to slags funktioner til forhåndsvisning: den visuelle sidegenerator, som er en "what you see is what you get"-eksempelrude (WYSIWYG), og et separat eksempelvindue.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-114">The authoring tool offers two kinds of preview features: visual page builder, which is a "what you see is what you get" (WYSIWYG) preview pane in the page editor, and a separate preview window.</span></span>

<span data-ttu-id="cb5b3-115">Mens du bruger sideeditoren, er der en "what you see is what you get"-forhåndsvisning (WYSIWYG) i den midterste rude.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-115">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="cb5b3-116">Denne forhåndsvisning opdateres automatisk, hver gang du gemmer siden.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-116">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="cb5b3-117">Du kan også opdatere den manuelt ved at vælge **Opdater** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-117">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="cb5b3-118">I forhåndsvisningen gengives siden, som webstedets brugere kan se den, men hjælpefunktioner vises oven på den.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-118">The preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="cb5b3-119">Når du er færdig med at redigere siden, kan det være en god ide at se forhåndsvisningen for at se, hvad kunderne kan se.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-119">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="cb5b3-120">Hvis du vil se forhåndsvisningen, skal du vælge **Forhåndsvisning** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-120">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="cb5b3-121">Forhåndsvisningen åbnes i et separat browservindue.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-121">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="cb5b3-122">Siden i vinduet med forhåndsvisning gengives på samme måde, som webstedets bruger kan se den.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-122">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="cb5b3-123">Du kan ændre størrelsen på vinduet for at sikre, at dynamiske moduler gengives korrekt i alle visninger.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-123">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="cb5b3-124">Der kræves godkendelse og korrekte tilladelser for at se en forhåndsvisning af indhold, der ikke er udgivet.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-124">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="cb5b3-125">Hvis du derfor deler URL-adressen til forhåndsvisningen med en anden, skal den pågældende person have de relevante rettigheder for at få adgang til indholdet.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-125">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="cb5b3-126">Udgive en side</span><span class="sxs-lookup"><span data-stu-id="cb5b3-126">Publish a page</span></span>

<span data-ttu-id="cb5b3-127">Når siden er færdig, er næste trin at udgive den, så eksterne brugere kan få vist indholdet.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-127">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="cb5b3-128">Før du kan udgive en side, skal du tjekke den ind ved at vælge **Afslut redigering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-128">Before you can publish a page, you must check it in by selecting **Finish editing** on the command bar.</span></span>

<span data-ttu-id="cb5b3-129">Du kan udgive og annullere udgivelsen af sider fra enten sidefremviseren eller sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-129">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="cb5b3-130">Sideeditoren viser en liste over sider og tillader massehandlinger.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-130">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="cb5b3-131">Sideeditoren kan kun bruges til at udgive eller annullere udgivelsen af en enkelt side, der er åben i den.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-131">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="cb5b3-132">Hvis du vil udgive en eller flere sider fra sidefremviseren, skal du vælge siderne, kontrollere, at de er tjekket ind, og derefter vælge **Publicer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-132">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="cb5b3-133">Siderne udgives, og du modtager en besked om handlingen i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-133">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="cb5b3-134">Hvis du vil udgive en enkelt side fra sideeditoren, er proceduren den samme.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-134">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="cb5b3-135">Mens siden er åben i sideeditoren, skal du kontrollere, at den er tjekket ind, og derefter vælge **Publicer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-135">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="cb5b3-136">Siden udgives, og du modtager en besked om handlingen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-136">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="cb5b3-137">Når du udgiver en side, udgives kun sidens indhold.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-137">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="cb5b3-138">Du og andre brugere kan først gå til siden og se den, når der er knyttet en URL-adresse til den.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-138">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="cb5b3-139">URL-adressen skal udgives separat.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-139">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb5b3-140">Før du kan udgive en side, skal alle de billeder eller fragmenter, som siden refererer til, allerede være publiceret.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-140">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="cb5b3-141">Gemme, se forhåndsvisning af og udgive en startside</span><span class="sxs-lookup"><span data-stu-id="cb5b3-141">Save, preview, and publish a home page</span></span>

<span data-ttu-id="cb5b3-142">Hvis du vil gemme, se forhåndsvisning af og udgive en startside, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-142">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="cb5b3-143">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-143">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="cb5b3-144">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-144">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="cb5b3-145">Find og vælg startsiden for at åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-145">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="cb5b3-146">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-146">Select **Edit**.</span></span>
1. <span data-ttu-id="cb5b3-147">Rediger siden efter behov.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-147">Modify the page as you require.</span></span>
1. <span data-ttu-id="cb5b3-148">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-148">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cb5b3-149">Brug feltet **Bemærkninger** til at skrive en note om de ændringer, du har foretaget, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-149">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="cb5b3-150">Vælg **Eksempel** for at få vist din side.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-150">Select **Preview** to preview your page.</span></span> <span data-ttu-id="cb5b3-151">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-151">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="cb5b3-152">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-152">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="cb5b3-153">Publicere en URL-adresse</span><span class="sxs-lookup"><span data-stu-id="cb5b3-153">Publish a URL</span></span>

<span data-ttu-id="cb5b3-154">Følg disse trin for at publicere en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-154">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="cb5b3-155">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-155">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="cb5b3-156">Vælg **URL-adresser** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-156">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="cb5b3-157">Find og vælg den URL-adresse, der skal publiceres.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-157">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="cb5b3-158">Vælg **Publicer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-158">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb5b3-159">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cb5b3-159">Additional resources</span></span>

[<span data-ttu-id="cb5b3-160">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="cb5b3-160">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="cb5b3-161">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="cb5b3-161">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cb5b3-162">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="cb5b3-162">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="cb5b3-163">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="cb5b3-163">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="cb5b3-164">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="cb5b3-164">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="cb5b3-165">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="cb5b3-165">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="cb5b3-166">Bekræft tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="cb5b3-166">Verify page content accessibility</span></span>](verify-accessibility.md)
