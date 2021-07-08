---
title: Antallet overskrider procenten for underlevering under oprettelse af en følgeseddel
description: Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for underlevering.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249074"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="06225-103">Antallet overskrider procenten for underlevering under oprettelse af en følgeseddel</span><span class="sxs-lookup"><span data-stu-id="06225-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="06225-104">Fejlkode: SYS24921</span><span class="sxs-lookup"><span data-stu-id="06225-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="06225-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="06225-105">Symptoms</span></span>

<span data-ttu-id="06225-106">Når du opretter en følgeseddel, indeholder den udgående last et antal, der overstiger procenten for underlevering.</span><span class="sxs-lookup"><span data-stu-id="06225-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="06225-107">Når du forsøger at oprette en følgeseddel, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="06225-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="06225-108">Linjen underleveres med %1 procent, men den tilladte underlevering er kun %2 procent.</span><span class="sxs-lookup"><span data-stu-id="06225-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="06225-109">Du kan derfor ikke oprette følgesedlen for lasten.</span><span class="sxs-lookup"><span data-stu-id="06225-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="06225-110">Årsag</span><span class="sxs-lookup"><span data-stu-id="06225-110">Cause</span></span>

<span data-ttu-id="06225-111">Det plukkede antal for lasten eller forsendelsen er mindre end det bestilte antal og ligger ikke inden for intervallet for procenten for underlevering.</span><span class="sxs-lookup"><span data-stu-id="06225-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="06225-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="06225-112">Resolution</span></span>

<span data-ttu-id="06225-113">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor der ikke kan oprettes en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="06225-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="06225-114">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="06225-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="06225-115">Juster procenten for underlevering.</span><span class="sxs-lookup"><span data-stu-id="06225-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="06225-116">Tilbagefør og foretag reguleringer.</span><span class="sxs-lookup"><span data-stu-id="06225-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="06225-117">Justere procenten for underlevering</span><span class="sxs-lookup"><span data-stu-id="06225-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="06225-118">Du kan bruge følgende procedure til at justere procenten for underlevering.</span><span class="sxs-lookup"><span data-stu-id="06225-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="06225-119">Gå til **Debitor \> Ordrer \> Alle ordrer**.</span><span class="sxs-lookup"><span data-stu-id="06225-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="06225-120">Vælg den salgsordre, som du ikke kan bogføre en følgeseddel for lasten for.</span><span class="sxs-lookup"><span data-stu-id="06225-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="06225-121">Vælg salgsordrelinjen for den vare, der overstiger procenten for underlevering, i oversigtspanelet  **Salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="06225-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="06225-122">Vælg **Levering** under fanen  **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="06225-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="06225-123">Angiv feltet **Underlevering** til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så du kan fortsætte med at oprette følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="06225-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="06225-124">Tilbageføre og foretage reguleringer</span><span class="sxs-lookup"><span data-stu-id="06225-124">Reverse and make adjustments</span></span>

<span data-ttu-id="06225-125">Tilbagefør alt det, der er bogført for lasten (f.eks. følgesedlen, forsendelsesbekræftelsen og arbejdet), foretag salgsordrereguleringer, frigiv ordren til lagerstedet igen, og fuldfør forsendelsesproceduren.</span><span class="sxs-lookup"><span data-stu-id="06225-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="06225-126">Brug følgende procedure til at annullere en følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="06225-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="06225-127">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="06225-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="06225-128">Vælg  **Annuller følgesedler** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06225-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="06225-129">Brug følgende procedure til at tilbageføre en forsendelsesbekræftelse.</span><span class="sxs-lookup"><span data-stu-id="06225-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="06225-130">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="06225-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="06225-131">Vælg  **Tilbagefør forsendelsesbekræftelse** i gruppen  **Tilbagefør** under fanen  **Levér og modtag** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="06225-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="06225-132">Benyt følgende fremgangsmåde for at tilbageføre arbejde.</span><span class="sxs-lookup"><span data-stu-id="06225-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="06225-133">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="06225-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="06225-134">Gå til handlingsruden, og vælg  **Tilbagefør arbejde** i gruppen  **Arbejde** under fanen  **Laster**.</span><span class="sxs-lookup"><span data-stu-id="06225-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
