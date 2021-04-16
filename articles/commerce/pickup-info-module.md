---
title: Modul med afhentningsoplysninger
description: I dette emne beskrives afhentningsoplysningsmodulet, og det beskriver, hvordan du kan føje det til betalingssider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 063701d5cd5714febeb32907346d9f6e5c2a2ca1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804399"
---
# <a name="pickup-information-module"></a><span data-ttu-id="7bdee-103">Modul til afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="7bdee-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7bdee-104">I dette emne beskrives afhentningsoplysningsmodulet, og det beskriver, hvordan du kan føje det til betalingssider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7bdee-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7bdee-105">Modulet med afhentningsoplysninger kan bruges i betalingsmodulet til at vise oplysninger om ordreafhentning.</span><span class="sxs-lookup"><span data-stu-id="7bdee-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="7bdee-106">Kunder kan få vist de tilgængelige afhentningsdatoer og tidsintervaller og derefter vælge et passende tidspunkt at afhente ordren.</span><span class="sxs-lookup"><span data-stu-id="7bdee-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="7bdee-107">En kunde kan f.eks. vælge at afhente en ordre kl. 15 den 21. marts i en butik i Slagelse.</span><span class="sxs-lookup"><span data-stu-id="7bdee-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="7bdee-108">Afhentningstider for de relevante butikker skal konfigureres i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7bdee-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="7bdee-109">Du kan finde flere oplysninger under [Oprette og opdatere tidsintervaller for kundeafhentning](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="7bdee-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="7bdee-110">Hvis der oprettes et afhentningsoplysningsmodul på en betalingsside, men der ikke er defineret nogen tidsintervaller for den butik, der er valgt til afhentning, vises der oplysninger i modulet, men brugeren kan ikke vælge nogen tidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="7bdee-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="7bdee-111">Tidsintervaller er valgfrie og er ikke påkrævede ved afgivelse af en ordre.</span><span class="sxs-lookup"><span data-stu-id="7bdee-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="7bdee-112">Hvis der er valgt flere varer til afhentning på tværs af flere butikker, vil brugeren have mulighed for at vælge et tidsinterval i afhentningsmodulet for hver butik, hvis der er tilgængelige tidsintervaller for den.</span><span class="sxs-lookup"><span data-stu-id="7bdee-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="7bdee-113">Understøttelse af tidsintervaller og afhentningsoplysningsmodulet på betalingssiden er tilgængelige i Dynamics 365 Commerce version 10.0.15 og nyere versioner.</span><span class="sxs-lookup"><span data-stu-id="7bdee-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="7bdee-114">I følgende illustration vises et eksempel på valg af tidsinterval via modulet med afhentningsoplysninger på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="7bdee-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Eksempel på et afhentningsoplysningsmodul på en betalingsside](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="7bdee-116">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="7bdee-116">Module properties</span></span>

- <span data-ttu-id="7bdee-117">**Overskrift** – Angiv en overskrift til modulet.</span><span class="sxs-lookup"><span data-stu-id="7bdee-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="7bdee-118">Vise tidsintervaloplysninger, når en ordre er afgivet</span><span class="sxs-lookup"><span data-stu-id="7bdee-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="7bdee-119">Når en ordre er afgivet, kan oplysninger om det valgte tidsinterval ses i [ordrebekræftelsesmodulet](order-confirmation-module.md) og [ordreoplysningsmodulet](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="7bdee-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="7bdee-120">Begge disse moduler har egenskaben **Vis tidsintervaloplysninger**.</span><span class="sxs-lookup"><span data-stu-id="7bdee-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="7bdee-121">Hvis du vil have vist det valgte tidsinterval under ordreprocessen, skal denne egenskab være indstillet til **Sand**.</span><span class="sxs-lookup"><span data-stu-id="7bdee-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="7bdee-122">Føje et afhentningsoplysningsmodul for betaling til en side</span><span class="sxs-lookup"><span data-stu-id="7bdee-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="7bdee-123">Du kan få flere oplysninger om, hvordan du føjer et afhentningsoplysningsmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="7bdee-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="7bdee-124">I følgende illustration vises et eksempel på en e-handelsbetalingside, der indeholder tidsintervaller for afhentningslinjevarer.</span><span class="sxs-lookup"><span data-stu-id="7bdee-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Eksempel på en e-handelsbetalingsside, der indeholder tidsintervaller for afhentningslinjevarer](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="7bdee-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7bdee-126">Additional resources</span></span>

[<span data-ttu-id="7bdee-127">Oprette og opdatere tidsintervaller for kundeafhentning</span><span class="sxs-lookup"><span data-stu-id="7bdee-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="7bdee-128">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="7bdee-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7bdee-129">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="7bdee-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7bdee-130">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="7bdee-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]