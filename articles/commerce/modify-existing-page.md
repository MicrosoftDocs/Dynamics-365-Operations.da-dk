---
title: Redigere en eksisterende webstedsside
description: Dette emne indeholder en beskrivelse af, hvordan du kan redigere en eksisterende webstedsside i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803723"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="d76ce-103">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="d76ce-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d76ce-104">Dette emne indeholder en beskrivelse af, hvordan du kan redigere en eksisterende webstedsside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d76ce-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d76ce-105">Når du skal redigere en side, skal du først åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="d76ce-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="d76ce-106">Gå til det websted, der indeholder siden, og søg derefter efter den ønskede side på listen over sider.</span><span class="sxs-lookup"><span data-stu-id="d76ce-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="d76ce-107">Hvis du ikke kan finde siden, kan du bruge funktionen til avanceret søgning i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="d76ce-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="d76ce-108">Skriv enten det præcise sidenavn, eller skriv de første par bogstaver i navnet og derefter en stjerne (\*).</span><span class="sxs-lookup"><span data-stu-id="d76ce-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="d76ce-109">Der vises en filtreret liste over sider.</span><span class="sxs-lookup"><span data-stu-id="d76ce-109">A filtered list of pages appears.</span></span> <span data-ttu-id="d76ce-110">Du kan bruge denne liste til at finde den ønskede side.</span><span class="sxs-lookup"><span data-stu-id="d76ce-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="d76ce-111">Når du har fundet siden, skal du vælge sidenavnet for at åbne siden i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="d76ce-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="d76ce-112">Hvis siden er synlig i sidefremviseren, kan du vælge **Rediger** og tjekke siden ud, før du åbner den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="d76ce-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="d76ce-113">På denne måde kan du checke flere sider ud på samme tid.</span><span class="sxs-lookup"><span data-stu-id="d76ce-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="d76ce-114">Når siden er åben i sideeditoren, skal du sørge for, at den er checket ud til dig.</span><span class="sxs-lookup"><span data-stu-id="d76ce-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="d76ce-115">Kommandolinjen i oprettelsesværktøjet er dynamisk, kontekstafhængig og tilstandsfølsom.</span><span class="sxs-lookup"><span data-stu-id="d76ce-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="d76ce-116">Derfor viser den kun de handlinger, du i øjeblikket kan udføre på siden.</span><span class="sxs-lookup"><span data-stu-id="d76ce-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="d76ce-117">Hvis siden f.eks. ikke er tjekket ud til dig, vises knapperne **Gem** og **Afslut redigering** ikke på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d76ce-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="d76ce-118">Sidetilstanden vises også i højre side af vinduet.</span><span class="sxs-lookup"><span data-stu-id="d76ce-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="d76ce-119">Hvis siden ikke allerede er tjekket ud til dig, skal du vælge **Rediger** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d76ce-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="d76ce-120">Kommandolinjen ændres, så den afspejler sidens nye tilstand.</span><span class="sxs-lookup"><span data-stu-id="d76ce-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="d76ce-121">Du modtager også en besked om, at siden blev checket ud til dig.</span><span class="sxs-lookup"><span data-stu-id="d76ce-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="d76ce-122">Det næste trin er at foretage de faktiske ændringer.</span><span class="sxs-lookup"><span data-stu-id="d76ce-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="d76ce-123">Du skal ofte bruge sidens dispositionstræ til venstre for at finde og vælge det modul, du vil ændre, og derefter foretage ændringer i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="d76ce-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="d76ce-124">Men ændringen kan undertiden omfatte tilføjelse eller fjernelse af modeller eller fragmenter.</span><span class="sxs-lookup"><span data-stu-id="d76ce-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="d76ce-125">Hvis du vil tilføje et fragment eller et modul, skal du bruge sidens dispositionstræ til at finde den plads, hvor du vil tilføje modulet eller fragmentet og derefter vælge ellipseknappen (**...**) for den pågældende plads.</span><span class="sxs-lookup"><span data-stu-id="d76ce-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="d76ce-126">Der vises en menu, der indeholder kommandoer til tilføjelse af et modul eller fragment.</span><span class="sxs-lookup"><span data-stu-id="d76ce-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="d76ce-127">Hvis du vil fjerne et modul eller fragment, skal du finde og markere det i sidedispositionstræet, vælge ellipseknappen og derefter vælge den kommando, der sletter modulet eller fragmentet.</span><span class="sxs-lookup"><span data-stu-id="d76ce-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="d76ce-128">Du kan også se og redigere egenskaberne for et modul, der er synligt i eksempelvisningen i den visuelle sidegenerator ved at vælge det direkte.</span><span class="sxs-lookup"><span data-stu-id="d76ce-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="d76ce-129">Når du er færdig med at foretage ændringer og se deres effekt, skal du tjekke siden ind ved at vælge **Afslut redigering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d76ce-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="d76ce-130">Vælg **Publicer** på kommandolinjen for at publicere dine ændringer med det samme.</span><span class="sxs-lookup"><span data-stu-id="d76ce-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="d76ce-131">Den senest indcheckede version af den side, du har ændret, publiceres og bliver tilgængelig for eksterne brugere, der går ind dit websted.</span><span class="sxs-lookup"><span data-stu-id="d76ce-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="d76ce-132">Eksempel: Ændre videoen på startsiden</span><span class="sxs-lookup"><span data-stu-id="d76ce-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="d76ce-133">I følgende eksempel vises, hvordan du kan ændre startsiden ved at ændre den video, der vises i videoafspillermodulet.</span><span class="sxs-lookup"><span data-stu-id="d76ce-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="d76ce-134">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="d76ce-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d76ce-135">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="d76ce-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="d76ce-136">Find og vælg startsiden for at åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="d76ce-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="d76ce-137">Vælg **Rediger** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d76ce-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="d76ce-138">Vælg **Hoved**-pladsen i sidedispositionen.</span><span class="sxs-lookup"><span data-stu-id="d76ce-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="d76ce-139">Udvid alle flydende containermoduler under **Hoved**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="d76ce-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="d76ce-140">Find og vælg videoafspillermodulet.</span><span class="sxs-lookup"><span data-stu-id="d76ce-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="d76ce-141">Vælg egenskaben **Video** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="d76ce-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="d76ce-142">Aktivvælgeren vises.</span><span class="sxs-lookup"><span data-stu-id="d76ce-142">The asset picker appears.</span></span>
1. <span data-ttu-id="d76ce-143">Vælg et tilgængeligt videoaktiv i aktivvælgeren, eller vælg **Upload nyt aktiv** for at overføre et nyt videoaktiv.</span><span class="sxs-lookup"><span data-stu-id="d76ce-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="d76ce-144">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d76ce-144">Select **OK**.</span></span>
1. <span data-ttu-id="d76ce-145">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="d76ce-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d76ce-146">Angiv **Ændrede videoen** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d76ce-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="d76ce-147">Vælg **Eksempel** for at få vist den opdaterede side.</span><span class="sxs-lookup"><span data-stu-id="d76ce-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="d76ce-148">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="d76ce-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="d76ce-149">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="d76ce-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d76ce-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d76ce-150">Additional resources</span></span>

[<span data-ttu-id="d76ce-151">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="d76ce-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d76ce-152">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="d76ce-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d76ce-153">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="d76ce-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d76ce-154">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="d76ce-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d76ce-155">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="d76ce-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d76ce-156">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="d76ce-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="d76ce-157">Bekræfte tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="d76ce-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="d76ce-158">Oprette dynamiske e-handelssider baseret på URL-parametre</span><span class="sxs-lookup"><span data-stu-id="d76ce-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
