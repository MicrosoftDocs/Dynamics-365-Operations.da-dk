---
title: Tilføj en side med politik om beskyttelse af personlige oplysninger
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer en side med politik om beskyttelse af personlige oplysninger i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a9e09a1d0dbd6c0dc94b5668bb29de6605e2ca9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980201"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="334c1-103">Tilføj en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="334c1-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="334c1-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer en side med politik om beskyttelse af personlige oplysninger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="334c1-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="334c1-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="334c1-105">Overview</span></span>

<span data-ttu-id="334c1-106">Overholdelse af privatlivets fred omfatter organisatoriske foranstaltninger, der informerer webstedets brugere om, hvordan deres data indsamles og håndteres.</span><span class="sxs-lookup"><span data-stu-id="334c1-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="334c1-107">Brugerne kan derefter beslutte, hvordan de ønsker, at deres personlige data skal håndteres, og kan foretage de nødvendige handlinger.</span><span class="sxs-lookup"><span data-stu-id="334c1-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="334c1-108">Gennemse Microsofts erklæring om beskyttelse af personlige oplysninger i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="334c1-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="334c1-109">Hvis du vil gennemse Microsofts erklæring om beskyttelse af personlige oplysninger, mens du er logget på oprettelsesværktøjerne i Dynamics 365 Commerce, skal du vælge knappen **Hjælp** (**?**) i øverste højre hjørne og derefter vælge **Beskyttelse af personlige oplysninger og cookies**.</span><span class="sxs-lookup"><span data-stu-id="334c1-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="334c1-110">Der åbnes en ny fane, som har et link til [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="334c1-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="334c1-111">Opret en side med politik for beskyttelse af personlige oplysninger for dit websted</span><span class="sxs-lookup"><span data-stu-id="334c1-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="334c1-112">I Dynamics 365 Commerce er der flere måder at give brugere af dit websted adgang til din privatlivspolitik på.</span><span class="sxs-lookup"><span data-stu-id="334c1-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="334c1-113">Dette afsnit viser, hvordan du opretter en side med politik om beskyttelse af personlige oplysninger og derefter refererer til siden ved hjælp af et sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="334c1-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="334c1-114">Følgende vejledning er et eksempel, der viser, hvordan man opbygger en generisk side med politik om beskyttelse af personlige oplysninger for et Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="334c1-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="334c1-115">Du er ansvarlig for at designe og implementere en side, som indeholder en politik om beskyttelse af personlige oplysninger, og som bedst muligt opfylder lovkravene til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="334c1-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="334c1-116">For at komme i gang skal du i oprettelsesværktøjerne gå til det websted, som du vil oprette en side med politik om beskyttelse af personlige oplysninger for.</span><span class="sxs-lookup"><span data-stu-id="334c1-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="334c1-117">Opret en skabelon</span><span class="sxs-lookup"><span data-stu-id="334c1-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="334c1-118">Hvis der allerede er oprettet en skabelon, som kan bruges til siden med politik for beskyttelse af personlige oplysninger, skal du springe frem til afsnittet [Opret en side med politik om beskyttelse af personlige oplysninger](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="334c1-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="334c1-119">Følg disse trin for at oprette en skabelon.</span><span class="sxs-lookup"><span data-stu-id="334c1-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="334c1-120">Gå til **Skabeloner**, og vælg derefter **Ny** for at oprette en sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="334c1-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="334c1-121">Angiv **Kampagnebannerskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="334c1-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="334c1-122">Tilføj eventuelle påkrævede moduler til de påkrævede sidepladser i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="334c1-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="334c1-123">Hold musen over de røde udråbstegn for vejledning.</span><span class="sxs-lookup"><span data-stu-id="334c1-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="334c1-124">(For eksempel kræver pladsen **HTML-hoved** muligvis et **Eksternt standardscript**-modul).</span><span class="sxs-lookup"><span data-stu-id="334c1-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="334c1-125">På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.</span><span class="sxs-lookup"><span data-stu-id="334c1-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="334c1-126">I modulet **Standardside** skal du på pladsen **Primær** tilføje et **Indholdsrig blokmodul**.</span><span class="sxs-lookup"><span data-stu-id="334c1-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="334c1-127">I **Indholdsrigt blokmodul** skal du tilføje et **Indholdsrigt blokelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="334c1-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="334c1-128">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="334c1-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="334c1-129">Opret en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="334c1-129">Build a privacy policy page</span></span>

<span data-ttu-id="334c1-130">Følg disse trin for at oprette en side med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="334c1-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="334c1-131">Gå til **Sider**, og vælg derefter **Ny** for at oprette en side.</span><span class="sxs-lookup"><span data-stu-id="334c1-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="334c1-132">Vælg skabelonen til siden med politikken for beskyttelse af personlige oplysninger i dialogboksen **Vælg en skabelon**.</span><span class="sxs-lookup"><span data-stu-id="334c1-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="334c1-133">Angiv et sidenavn og sidens URL-adresse, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="334c1-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="334c1-134">På pladsen **Primær** på siden skal du tilføje et **Indholdsrigt blokmodul**.</span><span class="sxs-lookup"><span data-stu-id="334c1-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="334c1-135">I **Indholdsrigt blokmodul** skal du tilføje et **Indholdsrigt blokelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="334c1-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="334c1-136">I egenskabsruden for **Indholdsrigt blokmodul** skal du vælge **Tilføj datakilde** og derefter vælge **RTF-indhold**.</span><span class="sxs-lookup"><span data-stu-id="334c1-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="334c1-137">I RTF-editoren skal du angive indholdet til siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="334c1-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="334c1-138">Udvid RTF-editoren til fuldskærmstilstand efter behov.</span><span class="sxs-lookup"><span data-stu-id="334c1-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="334c1-139">Når du er færdig med at indtaste indholdet, skal du vælge **Forhåndsvisning** for at få vist siden i webbrowseren.</span><span class="sxs-lookup"><span data-stu-id="334c1-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="334c1-140">Gør eventuelle resterende tilføjelser til sidens og modulets egenskaber færdig.</span><span class="sxs-lookup"><span data-stu-id="334c1-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="334c1-141">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="334c1-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="334c1-142">Følg disse trin for at publicere URL-adressen til siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="334c1-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="334c1-143">Gå til **URL**, og vælg URL-adressen for siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="334c1-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="334c1-144">Vælg **Publicer** for at publicere den valgte URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="334c1-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="334c1-145">Opret et link til siden med politik om beskyttelse af personlige oplysninger i en sidefod</span><span class="sxs-lookup"><span data-stu-id="334c1-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="334c1-146">Du kan tilføje et link til siden med politik om beskyttelse af personlige oplysninger til et fragment.</span><span class="sxs-lookup"><span data-stu-id="334c1-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="334c1-147">På denne måde kan du dele linket og opdatere det på tværs af flere webstedssider ved at referere til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="334c1-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="334c1-148">I dette eksempel vises, hvordan du føjer et link til siden med politik om beskyttelse af personlige oplysninger til et sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="334c1-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="334c1-149">Følg disse trin for at føje et link til sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="334c1-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="334c1-150">Gå til **Fragmenter**, og vælg derefter **Nyt** for at oprette et sidefragment.</span><span class="sxs-lookup"><span data-stu-id="334c1-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="334c1-151">Vælg modulet **Sidefod** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="334c1-151">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="334c1-152">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="334c1-152">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="334c1-153">På pladsen **Sidefodskategori** skal du tilføje modulet **Sidefodselement**.</span><span class="sxs-lookup"><span data-stu-id="334c1-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="334c1-154">Vælg **Linktekst** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="334c1-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="334c1-155">I dialogboksen **Linktekst** skal du angive linkteksten og linkmålet på siden med politik om beskyttelse af personlige oplysninger og derefter klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="334c1-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="334c1-156">Hvis du vil have URL-adressen tilføjet til siden med politik om beskyttelse af personlige oplysninger, skal du gå til **Sider** og derefter til siden med politik om beskyttelse af personlige oplysninger og kopierer URL-adressen fra egenskabsruden.</span><span class="sxs-lookup"><span data-stu-id="334c1-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="334c1-157">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="334c1-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="334c1-158">Se et eksempel på fragmentet, og test linket til siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="334c1-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="334c1-159">Der kan nu refereres til fragmentet i skabelonen for andre webstedssider.</span><span class="sxs-lookup"><span data-stu-id="334c1-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="334c1-160">Når der refereres til dette fragment i modulet **Sidefod** i en skabelon, vises linkreferencen på alle sider, der er oprettet ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="334c1-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="334c1-161">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="334c1-161">Additional resources</span></span>

[<span data-ttu-id="334c1-162">Oversigt over overholdelse</span><span class="sxs-lookup"><span data-stu-id="334c1-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="334c1-163">Tilgængelighedsfunktioner og -egenskaber</span><span class="sxs-lookup"><span data-stu-id="334c1-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="334c1-164">Cookie-compliance</span><span class="sxs-lookup"><span data-stu-id="334c1-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="334c1-165">Erstatte bruger-id'er, der er tilknyttet sporede indholdsændringer</span><span class="sxs-lookup"><span data-stu-id="334c1-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
