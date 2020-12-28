---
title: Vedligehold rute for en produktmodel
description: Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc41f99085e5f30ae29edce296a5e3752cbabd33
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424485"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="ab2f7-103">Vedligehold rute for en produktmodel</span><span class="sxs-lookup"><span data-stu-id="ab2f7-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab2f7-104">Kørsel af denne procedure kræver, at der findes en model til produktkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="ab2f7-105">Denne procedure bruger modellen Højttaler af topkvalitet i demofirmaet USMF til at føre dig gennem processen.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="ab2f7-106">Tilføj en ruteoperation</span><span class="sxs-lookup"><span data-stu-id="ab2f7-106">Add a route operation</span></span>
1. <span data-ttu-id="ab2f7-107">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ab2f7-108">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ab2f7-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ab2f7-110">Vælg modellen Højttaler af topkvalitet til denne øvelse.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="ab2f7-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ab2f7-112">Udvid sektionen Ruteoperationer.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="ab2f7-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-113">Click Add.</span></span>
7. <span data-ttu-id="ab2f7-114">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ab2f7-115">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ab2f7-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="ab2f7-117">Angiv oplysninger om ruteoperation</span><span class="sxs-lookup"><span data-stu-id="ab2f7-117">Enter route operation details</span></span>
1. <span data-ttu-id="ab2f7-118">Klik på Oplysninger om ruteoperation.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-118">Click Route operation details.</span></span>
2. <span data-ttu-id="ab2f7-119">Indtast eller vælg en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="ab2f7-120">I feltet Ope.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-120">In the Oper.</span></span> <span data-ttu-id="ab2f7-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-121">No.</span></span> <span data-ttu-id="ab2f7-122">skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-122">field, enter a number.</span></span>
    * <span data-ttu-id="ab2f7-123">Operationsnumre bestemmer ruteforløbet.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="ab2f7-124">Hver egenskab for en ruteoperation kan få en statisk værdi eller kan knyttes til en attribut.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="ab2f7-125">Tilknytning til en attribut medfører, at værdien angives som en del af konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="ab2f7-126">Indtast eller vælg en værdi i feltet Rutegruppe.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ab2f7-127">Rutegruppen afgør den væsentlige funktionsmåde i forbindelse med efterkalkulation, forbrug og installation.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="ab2f7-128">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="ab2f7-129">Klik på fanen Tider.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-129">Click the Times tab.</span></span>
7. <span data-ttu-id="ab2f7-130">I feltet Procesantal skal du angive et tal.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="ab2f7-131">Bestem, hvor mange der vil blive behandlet under én handling.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="ab2f7-132">Angiv et tal i feltet Timer/tid.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="ab2f7-133">Indtast tidsforholdet.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="ab2f7-134">Marker afkrydsningsfeltet Indstil.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-134">Select the Set check box.</span></span>
10. <span data-ttu-id="ab2f7-135">Angiv et tal i feltet Procestid.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ab2f7-136">Bestemme behandlingstiden for den mængde, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="ab2f7-137">Klik på fanen Ressourcebehov.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="ab2f7-138">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-138">Click Add.</span></span>
13. <span data-ttu-id="ab2f7-139">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ab2f7-140">Vælg en indstilling i feltet Kravtype.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="ab2f7-141">Beslut, om du vil angive bestemte ressourcer eller egenskaber, som de skal have.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="ab2f7-142">Indtast eller vælg en værdi i feltet Krav.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="ab2f7-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-143">Click OK.</span></span>

