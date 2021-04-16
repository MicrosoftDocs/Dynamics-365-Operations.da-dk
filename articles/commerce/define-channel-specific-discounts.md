---
title: Definere kanalspecifikke rabatter
description: Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler. Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal.
author: scott-tucker
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c4003bd78e400994f3c164d2f7e8e3aa5ce93146
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802063"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="e924f-104">Definere kanalspecifikke rabatter</span><span class="sxs-lookup"><span data-stu-id="e924f-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e924f-105">Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="e924f-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="e924f-106">Kanalspecifikke rabatter</span><span class="sxs-lookup"><span data-stu-id="e924f-106">Channel-specific discounts</span></span>

<span data-ttu-id="e924f-107">Detailhandlere tilbyder ofte forskellige rabatter i forskellige kanaler.</span><span class="sxs-lookup"><span data-stu-id="e924f-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="e924f-108">Dette er sker muligvis for at adressere de lokale markedsbetingelser eller for at imødegå konkurrerende detailhandlere.</span><span class="sxs-lookup"><span data-stu-id="e924f-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="e924f-109">Commerce bruger prisgrupper til at definere kanalspecifikke rabatter.</span><span class="sxs-lookup"><span data-stu-id="e924f-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="e924f-110">Prisgrupper kan tildeles til en eller flere af følgende enheder: kanaler, kataloger, tilhørsforhold og fordelskundeprogrammer.</span><span class="sxs-lookup"><span data-stu-id="e924f-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="e924f-111">I denne artikel beskrives kanaler, men de samme begreber gælder for katalograbatter, tilhørsforhold med rabatter og fordelskunderabatter.</span><span class="sxs-lookup"><span data-stu-id="e924f-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="e924f-112">Prisgrupper</span><span class="sxs-lookup"><span data-stu-id="e924f-112">Price groups</span></span>

<span data-ttu-id="e924f-113">[![Prisgrupper](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="e924f-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="e924f-114">Ovenstående diagram viser forholdet mellem enheder, der kan være på en transaktion (kanal, katalog, tilhørsforhold, debitor, fordelskundekort), og de forskellige rabattyper, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="e924f-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="e924f-115">Alle transaktionerne finder sted i en kanal, så kanalen vil garanteret være til stede i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="e924f-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="e924f-116">De resterende enheder er valgfri.</span><span class="sxs-lookup"><span data-stu-id="e924f-116">The remaining entities are optional.</span></span> <span data-ttu-id="e924f-117">På de enkelte masterdatasider er der et link til en relateret prisgruppeside, hvor du kan få vist og tilføje prisgrupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="e924f-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="e924f-118">En prisgruppe anvendes til at relatere fire forskellige typer enheder til rabatter, prisjusteringer og samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="e924f-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="e924f-119">Vi anbefaler, at du planlægger en strategi for, hvordan du navngiver dine prisgrupper for at holde dem organiseret.</span><span class="sxs-lookup"><span data-stu-id="e924f-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="e924f-120">En mulighed ville være at bruge et bogstav eller talpræfiks eller -suffiks til at skelne mellem de forskellige typer.</span><span class="sxs-lookup"><span data-stu-id="e924f-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="e924f-121">For eksempel 1-xxxxx for kanalprisgrupper og 2-xxxxx for katalogprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="e924f-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="e924f-122">Der er fire undersøgelsessider med fokus på hver af de handelsenheder, der kan have rabatter tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="e924f-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="e924f-123">**Kanalsprisgrupper** – Denne side viser en liste over kanaler og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e924f-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="e924f-124">**Katalogprisgrupper** – Denne side viser en liste over kataloger og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e924f-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="e924f-125">**Prisgrupper for fordelskunder** – Denne side viser en liste over fordelskundeprogrammer og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e924f-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="e924f-126">**Prisgrupper for tilhørsforhold** – Denne side viser en liste over tilhørsforhold og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="e924f-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="e924f-127">Rabatopsætning for eksempelkanal</span><span class="sxs-lookup"><span data-stu-id="e924f-127">Example channel discount set up</span></span>

<span data-ttu-id="e924f-128">Følgende eksempel illustrerer de opgaver, der er involveret i oprettelse af en kanalrabat.</span><span class="sxs-lookup"><span data-stu-id="e924f-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="e924f-129">I dette eksempel har du en kanal kaldet **Horsens**, og du vil oprette en ny rabat, kaldet **I skole igen**.</span><span class="sxs-lookup"><span data-stu-id="e924f-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="e924f-130">Da strategien for prissætning og rabat indeholder muligheden for kanalrabatter, opretter du altid en kanalspecifikke prisgruppe, når du opretter en kanal.</span><span class="sxs-lookup"><span data-stu-id="e924f-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="e924f-131">Du har prisgruppen **Horsens-PG**, og den er tildelt til kanalen **Horsens**.</span><span class="sxs-lookup"><span data-stu-id="e924f-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="e924f-132">Når du har oprettet den nye **I skole igen**-rabat, skal du klikke på **Prisgrupper** øverst på **Rabat** siden.</span><span class="sxs-lookup"><span data-stu-id="e924f-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="e924f-133">Siden **Detailprisgrupper** åbnes.</span><span class="sxs-lookup"><span data-stu-id="e924f-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="e924f-134">Klik derefter på **ny** , og vælg prisgruppen **Horsens-PG**.</span><span class="sxs-lookup"><span data-stu-id="e924f-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="e924f-135">Du kan nu aktivere rabatten og sende den til kanalen.</span><span class="sxs-lookup"><span data-stu-id="e924f-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e924f-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e924f-136">Additional resources</span></span>

[<span data-ttu-id="e924f-137">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="e924f-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]