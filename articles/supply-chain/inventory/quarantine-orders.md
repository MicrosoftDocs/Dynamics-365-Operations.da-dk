---
title: "Karantæneordrer"
description: "I dette emne beskrives, hvordan karantæneordrer bruges til at blokere for lager."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 7cb0463d386081084e6c1367cc0265f3083df583
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="quarantine-orders"></a><span data-ttu-id="85c01-103">Karantæneordrer</span><span class="sxs-lookup"><span data-stu-id="85c01-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="85c01-104">I dette emne beskrives, hvordan karantæneordrer bruges til at blokere for lager.</span><span class="sxs-lookup"><span data-stu-id="85c01-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="85c01-105">Karantæneordrer kan bruges til at blokere lager.</span><span class="sxs-lookup"><span data-stu-id="85c01-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="85c01-106">Det kan f.eks. være, at du vil sætte varer i karantæne af kvalitetskontrolmæssige årsager.</span><span class="sxs-lookup"><span data-stu-id="85c01-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="85c01-107">Lager, der er blevet sat i karantæne, overføres til et karantænelagersted.</span><span class="sxs-lookup"><span data-stu-id="85c01-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="85c01-108">**Bemærk!** Hvis du anvender avancerede lagerstyringsprocesser (i Lagerstedsstyring), bruges karantæneordrebehandling kun til retursalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="85c01-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="85c01-109">Sæt disponible lagervarer i karantæne</span><span class="sxs-lookup"><span data-stu-id="85c01-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="85c01-110">Når du sætter varer i karantæne, kan du enten oprette karantæneordrerne manuelt eller definere, at systemet skal oprette karantæneordrer automatisk under indgående behandling.</span><span class="sxs-lookup"><span data-stu-id="85c01-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="85c01-111">Du kan oprette karantæneordrer automatisk ved at vælge indstillingen **Karantænestyring** under fanen **Lagerpolitikker** på siden **Varemodelgrupper**.</span><span class="sxs-lookup"><span data-stu-id="85c01-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="85c01-112">Du skal også angive et standardkarantænelagersted i feltet **Karantænelagersted** for de modtagende lagersteder.</span><span class="sxs-lookup"><span data-stu-id="85c01-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="85c01-113">Når den fysisk disponible lagerbeholdning bliver registreret i en indkøbsordre eller produktionsordre, flyttes varerne i karantæne automatisk til et karantænelagersted i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85c01-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="85c01-114">Denne bevægelse opstår, fordi status for karantæneordren ændres til **Startet**.</span><span class="sxs-lookup"><span data-stu-id="85c01-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="85c01-115">Når du opretter karantæneordrer manuelt, behøver varen ikke at være sat op til karantænestyring i den tilknyttede varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="85c01-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="85c01-116">For denne proces skal du angive den disponible lagerbeholdning, der skulle sættes i karantæne, og det karantænelagersted, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="85c01-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="85c01-117">Du kan bruge karantæneordrestatusser til at planlægge processen.</span><span class="sxs-lookup"><span data-stu-id="85c01-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="85c01-118">Karantæneordrens status</span><span class="sxs-lookup"><span data-stu-id="85c01-118">Quarantine order statuses</span></span>
<span data-ttu-id="85c01-119">Karantæneordrer kan have følgende statusværdier:</span><span class="sxs-lookup"><span data-stu-id="85c01-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="85c01-120">Oprettet</span><span class="sxs-lookup"><span data-stu-id="85c01-120">Created</span></span>
-   <span data-ttu-id="85c01-121">Startet</span><span class="sxs-lookup"><span data-stu-id="85c01-121">Started</span></span>
-   <span data-ttu-id="85c01-122">Færdigmeldt</span><span class="sxs-lookup"><span data-stu-id="85c01-122">Reported as finished</span></span>
-   <span data-ttu-id="85c01-123">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="85c01-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="85c01-124">Oprettet</span><span class="sxs-lookup"><span data-stu-id="85c01-124">Created</span></span>

