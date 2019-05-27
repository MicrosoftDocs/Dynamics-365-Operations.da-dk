---
title: Oprette en operationsressource
description: En operationsressource udfører aktiviteterne i et projekt eller en produktionsproces.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9d8f13e29ea813eb9721ddca795b67837e2aa5e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558143"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="d0456-103">Oprette en operationsressource</span><span class="sxs-lookup"><span data-stu-id="d0456-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0456-104">En operationsressource udfører aktiviteterne i et projekt eller en produktionsproces.</span><span class="sxs-lookup"><span data-stu-id="d0456-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="d0456-105">Denne procedure viser, hvordan du definerer en operationsressource.</span><span class="sxs-lookup"><span data-stu-id="d0456-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="d0456-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d0456-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d0456-107">Gå til ressourcer.</span><span class="sxs-lookup"><span data-stu-id="d0456-107">Go to Resources.</span></span>
2. <span data-ttu-id="d0456-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d0456-108">Click New.</span></span>
3. <span data-ttu-id="d0456-109">Skriv en værdi i feltet Ressource.</span><span class="sxs-lookup"><span data-stu-id="d0456-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="d0456-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d0456-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="d0456-111">Definere kapacitets- og forbrugsparametre</span><span class="sxs-lookup"><span data-stu-id="d0456-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="d0456-112">Udvid sektionen Handling.</span><span class="sxs-lookup"><span data-stu-id="d0456-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="d0456-113">Angiv et tal i feltet Spildprocent.</span><span class="sxs-lookup"><span data-stu-id="d0456-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="d0456-114">Indtast eller vælg en værdi i feltet Opstillingsart.</span><span class="sxs-lookup"><span data-stu-id="d0456-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="d0456-115">Angiv den omkostningsart, der definerer, hvordan der tages højde for omkostning til opstilling.</span><span class="sxs-lookup"><span data-stu-id="d0456-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="d0456-116">Indtast eller vælg en værdi i feltet procestidsart.</span><span class="sxs-lookup"><span data-stu-id="d0456-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="d0456-117">Angiv den omkostningsart, der definerer, hvordan der tages højde for omkostning til procestid.</span><span class="sxs-lookup"><span data-stu-id="d0456-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="d0456-118">Indtast eller vælg en værdi i feltet Antalsart.</span><span class="sxs-lookup"><span data-stu-id="d0456-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="d0456-119">Angiv omkostningsarten, der definerer, hvordan der tages højde for ressourceomkostninger baseret på output-antal.</span><span class="sxs-lookup"><span data-stu-id="d0456-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="d0456-120">Vælg en indstilling i feltet Kapacitetsenhed.</span><span class="sxs-lookup"><span data-stu-id="d0456-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="d0456-121">Angiv den enhed, som kapaciteten af operationsressourcen udtrykkes i.</span><span class="sxs-lookup"><span data-stu-id="d0456-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="d0456-122">Indtast et tal i feltet Kapacitet.</span><span class="sxs-lookup"><span data-stu-id="d0456-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="d0456-123">Indtast et tal i feltet Effektivitetsprocent.</span><span class="sxs-lookup"><span data-stu-id="d0456-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="d0456-124">Angiv den effektivitet, du forventer af operationsressourcen.</span><span class="sxs-lookup"><span data-stu-id="d0456-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="d0456-125">Effektivitetsprocenten justerer operationsressourcens gennemløb og påvirker den tid, der er afsat til ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d0456-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="d0456-126">Angiv et tal i feltet Grovplanlægningsprocent.</span><span class="sxs-lookup"><span data-stu-id="d0456-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="d0456-127">Angiv den maksimale procent af kapaciteten af den operationsressource, som du vil bruge til grovplanlægning.</span><span class="sxs-lookup"><span data-stu-id="d0456-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="d0456-128">Vælg Ja i feltet Kapacitetsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="d0456-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="d0456-129">Angiv denne indstilling til Ja, hvis operationsressourcen skal planlægges ud fra den faktiske kapacitet, der er tilgængelig, og om der skal tages hensyn til eksisterende kapacitetsreservationer.</span><span class="sxs-lookup"><span data-stu-id="d0456-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="d0456-130">Hvis denne indstilling er angivet til Nej, antages operationsressourcen at have ubegrænset kapacitet, og ressourcen kan være overbooket.</span><span class="sxs-lookup"><span data-stu-id="d0456-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="d0456-131">Vælg Ja i feltet Flaskehalsressource.</span><span class="sxs-lookup"><span data-stu-id="d0456-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="d0456-132">Definere arbejdstider</span><span class="sxs-lookup"><span data-stu-id="d0456-132">Define working times</span></span>
1. <span data-ttu-id="d0456-133">Udvid sektionen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="d0456-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="d0456-134">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d0456-134">Click Add.</span></span>
3. <span data-ttu-id="d0456-135">Indtast eller vælg en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="d0456-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="d0456-136">Angiv den arbejdstidskalender, der definerer ressourcens kapacitet (i timer).</span><span class="sxs-lookup"><span data-stu-id="d0456-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="d0456-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d0456-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d0456-138">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d0456-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="d0456-139">Definere ressourceegenskaber</span><span class="sxs-lookup"><span data-stu-id="d0456-139">Define resource capabilities</span></span>
1. <span data-ttu-id="d0456-140">Udvid sektionen Egenskaber.</span><span class="sxs-lookup"><span data-stu-id="d0456-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="d0456-141">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d0456-141">Click Add.</span></span>
    * <span data-ttu-id="d0456-142">En funktion er en operationsressource evne til at udføre en bestemt aktivitet.</span><span class="sxs-lookup"><span data-stu-id="d0456-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="d0456-143">Planlægningsprogrammet allokerer ressourcer ved at sammenligne ressourcekravene for hver enkelt aktivitet med funktionerne i de tilgængelige operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="d0456-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="d0456-144">Indtast eller vælg en værdi i feltet Egenskab.</span><span class="sxs-lookup"><span data-stu-id="d0456-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="d0456-145">Angiv et tal i feltet Niveau.</span><span class="sxs-lookup"><span data-stu-id="d0456-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="d0456-146">Angiv det færdighedsniveau, som ressourcen behandler egenskaben med.</span><span class="sxs-lookup"><span data-stu-id="d0456-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="d0456-147">Angiv et tal i feltet Prioritet.</span><span class="sxs-lookup"><span data-stu-id="d0456-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="d0456-148">Angiv prioriteten af operationsressourcen med hensyn til egenskaben.</span><span class="sxs-lookup"><span data-stu-id="d0456-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="d0456-149">Når der planlægges efter prioritet, vælges operationsressourcen med den højeste prioritet (laveste numeriske værdi) først.</span><span class="sxs-lookup"><span data-stu-id="d0456-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="d0456-150">Tildele ressource til ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="d0456-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="d0456-151">Udvid sektionen Ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="d0456-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="d0456-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d0456-152">Click Add.</span></span>
    * <span data-ttu-id="d0456-153">Ressourcegruppen definerer rammerne for stedet, produktionsenheden og lagerstedet for operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="d0456-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="d0456-154">Operationsressourcen kan kun planlægges, når den tildeles til en ressourcegruppe og kun på det sted, hvor ressourcegruppen er placeret.</span><span class="sxs-lookup"><span data-stu-id="d0456-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="d0456-155">Indtast eller vælg en værdi i feltet Ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="d0456-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="d0456-156">Indtast eller vælg en værdi i feltet Indlagringslokalitet.</span><span class="sxs-lookup"><span data-stu-id="d0456-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="d0456-157">Angive lagerstedslokationen, som operationsressourcen forbruger materialer fra.</span><span class="sxs-lookup"><span data-stu-id="d0456-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

