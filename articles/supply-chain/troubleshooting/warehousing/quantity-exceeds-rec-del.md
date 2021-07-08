---
title: Det antal, som du forsøger at opdatere, overskrider det antal, der er modtaget/leveret.
description: Når du genererer en følgeseddel, indeholder den udgående last et plukket antal, der overstiger det arbejdsantal, der er plukket og reserveret til salgsordren.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249079"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="3e5d5-103">Det antal, som du forsøger at opdatere, overskrider det antal, der er modtaget/leveret</span><span class="sxs-lookup"><span data-stu-id="3e5d5-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="3e5d5-104">Fejlkode: SYS7676</span><span class="sxs-lookup"><span data-stu-id="3e5d5-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="3e5d5-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="3e5d5-105">Symptoms</span></span>

<span data-ttu-id="3e5d5-106">Når du genererer en følgeseddel, indeholder den udgående last et plukket antal, der overstiger det arbejdsantal, der er plukket og reserveret til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="3e5d5-107">Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="3e5d5-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="3e5d5-108">Det antal, du prøver at opdatere, overskrider det modtagne/leverede antal.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="3e5d5-109">Du kan derfor ikke oprette følgesedlen for lasten.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="3e5d5-110">Årsag</span><span class="sxs-lookup"><span data-stu-id="3e5d5-110">Cause</span></span>

<span data-ttu-id="3e5d5-111">Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="3e5d5-112">Dette problem kan for eksempel opstå, hvis antallet på lastlinjen, det arbejde, der er oprettet, eller det plukkede antal ikke er nøjagtigt.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="3e5d5-113">Løsning</span><span class="sxs-lookup"><span data-stu-id="3e5d5-113">Resolution</span></span>

<span data-ttu-id="3e5d5-114">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="3e5d5-115">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="3e5d5-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="3e5d5-116">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="3e5d5-117">Justere antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="3e5d5-118">Tilbageføre alle plukregistreringer og gentage pluk.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="3e5d5-119">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens</span><span class="sxs-lookup"><span data-stu-id="3e5d5-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="3e5d5-120">Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="3e5d5-121">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3e5d5-122">Vælg den last, som forsendelsen ikke kan oprettes for.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="3e5d5-123">Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="3e5d5-124">Notér værdien for feltet **Antal oprettet under arbejde**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="3e5d5-125">under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="3e5d5-126">Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="3e5d5-127">Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="3e5d5-128">Justere antallet for lastlinjen</span><span class="sxs-lookup"><span data-stu-id="3e5d5-128">Adjust the load line quantity</span></span>

<span data-ttu-id="3e5d5-129">Du kan bruge følgende procedure til at justere antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="3e5d5-130">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="3e5d5-131">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="3e5d5-132">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="3e5d5-133">Vælg lastlinjen for den vare, der forårsager et problem, under fanen  **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="3e5d5-134">Vælg **Reducer plukket antal** for at justere det plukkede antal.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="3e5d5-135">Angiv feltet **Reducer lastlinje**, så det afspejler justeringer på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="3e5d5-136">Tilbageføre alle plukregistreringer og gentage pluk</span><span class="sxs-lookup"><span data-stu-id="3e5d5-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="3e5d5-137">Hvis en person har brugt plukregistrering til at lukke en lastlinje uden arbejde, kan der forekomme en uoverensstemmelse mellem antallet på lastlinjen og det plukkede antal.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="3e5d5-138">I dette tilfælde skal manuel plukregistrering tilbageføres, og plukningen skal derefter udføres ved hjælp af mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="3e5d5-139">Du kan bruge følgende procedure til at tilbageføre plukregistreringen.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="3e5d5-140">Gå til **Debitor \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="3e5d5-141">Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="3e5d5-142">Vælg den salgsordrelinje, som plukregistrering er udført for, under fanen  **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="3e5d5-143">Vælg **Opdater linje \> Pluk** for at fortryde pluk af varerne.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-143">Select **Update line \> Pick** to unpick the items.</span></span>
