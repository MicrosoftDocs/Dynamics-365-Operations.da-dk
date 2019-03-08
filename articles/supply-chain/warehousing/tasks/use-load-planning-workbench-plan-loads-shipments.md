---
title: Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet
description: Denne fremgangsmåde viser, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "343897"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="d46c2-103">Planlægge laster og forsendelser ved hjælp af lastplanlægningspanelet</span><span class="sxs-lookup"><span data-stu-id="d46c2-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d46c2-104">Denne fremgangsmåde viser, hvordan lastplanlægningspanelet bruges til at oprette en belastning for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="d46c2-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="d46c2-105">Som en forudsætning skal vi skal oprette salgsordren.</span><span class="sxs-lookup"><span data-stu-id="d46c2-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="d46c2-106">Denne procedure er en del af det daglige arbejde for transportkoordinatoren.</span><span class="sxs-lookup"><span data-stu-id="d46c2-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="d46c2-107">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="d46c2-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="d46c2-108">Oprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="d46c2-108">Create a sales order</span></span>
1. <span data-ttu-id="d46c2-109">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="d46c2-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d46c2-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d46c2-110">Click New.</span></span>
3. <span data-ttu-id="d46c2-111">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d46c2-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d46c2-112">Vælg konto US-004.</span><span class="sxs-lookup"><span data-stu-id="d46c2-112">Select account US-004.</span></span>
5. <span data-ttu-id="d46c2-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d46c2-113">Click OK.</span></span>
6. <span data-ttu-id="d46c2-114">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d46c2-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d46c2-115">Vælg vare A0001.</span><span class="sxs-lookup"><span data-stu-id="d46c2-115">Select item A0001.</span></span>
    * <span data-ttu-id="d46c2-116">A0001 er aktiveret for transportstyring.</span><span class="sxs-lookup"><span data-stu-id="d46c2-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="d46c2-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d46c2-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d46c2-118">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="d46c2-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="d46c2-119">Skriv 24 i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="d46c2-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="d46c2-120">Vælg lagersted 24 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="d46c2-120">In this example select warehouse 24.</span></span> <span data-ttu-id="d46c2-121">Dette lagersted er aktiveret for transportstyring og avanceret lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="d46c2-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="d46c2-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d46c2-122">Click Save.</span></span>
12. <span data-ttu-id="d46c2-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d46c2-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="d46c2-124">Opret en ny belastning</span><span class="sxs-lookup"><span data-stu-id="d46c2-124">Create a new load</span></span>
1. <span data-ttu-id="d46c2-125">Gå til Transportstyring > Planlægning > Lastplanlægningspanel.</span><span class="sxs-lookup"><span data-stu-id="d46c2-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="d46c2-126">Klik på fanen Salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="d46c2-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="d46c2-127">Nu kan du opbygge belastningen for den salgsordre, som du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="d46c2-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="d46c2-128">Belastninger kan bygges baseret på udbud og efterspørgsel fra købsordrer, flytteordrer og salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="d46c2-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="d46c2-129">Klik på fanen Udbud og efterspørgsel i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d46c2-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="d46c2-130">Klik på Til ny last.</span><span class="sxs-lookup"><span data-stu-id="d46c2-130">Click To new load.</span></span>
5. <span data-ttu-id="d46c2-131">Klik på rullelisten i feltet Lastskabelons-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d46c2-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d46c2-132">Lastskabelonen definerer det maksimale mål for vægt og volumen af den samlede belastning.</span><span class="sxs-lookup"><span data-stu-id="d46c2-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="d46c2-133">For eksempel kan lastskabelonen repræsentere størrelsen af en container eller lastbil.</span><span class="sxs-lookup"><span data-stu-id="d46c2-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="d46c2-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d46c2-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d46c2-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d46c2-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="d46c2-136">Vurder og ruteplanlæg belastningen</span><span class="sxs-lookup"><span data-stu-id="d46c2-136">Rate and route the load</span></span>
1. <span data-ttu-id="d46c2-137">Klik på Vurdering og ruteplanlægning.</span><span class="sxs-lookup"><span data-stu-id="d46c2-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="d46c2-138">Klik på Satsrutepanel.</span><span class="sxs-lookup"><span data-stu-id="d46c2-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="d46c2-139">Klik på Satsbutik.</span><span class="sxs-lookup"><span data-stu-id="d46c2-139">Click Rate shop.</span></span>
4. <span data-ttu-id="d46c2-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d46c2-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d46c2-141">Klik på Tildel.</span><span class="sxs-lookup"><span data-stu-id="d46c2-141">Click Assign.</span></span>
6. <span data-ttu-id="d46c2-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d46c2-142">Close the page.</span></span>
7. <span data-ttu-id="d46c2-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d46c2-143">Close the page.</span></span>

