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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411004"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="129e8-103">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="129e8-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="129e8-104">Dette emne indeholder en beskrivelse af, hvordan du kan forbedre en produktside i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="129e8-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="129e8-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="129e8-105">Overview</span></span>

<span data-ttu-id="129e8-106">Webstedet bruger som standard en generisk side til at vise produktdata.</span><span class="sxs-lookup"><span data-stu-id="129e8-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="129e8-107">Denne side indeholder de grundlæggende oplysninger om produktet og de kontrolelementer, der skal bruges for at sælge det.</span><span class="sxs-lookup"><span data-stu-id="129e8-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="129e8-108">Du kan dog supplere de oplysninger, der kommer fra Commerce Scale Unit, med yderligere billeder eller tekst til et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="129e8-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="129e8-109">Denne proces kaldes forbedring af produktsiden.</span><span class="sxs-lookup"><span data-stu-id="129e8-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="129e8-110">I mange tilfælde skal du bruge en bestemt form for yderligere indhold til dine produkter.</span><span class="sxs-lookup"><span data-stu-id="129e8-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="129e8-111">Når du går til **Retail og Commerce** i oprettelsesværktøjet, får du vist en liste over produkter fra den kanal, der er tildelt til webstedet.</span><span class="sxs-lookup"><span data-stu-id="129e8-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="129e8-112">På denne liste angiver kolonnen **Forbedret**, om produktsiden for et produkt er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="129e8-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="129e8-113">Hvis der vises en markering i kolonnen, findes der en produktside, der er blevet forbedret, for produktet.</span><span class="sxs-lookup"><span data-stu-id="129e8-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="129e8-114">Hvis der ikke vises en markering, bruges standardproduktsiden og -indholdet til produktet.</span><span class="sxs-lookup"><span data-stu-id="129e8-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="129e8-115">Du kan gennemse både forbedrede og ikke-forbedrede produktsider ved at vælge et produktnavn på listen.</span><span class="sxs-lookup"><span data-stu-id="129e8-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="129e8-116">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="129e8-116">Enrich a product page</span></span>

<span data-ttu-id="129e8-117">Følg disse trin for at forbedre en produktside.</span><span class="sxs-lookup"><span data-stu-id="129e8-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="129e8-118">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="129e8-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="129e8-119">Vælg **Produkter** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="129e8-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="129e8-120">Vælg et produkt, der ikke har en forbedret produktside.</span><span class="sxs-lookup"><span data-stu-id="129e8-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="129e8-121">Vælg **Forbedre en produktside** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="129e8-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="129e8-122">Vælg **PDP-skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="129e8-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="129e8-123">Udvid **Hoved**-pladsen i dispositionstræet for siden til venstre.</span><span class="sxs-lookup"><span data-stu-id="129e8-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="129e8-124">Vælg ellipseknappen (**...**) til **Hoved**-pladsen, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="129e8-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="129e8-125">Vælg **Container 2**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="129e8-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="129e8-126">Vælg ellipseknappen til **Container 2**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="129e8-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="129e8-127">Vælg **Funktion**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="129e8-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="129e8-128">Angiv den opdaterede beskrivelse af produktet i feltet **RTF** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="129e8-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="129e8-129">Angiv overskriftstekst i feltet **Overskrift**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="129e8-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="129e8-130">Vælg **Gem**, og vælg derefter **Afslut redigering**.</span><span class="sxs-lookup"><span data-stu-id="129e8-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="129e8-131">Angiv **Forbedrede et produkt** i feltet **Kommentarer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="129e8-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="129e8-132">Hvis du vil se en forhåndsvisning af den forbedrede produktside, skal du vælge **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="129e8-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="129e8-133">Når du er færdig, skal du lukke eksempelfanen for at vende tilbage til oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="129e8-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="129e8-134">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="129e8-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="129e8-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="129e8-135">Additional resources</span></span>

[<span data-ttu-id="129e8-136">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="129e8-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="129e8-137">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="129e8-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="129e8-138">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="129e8-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="129e8-139">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="129e8-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="129e8-140">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="129e8-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="129e8-141">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="129e8-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="129e8-142">Bekræft tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="129e8-142">Verify page content accessibility</span></span>](verify-accessibility.md)
