---
title: Arbejde med fragmenter
description: Dette emne beskriver, hvorfor, hvornår og hvordan du bruger fragmenter i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3df2d99ef10f909cedef16167fb8d5a0024683b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210941"
---
# <a name="work-with-fragments"></a><span data-ttu-id="7667f-103">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="7667f-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="7667f-104">Dette emne beskriver, hvorfor, hvornår og hvordan du bruger fragmenter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7667f-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7667f-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="7667f-105">Overview</span></span>

<span data-ttu-id="7667f-106">Fragmenter giver en centraliseret oprettelsesoplevelse for modulkonfigurationer, der skal genbruges på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="7667f-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="7667f-107">F.eks. konfigureres sidehoveder, sidefødder og bannere ofte som fragmenter, fordi de deles på tværs af mange sider.</span><span class="sxs-lookup"><span data-stu-id="7667f-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="7667f-108">Du kan betragte fragmenter som miniaturewebsider, der kan indsættes på andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="7667f-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="7667f-109">Fragmenter har deres egen livscyklus.</span><span class="sxs-lookup"><span data-stu-id="7667f-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="7667f-110">Det vil sige, at de oprettes, refereres til, opdateres og slettes som uafhængige enheder i oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="7667f-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="7667f-111">Når fragmenter er konfigureret, kan de bruges overalt, hvor moduler bruges i strukturen for webstedet.</span><span class="sxs-lookup"><span data-stu-id="7667f-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="7667f-112">Der kan henvises til fragmenter på sider, i layout, i skabeloner og i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="7667f-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="7667f-113">Fragmenter kan integreres i op til syv niveauer inde i andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="7667f-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="7667f-114">Hvis du f.eks. vil promovere en begivenhed på tværs af mange sider på webstedet, kan du bruge et fragment.</span><span class="sxs-lookup"><span data-stu-id="7667f-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="7667f-115">Det første trin i oprettelsesprocessne for et nyt fragment er at vælge den type modul, du vil starte fra.</span><span class="sxs-lookup"><span data-stu-id="7667f-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="7667f-116">I dette eksempel kan du opbygge fragmentet fra et hero-modul.</span><span class="sxs-lookup"><span data-stu-id="7667f-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="7667f-117">Fragmenter kan opbygges fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="7667f-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="7667f-118">Du kan derefter konfigurere hero-fragmentet med dit specifikke kampagneindhold.</span><span class="sxs-lookup"><span data-stu-id="7667f-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="7667f-119">Du kan også lokalisere det efter behov.</span><span class="sxs-lookup"><span data-stu-id="7667f-119">You can also localize it as you require.</span></span> <span data-ttu-id="7667f-120">Det nye enkeltstående fragment kan derefter forbruges som et forudkonfigureret modul på hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="7667f-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="7667f-121">Du kan nemt føje det til skabeloner, til bestemte sider eller til andre fragmenter, der kan indeholde hero-moduler.</span><span class="sxs-lookup"><span data-stu-id="7667f-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="7667f-122">Alle de steder, hvor fragmentet tilføjes, er referencer til det centrale hero-fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="7667f-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="7667f-123">Hvis du udgiver ændringer til fragmentet, afspejles disse ændringer med det samme på alle de steder, hvor der refereres til fragmentet på tværs af webstedet.</span><span class="sxs-lookup"><span data-stu-id="7667f-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="7667f-124">Derfor giver fragmenterne praktisk og effektiv genbrug og centraladministration af modulkonfigurationer på et websted.</span><span class="sxs-lookup"><span data-stu-id="7667f-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="7667f-125">Ved effektivt at bruge dem kan du øge fleksibiliteten betydeligt og hjælpe med at reducere den omkostning, der er forbundet med at administrere webstedets indhold.</span><span class="sxs-lookup"><span data-stu-id="7667f-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="7667f-126">I følgende illustration vises, hvordan fragmenter kan bruges til at centralisere oprettelse af delte modulkonfigurationer på tværs af et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="7667f-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![En illustration, der viser, hvordan fragmenter kan bruges til at centralisere oprettelse af delte modulkonfigurationer på tværs af et e-handels-websted](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="7667f-128">Oprette et fragment</span><span class="sxs-lookup"><span data-stu-id="7667f-128">Create a fragment</span></span>

<span data-ttu-id="7667f-129">Du kan enten oprette et nyt fragment eller gemme en eksisterende modulkonfiguration som et fragment.</span><span class="sxs-lookup"><span data-stu-id="7667f-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="7667f-130">Gemme en eksisterende modulkonfiguration som et fragment</span><span class="sxs-lookup"><span data-stu-id="7667f-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="7667f-131">Hvis du vil konvertere et tidligere konfigureret modul til et fragment, der kan genbruges, skal du følge disse trin i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7667f-132">Åbn en side eller skabelon, der indeholder det modul, du vil konvertere til et fragment.</span><span class="sxs-lookup"><span data-stu-id="7667f-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="7667f-133">Vælg det tidligere konfigurerede modul i dispositionsruden til venstre eller direkte i den visuelle sidegenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="7667f-134">Vælg ellipsen (**...**) ud for navnet på modulet i enten dispositionsruden eller på værktøjslinjen for det valgte modul i den visuelle sidegenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="7667f-135">Vælg **Del som fragment**.</span><span class="sxs-lookup"><span data-stu-id="7667f-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="7667f-136">I dialogboksen **Gem som fragment** skal du angive et navn til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="7667f-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="7667f-137">Vælg **OK** for at gemme modulkonfigurationen som et fragment, der kan føjes til andre sider.</span><span class="sxs-lookup"><span data-stu-id="7667f-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="7667f-138">Opret et nyt fragment</span><span class="sxs-lookup"><span data-stu-id="7667f-138">Create a new fragment</span></span>

<span data-ttu-id="7667f-139">Udfør følgende trin for at oprette et nyt fragment i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7667f-140">Vælg **Fragmenter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="7667f-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="7667f-141">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7667f-141">Select **New**.</span></span> <span data-ttu-id="7667f-142">Der vises en **Nyt fragment**-dialogboks, hvor alle tilgængelige modultyper kan ses.</span><span class="sxs-lookup"><span data-stu-id="7667f-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="7667f-143">Som tidligere nævnt kan fragmenter oprettes ud fra en hvilken som helst modultype.</span><span class="sxs-lookup"><span data-stu-id="7667f-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="7667f-144">Vælg en modultype til dit fragment.</span><span class="sxs-lookup"><span data-stu-id="7667f-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="7667f-145">Hvis du vælger en generisk containermodultype, får du størst fleksibilitet, når du skal opdatere og konfigurere dit fragment senere.</span><span class="sxs-lookup"><span data-stu-id="7667f-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="7667f-146">Tilføje, fjerne eller redigere fragmenter på en side</span><span class="sxs-lookup"><span data-stu-id="7667f-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="7667f-147">I følgende procedurer beskrives, hvordan du kan tilføje, fjerne og redigere fragmenter.</span><span class="sxs-lookup"><span data-stu-id="7667f-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="7667f-148">Tilføje et fragment</span><span class="sxs-lookup"><span data-stu-id="7667f-148">Add a fragment</span></span>

<span data-ttu-id="7667f-149">Udfør følgende trin for at tilføje et fragment på en side i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7667f-150">Vælg en container eller en plads, som underordnede moduler kan føjes til, i dispositionsruden til venstre eller direkte i den visuelle sidegenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="7667f-151">Vælg ellipsen (**...**) ud for navnet på containeren eller pladsen.</span><span class="sxs-lookup"><span data-stu-id="7667f-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="7667f-152">Hvis du bruger den visuelle sidegenerator, skal du vælge plussymbolet (**+**).</span><span class="sxs-lookup"><span data-stu-id="7667f-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="7667f-153">Vælg **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="7667f-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="7667f-154">Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj fragment** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="7667f-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="7667f-155">Søg efter og vælg et fragment, der skal tilføjes, i dialogboksen **Vælg fragment**.</span><span class="sxs-lookup"><span data-stu-id="7667f-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="7667f-156">Hvis der ikke vises nogen tilgængelige fragmenter, skal du muligvis først oprette et fragment ud fra en modultype, som den valgte container eller plads understøtter.</span><span class="sxs-lookup"><span data-stu-id="7667f-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="7667f-157">Vælg det ønskede fragment for at føje det til containeren eller pladsen på siden.</span><span class="sxs-lookup"><span data-stu-id="7667f-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="7667f-158">De moduler, der er tilladt i en container eller plads, defineres af sidens skabelon eller modulernes egne definitioner.</span><span class="sxs-lookup"><span data-stu-id="7667f-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="7667f-159">Fjerne et fragment</span><span class="sxs-lookup"><span data-stu-id="7667f-159">Remove a fragment</span></span>

<span data-ttu-id="7667f-160">Hvis du vil fjerne et fragment fra en plads eller en container på en side i Commerce-webstedsgenerator, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7667f-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7667f-161">Vælg ellipseknappen (**...**) i dispositionsruden til venstre ud for navnet på det fragment, der skal fjernes, og vælg derefter symbolet med papirkurven.</span><span class="sxs-lookup"><span data-stu-id="7667f-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="7667f-162">Du kan også vælge fragmentet i den visuelle sidegenerator og vælge symbolet for papirkurven på fragmentets værktøjslinje.</span><span class="sxs-lookup"><span data-stu-id="7667f-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="7667f-163">Når du bliver bedt om at bekræfte, at du vil fjerne fragmentet, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7667f-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="7667f-164">Når du fjerner et fragment fra en side, fjerner du blot referencen til det fra den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="7667f-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="7667f-165">Du fjerner **ikke** fragmentet fra dit websted.</span><span class="sxs-lookup"><span data-stu-id="7667f-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="7667f-166">Hvis du vil slette fragmenter på dit websted, skal du anvende brugergrænsefladen i fragmentfremviseren.</span><span class="sxs-lookup"><span data-stu-id="7667f-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="7667f-167">Du kan kun slette fragmenter fra et websted, hvis der i øjeblikket ikke refereres til dem fra sider, skabeloner eller andre fragmenter.</span><span class="sxs-lookup"><span data-stu-id="7667f-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="7667f-168">Redigere et fragment</span><span class="sxs-lookup"><span data-stu-id="7667f-168">Edit a fragment</span></span>

<span data-ttu-id="7667f-169">Hvis du vil redigere fragmenter, skal du bruge fragmenteditoren.</span><span class="sxs-lookup"><span data-stu-id="7667f-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="7667f-170">Denne restriktion er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="7667f-170">This restriction is by design.</span></span> <span data-ttu-id="7667f-171">Det er med til at sikre, at forfatterne ikke forveksler redigering af modulerne for en bestemt side med processen til redigering af fragmenter, der kan deles på mange sider.</span><span class="sxs-lookup"><span data-stu-id="7667f-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="7667f-172">Udfør følgende trin for at redigere et fragment i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="7667f-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7667f-173">Vælg **Fragmenter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="7667f-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="7667f-174">Vælg det fragment, du vil redigere, under **Fragmenter**.</span><span class="sxs-lookup"><span data-stu-id="7667f-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="7667f-175">Rediger fragmentets modulegenskaber og struktur efter behov.</span><span class="sxs-lookup"><span data-stu-id="7667f-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="7667f-176">Processen minder om processen til redigering af moduler, der redigeres i sideeditorvisningen.</span><span class="sxs-lookup"><span data-stu-id="7667f-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="7667f-177">Du kan også redigere et fragment ved at vælge det på en side, i en skabelon eller i et overordnet fragment og derefter vælge **Rediger fragment** i ruden Egenskaber til højre.</span><span class="sxs-lookup"><span data-stu-id="7667f-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7667f-178">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7667f-178">Additional resources</span></span>

[<span data-ttu-id="7667f-179">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="7667f-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="7667f-180">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="7667f-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="7667f-181">Arbejde med forudindstillede layout</span><span class="sxs-lookup"><span data-stu-id="7667f-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="7667f-182">Arbejd med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="7667f-182">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]