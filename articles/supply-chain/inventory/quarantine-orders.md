---
title: Karantæneordrer
description: Dette emne beskriver, hvordan du bruger karantæneordrer til at blokere lagerbeholdning.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956176"
---
# <a name="quarantine-orders"></a><span data-ttu-id="bb633-103">Karantæneordrer</span><span class="sxs-lookup"><span data-stu-id="bb633-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb633-104">Dette emne beskriver, hvordan du bruger karantæneordrer til at blokere lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="bb633-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="bb633-105">Du kan blokere lagerbeholdning ved hjælp af karantæneordrer.</span><span class="sxs-lookup"><span data-stu-id="bb633-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="bb633-106">Det kan f.eks. være, at du vil sætte varer i karantæne af kvalitetskontrolmæssige årsager.</span><span class="sxs-lookup"><span data-stu-id="bb633-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="bb633-107">Lager, der er blevet sat i karantæne, overføres til et karantænelagersted.</span><span class="sxs-lookup"><span data-stu-id="bb633-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="bb633-108">Hvis du anvender avancerede lagerstyringsprocesser (i Lagerstedsstyring), bruges karantæneordrebehandling kun til retursalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="bb633-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="bb633-109">Sæt disponible lagervarer i karantæne</span><span class="sxs-lookup"><span data-stu-id="bb633-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="bb633-110">Når du sætter varer i karantæne, kan du enten oprette karantæneordrerne manuelt eller definere, at systemet skal oprette dem automatisk under indgående behandling.</span><span class="sxs-lookup"><span data-stu-id="bb633-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="bb633-111">Benyt følgende fremgangsmåde, hvis du vil konfigurere systemet til automatisk at generere karantæneordrer.</span><span class="sxs-lookup"><span data-stu-id="bb633-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="bb633-112">Gå til **Lagerstyring \> Opsætning \> Lagerbeholdning \> Varemodelgrupper**.</span><span class="sxs-lookup"><span data-stu-id="bb633-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="bb633-113">Vælg en relevant modelgruppe i listeruden, eller opret en ny modelgruppe.</span><span class="sxs-lookup"><span data-stu-id="bb633-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="bb633-114">I oversigtspanelet **Lagerpolitikker** skal du markere afkrydsningsfeltet **Karatænestyring**.</span><span class="sxs-lookup"><span data-stu-id="bb633-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="bb633-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bb633-115">Close the page.</span></span>
1. <span data-ttu-id="bb633-116">Du skal angive et standardlagersted for karantænen i feltet **Karantænelagersted** for de modtagende lagersteder.</span><span class="sxs-lookup"><span data-stu-id="bb633-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="bb633-117">Når en vare, der er registreret som modtaget på lagerstedet, tilhører en modelgruppe, hvor afkrydsningsfeltet **Karantænestyring** er markeret, genererer systemet en karantæneordre for den.</span><span class="sxs-lookup"><span data-stu-id="bb633-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="bb633-118">Karantæneordren beder arbejderne om at flytte varen til karantænelagerstedet.</span><span class="sxs-lookup"><span data-stu-id="bb633-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="bb633-119">Når du opretter karantæneordrer manuelt på siden **Karantæneordrer**, behøver varen ikke at være indstillet til karantænestyring i den tilknyttede varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="bb633-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="bb633-120">For denne proces skal du angive den disponible lagerbeholdning, der skulle sættes i karantæne, og det karantænelagersted, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="bb633-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="bb633-121">Du kan bruge karantæneordrestatusser til at planlægge processen.</span><span class="sxs-lookup"><span data-stu-id="bb633-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="bb633-122">Karantæneordrens status</span><span class="sxs-lookup"><span data-stu-id="bb633-122">Quarantine order statuses</span></span>

<span data-ttu-id="bb633-123">Karantæneordrer kan have følgende statusværdier:</span><span class="sxs-lookup"><span data-stu-id="bb633-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="bb633-124">Oprettet</span><span class="sxs-lookup"><span data-stu-id="bb633-124">Created</span></span>
- <span data-ttu-id="bb633-125">Startet</span><span class="sxs-lookup"><span data-stu-id="bb633-125">Started</span></span>
- <span data-ttu-id="bb633-126">Færdigmeldt</span><span class="sxs-lookup"><span data-stu-id="bb633-126">Reported as finished</span></span>
- <span data-ttu-id="bb633-127">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="bb633-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="bb633-128">Oprettet</span><span class="sxs-lookup"><span data-stu-id="bb633-128">Created</span></span>

