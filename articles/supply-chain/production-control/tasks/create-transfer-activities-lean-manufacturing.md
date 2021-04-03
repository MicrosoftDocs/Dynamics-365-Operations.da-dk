---
title: Oprette overførselsaktiviteter for lean manufacturing
description: Opret en overførselsaktivitet for lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e3c92c5fc9cdba7c77942fae5c32d625cc939f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237912"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="24074-103">Oprette overførselsaktiviteter for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="24074-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24074-104">Opret en overførselsaktivitet for lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="24074-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="24074-105">Forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="24074-105">Prerequisites:</span></span> 

1. <span data-ttu-id="24074-106">Der skal oprettes et produktionsflowet og en version, der ikke er aktive.</span><span class="sxs-lookup"><span data-stu-id="24074-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="24074-107">Lokaliteterne fra og til lagersted skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="24074-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="24074-108">Du kan også vælge at oprette genopfyldningsarbejdscellen eller den genopfyldte arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="24074-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="24074-109">Find produktionsflowversionen</span><span class="sxs-lookup"><span data-stu-id="24074-109">Find the production flow version</span></span>
1. <span data-ttu-id="24074-110">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="24074-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="24074-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="24074-112">Bemærk, at produktionsflowet skal have en version i kladdestatus.</span><span class="sxs-lookup"><span data-stu-id="24074-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="24074-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="24074-114">Opret en ny aktivitet</span><span class="sxs-lookup"><span data-stu-id="24074-114">Create a new activity</span></span>
1. <span data-ttu-id="24074-115">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="24074-115">Click Activities.</span></span>
    * <span data-ttu-id="24074-116">Kontroller, at det valgte produktionsflow har en version i udkast, og vælg den version.</span><span class="sxs-lookup"><span data-stu-id="24074-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="24074-117">Klik på Opret ny planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="24074-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="24074-118">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="24074-118">Click Next.</span></span>
4. <span data-ttu-id="24074-119">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="24074-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="24074-120">Vælg"Overfør" i feltet Aktivitetstype.</span><span class="sxs-lookup"><span data-stu-id="24074-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="24074-121">Skriv et tal i feltet Procesantal.</span><span class="sxs-lookup"><span data-stu-id="24074-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="24074-122">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="24074-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="24074-123">Vælg arbejdscellerne.</span><span class="sxs-lookup"><span data-stu-id="24074-123">Select the Work cells</span></span>
1. <span data-ttu-id="24074-124">Klik på rullelisten i feltet Genopfyldning for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="24074-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="24074-125">Vælg en arbejdscelle for at bruge arbejdscellens udlagringslokalitet som fra-lokalitet i overførselsaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="24074-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="24074-126">Det samme kan gøres med den genopfyldte arbejdscelle, som angiver mållokaliteten for overførselsaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="24074-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="24074-127">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="24074-128">Definer lageropdateringerne</span><span class="sxs-lookup"><span data-stu-id="24074-128">Define the inventory updates</span></span>
1. <span data-ttu-id="24074-129">Vælg en indstilling i feltet Produkt.</span><span class="sxs-lookup"><span data-stu-id="24074-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="24074-130">Bemærk, at en overførsel ikke ændrer produkttypen.</span><span class="sxs-lookup"><span data-stu-id="24074-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="24074-131">Du kan overføre færdige produkter eller halvfabrikata (overførsel mellem to aktiviteter i et produktionsflow og eventuelt en kanban-proces).</span><span class="sxs-lookup"><span data-stu-id="24074-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="24074-132">Når du overfører færdige produkter, kan du vælge plukning eller modtagelse af resultaterne i en lagertransaktion.</span><span class="sxs-lookup"><span data-stu-id="24074-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="24074-133">Definer overførselslokaliteterne</span><span class="sxs-lookup"><span data-stu-id="24074-133">Define the transfer locations</span></span>
1. <span data-ttu-id="24074-134">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="24074-134">Click Next.</span></span>
2. <span data-ttu-id="24074-135">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="24074-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="24074-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="24074-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="24074-138">Klik på rullelisten i feltet Lokation for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="24074-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="24074-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="24074-140">Vælg "Afsender" i feltet Fragtet af.</span><span class="sxs-lookup"><span data-stu-id="24074-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="24074-141">Indstillingerne omfatter: Afsender - den organisation, som driver forsendelseslagerstedet, Modtager - den organisation, som driver tilgangslagerstedet, Fragtmand - en tredjepartsforhandler.</span><span class="sxs-lookup"><span data-stu-id="24074-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="24074-142">Hvis driftsorganisationen er en kreditor, kræver overførselsaktiviteten en aftale for underleverandørarbejde.</span><span class="sxs-lookup"><span data-stu-id="24074-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="24074-143">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="24074-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="24074-144">Definer aktivitetstiderne</span><span class="sxs-lookup"><span data-stu-id="24074-144">Define the activity times</span></span>
1. <span data-ttu-id="24074-145">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="24074-146">Definitionen af en Kørsel er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="24074-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="24074-147">Kørslen bruges til at beregne omkostninger og procestider for kanban-job.</span><span class="sxs-lookup"><span data-stu-id="24074-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="24074-148">Kørsler bruges ikke til at beregne kapacitetsbelastninger og forbrug, som beregnes ud fra procestid, afledt fra produktionsflowversion-opgaven.</span><span class="sxs-lookup"><span data-stu-id="24074-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="24074-149">Angiv et tal i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="24074-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="24074-150">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="24074-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="24074-151">Vælg Tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="24074-151">Select the Time unit.</span></span>
5. <span data-ttu-id="24074-152">Skriv et tal i feltet Pr. antal.</span><span class="sxs-lookup"><span data-stu-id="24074-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="24074-153">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="24074-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="24074-154">Køtider er valgfri.</span><span class="sxs-lookup"><span data-stu-id="24074-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="24074-155">Angiv et tal i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="24074-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="24074-156">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="24074-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="24074-157">Vælg Tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="24074-157">Select the Time unit.</span></span>
10. <span data-ttu-id="24074-158">Skriv et tal i feltet Pr. antal.</span><span class="sxs-lookup"><span data-stu-id="24074-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="24074-159">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="24074-159">Click Next.</span></span>
12. <span data-ttu-id="24074-160">Klik på Finish.</span><span class="sxs-lookup"><span data-stu-id="24074-160">Click Finish.</span></span>
13. <span data-ttu-id="24074-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="24074-161">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]