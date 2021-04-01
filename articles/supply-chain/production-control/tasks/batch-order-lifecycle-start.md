---
title: Livscyklus for batchordre fra oprettelse til start
description: Denne procedure fører dig gennem den første del af livscyklussen for en batchordre.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67c44341b1c8633917f41fa82593ab66611ca1ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255415"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="1bc13-103">Livscyklus for batchordre fra oprettelse til start</span><span class="sxs-lookup"><span data-stu-id="1bc13-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bc13-104">Denne procedure fører dig gennem den første del af livscyklussen for en batchordre.</span><span class="sxs-lookup"><span data-stu-id="1bc13-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="1bc13-105">Fra oprettelse, forkalkulation og over planlægning af produktionsjob til den faktiske start på en batchordre.</span><span class="sxs-lookup"><span data-stu-id="1bc13-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="1bc13-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="1bc13-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="1bc13-107">Forudsætningerne for at køre proceduren med et andet datasæt er et frigivet produkt med en aktiv version af formel og rute.</span><span class="sxs-lookup"><span data-stu-id="1bc13-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="1bc13-108">Oprette en batchordre</span><span class="sxs-lookup"><span data-stu-id="1bc13-108">Create a batch order</span></span>
1. <span data-ttu-id="1bc13-109">Gå til Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="1bc13-109">Go to All production orders.</span></span>
2. <span data-ttu-id="1bc13-110">Klik på Ny batchordre.</span><span class="sxs-lookup"><span data-stu-id="1bc13-110">Click New batch order.</span></span>
3. <span data-ttu-id="1bc13-111">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="1bc13-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="1bc13-112">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="1bc13-112">Click Create.</span></span>
5. <span data-ttu-id="1bc13-113">Brug Quick Filter til at filtrere på feltet Produktion med værdien "b".</span><span class="sxs-lookup"><span data-stu-id="1bc13-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="1bc13-114">Få vist produktionsformel og forventede samprodukter</span><span class="sxs-lookup"><span data-stu-id="1bc13-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="1bc13-115">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="1bc13-116">Klik på Formel.</span><span class="sxs-lookup"><span data-stu-id="1bc13-116">Click Formula.</span></span>
3. <span data-ttu-id="1bc13-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-117">Close the page.</span></span>
4. <span data-ttu-id="1bc13-118">Klik på Ko-produkter.</span><span class="sxs-lookup"><span data-stu-id="1bc13-118">Click Co-products.</span></span>
5. <span data-ttu-id="1bc13-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="1bc13-120">Forkalkulere batchordren</span><span class="sxs-lookup"><span data-stu-id="1bc13-120">Estimate the batch order</span></span>
1. <span data-ttu-id="1bc13-121">Klik på Forkalkulation.</span><span class="sxs-lookup"><span data-stu-id="1bc13-121">Click Estimate.</span></span>
2. <span data-ttu-id="1bc13-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1bc13-122">Click OK.</span></span>
3. <span data-ttu-id="1bc13-123">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="1bc13-124">Klik på Vis beregningsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="1bc13-124">Click View calculation details.</span></span>
5. <span data-ttu-id="1bc13-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="1bc13-126">Frigive batchordren</span><span class="sxs-lookup"><span data-stu-id="1bc13-126">Release the batch order</span></span>
1. <span data-ttu-id="1bc13-127">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="1bc13-128">Klik på Frigiv.</span><span class="sxs-lookup"><span data-stu-id="1bc13-128">Click Release.</span></span>
3. <span data-ttu-id="1bc13-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1bc13-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="1bc13-130">Planlægge produktionsjob</span><span class="sxs-lookup"><span data-stu-id="1bc13-130">Schedule production jobs</span></span>
1. <span data-ttu-id="1bc13-131">Klik på Planlæg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="1bc13-132">Klik på Finplanlægge.</span><span class="sxs-lookup"><span data-stu-id="1bc13-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="1bc13-133">Vælg Nej i feltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="1bc13-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="1bc13-134">Vælg Nej i feltet Materialebegrænsning.</span><span class="sxs-lookup"><span data-stu-id="1bc13-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="1bc13-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1bc13-135">Click OK.</span></span>
6. <span data-ttu-id="1bc13-136">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="1bc13-137">Klik på Alle job.</span><span class="sxs-lookup"><span data-stu-id="1bc13-137">Click All jobs.</span></span>
8. <span data-ttu-id="1bc13-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="1bc13-139">Starte batchordren</span><span class="sxs-lookup"><span data-stu-id="1bc13-139">Start the batch order</span></span>
1. <span data-ttu-id="1bc13-140">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="1bc13-140">Click Start.</span></span>
2. <span data-ttu-id="1bc13-141">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="1bc13-141">Click the General tab.</span></span>
3. <span data-ttu-id="1bc13-142">Vælg Nej i feltet Bogfør plukliste nu.</span><span class="sxs-lookup"><span data-stu-id="1bc13-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="1bc13-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1bc13-143">Click OK.</span></span>
5. <span data-ttu-id="1bc13-144">Klik på Vis i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="1bc13-145">Klik på Plukliste.</span><span class="sxs-lookup"><span data-stu-id="1bc13-145">Click Picking list.</span></span>
7. <span data-ttu-id="1bc13-146">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1bc13-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="1bc13-147">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-147">Close the page.</span></span>
9. <span data-ttu-id="1bc13-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-148">Close the page.</span></span>
10. <span data-ttu-id="1bc13-149">Klik på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="1bc13-149">Click Route card.</span></span>
11. <span data-ttu-id="1bc13-150">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1bc13-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1bc13-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-151">Close the page.</span></span>
13. <span data-ttu-id="1bc13-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1bc13-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]