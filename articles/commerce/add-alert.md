---
title: Kampagnebannermodul
description: Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269768"
---
# <a name="promo-banner-module"></a><span data-ttu-id="9bc83-103">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="9bc83-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9bc83-104">Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9bc83-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9bc83-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="9bc83-105">Overview</span></span>

<span data-ttu-id="9bc83-106">Kampagnebannermoduler bruges til at vise indbyggede informationsmeddelelser på en side.</span><span class="sxs-lookup"><span data-stu-id="9bc83-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="9bc83-107">De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel.</span><span class="sxs-lookup"><span data-stu-id="9bc83-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="9bc83-108">Kampagnebannermoduler understøtter en sms-besked og et link.</span><span class="sxs-lookup"><span data-stu-id="9bc83-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="9bc83-109">Hvis der føjes flere meddelelser til et kampagnebannermodul, bliver det til et roterende banner, hvor du kan gå gennem alle meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="9bc83-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="9bc83-110">Kampagnebannermoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="9bc83-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="9bc83-111">Anvendelseseksempler på kampagnebannere i e-handel</span><span class="sxs-lookup"><span data-stu-id="9bc83-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="9bc83-112">Kampagnebannere kan bruges i webstedets overskift til at vise kampagner eller meddelelser, der gælder for hele webstedet, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="9bc83-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="9bc83-113">"Det årlige udsalg slutter om 10 dage"</span><span class="sxs-lookup"><span data-stu-id="9bc83-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="9bc83-114">"Store besparelser på skolestartudsalg.</span><span class="sxs-lookup"><span data-stu-id="9bc83-114">"Save big with back to school sale.</span></span> <span data-ttu-id="9bc83-115">Køb nu".</span><span class="sxs-lookup"><span data-stu-id="9bc83-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="9bc83-116">Egenskaber for kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="9bc83-116">Promo banner module properties</span></span>

| <span data-ttu-id="9bc83-117">Egenskabsnavn</span><span class="sxs-lookup"><span data-stu-id="9bc83-117">Property name</span></span>             | <span data-ttu-id="9bc83-118">Value</span><span class="sxs-lookup"><span data-stu-id="9bc83-118">Value</span></span>                              | <span data-ttu-id="9bc83-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9bc83-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="9bc83-120">Bannermeddelelser</span><span class="sxs-lookup"><span data-stu-id="9bc83-120">Banner messages</span></span>           | <span data-ttu-id="9bc83-121">Tekst og link</span><span class="sxs-lookup"><span data-stu-id="9bc83-121">Text and links</span></span>                     | <span data-ttu-id="9bc83-122">En matrix af tekst og link.</span><span class="sxs-lookup"><span data-stu-id="9bc83-122">An array of text and links.</span></span> |
| <span data-ttu-id="9bc83-123">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="9bc83-123">Autoplay</span></span>                  | <span data-ttu-id="9bc83-124">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9bc83-124">**True** or **False**</span></span>              | <span data-ttu-id="9bc83-125">En værdi, der angiver, om meddelelser automatisk gennemløbes, hvis der er konfigureret flere meddelelser.</span><span class="sxs-lookup"><span data-stu-id="9bc83-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="9bc83-126">Interval for glidende interval</span><span class="sxs-lookup"><span data-stu-id="9bc83-126">Slide transition interval</span></span> | <span data-ttu-id="9bc83-127">Et antal millisekunder (MS)</span><span class="sxs-lookup"><span data-stu-id="9bc83-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="9bc83-128">Det interval, der bruges til at gå gennem meddelelser.</span><span class="sxs-lookup"><span data-stu-id="9bc83-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="9bc83-129">Tillad afvis</span><span class="sxs-lookup"><span data-stu-id="9bc83-129">Allow dismiss</span></span>             | <span data-ttu-id="9bc83-130">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9bc83-130">**True** or **False**</span></span>              | <span data-ttu-id="9bc83-131">Hvis værdien er angivet til **Sand**, kan kunderne afvise påmindelsen.</span><span class="sxs-lookup"><span data-stu-id="9bc83-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="9bc83-132">Vis karruselslipper</span><span class="sxs-lookup"><span data-stu-id="9bc83-132">Show carousel flipper</span></span>     | <span data-ttu-id="9bc83-133">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="9bc83-133">**True** or **False**</span></span>              | <span data-ttu-id="9bc83-134">En værdi, der angiver, om karruselslippere skal vises, så kunder kan gå gennem flere bannerelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="9bc83-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="9bc83-135">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="9bc83-135">Text alignment</span></span>            | <span data-ttu-id="9bc83-136">**Højre**, **Venstre** eller **Centreret**</span><span class="sxs-lookup"><span data-stu-id="9bc83-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="9bc83-137">Tekstjusteringen i kampangebannermodulet.</span><span class="sxs-lookup"><span data-stu-id="9bc83-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="9bc83-138">Binding</span><span class="sxs-lookup"><span data-stu-id="9bc83-138">Link</span></span>                      | <span data-ttu-id="9bc83-139">En URL-adresse</span><span class="sxs-lookup"><span data-stu-id="9bc83-139">A URL</span></span>                              | <span data-ttu-id="9bc83-140">URL-adressen for et valgfrit link.</span><span class="sxs-lookup"><span data-stu-id="9bc83-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="9bc83-141">Føj et kampangebannermodul til en ny side</span><span class="sxs-lookup"><span data-stu-id="9bc83-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="9bc83-142">Hvis du vil føje et kampangebannermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9bc83-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9bc83-143">Vælg **Ny** for at oprette en sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="9bc83-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="9bc83-144">Angiv **Kampagnebannerskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bc83-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9bc83-145">Under **Sidedisposition**kan du føje et **Standardside**modul til **Brødtekst**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="9bc83-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="9bc83-146">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="9bc83-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="9bc83-147">Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **Kampangebannermodul**.</span><span class="sxs-lookup"><span data-stu-id="9bc83-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="9bc83-148">Tilføj et containermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="9bc83-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="9bc83-149">Angiv værdien **Bredde** til **Fyld container** i ruden til højre.</span><span class="sxs-lookup"><span data-stu-id="9bc83-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="9bc83-150">Føj et kampangebannermodul til containermodulet under **Sidedisposition**.</span><span class="sxs-lookup"><span data-stu-id="9bc83-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="9bc83-151">Tilføj en eller flere bannermeddelelser i indstillingerne for bannermodulet.</span><span class="sxs-lookup"><span data-stu-id="9bc83-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="9bc83-152">Hver meddelelse kan have tekst sammen med et link.</span><span class="sxs-lookup"><span data-stu-id="9bc83-152">Each message can have text together with a link.</span></span> <span data-ttu-id="9bc83-153">Du kan redigere de andre egenskaber for at tilpasse modulet yderligere.</span><span class="sxs-lookup"><span data-stu-id="9bc83-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="9bc83-154">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="9bc83-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9bc83-155">Øverst på siden vises en påmindelse med den tekst, du har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="9bc83-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="9bc83-156">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="9bc83-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="9bc83-157">Et kampagnebanner bruges typisk i sidehovedpladsen eller en underoverskriftplads.</span><span class="sxs-lookup"><span data-stu-id="9bc83-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9bc83-158">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9bc83-158">Additional resources</span></span>

[<span data-ttu-id="9bc83-159">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="9bc83-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9bc83-160">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="9bc83-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="9bc83-161">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="9bc83-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9bc83-162">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="9bc83-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="9bc83-163">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="9bc83-163">Video player module</span></span>](add-video-player.md)
