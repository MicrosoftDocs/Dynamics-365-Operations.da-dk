---
title: Anvende visningsindstillinger for produktdimensioner
description: I dette emne beskrives visningsindstillingerne for produktdimensioner, og det beskrives, hvordan de anvendes i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117215"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="6943c-103">Anvende visningsindstillinger for produktdimensioner</span><span class="sxs-lookup"><span data-stu-id="6943c-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6943c-104">I dette emne beskrives visningsindstillingerne for produktdimensioner, og det beskrives, hvordan de anvendes i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6943c-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6943c-105">Dynamics 365 Commerce understøtter størrelses-, typografi- og farvedimensioner for at skelne mellem produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="6943c-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="6943c-106">Dimensioner vises typisk som tekstværdier, for eksempel "Lille", "Mellem" og "Stor" for størrelser og "Sort" og "Brun" for farver.</span><span class="sxs-lookup"><span data-stu-id="6943c-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="6943c-107">Men hvis et produkt understøtter mange variationer, kan det være vanskeligt at gennemse produktvarianter, da der skal foretages flere valg for at få vist billedet for de enkelte varianter.</span><span class="sxs-lookup"><span data-stu-id="6943c-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="6943c-108">For at gøre det nemmere at gennemse produktvarianter kan version 10.0.20 af Commerce bruge billeder og hexadecimale (hex) koder til at vise dimensioner som prøver.</span><span class="sxs-lookup"><span data-stu-id="6943c-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="6943c-109">I Commerce-webstedsgenerator er dimensionsindtillingerne defineret i **Indstillinger for websted \> Udvidelser \> Dimensionsindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="6943c-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="6943c-110">I følgende illustration vises et eksempel på dimensionsindstillinger i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="6943c-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Eksempel på webstedsindstillinger i Commerce-webstedsgenerator](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="6943c-112">Der er to tilgængelige dimensionsindstillinger:</span><span class="sxs-lookup"><span data-stu-id="6943c-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="6943c-113">**Dimensioner, der skal vises som billede** – Angiv, hvilke dimensioner der skal vises som prøver på e-handelswebstedssider, for eksempel sider med produktoplysninger (PDP'er) og sider med lister over søgeresultater.</span><span class="sxs-lookup"><span data-stu-id="6943c-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="6943c-114">Enhver kombination af farve-, størrelses- og typografidimensioner kan vises som en prøve.</span><span class="sxs-lookup"><span data-stu-id="6943c-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="6943c-115">Hvis der vælges en dimension til visning som en prøve, søger Commerce-modulgengivelse efter en tilgængelig konfiguration af en hexkodeprøve.</span><span class="sxs-lookup"><span data-stu-id="6943c-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="6943c-116">Hvis der ikke er konfigureret en hexkode, søger systemlogik efter en konfiguration af billedets URL-adresse til prøven.</span><span class="sxs-lookup"><span data-stu-id="6943c-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="6943c-117">Hvis der hverken er konfigureret en hexkode eller en URL-adresse til et billede, vises der tekst.</span><span class="sxs-lookup"><span data-stu-id="6943c-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="6943c-118">I følgende illustration vises et eksempel, hvor en PDP på et e-handelswebsted inkluderer farve- og størrelsesprøver.</span><span class="sxs-lookup"><span data-stu-id="6943c-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="6943c-119">I dette eksempel konfigureres en hexkode for farvedimensionen.</span><span class="sxs-lookup"><span data-stu-id="6943c-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="6943c-120">Derfor vises prøver som farver.</span><span class="sxs-lookup"><span data-stu-id="6943c-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="6943c-121">Der er dog hverken konfigureret en hexkode eller en URL-adresse til et billede til størrelsesdimensionen.</span><span class="sxs-lookup"><span data-stu-id="6943c-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="6943c-122">Derfor vises der tekst.</span><span class="sxs-lookup"><span data-stu-id="6943c-122">Therefore, text is shown.</span></span>

    ![Eksempel på den farvedimension, der vises som prøver på en side med oplysninger om e-handelsprodukter](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="6943c-124">**Dimensioner, der skal vises på produktkortet** – Angiv, hvilke dimensioner der skal vises på produktkort, der vises på lister og på listesider.</span><span class="sxs-lookup"><span data-stu-id="6943c-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="6943c-125">Før en dimension kan vises på et produktkort, skal denne indstilling aktiveres for den pågældende dimension.</span><span class="sxs-lookup"><span data-stu-id="6943c-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="6943c-126">Indstillingen **Dimensioner, der skal vises som billede** skal også aktiveres.</span><span class="sxs-lookup"><span data-stu-id="6943c-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="6943c-127">Funktionsmåden for valgt prøve på produktkort er optimeret til farvedimensionen.</span><span class="sxs-lookup"><span data-stu-id="6943c-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="6943c-128">I forbindelse med andre dimensioner kan det være nødvendigt med en visningsudvidelse for at tilpasse funktionsmåden for valgt prøve.</span><span class="sxs-lookup"><span data-stu-id="6943c-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="6943c-129">I følgende illustration vises et eksempel, hvor en listeside på et e-handelswebsted indeholder produktkort, der indeholder farveprøver.</span><span class="sxs-lookup"><span data-stu-id="6943c-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Eksempel på den farvedimension, der vises som prøver på en side med en e-handelsliste](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="6943c-131">Du kan finde oplysninger om, hvordan du konfigurerer produktdimensioner, så de vises som prøver på webstedssider, under [Konfigurere produktdimensionsværdier, der skal vises som prøver](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="6943c-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6943c-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6943c-132">Additional resources</span></span>

[<span data-ttu-id="6943c-133">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="6943c-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6943c-134">Modul til søgeresultater</span><span class="sxs-lookup"><span data-stu-id="6943c-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="6943c-135">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="6943c-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6943c-136">Konfigurere produktdimensionsværdier, der skal vises som prøver</span><span class="sxs-lookup"><span data-stu-id="6943c-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
