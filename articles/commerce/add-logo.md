---
title: Tilføje et logo
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797593"
---
# <a name="add-a-logo"></a><span data-ttu-id="c983b-103">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="c983b-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c983b-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c983b-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c983b-105">Når du bygger dit websted, er en af de første ting, du sandsynligvis vil gøre at tilføje dit virksomheds- eller brandlogo til webstedets header.</span><span class="sxs-lookup"><span data-stu-id="c983b-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="c983b-106">Dynamics 365 Commerce-online modulbiblioteket indeholder et modul, der gør denne opgave nem.</span><span class="sxs-lookup"><span data-stu-id="c983b-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="c983b-107">Du kan føje et logo direkte til en skabelon, et layout eller en side.</span><span class="sxs-lookup"><span data-stu-id="c983b-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="c983b-108">På denne måde kan du nemt ændre det logo, der vises på bestemte sider eller grupper af sider.</span><span class="sxs-lookup"><span data-stu-id="c983b-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="c983b-109">Dette emne dækker dog det hyppigst forekommende scenarie, hvor du føjer dit logo til et sidehovedfragment, der kan genbruges på tværs af alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="c983b-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c983b-110">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="c983b-110">Prerequisites</span></span>

<span data-ttu-id="c983b-111">Før du kan føje et logo til alle siderne på dit websted, skal du fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="c983b-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="c983b-112">Upload dit logo til mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="c983b-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="c983b-113">Opret et sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="c983b-113">Create a header fragment.</span></span> <span data-ttu-id="c983b-114">Du kan finde flere oplysninger om, hvordan du opretter og bruger fragmenter i [Arbejd med fragtmenter](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="c983b-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="c983b-115">Medtag sidehovedfragmentet i skabelonen, som bruges til layoutet og modulinstillingerne for siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="c983b-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="c983b-116">Du kan finde flere oplysninger om skabeloner i [Arbejd med skabeloner](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c983b-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="c983b-117">Tilføj et logo til et sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="c983b-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="c983b-118">Følg disse trin for at tilføje et logo til sidehovedfragmentet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="c983b-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="c983b-119">Vælg **Fragmenter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="c983b-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c983b-120">Vælg det sidehovedfragment, du oprettede tidligere, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c983b-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="c983b-121">Udvid sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="c983b-121">Expand the header module.</span></span>
1. <span data-ttu-id="c983b-122">Angiv et billede og et link til logoet i egenskabsruden for sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="c983b-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="c983b-123">Gem sidehovedfragmentet, afslut redigeringen, og udgiv det.</span><span class="sxs-lookup"><span data-stu-id="c983b-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="c983b-124">Når du har udgivet det opdaterede sidehovedfragment, vises dit logo på alle de webstedssider, som bruger den skabelon, der indeholder sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="c983b-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c983b-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c983b-125">Additional resources</span></span>

[<span data-ttu-id="c983b-126">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="c983b-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c983b-127">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="c983b-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c983b-128">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="c983b-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c983b-129">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="c983b-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c983b-130">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="c983b-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c983b-131">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="c983b-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="c983b-132">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="c983b-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
