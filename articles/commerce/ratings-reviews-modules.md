---
title: Moduler til vurderinger og anmeldelser
description: I dette emne beskrives de vurderinger og vurderingsmoduler, der bruges på siderne med produktdetaljer i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 26658ebdbc70613baf30c344664133b9cf5911ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243763"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="434c6-103">Moduler til vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="434c6-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="434c6-104">I dette emne beskrives de vurderinger og vurderingsmoduler, der bruges på siderne med produktdetaljer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="434c6-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="434c6-105">Vurderinger og anmeldelser på e-Commerce-websteder gør det lettere for kunder at få oplysninger om produkter, før de træffer en beslutning om køb, og er også en mekanisme til at indsamle kundefeedback om produkter.</span><span class="sxs-lookup"><span data-stu-id="434c6-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="434c6-106">Vurderinger vises på produktlistesider, sider med kategorilister, søgeresultater og andre sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="434c6-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="434c6-107">Vurderingshistogrammer og produktanmeldelser vises på PDP'er.</span><span class="sxs-lookup"><span data-stu-id="434c6-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="434c6-108">Ved hjælp af knappen **Skriv en anmeldelse** kan kunderne sende vurderinger og anmeldelser af et produkt.</span><span class="sxs-lookup"><span data-stu-id="434c6-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="434c6-109">Disse PDP-funktioner styres af klassifikations- og evalueringsmoduler.</span><span class="sxs-lookup"><span data-stu-id="434c6-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="434c6-110">Modul til vurderinger og anmeldelser på produktoplysningssider</span><span class="sxs-lookup"><span data-stu-id="434c6-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="434c6-111">Tre moduler viser oversigten over vurderinger og anmeldelser på produktoplysningssider:</span><span class="sxs-lookup"><span data-stu-id="434c6-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="434c6-112">Modul til skrivning af anmeldelser</span><span class="sxs-lookup"><span data-stu-id="434c6-112">Write review module</span></span>
- <span data-ttu-id="434c6-113">Modul med produktanmeldelseslister</span><span class="sxs-lookup"><span data-stu-id="434c6-113">Product reviews list module</span></span>
- <span data-ttu-id="434c6-114">Vurderingshistogrammodul</span><span class="sxs-lookup"><span data-stu-id="434c6-114">Ratings histogram module</span></span>
 
<span data-ttu-id="434c6-115">Følgende illustration viser, hvordan vurderings- og anmeldelsesmodulerne ser ud på en side med produktoplysninger (PDP).</span><span class="sxs-lookup"><span data-stu-id="434c6-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Modul til vurderinger og anmeldelser på en produktoplysningsside](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="434c6-117">Yderligere oplysninger om optimering af PDP-skabeloner og -layout med henblik på deling af konfigurationerne til vurderings- og anmeldelsesmoduler mellem flere PDP'er på dit e-handelswebsted, finder du under [Oversigt over skabeloner og layout](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="434c6-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="434c6-118">I følgende illustration vises, hvordan dialogboksen **Tilføj modul** viser vurderings- og anmeldelsesmoduler i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="434c6-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="434c6-119">![Dialogboksen Tilføj modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="434c6-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="434c6-120">Modul til skrivning af anmeldelser</span><span class="sxs-lookup"><span data-stu-id="434c6-120">Write review module</span></span>

<span data-ttu-id="434c6-121">Modulet til skrivning af anmeldelser omfatter knappen **Skriv en anmeldelse**, der giver brugere mulighed for at logge på, tildele en vurdering og skrive en anmeldelse af et produkt.</span><span class="sxs-lookup"><span data-stu-id="434c6-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="434c6-122">I dette modul kan brugerne også redigere en vurdering eller en anmeldelse, som de tidligere har sendt.</span><span class="sxs-lookup"><span data-stu-id="434c6-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="434c6-123">Dette modul vises typisk over modulerne med vurderings- og anmeldelseslister på en produktoplysningsside.</span><span class="sxs-lookup"><span data-stu-id="434c6-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="434c6-124">I følgende illustration vises dialogboksen **Skriv en anmeldelse**, der vises, når en kunde vælger **Skriv en anmeldelse**.</span><span class="sxs-lookup"><span data-stu-id="434c6-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="434c6-125">Kunden kan bruge denne dialogboks til at sende en vurdering og en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="434c6-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="434c6-126">![Dialogboksen Skriv en anmeldelse](media/rnr-eCommerce-write-review-module.png) Følgende tabel viser den egenskab for modulet til skrivning af anmeldelser, der skal konfigureres i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="434c6-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="434c6-127">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="434c6-127">Property name</span></span> | <span data-ttu-id="434c6-128">Værdi</span><span class="sxs-lookup"><span data-stu-id="434c6-128">Value</span></span>        | <span data-ttu-id="434c6-129">Beskrivelse af egenskab</span><span class="sxs-lookup"><span data-stu-id="434c6-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="434c6-130">Navn</span><span class="sxs-lookup"><span data-stu-id="434c6-130">Name</span></span>          | <span data-ttu-id="434c6-131">Skriv anmeldelse</span><span class="sxs-lookup"><span data-stu-id="434c6-131">Write review</span></span> | <span data-ttu-id="434c6-132">Navnet på modulet til skrivning af anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="434c6-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="434c6-133">Vurderingshistogrammodul</span><span class="sxs-lookup"><span data-stu-id="434c6-133">Ratings histogram module</span></span>

