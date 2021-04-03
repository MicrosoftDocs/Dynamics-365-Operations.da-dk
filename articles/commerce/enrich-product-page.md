---
title: Forbedre en produktside
description: Dette emne indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d7899ac79805abeb55323bd21f83b3af38e09b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238672"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="9167e-103">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="9167e-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9167e-104">Dette emne indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9167e-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9167e-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="9167e-105">Overview</span></span>

<span data-ttu-id="9167e-106">Webstedet bruger som standard en generisk side til at vise produktdata.</span><span class="sxs-lookup"><span data-stu-id="9167e-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="9167e-107">Denne side indeholder de grundlæggende oplysninger om produktet og de kontrolelementer, der skal bruges for at sælge det.</span><span class="sxs-lookup"><span data-stu-id="9167e-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="9167e-108">Du kan dog supplere de oplysninger, der kommer fra Commerce Scale Unit, med yderligere billeder eller tekst til et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="9167e-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="9167e-109">Denne proces kaldes forbedring af produktsiden.</span><span class="sxs-lookup"><span data-stu-id="9167e-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="9167e-110">I mange tilfælde skal du bruge en bestemt form for yderligere indhold til dine produkter.</span><span class="sxs-lookup"><span data-stu-id="9167e-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="9167e-111">Når du går til **Retail og Commerce** i oprettelsesværktøjet, får du vist en liste over produkter fra den kanal, der er tildelt til webstedet.</span><span class="sxs-lookup"><span data-stu-id="9167e-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="9167e-112">På denne liste angiver kolonnen **Forbedret**, om produktsiden for et produkt er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="9167e-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="9167e-113">Hvis der vises en markering i kolonnen, findes der en produktside, der er blevet forbedret, for produktet.</span><span class="sxs-lookup"><span data-stu-id="9167e-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="9167e-114">Hvis der ikke vises en markering, bruges standardproduktsiden og -indholdet til produktet.</span><span class="sxs-lookup"><span data-stu-id="9167e-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="9167e-115">Du kan gennemse både forbedrede og ikke-forbedrede produktsider ved at vælge et produktnavn på listen.</span><span class="sxs-lookup"><span data-stu-id="9167e-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="9167e-116">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="9167e-116">Enrich a product page</span></span>

<span data-ttu-id="9167e-117">Følg disse trin for at forbedre en produktside.</span><span class="sxs-lookup"><span data-stu-id="9167e-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="9167e-118">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="9167e-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="9167e-119">Vælg **Produkter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="9167e-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="9167e-120">Vælg et produkt, der ikke har en forbedret produktside.</span><span class="sxs-lookup"><span data-stu-id="9167e-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="9167e-121">Vælg **Forbedre en produktside** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9167e-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="9167e-122">Vælg **PDP-skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9167e-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9167e-123">Udvid **Hoved**-pladsen i dispositionstræet for siden til venstre.</span><span class="sxs-lookup"><span data-stu-id="9167e-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="9167e-124">Vælg ellipseknappen (**...**) til **Hoved**-pladsen, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="9167e-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="9167e-125">Vælg **Container 2**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9167e-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="9167e-126">Vælg ellipseknappen til **Container 2**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="9167e-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="9167e-127">Vælg **Funktion**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9167e-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="9167e-128">Angiv den opdaterede beskrivelse af produktet i feltet **RTF** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="9167e-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="9167e-129">Angiv overskriftstekst i feltet **Overskrift**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9167e-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="9167e-130">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="9167e-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="9167e-131">Angiv **Forbedrede et produkt** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9167e-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="9167e-132">Hvis du vil se en forhåndsvisning af den forbedrede produktside, skal du vælge **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="9167e-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="9167e-133">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="9167e-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="9167e-134">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="9167e-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9167e-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9167e-135">Additional resources</span></span>

[<span data-ttu-id="9167e-136">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="9167e-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="9167e-137">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="9167e-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="9167e-138">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="9167e-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="9167e-139">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="9167e-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="9167e-140">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="9167e-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="9167e-141">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="9167e-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="9167e-142">Bekræfte tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="9167e-142">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="9167e-143">Oprette dynamiske e-handelssider baseret på URL-parametre</span><span class="sxs-lookup"><span data-stu-id="9167e-143">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]