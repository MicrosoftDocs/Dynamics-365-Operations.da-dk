---
title: Tilføj en favicon
description: I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 786ba02c312b7cdb3cf7f0689737084887d536bc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206337"
---
# <a name="add-a-favicon"></a><span data-ttu-id="53ae3-103">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="53ae3-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53ae3-104">I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.</span><span class="sxs-lookup"><span data-stu-id="53ae3-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="53ae3-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="53ae3-105">Overview</span></span>

<span data-ttu-id="53ae3-106">Et favoritikon er en lille grafikfil, der bl.a. vises under en webbrowserfane, på adresselinjen, i browserhistorikken og i bogmærker eller favoritter.</span><span class="sxs-lookup"><span data-stu-id="53ae3-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="53ae3-107">Det anbefales, at du føjer et favoritikon til dit websted, fordi det repræsenterer og forstærker dit varemærke og hjælper med at skelne dit websted fra andre websteder, som kunderne besøger.</span><span class="sxs-lookup"><span data-stu-id="53ae3-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="53ae3-108">Du kan føje flere favoritikoner med forskellig størrelse og filtype til webstedet, men i dette emne vises det, hvordan du tilføjer et enkelt favoritikon.</span><span class="sxs-lookup"><span data-stu-id="53ae3-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="53ae3-109">Du bruger imidlertid den samme proces og placering ved tilføjelse af flere favoritikoner.</span><span class="sxs-lookup"><span data-stu-id="53ae3-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="53ae3-110">Overføre et favoritikon til webstedets aktivsamling</span><span class="sxs-lookup"><span data-stu-id="53ae3-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="53ae3-111">Benyt følgende fremgangsmåde for at overføre et favoritikon til webstedets aktivsamling.</span><span class="sxs-lookup"><span data-stu-id="53ae3-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="53ae3-112">Vælg **Mediebibliotek** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="53ae3-112">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="53ae3-113">Vælg **Upload \> Upload medieelementer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="53ae3-113">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="53ae3-114">I vinduet Stifinder skal du gå til den favoritikonbilledfil, du vil uploade, vælge den og derefter vælge **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-114">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="53ae3-115">Angiv den påkrævede titel og alternative tekst i dialogboksen **Overfør medieelement**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-115">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="53ae3-116">Hvis du vil udgive billedet umiddelbart efter upload, skal du markere afkrydsningsfeltet **Publicer medieelementer efter upload**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-116">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="53ae3-117">Hvis du ikke markerer afkrydsningsfeltet **Publicer medieelementer efter upload**, skal du vende tilbage til siden **Medieelementer** og publicere favoritikonet manuelt senere.</span><span class="sxs-lookup"><span data-stu-id="53ae3-117">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="53ae3-118">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-118">Select **OK**.</span></span>
1. <span data-ttu-id="53ae3-119">Kopiér favoritikonets offentlige URL-adresse i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="53ae3-119">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="53ae3-120">Du kommer til at bruge denne URL-adresse senere.</span><span class="sxs-lookup"><span data-stu-id="53ae3-120">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="53ae3-121">Oprette HTML-koden til dit favoritikon</span><span class="sxs-lookup"><span data-stu-id="53ae3-121">Create the HTML for your favicon</span></span>

<span data-ttu-id="53ae3-122">Du opretter HTML-koden til favoritikonet ved hjælp af følgende HTML-streng.</span><span class="sxs-lookup"><span data-stu-id="53ae3-122">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="53ae3-123">I attributten **href** skal du erstatte **Public\_URL\_for\_your\_favicon** med den offentlige URL-adresse, du kopierede tidligere.</span><span class="sxs-lookup"><span data-stu-id="53ae3-123">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="53ae3-124">Oprette et fragment, der indeholder en metakode til dit favoritikon</span><span class="sxs-lookup"><span data-stu-id="53ae3-124">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="53ae3-125">Følg disse trin for at oprette et fragment, der indeholder en metakode til dit favoritikon.</span><span class="sxs-lookup"><span data-stu-id="53ae3-125">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="53ae3-126">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-126">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="53ae3-127">Vælg **Metakoder** i dialogboksen **Nyt fragment** som det modul, fragmentet er baseret på.</span><span class="sxs-lookup"><span data-stu-id="53ae3-127">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="53ae3-128">Angiv et navn til fragmentet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-128">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="53ae3-129">Vælg det underordnede **Standardmetamoder** i fragmenthierarkitræet.</span><span class="sxs-lookup"><span data-stu-id="53ae3-129">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="53ae3-130">Vælg **Tilføj** under **Metakoder** i ruden til højre, og angiv derefter den HTML-streng, du oprettede til favoritikonet tidligere.</span><span class="sxs-lookup"><span data-stu-id="53ae3-130">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="53ae3-131">Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere fragmentet.</span><span class="sxs-lookup"><span data-stu-id="53ae3-131">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="53ae3-132">Føj fragmentet for metakode til HTML-hovedsektionen på dine sider</span><span class="sxs-lookup"><span data-stu-id="53ae3-132">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="53ae3-133">Følge disse trin for at føj fragmentet for metakoder til sektionen for HTML-**hoved** på dine sider.</span><span class="sxs-lookup"><span data-stu-id="53ae3-133">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="53ae3-134">Gå til **Skabeloner**, åbn skabelonen for de sider, du vil føje dit favoritikon til, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-134">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="53ae3-135">Vælg ellipseknappen (**...**) i skabelonhierarkitræet til højre for containeren i **HTML-hovedet**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-135">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="53ae3-136">Vælg det fragment for metakoder, du oprettede tidligere, i dialogboksen **Vælg fragment**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="53ae3-136">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="53ae3-137">Vælg **Afslut redigering**, og vælg derefter **Publicer** for at publicere skabelonen.</span><span class="sxs-lookup"><span data-stu-id="53ae3-137">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="53ae3-138">Hvis webstedet bruger mere end én skabelon, skal du føje fragmentet for metakoder til dem alle.</span><span class="sxs-lookup"><span data-stu-id="53ae3-138">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="53ae3-139">Når du får vist sider, der er baseret på den skabelon, du har føjet til fragmentet for metakoder, burde du nu kunne se favoritikonet på browserfanen.</span><span class="sxs-lookup"><span data-stu-id="53ae3-139">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53ae3-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="53ae3-140">Additional resources</span></span>

[<span data-ttu-id="53ae3-141">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="53ae3-141">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="53ae3-142">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="53ae3-142">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="53ae3-143">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="53ae3-143">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="53ae3-144">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="53ae3-144">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="53ae3-145">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="53ae3-145">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="53ae3-146">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="53ae3-146">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="53ae3-147">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="53ae3-147">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]