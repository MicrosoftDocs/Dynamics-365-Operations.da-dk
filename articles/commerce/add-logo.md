---
title: Tilføj et logo
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411028"
---
# <a name="add-a-logo"></a><span data-ttu-id="5945d-103">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="5945d-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5945d-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5945d-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5945d-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="5945d-105">Overview</span></span>

<span data-ttu-id="5945d-106">Når du bygger dit websted, er en af de første ting, du sandsynligvis vil gøre at tilføje dit virksomheds- eller brandlogo til webstedets header.</span><span class="sxs-lookup"><span data-stu-id="5945d-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="5945d-107">Dynamics 365 Commerce-online modulbiblioteket indeholder et modul, der gør denne opgave nem.</span><span class="sxs-lookup"><span data-stu-id="5945d-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="5945d-108">Du kan føje et logo direkte til en skabelon, et layout eller en side.</span><span class="sxs-lookup"><span data-stu-id="5945d-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="5945d-109">På denne måde kan du nemt ændre det logo, der vises på bestemte sider eller grupper af sider.</span><span class="sxs-lookup"><span data-stu-id="5945d-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="5945d-110">Dette emne dækker dog det hyppigst forekommende scenarie, hvor du føjer dit logo til et sidehovedfragment, der kan genbruges på tværs af alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="5945d-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5945d-111">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="5945d-111">Prerequisites</span></span>

<span data-ttu-id="5945d-112">Før du kan føje et logo til alle siderne på dit websted, skal du fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="5945d-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="5945d-113">Upload dit logo til mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="5945d-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="5945d-114">Opret et sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="5945d-114">Create a header fragment.</span></span> <span data-ttu-id="5945d-115">Du kan finde flere oplysninger om, hvordan du opretter og bruger fragmenter i [Arbejd med fragtmenter](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="5945d-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="5945d-116">Medtag sidehovedfragmentet i skabelonen, som bruges til layoutet og modulinstillingerne for siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="5945d-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="5945d-117">Du kan finde flere oplysninger om skabeloner i [Arbejd med skabeloner](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="5945d-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="5945d-118">Tilføj et logo til et sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="5945d-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="5945d-119">Følg disse trin for at tilføje et logo til sidehovedfragmentet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="5945d-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="5945d-120">Vælg **Fragmenter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="5945d-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="5945d-121">Vælg det sidehovedfragment, du oprettede tidligere, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="5945d-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="5945d-122">Udvid sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="5945d-122">Expand the header module.</span></span>
1. <span data-ttu-id="5945d-123">Angiv et billede og et link til logoet i egenskabsruden for sidehovedmodulet.</span><span class="sxs-lookup"><span data-stu-id="5945d-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="5945d-124">Gem sidehovedfragmentet, afslut redigeringen, og udgiv det.</span><span class="sxs-lookup"><span data-stu-id="5945d-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="5945d-125">Når du har udgivet det opdaterede sidehovedfragment, vises dit logo på alle de webstedssider, som bruger den skabelon, der indeholder sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="5945d-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5945d-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5945d-126">Additional resources</span></span>

[<span data-ttu-id="5945d-127">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="5945d-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5945d-128">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="5945d-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5945d-129">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="5945d-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5945d-130">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="5945d-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5945d-131">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="5945d-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5945d-132">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="5945d-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5945d-133">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="5945d-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

