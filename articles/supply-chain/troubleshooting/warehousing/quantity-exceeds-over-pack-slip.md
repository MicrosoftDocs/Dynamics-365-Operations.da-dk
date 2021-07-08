---
title: Antallet overskrider procenten for overlevering under oprettelse af en følgeseddel
description: Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for overlevering.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249076"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="5ea8e-103">Antallet overskrider procenten for overlevering under oprettelse af en følgeseddel</span><span class="sxs-lookup"><span data-stu-id="5ea8e-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="5ea8e-104">Fejlkode: SYS24920</span><span class="sxs-lookup"><span data-stu-id="5ea8e-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="5ea8e-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="5ea8e-105">Symptoms</span></span>

<span data-ttu-id="5ea8e-106">Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for overlevering.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="5ea8e-107">Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="5ea8e-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="5ea8e-108">Linjen overleveres med %1 procent, men den tilladte overlevering er kun %2 procent.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="5ea8e-109">Du kan derfor ikke oprette følgesedlen for lasten.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="5ea8e-110">Årsag</span><span class="sxs-lookup"><span data-stu-id="5ea8e-110">Cause</span></span>

<span data-ttu-id="5ea8e-111">Det plukkede antal for lasten eller forsendelsen er mere end det bestilte antal og ligger ikke inden for intervallet for procenten for overlevering.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="5ea8e-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="5ea8e-112">Resolution</span></span>

<span data-ttu-id="5ea8e-113">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="5ea8e-114">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="5ea8e-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="5ea8e-115">Justere antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="5ea8e-116">Justere procenten for overlevering.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="5ea8e-117">Tilbagefør og foretag reguleringer.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="5ea8e-118">Justere antallet for lastlinjen</span><span class="sxs-lookup"><span data-stu-id="5ea8e-118">Adjust the load line quantity</span></span>

<span data-ttu-id="5ea8e-119">Du kan bruge følgende procedure til at justere antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="5ea8e-120">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5ea8e-121">Vælg den last, som følgesedlen ikke kan genereres for.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="5ea8e-122">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="5ea8e-123">Vælg lastlinjen for den vare, der overstiger procenten for overlevering, under fanen  **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="5ea8e-124">Vælg **Reducer plukket antal** for at justere det plukkede antal.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="5ea8e-125">Vælg **Ordre** under fanen  **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="5ea8e-126">Angiv feltet **Antal** til det plukkede antal (dvs. værdien for feltet **Antal oprettet under arbejde**), så du kan fortsætte med at generere følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="5ea8e-127">Justere procenten for overlevering</span><span class="sxs-lookup"><span data-stu-id="5ea8e-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="5ea8e-128">Du kan bruge følgende procedure til at justere procenten for overlevering.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="5ea8e-129">Gå til **Debitor \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="5ea8e-130">Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="5ea8e-131">Vælg salgsordrelinjen for den vare, der overstiger procenten for overlevering, i oversigtspanelet  **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="5ea8e-132">Vælg **Levering** under fanen  **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="5ea8e-133">Angiv feltet **Overlevering** til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så du kan fortsætte med at oprette følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="5ea8e-134">Tilbageføre og foretage reguleringer</span><span class="sxs-lookup"><span data-stu-id="5ea8e-134">Reverse and make adjustments</span></span>

<span data-ttu-id="5ea8e-135">Tilbagefør alt det, der er bogført for lasten (f.eks. følgesedlen, forsendelsesbekræftelsen og arbejdet), foretag salgsordrereguleringer, frigiv ordren til lagerstedet igen, og fuldfør forsendelsesproceduren.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="5ea8e-136">Brug følgende procedure til at annullere en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="5ea8e-137">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5ea8e-138">Vælg  **Annuller følgesedler** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="5ea8e-139">Brug følgende procedure til at tilbageføre en forsendelsesbekræftelse.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="5ea8e-140">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5ea8e-141">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="5ea8e-142">Benyt følgende fremgangsmåde for at tilbageføre arbejde.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="5ea8e-143">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5ea8e-144">Gå til handlingsruden, og vælg  **Tilbagefør arbejde** i gruppen  **Arbejde** under fanen  **Laster**.</span><span class="sxs-lookup"><span data-stu-id="5ea8e-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
