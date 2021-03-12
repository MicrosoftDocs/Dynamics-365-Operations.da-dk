---
title: Indholdsblokmodul
description: Dette emne omhandler indholdsblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6359c915d053bb00c969b166325f675c0003ead
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980351"
---
# <a name="content-block-module"></a><span data-ttu-id="e0241-103">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="e0241-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e0241-104">Dette emne omhandler indholdsblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e0241-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e0241-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="e0241-105">Overview</span></span>

<span data-ttu-id="e0241-106">Et indholdsblokmodul bruges til markedsføring af produkter eller kampagner via en kombination af billeder og tekst.</span><span class="sxs-lookup"><span data-stu-id="e0241-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="e0241-107">En forhandler kan f.eks. føje et indholdsblokmodul til startsiden på et e-handels-websted for at markedsføre et nyt produkt og tiltrække kundernes opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="e0241-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="e0241-108">Et indholdsblokmodul styres af data fra CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="e0241-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="e0241-109">Det er et separat modul, der ikke er afhængige af andre moduler på siden.</span><span class="sxs-lookup"><span data-stu-id="e0241-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="e0241-110">Et indholdsblokmodul kan placeres på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (f.eks. produkter, salg eller funktioner).</span><span class="sxs-lookup"><span data-stu-id="e0241-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="e0241-111">Eksempler på et indholdsblokmodul i e-handel</span><span class="sxs-lookup"><span data-stu-id="e0241-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="e0241-112">Et indholdsblokmodul kan bruges på startsiden for et e-handels-websted til at fremhæve kampagner og nye produkter.</span><span class="sxs-lookup"><span data-stu-id="e0241-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="e0241-113">Et indholdsblokmodul kan bruges på siden med produktdetaljer til at vise produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e0241-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="e0241-114">Der kan placeres flere indholdsblokmoduler i et karruselmodul for at fremhæve flere produkter eller kampagner.</span><span class="sxs-lookup"><span data-stu-id="e0241-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="e0241-115">Indholdsblokmoduler og temaer</span><span class="sxs-lookup"><span data-stu-id="e0241-115">Content block modules and themes</span></span>

<span data-ttu-id="e0241-116">Indholdsblokmoduler kan understøtte forskellige layout og typografier, der er baseret på et tema.</span><span class="sxs-lookup"><span data-stu-id="e0241-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="e0241-117">Fabrikam-temaet understøtter f.eks. tre layoutvariationer af et indholdsblokmodul: helt, funktion og flise.</span><span class="sxs-lookup"><span data-stu-id="e0241-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="e0241-118">Layoutet Helt viser et billede i baggrunden med tekstoverlejring.</span><span class="sxs-lookup"><span data-stu-id="e0241-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="e0241-119">Funktionslayoutet viser et billede og tekst ved siden af hinanden.</span><span class="sxs-lookup"><span data-stu-id="e0241-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="e0241-120">Fliselayoutet giver mulighed for flere indholdsblokke i et fliseformat.</span><span class="sxs-lookup"><span data-stu-id="e0241-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="e0241-121">Desuden kan temaet vise forskellige egenskaber for hvert layout.</span><span class="sxs-lookup"><span data-stu-id="e0241-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="e0241-122">En temaudvikler kan opbygge flere layout med flere typografier vha. indholdsblokmodulet.</span><span class="sxs-lookup"><span data-stu-id="e0241-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="e0241-123">Følgende billede viser et eksempel på et indholdsblokmodul med et Helte-layout.</span><span class="sxs-lookup"><span data-stu-id="e0241-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Eksempel på et hero-modul](./media/Hero.PNG)

<span data-ttu-id="e0241-125">Følgende billede viser et eksempel på et indholdsblokmodul med et funktionslayout.</span><span class="sxs-lookup"><span data-stu-id="e0241-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Eksempler på funktionsmoduler](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="e0241-127">Egenskaber for indholdblokmodul</span><span class="sxs-lookup"><span data-stu-id="e0241-127">Content block module properties</span></span>

