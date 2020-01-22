---
title: Arbejde med moduler
description: Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.
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
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914788"
---
# <a name="work-with-modules"></a><span data-ttu-id="51f21-103">Arbejde med moduler</span><span class="sxs-lookup"><span data-stu-id="51f21-103">Work with modules</span></span>

<span data-ttu-id="51f21-104">Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51f21-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="51f21-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="51f21-105">Overview</span></span>

<span data-ttu-id="51f21-106">Moduler er logiske byggeklodser, der udgør sidestrukturen, og de har forskellige formål og omfang.</span><span class="sxs-lookup"><span data-stu-id="51f21-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="51f21-107">Nogle moduler er containere på højt niveau, hvis eneste formål er at opbevare og organisere andre moduler (underordnede moduler).</span><span class="sxs-lookup"><span data-stu-id="51f21-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="51f21-108">Andre moduler, f.eks. et enkelt modul til billedplacering, har et meget specifikt formål.</span><span class="sxs-lookup"><span data-stu-id="51f21-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="51f21-109">Andre moduler som f.eks. et karruselmodul falder et sted mellem disse to kategorier.</span><span class="sxs-lookup"><span data-stu-id="51f21-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="51f21-110">Dynamics 365 Commerce-webstedet indeholder som standard et startsæt med modulbibliotek, der giver dig mulighed for at få de fleste grundlæggende e-handelsscenarier.</span><span class="sxs-lookup"><span data-stu-id="51f21-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="51f21-111">Du bør oprette et e-handels-websted, der dækker alt, ved at bruge disse moduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="51f21-112">Du kan dog også tilpasse disse moduler eller opbygge nye, tilpassede moduler til specifikke behov.</span><span class="sxs-lookup"><span data-stu-id="51f21-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="51f21-113">Hvis du vil bygge brugerdefinerede moduler, kan du få hjælp til at oprette et tilpasset modulbibliotek i et SDK (Software Development Kit) til moduldesign.</span><span class="sxs-lookup"><span data-stu-id="51f21-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="51f21-114">Containermoduler og pladser</span><span class="sxs-lookup"><span data-stu-id="51f21-114">Container modules and slots</span></span>

<span data-ttu-id="51f21-115">Som tidligere nævnt er nogle moduler designet til at rumme underordnede moduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="51f21-116">Disse moduler kaldes *containere*, og de giver mulighed for hierarkier af indlejrede moduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="51f21-117">Containermoduler indeholder *pladser*.</span><span class="sxs-lookup"><span data-stu-id="51f21-117">Container modules include *slots*.</span></span> <span data-ttu-id="51f21-118">Pladser bruges til at håndtere layoutet og formålet med underordnede moduler i containeren.</span><span class="sxs-lookup"><span data-stu-id="51f21-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="51f21-119">Et eksempel er et grundlæggende sidecontainermodul (et modul på øverste niveau for en side), der definerer flere vigtige pladser:</span><span class="sxs-lookup"><span data-stu-id="51f21-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="51f21-120">En sidehovedplads</span><span class="sxs-lookup"><span data-stu-id="51f21-120">A header slot</span></span>
- <span data-ttu-id="51f21-121">En brødtekstplads</span><span class="sxs-lookup"><span data-stu-id="51f21-121">A body slot</span></span>
- <span data-ttu-id="51f21-122">En sidefodsplads</span><span class="sxs-lookup"><span data-stu-id="51f21-122">A footer slot</span></span>

<span data-ttu-id="51f21-123">Modulets udvikler definerer disse pladser og bestemmer, hvilke underordnede moduler og hvor mange underordnede moduler der kan placeres direkte i det.</span><span class="sxs-lookup"><span data-stu-id="51f21-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="51f21-124">F.eks. understøtter sidehovedpladsen måske kun ét modul af typen **Sidehovedmodul**, mens brødtekstpladsen understøtter et ubegrænset antal moduler af enhver type (undtagen andre sidecontainermoduler).</span><span class="sxs-lookup"><span data-stu-id="51f21-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="51f21-125">I oprettelsesværktøjerne behøver sideforfattere ikke at vide på forhånd, hvilke moduler der kan anbringes på hver plads.</span><span class="sxs-lookup"><span data-stu-id="51f21-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="51f21-126">Når en sideforfatter vælger en plads og derefter prøver at vælge et modul, der skal føjes til den, vises en filtreret visning af modultyper, der understøttes for den pågældende plads.</span><span class="sxs-lookup"><span data-stu-id="51f21-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="51f21-127">Indholdsmoduler</span><span class="sxs-lookup"><span data-stu-id="51f21-127">Content modules</span></span>

