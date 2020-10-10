---
title: Tilpasse navigation på webstedet
description: I dette emne beskrives, hvordan du opretter et tilpasset onlinenavigationshierarki for at organisere dine produkter til gennemsyn på dit Microsoft Dynamics 365 Commerce-websted.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817224"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="27687-103">Tilpasse navigation på webstedet</span><span class="sxs-lookup"><span data-stu-id="27687-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="27687-104">I dette emne beskrives, hvordan du opretter et tilpasset onlinenavigationshierarki for at organisere dine produkter til gennemsyn på dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="27687-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="27687-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="27687-105">Overview</span></span>

<span data-ttu-id="27687-106">Onlinestorefronts giver typisk kunderne mulighed for at finde og gennemse produkter ved at navigere gennem produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="27687-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="27687-107">Denne egenskab leveres normalt af faner øverst på siden eller af en navigationslinje i venstre side.</span><span class="sxs-lookup"><span data-stu-id="27687-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="27687-108">I Dynamics 365 Commerce kan du oprette og administrere hierarkistrukturen i kategorinavigationen og de produkter, der er inkluderet i de forskellige kategorier.</span><span class="sxs-lookup"><span data-stu-id="27687-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="27687-109">Opret et navigationshierarki for kanal</span><span class="sxs-lookup"><span data-stu-id="27687-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="27687-110">Benyt følgende fremgangsmåde for at oprette et navigationshierarki for en kanal.</span><span class="sxs-lookup"><span data-stu-id="27687-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="27687-111">Gå til **Retail og Commerce \> Produkter og kategorier \> Kategori og produktstyring**.</span><span class="sxs-lookup"><span data-stu-id="27687-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="27687-112">Vælg **Kategorihierarkier**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="27687-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="27687-113">Giv hierarkiet et navn.</span><span class="sxs-lookup"><span data-stu-id="27687-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="27687-114">Den øverste kategori, du opretter, er rodnoden for kategorien.</span><span class="sxs-lookup"><span data-stu-id="27687-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="27687-115">Den vises ikke på webstedet.</span><span class="sxs-lookup"><span data-stu-id="27687-115">It won't be shown on your site.</span></span> <span data-ttu-id="27687-116">Hvis du vil oprette et kategorihierarki, hvor der vises en enkelt node på øverste niveau på webstedet, skal du oprette og navngive kategorien som underordnet i rodkategorien.</span><span class="sxs-lookup"><span data-stu-id="27687-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="27687-117">Vælg **Ny kategorinode**, og navngiv kategorien.</span><span class="sxs-lookup"><span data-stu-id="27687-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="27687-118">Fortsæt med at oprette sideordnede og underordnede kategorier efter behov.</span><span class="sxs-lookup"><span data-stu-id="27687-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="27687-119">Du kan nu tildele produkter til hver kategori, som du oprettede under kategorien på øverste niveau.</span><span class="sxs-lookup"><span data-stu-id="27687-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="27687-120">Tilpasse rækkefølgen af kategorier</span><span class="sxs-lookup"><span data-stu-id="27687-120">Customize the order of categories</span></span>

<span data-ttu-id="27687-121">De kategorier, du definerer, vises som standard i alfabetisk rækkefølge på dit websted.</span><span class="sxs-lookup"><span data-stu-id="27687-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="27687-122">Du kan dog også tilpasse visningsrækkefølgen for kategorier.</span><span class="sxs-lookup"><span data-stu-id="27687-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="27687-123">Tildele en kategorihierarkitype</span><span class="sxs-lookup"><span data-stu-id="27687-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="27687-124">Gå til **Retail og Commerce \> Produkter og kategorier \> Kategori og produktstyring**.</span><span class="sxs-lookup"><span data-stu-id="27687-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="27687-125">Vælg **Kategorihierarkier**.</span><span class="sxs-lookup"><span data-stu-id="27687-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="27687-126">Vælg **Tilknyt hierarkitype** i gruppen **Konfigurer** under fanen **Kategorihierarki** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="27687-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="27687-127">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="27687-127">Select **New**.</span></span>
1. <span data-ttu-id="27687-128">Vælg **Navigationshierarki for kanal** i feltet **Kategori for hierarkitype**.</span><span class="sxs-lookup"><span data-stu-id="27687-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="27687-129">I feltet **Kategorihierarki** skal du vælge det kanalnavigationshierarki, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="27687-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="27687-130">Publicere nye eller opdaterede navigationshierarkier</span><span class="sxs-lookup"><span data-stu-id="27687-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="27687-131">Udfør følgende trin for at gøre navigationshierarkiet tilgængeligt for din onlinestorefront.</span><span class="sxs-lookup"><span data-stu-id="27687-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="27687-132">Gå til **Retail og Commerce \> Konfiguration af kanal \> Kanalkategorier og produktattributter**.</span><span class="sxs-lookup"><span data-stu-id="27687-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="27687-133">Vælg din onlinebutik i træet til venstre.</span><span class="sxs-lookup"><span data-stu-id="27687-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="27687-134">Vælg **Publicer kanalopdateringer**.</span><span class="sxs-lookup"><span data-stu-id="27687-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="27687-135">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="27687-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="27687-136">Find og vælg **Job 1040** på listen.</span><span class="sxs-lookup"><span data-stu-id="27687-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="27687-137">Vælg **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="27687-137">Select **Run now**.</span></span>
1. <span data-ttu-id="27687-138">Gentag trin 5 og 6 for job 1070 og 1150.</span><span class="sxs-lookup"><span data-stu-id="27687-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="27687-139">Vise kategorier på dit websted</span><span class="sxs-lookup"><span data-stu-id="27687-139">Show categories on your site</span></span>