| <span data-ttu-id="e0241-128">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="e0241-128">Property name</span></span>  | <span data-ttu-id="e0241-129">Værdier</span><span class="sxs-lookup"><span data-stu-id="e0241-129">Values</span></span> | <span data-ttu-id="e0241-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e0241-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e0241-131">Billede</span><span class="sxs-lookup"><span data-stu-id="e0241-131">Image</span></span>          | <span data-ttu-id="e0241-132">Billedfil</span><span class="sxs-lookup"><span data-stu-id="e0241-132">Image file</span></span> | <span data-ttu-id="e0241-133">Der kan bruges et billede til at vise et produkt eller en kampagne.</span><span class="sxs-lookup"><span data-stu-id="e0241-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="e0241-134">Der kan overføres et billede til billedgalleriet, eller der kan bruges et eksisterende billede.</span><span class="sxs-lookup"><span data-stu-id="e0241-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="e0241-135">Overskrift</span><span class="sxs-lookup"><span data-stu-id="e0241-135">Heading</span></span>        | <span data-ttu-id="e0241-136">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="e0241-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e0241-137">Alle hero-moduler kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="e0241-137">Every hero module can have a heading.</span></span> <span data-ttu-id="e0241-138">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="e0241-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e0241-139">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="e0241-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e0241-140">Afsnit</span><span class="sxs-lookup"><span data-stu-id="e0241-140">Paragraph</span></span>      | <span data-ttu-id="e0241-141">Afsnitstekst</span><span class="sxs-lookup"><span data-stu-id="e0241-141">Paragraph text</span></span> | <span data-ttu-id="e0241-142">Hero-moduler understøtter afsnitstekst i RTF-format.</span><span class="sxs-lookup"><span data-stu-id="e0241-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="e0241-143">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="e0241-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="e0241-144">Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet.</span><span class="sxs-lookup"><span data-stu-id="e0241-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="e0241-145">Binding</span><span class="sxs-lookup"><span data-stu-id="e0241-145">Link</span></span>           | <span data-ttu-id="e0241-146">Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane**</span><span class="sxs-lookup"><span data-stu-id="e0241-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="e0241-147">Hero-moduler understøtter et eller flere links til "handlingsplaner".</span><span class="sxs-lookup"><span data-stu-id="e0241-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="e0241-148">Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet.</span><span class="sxs-lookup"><span data-stu-id="e0241-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="e0241-149">ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="e0241-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="e0241-150">Links kan konfigureres, så de åbnes under en ny fane.</span><span class="sxs-lookup"><span data-stu-id="e0241-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="e0241-151">Egenskaber for indholdsblokmodul, der vises af Fabrikam-temaet</span><span class="sxs-lookup"><span data-stu-id="e0241-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="e0241-152">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="e0241-152">Property name</span></span>  | <span data-ttu-id="e0241-153">Værdier</span><span class="sxs-lookup"><span data-stu-id="e0241-153">Values</span></span> | <span data-ttu-id="e0241-154">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e0241-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e0241-155">Placering af tekst</span><span class="sxs-lookup"><span data-stu-id="e0241-155">Text placement</span></span> | <span data-ttu-id="e0241-156">**Venstre**, **Højre**, **Midt**</span><span class="sxs-lookup"><span data-stu-id="e0241-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="e0241-157">Denne egenskab definerer placeringen af teksten i billedet.</span><span class="sxs-lookup"><span data-stu-id="e0241-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="e0241-158">Den gælder kun for Helte-layoutet.</span><span class="sxs-lookup"><span data-stu-id="e0241-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="e0241-159">Teksttema</span><span class="sxs-lookup"><span data-stu-id="e0241-159">Text theme</span></span>     | <span data-ttu-id="e0241-160">**Lys** eller **Mørk**</span><span class="sxs-lookup"><span data-stu-id="e0241-160">**Light** or **Dark**</span></span> | <span data-ttu-id="e0241-161">Der kan defineres et farveskema for teksten på basis af baggrundsbilledet.</span><span class="sxs-lookup"><span data-stu-id="e0241-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="e0241-162">Hvis billedet f. eks. har en mørk baggrund, kan der anvendes et lyst tema for at gøre teksten mere synlig og for at overholde tilgængelighedskravene til farvekontrast.</span><span class="sxs-lookup"><span data-stu-id="e0241-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="e0241-163">Den gælder kun for Helte-layoutet.</span><span class="sxs-lookup"><span data-stu-id="e0241-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="e0241-164">Billedplacering</span><span class="sxs-lookup"><span data-stu-id="e0241-164">Image placement</span></span>       | <span data-ttu-id="e0241-165">**Venstre**, **Højre**</span><span class="sxs-lookup"><span data-stu-id="e0241-165">**Left**,  **Right**</span></span> | <span data-ttu-id="e0241-166">Denne egenskab specificerer, om billedet skal være til venstre eller højre for teksten.</span><span class="sxs-lookup"><span data-stu-id="e0241-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="e0241-167">Den gælder kun for funktionslayoutet.</span><span class="sxs-lookup"><span data-stu-id="e0241-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="e0241-168">Føj et indholdsblokmodul til en ny side</span><span class="sxs-lookup"><span data-stu-id="e0241-168">Add a content block module to a new page</span></span>

<span data-ttu-id="e0241-169">Hvis du vil føje et hero-modul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e0241-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e0241-170">Gå til **Skabeloner**, og opret en sideskabelon med navnet **Indholdsblokskabelon**.</span><span class="sxs-lookup"><span data-stu-id="e0241-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="e0241-171">Tilføj et hero-modul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="e0241-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="e0241-172">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="e0241-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e0241-173">Brug den hero-skabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsblokside**.</span><span class="sxs-lookup"><span data-stu-id="e0241-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="e0241-174">Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e0241-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e0241-175">I dialogboksen **Tilføj modul** under **Vælg moduler** skal du vælge hero-modulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0241-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="e0241-176">Vælg indholdsblokmodulet i dispositionstræet til venstre.</span><span class="sxs-lookup"><span data-stu-id="e0241-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="e0241-177">Vælg **Tilføj et billede** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e0241-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="e0241-178">Vælg derefter et eksisterende billede, eller overfør et nyt billede.</span><span class="sxs-lookup"><span data-stu-id="e0241-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="e0241-179">Vælg **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="e0241-179">Select **Heading**.</span></span>
1. <span data-ttu-id="e0241-180">Tilføj overskriftsteksten i dialogboksen **Overskrift**, vælg overskriftsniveauet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0241-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="e0241-181">Tilføj tekst efter behov under **RTF-tekst**.</span><span class="sxs-lookup"><span data-stu-id="e0241-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="e0241-182">Vælg **Tilføj link**.</span><span class="sxs-lookup"><span data-stu-id="e0241-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="e0241-183">Tilføj linktekst, en URL-adresse og en ARIA-mærkat for linket i dialogboksen **Link**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0241-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="e0241-184">Vælg layoutet **Helt**.</span><span class="sxs-lookup"><span data-stu-id="e0241-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="e0241-185">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="e0241-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e0241-186">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="e0241-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e0241-187">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e0241-187">Additional resources</span></span>

[<span data-ttu-id="e0241-188">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="e0241-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e0241-189">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="e0241-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e0241-190">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="e0241-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e0241-191">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="e0241-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e0241-192">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="e0241-192">Video player module</span></span>](add-video-player.md)