<span data-ttu-id="85c01-125">Når en karantæneordre er oprettet manuelt, men varen endnu ikke er på karantænelagerstedet, har karantæneordren statussen **Oprettet**.</span><span class="sxs-lookup"><span data-stu-id="85c01-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="85c01-126">Der oprettes to lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="85c01-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="85c01-127">Én transaktion er en afgangspostering, der kan have statussen **I bestilling**, **Reserveret fysisk** eller **Plukket**.</span><span class="sxs-lookup"><span data-stu-id="85c01-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="85c01-128">Den anden transaktion er en tilgangspostering, der kan have statussen **Bestilt** eller **Registreret** på karantænelagerstedet.</span><span class="sxs-lookup"><span data-stu-id="85c01-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="85c01-129">Du kan reservere, plukke og registrere opdateringer til lageret ved hjælp af de sædvanlige processer.</span><span class="sxs-lookup"><span data-stu-id="85c01-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="85c01-130">Startet</span><span class="sxs-lookup"><span data-stu-id="85c01-130">Started</span></span>

<span data-ttu-id="85c01-131">Når en karantæneordren har statussen **Startet**, overføres lageret fra det almindelige lagersted til karantænelagerstedet, og der genereres to lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="85c01-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="85c01-132">Den ene postering har statussen **Trukket**, og den anden postering har statussen **Modtaget**.</span><span class="sxs-lookup"><span data-stu-id="85c01-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="85c01-133">Samtidig oprettes der to lagertransaktioner til håndtering af tilbageflytningen.</span><span class="sxs-lookup"><span data-stu-id="85c01-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="85c01-134">Disse transaktioner dateres ikke.</span><span class="sxs-lookup"><span data-stu-id="85c01-134">These transactions aren't dated.</span></span> <span data-ttu-id="85c01-135">Den ene postering har statussen **Reserveret fysisk**, og den anden postering har statussen **Bestilt**.</span><span class="sxs-lookup"><span data-stu-id="85c01-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="85c01-136">Færdigmeldt</span><span class="sxs-lookup"><span data-stu-id="85c01-136">Reported as finished</span></span>

<span data-ttu-id="85c01-137">Hvis du klikker på **Færdigmeld**, kan du færdigmelde en igangsat karantæneordre.</span><span class="sxs-lookup"><span data-stu-id="85c01-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="85c01-138">Varen frigives fra karantæne, men den er endnu ikke flyttet tilbage til det almindelige lagersted.</span><span class="sxs-lookup"><span data-stu-id="85c01-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="85c01-139">Flytningen tilbage til det almindelige lagersted kan behandles via en varemodtagelseskladde, som kan initialiseres under færdigmeldingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="85c01-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="85c01-140">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="85c01-140">Ended</span></span>

<span data-ttu-id="85c01-141">Når en karantæneordre afsluttes, flyttes varen fra karantænelagerstedet tilbage til det almindelige lagersted.</span><span class="sxs-lookup"><span data-stu-id="85c01-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="85c01-142">Status for varebevægelsen er angivet til **Solgt** på karantænelagerstedet og **Købt** på det almindelige lagersted.</span><span class="sxs-lookup"><span data-stu-id="85c01-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="85c01-143">Kassering af karantæneordre</span><span class="sxs-lookup"><span data-stu-id="85c01-143">Quarantine order scrap</span></span>
<span data-ttu-id="85c01-144">Du kan kassere lageret som en del af karantæneordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="85c01-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="85c01-145">Når du behandler en kassering, indstilles lagerstatus til **Solgt** med en afgangspostering fra karantænelagerstedet.</span><span class="sxs-lookup"><span data-stu-id="85c01-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="85c01-146">Se også</span><span class="sxs-lookup"><span data-stu-id="85c01-146">See also</span></span>
--------

[<span data-ttu-id="85c01-147">Lagerspærring</span><span class="sxs-lookup"><span data-stu-id="85c01-147">Inventory blocking</span></span>](inventory-blocking.md)

