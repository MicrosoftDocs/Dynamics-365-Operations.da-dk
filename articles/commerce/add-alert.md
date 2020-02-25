---
title: Kampagnebannermodul
description: Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025614"
---
# <a name="promo-banner-module"></a><span data-ttu-id="a7d08-103">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="a7d08-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a7d08-104">Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a7d08-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a7d08-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="a7d08-105">Overview</span></span>

<span data-ttu-id="a7d08-106">Kampagnebannermoduler bruges til at vise indbyggede informationsmeddelelser på en side.</span><span class="sxs-lookup"><span data-stu-id="a7d08-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="a7d08-107">De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel.</span><span class="sxs-lookup"><span data-stu-id="a7d08-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="a7d08-108">Kampagnebannermoduler understøtter en sms-besked og et link.</span><span class="sxs-lookup"><span data-stu-id="a7d08-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="a7d08-109">Hvis der føjes flere meddelelser til et kampagnebannermodul, bliver det til et roterende banner, hvor du kan gå gennem alle meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="a7d08-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="a7d08-110">Kampagnebannermoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="a7d08-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="a7d08-111">Anvendelseseksempler på kampagnebannere i e-handel</span><span class="sxs-lookup"><span data-stu-id="a7d08-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="a7d08-112">Kampagnebannere kan bruges i webstedets overskift til at vise kampagner eller meddelelser, der gælder for hele webstedet, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="a7d08-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="a7d08-113">"Det årlige udsalg slutter om 10 dage"</span><span class="sxs-lookup"><span data-stu-id="a7d08-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="a7d08-114">"Store besparelser på skolestartudsalg.</span><span class="sxs-lookup"><span data-stu-id="a7d08-114">"Save big with back to school sale.</span></span> <span data-ttu-id="a7d08-115">Køb nu".</span><span class="sxs-lookup"><span data-stu-id="a7d08-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="a7d08-116">Egenskaber for kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="a7d08-116">Promo banner module properties</span></span>

| <span data-ttu-id="a7d08-117">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="a7d08-117">Property name</span></span>             | <span data-ttu-id="a7d08-118">Value</span><span class="sxs-lookup"><span data-stu-id="a7d08-118">Value</span></span>                              | <span data-ttu-id="a7d08-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a7d08-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="a7d08-120">Bannermeddelelser</span><span class="sxs-lookup"><span data-stu-id="a7d08-120">Banner messages</span></span>           | <span data-ttu-id="a7d08-121">Tekst og link</span><span class="sxs-lookup"><span data-stu-id="a7d08-121">Text and links</span></span>                     | <span data-ttu-id="a7d08-122">En matrix af tekst og link.</span><span class="sxs-lookup"><span data-stu-id="a7d08-122">An array of text and links.</span></span> |
| <span data-ttu-id="a7d08-123">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="a7d08-123">Autoplay</span></span>                  | <span data-ttu-id="a7d08-124">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="a7d08-124">**True** or **False**</span></span>              | <span data-ttu-id="a7d08-125">En værdi, der angiver, om meddelelser automatisk gennemløbes, hvis der er konfigureret flere meddelelser.</span><span class="sxs-lookup"><span data-stu-id="a7d08-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="a7d08-126">Interval for glidende interval</span><span class="sxs-lookup"><span data-stu-id="a7d08-126">Slide transition interval</span></span> | <span data-ttu-id="a7d08-127">Et antal millisekunder (MS)</span><span class="sxs-lookup"><span data-stu-id="a7d08-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="a7d08-128">Det interval, der bruges til at gå gennem meddelelser.</span><span class="sxs-lookup"><span data-stu-id="a7d08-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="a7d08-129">Tillad afvis</span><span class="sxs-lookup"><span data-stu-id="a7d08-129">Allow dismiss</span></span>             | <span data-ttu-id="a7d08-130">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="a7d08-130">**True** or **False**</span></span>              | <span data-ttu-id="a7d08-131">Hvis værdien er angivet til **Sand**, kan kunderne afvise påmindelsen.</span><span class="sxs-lookup"><span data-stu-id="a7d08-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="a7d08-132">Vis karruselslipper</span><span class="sxs-lookup"><span data-stu-id="a7d08-132">Show carousel flipper</span></span>     | <span data-ttu-id="a7d08-133">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="a7d08-133">**True** or **False**</span></span>              | <span data-ttu-id="a7d08-134">En værdi, der angiver, om karruselslippere skal vises, så kunder kan gå gennem flere bannerelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="a7d08-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="a7d08-135">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="a7d08-135">Text alignment</span></span>            | <span data-ttu-id="a7d08-136">**Højre**, **Venstre** eller **Centreret**</span><span class="sxs-lookup"><span data-stu-id="a7d08-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="a7d08-137">Tekstjusteringen i kampangebannermodulet.</span><span class="sxs-lookup"><span data-stu-id="a7d08-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="a7d08-138">Binding</span><span class="sxs-lookup"><span data-stu-id="a7d08-138">Link</span></span>                      | <span data-ttu-id="a7d08-139">En URL-adresse</span><span class="sxs-lookup"><span data-stu-id="a7d08-139">A URL</span></span>                              | <span data-ttu-id="a7d08-140">URL-adressen for et valgfrit link.</span><span class="sxs-lookup"><span data-stu-id="a7d08-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="a7d08-141">Føj et kampangebannermodul til en ny side</span><span class="sxs-lookup"><span data-stu-id="a7d08-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="a7d08-142">Hvis du vil føje et kampangebannermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a7d08-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a7d08-143">Opret en sideskabelon med navnet **Kampangebannerskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a7d08-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="a7d08-144">Under **Sidedisposition**kan du føje et **Standardside**modul til **Brødtekst**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="a7d08-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="a7d08-145">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="a7d08-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="a7d08-146">Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **Kampangebannermodul**.</span><span class="sxs-lookup"><span data-stu-id="a7d08-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="a7d08-147">Tilføj et containermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="a7d08-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="a7d08-148">Angiv værdien **Bredde** til **Fyld container** i ruden til højre.</span><span class="sxs-lookup"><span data-stu-id="a7d08-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="a7d08-149">Føj et kampangebannermodul til containermodulet under **Sidedisposition**.</span><span class="sxs-lookup"><span data-stu-id="a7d08-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="a7d08-150">Tilføj en eller flere bannermeddelelser i indstillingerne for bannermodulet.</span><span class="sxs-lookup"><span data-stu-id="a7d08-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="a7d08-151">Hver meddelelse kan have tekst sammen med et link.</span><span class="sxs-lookup"><span data-stu-id="a7d08-151">Each message can have text together with a link.</span></span> <span data-ttu-id="a7d08-152">Du kan redigere de andre egenskaber for at tilpasse modulet yderligere.</span><span class="sxs-lookup"><span data-stu-id="a7d08-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="a7d08-153">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="a7d08-153">Save and preview the page.</span></span> <span data-ttu-id="a7d08-154">Øverst på siden vises en påmindelse med den tekst, du har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="a7d08-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="a7d08-155">Afslut redigeringen af siden, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="a7d08-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="a7d08-156">Et kampagnebanner bruges typisk i sidehovedpladsen eller en underoverskriftplads.</span><span class="sxs-lookup"><span data-stu-id="a7d08-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a7d08-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a7d08-157">Additional resources</span></span>

[<span data-ttu-id="a7d08-158">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="a7d08-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a7d08-159">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="a7d08-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a7d08-160">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="a7d08-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a7d08-161">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="a7d08-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="a7d08-162">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="a7d08-162">Video player module</span></span>](add-video-player.md)
