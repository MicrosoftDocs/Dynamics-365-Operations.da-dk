---
title: Tilføj et logo
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914611"
---
# <a name="add-a-logo"></a><span data-ttu-id="fd859-103">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="fd859-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fd859-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer et logo til dit websted i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd859-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd859-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="fd859-105">Overview</span></span>

<span data-ttu-id="fd859-106">Når du bygger dit websted, er en af de første ting, du sandsynligvis vil gøre at tilføje dit virksomheds- eller brandlogo til webstedets header.</span><span class="sxs-lookup"><span data-stu-id="fd859-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="fd859-107">Dynamics 365 Commerce-online startsæt indeholder et modul, der gør denne opgave nem.</span><span class="sxs-lookup"><span data-stu-id="fd859-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="fd859-108">Du kan føje et logo direkte til en skabelon, et layout eller en side.</span><span class="sxs-lookup"><span data-stu-id="fd859-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="fd859-109">På denne måde kan du nemt ændre det logo, der vises på bestemte sider eller grupper af sider.</span><span class="sxs-lookup"><span data-stu-id="fd859-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="fd859-110">Dette emne dækker dog det hyppigst forekommende scenarie, hvor du føjer dit logo til et sidehovedfragment, der kan genbruges på tværs af alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="fd859-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fd859-111">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="fd859-111">Prerequisites</span></span>

<span data-ttu-id="fd859-112">Før du kan føje et logo til alle siderne på dit websted, skal du fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="fd859-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="fd859-113">Overfør dit logo til den digitale aktivmanager, som du kan få adgang til fra siden **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="fd859-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="fd859-114">Opret et sidehovedfragment.</span><span class="sxs-lookup"><span data-stu-id="fd859-114">Create a header fragment.</span></span> <span data-ttu-id="fd859-115">Du kan finde flere oplysninger om, hvordan du opretter og bruger fragmenter i [Arbejd med fragtmenter](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="fd859-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="fd859-116">Medtag sidehovedfragmentet i skabelonen, som bruges til layoutet og modulinstillingerne for siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="fd859-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="fd859-117">Du kan finde flere oplysninger om skabeloner i [Arbejd med skabeloner](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fd859-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="fd859-118">Tilføj et logo til et sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="fd859-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="fd859-119">Følg disse trin for at tilføje et logo til sidehovedfragmentet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="fd859-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="fd859-120">Vælg **Fragmenter** i navigationsruden til venstre, og vælg derefter det sidehovedfragmentet, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="fd859-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="fd859-121">Vælg **Check ud**.</span><span class="sxs-lookup"><span data-stu-id="fd859-121">Select **Check out**.</span></span>
3. <span data-ttu-id="fd859-122">Udvid pladsen **Sidehoved** og **Logo**.</span><span class="sxs-lookup"><span data-stu-id="fd859-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="fd859-123">Vælg ellipseknappen (**...**) for pladsen til **Logo**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="fd859-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="fd859-124">Vælg logomodulet.</span><span class="sxs-lookup"><span data-stu-id="fd859-124">Select the logo module.</span></span>
6. <span data-ttu-id="fd859-125">Derefter skal du konfigurere logomodulet i egenskabsruden til højre, så det afbilleder dit logo.</span><span class="sxs-lookup"><span data-stu-id="fd859-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="fd859-126">Gem sidehovedfragmentet, check det ind, og publicer det.</span><span class="sxs-lookup"><span data-stu-id="fd859-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="fd859-127">Når du har udgivet det opdaterede sidehovedfragment, vises dit logo på alle de webstedssider, som bruger den skabelon, der indeholder sidehovedfragmentet.</span><span class="sxs-lookup"><span data-stu-id="fd859-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd859-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fd859-128">Additional resources</span></span>

[<span data-ttu-id="fd859-129">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="fd859-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="fd859-130">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="fd859-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fd859-131">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="fd859-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="fd859-132">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="fd859-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="fd859-133">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="fd859-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fd859-134">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="fd859-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="fd859-135">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="fd859-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