<span data-ttu-id="27687-140">Hvis du vil have vist din kategorihierarki i din onlinestorefront, skal du tilføje navigationsmenumodulet på den relevante placering i en skabelon eller et fragment.</span><span class="sxs-lookup"><span data-stu-id="27687-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="27687-141">Navigationsmenumodulet viser derefter dit navigationshierarki, hvis du har publiceret dit navigationshierarki til den kanal, som dit websted er bundet til.</span><span class="sxs-lookup"><span data-stu-id="27687-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="27687-142">Det navigationsmenumodul, der er inkluderet i modulbiblioteket, gør det kun muligt for brugere at navigere til kategorier, der ikke har underkategorier.</span><span class="sxs-lookup"><span data-stu-id="27687-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="27687-143">Hvis kunderne skal kunne navigere til kategorier, der har underkategorier, skal du tilpasse navigationsmenumodulet.</span><span class="sxs-lookup"><span data-stu-id="27687-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="27687-144">Tilføje brugerdefinerede navigationsindstillinger</span><span class="sxs-lookup"><span data-stu-id="27687-144">Add custom navigation options</span></span>

<span data-ttu-id="27687-145">I navigationsmenuen kan du tilføje navigationsindstillinger, der ikke er en del af dit produktkategorihierarki.</span><span class="sxs-lookup"><span data-stu-id="27687-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="27687-146">I slutningen af listen over produktkategorier kan du f.eks. tilføje et **Kontakt os**-element, der peger på en kontaktside, du har bygget til webstedet.</span><span class="sxs-lookup"><span data-stu-id="27687-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="27687-147">Hvis du vil føje brugerdefinerede navigationsindstillinger til navigationsmenuen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="27687-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="27687-148">Vælg navigationsmenumodulet i den skabelon eller det fragment, du vil tilpasse.</span><span class="sxs-lookup"><span data-stu-id="27687-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="27687-149">Vælg **Tilføj element** under fanen **Data** i egenskabsruden for at oprette et nyt (CMS)-navigationselement i indholdsstyringssystemet.</span><span class="sxs-lookup"><span data-stu-id="27687-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="27687-150">Indtast linktekst og en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="27687-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="27687-151">Gentag trin 2 og 3 for at tilføje flere brugerdefinerede navigationsindstillinger.</span><span class="sxs-lookup"><span data-stu-id="27687-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="27687-152">Når du er færdig, skal du vælge **Gem** for at gemme skabelonen eller fragmentet og derefter vælge **Afslut redigering** for at tjekke den ind.</span><span class="sxs-lookup"><span data-stu-id="27687-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27687-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="27687-153">Additional resources</span></span>

[<span data-ttu-id="27687-154">Oversigt over skabeloner og layout</span><span class="sxs-lookup"><span data-stu-id="27687-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="27687-155">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="27687-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="27687-156">Arbejde med forudindstillede layout</span><span class="sxs-lookup"><span data-stu-id="27687-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="27687-157">Arbejde med fragmenter</span><span class="sxs-lookup"><span data-stu-id="27687-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="27687-158">Arbejde med moduler</span><span class="sxs-lookup"><span data-stu-id="27687-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="27687-159">Oprette en side-URL</span><span class="sxs-lookup"><span data-stu-id="27687-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="27687-160">Arbejd med publiceringsgrupper</span><span class="sxs-lookup"><span data-stu-id="27687-160">Work with publish groups</span></span>](publish-groups.md)
