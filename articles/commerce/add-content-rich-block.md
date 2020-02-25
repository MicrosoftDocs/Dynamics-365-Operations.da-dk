---
title: Tekstblokmodul
description: Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025591"
---
# <a name="text-block-module"></a><span data-ttu-id="b61fb-103">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="b61fb-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b61fb-104">Dette emne omhandler tekstblokmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b61fb-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b61fb-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b61fb-105">Overview</span></span>

<span data-ttu-id="b61fb-106">Et tekstblokmodul er et modul, der bruges til at tilføje tekstindhold.</span><span class="sxs-lookup"><span data-stu-id="b61fb-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="b61fb-107">Det kan være oplysninger og kampagneindhold.</span><span class="sxs-lookup"><span data-stu-id="b61fb-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="b61fb-108">Tekstblokmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="b61fb-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="b61fb-109">De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="b61fb-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="b61fb-110">Eksempler på tekstblokmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="b61fb-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="b61fb-111">Tekstblokmoduler kan bruges på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="b61fb-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="b61fb-112">Til at få vist produktfunktioner på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="b61fb-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="b61fb-113">Til oplysninger på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="b61fb-113">For informational purposes on any page.</span></span> <span data-ttu-id="b61fb-114">De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".</span><span class="sxs-lookup"><span data-stu-id="b61fb-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="b61fb-115">Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="b61fb-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="b61fb-116">(f. eks. "Gratis levering af ordrer over $50").</span><span class="sxs-lookup"><span data-stu-id="b61fb-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="b61fb-117">For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").</span><span class="sxs-lookup"><span data-stu-id="b61fb-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="b61fb-118">Egenskaber for Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="b61fb-118">Text block module properties</span></span>

| <span data-ttu-id="b61fb-119">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="b61fb-119">Property name</span></span>     | <span data-ttu-id="b61fb-120">Value</span><span class="sxs-lookup"><span data-stu-id="b61fb-120">Value</span></span>                                            | <span data-ttu-id="b61fb-121">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b61fb-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="b61fb-122">RTF</span><span class="sxs-lookup"><span data-stu-id="b61fb-122">Rich text</span></span>         | <span data-ttu-id="b61fb-123">RTF</span><span class="sxs-lookup"><span data-stu-id="b61fb-123">Rich text</span></span>                                        | <span data-ttu-id="b61fb-124">Afsnitstekst.</span><span class="sxs-lookup"><span data-stu-id="b61fb-124">Paragraph text.</span></span> <span data-ttu-id="b61fb-125">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst.</span><span class="sxs-lookup"><span data-stu-id="b61fb-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="b61fb-126">Brugerdefineret klassenavn</span><span class="sxs-lookup"><span data-stu-id="b61fb-126">Custom class name</span></span> | <span data-ttu-id="b61fb-127">Klassenavn for overlappende typografiark (CSS)</span><span class="sxs-lookup"><span data-stu-id="b61fb-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="b61fb-128">Navnet på en brugerdefineret CSS-klasse, som en udvikler leverer til at formatere dette modul.</span><span class="sxs-lookup"><span data-stu-id="b61fb-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="b61fb-129">Klassenavnet skal defineres i temapakken.</span><span class="sxs-lookup"><span data-stu-id="b61fb-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="b61fb-130">Skrifttypens størrelse</span><span class="sxs-lookup"><span data-stu-id="b61fb-130">Font size</span></span>         | <span data-ttu-id="b61fb-131">**Lille**, **Mellem**, **Stor**eller **Ekstra stor**</span><span class="sxs-lookup"><span data-stu-id="b61fb-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="b61fb-132">Indholdets skriftstørrelse.</span><span class="sxs-lookup"><span data-stu-id="b61fb-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="b61fb-133">Føj et tekstblokmodul til en side</span><span class="sxs-lookup"><span data-stu-id="b61fb-133">Add a text block module to a page</span></span>

<span data-ttu-id="b61fb-134">Hvis du vil føje et tekstblokmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b61fb-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b61fb-135">Opret en sideskabelon med navnet **Indholdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="b61fb-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="b61fb-136">På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.</span><span class="sxs-lookup"><span data-stu-id="b61fb-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="b61fb-137">Afslut redigeringen af skabelonen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="b61fb-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="b61fb-138">Brug den indholdsskabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsside**.</span><span class="sxs-lookup"><span data-stu-id="b61fb-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="b61fb-139">Tilføj et containermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="b61fb-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="b61fb-140">Angiv egenskaben **Bredde** til **Fyld container**i egenskabsruden for containermodulet.</span><span class="sxs-lookup"><span data-stu-id="b61fb-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="b61fb-141">Føj et tekstblokmodul til containermodulet.</span><span class="sxs-lookup"><span data-stu-id="b61fb-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="b61fb-142">Føj tekst til **RTF-tekst**-feltet i egenskabsruden af tekstblokmodulet.</span><span class="sxs-lookup"><span data-stu-id="b61fb-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="b61fb-143">Afslut redigeringen af siden, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="b61fb-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b61fb-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b61fb-144">Additional resources</span></span>

[<span data-ttu-id="b61fb-145">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="b61fb-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b61fb-146">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="b61fb-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b61fb-147">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="b61fb-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b61fb-148">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="b61fb-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="b61fb-149">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="b61fb-149">Video player module</span></span>](add-video-player.md)

