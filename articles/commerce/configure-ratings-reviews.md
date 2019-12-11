---
title: Konfigurere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770475"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="97f4e-103">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="97f4e-104">I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f4e-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97f4e-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="97f4e-105">Overview</span></span>

<span data-ttu-id="97f4e-106">Vurderinger og anmeldelser på e-handels-websteder gør det lettere for kunder at få oplysninger om produkter, før de træffer en beslutning om køb, fordi de kan se, hvad andre kunder mener om disse produkter.</span><span class="sxs-lookup"><span data-stu-id="97f4e-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="97f4e-107">På e-handelswebsteder fungerer vurderinger og anmeldelser også som en mekanisme til indsamling af kundefeedback om produkter.</span><span class="sxs-lookup"><span data-stu-id="97f4e-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="97f4e-108">Vurderinger vises på produktlistesider, sider med kategorilister, søgeresultater og andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="97f4e-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="97f4e-109">Vurderingshistogrammer og produktanmeldelser vises på sider med produktoplysninger (PDP'er).</span><span class="sxs-lookup"><span data-stu-id="97f4e-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="97f4e-110">Ved hjælp af knappen **Skriv en anmeldelse** kan kunderne sende vurderinger og anmeldelser af et produkt.</span><span class="sxs-lookup"><span data-stu-id="97f4e-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="97f4e-111">Modul til vurderinger og anmeldelser på produktoplysningssider</span><span class="sxs-lookup"><span data-stu-id="97f4e-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="97f4e-112">Tre moduler viser oversigten over vurderinger og anmeldelser på produktoplysningssider:</span><span class="sxs-lookup"><span data-stu-id="97f4e-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="97f4e-113">Modul til skrivning af anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-113">Write review module</span></span>
- <span data-ttu-id="97f4e-114">Modul med produktanmeldelseslister</span><span class="sxs-lookup"><span data-stu-id="97f4e-114">Product reviews list module</span></span>
- <span data-ttu-id="97f4e-115">Vurderingshistogrammodul</span><span class="sxs-lookup"><span data-stu-id="97f4e-115">Ratings histogram module</span></span>
 
<span data-ttu-id="97f4e-116">Følgende illustration viser, hvordan vurderings- og anmeldelsesmodulerne ser ud på en side med produktoplysninger (PDP).</span><span class="sxs-lookup"><span data-stu-id="97f4e-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Modul til vurderinger og anmeldelser på en produktoplysningsside](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="97f4e-118">Yderligere oplysninger om optimering af PDP-skabeloner og -layout med henblik på deling af konfigurationerne til vurderings- og anmeldelsesmoduler mellem flere PDP'er på dit e-handelswebsted, finder du under [Oversigt over skabeloner og layout](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="97f4e-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="97f4e-119">I følgende illustration vises, hvordan dialogboksen **Tilføj modul** viser vurderings- og anmeldelsesmoduler i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f4e-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Dialogboksen Tilføj modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="97f4e-121">Modul til skrivning af anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-121">Write review module</span></span>

