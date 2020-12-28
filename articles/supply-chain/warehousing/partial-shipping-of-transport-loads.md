---
title: Delvis forsendelse af en transportlast
description: Dette emne forklarer, hvordan du kan afsende en last delvist og udskyde planlægning af kapaciteten for lasten.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424510"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="61c16-103">Delvis forsendelse af en transportlast</span><span class="sxs-lookup"><span data-stu-id="61c16-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="61c16-104">Ved at oprette en delvis lastforsendelse kan du håndtere laster, hvor kapaciteten ikke kan fastslås, før alle de salgslinjer er føjet til en last.</span><span class="sxs-lookup"><span data-stu-id="61c16-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="61c16-105">Processen kan derefter afsluttes, når det nøjagtige palleantal er kendt.</span><span class="sxs-lookup"><span data-stu-id="61c16-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="61c16-106">Du behøver derfor ikke beslutte, hvilke paller der tildeles hvilken transport, indtil det øjeblik hvor en transport lastes fysisk fra det midlertidige lager.</span><span class="sxs-lookup"><span data-stu-id="61c16-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="61c16-107">Denne funktion giver et alternativ til overholdelsen af en strengere struktur, hvor du skal bestemme, hvilke paller der tildeles hvilken transport, før pluk- eller lastningsarbejdet kan oprettes.</span><span class="sxs-lookup"><span data-stu-id="61c16-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="61c16-108">I stedet kan brugere konfigurere individuelle laster til bekræftelse af en dellevering.</span><span class="sxs-lookup"><span data-stu-id="61c16-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="61c16-109">Transportens lastningsprocesser for disse laster kan derefter udføres.</span><span class="sxs-lookup"><span data-stu-id="61c16-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="61c16-110">Derfor kan afdelingen for fragtplanlægning planlægge laster uden at overveje kapaciteten for de enkelte transporter.</span><span class="sxs-lookup"><span data-stu-id="61c16-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="61c16-111">På lastningstidspunktet kan arbejdere definere en ny transportlast, som en palle kan lastes til.</span><span class="sxs-lookup"><span data-stu-id="61c16-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="61c16-112">De kan også identificere en eksisterende transportlast.</span><span class="sxs-lookup"><span data-stu-id="61c16-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="61c16-113">Disse data kan registreres via en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="61c16-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="61c16-114">Derfor kan flere lagermedarbejdere laste lagervarer fra samme laster eller forskellige laster på samme lastbil.</span><span class="sxs-lookup"><span data-stu-id="61c16-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="61c16-115">Lasterne kan derefter blive leveret helt eller delvist.</span><span class="sxs-lookup"><span data-stu-id="61c16-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="61c16-116">For at laste lager fra en last til en bestemt transportlast og delvist levere lasten, skal arbejdet genereres ved hjælp af en lastningsklasse i en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="61c16-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="61c16-117">Almindeligt plukarbejde af typen **Pluk** lastes til en transportlast som f.eks. en lastbil.</span><span class="sxs-lookup"><span data-stu-id="61c16-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="61c16-118">Konfigurere transportlast til delvis levering</span><span class="sxs-lookup"><span data-stu-id="61c16-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="61c16-119">Opsætningen af delleveringer af laster består af følgende to procedurer.</span><span class="sxs-lookup"><span data-stu-id="61c16-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="61c16-120">Konfigurere lastningsstrategi</span><span class="sxs-lookup"><span data-stu-id="61c16-120">Set the loading strategy</span></span>

<span data-ttu-id="61c16-121">Du skal aktivere delvis lastning ved at angive lastningsstrategien.</span><span class="sxs-lookup"><span data-stu-id="61c16-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="61c16-122">Når du har oprettet lastningsstrategien, efter du har oprettet en last.</span><span class="sxs-lookup"><span data-stu-id="61c16-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="61c16-123">Vælg **Lokationsstyring** \> **Laster** \> **Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="61c16-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="61c16-124">Vælg en last, og klik derefter på **Hoved**.</span><span class="sxs-lookup"><span data-stu-id="61c16-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="61c16-125">I feltet **Lastningsstrategi** skal du vælge **Afsendelse af delvis last er tilladt**.</span><span class="sxs-lookup"><span data-stu-id="61c16-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="61c16-126">Oprette et menupunkt til lastning af transportlaster</span><span class="sxs-lookup"><span data-stu-id="61c16-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="61c16-127">Du skal oprette et nyt menupunkt, der muliggør lastning af transportlaster.</span><span class="sxs-lookup"><span data-stu-id="61c16-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="61c16-128">En transportlast gør det muligt at gruppere arbejdslinjer fra en eller flere laster.</span><span class="sxs-lookup"><span data-stu-id="61c16-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="61c16-129">Alt, der føjes til transportlasten, kan derefter afsendes ved hjælp af en mobil scanner.</span><span class="sxs-lookup"><span data-stu-id="61c16-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="61c16-130">Vælg **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="61c16-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="61c16-131">Vælg **Ny**, og i feltet **Tilstand** skal du derefter vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="61c16-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="61c16-132">Angiv indstillingen **Brug eksisterende arbejde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="61c16-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="61c16-133">På fanen **Generelt** i feltet **Ledet af** skal du vælge **Lastning af transport**.</span><span class="sxs-lookup"><span data-stu-id="61c16-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="61c16-134">For at muliggøre bekræftelse af en forsendelse på en mobil scanner skal du åbne feltet **Tilladt type for bekræftelse af afsendelse** og vælge **Transportlast**.</span><span class="sxs-lookup"><span data-stu-id="61c16-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="61c16-135">Bekræfte afsendelse af en transportlast fra klienten</span><span class="sxs-lookup"><span data-stu-id="61c16-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="61c16-136">Denne opsætning gør det muligt at bekræfte en transportlast, der omfatter en fuld last eller en delvist lastet last, der skal afsendes.</span><span class="sxs-lookup"><span data-stu-id="61c16-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="61c16-137">Vælg **Lokationsstyring** \> **Laster** \> **Transportlaster**.</span><span class="sxs-lookup"><span data-stu-id="61c16-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="61c16-138">I handlingsruden på fanen **Lever og modtag**, i gruppen **Bekræft** skal du vælge **Transport**.</span><span class="sxs-lookup"><span data-stu-id="61c16-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
