---
title: Arbejde med moduler
description: Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801355"
---
# <a name="work-with-modules"></a><span data-ttu-id="f5e69-103">Arbejde med moduler</span><span class="sxs-lookup"><span data-stu-id="f5e69-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5e69-104">Dette emne beskriver, hvornår og hvordan du bruger moduler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f5e69-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f5e69-105">Moduler er logiske byggeklodser, der udgør sidestrukturen, og de har forskellige formål og omfang.</span><span class="sxs-lookup"><span data-stu-id="f5e69-105">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="f5e69-106">Nogle moduler er containere på højt niveau, hvis eneste formål er at opbevare og organisere andre moduler (underordnede moduler).</span><span class="sxs-lookup"><span data-stu-id="f5e69-106">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="f5e69-107">Andre moduler, f.eks. et enkelt modul til billedplacering, har et meget specifikt formål.</span><span class="sxs-lookup"><span data-stu-id="f5e69-107">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="f5e69-108">Andre moduler som f.eks. et karruselmodul falder et sted mellem disse to kategorier.</span><span class="sxs-lookup"><span data-stu-id="f5e69-108">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="f5e69-109">Dynamics 365 Commerce-webstedet indeholder som standard et modulbibliotek, der giver dig mulighed for at få de fleste grundlæggende e-handelsscenarier.</span><span class="sxs-lookup"><span data-stu-id="f5e69-109">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="f5e69-110">Du bør oprette et e-handels-websted, der dækker alt, ved at bruge disse moduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-110">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="f5e69-111">Du kan dog også tilpasse disse moduler eller opbygge nye, tilpassede moduler til specifikke behov.</span><span class="sxs-lookup"><span data-stu-id="f5e69-111">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="f5e69-112">Hvis du vil bygge brugerdefinerede moduler, kan du få hjælp til at oprette et tilpasset modulbibliotek i et SDK (Software Development Kit) til moduldesign.</span><span class="sxs-lookup"><span data-stu-id="f5e69-112">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="f5e69-113">Containermoduler og pladser</span><span class="sxs-lookup"><span data-stu-id="f5e69-113">Container modules and slots</span></span>

<span data-ttu-id="f5e69-114">Som tidligere nævnt er nogle moduler designet til at rumme underordnede moduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-114">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="f5e69-115">Disse moduler kaldes *containere*, og de giver mulighed for hierarkier af indlejrede moduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-115">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="f5e69-116">Containermoduler indeholder *pladser*.</span><span class="sxs-lookup"><span data-stu-id="f5e69-116">Container modules include *slots*.</span></span> <span data-ttu-id="f5e69-117">Pladser bruges til at håndtere layoutet og formålet med underordnede moduler i containeren.</span><span class="sxs-lookup"><span data-stu-id="f5e69-117">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="f5e69-118">Et eksempel er et grundlæggende sidecontainermodul (et modul på øverste niveau for en side), der definerer flere vigtige pladser:</span><span class="sxs-lookup"><span data-stu-id="f5e69-118">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="f5e69-119">En sidehovedplads</span><span class="sxs-lookup"><span data-stu-id="f5e69-119">A header slot</span></span>
- <span data-ttu-id="f5e69-120">En undersidehovedplads</span><span class="sxs-lookup"><span data-stu-id="f5e69-120">A sub-header slot</span></span>
- <span data-ttu-id="f5e69-121">En hovedplads</span><span class="sxs-lookup"><span data-stu-id="f5e69-121">A main slot</span></span>
- <span data-ttu-id="f5e69-122">En sidefodsplads</span><span class="sxs-lookup"><span data-stu-id="f5e69-122">A footer slot</span></span>
- <span data-ttu-id="f5e69-123">En undersidefodsplads</span><span class="sxs-lookup"><span data-stu-id="f5e69-123">A sub-footer slot</span></span>

<span data-ttu-id="f5e69-124">Modulets udvikler definerer disse pladser og bestemmer, hvilke underordnede moduler og hvor mange underordnede moduler der kan placeres direkte i det.</span><span class="sxs-lookup"><span data-stu-id="f5e69-124">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="f5e69-125">F.eks. understøtter sidehovedpladsen måske kun ét modul af typen **Sidehovedmodul**, mens brødtekstpladsen understøtter et ubegrænset antal moduler af enhver type (undtagen andre sidecontainermoduler).</span><span class="sxs-lookup"><span data-stu-id="f5e69-125">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="f5e69-126">I oprettelsesværktøjerne behøver sideforfattere ikke at vide på forhånd, hvilke moduler der kan anbringes på hver plads.</span><span class="sxs-lookup"><span data-stu-id="f5e69-126">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="f5e69-127">Når en sideforfatter vælger en plads og derefter prøver at vælge et modul, der skal føjes til den, vises en filtreret visning af modultyper, der understøttes for den pågældende plads.</span><span class="sxs-lookup"><span data-stu-id="f5e69-127">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="f5e69-128">Indholdsmoduler</span><span class="sxs-lookup"><span data-stu-id="f5e69-128">Content modules</span></span>

