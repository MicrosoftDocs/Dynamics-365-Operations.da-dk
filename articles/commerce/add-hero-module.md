---
title: Hero-modul
description: Dette emne omhandler hero-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785379"
---
# <a name="hero-module"></a><span data-ttu-id="68527-103">Hero-modul</span><span class="sxs-lookup"><span data-stu-id="68527-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="68527-104">Dette emne omhandler hero-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="68527-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="68527-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="68527-105">Overview</span></span>

<span data-ttu-id="68527-106">Et hero-modul bruges til markedsføring af produkter eller kampagner via en kombination af billeder og tekst.</span><span class="sxs-lookup"><span data-stu-id="68527-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="68527-107">En forhandler kan f. eks. tilføje et hero-modul til startsiden på et e-handels-websted for at markedsføre et nyt produkt og tiltrække kundernes opmærksomhed.</span><span class="sxs-lookup"><span data-stu-id="68527-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="68527-108">Et hero-modul styres af data fra CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="68527-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="68527-109">Det er et separat modul, der ikke er afhængige af andre moduler på siden.</span><span class="sxs-lookup"><span data-stu-id="68527-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="68527-110">Et hero-modul kan placeres på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (f. eks. produkter, salg eller funktioner).</span><span class="sxs-lookup"><span data-stu-id="68527-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="68527-111">Eksempler på hero-moduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="68527-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="68527-112">Et hero-modul kan bruges på startsiden for et e-handels-websted til at fremhæve kampagner og nye produkter.</span><span class="sxs-lookup"><span data-stu-id="68527-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="68527-113">Et hero-modul kan bruges på siden med produktdetaljer til at vise produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="68527-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="68527-114">Der kan placeres flere hero-moduler i et karruselmodul for at fremhæve flere produkter eller kampagner.</span><span class="sxs-lookup"><span data-stu-id="68527-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="68527-115">Egenskaber for hero-modul</span><span class="sxs-lookup"><span data-stu-id="68527-115">Hero module properties</span></span>

| <span data-ttu-id="68527-116">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="68527-116">Property name</span></span>  | <span data-ttu-id="68527-117">Værdier</span><span class="sxs-lookup"><span data-stu-id="68527-117">Values</span></span> | <span data-ttu-id="68527-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="68527-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="68527-119">Billede</span><span class="sxs-lookup"><span data-stu-id="68527-119">Image</span></span>          | <span data-ttu-id="68527-120">Billedfil</span><span class="sxs-lookup"><span data-stu-id="68527-120">Image file</span></span> | <span data-ttu-id="68527-121">Der kan bruges et billede til at vise et produkt eller en kampagne.</span><span class="sxs-lookup"><span data-stu-id="68527-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="68527-122">Der kan overføres et billede til billedgalleriet, eller der kan bruges et eksisterende billede.</span><span class="sxs-lookup"><span data-stu-id="68527-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="68527-123">Overskrift</span><span class="sxs-lookup"><span data-stu-id="68527-123">Heading</span></span>        | <span data-ttu-id="68527-124">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="68527-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="68527-125">Alle hero-moduler kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="68527-125">Every hero module can have a heading.</span></span> <span data-ttu-id="68527-126">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="68527-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="68527-127">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="68527-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="68527-128">Afsnit</span><span class="sxs-lookup"><span data-stu-id="68527-128">Paragraph</span></span>      | <span data-ttu-id="68527-129">Afsnitstekst</span><span class="sxs-lookup"><span data-stu-id="68527-129">Paragraph text</span></span> | <span data-ttu-id="68527-130">Hero-moduler understøtter afsnitstekst i RTF-format.</span><span class="sxs-lookup"><span data-stu-id="68527-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="68527-131">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="68527-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="68527-132">Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet.</span><span class="sxs-lookup"><span data-stu-id="68527-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="68527-133">Binding</span><span class="sxs-lookup"><span data-stu-id="68527-133">Link</span></span>           | <span data-ttu-id="68527-134">Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane**</span><span class="sxs-lookup"><span data-stu-id="68527-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="68527-135">Hero-moduler understøtter et eller flere links til "handlingsplaner".</span><span class="sxs-lookup"><span data-stu-id="68527-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="68527-136">Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet.</span><span class="sxs-lookup"><span data-stu-id="68527-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="68527-137">ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="68527-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="68527-138">Links kan konfigureres, så de åbnes under en ny fane.</span><span class="sxs-lookup"><span data-stu-id="68527-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="68527-139">Placering af tekst</span><span class="sxs-lookup"><span data-stu-id="68527-139">Text placement</span></span> | <span data-ttu-id="68527-140">**Øverst til venstre**, **Øverst til højre**, **Øverst centreret**, **Nederst til venstre**, **Nederst til højre**, **Nederst i midten**, **Centreret til venstre**, **Centreret til højre** eller **Centreret centreret**</span><span class="sxs-lookup"><span data-stu-id="68527-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="68527-141">Denne egenskab definerer placeringen af billedet i forhold til teksten.</span><span class="sxs-lookup"><span data-stu-id="68527-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="68527-142">Hvis **Højre** f.eks. er valgt, vises billedet til højre for teksten.</span><span class="sxs-lookup"><span data-stu-id="68527-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="68527-143">Teksttema</span><span class="sxs-lookup"><span data-stu-id="68527-143">Text theme</span></span>     | <span data-ttu-id="68527-144">**Lys** eller **Mørk**</span><span class="sxs-lookup"><span data-stu-id="68527-144">**Light** or **Dark**</span></span> | <span data-ttu-id="68527-145">Der kan defineres et farveskema for teksten på basis af baggrundsbilledet.</span><span class="sxs-lookup"><span data-stu-id="68527-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="68527-146">Hvis billedet f. eks. har en mørk baggrund, kan der anvendes et lyst tema for at gøre teksten mere synlig og for at overholde tilgængelighedskravene til farvekontrast.</span><span class="sxs-lookup"><span data-stu-id="68527-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="68527-147">Graduering</span><span class="sxs-lookup"><span data-stu-id="68527-147">Gradient</span></span>       | <span data-ttu-id="68527-148">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="68527-148">**True** or **False**</span></span> | <span data-ttu-id="68527-149">Der kan anvendes en graduering på billedet til at overholde tilgængelighedskravene til farvekontrast.</span><span class="sxs-lookup"><span data-stu-id="68527-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="68527-150">Føje et hero-modul til en ny side</span><span class="sxs-lookup"><span data-stu-id="68527-150">Add a hero module to a new page</span></span>

