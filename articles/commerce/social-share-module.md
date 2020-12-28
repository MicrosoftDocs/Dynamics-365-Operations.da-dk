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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 510ca8b14d8b5334e50aca1b15d636c65fcc9888
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4411210"
---
# <a name="social-share-module"></a><span data-ttu-id="e43cc-103">Modulet Social deling</span><span class="sxs-lookup"><span data-stu-id="e43cc-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e43cc-104">Dette emne omhandler moduler for social deling og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e43cc-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e43cc-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="e43cc-105">Overview</span></span>

<span data-ttu-id="e43cc-106">Med moduler til social deling kan brugerne dele URL-adresser på et e-handels-websted på sociale medier som Facebook, Twitter, Pinterest og LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="e43cc-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="e43cc-107">URL-adresser til websider kan også deles via mail.</span><span class="sxs-lookup"><span data-stu-id="e43cc-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="e43cc-108">Moduler til social deling bruges ofte på sider med produktoplysninger (PDP-filer), som hjælper brugerne med at dele produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e43cc-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="e43cc-109">Hvert modul til social deling er en container for elementmoduler til social deling.</span><span class="sxs-lookup"><span data-stu-id="e43cc-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="e43cc-110">Hvert elementmodul til social deling kan konfigureres til at pege på et bestemt websted med sociale medier.</span><span class="sxs-lookup"><span data-stu-id="e43cc-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="e43cc-111">Integration med Facebook, Twitter, Pinterest, LinkedIn og mail understøttes som standard.</span><span class="sxs-lookup"><span data-stu-id="e43cc-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="e43cc-112">Når en bruger af webstedet vælger et socialt mediesymbol, startes en HTML-IFrame for det pågældende websted med sociale medier.</span><span class="sxs-lookup"><span data-stu-id="e43cc-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="e43cc-113">I iFrame kan brugeren logge på og bogføre sideindholdet, som de fik vist.</span><span class="sxs-lookup"><span data-stu-id="e43cc-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="e43cc-114">De enkelte sociale medieplatforme kan registrere cookies, så dette modul kræver, at brugerne af webstedet accepterer beskeden om samtykke til cookie.</span><span class="sxs-lookup"><span data-stu-id="e43cc-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="e43cc-115">Når cookie-samtykke ikke accepteres, vil modulet være skjult på siden.</span><span class="sxs-lookup"><span data-stu-id="e43cc-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="e43cc-116">Du kan få flere oplysninger under [Cookieoverholdelse](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="e43cc-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="e43cc-117">I følgende illustration fremhæves et eksempel på et modul til social deling, der bruges på en side med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="e43cc-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Eksempel på et modul til social deling](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="e43cc-119">Egenskaber for modul til social deling</span><span class="sxs-lookup"><span data-stu-id="e43cc-119">Social share module properties</span></span>

