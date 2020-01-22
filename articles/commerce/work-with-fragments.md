---
title: Arbejde med fragmenter
description: Dette emne beskriver, hvorfor, hvornår og hvordan du bruger fragmenter i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914694"
---
# <a name="work-with-fragments"></a><span data-ttu-id="c0c47-103">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="c0c47-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c0c47-104">Dette emne beskriver, hvorfor, hvornår og hvordan du bruger fragmenter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c0c47-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c0c47-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="c0c47-105">Overview</span></span>

<span data-ttu-id="c0c47-106">Fragmenter giver en centraliseret oprettelsesoplevelse for modulkonfigurationer, der skal genbruges på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="c0c47-107">F.eks. konfigureres sidehoveder, sidefødder og bannere ofte som fragmenter, fordi de deles på tværs af mange sider.</span><span class="sxs-lookup"><span data-stu-id="c0c47-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="c0c47-108">Du kan betragte fragmenter som miniaturewebsider, der kan indsættes på andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="c0c47-109">Fragmenter har deres egen livscyklus.</span><span class="sxs-lookup"><span data-stu-id="c0c47-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="c0c47-110">Det vil sige, at de oprettes, refereres til, opdateres og slettes som uafhængige enheder i oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="c0c47-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="c0c47-111">Når fragmenter er konfigureret, kan de bruges overalt, hvor moduler bruges i strukturen for webstedet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="c0c47-112">Der kan henvises til fragmenter på sider, i layout, i skabeloner og i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="c0c47-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c47-113">Fragmenter kan integreres i op til syv niveauer inde i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="c0c47-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="c0c47-114">Hvis du f.eks. vil promovere en begivenhed på tværs af mange sider på webstedet, kan du bruge et fragment.</span><span class="sxs-lookup"><span data-stu-id="c0c47-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="c0c47-115">Det første trin i oprettelsesprocessne for et nyt fragment er at vælge den type modul, du vil starte fra.</span><span class="sxs-lookup"><span data-stu-id="c0c47-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="c0c47-116">I dette eksempel kan du opbygge fragmentet fra et hero-modul.</span><span class="sxs-lookup"><span data-stu-id="c0c47-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c47-117">Fragmenter kan opbygges fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="c0c47-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="c0c47-118">Du kan derefter konfigurere hero-fragmentet med dit specifikke kampagneindhold.</span><span class="sxs-lookup"><span data-stu-id="c0c47-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="c0c47-119">Du kan også lokalisere det efter behov.</span><span class="sxs-lookup"><span data-stu-id="c0c47-119">You can also localize it as you require.</span></span> <span data-ttu-id="c0c47-120">Det nye enkeltstående fragment kan derefter forbruges som et forudkonfigureret modul på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="c0c47-121">Du kan nemt føje det til skabeloner, til bestemte sider eller til andre fragmenter, der kan indeholde hero-moduler.</span><span class="sxs-lookup"><span data-stu-id="c0c47-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="c0c47-122">Alle de steder, hvor fragmentet tilføjes, er referencer til det centrale hero-fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="c0c47-123">Hvis du udgiver ændringer til fragmentet, afspejles disse ændringer med det samme på alle de steder, hvor der refereres til fragmentet på tværs af webstedet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="c0c47-124">Derfor giver fragmenterne praktisk og effektiv genbrug og centraladministration af modulkonfigurationer på et websted.</span><span class="sxs-lookup"><span data-stu-id="c0c47-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="c0c47-125">Ved effektivt at bruge dem kan du øge fleksibiliteten betydeligt og hjælpe med at reducere den omkostning, der er forbundet med at administrere webstedets indhold.</span><span class="sxs-lookup"><span data-stu-id="c0c47-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="c0c47-126">I følgende illustration vises, hvordan fragmenter kan bruges til at centralisere oprettelse af delte modulkonfigurationer på tværs af et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="c0c47-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![En illustration, der viser, hvordan fragmenter kan bruges til at centralisere oprettelse af delte modulkonfigurationer på tværs af et e-handels-websted](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="c0c47-128">Oprette et fragment</span><span class="sxs-lookup"><span data-stu-id="c0c47-128">Create a fragment</span></span>

<span data-ttu-id="c0c47-129">Du kan enten oprette et nyt fragment eller gemme en eksisterende modulkonfiguration som et fragment.</span><span class="sxs-lookup"><span data-stu-id="c0c47-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="c0c47-130">Oprette et nyt fragment</span><span class="sxs-lookup"><span data-stu-id="c0c47-130">Create a new fragment</span></span>

<span data-ttu-id="c0c47-131">Følg disse trin for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="c0c47-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="c0c47-132">Vælg **Fragmenter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="c0c47-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c0c47-133">Vælg **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="c0c47-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="c0c47-134">Der vises en dialogboks, hvor alle tilgængelige modultyper kan ses.</span><span class="sxs-lookup"><span data-stu-id="c0c47-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="c0c47-135">Som tidligere nævnt kan fragmenter oprettes ud fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="c0c47-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="c0c47-136">Vælg en modultype til fragmentet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0c47-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="c0c47-137">Hvis du vælger en generisk containermodultype, får du størst fleksibilitet, når du skal opdatere og konfigurere dit fragment senere.</span><span class="sxs-lookup"><span data-stu-id="c0c47-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="c0c47-138">Gemme en eksisterende modulkonfiguration som et fragment</span><span class="sxs-lookup"><span data-stu-id="c0c47-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="c0c47-139">Hvis du vil konvertere et tidligere konfigureret modul til et fragment, der kan genbruges, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c0c47-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="c0c47-140">Åbn en side eller skabelon, der indeholder det modul, du vil konvertere til et fragment.</span><span class="sxs-lookup"><span data-stu-id="c0c47-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="c0c47-141">Vælg ellipseknappen (**...**) i dispositionsruden til venstre ud for navnet på modulet, og vælg derefter **Gem som fragment**.</span><span class="sxs-lookup"><span data-stu-id="c0c47-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="c0c47-142">Der vises en dialogboks.</span><span class="sxs-lookup"><span data-stu-id="c0c47-142">A dialog box appears.</span></span>
1. <span data-ttu-id="c0c47-143">Angiv et navn og metadata for fragmentet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="c0c47-144">Vælg **OK** for at gemme modulkonfigurationen som et fragment, der kan føjes til andre sider.</span><span class="sxs-lookup"><span data-stu-id="c0c47-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="c0c47-145">Tilføje, fjerne eller redigere fragmenter på en side</span><span class="sxs-lookup"><span data-stu-id="c0c47-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="c0c47-146">I følgende procedurer beskrives, hvordan du kan tilføje, fjerne og redigere fragmenter.</span><span class="sxs-lookup"><span data-stu-id="c0c47-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="c0c47-147">Tilføje et fragment</span><span class="sxs-lookup"><span data-stu-id="c0c47-147">Add a fragment</span></span>

<span data-ttu-id="c0c47-148">Følg disse trin for at føje et fragment til en side.</span><span class="sxs-lookup"><span data-stu-id="c0c47-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="c0c47-149">Vælg en container eller en plads, som underordnede moduler kan føjes til, i dispositionsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="c0c47-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="c0c47-150">Vælg ellipseknappen ud for navnet på containeren eller pladsen, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="c0c47-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="c0c47-151">Der vises en dialogboks.</span><span class="sxs-lookup"><span data-stu-id="c0c47-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0c47-152">Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj fragment** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="c0c47-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="c0c47-153">Søg efter og vælg et fragment, der skal tilføjes, i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c0c47-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="c0c47-154">Hvis der ikke vises nogen tilgængelige fragmenter, skal du muligvis først oprette et fragment ud fra en modultype, som den valgte container eller plads understøtter.</span><span class="sxs-lookup"><span data-stu-id="c0c47-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="c0c47-155">Vælg **OK** for at føje det valgte fragment til den valgte container eller plads på siden.</span><span class="sxs-lookup"><span data-stu-id="c0c47-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c47-156">De moduler, der er tilladt i en container eller plads, defineres af sidens skabelon eller modulernes egne definitioner.</span><span class="sxs-lookup"><span data-stu-id="c0c47-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="c0c47-157">Fjerne et fragment</span><span class="sxs-lookup"><span data-stu-id="c0c47-157">Remove a fragment</span></span>

<span data-ttu-id="c0c47-158">Hvis du vil fjerne et fragment fra en plads eller container på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c0c47-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="c0c47-159">Vælg ellipseknappen (...) i dispositionsruden til venstre ud for navnet på det fragment, der skal fjernes, og vælg derefter knappen med papirkurven.</span><span class="sxs-lookup"><span data-stu-id="c0c47-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="c0c47-160">Når du bliver bedt om at bekræfte, at du vil fjerne fragmentet, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0c47-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="c0c47-161">Når du fjerner et fragment fra en side, fjerner du blot referencen til det fra den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="c0c47-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="c0c47-162">Du fjerner **ikke** fragmentet fra dit websted.</span><span class="sxs-lookup"><span data-stu-id="c0c47-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="c0c47-163">Hvis du vil slette fragmenter på dit websted, skal du anvende brugergrænsefladen i fragmentfremviseren.</span><span class="sxs-lookup"><span data-stu-id="c0c47-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="c0c47-164">Du kan kun slette fragmenter fra et websted, hvis der i øjeblikket ikke refereres til dem fra sider, skabeloner eller andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="c0c47-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="c0c47-165">Redigere et fragment</span><span class="sxs-lookup"><span data-stu-id="c0c47-165">Edit a fragment</span></span>

<span data-ttu-id="c0c47-166">Hvis du vil redigere fragmenter, skal du bruge fragmenteditoren.</span><span class="sxs-lookup"><span data-stu-id="c0c47-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="c0c47-167">Denne restriktion er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="c0c47-167">This restriction is by design.</span></span> <span data-ttu-id="c0c47-168">Det er med til at sikre, at forfatterne ikke forveksler redigering af modulerne for en bestemt side med processen til redigering af fragmenter, der kan deles på mange sider.</span><span class="sxs-lookup"><span data-stu-id="c0c47-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="c0c47-169">Følg disse trin for at redigere et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="c0c47-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="c0c47-170">Vælg **Fragmenter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="c0c47-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c0c47-171">Vælg det fragment, du vil redigere, under **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="c0c47-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="c0c47-172">Rediger fragmentets modulegenskaber og struktur efter behov.</span><span class="sxs-lookup"><span data-stu-id="c0c47-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="c0c47-173">Processen minder om processen til redigering af moduler, der redigeres i sideeditorvisningen.</span><span class="sxs-lookup"><span data-stu-id="c0c47-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="c0c47-174">Du kan også redigere et fragment ved at vælge det på en side, i en skabelon eller i et overordnet fragment og derefter vælge **Rediger fragment** i ruden Egenskaber til højre.</span><span class="sxs-lookup"><span data-stu-id="c0c47-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0c47-175">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c0c47-175">Additional resources</span></span>

[<span data-ttu-id="c0c47-176">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="c0c47-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c0c47-177">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="c0c47-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="c0c47-178">Arbejde med forudindstillede layout</span><span class="sxs-lookup"><span data-stu-id="c0c47-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="c0c47-179">Arbejd med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="c0c47-179">Work with publish groups</span></span>](publish-groups.md)
