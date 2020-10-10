---
title: Karruselmodul
description: Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: f09f3f98d174f965a75e27ee6a5c2ed8599042fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816980"
---
# <a name="carousel-module"></a><span data-ttu-id="9e771-103">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="9e771-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e771-104">Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e771-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e771-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="9e771-105">Overview</span></span>

<span data-ttu-id="9e771-106">Et karruselmodul bruges til at placere flere kampagnevarer (herunder detaljerede billeder) i et roterende karruselbanner, som kunderne kan gennemse.</span><span class="sxs-lookup"><span data-stu-id="9e771-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="9e771-107">En detailhandler kan f. eks. bruge et karruselmodul på en hjemmeside for at vise flere nye produkter eller kampagner.</span><span class="sxs-lookup"><span data-stu-id="9e771-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="9e771-108">Du kan tilføje indholdsblokmoduler inde i et karruselmodul.</span><span class="sxs-lookup"><span data-stu-id="9e771-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="9e771-109">Egenskaberne for karruselmodulet definerer derefter, hvordan disse moduler gengives.</span><span class="sxs-lookup"><span data-stu-id="9e771-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="9e771-110">Eksempler på karruselmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="9e771-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="9e771-111">En karrusel, der indeholder flere kampagnemoduler, kan bruges på en startside.</span><span class="sxs-lookup"><span data-stu-id="9e771-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="9e771-112">En karrusel, der indeholder flere kampagnemoduler, kan bruges på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="9e771-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="9e771-113">En karrusel kan bruges på en hvilken som helst marketingside til at vise flere kampagner eller produkter.</span><span class="sxs-lookup"><span data-stu-id="9e771-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="9e771-114">Det følgende billede viser et eksempel på et karruselmodul, der bruges på en startside.</span><span class="sxs-lookup"><span data-stu-id="9e771-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="9e771-115">Dette karruselmodul indeholder flere blokelementer med indhold.</span><span class="sxs-lookup"><span data-stu-id="9e771-115">This carousel module contains multiple content block items.</span></span>

![Eksempel på et karruselmodul](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="9e771-117">Egenskaber for karruselmodul</span><span class="sxs-lookup"><span data-stu-id="9e771-117">Carousel module properties</span></span>

| <span data-ttu-id="9e771-118">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="9e771-118">Property name</span></span>             | <span data-ttu-id="9e771-119">Værdi</span><span class="sxs-lookup"><span data-stu-id="9e771-119">Value</span></span>                 | <span data-ttu-id="9e771-120">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="9e771-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="9e771-121">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="9e771-121">Autoplay</span></span>                  | <span data-ttu-id="9e771-122">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e771-122">**True** or **False**</span></span> | <span data-ttu-id="9e771-123">Hvis værdien er angivet til **Sand**, sker overgangen mellem varerne inde i karrusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="9e771-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="9e771-124">Hvis værdien er angivet til **Falsk**, sker der ingen overgang, medmindre kunden bruger tastaturet eller musen til at flytte fra en vare til den næste.</span><span class="sxs-lookup"><span data-stu-id="9e771-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="9e771-125">Interval for glidende interval</span><span class="sxs-lookup"><span data-stu-id="9e771-125">Slide transition interval</span></span> | <span data-ttu-id="9e771-126">En værdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="9e771-126">A value in seconds</span></span>    | <span data-ttu-id="9e771-127">Intervallet for overgange mellem varerne.</span><span class="sxs-lookup"><span data-stu-id="9e771-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="9e771-128">Overførselstype</span><span class="sxs-lookup"><span data-stu-id="9e771-128">Transition type</span></span>           | <span data-ttu-id="9e771-129">**Dias** eller **Udtoning**</span><span class="sxs-lookup"><span data-stu-id="9e771-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="9e771-130">Overgangseffekten mellem varer.</span><span class="sxs-lookup"><span data-stu-id="9e771-130">The transition effect between items.</span></span> |
| <span data-ttu-id="9e771-131">Skjul karruselslipper</span><span class="sxs-lookup"><span data-stu-id="9e771-131">Hide carousel flipper</span></span>     | <span data-ttu-id="9e771-132">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e771-132">**True** or **False**</span></span> | <span data-ttu-id="9e771-133">Hvis værdien er angivet til **Sand**, skjules karruselslipperen og sekvensindikatoren.</span><span class="sxs-lookup"><span data-stu-id="9e771-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="9e771-134">Tillad afvisning af karrusel</span><span class="sxs-lookup"><span data-stu-id="9e771-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="9e771-135">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9e771-135">**True** or **False**</span></span> | <span data-ttu-id="9e771-136">Hvis værdien er angivet til **Sand**, kan brugerne afvise karrusellen.</span><span class="sxs-lookup"><span data-stu-id="9e771-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="9e771-137">Føje et karruselmodul til en side</span><span class="sxs-lookup"><span data-stu-id="9e771-137">Add a carousel module to a page</span></span>

<span data-ttu-id="9e771-138">Hvis du vil føje et karruselmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9e771-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9e771-139">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="9e771-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="9e771-140">Angiv **Karruselskabelonskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e771-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9e771-141">På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.</span><span class="sxs-lookup"><span data-stu-id="9e771-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="9e771-142">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="9e771-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="9e771-143">Brug den karruselskabelon, som du netop har oprettet, til at oprette en side med navnet **Karruselside**.</span><span class="sxs-lookup"><span data-stu-id="9e771-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="9e771-144">Tilføj et containermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="9e771-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="9e771-145">Angiv værdien **Bredde** til **Fyld skærm** i ruden til højre.</span><span class="sxs-lookup"><span data-stu-id="9e771-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="9e771-146">Føj et karruselmodul til containermodulet under **Sidedisposition**.</span><span class="sxs-lookup"><span data-stu-id="9e771-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="9e771-147">Føj et indholdsblokmodul til karruselmodulet.</span><span class="sxs-lookup"><span data-stu-id="9e771-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="9e771-148">Angiv egenskaberne for indholdsblokmodulet ved at angive **Overskrift**, **Link**, **Layout** og andre egenskaber.</span><span class="sxs-lookup"><span data-stu-id="9e771-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="9e771-149">Tilføj og konfigurer et andet indholdsblokmodul.</span><span class="sxs-lookup"><span data-stu-id="9e771-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="9e771-150">Angiv yderligere egenskaber for karruselmodulet efter behov.</span><span class="sxs-lookup"><span data-stu-id="9e771-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="9e771-151">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="9e771-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9e771-152">Siden skal vise en karrusel, der indeholder to moduler (et hero-modul og et funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="9e771-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="9e771-153">Du kan ændre flere egenskaber for karrusel-, hero- og med funktionsmoduler for at opnå den ønskede effekt.</span><span class="sxs-lookup"><span data-stu-id="9e771-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="9e771-154">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="9e771-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e771-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9e771-155">Additional resources</span></span>

[<span data-ttu-id="9e771-156">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="9e771-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9e771-157">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="9e771-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="9e771-158">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="9e771-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9e771-159">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="9e771-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="9e771-160">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="9e771-160">Video player module</span></span>](add-video-player.md)
