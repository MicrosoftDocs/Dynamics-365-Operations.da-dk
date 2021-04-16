---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797425"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="cb045-103">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="cb045-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb045-104">I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="cb045-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="cb045-105">Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="cb045-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="cb045-106">Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="cb045-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="cb045-107">De fleste webanalysepakker kræver, at du tilføjer scriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="cb045-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="cb045-108">Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="cb045-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="cb045-109">Oprette et fragment, der kan genbruges, til scriptkoden</span><span class="sxs-lookup"><span data-stu-id="cb045-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="cb045-110">Et fragment giver dig mulighed for at genbruge indbygget eller ekstern scriptkode på alle sider på webstedet, uanset hvilken skabelon de bruger.</span><span class="sxs-lookup"><span data-stu-id="cb045-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="cb045-111">Oprette et fragment, der kan genbruges, til den indbyggede scriptkode</span><span class="sxs-lookup"><span data-stu-id="cb045-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="cb045-112">Udfør følgende trin for at oprette et fragment, der kan genbruges, til den indbyggede scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="cb045-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cb045-113">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb045-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="cb045-114">Vælg **Indbygget script** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="cb045-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="cb045-115">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb045-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="cb045-116">Vælg modulet **Indbygget standardscript** under det fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="cb045-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="cb045-117">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cb045-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="cb045-118">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="cb045-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cb045-119">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cb045-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cb045-120">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cb045-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="cb045-121">Oprette et fragment, der kan genbruges, til den eksterne scriptkode</span><span class="sxs-lookup"><span data-stu-id="cb045-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="cb045-122">Udfør følgende trin for at oprette et fragment, der kan genbruges, til den eksterne scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="cb045-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cb045-123">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cb045-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="cb045-124">Vælg **Eksternt script** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="cb045-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="cb045-125">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cb045-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="cb045-126">Vælg modulet **Eksternt standardscript** under det fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="cb045-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="cb045-127">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cb045-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="cb045-128">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="cb045-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cb045-129">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cb045-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cb045-130">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cb045-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="cb045-131">Hvis du har aktiveret indholdssikkerhedspolitik (CSP) for webstedet, skal du kontrollere, at alle eksterne URL-adresser er føjet til CSP-direktivet **script-src** i Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="cb045-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="cb045-132">Du kan finde flere oplysninger under [Administrere sikkerhedspolitik for indhold (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="cb045-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="cb045-133">Tilføje et fragment, der indeholder scriptkode, i en skabelon</span><span class="sxs-lookup"><span data-stu-id="cb045-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="cb045-134">Udfør følgende trin for at føje et fragment, der indeholder scriptkode, til en skabelon, i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="cb045-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cb045-135">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="cb045-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="cb045-136">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="cb045-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cb045-137">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="cb045-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="cb045-138">Vælg det fragment, du har oprettet til scriptkoden.</span><span class="sxs-lookup"><span data-stu-id="cb045-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="cb045-139">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cb045-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cb045-140">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cb045-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="cb045-141">Føje et eksternt script eller indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="cb045-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="cb045-142">Hvis du vil indsætte et indbygget eller eksternt script direkte i et sæt sider, der styres af en enkelt skabelon, behøver du ikke oprette et fragment først.</span><span class="sxs-lookup"><span data-stu-id="cb045-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="cb045-143">Føje et indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="cb045-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="cb045-144">Hvis du vil føje et indbygget script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="cb045-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cb045-145">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="cb045-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="cb045-146">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="cb045-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cb045-147">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="cb045-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb045-148">Vælg **Indbygget script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="cb045-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="cb045-149">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cb045-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="cb045-150">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="cb045-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cb045-151">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cb045-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cb045-152">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cb045-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="cb045-153">Føje et eksternt script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="cb045-153">Add an external script directly to a template</span></span>

<span data-ttu-id="cb045-154">Hvis du vil føje et eksternt script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="cb045-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cb045-155">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="cb045-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="cb045-156">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="cb045-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cb045-157">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="cb045-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cb045-158">Vælg **Eksternt script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="cb045-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="cb045-159">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cb045-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="cb045-160">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="cb045-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cb045-161">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="cb045-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cb045-162">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="cb045-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb045-163">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cb045-163">Additional resources</span></span>

[<span data-ttu-id="cb045-164">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="cb045-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="cb045-165">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="cb045-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="cb045-166">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="cb045-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="cb045-167">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="cb045-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="cb045-168">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="cb045-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="cb045-169">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="cb045-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="cb045-170">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="cb045-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
