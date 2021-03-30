---
title: Tekstblokmodul
description: Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206385"
---
# <a name="text-block-module"></a><span data-ttu-id="8ff5a-103">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="8ff5a-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ff5a-104">Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8ff5a-105">Et tekstblokmodul er et modul, der bruges til at tilføje tekstindhold.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="8ff5a-106">Det kan være oplysninger og kampagneindhold.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="8ff5a-107">Tekstblokmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="8ff5a-108">De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="8ff5a-109">Eksempler på tekstblokmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="8ff5a-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="8ff5a-110">Tekstblokmoduler kan bruges på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="8ff5a-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="8ff5a-111">Til at få vist produktfunktioner på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="8ff5a-112">Til oplysninger på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-112">For informational purposes on any page.</span></span> <span data-ttu-id="8ff5a-113">De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".</span><span class="sxs-lookup"><span data-stu-id="8ff5a-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="8ff5a-114">Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="8ff5a-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="8ff5a-115">(f. eks. "Gratis levering af ordrer over $50").</span><span class="sxs-lookup"><span data-stu-id="8ff5a-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="8ff5a-116">For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").</span><span class="sxs-lookup"><span data-stu-id="8ff5a-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="8ff5a-117">Det følgende billede viser et eksempel på et tekstblokmodul, der bruges på en startside.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Eksempel på et tekstblokmodul](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="8ff5a-119">Egenskaber for Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="8ff5a-119">Text block module properties</span></span>

| <span data-ttu-id="8ff5a-120">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="8ff5a-120">Property name</span></span>     | <span data-ttu-id="8ff5a-121">Værdi</span><span class="sxs-lookup"><span data-stu-id="8ff5a-121">Value</span></span>                                            | <span data-ttu-id="8ff5a-122">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="8ff5a-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="8ff5a-123">RTF</span><span class="sxs-lookup"><span data-stu-id="8ff5a-123">Rich text</span></span>         | <span data-ttu-id="8ff5a-124">RTF</span><span class="sxs-lookup"><span data-stu-id="8ff5a-124">Rich text</span></span>                                        | <span data-ttu-id="8ff5a-125">Afsnitstekst.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-125">Paragraph text.</span></span> <span data-ttu-id="8ff5a-126">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="8ff5a-127">Brugerdefineret klassenavn</span><span class="sxs-lookup"><span data-stu-id="8ff5a-127">Custom class name</span></span> | <span data-ttu-id="8ff5a-128">Klassenavn for overlappende typografiark (CSS)</span><span class="sxs-lookup"><span data-stu-id="8ff5a-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="8ff5a-129">Navnet på en brugerdefineret CSS-klasse, som en udvikler leverer til at formatere dette modul.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="8ff5a-130">Klassenavnet skal defineres i temapakken.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="8ff5a-131">Skrifttypens størrelse</span><span class="sxs-lookup"><span data-stu-id="8ff5a-131">Font size</span></span>         | <span data-ttu-id="8ff5a-132">**Lille**, **Mellem**, **Stor** eller **Ekstra stor**</span><span class="sxs-lookup"><span data-stu-id="8ff5a-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="8ff5a-133">Indholdets skriftstørrelse.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="8ff5a-134">Føj et tekstblokmodul til en side</span><span class="sxs-lookup"><span data-stu-id="8ff5a-134">Add a text block module to a page</span></span>

<span data-ttu-id="8ff5a-135">Hvis du vil føje et tekstblokmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8ff5a-136">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="8ff5a-137">I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Indholdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="8ff5a-138">På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8ff5a-139">I dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8ff5a-140">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="8ff5a-141">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="8ff5a-142">Vælg dialogboksen **Vælg en skabelon**, og vælg **Indholdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="8ff5a-143">Under **Sidenavn** skal du angive **Indholdsside** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="8ff5a-144">På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8ff5a-145">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8ff5a-146">Angiv egenskaben **Bredde** til **Fyld container** i egenskabsruden for containermodulet.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="8ff5a-147">På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8ff5a-148">I dialogboksen **Tilføj modul** skal du vælge modulet **Tekstblok** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="8ff5a-149">Føj tekst til **RTF-tekst**-feltet i egenskabsruden af tekstblokmodulet.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="8ff5a-150">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="8ff5a-151">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="8ff5a-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ff5a-152">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8ff5a-152">Additional resources</span></span>

[<span data-ttu-id="8ff5a-153">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="8ff5a-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8ff5a-154">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="8ff5a-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="8ff5a-155">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="8ff5a-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8ff5a-156">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="8ff5a-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="8ff5a-157">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="8ff5a-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]