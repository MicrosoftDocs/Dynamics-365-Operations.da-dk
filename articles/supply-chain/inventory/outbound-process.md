---
title: Oversigt over udgående proces
description: Dette emne indeholder en oversigt over den udgående proces i Lagerstyring.
author: perlynne
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2f6638b3e79be5a2ebdbf6e5773285406239a080
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865442"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="0e6a0-103">Oversigt over udgående proces</span><span class="sxs-lookup"><span data-stu-id="0e6a0-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e6a0-104">Dette emne indeholder en oversigt over den udgående proces i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="0e6a0-105">Udlagringsordrer</span><span class="sxs-lookup"><span data-stu-id="0e6a0-105">Output orders</span></span>

<span data-ttu-id="0e6a0-106">Udlagringsordrer bruges til at sammenkæde salgsordrelinjer og flytteordrelinjer med udgående plukprocesser, der bruger pluklister.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="0e6a0-107">Når pluklister genereres fra enten salgsordrer eller flytteordrer, oprettes udlagringsordrer og forsendelser automatisk.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="0e6a0-108">En plukliste har en en til en-relation med en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="0e6a0-109">Flytteordreforsendelsen eller salgsordrefølgesedlen kan behandles fra forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="0e6a0-110">Følgende diagram viser en oversigt over processen for udgående ordrer.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="0e6a0-111">[![Oversigt over processen for udgående ordre](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="0e6a0-112">Du kan konfigurere udgående regler for at definere, hvordan programmet skal håndtere den udgående proces.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="0e6a0-113">Du kan bruge disse regler til at styre forsendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="0e6a0-114">Du kan især bruge reglerne til at styre, hvilket stadie i processen en forsendelse kan sendes under.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="0e6a0-115">Følgende indstillinger definerer, hvordan udgående processer håndteres.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="0e6a0-116">Status for plukrute for salgsordrer og flytteordrer</span><span class="sxs-lookup"><span data-stu-id="0e6a0-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="0e6a0-117">Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**, og under fanen **Opdateringer** skal du vælge en værdi i feltet **Plukrutestatus**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="0e6a0-118">[![Feltet Plukrutestatus for salgsordrer](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="0e6a0-119">Hvis feltet **Plukrutestatus** er angivet til **Fuldført**, sker plukprocessen automatisk som en del af processen til oprettelse af pluklister.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="0e6a0-120">Hvis feltet er angivet til **Aktiveret**, skal pluklinjerne opdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="0e6a0-121">Den samme opsætning gælder for flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="0e6a0-122">Gå til **Lagerstyring** \> **Konfiguration** \> **Parametre til lager- og lokationsstyring**, og under fanen **Transport** skal du derefter vælge en værdi i feltet **Plukrutestatus**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="0e6a0-123">[![Feltet Plukrutestatus for flytteordrer](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="0e6a0-124">Afslut udgående lagerordrer</span><span class="sxs-lookup"><span data-stu-id="0e6a0-124">End output inventory orders</span></span>

<span data-ttu-id="0e6a0-125">Gå til **Lagerstyring** \> **Konfiguration** \> **Parametre til lager- og lokationsstyring**, og angive derefter under fanen **Generelt** indstillingen **Afslut udgående lagerordre**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="0e6a0-126">[![Indstillingen Afslut udgående lagerordre](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="0e6a0-127">Når lagermedarbejderen reducerer pluklisteantallene, fjernes de tilsvarende lagerordreantal fra forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="0e6a0-128">Når pluklisten opdateres på et tidspunkt, rapporteres den resterende mængde tilbage til ordren, hvis indstillingen **Afslut udgående lagerordre** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="0e6a0-129">Hvis den **Afslut udgående lagerordre** er angivet til **Nej**, bevares de resterende mængder som et åbent udlagringsordreantal og skal føjes til en ny plukliste som en del af funktionen **Åbne udlagringsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="0e6a0-130">[![Kommandoen Åbn udlagringsordrer i menuen Funktioner](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="0e6a0-131">[![Menuen Funktioner på siden Åbne udlagringsordrer](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="0e6a0-132">Reducer antal</span><span class="sxs-lookup"><span data-stu-id="0e6a0-132">Reduce quantity</span></span>

<span data-ttu-id="0e6a0-133">Den tredje parameter, som du kan bruge som en del af processen til oprettelse af pluklister er parameteren **Reducer antal**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="0e6a0-134">Indstillingen af denne parameter bruges sammen med indstillingen **Reservation**, der udløser en reservationsproces som en del af frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="0e6a0-135">[![Parameteren Reducer antal](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="0e6a0-136">Eksempel på en udgående proces for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="0e6a0-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="0e6a0-137">I dette eksempel er der en salgsordre på to varer.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="0e6a0-138">Under pluklisteoprettelsen vælger du parameteren **Reducer antal**.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="0e6a0-139">Derfor kan du kun frigive og oprette pluklinjer for tilgængeligt disponibelt lager.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="0e6a0-140">Plukningen skal rapporteres via en registreringsproces for pluklister (**Plukrutestatus** = **Aktiveret**).</span><span class="sxs-lookup"><span data-stu-id="0e6a0-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="0e6a0-141">Det lager, der ikke allerede er reserveret, reserveres under pluklisteoprettelsen.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="0e6a0-142">Den ikke-disponible lagerbeholdning kan enten fjernet fra salgsordren eller frigives til lageret til senere udgående behandling, når lagerbeholdningen ikke er disponibel til pluk.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="0e6a0-143">[![Opdater pluklisten](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="0e6a0-144">Så snart pluklinjerne er blevet plukket på siden **Pluklisteregistrering**, fuldføres den tilknyttede forsendelse.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="0e6a0-145">Processen for følgesedler for salgsordren kan derefter initialiseres baseret på den plukkede lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="0e6a0-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="0e6a0-146">[![Opdater udgående forsendelser](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="0e6a0-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
