---
title: iFrame-modul
description: I dette emne dækkes iFrame-modulet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665390"
---
# <a name="iframe-module"></a><span data-ttu-id="51dc1-103">iFrame-modul</span><span class="sxs-lookup"><span data-stu-id="51dc1-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="51dc1-104">I dette emne dækkes iFrame-modulet, og det beskriver, hvordan du kan føje det til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51dc1-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="51dc1-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="51dc1-105">Overview</span></span>

<span data-ttu-id="51dc1-106">Et iFrame-modul indeholder en iframe (indbygget ramme), der fungerer som vært for eksternt indhold på et websted.</span><span class="sxs-lookup"><span data-stu-id="51dc1-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="51dc1-107">Det kan f.eks. bruges som vært for en YouTube-video eller PDF-filfremviser på en side på et websted.</span><span class="sxs-lookup"><span data-stu-id="51dc1-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="51dc1-108">Et iFrame-modul kræver en URL-destination.</span><span class="sxs-lookup"><span data-stu-id="51dc1-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="51dc1-109">Derefter vil den være vært for indholdet af målsiden i et HTML **iframe**-element.</span><span class="sxs-lookup"><span data-stu-id="51dc1-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="51dc1-110">Eksterne URL-adresser skal være på listen over tilladte i henhold til direktiverne om indholdssikkerhedspolitik (CSP) pr. websted.</span><span class="sxs-lookup"><span data-stu-id="51dc1-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="51dc1-111">Til iframe-indhold skal URL-adresser tillades ved hjælp af **frame-ancestor**-direktivet.</span><span class="sxs-lookup"><span data-stu-id="51dc1-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="51dc1-112">Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="51dc1-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="51dc1-113">iFrame-modulet er tilgængeligt i Dynamics 365 Commerce version 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="51dc1-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="51dc1-114">Følgende billede viser eksempler på iFrame-moduler, der præsenterer eksterne videoer på websider.</span><span class="sxs-lookup"><span data-stu-id="51dc1-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Eksempel på iFrame-moduler, der præsenterer eksterne videoer](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="51dc1-116">Egenskaber for iFrame-modul</span><span class="sxs-lookup"><span data-stu-id="51dc1-116">Iframe module properties</span></span>

| <span data-ttu-id="51dc1-117">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="51dc1-117">Property name</span></span>             | <span data-ttu-id="51dc1-118">Værdi</span><span class="sxs-lookup"><span data-stu-id="51dc1-118">Value</span></span>                 | <span data-ttu-id="51dc1-119">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="51dc1-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="51dc1-120">Overskrift</span><span class="sxs-lookup"><span data-stu-id="51dc1-120">Heading</span></span> | <span data-ttu-id="51dc1-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="51dc1-121">Text</span></span> | <span data-ttu-id="51dc1-122">Overskrift for modulet.</span><span class="sxs-lookup"><span data-stu-id="51dc1-122">The heading for the module.</span></span> |
| <span data-ttu-id="51dc1-123">Mål-URL-adresse</span><span class="sxs-lookup"><span data-stu-id="51dc1-123">Target URL</span></span> | <span data-ttu-id="51dc1-124">URL</span><span class="sxs-lookup"><span data-stu-id="51dc1-124">URL</span></span> | <span data-ttu-id="51dc1-125">Den URL-adresse, der har modulet som vært.</span><span class="sxs-lookup"><span data-stu-id="51dc1-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="51dc1-126">Højde</span><span class="sxs-lookup"><span data-stu-id="51dc1-126">Height</span></span> | <span data-ttu-id="51dc1-127">Antal eller procentdel</span><span class="sxs-lookup"><span data-stu-id="51dc1-127">Number or percentage</span></span> | <span data-ttu-id="51dc1-128">Højden på modulet i pixel eller som en procentdel.</span><span class="sxs-lookup"><span data-stu-id="51dc1-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="51dc1-129">Værdien **100** vil f.eks. blive behandlet som et antal pixel, og værdien **100 %** vil blive behandlet som en procentdel.</span><span class="sxs-lookup"><span data-stu-id="51dc1-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="51dc1-130">Aria-label</span><span class="sxs-lookup"><span data-stu-id="51dc1-130">Aria label</span></span> | <span data-ttu-id="51dc1-131">Tekst</span><span class="sxs-lookup"><span data-stu-id="51dc1-131">Text</span></span> | <span data-ttu-id="51dc1-132">En tilgængelig ARIA-etiket (Accessible Rich Internet Applications) kan defineres af hensyn til tilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="51dc1-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="51dc1-133">Føj et iFrame-modul til en side</span><span class="sxs-lookup"><span data-stu-id="51dc1-133">Add an iframe module to a page</span></span>

<span data-ttu-id="51dc1-134">Hvis du vil føje et iFrame-modul til en side, der viser en ekstern video, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="51dc1-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="51dc1-135">Gå til **Skabeloner**, og vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="51dc1-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="51dc1-136">I dialogboksen **Ny skabelon** skal du under **Skabelonnavn** angive **Marketingskabelon** og derefter klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="51dc1-137">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="51dc1-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="51dc1-138">Gå til **Sider**, og vælg **Ny** for at oprette en ny side.</span><span class="sxs-lookup"><span data-stu-id="51dc1-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="51dc1-139">I dialogboksen **Vælg en skabelon** skal du vælge skabelonen **Marketingskabelon**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="51dc1-140">Under **Sidenavn** skal du angive **Marketingside** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="51dc1-141">På pladsen **Hoved** på den nye side skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="51dc1-142">I dialogboksen **Tilføj modul** skal du vælge modulet **Container** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="51dc1-143">Angiv **Bredde**-værdien til **Fuld container** i egenskabsruden for modulet.</span><span class="sxs-lookup"><span data-stu-id="51dc1-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="51dc1-144">På pladsen **Container** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="51dc1-145">I dialogboksen **Tilføj modul** skal du vælge modulet **iFrame** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="51dc1-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="51dc1-146">I ruden med egenskaber for modulet skal du indstille **Mål-URL-adresse** til en ekstern URL-adresse til en video.</span><span class="sxs-lookup"><span data-stu-id="51dc1-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="51dc1-147">Angiv andre egenskaber, f.eks **Overskrift** og **Højde**, som du har brug for.</span><span class="sxs-lookup"><span data-stu-id="51dc1-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="51dc1-148">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="51dc1-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="51dc1-149">Gå til siden Marketing på dit websted.</span><span class="sxs-lookup"><span data-stu-id="51dc1-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="51dc1-150">Du bør kunne se, at videoen gengives i iFrame-modulet.</span><span class="sxs-lookup"><span data-stu-id="51dc1-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="51dc1-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="51dc1-151">Additional resources</span></span>

[<span data-ttu-id="51dc1-152">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="51dc1-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="51dc1-153">Administrere sikkerhedspolitik for indhold (CSP)</span><span class="sxs-lookup"><span data-stu-id="51dc1-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
