---
title: "Udgående proces"
description: "Dette emne indeholder en oversigt over den udgående proces i Lagerstyring."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: da-dk
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="3f69f-103">Udgående proces</span><span class="sxs-lookup"><span data-stu-id="3f69f-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3f69f-104">Dette emne indeholder en oversigt over den udgående proces i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="3f69f-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="3f69f-105">Udlagringsordrer</span><span class="sxs-lookup"><span data-stu-id="3f69f-105">Output orders</span></span>

<span data-ttu-id="3f69f-106">Udlagringsordrer bruges til at sammenkæde salgsordrelinjer og flytteordrelinjer med udgående plukprocesser, der bruger pluklister.</span><span class="sxs-lookup"><span data-stu-id="3f69f-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="3f69f-107">Når pluklister genereres fra enten salgsordrer eller flytteordrer, oprettes udlagringsordrer og forsendelser automatisk.</span><span class="sxs-lookup"><span data-stu-id="3f69f-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="3f69f-108">En plukliste har en en til en-relation med en forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3f69f-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="3f69f-109">Flytteordreforsendelsen eller salgsordrefølgesedlen kan behandles fra forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="3f69f-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="3f69f-110">Følgende diagram viser en oversigt over processen for udgående ordrer.</span><span class="sxs-lookup"><span data-stu-id="3f69f-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="3f69f-111">[![Oversigt over processen for udgående ordre](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="3f69f-112">Du kan konfigurere udgående regler for at definere, hvordan programmet skal håndtere den udgående proces.</span><span class="sxs-lookup"><span data-stu-id="3f69f-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="3f69f-113">Du kan bruge disse regler til at styre forsendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="3f69f-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="3f69f-114">Du kan især bruge reglerne til at styre, hvilket stadie i processen en forsendelse kan sendes under.</span><span class="sxs-lookup"><span data-stu-id="3f69f-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="3f69f-115">Følgende indstillinger definerer, hvordan udgående processer håndteres.</span><span class="sxs-lookup"><span data-stu-id="3f69f-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="3f69f-116">Status for plukrute for salgsordrer og flytteordrer</span><span class="sxs-lookup"><span data-stu-id="3f69f-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="3f69f-117">Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**, og under fanen **Opdateringer** skal du vælge en værdi i feltet **Plukrutestatus**.</span><span class="sxs-lookup"><span data-stu-id="3f69f-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="3f69f-118">[![Feltet Plukrutestatus for salgsordrer](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="3f69f-119">Hvis feltet **Plukrutestatus** er angivet til **Fuldført**, sker plukprocessen automatisk som en del af processen til oprettelse af pluklister.</span><span class="sxs-lookup"><span data-stu-id="3f69f-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="3f69f-120">Hvis feltet er angivet til **Aktiveret**, skal pluklinjerne opdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="3f69f-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="3f69f-121">Den samme opsætning gælder for flytteordrer.</span><span class="sxs-lookup"><span data-stu-id="3f69f-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="3f69f-122">Gå til **Lagerstyring** \> **Konfiguration** \> **Parametre til lager- og lokationsstyring**, og under fanen **Transport** skal du derefter vælge en værdi i feltet **Plukrutestatus**.</span><span class="sxs-lookup"><span data-stu-id="3f69f-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="3f69f-123">[![Feltet Plukrutestatus for flytteordrer](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="3f69f-124">Afslut udgående lagerordrer</span><span class="sxs-lookup"><span data-stu-id="3f69f-124">End output inventory orders</span></span>

<span data-ttu-id="3f69f-125">Gå til **Lagerstyring** \> **Konfiguration** \> **Parametre til lager- og lokationsstyring**, og angive derefter under fanen **Generelt** indstillingen **Afslut udgående lagerordre**.</span><span class="sxs-lookup"><span data-stu-id="3f69f-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="3f69f-126">[![Indstillingen Afslut udgående lagerordre](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="3f69f-127">Sommetider kan nogle varer på lageret ikke plukkes som en del af pluklisteprocessen.</span><span class="sxs-lookup"><span data-stu-id="3f69f-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="3f69f-128">Denne situation kan for eksempel opstå, hvis en lagermedarbejder reducerer antallet på pluklinjer og behandler pluklisten.</span><span class="sxs-lookup"><span data-stu-id="3f69f-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="3f69f-129">Hvis indstillingen **Afslut udgående lagerordre** er angivet til **Ja**, rapporteres de resterende uplukkede mængder tilbage til ordreniveauet.</span><span class="sxs-lookup"><span data-stu-id="3f69f-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="3f69f-130">Hvis indstillingen er angivet til **Nej**, bevares de resterende uplukkede mængder som et åbent udlagringsordreantal.</span><span class="sxs-lookup"><span data-stu-id="3f69f-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="3f69f-131">I dette tilfælde forbliver mængderne frigivet til lageret og skal føjes til en ny plukliste som en del af funktionen **Åbne udlagringsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3f69f-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="3f69f-132">[![Kommandoen Åbn udlagringsordrer i menuen Funktioner](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="3f69f-133">[![Menuen Funktioner på siden Åbne udlagringsordrer](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="3f69f-134">Reducer antal</span><span class="sxs-lookup"><span data-stu-id="3f69f-134">Reduce quantity</span></span>

<span data-ttu-id="3f69f-135">Den tredje parameter, som du kan bruge som en del af processen til oprettelse af pluklister er parameteren **Reducer antal**.</span><span class="sxs-lookup"><span data-stu-id="3f69f-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="3f69f-136">Indstillingen af denne parameter bruges sammen med indstillingen **Reservation**, der udløser en reservationsproces som en del af frigivelsen til lageret.</span><span class="sxs-lookup"><span data-stu-id="3f69f-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="3f69f-137">[![Parameteren Reducer antal](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="3f69f-138">Eksempel på en udgående proces for en salgsordre</span><span class="sxs-lookup"><span data-stu-id="3f69f-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="3f69f-139">I dette eksempel er der en salgsordre på to varer.</span><span class="sxs-lookup"><span data-stu-id="3f69f-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="3f69f-140">Under pluklisteoprettelsen vælger du parameteren **Reducer antal**.</span><span class="sxs-lookup"><span data-stu-id="3f69f-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="3f69f-141">Derfor kan du kun frigive og oprette pluklinjer for tilgængeligt disponibelt lager.</span><span class="sxs-lookup"><span data-stu-id="3f69f-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="3f69f-142">Plukningen skal rapporteres via en registreringsproces for pluklister (**Plukrutestatus** = **Aktiveret**).</span><span class="sxs-lookup"><span data-stu-id="3f69f-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="3f69f-143">Det lager, der ikke allerede er reserveret, reserveres under pluklisteoprettelsen.</span><span class="sxs-lookup"><span data-stu-id="3f69f-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="3f69f-144">Den ikke-disponible lagerbeholdning kan enten fjernet fra salgsordren eller frigives til lageret til senere udgående behandling, når lagerbeholdningen ikke er disponibel til pluk.</span><span class="sxs-lookup"><span data-stu-id="3f69f-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="3f69f-145">[![Opdater pluklisten](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="3f69f-146">Så snart pluklinjerne er blevet plukket på siden **Pluklisteregistrering**, fuldføres den tilknyttede forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3f69f-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="3f69f-147">Processen for følgesedler for salgsordren kan derefter initialiseres baseret på den plukkede lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="3f69f-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="3f69f-148">[![Opdater udgående forsendelser](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="3f69f-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

