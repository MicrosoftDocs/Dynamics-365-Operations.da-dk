---
title: Definere kanalspecifikke rabatter
description: "Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler. Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 34039b298e8994e50a7c06ef034698e8c1264389
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="define-channel-specific-discounts"></a><span data-ttu-id="bcc77-104">Definere kanalspecifikke rabatter</span><span class="sxs-lookup"><span data-stu-id="bcc77-104">Define channel-specific discounts</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="bcc77-105">Detailhandlere angiver ofte forskellige rabatter i forskellige kanaler.</span><span class="sxs-lookup"><span data-stu-id="bcc77-105">Retailers often set different discounts in different channels.</span></span> <span data-ttu-id="bcc77-106">Dette emne gennemgår de begreber, du skal kende for at oprette en rabat til en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="bcc77-106">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span> 

<a name="channel-specific-discounts"></a><span data-ttu-id="bcc77-107">Kanalspecifikke rabatter</span><span class="sxs-lookup"><span data-stu-id="bcc77-107">Channel-specific discounts</span></span>
--------------------------

<span data-ttu-id="bcc77-108">Detailhandlere tilbyder ofte forskellige rabatter i forskellige kanaler.</span><span class="sxs-lookup"><span data-stu-id="bcc77-108">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="bcc77-109">Dette er sker muligvis for at adressere de lokale markedsbetingelser eller for at imødegå konkurrerende detailhandlere.</span><span class="sxs-lookup"><span data-stu-id="bcc77-109">This is may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="bcc77-110">Microsoft Dynamics 365 for Retail bruger prisgrupper til at definere kanalspecifikke rabatter.</span><span class="sxs-lookup"><span data-stu-id="bcc77-110">Microsoft Dynamics 365 for Retail uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="bcc77-111">Prisgrupper kan tildeles til en eller flere af følgende enheder: kanaler, kataloger, tilhørsforhold og fordelskundeprogrammer.</span><span class="sxs-lookup"><span data-stu-id="bcc77-111">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="bcc77-112">I denne artikel beskrives kanaler, men de samme begreber gælder for katalograbatter, tilhørsforhold med rabatter og fordelskunderabatter.</span><span class="sxs-lookup"><span data-stu-id="bcc77-112">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="bcc77-113">Prisgrupper</span><span class="sxs-lookup"><span data-stu-id="bcc77-113">Price groups</span></span>

<span data-ttu-id="bcc77-114">[![Prisgrupper](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="bcc77-114">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="bcc77-115">Ovenstående diagram viser forholdet mellem enheder, der kan være på en transaktion (kanal, katalog, tilhørsforhold, debitor, fordelskundekort), og de forskellige rabattyper, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="bcc77-115">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="bcc77-116">Alle transaktionerne finder sted i en kanal, så kanalen vil garanteret være til stede i en transaktion.</span><span class="sxs-lookup"><span data-stu-id="bcc77-116">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="bcc77-117">De resterende enheder er valgfri.</span><span class="sxs-lookup"><span data-stu-id="bcc77-117">The remaining entities are optional.</span></span> <span data-ttu-id="bcc77-118">På de enkelte masterdatasider er der et link til en relateret prisgruppeside, hvor du kan få vist og tilføje prisgrupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="bcc77-118">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="bcc77-119">En prisgruppe anvendes til at relatere fire forskellige typer enheder til rabatter, prisjusteringer og samhandelsaftaler.</span><span class="sxs-lookup"><span data-stu-id="bcc77-119">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="bcc77-120">Vi anbefaler, at du planlægger en strategi for, hvordan du navngiver dine prisgrupper for at holde dem organiseret.</span><span class="sxs-lookup"><span data-stu-id="bcc77-120">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="bcc77-121">En mulighed ville være at bruge et bogstav eller talpræfiks eller -suffiks til at skelne mellem de forskellige typer.</span><span class="sxs-lookup"><span data-stu-id="bcc77-121">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="bcc77-122">For eksempel 1-xxxxx for kanalprisgrupper og 2-xxxxx for katalogprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="bcc77-122">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="bcc77-123">Der er fire undersøgelsessider med fokus på hver af de detailenheder, der kan have rabatter tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="bcc77-123">There are four inquiry pages that focus on each of the retail entities that can have discounts associated to them.</span></span>

-   <span data-ttu-id="bcc77-124">**Detailkanalsprisgrupper**–Denne side viser en liste over kanaler og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc77-124">**Retail channel price groups** - This page shows a list of channels and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="bcc77-125">**Katalogprisgrupper**–Denne side viser en liste over kataloger og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc77-125">**Catalog price groups** - This page shows a list of catalogs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="bcc77-126">**Prisgrupper for fordelskunder**–Denne side viser en liste over fordelskundeprogrammer og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc77-126">**Loyalty price groups** - This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
-   <span data-ttu-id="bcc77-127">**Prisgrupper for tilhørsforhold**–Denne side viser en liste over tilhørsforhold og rabatter, der er kædet sammen for hver prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="bcc77-127">**Affiliation price groups** - This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="bcc77-128">Rabatopsætning for eksempelkanal</span><span class="sxs-lookup"><span data-stu-id="bcc77-128">Example channel discount set up</span></span>
<span data-ttu-id="bcc77-129">Følgende eksempel illustrerer de opgaver, der er involveret i oprettelse af en kanalrabat.</span><span class="sxs-lookup"><span data-stu-id="bcc77-129">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1.  <span data-ttu-id="bcc77-130">I dette eksempel har du en kanal kaldet **Horsens**, og du vil oprette en ny rabat, kaldet **I skole igen.**</span><span class="sxs-lookup"><span data-stu-id="bcc77-130">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School.**</span></span>
2.  <span data-ttu-id="bcc77-131">Da strategien for prissætning og rabat indeholder muligheden for kanalrabatter, opretter du altid en kanalspecifikke prisgruppe, når du opretter en kanal.</span><span class="sxs-lookup"><span data-stu-id="bcc77-131">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3.  <span data-ttu-id="bcc77-132">Du har prisgruppen **Horsens-PG**, og den er tildelt til kanalen **Horsens**.</span><span class="sxs-lookup"><span data-stu-id="bcc77-132">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4.  <span data-ttu-id="bcc77-133">Når du har oprettet den nye **I skole igen**-rabat, skal du klikke på **Prisgrupper** øverst på **Rabat** siden.</span><span class="sxs-lookup"><span data-stu-id="bcc77-133">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="bcc77-134">Siden **Detailprisgrupper** åbnes.</span><span class="sxs-lookup"><span data-stu-id="bcc77-134">The **Discount price groups** page will open.</span></span> <span data-ttu-id="bcc77-135">Klik derefter på **ny** , og vælg prisgruppen **Horsens-PG**.</span><span class="sxs-lookup"><span data-stu-id="bcc77-135">Next, click **New** and select the **Houston-PG** price group.</span></span>
5.  <span data-ttu-id="bcc77-136">Du kan nu aktivere rabatten og sende den til kanalen.</span><span class="sxs-lookup"><span data-stu-id="bcc77-136">Now you can enable the discount and push it to the channel.</span></span>



<a name="see-also"></a><span data-ttu-id="bcc77-137">Se også</span><span class="sxs-lookup"><span data-stu-id="bcc77-137">See also</span></span>
--------

[<span data-ttu-id="bcc77-138">Prisjusteringer og rabatter</span><span class="sxs-lookup"><span data-stu-id="bcc77-138">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)




