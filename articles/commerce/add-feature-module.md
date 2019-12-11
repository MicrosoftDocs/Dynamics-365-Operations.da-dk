---
title: Funktionsmodul
description: Dette emne omhandler funktionsmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785277"
---
# <a name="feature-module"></a><span data-ttu-id="95a84-103">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="95a84-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="95a84-104">Dette emne omhandler funktionsmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="95a84-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="95a84-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="95a84-105">Overview</span></span>

<span data-ttu-id="95a84-106">Et funktionsmodul bruges til markedsføring af produkter eller kampagner via en kombination af billeder og tekst.</span><span class="sxs-lookup"><span data-stu-id="95a84-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="95a84-107">En forhandler kan f. eks. føje et funktionsmodul til en side med produktdetaljer for at fremhæve produktets funktioner.</span><span class="sxs-lookup"><span data-stu-id="95a84-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="95a84-108">Et funktionsmodul styres af data fra CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="95a84-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="95a84-109">Det er et separat modul, der ikke er afhængige af andre moduler på siden.</span><span class="sxs-lookup"><span data-stu-id="95a84-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="95a84-110">Et funktionsmodul kan placeres på alle sider på websteder, hvor en forhandler ønsker at markedsføre eller vise noget (f. eks. produkter, salg eller funktioner).</span><span class="sxs-lookup"><span data-stu-id="95a84-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="95a84-111">Eksempler på funktionsmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="95a84-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="95a84-112">Et funktionsmodul kan bruges på følgende sider:</span><span class="sxs-lookup"><span data-stu-id="95a84-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="95a84-113">På en side med produktdetaljer til visning af produktfunktioner</span><span class="sxs-lookup"><span data-stu-id="95a84-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="95a84-114">På startsiden til visning af produkter</span><span class="sxs-lookup"><span data-stu-id="95a84-114">The home page, to promote products</span></span>
- <span data-ttu-id="95a84-115">På en kategoriside til fremhævning af en produktkategori</span><span class="sxs-lookup"><span data-stu-id="95a84-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="95a84-116">Egenskaber for funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="95a84-116">Feature module properties</span></span>

