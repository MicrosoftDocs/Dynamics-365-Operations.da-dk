---
title: Kampagnebannermodul
description: Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: d9debd16b18300d090bde1862a16920d8e9185eb
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817248"
---
# <a name="promo-banner-module"></a><span data-ttu-id="b30ec-103">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="b30ec-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b30ec-104">Dette emne omhandler kampagnebannermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b30ec-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b30ec-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b30ec-105">Overview</span></span>

<span data-ttu-id="b30ec-106">Kampagnebannermoduler bruges til at vise indbyggede informationsmeddelelser på en side.</span><span class="sxs-lookup"><span data-stu-id="b30ec-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="b30ec-107">De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel.</span><span class="sxs-lookup"><span data-stu-id="b30ec-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="b30ec-108">Kampagnebannermoduler understøtter en sms-besked og et link.</span><span class="sxs-lookup"><span data-stu-id="b30ec-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="b30ec-109">Hvis der føjes flere meddelelser til et kampagnebannermodul, bliver det til et roterende banner, hvor du kan gå gennem alle meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="b30ec-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="b30ec-110">Kampagnebannermoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="b30ec-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="b30ec-111">Anvendelseseksempler på kampagnebannere i e-handel</span><span class="sxs-lookup"><span data-stu-id="b30ec-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="b30ec-112">Kampagnebannere kan bruges i webstedets overskift til at vise kampagner eller meddelelser, der gælder for hele webstedet, som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="b30ec-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="b30ec-113">"Det årlige udsalg slutter om 10 dage"</span><span class="sxs-lookup"><span data-stu-id="b30ec-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="b30ec-114">"Store besparelser på skolestartudsalg.</span><span class="sxs-lookup"><span data-stu-id="b30ec-114">"Save big with back to school sale.</span></span> <span data-ttu-id="b30ec-115">Køb nu".</span><span class="sxs-lookup"><span data-stu-id="b30ec-115">Shop Now."</span></span>

<span data-ttu-id="b30ec-116">"Butik for Thanksgiving-SALG!"</span><span class="sxs-lookup"><span data-stu-id="b30ec-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="b30ec-117">Det følgende billede viser et eksempel på et reklamebanner.</span><span class="sxs-lookup"><span data-stu-id="b30ec-117">The following image shows an example of a promo banner.</span></span>

