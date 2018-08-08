---
title: Oprette en ny lageropbygning
description: "Denne procedure viser, hvordan du kan angiver oplysninger om placeringer på et lagersted."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 11ad27e68e8eb499b2cf8e477d3dbf51d930b736
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="aa36c-103">Oprette en ny lageropbygning</span><span class="sxs-lookup"><span data-stu-id="aa36c-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa36c-104">Denne procedure viser, hvordan du kan angiver oplysninger om placeringer på et lagersted.</span><span class="sxs-lookup"><span data-stu-id="aa36c-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="aa36c-105">Dette gælder for kun for lagersteder, der er oprettet ved hjælp af "grundlæggende lagerfunktioner" i modulet Lagerstyring, ikke for lagersteder, der er oprettet i modulet Lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="aa36c-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="aa36c-106">Du kan bruge denne procedure på demofirmaet USMF eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="aa36c-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="aa36c-107">Angiv lokalitetens standardkapacitet</span><span class="sxs-lookup"><span data-stu-id="aa36c-107">Set the default location capacity</span></span>
1. <span data-ttu-id="aa36c-108">Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="aa36c-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="aa36c-109">Klik på fanen Lokaliteter.</span><span class="sxs-lookup"><span data-stu-id="aa36c-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="aa36c-110">Angiv et tal i feltet Standardbredde.</span><span class="sxs-lookup"><span data-stu-id="aa36c-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="aa36c-111">Angiv et tal i feltet Standarddybde.</span><span class="sxs-lookup"><span data-stu-id="aa36c-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="aa36c-112">Angiv et tal i feltet Standardhøjde.</span><span class="sxs-lookup"><span data-stu-id="aa36c-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="aa36c-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="aa36c-113">Click Save.</span></span>
7. <span data-ttu-id="aa36c-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aa36c-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="aa36c-115">Definer formatet for navnet på lokaliteten</span><span class="sxs-lookup"><span data-stu-id="aa36c-115">Define the location name format</span></span>
1. <span data-ttu-id="aa36c-116">Gå til Lagerstyring > Opsætning > Lageropdeling > Lagersteder.</span><span class="sxs-lookup"><span data-stu-id="aa36c-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="aa36c-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="aa36c-117">Click New.</span></span>
3. <span data-ttu-id="aa36c-118">Skriv en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="aa36c-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="aa36c-119">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="aa36c-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="aa36c-120">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="aa36c-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="aa36c-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="aa36c-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="aa36c-122">Slå udvidelsen af sektionen Lokationsnavne til/fra.</span><span class="sxs-lookup"><span data-stu-id="aa36c-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="aa36c-123">Indstillingerne i denne sektion definerer standardformatet for navne på lokaliteter.</span><span class="sxs-lookup"><span data-stu-id="aa36c-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="aa36c-124">I vores eksempel medtager vi gangnummer, reolnummer og hyldenummer.</span><span class="sxs-lookup"><span data-stu-id="aa36c-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="aa36c-125">Du kan angive indstillingen Medtag gang til Ja.</span><span class="sxs-lookup"><span data-stu-id="aa36c-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="aa36c-126">Du kan angive indstillingen Medtag reol til Ja.</span><span class="sxs-lookup"><span data-stu-id="aa36c-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="aa36c-127">Angiv en værdi for reolen i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="aa36c-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="aa36c-128">For eksempel: -##</span><span class="sxs-lookup"><span data-stu-id="aa36c-128">For example: -##</span></span>  
11. <span data-ttu-id="aa36c-129">Du kan angive indstillingen Medtag hylde til Ja.</span><span class="sxs-lookup"><span data-stu-id="aa36c-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="aa36c-130">Angiv en værdi for hylden i feltet Format.</span><span class="sxs-lookup"><span data-stu-id="aa36c-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="aa36c-131">For eksempel: -##</span><span class="sxs-lookup"><span data-stu-id="aa36c-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="aa36c-132">Definer lagerstedslokationer</span><span class="sxs-lookup"><span data-stu-id="aa36c-132">Define warehouse locations</span></span>
1. <span data-ttu-id="aa36c-133">Klik på Lagersted i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="aa36c-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="aa36c-134">Klik på Guiden Lokation.</span><span class="sxs-lookup"><span data-stu-id="aa36c-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="aa36c-135">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-135">Click Next.</span></span>
4. <span data-ttu-id="aa36c-136">Fjern markeringen af indstillingen Forsendelsesområder</span><span class="sxs-lookup"><span data-stu-id="aa36c-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="aa36c-137">Fjern markeringen af indstillingen Bulkvarelokationer</span><span class="sxs-lookup"><span data-stu-id="aa36c-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="aa36c-138">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-138">Click Next.</span></span>
7. <span data-ttu-id="aa36c-139">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-139">Click Next.</span></span>
8. <span data-ttu-id="aa36c-140">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-140">Click Next.</span></span>
9. <span data-ttu-id="aa36c-141">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-141">Click Next.</span></span>
10. <span data-ttu-id="aa36c-142">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-142">Click Next.</span></span>
11. <span data-ttu-id="aa36c-143">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-143">Click Next.</span></span>
12. <span data-ttu-id="aa36c-144">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-144">Click Next.</span></span>
    * <span data-ttu-id="aa36c-145">Bemærk, at de fysiske dimensioner, der vises på denne side, er dem, du har angivet i starten af denne procedure.</span><span class="sxs-lookup"><span data-stu-id="aa36c-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="aa36c-146">Klik på Næste.</span><span class="sxs-lookup"><span data-stu-id="aa36c-146">Click Next.</span></span>
14. <span data-ttu-id="aa36c-147">Klik på Finish.</span><span class="sxs-lookup"><span data-stu-id="aa36c-147">Click Finish.</span></span>
15. <span data-ttu-id="aa36c-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aa36c-148">Close the page.</span></span>
16. <span data-ttu-id="aa36c-149">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="aa36c-149">Refresh the page.</span></span>

