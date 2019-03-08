---
title: Rette oplysninger om lagersproing
description: Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde for at korrigere lagersporingsoplysninger.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfe0f6995598757dcea824e1bb4f7ef8ab54a67b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "354477"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="a597a-103">Rette oplysninger om lagersproing</span><span class="sxs-lookup"><span data-stu-id="a597a-103">Correct inventory tracking information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a597a-104">Denne procedure fører dig gennem processen med at oprette og bogføre en lageroverførselskladde for at korrigere lagersporingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a597a-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="a597a-105">I dette eksempel vil vi opdatere oplysningerne for en batchstyret vare ved at ændre en forkert registreret batch til en anden batch.</span><span class="sxs-lookup"><span data-stu-id="a597a-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="a597a-106">Du kan gennemgå denne procedure i demodatafirmaet USPI eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a597a-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="a597a-107">Hvis du bruger dine egne data, skal du have en vare, der er batchaktiveret, og den må ikke være placeringsstyret.</span><span class="sxs-lookup"><span data-stu-id="a597a-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="a597a-108">Du skal også have oprettet et lagerkladdenavn for lageroverførsler.</span><span class="sxs-lookup"><span data-stu-id="a597a-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="a597a-109">Disse opgaver udføres normalt af en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="a597a-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="a597a-110">Oprette en lageroverførselskladde</span><span class="sxs-lookup"><span data-stu-id="a597a-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="a597a-111">Gå til Overfør.</span><span class="sxs-lookup"><span data-stu-id="a597a-111">Go to Transfer.</span></span>
2. <span data-ttu-id="a597a-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a597a-112">Click New.</span></span>
3. <span data-ttu-id="a597a-113">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a597a-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a597a-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a597a-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="a597a-115">Oprette journallinjer</span><span class="sxs-lookup"><span data-stu-id="a597a-115">Create journal lines</span></span>
1. <span data-ttu-id="a597a-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a597a-116">Click New.</span></span>
2. <span data-ttu-id="a597a-117">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="a597a-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a597a-118">Hvis du bruger USPI, skal du vælge vare M5003.</span><span class="sxs-lookup"><span data-stu-id="a597a-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="a597a-119">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="a597a-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="a597a-120">Klik på fanen Lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="a597a-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="a597a-121">Indtast eller vælg en værdi i feltet Batchnummer.</span><span class="sxs-lookup"><span data-stu-id="a597a-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="a597a-122">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="a597a-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="a597a-123">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="a597a-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="a597a-124">Indtast eller vælg en værdi i feltet Batchnummer.</span><span class="sxs-lookup"><span data-stu-id="a597a-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="a597a-125">Bogfør kladden</span><span class="sxs-lookup"><span data-stu-id="a597a-125">Post the journal</span></span>
1. <span data-ttu-id="a597a-126">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="a597a-126">Click Post.</span></span>
2. <span data-ttu-id="a597a-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a597a-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="a597a-128">Kontrollere sporingsoplysninger</span><span class="sxs-lookup"><span data-stu-id="a597a-128">Check tracing information</span></span>
1. <span data-ttu-id="a597a-129">Klik på lager.</span><span class="sxs-lookup"><span data-stu-id="a597a-129">Click Inventory.</span></span>
2. <span data-ttu-id="a597a-130">Klik på Spor.</span><span class="sxs-lookup"><span data-stu-id="a597a-130">Click Trace.</span></span>
3. <span data-ttu-id="a597a-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a597a-131">Click OK.</span></span>
    * <span data-ttu-id="a597a-132">Ved hjælp af disse sporingsoplysninger kan du spore, hvilken batch du rettede lageret fra.</span><span class="sxs-lookup"><span data-stu-id="a597a-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="a597a-133">Du kan også bruge siden Varesporing til at se disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a597a-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="a597a-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a597a-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="a597a-135">Kontrollere lagerposteringer</span><span class="sxs-lookup"><span data-stu-id="a597a-135">Check inventory transactions</span></span>
1. <span data-ttu-id="a597a-136">Klik på lager.</span><span class="sxs-lookup"><span data-stu-id="a597a-136">Click Inventory.</span></span>
2. <span data-ttu-id="a597a-137">Klik på Transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a597a-137">Click Transactions.</span></span>
    * <span data-ttu-id="a597a-138">Her kan du se de posteringer, der blev oprettet, da du bogførte kladden.</span><span class="sxs-lookup"><span data-stu-id="a597a-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