| <span data-ttu-id="e43cc-120">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="e43cc-120">Property name</span></span>             | <span data-ttu-id="e43cc-121">Værdi</span><span class="sxs-lookup"><span data-stu-id="e43cc-121">Value</span></span>                 | <span data-ttu-id="e43cc-122">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e43cc-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e43cc-123">Overskrift</span><span class="sxs-lookup"><span data-stu-id="e43cc-123">Caption</span></span>                  | <span data-ttu-id="e43cc-124">Tekst</span><span class="sxs-lookup"><span data-stu-id="e43cc-124">Text</span></span> | <span data-ttu-id="e43cc-125">Denne egenskab angiver en titel til modulet.</span><span class="sxs-lookup"><span data-stu-id="e43cc-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="e43cc-126">Retning</span><span class="sxs-lookup"><span data-stu-id="e43cc-126">Orientation</span></span> | <span data-ttu-id="e43cc-127">**Lodret** eller **Vandret**</span><span class="sxs-lookup"><span data-stu-id="e43cc-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="e43cc-128">Denne egenskab definerer layoutretningen for sociale mediers elementer.</span><span class="sxs-lookup"><span data-stu-id="e43cc-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="e43cc-129">Egenskaber for elementmodul til social deling</span><span class="sxs-lookup"><span data-stu-id="e43cc-129">Social share item module properties</span></span>
| <span data-ttu-id="e43cc-130">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="e43cc-130">Property name</span></span>             | <span data-ttu-id="e43cc-131">Værdi</span><span class="sxs-lookup"><span data-stu-id="e43cc-131">Value</span></span>                 | <span data-ttu-id="e43cc-132">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e43cc-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e43cc-133">Sociale medier</span><span class="sxs-lookup"><span data-stu-id="e43cc-133">Social media</span></span>              | <span data-ttu-id="e43cc-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="e43cc-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="e43cc-135">En rullemenu med en liste over sociale mediers platforme.</span><span class="sxs-lookup"><span data-stu-id="e43cc-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="e43cc-136">Ikon</span><span class="sxs-lookup"><span data-stu-id="e43cc-136">Icon</span></span> |<span data-ttu-id="e43cc-137">Billede</span><span class="sxs-lookup"><span data-stu-id="e43cc-137">Image</span></span>    | <span data-ttu-id="e43cc-138">Dette er det billede, der vil blive vist for de respektive sociale medier.</span><span class="sxs-lookup"><span data-stu-id="e43cc-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="e43cc-139">Som bedste fremgangsmåde kan du se sociale medieplatformes SDK for at få det anbefalede billede til hver platform.</span><span class="sxs-lookup"><span data-stu-id="e43cc-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="e43cc-140">Tilføje et modul til social deling i et købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="e43cc-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="e43cc-141">Følg disse trin for at tilføje et modul til social deling i et købefeltmodul.</span><span class="sxs-lookup"><span data-stu-id="e43cc-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="e43cc-142">Vælg **Sider** på webstedet Fabrikam, og vælg derefter siden **DefaultPDP** for at åbne siden med produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="e43cc-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="e43cc-143">På pladsen **Købefelt (påkrævet)** skal du vælge ellipsen (**...**) og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e43cc-144">I dialogboksen **Tilføj modul** skal du vælge modulet **Social deling** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e43cc-145">På pladsen **Social deling** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e43cc-146">I dialogboksen **Tilføj modul** skal du vælge modulet **SocialShare** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e43cc-147">Vælg **Vandret** under **Retning** i ruden Egenskaber for modulet **SocialShare**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="e43cc-148">Tilføj eventuelt en billedtekst.</span><span class="sxs-lookup"><span data-stu-id="e43cc-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="e43cc-149">På pladsen **SocialShare** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e43cc-150">I dialogboksen **Tilføj modul** skal du vælge modulet **SocialShareItem** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e43cc-151">I ruden Egenskaber for modulet **SocialShareItem** skal du under **Sociale medier** vælge **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="e43cc-152">I ruden Egenskaber for modulet **SocialShareItem** skal du under **Ikon** vælge **+ Tilføj et billede**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="e43cc-153">I dialogboksen **Medievælger** skal du vælge Facebook-logobilledet og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e43cc-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="e43cc-154">Hvis der ikke findes et Facebook-logo, skal du vælge **Upload nyt medieelement** for at uploade det.</span><span class="sxs-lookup"><span data-stu-id="e43cc-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="e43cc-155">Tilføj og konfigurer yderligere **SocialShareItem**-moduler efter behov.</span><span class="sxs-lookup"><span data-stu-id="e43cc-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="e43cc-156">Vælg **Gem**, og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="e43cc-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="e43cc-157">Siden viser modulet til social deling.</span><span class="sxs-lookup"><span data-stu-id="e43cc-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="e43cc-158">Vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="e43cc-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e43cc-159">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e43cc-159">Additional resources</span></span>

[<span data-ttu-id="e43cc-160">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="e43cc-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e43cc-161">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="e43cc-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e43cc-162">Cookieoverholdelse</span><span class="sxs-lookup"><span data-stu-id="e43cc-162">Cookie compliance</span></span>](cookie-compliance.md)
