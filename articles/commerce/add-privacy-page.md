---
title: Tilføj en side med politik om beskyttelse af personlige oplysninger
description: Dette emne indeholder en beskrivelse af, hvordan du tilføjer en side med politik om beskyttelse af personlige oplysninger i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797521"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="36a62-103">Tilføje en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="36a62-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36a62-104">Dette emne indeholder en beskrivelse af, hvordan du tilføjer en side med politik om beskyttelse af personlige oplysninger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="36a62-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="36a62-105">Overholdelse af privatlivets fred omfatter organisatoriske foranstaltninger, der informerer webstedets brugere om, hvordan deres data indsamles og håndteres.</span><span class="sxs-lookup"><span data-stu-id="36a62-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="36a62-106">Brugerne kan derefter beslutte, hvordan de ønsker, at deres personlige data skal håndteres, og kan foretage de nødvendige handlinger.</span><span class="sxs-lookup"><span data-stu-id="36a62-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="36a62-107">Gennemse Microsofts erklæring om beskyttelse af personlige oplysninger i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="36a62-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="36a62-108">Hvis du vil gennemse Microsofts erklæring om beskyttelse af personlige oplysninger, mens du er logget på oprettelsesværktøjerne i Dynamics 365 Commerce, skal du vælge knappen **Hjælp** (**?**) i øverste højre hjørne og derefter vælge **Beskyttelse af personlige oplysninger og cookies**.</span><span class="sxs-lookup"><span data-stu-id="36a62-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="36a62-109">Der åbnes en ny fane, som har et link til [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="36a62-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="36a62-110">Opret en side med politik for beskyttelse af personlige oplysninger for dit websted</span><span class="sxs-lookup"><span data-stu-id="36a62-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="36a62-111">I Dynamics 365 Commerce er der flere måder at give brugere af dit websted adgang til din privatlivspolitik på.</span><span class="sxs-lookup"><span data-stu-id="36a62-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="36a62-112">Dette afsnit viser, hvordan du opretter en side med politik om beskyttelse af personlige oplysninger og derefter refererer til siden ved hjælp af et sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="36a62-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="36a62-113">Følgende vejledning er et eksempel, der viser, hvordan man opbygger en generisk side med politik om beskyttelse af personlige oplysninger for et Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="36a62-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="36a62-114">Du er ansvarlig for at designe og implementere en side, som indeholder en politik om beskyttelse af personlige oplysninger, og som bedst muligt opfylder lovkravene til din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="36a62-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="36a62-115">For at komme i gang skal du i oprettelsesværktøjerne gå til det websted, som du vil oprette en side med politik om beskyttelse af personlige oplysninger for.</span><span class="sxs-lookup"><span data-stu-id="36a62-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="36a62-116">Opret en skabelon</span><span class="sxs-lookup"><span data-stu-id="36a62-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="36a62-117">Hvis der allerede er oprettet en skabelon, som kan bruges til siden med politik for beskyttelse af personlige oplysninger, skal du springe frem til afsnittet [Opret en side med politik om beskyttelse af personlige oplysninger](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="36a62-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="36a62-118">Følg disse trin for at oprette en skabelon.</span><span class="sxs-lookup"><span data-stu-id="36a62-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="36a62-119">Gå til **Skabeloner**, og vælg derefter **Ny** for at oprette en sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="36a62-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="36a62-120">Angiv **Kampagnebannerskabelon** under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="36a62-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="36a62-121">Tilføj eventuelle påkrævede moduler til de påkrævede sidepladser i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="36a62-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="36a62-122">Hold musen over de røde udråbstegn for vejledning.</span><span class="sxs-lookup"><span data-stu-id="36a62-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="36a62-123">(For eksempel kræver pladsen **HTML-hoved** muligvis et **Eksternt standardscript**-modul).</span><span class="sxs-lookup"><span data-stu-id="36a62-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="36a62-124">På pladsen **Brødtekst** skal du tilføje et **Standardside**-modul.</span><span class="sxs-lookup"><span data-stu-id="36a62-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="36a62-125">I modulet **Standardside** skal du på pladsen **Primær** tilføje et **Indholdsrig blokmodul**.</span><span class="sxs-lookup"><span data-stu-id="36a62-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="36a62-126">I **Indholdsrigt blokmodul** skal du tilføje et **Indholdsrigt blokelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="36a62-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="36a62-127">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="36a62-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="36a62-128">Opret en side med politik om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="36a62-128">Build a privacy policy page</span></span>

<span data-ttu-id="36a62-129">Følg disse trin for at oprette en side med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36a62-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="36a62-130">Gå til **Sider**, og vælg derefter **Ny** for at oprette en side.</span><span class="sxs-lookup"><span data-stu-id="36a62-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="36a62-131">Vælg skabelonen til siden med politikken for beskyttelse af personlige oplysninger i dialogboksen **Vælg en skabelon**.</span><span class="sxs-lookup"><span data-stu-id="36a62-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="36a62-132">Angiv et sidenavn og sidens URL-adresse, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="36a62-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="36a62-133">På pladsen **Primær** på siden skal du tilføje et **Indholdsrigt blokmodul**.</span><span class="sxs-lookup"><span data-stu-id="36a62-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="36a62-134">I **Indholdsrigt blokmodul** skal du tilføje et **Indholdsrigt blokelement**-modul.</span><span class="sxs-lookup"><span data-stu-id="36a62-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="36a62-135">I egenskabsruden for **Indholdsrigt blokmodul** skal du vælge **Tilføj datakilde** og derefter vælge **RTF-indhold**.</span><span class="sxs-lookup"><span data-stu-id="36a62-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="36a62-136">I RTF-editoren skal du angive indholdet til siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36a62-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="36a62-137">Udvid RTF-editoren til fuldskærmstilstand efter behov.</span><span class="sxs-lookup"><span data-stu-id="36a62-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="36a62-138">Når du er færdig med at indtaste indholdet, skal du vælge **Forhåndsvisning** for at få vist siden i webbrowseren.</span><span class="sxs-lookup"><span data-stu-id="36a62-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="36a62-139">Gør eventuelle resterende tilføjelser til sidens og modulets egenskaber færdig.</span><span class="sxs-lookup"><span data-stu-id="36a62-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="36a62-140">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="36a62-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="36a62-141">Følg disse trin for at publicere URL-adressen til siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36a62-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="36a62-142">Gå til **URL**, og vælg URL-adressen for siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36a62-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="36a62-143">Vælg **Publicer** for at publicere den valgte URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="36a62-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="36a62-144">Opret et link til siden med politik om beskyttelse af personlige oplysninger i en sidefod</span><span class="sxs-lookup"><span data-stu-id="36a62-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="36a62-145">Du kan tilføje et link til siden med politik om beskyttelse af personlige oplysninger til et fragment.</span><span class="sxs-lookup"><span data-stu-id="36a62-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="36a62-146">På denne måde kan du dele linket og opdatere det på tværs af flere webstedssider ved at referere til fragmentet.</span><span class="sxs-lookup"><span data-stu-id="36a62-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="36a62-147">I dette eksempel vises, hvordan du føjer et link til siden med politik om beskyttelse af personlige oplysninger til et sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="36a62-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="36a62-148">Følg disse trin for at føje et link til sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="36a62-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="36a62-149">Gå til **Fragmenter**, og vælg derefter **Nyt** for at oprette et sidefragment.</span><span class="sxs-lookup"><span data-stu-id="36a62-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="36a62-150">Vælg modulet **Sidefod** i dialogboksen **Nyt fragment**.</span><span class="sxs-lookup"><span data-stu-id="36a62-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="36a62-151">Angiv et navn til fragmentet under **Fragmentnavn**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="36a62-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="36a62-152">På pladsen **Sidefodskategori** skal du tilføje modulet **Sidefodselement**.</span><span class="sxs-lookup"><span data-stu-id="36a62-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="36a62-153">Vælg **Linktekst** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="36a62-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="36a62-154">I dialogboksen **Linktekst** skal du angive linkteksten og linkmålet på siden med politik om beskyttelse af personlige oplysninger og derefter klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="36a62-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="36a62-155">Hvis du vil have URL-adressen tilføjet til siden med politik om beskyttelse af personlige oplysninger, skal du gå til **Sider** og derefter til siden med politik om beskyttelse af personlige oplysninger og kopierer URL-adressen fra egenskabsruden.</span><span class="sxs-lookup"><span data-stu-id="36a62-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="36a62-156">Vælg **Gem**, vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="36a62-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="36a62-157">Se et eksempel på fragmentet, og test linket til siden med politik om beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36a62-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="36a62-158">Der kan nu refereres til fragmentet i skabelonen for andre webstedssider.</span><span class="sxs-lookup"><span data-stu-id="36a62-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="36a62-159">Når der refereres til dette fragment i modulet **Sidefod** i en skabelon, vises linkreferencen på alle sider, der er oprettet ved hjælp af denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="36a62-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36a62-160">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="36a62-160">Additional resources</span></span>

[<span data-ttu-id="36a62-161">Oversigt over overholdelse</span><span class="sxs-lookup"><span data-stu-id="36a62-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="36a62-162">Tilgængelighedsfunktioner og -egenskaber</span><span class="sxs-lookup"><span data-stu-id="36a62-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="36a62-163">Cookie-compliance</span><span class="sxs-lookup"><span data-stu-id="36a62-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="36a62-164">Erstatte bruger-id'er, der er tilknyttet sporede indholdsændringer</span><span class="sxs-lookup"><span data-stu-id="36a62-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
