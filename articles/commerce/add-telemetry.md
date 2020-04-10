---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154080"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="61670-103">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="61670-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61670-104">I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="61670-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="61670-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="61670-105">Overview</span></span>

<span data-ttu-id="61670-106">Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="61670-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="61670-107">Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="61670-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="61670-108">De fleste webanalysepakker kræver, at du tilføjer klientside-scriptkode i elementet **\<head\>** i HTML-koden for alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="61670-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="61670-109">Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="61670-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="61670-110">Oprette et sidefragment, der kan genbruges, til scriptkoden</span><span class="sxs-lookup"><span data-stu-id="61670-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="61670-111">Et sidefragment giver dig mulighed for at genbruge indbygget eller ekstern scriptkode på alle sider på webstedet, uanset hvilken skabelon de bruger.</span><span class="sxs-lookup"><span data-stu-id="61670-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="61670-112">Oprette et sidefragment, der kan genbruges, til den indbyggede scriptkode</span><span class="sxs-lookup"><span data-stu-id="61670-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="61670-113">Udfør følgende trin for at oprette et sidefragment, der kan genbruges, til den indbyggede scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="61670-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="61670-114">Gå til **Sidefragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="61670-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="61670-115">Vælg **Indbygget script** i dialogboksen **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="61670-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="61670-116">Angiv et navn til fragmentet under **Sidefragmentsnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="61670-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="61670-117">Vælg modulet **Indbygget standardscript** under det sidefragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="61670-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="61670-118">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="61670-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="61670-119">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="61670-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="61670-120">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="61670-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="61670-121">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="61670-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="61670-122">Oprette et sidefragment, der kan genbruges, til den eksterne scriptkode</span><span class="sxs-lookup"><span data-stu-id="61670-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="61670-123">Udfør følgende trin for at oprette et sidefragment, der kan genbruges, til den eksterne scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="61670-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="61670-124">Gå til **Sidefragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="61670-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="61670-125">Vælg **Eksternt script** i dialogboksen **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="61670-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="61670-126">Angiv et navn til fragmentet under **Sidefragmentsnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="61670-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="61670-127">Vælg modulet **Eksternt standardscript** under det sidefragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="61670-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="61670-128">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="61670-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="61670-129">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="61670-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="61670-130">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="61670-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="61670-131">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="61670-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="61670-132">Føje et sidefragment, der indeholder scriptkode, til en skabelon</span><span class="sxs-lookup"><span data-stu-id="61670-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="61670-133">Udfør følgende trin for at føje et sidefragment, der indeholder scriptkode, til en skabelon, i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="61670-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="61670-134">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="61670-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="61670-135">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="61670-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="61670-136">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="61670-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="61670-137">Vælg det fragment, du har oprettet til scriptkoden.</span><span class="sxs-lookup"><span data-stu-id="61670-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="61670-138">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="61670-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="61670-139">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="61670-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="61670-140">Føje et eksternt script eller indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="61670-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="61670-141">Hvis du vil indsætte et indbygget eller eksternt script direkte i et sæt sider, der styres af en enkelt skabelon, behøver du ikke oprette et sidefragment først.</span><span class="sxs-lookup"><span data-stu-id="61670-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="61670-142">Føje et indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="61670-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="61670-143">Hvis du vil føje et indbygget script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="61670-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="61670-144">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="61670-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="61670-145">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="61670-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="61670-146">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="61670-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="61670-147">Vælg **Indbygget script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="61670-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="61670-148">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="61670-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="61670-149">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="61670-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="61670-150">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="61670-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="61670-151">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="61670-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="61670-152">Føje et eksternt script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="61670-152">Add an external script directly to a template</span></span>

<span data-ttu-id="61670-153">Hvis du vil føje et eksternt script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="61670-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="61670-154">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="61670-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="61670-155">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="61670-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="61670-156">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="61670-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="61670-157">Vælg **Eksternt script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="61670-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="61670-158">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="61670-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="61670-159">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="61670-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="61670-160">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="61670-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="61670-161">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="61670-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61670-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="61670-162">Additional resources</span></span>

[<span data-ttu-id="61670-163">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="61670-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="61670-164">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="61670-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="61670-165">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="61670-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="61670-166">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="61670-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="61670-167">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="61670-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="61670-168">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="61670-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="61670-169">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="61670-169">Add languages to your site</span></span>](add-languages-to-site.md)
