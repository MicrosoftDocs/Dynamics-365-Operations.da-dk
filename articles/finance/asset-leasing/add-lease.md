---
title: Tilføj eller Kopiér leasinger (prøveversion)
description: Dette emne beskriver, hvordan du opretter en ny leasing ved at angive oplysninger om den i aktivleasing eller ved at kopiere oplysninger fra en eksisterende leasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: abbf04d009a4b347792cd8b317e334da2a4cbbee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969597"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="39112-103">Tilføj eller Kopiér leasinger (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="39112-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39112-104">Dette emne forklarer, hvordan du kan oprette en leasing fra bunden af aktivleasing, og hvordan du kan oprette en leasing ved at kopiere en eksisterende leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="39112-105">Processen til oprettelse af en leasing fra bunden omfatter angivelse af oplysninger til den nye leasing og oprettelse af en plan for leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="39112-106">Når der er konfigureret mindst én leasing, kan det være nemmere at kopiere oplysningerne fra en eksisterende leasing og derefter redigere disse oplysninger, når du har brug for at oprette en ny leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="39112-107">Oprette en leasing</span><span class="sxs-lookup"><span data-stu-id="39112-107">Create a lease</span></span>

<span data-ttu-id="39112-108">Udfør følgende trin for at oprette en leasing i aktivleasing.</span><span class="sxs-lookup"><span data-stu-id="39112-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="39112-109">Gå til siden **Leasingoversigt**, og vælg **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="39112-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="39112-110">Angiv oplysninger om leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-110">Enter the lease information.</span></span> <span data-ttu-id="39112-111">De felter, der skal bruges, har røde kanter.</span><span class="sxs-lookup"><span data-stu-id="39112-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="39112-112">Oprette en leasingplan</span><span class="sxs-lookup"><span data-stu-id="39112-112">Create a lease schedule</span></span>

<span data-ttu-id="39112-113">Når du er færdig med at angive oplysninger om en leasing, skal du udføre følgende trin for at oprette en leasingplan.</span><span class="sxs-lookup"><span data-stu-id="39112-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="39112-114">De økonomiske dimensioner kan ændres på baggrund af eventuelle brugerdefinerede økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="39112-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="39112-115">Vælg **Opret planer** for at generere leasingkartotekerne.</span><span class="sxs-lookup"><span data-stu-id="39112-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="39112-116">Leasingkartotekerne omfatter planerne for betaling, amortisering, afskrivning og repræsentationer.</span><span class="sxs-lookup"><span data-stu-id="39112-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="39112-117">Hvis du vil have adgang til leasingkartoteker og få vist de nyoprettede planer, skal du vælge fanen **Kartoteker**.</span><span class="sxs-lookup"><span data-stu-id="39112-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="39112-118">På siden **Kartotekoplysninger** kan du se, hvordan rettigheden redegøres for de kartoteker, der er tildelt til den.</span><span class="sxs-lookup"><span data-stu-id="39112-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="39112-119">Herfra kan du få vist planlægninger af leasingen.</span><span class="sxs-lookup"><span data-stu-id="39112-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="39112-120">Betalingsplanen indeholder input fra fanen **Betalingsplanlinjer** på siden **Tilføj leasing**.</span><span class="sxs-lookup"><span data-stu-id="39112-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="39112-121">Du kan stadig ændre hvert betalingsbeløb og variabel betaling.</span><span class="sxs-lookup"><span data-stu-id="39112-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="39112-122">Leasingforpligtelsen beregnes på baggrund af den ændrede betalingsplan.</span><span class="sxs-lookup"><span data-stu-id="39112-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="39112-123">Når du er færdig med at gennemse betalingsplanen, skal du vælge **Bekræft plan**.</span><span class="sxs-lookup"><span data-stu-id="39112-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="39112-124">Når planen er bekræftet, er rettigheden ikke længere tilgængelig til redigering.</span><span class="sxs-lookup"><span data-stu-id="39112-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39112-125">Systemet beregner automatisk leasingperioden fra betalingsplanlinjerne på siden **Tilføj leasing**.</span><span class="sxs-lookup"><span data-stu-id="39112-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="39112-126">Hvis leasingperioden skal beregnes i måneder, finder systemet differencen mellem startdatoen og slutdatoen for en bestemt betalingsplanlinje.</span><span class="sxs-lookup"><span data-stu-id="39112-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="39112-127">Der flyttes derefter til den næste betalingsplanlinje og finder differencen igen.</span><span class="sxs-lookup"><span data-stu-id="39112-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="39112-128">Til sidst summerer systemet alle de beløb, der skal fastlægges for leasingperioden i måneder.</span><span class="sxs-lookup"><span data-stu-id="39112-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="39112-129">Hvis du vil have vist de beregnede perioders renteudgifter, skal du åbne siden **Amortiseringsplanen for leasingforpligtelse**.</span><span class="sxs-lookup"><span data-stu-id="39112-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="39112-130">Hvis du vil have vist beregnede lineære afskrivninger, skal du åbne siden **Afskrivningsplan for aktiver**.</span><span class="sxs-lookup"><span data-stu-id="39112-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="39112-131">Når du er færdig med at gennemse det beregnede beløb, kan du oprette postering af den oprindelige genkendelseskladde på siden **Første indregning**.</span><span class="sxs-lookup"><span data-stu-id="39112-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="39112-132">Du får vist en meddelelse om, at kladden er oprettet.</span><span class="sxs-lookup"><span data-stu-id="39112-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39112-133">Kladdeposten bogføres ikke i Finans, før du bogfører posten manuelt.</span><span class="sxs-lookup"><span data-stu-id="39112-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="39112-134">Hvis du vil gennemse den foreslåede oprindelige genkendelsespost, før du bogfører den, skal du vælge **Aktivleasingkladde**.</span><span class="sxs-lookup"><span data-stu-id="39112-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39112-135">Aktivleasingkladde kan ikke oprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="39112-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="39112-136">Den oprettes automatisk, når der oprettes planlagte tidsplaner.</span><span class="sxs-lookup"><span data-stu-id="39112-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="39112-137">Når du er færdig med at gennemse journalposten for den oprindelige genkendelseskladde og er klar til at bogføre den, skal du vælge **Bogfør** for at genkende brugsretsaktivet (ROU) og rettighedspassiver i Finans.</span><span class="sxs-lookup"><span data-stu-id="39112-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="39112-138">Kopiere en leasing</span><span class="sxs-lookup"><span data-stu-id="39112-138">Copy a lease</span></span>

