---
title: Redigere en eksisterende webstedsside
description: Dette emne indeholder en beskrivelse af, hvordan du kan redigere en eksisterende webstedsside i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 8ca23dcf568cb0df6934f0d6201e4aafba5f9ba1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411160"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="cdb07-103">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="cdb07-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cdb07-104">Dette emne indeholder en beskrivelse af, hvordan du kan redigere en eksisterende webstedsside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cdb07-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cdb07-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="cdb07-105">Overview</span></span>

<span data-ttu-id="cdb07-106">Når du skal redigere en side, skal du først åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cdb07-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="cdb07-107">Gå til det websted, der indeholder siden, og søg derefter efter den ønskede side på listen over sider.</span><span class="sxs-lookup"><span data-stu-id="cdb07-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="cdb07-108">Hvis du ikke kan finde siden, kan du bruge funktionen til avanceret søgning i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="cdb07-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="cdb07-109">Skriv enten det præcise sidenavn, eller skriv de første par bogstaver i navnet og derefter en stjerne (\*).</span><span class="sxs-lookup"><span data-stu-id="cdb07-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="cdb07-110">Der vises en filtreret liste over sider.</span><span class="sxs-lookup"><span data-stu-id="cdb07-110">A filtered list of pages appears.</span></span> <span data-ttu-id="cdb07-111">Du kan bruge denne liste til at finde den ønskede side.</span><span class="sxs-lookup"><span data-stu-id="cdb07-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="cdb07-112">Når du har fundet siden, skal du vælge sidenavnet for at åbne siden i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cdb07-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="cdb07-113">Hvis siden er synlig i sidefremviseren, kan du vælge **Rediger** og tjekke siden ud, før du åbner den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cdb07-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="cdb07-114">På denne måde kan du checke flere sider ud på samme tid.</span><span class="sxs-lookup"><span data-stu-id="cdb07-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="cdb07-115">Når siden er åben i sideeditoren, skal du sørge for, at den er checket ud til dig.</span><span class="sxs-lookup"><span data-stu-id="cdb07-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="cdb07-116">Kommandolinjen i oprettelsesværktøjet er dynamisk, kontekstafhængig og tilstandsfølsom.</span><span class="sxs-lookup"><span data-stu-id="cdb07-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="cdb07-117">Derfor viser den kun de handlinger, du i øjeblikket kan udføre på siden.</span><span class="sxs-lookup"><span data-stu-id="cdb07-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="cdb07-118">Hvis siden f.eks. ikke er tjekket ud til dig, vises knapperne **Gem** og **Afslut redigering** ikke på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="cdb07-119">Sidetilstanden vises også i højre side af vinduet.</span><span class="sxs-lookup"><span data-stu-id="cdb07-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="cdb07-120">Hvis siden ikke allerede er tjekket ud til dig, skal du vælge **Rediger** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="cdb07-121">Kommandolinjen ændres, så den afspejler sidens nye tilstand.</span><span class="sxs-lookup"><span data-stu-id="cdb07-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="cdb07-122">Du modtager også en besked om, at siden blev checket ud til dig.</span><span class="sxs-lookup"><span data-stu-id="cdb07-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="cdb07-123">Det næste trin er at foretage de faktiske ændringer.</span><span class="sxs-lookup"><span data-stu-id="cdb07-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="cdb07-124">Du skal ofte bruge sidens dispositionstræ til venstre for at finde og vælge det modul, du vil ændre, og derefter foretage ændringer i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cdb07-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="cdb07-125">Men ændringen kan undertiden omfatte tilføjelse eller fjernelse af modeller eller fragmenter.</span><span class="sxs-lookup"><span data-stu-id="cdb07-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="cdb07-126">Hvis du vil tilføje et fragment eller et modul, skal du bruge sidens dispositionstræ til at finde den plads, hvor du vil tilføje modulet eller fragmentet og derefter vælge ellipseknappen (**...**) for den pågældende plads.</span><span class="sxs-lookup"><span data-stu-id="cdb07-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="cdb07-127">Der vises en menu, der indeholder kommandoer til tilføjelse af et modul eller fragment.</span><span class="sxs-lookup"><span data-stu-id="cdb07-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="cdb07-128">Hvis du vil fjerne et modul eller fragment, skal du finde og markere det i sidedispositionstræet, vælge ellipseknappen og derefter vælge den kommando, der sletter modulet eller fragmentet.</span><span class="sxs-lookup"><span data-stu-id="cdb07-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="cdb07-129">Du kan også se og redigere egenskaberne for et modul, der er synligt i eksempelvisningen i den visuelle sidegenerator ved at vælge det direkte.</span><span class="sxs-lookup"><span data-stu-id="cdb07-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="cdb07-130">Når du er færdig med at foretage ændringer og se deres effekt, skal du tjekke siden ind ved at vælge **Afslut redigering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="cdb07-131">Vælg **Publicer** på kommandolinjen for at publicere dine ændringer med det samme.</span><span class="sxs-lookup"><span data-stu-id="cdb07-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="cdb07-132">Den senest indcheckede version af den side, du har ændret, publiceres og bliver tilgængelig for eksterne brugere, der går ind dit websted.</span><span class="sxs-lookup"><span data-stu-id="cdb07-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="cdb07-133">Eksempel: Ændre videoen på startsiden</span><span class="sxs-lookup"><span data-stu-id="cdb07-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="cdb07-134">I følgende eksempel vises, hvordan du kan ændre startsiden ved at ændre den video, der vises i videoafspillermodulet.</span><span class="sxs-lookup"><span data-stu-id="cdb07-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="cdb07-135">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="cdb07-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="cdb07-136">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="cdb07-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="cdb07-137">Find og vælg startsiden for at åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="cdb07-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="cdb07-138">Vælg **Rediger** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="cdb07-139">Vælg **Hoved**-pladsen i sidedispositionen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="cdb07-140">Udvid alle flydende containermoduler under **Hoved**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="cdb07-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="cdb07-141">Find og vælg videoafspillermodulet.</span><span class="sxs-lookup"><span data-stu-id="cdb07-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="cdb07-142">Vælg egenskaben **Video** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cdb07-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="cdb07-143">Aktivvælgeren vises.</span><span class="sxs-lookup"><span data-stu-id="cdb07-143">The asset picker appears.</span></span>
1. <span data-ttu-id="cdb07-144">Vælg et tilgængeligt videoaktiv i aktivvælgeren, eller vælg **Upload nyt aktiv** for at overføre et nyt videoaktiv.</span><span class="sxs-lookup"><span data-stu-id="cdb07-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="cdb07-145">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdb07-145">Select **OK**.</span></span>
1. <span data-ttu-id="cdb07-146">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cdb07-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cdb07-147">Angiv **Ændrede videoen** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdb07-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="cdb07-148">Vælg **Eksempel** for at få vist den opdaterede side.</span><span class="sxs-lookup"><span data-stu-id="cdb07-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="cdb07-149">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="cdb07-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="cdb07-150">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cdb07-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdb07-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cdb07-151">Additional resources</span></span>

[<span data-ttu-id="cdb07-152">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="cdb07-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cdb07-153">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="cdb07-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="cdb07-154">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="cdb07-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="cdb07-155">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="cdb07-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="cdb07-156">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="cdb07-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="cdb07-157">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="cdb07-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="cdb07-158">Bekræft tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="cdb07-158">Verify page content accessibility</span></span>](verify-accessibility.md)
