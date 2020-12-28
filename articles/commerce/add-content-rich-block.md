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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411015"
---
# <a name="text-block-module"></a><span data-ttu-id="f9827-103">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="f9827-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9827-104">Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f9827-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f9827-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f9827-105">Overview</span></span>

<span data-ttu-id="f9827-106">Et tekstblokmodul er et modul, der bruges til at tilføje tekstindhold.</span><span class="sxs-lookup"><span data-stu-id="f9827-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="f9827-107">Det kan være oplysninger og kampagneindhold.</span><span class="sxs-lookup"><span data-stu-id="f9827-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="f9827-108">Tekstblokmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="f9827-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="f9827-109">De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="f9827-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="f9827-110">Eksempler på tekstblokmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="f9827-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="f9827-111">Tekstblokmoduler kan bruges på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="f9827-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="f9827-112">Til at få vist produktfunktioner på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="f9827-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="f9827-113">Til oplysninger på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="f9827-113">For informational purposes on any page.</span></span> <span data-ttu-id="f9827-114">De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".</span><span class="sxs-lookup"><span data-stu-id="f9827-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="f9827-115">Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="f9827-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="f9827-116">(f. eks. "Gratis levering af ordrer over $50").</span><span class="sxs-lookup"><span data-stu-id="f9827-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="f9827-117">For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").</span><span class="sxs-lookup"><span data-stu-id="f9827-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="f9827-118">Det følgende billede viser et eksempel på et tekstblokmodul, der bruges på en startside.</span><span class="sxs-lookup"><span data-stu-id="f9827-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Eksempel på et tekstblokmodul](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="f9827-120">Egenskaber for Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="f9827-120">Text block module properties</span></span>

| <span data-ttu-id="f9827-121">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="f9827-121">Property name</span></span>     | <span data-ttu-id="f9827-122">Værdi</span><span class="sxs-lookup"><span data-stu-id="f9827-122">Value</span></span>                                            | <span data-ttu-id="f9827-123">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="f9827-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="f9827-124">RTF</span><span class="sxs-lookup"><span data-stu-id="f9827-124">Rich text</span></span>         | <span data-ttu-id="f9827-125">RTF</span><span class="sxs-lookup"><span data-stu-id="f9827-125">Rich text</span></span>                                        | <span data-ttu-id="f9827-126">Afsnitstekst.</span><span class="sxs-lookup"><span data-stu-id="f9827-126">Paragraph text.</span></span> <span data-ttu-id="f9827-127">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst.</span><span class="sxs-lookup"><span data-stu-id="f9827-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="f9827-128">Brugerdefineret klassenavn</span><span class="sxs-lookup"><span data-stu-id="f9827-128">Custom class name</span></span> | <span data-ttu-id="f9827-129">Klassenavn for overlappende typografiark (CSS)</span><span class="sxs-lookup"><span data-stu-id="f9827-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="f9827-130">Navnet på en brugerdefineret CSS-klasse, som en udvikler leverer til at formatere dette modul.</span><span class="sxs-lookup"><span data-stu-id="f9827-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="f9827-131">Klassenavnet skal defineres i temapakken.</span><span class="sxs-lookup"><span data-stu-id="f9827-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="f9827-132">Skrifttypens størrelse</span><span class="sxs-lookup"><span data-stu-id="f9827-132">Font size</span></span>         | <span data-ttu-id="f9827-133">**Lille**, **Mellem**, **Stor** eller **Ekstra stor**</span><span class="sxs-lookup"><span data-stu-id="f9827-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="f9827-134">Indholdets skriftstørrelse.</span><span class="sxs-lookup"><span data-stu-id="f9827-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="f9827-135">Føj et tekstblokmodul til en side</span><span class="sxs-lookup"><span data-stu-id="f9827-135">Add a text block module to a page</span></span>

<span data-ttu-id="f9827-136">Hvis du vil føje et tekstblokmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f9827-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f9827-137">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="f9827-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f9827-138">I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Indholdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="f9827-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="f9827-139">På pladsen **Brødtekst** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f9827-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9827-140">I dialogboksen **Tilføj modul** skal du vælge modulet **Standardside** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9827-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f9827-141">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="f9827-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f9827-142">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="f9827-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f9827-143">Vælg dialogboksen **Vælg en skabelon**, og vælg **Indholdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="f9827-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="f9827-144">Under **Sidenavn** skal du angive **Indholdsside** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9827-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f9827-145">På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f9827-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9827-146">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9827-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f9827-147">Angiv egenskaben **Bredde** til **Fyld container** i egenskabsruden for containermodulet.</span><span class="sxs-lookup"><span data-stu-id="f9827-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f9827-148">På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f9827-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f9827-149">I dialogboksen **Tilføj modul** skal du vælge modulet **Tekstblok** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9827-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="f9827-150">Føj tekst til **RTF-tekst**-feltet i egenskabsruden af tekstblokmodulet.</span><span class="sxs-lookup"><span data-stu-id="f9827-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="f9827-151">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="f9827-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f9827-152">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="f9827-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9827-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f9827-153">Additional resources</span></span>

[<span data-ttu-id="f9827-154">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="f9827-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f9827-155">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="f9827-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f9827-156">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="f9827-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="f9827-157">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="f9827-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f9827-158">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="f9827-158">Video player module</span></span>](add-video-player.md)