| <span data-ttu-id="95a84-117">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="95a84-117">Property name</span></span>     | <span data-ttu-id="95a84-118">Værdier</span><span class="sxs-lookup"><span data-stu-id="95a84-118">Values</span></span> | <span data-ttu-id="95a84-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="95a84-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="95a84-120">Billede</span><span class="sxs-lookup"><span data-stu-id="95a84-120">Image</span></span>             | <span data-ttu-id="95a84-121">Billedfil</span><span class="sxs-lookup"><span data-stu-id="95a84-121">Image file</span></span> | <span data-ttu-id="95a84-122">Der kan bruges et billede til markedsføring af produktet eller kampagnen.</span><span class="sxs-lookup"><span data-stu-id="95a84-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="95a84-123">Der kan overføres et billede til billedgalleriet, eller der kan bruges et eksisterende billede.</span><span class="sxs-lookup"><span data-stu-id="95a84-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="95a84-124">Overskrift</span><span class="sxs-lookup"><span data-stu-id="95a84-124">Heading</span></span>           | <span data-ttu-id="95a84-125">Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**)</span><span class="sxs-lookup"><span data-stu-id="95a84-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="95a84-126">Alle funktionsmoduler kan have en overskrift.</span><span class="sxs-lookup"><span data-stu-id="95a84-126">Every feature module can have a heading.</span></span> <span data-ttu-id="95a84-127">Overskrift koden **H2** bruges som standard til overskriften.</span><span class="sxs-lookup"><span data-stu-id="95a84-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="95a84-128">Koden kan dog ændres, så den opfylder tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="95a84-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="95a84-129">Afsnit</span><span class="sxs-lookup"><span data-stu-id="95a84-129">Paragraph</span></span>         | <span data-ttu-id="95a84-130">Afsnitstekst</span><span class="sxs-lookup"><span data-stu-id="95a84-130">Paragraph text</span></span> | <span data-ttu-id="95a84-131">Funktionsmoduler understøtter afsnitstekst i RTF-format.</span><span class="sxs-lookup"><span data-stu-id="95a84-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="95a84-132">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst samt hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="95a84-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="95a84-133">Nogle af disse funktioner kan tilsidesættes af det sidetema, der anvendes på modulet.</span><span class="sxs-lookup"><span data-stu-id="95a84-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="95a84-134">Binding</span><span class="sxs-lookup"><span data-stu-id="95a84-134">Link</span></span>              | <span data-ttu-id="95a84-135">Linktekst, URL-adresse for link, ARIA-mærkat (Accessible Rich Internet Applications) og **Åbn link under ny fane**</span><span class="sxs-lookup"><span data-stu-id="95a84-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="95a84-136">Funktionsmoduler understøtter et eller flere links til "handlingsplaner".</span><span class="sxs-lookup"><span data-stu-id="95a84-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="95a84-137">Hvis der tilføjes et link, er linktekst, en URL-adresse og en ARIA-mærkat påkrævet.</span><span class="sxs-lookup"><span data-stu-id="95a84-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="95a84-138">ARIA-mærkater skal være beskrivende for at imødekomme tilgængelighedskravene.</span><span class="sxs-lookup"><span data-stu-id="95a84-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="95a84-139">Links kan konfigureres, så de åbnes under en ny fane.</span><span class="sxs-lookup"><span data-stu-id="95a84-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="95a84-140">Billedplacering</span><span class="sxs-lookup"><span data-stu-id="95a84-140">Image placement</span></span>   | <span data-ttu-id="95a84-141">**Højre**, **Venstre**, **Øverst**eller **Nederst**</span><span class="sxs-lookup"><span data-stu-id="95a84-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="95a84-142">Denne egenskab definerer placeringen af billedet i forhold til teksten.</span><span class="sxs-lookup"><span data-stu-id="95a84-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="95a84-143">Hvis **Højre** f.eks. er valgt, vises billedet til højre for teksten.</span><span class="sxs-lookup"><span data-stu-id="95a84-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="95a84-144">Størrelse af billedkolonne</span><span class="sxs-lookup"><span data-stu-id="95a84-144">Image column size</span></span> | <span data-ttu-id="95a84-145">En værdi mellem **1** og **12**</span><span class="sxs-lookup"><span data-stu-id="95a84-145">A value from **1** through **12**</span></span> | <span data-ttu-id="95a84-146">Denne egenskab definerer billedets størrelse i forhold til teksten.</span><span class="sxs-lookup"><span data-stu-id="95a84-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="95a84-147">Størrelsen udtrykkes som et antal kolonner på siden.</span><span class="sxs-lookup"><span data-stu-id="95a84-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="95a84-148">Der er 12 kolonner på en side.</span><span class="sxs-lookup"><span data-stu-id="95a84-148">There are 12 columns on a page.</span></span> <span data-ttu-id="95a84-149">Billedet og teksten har som standard samme størrelse (seks kolonner hver).</span><span class="sxs-lookup"><span data-stu-id="95a84-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="95a84-150">Størrelsen kan dog justeres efter behov.</span><span class="sxs-lookup"><span data-stu-id="95a84-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="95a84-151">Føje et funktions til en ny side</span><span class="sxs-lookup"><span data-stu-id="95a84-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="95a84-152">Hvis du vil føje et funktionsmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="95a84-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="95a84-153">Gå til **Skabeloner**, og opret en sideskabelon med navnet **funktionsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="95a84-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="95a84-154">Tilføj et funktionsmodul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="95a84-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="95a84-155">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="95a84-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="95a84-156">Brug den funktionsskabelon, som du netop har oprettet, til at oprette en side med navnet **funktionsside**.</span><span class="sxs-lookup"><span data-stu-id="95a84-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="95a84-157">Vælg pladsen **Hoved** på standardsiden, vælg ellipseknappen (**...**), og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="95a84-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95a84-158">I dialogboksen **Tilføj modul** under **Vælg moduler** skal du vælge et funktionsmodul og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="95a84-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="95a84-159">Vælg funktionsmodulet i dispositionstræet til venstre.</span><span class="sxs-lookup"><span data-stu-id="95a84-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="95a84-160">Vælg **Tilføj et billede** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="95a84-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="95a84-161">Vælg derefter et eksisterende billede, eller overfør et nyt billede.</span><span class="sxs-lookup"><span data-stu-id="95a84-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="95a84-162">Vælg **Overskrift**.</span><span class="sxs-lookup"><span data-stu-id="95a84-162">Select **Heading**.</span></span>
1. <span data-ttu-id="95a84-163">Tilføj overskriftsteksten i dialogboksen **Overskrift**, vælg overskriftsniveauet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="95a84-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="95a84-164">Tilføj tekst efter behov under **RTF-tekst**.</span><span class="sxs-lookup"><span data-stu-id="95a84-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="95a84-165">Vælg **Tilføj handlingslink**.</span><span class="sxs-lookup"><span data-stu-id="95a84-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="95a84-166">Tilføj linktekst, en URL-adresse og en ARIA-mærkat for linket i dialogboksen **Handlingslink**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="95a84-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="95a84-167">Gem siden, og se dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="95a84-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="95a84-168">Tjek siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="95a84-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95a84-169">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="95a84-169">Additional resources</span></span>

[<span data-ttu-id="95a84-170">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="95a84-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="95a84-171">Påmindelsesmodul</span><span class="sxs-lookup"><span data-stu-id="95a84-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="95a84-172">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="95a84-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="95a84-173">Indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="95a84-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="95a84-174">Indholdsplaceringsmodul</span><span class="sxs-lookup"><span data-stu-id="95a84-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="95a84-175">Hero-modul</span><span class="sxs-lookup"><span data-stu-id="95a84-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="95a84-176">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="95a84-176">Video player module</span></span>](add-video-player.md)
