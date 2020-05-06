---
title: Forbedre en kategorilandingsside
description: Dette emne omhandler forbedring af kategorisider i Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca31ec7d2eee7d2b0c863506338341a870ff07ee
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269837"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="b9a3f-103">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="b9a3f-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b9a3f-104">Dette emne omhandler forbedring af kategorisider i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b9a3f-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b9a3f-105">Overview</span></span>

<span data-ttu-id="b9a3f-106">Commerce angiver en landingsside for den standardkategori, der bruges, når der vises kategoridata.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="b9a3f-107">En standardkategoriside indeholder de påkrævede elementer, f.eks. afgrænsere, kategoriseret produktplacering, sorteringsindstillinger, en oversigt over valgmuligheder og kontrolelementer til sideinddeling.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="b9a3f-108">Men i stedet for at bruge standardkategorisiden kan du bruge en "forbedret" kategorilandingsside, der har mere indhold og mere specifikke elementer.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="b9a3f-109">En typisk forbedring kan omfatte tilføjelse af kategorispecifikt marketingindhold på kategorisiden.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="b9a3f-110">Dette indhold kan omfatte produktplacering på tværs af kategorier med henblik på tillægssalg, redaktionelle lister, billeder, videoer og anden tekst.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="b9a3f-111">Du kan enten redigere standardkategorisiden eller definere en anden kategoriside for en bestemt kategori.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Forbedre en kategorilandingsside](./media/CategoryLandingPages.png)

<span data-ttu-id="b9a3f-113">I Commerce-webstedsgeneratoren indeholder siden **Produkter** en liste over kategorier fra den kanal, der er tildelt webstedet.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="b9a3f-114">Hvis status **Forbedret** er valgt for en kategoriside, er den pågældende kategoriside blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="b9a3f-115">Ellers bruges standardkategorisiden og standardindholdet til kategorien.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="b9a3f-116">Du kan gennemse både de forbedrede og de ikke-forbedrede kategorisider for en kategori ved at vælge kategorinavnet.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="b9a3f-117">Benyt følgende fremgangsmåde for at forbedre en kategoriside.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="b9a3f-118">Vælg navnet på den kategori, du vil forbedre kategorisiden for, på siden **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="b9a3f-119">Standardkategorisiden for den valgte kategori åbnes i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="b9a3f-120">Vælg **Forbedring af kategoriside**.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="b9a3f-121">Vælg en skabelon til den forbedrede kategoriside.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="b9a3f-122">Hvis du kun foretager mindre ændringer, kan du vælge standardkategorisiden.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="b9a3f-123">Du kan også vælge en bestemt skabelon for kategorisiden.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="b9a3f-124">Når du vælger skabelonen, åbnes sideeditoren, og den valgte skabelon bruges til at oprette en ny kategoriside for den valgte kategori.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="b9a3f-125">Siden er checket ud til dig, og du kan nu foretage dine ændringer.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="b9a3f-126">Moduler, der bruger kategorispecifikationsdata, bruger dataene fra den valgte kategori.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="b9a3f-127">Indstillingerne for den skabelon, du vælger, bestemmer, hvilke ændringer du kan foretage.</span><span class="sxs-lookup"><span data-stu-id="b9a3f-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9a3f-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b9a3f-128">Additional resources</span></span>

[<span data-ttu-id="b9a3f-129">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="b9a3f-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b9a3f-130">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="b9a3f-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b9a3f-131">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="b9a3f-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b9a3f-132">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="b9a3f-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b9a3f-133">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="b9a3f-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b9a3f-134">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="b9a3f-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b9a3f-135">Bekræft tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="b9a3f-135">Verify page content accessibility</span></span>](verify-accessibility.md)