<span data-ttu-id="97f4e-122">Modulet til skrivning af anmeldelser omfatter knappen **Skriv en anmeldelse**, der giver brugere mulighed for at logge på, tildele en vurdering og skrive en anmeldelse af et produkt.</span><span class="sxs-lookup"><span data-stu-id="97f4e-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="97f4e-123">I dette modul kan brugerne også redigere en vurdering eller en anmeldelse, som de tidligere har sendt.</span><span class="sxs-lookup"><span data-stu-id="97f4e-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="97f4e-124">Dette modul vises typisk over modulerne med vurderings- og anmeldelseslister på en produktoplysningsside.</span><span class="sxs-lookup"><span data-stu-id="97f4e-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="97f4e-125">I følgende illustration vises dialogboksen **Skriv en anmeldelse**, der vises, når en kunde vælger **Skriv en anmeldelse**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="97f4e-126">Kunden kan bruge denne dialogboks til at sende en vurdering og en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="97f4e-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Dialogboksen Skriv en anmeldelse](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="97f4e-128">Følgende tabel viser den egenskab for modulet til skrivning af anmeldelser, der skal konfigureres i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="97f4e-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="97f4e-129">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="97f4e-129">Property name</span></span> | <span data-ttu-id="97f4e-130">Værdi</span><span class="sxs-lookup"><span data-stu-id="97f4e-130">Value</span></span>        | <span data-ttu-id="97f4e-131">Beskrivelse af egenskab</span><span class="sxs-lookup"><span data-stu-id="97f4e-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="97f4e-132">Navn</span><span class="sxs-lookup"><span data-stu-id="97f4e-132">Name</span></span>          | <span data-ttu-id="97f4e-133">Skriv anmeldelse</span><span class="sxs-lookup"><span data-stu-id="97f4e-133">Write review</span></span> | <span data-ttu-id="97f4e-134">Navnet på modulet til skrivning af anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="97f4e-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="97f4e-135">Vurderingshistogrammodul</span><span class="sxs-lookup"><span data-stu-id="97f4e-135">Ratings histogram module</span></span>

<span data-ttu-id="97f4e-136">Vurderingshistogrammodulet viser et histogram over vurderinger.</span><span class="sxs-lookup"><span data-stu-id="97f4e-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="97f4e-137">Dette modul vises typisk mellem modulet til skrivning af anmeldelse og modulet med liste over produktanmeldelser på en produktoplysningsside (PDP).</span><span class="sxs-lookup"><span data-stu-id="97f4e-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="97f4e-138">Vurderingshistogrammodulet kræver ingen konfiguration.</span><span class="sxs-lookup"><span data-stu-id="97f4e-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="97f4e-139">Du skal blot tilføje modulet i PDP-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="97f4e-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="97f4e-140">I følgende illustrationer vises, hvordan en PDP-skabelon ser ud i Dynamics 365 Commerce, når vurderings- og anmeldelsesmoduler er konfigureret til visning på PDP'er.</span><span class="sxs-lookup"><span data-stu-id="97f4e-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP-skabelon, når vurderinger og anmeldelser er konfigureret til visning på PDP'er](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="97f4e-142">Modul med produktanmeldelseslister</span><span class="sxs-lookup"><span data-stu-id="97f4e-142">Product reviews list module</span></span>

<span data-ttu-id="97f4e-143">Modulet med lister over produktanmeldelser viser en oversigt over produktanmeldelser sammen med indstillinger for sortering, filtrering og sideinddeling.</span><span class="sxs-lookup"><span data-stu-id="97f4e-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="97f4e-144">Dette modul vises typisk efter vurderingshistogrammodulet på en PDP.</span><span class="sxs-lookup"><span data-stu-id="97f4e-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="97f4e-145">Følgende tabel viser de egenskaber for modulet med produktanmeldelseslister, der skal konfigureres i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="97f4e-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="97f4e-146">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="97f4e-146">Property name</span></span>              | <span data-ttu-id="97f4e-147">Værdi</span><span class="sxs-lookup"><span data-stu-id="97f4e-147">Value</span></span> | <span data-ttu-id="97f4e-148">Beskrivelse af egenskab</span><span class="sxs-lookup"><span data-stu-id="97f4e-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="97f4e-149">Anmeldelser, der vises på hver side</span><span class="sxs-lookup"><span data-stu-id="97f4e-149">Reviews shown on each page</span></span> | <span data-ttu-id="97f4e-150">10</span><span class="sxs-lookup"><span data-stu-id="97f4e-150">10</span></span>    | <span data-ttu-id="97f4e-151">Det antal anmeldelser, der skal vises ad gangen på en PDP.</span><span class="sxs-lookup"><span data-stu-id="97f4e-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="97f4e-152">Knapperne **Næste** og **Forrige** er medtaget, så brugerne kan bevæge sig gennem siderne i en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="97f4e-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="97f4e-153">Vurderingshistogram – oversigtsvisning</span><span class="sxs-lookup"><span data-stu-id="97f4e-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="97f4e-154">Modulet med produktanmeldelseslister indeholder en plads, hvor du kan tilføje et vurderingshistogrammodul.</span><span class="sxs-lookup"><span data-stu-id="97f4e-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="97f4e-155">I følgende illustration vises, hvordan du kan tilføje et vurderingshistogrammodul i modulet med produktanmeldelseslister i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f4e-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Tilføje et vurderingshistogrammodul i et modul med produktanmeldelseslister](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="97f4e-157">Konfigurere et websted til visning af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="97f4e-158">Konfigurationsværdier for vurderinger og anmeldelser, f.eks. leje-ID, anmeldelsers tekstlængde og længden af titler på anmeldelser, konfigureres på webstedsniveau.</span><span class="sxs-lookup"><span data-stu-id="97f4e-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="97f4e-159">Udfør følgende trin for at konfigurere et websted til at vise vurderinger og anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="97f4e-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="97f4e-160">Gå til **Startside \> Websteder**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="97f4e-161">Vælg navnet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="97f4e-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="97f4e-162">Gå til **Administration af websted \> Udvidelsesmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="97f4e-163">Angiv det maksimale antal tegn som anmeldelsesteksten må have (f.eks. **1000**) i feltet **Anmeldelsens maksimale tekstlængde**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="97f4e-164">Angiv det maksimale antal tegn som anmeldelsestitler må have (f.eks. **55**) i feltet **Maksimal længde af anmeldelsestitel**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="97f4e-165">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="97f4e-166">I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f4e-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfiguration af et websted til visning af vurderinger og anmeldelser](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="97f4e-168">Sammenkæde en produktvurdering med anmeldelsessektionen på en PDP</span><span class="sxs-lookup"><span data-stu-id="97f4e-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="97f4e-169">En produktvurdering vises under produkttitlen øverst på PDP.</span><span class="sxs-lookup"><span data-stu-id="97f4e-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="97f4e-170">Produktvurderingen kan konfigureres, så den sammenkædes med sektionen **Anmeldelser** på samme PDP.</span><span class="sxs-lookup"><span data-stu-id="97f4e-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="97f4e-171">Hvis du vil knytte en produktvurdering til sektionen **Anmeldelser** på PDP'en, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="97f4e-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="97f4e-172">Åbn PDP-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="97f4e-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="97f4e-173">Gå til **Indstillinger for købefeltcontainermodul**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="97f4e-174">Vælg **Produktvurderinger** under **Købefelt**, og markér derefter afkrydsningsfeltet **Sammenkæd klik til modul med hele anmeldelsen**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="97f4e-175">I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f4e-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Sammenkædning af en produktvurdering med anmeldelsessektionen på en PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="97f4e-177">Konfigurere linket til siden til beskyttelse af personlige oplysninger og politik</span><span class="sxs-lookup"><span data-stu-id="97f4e-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="97f4e-178">Følg disse trin for at konfigurere linket til siden om beskyttelse af personlige oplysninger og politik.</span><span class="sxs-lookup"><span data-stu-id="97f4e-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="97f4e-179">Gå til **Startside \> Websteder**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="97f4e-180">Vælg navnet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="97f4e-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="97f4e-181">Gå til **Administration af websted \> Udvidelsesmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="97f4e-182">Vælg **Tilføj et link** under **RNR - beskyttelse af personlige oplysninger og politik** under fanen **Ruter**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="97f4e-183">Hvis der allerede er angivet et link, og du vil erstatte det, skal du markere linket.</span><span class="sxs-lookup"><span data-stu-id="97f4e-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="97f4e-184">Vælg linket til siden om beskyttelse af personlige oplysninger og politik i dialogboksen **Tilføj et link**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="97f4e-185">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="97f4e-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="97f4e-186">I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97f4e-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfiguration af linket til siden til beskyttelse af personlige oplysninger og politik](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="97f4e-188">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="97f4e-188">Additional resources</span></span>

[<span data-ttu-id="97f4e-189">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="97f4e-190">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="97f4e-191">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="97f4e-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="97f4e-192">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="97f4e-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
