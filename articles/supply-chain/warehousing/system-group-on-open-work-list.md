---
title: "Systemgruppering på en åben opgaveliste"
description: "Dette emne beskriver, hvordan du filtrerer oversigten over åbne opgaver på en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="ed5af-103">Systemgruppering på en åben opgaveliste</span><span class="sxs-lookup"><span data-stu-id="ed5af-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ed5af-104">Ved hjælp af et felt til systemgruppering kan du filtrere en oversigt over åbne opgaver uden at skulle redigere menupunktet for mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="ed5af-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="ed5af-105">Hvis det er relevant, fungerer systemgruppering til filtrering af en opgaveliste på et enkelt felt med opgaveoverskrift.</span><span class="sxs-lookup"><span data-stu-id="ed5af-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="ed5af-106">Du kan ikke bruge systemgruppering til at filtrere online feltniveauer.</span><span class="sxs-lookup"><span data-stu-id="ed5af-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="ed5af-107">Konfigurere systemgruppering på en oversigt over åbent arbejde</span><span class="sxs-lookup"><span data-stu-id="ed5af-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="ed5af-108">Brug disse trin til at konfigurere systemgruppering på en oversigt over åbent arbejde.</span><span class="sxs-lookup"><span data-stu-id="ed5af-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="ed5af-109">Vælg et menupunkt på en mobilenhed, vælg **Tilstand: indirekte** og **Aktivitetskode: Vis oversigt over åbent arbejde**.</span><span class="sxs-lookup"><span data-stu-id="ed5af-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="ed5af-110">Følgende valgmuligheder bliver tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="ed5af-110">The following options become available.</span></span> <span data-ttu-id="ed5af-111">Disse indstillinger er påkrævet for systemgruppering på en oversigt over åbent arbejde.</span><span class="sxs-lookup"><span data-stu-id="ed5af-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="ed5af-112">Indstilling</span><span class="sxs-lookup"><span data-stu-id="ed5af-112">Option</span></span>        | <span data-ttu-id="ed5af-113">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="ed5af-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="ed5af-114">Tillad systemgruppering</span><span class="sxs-lookup"><span data-stu-id="ed5af-114">Allow system grouping</span></span>   | <span data-ttu-id="ed5af-115">Aktiverer systemgruppering for et valgt menupunkt på arbejdslisten.</span><span class="sxs-lookup"><span data-stu-id="ed5af-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="ed5af-116">Systemgrupperingsfelt</span><span class="sxs-lookup"><span data-stu-id="ed5af-116">System grouping field</span></span>   | <span data-ttu-id="ed5af-117">Kun tilgængelig, hvis **Tillad systemarbejde** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ed5af-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="ed5af-118">Markér det felt, der bestemmer, hvordan plukkearbejde grupperes for arbejdere.</span><span class="sxs-lookup"><span data-stu-id="ed5af-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="ed5af-119">Hvis du f.eks. vælger feltet **ShipmentId**, scanner arbejderen forsendelses-id for at gruppere plukkearbejdet.</span><span class="sxs-lookup"><span data-stu-id="ed5af-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="ed5af-120">Alt arbejde for forsendelsen knyttes derefter til arbejderen.</span><span class="sxs-lookup"><span data-stu-id="ed5af-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="ed5af-121">Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet.</span><span class="sxs-lookup"><span data-stu-id="ed5af-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="ed5af-122">Brug feltet **Systemgrupperingslabel** til at informere arbejderen, hvad der skal scannes.</span><span class="sxs-lookup"><span data-stu-id="ed5af-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="ed5af-123">Systemgrupperingslabel</span><span class="sxs-lookup"><span data-stu-id="ed5af-123">System grouping label</span></span>   | <span data-ttu-id="ed5af-124">Kun tilgængelig, hvis **Tillad systemarbejde** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ed5af-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="ed5af-125">Angiv oplysninger arbejderen om, hvad der skal scannes, når plukkearbejde er grupperet.</span><span class="sxs-lookup"><span data-stu-id="ed5af-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="ed5af-126">Hvis du f.eks. bruger feltet **ShipmentId** til at gruppere plukkearbejde efter forsendelse, kan du skrive Forsendelses-id i feltet.</span><span class="sxs-lookup"><span data-stu-id="ed5af-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="ed5af-127">Dette felt kræver, at du opretter et menupunkt, der bruger eksisterende arbejde, der er grupperet af systemet.</span><span class="sxs-lookup"><span data-stu-id="ed5af-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="ed5af-128">Du skal også vælge det felt, der skal grupperes efter, i feltet **Systemgruppering**.</span><span class="sxs-lookup"><span data-stu-id="ed5af-128">You must also select the field to group by in the **System grouping** field.</span></span>|

