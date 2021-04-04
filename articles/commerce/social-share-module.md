---
title: Modulet Social deling
description: Dette emne omhandler moduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0e7f30686894f9cf92257e99d95cc8b00f76f899
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234311"
---
# <a name="social-share-module"></a><span data-ttu-id="599f3-103">Modul til deling på sociale medier</span><span class="sxs-lookup"><span data-stu-id="599f3-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="599f3-104">Dette emne omhandler moduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="599f3-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="599f3-105">Med moduler til social deling kan brugerne dele URL-adresser på et e-handels-websted på sociale medier som Facebook, Twitter, Pinterest og LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="599f3-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="599f3-106">URL-adresser til websider kan også deles via mail.</span><span class="sxs-lookup"><span data-stu-id="599f3-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="599f3-107">Moduler til social deling bruges ofte på sider med produktoplysninger (PDP-filer), som hjælper brugerne med at dele produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="599f3-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="599f3-108">Hvert modul til social deling er en container for elementmoduler til social deling.</span><span class="sxs-lookup"><span data-stu-id="599f3-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="599f3-109">Hvert elementmodul til social deling kan konfigureres til at pege på et bestemt websted med sociale medier.</span><span class="sxs-lookup"><span data-stu-id="599f3-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="599f3-110">Integration med Facebook, Twitter, Pinterest, LinkedIn og mail understøttes som standard.</span><span class="sxs-lookup"><span data-stu-id="599f3-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="599f3-111">Når en bruger af webstedet vælger et socialt mediesymbol, startes en HTML-IFrame for det pågældende websted med sociale medier.</span><span class="sxs-lookup"><span data-stu-id="599f3-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="599f3-112">I iFrame kan brugeren logge på og bogføre sideindholdet, som de fik vist.</span><span class="sxs-lookup"><span data-stu-id="599f3-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="599f3-113">De enkelte sociale medieplatforme kan registrere cookies, så dette modul kræver, at brugerne af webstedet accepterer beskeden om samtykke til cookie.</span><span class="sxs-lookup"><span data-stu-id="599f3-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="599f3-114">Når cookie-samtykke ikke accepteres, vil modulet være skjult på siden.</span><span class="sxs-lookup"><span data-stu-id="599f3-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="599f3-115">Du kan få flere oplysninger under [Cookieoverholdelse](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="599f3-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="599f3-116">I følgende illustration fremhæves et eksempel på et modul til social deling, der bruges på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="599f3-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Eksempel på et modul til social deling](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="599f3-118">Egenskaber for modul til social deling</span><span class="sxs-lookup"><span data-stu-id="599f3-118">Social share module properties</span></span>