![Eksempel på et reklamebannermodul](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="b30ec-119">Egenskaber for kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="b30ec-119">Promo banner module properties</span></span>

| <span data-ttu-id="b30ec-120">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="b30ec-120">Property name</span></span>             | <span data-ttu-id="b30ec-121">Værdi</span><span class="sxs-lookup"><span data-stu-id="b30ec-121">Value</span></span>                              | <span data-ttu-id="b30ec-122">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="b30ec-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="b30ec-123">Bannermeddelelser</span><span class="sxs-lookup"><span data-stu-id="b30ec-123">Banner messages</span></span>           | <span data-ttu-id="b30ec-124">Tekst og link</span><span class="sxs-lookup"><span data-stu-id="b30ec-124">Text and links</span></span>                     | <span data-ttu-id="b30ec-125">En matrix af tekst og link.</span><span class="sxs-lookup"><span data-stu-id="b30ec-125">An array of text and links.</span></span> |
| <span data-ttu-id="b30ec-126">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="b30ec-126">Autoplay</span></span>                  | <span data-ttu-id="b30ec-127">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="b30ec-127">**True** or **False**</span></span>              | <span data-ttu-id="b30ec-128">En værdi, der angiver, om meddelelser automatisk gennemløbes, hvis der er konfigureret flere meddelelser.</span><span class="sxs-lookup"><span data-stu-id="b30ec-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="b30ec-129">Interval for glidende interval</span><span class="sxs-lookup"><span data-stu-id="b30ec-129">Slide transition interval</span></span> | <span data-ttu-id="b30ec-130">Et antal millisekunder (MS)</span><span class="sxs-lookup"><span data-stu-id="b30ec-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="b30ec-131">Det interval, der bruges til at gå gennem meddelelser.</span><span class="sxs-lookup"><span data-stu-id="b30ec-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="b30ec-132">Tillad afvis</span><span class="sxs-lookup"><span data-stu-id="b30ec-132">Allow dismiss</span></span>             | <span data-ttu-id="b30ec-133">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="b30ec-133">**True** or **False**</span></span>              | <span data-ttu-id="b30ec-134">Hvis værdien er angivet til **Sand**, kan kunderne afvise påmindelsen.</span><span class="sxs-lookup"><span data-stu-id="b30ec-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="b30ec-135">Vis karruselslipper</span><span class="sxs-lookup"><span data-stu-id="b30ec-135">Show carousel flipper</span></span>     | <span data-ttu-id="b30ec-136">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="b30ec-136">**True** or **False**</span></span>              | <span data-ttu-id="b30ec-137">En værdi, der angiver, om karruselslippere skal vises, så kunder kan gå gennem flere bannerelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="b30ec-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="b30ec-138">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="b30ec-138">Text alignment</span></span>            | <span data-ttu-id="b30ec-139">**Højre**, **Venstre** eller **Centreret**</span><span class="sxs-lookup"><span data-stu-id="b30ec-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="b30ec-140">Tekstjusteringen i kampangebannermodulet.</span><span class="sxs-lookup"><span data-stu-id="b30ec-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="b30ec-141">Binding</span><span class="sxs-lookup"><span data-stu-id="b30ec-141">Link</span></span>                      | <span data-ttu-id="b30ec-142">En URL-adresse</span><span class="sxs-lookup"><span data-stu-id="b30ec-142">A URL</span></span>                              | <span data-ttu-id="b30ec-143">URL-adressen for et valgfrit link.</span><span class="sxs-lookup"><span data-stu-id="b30ec-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="b30ec-144">Føj et kampangebannermodul til en ny side</span><span class="sxs-lookup"><span data-stu-id="b30ec-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="b30ec-145">Hvis du vil føje et kampangebannermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b30ec-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b30ec-146">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="b30ec-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b30ec-147">Angiv **Kampagnebannerskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b30ec-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b30ec-148">Under **Sidedisposition**kan du føje et **Standardside**modul til **Brødtekst**-pladsen.</span><span class="sxs-lookup"><span data-stu-id="b30ec-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="b30ec-149">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="b30ec-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="b30ec-150">Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **Kampangebannermodul**.</span><span class="sxs-lookup"><span data-stu-id="b30ec-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="b30ec-151">Tilføj et containermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="b30ec-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="b30ec-152">Angiv værdien **Bredde** til **Fyld container** i ruden til højre.</span><span class="sxs-lookup"><span data-stu-id="b30ec-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="b30ec-153">Føj et kampangebannermodul til containermodulet under **Sidedisposition**.</span><span class="sxs-lookup"><span data-stu-id="b30ec-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="b30ec-154">Tilføj en eller flere bannermeddelelser i indstillingerne for bannermodulet.</span><span class="sxs-lookup"><span data-stu-id="b30ec-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="b30ec-155">Hver meddelelse kan have tekst sammen med et link.</span><span class="sxs-lookup"><span data-stu-id="b30ec-155">Each message can have text together with a link.</span></span> <span data-ttu-id="b30ec-156">Du kan redigere de andre egenskaber for at tilpasse modulet yderligere.</span><span class="sxs-lookup"><span data-stu-id="b30ec-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="b30ec-157">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="b30ec-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="b30ec-158">Øverst på siden vises en påmindelse med den tekst, du har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="b30ec-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="b30ec-159">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="b30ec-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="b30ec-160">Et kampagnebanner bruges typisk i sidehovedpladsen eller en underoverskriftplads.</span><span class="sxs-lookup"><span data-stu-id="b30ec-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b30ec-161">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b30ec-161">Additional resources</span></span>

[<span data-ttu-id="b30ec-162">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="b30ec-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b30ec-163">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="b30ec-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b30ec-164">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="b30ec-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b30ec-165">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="b30ec-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="b30ec-166">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="b30ec-166">Video player module</span></span>](add-video-player.md)
