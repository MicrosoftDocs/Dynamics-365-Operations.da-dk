---
title: Videoafspillermodul
description: Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025637"
---
# <a name="video-player-module"></a><span data-ttu-id="62c59-103">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="62c59-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="62c59-104">Dette emne omhandler videoafspillermoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="62c59-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62c59-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="62c59-105">Overview</span></span>

<span data-ttu-id="62c59-106">Videoafspillermodulet bruges til at understøtte videoafspilning.</span><span class="sxs-lookup"><span data-stu-id="62c59-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="62c59-107">Den kan føjes til en hvilken som helst side, som videoindholdet uploades til og vises i CMS (Content Management system).</span><span class="sxs-lookup"><span data-stu-id="62c59-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="62c59-108">Videoafspillermodulet understøtter medietypen .mp4.</span><span class="sxs-lookup"><span data-stu-id="62c59-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="62c59-109">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="62c59-109">Video player module</span></span>

<span data-ttu-id="62c59-110">Videoafspillermodulet kan bruges til at vise videoer på et e-handels-websted.</span><span class="sxs-lookup"><span data-stu-id="62c59-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="62c59-111">Det understøtter alle afspilningsmuligheder, f.eks. afspilning, pause, fuld størrelse, lydbeskrivelser og undertekster.</span><span class="sxs-lookup"><span data-stu-id="62c59-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="62c59-112">Videoafspillermodulet understøtter også tilpasning af undertekster, så de opfylder Microsofts tilgængelighedsstandarder.</span><span class="sxs-lookup"><span data-stu-id="62c59-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="62c59-113">Du kan f. eks. tilpasse skriftstørrelsen og baggrundsfarven.</span><span class="sxs-lookup"><span data-stu-id="62c59-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="62c59-114">Videoafspillermodulet understøtter også sekundære lydspor.</span><span class="sxs-lookup"><span data-stu-id="62c59-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="62c59-115">I forbindelse med at en video uploades til CMS, kan der også uploades et sekundært lydspor.</span><span class="sxs-lookup"><span data-stu-id="62c59-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="62c59-116">Videoafspillermodulet kan derefter afspille det sekundære lydspor, hvis en bruger vælger det.</span><span class="sxs-lookup"><span data-stu-id="62c59-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="62c59-117">Eksempler på videoafspillermoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="62c59-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="62c59-118">Instruktionsvideoer på sider med produktoplysninger eller marketingsider</span><span class="sxs-lookup"><span data-stu-id="62c59-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="62c59-119">Kampagnevideoer eller videoer om politikker på en hvilken som helst marketingside</span><span class="sxs-lookup"><span data-stu-id="62c59-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="62c59-120">Marketingvideoer, der fremhæver produktfunktioner på sider med produktdetaljer eller marketingsider</span><span class="sxs-lookup"><span data-stu-id="62c59-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="62c59-121">Egenskaber for videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="62c59-121">Video player module properties</span></span>