<span data-ttu-id="434c6-134">Vurderingshistogrammodulet viser et histogram over vurderinger.</span><span class="sxs-lookup"><span data-stu-id="434c6-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="434c6-135">Dette modul vises typisk mellem modulet til skrivning af anmeldelse og modulet med liste over produktanmeldelser på en produktoplysningsside (PDP).</span><span class="sxs-lookup"><span data-stu-id="434c6-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="434c6-136">Vurderingshistogrammodulet kræver ingen konfiguration.</span><span class="sxs-lookup"><span data-stu-id="434c6-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="434c6-137">Du skal blot tilføje modulet i PDP-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="434c6-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="434c6-138">I følgende illustrationer vises, hvordan en PDP-skabelon ser ud i Dynamics 365 Commerce, når vurderings- og anmeldelsesmoduler er konfigureret til visning på PDP'er.</span><span class="sxs-lookup"><span data-stu-id="434c6-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="434c6-139">![PDP-skabelon, når vurderinger og anmeldelser er konfigureret til visning på PDP'er](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="434c6-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="434c6-140">Modul med produktanmeldelseslister</span><span class="sxs-lookup"><span data-stu-id="434c6-140">Product reviews list module</span></span>

<span data-ttu-id="434c6-141">Modulet med lister over produktanmeldelser viser en oversigt over produktanmeldelser sammen med indstillinger for sortering, filtrering og sideinddeling.</span><span class="sxs-lookup"><span data-stu-id="434c6-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="434c6-142">Dette modul vises typisk efter vurderingshistogrammodulet på en PDP.</span><span class="sxs-lookup"><span data-stu-id="434c6-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="434c6-143">Følgende tabel viser de egenskaber for modulet med produktanmeldelseslister, der skal konfigureres i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="434c6-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="434c6-144">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="434c6-144">Property name</span></span>              | <span data-ttu-id="434c6-145">Værdi</span><span class="sxs-lookup"><span data-stu-id="434c6-145">Value</span></span> | <span data-ttu-id="434c6-146">Beskrivelse af egenskab</span><span class="sxs-lookup"><span data-stu-id="434c6-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="434c6-147">Anmeldelser, der vises på hver side</span><span class="sxs-lookup"><span data-stu-id="434c6-147">Reviews shown on each page</span></span> | <span data-ttu-id="434c6-148">10</span><span class="sxs-lookup"><span data-stu-id="434c6-148">10</span></span>    | <span data-ttu-id="434c6-149">Det antal anmeldelser, der skal vises ad gangen på en PDP.</span><span class="sxs-lookup"><span data-stu-id="434c6-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="434c6-150">Knapperne **Næste** og **Forrige** er medtaget, så brugerne kan bevæge sig gennem siderne i en anmeldelse.</span><span class="sxs-lookup"><span data-stu-id="434c6-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="434c6-151">Vurderingshistogram – oversigtsvisning</span><span class="sxs-lookup"><span data-stu-id="434c6-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="434c6-152">Modulet med produktanmeldelseslister indeholder en plads, hvor du kan tilføje et vurderingshistogrammodul.</span><span class="sxs-lookup"><span data-stu-id="434c6-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="434c6-153">I følgende illustration vises, hvordan du kan tilføje et vurderingshistogrammodul i modulet med produktanmeldelseslister i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="434c6-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Tilføje et vurderingshistogrammodul i et modul med produktanmeldelseslister](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="434c6-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="434c6-155">Additional resources</span></span>

[<span data-ttu-id="434c6-156">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="434c6-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="434c6-157">Container-modul</span><span class="sxs-lookup"><span data-stu-id="434c6-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="434c6-158">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="434c6-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="434c6-159">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="434c6-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="434c6-160">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="434c6-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="434c6-161">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="434c6-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="434c6-162">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="434c6-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]