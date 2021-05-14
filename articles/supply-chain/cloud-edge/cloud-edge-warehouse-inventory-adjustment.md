---
title: Lagerregulering for lagersted
description: Dette emne indeholder oplysninger om lagerstedets lagerreguleringskladde og behandling, når du bruger skaleringsenheder.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938220"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="a00c7-103">Lagerregulering for lagersted</span><span class="sxs-lookup"><span data-stu-id="a00c7-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a00c7-104">Funktionen Lagersteds lagerregulering anvendes ved kørsel af cloud- og kantskaleringsenheder til [produktionsbelastninger](cloud-edge-workload-manufacturing.md) og [belastninger i lagerstyring](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="a00c7-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="a00c7-105">Når en arbejder udfører en lagerregulering ved hjælp af lagerstedsappen i forhold til belastningen for lagerstedsstyring i en skaleringsenhed, skal opdateringen af den fysiske disponible lagerbeholdning behandles af batchjobbet **Lagerregulering for lagersted**, som du kan køre og planlægge ved at gå til **Lagerstedsstyring > Periodiske opgaver > Lagerreguleringskladde for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="a00c7-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="a00c7-106">Følgende arbejdsprocesser for lagerstedsappen bruger aktuelt **Lagerreguleringskladde for lagersted** til arbejdsbelastninger for skaleringsenhed:</span><span class="sxs-lookup"><span data-stu-id="a00c7-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="a00c7-107">Regulering ind/ud</span><span class="sxs-lookup"><span data-stu-id="a00c7-107">Adjustment in/out</span></span>
- <span data-ttu-id="a00c7-108">Cyklusoptælling</span><span class="sxs-lookup"><span data-stu-id="a00c7-108">Cycle counting</span></span>
- <span data-ttu-id="a00c7-109">Indlæsning af nummerplade</span><span class="sxs-lookup"><span data-stu-id="a00c7-109">License plate loading</span></span>

<span data-ttu-id="a00c7-110">Flere lagertransaktioner oprettes som en del skyen eller edge i en lagerreguleringsproces, fordi hubbens og skaleringsenhedens installationer deler lagerposter.</span><span class="sxs-lookup"><span data-stu-id="a00c7-110">Several inventory transactions are created as part of cloud and edge an inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="a00c7-111">Eksempel på lagerregulering</span><span class="sxs-lookup"><span data-stu-id="a00c7-111">Inventory adjustment example</span></span>

<span data-ttu-id="a00c7-112">I dette eksempel har en lagerarbejder brugt lagerstedsappen til at registrere tilføjelse af disponibel lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="a00c7-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="a00c7-113">For det første opretter arbejdsbelastningen for skaleringsenheden en lagerreguleringstransaktion for lagerstedet med henblik på den positive fysiske regulering, som derefter synkroniseres med hubben og resulterer i en stigning i den disponible lagerbeholdning i hubbben.</span><span class="sxs-lookup"><span data-stu-id="a00c7-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="a00c7-114">Type</span><span class="sxs-lookup"><span data-stu-id="a00c7-114">Type</span></span>                                    | <span data-ttu-id="a00c7-115">Skalaenhed</span><span class="sxs-lookup"><span data-stu-id="a00c7-115">Scale unit</span></span> | <span data-ttu-id="a00c7-116">Vej</span><span class="sxs-lookup"><span data-stu-id="a00c7-116">Direction</span></span> | <span data-ttu-id="a00c7-117">Hub</span><span class="sxs-lookup"><span data-stu-id="a00c7-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="a00c7-118">Lagerregulering for lagersted</span><span class="sxs-lookup"><span data-stu-id="a00c7-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="a00c7-119">+1</span><span class="sxs-lookup"><span data-stu-id="a00c7-119">+1</span></span>         | ->        | <span data-ttu-id="a00c7-120">+1</span><span class="sxs-lookup"><span data-stu-id="a00c7-120">+1</span></span>  |