| <span data-ttu-id="62c59-122">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="62c59-122">Property name</span></span>         | <span data-ttu-id="62c59-123">Værdi</span><span class="sxs-lookup"><span data-stu-id="62c59-123">Value</span></span>                               | <span data-ttu-id="62c59-124">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="62c59-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="62c59-125">Automatisk afspilning</span><span class="sxs-lookup"><span data-stu-id="62c59-125">Auto play</span></span>             | <span data-ttu-id="62c59-126">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-126">**True** or **False**</span></span>               | <span data-ttu-id="62c59-127">Når værdien er angivet til **Sand**, afspilles videoen automatisk.</span><span class="sxs-lookup"><span data-stu-id="62c59-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="62c59-128">Slå mikrofon fra</span><span class="sxs-lookup"><span data-stu-id="62c59-128">Mute</span></span>                  | <span data-ttu-id="62c59-129">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-129">**True** or **False**</span></span>               | <span data-ttu-id="62c59-130">Når værdien er angivet til **Sand**, deaktiveres lyden.</span><span class="sxs-lookup"><span data-stu-id="62c59-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="62c59-131">Standardværdien for denne afspiller er **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="62c59-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="62c59-132">I Google Chrome-browseren er automatisk afspilning af videoer som standard slået fra, og lyden afspilles kun, hvis brugeren afspiller videoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="62c59-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="62c59-133">Løkke</span><span class="sxs-lookup"><span data-stu-id="62c59-133">Loop</span></span>                  | <span data-ttu-id="62c59-134">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-134">**True** or **False**</span></span>               | <span data-ttu-id="62c59-135">Når værdien er angivet til **Sand**, afspilles videoen gentagne gange i en løkke.</span><span class="sxs-lookup"><span data-stu-id="62c59-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="62c59-136">Medier</span><span class="sxs-lookup"><span data-stu-id="62c59-136">Media</span></span>                 | <span data-ttu-id="62c59-137">Videofilens sti og navn</span><span class="sxs-lookup"><span data-stu-id="62c59-137">Video file path and name</span></span> | <span data-ttu-id="62c59-138">Den videofil, der afspilles af videoafspilleren.</span><span class="sxs-lookup"><span data-stu-id="62c59-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="62c59-139">Afspil i fuldskærmstilstand</span><span class="sxs-lookup"><span data-stu-id="62c59-139">Play fullscreen</span></span>       | <span data-ttu-id="62c59-140">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-140">**True** or **False**</span></span>               | <span data-ttu-id="62c59-141">Når værdien er angivet til **Sand**, afspilles videoen i fuldskærmstilstand.</span><span class="sxs-lookup"><span data-stu-id="62c59-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="62c59-142">Udløser til midlertidig afbrydelse af afspilning</span><span class="sxs-lookup"><span data-stu-id="62c59-142">Play pause trigger</span></span>    | <span data-ttu-id="62c59-143">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-143">**True** or **False**</span></span>               | <span data-ttu-id="62c59-144">Når værdien er angivet til **Sand**, vises afspil/pause-knappen på videoen.</span><span class="sxs-lookup"><span data-stu-id="62c59-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="62c59-145">Knapper til videoafspiller</span><span class="sxs-lookup"><span data-stu-id="62c59-145">Video player controls</span></span> | <span data-ttu-id="62c59-146">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-146">**True** or **False**</span></span>               | <span data-ttu-id="62c59-147">Når værdien er angivet til **Sand**, vises alle videoafspillerens kontrolelementer.</span><span class="sxs-lookup"><span data-stu-id="62c59-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="62c59-148">Disse kontrolelementer omfatter knapper til afspilning og pause, en statusindikator og valg af undertekster.</span><span class="sxs-lookup"><span data-stu-id="62c59-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="62c59-149">Skjul plakatbillede</span><span class="sxs-lookup"><span data-stu-id="62c59-149">Hide poster image</span></span>     | <span data-ttu-id="62c59-150">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="62c59-150">**True** or **False**</span></span>               | <span data-ttu-id="62c59-151">En video kan have en plakatramme.</span><span class="sxs-lookup"><span data-stu-id="62c59-151">A video can have a poster frame.</span></span> <span data-ttu-id="62c59-152">Når værdien for denne egenskab er angivet til **Sand**, er plakatrammen skjult.</span><span class="sxs-lookup"><span data-stu-id="62c59-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="62c59-153">Maskeringsniveau</span><span class="sxs-lookup"><span data-stu-id="62c59-153">Mask level</span></span>            | <span data-ttu-id="62c59-154">Et tal mellem **0** og **100**</span><span class="sxs-lookup"><span data-stu-id="62c59-154">A number from **0** through **100**</span></span> | <span data-ttu-id="62c59-155">Den maske, der anvendes på videoen til stylingen.</span><span class="sxs-lookup"><span data-stu-id="62c59-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="62c59-156">Føje et videoafspillermodul til en side</span><span class="sxs-lookup"><span data-stu-id="62c59-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="62c59-157">Før du opretter et videoafspillermodul, skal du først uploade en video til mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="62c59-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="62c59-158">Hvis du vil føje et videoafspillermodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="62c59-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="62c59-159">Opret en sideskabelon med navnet **videoafspillerskabelon**.</span><span class="sxs-lookup"><span data-stu-id="62c59-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="62c59-160">Tilføj et containermodul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="62c59-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="62c59-161">Tilføj videoafspiller- og atmosfæreskabende videoafspiller-modulet i containermodulet.</span><span class="sxs-lookup"><span data-stu-id="62c59-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="62c59-162">Afslut redigeringen af skabelonen, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="62c59-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="62c59-163">Brug den indholdsskabelon, som du har oprettet, til at oprette en side med navnet **videoafspillerside**.</span><span class="sxs-lookup"><span data-stu-id="62c59-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="62c59-164">Tilføj et videoafspillermodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="62c59-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="62c59-165">Vælg **Tilføj en video**i egenskabsruden for videoafspillermodulet.</span><span class="sxs-lookup"><span data-stu-id="62c59-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="62c59-166">Vælg en video i dialogboksen **Medievælger**, og vælg derefter **Upload nyt medieelement**.</span><span class="sxs-lookup"><span data-stu-id="62c59-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="62c59-167">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="62c59-167">Save and preview the page.</span></span> <span data-ttu-id="62c59-168">Nu vises videomodulet på siden.</span><span class="sxs-lookup"><span data-stu-id="62c59-168">You should see the video module on the page.</span></span> <span data-ttu-id="62c59-169">Du kan ændre flere indstillinger for at tilpasse funktionsmåden af modulet.</span><span class="sxs-lookup"><span data-stu-id="62c59-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="62c59-170">Afslut redigeringen af siden, og udgiv den.</span><span class="sxs-lookup"><span data-stu-id="62c59-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62c59-171">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="62c59-171">Additional resources</span></span>

[<span data-ttu-id="62c59-172">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="62c59-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="62c59-173">Kampagnebannermodul</span><span class="sxs-lookup"><span data-stu-id="62c59-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="62c59-174">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="62c59-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="62c59-175">Tekstblokmodul</span><span class="sxs-lookup"><span data-stu-id="62c59-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="62c59-176">Indholdsblokmodul</span><span class="sxs-lookup"><span data-stu-id="62c59-176">Content block module</span></span>](add-hero-module.md)
