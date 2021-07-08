---
title: Plukket antal er ikke tilstrækkeligt under generering af følgeseddel
description: Når du genererer en følgeseddel, indeholder den udgående last et plukket antal, der ikke svarer til det oprettede arbejdsantal på lastlinjen.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249078"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="50b55-103">Plukket antal er ikke tilstrækkeligt under generering af følgeseddel</span><span class="sxs-lookup"><span data-stu-id="50b55-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="50b55-104">Fejlkode: SYS54073</span><span class="sxs-lookup"><span data-stu-id="50b55-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="50b55-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="50b55-105">Symptoms</span></span>

<span data-ttu-id="50b55-106">Når du genererer en følgeseddel, indeholder den udgående last et plukket antal, der ikke svarer til det oprettede arbejdsantal på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="50b55-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="50b55-107">Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="50b55-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="50b55-108">Da der er plukket %1, kan der ikke kun opdateres %2, når resten efterfølgende skal være %3.</span><span class="sxs-lookup"><span data-stu-id="50b55-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="50b55-109">Du kan derfor ikke oprette følgesedlen for lasten.</span><span class="sxs-lookup"><span data-stu-id="50b55-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="50b55-110">Årsag</span><span class="sxs-lookup"><span data-stu-id="50b55-110">Cause</span></span>

<span data-ttu-id="50b55-111">Følgesedlen kan ikke oprettes i dens aktuelle tilstand, da en af følgende betingelser kan være til stede:</span><span class="sxs-lookup"><span data-stu-id="50b55-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="50b55-112">Det relaterede arbejde er endnu ikke plukket og flyttet til det endelige afsendelsessted.</span><span class="sxs-lookup"><span data-stu-id="50b55-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="50b55-113">Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.</span><span class="sxs-lookup"><span data-stu-id="50b55-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="50b55-114">Antallet på lastlinjen, det oprettede arbejdsantal og det plukkede arbejdsantal stemmer ikke overens.</span><span class="sxs-lookup"><span data-stu-id="50b55-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="50b55-115">Løsning</span><span class="sxs-lookup"><span data-stu-id="50b55-115">Resolution</span></span>

<span data-ttu-id="50b55-116">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="50b55-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="50b55-117">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="50b55-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="50b55-118">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="50b55-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="50b55-119">Justere antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="50b55-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="50b55-120">Tilbageføre alle plukregistreringer og gentage pluk.</span><span class="sxs-lookup"><span data-stu-id="50b55-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="50b55-121">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens</span><span class="sxs-lookup"><span data-stu-id="50b55-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="50b55-122">Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="50b55-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="50b55-123">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="50b55-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="50b55-124">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="50b55-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="50b55-125">Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="50b55-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="50b55-126">Notér værdien for feltet **Antal oprettet under arbejde**.</span><span class="sxs-lookup"><span data-stu-id="50b55-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="50b55-127">under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="50b55-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="50b55-128">Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="50b55-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="50b55-129">Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="50b55-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="50b55-130">Justere antallet for lastlinjen</span><span class="sxs-lookup"><span data-stu-id="50b55-130">Adjust the load line quantity</span></span>

<span data-ttu-id="50b55-131">Du kan bruge følgende procedure til at justere antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="50b55-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="50b55-132">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="50b55-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="50b55-133">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="50b55-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="50b55-134">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="50b55-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="50b55-135">Vælg lastlinjen for den vare, der forårsager et problem, under fanen  **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="50b55-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="50b55-136">Vælg **Reducer plukket antal** for at justere det plukkede antal.</span><span class="sxs-lookup"><span data-stu-id="50b55-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="50b55-137">Angiv feltet **Reducer lastlinje**, så det afspejler justeringer på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="50b55-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="50b55-138">Tilbageføre alle plukregistreringer og gentage pluk</span><span class="sxs-lookup"><span data-stu-id="50b55-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="50b55-139">Problemet kan forekomme, fordi en anden har brugt plukregistrering til at lukke en lastlinje uden arbejde.</span><span class="sxs-lookup"><span data-stu-id="50b55-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="50b55-140">I dette tilfælde skal manuel plukregistrering tilbageføres, og plukningen skal derefter udføres ved hjælp af mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="50b55-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="50b55-141">Du kan bruge følgende procedure til at tilbageføre plukregistreringen.</span><span class="sxs-lookup"><span data-stu-id="50b55-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="50b55-142">Gå til **Debitor \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="50b55-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="50b55-143">Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="50b55-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="50b55-144">Vælg den salgsordrelinje, som plukregistrering er udført for, under fanen  **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="50b55-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="50b55-145">Vælg **Opdater linje \> Pluk** for at fortryde pluk af varerne.</span><span class="sxs-lookup"><span data-stu-id="50b55-145">Select **Update line \> Pick** to unpick the items.</span></span>
