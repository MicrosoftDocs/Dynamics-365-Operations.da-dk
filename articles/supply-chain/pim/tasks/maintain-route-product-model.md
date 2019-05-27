---
title: Vedligehold rute for en produktmodel
description: Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567693"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="17271-103">Vedligehold rute for en produktmodel</span><span class="sxs-lookup"><span data-stu-id="17271-103">Maintain route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17271-104">Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="17271-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="17271-105">Denne procedure bruger modellen Højttaler af topkvalitet i demofirmaet USMF til at føre dig gennem processen.</span><span class="sxs-lookup"><span data-stu-id="17271-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="17271-106">Tilføj en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="17271-106">Add a route operation</span></span>
1. <span data-ttu-id="17271-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="17271-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="17271-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="17271-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="17271-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="17271-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="17271-110">Vælg modellen Højttaler af topkvalitet til denne øvelse.</span><span class="sxs-lookup"><span data-stu-id="17271-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="17271-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="17271-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="17271-112">Udvid sektionen Ruteoperationer.</span><span class="sxs-lookup"><span data-stu-id="17271-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="17271-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="17271-113">Click Add.</span></span>
7. <span data-ttu-id="17271-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="17271-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="17271-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="17271-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="17271-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="17271-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="17271-117">Angiv oplysninger om ruteoperation</span><span class="sxs-lookup"><span data-stu-id="17271-117">Enter route operation details</span></span>
1. <span data-ttu-id="17271-118">Klik på Oplysninger om ruteoperation.</span><span class="sxs-lookup"><span data-stu-id="17271-118">Click Route operation details.</span></span>
2. <span data-ttu-id="17271-119">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="17271-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="17271-120">I feltet Ope.</span><span class="sxs-lookup"><span data-stu-id="17271-120">In the Oper.</span></span> <span data-ttu-id="17271-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="17271-121">No.</span></span> <span data-ttu-id="17271-122">skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="17271-122">field, enter a number.</span></span>
    * <span data-ttu-id="17271-123">Operationsnumre bestemmer ruteforløbet.</span><span class="sxs-lookup"><span data-stu-id="17271-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="17271-124">Hver egenskab for en ruteoperation kan få en statisk værdi eller kan knyttes til en attribut.</span><span class="sxs-lookup"><span data-stu-id="17271-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="17271-125">Tilknytning til en attribut medfører, at værdien angives som en del af konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="17271-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="17271-126">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="17271-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="17271-127">Rutegruppen afgør den væsentlige funktionsmåde i forbindelse med efterkalkulation, forbrug og installation.</span><span class="sxs-lookup"><span data-stu-id="17271-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="17271-128">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="17271-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="17271-129">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="17271-129">Click the Times tab.</span></span>
7. <span data-ttu-id="17271-130">I feltet Procesantal skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="17271-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="17271-131">Bestem, hvor mange der vil blive behandlet under én handling.</span><span class="sxs-lookup"><span data-stu-id="17271-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="17271-132">Angiv et tal i feltet Timer/tid.</span><span class="sxs-lookup"><span data-stu-id="17271-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="17271-133">Indtast tidsforholdet.</span><span class="sxs-lookup"><span data-stu-id="17271-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="17271-134">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="17271-134">Select the Set check box.</span></span>
10. <span data-ttu-id="17271-135">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="17271-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="17271-136">Bestemme behandlingstiden for den mængde, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="17271-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="17271-137">Klik på fanen Ressourcebehov.</span><span class="sxs-lookup"><span data-stu-id="17271-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="17271-138">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="17271-138">Click Add.</span></span>
13. <span data-ttu-id="17271-139">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="17271-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="17271-140">Vælg en indstilling i feltet Kravtype.</span><span class="sxs-lookup"><span data-stu-id="17271-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="17271-141">Beslut, om du vil angive bestemte ressourcer eller egenskaber, som de skal have.</span><span class="sxs-lookup"><span data-stu-id="17271-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="17271-142">Indtast eller vælg en værdi i feltet Krav.</span><span class="sxs-lookup"><span data-stu-id="17271-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="17271-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="17271-143">Click OK.</span></span>