<span data-ttu-id="a00c7-121">Derefter behandler hubben en optællingskladdebogføring, der modtages via [meddelelser for meddelelsesprocessoren](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a00c7-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="a00c7-122">Derved opdateres den ekstra disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="a00c7-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="a00c7-123">For at forhindre dobbelt disponibel lagerbeholdning opretter hubnen en modkontering som en del af denne proces og fjerner den tidligere registrerede disponible lagerbeholdning, som er knyttet til lagerreguleringen for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="a00c7-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="a00c7-124">Type</span><span class="sxs-lookup"><span data-stu-id="a00c7-124">Type</span></span>                                    | <span data-ttu-id="a00c7-125">Skalaenhed</span><span class="sxs-lookup"><span data-stu-id="a00c7-125">Scale unit</span></span> | <span data-ttu-id="a00c7-126">Vej</span><span class="sxs-lookup"><span data-stu-id="a00c7-126">Direction</span></span> | <span data-ttu-id="a00c7-127">Hub</span><span class="sxs-lookup"><span data-stu-id="a00c7-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="a00c7-128">Tælling</span><span class="sxs-lookup"><span data-stu-id="a00c7-128">Counting</span></span>                                | <span data-ttu-id="a00c7-129">+1</span><span class="sxs-lookup"><span data-stu-id="a00c7-129">+1</span></span>         | <-        | <span data-ttu-id="a00c7-130">+1</span><span class="sxs-lookup"><span data-stu-id="a00c7-130">+1</span></span>  |
| <span data-ttu-id="a00c7-131">Lagerregulering for lagersted (modkontering)</span><span class="sxs-lookup"><span data-stu-id="a00c7-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="a00c7-132">-1</span><span class="sxs-lookup"><span data-stu-id="a00c7-132">-1</span></span>         | <-        | <span data-ttu-id="a00c7-133">-1</span><span class="sxs-lookup"><span data-stu-id="a00c7-133">-1</span></span>  |

<span data-ttu-id="a00c7-134">Når en skaleringsenhed har oprettet en **Lagerreguleringskladde for lagersted** i hubben, kan du gennemse både den **Optællingskladde** og **Modkonteringskladde**, som er oprettet af hubben som en del af reguleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="a00c7-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="a00c7-135">Du kan gennemgå hver af disse kladdeposter og transaktioner i Supply Chain Management ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a00c7-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="a00c7-136">Log på skaleringsenheden.</span><span class="sxs-lookup"><span data-stu-id="a00c7-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="a00c7-137">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Lagerreguleringskladde for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="a00c7-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="a00c7-138">Søg efter og åbn den kladde, der registrerede ændringen af den disponible lagerbeholdning, på siden **Lagerreguleringskladde for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="a00c7-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="a00c7-139">Sektionen **Kladdelinjer** viser hver regulering, der er registreret i denne kladde.</span><span class="sxs-lookup"><span data-stu-id="a00c7-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="a00c7-140">Log på hubben.</span><span class="sxs-lookup"><span data-stu-id="a00c7-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="a00c7-141">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Lagerreguleringskladde for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="a00c7-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="a00c7-142">På siden **Lagerreguleringskladde for lagersted** bør du kunne se den samme kladde, hvis hubben og skaleringsenheden er synkroniserede.</span><span class="sxs-lookup"><span data-stu-id="a00c7-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="a00c7-143">Åbn kladden.</span><span class="sxs-lookup"><span data-stu-id="a00c7-143">Open the journal.</span></span> <span data-ttu-id="a00c7-144">Hvis [meddelelserne fra meddelelsesprocessoren](cloud-edge-message-processor-messages.md) er blevet behandlet, vises hyperlinks til **Optællingsklade** og **Modkonteringskladde** i hovedet.</span><span class="sxs-lookup"><span data-stu-id="a00c7-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="a00c7-145">**Optællingskladde** skal vise de samme dimensionsværdier som kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="a00c7-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="a00c7-146">**Modkonteringskladde** skal vise modkonteringen, der fjerner den dobbelte lagerregulering.</span><span class="sxs-lookup"><span data-stu-id="a00c7-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="a00c7-147">Når al synkronisering og behandling er fuldført, synkroniseres **Optællingskladde** og **Modkonteringskladde** tilbage til skaleringsenheden.</span><span class="sxs-lookup"><span data-stu-id="a00c7-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="a00c7-148">De kan også ses fra den relevante side for **Lagerreguleringskladde for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="a00c7-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
