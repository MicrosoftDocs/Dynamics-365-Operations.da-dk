---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001129"
---
# <a name="footer-module"></a><span data-ttu-id="ac054-103">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="ac054-104">Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ac054-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ac054-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="ac054-105">Overview</span></span>

<span data-ttu-id="ac054-106">Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden.</span><span class="sxs-lookup"><span data-stu-id="ac054-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="ac054-107">Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="ac054-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="ac054-108">Egenskaber for sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-108">Footer module properties</span></span> 

<span data-ttu-id="ac054-109">Som de fleste containere understøtter et sidefodsmodul egenskaber for overskrift og bredde.</span><span class="sxs-lookup"><span data-stu-id="ac054-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="ac054-110">Det understøtter også tilføjelse af flere sidefodskategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="ac054-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="ac054-111">Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.</span><span class="sxs-lookup"><span data-stu-id="ac054-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="ac054-112">Moduler, der er tilgængelige i et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-112">Modules available in a footer module</span></span>

<span data-ttu-id="ac054-113">**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="ac054-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="ac054-114">Overskriften kan enten bruges alene eller sammen med et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="ac054-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="ac054-115">Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).</span><span class="sxs-lookup"><span data-stu-id="ac054-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="ac054-116">**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="ac054-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="ac054-117">Der skal angives en destination.</span><span class="sxs-lookup"><span data-stu-id="ac054-117">A destination is required.</span></span> <span data-ttu-id="ac054-118">Standarddestinationsværdien er #, som fører brugeren op til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="ac054-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="ac054-119">Oprette et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-119">Author a footer module</span></span>

1. <span data-ttu-id="ac054-120">Vælg **Fragmenter** i navigationsruden, og vælg derefter **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="ac054-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ac054-121">Vælg sidefodsmodulet i dialogboksen **Nyt sidefodsfragment**, angiv et navn til sidefragmentet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac054-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ac054-122">Vælg dispositionstræet til venstre, vælg ellipseknappen (**...**) for sidefodsmodulet, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="ac054-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ac054-123">I dialogboksen **Tilføj modul** skal du vælge sidefodskategorimodulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac054-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="ac054-124">Vælg dispositionstræet, vælg ellipseknappen for sidefodskategorien, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="ac054-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ac054-125">I dialogboksen **Tilføj modul** skal du vælge sidefodselementmodulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac054-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="ac054-126">Vælg sidefodselementmodulet i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="ac054-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="ac054-127">I egenskabsruden til højre skal du derefter konfigurere overskriften, linket og linkteksten og billedet, som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="ac054-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="ac054-128">Gentag trin 5 til 7 for at tilføje flere sidefodselementer.</span><span class="sxs-lookup"><span data-stu-id="ac054-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="ac054-129">Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipseknappen for sidefodskategorien og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="ac054-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ac054-130">I dialogboksen **Tilføj modul** skal du vælge Tilbage til toppen-modulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac054-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="ac054-131">Vælg Tilbage til toppen-modulet i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="ac054-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="ac054-132">Derefter skal du konfigurere Tilbage til toppen-modulet efter behov i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="ac054-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="ac054-133">Gem sidefragmentet, check det ind, og publicer det.</span><span class="sxs-lookup"><span data-stu-id="ac054-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="ac054-134">Udfør følgende trin på hver sideskabelon, der er oprettet til webstedet.</span><span class="sxs-lookup"><span data-stu-id="ac054-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="ac054-135">Tilføj det sidefodsfragment, du har oprettet, i sidefodsmodulet sidefod på **Hoved**-pladsen på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="ac054-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="ac054-136">Gem skabelonen, tjek den ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="ac054-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="ac054-137">Ved at føje sidefragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.</span><span class="sxs-lookup"><span data-stu-id="ac054-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac054-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ac054-138">Additional resources</span></span>

[<span data-ttu-id="ac054-139">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="ac054-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ac054-140">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="ac054-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ac054-141">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ac054-142">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ac054-143">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ac054-144">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ac054-145">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ac054-146">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="ac054-146">Footer module</span></span>](author-footer-module.md)
