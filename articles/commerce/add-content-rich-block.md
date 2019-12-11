---
title: Indholdsrig blok-modul
description: Dette emne omhandler indholdsrig blok-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785415"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="038be-103">Indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="038be-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="038be-104">Dette emne omhandler indholdsrig blok-moduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="038be-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="038be-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="038be-105">Overview</span></span>

<span data-ttu-id="038be-106">Et indholdsrig blok-modul er en særlig container, der ét eller flere indholdsrig blok-elementer kan placeres i.</span><span class="sxs-lookup"><span data-stu-id="038be-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="038be-107">Indholdsrig blok-moduler bruges til tekstindhold på en side.</span><span class="sxs-lookup"><span data-stu-id="038be-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="038be-108">Det kan både være oplysninger og kampagneindhold.</span><span class="sxs-lookup"><span data-stu-id="038be-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="038be-109">Indholdsrig blok-moduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="038be-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="038be-110">De er separate moduler, der ikke er afhængige af sidekontekst eller andre moduler.</span><span class="sxs-lookup"><span data-stu-id="038be-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="038be-111">Eksempler på indholdsrig blok-moduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="038be-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="038be-112">Indholdsrig blok-moduler kan bruges på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="038be-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="038be-113">Til at få vist produktfunktioner på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="038be-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="038be-114">Til oplysninger på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="038be-114">For informational purposes on any page.</span></span> <span data-ttu-id="038be-115">De kan f. eks. indeholde en beskrivelse af fordelene ved fordelskundeprogrammer, leverings- og returneringspolitikker, besvarelse af ofte stillede spørgsmål eller oplysninger om indholdet af "Om os".</span><span class="sxs-lookup"><span data-stu-id="038be-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="038be-116">Til tilføjelse af brugerdefinerede meddelelser på en side med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="038be-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="038be-117">(f. eks. "Gratis levering af ordrer over $50").</span><span class="sxs-lookup"><span data-stu-id="038be-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="038be-118">For ansvarsfraskrivelser og kontaktoplysninger på sider med produktdetaljer, indkøbsvognsider, betalingssider og andre sider (f. eks. "Levering og returnering sker i henhold til butikkens politikker").</span><span class="sxs-lookup"><span data-stu-id="038be-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="038be-119">Egenskaber for indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="038be-119">Content rich block module properties</span></span>

| <span data-ttu-id="038be-120">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="038be-120">Property name</span></span>     | <span data-ttu-id="038be-121">Værdi</span><span class="sxs-lookup"><span data-stu-id="038be-121">Value</span></span>                                 | <span data-ttu-id="038be-122">Egenskab</span><span class="sxs-lookup"><span data-stu-id="038be-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="038be-123">Antal kolonner</span><span class="sxs-lookup"><span data-stu-id="038be-123">Number of columns</span></span> | <span data-ttu-id="038be-124">Et tal mellem **1** og **4**</span><span class="sxs-lookup"><span data-stu-id="038be-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="038be-125">Antallet af kolonner i en indholdsrig blok.</span><span class="sxs-lookup"><span data-stu-id="038be-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="038be-126">Der kan være op til fire kolonner.</span><span class="sxs-lookup"><span data-stu-id="038be-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="038be-127">Bredde</span><span class="sxs-lookup"><span data-stu-id="038be-127">Width</span></span>             | <span data-ttu-id="038be-128">**Tilpas til container** eller **Udfyld skærm**</span><span class="sxs-lookup"><span data-stu-id="038be-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="038be-129">Hvis værdien er angivet til **Tilpas til container**, begrænses varerne i containeren til containerens bredde.</span><span class="sxs-lookup"><span data-stu-id="038be-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="038be-130">Hvis værdien er angivet til **Udfyld skærm**, begrænses varerne ikke til containerbredden, men kan gå i fuldskærmstilstand.</span><span class="sxs-lookup"><span data-stu-id="038be-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="038be-131">Du kan ændre værdien for at opnå det ønskede layout.</span><span class="sxs-lookup"><span data-stu-id="038be-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="038be-132">Egenskaber for element for indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="038be-132">Content rich block item module properties</span></span>

