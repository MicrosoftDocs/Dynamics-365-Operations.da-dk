---
title: Oprette en side-URL
description: I dette emne beskrives de grundlæggende begreber og procedurer til oprettelse af en URL-adresse til en side på dit websted.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: ab7325dd4060392ed43e59c1ad48069d294d81c0
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697542"
---
# <a name="create-a-page-url"></a><span data-ttu-id="2d008-103">Oprette en side-URL</span><span class="sxs-lookup"><span data-stu-id="2d008-103">Create a page URL</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2d008-104">I dette emne beskrives de grundlæggende begreber og procedurer til oprettelse af en URL-adresse til en side på dit websted.</span><span class="sxs-lookup"><span data-stu-id="2d008-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="2d008-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="2d008-105">Overview</span></span>

<span data-ttu-id="2d008-106">Den fuldstændige eller absolutte URL-adresse, der peger på en side på dit websted, består af særskilte dele.</span><span class="sxs-lookup"><span data-stu-id="2d008-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="2d008-107">URL-adressen `https://www.contoso.com/en-us/contactus` har f.eks. følgende dele:</span><span class="sxs-lookup"><span data-stu-id="2d008-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="2d008-108">`https://www.contoso.com` – HTTP-protokollen og webstedets domæne.</span><span class="sxs-lookup"><span data-stu-id="2d008-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="2d008-109">`/en-us` – Webstedets sprogsti.</span><span class="sxs-lookup"><span data-stu-id="2d008-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="2d008-110">`/contactus` – Den relative URL-adresse til siden **Kontakt os**.</span><span class="sxs-lookup"><span data-stu-id="2d008-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="2d008-111">En relativ URL-adresse kaldes også en *URL-slug*.</span><span class="sxs-lookup"><span data-stu-id="2d008-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="2d008-112">Du angiver webstedets domæne og den valgfrie sprogsti, når du konfigurerer webstedet.</span><span class="sxs-lookup"><span data-stu-id="2d008-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="2d008-113">Du kan føje flere domæner og sprogstier til webstedet via siden for onlinebutikker i indstillingerne for webstedet.</span><span class="sxs-lookup"><span data-stu-id="2d008-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="2d008-114">URL-sluggen for en side findes som en selvstændig enhed i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="2d008-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="2d008-115">En sides URL-adresse består af to dele: et navn, der repræsenterer URL-sluggen, og en pointer til en side på enten webstedet eller et eksternt websted.</span><span class="sxs-lookup"><span data-stu-id="2d008-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="2d008-116">En side-URL-adresse kan også konfigureres til at fungere som omdirigering til en anden side på enten webstedet eller et eksternt websted.</span><span class="sxs-lookup"><span data-stu-id="2d008-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="2d008-117">Oprette en side-URL</span><span class="sxs-lookup"><span data-stu-id="2d008-117">Create a page URL</span></span>

<span data-ttu-id="2d008-118">Der er to måder at oprette side-URL-adresser på:</span><span class="sxs-lookup"><span data-stu-id="2d008-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="2d008-119">Automatisk, når du opretter en side</span><span class="sxs-lookup"><span data-stu-id="2d008-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="2d008-120">Manuelt fra siden **URL-adresser**</span><span class="sxs-lookup"><span data-stu-id="2d008-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="2d008-121">Oprette en side-URL-adresse, når du opretter en side</span><span class="sxs-lookup"><span data-stu-id="2d008-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="2d008-122">Hvis du angiver et navn i feltet **URL-adresse**, når du opretter en ny side, oprettes der automatisk en side-URL-adresse, der peger på den pågældende side, på siden **URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="2d008-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="2d008-123">Når du har publiceret URL-adressen og den side, den peger på, kan brugerne af webstedet (dine kunder) få adgang til den side, der er knyttet til URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="2d008-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="2d008-124">Hvis du publicerer en URL-adresse uden at publicere den side, den peger på, får webstedets brugere en 404-fejl, når de forsøger at få adgang til siden.</span><span class="sxs-lookup"><span data-stu-id="2d008-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="2d008-125">Hvis du publicerer en side uden at publicere den URL-adresse, der peger på den, kan der ikke opnås adgang til siden ved hjælp af en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="2d008-126">Oprette en side-URL-adresse manuelt</span><span class="sxs-lookup"><span data-stu-id="2d008-126">Manually create a page URL</span></span>