<span data-ttu-id="f5e69-129">Indholdsmoduler har indhold og medieelementer, f.eks. tekst (f.eks. overskrifter, afsnit og links) eller aktivreferencer (f.eks. billeder, video og PDF-filer).</span><span class="sxs-lookup"><span data-stu-id="f5e69-129">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="f5e69-130">Typiske indholdsmodultyper omfatter indholdsblok, tekstblok og kampagnebannermoduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-130">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="f5e69-131">Moduler af disse tre typer kan indeholde tekst eller medier, og de kræver ingen underordnede moduler for at gøre noget synligt på en side.</span><span class="sxs-lookup"><span data-stu-id="f5e69-131">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="f5e69-132">Størstedelen af typiske, daglige side- og indholdsoprettelsesaktiviteter omfatter indholdsmoduler, primært fordi disse moduler definerer det faktiske indhold, der gengives i de overordnede containermoduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-132">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="f5e69-133">Mange indholdsmoduler er tilgængelige, og disse moduler er typisk de sidste stykker, du skal føje til sidens hierarki af indlejrede moduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-133">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="f5e69-134">I følgende illustration vises, hvordan moduler er indlejret i de overordnede containermodulpladser.</span><span class="sxs-lookup"><span data-stu-id="f5e69-134">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Indlejring af moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="f5e69-136">Tilføje eller fjerne moduler</span><span class="sxs-lookup"><span data-stu-id="f5e69-136">Add or remove modules</span></span>

<span data-ttu-id="f5e69-137">I følgende procedurer beskrives, hvordan du kan tilføje og fjerne moduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-137">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="f5e69-138">Tilføje et modul</span><span class="sxs-lookup"><span data-stu-id="f5e69-138">Add a module</span></span>

<span data-ttu-id="f5e69-139">Hvis du vil tilføje et modul på en plads eller container på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-139">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-140">Vælg en container eller en plads, som et underordnet modul kan føjes til, i dispositionsruden til venstre eller direkte i hovedlærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-140">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5e69-141">Moduldesigneren definerer listen over de modultyper, der kan føjes til en bestemt modulplads.</span><span class="sxs-lookup"><span data-stu-id="f5e69-141">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="f5e69-142">Skabelonoprettere kan derefter begrænse de tilladte modulindstillinger for at sikre konsistent optimering af søgemaskiner og redigeringseffektivitet for alle de sider, der er bygget ud fra en bestemt skabelon.</span><span class="sxs-lookup"><span data-stu-id="f5e69-142">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="f5e69-143">Dialogboksen **Tilføj modul** filtreres automatisk, når et modul føjes til en plads, så der kun vises moduler, der understøttes i den valgte container eller plads.</span><span class="sxs-lookup"><span data-stu-id="f5e69-143">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="f5e69-144">Listen over tilladte moduler bestemmes af sidens skabelon eller definitionen af containerens modul.</span><span class="sxs-lookup"><span data-stu-id="f5e69-144">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="f5e69-145">Hvis du bruger dispositionsruden, skal du vælge ellipsen (**...**) ud for modulnavnet og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-145">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="f5e69-146">Hvis du bruger kontrolelementerne direkte i lærredet, skal du vælge plussymbolet (**+**) i en tom plads eller ved siden af det aktuelt valgte modul og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-146">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5e69-147">Hvis containeren eller pladsen ikke understøtter nye underordnede moduler, er indstillingen **Tilføj modul** ikke tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="f5e69-147">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="f5e69-148">Vælg et modul, der skal tilføjes på siden, i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-148">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="f5e69-149">**Indholdsblok** er en god modultype, som begyndere kan arbejde med.</span><span class="sxs-lookup"><span data-stu-id="f5e69-149">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="f5e69-150">Vælg **OK** for at føje det valgte modul til den valgte container eller plads på siden.</span><span class="sxs-lookup"><span data-stu-id="f5e69-150">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="f5e69-151">Fjerne et modul</span><span class="sxs-lookup"><span data-stu-id="f5e69-151">Remove a module</span></span>

