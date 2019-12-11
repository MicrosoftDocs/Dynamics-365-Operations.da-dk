---
title: Arbejde med forudindstillede layout
description: Dette emne beskriver, hvordan du kan arbejde med forudindstillede layout i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f2c0638caa7e4f6f831e592e3f7e3f5ab7d1d81
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697813"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="60f8d-103">Arbejde med forudindstillede layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-103">Work with preset layouts</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="60f8d-104">Dette emne beskriver, hvordan du kan arbejde med forudindstillede layout i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="60f8d-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60f8d-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="60f8d-105">Overview</span></span>

<span data-ttu-id="60f8d-106">Før du fuldfører procedurerne i dette emne, skal du sørge for at læse [Forudindstillede og brugerdefinerede layout](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="60f8d-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="60f8d-107">Du kan finde en generel oversigt under [Oversigt over skabeloner og layout](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="60f8d-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="60f8d-108">Oprette et nyt forudindstillet layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-108">Create a new preset layout</span></span>

<span data-ttu-id="60f8d-109">Der findes to metoder til oprettelse af et forudindstillet layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="60f8d-110">Du kan gemme et eksisterende brugerdefineret layout som et nyt forudindstillet layout, eller du kan oprette et forudindstillet layout fra bunden.</span><span class="sxs-lookup"><span data-stu-id="60f8d-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="60f8d-111">Oprette et forudindstillet layout ud fra et eksisterende brugerdefineret layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="60f8d-112">Du kan oprette et forudindstillet layout ud fra et eksisterende brugerdefineret layout ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="60f8d-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="60f8d-113">Åbn en eksisterende side, der ikke aktuelt bruger et foruddefineret layout, og som har en modulstruktur, du vil genbruge til andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="60f8d-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="60f8d-114">Vælg **Check ud**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-114">Select **Check out**.</span></span>
1. <span data-ttu-id="60f8d-115">Vælg **Gem som nyt layout**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-115">Select **Save as new layout**.</span></span> <span data-ttu-id="60f8d-116">Dialogboksen **Gem som nyt layout** vises.</span><span class="sxs-lookup"><span data-stu-id="60f8d-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="60f8d-117">Indtast et navn og en beskrivelse til det forudindstillede layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="60f8d-118">De værdier, du angiver, vises for andre forfattere, når de opretter nye sider ud fra dit layout eller skifter til det.</span><span class="sxs-lookup"><span data-stu-id="60f8d-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="60f8d-119">Angiv derfor værdier, der vil være nyttige for sideforfattere.</span><span class="sxs-lookup"><span data-stu-id="60f8d-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="60f8d-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-120">Select **OK**.</span></span>

<span data-ttu-id="60f8d-121">Det forudindstillede layout er nu tilgængeligt, når du opretter nye sider eller vælger et andet layout for en side i samme skabelonhierarki.</span><span class="sxs-lookup"><span data-stu-id="60f8d-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="60f8d-122">Hvis du hurtigt vil se, om en bestemt side i øjeblikket er bundet til et foruddefineret layout, skal du vælge siden i listevisningen af sider og undersøge metadata til layout i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="60f8d-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="60f8d-123">Oprette et nyt forudindstillet layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-123">Create a new preset layout</span></span>

<span data-ttu-id="60f8d-124">Du kan oprette et forudindstillet layout fra bunden ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="60f8d-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="60f8d-125">Vælg **Layout** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="60f8d-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="60f8d-126">Vælg **Nyt layout**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-126">Select **New Layout**.</span></span> <span data-ttu-id="60f8d-127">Dialogboksen **Nyt layout** vises.</span><span class="sxs-lookup"><span data-stu-id="60f8d-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="60f8d-128">Vælg den skabelon, der skal bruges til dit forudindstillede layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="60f8d-129">Indtast et navn og en beskrivelse til det forudindstillede layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="60f8d-130">De værdier, du angiver, vises for andre forfattere, når de opretter nye sider ud fra dit layout eller skifter til det.</span><span class="sxs-lookup"><span data-stu-id="60f8d-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="60f8d-131">Angiv derfor værdier, der vil være nyttige for sideforfattere.</span><span class="sxs-lookup"><span data-stu-id="60f8d-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="60f8d-132">Vælg **OK** for at oprette det nye forudindstillede layout og åbne layouteditoren.</span><span class="sxs-lookup"><span data-stu-id="60f8d-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="60f8d-133">Tilføj og konfigurer moduler ved hjælp af dispositionstræet til venstre og egenskabsruden til højre i layouteditoren.</span><span class="sxs-lookup"><span data-stu-id="60f8d-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="60f8d-134">(Processen minder om processen for tilføjelse og konfiguration af moduler til en skabelon i skabeloneditoren). Placeringen af moduler og eventuelle låste standardindstillinger bliver den centraliserede modulkonfiguration for alle de sider, der bruger dette foruddefinerede layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="60f8d-135">Redigere et forudindstillet layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-135">Modify a preset layout</span></span>

<span data-ttu-id="60f8d-136">Benyt følgende fremgangsmåde for at redigere et forudindstillet layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="60f8d-137">Vælg **Layout** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="60f8d-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="60f8d-138">Vælg det modul, der skal redigeres, i dispositionstræet til venstre i layouteditoren.</span><span class="sxs-lookup"><span data-stu-id="60f8d-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="60f8d-139">Udfør derefter ethvert af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="60f8d-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="60f8d-140">Hvis du vil flytte et modul op eller ned inden for det overordnede objekt, skal du vælge ellipseknappen (**...**) for modulet og vælge **Flyt op** eller **Flyt ned**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="60f8d-141">Hvis du vil ændre standardindstillingerne i et modul, skal du bruge egenskabsruden til at angive standardværdier og derefter låse dem til alle downstream-sider.</span><span class="sxs-lookup"><span data-stu-id="60f8d-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="60f8d-142">Hvis du vil føje nye moduler eller fragmenter til containermoduler, skal du vælge ellipseknappen og derefter vælge **Tilføj modul** eller **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="60f8d-143">Hvis du vil fjerne et modul fra layoutet, skal du vælge ellipseknappen og derefter vælge **Slet**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="60f8d-144">Ændre et forudindstillet layouttema</span><span class="sxs-lookup"><span data-stu-id="60f8d-144">Change a preset layout theme</span></span>

<span data-ttu-id="60f8d-145">En typisk praksis er at angive et standardtema for alle sider, der bruger et forudindstillet layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="60f8d-146">Hvis du vil angive eller ændre temaet for alle de underordnede sider, der bruger det forudindstillede layout, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="60f8d-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="60f8d-147">Vælg sidecontainermodulet i dispositionstræet til venstre i layouteditoren.</span><span class="sxs-lookup"><span data-stu-id="60f8d-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="60f8d-148">(Dette modul er typisk den anden node og hedder **Standardside**).</span><span class="sxs-lookup"><span data-stu-id="60f8d-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="60f8d-149">Vælg et tema i feltet **Tema** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="60f8d-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="60f8d-150">Gemme, checke ind, se forhåndsvisning af og publicere et forudindstillet layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="60f8d-151">Følg disse trin for at gemme og checke dit forudindstillede layout ind.</span><span class="sxs-lookup"><span data-stu-id="60f8d-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="60f8d-152">Vælg **Gem** øverst i layouteditoren.</span><span class="sxs-lookup"><span data-stu-id="60f8d-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="60f8d-153">Gemte ændringer påvirker ikke downstream-sider, før de er checket ind.</span><span class="sxs-lookup"><span data-stu-id="60f8d-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="60f8d-154">Vælg **Check ind**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-154">Select **Check In**.</span></span> <span data-ttu-id="60f8d-155">Dine ændringer er nu synlige for downstream-arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="60f8d-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="60f8d-156">Hvis du vil se ændringerne på forhånd, skal du enten åbne en eksisterende side, der bruger det forudindstillede layout, eller oprette en ny side ud fra layoutet.</span><span class="sxs-lookup"><span data-stu-id="60f8d-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="60f8d-157">Når du har set ændringerne af det forudindstillede layout, skal du følge et af disse trin for at publicere layoutet til dit aktive websted:</span><span class="sxs-lookup"><span data-stu-id="60f8d-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="60f8d-158">Gå til **Layout**, vælg layoutet, og vælg derefter **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="60f8d-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="60f8d-159">Vælg **Publicer** i layouteditoren.</span><span class="sxs-lookup"><span data-stu-id="60f8d-159">In the layout editor, select **Publish**.</span></span>
* <span data-ttu-id="60f8d-160">Publicer en side, der refererer til det ikke-publicerede layout.</span><span class="sxs-lookup"><span data-stu-id="60f8d-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="60f8d-161">Layoutet vil automatisk blive publiceret.</span><span class="sxs-lookup"><span data-stu-id="60f8d-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="60f8d-162">Der kan refereres til forudindstillede layout fra flere sider.</span><span class="sxs-lookup"><span data-stu-id="60f8d-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="60f8d-163">Når du publicerer et forudindstillet layout, skal du være opmærksom på, at du kan påvirke layoutet af flere sider.</span><span class="sxs-lookup"><span data-stu-id="60f8d-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60f8d-164">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="60f8d-164">Additional resources</span></span>

[<span data-ttu-id="60f8d-165">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="60f8d-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="60f8d-166">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="60f8d-166">Work with templates</span></span>](work-with-templates.md)
