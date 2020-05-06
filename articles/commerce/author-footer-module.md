---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269626"
---
# <a name="footer-module"></a><span data-ttu-id="f47e4-103">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="f47e4-104">Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f47e4-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f47e4-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="f47e4-105">Overview</span></span>

<span data-ttu-id="f47e4-106">Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden.</span><span class="sxs-lookup"><span data-stu-id="f47e4-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="f47e4-107">Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="f47e4-108">Egenskaber for sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-108">Footer module properties</span></span> 

<span data-ttu-id="f47e4-109">Som de fleste containere understøtter et sidefodsmodul egenskaber for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="f47e4-109">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="f47e4-110">Det understøtter også tilføjelse af flere sidefodskategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="f47e4-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="f47e4-111">Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.</span><span class="sxs-lookup"><span data-stu-id="f47e4-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="f47e4-112">Moduler, der er tilgængelige i et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-112">Modules available in a footer module</span></span>

<span data-ttu-id="f47e4-113">**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="f47e4-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="f47e4-114">Overskriften kan enten bruges alene eller sammen med et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="f47e4-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="f47e4-115">Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).</span><span class="sxs-lookup"><span data-stu-id="f47e4-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="f47e4-116">**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="f47e4-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="f47e4-117">Der skal angives en destination.</span><span class="sxs-lookup"><span data-stu-id="f47e4-117">A destination is required.</span></span> <span data-ttu-id="f47e4-118">Standarddestinationsværdien er #, som fører brugeren op til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="f47e4-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="f47e4-119">Oprette et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-119">Author a footer module</span></span>

1. <span data-ttu-id="f47e4-120">Vælg **Fragmenter** i navigationsruden, og vælg derefter **Nyt sidefragment**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="f47e4-121">Vælg sidefodsmodulet i dialogboksen **Nyt sidefodsfragment**, angiv et navn til sidefragmentet, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f47e4-122">Vælg dispositionstræet til venstre, vælg ellipseknappen (**...**) for sidefodsmodulet, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f47e4-123">I dialogboksen **Tilføj modul** skal du vælge sidefodskategorimodulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="f47e4-124">Vælg dispositionstræet, vælg ellipseknappen for sidefodskategorien, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f47e4-125">I dialogboksen **Tilføj modul** skal du vælge sidefodselementmodulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="f47e4-126">Vælg sidefodselementmodulet i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="f47e4-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="f47e4-127">I egenskabsruden til højre skal du derefter konfigurere overskriften, linket og linkteksten og billedet, som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="f47e4-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="f47e4-128">Gentag trin 5 til 7 for at tilføje flere sidefodselementer.</span><span class="sxs-lookup"><span data-stu-id="f47e4-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="f47e4-129">Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipseknappen for sidefodskategorien og derefter vælge **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f47e4-130">I dialogboksen **Tilføj modul** skal du vælge Tilbage til toppen-modulet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f47e4-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="f47e4-131">Vælg Tilbage til toppen-modulet i dispositionstræet.</span><span class="sxs-lookup"><span data-stu-id="f47e4-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="f47e4-132">Derefter skal du konfigurere Tilbage til toppen-modulet efter behov i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="f47e4-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="f47e4-133">Vælg **Gem**, vælg **Afslut redigering** for at tjekke sidefragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="f47e4-133">Select **Save**, select **Finish editing** to check in the page fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f47e4-134">Udfør følgende trin på hver sideskabelon, der er oprettet til webstedet.</span><span class="sxs-lookup"><span data-stu-id="f47e4-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="f47e4-135">Tilføj det sidefodsfragment, du har oprettet, i sidefodsmodulet sidefod på **Hoved**-pladsen på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="f47e4-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f47e4-136">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="f47e4-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f47e4-137">Ved at føje sidefragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.</span><span class="sxs-lookup"><span data-stu-id="f47e4-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f47e4-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f47e4-138">Additional resources</span></span>

[<span data-ttu-id="f47e4-139">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="f47e4-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f47e4-140">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="f47e4-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f47e4-141">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f47e4-142">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f47e4-143">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f47e4-144">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f47e4-145">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f47e4-146">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="f47e4-146">Footer module</span></span>](author-footer-module.md)
