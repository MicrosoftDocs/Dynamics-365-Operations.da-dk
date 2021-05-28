---
title: Anvende indstillinger for måleenheder
description: Dette emne dækker indstillinger for måleenheder og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022368"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="91aea-103">Anvende indstillinger for måleenheder</span><span class="sxs-lookup"><span data-stu-id="91aea-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="91aea-104">Dette emne dækker indstillinger for måleenheder og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91aea-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="91aea-105">Et produkt kan sælges i forskellige enheder, f.eks. "stk.", "par" og "dusin".</span><span class="sxs-lookup"><span data-stu-id="91aea-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="91aea-106">I Commerce-hovedkvarteret kan måleenheden for salg defineres for et produkt og vises på en e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="91aea-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="91aea-107">Hvis en detailsælger f.eks. sælger et produkt både enkeltvis og i dusiner, kan de tilgængelige måleenheder vises sammen med andre produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="91aea-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="91aea-108">I eksemplet i følgende illustration er måleenheden for salg **stk.** (hver) konfigureret for et produkt i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="91aea-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Eksempel på et produkt, der er konfigureret med en måleenhed i Commerce-hovedkvarteret](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="91aea-110">Understøttelse af anvendelse og visning af måleenheden er tilgængelig fra og med Commerce version 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="91aea-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="91aea-111">Indstillinger for måleenheder</span><span class="sxs-lookup"><span data-stu-id="91aea-111">Unit of measure settings</span></span>

<span data-ttu-id="91aea-112">Visningsindstillinger for måleenheder er defineret i Commerce Site Builder under **Webstedsindstillinger \> Udvidelser \> Vis måleenhed for produkter**.</span><span class="sxs-lookup"><span data-stu-id="91aea-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="91aea-113">Der findes tre understøttede indstillinger:</span><span class="sxs-lookup"><span data-stu-id="91aea-113">There are three supported settings:</span></span>

- <span data-ttu-id="91aea-114">**Vis ikke** – Når denne indstilling er valgt, viser e-handelswebstedet ikke måleenheden for produktet.</span><span class="sxs-lookup"><span data-stu-id="91aea-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="91aea-115">Denne funktionsmåde er standard.</span><span class="sxs-lookup"><span data-stu-id="91aea-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="91aea-116">**Vis i købsoplevelsen for produkt** – Når denne indstilling er valgt, vises måleenheden i produktoplysninger, indkøbsvogn, betaling, ordrehistorik og ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="91aea-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="91aea-117">**Vis i gennemsyn af produkter og købsoplevelse** – Når denne indstilling er valgt, vises måleenheden på siderne med købsoplevelsen for produktet og når produkter gennemses.</span><span class="sxs-lookup"><span data-stu-id="91aea-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="91aea-118">Som en del af denne funktionsmåde vises måleenheder i søgeresultater og moduler til produktsamling.</span><span class="sxs-lookup"><span data-stu-id="91aea-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91aea-119">Visningsindstillinger for måleenhed er tilgængelige med frigivelsen af Commerce version 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="91aea-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="91aea-120">Hvis du opdaterer fra en ældre version af Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="91aea-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="91aea-121">Du kan finde instruktioner i [Opdateringer af SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="91aea-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="91aea-122">Moduler, der bruger indstillinger for måleenhed</span><span class="sxs-lookup"><span data-stu-id="91aea-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="91aea-123">Moduler, der bruger indstillingerne for måleenhed, omfatter modulerne for købsfelt, ønskeliste, indkøbsvogn, indkøbsvogn, container med søgeresultater, produktsamling, betaling og ordredetaljer.</span><span class="sxs-lookup"><span data-stu-id="91aea-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="91aea-124">I eksemplet i følgende illustration viser en PDP (Product Details Page) måleenheden (**stk.**) for et produkt.</span><span class="sxs-lookup"><span data-stu-id="91aea-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Eksempel på en PDP, der viser måleenheden](./media/Productunit-PDP.png)

<span data-ttu-id="91aea-126">I eksemplet i følgende illustration viser et produktsamlingsmodeul måleenheden (**stk.**) for et produkt.</span><span class="sxs-lookup"><span data-stu-id="91aea-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Eksempel på et produktsamlingsmodul, der viser måleenheden](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="91aea-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="91aea-128">Additional resources</span></span>

[<span data-ttu-id="91aea-129">Modulbibliotek, oversigt</span><span class="sxs-lookup"><span data-stu-id="91aea-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="91aea-130">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="91aea-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="91aea-131">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="91aea-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="91aea-132">Kontostyringssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="91aea-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="91aea-133">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="91aea-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
