---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6e7b0ad4fe0723575a0ec55a9b02d110568db58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797227"
---
# <a name="footer-module"></a><span data-ttu-id="27db3-103">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="27db3-104">Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27db3-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="27db3-105">Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden.</span><span class="sxs-lookup"><span data-stu-id="27db3-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="27db3-106">Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="27db3-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="27db3-107">Det følgende billede viser et eksempel på et sidefodsmodul på en webstedside.</span><span class="sxs-lookup"><span data-stu-id="27db3-107">The following image shows an example of a footer module on a site page.</span></span>

![Eksempel på et sidefodsmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties&quot;></a><span data-ttu-id=&quot;27db3-109&quot;>Egenskaber for sidefodsmodul</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-109&quot;>Footer module properties</span></span> 

<span data-ttu-id=&quot;27db3-110&quot;>Som de fleste containere understøtter et sidefodsmodul egenskaber for overskriften og bredden.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-110&quot;>Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id=&quot;27db3-111&quot;>Det understøtter også tilføjelse af flere sidefodskategorimoduler.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-111&quot;>It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id=&quot;27db3-112&quot;>Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-112&quot;>Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name=&quot;modules-available-in-a-footer-module&quot;></a><span data-ttu-id=&quot;27db3-113&quot;>Moduler, der er tilgængelige i et sidefodsmodul</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-113&quot;>Modules available in a footer module</span></span>

<span data-ttu-id=&quot;27db3-114&quot;>**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-114&quot;>**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id=&quot;27db3-115&quot;>Overskriften kan enten bruges alene eller sammen med et billede og et link.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;27db3-115&quot;>The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id=&quot;27db3-116&quot;>Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som &quot;Kontakt os&quot; og &quot;Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).</span><span class="sxs-lookup"><span data-stu-id="27db3-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="27db3-117">**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="27db3-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="27db3-118">Der skal angives en destination.</span><span class="sxs-lookup"><span data-stu-id="27db3-118">A destination is required.</span></span> <span data-ttu-id="27db3-119">Standarddestinationsværdien er \#, som fører brugeren op til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="27db3-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="27db3-120">Opret et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-120">Create a footer module</span></span>

1. <span data-ttu-id="27db3-121">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="27db3-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="27db3-122">I dialogboksen **Nyt fragment** skal du vælge modulet **Container**, angive et navn for fragmentet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="27db3-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="27db3-123">På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="27db3-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="27db3-124">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodskategori** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="27db3-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="27db3-125">På pladsen **Sidefodskategori** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="27db3-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="27db3-126">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodselement** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="27db3-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="27db3-127">Vælg pladsen **Sidefodselement**, og konfigurer overskriften, linket og linkteksten samt billede som påkrævet, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="27db3-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="27db3-128">Gentag hver gang trin 5-7 for at tilføje flere sidefodselementer.</span><span class="sxs-lookup"><span data-stu-id="27db3-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="27db3-129">Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipsen (**...**) på pladsen **Sidefodskategori** og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="27db3-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="27db3-130">I dialogboksen **Tilføj modul** skal du vælge modulet **Tilbage til toppen** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="27db3-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="27db3-131">Vælg pladsen **Tilbage til toppen**, og konfigurer teksten og andre modulegenskaber som påkrævet, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="27db3-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="27db3-132">Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="27db3-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="27db3-133">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="27db3-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="27db3-134">På pladsen **Sidefod** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="27db3-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="27db3-135">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="27db3-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="27db3-136">Ved at føje fragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.</span><span class="sxs-lookup"><span data-stu-id="27db3-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27db3-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="27db3-137">Additional resources</span></span>

[<span data-ttu-id="27db3-138">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="27db3-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="27db3-139">Container-modul</span><span class="sxs-lookup"><span data-stu-id="27db3-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="27db3-140">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="27db3-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="27db3-141">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="27db3-142">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="27db3-143">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="27db3-144">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="27db3-145">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="27db3-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]