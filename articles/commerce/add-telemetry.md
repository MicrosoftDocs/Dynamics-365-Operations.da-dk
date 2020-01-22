---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914533"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="12de9-103">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="12de9-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="12de9-104">I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="12de9-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="12de9-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="12de9-105">Overview</span></span>

<span data-ttu-id="12de9-106">Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="12de9-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="12de9-107">Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="12de9-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="12de9-108">De fleste webanalysepakker kræver, at du tilføjer klientside-scriptkode i elementet **\<head\>** i HTML-koden for alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="12de9-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="12de9-109">Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="12de9-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="12de9-110">Oprette et fragment, der kan genbruges, til scriptkoden</span><span class="sxs-lookup"><span data-stu-id="12de9-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="12de9-111">Når du har oprettet et fragment til scriptkoden, kan det genbruges på tværs af alle sider på dit websted.</span><span class="sxs-lookup"><span data-stu-id="12de9-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="12de9-112">Gå til **Fragmenter \> Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="12de9-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="12de9-113">Vælg **Eksternt script**, angiv et navn til fragmentet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="12de9-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="12de9-114">Vælge det underordnede **script-injektor**-modul til det fragment, du lige har oprettet, i fragmenthierarkiet.</span><span class="sxs-lookup"><span data-stu-id="12de9-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="12de9-115">Tilføj klientsidescriptet i egenskabsruden til højre, og angiv andre konfigurationsindstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="12de9-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="12de9-116">Føje fragmentet til skabeloner</span><span class="sxs-lookup"><span data-stu-id="12de9-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="12de9-117">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="12de9-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="12de9-118">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="12de9-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="12de9-119">Vælg ellipseknappen (**...**) for pladsen **HTML-hoved**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="12de9-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="12de9-120">Vælg det fragment, du har oprettet til scriptkoden.</span><span class="sxs-lookup"><span data-stu-id="12de9-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="12de9-121">Gem skabelonen ind, og tjek den ind.</span><span class="sxs-lookup"><span data-stu-id="12de9-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="12de9-122">Når du er færdig, skal du publicere fragmentet og masterskabelonen.</span><span class="sxs-lookup"><span data-stu-id="12de9-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="12de9-123">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="12de9-123">Additional resources</span></span>

[<span data-ttu-id="12de9-124">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="12de9-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="12de9-125">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="12de9-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="12de9-126">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="12de9-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="12de9-127">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="12de9-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="12de9-128">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="12de9-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="12de9-129">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="12de9-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="12de9-130">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="12de9-130">Add languages to your site</span></span>](add-languages-to-site.md)

