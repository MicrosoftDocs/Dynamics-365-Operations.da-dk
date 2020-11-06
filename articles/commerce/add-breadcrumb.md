---
title: Brødkrummemodul
description: Dette emne omhandler brødkrummemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 05e8614f53db2593ade92fdb42dc0dfe869e9407
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055398"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="46c36-103">Brødkrummemodul</span><span class="sxs-lookup"><span data-stu-id="46c36-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46c36-104">Dette emne omhandler brødkrummemoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="46c36-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="46c36-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="46c36-105">Overview</span></span>

<span data-ttu-id="46c36-106">Brødkrummemoduler bruges til at tillade sekundær navigation på webstedssider.</span><span class="sxs-lookup"><span data-stu-id="46c36-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="46c36-107">De vises normalt øverst på en side under overskriften.</span><span class="sxs-lookup"><span data-stu-id="46c36-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="46c36-108">Selvom der kan føjes brødkrummemoduler til en hvilken som helst side, bruges de oftest på sider med produktoplysninger (PDP'er) til visning af produktkategorihierarkiet og er en hurtig måde at bevæge dig rundt på et websted på.</span><span class="sxs-lookup"><span data-stu-id="46c36-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="46c36-109">Et brødkrummemodul kan også bruges til at vise et "Tilbage til resultater"-link, når brugerne åbner en PDP fra en søge- eller listeside.</span><span class="sxs-lookup"><span data-stu-id="46c36-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="46c36-110">På denne måde kan brugerne hurtigt vende tilbage til deres filtrerede listeside for at fortsætte med at handle.</span><span class="sxs-lookup"><span data-stu-id="46c36-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="46c36-111">På sider med produktkategorikontekst, f.eks. PDP'er og kategorisider, viser brødkrummemoduler kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="46c36-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="46c36-112">På sider, der ikke har kategorikontekst, viser brødkrummemoduler som standard **&lt;Webstedsrod&gt; / &lt;Aktuel side&gt;**.</span><span class="sxs-lookup"><span data-stu-id="46c36-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="46c36-113">Brødkrummemoduler kan også konfigureres manuelt på andre typer webstedssider, så der vises links til bestemte sider på webstedet.</span><span class="sxs-lookup"><span data-stu-id="46c36-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="46c36-114">Brødkrummemodulet er tilgængeligt i Dynamics 365 Commerce version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="46c36-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="46c36-115">Det følgende billede viser et eksempel på et brødkrummemodul, der viser kategorihierarkiet på en PDP.</span><span class="sxs-lookup"><span data-stu-id="46c36-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Eksempel på et brødkrummemodul](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="46c36-117">Indstillinger for brødkrummemodul</span><span class="sxs-lookup"><span data-stu-id="46c36-117">Breadcrumb module settings</span></span>

<span data-ttu-id="46c36-118">Brødkrummemodulet er afhængigt af indstillingen **Visningstype for brødkrumme på PDP** , som defineres i **Webstedsindstillinger \>Udvidelser** i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="46c36-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="46c36-119">Denne indstilling har tre mulige værdier:</span><span class="sxs-lookup"><span data-stu-id="46c36-119">This setting has three possible values:</span></span>

- <span data-ttu-id="46c36-120">**Vis kategorihierarki** – Når denne værdi er valgt, vil brødkrummemodulet vise hele kategorihierarkiet for det produkt, der ses på PDP'en.</span><span class="sxs-lookup"><span data-stu-id="46c36-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="46c36-121">**Vis tilbage til resultater** – Når denne værdi er valgt, vil brødkrummemodulet vise linket "Tilbage til resultater" på en PDP, hvis brugeren åbnede PDP'en fra et modul, der tillader linket "Tilbage til resultater".</span><span class="sxs-lookup"><span data-stu-id="46c36-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="46c36-122">Denne funktionalitet er tilgængelig, når brugere navigerer fra listesider for kategorier, søgninger, lister og anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="46c36-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="46c36-123">For at understøtte denne funktion har moduler med produktsamlinger og søgeresultater en egenskab, der har fået navnet **Tillad tilbage til resultater på PDP**.</span><span class="sxs-lookup"><span data-stu-id="46c36-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="46c36-124">Denne egenskab giver dig fleksibiliteten til at definere, hvilke moduler der skal understøtte linkfunktionen "Tilbage til resultater" på PDP'en.</span><span class="sxs-lookup"><span data-stu-id="46c36-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="46c36-125">Hvis f.eks. **Vis tilbage til resultater** er valgt for indstillingen **Visningstype for brødkrumme på PDP** for brødkrummemodulet, og **Tillad tilbage til resultater på PDP** er valgt for søgesidens modul for søgeresultater, vises linket "Tilbage til resultater", når brugere går fra søgesiden til en PDP.</span><span class="sxs-lookup"><span data-stu-id="46c36-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="46c36-126">**Vis kategorihierarki og tilbage til resultater** – Denne værdi er en kombination af de to foregående.</span><span class="sxs-lookup"><span data-stu-id="46c36-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="46c36-127">Når denne værdi er valgt, viser brødkrummemodulet både det fulde kategorihierarki og linket "Tilbage til resultater" (hvis det er konfigureret) på en PDP.</span><span class="sxs-lookup"><span data-stu-id="46c36-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46c36-128">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="46c36-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="46c36-129">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="46c36-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="46c36-130">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="46c36-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="46c36-131">Egenskaber for brødkrummemodul</span><span class="sxs-lookup"><span data-stu-id="46c36-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="46c36-132">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="46c36-132">Property name</span></span> | <span data-ttu-id="46c36-133">Værdier</span><span class="sxs-lookup"><span data-stu-id="46c36-133">Values</span></span> | <span data-ttu-id="46c36-134">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="46c36-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="46c36-135">Rod</span><span class="sxs-lookup"><span data-stu-id="46c36-135">Root</span></span> | <span data-ttu-id="46c36-136">Tekst eller link</span><span class="sxs-lookup"><span data-stu-id="46c36-136">Text or link</span></span>| <span data-ttu-id="46c36-137">Denne valgfrie egenskab angiver linktekst og en linkdestination for brødkrummens webstedsrod.</span><span class="sxs-lookup"><span data-stu-id="46c36-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="46c36-138">Hvis denne egenskab ikke er konfigureret, vil der ikke blive defineret en rod.</span><span class="sxs-lookup"><span data-stu-id="46c36-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="46c36-139">Link til brødkrumme</span><span class="sxs-lookup"><span data-stu-id="46c36-139">Breadcrumb link</span></span> | <span data-ttu-id="46c36-140">Binding</span><span class="sxs-lookup"><span data-stu-id="46c36-140">Link</span></span> | <span data-ttu-id="46c36-141">Denne valgfrie egenskab angiver links til en manuelt konfigureret brødkrumme, hvis disse links er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="46c36-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="46c36-142">Links vises i den rækkefølge, de er angivet i.</span><span class="sxs-lookup"><span data-stu-id="46c36-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="46c36-143">Føje et brødkrummemodul til en ny side</span><span class="sxs-lookup"><span data-stu-id="46c36-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="46c36-144">Hvis du vil føje et brødkrummemodul til en PDP og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="46c36-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="46c36-145">Gå til **Indstillinger for websted /> Udvidelser** og derefter til **Visningstype for brødkrumme på PDP** , vælg **Vis kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="46c36-145">Go to **Site Settings /> Extensions** , and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="46c36-146">Gå til **Skabeloner** , og vælg PDP-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="46c36-146">Go to **Templates** , and select the PDP template.</span></span>
1. <span data-ttu-id="46c36-147">På pladsen **Container** , der indeholder købefeltmodulet, skal du vælge ellipsen ( **...** ) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="46c36-147">In the **Container** slot that contains the buy box module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="46c36-148">I dialogboksen **Tilføj modul** skal du vælge modulet **Brødkrumme** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="46c36-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="46c36-149">Vælg **Gem** , vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="46c36-149">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="46c36-150">Gå til **Sider** , og åbn en PDP, der bruger PDP-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="46c36-150">Go to **Pages** , and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="46c36-151">Hvis der endnu ikke findes en PDP, skal du oprette en.</span><span class="sxs-lookup"><span data-stu-id="46c36-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="46c36-152">På pladsen **Container** , der indeholder købefeltmodulet, skal du vælge ellipsen ( **...** ) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="46c36-152">In the **Container** slot that contains the buy box module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="46c36-153">I dialogboksen **Tilføj modul** skal du vælge modulet **Brødkrumme** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="46c36-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="46c36-154">I egenskabsruden for pladsen **Brødkrumme** skal du under **Rod** vælge **Linktekst**.</span><span class="sxs-lookup"><span data-stu-id="46c36-154">In the properties pane of the **Breadcrumb** slot, under **Root** , select **Link text**.</span></span>
1. <span data-ttu-id="46c36-155">I dialogboksen **Linktekst** skal du skrive **Start** og derefter under **Linkdestination** vælge **Tilføj et link**.</span><span class="sxs-lookup"><span data-stu-id="46c36-155">In the **Link text** dialog box, enter **Home** , and then, under **Link target** , select **Add a link**.</span></span>
1. <span data-ttu-id="46c36-156">I dialogboksen **Tilføj et link** skal du vælge et link for brødkrummeroden og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="46c36-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="46c36-157">Vælg **Gem** , og vælg derefter **Vis** for at få vist siden.</span><span class="sxs-lookup"><span data-stu-id="46c36-157">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="46c36-158">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="46c36-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46c36-159">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="46c36-159">Additional resources</span></span>

[<span data-ttu-id="46c36-160">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="46c36-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="46c36-161">Navigationsmenumodul</span><span class="sxs-lookup"><span data-stu-id="46c36-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="46c36-162">Webstedsvælgermodul</span><span class="sxs-lookup"><span data-stu-id="46c36-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="46c36-163">Oversigt over standardlandingsside for kategori og side for søgeresultater</span><span class="sxs-lookup"><span data-stu-id="46c36-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="46c36-164">Produktsamlingsmoduler</span><span class="sxs-lookup"><span data-stu-id="46c36-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="46c36-165">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="46c36-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="46c36-166">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="46c36-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
