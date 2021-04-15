---
title: Konfigurere vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5161755b9e15e93fbb5eeb6404ea0820f7068ea7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796069"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="7eb49-103">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="7eb49-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7eb49-104">I dette emne beskrives, hvordan du konfigurerer dit e-handels-websted, så det kan vise kundevurderinger og -anmeldelser i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb49-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7eb49-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="7eb49-105">Overview</span></span>

<span data-ttu-id="7eb49-106">Vurderinger og anmeldelser på e-Commerce-websteder gør det lettere for kunder at få oplysninger om produkter, før de træffer en beslutning om køb, fordi de kan se, hvad andre kunder mener om disse produkter.</span><span class="sxs-lookup"><span data-stu-id="7eb49-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="7eb49-107">På e-handelswebsteder fungerer vurderinger og anmeldelser også som en mekanisme til indsamling af kundefeedback om produkter.</span><span class="sxs-lookup"><span data-stu-id="7eb49-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="7eb49-108">Konfigurere et websted til visning af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="7eb49-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="7eb49-109">Konfigurationsværdier for vurderinger og anmeldelser, f.eks. leje-ID, anmeldelsers tekstlængde og længden af titler på anmeldelser, konfigureres på webstedsniveau.</span><span class="sxs-lookup"><span data-stu-id="7eb49-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="7eb49-110">Udfør følgende trin for at konfigurere et websted til at vise vurderinger og anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="7eb49-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="7eb49-111">Gå til **Startside \> Websteder**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="7eb49-112">Vælg navnet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="7eb49-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="7eb49-113">Gå til **Webstedsindstillinger \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="7eb49-114">Angiv det maksimale antal tegn som anmeldelsesteksten må have (f.eks. **1000**) i feltet **Anmeldelsens maksimale tekstlængde**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="7eb49-115">Angiv det maksimale antal tegn som anmeldelsestitler må have (f.eks. **55**) i feltet **Maksimal længde af anmeldelsestitel**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="7eb49-116">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="7eb49-117">I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb49-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfiguration af et websted til visning af vurderinger og anmeldelser](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="7eb49-119">Sammenkæde en produktvurdering med anmeldelsessektionen på en PDP</span><span class="sxs-lookup"><span data-stu-id="7eb49-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="7eb49-120">En produktvurdering vises under produkttitlen øverst på PDP.</span><span class="sxs-lookup"><span data-stu-id="7eb49-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="7eb49-121">Produktvurderingen kan konfigureres, så den sammenkædes med sektionen **Anmeldelser** på samme PDP.</span><span class="sxs-lookup"><span data-stu-id="7eb49-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="7eb49-122">Hvis du vil knytte en produktvurdering til sektionen **Anmeldelser** på PDP'en, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7eb49-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="7eb49-123">Åbn PDP-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="7eb49-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="7eb49-124">Gå til **Indstillinger for købefeltcontainermodul**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="7eb49-125">Vælg **Produktvurderinger** under **Købefelt**, og markér derefter afkrydsningsfeltet **Sammenkæd klik til modul med hele anmeldelsen**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="7eb49-126">I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb49-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Sammenkædning af en produktvurdering med anmeldelsessektionen på en PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="7eb49-128">Konfigurere linket til siden til beskyttelse af personlige oplysninger og politik</span><span class="sxs-lookup"><span data-stu-id="7eb49-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="7eb49-129">Følg disse trin for at konfigurere linket til siden om beskyttelse af personlige oplysninger og politik.</span><span class="sxs-lookup"><span data-stu-id="7eb49-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="7eb49-130">Gå til **Startside \> Websteder**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="7eb49-131">Vælg navnet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="7eb49-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="7eb49-132">Gå til **Webstedsindstillinger \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="7eb49-133">Vælg **Tilføj et link** under **RNR - beskyttelse af personlige oplysninger og politik** under fanen **Ruter**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="7eb49-134">Hvis der allerede er angivet et link, og du vil erstatte det, skal du markere linket.</span><span class="sxs-lookup"><span data-stu-id="7eb49-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="7eb49-135">Vælg linket til siden om beskyttelse af personlige oplysninger og politik i dialogboksen **Tilføj et link**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="7eb49-136">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="7eb49-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="7eb49-137">I følgende illustration vises, hvordan denne konfiguration ser ud i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7eb49-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfiguration af linket til siden til beskyttelse af personlige oplysninger og politik](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="7eb49-139">Konfigurer vurderings- og anmeldelsesmoduler på sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="7eb49-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="7eb49-140">For yderligere oplysninger om konfiguration af vurderings- og anmeldelsesmoduler på sider med produktdetaljer se [Vurderings- og anmeldelsesmoduler](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="7eb49-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7eb49-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7eb49-141">Additional resources</span></span>

[<span data-ttu-id="7eb49-142">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="7eb49-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="7eb49-143">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="7eb49-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="7eb49-144">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="7eb49-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="7eb49-145">Konfigurer vurderings- og anmeldelsesmoduler på sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="7eb49-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="7eb49-146">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="7eb49-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]