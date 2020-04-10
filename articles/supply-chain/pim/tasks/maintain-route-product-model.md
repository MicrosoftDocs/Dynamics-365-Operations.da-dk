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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cc8b8137fb043dab3910ebea92e0a4152c80c97
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149912"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="c911f-103">Vedligehold rute for en produktmodel</span><span class="sxs-lookup"><span data-stu-id="c911f-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c911f-104">Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c911f-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="c911f-105">Denne procedure bruger modellen Højttaler af topkvalitet i demofirmaet USMF til at føre dig gennem processen.</span><span class="sxs-lookup"><span data-stu-id="c911f-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="c911f-106">Tilføj en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="c911f-106">Add a route operation</span></span>
1. <span data-ttu-id="c911f-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="c911f-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c911f-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="c911f-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="c911f-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c911f-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c911f-110">Vælg modellen Højttaler af topkvalitet til denne øvelse.</span><span class="sxs-lookup"><span data-stu-id="c911f-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="c911f-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c911f-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c911f-112">Udvid sektionen Ruteoperationer.</span><span class="sxs-lookup"><span data-stu-id="c911f-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="c911f-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c911f-113">Click Add.</span></span>
7. <span data-ttu-id="c911f-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c911f-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c911f-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c911f-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="c911f-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c911f-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="c911f-117">Angiv oplysninger om ruteoperation</span><span class="sxs-lookup"><span data-stu-id="c911f-117">Enter route operation details</span></span>
1. <span data-ttu-id="c911f-118">Klik på Oplysninger om ruteoperation.</span><span class="sxs-lookup"><span data-stu-id="c911f-118">Click Route operation details.</span></span>
2. <span data-ttu-id="c911f-119">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="c911f-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="c911f-120">I feltet Ope.</span><span class="sxs-lookup"><span data-stu-id="c911f-120">In the Oper.</span></span> <span data-ttu-id="c911f-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="c911f-121">No.</span></span> <span data-ttu-id="c911f-122">skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="c911f-122">field, enter a number.</span></span>
    * <span data-ttu-id="c911f-123">Operationsnumre bestemmer ruteforløbet.</span><span class="sxs-lookup"><span data-stu-id="c911f-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="c911f-124">Hver egenskab for en ruteoperation kan få en statisk værdi eller kan knyttes til en attribut.</span><span class="sxs-lookup"><span data-stu-id="c911f-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="c911f-125">Tilknytning til en attribut medfører, at værdien angives som en del af konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c911f-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="c911f-126">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="c911f-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="c911f-127">Rutegruppen afgør den væsentlige funktionsmåde i forbindelse med efterkalkulation, forbrug og installation.</span><span class="sxs-lookup"><span data-stu-id="c911f-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="c911f-128">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="c911f-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="c911f-129">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="c911f-129">Click the Times tab.</span></span>
7. <span data-ttu-id="c911f-130">I feltet Procesantal skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="c911f-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="c911f-131">Bestem, hvor mange der vil blive behandlet under én handling.</span><span class="sxs-lookup"><span data-stu-id="c911f-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="c911f-132">Angiv et tal i feltet Timer/tid.</span><span class="sxs-lookup"><span data-stu-id="c911f-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="c911f-133">Indtast tidsforholdet.</span><span class="sxs-lookup"><span data-stu-id="c911f-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="c911f-134">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="c911f-134">Select the Set check box.</span></span>
10. <span data-ttu-id="c911f-135">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="c911f-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="c911f-136">Bestemme behandlingstiden for den mængde, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="c911f-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="c911f-137">Klik på fanen Ressourcebehov.</span><span class="sxs-lookup"><span data-stu-id="c911f-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="c911f-138">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c911f-138">Click Add.</span></span>
13. <span data-ttu-id="c911f-139">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c911f-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c911f-140">Vælg en indstilling i feltet Kravtype.</span><span class="sxs-lookup"><span data-stu-id="c911f-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="c911f-141">Beslut, om du vil angive bestemte ressourcer eller egenskaber, som de skal have.</span><span class="sxs-lookup"><span data-stu-id="c911f-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="c911f-142">Indtast eller vælg en værdi i feltet Krav.</span><span class="sxs-lookup"><span data-stu-id="c911f-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="c911f-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c911f-143">Click OK.</span></span>