<span data-ttu-id="51f21-128">Indholdsmoduler har indhold og medieelementer, f.eks. tekst (f.eks. overskrifter, afsnit og links) eller aktivreferencer (f.eks. billeder, video og PDF-filer).</span><span class="sxs-lookup"><span data-stu-id="51f21-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="51f21-129">Eksempler på typiske indholdsmodultyper er **Hero**, **Funktion** og **Banner**.</span><span class="sxs-lookup"><span data-stu-id="51f21-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="51f21-130">Moduler af disse tre typer kan indeholde tekst eller medier, og de kræver ingen underordnede moduler for at gøre noget synligt på en side.</span><span class="sxs-lookup"><span data-stu-id="51f21-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="51f21-131">Størstedelen af typiske, daglige side- og indholdsoprettelsesaktiviteter omfatter indholdsmoduler, primært fordi disse moduler definerer det faktiske indhold, der gengives i de overordnede containermoduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="51f21-132">Mange indholdsmoduler er tilgængelige, og disse moduler er typisk de sidste stykker, du skal føje til sidens hierarki af indlejrede moduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="51f21-133">I følgende illustration vises, hvordan moduler er indlejret i de overordnede containermodulpladser.</span><span class="sxs-lookup"><span data-stu-id="51f21-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Indlejring af moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="51f21-135">Tilføje eller fjerne moduler</span><span class="sxs-lookup"><span data-stu-id="51f21-135">Add or remove modules</span></span>

<span data-ttu-id="51f21-136">I følgende procedurer beskrives, hvordan du kan tilføje og fjerne moduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="51f21-137">Tilføje et modul</span><span class="sxs-lookup"><span data-stu-id="51f21-137">Add a module</span></span>

<span data-ttu-id="51f21-138">Hvis du vil tilføje et modul på en plads eller container på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="51f21-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="51f21-139">Vælg en container eller en plads, som et underordnet modul kan føjes til, i dispositionsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="51f21-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51f21-140">Moduldesigneren definerer listen over de modultyper, der kan føjes til en bestemt modulplads.</span><span class="sxs-lookup"><span data-stu-id="51f21-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="51f21-141">Skabelonoprettere kan derefter begrænse de tilladte modulindstillinger for at sikre konsistent optimering af søgemaskiner og redigeringseffektivitet for alle sider, der er bygget ud fra en bestemt skabelon.</span><span class="sxs-lookup"><span data-stu-id="51f21-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="51f21-142">Vælg ellipseknappen (**...**) til modulet, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="51f21-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="51f21-143">Dialogboksen **Tilføj modul** vises.</span><span class="sxs-lookup"><span data-stu-id="51f21-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="51f21-144">Denne dialogboks filtreres automatisk, så der kun vises moduler, der understøttes i den valgte container eller plads.</span><span class="sxs-lookup"><span data-stu-id="51f21-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="51f21-145">Listen over moduler bestemmes af sidens skabelon eller definitionen af containerens modul.</span><span class="sxs-lookup"><span data-stu-id="51f21-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51f21-146">Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj modul** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="51f21-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="51f21-147">Søg efter og vælg et modul, der skal tilføjes på siden, i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="51f21-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="51f21-148">**Funktion** og **Hero** er egnede modultyper, som begyndere kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="51f21-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="51f21-149">Vælg **OK** for at føje det valgte modul til den valgte container eller plads på siden.</span><span class="sxs-lookup"><span data-stu-id="51f21-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="51f21-150">Fjerne et modul</span><span class="sxs-lookup"><span data-stu-id="51f21-150">Remove a module</span></span>