<span data-ttu-id="f5e69-152">Hvis du vil fjerne et modul fra en plads eller container på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-152">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-153">Vælg ellipseknappen (**...**) i dispositionsruden til venstre ud for navnet på det modul, der skal fjernes, og vælg derefter symbolet med papirkurven.</span><span class="sxs-lookup"><span data-stu-id="f5e69-153">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="f5e69-154">Du kan også vælge papirkurvesymbolet på værktøjslinjen i det valgte modul på hovedlærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-154">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="f5e69-155">Når du bliver bedt om at bekræfte, at du vil fjerne modulet, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-155">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="f5e69-156">Flytte et modul til en ny position</span><span class="sxs-lookup"><span data-stu-id="f5e69-156">Move a module to a new position</span></span>

<span data-ttu-id="f5e69-157">Hvis du vil flytte et modul til en ny position på siden, skal du bruge en af følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="f5e69-157">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="f5e69-158">Flytte et modul ved hjælp af dispositionsruden</span><span class="sxs-lookup"><span data-stu-id="f5e69-158">Move a module using the outline pane</span></span>

<span data-ttu-id="f5e69-159">Hvis du vil flytte et modul ved hjælp af dispositionsruden, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-159">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-160">Markér og hold fast i det modul, du vil flytte, i dispositionsruden, og træk derefter modulet til en ny placering i dispositionen.</span><span class="sxs-lookup"><span data-stu-id="f5e69-160">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="f5e69-161">Den blå linje i konturen og på lærredet angiver, hvor modulet kan placeres.</span><span class="sxs-lookup"><span data-stu-id="f5e69-161">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="f5e69-162">Slip modulet på den nye placering.</span><span class="sxs-lookup"><span data-stu-id="f5e69-162">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="f5e69-163">Flytte et modul direkte i lærredet</span><span class="sxs-lookup"><span data-stu-id="f5e69-163">Move a module directly within the canvas</span></span>

<span data-ttu-id="f5e69-164">Hvis du vil flytte et modul direkte i lærredet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-164">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-165">Vælg det modul, du vil flytte, i lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-165">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="f5e69-166">Vælg enten et symbol for opadgående eller nedadgående pil på værktøjslinjen for modulet, og træk derefter pilen til en ny placering på siden.</span><span class="sxs-lookup"><span data-stu-id="f5e69-166">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="f5e69-167">Den blå linje i lærredet og konturen angiver, hvor modulet kan placeres.</span><span class="sxs-lookup"><span data-stu-id="f5e69-167">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="f5e69-168">Hvis et modul ikke kan flyttes op eller ned, vil pilesymbolet være nedtonet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-168">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="f5e69-169">Slip modulet på den nye placering.</span><span class="sxs-lookup"><span data-stu-id="f5e69-169">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="f5e69-170">Flytte et modul ved hjælp af ellipsemenuen</span><span class="sxs-lookup"><span data-stu-id="f5e69-170">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="f5e69-171">Hvis du vil flytte et modul ved hjælp af ellipsemenuen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-171">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-172">Vælg et modul enten i dispositionen eller på lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-172">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="f5e69-173">Vælg ellipsen (**...**) ud for navnet på modulet i dispositionsruden eller på værktøjslinjen for modulet på lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-173">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="f5e69-174">Hvis modulet kan flyttes op eller ned inden for containeren eller pladsen, kan du se indstillingerne for **Flyt op** eller **Flyt ned**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-174">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="f5e69-175">Vælg den ønskede indstilling for flytning for at flytte modulet op eller ned i forhold til dets sidestillede.</span><span class="sxs-lookup"><span data-stu-id="f5e69-175">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="f5e69-176">Konfigurere moduler</span><span class="sxs-lookup"><span data-stu-id="f5e69-176">Configure modules</span></span>

<span data-ttu-id="f5e69-177">I følgende procedurer beskrives, hvordan du kan konfigurere indholds- og containermoduler.</span><span class="sxs-lookup"><span data-stu-id="f5e69-177">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="f5e69-178">Konfigurere et indholdsmodul</span><span class="sxs-lookup"><span data-stu-id="f5e69-178">Configure a content module</span></span>

