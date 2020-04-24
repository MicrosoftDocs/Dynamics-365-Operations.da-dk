---
title: Oprette procesaktiviteter for lean manufacturing
description: Opret et procesaktivitet til lean manufacturing.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc93f3f696f470d7e2f174bd3342f0877e0b4e74
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212152"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="75468-103">Oprette procesaktiviteter for lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="75468-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75468-104">Opret et procesaktivitet til lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="75468-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="75468-105">Forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="75468-105">Prerequisites:</span></span> 

1. <span data-ttu-id="75468-106">Der skal oprettes et produktionsflowet og en version, der ikke er aktive.</span><span class="sxs-lookup"><span data-stu-id="75468-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="75468-107">Der skal oprettes en arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="75468-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="75468-108">Find produktionsflowversionen</span><span class="sxs-lookup"><span data-stu-id="75468-108">Find the production flow version</span></span>
1. <span data-ttu-id="75468-109">Gå til Produktionsstyring > Opsætning > Lean produktionsflow > Produktionsflow.</span><span class="sxs-lookup"><span data-stu-id="75468-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="75468-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="75468-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="75468-112">Opret en ny aktivitet</span><span class="sxs-lookup"><span data-stu-id="75468-112">Create a new activity</span></span>
1. <span data-ttu-id="75468-113">Klik på Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="75468-113">Click Activities.</span></span>
    * <span data-ttu-id="75468-114">Kontroller, at det valgte produktionsflow har en version i udkast, og vælg den version.</span><span class="sxs-lookup"><span data-stu-id="75468-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="75468-115">Klik på Opret ny planaktivitet.</span><span class="sxs-lookup"><span data-stu-id="75468-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="75468-116">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="75468-116">Click Next.</span></span>
4. <span data-ttu-id="75468-117">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="75468-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="75468-118">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="75468-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="75468-119">Bemærk, at navnet skal være entydigt for et givet produktionsflow for alle versioner.</span><span class="sxs-lookup"><span data-stu-id="75468-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="75468-120">Skriv et tal i feltet Procesantal.</span><span class="sxs-lookup"><span data-stu-id="75468-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="75468-121">Bemærk, at uanset hvilket antal af job der skal behandles, er dette minimumantal pr. job til at beregne arbejdsomkostning.</span><span class="sxs-lookup"><span data-stu-id="75468-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="75468-122">Hvis jobantal afviger fra dette antal, oprettes arbejdsomkostningsafvigelse.</span><span class="sxs-lookup"><span data-stu-id="75468-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="75468-123">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="75468-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="75468-124">Vælg arbejdscellen</span><span class="sxs-lookup"><span data-stu-id="75468-124">Select the work cell</span></span>
1. <span data-ttu-id="75468-125">Klik på rullelisten i feltet Arbejdscelle for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="75468-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="75468-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="75468-127">Definer lageropdateringerne</span><span class="sxs-lookup"><span data-stu-id="75468-127">Define the inventory updates</span></span>
1. <span data-ttu-id="75468-128">Marker eller fjern opdateringen i afkrydsningsfeltet Opdater lagertilgang.</span><span class="sxs-lookup"><span data-stu-id="75468-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="75468-129">Hvis Opdater lagerbeholdning = Nej, kan du definere aktiviteten for at modtage et halvfabrikataprodukt (aktiviteten ikke når op på det næste niveau i Styklisten).</span><span class="sxs-lookup"><span data-stu-id="75468-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="75468-130">Du kan også vælge for at forbruge halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="75468-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="75468-131">Definer plukaktiviteterne</span><span class="sxs-lookup"><span data-stu-id="75468-131">Define the picking activities</span></span>
1. <span data-ttu-id="75468-132">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="75468-132">Click Next.</span></span>
2. <span data-ttu-id="75468-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="75468-134">Der oprettes en standardplukaktiviteten for indlagringslokation af den valgte arbejdscelle.</span><span class="sxs-lookup"><span data-stu-id="75468-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="75468-135">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="75468-135">Click Add.</span></span>
    * <span data-ttu-id="75468-136">Du kan oprette yderligere plukaktiviteter for specifikke produkter, der ikke opbevares på arbejdscellens inputaktivitet.</span><span class="sxs-lookup"><span data-stu-id="75468-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="75468-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="75468-138">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="75468-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="75468-139">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="75468-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="75468-140">Med denne definition plukkes alle materialer, der forbruges i aktiviteten, fra standardinputlagerstedet og lokaliteten med undtagelse af den vare, der er defineret i den anden plukaktivitet.</span><span class="sxs-lookup"><span data-stu-id="75468-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="75468-141">Dette element vil blive plukket fra et andet lagersted og en anden lokalitet.</span><span class="sxs-lookup"><span data-stu-id="75468-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="75468-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="75468-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="75468-144">Vælg eller fjern markeringen i afkrydsningsfeltet Registrer spild.</span><span class="sxs-lookup"><span data-stu-id="75468-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="75468-145">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="75468-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="75468-146">Definer aktivitetstiderne</span><span class="sxs-lookup"><span data-stu-id="75468-146">Define the activity times</span></span>
1. <span data-ttu-id="75468-147">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="75468-148">Definitionen af en Kørsel er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="75468-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="75468-149">Kørslen bruges til at beregne omkostninger og procestider for kanban-job.</span><span class="sxs-lookup"><span data-stu-id="75468-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="75468-150">Kørsler bruges ikke til at beregne kapacitetsbelastninger og forbrug, som beregnes ud fra procestid, afledt fra produktionsflowversion-opgaven.</span><span class="sxs-lookup"><span data-stu-id="75468-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="75468-151">Angiv et tal i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="75468-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="75468-152">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="75468-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="75468-153">Vælg Tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="75468-153">Select the Time unit.</span></span>
5. <span data-ttu-id="75468-154">Skriv et tal i feltet Pr. antal.</span><span class="sxs-lookup"><span data-stu-id="75468-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="75468-155">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75468-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="75468-156">Køtider er valgfri.</span><span class="sxs-lookup"><span data-stu-id="75468-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="75468-157">Angiv et tal i feltet Tid.</span><span class="sxs-lookup"><span data-stu-id="75468-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="75468-158">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="75468-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="75468-159">Vælg Tidsenhed.</span><span class="sxs-lookup"><span data-stu-id="75468-159">Select the Time unit.</span></span>
10. <span data-ttu-id="75468-160">Skriv et tal i feltet Pr. antal.</span><span class="sxs-lookup"><span data-stu-id="75468-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="75468-161">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="75468-161">Click Next.</span></span>
12. <span data-ttu-id="75468-162">Klik på Finish.</span><span class="sxs-lookup"><span data-stu-id="75468-162">Click Finish.</span></span>
13. <span data-ttu-id="75468-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="75468-163">Close the page.</span></span>

