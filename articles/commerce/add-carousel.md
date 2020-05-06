---
title: Karruselmodul
description: Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269722"
---
# <a name="carousel-module"></a><span data-ttu-id="f8a1d-103">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="f8a1d-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8a1d-104">Dette emne omhandler karruselmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8a1d-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f8a1d-105">Overview</span></span>

<span data-ttu-id="f8a1d-106">Et karruselmodul bruges til at placere flere kampagnevarer (herunder detaljerede billeder) i et roterende karruselbanner, som kunderne kan gennemse.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f8a1d-107">En detailhandler kan f. eks. bruge et karruselmodul på en hjemmeside for at vise flere nye produkter eller kampagner.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f8a1d-108">Du kan tilføje indholdsblokmoduler inde i et karruselmodul.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f8a1d-109">Egenskaberne for karruselmodulet definerer derefter, hvordan disse moduler gengives.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f8a1d-110">Eksempler på karruselmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="f8a1d-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f8a1d-111">En karrusel, der indeholder flere kampagnemoduler, kan bruges på en startside.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f8a1d-112">En karrusel, der indeholder flere kampagnemoduler, kan bruges på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f8a1d-113">En karrusel kan bruges på en hvilken som helst marketingside til at vise flere kampagner eller produkter.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="f8a1d-114">Egenskaber for karruselmodul</span><span class="sxs-lookup"><span data-stu-id="f8a1d-114">Carousel module properties</span></span>

| <span data-ttu-id="f8a1d-115">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="f8a1d-115">Property name</span></span>             | <span data-ttu-id="f8a1d-116">Værdi</span><span class="sxs-lookup"><span data-stu-id="f8a1d-116">Value</span></span>                 | <span data-ttu-id="f8a1d-117">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f8a1d-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f8a1d-118">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="f8a1d-118">Autoplay</span></span>                  | <span data-ttu-id="f8a1d-119">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="f8a1d-119">**True** or **False**</span></span> | <span data-ttu-id="f8a1d-120">Hvis værdien er angivet til **Sand**, sker overgangen mellem varerne inde i karrusellen automatisk.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f8a1d-121">Hvis værdien er angivet til **Falsk**, sker der ingen overgang, medmindre kunden bruger tastaturet eller musen til at flytte fra en vare til den næste.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f8a1d-122">Interval for glidende interval</span><span class="sxs-lookup"><span data-stu-id="f8a1d-122">Slide transition interval</span></span> | <span data-ttu-id="f8a1d-123">En værdi i sekunder</span><span class="sxs-lookup"><span data-stu-id="f8a1d-123">A value in seconds</span></span>    | <span data-ttu-id="f8a1d-124">Intervallet for overgange mellem varerne.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f8a1d-125">Overførselstype</span><span class="sxs-lookup"><span data-stu-id="f8a1d-125">Transition type</span></span>           | <span data-ttu-id="f8a1d-126">**Dias** eller **Udtoning**</span><span class="sxs-lookup"><span data-stu-id="f8a1d-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="f8a1d-127">Overgangseffekten mellem varer.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-127">The transition effect between items.</span></span> |
| <span data-ttu-id="f8a1d-128">Skjul karruselslipper</span><span class="sxs-lookup"><span data-stu-id="f8a1d-128">Hide carousel flipper</span></span>     | <span data-ttu-id="f8a1d-129">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="f8a1d-129">**True** or **False**</span></span> | <span data-ttu-id="f8a1d-130">Hvis værdien er angivet til **Sand**, skjules karruselslipperen og sekvensindikatoren.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f8a1d-131">Tillad afvisning af karrusel</span><span class="sxs-lookup"><span data-stu-id="f8a1d-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="f8a1d-132">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="f8a1d-132">**True** or **False**</span></span> | <span data-ttu-id="f8a1d-133">Hvis værdien er angivet til **Sand**, kan brugerne afvise karrusellen.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f8a1d-134">Føje et karruselmodul til en side</span><span class="sxs-lookup"><span data-stu-id="f8a1d-134">Add a carousel module to a page</span></span>

<span data-ttu-id="f8a1d-135">Hvis du vil føje et karruselmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f8a1d-136">Vælg **Ny** for at oprette en sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="f8a1d-137">Angiv **Karruselskabelonskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f8a1d-138">På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f8a1d-139">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f8a1d-140">Brug den karruselskabelon, som du netop har oprettet, til at oprette en side med navnet **Karruselside**.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f8a1d-141">Tilføj et containermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f8a1d-142">Angiv værdien **Bredde** til **Fyld skærm** i ruden til højre.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f8a1d-143">Føj et karruselmodul til containermodulet under **Sidedisposition**.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f8a1d-144">Føj et indholdsblokmodul til karruselmodulet.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f8a1d-145">Angiv egenskaberne for indholdsblokmodulet ved at angive **Overskrift**, **Link**, **Layout** og andre egenskaber.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f8a1d-146">Tilføj og konfigurer et andet indholdsblokmodul.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f8a1d-147">Angiv yderligere egenskaber for karruselmodulet efter behov.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f8a1d-148">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f8a1d-149">Siden skal vise en karrusel, der indeholder to moduler (et hero-modul og et funktionsmodul).</span><span class="sxs-lookup"><span data-stu-id="f8a1d-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f8a1d-150">Du kan ændre flere egenskaber for karrusel-, hero- og med funktionsmoduler for at opnå den ønskede effekt.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f8a1d-151">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="f8a1d-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8a1d-152">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f8a1d-152">Additional resources</span></span>

[<span data-ttu-id="f8a1d-153">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="f8a1d-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f8a1d-154">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="f8a1d-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f8a1d-155">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="f8a1d-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f8a1d-156">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="f8a1d-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f8a1d-157">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="f8a1d-157">Video player module</span></span>](add-video-player.md)