<span data-ttu-id="39112-139">Ved leasing af aktiver kan du kopiere oplysningerne til en leasing for at oprette en ny leasing, der har de samme oplysninger.</span><span class="sxs-lookup"><span data-stu-id="39112-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="39112-140">Du kan derefter ændre leasingfelterne, før du opretter planerne for den kopierede leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="39112-141">Vælg den leasing, der skal kopieres på siden **Leasingoversigt**, og vælg derefter **Kopiér leasing** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="39112-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39112-142">Hvis den **manuelle** parameter er slået fra for nummerserien for lease-id, oprettes det næste nummer i sekvensen automatisk som rettigheds-id for den kopierede leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="39112-143">Hvis parameteren **Manuel** er slået til, får du vist en meddelelse, hvor du bliver bedt om at angive et leasing-id, før du fortsætter med at kopiere leasingen.</span><span class="sxs-lookup"><span data-stu-id="39112-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="39112-144">Vælg **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="39112-144">Select **Copy**.</span></span> <span data-ttu-id="39112-145">Oplysningerne om leasingen for den valgte leasing kopieres til en ny leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="39112-146">Du kan derefter redigere oplysningerne om den nye leasing, før du gemmer den, og opretter planlægningen af leasing.</span><span class="sxs-lookup"><span data-stu-id="39112-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="39112-147">Aktivleasingkladde</span><span class="sxs-lookup"><span data-stu-id="39112-147">Asset leasing journal</span></span>

<span data-ttu-id="39112-148">Alle de kladdeposteringer, der er oprettet under Aktiv leasing, findes i Aktivleasingkladden.</span><span class="sxs-lookup"><span data-stu-id="39112-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="39112-149">På siden **Aktivleasingkladde** (**Aktivleasing\> Kladdeposteringer \> Aktivleasingkladde**) kan du filtrere efter bogføringsstatus, få vist bestemte kladdeposteringer og bilag og bogføre ikke-bogførte kladdeposter.</span><span class="sxs-lookup"><span data-stu-id="39112-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="39112-150">Aktivleasingkladde kan ikke oprettes manuelt.</span><span class="sxs-lookup"><span data-stu-id="39112-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="39112-151">Den oprettes automatisk, når der oprettes planlagte tidsplaner.</span><span class="sxs-lookup"><span data-stu-id="39112-151">It's automatically created when lease schedules are created.</span></span>
