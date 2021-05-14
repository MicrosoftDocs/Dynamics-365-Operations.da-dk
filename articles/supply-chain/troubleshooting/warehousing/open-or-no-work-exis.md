---
title: Du kan ikke bekræfte en forsendelse på grund af ufuldstændig eller manglende arbejde
description: Du kan ikke bekræfte en forsendelse på grund af ufuldstændig eller manglende arbejde
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938442"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="e9f89-103">Du kan ikke bekræfte en forsendelse på grund af ufuldstændig eller manglende arbejde</span><span class="sxs-lookup"><span data-stu-id="e9f89-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="e9f89-104">Fejlkode: WAX515</span><span class="sxs-lookup"><span data-stu-id="e9f89-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="e9f89-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="e9f89-105">Symptoms</span></span>

<span data-ttu-id="e9f89-106">Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="e9f89-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="e9f89-107">Forsendelsen af lasten %1 kan ikke bekræftes, fordi alt arbejde på lasten skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="e9f89-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="e9f89-108">Du kan derfor ikke bekræfte forsendelsen for lasten.</span><span class="sxs-lookup"><span data-stu-id="e9f89-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e9f89-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="e9f89-109">Cause</span></span>

<span data-ttu-id="e9f89-110">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="e9f89-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="e9f89-111">Inden du kan bekræfte forsendelsen, skal der som minimum være udført noget arbejde med lasten, og alt arbejde skal have statussen *Lukket* eller *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="e9f89-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="e9f89-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="e9f89-112">Resolution</span></span>

<span data-ttu-id="e9f89-113">Kontrollér de relaterede salgsordrer eller flytteordrer for lasten eller forsendelsen, og kontrollér, at alt relateret arbejde er fuldført eller annulleret.</span><span class="sxs-lookup"><span data-stu-id="e9f89-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="e9f89-114">Du kan arbejde med forsendelser og last på flere sider.</span><span class="sxs-lookup"><span data-stu-id="e9f89-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="e9f89-115">Følgende underafsnit indeholder nogle få eksempler.</span><span class="sxs-lookup"><span data-stu-id="e9f89-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="e9f89-116">Side for alle laster</span><span class="sxs-lookup"><span data-stu-id="e9f89-116">All loads page</span></span>

1. <span data-ttu-id="e9f89-117">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="e9f89-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e9f89-118">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="e9f89-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e9f89-119">under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="e9f89-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="e9f89-120">Kontrollér status for hvert arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="e9f89-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="e9f89-121">Følg op på hvert arbejds-id, der ikke har statussen *Lukket* eller *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="e9f89-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="e9f89-122">Når hvert arbejds-id har statussen *Lukket* eller *Annulleret*, kan du prøve igen at bekræfte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="e9f89-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="e9f89-123">Side for alle forsendelser</span><span class="sxs-lookup"><span data-stu-id="e9f89-123">All shipments page</span></span>

1. <span data-ttu-id="e9f89-124">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="e9f89-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="e9f89-125">Vælg den forsendelse, der ikke kan bekræftes.</span><span class="sxs-lookup"><span data-stu-id="e9f89-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="e9f89-126">Vælg **Forsendelser** i gruppen **Arbejde** i handlingsruden, og vælg **Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="e9f89-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="e9f89-127">Kontrollér status for hvert arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="e9f89-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="e9f89-128">Følg op på hvert arbejds-id, der ikke har statussen *Lukket* eller *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="e9f89-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="e9f89-129">Når hvert arbejds-id har statussen *Lukket* eller *Annulleret*, kan du prøve igen at bekræfte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="e9f89-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="e9f89-130">Side for alt arbejde</span><span class="sxs-lookup"><span data-stu-id="e9f89-130">All work page</span></span>

1. <span data-ttu-id="e9f89-131">Gå til **Lagerstedsstyring \> Arbejde \> Alt arbejde**.</span><span class="sxs-lookup"><span data-stu-id="e9f89-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="e9f89-132">Vælg det arbejde for ordrenummeret, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="e9f89-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e9f89-133">I handlingsruden under fanen **Forsendelse** i gruppen **Forsendelse** skal du vælge **Bekræft forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="e9f89-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="e9f89-134">Kontrollér status for hvert arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="e9f89-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="e9f89-135">Følg op på hvert arbejds-id, der ikke har statussen *Lukket* eller *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="e9f89-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="e9f89-136">Når hvert arbejds-id har statussen *Lukket* eller *Annulleret*, kan du prøve igen at bekræfte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="e9f89-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