<span data-ttu-id="51f21-151">Hvis du vil fjerne et modul fra en plads eller container på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="51f21-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="51f21-152">Vælg ellipseknappen i dispositionsruden til venstre ud for navnet på det modul, der skal fjernes, og vælg derefter knappen med papirkurven.</span><span class="sxs-lookup"><span data-stu-id="51f21-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="51f21-153">Når du bliver bedt om at bekræfte, at du vil fjerne modulet, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="51f21-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="51f21-154">Konfigurere moduler</span><span class="sxs-lookup"><span data-stu-id="51f21-154">Configure modules</span></span>

<span data-ttu-id="51f21-155">I følgende procedurer beskrives, hvordan du kan konfigurere indholds- og containermoduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="51f21-156">Konfigurere et indholdsmodul</span><span class="sxs-lookup"><span data-stu-id="51f21-156">Configure a content module</span></span>

<span data-ttu-id="51f21-157">Hvis du vil konfigurere et indholdsmodul på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="51f21-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="51f21-158">Vælg en indholdsmodultype i dispositionsruden til venstre (f.eks. **Funktion**, **Hero** eller **Banner**).</span><span class="sxs-lookup"><span data-stu-id="51f21-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="51f21-159">Udvid de indlejrede kontrolelementer i ruden Egenskaber til højre ved at vælge overskrifterne, og angiv eventuelle nødvendige kontrolværdier.</span><span class="sxs-lookup"><span data-stu-id="51f21-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="51f21-160">Hvis ruden Egenskaber indeholder afsnittet **Datakonfiguration**, skal du vælge det for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="51f21-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="51f21-161">Gå ellers til trin 5.</span><span class="sxs-lookup"><span data-stu-id="51f21-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="51f21-162">Hvis knappen **Tilføj datakilde** ikke er markeret, skal du markere den og derefter vælge de indholdselementer, der skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="51f21-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="51f21-163">Angiv indstillinger for nødvendige eller ønskede kontrolelementer til moduler.</span><span class="sxs-lookup"><span data-stu-id="51f21-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="51f21-164">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="51f21-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="51f21-165">Konfigurere et containermodul</span><span class="sxs-lookup"><span data-stu-id="51f21-165">Configure a container module</span></span>

<span data-ttu-id="51f21-166">Hvis du vil konfigurere et containermodul på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="51f21-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="51f21-167">Vælg et containermodul på siden (f.eks. et karrusel- eller flydende containermodul).</span><span class="sxs-lookup"><span data-stu-id="51f21-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="51f21-168">Udvid de indlejrede kontrolelementer i ruden Egenskaber til højre ved at vælge overskrifterne, og angiv eventuelle nødvendige kontrolværdier.</span><span class="sxs-lookup"><span data-stu-id="51f21-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="51f21-169">Vælg ellipseknappen i dispositionsruden til venstre ud for navnet på enten containeren eller pladser inde i containeren, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="51f21-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="51f21-170">Føj derefter underordnede moduler til den valgte container.</span><span class="sxs-lookup"><span data-stu-id="51f21-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="51f21-171">Du kan finde flere oplysninger i proceduren [Tilføje et modul](#add-a-module) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="51f21-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="51f21-172">Hvis der findes flere underordnede moduler som sidestillede i en overordnet container, kan du ændre deres visningsrækkefølge i den overordnede container.</span><span class="sxs-lookup"><span data-stu-id="51f21-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="51f21-173">Vælg ellipseknappen for et modul, og brug derefter knapperne pil op og pil ned.</span><span class="sxs-lookup"><span data-stu-id="51f21-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51f21-174">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="51f21-174">Additional resources</span></span>

[<span data-ttu-id="51f21-175">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="51f21-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="51f21-176">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="51f21-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="51f21-177">Arbejde med forudindstillede layout</span><span class="sxs-lookup"><span data-stu-id="51f21-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="51f21-178">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="51f21-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="51f21-179">Føje et containermodul til en side</span><span class="sxs-lookup"><span data-stu-id="51f21-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="51f21-180">Føje moduler for indholdsplacering til en side</span><span class="sxs-lookup"><span data-stu-id="51f21-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="51f21-181">Arbejd med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="51f21-181">Work with publish groups</span></span>](publish-groups.md)