<span data-ttu-id="68527-151">Hvis du vil føje et hero-modul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="68527-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="68527-152">Gå til **Skabeloner**, og opret en sideskabelon med navnet **hero-skabelon**.</span><span class="sxs-lookup"><span data-stu-id="68527-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="68527-153">Tilføj et hero-modul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="68527-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="68527-154">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="68527-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="68527-155">Brug den hero-skabelon, som du netop har oprettet, til at oprette en side med navnet **hero-side**.</span><span class="sxs-lookup"><span data-stu-id="68527-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="68527-156">Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="68527-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="68527-157">I dialogboksen **Tilføj modul** under **Vælg moduler** skal du vælge hero-modulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="68527-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="68527-158">Vælg hero-modulet i dispositionstræet til venstre.</span><span class="sxs-lookup"><span data-stu-id="68527-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="68527-159">Vælg **Tilføj et billede** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="68527-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="68527-160">Vælg derefter et eksisterende billede, eller overfør et nyt billede.</span><span class="sxs-lookup"><span data-stu-id="68527-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="68527-161">Vælg **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="68527-161">Select **Heading**.</span></span>
1. <span data-ttu-id="68527-162">Tilføj overskriftsteksten i dialogboksen **Overskrift**, vælg overskriftsniveauet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="68527-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="68527-163">Tilføj tekst efter behov under **RTF-tekst**.</span><span class="sxs-lookup"><span data-stu-id="68527-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="68527-164">Vælg **Tilføj handlingslink**.</span><span class="sxs-lookup"><span data-stu-id="68527-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="68527-165">Tilføj linktekst, en URL-adresse og en ARIA-mærkat for linket i dialogboksen **Handlingslink**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="68527-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="68527-166">Gem siden, og se dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="68527-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="68527-167">Tjek siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="68527-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68527-168">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="68527-168">Additional resources</span></span>

[<span data-ttu-id="68527-169">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="68527-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="68527-170">Påmindelsesmodul</span><span class="sxs-lookup"><span data-stu-id="68527-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="68527-171">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="68527-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="68527-172">Indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="68527-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="68527-173">Indholdsplaceringsmodul</span><span class="sxs-lookup"><span data-stu-id="68527-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="68527-174">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="68527-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="68527-175">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="68527-175">Video player module</span></span>](add-video-player.md)
