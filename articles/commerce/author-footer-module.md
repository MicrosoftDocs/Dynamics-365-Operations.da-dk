---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411191"
---
# <a name="footer-module"></a><span data-ttu-id="382dc-103">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="382dc-104">Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="382dc-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="382dc-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="382dc-105">Overview</span></span>

<span data-ttu-id="382dc-106">Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden.</span><span class="sxs-lookup"><span data-stu-id="382dc-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="382dc-107">Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="382dc-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="382dc-108">Det følgende billede viser et eksempel på et sidefodsmodul på en webstedside.</span><span class="sxs-lookup"><span data-stu-id="382dc-108">The following image shows an example of a footer module on a site page.</span></span>

![Eksempel på et sidefodsmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="382dc-110">Egenskaber for sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-110">Footer module properties</span></span> 

<span data-ttu-id="382dc-111">Som de fleste containere understøtter et sidefodsmodul egenskaber for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="382dc-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="382dc-112">Det understøtter også tilføjelse af flere sidefodskategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="382dc-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="382dc-113">Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.</span><span class="sxs-lookup"><span data-stu-id="382dc-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="382dc-114">Moduler, der er tilgængelige i et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-114">Modules available in a footer module</span></span>

<span data-ttu-id="382dc-115">**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="382dc-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="382dc-116">Overskriften kan enten bruges alene eller sammen med et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="382dc-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="382dc-117">Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).</span><span class="sxs-lookup"><span data-stu-id="382dc-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="382dc-118">**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="382dc-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="382dc-119">Der skal angives en destination.</span><span class="sxs-lookup"><span data-stu-id="382dc-119">A destination is required.</span></span> <span data-ttu-id="382dc-120">Standarddestinationsværdien er \#, som fører brugeren op til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="382dc-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="382dc-121">Opret et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-121">Create a footer module</span></span>

1. <span data-ttu-id="382dc-122">Gå til **Sidefragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="382dc-122">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="382dc-123">I dialogboksen **Nyt sidefragment** skal du vælge modulet **Container**, angive et navn for sidefragmentet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="382dc-123">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="382dc-124">På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="382dc-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="382dc-125">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodskategori** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="382dc-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="382dc-126">På pladsen **Sidefodskategori** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="382dc-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="382dc-127">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodselement** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="382dc-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="382dc-128">Vælg pladsen **Sidefodselement**, og konfigurer overskriften, linket og linkteksten samt billede som påkrævet, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="382dc-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="382dc-129">Gentag hver gang trin 5-7 for at tilføje flere sidefodselementer.</span><span class="sxs-lookup"><span data-stu-id="382dc-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="382dc-130">Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipsen (**...**) på pladsen **Sidefodskategori** og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="382dc-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="382dc-131">I dialogboksen **Tilføj modul** skal du vælge modulet **Tilbage til toppen** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="382dc-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="382dc-132">Vælg pladsen **Tilbage til toppen**, og konfigurer teksten og andre modulegenskaber som påkrævet, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="382dc-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="382dc-133">Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="382dc-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="382dc-134">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="382dc-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="382dc-135">På pladsen **Sidefod** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="382dc-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="382dc-136">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="382dc-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="382dc-137">Ved at føje sidefragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.</span><span class="sxs-lookup"><span data-stu-id="382dc-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="382dc-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="382dc-138">Additional resources</span></span>

[<span data-ttu-id="382dc-139">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="382dc-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="382dc-140">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="382dc-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="382dc-141">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="382dc-142">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="382dc-143">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="382dc-144">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="382dc-145">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="382dc-146">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="382dc-146">Footer module</span></span>](author-footer-module.md)