<span data-ttu-id="f5e69-179">Hvis du vil konfigurere et indholdsmodul på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-179">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-180">Udvid træet i dispositionsruden til venstre, og vælg et indholdsmodul (f.eks. **Indholdsblok**).</span><span class="sxs-lookup"><span data-stu-id="f5e69-180">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="f5e69-181">Eller vælg modulet i hovedlærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-181">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="f5e69-182">Angiv egenskaber for de ønskede kontrolelementer til moduler i ruden Egenskaber for modul til højre.</span><span class="sxs-lookup"><span data-stu-id="f5e69-182">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="f5e69-183">Vælg **Gem** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="f5e69-183">On the command bar, select **Save**.</span></span> <span data-ttu-id="f5e69-184">Dette vil også opdatere eksemplet på lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-184">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="f5e69-185">Redigere tekstegenskaber for modul</span><span class="sxs-lookup"><span data-stu-id="f5e69-185">Edit module text properties</span></span>

<span data-ttu-id="f5e69-186">Tekstegenskaber for modul, der ikke er skrivebeskyttet, kan redigeres direkte i lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-186">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="f5e69-187">Benyt følgende fremgangsmåde for at redigere egenskaber for modultekst.</span><span class="sxs-lookup"><span data-stu-id="f5e69-187">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-188">Vælg tekstkontrolelementet på lærredet, og placer derefter markøren på det sted, hvor du vil redigere teksten.</span><span class="sxs-lookup"><span data-stu-id="f5e69-188">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="f5e69-189">Indtast tekstindholdet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-189">Enter your text content.</span></span>
1. <span data-ttu-id="f5e69-190">Vælg et vilkårligt sted uden for tekstindholdet for at fortsætte med at redigere andet indhold.</span><span class="sxs-lookup"><span data-stu-id="f5e69-190">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="f5e69-191">Valg af indbygget billede</span><span class="sxs-lookup"><span data-stu-id="f5e69-191">Inline image selection</span></span>

<span data-ttu-id="f5e69-192">Modulbilleder, der ikke er skrivebeskyttet, kan ændres direkte i lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-192">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="f5e69-193">Hvis du vil vælge et nyt billede for et indholdsmodul, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-193">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-194">Dobbeltklik på billedet på lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-194">In the canvas, double-click the image.</span></span> <span data-ttu-id="f5e69-195">Dette vil åbne vinduet med medievælgeren.</span><span class="sxs-lookup"><span data-stu-id="f5e69-195">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="f5e69-196">Find og vælg et nyt billede, du vil bruge, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-196">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="f5e69-197">Det nye billede gengives nu på lærredet.</span><span class="sxs-lookup"><span data-stu-id="f5e69-197">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="f5e69-198">Konfigurere et containermodul</span><span class="sxs-lookup"><span data-stu-id="f5e69-198">Configure a container module</span></span>

<span data-ttu-id="f5e69-199">Hvis du vil konfigurere et containermodul på en side, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f5e69-199">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="f5e69-200">Vælg et containermodul på siden (f.eks. et karrusel- eller flydende containermodul).</span><span class="sxs-lookup"><span data-stu-id="f5e69-200">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="f5e69-201">Udvid de indlejrede kontrolelementer i ruden Egenskaber til højre ved at vælge overskrifterne, og angiv eventuelle nødvendige kontrolværdier.</span><span class="sxs-lookup"><span data-stu-id="f5e69-201">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="f5e69-202">Vælg ellipseknappen i dispositionsruden til venstre ud for navnet på enten containeren eller pladser inde i containeren, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f5e69-202">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="f5e69-203">Føj derefter underordnede moduler til den valgte container.</span><span class="sxs-lookup"><span data-stu-id="f5e69-203">Then, add child modules to the selected container.</span></span> <span data-ttu-id="f5e69-204">Du kan finde flere oplysninger i afsnittet [Arbejde med moduler](#add-a-module) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="f5e69-204">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="f5e69-205">Hvis der findes flere underordnede moduler som sidestillede i en overordnet container, kan du ændre deres visningsrækkefølge i den overordnede container.</span><span class="sxs-lookup"><span data-stu-id="f5e69-205">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="f5e69-206">Vælg ellipseknappen for et modul, og brug derefter knapperne pil op og pil ned.</span><span class="sxs-lookup"><span data-stu-id="f5e69-206">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5e69-207">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f5e69-207">Additional resources</span></span>

[<span data-ttu-id="f5e69-208">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="f5e69-208">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f5e69-209">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="f5e69-209">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f5e69-210">Arbejde med forudindstillede layout</span><span class="sxs-lookup"><span data-stu-id="f5e69-210">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="f5e69-211">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="f5e69-211">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f5e69-212">Føje et containermodul til en side</span><span class="sxs-lookup"><span data-stu-id="f5e69-212">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="f5e69-213">Arbejde med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="f5e69-213">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