<span data-ttu-id="2d008-127">Når du opretter nye sider, skal du ikke angive en side-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="2d008-128">Hvis du lader feltet URL-adresse være tomt, oprettes siden i en ikke-sammenkædet tilstand.</span><span class="sxs-lookup"><span data-stu-id="2d008-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="2d008-129">I dette tilfælde kan kunderne ikke få adgang til siden, selvom den er publiceret.</span><span class="sxs-lookup"><span data-stu-id="2d008-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="2d008-130">Hvis du vil gøre siden tilgængelig, skal du oprette URL-adressen manuelt og knytte den til siden.</span><span class="sxs-lookup"><span data-stu-id="2d008-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="2d008-131">Hvis du vil oprette en sides URL-adresse manuelt, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2d008-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="2d008-132">På siden **URL-adresser** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2d008-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="2d008-133">Vælg den side på webstedet, som skal tilknyttes URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="2d008-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="2d008-134">Angiv URL-sluggen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d008-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="2d008-135">På dette tidspunkt er URL-adressen i kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="2d008-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="2d008-136">Den skal publiceres, før brugerne af webstedet kan få adgang til den tilknyttede side.</span><span class="sxs-lookup"><span data-stu-id="2d008-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="2d008-137">Opdatere en side-URL-adresse</span><span class="sxs-lookup"><span data-stu-id="2d008-137">Update a page URL</span></span>

<span data-ttu-id="2d008-138">Udfør følgende trin for at opdatere destinationssiden for en side-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="2d008-139">Vælg den URL-adresse, der skal opdateres, på siden **URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="2d008-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="2d008-140">Vælg ellipseknappen (**...**) ud for destinationssidefeltet i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="2d008-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="2d008-141">I dialogboksen skal du vælge en anden side og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d008-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="2d008-142">Gem og udgiv URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="2d008-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="2d008-143">Omdirigere en side-URL-adresse</span><span class="sxs-lookup"><span data-stu-id="2d008-143">Redirect a page URL</span></span>

<span data-ttu-id="2d008-144">Det kan ske, at du ønsker, at dine kunder skal have vist en anden side, når de anmoder om en bestemt URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="2d008-145">I disse tilfælde er den bedste og nemmeste fremgangsmåde ofte at ændre den side, som side-URL-adressen peger på.</span><span class="sxs-lookup"><span data-stu-id="2d008-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="2d008-146">Du kan dog have berettigede grunde til at bruge HTTP 301- eller 3023-omdirigeringer til at omdirigere anmodninger om en URL-adresse til en anden URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="2d008-147">Hvis du vil omdirigere en URL-adresse til en anden URL-adresse, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2d008-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="2d008-148">Vælg den URL-adresse, der skal opdateres, på siden **URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="2d008-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="2d008-149">Vælg **Omdiriger** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="2d008-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="2d008-150">Vælg en destination for omdirigeringen:</span><span class="sxs-lookup"><span data-stu-id="2d008-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="2d008-151">Hvis du vil pege på en anden side på dit websted, skal du vælge **Intern URL-adresse**, vælge ellipseknappen (**...**) og derefter vælge den URL-adresse, der skal omdirigeres til.</span><span class="sxs-lookup"><span data-stu-id="2d008-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="2d008-152">Hvis du vil pege på en side på det eksterne websted, skal du vælge **Ekstern URL-adresse** og derefter angive den fuldstændige URL-adresse for denne side.</span><span class="sxs-lookup"><span data-stu-id="2d008-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="2d008-153">Husk at medtage protokollen.</span><span class="sxs-lookup"><span data-stu-id="2d008-153">Be sure to include the protocol.</span></span> <span data-ttu-id="2d008-154">Angiv for eksempel `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="2d008-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="2d008-155">Hvis URL-adressen allerede omdirigerer til en intern URL-adresse, skal du vælge **Ryd valg**, før du kan angive en ekstern URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="2d008-156">Vælg en omdirigeringstype:</span><span class="sxs-lookup"><span data-stu-id="2d008-156">Select a redirect type:</span></span>

    - <span data-ttu-id="2d008-157">**Permanent omdirigering (301)** – Vælg denne indstilling, når du ved, at dit indhold flyttes permanent og ikke vender tilbage til den forrige URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="2d008-158">Søgemaskiner tildeler SEO-værdien (Search Engine Optimization) for URL-adressen til omdirigering til den URL-adresse, der omdirigeres til, og opdaterer deres post til at vise den nye URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="2d008-159">**Midlertidig omdirigering (302)** – Vælg denne indstilling for at omdirigere trafik uden at opdatere søgemaskiner.</span><span class="sxs-lookup"><span data-stu-id="2d008-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="2d008-160">Denne fremgangsmåde bruges typisk, hvis indholdet hurtigt vender tilbage til den forrige URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="2d008-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="2d008-161">Når du er klar til at implementere omdirigeringen, skal du gemme og udgive URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="2d008-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d008-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2d008-162">Additional resources</span></span>

[<span data-ttu-id="2d008-163">Tilpasse navigation på webstedet</span><span class="sxs-lookup"><span data-stu-id="2d008-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="2d008-164">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="2d008-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2d008-165">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="2d008-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2d008-166">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="2d008-166">Add languages to your site</span></span>](add-languages-to-site.md)