| <span data-ttu-id="038be-133">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="038be-133">Property name</span></span> | <span data-ttu-id="038be-134">Værdi</span><span class="sxs-lookup"><span data-stu-id="038be-134">Value</span></span>          | <span data-ttu-id="038be-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="038be-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="038be-136">Afsnit</span><span class="sxs-lookup"><span data-stu-id="038be-136">Paragraph</span></span>     | <span data-ttu-id="038be-137">Afsnitstekst</span><span class="sxs-lookup"><span data-stu-id="038be-137">Paragraph text</span></span> | <span data-ttu-id="038be-138">Den tekst, der følger med alle elementer for indholdsrig blok.</span><span class="sxs-lookup"><span data-stu-id="038be-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="038be-139">Nogle grundlæggende RTF-funktioner understøttes, f. eks. fed, understreget og kursiv tekst.</span><span class="sxs-lookup"><span data-stu-id="038be-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="038be-140">Føje et indholdsrigt blokmodul til en side</span><span class="sxs-lookup"><span data-stu-id="038be-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="038be-141">Hvis du vil føje et indholdsrig blok-modul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="038be-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="038be-142">Opret en sideskabelon med navnet **Indholdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="038be-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="038be-143">Tilføj et indholdsrig blok-modul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="038be-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="038be-144">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="038be-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="038be-145">Brug den indholdsskabelon, som du netop har oprettet, til at oprette en side med navnet **Indholdsside**.</span><span class="sxs-lookup"><span data-stu-id="038be-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="038be-146">Tilføj et indholdsrig blok-modul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="038be-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="038be-147">Angiv antallet af kolonner til **2**i egenskaberne for indholdsrig blok-modulet.</span><span class="sxs-lookup"><span data-stu-id="038be-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="038be-148">Vælg **Tilføj et modul**i indholdsrig blok-modulet, og tilføj et element for indholdsrig blok (f. eks. **element1**).</span><span class="sxs-lookup"><span data-stu-id="038be-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="038be-149">Tilføj afsnitstekst i det nye element for indholdsrig blok.</span><span class="sxs-lookup"><span data-stu-id="038be-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="038be-150">Vælg **Tilføj et modul**i indholdsrig blok-modulet, og tilføj et element for indholdsrig blok (f. eks. **element2**).</span><span class="sxs-lookup"><span data-stu-id="038be-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="038be-151">Tilføj afsnitstekst i det nye element for indholdsrig blok.</span><span class="sxs-lookup"><span data-stu-id="038be-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="038be-152">Gem siden, og se ændringerne.</span><span class="sxs-lookup"><span data-stu-id="038be-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="038be-153">Der vises to RTF-blokke i en visning med to kolonner.</span><span class="sxs-lookup"><span data-stu-id="038be-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="038be-154">Tjek siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="038be-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="038be-155">Hvis du tilføjer et tredje element for indholdsrig blok, stables det under de to elementer, som du tidligere har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="038be-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="038be-156">Hvis du ændrer antallet af kolonner og elementer i beholderen, kan du opnå forskellige layout for tekstindhold.</span><span class="sxs-lookup"><span data-stu-id="038be-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="038be-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="038be-157">Additional resources</span></span>

[<span data-ttu-id="038be-158">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="038be-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="038be-159">Påmindelsesmodul</span><span class="sxs-lookup"><span data-stu-id="038be-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="038be-160">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="038be-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="038be-161">Indholdsplaceringsmodul</span><span class="sxs-lookup"><span data-stu-id="038be-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="038be-162">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="038be-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="038be-163">Hero-modul</span><span class="sxs-lookup"><span data-stu-id="038be-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="038be-164">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="038be-164">Video player module</span></span>](add-video-player.md)