| <span data-ttu-id="599f3-119">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="599f3-119">Property name</span></span>             | <span data-ttu-id="599f3-120">Værdi</span><span class="sxs-lookup"><span data-stu-id="599f3-120">Value</span></span>                 | <span data-ttu-id="599f3-121">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="599f3-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="599f3-122">Overskrift</span><span class="sxs-lookup"><span data-stu-id="599f3-122">Caption</span></span>                  | <span data-ttu-id="599f3-123">Tekst</span><span class="sxs-lookup"><span data-stu-id="599f3-123">Text</span></span> | <span data-ttu-id="599f3-124">Denne egenskab angiver en titel til modulet.</span><span class="sxs-lookup"><span data-stu-id="599f3-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="599f3-125">Retning</span><span class="sxs-lookup"><span data-stu-id="599f3-125">Orientation</span></span> | <span data-ttu-id="599f3-126">**Lodret** eller **Vandret**</span><span class="sxs-lookup"><span data-stu-id="599f3-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="599f3-127">Denne egenskab definerer layoutretningen for sociale mediers elementer.</span><span class="sxs-lookup"><span data-stu-id="599f3-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="599f3-128">Egenskaber for elementmodul til social deling</span><span class="sxs-lookup"><span data-stu-id="599f3-128">Social share item module properties</span></span>
| <span data-ttu-id="599f3-129">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="599f3-129">Property name</span></span>             | <span data-ttu-id="599f3-130">Værdi</span><span class="sxs-lookup"><span data-stu-id="599f3-130">Value</span></span>                 | <span data-ttu-id="599f3-131">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="599f3-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="599f3-132">Sociale medier</span><span class="sxs-lookup"><span data-stu-id="599f3-132">Social media</span></span>              | <span data-ttu-id="599f3-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="599f3-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="599f3-134">En rullemenu med en liste over sociale mediers platforme.</span><span class="sxs-lookup"><span data-stu-id="599f3-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="599f3-135">Ikon</span><span class="sxs-lookup"><span data-stu-id="599f3-135">Icon</span></span> |<span data-ttu-id="599f3-136">Billede</span><span class="sxs-lookup"><span data-stu-id="599f3-136">Image</span></span>    | <span data-ttu-id="599f3-137">Dette er det billede, der vil blive vist for de respektive sociale medier.</span><span class="sxs-lookup"><span data-stu-id="599f3-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="599f3-138">Som bedste fremgangsmåde kan du se sociale medieplatformes SDK for at få det anbefalede billede til hver platform.</span><span class="sxs-lookup"><span data-stu-id="599f3-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="599f3-139">Tilføje et modul til social deling i et købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="599f3-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="599f3-140">Følg disse trin for at tilføje et modul til social deling i et købefeltmodul.</span><span class="sxs-lookup"><span data-stu-id="599f3-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="599f3-141">Vælg **Sider** på webstedet Fabrikam, og vælg derefter siden **DefaultPDP** for at åbne siden med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="599f3-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="599f3-142">På pladsen **Købefelt (påkrævet)** skal du vælge ellipsen (**...**) og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="599f3-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="599f3-143">I dialogboksen **Tilføj modul** skal du vælge modulet **Social deling** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="599f3-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="599f3-144">På pladsen **Social deling** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="599f3-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="599f3-145">I dialogboksen **Tilføj modul** skal du vælge modulet **SocialShare** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="599f3-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="599f3-146">Vælg **Vandret** under **Retning** i ruden Egenskaber for modulet **SocialShare**.</span><span class="sxs-lookup"><span data-stu-id="599f3-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="599f3-147">Tilføj eventuelt en billedtekst.</span><span class="sxs-lookup"><span data-stu-id="599f3-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="599f3-148">På pladsen **SocialShare** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="599f3-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="599f3-149">I dialogboksen **Tilføj modul** skal du vælge modulet **SocialShareItem** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="599f3-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="599f3-150">I ruden Egenskaber for modulet **SocialShareItem** skal du under **Sociale medier** vælge **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="599f3-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="599f3-151">I ruden Egenskaber for modulet **SocialShareItem** skal du under **Ikon** vælge **+ Tilføj et billede**.</span><span class="sxs-lookup"><span data-stu-id="599f3-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="599f3-152">I dialogboksen **Medievælger** skal du vælge Facebook-logobilledet og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="599f3-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="599f3-153">Hvis der ikke findes et Facebook-logo, skal du vælge **Upload nyt medieelement** for at uploade det.</span><span class="sxs-lookup"><span data-stu-id="599f3-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="599f3-154">Tilføj og konfigurer yderligere **SocialShareItem**-moduler efter behov.</span><span class="sxs-lookup"><span data-stu-id="599f3-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="599f3-155">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="599f3-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="599f3-156">Siden viser modulet til social deling.</span><span class="sxs-lookup"><span data-stu-id="599f3-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="599f3-157">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="599f3-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="599f3-158">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="599f3-158">Additional resources</span></span>

[<span data-ttu-id="599f3-159">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="599f3-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="599f3-160">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="599f3-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="599f3-161">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="599f3-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]