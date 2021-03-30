---
title: Sidefodsmodul
description: Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16c9ca145aff97f0af242da4cf662367f1f4ca3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211442"
---
# <a name="footer-module"></a><span data-ttu-id="5cbad-103">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="5cbad-104">Dette emne omhandler sidefodsmoduler og beskriver, hvordan du kan oprette dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5cbad-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5cbad-105">Sidefodsmodulet er en særlig container, der bruges som vært for de moduler, der vises i sidefoden.</span><span class="sxs-lookup"><span data-stu-id="5cbad-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="5cbad-106">Det kan f.eks. indeholde hyperlinks til forskellige sider på tværs af webstedet, som f.eks. siderne **Kontakt os** og **Butikspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="5cbad-107">Det følgende billede viser et eksempel på et sidefodsmodul på en webstedside.</span><span class="sxs-lookup"><span data-stu-id="5cbad-107">The following image shows an example of a footer module on a site page.</span></span>

![Eksempel på et sidefodsmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="5cbad-109">Egenskaber for sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-109">Footer module properties</span></span> 

<span data-ttu-id="5cbad-110">Som de fleste containere understøtter et sidefodsmodul egenskaber for overskriften og bredden.</span><span class="sxs-lookup"><span data-stu-id="5cbad-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="5cbad-111">Det understøtter også tilføjelse af flere sidefodskategorimoduler.</span><span class="sxs-lookup"><span data-stu-id="5cbad-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="5cbad-112">Hver af de sidefodskategorimodul, der tilføjes, gengives som en kolonne i sidefodsmodulet.</span><span class="sxs-lookup"><span data-stu-id="5cbad-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="5cbad-113">Moduler, der er tilgængelige i et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-113">Modules available in a footer module</span></span>

<span data-ttu-id="5cbad-114">**Sidefodselementer** – Et sidefodselementmodul kan indeholde en overskrift, et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="5cbad-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="5cbad-115">Overskriften kan enten bruges alene eller sammen med et billede og et link.</span><span class="sxs-lookup"><span data-stu-id="5cbad-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="5cbad-116">Alle links i sidefoden kan konfigureres, så de kun har tekst (f.eks. links som "Kontakt os" og "Beskyttelse af personlige oplysninger"), eller så det indeholder både tekst og et billede (f.eks. sociale medielinks).</span><span class="sxs-lookup"><span data-stu-id="5cbad-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="5cbad-117">**Tilbage til toppen** – Et tilbage til toppen-modul indeholder et link til hurtig navigation til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="5cbad-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="5cbad-118">Der skal angives en destination.</span><span class="sxs-lookup"><span data-stu-id="5cbad-118">A destination is required.</span></span> <span data-ttu-id="5cbad-119">Standarddestinationsværdien er \#, som fører brugeren op til toppen af siden.</span><span class="sxs-lookup"><span data-stu-id="5cbad-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="5cbad-120">Opret et sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-120">Create a footer module</span></span>

1. <span data-ttu-id="5cbad-121">Gå til **Fragmenter**, og vælg **Nyt** for at oprette et nyt fragment.</span><span class="sxs-lookup"><span data-stu-id="5cbad-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="5cbad-122">I dialogboksen **Nyt fragment** skal du vælge modulet **Container**, angive et navn for fragmentet og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="5cbad-123">På pladsen **Standardcontainer** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5cbad-124">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodskategori** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5cbad-125">På pladsen **Sidefodskategori** skal du vælge ellipsen (**...**) og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5cbad-126">I dialogboksen **Tilføj modul** skal du vælge modulet **Sidefodselement** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5cbad-127">Vælg pladsen **Sidefodselement**, og konfigurer overskriften, linket og linkteksten samt billede som påkrævet, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="5cbad-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="5cbad-128">Gentag hver gang trin 5-7 for at tilføje flere sidefodselementer.</span><span class="sxs-lookup"><span data-stu-id="5cbad-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="5cbad-129">Hvis du vil føje et "Tilbage til toppen"-link til din sidefod, skal du vælge ellipsen (**...**) på pladsen **Sidefodskategori** og derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="5cbad-130">I dialogboksen **Tilføj modul** skal du vælge modulet **Tilbage til toppen** og derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cbad-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5cbad-131">Vælg pladsen **Tilbage til toppen**, og konfigurer teksten og andre modulegenskaber som påkrævet, i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="5cbad-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="5cbad-132">Vælg **Afslut redigering** for at tjekke fragmentet ind, og vælg derefter **Publicer** for at publicere det.</span><span class="sxs-lookup"><span data-stu-id="5cbad-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5cbad-133">Du kan medvirke til at sikre, at der vises et sidehoved på hver side, ved at følge disse trin i hver sideskabelon, der oprettes for webstedet.</span><span class="sxs-lookup"><span data-stu-id="5cbad-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="5cbad-134">På pladsen **Sidefod** i modulet **Standardside** skal du tilføje det sidefodsfragment, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="5cbad-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="5cbad-135">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="5cbad-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5cbad-136">Ved at føje fragmentet til sideskabeloner kan du sikre, at sidefoden gengives på alle sider.</span><span class="sxs-lookup"><span data-stu-id="5cbad-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cbad-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5cbad-137">Additional resources</span></span>

[<span data-ttu-id="5cbad-138">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="5cbad-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5cbad-139">Container-modul</span><span class="sxs-lookup"><span data-stu-id="5cbad-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5cbad-140">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="5cbad-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5cbad-141">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5cbad-142">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5cbad-143">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5cbad-144">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5cbad-145">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="5cbad-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]