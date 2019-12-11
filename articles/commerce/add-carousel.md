---
title: Karruselmodul
description: Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785231"
---
# <a name="carousel-module"></a><span data-ttu-id="7d6d7-103">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7d6d7-104">Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d6d7-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="7d6d7-105">Overview</span></span>

<span data-ttu-id="7d6d7-106">Et karruselmodul bruges til at placere flere kampagnevarer i en karrusel, som kunderne kan gennemse.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="7d6d7-107">Det er et særligt containermodul, der er vært for andre moduler.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="7d6d7-108">En detailhandler kan f. eks. bruge et karruselmodul på en hjemmeside for at vise flere nye produkter eller kampagner.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="7d6d7-109">Du kan tilføje hero- og funktionsmoduler inde i et karruselmodul.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="7d6d7-110">Egenskaberne for karruselmodulet definerer derefter, hvordan disse moduler gengives.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="7d6d7-111">Eksempler på karruselmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="7d6d7-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="7d6d7-112">En karrusel, der indeholder flere kampagnemoduler, kan bruges på en startside.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="7d6d7-113">En karrusel, der indeholder flere kampagnemoduler, kan bruges på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="7d6d7-114">En karrusel kan bruges på en hvilken som helst marketingside til at vise flere kampagner eller produkter.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="7d6d7-115">Egenskaber for karruselmodul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-115">Carousel module properties</span></span>

| <span data-ttu-id="7d6d7-116">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="7d6d7-116">Property name</span></span>             | <span data-ttu-id="7d6d7-117">Værdi</span><span class="sxs-lookup"><span data-stu-id="7d6d7-117">Value</span></span>                                | <span data-ttu-id="7d6d7-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7d6d7-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="7d6d7-119">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="7d6d7-119">Autoplay</span></span>                  | <span data-ttu-id="7d6d7-120">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="7d6d7-120">**True** or **False**</span></span>                | <span data-ttu-id="7d6d7-121">Hvis værdien er angivet til **Sand**, sker overgangen mellem varerne inde i karrusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="7d6d7-122">Hvis værdien er angivet til **Falsk**, sker der ingen overgang, medmindre kunden bruger tastaturet eller musen til at flytte fra en vare til den næste.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="7d6d7-123">Interval for glidende interval</span><span class="sxs-lookup"><span data-stu-id="7d6d7-123">Slide transition interval</span></span> | <span data-ttu-id="7d6d7-124">En værdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="7d6d7-124">A value in seconds</span></span>                   | <span data-ttu-id="7d6d7-125">Intervallet for overgange mellem varerne.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="7d6d7-126">Animation af overgang</span><span class="sxs-lookup"><span data-stu-id="7d6d7-126">Transition animation</span></span>      | <span data-ttu-id="7d6d7-127">**Dias** eller **Udtoning**</span><span class="sxs-lookup"><span data-stu-id="7d6d7-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="7d6d7-128">Overgangseffekten.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-128">The transition effect.</span></span> |
| <span data-ttu-id="7d6d7-129">Bredde</span><span class="sxs-lookup"><span data-stu-id="7d6d7-129">Width</span></span>                     | <span data-ttu-id="7d6d7-130">**Tilpas til container** eller **Udfyld skærm**</span><span class="sxs-lookup"><span data-stu-id="7d6d7-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="7d6d7-131">Hvis værdien er angivet til **Tilpas til container**, begrænses varerne i karrusellen til karrusellens bredde.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="7d6d7-132">Hvis værdien er angivet til **Udfyld skærm**, begrænses varerne ikke til karrusel bredden, men kan gå i fuldskærmstilstand.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="7d6d7-133">Du kan ændre værdien for at opnå det ønskede layout.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="7d6d7-134">Føje et karruselmodul til en side</span><span class="sxs-lookup"><span data-stu-id="7d6d7-134">Add a carousel module to a page</span></span>

<span data-ttu-id="7d6d7-135">Hvis du vil føje et karruselmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7d6d7-136">Opret en sideskabelon med navnet **karruselskabelon**.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="7d6d7-137">Tilføj et karruselmodul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="7d6d7-138">Føj et hero-modul til karruselmodulet.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="7d6d7-139">Føj et funktionsmodul til karruselmodulet.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="7d6d7-140">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="7d6d7-141">Brug den karruselskabelon, som du netop har oprettet, til at oprette en side med navnet **karruselside**.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="7d6d7-142">Tilføj et karruselmodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="7d6d7-143">Angiv egenskaben **Bredde** i karruselmodulet til **Udfyld skærm**.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="7d6d7-144">Angiv egenskaben **Animation af overgang** til **Dias**.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="7d6d7-145">Føj et hero-modul til karruselmodulet.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="7d6d7-146">Tilføj et billede og en overskrift i hero-modulet, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="7d6d7-147">Føj et funktionsmodul til karruselmodulet.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="7d6d7-148">Tilføj et billede, en overskrift og et tekstafsnit i funktionsmodulet.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="7d6d7-149">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-149">Save and preview the page.</span></span> <span data-ttu-id="7d6d7-150">Siden skal vise en karrusel, der indeholder to moduler (et hero-modul og et funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="7d6d7-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="7d6d7-151">Du kan ændre flere egenskaber for karrusel-, hero- og med funktionsmoduler for at opnå den ønskede effekt.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="7d6d7-152">Tjek siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d6d7-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7d6d7-153">Additional resources</span></span>

[<span data-ttu-id="7d6d7-154">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="7d6d7-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7d6d7-155">Påmindelsesmodul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="7d6d7-156">Indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="7d6d7-157">Indholdsplaceringsmodul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="7d6d7-158">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="7d6d7-159">Hero-modul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="7d6d7-160">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="7d6d7-160">Video player module</span></span>](add-video-player.md)
