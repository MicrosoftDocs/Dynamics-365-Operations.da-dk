---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901490"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="e6265-103">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="e6265-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6265-104">I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="e6265-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="e6265-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="e6265-105">Overview</span></span>

<span data-ttu-id="e6265-106">Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="e6265-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="e6265-107">Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="e6265-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="e6265-108">De fleste webanalysepakker kræver, at du tilføjer scriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="e6265-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="e6265-109">Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="e6265-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="e6265-110">Oprette et fragment, der kan genbruges, til scriptkoden</span><span class="sxs-lookup"><span data-stu-id="e6265-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="e6265-111">Et fragment giver dig mulighed for at genbruge indbygget eller ekstern scriptkode på alle sider på webstedet, uanset hvilken skabelon de bruger.</span><span class="sxs-lookup"><span data-stu-id="e6265-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="e6265-112">Oprette et fragment, der kan genbruges, til den indbyggede scriptkode</span><span class="sxs-lookup"><span data-stu-id="e6265-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="e6265-113">Udfør følgende trin for at oprette et fragment, der kan genbruges, til den indbyggede scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="e6265-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6265-114">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e6265-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="e6265-115">Vælg **Indbygget script** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="e6265-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="e6265-116">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6265-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e6265-117">Vælg modulet **Indbygget standardscript** under det fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="e6265-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="e6265-118">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e6265-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="e6265-119">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="e6265-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e6265-120">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="e6265-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e6265-121">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e6265-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="e6265-122">Oprette et fragment, der kan genbruges, til den eksterne scriptkode</span><span class="sxs-lookup"><span data-stu-id="e6265-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="e6265-123">Udfør følgende trin for at oprette et fragment, der kan genbruges, til den eksterne scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="e6265-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6265-124">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e6265-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="e6265-125">Vælg **Eksternt script** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="e6265-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="e6265-126">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6265-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e6265-127">Vælg modulet **Eksternt standardscript** under det fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="e6265-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="e6265-128">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e6265-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="e6265-129">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="e6265-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e6265-130">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="e6265-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e6265-131">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e6265-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="e6265-132">Hvis du har aktiveret indholdssikkerhedspolitik (CSP) for webstedet, skal du kontrollere, at alle eksterne URL-adresser er føjet til CSP-direktivet **script-src** i Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="e6265-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="e6265-133">Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="e6265-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="e6265-134">Tilføje et fragment, der indeholder scriptkode, i en skabelon</span><span class="sxs-lookup"><span data-stu-id="e6265-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="e6265-135">Udfør følgende trin for at føje et fragment, der indeholder scriptkode, til en skabelon, i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="e6265-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6265-136">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="e6265-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e6265-137">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="e6265-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e6265-138">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="e6265-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="e6265-139">Vælg det fragment, du har oprettet til scriptkoden.</span><span class="sxs-lookup"><span data-stu-id="e6265-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="e6265-140">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="e6265-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e6265-141">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e6265-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="e6265-142">Føje et eksternt script eller indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="e6265-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="e6265-143">Hvis du vil indsætte et indbygget eller eksternt script direkte i et sæt sider, der styres af en enkelt skabelon, behøver du ikke oprette et fragment først.</span><span class="sxs-lookup"><span data-stu-id="e6265-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="e6265-144">Føje et indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="e6265-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="e6265-145">Hvis du vil føje et indbygget script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e6265-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6265-146">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="e6265-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e6265-147">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="e6265-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e6265-148">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e6265-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6265-149">Vælg **Indbygget script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e6265-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="e6265-150">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e6265-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="e6265-151">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="e6265-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e6265-152">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="e6265-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e6265-153">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e6265-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="e6265-154">Føje et eksternt script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="e6265-154">Add an external script directly to a template</span></span>

<span data-ttu-id="e6265-155">Hvis du vil føje et eksternt script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e6265-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6265-156">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="e6265-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e6265-157">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="e6265-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e6265-158">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e6265-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e6265-159">Vælg **Eksternt script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e6265-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="e6265-160">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e6265-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="e6265-161">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="e6265-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e6265-162">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="e6265-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e6265-163">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e6265-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6265-164">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e6265-164">Additional resources</span></span>

[<span data-ttu-id="e6265-165">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="e6265-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e6265-166">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="e6265-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e6265-167">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="e6265-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e6265-168">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="e6265-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e6265-169">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="e6265-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e6265-170">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="e6265-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e6265-171">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="e6265-171">Add languages to your site</span></span>](add-languages-to-site.md)