<span data-ttu-id="bb633-129">Når en karantæneordre er oprettet manuelt, men varen endnu ikke er på karantænelagerstedet, har karantæneordren statussen **Oprettet**.</span><span class="sxs-lookup"><span data-stu-id="bb633-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="bb633-130">Der oprettes to lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="bb633-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="bb633-131">Én transaktion er en afgangspostering, der kan have statussen **I bestilling**, **Reserveret fysisk** eller **Plukket**.</span><span class="sxs-lookup"><span data-stu-id="bb633-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="bb633-132">Den anden transaktion er en tilgangspostering, der kan have statussen **Bestilt** eller **Registreret** på karantænelagerstedet.</span><span class="sxs-lookup"><span data-stu-id="bb633-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="bb633-133">Du kan reservere, plukke og registrere opdateringer til lageret ved hjælp af de sædvanlige processer.</span><span class="sxs-lookup"><span data-stu-id="bb633-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="bb633-134">Startet</span><span class="sxs-lookup"><span data-stu-id="bb633-134">Started</span></span>

<span data-ttu-id="bb633-135">Når en karantæneordren har statussen **Startet**, overføres lageret fra det almindelige lagersted til karantænelagerstedet, og der genereres to lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="bb633-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="bb633-136">Den ene postering har statussen **Trukket**, og den anden postering har statussen **Modtaget**.</span><span class="sxs-lookup"><span data-stu-id="bb633-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="bb633-137">Samtidig oprettes der to lagertransaktioner til håndtering af tilbageflytningen.</span><span class="sxs-lookup"><span data-stu-id="bb633-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="bb633-138">Disse transaktioner dateres ikke.</span><span class="sxs-lookup"><span data-stu-id="bb633-138">These transactions aren't dated.</span></span> <span data-ttu-id="bb633-139">Den ene postering har statussen **Reserveret fysisk**, og den anden postering har statussen **Bestilt**.</span><span class="sxs-lookup"><span data-stu-id="bb633-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="bb633-140">Færdigmeldt</span><span class="sxs-lookup"><span data-stu-id="bb633-140">Reported as finished</span></span>

<span data-ttu-id="bb633-141">Hvis du vil færdigmelde en igangsat karantæneordre, skal du åbne ordren og vælge **Færdigmeld** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="bb633-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="bb633-142">Varen frigives fra karantæne, men den er endnu ikke flyttet tilbage til det almindelige lagersted.</span><span class="sxs-lookup"><span data-stu-id="bb633-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="bb633-143">Flytningen tilbage til det almindelige lagersted kan behandles via en varemodtagelseskladde, som kan initialiseres under færdigmeldingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="bb633-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="bb633-144">Afsluttet</span><span class="sxs-lookup"><span data-stu-id="bb633-144">Ended</span></span>

<span data-ttu-id="bb633-145">Når en karantæneordre afsluttes, flyttes varen fra karantænelagerstedet tilbage til det almindelige lagersted.</span><span class="sxs-lookup"><span data-stu-id="bb633-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="bb633-146">Status for varebevægelsen er angivet til *Solgt* på karantænelagerstedet og *Købt* på det almindelige lagersted.</span><span class="sxs-lookup"><span data-stu-id="bb633-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="bb633-147">Kassering af karantæneordre</span><span class="sxs-lookup"><span data-stu-id="bb633-147">Quarantine order scrap</span></span>

<span data-ttu-id="bb633-148">Du kan kassere lageret som en del af karantæneordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="bb633-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="bb633-149">Når du behandler en kassering, indstilles lagerstatus til *Solgt* med en afgangstransaktion fra karantænelagerstedet.</span><span class="sxs-lookup"><span data-stu-id="bb633-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb633-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bb633-150">Additional resources</span></span>

- [<span data-ttu-id="bb633-151">Lagerblokering</span><span class="sxs-lookup"><span data-stu-id="bb633-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
