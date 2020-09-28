---
title: Tilføje scriptkode til sider på websteder for at understøtte telemetri
description: I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761243"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="90565-103">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="90565-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="90565-104">I dette emne beskrives det, hvordan du føjer klientside-scriptkode til siderne på webstedet for at understøtte samlingen af telemetri på klientsiden.</span><span class="sxs-lookup"><span data-stu-id="90565-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="90565-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="90565-105">Overview</span></span>

<span data-ttu-id="90565-106">Web Analytics er et vigtigt værktøj, når du vil forstå, hvordan dine kunder interagerer med dit websted og træffe beslutninger, der kan hjælpe med at optimere oplevelsen i forbindelse med maksimal konvertering.</span><span class="sxs-lookup"><span data-stu-id="90565-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="90565-107">Der findes mange tilgængelige webanalysepakker, som kan hjælpe dig med at nå disse mål, f. eks. Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="90565-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="90565-108">De fleste webanalysepakker kræver, at du tilføjer scriptkode på klientsiden i **\<head\>**-elementet i HTML-koden for alle siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="90565-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="90565-109">Instruktionerne i dette emne gælder også for andre brugerdefinerede funktioner på klientsiden, som Microsoft Dynamics 365 Commerce ikke tilbyder som oprindelige funktioner.</span><span class="sxs-lookup"><span data-stu-id="90565-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="90565-110">Oprette et fragment, der kan genbruges, til scriptkoden</span><span class="sxs-lookup"><span data-stu-id="90565-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="90565-111">Et fragment giver dig mulighed for at genbruge indbygget eller ekstern scriptkode på alle sider på webstedet, uanset hvilken skabelon de bruger.</span><span class="sxs-lookup"><span data-stu-id="90565-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="90565-112">Oprette et fragment, der kan genbruges, til den indbyggede scriptkode</span><span class="sxs-lookup"><span data-stu-id="90565-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="90565-113">Udfør følgende trin for at oprette et fragment, der kan genbruges, til den indbyggede scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="90565-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90565-114">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="90565-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="90565-115">Vælg **Indbygget script** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="90565-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="90565-116">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="90565-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="90565-117">Vælg modulet **Indbygget standardscript** under det fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="90565-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="90565-118">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="90565-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="90565-119">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="90565-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="90565-120">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="90565-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="90565-121">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="90565-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="90565-122">Oprette et fragment, der kan genbruges, til den eksterne scriptkode</span><span class="sxs-lookup"><span data-stu-id="90565-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="90565-123">Udfør følgende trin for at oprette et fragment, der kan genbruges, til den eksterne scriptkode i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="90565-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90565-124">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="90565-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="90565-125">Vælg **Eksternt script** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="90565-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="90565-126">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="90565-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="90565-127">Vælg modulet **Eksternt standardscript** under det fragment, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="90565-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="90565-128">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="90565-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="90565-129">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="90565-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="90565-130">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="90565-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="90565-131">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="90565-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="90565-132">Tilføje et fragment, der indeholder scriptkode, i en skabelon</span><span class="sxs-lookup"><span data-stu-id="90565-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="90565-133">Udfør følgende trin for at føje et fragment, der indeholder scriptkode, til en skabelon, i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="90565-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90565-134">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="90565-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="90565-135">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="90565-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="90565-136">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="90565-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="90565-137">Vælg det fragment, du har oprettet til scriptkoden.</span><span class="sxs-lookup"><span data-stu-id="90565-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="90565-138">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="90565-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="90565-139">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="90565-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="90565-140">Føje et eksternt script eller indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="90565-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="90565-141">Hvis du vil indsætte et indbygget eller eksternt script direkte i et sæt sider, der styres af en enkelt skabelon, behøver du ikke oprette et fragment først.</span><span class="sxs-lookup"><span data-stu-id="90565-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="90565-142">Føje et indbygget script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="90565-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="90565-143">Hvis du vil føje et indbygget script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="90565-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90565-144">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="90565-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="90565-145">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="90565-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="90565-146">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="90565-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="90565-147">Vælg **Indbygget script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="90565-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="90565-148">Angiv dit klientsidescript under **Indbygget script** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="90565-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="90565-149">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="90565-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="90565-150">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="90565-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="90565-151">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="90565-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="90565-152">Føje et eksternt script til en skabelon</span><span class="sxs-lookup"><span data-stu-id="90565-152">Add an external script directly to a template</span></span>

<span data-ttu-id="90565-153">Hvis du vil føje et eksternt script direkte til en skabelon i webstedsgeneratoren, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="90565-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="90565-154">Gå til **Skabeloner**, og åbn skabelonen for de sider, du vil føje din scriptkode til.</span><span class="sxs-lookup"><span data-stu-id="90565-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="90565-155">Udvid skabelon hierarkiet i ruden til venstre for at få vist pladsen **HTML-hoved**.</span><span class="sxs-lookup"><span data-stu-id="90565-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="90565-156">Vælg ellipseknappen (**...**) i pladsen **HTML-hoved**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="90565-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="90565-157">Vælg **Eksternt script** i dialogboksen **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="90565-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="90565-158">Tilføj en ekstern eller relativ URL-adresse til den eksterne scriptkilde under **Scriptkilde** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="90565-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="90565-159">Konfigurer derefter andre indstillinger efter behov.</span><span class="sxs-lookup"><span data-stu-id="90565-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="90565-160">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="90565-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="90565-161">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="90565-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90565-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="90565-162">Additional resources</span></span>

[<span data-ttu-id="90565-163">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="90565-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="90565-164">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="90565-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="90565-165">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="90565-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="90565-166">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="90565-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="90565-167">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="90565-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="90565-168">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="90565-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="90565-169">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="90565-169">Add languages to your site</span></span>](add-languages-to-site.md)
