---
title: Vurderingsprofiler
description: Dette emne beskriver, hvordan du konfigurerer data til vurderingsprofiler.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828436"
---
# <a name="rating-profiles"></a><span data-ttu-id="7d67b-103">Vurderingsprofiler</span><span class="sxs-lookup"><span data-stu-id="7d67b-103">Rating profiles</span></span>

<span data-ttu-id="7d67b-104">En vurderingsprofil ligner en logistikkontrakt (men ikke en juridisk kontrakt).</span><span class="sxs-lookup"><span data-stu-id="7d67b-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="7d67b-105">Den anvendes til at bestemme transporttariffer for laster.</span><span class="sxs-lookup"><span data-stu-id="7d67b-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="7d67b-106">Hver vurderingsprofil er entydig for en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="7d67b-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="7d67b-107">I profilen knytter du fragtmanden til en satsmaster.</span><span class="sxs-lookup"><span data-stu-id="7d67b-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="7d67b-108">Satsmasteren definerer tildelingen af satsgrundlaget og selve satsgrundlaget.</span><span class="sxs-lookup"><span data-stu-id="7d67b-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="7d67b-109">Satsgrundlaget bestemmer satsen for fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="7d67b-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="7d67b-110">Du kan konfigurere en vurderingsprofil ved hjælp af en generisk side, der indeholder en oversigt over alle eksisterende vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="7d67b-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="7d67b-111">Du kan også angive en vurderingsprofil direkte fra fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="7d67b-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="7d67b-112">I begge tilfælde er de oplysninger, du konfigurerer for vurderingsprofilen, de samme.</span><span class="sxs-lookup"><span data-stu-id="7d67b-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="7d67b-113">Oprette eller redigere en vurderingsprofil på siden Vurderingsprofiler</span><span class="sxs-lookup"><span data-stu-id="7d67b-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="7d67b-114">På siden **Vurderingsprofiler** kan du gennemse alle tilgængelige vurderingsprofiler.</span><span class="sxs-lookup"><span data-stu-id="7d67b-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="7d67b-115">Du kan også redigere eksisterende profiler og oprette nye profiler.</span><span class="sxs-lookup"><span data-stu-id="7d67b-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="7d67b-116">Gå til **Transportstyring \> Opsætning \> Vurdering \> Vurderingsprofil**.</span><span class="sxs-lookup"><span data-stu-id="7d67b-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="7d67b-117">Vælg **Ny** i handlingsruden for at tilføje en ny vurderingsprofil eller **Rediger** for at redigere en eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="7d67b-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="7d67b-118">Angiv følgende felter i rækken for den nye eller eksisterende vurderingsprofil:</span><span class="sxs-lookup"><span data-stu-id="7d67b-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="7d67b-119">**Vurderingsprofil** – Angiv et entydigt id for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="7d67b-120">**Navn** – Angiv et sigende navn til vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="7d67b-121">**Fragtmand** – Vælg en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="7d67b-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="7d67b-122">Den vurderingsprofil, du konfigurerer, vil også blive vist på siden **Fragtmænd** for den valgte fragtmand.</span><span class="sxs-lookup"><span data-stu-id="7d67b-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="7d67b-123">**Lokation** og **Lagersted** – Vælg en lokation og et lagersted.</span><span class="sxs-lookup"><span data-stu-id="7d67b-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="7d67b-124">**Satsprogram** – Vælg satsprogrammet for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="7d67b-125">**Satsmaster** – Vælg satsmasteren for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="7d67b-126">Du kan bruge satsmasteren til at definere en satsgrundlagstype og et satsgrundlag.</span><span class="sxs-lookup"><span data-stu-id="7d67b-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="7d67b-127">Du kan finde flere oplysninger i [Konfigurere satsmaster](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="7d67b-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="7d67b-128">**Program til transittid** – Vælg programmet til transittid for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="7d67b-129">**Brændstofindeks** – Vælg fragtmandens brændstofindeks for vurderingsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="7d67b-130">**Gældende startdato og -klokkeslæt** og **Gældende slutdato og -klokkeslæt** – Definer den periode, hvor vurderingsprofilen skal være aktiv.</span><span class="sxs-lookup"><span data-stu-id="7d67b-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="7d67b-131">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7d67b-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="7d67b-132">Oprette en vurderingsprofil direkte på siden Fragtmænd</span><span class="sxs-lookup"><span data-stu-id="7d67b-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="7d67b-133">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.</span><span class="sxs-lookup"><span data-stu-id="7d67b-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="7d67b-134">Vælg en fragtmand på listen.</span><span class="sxs-lookup"><span data-stu-id="7d67b-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="7d67b-135">I oversigtspanelet **Vurderingsprofiler** skal du vælge **Ny** for at oprette en vurderingsprofil.</span><span class="sxs-lookup"><span data-stu-id="7d67b-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="7d67b-136">Angiv felterne for den nye vurderingsprofil.</span><span class="sxs-lookup"><span data-stu-id="7d67b-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="7d67b-137">Disse felter svarer til felterne på siden **Vurderingsprofiler** som beskrevet i det forrige afsnit i dette emne.</span><span class="sxs-lookup"><span data-stu-id="7d67b-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="7d67b-138">Profiler, der oprettes på siden **Fragtmænd**, vises også på siden **Vurderingsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="7d67b-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]